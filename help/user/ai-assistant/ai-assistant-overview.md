---
title: Assistente AI in Journey Optimizer B2B edition
description: Scopri l’Assistente all’intelligenza artificiale e come può aiutarti a navigare nei concetti dei prodotti e ad accedere a informazioni operative personalizzate per il tuo ambiente.
feature: AI Assistant
role: User, Admin
level: Beginner
exl-id: 52ff66d2-1969-4e2c-985a-c75e613368de
source-git-commit: 4a54548ad061fc778fae3bc4b8499f3716850e4a
workflow-type: tm+mt
source-wordcount: '1261'
ht-degree: 4%

---

# Assistente AI in Journey Optimizer B2B edition

L&#39;Assistente IA in Journey Optimizer B2B edition viene creato dalla stessa base tecnologica di [Assistente IA in Adobe Experience Platform](https://experienceleague.adobe.com/it/docs/experience-platform/ai-assistant/home){target="_blank"}. Si tratta di un’esperienza di conversazione che puoi utilizzare per accelerare i flussi di lavoro in Adobe Journey Optimizer B2B edition. È possibile utilizzare l’Assistente AI per comprendere meglio le funzionalità del prodotto, risolvere i problemi o eseguire ricerche attraverso informazioni e trovare informazioni operative per Journey Optimizer B2B edition.

>[!IMPORTANT]
>
>È necessario un accordo per le [linee guida per l&#39;utente](https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html) prima di poter utilizzare l&#39;Assistente IA in Journey Optimizer B2B edition. Questo contratto contiene anche il contratto beta pubblico, in modo da poter utilizzare funzioni aggiuntive di AI Assistant durante il rollout in capacità beta.

+++Visualizza l&#39;interfaccia del contratto utente

![Prima pagina del contratto utente.](./assets/user-agreement-1.png)

![Ultima pagina del contratto utente.](./assets/user-agreement-2.png)

+++

## Funzionalità di AI Assistant in Journey Optimizer B2B edition

Per formulare una risposta alle domande inviate, l’Assistente AI esegue una query su un database e converte i dati dal database in una risposta leggibile. Questa risposta è una rappresentazione interna dei dati sottostanti ed è anche nota come _&#x200B;**_Knowledge Graph_**&#x200B;_, un Web completo di concetti, dati e metadati per una determinata risposta. Il Knowledge Graph è costituito da sottografi a cui viene fatto riferimento ogni volta che vengono inviate query:

* Documentazione di Experience League.
* Artefatti operativi, come schemi, campi, tipi di pubblico e percorsi.

Prima di inviare una query di Assistente IA, considera il tipo di richiesta necessario:

### Conoscenza del prodotto

Per conoscenza del prodotto si intendono i concetti e gli argomenti basati sulla documentazione di Journey Optimizer B2B edition su Adobe Experience League. Le domande relative alla conoscenza del prodotto possono essere ulteriormente specificate nei seguenti sottogruppi:

| Conoscenza del prodotto | Esempi |
| --- | --- |
| Apprendimento puntato | <li>Che cos’è un gruppo di acquisto? <li> Mostrami un esempio di modello per ruoli di gruppo di acquisto? |
| Rilevamento aperto | <li>Quali sono i passaggi per creare gruppi di acquisto? <li>Come si utilizzano i campi personalizzati nei modelli di ruolo di un gruppo di acquisto? |
| Risoluzione dei problemi | <li>Perché non sono stati creati gruppi di acquisto per il mio percorso? <li>Perché non riesco a trovare gli Eventi esperienza da ascoltare nel percorso? |

### Informazioni operative

_Informazioni operative_ si riferisce alle risposte che l&#39;Assistente AI genera sugli oggetti metadati (attributi, pubblico dell&#39;account, flussi di dati, set di dati, destinazioni, percorsi di account, schemi, origini, modelli di gruppi di acquisto e interessi delle soluzioni). Queste informazioni includono conteggi, ricerche e impatto sulla derivazione. Non esaminano i dati all’interno della sandbox.

* Quale pubblico dell’account ha la dimensione di pubblico più grande e qual è tale dimensione?
* Quanti tipi di pubblico dell’account non sono mai stati utilizzati in alcun percorso?
* Quali percorsi attivi utilizzano l&#39;interesse della soluzione _x_?

Puoi porre domande all’Assistente AI sulle informazioni operative nei seguenti domini:

| Dominio | Metadati supportati | Metadati non supportati |
| --- | --- | --- |
| Attributi/campi | <li>Ricerca nome attributo <li>Attributo: relazione schema <li>Attributo: relazione set di dati <li>Attributo: relazione pubblico <li>Attributo - relazione di destinazione | <li>Classe attributo <li>Audit <li>Stato obsoleto <li>Etichette <li>Valore memorizzato negli attributi |
| Pubblico dell&#39;account <br><br>**_Nota:_**&#x200B;l&#39;Assistente all&#39;intelligenza artificiale B2B di AJO può rispondere solo alle domande sul pubblico per i tipi di pubblico dell&#39;account, mentre l&#39;Assistente all&#39;intelligenza artificiale di Experience Platform può rispondere alle domande solo per i tipi di pubblico della persona | <li>Conteggio del pubblico <li>Tipo di pubblico (in streaming o in batch) <li>Date di creazione/modifica <li>Stato attivazione <li>Conteggio membri <li>Pubblico duplicato <li>Ricerca per nome e ID | <li>Sovrapposizioni del pubblico <li>Attivazione pubblico <li>Audit <li>Crea/modifica <li>Etichette <li>Tendenze delle qualifiche dei membri |
| Flussi di dati | <li>Conteggi dei flussi di dati <li>Stato del flusso di dati <li>Flusso di dati: relazione set di dati <li>Flusso di dati - relazione di origine | <li>Creazione/modifica <li>Relazioni flusso di dati-batch <li>Acquisisci conteggio profili |
| Set di dati | <li>Conteggio set di dati <li>Stato abilitazione profilo <li>Data di creazione/modifica <li>Set di dati: relazione schema <li>Set di dati: relazione pubblico <li>Set di dati: relazione attributo <li>Set di dati: relazione flusso di dati <li>Ricerca nome <li>Ricerca per nome e ID | <li>Audit <li>Creato da <li>Set di dati: relazione batch <li>Creazione/modifica del set di dati <li>Dimensione set di dati <li>Numero di profili <li>Numero di righe <li>Ricerca di valori |
| Destinazioni | <li>Conteggi di destinazione configurati <li>Destinazione - Relazione pubblico <li>Relazione attributo di destinazione | <li>Configurazione account <li>Informazioni sulle credenziali dell&#39;account <li>Profili univoci attivati |
| Percorsi (Percorsi di account) | <li>Conteggio <li>Ricerca per nome e ID <li>Stato del percorso <li>Date di creazione/modifica | <li>Attributi - Audit relazioni percorso <li>Creazione/modifica <li>Creato da |
| Schemi | <li>Conteggi schema <li>Data di creazione/modifica <li>Schema - relazione attributo <li>Schema: relazione tra set di dati <li>Schema: relazione pubblico <li>Stato abilitazione profilo <li>Ricerca nome <li>Ricerca per nome e ID | <li>Audit <li>Creazione/modifica <li>Creato da <li>Gruppi di campi <li>Identità <li>Spazi dei nomi delle identità <li>Etichette <li>Numero di profili |
| Origini | <li>Conteggi account <li>Stato account <li>Flussi di dati attivi/inattivi per ogni account <li>Connettore Source - relazione flusso di dati <li>Account Source - relazione flusso di dati | <li>Informazioni sulle credenziali dell’account <li>Configurazione accountMetriche di acquisizione dati <li>Numero di profilesSource - relazioni batch |
| Modello per gruppo di acquisto | <li>Conteggi <li>Stato <li>Ruoli <li>Ricerca per nome e ID | <li>Regole ruolo |
| Interesse soluzione | <li>Conteggi <li>Stato <li>Interesse soluzione - Relazione modello gruppo di acquisto <li>Ricerca per nome e ID | <li>Interesse soluzione - Relazione tra gruppo di acquisto |

{style="table-layout:fixed"}

Per le domande sulle informazioni operative, le risposte potrebbero non riflettere lo stato corrente dell’interfaccia utente. I dati che supportano queste domande vengono aggiornati una volta ogni 24 ore. Ad esempio, le modifiche apportate dagli utenti in Real-Time CDP durante il giorno vengono sincronizzate con gli archivi dati di notte e quindi diventano disponibili per le domande degli utenti di mattina. Accedi a una sandbox per informazioni su dati specifici relativi agli oggetti.

### Ambito della funzione

Attualmente, l’ambito di AI Assistant è il seguente:

* **Conoscenza del prodotto**: l&#39;Assistente all&#39;intelligenza artificiale è in grado di rispondere alle domande relative alla conoscenza del prodotto per Real-Time Customer Data Platform e Adobe Journey Optimizer B2B edition.

* **Informazioni operative**: è possibile porre domande all&#39;Assistente AI per informazioni operative sui seguenti oggetti dati: attributi, pubblico dell&#39;account, flussi di dati, set di dati, destinazioni, percorsi di account, schemi, origini, modelli di gruppi di acquisto e interessi delle soluzioni.

### Privacy, sicurezza e governance

L’Assistente per l’intelligenza artificiale in Journey Optimizer B2B edition è progettato per garantire la privacy, la sicurezza e la governance in prima linea. Consulta le seguenti informazioni per scoprire le funzionalità incentrate sulla fiducia del cliente che puoi aspettarti dall’Assistente AI:

* Nessun dato personale viene utilizzato oggi da AI Assistant, anche a scopo di formazione.

* Ai Assistant non è a conoscenza dei dati dei clienti, ad esempio persone, account, opportunità e gruppi di acquisto.

* Per interagire con l&#39;Assistente AI è necessario disporre di autorizzazioni esplicite.

   * Un amministratore può impostare le autorizzazioni utilizzando [Interfaccia utente autorizzazioni](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/abac/permissions-ui/permissions){target="_blank"} e [Admin Console](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/ui/browse){target="_blank"}.

   * Le autorizzazioni sono granulari e l’amministratore della sandbox può configurare quali utenti possono porre diverse categorie di domande (domande basate sulla conoscenza del prodotto con l’Assistente AI o domande su informazioni operative).

* È possibile visualizzare un registro delle interazioni precedenti con l’Assistente AI con un criterio di conservazione di 30 giorni.

* L’Assistente AI si basa sui dati specifici delle sandbox e sulla documentazione pubblica di Adobe quando si rispondono alle richieste degli utenti. I dati non sono condivisi tra sandbox diverse.

* I prompt forniti all&#39;Assistente IA non vengono condivisi con altri clienti.

### Domande frequenti

Di seguito è riportato un elenco di risposte alle domande più frequenti sull’Assistente IA in Journey Optimizer B2B edition.

**Le informazioni dell&#39;Assistente di IA sono fornite in tempo reale?**

I dati presentati nelle risposte dell’Assistente AI vengono aggiornati ogni giorno. Questo ciclo significa che i dati inclusi nelle risposte possono essere anteriori di 24 ore rispetto ai dati visualizzati nell’interfaccia utente al momento della risposta.

**Quali sono le funzionalità dell&#39;Assistente di intelligenza artificiale?**

L’Assistente AI è in grado di rispondere alle domande relative alle conoscenze sui prodotti Adobe e alle informazioni operative sugli artefatti operativi.

**L&#39;Assistente AI può fornire informazioni sui dati dei clienti?**

No. L’Assistente AI non ha accesso ai dati del cliente e pertanto non viene esaminato o utilizzato dall’Assistente AI.

**Le informazioni personali vengono utilizzate nei dati di formazione dell&#39;Assistente di intelligenza artificiale?**

L’Assistente AI non utilizza informazioni personali a scopo di formazione. Non fornire informazioni personali su di te (compreso il tuo nome o le tue informazioni di contatto) o su altre parti di AI Assistant.

## Passaggi successivi

Con una conoscenza generale di AI Assistant, procedi all’abilitazione e all’utilizzo di AI Assistant durante i flussi di lavoro. Per ulteriori informazioni, consulta la seguente documentazione:

* [Abilitare l’accesso all’Assistente IA](./enable-ai-assistant-access.md)
* [Guida alle domande](./question-guidance.md)
* [Utilizzo dell’Assistente IA](./use-ai-assistant.md)
