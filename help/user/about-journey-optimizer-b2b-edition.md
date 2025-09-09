---
title: Panoramica di Adobe Journey Optimizer B2B Edition
description: 'Scopri Adobe Journey Optimizer B2B edition: orchestrare percorsi di account con gruppi di acquisto, approfondimenti sull’intelligenza artificiale e l’integrazione di Experience Platform per il marketing B2B.'
exl-id: fdfbafdf-826f-44e9-bbb6-5e729d0e18ef
source-git-commit: d3247a48ff1fbda54c559fa03580865da7252935
workflow-type: tm+mt
source-wordcount: '819'
ht-degree: 90%

---

# Panoramica di Adobe Journey Optimizer B2B Edition

Con Adobe Journey Optimizer B2B Edition, puoi orchestrare account e percorsi del gruppo acquisti utilizzando l’intelligenza artificiale generativa incorporata e l’automazione leader di settore per ottimizzare la domanda di offerte specifiche utilizzando gruppi di acquisto qualificati per il marketing.

## Percorsi di account con gruppi di acquisto

Quando si confrontano Adobe Journey Optimizer B2B edition con gli standard Marketo Engage e Adobe Journey Optimizer, la distinzione chiave è che i percorsi di account spostano gli account nel Percorso, non le persone. Una persona associata a un account in genere presenta una progressione non lineare basata sull’avanzamento dell’account nel percorso e non sulle singole azioni. Ad esempio, quando un account si trova nella fase iniziale del percorso di acquisto, le informazioni inviate potrebbero riguardare le funzionalità o le caratteristiche generali della soluzione. Più avanti nel processo di acquisto, il contenuto potrebbe diventare più mirato su offerte particolari o altri elementi destinati a chiudere una vendita. Dopo l’acquisto della soluzione, le informazioni potrebbero cambiare nuovamente per fornire guide pratiche, best practice o informazioni su eventi successivi, oppure con contenuti su ulteriori upsell. Anche se un singolo utente non ha interagito con il contenuto della fase iniziale, desideri comunque farlo avanzare alla fase corrente non in base alle proprie azioni, ma a quelle di altre persone all’interno del proprio account o gruppo di acquisto.

## Architettura di alto livello

Adobe Journey Optimizer B2B Edition utilizza i _tipi di pubblico dell’account_ e i _tipi di pubblico delle persone_ di Adobe Experience Platform per alimentare un percorso di account, che viene eseguito all’interno di Marketo Engage. Experience Platform è sempre la fonte di verità per questi dati, ma tutta l’esecuzione e l’elaborazione del percorso dell’account avviene all’interno dell’infrastruttura di marketing B2B di Marketo Engage. L’orchestrazione riporta i dati a Experience Platform quasi in tempo reale tramite il connettore di origine Marketo Engage - edizione B2B di Adobe Real-Time CDP esistente, che trasmette le modifiche ai dati da Marketo Engage a Experience Platform.

![Architettura dei dati di alto livello](./assets/high-level-data-architecture.png){width="500" zoomable="yes"}

>[!NOTE]
>
>Verifica i diritti delle licenze e la corrispondente [descrizione del prodotto](https://helpx.adobe.com/it/legal/product-descriptions/adobe-journey-optimizer-b2b.html){target="_blank"} sui guardrail delle prestazioni e le limitazioni statiche.

### Modello di abbonamento

Un abbonamento Journey Optimizer B2B Edition è definito da una coppia di sandbox Experience Platform (AEP) con un abbonamento Marketo Engage _Munchkin_. Non è possibile associare un singolo abbonamento Marketo Engage a più di una sandbox AEP. Se non scegli di associare un abbonamento Marketo Engage esistente a Journey Optimizer B2B Edition, ti viene fornito un nuovo abbonamento Marketo Engage vuoto da utilizzare con Journey Optimizer B2B Edition.

Lo scopo di Experience Platform in questa configurazione è quello di fornire una vista unificata dei dati provenienti dalle istanze di Marketo Engage (e da tutti i sistemi CRM associati), e quindi di poter intervenire sui dati unificati utilizzando un percorso di account.

### Operazioni del percorso di account

I percorsi di account vengono creati in Journey Optimizer B2B Edition e memorizzati nell’istanza Marketo Engage associata all’abbonamento. Anche se è memorizzato nell’archivio dati di Marketo Engage, non è visibile dall’interfaccia utente di Marketo Engage ed è utilizzabile solo da Journey Optimizer B2B Edition.

Un percorso di account inizia sempre con la selezione di un segmento di account da utilizzare come pubblico di account per il percorso. La selezione del pubblico utilizza il componente standard del selettore del pubblico di Experience Platform. Gli addetti al marketing possono quindi implementare il percorso di account suddividendo i percorsi del percorso in base ai propri criteri, che possono includere criteri di account, persone o gruppi di acquisto. In ogni ramo è possibile eseguire azioni per implementare il percorso, ad esempio inviare un messaggio e-mail o attendere che si verifichi un evento.

Dopo la creazione, il percorso di account deve essere pubblicato. Al momento della pubblicazione, il percorso di account viene convalidato e convertito in una serie di campagne Marketo Engage che implementano l’esperienza di percorso. I servizi di integrazione dati vengono contattati per avviare il flusso di dati che, a sua volta, avvia le operazioni del percorso dell’account. Il primo passaggio consiste nel creare i segmenti per le persone dell’account.

### Flusso di dati

Journey Optimizer B2B Edition utilizza la segmentazione dell’account Real-Time CDP sia per la definizione che per l’esecuzione dei segmenti dell’account e dei segmenti della persona dell’account correlati, richiesti dai percorsi. Quando viene eseguito un percorso pubblicato, i dati sulle persone e sugli account possono cambiare e vengono raccolti i dati sulle persone che interagiscono con il percorso. Journey Optimizer B2B Edition si basa sul connettore di origine di Marketo Engage per consentire all’edizione B2B di Real-Time CDP di riportare le modifiche ai dati alla sandbox di Experience Platform, che è la fonte della verità.  Questi dati vengono inviati ad AEP quasi in tempo reale.

Solo i tipi di dati esistenti supportati dal connettore di origine di Marketo Engage (account, persone e opportunità) tornano in Real-Time CDP. Ciò significa che i dati del gruppo di acquisto non fluiscono in AEP e risiedono invece nell’istanza Marketo Engage utilizzata dall’abbonamento Journey Optimizer B2B Edition.
