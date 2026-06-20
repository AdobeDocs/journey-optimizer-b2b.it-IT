---
title: Risorse
description: Gestisci le risorse immagine da Journey Optimizer B2B Prime per e-mail, modelli e frammenti visivi.
feature: Assets, Content
role: User
badgeBeta: label="Beta" type="informative" tooltip="Questa funzione fa parte di una versione beta limitata."
autotag-review: '2026-06-18T20:11:57.611Z'
TQID: 'https://experienceleague.adobe.com/Xsl4zqpk4xqXuOS85Z5U08tnbv8GWm3FXdqsegPCBI4'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: e666e996-b2cf-4c45-8fc2-1c625212ababid: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2: id: c8402946-ff35-44c5-ab98-74c1bba0975fid: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 1894dc537653c08a3e8d10cde14bd651f206d946
workflow-type: tm+mt
source-wordcount: 786
ht-degree: 18%

---

# Risorse

In [!DNL Adobe Journey Optimizer B2B Prime], le risorse sono in genere le immagini utilizzate durante la progettazione del contenuto per supportare i percorsi. Puoi utilizzare queste immagini nei tuoi [messaggi e-mail](email-authoring.md), [modelli e-mail](templates.md) e [frammenti visivi](email-authoring.md#visual-fragments) dal selettore risorse o da una semplice interfaccia a trascinamento all&#39;interno dello spazio di progettazione visiva.

Formati di file supportati: JPG, JPEG, GIF, PNG, EPS, SVG e RGB

>[!NOTE]
>
>In questa versione di Beta, puoi scegliere immagini e risorse da una copia unica della libreria di risorse Marketo Engage direttamente nell’area di lavoro delle e-mail. La modifica delle risorse in Marketo Engage dopo la copia iniziale è **not** riflessa in [!DNL Journey Optimizer B2B Prime].
>
>È possibile caricare risorse immagine aggiuntive dalla libreria _[!UICONTROL Assets]_ o dallo spazio di progettazione dei contenuti. Queste risorse caricate sono disponibili per l&#39;utilizzo solo nell&#39;istanza [!DNL Journey Optimizer B2B Prime].
>
>L’importazione di risorse da sistemi esterni e l’accesso a una libreria di risorse precompilata non sono ancora disponibili. Le versioni future dovrebbero includere l’importazione delle risorse dai sistemi esistenti, il supporto delle cartelle e funzionalità estese di gestione delle risorse.

<!-- You can [edit these assets using Adobe Express](./image-edit-adobe-express.md), and move them into folders to organize them for use across your emails, templates, and fragments. -->

La libreria **Assets** fornisce l&#39;accesso all&#39;archivio centralizzato per l&#39;archiviazione e la gestione delle immagini e di altre risorse creative. Include funzionalità basate sull’intelligenza artificiale che generano automaticamente metadati e consentono la ricerca in linguaggio naturale.

Nel menu di navigazione a sinistra, espandi **[!UICONTROL Gestione contenuto]** e seleziona **[!UICONTROL Assets]**.

![Visualizzazione elenco librerie Assets con colonne di metadati ordinabili](./assets/dam-asset-library-list-view.png){width="800" zoomable="yes"}

>[!BEGINSHADEBOX]

La prima volta che accedi alla libreria _[!UICONTROL Assets]_, rivedi le [_[!UICONTROL Condizioni d&#39;uso generative per l&#39;intelligenza artificiale ]_](https://www.adobe.com/it/legal/licenses-terms/adobe-gen-ai-user-guidelines.html) e conferma il tuo contratto.

![Finestra di dialogo del contratto Generative AI Terms of Use nella libreria Assets](./assets/dam-asset-library-gen-ai-agree.png){width="500"}

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

Seleziona una risorsa nella vista a elenco o a galleria per aprirne la vista dei dettagli a destra, che mostra una descrizione generata dall’intelligenza artificiale, tag, parole chiave e campi di metadati aggiuntivi. Queste informazioni vengono generate automaticamente al caricamento della risorsa. Seleziona la scheda **[!UICONTROL Metadati IA]** per rivedere la descrizione, i tag e i metadati generati.

![Visualizzazione dettagli risorsa con metadati e tag generati da IA](./assets/dam-asset-library-select-image-metadata.png){width="700" zoomable="yes"}

## Caricare una risorsa {#upload}

1. Fai clic su **[!UICONTROL Carica]** in alto a destra.

1. Nella finestra di dialogo, trascina e rilascia un file dal sistema locale.

   ![Carica una risorsa immagine](./assets/dam-upload-assets-dialog.png){width="450"}

   In alternativa, è possibile fare clic su **[!UICONTROL Seleziona file dal computer]** per utilizzare il file system locale per individuare e selezionare il file.

1. Fare clic su **[!UICONTROL Carica file]** per confermare e caricare il file nel repository.

Al termine del caricamento, il sistema genera automaticamente una descrizione, assegna tag e parole chiave ed estrae attributi visivi come l’oggetto e l’impostazione. Non è richiesta alcuna assegnazione tag manuale. La nuova immagine viene visualizzata con lo stato _[!UICONTROL ELABORAZIONE]_ fino al completamento del processo.

![Nuova risorsa immagine in elaborazione](./assets/dam-asset-library-upload-processing.png){width="700" zoomable="yes"}

## Utilizzare le risorse per l’authoring dei contenuti {#assets-authoring}

Utilizza le risorse durante l’authoring di e-mail, modelli di e-mail e frammenti visivi. L&#39;editor del contenuto visivo fornisce l&#39;accesso alle immagini nella libreria _Assets_. Puoi anche caricare una risorsa di immagine, che la inserisce nell’archivio delle risorse interno.

Puoi scegliere la risorsa immagine quando modifichi le impostazioni per un componente immagine o direttamente sull’area di lavoro:

* **_Componente vuoto_** - Quando si aggiunge un componente immagine all&#39;area di lavoro, questo è vuoto e consente di scegliere o importare facilmente un file di immagine.

  ![Scegliere un’origine per selezionare un file di immagine per il componente immagine vuoto](./assets/dam-assets-image-component-empty.png){width="500"}

* **_Barra degli strumenti del componente immagine_** - Se nell&#39;area di lavoro è selezionato un componente immagine, la barra degli strumenti consente di scegliere facilmente un&#39;origine e selezionare il file immagine.

  ![Utilizzare la barra degli strumenti per la scelta dell’origine da cui selezionare un file di immagine per il componente immagine](./assets/dam-assets-image-toolbar-settings.png){width="500"}

* **_Impostazioni del componente immagine_** - Se nell&#39;area di lavoro è selezionato un componente immagine, è possibile visualizzare e modificare le impostazioni nel pannello di destra. Per aggiungere o modificare il file immagine visualizzato nel componente, scegli il tipo di origine e seleziona un file di immagine.

  ![Modifica le impostazioni del componente immagine nel pannello a destra](./assets/dam-assets-image-settings.png){width="350"}

Fai clic su **[!UICONTROL Seleziona risorsa]** per aprire il selettore risorse, in cui puoi scegliere un&#39;immagine dall&#39;archivio risorse [!DNL Journey Optimizer B2B Prime].

![Seleziona una risorsa immagine](./assets/dam-assets-internal-image-selected.png){width="700" zoomable="yes"}

Puoi utilizzare la ricerca e i filtri per individuare la risorsa immagine desiderata. Seleziona la risorsa e fai clic su **[!UICONTROL Seleziona]** per utilizzarla per il componente immagine.

Puoi anche scegliere una risorsa immagine nelle impostazioni dello sfondo di un componente struttura.
