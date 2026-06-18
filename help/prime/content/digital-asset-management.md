---
title: Risorse
description: Gestisci le risorse immagine da Journey Optimizer B2B edition per e-mail, modelli e frammenti visivi.
feature: Assets, Content
role: User
badge: label="Beta" type="Informative"
autotag-review: '2026-06-18T20:11:57.611Z'
TQID: 'https://experienceleague.adobe.com/Xsl4zqpk4xqXuOS85Z5U08tnbv8GWm3FXdqsegPCBI4'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: e666e996-b2cf-4c45-8fc2-1c625212abab
  - id: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2:
  - id: c8402946-ff35-44c5-ab98-74c1bba0975f
  - id: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 0e90250101eef0572af0382cc7d24bca727d2b75
workflow-type: tm+mt
source-wordcount: 495
ht-degree: 3%

---

# Risorse

In [!DNL Adobe Journey Optimizer B2B Prime], le risorse sono in genere le immagini utilizzate durante la progettazione del contenuto per supportare i percorsi. Puoi utilizzare queste immagini nelle e-mail, nei modelli e nei frammenti visivi dal selettore delle risorse o tramite una semplice interfaccia a trascinamento all’interno dello spazio di progettazione visiva.

Formati di file supportati: JPG, JPEG, GIF, PNG, EPS, SVG e RGB


&#x200B;>>
L’importazione di risorse da sistemi esterni, come Marketo Engage DAM, e l’accesso a una libreria di risorse precompilata non sono ancora disponibili. Le versioni future dovrebbero includere l’importazione delle risorse dai sistemi esistenti, il supporto delle cartelle e funzionalità estese di gestione delle risorse.

<!-- You can [edit these assets using Adobe Express](./image-edit-adobe-express.md), and move them into folders to organize them for use across your emails, templates, and fragments. -->

La libreria **Assets** fornisce l&#39;accesso all&#39;archivio centralizzato per l&#39;archiviazione e la gestione delle immagini e di altre risorse creative. Include funzionalità basate sull’intelligenza artificiale che generano automaticamente metadati e consentono la ricerca in linguaggio naturale.

Nel menu di navigazione a sinistra, espandi **[!UICONTROL Gestione contenuto]** e seleziona **[!UICONTROL Assets]**.

>[!NOTE]
>
>In questa versione di Beta, puoi scegliere immagini e risorse da una copia unica della libreria di risorse Marketo Engage direttamente nell’area di lavoro delle e-mail. È inoltre possibile caricare risorse immagine aggiuntive dalla libreria _[!UICONTROL Assets]_ o dallo spazio di progettazione dei contenuti. Queste risorse caricate sono disponibili per l&#39;utilizzo solo nell&#39;istanza [!DNL Adobe Journey Optimizer B2B Prime].

![Libreria Assets](./assets/dam-asset-library-list-view.png){width="800" zoomable="yes"}

>[!BEGINSHADEBOX]

La prima volta che accedi alla libreria _[!UICONTROL Assets]_, rivedi le _[!UICONTROL Condizioni d&#39;uso Generative AI]_ e fai clic su **[!UICONTROL Accetto e continua]**.

![Libreria Assets](./assets/dam-asset-library-gen-ai-agree.png){width="500"}

>[!ENDSHADEBOX]

La libreria supporta due opzioni di layout:

* **[!UICONTROL Elenco]** — Fai clic sull&#39;icona _Vista a elenco_ ( ![Icona Vista a elenco](../../assets/do-not-localize/icon-falco-list-view.svg) ) per visualizzare le risorse in una tabella ordinabile con colonne di metadati.
* **[!UICONTROL Galleria]** — Fai clic sull&#39;icona _Visualizzazione Raccolta_ ( ![Icona Visualizzazione Raccolta](../../assets/do-not-localize/icon-falco-gallery-view.svg) ) per visualizzare le risorse come griglia di miniature visiva.

## Cercare risorse {#find-assets}

Utilizza il campo _[!UICONTROL Cerca]_ per trovare le risorse descrivendo cosa ti serve in linguaggio naturale. I risultati della ricerca si basano su metadati generati dall’intelligenza artificiale, pertanto non sei limitato alla ricerca per nome file.

**Esempi:**

* `team members`
* `nature`
* `exercise`

![Immagine selezionata dai risultati di ricerca nella libreria Assets](./assets/dam-asset-library-select-image.png){width="700" zoomable="yes"}

## Visualizza dettagli risorsa {#view-details}

Seleziona una risorsa per aprirne la vista dei dettagli. La vista dei dettagli visualizza una descrizione generata dall’intelligenza artificiale, tag e parole chiave e campi di metadati aggiuntivi. Queste informazioni vengono generate automaticamente al caricamento della risorsa.

Seleziona una risorsa nella vista a elenco o a galleria per aprirne la vista dei dettagli a destra. Seleziona la scheda metadati IA per visualizzare la descrizione, i tag e i metadati generati dall’intelligenza artificiale.

![Immagine selezionata dai risultati di ricerca nella libreria Assets](./assets/dam-asset-library-select-image-metadata.png){width="700" zoomable="yes"}

## Caricare una risorsa {#upload}

1. Fai clic su **[!UICONTROL Carica]** in alto a destra.

1. Nella finestra di dialogo, trascina e rilascia un file dal sistema locale.

   ![Carica una risorsa immagine](./assets/dam-upload-assets-dialog.png){width="450"}

   In alternativa, è possibile fare clic su **[!UICONTROL Seleziona file dal computer]** per utilizzare il file system locale per individuare e selezionare il file.

1. Fare clic su **[!UICONTROL Carica file]** per confermare e caricare il file nel repository.

Al termine del caricamento, il sistema genera automaticamente una descrizione, assegna tag e parole chiave ed estrae attributi visivi come l’oggetto e l’impostazione. Non è richiesta alcuna assegnazione tag manuale. La nuova immagine viene visualizzata con lo stato _[!UICONTROL ELABORAZIONE]_ fino al completamento del processo.

![Nuova risorsa immagine in elaborazione](./assets/dam-asset-library-upload-processing.png){width="700" zoomable="yes"}
<!-- -->
