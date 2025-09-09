---
title: Utilizzare Experience Manager Assets
description: 'Accedi e utilizza le immagini AEM Assets nell’authoring dei contenuti: trascina e rilascia, cerca, filtra e sincronizza automaticamente le modifiche in Journey Optimizer B2B edition.'
feature: Assets, Content, Integrations
role: User
exl-id: c6864981-209c-4123-8d3f-24deb07026a0
source-git-commit: 79012352c3ae4e2f3d38b632b1f523d262f74f96
workflow-type: tm+mt
source-wordcount: '560'
ht-degree: 2%

---

# Utilizzare le risorse di Experience Manager

Quando [!DNL Adobe Experience Manager Assets as a Cloud Service] è integrato con [!DNL Adobe Journey Optimizer B2B Edition], è possibile individuare e accedere facilmente alle risorse digitali da utilizzare nei contenuti di marketing. Mentre crei i contenuti, le risorse sono accessibili dall&#39;elemento _[!UICONTROL Experience Manager Assets]_ nell&#39;area di navigazione a sinistra e durante l&#39;authoring dei contenuti e-mail per un percorso di account.

{{aem-assets-licensing-note}}

Quando si utilizzano queste risorse digitali, le modifiche più recenti in [!DNL Assets as a Cloud Service] si propagano automaticamente alle campagne e-mail live tramite riferimenti collegati. Se le immagini vengono eliminate in [!DNL Adobe Experience Manager Assets as a Cloud Service], le immagini vengono visualizzate con un riferimento interrotto nelle e-mail. Quando le risorse attualmente utilizzate nei percorsi di account vengono modificate o eliminate, gli autori del percorso ricevono una notifica sulle modifiche apportate all’immagine e sull’elenco dei percorsi che la utilizzano. Tutte le modifiche apportate alle risorse devono essere eseguite nell&#39;archivio centrale [!DNL Adobe Experience Manager Assets].

Se nell&#39;ambiente sono presenti una o più connessioni a [archivi Assets](../admin/configure-aem-repositories.md), gli autori di contenuto possono utilizzare [!DNL Experience Manager Assets] come origine per le risorse durante la creazione di un messaggio e-mail, un modello e-mail o un frammento visivo.

>[!IMPORTANT]
>
>Un amministratore deve aggiungere gli utenti che hanno bisogno di accedere ad Assets ai profili di prodotto Utenti consumer di Assets e Utenti di Assets. [Ulteriori informazioni](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/security/ims-support#managing-products-and-user-access-in-admin-console){target="_blank"}

## Accedere alle immagini di AEM Assets

Nello spazio di progettazione del contenuto, fai clic sull&#39;icona _[!UICONTROL Experience Manager Assets]_ ( ![icona Experience Manager Assets](../../assets/do-not-localize/icon-assets-aem.svg) ) nella barra laterale a sinistra. In questo modo il pannello strumenti diventa un elenco delle risorse disponibili nell’archivio selezionato.

![Fai clic sull&#39;icona del selettore Assets per accedere alle risorse immagine](./assets/content-assets-selector-aem-assets.png){width="700" zoomable="yes"}

>[!NOTE]
>
>Attualmente, in [!DNL Adobe Experience Manager Assets] sono supportate solo le risorse immagine di [!DNL Adobe Journey Optimizer B2B Edition]. Le modifiche alle risorse devono essere eseguite dall&#39;archivio centrale [!DNL Adobe Experience Manager Assets]. [Ulteriori informazioni](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/assets/manage/manage-digital-assets){target="_blank"}

### Modificare l’archivio visualizzato

Se sono presenti più repository AEM connessi, fare clic sulla freccia del menu per **[!UICONTROL Repository]** per scegliere il repository che si desidera visualizzare nel pannello sinistro.

![Scegli un archivio AEM Assets per accedere alle risorse immagine](./assets/content-assets-selector-aem-repo.png){width="700" zoomable="yes"}

Esistono diversi metodi per aggiungere una risorsa immagine all’area di lavoro visiva.

### Trascina un’immagine

1. Sfoglia le miniature delle immagini visualizzate nel pannello a sinistra.

1. Trascina la miniatura dell’immagine e rilasciala nell’area di lavoro, per aggiungere il nuovo componente immagine.

   ![Trascina una risorsa immagine](./assets/content-drag-drop-image-aem-assets.png){width="700" zoomable="yes"}

## Trovare e selezionare un&#39;immagine

1. Aggiungi un componente immagine all&#39;area di lavoro e fai clic su **[!UICONTROL Experience Manager Assets]** per aprire la finestra di dialogo _[!UICONTROL Seleziona Assets]_.

   ![Seleziona una risorsa per il componente immagine](./assets/content-image-component-empty.png){width="600" zoomable="yes"}

1. Dalla finestra di dialogo, scegli un’immagine utilizzando gli strumenti disponibili per individuare la risorsa necessaria:

   * Modifica l&#39;**[!UICONTROL Archivio]** in alto a destra.

   * Fai clic su **[!UICONTROL Gestisci risorse]** in alto a destra per aprire l&#39;archivio Assets in un&#39;altra scheda del browser e utilizzare gli strumenti di gestione AEM Assets.

   * Fai clic sul selettore _Tipo di visualizzazione_ in alto a destra per modificare la visualizzazione in **[!UICONTROL Vista a elenco]**, **[!UICONTROL Vista griglia]**, **[!UICONTROL Vista galleria]** o **[!UICONTROL Vista a cascata]**.

   * Fai clic sull&#39;icona _Ordinamento_ per modificare l&#39;ordinamento tra crescente e decrescente.

     ![Utilizzare gli strumenti nella finestra di dialogo Seleziona Assets per trovare e selezionare una risorsa immagine](./assets/content-select-assets-dialog-aem.png){width="700" zoomable="yes"}

   * Fare clic sulla freccia del menu **[!UICONTROL Ordina per]** per modificare i criteri di ordinamento in **[!UICONTROL Nome]**, **[!UICONTROL Dimensione]** o **[!UICONTROL Modificato]**.

   * Fai clic sull&#39;icona _Filtro_ in alto a sinistra per filtrare gli elementi visualizzati in base ai criteri.

   * Immetti il testo da cercare nel campo Ricerca per filtrare gli elementi visualizzati in modo che corrispondano al nome della risorsa.

   ![Utilizza i filtri e il campo di ricerca per individuare la risorsa](./assets/content-select-assets-dialog-aem-filter.png){width="700" zoomable="yes"}

1. Fai clic su **[!UICONTROL Seleziona]**.
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
