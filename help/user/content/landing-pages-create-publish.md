---
title: Creare e pubblicare le pagine di destinazione
description: 'Creazione, progettazione e pubblicazione di pagine di destinazione per i percorsi: creazione da zero, importazione di HTML, aggiunta di moduli, personalizzazione del contenuto e collegamento dalle e-mail in Journey Optimizer B2B edition.'
feature: Landing Pages, Content
role: User
autotag-review: '2026-05-27T16:10:09.537Z'
TQID: 'https://experienceleague.adobe.com/e-tguY-9v6CPOehYL7vI22fzQBk3L0h1EOpa-e54q7A'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: e666e996-b2cf-4c45-8fc2-1c625212abab
subfeature_v2: id: a96755d6-1f54-4f3f-a971-d31f83705ab7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: e0eb8757-182f-49f3-94a4-1587d16f5094id: e4bd5f48-22a4-465d-a046-5ffb52e27856
source-git-commit: 144848cff6a37691ccbe7a83b78f9db33d8a2b3d
workflow-type: tm+mt
source-wordcount: 1719
ht-degree: 11%

---

# Creare e pubblicare pagine di destinazione

In qualità di addetto al marketing, puoi definire e pubblicare le pagine da incorporare nei percorsi di account e persone. Quando aggiungi una nuova pagina di destinazione, configuri la pagina principale e le eventuali pagine secondarie, progetta il contenuto, verificalo e pubblicalo.

![Diagramma del flusso di lavoro della pagina di destinazione](./assets/landing-page-work-flow-diagram-no-subpages.svg)

>[!BEGINSHADEBOX]

## Prerequisiti per la pagina di destinazione {#landing-page-prerequisites}

Prima che gli esperti di marketing possano creare pagine di destinazione per supportare i loro percorsi e le loro campagne, devono essere attive le seguenti configurazioni e risorse:

* [Sottodominio della pagina di destinazione](../admin/configure-channels-landing-pages.md#lp-subdomains): configura un sottodominio dedicato all&#39;hosting delle pagine di destinazione.
* [Predefinito per pagina di destinazione](../admin/configure-channels-landing-pages.md#lp-presets) - Un predefinito definisce il sottodominio e le altre impostazioni applicate alle pagine di destinazione.
* [Modulo](./forms.md) (per casi di utilizzo di acquisizione dati): obbligatorio quando si desidera incorporare un modulo in una pagina di destinazione e inviare dati ad Experience Platform.
  <!-- * Subscription list (for subscription use cases) - Required if you want customers to subscribe to or unsubscribe from a specific service. This is in AJO B2C-->

>[!ENDSHADEBOX]

## Creare una pagina di destinazione {#create-landing-page}

>[!CONTEXTUALHELP]
>id="ajo-b2b_lp_create"
>title="Definire e configurare la pagina di destinazione"
>abstract="Per creare una pagina di destinazione, devi selezionare un predefinito; configurare la pagina principale e le pagine secondarie; e infine verificare la pagina prima di pubblicarla."

1. Vai alla navigazione a sinistra e seleziona **[!UICONTROL Gestione contenuto]** > **[!UICONTROL Pagine di destinazione]**.

1. Fai clic su **[!UICONTROL Crea pagina di destinazione]** in alto a destra.

1. Nella pagina, immetti un **[!UICONTROL Titolo]** (obbligatorio) e **[!UICONTROL Descrizione]** (facoltativo) utili.

   Criteri di titolo e descrizione:

   * Titolo: massimo 100 caratteri, deve essere univoco, senza distinzione tra maiuscole e minuscole

   * Descrizione: massimo 300 caratteri

   * Alpha, caratteri numerici e speciali sono consentiti

   * I caratteri riservati sono **_non consentiti_**: `\ / : * ? " < > |`

   ![Crea pagina di destinazione](./assets/landing-page-create.png){width="600"}

1. Seleziona un **[!UICONTROL predefinito]**.

   Un amministratore di prodotto [configura un predefinito](../admin/configure-channels-landing-pages.md#lp-presets) per definire il sottodominio e altre impostazioni utilizzate per le pagine di destinazione. È possibile selezionare un predefinito e quindi fare clic su **[!UICONTROL Visualizza predefinito]** per aprire i dettagli del predefinito e controllare le impostazioni per verificare che corrisponda ai requisiti della pagina di destinazione.

1. Fai clic su **[!UICONTROL Crea]**.

   Viene visualizzata la pagina principale e le relative proprietà.

   ![Nuova pagina di destinazione - proprietà pagina principale](./assets/landing-page-primary-new-properties.png){width="700" zoomable="yes"}

## Configurare la pagina principale {#configure-primary-page}

>[!CONTEXTUALHELP]
>id="ajo-b2b_lp_primary_page"
>title="Definire le impostazioni della pagina principale"
>abstract="Definisci la pagina principale, che viene visualizzata immediatamente quando un destinatario fa clic sul collegamento della pagina di destinazione, ad esempio da un’e-mail o da un sito web."

>[!CONTEXTUALHELP]
>id="ajo-b2b_lp_access_settings"
>title="Definire l’URL della pagina di destinazione"
>abstract="In questa sezione, definisci un URL univoco per la pagina di destinazione. Per la prima parte dell’URL, devi aver già impostato un sottodominio della pagina di destinazione come parte del predefinito selezionato."

1. Modifica il **[!UICONTROL Nome pagina]** in base alle tue esigenze, che per impostazione predefinita è _Pagina principale_.

1. Definisci la parte finale dell’URL della pagina.

   Il predefinito selezionato determina la prima parte dell’URL.

   >[!CAUTION]
   >
   >L’URL della pagina di destinazione deve essere univoco.
   >
   >Non puoi accedere alla pagina di destinazione semplicemente copiando e incollando questo URL in un browser web, anche se pubblicato. Testalo utilizzando la funzione di anteprima.

1. Se desideri una pagina di destinazione anonima, disabilita l&#39;opzione **[!UICONTROL Richiedi utenti identificati]**.

   <!-- The option 'Require identified users' would be visible in both AJO & AJOB2B when the Landing page is of type 'Data capture' -->

1. Fai clic sull&#39;icona _Calendario_ ( ![Icona Calendario](../assets/do-not-localize/icon-calendar.svg) ) per impostare la **[!UICONTROL Scadenza pagina]**.

   Dopo aver selezionato una data di scadenza, scegli l’azione alla scadenza della pagina:

   * **[!UICONTROL URL di reindirizzamento]** - Immettere l&#39;URL della pagina da utilizzare come reindirizzamento.

     ![Scadenza pagina di destinazione - URL di reindirizzamento](./assets/landing-page-expiry-redirect-url.png){width="400"}

     <!-- * **[!UICONTROL Custom page]** - Configure a subpage and select it from the list. -->
   * **[!UICONTROL Errore del browser]** - Immettere il testo dell&#39;errore da visualizzare al posto della pagina.

     ![Scadenza pagina di destinazione - errore del browser](./assets/landing-page-expiry-browser-error.png){width="400"}

## Scegli il tipo di progettazione del contenuto {#choose-design-type}

Per aggiungere il _[!UICONTROL contenuto]_ per la pagina, fare clic su **[!UICONTROL Apri Designer]**. La home page di _[!UICONTROL Crea la pagina di destinazione principale]_ viene caricata e il processo di progettazione inizia scegliendo come avviare la progettazione:

* [[!UICONTROL Progetta da zero]](#design-from-scratch)
* [[!UICONTROL Crea il tuo codice]](#code-your-own)
* [[!UICONTROL Importa HTML]](#import-html)
* [Utilizzare un modello di pagina di destinazione](#select-template)

![Scegli come iniziare la progettazione della pagina di destinazione](./assets/landing-page-create-design.png){width="800" zoomable="yes"}

Dopo aver selezionato il metodo preferito per avviare la progettazione della pagina di destinazione, utilizzare gli strumenti di progettazione visiva per [completare il contenuto della pagina](./landing-page-design.md).

### Creare da zero {#design-from-scratch}

Utilizza l’editor di contenuto visivo per definire la struttura del contenuto della pagina di destinazione. Aggiungendo e spostando componenti strutturali con semplici azioni di trascinamento della selezione, puoi progettare la forma del contenuto della pagina in pochi secondi.

1. Dalla home page _[!UICONTROL Crea la pagina di destinazione principale]_, seleziona l&#39;opzione **[!UICONTROL Progetta da zero]**.

1. Scegli come gestire lo stile per il contenuto della pagina:

   * **[!UICONTROL Usa temi]** - Scegliere questa opzione per creare il contenuto della pagina in _modalità tema_. In questa modalità è possibile utilizzare un [tema marchio](./brand-themes.md) definito per semplificare il processo di authoring dei contenuti e assicurarsi che la progettazione sia allineata agli standard definiti.

   * **[!UICONTROL Stile manuale]** - Scegliere questa opzione per creare il contenuto della pagina in _Modalità manuale_. In questa modalità, puoi impostare manualmente lo stile per tutti i componenti di struttura e contenuto aggiunti all’area di lavoro vuota.

1. Fai clic su **[!UICONTROL Conferma]**.

1. [Aggiungi struttura e contenuto](./landing-page-design.md#structure-content-landing-page) alla pagina.

### Crea il codice {#code-your-own}

_Crea un codice personalizzato_ ti consente di scrivere o incollare HTML non elaborato per creare il contenuto della pagina direttamente nello spazio di progettazione. Utilizzare questa modalità quando è necessario il controllo completo del markup. L’utilizzo di questa modalità richiede specifiche competenze HTML.

Dopo aver scelto questa modalità, rimani nell’editor di codice e non puoi passare all’editor visivo.

1. Dalla home page _[!UICONTROL Crea la pagina di destinazione principale]_, seleziona l&#39;opzione **[!UICONTROL Crea il codice]**.

1. Immetti o incolla il codice HTML non elaborato.

Se vuoi cancellare il contenuto della pagina e iniziare da una nuova progettazione, seleziona **[!UICONTROL Cambia progettazione]** dal menu delle opzioni.

### Importa HTML {#import-html}

Adobe Journey Optimizer B2B edition consente di importare contenuti HTML esistenti per progettare le pagine di destinazione.

{{$include /help/_includes/content-design-import.md}}

![Importa contenuto HTML in un file zip](./assets/templates-import-zip-file.png){width="500"}

>[!NOTE]
>
>L’utilizzo di un tag `<table>` come primo livello in un file HTML può causare la perdita di stile, incluse le impostazioni di sfondo e larghezza nel tag del livello superiore.

Puoi personalizzare il contenuto importato in base alle esigenze con lo spazio di progettazione visiva.

### Seleziona un modello {#select-template}

[!BADGE Beta]{type=Informative tooltip="Funzione Beta"}

Se desideri utilizzare un modello di pagina di destinazione, puoi scegliere tra:

* **Modelli di esempio**. L’interfaccia B2B edition di Journey Optimizer offre una raccolta di modelli di pagina di destinazione pronti all’uso che puoi utilizzare come punto di partenza per la progettazione della pagina di destinazione.

* **Modelli salvati**. Utilizza un modello personalizzato salvato creato da un membro dell&#39;organizzazione utilizzando il menu _[!UICONTROL Modelli]_ <!-- or the _[!UICONTROL Save as content template]_ option when designing a landing page. -->

Utilizza la sezione _[!UICONTROL Seleziona modello struttura]_ per iniziare a creare il contenuto da un modello. Puoi utilizzare un modello di esempio o un modello di pagina di destinazione personalizzato salvato dall’istanza di Journey Optimizer B2B edition.

>[!BEGINTABS]

>[!TAB Modelli salvati]

Nella home page di _Crea pagina di destinazione principale_ viene visualizzata la scheda _Modelli di esempio_ per impostazione predefinita. Per utilizzare un modello personalizzato, selezionare la scheda **[!UICONTROL Modelli salvati]**.

Viene visualizzato l’elenco di tutti i modelli di pagina di destinazione salvati. Puoi ordinarli per _[!UICONTROL Nome]_, _[!UICONTROL Ultima modifica]_ e _[!UICONTROL Ultima creazione]_.

![Scegli un modello salvato](./assets/landing-page-design-saved-templates-sort-by.png){width="700" zoomable="yes"}

Seleziona una miniatura modello per visualizzare un’anteprima. In modalità anteprima puoi spostarti tra tutti i modelli di una categoria (campione o salvato, a seconda della selezione) utilizzando le frecce destra e sinistra.

![Anteprima del modello salvato](./assets/landing-page-design-saved-template-preview.png){width="800" zoomable="yes"}

Quando la visualizzazione corrisponde a quella che si desidera utilizzare, fare clic su **[!UICONTROL Usa questo modello]** in alto a destra nella finestra di anteprima.

Questa azione copia il contenuto nello spazio di progettazione visiva, dove puoi modificarlo in base alle esigenze.

<!-- 
>[!NOTE]
>
>Saved templates may have governance (content locking) settings applied to one or more components. The design tools provide guidelines about locked components when you [author content from a governed template](./email-authoring-governance.md). 
-->

>[!TAB Modelli di esempio]

Adobe Journey Optimizer B2B edition offre una selezione di _modelli predefiniti_ di pagina di destinazione, che possono essere utilizzati per creare pagine di destinazione e modelli di pagina di destinazione personalizzati.

<!-- ![Choose a sample template provided by Adobe](../assets/content-design-shared/templates-design-samples.png){width="800" zoomable="yes"} -->

>[!ENDTABS]

## Controllare gli avvisi {#check-alerts}

Quando progetti il contenuto di una pagina di destinazione, gli avvisi vengono visualizzati in alto a destra quando mancano le impostazioni chiave.

![Avvisi per problemi di contenuto della pagina](./assets/alerts-button.png){width="250"}

Se non trovi questo pulsante, non sono stati rilevati problemi.

Esistono due tipi di avvisi:

* **_Avvisi_** che fanno riferimento a consigli e best practice, ad esempio:

   * `Placeholder links are present in the landing page body`: non dimenticare di sostituire i segnaposto con collegamenti validi.

   * `Text version of HTML is empty`: non dimenticare di definire una versione testuale del corpo della pagina, che viene utilizzata quando non è possibile visualizzare il contenuto HTML.

   * `Empty link is present in page body`: verificare che tutti i collegamenti nella pagina siano corretti.

* **_Errori_** che impediscono di testare o attivare il percorso o la campagna finché non vengono risolti, ad esempio:

   * `The landing page content is empty`: contenuto pagina obbligatorio.

## Verificare la pagina di destinazione {#test-landing-page}

>[!CONTEXTUALHELP]
>id="ajo-b2b_preview_lp_profiles"
>title="Visualizzare l’anteprima e testare la pagina di destinazione"
>abstract="Una volta definite le impostazioni e il contenuto della pagina di destinazione, utilizza i profili di test per visualizzare in anteprima la pagina."

Una volta definiti le impostazioni e il contenuto della pagina di destinazione, puoi utilizzare i profili di test per visualizzare l’anteprima della pagina. Se hai inserito [contenuti personalizzati](./personalization.md), puoi verificare come vengono visualizzati nella pagina di destinazione utilizzando i dati del profilo di test.

>[!PREREQUISITES]
>
>Per visualizzare in anteprima e verificare le pagine di destinazione, devi disporre dell&#39;autorizzazione **[!UICONTROL Pubblica messaggi]** e di un set di dati definito contenente [profili di test](../audiences/test-profiles.md).

1. Fai clic su **[!UICONTROL Anteprima e test]** per aprire la selezione del profilo di test.

   >[!NOTE]
   >
   >È inoltre possibile utilizzare **[!UICONTROL Simula contenuto]** nello spazio di progettazione visiva.

1. Dalla schermata _[!UICONTROL Simula]_, seleziona un profilo di test.

   ![Simula contenuto pagina di destinazione per il profilo selezionato](./assets/landing-page-simulate.png){width="700" zoomable="yes"}

   Se i profili necessari non sono elencati, fare clic su **[!UICONTROL Gestisci profili di test]** per utilizzare un indirizzo di posta elettronica [profilo di test](../audiences/test-profiles.md) noto e aggiungerlo all&#39;elenco.

   +++Aggiungere profili di test

   Per **[!UICONTROL Spazio dei nomi identità]**, fai clic sull&#39;icona _Seleziona_ ( ![Seleziona icona](../assets/do-not-localize/icon-select-data.svg) ) e scegli lo spazio dei nomi `Email` da utilizzare per testare i profili.

   ![Gestione dei profili di test impostati Spazio dei nomi identità e-mail](./assets/manage-test-profiles.png){width="700" zoomable="yes"}

   Nel campo **[!UICONTROL Valore identità]** immettere l&#39;indirizzo di posta elettronica per identificare il profilo di test e fare clic su **[!UICONTROL Aggiungi profilo]**. Puoi ripetere questa operazione per aggiungere più profili.

   ![Gestire i profili di test e aggiungere i profili](./assets/manage-test-profiles-add.png){width="700" zoomable="yes"}

   Fai clic sulla freccia indietro in alto a sinistra per tornare alla pagina _[!UICONTROL Simula]_.

   +++

1. Seleziona **[!UICONTROL Apri anteprima]** per verificare la pagina di destinazione.

   L’anteprima della pagina di destinazione viene visualizzata in una nuova scheda. I dati del profilo di test selezionati sostituiscono gli elementi personalizzati.

   ![Anteprima della pagina di destinazione con i dati del profilo](assets/landing-page-preview.png){width="600"}

1. Seleziona altri profili di test per visualizzare in anteprima il rendering per ogni variante della pagina di destinazione.

## Pubblicare la pagina {#publish-landing-page}

>[!PREREQUISITES]
>
>Per pubblicare le pagine di destinazione, devi disporre dell&#39;autorizzazione **[!UICONTROL Pubblica messaggi]**.  Prima di pubblicare, [verifica e risolvi tutti gli avvisi](#check-alerts).

Quando la pagina della bozza soddisfa i criteri e desideri renderla disponibile per il collegamento dai messaggi di percorso, fai clic su **[!UICONTROL Pubblica]** in alto a destra. Nella finestra di dialogo di conferma, fai clic su **[!UICONTROL Pubblica]**.

![Finestra di dialogo di conferma per la pubblicazione](./assets/landing-page-publish-confirm.png){width="250"}

Quando la pagina di destinazione viene pubblicata, viene visualizzata nell&#39;elenco delle pagine di destinazione con lo stato **_[!UICONTROL Pubblicato]_**. Ciò significa che è attivo e pronto per essere utilizzato in un messaggio e-mail, SMS o WhatsApp inviato tramite un percorso.

Non puoi accedere alla pagina di destinazione pubblicata copiando e incollando l’URL in un browser web. Puoi testarlo in qualsiasi momento utilizzando la [funzione di anteprima](#test-landing-page).

Puoi monitorare l’impatto della pagina di destinazione tramite rapporti specifici.
