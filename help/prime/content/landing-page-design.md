---
title: Progettazione pagina di destinazione
description: 'Progettare pagine di destinazione con strumenti visivi: aggiungi componenti di contenuto, moduli, CSS personalizzati, personalizzazione e anteprima del dispositivo per percorsi di persone in Journey Optimizer B2B Prime.'
badgeBeta: label="Beta" type="informative" tooltip="Questa funzione fa parte di una versione beta limitata."
feature: Landing Pages, Content Design Tools
role: User
autotag-review: '2026-07-08T20:36:05.221Z'
TQID: 'https://experienceleague.adobe.com/M8OA0CPihuuX5h9J-ZrGJOPHkHLwatX5VhBa8co4r4Y'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: aed878b8-11d0-487c-828b-d23b2051ec37
  - id: e666e996-b2cf-4c45-8fc2-1c625212abab
subfeature_v2:
  - id: a96755d6-1f54-4f3f-a971-d31f83705ab7
  - id: e7bdffdc-2950-4be5-8c23-84240a995090
  - id: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 75a4fec07c880f52ac1e8981b5f4416a2f69afe9
workflow-type: tm+mt
source-wordcount: 568
ht-degree: 2%

---

# Progettazione pagina di destinazione

Dopo aver [creato una pagina di destinazione](./landing-pages-create-publish.md#create-landing-page), utilizza lo spazio di progettazione visiva per creare i componenti strutturali e di contenuto nella pagina.

## Aggiungere struttura e contenuto {#structure-content-landing-page}

{{$include /help/_includes/content-design-components-prime.md}}

### Aggiungere CSS personalizzato {#add-custom-css}

Puoi aggiungere un CSS personalizzato direttamente nello spazio di progettazione della pagina di destinazione. Utilizza CSS personalizzato per applicare uno stile avanzato e specifico, per una maggiore flessibilità e un maggiore controllo sull’aspetto del contenuto. È consigliabile aggiungere questo stile di livello più alto prima di includere componenti quali immagini, pulsanti e testo.

Con almeno un componente di contenuto nell&#39;area di lavoro, seleziona il componente **[!UICONTROL Corpo]** nella struttura di navigazione a sinistra per accedere all&#39;editor CSS personalizzato.

![Accedere agli stili del corpo](../../user/content/assets/landing-page-body-styles-css.png){width="800" zoomable="yes"}

Consulta [Aggiungi CSS personalizzato per il contenuto](./design-custom-css.md) per i passaggi, le regole di sintassi e la risoluzione dei problemi.

### Aggiungere risorse {#add-assets}

Nello spazio di progettazione visiva, seleziona l&#39;icona _Assets_ ( ![icona Assets](../../assets/do-not-localize/icon-assets-me.svg) ) nella barra di navigazione a sinistra per sfogliare e selezionare le risorse immagine dalla libreria di risorse [!DNL Journey Optimizer B2B Prime].

Per i passaggi per selezionare, sostituire o caricare le risorse immagine, consulta [Utilizzare le risorse per l&#39;authoring dei contenuti](./digital-asset-management.md#assets-authoring).

### Aggiungi moduli {#add-forms}

{{$include /help/_includes/content-design-add-forms.md}}

### Spostarsi tra livelli, impostazioni e stili {#navigate-layers-settings-styles}

{{$include /help/_includes/content-design-navigation.md}}

### Personalizzazione dei contenuti {#personalize-content}

[!DNL Journey Optimizer B2B Prime] utilizza la sintassi Handlebars per la personalizzazione. I token vengono sostituiti con i valori dei dati del profilo di ciascun visitatore quando viene visualizzata la pagina di destinazione.

_Per aggiungere la personalizzazione :_

1. Seleziona il componente testo e fai clic sull&#39;icona _Aggiungi personalizzazione_ ( ![icona Personalizza](../../user/assets/do-not-localize/icon-personalize.svg) ) nella barra degli strumenti.
1. Nella finestra di dialogo di personalizzazione, sfoglia la struttura dello schema a sinistra e seleziona un attributo. L’editor inserisce l’espressione Handlebars corrispondente.
1. Se necessario, aggiungi un valore di fallback per gestire i dati mancanti.
1. Fai clic su **[!UICONTROL Conferma]** o **[!UICONTROL Inserisci]**. L’espressione viene visualizzata in linea nel campo.

Per informazioni dettagliate sugli strumenti e sulla sintassi dell&#39;editor espressioni, vedere [Editor Personalization](./personalization-expressions.md).

### Modifica tracciamento URL collegato {#linked-url-tracking}

{{$include /help/_includes/content-design-links.md}}

![Fai clic sull&#39;icona Modifica per accedere al tracciamento dei collegamenti](../../user/content/assets/landing-page-link-tracking.png){width="400"}

Utilizza il **[!UICONTROL Tipo di tracciamento]** per controllare il tracciamento del collegamento:

* **[!UICONTROL Tracciato]** - Attiva il tracciamento sull&#39;URL del collegamento.
* **[!UICONTROL Mai]** - Non attiva mai il tracciamento dell&#39;URL del collegamento.

### Salvare i dati {#save-your-work}

Fai clic su **[!UICONTROL Salva]** in qualsiasi momento per salvare la bozza della pagina di destinazione.

Puoi continuare ad apportare modifiche alla pagina della bozza. Quando sei pronto per visualizzare la pagina e renderla disponibile per il collegamento in un messaggio e-mail o SMS, puoi pubblicare la pagina.

### Opzioni di visualizzazione {#view-options}

Sfrutta le opzioni di convalida della visualizzazione e del contenuto disponibili nello spazio di progettazione visiva.

* Zoom in/out del contenuto tra le opzioni di zoom predefinite.

* Cambia la visualizzazione del contenuto tra desktop, dispositivi mobili o solo testo/solo testo.
   * Fai clic sull&#39;icona _Visualizza_ per l&#39;anteprima del contenuto tra i dispositivi.
   * Seleziona uno dei dispositivi predefiniti o immetti dimensioni personalizzate per visualizzare in anteprima il contenuto.

### Altre opzioni {#more-options}

Dal menu _[!UICONTROL Altro ...]_ nella parte superiore dello spazio di progettazione visiva, è possibile eseguire le azioni seguenti:

![Fai clic su Altro per accedere alle azioni della pagina di destinazione](../../user/content/assets/landing-page-designer-more-menu.png){width="500"}

* **[!UICONTROL Ripristina pagina di destinazione]** - Fare clic su questa opzione per cancellare l&#39;area di lavoro di progettazione visiva e ricominciare a creare il contenuto della pagina.
* **[!UICONTROL Modifica la progettazione]** - Torna alla _[!UICONTROL home page di creazione della pagina di destinazione principale]_. A questo punto è possibile scegliere un altro modello per riavviare il processo di progettazione oppure scegliere di progettare la pagina da zero in un&#39;area di lavoro vuota.
* **[!UICONTROL Esporta HTML]** - Scarica il contenuto nell&#39;area di lavoro visiva nel tuo sistema locale in formato HTML racchiuso in un file zip.
