---
title: Linee guida sulle domande per l’Assistente AI
description: Scopri come scrivere domande efficaci per l’Assistente AI in Journey Optimizer B2B edition.
feature: AI Assistant
role: User
level: Beginner
exl-id: 65541246-7f4f-442f-8293-df036ea1c4ac
source-git-commit: 4a54548ad061fc778fae3bc4b8499f3716850e4a
workflow-type: tm+mt
source-wordcount: '884'
ht-degree: 1%

---

# Linee guida sulle domande per l’Assistente AI in Journey Optimizer B2B edition

Rivedi il seguente set di domande di esempio per l’esecuzione di query sull’Assistente IA in Journey Optimizer B2B edition. Queste informazioni includono anche suggerimenti su come formulare le domande per ottenere risposte ottimali dall’Assistente AI.

## Domande basate su obiettivi

Le domande di esempio seguenti sono raggruppate in base agli obiettivi che è possibile raggiungere quando si utilizza l’Assistente IA:

| Obiettivo | Descrizione | Esempio |
| --- | --- | --- |
| Concetti di apprendimento e flussi di lavoro continui | In qualità di utente principiante, puoi utilizzare AI Assistant per apprendere i concetti di Real-Time CDP e Adobe Journey Optimizer B2B edition e per integrare te stesso in prodotti e funzionalità che non conosci. <br>In qualità di utente esperto, puoi utilizzare l&#39;Assistente AI per risolvere un caso limite che potrebbe bloccare il flusso di lavoro. | <li>Dimmi alcuni casi d’uso per Real-Time CDP. <li>Spiegami il concetto di Gruppo acquisti. |
| Risoluzione dei problemi | Utilizza l’Assistente AI per scoprire come eseguire il debug degli errori di base che potrebbero verificarsi nel flusso di lavoro. | <li>Cosa significa questo errore &lt;ERROR_MESSAGE>? <li>Perché non riesco a eliminare il pubblico denominato &quot;...&quot;? |
| Igiene delle sandbox | Utilizza l’Assistente AI per identificare eventuali oggetti duplicati o inutilizzati in modo da poter gestire la sandbox in modo efficiente. | <li>Puoi mostrarmi tipi di pubblico simili per l’account? <li>Esistono schemi a cui non è associato un set di dati? |
| Analisi del valore | Utilizza l’Assistente AI per identificare gli oggetti dati più utilizzati e valutare eventuali indicatori di prestazioni o trovare gli oggetti dati più importanti. | <li>Quanti account ci sono nella definizione del segmento &quot;...&quot;? <li>Quando i tipi di pubblico sono stati attivati nella destinazione Pubblico di Experience Cloud? |
| Ricerca | Utilizza l’Assistente AI per trovare gli oggetti Experience Platform e Adobe Journey Optimizer B2B edition supportati, ad esempio il pubblico dell’account, i set di dati, le destinazioni, gli schemi, le origini, i percorsi di account, i modelli di gruppi di acquisto e gli interessi delle soluzioni | <li>Elenca i tipi di pubblico contenenti &quot;Luma&quot; nel nome utilizzati nei percorsi di account. <li>Quali attributi sono presenti nello schema XDM &quot;Luma: Azioni personalizzate&quot;? |
| Analisi dell&#39;impatto | Utilizza l’Assistente AI per identificare gli oggetti dati utilizzati in alcuni flussi di lavoro in modo da poter valutare l’impatto di eventuali modifiche. | <li>Quali tipi di pubblico dell&#39;account utilizzano `workEmail.address` nello schema &quot;Persona B2B&quot;? <li>Quali set di dati sono ... `jobTitle` archiviati in? |

## Formulazione delle domande

Per ottenere una risposta il più accurata possibile, è necessario formulare le domande all’Assistente IA con chiarezza e contesto. Consulta il seguente elenco di suggerimenti per indicazioni su come porre una domanda chiara con il contesto:

* Dichiara il tuo compito e/o la tua domanda in modo conciso.
* Evita un linguaggio ambiguo o una sintassi troppo complessa per facilitare la comprensione.
* Fornisci un contesto rilevante relativo all’attività e/o alla domanda, in quanto il contesto può aiutare l’Assistente AI a generare risposte più rilevanti.

Le tabelle seguenti forniscono alcune best practice che è possibile seguire quando si utilizza l’Assistente IA:

| Esegui | Esempio |
| --- | --- |
| <li>Specificare l&#39;oggetto o le informazioni da recuperare o analizzare. <li>Provare a inserire i nomi degli oggetti dati tra virgolette. <li>Se si conosce solo una parte del nome dell&#39;oggetto, è possibile specificarlo nella domanda. | <li>Quali set di dati utilizzano lo schema &quot;Account B2B&quot;? <li>Mostra i tipi di pubblico attivati il cui nome contiene &quot;Account&quot;. Classificarli in base al numero di membri. |
| <li>Evita ambiguità e usa un linguaggio chiaro. <li>Utilizza una terminologia precisa per garantire una maggiore chiarezza nella query. <li>Quando fai domande su Adobe Experience Platform e Adobe Journey Optimizer B2B edition, prova a utilizzare la terminologia specifica di Experience Platform o Adobe Journey Optimizer B2B edition per migliorare la pertinenza delle risposte. | <li>Quanti membri ci sono in &quot;Il mio pubblico account&quot;? <li>Quanti percorsi di account utilizzano il pubblico dell’account &quot;Pubblico del mio account&quot;? |
| <li>Fornisci contesto o specifica un criterio per filtrare i risultati. <li>Utilizza un criterio di filtro nelle domande per limitare il volume di dati nella risposta. | <li>Mostra i tipi di pubblico dell’account che non sono stati attivati e sono stati creati più di 6 mesi fa e che non sono mai stati modificati. <li>Mostra i percorsi di account pubblicati negli ultimi 7 giorni e utilizza un pubblico di account con più di 1000 membri |

| Non | Esempio |
| --- | --- |
| Utilizza un linguaggio vago o ambiguo. | <li>Datemi informazioni sui set di dati. <li>Cosa fa il percorso x? <li>Quanti utenti ho in &quot;ACME Audience&quot;? <li>Mostra segmenti. <li>Attributi elenco. |
| Eseguire richieste incomplete. | <li>&quot;Luma - Set di dati fedeltà&quot; |
| Assumere conoscenze senza contesti. | <li>Pubblico negli ultimi 6 mesi. <li>Crea una query per me. <li>Crea un percorso per me |
| Formulare query eccessivamente complesse. | <li>Fornisci un’analisi completa della derivazione dei dati tra tutti gli oggetti e le loro dipendenze. |
| Omettere criteri o parametri. | <li>Mostra i set di dati. |

## Esempi di domande non supportate

L’elenco seguente include esempi di domande che l’Assistente IA in Journey Optimizer B2B edition non supporta attualmente:

* Quali tipi di pubblico dell’account utilizzano il campo workEmail.address del gruppo di campi ... nelle sue condizioni? 
* Mostra il numero di percorsi attivi utilizzando tipi di pubblico dell&#39;account di dimensioni superiori a 10.000, 5000-10.000, 1000-5000 e inferiori a 1000, in una visualizzazione di distribuzione
* Chi ha effettuato l’ultimo aggiornamento nel percorso di account x?
* Quanti percorsi attivi aggiungono membri del gruppo di acquisto per l&#39;interesse della soluzione x?
* Quali percorsi attivi aggiungono membri del gruppo di acquisto per l&#39;interesse della soluzione x?
* Qual è il titolo decisionale più comune per l’acquisto di modelli di gruppo?
* Chi sono i responsabili decisionali per l’acquisto del modello di gruppo x?

## Passaggi successivi

Per informazioni sull&#39;utilizzo delle funzionalità dell&#39;Assistente di intelligenza artificiale durante i flussi di lavoro, vedere [Utilizzare l&#39;Assistente di intelligenza artificiale in Journey Optimizer B2B edition](./use-ai-assistant.md).
