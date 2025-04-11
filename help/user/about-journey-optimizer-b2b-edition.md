---
title: Panoramica di Adobe Systems Journey Optimizer B2B Edition
description: Scopri le funzioni chiave, i casi d’uso e le architetture di Adobe Journey Optimizer B2B Edition.
exl-id: fdfbafdf-826f-44e9-bbb6-5e729d0e18ef
source-git-commit: 5ca03b12fd459c64b245ad95e60a382c355922f9
workflow-type: tm+mt
source-wordcount: '811'
ht-degree: 5%

---

# Panoramica di Adobe Systems Journey Optimizer B2B Edition

Con Adobe Journey Optimizer B2B Edition, puoi orchestrare account e percorsi del gruppo acquisti utilizzando l’intelligenza artificiale generativa incorporata e l’automazione leader di settore per ottimizzare la domanda di offerte specifiche utilizzando gruppi di acquisto qualificati per il marketing.

## Percorsi di account con gruppi di acquisto

Confrontando Adobe Journey Optimizer B2B edition con Marketo Engage e Adobe Journey Optimizer Standard, la distinzione chiave è che i percorsi di account spostano gli account nel Percorso, non le persone. Una persona associata a un account in genere presenta una progressione non lineare basata sull’avanzamento dell’account nel percorso e non sulle singole azioni. Ad esempio, quando un account si trova nella fase iniziale del percorso di acquisto, le informazioni inviate potrebbero riguardare le funzionalità o le caratteristiche generali della soluzione. Più avanti nel processo di acquisto, il contenuto potrebbe diventare più mirato su offerte particolari o altri elementi destinati a chiudere una vendita. Dopo l’acquisto della soluzione, le informazioni potrebbero cambiare nuovamente per fornire guide pratiche, best practice o informazioni sui prossimi eventi, oppure con contenuti su ulteriori upselling. Anche se un utente non ha interagito con il contenuto della fase iniziale, desideri comunque farla avanzare alla fase corrente in base non alle proprie azioni, ma alle azioni di altre persone all’interno del proprio account o gruppo di acquisto.

## Architettura di alto livello

Adobe Journey Optimizer B2B edition utilizza _tipi di pubblico per account_ e _tipi di pubblico per persone_ di Adobe Experience Platform per alimentare un percorso di account, che viene eseguito all&#39;interno di Marketo Engage. Experience Platform è sempre la fonte di verità per questi dati, ma tutta l&#39;esecuzione e l&#39;elaborazione del viaggio account avviene all&#39;interno della Marketo Engage B2B dell&#39;infrastruttura marketing. L’orchestrazione riporta i dati ad Experience Platform quasi in tempo reale tramite il connettore di origine Marketo Engage - Adobe Real-Time CDP B2B edition esistente, che trasmette le modifiche ai dati da Marketo Engage ad Experience Platform.

![Architettura dei dati di alto livello](./assets/high-level-data-architecture.png){width="500" zoomable="yes"}

>[!NOTE]
>
>Controlla i diritti di licenza e la descrizione](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer-b2b.html){target="_blank"} del prodotto corrispondente [sui guardrail delle prestazioni e sulle limitazioni statiche.

### Modello di abbonamento

Una sottoscrizione Journey Optimizer B2B edition è definita da una coppia di sandbox Experience Platform (AEP) con una sottoscrizione Marketo Engage _Munchkin_. Non è possibile associare un singolo abbonamento Marketo Engage a più di una sandbox AEP. Se non si sceglie di associare un abbonamento Marketo Engage esistente a Journey Optimizer B2B edition, viene effettuato il provisioning con un nuovo abbonamento Marketo Engage vuoto da utilizzare con Journey Optimizer B2B edition.

Lo scopo di Experience Platform in questa configurazione è quello di fornire una vista unificata dei dati provenienti dalle istanze di Marketo Engage (e da tutti i sistemi CRM associati), e quindi di poter intervenire sui dati unificati utilizzando un percorso di account.

### Operazioni del percorso di conti

I percorsi di account vengono creati in Journey Optimizer B2B edition e memorizzati nell’istanza Marketo Engage associata all’abbonamento. Anche se è memorizzato nell’archivio dati di Marketo Engage, non è visibile dall’interfaccia utente di Marketo Engage ed è utilizzabile solo da Journey Optimizer B2B edition.

Un percorso di account inizia sempre con la selezione di un segmento di account da utilizzare come pubblico di account per il percorso. La selezione del pubblico utilizza il componente standard del selettore del pubblico di Experience Platform. Gli esperti di marketing possono quindi implementare il percorso account suddividendo i percorsi del percorso in base ai propri criteri, che possono includere criteri di account, criteri di persone o criteri del gruppo di acquisto. In ogni filiale è possibile eseguire azioni per implementare il viaggio, ad esempio l&#39;invio di un&#39;e-mail o l&#39;attesa che si verifichi un evento.

Una volta creato, il percorso account deve essere pubblicato. In pubblicare momento, il percorso account viene convalidato e convertito in una serie di campagne Marketo Engage che implementare l&#39;esperienza di viaggio. I Data Integration Services vengono contattati per avviare il flusso di dati che, a sua volta, avvia le operazioni di account percorso. Il primo passo consiste nel creare i segmenti per le persone dell&#39;account.

### Flusso dei dati

Journey Optimizer B2B edition utilizza la segmentazione dell’account Real-Time CDP sia per la definizione che per l’esecuzione dei segmenti dell’account e dei segmenti della persona dell’account correlati richiesti dai percorsi. Quando viene eseguito un percorso pubblicato, i dati sulle persone e sugli account possono cambiare e i dati vengono raccolti sulle persone che interagiscono con il percorso. Journey Optimizer B2B edition si basa sul connettore di origine di Marketo Engage per consentire a Real-Time CDP B2B edition di riportare le modifiche ai dati alla sandbox di Experience Platform, che è l’origine della verità.  Questi dati vengono inviati ad AEP quasi in tempo reale.

Solo i tipi di dati esistenti supportati dal connettore di origine di Marketo Engage (account, persone e opportunità) tornano in Real-Time CDP. Ciò significa che i dati del gruppo di acquisto non fluiscono in AEP e risiedono invece nell’istanza Marketo Engage utilizzata dall’abbonamento Journey Optimizer B2B edition.
