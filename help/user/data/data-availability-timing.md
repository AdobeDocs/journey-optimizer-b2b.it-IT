---
title: Disponibilità dei dati e tempistica di sincronizzazione
description: Scopri la rapidità con cui le modifiche ai dati vengono visualizzate in [!DNL Journey Optimizer B2B Edition] percorsi e quali sequenze temporali sono normali.
feature: Journeys, Data Management
role: User
autotag-review: '2026-10-08T18:36:33.252Z'
TQID: 'https://experienceleague.adobe.com/PA1IeRHnGWHmBtDpffzveoWIHOn99-Ctt4Y0OQb7CwE'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
    internal-label: Journey Optimizer B2B Edition
  - id: edbd1a0e-46c8-49da-8c10-dba9ec80bba9
    internal-label: Experience Platform
  - id: b27e5950-9033-45ac-9f86-eb22e567f615
    internal-label: Marketo Engage
feature_v2:
  - id: 095e8119-1425-57eb-9d8c-9e684f2c9771
    internal-label: Audiences
  - id: 33ca0c14-7e3b-55a1-8fd7-8a61b47da4e1
    internal-label: B2B
  - id: a4b836d9-ffdd-4df3-a62a-f78b830cf059
    internal-label: Journeys
  - id: a50ad69b-1331-40e9-b634-531a085a6a54
    internal-label: Identities
  - id: afadf741-c5fe-42cd-8013-23bb6ff2d1bc
    internal-label: Buying Groups
  - id: beb5f4be-cec3-471a-9db6-831a77dd3ac9
    internal-label: Audiences
  - id: eec185bd-7d60-4193-ba3f-da427569936a
    internal-label: Destinations
  - id: f2da1b69-6919-4386-a5d2-9c7b5c9033db
    internal-label: Data management
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: d378ca77-2da1-4f39-ad92-1917fe974a38
    internal-label: Experienced
topic_v2:
  - id: df401a2a-327d-468c-a5e4-b7b7ccd071a0
    internal-label: Data integration
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
    internal-label: Data management
source-git-commit: 827c313f032d482ac2b0a5fa8f41d6506e67b9cb
workflow-type: tm+mt
source-wordcount: '612'
ht-degree: 0%
---
# Disponibilità dei dati e tempistica di sincronizzazione {#data-availability}

Utilizzare questo argomento per comprendere la velocità con cui le modifiche ai dati vengono visualizzate nei [!DNL Adobe Journey Optimizer B2B Edition] percorsi e quali sequenze temporali sono normali. Conoscere la tempistica prevista consente di progettare i percorsi di conseguenza e di riconoscere il comportamento previsto in caso di ritardo.

## Tempi di attesa previsti

| Tipo di dati | Disponibilità tipica |
| --- | --- |
| [Appartenenza al pubblico](#daily-refresh) | Fino a 24 ore (ciclo giornaliero) |
| [Modifiche alla relazione tra account e persona](#daily-refresh) | Fino a 24 ore (ciclo giornaliero) |
| [Dati da [!DNL Experience Platform] a [!DNL Journey Optimizer B2B Edition]](#platform-sync) | Fino a 30 minuti (quasi in tempo reale) |
| [Dati da [!DNL Journey Optimizer B2B Edition] a [!DNL Experience Platform]](#platform-sync) | Fino a quattro ore (microbatch) |
| [Eventi attività, ad esempio clic e aperture](#activity-and-actions) | Fino a quattro ore |
| [[!DNL Marketo Engage] aggiungi o rimuovi elenco](#activity-and-actions) | Entro 30 minuti (quasi in tempo reale) |
| [Eventi generati da Journey Optimizer B2B Edition](#activity-and-actions) | Utilizzabile solo in tipi di pubblico in batch |
| [Popolazione pubblico LinkedIn](#linkedin-timing) | Stesso giorno a 36-40 ore (caso peggiore) |

## Dati sul pubblico e sulle relazioni {#daily-refresh}

[!DNL Journey Optimizer B2B Edition] valuta l&#39;appartenenza al pubblico dell&#39;account e della persona una volta al giorno, attivata da un modulo di pianificazione dei processi batch. Di conseguenza:

* Gli account o le persone che si qualificano per un pubblico possono accedere a un percorso entro 24 ore dalla qualifica.
* Le modifiche ai criteri di pubblico diventano effettive nel successivo ciclo di valutazione giornaliero.
* Se un account è qualificato per un pubblico oggi ma non è ancora entrato nel percorso, attendi il completamento del ciclo giornaliero successivo prima di eseguire l’indagine.
* Quando l&#39;associazione dell&#39;account di una persona cambia, ad esempio quando un contatto si sposta su un account diverso, l&#39;aggiornamento della relazione si propaga entro 24 ore attraverso il ciclo di sincronizzazione giornaliero. I percorsi che dipendono dall’iscrizione all’account riflettono la relazione aggiornata dopo il successivo ciclo giornaliero. Non è necessaria alcuna azione.

>[!TIP]
>
>Progetta percorsi con la consapevolezza che l’iscrizione al pubblico viene aggiornata ogni giorno, non in tempo reale. Se hai bisogno di risposte quasi in tempo reale, utilizza [trigger basati su eventi](../journeys/listen-for-event-nodes.md) invece di voci basate su pubblico.

## Sincronizzazione dati con [!DNL Experience Platform] {#platform-sync}

[!DNL Experience Platform] è l&#39;archivio dati principale per account, persone e opportunità e [!DNL Journey Optimizer B2B Edition] è proprietario di percorsi, gruppi di acquisto e ruoli dei gruppi di acquisto. [Ulteriori informazioni sull&#39;architettura](../about-journey-optimizer-b2b-edition.md#high-level-architecture).

I dati si spostano tra i due sistemi in entrambe le direzioni a un ritmo diverso:

* Da **[!DNL Experience Platform]a[!DNL Journey Optimizer B2B Edition]** - La sincronizzazione dei dati può richiedere fino a 30 minuti quasi in tempo reale.
* Da **[!DNL Journey Optimizer B2B Edition]a[!DNL Experience Platform]** - I dati vengono sincronizzati in microbatch e possono richiedere fino a 4 ore.

## Eventi attività e azioni percorso {#activity-and-actions}

La tempistica per i dati di attività e le azioni di percorso dipende dal modo in cui i dati si spostano tra i sistemi:

* **Dati attività** - La visualizzazione dei record di attività della persona, ad esempio aperture di e-mail, clic sui collegamenti e riempimenti di moduli, può richiedere circa quattro ore in [!DNL Journey Optimizer B2B Edition]. Questa tempistica si applica ai dati di attività batch; [!DNL Experience Platform] i trigger di Experience Event utilizzano dati in streaming e possono reagire quasi in tempo reale.
* **[!DNL Marketo Engage]azioni** - Le azioni di Percorso che chiamano [!DNL Marketo Engage] sono quasi in tempo reale perché sono chiamate API. Quando ad esempio un passaggio di percorso aggiunge o rimuove una persona da un elenco [!DNL Marketo], l&#39;azione viene in genere completata entro 30 minuti. [Ulteriori informazioni sulle azioni di percorso](../journeys/action-nodes.md).
* **Azioni che passano attraverso[!DNL Experience Platform]**. Qualsiasi azione che ritorni prima a [!DNL Experience Platform] viene eseguita in batch, pertanto è soggetta a temporizzazione in batch anziché in tempo quasi reale.
* **Gli eventi generati da[!DNL Journey Optimizer B2B Edition]** - Gli eventi generati da [!DNL Journey Optimizer B2B Edition] in [!DNL Experience Platform] possono essere utilizzati solo in tipi di pubblico in batch.

## [!DNL LinkedIn] destinazioni pubblico {#linkedin-timing}

Se il percorso include un&#39;azione di destinazione [!DNL LinkedIn], dopo la pubblicazione del percorso è prevista la seguente sequenza temporale.

| Scenario | Attesa prevista |
| --- | --- |
| Gli account erano già nel pubblico quando il percorso è stato pubblicato | Stesso giorno, se l’elaborazione viene completata prima della mezzanotte ora locale |
| Account arrivati dopo la pubblicazione del percorso | Fino a 24 ore |
| Account arrivati dopo la prima finestra di sincronizzazione giornaliera | Fino a 36-40 ore |

[!DNL LinkedIn] conteggi dei pubblici potrebbero non essere aggiornati immediatamente. Questo ritardo è previsto durante l&#39;elaborazione di [!DNL Experience Platform] e la consegna del file del pubblico a [!DNL LinkedIn]. Se il conteggio del pubblico è ancora 0 dopo 48 ore, indagare. [Ulteriori informazioni sui tipi di pubblico corrispondenti all&#39;account LinkedIn](./linkedin-account-matched-audiences.md).
