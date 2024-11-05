---
title: Authoring dei modelli e-mail
description: Scopri come creare modelli e-mail di contenuto che possono essere utilizzati per le e-mail del percorso di account per riutilizzare le progettazioni in modo semplice ed efficiente.
feature: Email Authoring, Content
source-git-commit: 8315c760e573aa36819652798a400206e6268ccc
workflow-type: tm+mt
source-wordcount: '496'
ht-degree: 7%

---

# Authoring dei modelli e-mail

Dopo aver [creato un modello e-mail](./email-templates.md#create-an-email-template), utilizza la finestra di progettazione visiva per creare i componenti struttura e contenuto nel modello e-mail.

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

### Aggiungi frammenti

Nell&#39;editor del contenuto visivo, l&#39;icona _Frammenti_ è visualizzata a sinistra. L’esempio seguente illustra i passaggi per aggiungere frammenti al contenuto del modello.

1. Per aprire l&#39;elenco dei frammenti, seleziona l&#39;icona _Frammenti_ ( ![Icona Frammenti](../assets/do-not-localize/icon-fragments.svg) ).

   Puoi eseguire le seguenti operazioni:

   * Ordina l’inserzione.
   * Sfoglia, Cerca o filtra l’inserzione.
   * Consente di passare dalla visualizzazione Anteprima alla visualizzazione Elenco.
   * Aggiorna l’elenco per riflettere eventuali frammenti creati di recente.

   ![Selezionare un frammento dall&#39;elenco](./assets/visual-designer-fragments.png){width="700" zoomable="yes"}

1. Trascina uno dei frammenti nel segnaposto del componente strutturale.

   L’editor esegue il rendering del frammento all’interno della sezione/elemento della struttura e-mail.

Il contenuto del frammento viene aggiornato dinamicamente all’interno della struttura per mostrare come appare il contenuto nell’e-mail.

>[!TIP]
>
>Se desideri che il frammento occupi l’intero layout orizzontale all’interno dell’e-mail, aggiungi una struttura di colonne 1:1, quindi trascina e rilascia il frammento al suo interno.

Dopo il salvataggio, l&#39;e-mail viene visualizzata nella pagina dei dettagli del frammento quando si seleziona la scheda _[!UICONTROL Usato da]_ nel riepilogo. I frammenti aggiunti a un modello e-mail non sono modificabili all’interno del modello: il frammento di origine definisce il contenuto.

### Aggiungere risorse

{{$include /help/_includes/content-design-assets.md}}

### Spostarsi tra livelli, impostazioni e stili

{{$include /help/_includes/content-design-navigation.md}}

### Personalizzare il contenuto

{{$include /help/_includes/content-design-personalization.md}}

### Modifica tracciamento URL collegato

{{$include /help/_includes/content-design-links.md}}

## Opzioni di visualizzazione

Sfrutta le opzioni di convalida della visualizzazione e del contenuto disponibili nella finestra di progettazione visiva.

* Zoom in/out del contenuto tra le opzioni di zoom predefinite.

* Cambia la visualizzazione del contenuto tra desktop, dispositivi mobili o solo testo/solo testo.
   * Fai clic sull&#39;icona _Occhio_ per visualizzare l&#39;anteprima del contenuto tra i dispositivi.
   * Seleziona uno dei dispositivi predefiniti o immetti dimensioni personalizzate per visualizzare in anteprima il contenuto.

### Altre opzioni

Dal menu _[!UICONTROL Altro ...]_ nella parte superiore della finestra di progettazione e-mail, puoi eseguire le azioni seguenti:

![Fai clic su Altro per accedere alle azioni del modello](./assets/visual-designer-more-menu.png){width="500"}

* **[!UICONTROL Ripristina modello]** - Fare clic su questa opzione per cancellare l&#39;area di lavoro della finestra di progettazione visiva in un&#39;area vuota e riavviare la creazione del contenuto.
* **[!UICONTROL Salva come frammento]** - Consente di salvare tutte o alcune parti del modello come frammento da riutilizzare in più e-mail o modelli di e-mail. Fornisci un nome e una descrizione per il frammento, quindi salvalo nell’elenco dei frammenti disponibili.
* **[!UICONTROL Modifica la progettazione]** - Torna alla pagina _Progetta modello_. A questo punto è possibile scegliere di progettare il modello da zero o di utilizzare un modello esistente per riavviare il processo di progettazione.
* **[!UICONTROL Esporta HTML]** - Scarica il contenuto nell&#39;area di lavoro visiva nel sistema locale in formato HTML compresso come file zip.
