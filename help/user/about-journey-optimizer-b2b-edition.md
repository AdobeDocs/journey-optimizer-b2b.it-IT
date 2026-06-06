---
title: Panoramica di Adobe Journey Optimizer B2B Edition
description: 'Scopri Adobe Journey Optimizer B2B Edition: orchestra percorsi di account con gruppi acquisti, approfondimenti sull’IA e l’integrazione di Experience Platform per il marketing B2B.'
exl-id: fdfbafdf-826f-44e9-bbb6-5e729d0e18ef
autotag-review: 2026-04-29T23:21:13.339Z
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: f467931a-9b22-4ca8-869f-adfbd64061ce
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: df401a2a-327d-468c-a5e4-b7b7ccd071a0
TQID: https://experienceleague.adobe.com/L58cK4MP-S-8U9fFiXU2qZn4HCieNzjoOaSRCLkyanI
source-git-commit: ca0c6b10cf6a979249901d514116f373014544ad
workflow-type: tm+mt
source-wordcount: 803
ht-degree: 66%

---

# Panoramica di Adobe Journey Optimizer B2B Edition

Con Adobe Journey Optimizer B2B Edition, puoi orchestrare account e percorsi del gruppo acquisti utilizzando l’intelligenza artificiale generativa incorporata e l’automazione leader di settore per ottimizzare la domanda di offerte specifiche utilizzando gruppi di acquisto qualificati per il marketing.

## Percorsi di account con gruppi di acquisto

Quando si confrontano i percorsi di account con le funzionalità di percorso in Marketo Engage e Adobe Journey Optimizer Standard, la distinzione chiave è che i percorsi di account spostano gli account nel percorso, non le persone. Una persona associata a un account in genere presenta una progressione non lineare basata sull’avanzamento dell’account nel percorso e non sulle singole azioni. Ad esempio, quando un account si trova nella fase iniziale del percorso di acquisto, le informazioni inviate riguardano in genere le funzionalità o le caratteristiche generali della soluzione. Più avanti nel processo di acquisto, il contenuto diventa più mirato su offerte particolari o altri elementi orientati alla chiusura di una vendita. Dopo l’acquisto della soluzione, le informazioni cambiano nuovamente per fornire guide pratiche, best practice o informazioni sui prossimi eventi o contenuti su ulteriori upselling. Anche se un individuo non ha interagito con i contenuti della fase iniziale, puoi farli avanzare alla fase corrente in base alle azioni di altri all’interno del suo account o gruppo di acquisto.

## Architettura di alto livello

Adobe Journey Optimizer B2B Edition utilizza i _tipi di pubblico di account_ e i _tipi di pubblico di persone_ di Adobe Experience Platform per alimentare un percorso per account, che viene eseguito all’interno di Marketo Engage. Experience Platform è sempre l’origine principale di questi dati, ma tutte le operazioni di esecuzione ed elaborazione del percorso di account vengono eseguite nell’infrastruttura di marketing B2B di Marketo Engage. L’orchestrazione riporta i dati a Experience Platform quasi in tempo reale tramite il connettore di origine Marketo Engage - edizione B2B di Adobe Real-Time CDP esistente, che trasmette le modifiche ai dati da Marketo Engage a Experience Platform.

![Architettura dei dati di alto livello](./assets/high-level-data-architecture.png){width="500" zoomable="yes"}

>[!NOTE]
>
>Verifica i diritti delle licenze e la corrispondente [descrizione del prodotto](https://helpx.adobe.com/it/legal/product-descriptions/adobe-journey-optimizer-b2b.html){target="_blank"} sui guardrail delle prestazioni e le limitazioni statiche.

### Modello di abbonamento

Una coppia di sandbox Experience Platform (AEP) con una sottoscrizione a Marketo Engage _Munchkin_ definisce una sottoscrizione a Journey Optimizer B2B edition. Non è possibile associare un singolo abbonamento Marketo Engage a più di una sandbox AEP. Se non scegli di associare un abbonamento Marketo Engage esistente a Journey Optimizer B2B Edition, ti viene fornito un nuovo abbonamento Marketo Engage vuoto da utilizzare con Journey Optimizer B2B Edition.

Experience Platform fornisce una vista unificata dei dati provenienti dalle istanze di Marketo Engage e dai sistemi CRM associati per agire su tali dati utilizzando un percorso di account.

### Operazioni del percorso di account

I percorsi di account vengono creati in Journey Optimizer B2B Edition e memorizzati nell’istanza Marketo Engage associata all’abbonamento. Anche se sono memorizzati nell’archivio dati di Marketo Engage, non sono visibili dall’interfaccia utente di Marketo Engage e sono utilizzabili solo in Journey Optimizer B2B edition.

Un percorso di account inizia sempre con la selezione di un segmento di account da utilizzare come pubblico di account per il percorso. La selezione del pubblico utilizza il componente standard del selettore del pubblico di Experience Platform. Gli esperti marketing possono quindi implementare il percorso di account suddividendone i percorsi in base ai propri criteri, che possono includere i criteri dell’account, delle persone o del gruppo acquisti. In ogni ramo è possibile eseguire azioni per implementare il percorso, ad esempio inviare un messaggio e-mail o attendere che si verifichi un evento.

Dopo la creazione, il percorso di account deve essere pubblicato. Al momento della pubblicazione, il percorso di account viene convalidato e convertito in una serie di campagne Marketo Engage che implementano l’esperienza di percorso. Data Integration Services viene contattato per avviare il flusso di dati che, a sua volta, avvia le operazioni del percorso dell&#39;account. Il primo passaggio consiste nel creare i segmenti per le persone dell’account.

### Flusso di dati

Journey Optimizer B2B Edition utilizza la segmentazione dell’account Real-Time CDP sia per la definizione che per l’esecuzione dei segmenti dell’account e dei segmenti della persona dell’account correlati, richiesti dai percorsi. Quando viene eseguito un percorso pubblicato, i dati sulle persone e sugli account possono cambiare e vengono raccolti i dati sulle persone che interagiscono con il percorso. Journey Optimizer B2B edition si basa sul connettore di origine di Marketo Engage per consentire a Real-Time CDP B2B edition di riportare le modifiche ai dati alla sandbox di Experience Platform, che è l’origine dati principale.  Questi dati vengono inviati ad AEP quasi in tempo reale.

Solo i tipi di dati esistenti supportati dal connettore di origine di Marketo Engage (account, persone e opportunità) tornano in Real-Time CDP. Ciò significa che i dati del gruppo di acquisto non fluiscono in AEP e risiedono invece nell’istanza Marketo Engage utilizzata dall’abbonamento Journey Optimizer B2B Edition.
