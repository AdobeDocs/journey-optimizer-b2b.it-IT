---
title: Frammenti
description: Scopri come creare e utilizzare frammenti di contenuto visivo come componenti riutilizzabili per e-mail e modelli e-mail in Adobe Journey Optimizer B2B Edition.
feature: Content, Email Authoring
exl-id: 3c1d2ca0-d009-4a2a-9d81-1a838845b7fa
source-git-commit: 8e55e4444a363a5699574c2fa1ed256fdb690dd0
workflow-type: tm+mt
source-wordcount: '1849'
ht-degree: 2%

---

# Frammenti

Un frammento è un componente riutilizzabile a cui è possibile fare riferimento in una o più e-mail e modelli e-mail in Adobe Journey Optimizer B2B Edition. In genere si tratta di un blocco di contenuto (testo, immagine o entrambi) che può essere precreato e inserito rapidamente in un modello e-mail o e-mail. Con questa funzionalità, puoi precreare più blocchi di contenuto personalizzati da utilizzare da parte dei membri del team di marketing per assemblare contenuti e-mail e migliorare così il processo di progettazione. I casi d’uso comuni includono blocchi di contenuto di intestazione/piè di pagina per e-mail, banner di invito per eventi e saluti stagionali.

Per utilizzare al meglio i frammenti nei flussi di lavoro:

* _Crea frammenti personalizzati_ - Crea frammenti visivi da zero o salvando il contenuto come frammento dall&#39;editor di contenuti visivi.
* _Riutilizza frammenti_ - Puoi utilizzarli nel contenuto per il numero di volte necessario.

## Frammenti visivi

I frammenti visivi sono blocchi visivi predefiniti creati utilizzando l’editor di contenuto visivo che puoi riutilizzare in più e-mail o modelli e-mail. L’ambito corrente di Journey Optimizer B2B Edition e questa documentazione sono quelli dei soli frammenti visivi. I frammenti basati su espressioni non sono ancora supportati in Journey Optimizer B2B Edition.

## Accedere e gestire i frammenti

Per accedere ai frammenti visivi in Adobe Journey Optimizer B2B Edition, vai alla navigazione a sinistra e fai clic su **[!UICONTROL Gestione contenuto]** > **[!UICONTROL Frammenti]**. Questa azione apre una pagina di elenco con tutti i frammenti creati nell’istanza elencata in una tabella.

![Accedere alla libreria frammenti](./assets/fragments-list.png){width="700" zoomable="yes"}

La tabella è ordinata in base alla colonna _[!UICONTROL Modificato]_, con i frammenti aggiornati più di recente nella parte superiore per impostazione predefinita. Fai clic sul titolo della colonna per passare da crescente a decrescente.

Per cercare un frammento in base al nome, immetti una stringa di testo nella barra di ricerca per trovare una corrispondenza. Fai clic sull&#39;icona _Filtro_ per filtrare gli elementi visualizzati in base ai criteri specificati.

![Filtra i frammenti visualizzati](./assets/fragments-list-filtered.png){width="700" zoomable="yes"}

Personalizzare le colonne da visualizzare nella tabella facendo clic sull&#39;icona _Personalizza tabella_ in alto a destra. Selezionare le colonne da visualizzare e fare clic su **[!UICONTROL Applica]**.

## Creare i frammenti

È possibile creare nuovi frammenti visivi in Journey Optimizer B2B Edition facendo clic su **[!UICONTROL Crea frammento]** in alto a destra.

1. Nella finestra di dialogo _[!UICONTROL Crea frammento]_, immetti un **[!UICONTROL Nome]** e una **[!UICONTROL Descrizione]** utili (facoltativi).

   Requisiti dei frammenti:

   * Nome: massimo 100 caratteri, deve essere univoco, senza distinzione tra maiuscole e minuscole

   * Descrizione: massimo 300 caratteri

   * Sono consentiti caratteri Alpha, numerici e speciali

   * I caratteri riservati sono **_non consentiti_**: `\ / : * ? " < > |`

   ![Finestra di dialogo Crea frammento](./assets/assets-fragments-create-dialog.png){width="400"}

1. Fai clic su **[!UICONTROL Crea]**.

   L’editor di contenuto visivo si apre con un’area di lavoro vuota.

<!-- To be linked to the corresponding sections on this page: Adobe Journey Optimizer B2B Edition - Email Templates

Adding structure and content
Adding assets
Navigating the layers
Previewing & editing URLs
View options
More options -->

### Aggiungere struttura e contenuto {#design-fragment}

>[!CONTEXTUALHELP]
>id="ajo-b2b_structure_components_fragment"
>title="Aggiungere i componenti Struttura"
>abstract="I componenti della struttura definiscono il layout del frammento. Per iniziare a progettare il contenuto del frammento, trascina un componente **Struttura** nell’area di lavoro."

>[!CONTEXTUALHELP]
>id="ajo-b2b_content_components_fragment"
>title="Informazioni sui componenti per contenuti"
>abstract="I componenti di contenuto sono segnaposto di contenuto vuoti che possono essere utilizzati per creare il layout di un frammento."

{{$include /help/_includes/content-design-components.md}}

### Aggiungere risorse

{{$include /help/_includes/content-design-assets.md}}

### Spostarsi tra livelli, impostazioni e stili

{{$include /help/_includes/content-design-navigation.md}}

### Personalizzare il contenuto

{{$include /help/_includes/content-design-personalization.md}}

### Modifica tracciamento URL collegato

{{$include /help/_includes/content-design-links.md}}

## Visualizza dettagli frammento

Fai clic sul nome di un frammento nella pagina dell’elenco per aprire la pagina dei dettagli del frammento. Puoi scegliere di modificare il frammento, rinominarlo o aggiornare la descrizione del frammento. Per salvare automaticamente le modifiche, apporta gli aggiornamenti e fai clic all’esterno del campo nome o descrizione.

>[!NOTE]
>
>Se un frammento pubblicato è utilizzato da un’e-mail o da un modello e-mail, non puoi modificare il nome o il contenuto. Puoi creare una versione bozza se desideri apportare modifiche al frammento.

![Visualizza dettagli per un frammento pubblicato](./assets/fragment-details-published.png){width="600" zoomable="yes"}

Fai clic su **[!UICONTROL Modifica frammento]** per aprire il frammento nell&#39;editor di contenuti visivi.

Uscire dalla visualizzazione in qualsiasi momento facendo clic sulla freccia _Indietro_ in alto a sinistra, per tornare alla pagina dell&#39;elenco _Frammenti_.

## Visualizza frammento utilizzato da riferimenti

Nella pagina dei dettagli del frammento, fai clic sulla scheda **[!UICONTROL Usato da]** per visualizzare i dettagli sulla posizione in cui il frammento è attualmente utilizzato in Journey Optimizer B2B Edition, tra e-mail, modelli e frammenti di posta elettronica.

>[!IMPORTANT]
>
>Non è possibile eliminare i frammenti attualmente utilizzati da e-mail o modelli e-mail.

I riferimenti vengono visualizzati in base alla categoria: _E-mail_ o _Modello e-mail_. Le e-mail in Journey Optimizer B2B Edition sono incorporate e create all’interno di percorsi di account, pertanto il percorso principale dell’e-mail che utilizza il frammento viene visualizzato in riferimenti.

![Utilizzato dai riferimenti per il frammento](./assets/fragment-used-by-published.png){width="600" zoomable="yes"}

Fai clic sul collegamento per aprire l’e-mail o il modello e-mail corrispondente in cui viene utilizzato il frammento.

## Elimina frammenti

Qualsiasi frammento attualmente utilizzato da un messaggio e-mail o da un modello e-mail non può essere eliminato. Prima di avviare la rimozione di un frammento, assicurati di controllare i riferimenti a _usato da_. Inoltre, una rimozione non può essere annullata, pertanto controlla prima di avviare un’azione di eliminazione.

Puoi eliminare un frammento utilizzando uno dei seguenti metodi:

* Dai dettagli del frammento a destra, fai clic su **[!UICONTROL Elimina]**.
* Nella pagina dell&#39;elenco _[!UICONTROL Frammenti]_, fare clic sui puntini di sospensione accanto al frammento e scegliere **[!UICONTROL Elimina]**.

Questa azione apre una finestra di dialogo di conferma. È possibile interrompere il processo facendo clic su **[!UICONTROL Annulla]** oppure su **[!UICONTROL Elimina]** per confermare l&#39;eliminazione.

![Finestra di dialogo Elimina frammento](./assets/fragment-delete-dialog.png){width="400"}

Se il frammento è attualmente in uso, l’azione apre una finestra di dialogo informativa che avvisa che non è possibile eliminarlo. Fare clic su **[!UICONTROL OK]** per interrompere l&#39;azione di eliminazione.

![Finestra di dialogo Elimina frammento - impossibile eliminare il frammento in uso](./assets/fragment-delete-dialog-in-use.png){width="400"}

## Modificare i frammenti

Puoi modificare un frammento utilizzando uno dei seguenti metodi:

* Dai dettagli del frammento a destra, fai clic su **[!UICONTROL Modifica]**.
* Dalla pagina dell&#39;elenco _[!UICONTROL Frammenti]_, fai clic sui puntini di sospensione accanto al frammento e scegli **[!UICONTROL Modifica]**.

Questa azione consente di aprire il frammento in un editor di contenuti visivi, in cui è possibile modificare il frammento utilizzando una qualsiasi delle funzionalità per la [creazione di un frammento](#create-fragments).

## Frammenti duplicati

Puoi duplicare un frammento utilizzando uno dei seguenti metodi:

* Dalla pagina dell&#39;elenco _[!UICONTROL Frammenti]_, fai clic sull&#39;icona _Altro_ (**...**) accanto al nome del frammento e scegli **[!UICONTROL Duplica]**.
* Nella parte superiore destra della pagina dei dettagli del frammento, fare clic su **[!UICONTROL ... Altro]** e scegli **[!UICONTROL Duplicato]**.

![Duplica il frammento](./assets/fragment-details-duplicate.png){width="600" zoomable="yes"}

Nella finestra di dialogo, inserisci un nome utile (univoco) e una descrizione. Fai clic su **[!UICONTROL Duplica]** per completare l&#39;azione.

![Immettere un nome e una descrizione per il frammento duplicato](./assets/fragment-duplicate-dialog.png){width="400"}

Il frammento duplicato (nuovo) viene quindi visualizzato nell&#39;elenco _Frammenti_.

## Salvare un frammento da e-mail o contenuto del modello

Quando crei/modifichi un modello e-mail o e-mail nell’editor di contenuto visivo, puoi scegliere di salvare tutto o parte del contenuto come frammento in modo che sia disponibile per il riutilizzo.

1. Quando hai del contenuto da salvare come frammento, fai clic su **[!UICONTROL Altro]** e scegli **[!UICONTROL Salva come frammento]**.

1. Seleziona i diversi elementi da includere nel frammento.

   Selezionare più strutture tenendo premuto il pulsante Maiusc o Ctrl.

   È possibile selezionare solo strutture adiacenti e l&#39;interfaccia non consente di selezionare elementi non adiacenti.

1. Con il contenuto selezionato, fai clic su **[!UICONTROL Crea]** in alto a destra.

1. Nella finestra di dialogo, immetti un nome e una descrizione utili per il frammento. Quindi fare clic su **[!UICONTROL Crea]**.

   Il nuovo frammento viene quindi visualizzato nella pagina di elenco _Frammenti_ ed è disponibile anche all&#39;interno di e-mail e modelli di e-mail.

## Aggiungere frammenti visivi all’e-mail o al contenuto del modello

I frammenti sono progettati per il riutilizzo e possono essere inseriti per la creazione di modelli e-mail e e-mail. Puoi aggiungere fino a 30 frammenti in un messaggio e-mail o in un modello. I frammenti possono essere nidificati fino a un solo livello.

>[!BEGINTABS]

>[!TAB Aggiungere frammenti a un&#39;e-mail]

1. Passa a **[!UICONTROL Percorsi di account]** e apri un percorsi percorso esistente o creane uno nuovo.

1. Crea un nodo [_[!UICONTROL Invia e-mail ]_](./email-authoring.md#add-an-email-action-in-an-account-journey).

1. Crea o modifica [contenuto e-mail per il nodo](./email-authoring.md#create-the-email-content).

1. Trascina e rilascia un elemento dal menu **[!UICONTROL Componenti]** per fornire una _struttura_ per il frammento.

1. Per aprire l&#39;elenco dei frammenti pubblicati, fare clic sull&#39;icona _Frammenti_.

   Puoi eseguire le seguenti operazioni:
   * Ordina l’inserzione.
   * Sfoglia, cerca e filtra l’inserzione.
   * Passa dalla visualizzazione scheda (miniatura) a quella elenco e viceversa.
   * Aggiorna l’elenco per riflettere eventuali frammenti creati di recente.

   ![Cerca un frammento nella finestra di progettazione visiva](./assets/fragments-list-designer-search.png){width="600"}

1. Trascina e rilascia uno dei frammenti nel segnaposto del componente struttura.

   L’editor esegue il rendering del frammento all’interno della sezione/elemento della struttura e-mail.

Il contenuto del frammento viene aggiornato dinamicamente all’interno della struttura per eseguire il rendering di un’immagine del modo in cui il contenuto viene visualizzato nell’e-mail.

>[!TIP]
>
>Se desideri che il frammento occupi l&#39;intero layout orizzontale all&#39;interno del messaggio e-mail, aggiungi una struttura di [!UICONTROL 1:1 colonna], quindi trascina e rilascia il frammento al suo interno.

Dopo il salvataggio, l&#39;e-mail viene visualizzata nella pagina dei dettagli del frammento quando viene selezionata la scheda _[!UICONTROL Usato da]_. I frammenti aggiunti a un’e-mail non sono modificabili all’interno dell’e-mail o del modello; il frammento di origine pubblicato definisce il contenuto.

>[!TAB Aggiungere frammenti a un modello di e-mail]

1. Nel menu di navigazione a sinistra, fai clic su **[!UICONTROL Gestione contenuto]** > **[!UICONTROL Modelli]**.

1. Crea un nuovo modello o apri un modello e-mail esistente e fai clic su **[!UICONTROL Modifica modello e-mail]**.

1. Trascina e rilascia un elemento dal menu **[!UICONTROL Componenti]** per fornire una _struttura_ per il frammento.

1. Per aprire l&#39;elenco dei frammenti, fare clic sull&#39;icona _Frammenti_.

   Puoi eseguire le seguenti operazioni:
   * Ordina l’inserzione.
   * Sfoglia, cerca e filtra l’inserzione.
   * Passa dalla visualizzazione scheda (miniatura) a quella elenco e viceversa.
   * Aggiorna l’elenco per riflettere eventuali frammenti creati di recente.

   ![Cerca un frammento nella finestra di progettazione visiva](./assets/fragments-list-designer-search.png){width="600"}

1. Trascina e rilascia uno dei frammenti nel segnaposto del componente struttura.

   L’editor esegue il rendering del frammento all’interno della sezione/elemento della struttura del modello e-mail.

1. Trascina e rilascia uno dei frammenti nel segnaposto del componente struttura.

   L’editor esegue il rendering del frammento all’interno della sezione/elemento della struttura del modello e-mail.

>[!TIP]
>
>Se desideri che il frammento occupi l&#39;intero layout orizzontale all&#39;interno del modello e-mail, aggiungi una struttura di _[!UICONTROL 1:1 colonna]_, quindi trascina e rilascia il frammento al suo interno.

Dopo il salvataggio, il modello e-mail viene visualizzato nella pagina dei dettagli del frammento quando viene selezionata la scheda _[!UICONTROL Usato da]_. I frammenti aggiunti a un modello e-mail non sono modificabili all’interno del modello: il frammento di origine pubblicato definisce il contenuto.

>[!ENDTABS]

## Azioni sui frammenti durante l’authoring di e-mail e modelli

Quando un frammento viene aggiunto a un’e-mail o a un modello e-mail, non è possibile modificarne il contenuto all’interno dell’e-mail o del modello. Tuttavia, puoi applicare le seguenti azioni:

* **[!UICONTROL Elimina]** - Questa azione rimuove il frammento dal contenuto del modello e-mail o e-mail corrente (l&#39;origine del frammento non è interessata).
* **[!UICONTROL Aggiorna]** - Questa azione aggiorna il contenuto del frammento nel modello e-mail o e-mail corrente. L’aggiornamento è utile quando desideri riflettere eventuali modifiche recenti apportate al frammento dopo l’aggiunta all’e-mail o al modello e-mail.
* **[!UICONTROL Duplicato]** - Questa azione duplica il frammento all&#39;interno dello stesso e-mail o modello e-mail all&#39;interno dell&#39;editor, con le stesse dimensioni e aggiunto appena sotto di esso.
* **[!UICONTROL Apri frammento]** - Questa azione apre una nuova scheda del browser con la pagina e i dettagli dell&#39;editor frammenti.
* **[!UICONTROL Interrompi ereditarietà]** - Questa azione interrompe l&#39;ereditarietà del frammento (e delle relative modifiche) dall&#39;origine. Utilizza questa azione per rendere il contenuto del frammento disponibile come contenuto indipendente e modificabile all’interno del modello e-mail o e-mail. Questa azione rimuove anche il modello e-mail o e-mail dal riferimento _Usato da_ per il frammento originale.

Quando selezioni il frammento nella pagina dell’editor, queste azioni sono disponibili nella barra degli strumenti contestuale e nel pannello delle proprietà a destra.

![Applica azioni al frammento selezionato](./assets/fragment-actions-email-authoring.png){width="600" zoomable="yes"}