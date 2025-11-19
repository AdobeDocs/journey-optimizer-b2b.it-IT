---
title: Risorse
description: Gestisci le risorse immagine da Journey Optimizer B2B edition e AEM Assets per e-mail, modelli e frammenti.
feature: Assets, Content
role: User
exl-id: f3848e65-3196-4d1f-90cf-7aa6ceeafabb
source-git-commit: 1c5a08b293db9287d03b103d794cc17a1c186af0
workflow-type: tm+mt
source-wordcount: '852'
ht-degree: 60%

---

# Risorse

In [!DNL Adobe Journey Optimizer B2B Edition], le risorse sono in genere le immagini utilizzate durante la progettazione di contenuti per supportare percorsi account. Puoi utilizzare queste immagini nelle e-mail, nei modelli e nei frammenti di e-mail dal selettore delle risorse o da una semplice interfaccia a trascinamento all’interno dello spazio di progettazione visiva.

[!DNL Journey Optimizer B2B Edition] offre ai designer e agli addetti al marketing l&#39;accesso a due tipi di librerie di risorse: un archivio risorse [!DNL Journey Optimizer B2B Edition] interno e [!DNL Adobe Experience Manager Assets as a Cloud Service]. È possibile utilizzare solo l&#39;archivio incorporato o entrambi i tipi di libreria contemporaneamente (in base alla licenza [!DNL Experience Manager Assets] di cui si dispone).

## Gestione delle risorse

Se è stato eseguito il provisioning con [!DNL Adobe Experience Manager as a Cloud Services] ed è configurato come origine risorsa in [!DNL Journey Optimizer B2B Edition], è possibile accedere a entrambi i tipi di repository quando l&#39;account utente dispone delle autorizzazioni necessarie. Questi archivi sono separati e non sincronizzati. È possibile utilizzare immagini da entrambe le origini.

### Risorse interne

Per impostazione predefinita, l&#39;archivio risorse interno viene fornito con ogni sottoscrizione [!DNL Journey Optimizer B2B Edition]. Ciò significa che si dispone dell&#39;accesso a qualsiasi risorsa immagine memorizzata nel file system di risorse [!DNL Adobe Marketo Engage] connesso. Puoi utilizzare questo archivio come libreria locale di risorse, inclusa la possibilità di caricare e scaricare risorse. Puoi anche utilizzare queste risorse all’interno del contenuto del percorso.

Puoi [modificare queste risorse utilizzando Adobe Express](./image-edit-adobe-express.md) e spostarle in cartelle per organizzarle per l&#39;utilizzo nelle e-mail, nei modelli e nei frammenti.

Formati di file supportati: JPG, JPEG, GIF, PNG, EPS, SVG e RGB

### Adobe Experience Manager Assets as a Cloud Service

Riunisci flussi di lavoro creativi e di marketing utilizzando [!DNL Adobe Experience Manager Assets]. È integrato in modo nativo con [!DNL Journey Optimizer B2B Edition], per consentirti di accedere facilmente ad Assets as a Cloud Service per scoprire e utilizzare le risorse digitali. Fornisce l’accesso al tuo archivio di risorse da utilizzare per compilare i messaggi.

[!DNL Adobe Journey Optimizer B2B Edition] può connettersi a [!DNL Adobe Experience Manager Assets as a Cloud Service] per la gestione centralizzata delle risorse che estende il tuo sistema creativo e unifica le risorse digitali per la distribuzione delle esperienze. [!DNL Adobe Experience Manager Assets as a Cloud Service] offre una soluzione cloud di facile utilizzo per la gestione efficiente delle risorse digitali e le operazioni Dynamic Media. Incorpora perfettamente funzioni avanzate, tra cui l’intelligenza artificiale e l’apprendimento automatico.

Ulteriori informazioni nella [documentazione di Adobe Experience Manager as a Cloud Service](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/assets/overview){target="_blank"}.

{{aem-assets-licensing-note}}

Accedi a [!DNL Adobe Experience Manager Assets] direttamente all’interno di [!DNL Journey Optimizer B2B Edition] dall’elemento **[!UICONTROL Experience Manager Assets]** nella navigazione a sinistra della progettazione dei contenuti. Puoi anche accedere alle risorse e alle cartelle durante la progettazione di e-mail, modelli e-mail e contenuti di frammenti visivi.

Attualmente, in Adobe Journey Optimizer B2B Edition è possibile utilizzare solo immagini di Adobe Experience Manager Assets.

## Utilizzare le risorse per l’authoring dei contenuti

Utilizza le risorse durante l’authoring di e-mail, modelli di e-mail e frammenti visivi. L’editor di contenuti visivi consente di accedere alle immagini negli archivi delle risorse collegate. Se disponi anche di una sottoscrizione per Experience Manager Assets as a Cloud Service, puoi scegliere le risorse immagine da entrambe le origini. Puoi anche caricare una risorsa di immagine, che la inserisce nell’archivio delle risorse interno.

Puoi scegliere l’origine dell’immagine quando modifichi le impostazioni di un componente immagine o direttamente nell’area di lavoro.

* **_Impostazioni del componente immagine_** - Se nell&#39;area di lavoro è selezionato un componente immagine, è possibile visualizzare e modificare le impostazioni nel pannello di destra. Per aggiungere o modificare il file immagine visualizzato nel componente, scegli il tipo di origine e seleziona un file di immagine.

  ![Modifica le impostazioni del componente immagine nel pannello a destra](./assets/content-assets-image-settings.png){width="350"}

* **_Componente vuoto_** - Quando si aggiunge un componente immagine all&#39;area di lavoro, questo è vuoto e consente di scegliere facilmente un&#39;origine e selezionare un file di immagine.

  ![Scegliere un’origine per selezionare un file di immagine per il componente immagine vuoto](./assets/content-assets-image-component-empty.png){width="500"}

* **_Barra degli strumenti del componente immagine_** - Se nell&#39;area di lavoro è selezionato un componente immagine, la barra degli strumenti consente di scegliere facilmente un&#39;origine e selezionare il file immagine.

  ![Utilizzare la barra degli strumenti per la scelta dell’origine da cui selezionare un file di immagine per il componente immagine](./assets/content-assets-image-toolbar-settings.png){width="500"}

Puoi aggiungere una risorsa immagine, a seconda dell’origine, mentre esegui l’authoring del contenuto. Puoi anche scegliere una risorsa immagine nelle impostazioni dello sfondo di un componente struttura.

>[!BEGINTABS]

>[!TAB Seleziona risorsa]

Fai clic su **[!UICONTROL Seleziona risorsa]** per aprire il selettore risorse, in cui puoi scegliere un&#39;immagine dall&#39;archivio risorse di Journey Optimizer B2B edition.

![Seleziona una risorsa immagine](./assets/content-assets-internal-image-selected.png){width="700" zoomable="yes"}

Puoi utilizzare la ricerca e i filtri per individuare la risorsa immagine desiderata. Seleziona la risorsa e fai clic su **[!UICONTROL Seleziona]** per utilizzarla per il componente immagine.

Per informazioni più dettagliate sull&#39;utilizzo di risorse immagine interne, consulta [Utilizzare risorse nel contenuto](./internal-image-assets.md#use-assets-in-your-content).

>[!TAB Experience Manager Assets]

Fai clic su **[!UICONTROL Experience Manager Assets]** per aprire il selettore risorse, dove puoi scegliere un’immagine dall’archivio Experience Manager Assets.

![Selezionare una risorsa immagine dall’archivio di AEM Assets](./assets/content-assets-image-aem-selected.png){width="700" zoomable="yes"}

Puoi utilizzare la ricerca e i filtri per individuare la risorsa immagine desiderata. Seleziona la risorsa e fai clic su **[!UICONTROL Seleziona]** per utilizzarla per il componente immagine.

Per informazioni più dettagliate sull’utilizzo dei file di immagine da [!DNL Experience Manager Assets], consulta [Accedere alle immagini di AEM Assets](./aem-assets.md#access-aem-assets-images).

>[!TAB Importare file multimediali]

Fai clic su **[!UICONTROL Importa file multimediali]** per selezionare un file di immagine e importarlo come risorsa da utilizzare per il contenuto di Journey Optimizer B2B Edition.

![Selezionare un file di immagine personale da importare come risorsa](./assets/content-assets-image-import-file-selected.png){width="450" zoomable="yes"}

Dopo aver trascinato il file o averlo selezionato dal sistema dei file, fai clic su **[!UICONTROL Importa]**. La risorsa importata è archiviata nell&#39;archivio risorse [!DNL Journey Optimizer B2B Edition].

>[!ENDTABS]
