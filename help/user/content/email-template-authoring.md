---
title: Authoring di modelli e-mail
description: Crea modelli e-mail riutilizzabili con strumenti di progettazione visiva, CSS personalizzati, frammenti e personalizzazione per percorsi di account in Journey Optimizer B2B edition.
feature: Templates, Email Authoring, Content
role: User
exl-id: 2d532f93-c452-400a-8a82-e1f0eb89b199
source-git-commit: 9f8953423e3b6d578155431c7638e4fec9abf86a
workflow-type: tm+mt
source-wordcount: '540'
ht-degree: 2%

---

# Authoring di modelli e-mail

Dopo aver [creato un modello e-mail](./email-templates.md#create-an-email-template), utilizza lo spazio di progettazione visiva per creare i componenti struttura e contenuto nel modello e-mail.

## Aggiungere struttura e contenuto {#structure-content}

{{$include /help/_includes/content-design-components.md}}

### Aggiungere CSS personalizzato

Puoi aggiungere CSS personalizzato direttamente nello spazio di progettazione del modello e-mail. Utilizza CSS personalizzato per applicare uno stile avanzato e specifico, per una maggiore flessibilità e un maggiore controllo sull’aspetto del contenuto. È consigliabile aggiungere questo stile di livello più alto prima di includere componenti quali immagini, pulsanti e testo.

Con almeno un componente di contenuto nell&#39;area di lavoro, seleziona il componente **[!UICONTROL Corpo]** nella struttura di navigazione a sinistra per accedere all&#39;editor CSS personalizzato.

![Accedere agli stili del corpo](./assets/email-template-body-styles.png){width="800" zoomable="yes"}

{{$include /help/_includes/content-design-custom-css.md}}

### Aggiungi frammenti

>[!NOTE]
>
>I frammenti non sono compatibili tra la _modalità tema_ e la _modalità manuale_ nel contenuto dell&#39;e-mail. Per utilizzare un frammento nel contenuto dell&#39;e-mail in cui viene applicato un tema, è necessario creare il frammento anche in _modalità tema_.

{{$include /help/_includes/content-design-use-fragments.md}}

Dopo il salvataggio, il modello viene visualizzato nella pagina dei dettagli del frammento quando si seleziona la scheda _[!UICONTROL Usato da]_ nel riepilogo.

### Aggiungere risorse immagine

{{$include /help/_includes/content-design-assets.md}}

### Spostarsi tra livelli, impostazioni e stili

{{$include /help/_includes/content-design-navigation.md}}

### Personalizzazione dei contenuti

{{$include /help/_includes/content-design-personalization-email.md}}

### Modifica tracciamento URL collegato

{{$include /help/_includes/content-design-links.md}}

### Applica stile modalità scura

Utilizza la _modalità scura_ per verificare la presenza di un tema scuro nel client di posta elettronica. Una modalità scura o un tema consente a un client e-mail o a un’app di supporto di visualizzare e-mail con sfondi più scuri e colori più chiari per testo, pulsanti e altri elementi visivi. In alto a destra nell&#39;area di progettazione, imposta il selettore su _modalità scura_ ( ![icona modalità scura](../assets/do-not-localize/icon-content-dark-mode.svg) ). Quindi, visualizza in anteprima e definisci le impostazioni personalizzate specifiche utilizzate per la visualizzazione dai client e-mail di supporto quando il loro tema scuro è abilitato.

![Area di lavoro di progettazione e-mail con il selettore della modalità scura e il contenuto delle e-mail visualizzato in tale modalità](./assets/email-color-mode-dark-selector.png){width="700" zoomable="yes"}

Per ulteriori informazioni sullo stile della modalità scura e sulle best practice, vedere [Modalità scura per il contenuto delle e-mail](./email-dark-mode.md).

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
* **[!UICONTROL Modifica la progettazione]** - Torna alla pagina _Progetta la tua e-mail_. A questo punto è possibile scegliere un altro modello per riavviare il processo di progettazione. Puoi anche scegliere di progettare il contenuto da zero con un&#39;area di lavoro vuota (_Modalità classica_) o utilizzando un [tema del marchio](./brand-themes.md) (_Modalità tema_).
* **[!UICONTROL Esporta HTML]** - Scarica il contenuto nell&#39;area di lavoro visiva nel tuo sistema locale in formato HTML racchiuso in un file zip.
