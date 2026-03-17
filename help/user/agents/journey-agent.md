---
title: Journey Agent B2B
description: Scopri come utilizzare il Journey Agent basato sull’intelligenza artificiale e le sue competenze per creare, gestire e osservare solidi percorsi B2B.
feature: Account Journeys, Person Journeys, Agentic AI
role: User
exl-id: 5d2945ab-4f6c-4d9c-b0a1-1a93dc1849f3
source-git-commit: 51bb47fe4f494095f1c598639f02f273b9a125ae
workflow-type: tm+mt
source-wordcount: '1170'
ht-degree: 0%

---

# Journey Agent B2B

Journey Agent B2B è un assistente basato sull’intelligenza artificiale in Adobe Journey Optimizer B2B edition che consente di progettare, eseguire, ottimizzare e monitorare i percorsi B2B attraverso il linguaggio naturale. Riduce il tempo e la complessità necessari per la creazione e la gestione dei percorsi dei clienti, combinando automazione, consigli basati sui dati e osservabilità in tempo reale.

![Prompt B2B di Journey Agent](./assets/journey-agent-prompt.png)

Journey Agent B2B fornisce una serie di competenze IA, ognuna incentrata su un aspetto diverso del ciclo di vita del percorso B2B. Le abilità attualmente disponibili sono:

* **[Percorso abilità di compilazione](#journey-build-skill)** - Crea, aggiorna e ottimizza percorsi dai prompt del linguaggio naturale
* **[Percorso di abilità di osservabilità](#journey-observability-skill)** - Poni domande su come gli account e le persone passano attraverso i percorsi attivi

## Abilità di Percorsi Build

L’abilità di creazione del Percorso traduce i tuoi obiettivi di marketing, la strategia di coinvolgimento e i KPI in percorsi di clienti B2B completi. Affronta oggi tre sfide chiave per gli esperti di marketing B2B:

* Gestire percorsi di clienti sempre più complessi (complessità in termini di pubblico, contenuti e messaggi, omnicanale)
* Aumento dell&#39;efficienza in un contesto di budget più limitati
* Come strutturare il percorso cliente ottimale

In qualità di addetto al marketing, puoi utilizzare questa abilità per:

* **Creazione** - Traduci i tuoi obiettivi di marketing, prodotti, strategia di coinvolgimento e KPI in un percorso clienti personalizzato con automazione e condizioni
* **Consiglia** - Sfrutta il coinvolgimento di marketing passato e altri dati storici per ottimizzare la creazione di percorsi
* **Ottimizza** - Analizza, regola e ottimizza i percorsi attivi in base alle previsioni o alle prestazioni effettive
* **Gestisci** - Assegna priorità, gestisci e gestisci percorsi sovrapposti e consegna messaggi

### Utilizzo di base

Per utilizzare l’abilità Journey Agent Build, digita nella finestra del prompt cosa stai cercando di creare, utilizzando il linguaggio naturale:

&quot;Creare un percorso B2B per invitare i decision maker a un roadshow negli account coinvolti che molto probabilmente aprirà una nuova pipeline.&quot;

![Richiesta B2B dell&#39;agente di Percorso per l&#39;abilità di compilazione](./assets/journey-agent-tasks.png)

Più dettagli puoi fornire, migliore sarà la risposta. Se disponi di materiali di marketing esistenti che descrivono l’evento, o il tuo prodotto, ecc., incollali nel prompt, in modo che l’agente abbia una migliore percezione dell’obiettivo.

&quot;Agisci come stratega del percorso B2B per creare un percorso di account cliente in più fasi che coinvolga decisori e responsabili marketing nella prima fase di esplorazione di `<Solution Name>`. L&#39;obiettivo è quello di convertire i visitatori anonimi in contatti noti, approfondire il coinvolgimento con contenuti rilevanti su `<domain>`.com e lead qualificati principali per `<Product Name>` attività di vendita. Utilizza canali quali e-mail e media a pagamento, sfruttando i segmenti di pubblico e i contenuti esistenti. Strutturare il percorso in fasi di consapevolezza, considerazione e valutazione per 4-6 settimane, con chiari trigger, azioni e obiettivi per ogni fase. Includi KPI come tassi di conversione, punteggi di coinvolgimento e richieste demo e restituisce l’output come un flusso di percorso strutturato.&quot;

Questo prompt dettagliato fornisce:

* **Cancella intento**: cosa desideri che faccia l&#39;intelligenza artificiale? Specifica l&#39;attività o il risultato.
* **Ricco di contesto**: fornisci informazioni di base o vincoli rilevanti. Se possibile, includi esempi o riferimenti.
* **Formato strutturato**: utilizzare punti elenco, passaggi numerati o modelli.
* **Assegnazione ruolo**: specifica il ruolo dell&#39;IA - &#39;Agisci come analista di dati...&#39;

Utilizza l’agente per iterare il perfezionamento: inizia con semplice, quindi perfeziona il prompt in base ai risultati. I cicli di feedback migliorano i risultati nel tempo.

### Creazione di percorsi B2B end-to-end

L’abilità di creazione del Percorso può generare un flusso di percorso end-to-end (percorso account o persona) dai prompt di testo e dai metadati in linguaggio naturale, attraverso un’esperienza di conversazione anziché un’interfaccia utente tradizionale.

Esempi di prompt di Percorso end-to-end:

* Crea un percorso cross-channel per promuovere account che non sono stati coinvolti con il mio contenuto negli ultimi 30 giorni.
* Crea un percorso per effettuare vendite incrociate di una soluzione ad account che mostrano intenti elevati senza pipeline aperta, fornendo contenuti personalizzati per i ruoli più importanti dei gruppi di acquisto.
* Creare un percorso B2B per invitare i responsabili decisionali a un roadshow negli account coinvolti che molto probabilmente aprirà una nuova pipeline.
* Crea un percorso per gli account con spazi vuoti con l’intento per la mia soluzione, concentrandosi sulle persone coinvolte nel contenuto del sito web.

### Percorsi multi-stage

Puoi agire come progettista di percorsi B2B per creare un percorso di account cliente in più fasi che informi i responsabili decisionali e gli utenti marketing fin dalle prime fasi della fase di esplorazione.
L’obiettivo è quello di convertire i visitatori anonimi in contatti noti, rafforzare il coinvolgimento con contenuti rilevanti e lead altamente qualificati per attività di vendita.

* Utilizza canali come `Email`, `Paid media`, `Personalized web experiences` per sfruttare i segmenti di pubblico e i contenuti esistenti.
* Strutturare il percorso in `awareness`, `consideration` e `evaluation` fasi nell&#39;arco di 4-6 settimane, con trigger, azioni e obiettivi chiari per ciascuna fase.
* Includere i KPI, ad esempio `conversion rates`, `engagement scores` e `demo requests`, e restituire l&#39;output come un flusso di percorso strutturato.

## Osservabilità percorso abilità

L’abilità Osservabilità del Percorso consente di porre domande in linguaggio naturale sul modo in cui gli account e le persone si spostano nei percorsi B2B, senza scavare tra mappe di percorso, registri o dashboard. Copre due aree principali: progressione del percorso e osservabilità della sincronizzazione dei dati.

È possibile accedervi in due posizioni all’interno di Journey Optimizer B2B edition:

* **Assistente sulla barra a destra nella mappa del percorso** - Poni domande specifiche per il percorso direttamente dalla mappa del percorso. Il nome del percorso viene inserito automaticamente nel contesto.

* **Pagina dell&#39;Assistente a schermo intero** - Una visualizzazione conversazionale più ampia adatta a domande complesse o con più account ed esplorando più percorsi.

### Percorsi insight a livello di account

Traccia il flusso di un account specifico in un percorso ponendo domande come:

* &quot;Datemi le informazioni di base sull&#39;account ACME Industries.&quot;
* &quot;Dimmi in che modo l&#39;account Northstar Services ha adottato la strategia ABM Nurture del percorso.&quot;
* &quot;Quando è iniziato questo percorso l’account Contoso LLC?&quot;

### Ragionamento e conteggi del percorso a nodi separati

Scopri perché è stato acquisito un ramo e quante persone o account hanno seguito ciascun percorso:

* &quot;Perché l’account QiDemoAccount24 è passato al percorso tecnologico della California a split node c764a9?&quot;
* &quot;Assegnami il conteggio delle persone per ogni percorso in split node-459c7c.&quot;
* &quot;Mostrami le persone nel percorso di San Jose per Account8.&quot;

L&#39;agente analizza la logica di suddivisione, gli attributi del conto e le attività per spiegare le decisioni di instradamento e restituire i conteggi per percorso o gli elenchi di persone.

### Risultati di percorso a livello di persone

Analizza i singoli risultati all’interno di un account o in un intero percorso, utile soprattutto per l’analisi di gruppo e per tenere traccia del comportamento del responsabile delle decisioni rispetto a quello dell’influencer:

* &quot;Assegnami il conteggio delle persone in ogni percorso per questo nodo suddiviso per Account123.&quot;
* &quot;Elenca le persone nel percorso di salto nascosto.&quot;
* &quot;Visualizza persone nel percorso di San Diego per questo account&quot;.

### Ciclo di vita e tempistica del percorso

Recupera le marche temporali chiave per un percorso o per account specifici:

* &quot;Quando è nato questo percorso?&quot;
* &quot;Quando è entrato il primo account in questo percorso?&quot;
* &quot;Quando è iniziato questo percorso l’account QiDemoAccount50?&quot;

### Pubblico esterno e visibilità dell’attivazione

Per i percorsi che inviano messaggi push a canali esterni, come LinkedIn, puoi controllare lo stato di attivazione:

* &quot;bsmith@acme.com è nel pubblico esterno?&quot;
* &quot;Elenca tutte le persone attivate in LinkedIn tramite ObservabilityExtAudience01.&quot;

### Sincronizzazione dei dati e osservabilità della pipeline

L’abilità Observability può anche far emergere informazioni sullo stato di sincronizzazione dei dati per facilitare la risoluzione dei problemi relativi all’eventuale esclusione di un account o di un lead da un percorso:

* Metriche e stato del processo di esportazione del pubblico esterno
* Programmi di segmentazione batch e tempi di completamento
* Pianificazione della manutenzione del gruppo di acquisto
* Statistiche gestione processi (completato/non riuscito)