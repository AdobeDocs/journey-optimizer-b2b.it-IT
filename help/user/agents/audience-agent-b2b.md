---
title: Abilità del pubblico per account e persone B2B
description: Scopri le competenze relative al pubblico per gli account e le persone B2B. Esplora le finalità del prodotto, identifica gli utenti tipo, valuta la copertura dei ruoli e crea modelli di gruppi di acquisto.
feature: Agentic AI, Audiences
role: User
exl-id: c1210912-66ba-4b5f-8f3b-96eb6280c926
autotag-review: '2026-06-05T16:43:42.459Z'
TQID: 'https://experienceleague.adobe.com/d7KMYbH0NpoYGnBdTCmCpzLgpGIYfNP-YIFCQUjZpIg'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
    internal-label: Journey Optimizer B2B Edition
feature_v2:
  - id: afadf741-c5fe-42cd-8013-23bb6ff2d1bc
    internal-label: Buying Groups
  - id: beb5f4be-cec3-471a-9db6-831a77dd3ac9
    internal-label: Audiences
  - id: bef5003b-cad2-4f40-bdb2-a80426d52ef5
    internal-label: AI Assistant
subfeature_v2:
  - id: ff10f619-348f-47e3-99bf-3ce4c817cf2c
    internal-label: Agentic AI
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
    internal-label: Metadata
  - id: bbbea26f-9621-49eb-9ab8-e06fb3bbce8c
    internal-label: Artificial intelligence
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
  - id: f8667931-f646-4dd3-af2a-b9d0cb8098ad
    internal-label: Taxonomy
source-git-commit: ce5504e7a539c38b489fddc103358029edf1cfba
workflow-type: tm+mt
source-wordcount: '1692'
ht-degree: 1%
---
# Competenze del pubblico per account e persone B2B

Utilizza le abilità del pubblico per B2B nell&#39;interfaccia [!DNL CX Coworker]. Esplora le finalità del prodotto tra account e persone. Identifica gli utenti tipo pertinenti, valuta la copertura del gruppo di acquisto e crea modelli di ruolo per il gruppo di acquisto.

* Valuta l’interesse del conto in prodotti specifici e confronta le tendenze di intento.
* Identifica persone e utenti tipo associati al prodotto interessato.
* Rivedi i ruoli del gruppo di acquisto e identifica le lacune di copertura.
* Genera e perfeziona modelli di ruolo per gruppi di acquisto.

>[!PREREQUISITES]
>
>Prima di utilizzare le abilità di pubblico per account e persone B2B, configura le seguenti definizioni e mappature di dati:
>
>* [Tassonomia e mappatura dei dati intento](../admin/intent-data.md)
>* [Mappatura campo XDM](#xdm-data-prerequisites)

Fai clic sull&#39;icona _Chiedi a[!DNL Coworker]_ ( ![Chiedi a [!DNL Coworker]](../assets/do-not-localize/icon-ask-coworker.svg) ) nella parte superiore dell&#39;applicazione per aprire l&#39;applicazione [!DNL Coworker]. Inserisci il prompt della lingua naturale nell’interfaccia della chat.

![Prompt del pubblico in [!DNL CX Coworker]](./assets/audience-skills-prompt.png){width="800" zoomable="yes"}

## Aree principali di specializzazione del pubblico

Utilizza le aree di interesse per le competenze del pubblico per esplorare le finalità dell’account, comprendere persone e utenti tipo e preparare modelli di gruppi di acquisto.

| Focus | Attività |
| ----- | ----- |
| Intento account | Valutare l&#39;intento dell&#39;account per prodotti specifici utilizzando livelli di intento bassi, medi e alti. Confronta le tendenze di interesse dei prodotti nel tempo e identifica i conti che mostrano interesse per prodotti specifici. Rivedi i pattern di coinvolgimento e la copertura dell’utente tipo. |
| Persone e utenti tipo | Identifica e classifica gli utenti tipo in base all’intento del prodotto per uno o più prodotti. Rivedi le metriche dell’opportunità, tra cui il tasso di vincita, il tasso di iscrizione e i conteggi. Mappa gli utenti tipo a ruoli quali _Champion_, _Decision Maker_ e _Influencer_ e rivedi le spiegazioni per le assegnazioni di ruolo. |
| Copertura gruppo di acquisto | Valuta le dimensioni del gruppo di acquisto e la copertura dell’utente tipo tra gli account. Rivedi la distribuzione dei ruoli e identifica gli utenti tipo o i ruoli mancanti. Trova account con campioni identificati in recenti offerte. |
| Acquisto di modelli di gruppo | Genera modelli di ruolo per gruppi di acquisto per prodotti specifici ed esamina le mappature utente consigliate. Affina i modelli includendo o escludendo utenti tipo e ruoli. Convalida i ruoli richiesti prima di creare gruppi di acquisto. |

## Limitazioni

Gli approfondimenti sul pubblico dipendono dalla tassonomia di intento configurata, dalle mappature dei campi XDM e dai dati dell’evento esperienza. Dati di opportunità incompleti, tassonomia mancante o obsoleta oppure identificatori di profilo e account mancanti possono ridurre l’affidabilità di insight.

Il calcolo dell&#39;intento utilizza solo questi eventi esperienza: `directMarketing.emailClicked`, `directMarketing.emailOpened`, `directMarketing.emailUnsubscribed` e `web.webpagedetails.pageViews`.

## Esempi di prompt

Immettere i seguenti prompt nell&#39;interfaccia [!DNL CX Coworker] per esplorare le finalità dell&#39;account, comprendere persone e utenti tipo e preparare modelli di gruppi di acquisto.

### Intento account

Esplora l’interesse dell’account per i prodotti ed esamina le modifiche nell’intento.

* Mostra la finestra di tendenza: aggiornamenti più recenti e meno recenti per l’intento di prodotto dell’account per prodotto.
* Quali account hanno un intento basso per qualsiasi prodotto ma hanno ancora opportunità aperte (vale la pena nutrirsi)?
* Quali nuovi segnali di intento sono stati registrati per `<account_name>` questa settimana?

### Persone e utenti tipo

Identifica gli utenti tipo associati all’interesse per il prodotto e rivedi i ruoli dei gruppi di acquisto consigliati.

* Mostra gli utenti tipo associati a `<product>`.
* Mostra il ruolo per il consiglio di mappatura persona per `<product>`.
* Per `<product>`, elenca gli utenti tipo e i ruoli con le relative metriche opportunità (tasso di vincita, tasso di iscrizione, conteggi).

### Acquisto di gruppi e modelli

Rivedi l’intento del gruppo di acquisto e la copertura, quindi genera o perfeziona i modelli.

* Per `<product>`, elenca i gruppi di acquisto con finalità di prodotto e punteggi.
* Per gli account in `<industry>`, qual è la copertura media degli utenti tipo per l&#39;account per `<product>`?
* Creare un modello di gruppo di acquisto per `<product>`.
* Creare un modello di gruppo di acquisto per `<product>` senza l&#39;utente tipo `<persona>` e rimuovere il ruolo `<role>`.

## Concetti

Utilizza questi concetti per interpretare le finalità dell’account, le classificazioni utente e i consigli del gruppo di acquisto.

| Concetto | Spiegazione |
| ------- | ----------- |
| Rilevamento del pubblico | Analizza i segnali di coinvolgimento di prime parti tra le persone in un account per identificare gli interessi del prodotto e gli utenti tipo rilevanti. L’analisi considera i 18 mesi precedenti di attività, inclusa l’attività prima della chiusura dell’opportunità. I modelli di coinvolgimento possono indicare l’intento del prodotto quando i dati dell’opportunità sono incompleti, ma la mancanza di dati può ridurre l’affidabilità di insight. |
| Utente tipo | Le persone vengono raggruppate in base alla qualifica professionale, alla funzione e all&#39;anzianità normalizzate. Utilizza gli utenti tipo per capire chi è coinvolto all’interno di un account, inclusi i responsabili decisionali, gli influencer e i ruoli di supporto. |
| Mappatura dei ruoli del gruppo di acquisto | Associa gli utenti tipo a ruoli di gruppo di acquisto specifici per il prodotto in base a qualifica, funzione, anzianità e attributi configurati. Questi ruoli rappresentano le persone all’interno di un account che influenzano o decidono un acquisto. Rivedi la copertura per identificare i ruoli mancanti. |
| Dati dell’opportunità per la classificazione tipo | La fase di opportunità, la data di chiusura e le mappature opportunità-prodotto supportano la classificazione personale per ogni prodotto. Quando i dati dell’opportunità sono incompleti, la classificazione utilizza il volume dell’attività e il decadimento temporale per dare più peso all’attività recente.<br/><br/>Il collegamento del prodotto utilizza una tabella di mappatura opportunità-prodotto fornita o generata, se disponibile. In caso contrario, la corrispondenza approssimativa collega le opportunità ai prodotti. Se non è disponibile alcun collegamento, l’intento del prodotto viene dedotto dall’attività recente prima della data di chiusura dell’opportunità. Questi metodi di fallback non eliminano i limiti di affidabilità dei dati incompleti. |
| Analisi dell’opportunità | L’analisi storica delle opportunità utilizza tre dimensioni per identificare i modelli utente associati ai risultati di acquisto:<ul><li>Percentuale di vittorie: misura la frequenza con cui si vincono le opportunità quando sono coinvolti determinati utenti tipo. I modelli di persona associati a tassi di vincita più alti ricevono più peso.</li><li>Tasso di iscrizione: misura la frequenza con cui un utente tipo viene visualizzato nelle opportunità per un determinato prodotto.</li><li>Influenza personale: misura il modo in cui il coinvolgimento o l’attività dell’utente tipo sono correlati alle vincite, oltre a determinare se l’utente tipo è presente o meno.</li></ul>Questi segnali informano le finalità dell’account, la mappatura dell’utente tipo e i consigli del gruppo di acquisto. |
| Intento | L’intento indica l’interesse del prodotto attraverso il coinvolgimento, ad esempio visite a pagine web o clic sui collegamenti e-mail. La tassonomia dei prodotti collega l’attività di coinvolgimento a parole chiave, prodotti e categorie di prodotti. La profondità e la frequenza del coinvolgimento determinano singoli punteggi di intento per ogni parola chiave, prodotto o categoria di prodotto.<br/><br/>I punteggi indicano la forza dell&#39;interesse: Intento basso: `<=0.2`, Intento Medium: `0.2 < score <= 0.6`, Intento alto: `0.6 < score <= 1`.<br/><br/>I punteggi di Intento individuale vengono aggregati tra le persone nello stesso account per determinare l&#39;intento dell&#39;account. |
| Ruoli che influenzano un gruppo di acquisto | I ruoli del gruppo di acquisto rappresentano contributi diversi a una decisione di acquisto. _I responsabili delle decisioni_ controllano in genere le approvazioni del budget. _Influencer_ valutazione forma e consigli. _Champions_ genera consenso interno. _Utenti finali_ convalidano l&#39;adattamento del prodotto.<br/><br/>Rivedi le assegnazioni dei ruoli e la copertura per capire chi influenza la decisione e dove permangono le lacune del coinvolgimento. |
| Copertura di persone o ruoli | La copertura misura quanti utenti tipo o ruoli previsti dispongono di almeno un rappresentante all’interno di un account. Per un prodotto con _N_ utenti tipo o ruoli previsti, la copertura completa indica che sono rappresentati tutti i _N_. La copertura parziale ne fa mancare una parte. Utilizza la copertura per valutare la completezza del gruppo di acquisto e individuare le lacune. |

## Prerequisiti per i dati XDM

Configura le seguenti mappature di campi XDM per supportare l’analisi dell’intento dell’account, l’identificazione dell’utente tipo e la mappatura dei ruoli del gruppo di acquisto.

### Mappatura campo XDM

<table>
  <tbody>
    <tr>
      <th>Campo XDM</th>
      <th>Entità</th>
      <th>Definizione di business</th>
      <th>Dettagli aggiuntivi</th>
    </tr>
    <tr>
      <td>
        <p>
          <span>b2b.accountKey.sourceKey</span>
        </p>
      </td>
      <td>
        <p>
          <span>Profili</span>
        </p>
      </td>
      <td>Identificatore account, utilizzato nei join dei dati relativi a opportunità, evento e intento</td>
      <td rowspan="2">Analisi opportunità<br/>Esplorazione account<br/>
        <br/>
      </td>
    </tr>
    <tr>
      <td>
        <p>
          <span>b2b.personKey.sourceKey</span>
        </p>
      </td>
      <td>
        <p>
          <span>Profili</span>
        </p>
      </td>
      <td>Identificatore della persona, utilizzato nei join che coinvolgono i dati evento ai dati profilo</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>extendedWorkDetails.departments</span>
        </p>
      </td>
      <td>
        <p>
          <span> profili</span>
        </p>
      </td>
      <td>Reparto del profilo/persona</td>
      <td rowspan="5">
        <p>
          <br/>
        </p>
        <p>Mappatura personale</p>
      </td>
    </tr>
    <tr class="">
      <td>
        <p>
          <span>extendedWorkDetails.jobTitle</span>
        </p>
      </td>
      <td>
        <p>
          <span> profili</span>
        </p>
      </td>
      <td>Qualifica del profilo/persona utilizzato nel calcolo dell’utente tipo</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>nome.nome.nomeNome</span>
        </p>
      </td>
      <td>
        <p>
          <span >Profili</span>
        </p>
      </td>
      <td>Visualizza il nome della persona nei risultati corrispondenti alla query.</td>
    </tr>
    <tr class="">
      <td>
        <p>
          <span>nome.nome.nomeCompleto</span>
        </p>
      </td>
      <td>
        <p>
          <span> profili</span>
        </p>
      </td>
      <td>Visualizza il nome completo della persona nei risultati corrispondenti alla query.</td>
    </tr>
    <tr class="">
      <td>
        <p>
          <span>nome.cognome</span>
        </p>
      </td>
      <td>
        <p>
          <span> profili</span>
        </p>
      </td>
      <td>Visualizza il cognome della persona nei risultati corrispondenti alla query.</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>accountKey.sourceKey</span>
        </p>
      </td>
      <td>
        <p>
          <span> account</span>
        </p>
      </td>
      <td>Identificatore account, utilizzato nei join dei dati relativi a opportunità, evento e intento</td>
      <td>Analisi opportunità<br/>Esplorazione account</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>nomeAccount</span>
        </p>
      </td>
      <td>
        <p>
          <span>Account</span>
        </p>
      </td>
      <td>Visualizza il nome dell'account nei risultati corrispondenti alla query.</td>
      <td rowspan="4">
        <p>
          <br/>
        </p>
        <p>
          <br/>
        </p>
        <p>
          <br/>
        </p>
        <p>Esplorazione account</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>
          <span>accountDescription</span>
        </p>
      </td>
      <td>
        <p>
          <span>Account</span>
        </p>
      </td>
      <td>Supporta il filtraggio dell’account in base alla descrizione dell’account in base alla query.</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>accountOrganization.industry</span>
        </p>
      </td>
      <td>
        <p>
          <span> account</span>
        </p>
      </td>
      <td>Supporta il filtraggio degli account per settore in base alla query.</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>accountBillingAddress.region</span>
        </p>
      </td>
      <td>
        <p>
          <span> account</span>
        </p>
      </td>
      <td>Supporta il filtraggio dell’account per area dell’indirizzo di fatturazione in base alla query.</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>accountKey.sourceKey</span>
        </p>
      </td>
      <td>
        <p>
          <span>Opportunità</span>
        </p>
      </td>
      <td>Identificatore account, utilizzato nei join dei dati relativi a opportunità, evento e intento</td>
      <td rowspan="2">
        <p>Analisi opportunità<br/>Esplorazione account</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>
          <span>optionKey.sourceKey</span>
        </p>
      </td>
      <td>
        <p>
          <span>Opportunità</span>
        </p>
      </td>
      <td>Identificatore dell’opportunità, utilizzato nei join per i dati dell’account</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>NomeOpportunità</span>
        </p>
      </td>
      <td>
        <p>
          <span> opportunità</span>
        </p>
      </td>
      <td>Nome dell’opportunità utilizzato nell’analisi dell’opportunità.</td>
      <td rowspan="5">
        <p>
          <br/>
        </p>
        <p>
          <br/>
        </p>
        <p>
          <br/>
        </p>
        <p>
          <br/>
        </p>
        <p>
          <br/>
        </p>
        <p>Analisi dell’opportunità</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>
          <span>isWon</span>
        </p>
      </td>
      <td>
        <p>
          <span>Opportunità</span>
        </p>
      </td>
      <td>Se l’opportunità è vinta (binario)</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>descrizione opportunità</span>
        </p>
      </td>
      <td>
        <p>
          <span>Opportunità</span>
        </p>
      </td>
      <td>Descrizione dell’opportunità utilizzata nell’analisi dell’opportunità.</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>importo opportunità</span>
        </p>
      </td>
      <td>
        <p>
          <span>Opportunità</span>
        </p>
      </td>
      <td>Importo di $ coinvolto nell’opportunità</td>
    </tr>
    <tr class="">
      <td>
        <p>
          <span>tipoOpportunità</span>
        </p>
      </td>
      <td>
        <p>
          <span>Opportunità</span>
        </p>
      </td>
      <td>Tipo di opportunità</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>faseOpportunità</span>
        </p>
      </td>
      <td>
        <p>
          <span> opportunità</span>
        </p>
      </td>
      <td>Fase dell’opportunità (vinta chiusa o persa chiusa o qualsiasi fase intermedia) </td>
      <td rowspan="4">
        <p>Analisi opportunità<br/>Esplorazione account</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>
          <span>actualCloseDate</span>
        </p>
      </td>
      <td>
        <p>
          <span>Opportunità</span>
        </p>
      </td>
      <td>Data effettiva di chiusura dell’opportunità</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>expectedCloseDate</span>
        </p>
      </td>
      <td>
        <p>
          <span> opportunità</span>
        </p>
      </td>
      <td>Data di chiusura prevista dell’opportunità</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>extSourceSystemAudit.createdDate</span>
        </p>
      </td>
      <td>
        <p>
          <span>Opportunità</span>
        </p>
      </td>
      <td>Data di creazione per questa opportunità</td>
    </tr>
  </tbody>
</table>

### Dati di tassonomia

Le abilità del pubblico utilizzano dati di intento di prime parti da [!DNL Adobe Journey Optimizer B2B Edition]. Il calcolo dell’intento collega la tassonomia dei prodotti con l’attività di coinvolgimento e aggrega i singoli punteggi a livello di account.

1. Il calcolo dell&#39;intento richiede i dati della tassonomia (prodotti del cliente e parole chiave corrispondenti) da Clienti > Tassonomia
1. I dati di tassonomia vengono utilizzati per etichettare i dati evento (etichettatura delle risorse). Questi dati forniscono informazioni approfondite sulle parole chiave e i prodotti a cui i visitatori sono interessati in base ai loro dati evento > Etichettatura risorse 
1. Le risorse con etichetta (dati evento) vengono combinate con i comportamenti dei visitatori (numero di pagine visitate) per determinare l’intento di un visitatore a livello di parola chiave, prodotto e categoria di prodotto → calcolo dell’intento
1. I punteggi di intento a livello di profilo visitatore vengono aggregati a livello di account per determinare l’intento dell’account in una determinata parola chiave, prodotto e categoria di prodotto > Aggregazione account intento

I campi seguenti sono obbligatori oltre a [configurare la tassonomia intento](../admin/intent-data.md):

<table>
  <tbody>
    <tr>
      <th>Campo XDM</th>
      <th>Entità</th>
      <th>Definizione di business</th>
    </tr>
    <tr>
      <th>
        <br/>
      </th>
      <th>
        <br/>
      </th>
      <td>profilo della persona</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>_acp_system_metadata.primaryIdentity.namespace.code<br/>
          </span>
        </p>
      </td>
      <td>
        <p>
          <span>Profilo</span>
        </p>
      </td>
      <td>Consente di identificare un identificatore di persona (e-mail o b2b_person)</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>_acp_system_metadata.primaryIdentity.id
          </span>
        </p>
      </td>
      <td>
        <p>
          <span>Profilo</span>
        </p>
      </td>
      <td>namespace_id</td>
    </tr>
    <tr>
      <td>
        <ul>
          <li>keyword_id</li>
          <li>keyword_name</li>
          <li>product_id</li>
          <li>product_name</li>
          <li>product_category_id</li>
          <li>product_category_name</li>
        </ul>
      </td>
      <td>
        <p>
          <br/>
        </p>
      </td>
      <td>Utilizzato come tassonomia per etichettare le risorse (eventi di esperienza, come e-mail su cui è stato fatto clic, pagine web visitate)</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>timestamp</span>
        </p>
      </td>
      <td>
        <p>
          <span>Evento esperienza</span>
        </p>
      </td>
      <td>Utilizzato per il tempo necessario per ottenere la retrocompilazione e l’esecuzione incrementale</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>eventType</span>
        </p>
      </td>
      <td>
        <p>
          <span>Evento esperienza</span>
        </p>
      </td>
      <td>Identifica il tipo di evento. Il calcolo dell'intento utilizza solo <code>directMarketing.emailClicked</code>, <code>directMarketing.emailOpened</code>, <code>directMarketing.emailUnsubscribed</code> e <code>web.webpagedetails.pageViews</code>.
      </td>
    </tr>
    <tr>
      <td>
        <p>
          <span>directMarketing.mailingName</span>
        </p>
      </td>
      <td>
        <p>
          <span>Evento esperienza</span>
        </p>
      </td>
      <td>Solo per riferimento/contabilità; informazioni sul nome della campagna</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>directMarketing.mailingKey.sourceID</span>
        </p>
      </td>
      <td>
        <p>
          <span>Evento esperienza</span>
        </p>
      </td>
      <td>Solo per riferimento/contabilità; informazioni sull’ID sorgente per il quale è indirizzata l’e-mail</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>directMarketing.mailingKey.sourceInstanceID<br/>
          </span>
        </p>
      </td>
      <td>
        <p>
          <span>Evento esperienza</span>
        </p>
      </td>
      <td>Solo per riferimento/contabilità: informazioni sull’istanza di origine per la quale è destinata l’e-mail</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>directMarketing.mailingKey.sourceKey<br/>
          </span>
        </p>
      </td>
      <td>
        <p>
          <span>Evento esperienza</span>
        </p>
      </td>
      <td>Utilizzato per recuperare il contenuto delle e-mail dal data center [!DNL Adobe Marketo Engage]. Comprende (SourceID@SourceInstanceID.SourceType).</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>directMarketing.mailingKey.sourceType<br/>
          </span>
        </p>
      </td>
      <td>
        <p>
          <span>Evento esperienza</span>
        </p>
      </td>
      <td>Solo per riferimento/contabilità; informazioni sul tipo di sorgente o da dove ha avuto origine la sorgente </td>
    </tr>
    <tr>
      <td>
        <p>
          <span>web.webPageDetails<br/>
          </span>
        </p>
      </td>
      <td>
        <p>
          <span>Evento esperienza</span>
        </p>
      </td>
      <td>Informazioni sull’origine della visita della pagina web</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>web.webPageDetails.name<br/>
          </span>
        </p>
      </td>
      <td>
        <p>
          <span>Evento esperienza</span>
        </p>
      </td>
      <td>URL effettivo utilizzato per ottenere il contenuto</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>web.webPageDetails.queryParameters</span>
        </p>
      </td>
      <td>
        <p>
          <span>Evento esperienza</span>
        </p>
      </td>
      <td>Parametro di query aggiuntivo per l’URL utilizzato per recuperare il contenuto di destinazione </td>
    </tr>
    <tr>
      <td>
        <p>
          <span>web.webPageDetails.isPersonalizedURL</span>
        </p>
      </td>
      <td>
        <p>
          <span>Evento esperienza</span>
        </p>
      </td>
      <td>Solo per riferimento/contabilità</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>web.webPageDetails.webPageKey.sourceID<br/>
          </span>
        </p>
      </td>
      <td>
        <p>
          <span>Evento esperienza</span>
        </p>
      </td>
      <td>Solo per riferimento/contabilità; informazioni sull’ID sorgente per il quale è indirizzata l’e-mail</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>web.webPageDetails.webPageKey.sourceInstanceID<br/>
          </span>
        </p>
      </td>
      <td>
        <p>
          <span>Evento esperienza</span>
        </p>
      </td>
      <td>Solo per riferimento/contabilità; informazioni sull’istanza di origine per la quale è stato eseguito il targeting dell’e-mail</td>
    </tr>
    <tr class="">
      <td>
        <p>
          <span>web.webPageDetails.webPageKey.sourceKey<br/>
          </span>
        </p>
      </td>
      <td>
        <span>Evento esperienza</span>
      </td>
      <td>Solo per riferimento/contabilità; è composto da (SourceID@SourceInstanceID.SourceType)</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>web.webPageDetails.webPageKey.sourceType</span>
        </p>
      </td>
      <td>
        <span>Evento esperienza</span>
      </td>
      <td>Solo a fini di riferimento/contabilità; informazioni relative al tipo di fonte o alla provenienza</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>web.webPageDetails.webPageKey.URL</span>
        </p>
      </td>
      <td>
        <span>Evento esperienza</span>
      </td>
      <td>Utilizzato per recuperare l’URL effettivo se web.webPageDetails.name non lo contiene.</td>
    </tr>
  </tbody>
</table>
