---
title: Authoring dei modelli e-mail
description: Scopri come creare modelli e-mail di contenuto che possono essere utilizzati per le e-mail del percorso di account per riutilizzare le progettazioni in modo semplice ed efficiente.
feature: Templates, Email Authoring, Content
role: User
exl-id: 2d532f93-c452-400a-8a82-e1f0eb89b199
source-git-commit: 9b053f81e3074f03740fe1f3b69f632219ad269a
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 10%

---

# Authoring di modelli e-mail

Dopo aver [creato un modello e-mail](./email-templates.md#create-an-email-template), utilizza lo spazio di progettazione visiva per creare i componenti struttura e contenuto nel modello e-mail.

## Aggiungere struttura e contenuto {#structure-content}

>[!CONTEXTUALHELP]
>id="ajo-b2b_structure_components_template"
>title="Aggiungere i componenti Struttura"
>abstract="I componenti della struttura definiscono il layout del modello. Per iniziare a progettare il contenuto del modello, trascina un componente **Struttura** nell’area di lavoro."

>[!CONTEXTUALHELP]
>id="ajo-b2b_content_components_template"
>title="Informazioni sui componenti per contenuti"
>abstract="I componenti di contenuto sono segnaposto di contenuto vuoti che possono essere utilizzati per creare il layout di un modello."

{{$include /help/_includes/content-design-components.md}}

### Aggiungere CSS personalizzato

Puoi aggiungere CSS personalizzato direttamente nello spazio di progettazione del modello e-mail. Utilizza CSS personalizzato per applicare uno stile avanzato e specifico, per una maggiore flessibilità e un maggiore controllo sull’aspetto del contenuto. È consigliabile aggiungere questo stile di livello più alto prima di includere componenti quali immagini, pulsanti e testo.

Con almeno un componente di contenuto nell&#39;area di lavoro, seleziona il componente **[!UICONTROL Corpo]** nella struttura di navigazione a sinistra per accedere all&#39;editor CSS personalizzato.

![Accedere agli stili del corpo](./assets/email-template-body-styles.png){width="800" zoomable="yes"}

{{$include /help/_includes/content-design-custom-css.md}}

### Aggiungi frammenti

{{$include /help/_includes/content-design-use-fragments.md}}

Dopo il salvataggio, il modello viene visualizzato nella pagina dei dettagli del frammento quando si seleziona la scheda _[!UICONTROL Usato da]_ nel riepilogo.

### Aggiungere risorse

{{$include /help/_includes/content-design-assets.md}}

### Spostarsi tra livelli, impostazioni e stili

{{$include /help/_includes/content-design-navigation.md}}

### Personalizzazione dei contenuti

{{$include /help/_includes/content-design-personalization-email.md}}

### Modifica tracciamento URL collegato

{{$include /help/_includes/content-design-links.md}}

## Opzioni di visualizzazione

Sfrutta le opzioni di convalida della visualizzazione e del contenuto disponibili nello spazio di progettazione visiva.

* Zoom in/out del contenuto tra le opzioni di zoom predefinite.

* Cambia la visualizzazione del contenuto tra desktop, dispositivi mobili o solo testo/solo testo.
   * Fai clic sull&#39;icona _Occhio_ per visualizzare l&#39;anteprima del contenuto tra i dispositivi.
   * Seleziona uno dei dispositivi predefiniti o immetti dimensioni personalizzate per visualizzare in anteprima il contenuto.

### Altre opzioni

Dal menu _[!UICONTROL Altro ...]_ nella parte superiore dello spazio di progettazione delle e-mail, puoi eseguire le azioni seguenti:

![Fai clic su Altro per accedere alle azioni del modello](./assets/visual-designer-more-menu.png){width="500"}

* **[!UICONTROL Ripristina modello]** - Fare clic su questa opzione per cancellare l&#39;area di progettazione in un&#39;area vuota e riavviare la creazione del contenuto.
* **[!UICONTROL Salva come frammento]** - Consente di salvare tutte o alcune parti del modello come frammento da riutilizzare in più e-mail o modelli di e-mail. Fornisci un nome e una descrizione per il frammento, quindi salvalo nell’elenco dei frammenti disponibili.
* **[!UICONTROL Modifica la progettazione]** - Torna alla pagina _Progetta modello_. A questo punto è possibile scegliere di progettare il modello da zero o di utilizzare un modello esistente per riavviare il processo di progettazione.
* **[!UICONTROL Esporta HTML]** - Scarica il contenuto nell&#39;area di lavoro visiva nel tuo sistema locale in formato HTML racchiuso in un file zip.
