---
title: Configurare gli archivi di risorse di Experience Manager
description: Scopri come configurare una connessione agli archivi Experience Manager Assets per l’utilizzo nell’authoring dei contenuti Journey Optimizer B2B edition.
feature: Assets, Integrations
role: Admin
exl-id: 4cdfc8bc-823f-4320-a2c3-08226f26eec2
source-git-commit: 1eaaf92fdec538bec4f3d70cc65dee141971b0c5
workflow-type: tm+mt
source-wordcount: '719'
ht-degree: 0%

---

# Configurare gli archivi di risorse di Experience Manager

[!DNL Adobe Journey Optimizer B2B Edition] si integra con [!DNL Adobe Experience Manager Assets as a Cloud Service], consentendo l&#39;utilizzo di risorse nel contenuto dell&#39;e-mail. Garantisce la trasparenza scambiando informazioni con [!DNL Experience Manager Assets]. Configurare la connessione a [!DNL Adobe Experience Assets] per abilitare questa funzionalità.

Adobe Experience Manager Cloud Manager è organizzato in programmi e ogni programma dispone di più ambienti e archivi ([Ulteriori informazioni](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/implementing/using-cloud-manager/programs/program-types){target="_blank"}). Quando configuri Adobe Experience Manager Assets in Adobe Journey Optimizer B2B edition, puoi impostare connessioni a ogni archivio che desideri utilizzare per accedere alle risorse digitali.

{{aem-assets-licensing-note}}

## Prerequisiti

* Genera le credenziali del servizio per l&#39;ambiente desiderato in AEM Headless Developer Console ([Ulteriori informazioni](https://experienceleague.adobe.com/it/docs/experience-manager-learn/getting-started-with-aem-headless/authentication/service-credentials#generate-service-credentials){target="_blank"}).
* Ottenere i certificati necessari per la connessione. Come best practice, assicurati che i certificati rimangano almeno sei mesi prima della scadenza. I certificati scadono ogni 365 giorni.
* Adobe Journey Optimizer B2B edition supporta l’accesso a un’origine per la gestione delle risorse digitali alla volta. Prima di cambiare, assicurati che le risorse richieste siano disponibili in Adobe Experience Manager.

>[!IMPORTANT]
>
>Le credenziali del servizio sono autentiche e contengono una chiave privata. Queste credenziali devono essere archiviate, gestite e accessibili in base ai criteri IT e di sicurezza dell&#39;organizzazione.

## Aggiungere una connessione all’archivio

1. Nel menu di navigazione a sinistra, scegli **[!UICONTROL Amministrazione]** > **[!UICONTROL Configurazione]**.

1. Fai clic su **[!UICONTROL Assets]** nel pannello intermedio.

   ![Accedere allo spazio di configurazione di Assets](./assets/configuration-assets-aem.png){width="700" zoomable="yes"}

<!--   The default digital asset management option is configured as `Adobe Marketo Engage`.
-->
Da qui puoi configurare una alla volta le connessioni a ciascun archivio dell’ambiente AEM.

1. Nella casella _[!UICONTROL Adobe Experience Manager Assets]_ fare clic sulla freccia accanto a **[!UICONTROL Configura un repository]** e scegliere il repository.

   ![Scegliere un repository AEM Assets](./assets/configure-assets-aem-choose-respository.png){width="500"}

1. Fai clic su **[!UICONTROL Aggiungi un certificato]** e utilizza gli strumenti di dialogo per caricare il file.

   Puoi caricare un file .json trascinandolo nella finestra di dialogo. Puoi anche fare clic sul collegamento per individuare e selezionare un file dal sistema.

   ![Carica il file JSON del certificato](./assets/configuration-assets-aem-upload-cert.png){width="500"}

   Dopo il caricamento, il certificato viene visualizzato nella parte inferiore.

   >[!NOTE]
   >
   >Se viene utilizzato un file non valido, nella finestra di dialogo viene visualizzato un errore nella parte inferiore.

   Fai clic su **[!UICONTROL Aggiungi]** per completare il certificato.

1. Fai clic sulla freccia indietro (←) per tornare alla pagina di configurazione principale.

   L’archivio configurato viene visualizzato nella tabella sotto il pannello di selezione. È possibile aggiungere un altro archivio ripetendo i passaggi 3-4.

   ![Esaminare gli archivi di risorse AEM configurati](./assets/configuration-assets-aem-repositories.png){width="600" zoomable="yes"}

Al termine della configurazione degli archivi, i membri del team possono selezionare [!DNL Adobe Experience Manager Assets] durante l&#39;authoring dei contenuti.

>[!NOTE]
>
>Adobe Journey Optimizer B2B edition supporta l’accesso a un’origine per la gestione delle risorse digitali alla volta durante l’authoring dei contenuti. 

## Sostituire un certificato

I certificati scadono ogni 365 giorni dalla data di creazione. Per garantire che il team possa continuare ad accedere alle risorse, sostituisci il certificato prima della scadenza.

>[!NOTE]
>
>[!DNL Adobe Journey Optimizer B2B Edition] comunica con [!DNL Experience Manager Assets] per informazioni sulla sintassi. La connessione deve rimanere attiva per un utilizzo affidabile della sincronizzazione dei dati e per evitare discrepanze di dati. Gli amministratori ricevono notifiche sulla scadenza dei certificati tramite notifiche in-app. Le date di scadenza vengono visualizzate anche nella sottosezione _Assets_ dell&#39;area _[!UICONTROL Amministrazione]_.

1. Nella pagina di gestione delle risorse digitali, individua l’elenco degli archivi configurati.

1. Fai clic sull’archivio desiderato per sostituire il certificato.

1. Fare clic sull&#39;icona dei puntini di sospensione (**...**) per il file di certificato per visualizzare le opzioni relative alle azioni.

   ![Accedi al menu delle opzioni per il certificato del repository di risorse di AEM](./assets/configuration-assets-aem-repo-menu.png){width="600" zoomable="yes"}

1. Scegliere **[!UICONTROL Sostituisci]** per aprire la finestra di dialogo per il caricamento del file.

1. Carica un file trascinandolo nella finestra di dialogo o utilizzando il collegamento. Verifica che il file sia di tipo JSON.

   ![Carica il file JSON del certificato del repository delle risorse di AEM sostitutivo](./assets/configuration-assets-aem-upload-replacement-cert.png){width="500"}

1. Fai clic su **[!UICONTROL Sostituisci]** per confermare il caricamento.

## Visualizzare un certificato

Puoi visualizzare il file JSON del certificato associato alla connessione all’archivio.

1. Nella pagina di gestione delle risorse digitali, individua l’elenco degli archivi configurati.

1. Fare clic sull&#39;archivio connesso.

1. Fare clic sull&#39;icona dei puntini di sospensione (**...**) per il file di certificato per visualizzare le opzioni relative alle azioni.

1. Scegliere **[!UICONTROL Visualizza]**.

   ![Visualizzare il file JSON del certificato per un repository di risorse AEM connesso](./assets/configuration-assets-aem-view-cert.png){width="600"}

1. Fare clic su **[!UICONTROL Chiudi]** per tornare alla pagina Configura repository.

## Eliminare una connessione all’archivio

L’eliminazione di un archivio rimuove l’accesso degli utenti all’ambiente Experience Manager Assets all’interno di Journey Optimizer B2B edition.

1. Nella pagina _[!UICONTROL Gestione risorse digitali]_, individua l&#39;elenco degli archivi di risorse configurati.

1. Fai clic sul nome dell’archivio desiderato per modificare la connessione.

1. Fare clic sull&#39;icona dei puntini di sospensione (**...**) per il file di certificato per visualizzare le opzioni relative alle azioni.

1. Scegliere **[!UICONTROL Elimina]**.

1. Nella finestra di dialogo di conferma, fai clic su **[!UICONTROL Elimina]**.
<!--

## Switch back to Adobe Marketo Engage Assets

Select Adobe Marketo Engage digital asset management in the Assets section.

After the confirmation, the Adobe Marketo Engage assets library is available for users.
-->
