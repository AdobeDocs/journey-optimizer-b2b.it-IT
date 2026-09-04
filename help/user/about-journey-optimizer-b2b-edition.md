---
title: Panoramica di Adobe Journey Optimizer B2B Edition
description: 'Scopri Adobe Journey Optimizer B2B Edition: orchestra percorsi di account con gruppi acquisti, approfondimenti sull’IA e l’integrazione di Experience Platform per il marketing B2B.'
exl-id: fdfbafdf-826f-44e9-bbb6-5e729d0e18ef
autotag-review: 2026-04-29T23:21:13.339Z
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: f467931a-9b22-4ca8-869f-adfbd64061ce
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: df401a2a-327d-468c-a5e4-b7b7ccd071a0
TQID: https://experienceleague.adobe.com/L58cK4MP-S-8U9fFiXU2qZn4HCieNzjoOaSRCLkyanI
source-git-commit: 8d2fc3ebc7df1674ac9af441679228a9e19d8d5a
workflow-type: tm+mt
source-wordcount: 739
ht-degree: 15%

---

# Panoramica di Adobe Journey Optimizer B2B Edition

Con Adobe Journey Optimizer B2B edition, puoi orchestrare percorsi di persone e account utilizzando l’intelligenza artificiale generativa integrata e l’automazione leader di settore per massimizzare la domanda di offerte specifiche utilizzando gruppi di acquisto qualificati per il marketing.

## Percorsi di account con gruppi di acquisto

Quando si confrontano i percorsi di account con le funzionalità di percorso in Marketo Engage e Adobe Journey Optimizer Standard, la distinzione chiave è che i percorsi di account spostano gli account nel percorso, non le persone. Una persona associata a un account in genere presenta una progressione non lineare basata sull’avanzamento dell’account nel percorso e non sulle singole azioni. Ad esempio, quando un account si trova nella fase iniziale del percorso di acquisto, le informazioni inviate riguardano in genere le funzionalità o le caratteristiche generali della soluzione. Più avanti nel processo di acquisto, il contenuto diventa più mirato su offerte particolari o altri elementi orientati alla chiusura di una vendita. Dopo l’acquisto della soluzione, le informazioni cambiano nuovamente per fornire guide pratiche, best practice, informazioni sui prossimi eventi o contenuti su ulteriori upselling. Anche se un individuo non ha interagito con i contenuti della fase iniziale, puoi farli avanzare alla fase corrente in base alle azioni di altri all’interno del suo account o gruppo di acquisto.

## Architettura di alto livello

Adobe Journey Optimizer B2B edition è basato su Adobe Experience Platform, incluso Real-Time CDP B2B. Journey Optimizer B2B edition e Marketo Engage vengono eseguiti su sistemi separati, ciascuno con un proprio archivio dati. Experience Platform è l’archivio dati principale e la fonte autorevole per account, persone e opportunità. Journey Optimizer B2B edition è il proprietario dei percorsi di account, dei gruppi di acquisto e dei ruoli dei gruppi di acquisto.

Un’istanza dedicata di Marketo Engage supporta ogni abbonamento a Journey Optimizer B2B edition. In questa istanza non vengono memorizzati i percorsi di account, i tipi di pubblico o i gruppi di acquisto. Al contrario, fornisce diritti e servizi di back-end, come la consegna di e-mail, la configurazione del mittente e i domini di branding.

Per supportare le azioni di percorso, puoi anche collegare una o più istanze Marketo Engage esistenti, inclusa l’istanza di produzione. Le azioni di percorso consentono agli addetti al marketing di coordinare i percorsi basati su account in Journey Optimizer B2B edition con campagne basate su lead in Marketo Engage, ad esempio aggiungendo persone a un elenco o a una campagna di richieste. [Ulteriori informazioni sulla connessione delle istanze di Marketo Engage](./admin/marketo-actions-connect.md).

![Architettura dei dati di alto livello che mostra Journey Optimizer B2B edition connesso a Adobe Experience Platform come fonte di verità per il pubblico di utenti e account, un&#39;istanza Marketo Engage dedicata che fornisce servizi di adesione e back-end e un&#39;istanza Marketo Engage di produzione facoltativa utilizzata per eseguire azioni di percorso.](./assets/high-level-data-architecture.png){zoomable="yes"}

>[!NOTE]
>
>Controlla i diritti delle licenze e la corrispondente [descrizione del prodotto](https://helpx.adobe.com/it/legal/product-descriptions/adobe-journey-optimizer-b2b.html){target="_blank"} per i guardrail delle prestazioni e le limitazioni statiche.

### Modello di abbonamento

Una sandbox di Experience Platform associata a un’istanza Marketo Engage dedicata definisce un abbonamento a Journey Optimizer B2B edition. Questa istanza dedicata è separata dall’istanza Marketo Engage di produzione ed esiste per supportare diritti e servizi back-end anziché archiviare i dati del percorso dell’account. [Ulteriori informazioni sulla configurazione](./setup-ultimate.md).

Experience Platform fornisce una visualizzazione unificata dei dati provenienti dalle istanze Marketo Engage e dai sistemi di gestione delle relazioni con i clienti connessi. Utilizza questi dati unificati per generare ed eseguire i percorsi.

### Operazioni di percorso

Journey Optimizer B2B edition crea, archivia ed esegue i percorsi di account. I percorsi di account non vengono visualizzati in Marketo Engage e sono utilizzabili solo in Journey Optimizer B2B edition.

Un percorso inizia sempre con un pubblico che qualifica i lead o gli account e le loro persone per il percorso. Seleziona questo pubblico utilizzando il selettore di pubblico standard di Experience Platform. Gli addetti al marketing implementano il percorso suddividendo i percorsi in base ai criteri dell’account, delle persone o dei gruppi di acquisto. In ogni percorso, le azioni inviano comunicazioni o attendono che si verifichi un evento.

Dopo aver creato un percorso di account, pubblicalo per renderlo attivo. I conti idonei inseriscono un percorso pubblicato entro 24 ore.

### Flusso di dati

Journey Optimizer B2B edition funziona come destinazione di Adobe Real-Time CDP B2B edition. Utilizza la segmentazione degli account di Real-Time CDP per creare e valutare i tipi di pubblico degli account e delle persone che qualificano account e persone per un percorso. Quando pubblichi un percorso, Journey Optimizer B2B edition attiva i tipi di pubblico idonei da Experience Platform.

I gruppi di acquisto, i ruoli dei gruppi di acquisto e i punteggi dei gruppi di acquisto vengono creati e memorizzati in Journey Optimizer B2B edition. [Ulteriori informazioni sull&#39;acquisto di gruppi](./buying-groups/buying-groups-overview.md).
