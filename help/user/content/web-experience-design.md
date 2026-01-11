---
title: Progettazione esperienza web
description: 'Progetta esperienze web con editor visivi e non visivi: aggiungi modifiche, gestisci aggiornamenti dei contenuti, abilita il tracciamento dei clic e personalizza i contenuti in Journey Optimizer B2B edition.'
feature: Content Design Tools, Channels
role: User
badgeBeta: label="Beta" type="informative" tooltip="Questa funzione è attualmente in versione beta limitata"
source-git-commit: d01f4c14f72ebf78b10e4fc6691df42707bedb47
workflow-type: tm+mt
source-wordcount: '2333'
ht-degree: 0%

---

# Progettazione esperienza web

Dopo aver [creato un&#39;esperienza Web](./web-experiences.md#create-a-web-experience), utilizza lo spazio di progettazione del contenuto per definire le modifiche da applicare alle pagine Web.

>[!BEGINSHADEBOX]

**Prerequisiti**

Prima di poter progettare esperienze web, assicurati di soddisfare i seguenti requisiti:

* Un amministratore di prodotto ha configurato uno o più canali web per definire gli URL (pagine) da includere per un’esperienza web. Per ulteriori informazioni, vedere [Configurazioni del canale Web](../admin/configure-channels-web.md).

* Il sito Web include [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/en/docs/experience-platform/collection/js/js-overview) (`alloy.js`) implementato per l&#39;identificazione dei visitatori e la distribuzione dei contenuti. È richiesto Adobe Experience Platform Web SDK versione 2.16 o successiva.

* Hai le [autorizzazioni](../admin/user-management.md#b2b-product-permissions) necessarie per creare e gestire esperienze Web in un percorso:
   * _[!UICONTROL Campagne]_ > _[!UICONTROL Gestisci campagne]_ - Necessario per aggiungere o aggiornare un nodo di azione di personalizzazione Web.
   * _[!UICONTROL Campagne]_ > _[!UICONTROL Visualizza campagne]_ - Necessario per visualizzare i dettagli dei nodi di un&#39;azione di personalizzazione Web.

>[!ENDSHADEBOX]

>[!IMPORTANT]
>
>Prima di progettare un’esperienza web, accertati di aver installato l’estensione del browser Adobe Experience Cloud Visual Editing Helper per il browser web. Questa estensione è necessaria per aprire, creare e visualizzare in anteprima le pagine Web in modo affidabile nello spazio di progettazione di Journey Optimizer B2B edition Web Experience.<br/>
>
>Google Chrome e Microsoft Edge sono attualmente gli unici browser che supportano l’estensione e l’authoring di esperienze web in Journey Optimizer B2B edition. Per ulteriori informazioni, vedere [Installare l&#39;estensione Helper per editing video](./web-experiences.md#install-the-visual-editing-helper-extension).

## Editor esperienza web

Journey Optimizer B2B edition fornisce due tipi di editor per la progettazione di modifiche Web:

| Editor | Descrizione | Ideale per |
| ------ | ----------- | -------- |
| [Editor visivo](#visual-editor) | Un editor di WYSIWYG (_What You See Is What You Get_) che visualizza il sito Web e consente di selezionare e modificare direttamente gli elementi. Richiede l&#39;estensione [Helper per editing video](./web-experiences.md#install-the-visual-editing-helper-extension) nel browser Web Google Chrome o Microsoft Edge. | Apportare modifiche visive agli elementi visibili della pagina, ad esempio testo, immagini, pulsanti e banner. |
| [Editor non visivo](#non-visual-editor) | Un editor basato su codice per applicare modifiche che non possono essere apportate tramite l’editor visivo. | Esecuzione del targeting di elementi difficili da selezionare visivamente, applicazione di modifiche CSS avanzate o modifica di elementi nascosti. |

Nelle proprietà dell&#39;esperienza Web, utilizza l&#39;opzione **[!UICONTROL Editor visivo]** per determinare il tipo di editor. Abilita l’opzione per utilizzare l’editor visivo o disabilitala per utilizzare l’editor non visivo.

![Opzione editor visivo abilitata](./assets/web-experience-design-visual-editor-option.png){width="400"}

## Editor visivo {#visual-editor}

>[!CONTEXTUALHELP]
>id="ajo-b2b_web_experience_browse"
>title="Utilizzare la modalità Sfoglia"
>abstract="In questa modalità, puoi passare alla pagina esatta da personalizzare per la configurazione del canale web selezionato."

L’editor visivo carica le pagine web all’interno di un iframe, dove puoi selezionare gli elementi e applicare le modifiche direttamente nell’anteprima della pagina. Completa i seguenti passaggi per utilizzare l’editor visivo per progettare l’esperienza web:

1. Con la scheda _[!UICONTROL Contenuto]_ visualizzata nella pagina dei dettagli dell&#39;esperienza Web, fai clic su **[!UICONTROL Modifica esperienza Web]** nel pannello di destra.

   L’editor visivo carica il sito web in base alla configurazione del canale web.

   ![Editor visivo esperienza Web](./assets/web-experience-design-visual-editor.png){width="800" zoomable="yes"}

1. Se necessario, fai clic su **[!UICONTROL Sfoglia]** in alto a destra e utilizza la barra di navigazione del sito per caricare la pagina specifica da modificare.

   Puoi anche immettere l’URL della pagina nel campo nella parte superiore.

   >[!NOTE]
   >
   >Assicurati che la pagina caricata corrisponda ai pattern URL definiti nella configurazione del canale web. Fai clic su **[!UICONTROL Visualizza dettagli configurazione]** in alto a destra per visualizzare l&#39;URL o le regole di corrispondenza della pagina per la configurazione del canale Web selezionata.

   ![Modalità Sfoglia nell&#39;editor visivo](./assets/web-experience-design-visual-editor-browse.png){width="700" zoomable="yes"}

   <!-- If the web channel configuration is defined using page matching rules, use the left and right arrows to sequence through the matched pages -- right now these buttons don't do anything -->

   Fai clic su **[!UICONTROL Progettazione]** in alto a destra per caricare la pagina nello spazio di progettazione.

1. Per definire la modalità di modifica della pagina visualizzata per l’esperienza web, puoi:

   * [Inserire nuovi componenti](#insert-new-components) (divisore, HTML, immagine, intestazione, paragrafo o collegamento) nella pagina per l&#39;esperienza Web.

   * Seleziona un elemento esistente dalla pagina, ad esempio un&#39;immagine, un pulsante, un paragrafo, un testo, un contenitore, un&#39;intestazione o un collegamento, e [modificalo per l&#39;esperienza Web](#modify-elements).

   * [Aggiungi il tracciamento dei clic](#click-tracking-for-web-experiences) per gli elementi che misurano il coinvolgimento e raccolgono informazioni.

1. Ripeti il passaggio 2 per caricare altre pagine da includere nell’esperienza web e ripeti il passaggio 3 per definire le modifiche di pagina.

1. [Rivedi le modifiche](#manage-modifications) e apporta le modifiche necessarie.

1. Al termine delle modifiche, fai clic sulla freccia a sinistra sopra l’editor per tornare alle proprietà dell’esperienza web.

### Modificare gli elementi

Fai clic su un elemento nella pagina visualizzata per selezionarlo. Un bordo blu indica l’elemento selezionato e viene visualizzata una barra degli strumenti contestuale con opzioni di modifica.

![Selezionare un elemento da modificare](./assets/web-experience-design-select-element.png){width="700" zoomable="yes"}

Le opzioni della barra degli strumenti dipendono dal tipo di componente selezionato:

| Azione | Descrizione |
| ------ | ----------- |
| **[!UICONTROL Opzioni testo]** | Modifica la classe o lo stile del testo dell’elemento selezionato. |
| **[!UICONTROL Scegli immagine]** | Sostituisci l’origine dell’immagine o aggiungi un’immagine all’elemento. |
| **[!UICONTROL Modifica collegamento / Aggiungi collegamento]** | Modifica o aggiungi un URL di collegamento. |
| **[!UICONTROL Disponi]** | Sposta l&#39;elemento selezionato indietro o avanti all&#39;interno della visualizzazione. |
| **[!UICONTROL Aggiungere la personalizzazione]** | Inserire la personalizzazione. |
| **[!UICONTROL Elemento traccia clic]** | Aggiungi il tracciamento dei clic per l’elemento. |
| **[!UICONTROL Elimina]** | Rimuovi l’elemento selezionato dalla pagina. |

Per un elemento selezionato, le proprietà nel pannello di destra cambiano per riflettere lo stile e le azioni disponibili. Fai clic su un’icona di azione nella parte superiore del pannello per duplicare, tracciare, eliminare o nascondere l’elemento selezionato.

![fare clic sull&#39;icona di un&#39;azione per l&#39;elemento selezionato](./assets/web-experience-design-visual-editor-element-properties-icons.png){width="300"}

+++Elementi di testo

1. Seleziona un elemento di testo nella pagina.

1. Immettere il nuovo contenuto di testo oppure selezionare una stringa di testo e immettere il testo sostitutivo.

1. (Facoltativo) Utilizza le [opzioni di formattazione del testo](./content-components.md#text), ad esempio grassetto, corsivo e allineamento.

1. Fai clic all’esterno dell’elemento di testo per applicare la modifica.

Per ulteriori informazioni sulle opzioni di stile del testo per i componenti di testo, vedere [Componenti contenuto](./content-components.md#text).

+++

+++Elementi immagine

1. Seleziona un elemento immagine nella pagina.

1. Fai clic sull&#39;icona _[!UICONTROL Scegli immagine]_ nella barra degli strumenti contestuale o nel pannello di destra.

1. Sfoglia e seleziona un’immagine dalla libreria delle risorse.

1. Utilizza le [opzioni di stile immagine](./content-components.md#image) nel pannello di destra, in base alle esigenze.

+++

+++Elementi pulsante

1. Seleziona un elemento pulsante sulla pagina.

1. (Facoltativo) Immetti un nuovo testo per il pulsante oppure seleziona la stringa di testo e immetti il testo sostitutivo.

   Puoi utilizzare la personalizzazione per modificare il testo del pulsante utilizzando i dati dei profili dell’account o della persona.

1. Utilizza le [opzioni di stile del pulsante](./content-components.md#button) nel pannello di destra, in base alle esigenze.

+++

+++ Elementi contenitore

1. Seleziona un elemento contenitore nella pagina.

1. Utilizza le [opzioni di stile del contenitore](./content-components.md#container) nel pannello di destra, in base alle esigenze.

+++

### Inserire nuovi componenti

Quando si seleziona l&#39;icona **+** nella struttura di spostamento a sinistra dell&#39;editor visivo, è possibile aggiungere i seguenti tipi di componenti alla pagina come modifica dell&#39;esperienza Web:

* **[!UICONTROL Divisore]** - Utilizzare questo componente per inserire una linea di divisione per organizzare il layout e il contenuto dell&#39;e-mail. Potete regolare gli attributi di stile, ad esempio il colore della linea, lo stile e l&#39;altezza, dalle proprietà nel pannello di destra. Per ulteriori informazioni, vedere [Divider](./content-components.md#divider) in _Componenti contenuto_.
* **[!UICONTROL HTML]** - Utilizza questo componente per copiare e incollare il codice HTML nella struttura esistente. Consente di creare componenti HTML modulari gratuiti per riutilizzare alcuni contenuti esterni. Per ulteriori informazioni, vedere [HTML](./content-components.md#html) in _Componenti contenuto_.
* **[!UICONTROL Immagine]** - Utilizzare questo componente per inserire un file di immagine nella pagina. Potete regolare gli attributi di stile, ad esempio la larghezza e l&#39;altezza, dalle proprietà nel pannello di destra. Per ulteriori informazioni, vedere [Immagine](./content-components.md#image) in _Componenti contenuto_.
* **[!UICONTROL Intestazione]** - Utilizzare questo componente per inserire il testo della classe di intestazione. Potete regolare gli attributi di stile, ad esempio il colore del testo, lo stile, il font e le dimensioni, dalle proprietà nel pannello di destra. Per ulteriori informazioni, vedere [Testo](./content-components.md#text) in _Componenti contenuto_.
* **[!UICONTROL Paragrafo]** - Utilizzare questo componente per inserire un elemento di testo standard. Potete regolare gli attributi di stile, ad esempio il colore del testo, lo stile, il font e le dimensioni, dalle proprietà nel pannello di destra. Per ulteriori informazioni, vedere [Testo](./content-components.md#text) in _Componenti contenuto_.
* **[!UICONTROL Collegamento]** - Utilizzare questo componente per inserire un collegamento di testo autonomo a un URL specificato. Potete regolare gli attributi di stile, ad esempio il colore del testo, lo stile, l&#39;allineamento e le dimensioni, dalle proprietà nel pannello di destra.

Seleziona un tipo di componente a sinistra, quindi passa il cursore su un elemento adiacente al punto in cui desideri aggiungerlo.

![Interfaccia dell&#39;editor visivo - nuovo componente](./assets/web-experience-design-visual-editor-insert-component.png){width="800" zoomable="yes"}

Fai clic su uno dei pulsanti visualizzati per posizionare il componente:

* ***[!UICONTROL Inserisci prima]** - Inserisci il componente prima dell&#39;elemento selezionato.
* ***[!UICONTROL Inserisci dopo]** - Inserisci il componente dopo l&#39;elemento selezionato.

Per deselezionare un tipo di componente per l&#39;inserimento, fare clic su **[!UICONTROL ESC]** nel banner contestuale blu visualizzato nella parte superiore della pagina.

## Editor non visivo {#non-visual-editor}

Utilizza l’editor non visivo quando devi apportare modifiche che non possono essere facilmente apportate nell’editor visivo. Questo approccio basato su codice offre un controllo preciso sul targeting e sulla modifica degli elementi. Completa i seguenti passaggi per utilizzare l’editor non visivo per progettare l’esperienza web:

1. Con la scheda _[!UICONTROL Contenuto]_ visualizzata nella pagina dei dettagli dell&#39;esperienza Web, fai clic su **[!UICONTROL Aggiungi modifica]** nel pannello di destra.

   L’editor non visivo carica una pagina basata sulla configurazione del canale web.

   ![Interfaccia editor non visivo](./assets/web-experience-design-non-visual-editor.png){width="800" zoomable="yes"}

1. Definisci la prima modifica da apportare.

   Nel pannello laterale sinistro viene visualizzato un elenco delle eventuali modifiche esistenti. Fai clic su **[!UICONTROL Aggiungi]** per definire una nuova modifica. Se non sono state definite modifiche, il pannello utilizza per impostazione predefinita le opzioni _[!UICONTROL Aggiungi modifica]_.

   * Scegli il **[!UICONTROL tipo di modifica]**:

     | Tipo | Descrizione |
     | ---- | ----------- |
     | [**[!UICONTROL Selettore CSS]**](#css-selector-modifications) | Elementi di destinazione che utilizzano una stringa del selettore CSS. |
     | [**[!UICONTROL Pagina]**](#page-modifications) | Inserire HTML, CSS o JavaScript personalizzati negli elementi a livello di pagina, ad esempio `<head>` o `<body>`. |

   * Configura i parametri di modifica in base al tipo:

      * **[!UICONTROL Selettore CSS]** - Inserisci un selettore CSS valido per eseguire il targeting di elementi specifici.
      * **[!UICONTROL Tipo azione]** - Scegliere l&#39;azione da eseguire (modifica, nascondi, elimina, inserisci, sostituisci).
      * **[!UICONTROL Contenuto]** - Fornisci il contenuto o lo stile da applicare.

1. Fai clic su **[!UICONTROL Salva]** per applicare la modifica.

### Modifiche al selettore CSS

Le modifiche apportate al selettore CSS consentono di eseguire il targeting degli elementi con precisione utilizzando la sintassi standard del selettore CSS.

1. Scegli **[!UICONTROL Selettore CSS]** come tipo di modifica.

1. Immetti il selettore nel campo **[!UICONTROL Selettore elemento CSS]**.

<!-- This field helps you find and select the HTML elements (or nodes in the DOM tree). -->

    **Selettori di esempio:**
    
    | Selettore | Target |
    | -------- | ------- |
    | &quot;#hero-banner&quot; | Elemento con ID &quot;hero-banner&quot; |
    | `.cta-button` | Tutti gli elementi con la classe `cta-button` |
    | &quot;header nav a&quot; | Collegamenti all’interno della navigazione, all’interno dell’intestazione |
    | `[data-offer=&quot;premium&quot;]` | Elementi con un attributo di dati specifico |

1. Scegli un tipo di azione **&#x200B;**&#x200B;e specifica le informazioni o il contenuto richiesti.

   * **[!UICONTROL Imposta contenuto]** - Immettere il testo nel campo **[!UICONTROL Contenuto]** per l&#39;elemento identificato dal valore _[!UICONTROL Selettore elemento CSS]_.

   * **[!UICONTROL Imposta attributo]** - Specifica un attributo da associare al selettore CSS corrente in modo che l&#39;elemento possa essere identificato da questo attributo. Immettere un nome nel campo **[!UICONTROL Nome attributo]** e un valore nel campo **[!UICONTROL Contenuto]**. Se l&#39;attributo esiste già, il valore viene aggiornato; in caso contrario, viene aggiunto un nuovo attributo con il nome e il valore specificati.

   ![Modifica del selettore CSS dell&#39;editor non visivo](./assets/web-experience-design-non-visual-editor-modification-css-selector.png){width="800" zoomable="yes"}

1. (Facoltativo) Fai clic su **[!UICONTROL Aggiungi personalizzazione]** e utilizza l&#39;[editor di personalizzazione](./personalization.md#personalization-editor) per creare una personalizzazione personalizzata per il contenuto.

### Modifiche pagina

È possibile aggiungere codice personalizzato utilizzando il tipo di modifica Pagina `<head>`. L&#39;elemento `<head>` è un contenitore per metadati (dati sui dati) e si trova tra il tag `<html>` e il tag `<body>`. In questo caso, il codice non attende gli eventi di caricamento del corpo del testo o della pagina, ma viene eseguito all’inizio del caricamento della pagina.

L&#39;elemento `<head>` viene comunemente utilizzato per aggiungere codice JavaScript o CSS nella parte superiore della pagina. I selettori per le azioni visive successive dipendono dagli elementi HTML aggiunti in questa scheda.

>[!NOTE]
>
>Il codice personalizzato viene eseguito nel browser del visitatore. Assicurati che il codice sia sicuro, testato e non influisca negativamente sulle prestazioni della pagina o sull’esperienza utente.

1. Scegliere **[!UICONTROL Pagina`<head>`]** come tipo di modifica.

1. Aggiungi il codice personalizzato nella casella **[!UICONTROL Contenuto]**.

   >[!CAUTION]
   >
   >È possibile aggiungere solo `<script>` e `<style>` elementi alla sezione `<head>`. L&#39;aggiunta di `<div>` tag e di altri elementi potrebbe causare il popolamento di `<head>` elementi rimanenti all&#39;interno di `<body>`.

   ![Modifica intestazione pagina editor non visivo](./assets/web-experience-design-non-visual-editor-modification-page-head.png){width="800" zoomable="yes"}

1. (Facoltativo) Fai clic su **[!UICONTROL Aggiungi personalizzazione]** e utilizza l&#39;[editor di personalizzazione](./personalization.md#personalization-editor) per creare una personalizzazione personalizzata per il contenuto.

## Gestire le modifiche {#manage-modifications}

>[!CONTEXTUALHELP]
>id="ajo-b2b_web_experience_modifications"
>title="Gestire con facilità tutte le modifiche"
>abstract="Utilizzando questo riquadro, puoi navigare e gestire tutte le regolazioni e le aggiunte definite per la pagina web."

Tutte le modifiche create vengono tracciate e possono essere gestite dal pannello **[!UICONTROL Modifiche]** dell&#39;editor visivo e dell&#39;editor non visivo. Fai clic sull&#39;icona _[!UICONTROL Modifiche]_ <!-- ( ![Modifications icon](../assets/do-not-localize/icon-web-exp-modifications.svg) ) -->nella barra degli strumenti a sinistra per visualizzare tutte le modifiche.

Ogni record di modifica include:

* L’elemento o il selettore di destinazione
* Il tipo di modifica (ad esempio modifica, nascondi o inserisci)
* Anteprima della modifica

![Pannello modifiche](./assets/web-experience-design-modifications-list.png){width="500" zoomable="yes"}

### Modificare una modifica

1. Nell&#39;elenco _[!UICONTROL Modifiche]_ trovare la modifica che si desidera modificare.

1. Fai clic sull&#39;icona _Altro menu_ ( **...** ) e scegli **[!UICONTROL Modifica]**.

1. Aggiorna le proprietà di modifica in base alle esigenze.

1. Fai clic su **[!UICONTROL Salva]** per salvare le modifiche.

### Eliminare una modifica

1. Nell&#39;elenco _[!UICONTROL Modifiche]_ trovare la modifica che si desidera rimuovere.

1. Fai clic sull&#39;icona _Altro menu_ ( **...** ) e scegli **[!UICONTROL Elimina modifica]**.

1. Quando richiesto, confermare la rimozione.

<!-- ### Reorder modifications

Modifications are applied in the order that they appear in the list. If you have multiple modifications that affect the same element, the order may impact the final result.

Drag and drop modifications in the list to change the order. The preview updates to reflect the new modification order. -->

## Anteprima delle modifiche

Prima della pubblicazione, visualizza in anteprima come vengono visualizzate le modifiche ai visitatori.

Utilizza le opzioni di anteprima del dispositivo nella parte superiore dell’editor visivo per visualizzare le modifiche su:

* Desktop
* Tablet
* Dispositivi mobili

![Modifica il dimensionamento del dispositivo per l&#39;anteprima](./assets/web-experience-design-device-view.png){width="550" zoomable="yes"}

L’anteprima viene aggiornata per mostrare il rendering delle modifiche su ogni dimensione del dispositivo.

Utilizza la barra URL per passare a pagine diverse all’interno della configurazione del canale web. Quindi, verifica che le modifiche vengano applicate correttamente alle pagine di destinazione in base alle regole di corrispondenza URL.

## Tracciamento dei clic per esperienze web {#web-click-tracking}

Tieni traccia delle interazioni dell’utente con gli elementi per misurare il coinvolgimento e raccogliere informazioni approfondite. I dati di tracciamento dei clic sono disponibili nei rapporti di coinvolgimento e possono essere utilizzati per misurare l’efficacia delle modifiche apportate all’esperienza web.

Quando la tua esperienza web è attivata (dal vivo), puoi anche creare rapporti utilizzando Adobe Customer Journey Analytics (che richiede un abbonamento al prodotto). Per migliorare il monitoraggio dell’esperienza web, puoi anche tenere traccia dei clic su qualsiasi elemento specifico del sito web. Il tracciamento ti consente di visualizzare il numero di clic per tale elemento nei rapporti web.

Per ulteriori informazioni su Customer Journey Analytics e sulla creazione di report Web, consulta la [documentazione di Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-landing).

1. Seleziona un elemento nell’editor esperienze web, ad esempio un’immagine o un collegamento.

1. Nella barra degli strumenti contestuale o delle proprietà dell&#39;elemento fare clic sull&#39;icona _[!UICONTROL Fai clic su elemento traccia]_.

   ![Abilita il tracciamento dei clic per gli elementi esperienza Web](./assets/web-experience-design-visual-editor-click-tracking-icons.png){width="600" zoomable="yes"}

1. Apri l&#39;elenco dei brani per clic nel pannello a sinistra e modifica il valore **[!UICONTROL Azioni tracciate]** per identificare questa interazione nei rapporti.

   ![Imposta l&#39;identificazione del tracciamento dei clic per l&#39;esperienza Web](./assets/web-experience-design-visual-editor-click-tracking-identifier.png){width="600" zoomable="yes"}
