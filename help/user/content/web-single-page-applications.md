---
title: Applicazioni a pagina singola
description: 'Creazione di esperienze web per applicazioni a pagina singola: configurazione del tracciamento delle visualizzazioni, gestione dei contenuti dinamici e gestione della navigazione lato client in Journey Optimizer B2B edition.'
feature: Channels, Personalization
role: User
badgeBeta: label="Beta" type="informative" tooltip="Questa funzione è attualmente in versione beta limitata"
source-git-commit: e50b6830736bf763d3aae6a58595e868bbac36e0
workflow-type: tm+mt
source-wordcount: '835'
ht-degree: 0%

---

# Applicazioni a pagina singola

Le applicazioni a pagina singola presentano problematiche specifiche per la personalizzazione web, in quanto aggiornano dinamicamente il contenuto della pagina senza ricaricamenti dell’intera pagina. Journey Optimizer B2B edition fornisce strumenti specializzati per gestire in modo efficace la personalizzazione delle applicazioni a pagina singola.

## Informazioni sulle applicazioni a pagina singola

A differenza dei siti web tradizionali a più pagine in cui ogni navigazione attiva un caricamento di pagina completo, le applicazioni a pagina singola utilizzano JavaScript per aggiornare i contenuti in modo dinamico mantenendo una singola pagina HTML. Questo approccio crea diverse considerazioni per le esperienze web:

* **Nessuna pagina ricaricata** - Le modifiche al contenuto si verificano senza attivare gli eventi di caricamento pagina tradizionali.
* **Visualizzazioni virtuali** - Diverse _visualizzazioni_ o _schermate_ all&#39;interno dell&#39;applicazione a pagina singola che devono essere tracciate come pagine separate.
* **Routing lato client** - I router JavaScript (come React Router, Vue Router e Angular Router) gestiscono le richieste di navigazione anziché quelle dei server.
* **DOM dinamico** - È possibile creare, modificare o rimuovere elementi di pagina dopo il caricamento della pagina iniziale.

## Configurare il supporto per applicazioni a pagina singola

Per personalizzare le applicazioni a pagina singola in modo efficace, devi configurare il tracciamento delle visualizzazioni in modo che Journey Optimizer B2B edition possa identificare quando gli utenti passano da una visualizzazione virtuale all’altra.

### Impostare le dichiarazioni di visualizzazione

Collabora con il tuo team di sviluppo per implementare le dichiarazioni di visualizzazione utilizzando Adobe Web SDK. L&#39;utilizzo di queste dichiarazioni di visualizzazione comporta la chiamata del comando `sendEvent` con le informazioni di visualizzazione ogni volta che l&#39;applicazione a pagina singola passa a una nuova visualizzazione.

**Implementazione di esempio:**

```javascript
// When a new view is rendered in your SPA
alloy("sendEvent", {
  "xdm": {
    "web": {
      "webPageDetails": {
        "viewName": "product-detail",
        "URL": window.location.href
      }
    }
  },
  "data": {
    "__adobe": {
      "target": {
        "viewName": "product-detail"
      }
    }
  }
});
```

### Visualizza convenzioni di denominazione

Utilizzare nomi di visualizzazione coerenti e descrittivi corrispondenti alla struttura logica dell&#39;applicazione:

| Visualizzazione | Nome esempio |
| ---- | ------------ |
| Pagina Home | `home` |
| Elenco prodotti | `product-list` |
| Dettagli prodotto | `product-detail` |
| Carrello | `cart` |
| Pagamento | `checkout` |
| Dashboard account | `account-dashboard` |

>[!NOTE]
>
>I nomi delle visualizzazioni fanno distinzione tra maiuscole e minuscole. Utilizza una convenzione di denominazione coerente (si consiglia di usare lettere minuscole e trattini) nell’implementazione.

## Creare esperienze web per applicazioni a pagina singola

Quando crei esperienze web per applicazioni a pagina singola, prendi in considerazione le seguenti best practice:

### Visualizzazioni specifiche di Target

* Nella [configurazione del canale web](../admin/configure-channels-web.md), imposta le regole di corrispondenza URL che sono in linea con la struttura di indirizzamento dell&#39;applicazione a pagina singola.

* Quando crei modifiche, specifica la vista a cui applicare la modifica.

* Utilizza i selettori CSS che eseguono il targeting di elementi specifici per ogni visualizzazione.

### Gestire i contenuti dinamici

Le applicazioni a pagina singola spesso caricano il contenuto in modo dinamico dopo il rendering della pagina iniziale. Utilizza queste tecniche per garantire la corretta applicazione delle modifiche:

#### Attendi elementi

Configura le modifiche per attendere che esistano gli elementi target prima di applicare:

1. Nell’editor non visivo, aggiungi una modifica con un selettore CSS.

1. Abilita **[!UICONTROL Attendi l&#39;elemento]** e specifica il tempo di attesa massimo.

1. La modifica viene applicata una volta che l’elemento target viene visualizzato nel DOM.

#### Utilizzare osservatori delle mutazioni

Per i contenuti altamente dinamici, il Web SDK include osservatori delle mutazioni incorporati che rilevano quando vengono aggiunti nuovi elementi alla pagina. Questi osservatori garantiscono che le modifiche vengano applicate anche quando gli elementi vengono caricati in modo asincrono.

### Framework SPA

Le esperienze web di Journey Optimizer B2B edition funzionano con i framework SPA più diffusi:

| Framework | Considerazioni |
| --------- | -------------- |
| **React** | Le modifiche vengono applicate dopo che React esegue il rendering dei componenti nel DOM. Utilizza nomi di classi o attributi di dati per il targeting. |
| **Angular** | Elementi di destinazione dopo l’esecuzione del rilevamento delle modifiche di Angular. Evitare di eseguire il rendering degli elementi di targeting con `*ngIf`. |
| **Vue.js** | Attendi che `nextTick` del volume verifichi che gli elementi siano nel DOM. Utilizza riferimenti o attributi personalizzati per il targeting stabile. |
| **Avanti.js / Nuxt.js** | Per le pagine SSR/SSG, assicurati che l’idratazione di Web SDK sia completata prima di attendere modifiche. |

## Best practice per la personalizzazione con applicazioni a pagina singola

### Utilizzare selettori stabili

Le applicazioni a pagina singola generano spesso nomi o ID di classi dinamici (in particolare con le soluzioni CSS-in-JS). In alternativa, puoi utilizzare:

* **Attributi dati** - Aggiungere attributi dati personalizzati (`data-testid`, `data-section`, ecc.) agli elementi di destinazione.
* **HTML semantico** - Target basato su struttura HTML ed elementi semantici.
* **Attributi ID** - Se possibile, utilizza attributi ID stabili.

**Esempio:**

```html
<!-- Instead of targeting dynamic class names -->
<button class="css-1a2b3c4d">Sign Up</button>

<!-- Add a stable data attribute -->
<button class="css-1a2b3c4d" data-action="signup">Sign Up</button>
```

**Selettore CSS:** `[data-action="signup"]`

### Visualizzazioni di prova

Durante il test delle esperienze web SPA:

1. Naviga tra tutte le viste a cui si applicano le modifiche.

1. Verificare l&#39;intero flusso dell&#39;utente, compresi:
   * Navigazione diretta a una visualizzazione (collegamenti profondi)
   * Navigazione da altre viste nell’applicazione a pagina singola
   * Navigazione avanti e indietro del browser

1. Verifica che le modifiche vengano applicate nuovamente quando si torna a una visualizzazione visitata in precedenza.

### Gestire le transizioni di visualizzazione

Alcune applicazioni a pagina singola utilizzano animazioni o transizioni tra viste. Considera:

* **Intervallo** - Assicurati che le modifiche vengano applicate dopo il completamento delle animazioni di transizione.
* **Visibilità elemento** - Gli elementi possono esistere ma essere nascosti durante le transizioni.
* **Sfarfallio** - Applica le modifiche in tempo utile per evitare modifiche visibili al contenuto.

## Risoluzione dei problemi

Durante l’esame delle modifiche alla progettazione dell’applicazione a pagina singola, utilizza le seguenti raccomandazioni per risolvere alcuni problemi comuni:

* **Modifiche non visualizzate** - Se le modifiche non sono visualizzate nell&#39;applicazione a pagina singola:

   1. **Verifica il rilevamento della visualizzazione**. Verificare che `sendEvent` chiamate includano il nome della visualizzazione corretto.

   1. **Verifica esistenza elemento** - Assicurati che gli elementi di destinazione siano nel DOM quando vengono applicate le modifiche.

   1. **Rivedi selettori** - Conferma che i selettori CSS corrispondano alla struttura DOM effettiva.

   1. **Controlla la console** - Cerca errori JavaScript che potrebbero impedire le modifiche.

* **Modifiche che compaiono brevemente e poi scompaiono** - Questo problema si verifica in genere quando l&#39;applicazione a pagina singola esegue nuovamente il rendering e sostituisce gli elementi modificati:

   1. Utilizza selettori CSS più specifici che rimangono stabili tra i diversi rendering.

   1. Consenti agli osservatori delle mutazioni di applicare nuovamente le modifiche quando gli elementi vengono ricreati.

   1. Collabora con il tuo team di sviluppo per aggiungere attributi stabili agli elementi target.

* **Modifiche duplicate** - Se le modifiche vengono visualizzate più volte:

   1. Verifica che gli eventi di tracciamento della visualizzazione vengano attivati una sola volta per ogni transizione di visualizzazione.

   1. Verifica che le modifiche abbiano un ambito di visualizzazione specifico anziché essere applicate a livello globale.

## Argomenti correlati

* [Panoramica sulle esperienze web](./web-experiences.md)
* [Progettazione esperienza web](./web-experience-design.md)
* [Configurazioni del canale web](../admin/configure-channels-web.md)