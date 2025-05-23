---
title: Authoring dei messaggi e-mail
description: Scopri come creare contenuti e-mail in Adobe Journey Optimizer B2B. Utilizza modelli, importazioni HTML e strumenti basati sull’intelligenza artificiale per personalizzare e ottimizzare le comunicazioni e-mail.
feature: Email Authoring, Content Design Tools
role: User
exl-id: 0f4ae644-ade7-49a0-935c-7f4779c25ffb
source-git-commit: 633f23525a6fd2b03460ecbef17379077d6b51d2
workflow-type: tm+mt
source-wordcount: '928'
ht-degree: 15%

---

# Authoring dei messaggi e-mail

Dopo aver [aggiunto una nuova<!-- or duplicated --> risorsa e-mail a un nodo azione di percorso](./add-email.md), puoi definire il contenuto del messaggio e-mail.

Fai clic su **[!UICONTROL Modifica contenuto e-mail]** nella scheda _[!UICONTROL Dettagli]_ nel pannello di destra.

![Fare clic su Modifica contenuto e-mail ](./assets/add-email-content.png){width="700" zoomable="yes"}

Questa azione avvia gli strumenti di progettazione delle e-mail, in cui puoi scegliere come progettare le e-mail dalle seguenti opzioni:

* [Progetta il tuo indirizzo e-mail da zero](#design-your-email-from-scratch) utilizzando l&#39;interfaccia di E-mail Designer.

* [Importa contenuto HTML esistente](#import-existing-html-content) da un file o da una cartella .zip.

* [Selezionare un modello esistente](#select-a-template) da un elenco di modelli di posta elettronica predefiniti o personalizzati.

Dopo aver creato e personalizzato il contenuto dell’e-mail, puoi esportarlo per la convalida o per un utilizzo successivo. Fai clic su **[!UICONTROL Esporta HTML]** per salvare il contenuto come file .zip che include il HTML e le risorse.

>[!TIP]
>
>Utilizza l’Assistente AI in Adobe Journey Optimizer B2B edition, basato su intelligenza artificiale generativa, per elevare i contenuti al livello successivo. L’Assistente AI può aiutarti a ottimizzare l’impatto delle consegne generando e-mail intere, contenuto di testo mirato e ricevendo consigli dall’Assistente AI per le immagini che risuonano con il tuo pubblico. [Ulteriori informazioni](./ai-assistant-emails.md)

## Creare e-mail da zero {#design-from-scratch}

>[!CONTEXTUALHELP]
>id="ajo-b2b_structure_components_landing_page"
>title="Aggiungere i componenti Struttura"
>abstract="I componenti della struttura definiscono il layout della pagina di destinazione. Per iniziare a progettare il contenuto della pagina di destinazione, trascina un componente **Struttura** nell’area di lavoro."

>[!CONTEXTUALHELP]
>id="ajo-b2b_content_components_landing_page"
>title="Informazioni sui componenti per contenuti"
>abstract="I componenti dei contenuti sono dei segnaposto di contenuto vuoti che possono essere utilizzati per creare il layout di una pagina di destinazione."

Utilizza lo spazio di progettazione del contenuto visivo per definire la struttura e il contenuto dell’e-mail. Aggiungendo e spostando componenti strutturali con semplici azioni di trascinamento della selezione, puoi progettare la forma del contenuto dell’e-mail riutilizzabile in pochi secondi.

1. Dalla home page di _[!UICONTROL Progetta modello]_, seleziona l&#39;opzione **[!UICONTROL Progetta da zero]**.
1. [Aggiungi struttura e contenuto](#add-structure-and-content) al messaggio di posta elettronica.
1. [Aggiungi risorse immagine](#add-assets) al messaggio e-mail.
1. [Personalizzare il contenuto dell&#39;e-mail](#personalize-content).
1. [Rivedi e aggiorna i collegamenti](#preview-and-edit-linked-urls).

<!-- If needed, you can further personalize your email by clicking **[!UICONTROL Switch to code editor]** from the advanced menu. The code editor allows you to edit the email source code, such as adding tracking or custom HTML tags.

>[!CAUTION]
>
>You cannot revert back to the visual designer for this email after switching to the code editor. -->

Al termine, fai clic su **[!UICONTROL Simula contenuto]** in alto per verificare il rendering. È possibile scegliere la visualizzazione desktop o mobile.

Quando si è soddisfatti del contenuto, fare clic su **[!UICONTROL Salva]**.

## Importa contenuto HTML esistente

{{$include /help/_includes/content-design-import.md}}

![importa contenuto html in un file zip](./assets/email-import-zip-file.png){width="500"}

>[!NOTE]
>
>L&#39;utilizzo di un tag `<table>` come primo livello in un file HTML può causare la perdita di stile, incluse le impostazioni di sfondo e larghezza nel tag del livello superiore.

Puoi personalizzare il contenuto importato in base alle esigenze con gli strumenti dell’editor e-mail visivo.

## Seleziona un modello

{{$include /help/_includes/content-design-select-template.md}}

>[!NOTE]
>
> Ai modelli salvati possono essere applicate impostazioni di governance (blocco del contenuto) a uno o più componenti. La finestra di progettazione visiva fornisce indicazioni sui componenti bloccati quando si [crea un messaggio e-mail da un modello gestito](./email-authoring-governance.md).

## Aggiungere struttura e contenuto {#structure-content}

>[!CONTEXTUALHELP]
>id="ajo-b2b_structure_components_email"
>title="Aggiungere i componenti Struttura"
>abstract="I componenti della struttura definiscono il layout del messaggio e-mail. Per iniziare a progettare il contenuto delle e-mail, trascina un componente **Struttura** nell’area di lavoro."

>[!CONTEXTUALHELP]
>id="ajo-b2b_content_components_email"
>title="Informazioni sui componenti per contenuti"
>abstract="I componenti per contenuti sono dei segnaposto di contenuto vuoti che possono essere utilizzati per creare il layout di un’e-mail."

{{$include /help/_includes/content-design-components.md}}

### Aggiungi frammenti

{{$include /help/_includes/content-design-use-fragments.md}}

Dopo il salvataggio, l&#39;e-mail viene visualizzata nella pagina dei dettagli del frammento quando si seleziona la scheda _[!UICONTROL Usato da]_ nel riepilogo.

### Aggiungere risorse

{{$include /help/_includes/content-design-assets.md}}

### Spostarsi tra livelli, impostazioni e stili

{{$include /help/_includes/content-design-navigation.md}}

### Personalizzazione dei contenuti

{{$include /help/_includes/content-design-personalization.md}}

>[!NOTE]
>
>Se per il percorso di account sono definiti _[!UICONTROL I miei token]_, è possibile utilizzare anche questi token specifici del percorso per il contenuto delle e-mail. Per ulteriori informazioni, consulta [Token personalizzati per la personalizzazione delle e-mail](./personalization-my-tokens.md).

### Modifica tracciamento URL collegato

{{$include /help/_includes/content-design-links.md}}

### Opzioni di visualizzazione

Sfrutta le opzioni di convalida di visualizzazione e contenuto disponibili nell’editor e-mail visivo.

* Zoom in/out del contenuto tra le opzioni di zoom predefinite.

* Cambia la visualizzazione del contenuto tra desktop, dispositivi mobili o solo testo/solo testo.
   * Fai clic sull&#39;icona _Visualizza_ per l&#39;anteprima del contenuto tra i dispositivi.
   * Seleziona uno dei dispositivi predefiniti o immetti dimensioni personalizzate per visualizzare in anteprima il contenuto.

### Altre opzioni

Dal menu _[!UICONTROL Altro ...]_ nella parte superiore dello spazio di progettazione delle e-mail, puoi eseguire le azioni seguenti:

![Fai clic su Altro per accedere alle azioni del modello](./assets/email-designer-more-menu.png){width="500"}

* **[!UICONTROL Reimposta e-mail]** - Fare clic su questa opzione per cancellare l&#39;area di lavoro di progettazione e-mail visiva in una lavagna vuota e riavviare la creazione del contenuto.
* **[!UICONTROL Salva come frammento]** - Salva tutte o alcune parti dell&#39;e-mail come frammento da riutilizzare in più e-mail o modelli di e-mail. Fornisci un nome e una descrizione per il frammento, quindi salvalo nell’elenco dei frammenti disponibili.
* **[!UICONTROL Modifica la progettazione]** - Torna alla pagina _Progetta la tua e-mail_. Da lì, puoi scegliere un altro modello per riavviare il processo di progettazione o scegliere di progettare il contenuto da zero in un&#39;area di lavoro nera.\
* **[!UICONTROL Salva come modello di contenuto]** - Salva il corpo dell&#39;e-mail come modello e-mail da riutilizzare in più e-mail o modelli e-mail. Fornisci un nome e una descrizione per il modello, quindi salvalo nell’elenco dei modelli e-mail salvati.
* **[!UICONTROL Esporta HTML]** - Scarica il contenuto nell&#39;area di lavoro visiva nel tuo sistema locale in formato HTML racchiuso in un file zip.

## Controllare e testare l’e-mail {#preview-test}

>[!CONTEXTUALHELP]
>id="ajo-b2b_email_preview_simulate"
>title="Controllare come viene eseguito il rendering del contenuto"
>abstract="Una volta definito il contenuto, puoi visualizzarne l’anteprima e verificare se il rendering è corretto in base al canale in uso."

Una volta definito il contenuto del messaggio, puoi utilizzare i profili di test per visualizzarne l’anteprima, inviare bozze e controllarne il rendering nei client desktop, mobili e basati su Web più diffusi. Se hai inserito dei contenuti personalizzati, puoi visualizzare in anteprima come questi contenuti vengono visualizzati nel messaggio utilizzando i dati del profilo di test.

Per visualizzare in anteprima il contenuto dell&#39;e-mail, fai clic su **[!UICONTROL Simula contenuto]** e quindi aggiungi un profilo di test per verificare il messaggio utilizzando i dati del profilo di test.

![Simula il contenuto dell&#39;e-mail per controllare la progettazione](./assets/email-designer-simulate-content.png){width="700" zoomable="yes"}
