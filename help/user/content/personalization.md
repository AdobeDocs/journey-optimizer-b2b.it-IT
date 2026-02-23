---
title: Personalizzazione dei contenuti
description: Personalizza le e-mail B2B utilizzando token di account, persona e di sistema in Journey Optimizer B2B edition. Scopri come utilizzare l’editor e la sintassi di personalizzazione.
feature: Personalization, Content Design Tools, Email Authoring
topic: Personalization
role: User, Developer
level: Intermediate
keywords: espressione, editor, start, personalization
exl-id: 60bf2e06-8d6e-4cc4-8aff-5c5ca11f05ab
source-git-commit: 10e02b821609c48b82ea0248501daa60de6daa12
workflow-type: tm+mt
source-wordcount: '756'
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

Aggiungi la personalizzazione a qualsiasi campo o componente di contenuto facendo clic sull&#39;icona _Aggiungi personalizzazione_ ( ![Aggiungi icona personalizzazione](../../assets/do-not-localize/icon-personalization-field.svg) ).

![Editor Personalization](./assets/personalization-editor.png){width="800" zoomable="yes"}

>[!NOTE]
>
>Le informazioni seguenti sull&#39;editor di personalizzazione riflettono le modifiche disponibili per gli ambienti [!DNL Journey Optimizer B2B Edition] per i quali è stato eseguito il provisioning nell&#39;architettura [semplificata](../simplified-architecture.md).

### Token e funzioni di assistenza

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

### Set di dati personalizzati

[!BADGE Beta]{type=Informative tooltip="Funzione Beta"}

Puoi utilizzare gli schemi relazionali per la personalizzazione delle e-mail. Gli oggetti personalizzati sono definiti all&#39;interno di _schemi relazionali_ e un amministratore di prodotto può [configurare i campi dello schema relazionale](../admin/xdm-field-management.md#relational-schemas) in [!DNL Journey Optimizer B2B Edition]. Questi campi sono accessibili nell’editor di personalizzazione. Sono disponibili solo oggetti personalizzati con una relazione uno-a-molti (1:M) con Persone o Account.

>[!IMPORTANT]
>
>Prima di utilizzare oggetti personalizzati per la personalizzazione tramite script, accertati di rivedere e comprendere il [linguaggio di modelli Handlebars](https://handlebarsjs.com/guide/), la [sintassi di personalizzazione](./personalization-syntax.md) e le [funzioni di supporto](./personalization-helper-functions.md) integrate.

Quando definisci la personalizzazione utilizzando oggetti personalizzati, puoi accedere a tutte le variabili in oggetti accessibili tramite script nei **[!UICONTROL token di Personalization]** (persona/lead, account, sistema e My Tokens) e nei **[!UICONTROL oggetti personalizzati]** (schemi relazionali). Con gli oggetti personalizzati selezionati, è possibile visualizzare i campi facendo clic sulla cartella degli oggetti personalizzati. Fare clic su **+** per ogni campo da aggiungere all&#39;espressione.

![Editor Personalization - Classi basate su modello - aggiunta di campi oggetto personalizzati](./assets/personalization-editor-custom-object-fields.png){width="700" zoomable="yes"}
