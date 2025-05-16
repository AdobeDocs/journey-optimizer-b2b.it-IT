---
title: Frammenti
description: Scopri come creare e utilizzare frammenti di contenuto visivo come componenti riutilizzabili per e-mail e modelli e-mail in Adobe Journey Optimizer B2B edition.
feature: Fragments, Content
role: User
exl-id: 3c1d2ca0-d009-4a2a-9d81-1a838845b7fa
source-git-commit: 4a54548ad061fc778fae3bc4b8499f3716850e4a
workflow-type: tm+mt
source-wordcount: '2624'
ht-degree: 2%

---

# Frammenti

Un frammento è un componente riutilizzabile a cui è possibile fare riferimento in uno o più e-mail e modelli e-mail in Adobe Journey Optimizer B2B edition. In genere si tratta di un blocco di contenuto (testo, immagine o entrambi) che può essere precreato e inserito rapidamente in un modello e-mail o e-mail. Con questa funzionalità, puoi precreare più blocchi di contenuto personalizzati da utilizzare da parte dei membri del team di marketing per assemblare contenuti e-mail e migliorare così il processo di progettazione. I casi d’uso comuni includono blocchi di contenuto di intestazione/piè di pagina per e-mail, banner di invito per eventi e saluti stagionali.

>[!BEGINSHADEBOX]

**Frammenti visivi**

I frammenti visivi sono blocchi visivi predefiniti creati mediante la finestra di progettazione del contenuto visivo che puoi riutilizzare in più e-mail o modelli e-mail. L’ambito corrente di Journey Optimizer B2B edition e di questa documentazione è quello dei soli frammenti visivi. I frammenti basati su espressioni non sono ancora supportati in Journey Optimizer B2B edition.

>[!ENDSHADEBOX]

Per utilizzare al meglio i frammenti nei flussi di lavoro:

* _Crea frammenti personalizzati_ - Crea frammenti visivi da zero o salvando il contenuto come frammento dall&#39;editor di contenuti visivi.
* _Riutilizza frammenti_ - Puoi utilizzarli nel contenuto per il numero di volte necessario.

## Accedere e gestire i frammenti

Per accedere ai frammenti visivi in Adobe Journey Optimizer B2B edition, vai alla navigazione a sinistra e fai clic su **[!UICONTROL Gestione contenuto]** > **[!UICONTROL Frammenti]**. Questa azione apre una pagina di elenco con tutti i frammenti creati nell’istanza elencata in una tabella.

![Accedere alla libreria frammenti](./assets/fragments-list.png){width="700" zoomable="yes"}

La tabella è ordinata in base alla colonna _[!UICONTROL Modificato]_, con i frammenti aggiornati più di recente nella parte superiore per impostazione predefinita. Fai clic sul titolo della colonna per passare da crescente a decrescente.

### Stato e ciclo di vita del frammento

Lo stato del frammento determina la sua disponibilità per l’utilizzo in un messaggio o in un modello e-mail e le modifiche che puoi apportarvi.

| Stato | Descrizione |
| -------------------- | ----------- |
| Bozza | Quando crei un frammento, questo si trova nello stato Bozza. Rimane in questo stato mentre definisci o modifichi il contenuto visivo fino a quando non lo pubblichi per l’utilizzo in un e-mail o in un modello e-mail. Azioni disponibili:<br/><ul><li>Modifica tutti i dettagli<li>Modifica in designer visivo<li>Pubblica<li>Duplica<li>Elimina |
| Pubblicato | Quando pubblichi un frammento, questo diventa disponibile per l’utilizzo in un’e-mail o in un modello e-mail. Il contenuto del frammento pubblicato non può essere modificato nella finestra di progettazione visiva. Azioni disponibili:<br/><ul><li>Modifica descrizione<li>Aggiungi a un messaggio e-mail o a un modello<li>Crea versione bozza<li>Duplica<li>Elimina (se non in uso) |
| Pubblicato con bozza | Quando crei una bozza da un frammento pubblicato, la versione pubblicata rimane disponibile per l’utilizzo in un modello e-mail o e-mail e il contenuto della bozza può essere modificato nella finestra di progettazione visiva. Se pubblichi la versione bozza, questa sostituisce la versione pubblicata corrente e il contenuto viene aggiornato nelle e-mail e nei modelli e-mail in cui è in uso. Azioni disponibili:<br/><ul><li>Modifica descrizione<li>Aggiungi a un messaggio e-mail o a un modello<li>Modifica versione bozza in Progettazione visiva<li>Pubblica versione bozza<li>Duplica<li>Elimina (se non in uso) |

![Ciclo di vita stato frammento](./assets/status-lifecycle-diagram.png){zoomable="yes"}

>[!IMPORTANT]
>
>Lo stato del frammento è stato introdotto nella versione di agosto di Journey Optimizer B2B edition. Tutti i frammenti creati prima di questa versione hanno lo stato _Bozza_, anche se vengono utilizzati in un messaggio e-mail o in un modello. Se apporti modifiche a questi frammenti, devi pubblicare il frammento per propagare le modifiche.

### Filtrare l’elenco dei frammenti

Per cercare un frammento in base al nome, immetti una stringa di testo nella barra di ricerca per trovare una corrispondenza. Fai clic sull&#39;icona _Filtro_ ( ![Mostra o nascondi icona filtri](../assets/do-not-localize/icon-filter.svg) ) per visualizzare le opzioni di filtro disponibili e modificare le impostazioni per filtrare gli elementi visualizzati in base ai criteri specificati.

![Filtra i frammenti visualizzati](./assets/fragments-list-filtered.png){width="700" zoomable="yes"}

### Personalizzare la visualizzazione delle colonne

Personalizza le colonne da visualizzare nella tabella facendo clic sull&#39;icona _Personalizza tabella_ ( ![Personalizza icona tabella](../assets/do-not-localize/icon-column-settings.svg) ) in alto a destra.

Nella finestra di dialogo, seleziona le colonne da visualizzare e fai clic su **[!UICONTROL Applica]**.

![Selezionare le colonne da visualizzare](./assets/fragments-customize-table-dialog.png){width="300"}

## Creare i frammenti

Per creare nuovi frammenti visivi in Journey Optimizer B2B edition, fai clic su **[!UICONTROL Crea frammento]** in alto a destra.

1. Nella finestra di dialogo _[!UICONTROL Crea frammento]_, immetti un **[!UICONTROL Nome]** e una **[!UICONTROL Descrizione]** utili (facoltativi).

   Requisiti dei frammenti:

   * Nome: massimo 100 caratteri, deve essere univoco, senza distinzione tra maiuscole e minuscole

   * Descrizione: massimo 300 caratteri

   * Alpha, caratteri numerici e speciali sono consentiti

   * I caratteri riservati sono **_non consentiti_**: `\ / : * ? " < > |`

   ![Finestra di dialogo Crea frammento](./assets/assets-fragments-create-dialog.png){width="400"}

1. Fai clic su **[!UICONTROL Crea]**.

   La finestra di progettazione visiva viene aperta con un&#39;area di lavoro vuota.

1. Utilizza gli strumenti di progettazione del contenuto per creare il contenuto del frammento visivo:

   * [Aggiungere struttura e contenuto](./fragment-authoring.md#add-structure-and-content)
   * [Aggiungi Assets](./fragment-authoring.md#add-assets)
   * [Spostarsi tra livelli, impostazioni e stili](./fragment-authoring.md#navigate-the-layers-settings-and-styles)
   * [Personalizzazione dei contenuti](./fragment-authoring.md#personalize-content)
   * [Abilita campi personalizzati](./fragment-authoring.md#enable-fragment-customization)
   * [Modifica tracciamento URL collegato](./fragment-authoring.md#edit-linked-url-tracking)

1. Fai clic su **[!UICONTROL Salva]** in qualsiasi momento per salvare la bozza del frammento.

1. Quando sei pronto a rendere il frammento disponibile per l&#39;utilizzo in un messaggio e-mail o in un modello e-mail, fai clic su **[!UICONTROL Pubblica]**.

## Visualizza dettagli frammento

Fai clic sul nome di un frammento nella pagina dell’elenco per aprire la pagina dei dettagli del frammento. Puoi scegliere di modificare il frammento, rinominarlo o aggiornare la descrizione del frammento. Per salvare automaticamente le modifiche, apporta gli aggiornamenti e fai clic all’esterno del campo nome o descrizione.

>[!NOTE]
>
>Se un frammento pubblicato è utilizzato da un’e-mail o da un modello e-mail, non puoi modificare il nome o il contenuto. Puoi creare una versione bozza se desideri apportare modifiche al frammento.

![Visualizza dettagli per un frammento pubblicato](./assets/fragment-details-published.png){width="600" zoomable="yes"}

Fai clic su **[!UICONTROL Modifica frammento]** per aprire il frammento nell&#39;editor di contenuti visivi.

Uscire dalla visualizzazione in qualsiasi momento facendo clic sulla freccia _Indietro_ in alto a sinistra, per tornare alla pagina dell&#39;elenco _Frammenti_.

## Visualizza frammento utilizzato da riferimenti

Nella pagina dei dettagli del frammento, fai clic sulla scheda **[!UICONTROL Usato da]** per visualizzare i dettagli sulla posizione in cui il frammento è attualmente utilizzato in Journey Optimizer B2B edition, nelle e-mail, nei modelli e-mail e nei frammenti.

>[!IMPORTANT]
>
>Non è possibile eliminare i frammenti attualmente utilizzati da e-mail o modelli e-mail.

I riferimenti vengono visualizzati in base alla categoria: _E-mail_ o _Modello e-mail_. Le e-mail in Journey Optimizer B2B edition sono incorporate e create all’interno di percorsi di account, pertanto il percorso principale dell’e-mail che utilizza il frammento viene visualizzato in riferimenti.

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

Le modifiche apportate a un frammento dipendono dal suo stato corrente:

* Quando un frammento è nello stato _Bozza_, puoi modificarne i dettagli e il contenuto visivo.
* Quando un frammento è nello stato _Pubblicato_, puoi modificare la descrizione del frammento, ma non il nome. Non è possibile modificare il contenuto visivo.
* Quando un frammento è in stato _Pubblicato con bozza_, la modifica dei dettagli è limitata alla descrizione. Puoi anche modificare il contenuto visivo della versione bozza.

>[!BEGINTABS]

>[!TAB Bozza]

1. Nella pagina dell&#39;elenco _[!UICONTROL Frammenti]_ fare clic sul nome del frammento per aprirlo.

   Viene visualizzata un’anteprima del contenuto visivo, con i dettagli del frammento a destra.

1. Modifica uno dei dettagli, ad esempio nome e descrizione.

   ![Dettagli per frammento con stato Bozza](./assets/fragment-draft-details.png){width="600" zoomable="yes"}

1. Per apportare modifiche al contenuto nella finestra di progettazione visiva, fare clic su **[!UICONTROL Modifica frammento]**.

   Utilizza gli strumenti di progettazione visiva secondo necessità:

   * [Aggiungere struttura e contenuto](./fragment-authoring.md#add-structure-and-content)
   * [Aggiungi Assets](./fragment-authoring.md#add-assets)
   * [Spostarsi tra livelli, impostazioni e stili](./fragment-authoring.md#navigate-the-layers-settings-and-styles)
   * [Personalizzazione dei contenuti](./fragment-authoring.md#personalize-content)
   * [Abilita campi personalizzati](./fragment-authoring.md#enable-fragment-customization)
   * [Modifica tracciamento URL collegato](./fragment-authoring.md#edit-linked-url-tracking)

   Fai clic su **[!UICONTROL Salva]** o **[!UICONTROL Salva e chiudi]** per tornare ai dettagli del frammento.

1. Quando il frammento soddisfa i criteri e desideri renderlo disponibile per l&#39;utilizzo in un&#39;e-mail o in un modello e-mail, fai clic su **[!UICONTROL Pubblica]**.

>[!TAB Pubblicato]

1. Nella pagina dell&#39;elenco _[!UICONTROL Frammenti]_ fare clic sul nome del frammento per aprirlo.

   Viene visualizzata un’anteprima del contenuto visivo, con i dettagli del frammento a destra.

1. Se necessario, modifica la descrizione.

   Per un frammento pubblicato, non è possibile modificare tutti gli altri dettagli.

1. Se desideri aggiornare il contenuto, fai clic su **[!UICONTROL Crea versione bozza]** in alto a destra.

   Fare clic su **[!UICONTROL OK]** nella finestra di dialogo per aprire la versione bozza nella finestra di progettazione visiva.

   ![Finestra di dialogo Crea bozza versione](./assets/fragments-create-draft-version.png){width="300"}

   Utilizza gli strumenti di progettazione visiva secondo necessità:

   * [Aggiungere struttura e contenuto](./fragment-authoring.md#add-structure-and-content)
   * [Aggiungi Assets](./fragment-authoring.md#add-assets)
   * [Spostarsi tra livelli, impostazioni e stili](./fragment-authoring.md#navigate-the-layers-settings-and-styles)
   * [Personalizzazione dei contenuti](./fragment-authoring.md#personalize-content)
   * [Abilita campi personalizzati](./fragment-authoring.md#enable-fragment-customization)
   * [Modifica tracciamento URL collegato](./fragment-authoring.md#edit-linked-url-tracking)

   Fai clic su **[!UICONTROL Salva]** o **[!UICONTROL Salva e chiudi]** per tornare ai dettagli del frammento.

1. Quando il frammento bozza soddisfa i criteri e desideri rendere le modifiche disponibili per l&#39;utilizzo in un messaggio e-mail o in un modello e-mail, fai clic su **[!UICONTROL Pubblica]**.

   Quando pubblichi la versione bozza, questa sostituisce la versione pubblicata corrente e il contenuto viene aggiornato nelle e-mail e nei modelli e-mail in cui è già in uso.

>[!TAB Pubblicato con bozza]

Esistono due modi per aprire la versione bozza per la modifica dalla pagina di elenco _[!UICONTROL Frammenti]_:

* Fai clic sull&#39;icona _Altro_ (**...**) accanto al nome del frammento e scegli **[!UICONTROL Apri versione bozza]**.

  ![Apri versione bozza](./assets/fragments-create-draft-version.png){width="300"}

* Fai clic sul nome del frammento per aprirlo. Quindi, fai clic su **[!UICONTROL Apri versione bozza]** in alto a destra.

  Viene visualizzata un’anteprima del contenuto visivo per la versione bozza, con i dettagli del frammento a destra.

Per aggiornare il contenuto:

1. Fai clic su **[!UICONTROL Modifica frammento]** in alto a destra. Utilizza gli strumenti di progettazione visiva secondo necessità:

   * [Aggiungere struttura e contenuto](./fragment-authoring.md#add-structure-and-content)
   * [Aggiungi Assets](./fragment-authoring.md#add-assets)
   * [Spostarsi tra livelli, impostazioni e stili](./fragment-authoring.md#navigate-the-layers-settings-and-styles)
   * [Personalizzazione dei contenuti](./fragment-authoring.md#personalize-content)
   * [Abilita campi personalizzati](./fragment-authoring.md#enable-fragment-customization)
   * [Modifica tracciamento URL collegato](./fragment-authoring.md#edit-linked-url-tracking)

   Fai clic su **[!UICONTROL Salva]** o **[!UICONTROL Salva e chiudi]** per tornare ai dettagli del frammento.

1. Quando il frammento bozza soddisfa i criteri e desideri rendere le modifiche disponibili per l&#39;utilizzo in un messaggio e-mail o in un modello e-mail, fai clic su **[!UICONTROL Pubblica]**.

   Quando pubblichi la versione bozza, questa sostituisce la versione pubblicata corrente e il contenuto viene aggiornato nelle e-mail e nei modelli e-mail in cui è già in uso.

>[!ENDTABS]

## Frammenti duplicati

Puoi duplicare un frammento utilizzando uno dei seguenti metodi:

* Dalla pagina dell&#39;elenco _[!UICONTROL Frammenti]_, fai clic sull&#39;icona _Altro_ (**...**) accanto al nome del frammento e scegli **[!UICONTROL Duplica]**.
* Nella parte superiore destra della pagina dei dettagli del frammento, fare clic su **[!UICONTROL ... Altro]** e scegli **[!UICONTROL Duplicato]**.

![Duplica il frammento](./assets/fragment-details-duplicate.png){width="600" zoomable="yes"}

Nella finestra di dialogo, inserisci un nome utile (univoco) e una descrizione. Fai clic su **[!UICONTROL Duplica]** per completare l&#39;azione.

![Immettere un nome e una descrizione per il frammento duplicato](./assets/fragment-duplicate-dialog.png){width="400"}

Il frammento duplicato (nuovo) viene quindi visualizzato nell&#39;elenco _Frammenti_.

## Salvare un nuovo frammento da e-mail o contenuto del modello

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

1. Crea un nodo [_[!UICONTROL Invia e-mail &#x200B;]_](./add-email.md#add-an-email-action-node-in-a-journey).

1. Crea o modifica [contenuto e-mail per il nodo](./email-authoring.md).

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
