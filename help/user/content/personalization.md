---
title: Personalizzazione dei contenuti
description: Personalizza le e-mail B2B utilizzando token di account, persona e di sistema in Journey Optimizer B2B edition. Scopri come utilizzare l’editor e la sintassi di personalizzazione.
feature: Personalization, Content Design Tools, Email Authoring
topic: Personalization
role: User, Developer
level: Intermediate
keywords: espressione, editor, start, personalization
source-git-commit: fee5bddcce11b3035da6ab93b18bcc7006b4b554
workflow-type: tm+mt
source-wordcount: '610'
ht-degree: 0%

---

# Personalizzazione dei contenuti {#add-personalization}

>[!CONTEXTUALHELP]
>id="aj-b2b_personalization"
>title="Personalizzare le esperienze dei contenuti"
>abstract="Utilizza **Adobe Journey Optimizer B2B edition** per adattare i messaggi a ogni destinatario specifico sfruttando i dati e le informazioni di cui disponi su di essi. Può essere il nome, il settore, il titolo e altro ancora."

Le funzionalità di personalizzazione di [!DNL Adobe Journey Optimizer B2B Edition] consentono di adattare i messaggi di posta elettronica a ogni destinatario specifico sfruttando i dati e le informazioni disponibili su di essi. Può essere il nome, il settore, il titolo e altro ancora.

Utilizzando l&#39;_editor personalizzazione_, puoi selezionare, disporre, personalizzare e convalidare tutti i dati per creare una personalizzazione personalizzata per il contenuto. Utilizza vari strumenti, ad esempio le funzioni di assistenza, per adattare i messaggi. L&#39;editor utilizza una sintassi di personalizzazione in linea basata su _Handlebars_, in cui le espressioni sono costruite con contenuti racchiusi tra parentesi graffe `{{}}`.

Durante l’elaborazione del messaggio, Journey Optimizer B2B edition sostituisce l’espressione con i dati contenuti nel set di dati di Adobe Experience Platform e nei valori del sistema locale. `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}`, ad esempio, diventa `Hello John Doe` in modo dinamico.

Utilizzando questa sintassi, puoi personalizzare i messaggi in più campi, tra cui righe dell’oggetto e-mail, corpo del messaggio e informazioni sul mittente.

## Token Personalization

In [!DNL Journey Optimizer B2B Edition], puoi creare il contenuto dinamico delle e-mail utilizzando i token di personalizzazione:

* **Token account** - Questi token si basano sugli attributi dell&#39;account, ad esempio _nome account_, _settore_ e _numero di dipendenti_. Utilizza questi token per popolare i dati attributo gestiti dallo schema **_Dettagli account aziendale XDM_**, definito in Adobe Experience Platform.

* **Token persona** - Questi token si basano sugli attributi della persona aziendale, ad esempio _nome_, _titolo processo_ e _nome società_. Utilizza questi token per popolare i dati attributo gestiti dallo schema **_Dettagli persona aziendale XDM_**, definito in Adobe Experience Platform.

* **Token di sistema** - Questi token si basano sui valori dei campi di sistema, ad esempio _data_, _ora_ e _collegamento per annullare l&#39;abbonamento_.

* **Token personali** (quando definito per il percorso) - I [token personalizzati definiti per il percorso](./personalization-my-tokens.md) in cui si trova l&#39;e-mail.

>[!NOTE]
>
>Ulteriori informazioni sugli schemi XDM nella [documentazione di Adobe Experience Platform Data Model (XDM)](https://experienceleague.adobe.com/it/docs/experience-platform/xdm/home){target="_blank"}.

## Editor Personalization

L’editor di personalizzazione è disponibile in ogni contesto in cui è necessario definire la personalizzazione nel contenuto delle e-mail. Nell’editor puoi selezionare, disporre, personalizzare e convalidare tutti i dati per creare una personalizzazione personalizzata per il contenuto.

>[!NOTE]
>
>Le informazioni seguenti per l&#39;editor di personalizzazione riflettono le modifiche disponibili per gli ambienti Journey Optimizer B2B edition che dispongono del provisioning nell&#39;architettura [semplificata](../simplified-architecture.md).

Aggiungi la personalizzazione a qualsiasi campo o componente di contenuto facendo clic sull&#39;icona _Aggiungi personalizzazione_ ( ![Aggiungi icona personalizzazione](../../assets/do-not-localize/icon-personalization-field.svg) ).

![Editor Personalization](./assets/personalization-editor.png){width="800" zoomable="yes"}

Per utilizzare un token di personalizzazione o una funzione di supporto, individuarlo nel riquadro di navigazione a sinistra e fare clic su **+** per aggiungerlo all&#39;espressione.

Fai clic sull&#39;icona _Altro menu_ ( **...** ) accanto all&#39;icona _Aggiungi_ ( **+** ) per visualizzare maggiori dettagli per ciascun attributo e aggiungere gli attributi utilizzati più di frequente ai _preferiti_. Gli attributi aggiunti ai preferiti sono accessibili dal menu **[!UICONTROL Preferiti]** nell&#39;area di navigazione a sinistra dell&#39;editor.

![Editor Personalization - menu Altro token](./assets/personalization-editor-token-more-menu.png){width="800" zoomable="yes"}

<!-- >>[!NOTE]
>
>By default, the attributes list shows only populated attributes. To display all attributes, click the _Settings_ icon above the search field and toggle off the **[!UICONTROL Show only populated attributes]** option.
-->
Puoi anche definire una stringa di testo di fallback predefinita che viene visualizzata se un attributo di profilo di tipo stringa è vuoto. Fai clic sull&#39;icona _Altro menu_ ( **...** ) per l&#39;attributo e seleziona **[!UICONTROL Inserisci con testo di fallback]**. Immettere il testo da visualizzare quando il valore dell&#39;attributo per un profilo è vuoto, quindi fare clic su **[!UICONTROL Aggiungi]**.

È consigliabile convalidare l’espressione prima di inserirla nel contenuto. Fai clic su **[!UICONTROL Convalida]** nella parte inferiore dell&#39;editor per verificare la sintassi e verificare che non siano presenti errori.

![Codice convalidato dall&#39;editor di Personalization](./assets/personalization-editor-validated.png){width="500"}

Quando l&#39;espressione è completa e priva di errori, fare clic su **[!UICONTROL Salva]**.

<!-- ## Personalization experimentation {#playground}

**[!DNL Adobe Journey Optimizer]** includes an interactive tool designed to help you learn and experiment with personalization capabilities.

This playground provides a simulated environment to write and test personalization code using sample data without requiring live datasets. You can leverage predefined code samples, edit dummy profile payloads, and preview the output of your personalization code in real-time. 

![personalization playground](assets/playground.png)

➡️ [Access the personalization playground](https://experienceleague.adobe.com/it/apps/journey-optimizer/ajo-personalization){target="_blank"} 

## How-to videos{#video-perso}

Learn how to use contextual event information from a journey to personalize a message.

>[!VIDEO](https://video.tv.adobe.com/v/334165?quality=12)

Learn how to add profile-based personalization to a message and how to use audience membership as a pre-condition to a personalization block.

>[!VIDEO](https://video.tv.adobe.com/v/334078?quality=12)

Learn how to leverage the personalization editor playground to write and test personalization code using sample data.

>[!VIDEO](https://video.tv.adobe.com/v/3457868?quality=12) -->