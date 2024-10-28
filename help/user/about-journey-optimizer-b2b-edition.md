---
title: Panoramica di Adobe Journey Optimizer B2B edition
description: Scopri le funzioni chiave, i casi d’uso e le architetture di Adobe Journey Optimizer B2B Edition.
exl-id: fdfbafdf-826f-44e9-bbb6-5e729d0e18ef
source-git-commit: d1696eb54c9ff25963b51a0e3934a02e103923e4
workflow-type: tm+mt
source-wordcount: '811'
ht-degree: 5%

---

# Panoramica di Adobe Journey Optimizer B2B edition

Con Adobe Journey Optimizer B2B Edition, puoi orchestrare account e percorsi del gruppo acquisti utilizzando l’intelligenza artificiale generativa integrata e l’automazione leader di settore per ottimizzare la domanda di offerte specifiche utilizzando gruppi di acquisto qualificati per il marketing.

## Percorsi di account con gruppi di acquisto

Confrontando Adobe Journey Optimizer B2B edition con il Marketo Engage e lo standard Adobe Journey Optimizer, la distinzione chiave è che i percorsi di account spostano gli account nel Percorso, non le persone. Una persona associata a un account in genere presenta una progressione non lineare basata sull’avanzamento dell’account nel percorso e non sulle singole azioni. Ad esempio, quando un account si trova nella fase iniziale del percorso di acquisto, le informazioni inviate potrebbero riguardare le funzionalità o le caratteristiche generali della soluzione. Più avanti nel processo di acquisto, il contenuto potrebbe diventare più mirato su offerte particolari o altri elementi destinati a chiudere una vendita. Dopo l’acquisto della soluzione, le informazioni potrebbero cambiare nuovamente per fornire guide pratiche, best practice o informazioni sui prossimi eventi, oppure con contenuti su ulteriori upselling. Anche se un utente non ha interagito con il contenuto della fase iniziale, desideri comunque farla avanzare alla fase corrente in base non alle proprie azioni, ma alle azioni di altre persone all’interno del proprio account o gruppo di acquisto.

## Architettura di alto livello

Adobe Journey Optimizer B2B edition utilizza _tipi di pubblico per account_ e _tipi di pubblico per persone_ di Adobe Experience Platform per alimentare un percorso di account, che viene eseguito all&#39;interno del Marketo Engage. L’Experience Platform è sempre la fonte di verità per questi dati, ma tutta l’esecuzione e l’elaborazione del percorso dell’account avviene all’interno dell’infrastruttura di marketing B2B di Marketo Engage. L’orchestrazione porta i dati all’Experience Platform quasi in tempo reale dal connettore di origine di Marketo Engage esistente, Adobe Real-Time CDP B2B edition, che trasmette le modifiche dei dati da un Marketi Engage Experience Platform all’altro.

![Architettura dei dati di alto livello](./assets/high-level-data-architecture.png){width="500" zoomable="yes"}

>[!NOTE]
>
>Controlla i diritti delle licenze e la corrispondente [descrizione del prodotto](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer-b2b.html){target="_blank"} sui guardrail delle prestazioni e le limitazioni statiche.

### Modello di abbonamento

Una sottoscrizione Journey Optimizer B2B edition è definita da una coppia di sandbox Experience Platform (AEP) con una sottoscrizione Marketo Engage _Munchkin_. Non è possibile associare un singolo abbonamento di Marketo Engage a più sandbox di AEP. Se non si sceglie di associare un abbonamento di Marketo Engage esistente a Journey Optimizer B2B edition, viene fornito un nuovo abbonamento di Marketo Engage vuoto da utilizzare con Journey Optimizer B2B edition.

Lo scopo di questo Experience Platform è quello di fornire una vista unificata dei dati provenienti dalle istanze del Marketo Engage (e da tutti i sistemi CRM collegati), e quindi di poter intervenire sui dati unificati utilizzando un percorso di account.

### Operazioni del percorso di conti

I percorsi di account vengono creati in Journey Optimizer B2B edition e memorizzati nell’istanza di Marketo Engage associata all’abbonamento. Sebbene sia memorizzato nell’archivio dati del Marketo Engage, non è visibile dall’interfaccia utente del Marketo Engage ed è utilizzabile solo da Journey Optimizer B2B edition.

Un percorso di account inizia sempre con la selezione di un segmento di account da utilizzare come pubblico di account per il percorso. La selezione del pubblico utilizza il componente standard del selettore del pubblico di Experience Platform. Gli addetti al marketing possono quindi implementare il percorso di account suddividendo i percorsi del percorso in base ai propri criteri, che possono includere criteri di account, persone o gruppi di acquisto. In ogni ramo è possibile eseguire azioni per implementare il percorso, ad esempio inviare un messaggio e-mail o attendere che si verifichi un evento.

Dopo la creazione, il percorso di account deve essere pubblicato. Al momento della pubblicazione, il percorso di account viene convalidato e convertito in una serie di campagne di Marketo Engage che implementano l’esperienza di percorso. Data Integration Services viene contattato per avviare il flusso di dati che, a sua volta, avvia le operazioni del percorso dell&#39;account. Il primo passaggio consiste nel creare i segmenti per le persone dell’account.

### Flusso di dati

Journey Optimizer B2B edition utilizza la segmentazione dell’account Real-Time CDP sia per la definizione che per l’esecuzione dei segmenti dell’account e dei segmenti della persona dell’account correlati richiesti dai percorsi. Quando viene eseguito un percorso pubblicato, i dati sulle persone e sugli account possono cambiare e i dati vengono raccolti sulle persone che interagiscono con il percorso. Journey Optimizer B2B edition si basa sul connettore di origine del Marketo Engage affinché Real-Time CDP B2B edition possa riportare le modifiche ai dati nella sandbox Experience Platform, che è l’origine della verità.  Questi dati vengono consegnati ad AEP quasi in tempo reale.

Solo i tipi di dati esistenti supportati dal connettore di origine del Marketo Engage (account, persone e opportunità) tornano in Real-Time CDP. Ciò significa che i dati del gruppo di acquisto non fluiscono in AEP e risiedono invece nell’istanza di Marketo Engage utilizzata dall’abbonamento Journey Optimizer B2B edition.
