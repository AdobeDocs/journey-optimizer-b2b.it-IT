---
title: Utilizzare Experience Manager Assets
description: Scopri come utilizzare le risorse di immagini da un archivio AEM Assets connesso durante l’authoring dei contenuti in Adobe Journey Optimizer B2B Edition.
feature: Assets, Content
exl-id: c6864981-209c-4123-8d3f-24deb07026a0
source-git-commit: 7103e4f6666482a72511661dfaed1392d4eb16b1
workflow-type: tm+mt
source-wordcount: '646'
ht-degree: 1%

---

# Utilizzare risorse Experience Manager

Quando Adobe Experience Manager Assets as a Cloud Service è integrato con Adobe Journey Optimizer B2B Edition, puoi individuare e accedere facilmente alle risorse digitali da utilizzare nei contenuti di marketing. Quando crei i contenuti, le risorse sono accessibili dall&#39;elemento _[!UICONTROL Assets]_ nell&#39;area di navigazione a sinistra e quando crei contenuti e-mail per un percorso di account. Puoi anche caricare le risorse nell’archivio as a Cloud Service di AEM Assets connesso direttamente da Adobe Journey Optimizer B2B Edition.

>[!NOTE]
>
>Attualmente, in Adobe Journey Optimizer B2B Edition sono supportate solo le risorse di immagini di Adobe Experience Manager Assets. Le modifiche alle risorse devono essere effettuate dall’archivio centrale di Adobe Experience Manager Assets. [Ulteriori informazioni](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/manage-digital-assets)

Quando utilizzi queste risorse digitali, le modifiche più recenti apportate in Assets as a Cloud Service si propagano automaticamente alle campagne e-mail live tramite riferimenti collegati. Se le immagini vengono eliminate in Adobe Experience Manager Assets as a Cloud Service, nelle e-mail vengono visualizzate con un riferimento non funzionante. Quando le risorse attualmente utilizzate nei percorsi di account vengono modificate o eliminate, gli autori del percorso ricevono una notifica sulle modifiche apportate all’immagine e sull’elenco dei percorsi che la utilizzano. Tutte le modifiche apportate alle risorse devono essere effettuate nell’archivio centrale di Adobe Experience Manager Assets.

## Utilizza AEM Assets come origine dell’immagine

Se nell&#39;ambiente sono presenti una o più connessioni a [archivi Assets](../admin/configure-aem-repositories.md), è possibile designare AEM Assets come origine per le risorse quando si creano o si visualizzano i dettagli di un messaggio e-mail, un modello e-mail o un frammento visivo.

* Quando crei un nuovo contenuto, scegli `AEM Assets` come elemento **[!UICONTROL Image Source]** nella finestra di dialogo.

  ![Seleziona AEM Assets come origine immagine nella finestra di dialogo per la creazione](./assets/create-dialog-aem-assets.png){width="400"}

* Quando apri una risorsa di contenuto esistente, scegli `AEM Assets` nel pannello _[!UICONTROL Corpo]_ a destra.

  ![Seleziona AEM Assets come origine immagine nelle proprietà](./assets/content-source-aem-assets.png){width="700" zoomable="yes"}

## Accedere alle risorse per la creazione

>[!IMPORTANT]
>
>Un amministratore deve aggiungere gli utenti che hanno bisogno di accedere ad Assets ai profili di prodotto Utenti consumer di Assets e Utenti di Assets. [Ulteriori informazioni](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/security/ims-support#managing-products-and-user-access-in-admin-console)

Nell&#39;editor di contenuti visivi, fai clic sull&#39;icona _Selettore risorse_ nella barra laterale a sinistra. In questo modo il pannello strumenti diventa un elenco delle risorse disponibili nell’archivio selezionato.

![Fai clic sull&#39;icona del selettore Assets per accedere alle risorse immagine](./assets/content-assets-selector-aem-assets.png){width="700" zoomable="yes"}

Se sono presenti più repository AEM connessi, fare clic sulla freccia del menu relativa a **[!UICONTROL Repository]** per scegliere il repository che si desidera utilizzare.

![Scegli un archivio AEM Assets per accedere alle risorse immagine](./assets/content-assets-selector-aem-repo.png){width="700" zoomable="yes"}

Esistono diversi metodi per aggiungere una risorsa immagine all’area di lavoro visiva:

* Trascina e rilascia la miniatura di un’immagine dal menu di navigazione a sinistra.

  ![Scegli un archivio AEM Assets per accedere alle risorse immagine](./assets/content-drag-drop-image-aem-assets.png){width="700" zoomable="yes"}

* Aggiungi un componente immagine all&#39;area di lavoro e fai clic su **[!UICONTROL Sfoglia]** per aprire la finestra di dialogo _[!UICONTROL Seleziona Assets]_.

  Dalla finestra di dialogo, puoi scegliere un’immagine dall’archivio selezionato.

  Sono disponibili diversi strumenti per aiutarti a individuare la risorsa di cui hai bisogno.

  ![usa lo strumento nella finestra di dialogo Seleziona Assets per trovare e selezionare una risorsa immagine](./assets/content-select-assets-dialog-aem.png){width="700" zoomable="yes"}

   * Modifica l&#39;**[!UICONTROL Archivio]** in alto a destra.

   * Fai clic su **[!UICONTROL Gestisci risorse]** in alto a destra per aprire l&#39;archivio Assets in un&#39;altra scheda del browser e utilizzare gli strumenti di gestione AEM Assets.

   * Fai clic sul selettore _Tipo di visualizzazione_ in alto a destra per modificare la visualizzazione in **[!UICONTROL Vista a elenco]**, **[!UICONTROL Vista griglia]**, **[!UICONTROL Vista galleria]** o **[!UICONTROL Vista a cascata]**.

   * Fai clic sull&#39;icona _Ordinamento_ per modificare l&#39;ordinamento tra crescente e decrescente.

   * Fare clic sulla freccia del menu **[!UICONTROL Ordina per]** per modificare i criteri di ordinamento in **[!UICONTROL Nome]**, **[!UICONTROL Dimensione]** o **[!UICONTROL Modificato]**.

   * Fai clic sull&#39;icona _Filtro_ in alto a sinistra per filtrare gli elementi visualizzati in base ai criteri.

   * Immetti il testo da cercare nel campo Ricerca per filtrare gli elementi visualizzati in modo che corrispondano al nome della risorsa.

  ![Utilizza i filtri e il campo di ricerca per individuare la risorsa](./assets/content-select-assets-dialog-aem-filter.png){width="700" zoomable="yes"}

<!-- 
## Upload assets

To import files to Assets as a Cloud Service, you first need to browse or create the folder to be used for storage. You can then import an asset and add it to your email content. After assets are uploaded, you can [use the image assets as you author content](./assets-overview.md#add-assets-to-your-content).

1. While authoring your content in the email designer, drag an image element into the canvas. 

   The properties on the right reflect the image element selection. 

1. Click **[!UICONTROL Import media]** to open the _[!UICONTROL Upload image]_ dialog.

1. If your file system is open to your image file, drag and drop the file on the box in the dialog.

   ![Upload image file to Assets repository](./assets/email-designer-image-upload.png){width="700" zoomable="yes"}

   You can also click the **[!UICONTROL Select a file from your computer]** link and use your file system to locate and select the image file. Click Open and the image file is displayed in the box.

1. Click **[!UICONTROL Import]**.

-->
