---
title: Modelli e-mail
description: 'Creazione di modelli e-mail riutilizzabili da zero, importazione HTML o progettazioni esistenti: gestione di modelli per percorsi di account in Journey Optimizer B2B edition.'
feature: Templates, Email Authoring, Content
role: User
exl-id: 4e146802-e3ef-4528-b581-191e28afe86f
source-git-commit: b27b4485e5d778f0d4cbcad7392ab19c42a79e14
workflow-type: tm+mt
source-wordcount: '1533'
ht-degree: 0%

---

# Modelli e-mail

Per accelerare e migliorare la progettazione, è possibile creare modelli di e-mail autonomi per riutilizzare il contenuto personalizzato tra i percorsi di account [!DNL Adobe Journey Optimizer B2B Edition]. Tramite i modelli, i membri del gruppo orientati al contenuto possono lavorare sul contenuto delle e-mail al di fuori dei percorsi. Gli esperti di marketing possono quindi riutilizzare e adattare questi modelli autonomi all’interno dei loro percorsi. Ad esempio, un membro del team è responsabile solo del contenuto, senza accesso ai percorsi di account. Tuttavia, possono creare un modello e-mail che gli esperti di marketing possono selezionare come punto di partenza per le comunicazioni e-mail e personalizzarlo in base ai requisiti del percorso.

## Accedere e gestire i modelli e-mail

Per accedere ai modelli e-mail in [!DNL Journey Optimizer B2B Edition], vai alla navigazione a sinistra e fai clic su **[!UICONTROL Gestione contenuto]** > **[!UICONTROL Modelli]**. Nel pannello laterale, seleziona **[!UICONTROL Modelli e-mail]**.

Questa azione apre una pagina di elenco con tutti i modelli e-mail creati nell’istanza elencata in formato tabella.

Per impostazione predefinita, l&#39;elenco è ordinato in base alla colonna _[!UICONTROL Modificato]_, con i modelli aggiornati più di recente nella parte superiore. Fai clic sul titolo della colonna per passare da crescente a decrescente.

Per cercare un modello per nome, immettere una stringa di testo nella barra di ricerca. Fai clic sull&#39;icona _Filtro_ in alto a sinistra per filtrare l&#39;elenco in base alle date di creazione o modifica e ai modelli creati o modificati.

![Accedi alla libreria dei modelli e-mail e filtra per nome e date](./assets/templates-list-search-filter.png){width="800" zoomable="yes"}

Personalizza le colonne da visualizzare nella tabella facendo clic sull&#39;icona _Personalizza tabella_ ( ![Personalizza icona tabella](../assets/do-not-localize/icon-column-settings.svg) ) in alto a destra. Selezionare le colonne da visualizzare e fare clic su **[!UICONTROL Applica]**.

Dall’elenco dei modelli visualizzato, puoi eseguire le azioni descritte nelle sezioni seguenti.

## Creare un modello e-mail

Puoi creare un modello di e-mail dalla pagina dell&#39;elenco dei modelli facendo clic su **[!UICONTROL Crea modello]** in alto a destra.

1. Nella finestra di dialogo, immetti un **[!UICONTROL Nome]** e una **[!UICONTROL Descrizione]** utili (facoltativi).

   ![Immetti le proprietà iniziali per il nuovo modello di e-mail](./assets/templates-create-dialog.png){width="400"}

1. Fai clic su **[!UICONTROL Crea]**.

Viene visualizzata la pagina _[!UICONTROL Progetta modello]_ contenente più opzioni per la creazione del modello: _[!UICONTROL Progetta da zero]_, _[!UICONTROL Importa HTML]_ o _[!UICONTROL Seleziona modello struttura]_.

![Scegli come iniziare con la progettazione del modello e-mail](./assets/templates-create-design.png){width="800" zoomable="yes"}

Dopo aver selezionato il metodo da utilizzare per avviare la progettazione del modello e-mail, utilizza lo spazio di progettazione visiva per [creare il contenuto del modello e-mail](./email-template-authoring.md).

### Creare da zero

Utilizza l’editor di contenuto visivo per definire la struttura del contenuto dell’e-mail. Aggiungendo e spostando componenti strutturali con semplici azioni di trascinamento della selezione, puoi progettare la forma del contenuto dell’e-mail riutilizzabile in pochi secondi.

>[!NOTE]
>
>Gli strumenti di progettazione disponibili equivalgono agli strumenti utilizzati per la creazione di [e-mail](./email-authoring.md). La differenza sta nel fatto che questo contenuto viene salvato come modello che può essere riutilizzato in più nodi _invia e-mail_ all&#39;interno di percorsi di account.

1. Dalla home page di _[!UICONTROL Progetta modello]_, seleziona l&#39;opzione **[!UICONTROL Progetta da zero]**.

1. Nella finestra di dialogo _[!UICONTROL Crea e-mail]_, scegli il tipo di contenuto e-mail che desideri utilizzare per il modello.

   * **[!UICONTROL Usa temi]** - Scegliere questa opzione per creare il modello di posta elettronica in _modalità tema_. In questa modalità, puoi utilizzare un tema del brand definito per semplificare il processo di authoring dei contenuti e assicurarti che la progettazione sia allineata agli standard definiti.

   ![Crea la tua e-mail - Usa temi](./assets/create-email-use-theme.png){width="450"}

   * **[!UICONTROL Stile manuale]** - Scegliere questa opzione per creare il modello di posta elettronica in _Modalità manuale_. In questa modalità, puoi impostare manualmente lo stile per tutti i componenti di struttura e contenuto aggiunti all’area di lavoro vuota.

1. (_Modalità temi_) Applica un tema.

   Nello spazio di progettazione delle e-mail, fai clic sull&#39;icona _Temi_ ( ![Icona Temi](../assets/do-not-localize/icon-design-themes.svg) ) a destra.

   ![Spazio di progettazione e-mail - Icona Temi selezionata](./assets/email-design-themes-icon-selected.png){width="600" zoomable="yes"}

   Viene visualizzato il tema predefinito o applicato al modello. Puoi cambiare le varianti di colore per questo tema.

   Fai clic sulla freccia accanto al tema visualizzato per visualizzare l’elenco dei temi personalizzati e Adobe disponibili. Seleziona **[!UICONTROL I miei temi]** per utilizzare un tema personalizzato creato per la tua organizzazione.

   Quando si fa clic all&#39;esterno dell&#39;elenco, il tema selezionato applica gli stili. Puoi alternare tra le varianti di colore.

1. [Aggiungi struttura e contenuto](./email-authoring.md#add-structure-and-content) al modello.

   Se è presente un tema applicato, i componenti aggiunti ereditano automaticamente gli stili definiti nel tema.

### Importa HTML

Adobe Journey Optimizer B2B edition consente di importare contenuti HTML esistenti per progettare modelli e-mail.

{{$include /help/_includes/content-design-import.md}}

![importa contenuto html in un file zip](./assets/templates-import-zip-file.png){width="500"}

>[!NOTE]
>
>L&#39;utilizzo di un tag `<table>` come primo livello in un file HTML può causare la perdita di stile, incluse le impostazioni di sfondo e larghezza nel tag del livello superiore.

Puoi personalizzare il contenuto importato in base alle esigenze nello spazio di progettazione visiva.

### Seleziona un modello struttura

{{$include /help/_includes/content-design-select-template.md}}

## Visualizza dettagli modello e-mail

Nella pagina di elenco Modelli, fai clic sul nome di un modello e-mail per aprire la pagina dei dettagli del modello e-mail. Da qui puoi visualizzare le proprietà di base del modello e-mail e accedere all’editor del contenuto visivo per apportare modifiche al contenuto del modello.

![Accedi alla libreria dei modelli e-mail e filtra per nome e date](./assets/template-details.png){width="700" zoomable="yes"}

* Visualizza i dettagli del modello e-mail, ad esempio nome e descrizione. Queste impostazioni possono essere modificate. Fare clic all&#39;esterno della casella della descrizione per salvare automaticamente le modifiche.

* Visualizza le proprietà del modello e-mail, ad esempio creato da, creato in data, aggiornato da ultimo in data e modificato da.

* Fai clic su **[!UICONTROL Altro]** in alto a destra per eseguire azioni rapide sul modello e-mail, ad esempio _Duplica_ e _Elimina_.

* Se sono presenti avvisi attivi (errori e avvisi per il modello e-mail), fai clic su **[!UICONTROL Avvisi]** in alto a destra per visualizzare le informazioni.

  Questi avvisi non vietano l’utilizzo del modello e-mail per la creazione di e-mail. Queste informazioni forniscono agli addetti al marketing del tuo team visibilità su ciò che potrebbe non funzionare e sugli aggiornamenti necessari prima che possano essere utilizzati per la consegna.

## Visualizza modello e-mail utilizzato da riferimenti

Nella pagina dei dettagli dei modelli e-mail, fai clic sulla scheda **[!UICONTROL Usato da]** per visualizzare i dettagli di dove questo modello e-mail viene utilizzato nelle e-mail tra percorsi di account.

![Fare clic sulla scheda Utilizzato da per verificare l&#39;utilizzo del modello](./assets/template-details-used-by.png){width="400"}

Le e-mail in Journey Optimizer B2B edition vengono incorporate e create all’interno di percorsi, pertanto il percorso principale dell’e-mail che utilizza il modello viene visualizzato in riferimenti.

* Fai clic sul collegamento per passare all’e-mail del percorso corrispondente in cui viene utilizzato il modello e-mail.

* Uscire dalla visualizzazione in qualsiasi momento facendo clic sulla freccia Indietro, che consente di tornare alla pagina dell&#39;elenco.

## Modifica modelli e-mail

Questa azione può essere intrapresa da:

* La pagina dei dettagli - Fai clic su **[!UICONTROL Modifica modello e-mail]**.
* Pagina dell&#39;elenco - Fai clic sui puntini di sospensione (**...**) accanto a un modello di e-mail e scegli **[!UICONTROL Modifica]**.

Questa azione ti porta alla pagina _Progetta il modello_ o alla pagina dell&#39;editor di contenuti visivi (in base all&#39;ultimo stato salvato del modello e-mail). Da qui puoi modificare il contenuto del modello e-mail in base alle esigenze. Per informazioni sulle opzioni di modifica, consulta [Creare modelli e-mail](#create-email-templates).

## Modelli e-mail duplicati

Puoi duplicare un modello e-mail utilizzando uno dei seguenti metodi:

* Dai dettagli del modello e-mail a destra, espandi **[!UICONTROL Altro]** e fai clic su **[!UICONTROL Duplica]**.

  ![Fai clic su Altro per accedere alle azioni Elimina e Duplica](./assets/template-details-more-menu.png){width="400"}

* Dalla pagina di elenco dei _[!UICONTROL modelli di posta elettronica]_, fai clic sui puntini di sospensione (...) accanto al modello e scegli **[!UICONTROL Duplica]**.

Nella finestra di dialogo, inserisci un nome utile (univoco) e una descrizione. Fai clic su **[!UICONTROL Duplica]** per completare l&#39;azione.

Il (nuovo) modello e-mail duplicato viene quindi visualizzato nell&#39;elenco _[!UICONTROL Modelli e-mail]_.

## Elimina modelli e-mail

Una rimozione del modello e-mail non può essere annullata, pertanto controlla prima di avviare un’azione di eliminazione. Puoi eliminare un modello e-mail utilizzando uno dei seguenti metodi:

* Dai dettagli del modello a destra, espandi **[!UICONTROL Altro]** e fai clic su **[!UICONTROL Elimina]**.
* Dalla pagina di elenco dei _[!UICONTROL modelli di posta elettronica]_, fai clic sui puntini di sospensione (...) accanto al modello e scegli **[!UICONTROL Elimina]**.

  ![Fare clic su ... per accedere alle azioni Duplica ed Elimina](./assets/templates-list-more-menu.png){width="500"}

Questa azione apre una finestra di dialogo di conferma. È possibile interrompere il processo facendo clic su **[!UICONTROL Annulla]** oppure su **[!UICONTROL Elimina]** per confermare la rimozione.

## Eseguire azioni in blocco

Dalla pagina di elenco dei modelli e-mail, seleziona più modelli alla volta selezionando le caselle di controllo a sinistra. Quando selezioni più modelli, nella parte inferiore viene visualizzato un banner.

![Un banner visualizza il numero di modelli selezionati e l&#39;icona Elimina](./assets/templates-multi-select-banner.png){width="600"}

**[!UICONTROL Elimina]** - È possibile eliminare fino a un massimo di 20 modelli alla volta. Una finestra di dialogo di conferma consente di interrompere l’azione o confermare la rimozione dei modelli.

## Creare un messaggio e-mail da un modello salvato

Dalla schermata _Crea e-mail_, utilizza la sezione _Seleziona modello struttura_ per iniziare a creare il contenuto da un modello.

Per iniziare a creare i contenuti con uno dei modelli e-mail creati, procedi come segue:

1. Accedi al Designer di posta elettronica dalla pagina _Modifica contenuto_.

   Nella pagina _Crea messaggio e-mail_, la scheda _Modelli di esempio_ è selezionata per impostazione predefinita.

1. Per utilizzare un modello e-mail personalizzato, seleziona la scheda **[!UICONTROL Modelli salvati]**.

   In questa scheda viene visualizzato un elenco di tutti i modelli e-mail creati nella sandbox. Puoi ordinarli _Per nome_, _Ultima modifica_ e _Ultima creazione_.

1. Seleziona dall’elenco il modello desiderato.

   Dopo la selezione, viene visualizzata un&#39;anteprima del modello. In modalità anteprima puoi spostarti tra tutti i modelli di una categoria (campione o salvato, a seconda della selezione) utilizzando le frecce destra e sinistra.

1. Fai clic su **[!UICONTROL Usa questo modello]** in alto a destra.

1. Dall’area di progettazione visiva, modifica il contenuto in base alle esigenze.
