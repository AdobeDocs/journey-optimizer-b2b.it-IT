---
title: Modelli e-mail
description: Scopri come creare e modificare modelli e-mail da utilizzare per creare e-mail di percorso dell’account in modo semplice ed efficiente.
feature: Email Authoring, Content
source-git-commit: 77514070a54b41bd833eb4d186ae4b860df9e0f8
workflow-type: tm+mt
source-wordcount: '2270'
ht-degree: 0%

---

# Modelli e-mail

Per una progettazione più rapida e migliorata, puoi creare modelli e-mail autonomi per riutilizzare contenuti personalizzati in percorsi di account Adobe Journey Optimizer B2B Edition. Tramite i modelli, i membri del gruppo orientati al contenuto possono lavorare sul contenuto delle e-mail al di fuori dei percorsi. Gli esperti di marketing possono quindi riutilizzare e adattare questi modelli autonomi all’interno dei loro percorsi di account. Ad esempio, un membro del team è responsabile solo del contenuto, senza accesso ai percorsi di account. Tuttavia, possono creare un modello e-mail che gli esperti di marketing possono selezionare come punto di partenza per le comunicazioni e-mail e personalizzarlo in base ai requisiti del percorso.

## Accedere e gestire i modelli e-mail

Per accedere ai modelli e-mail nell&#39;edizione B2B di Adobe Journey Optimizer, vai alla navigazione a sinistra e fai clic su **[!UICONTROL Gestione contenuto]** > **[!UICONTROL Modelli]**. Questa azione apre una pagina di elenco con tutti i modelli e-mail creati nell’istanza elencata in una tabella.

È possibile ordinare la tabella in base a una qualsiasi delle colonne facendo clic sul titolo della colonna.

Per cercare un modello per nome, immettere una stringa di testo nella barra di ricerca.

Personalizzare le colonne da visualizzare nella tabella facendo clic sull&#39;icona _Personalizza tabella_ in alto a destra. Selezionare le colonne da visualizzare e fare clic su **[!UICONTROL Applica]**.

Dalla pagina dell&#39;elenco è possibile eseguire le azioni descritte nelle sezioni seguenti.

## Creare modelli e-mail

Puoi creare un nuovo modello di e-mail dalla pagina di elenco dei modelli di e-mail facendo clic su **[!UICONTROL Crea modello]** in alto a destra.

Nella finestra di dialogo, immetti un nome e una descrizione utili, quindi fai clic su **[!UICONTROL Crea]**.

Viene visualizzata la pagina _[!UICONTROL Progetta il modello]_ che fornisce diverse opzioni per la creazione del modello: Progetta da zero, Importa HTML o seleziona un modello struttura.

### Progettare da zero

Utilizza e-mail designer per definire la struttura del contenuto delle e-mail. Aggiungendo e spostando elementi strutturali con semplici azioni di trascinamento della selezione, puoi progettare la forma del contenuto dell’e-mail riutilizzabile in pochi secondi.

1. Dalla home page di _[!UICONTROL Progetta modello]_, seleziona l&#39;opzione **[!UICONTROL Progetta da zero]**.

1. Inizia a progettare il contenuto trascinando i componenti nell’area di lavoro per definire il layout strutturale dell’e-mail.

   Gli strumenti di progettazione disponibili sono equivalenti a quelli utilizzati per la creazione di e-mail. La differenza è che questo contenuto viene quindi salvato come modello che può essere riutilizzato su più nodi e-mail di invio all’interno di percorsi di account.

### Importa HTML

L’edizione B2B di Adobe Journey Optimizer consente di importare contenuti HTML esistenti per progettare i modelli e-mail. Il contenuto può essere:

* File HTML con un foglio di stile incorporato.
* Un file .zip che include un file HTML, il foglio di stile (.css) e le immagini

  >[!NOTE]
  >
  >La struttura del file .zip non è soggetta a vincoli. Tuttavia, i riferimenti devono essere relativi e adattarsi alla struttura ad albero della cartella .zip.

1. Dalla home page di _[!UICONTROL Progettare il modello]_, selezionare l&#39;opzione **[!UICONTROL Importa HTML]**.

1. Trascina e rilascia il file HTML o .zip contenente il contenuto HTML e fai clic su **[!UICONTROL Importa]**.

   Dopo il caricamento del contenuto di HTML, il contenuto si trova in _modalità di compatibilità_. In questa modalità, puoi solo personalizzare il testo, aggiungere collegamenti o includere risorse nel contenuto.

1. Per utilizzare i componenti di contenuto di e-mail designer, fare clic sulla scheda **[!UICONTROL Convertitore HTML]** e quindi su **[!UICONTROL Converti]**.

>[!NOTE]
>
>L&#39;utilizzo di un tag `<table>` come primo livello in un file HTML può causare la perdita di stile, incluse le impostazioni di sfondo e larghezza nel tag del livello superiore.

Puoi personalizzare il contenuto importato in base alle esigenze con gli strumenti dell’editor e-mail visivo.

### Seleziona un modello struttura

Dalla home page di _[!UICONTROL Progettare il modello]_, utilizzare la sezione Seleziona modello struttura per iniziare a creare il contenuto da un modello. Puoi utilizzare un modello di esempio o un modello e-mail salvato dall’istanza Journey Optimizer B2B Edition.

>[!BEGINTABS]

>[!TAB Modelli salvati]

Nella home page di _Progettare il modello_, la scheda _Modelli di esempio_ è selezionata per impostazione predefinita. Per utilizzare un modello personalizzato, selezionare la scheda **[!UICONTROL Modelli salvati]**.

Viene visualizzato l’elenco di tutti i modelli e-mail creati nella sandbox corrente. Puoi ordinarli per nome, Ultima modifica e Ultima creazione.

Selezionare il modello desiderato dall&#39;elenco.

Dopo la selezione, viene visualizzata un&#39;anteprima del modello. In modalità anteprima puoi spostarti tra tutti i modelli di una categoria (campione o salvato, a seconda della selezione) utilizzando le frecce destra e sinistra.

Quando la visualizzazione corrisponde a quella che si desidera utilizzare, fare clic su Usa questo modello in alto a destra nella finestra di anteprima.

Questa azione copia il contenuto nel designer del contenuto visivo, dove puoi modificarlo in base alle esigenze.

>[!TAB Modello di esempio]

Adobe Journey Optimizer B2B Edition offre una selezione di modelli e-mail forniti come preconfigurati, che possono essere utilizzati per creare e-mail e modelli e-mail.

>[!ENDTABS]

## Aggiungi struttura e contenuto

Inizia a progettare il contenuto trascinando le strutture dal menu **[!UICONTROL Componenti]** nell&#39;area di lavoro per definire il layout dell&#39;e-mail.

Aggiungi tutte le strutture necessarie e modificane le impostazioni nelle proprietà dell’elemento a destra.

Seleziona il componente _n:n column_ per definire il numero di colonne desiderato (tra tre e 10). Definite la larghezza di ciascuna colonna spostando le frecce in basso.

>[!NOTE]
>
>Le dimensioni di ogni colonna non possono essere inferiori al 10% della larghezza totale del componente struttura. Puoi rimuovere solo colonne vuote.

Espandi la sezione **[!UICONTROL Contents]** e aggiungi tutti gli elementi necessari in uno o più componenti della struttura.

Ogni componente può essere ulteriormente personalizzato utilizzando le schede _[!UICONTROL Impostazioni]_ o _[!UICONTROL Stile]_ nel pannello di destra. Ad esempio, puoi modificare lo stile del testo, la spaziatura interna o il margine di ciascun componente.

## Navigare tra livelli, impostazioni e stile

L’esempio seguente illustra i passaggi per regolare la spaziatura e l’allineamento verticale all’interno di un componente struttura composto da tre colonne.

1. Seleziona il componente struttura direttamente nel messaggio e-mail o utilizzando la struttura di navigazione disponibile nel menu a sinistra.

1. Dalla barra degli strumenti, fare clic su **[!UICONTROL Selezionare una colonna]** e scegliere quella che si desidera modificare.

   Puoi anche selezionarla dall’albero della struttura. I parametri modificabili per tale colonna vengono visualizzati nella scheda _[!UICONTROL Stili]_.

1. In **[!UICONTROL Allineamento]**, seleziona l&#39;icona _Superiore_, _Centro_ o _Inferiore_.

1. In **[!UICONTROL Spaziatura interna]**, definire la spaziatura per tutti i lati.

   Selezionare **[!UICONTROL Spaziatura interna diversa per ogni lato]** per ottimizzare la spaziatura. Fai clic sull’icona del lucchetto per interrompere la sincronizzazione.

1. Se necessario, regolare l&#39;allineamento e la spaziatura per le altre colonne.

1. Salva le modifiche.

## Personalizzare il contenuto

L’esempio seguente illustra i passaggi per personalizzare il contenuto del modello utilizzando gli attributi lead/account e i token di sistema.

1. Seleziona il componente testo e fai clic sull&#39;icona _Aggiungi personalizzazione_ nella barra degli strumenti.

   Questa azione apre la finestra di dialogo _Modifica Personalization_.

1. Trascina e rilascia uno o più token nello spazio vuoto.

1. Fai clic su **[!UICONTROL Salva]**.

## Aggiungi frammenti

Nell&#39;editor del contenuto visivo, l&#39;icona _Frammenti_ è visualizzata a sinistra. L’esempio seguente illustra i passaggi per aggiungere frammenti al contenuto del modello.

1. Per aprire l&#39;elenco dei frammenti, fare clic sull&#39;icona _Frammenti_.

   È possibile:

   * Ordina l’inserzione.
   * Sfoglia, Cerca o filtra l’inserzione.
   * Consente di passare dalla visualizzazione Anteprima alla visualizzazione Elenco.
   * Aggiorna l’elenco per riflettere eventuali frammenti creati di recente.

1. Trascina e rilascia uno dei frammenti nel segnaposto del componente struttura.

   L’editor esegue il rendering del frammento all’interno della sezione/elemento della struttura e-mail.

Il contenuto del frammento viene aggiornato dinamicamente all’interno della struttura per eseguire il rendering di un’immagine del modo in cui il contenuto viene visualizzato nell’e-mail.

Se desideri aggiungere il frammento in modo che occupi l’intero layout orizzontale all’interno dell’e-mail, aggiungi una struttura di colonne 1:1 e quindi trascina e rilascia il frammento all’interno di esso.

Dopo il salvataggio, l’e-mail viene visualizzata nella pagina dei dettagli del frammento > Utilizzato da. I frammenti aggiunti a un modello e-mail non sono modificabili all’interno del modello; il contenuto è definito dal frammento di origine.

## Aggiungere risorse

Nell&#39;editor del contenuto visivo, l&#39;icona _Assets_ è visualizzata a sinistra. L’esempio seguente illustra i passaggi necessari per aggiungere risorse al contenuto del modello.

1. Per aprire la libreria di risorse, fai clic sull&#39;icona _Assets_.

   Dal selettore delle risorse, puoi selezionare direttamente le risorse memorizzate nella libreria Assets.

1. Fai doppio clic sulla cartella contenente le risorse necessarie.

1. Trascina e rilascia una o più risorse di immagini in un componente struttura.

## Anteprima e modifica degli URL

1. Fai clic sulla scheda _[!UICONTROL Collegamenti]_ a sinistra per visualizzare tutti gli URL del contenuto da tracciare.

1. Se necessario, modificare il _Tipo di tracciamento_ o _Etichetta_ e aggiungere _Tag_.

## Opzioni di visualizzazione

Sfrutta le opzioni di convalida di visualizzazione e contenuto disponibili nell’editor e-mail visivo.

* Zoom in/out del contenuto tra le opzioni di zoom predefinite.

* Cambia la visualizzazione del contenuto tra desktop, dispositivi mobili o solo testo/solo testo.
   * Fai clic sull&#39;icona _Occhio_ per visualizzare l&#39;anteprima del contenuto tra i dispositivi.
   * Seleziona uno dei dispositivi predefiniti o immetti dimensioni personalizzate per visualizzare in anteprima il contenuto.

## Altre opzioni

Dal selettore _Altre opzioni_ nell&#39;editor di contenuto visivo, è possibile eseguire le azioni seguenti:

* **Ripristina modello** - Fare clic su questa opzione per cancellare l&#39;area di lavoro di progettazione e-mail visiva in un&#39;area di lavoro vuota e riavviare la creazione del contenuto.
* **Salva come frammento** - Salva tutto o parte del frammento come frammento da riutilizzare in più e-mail o modelli di e-mail. Fornisci un nome e una descrizione per i frammenti e li inserisci nell’elenco dei frammenti disponibili.
* **Modifica la progettazione** - Torna alla pagina _Progetta modello_. Da qui puoi intraprendere qualsiasi azione come descritto nella sezione &quot;Creare modelli e-mail&quot;.
* **Esporta HTML** - Scarica il contenuto nell&#39;area di lavoro visiva nel sistema locale in formato HTML compresso come file zip.

## Visualizza dettagli modello e-mail

Fai clic sul nome di un modello e-mail per aprirne la pagina dei dettagli.

Esegui azioni rapide sul modello e-mail, ad esempio _Duplica_ e _Elimina_, in alto a destra.

Puoi anche visualizzare gli avvisi (errori e avvisi per il modello e-mail) facendo clic sul pulsante Avvisi. Anche se questi avvisi non vietano l’utilizzo del modello e-mail nella creazione di e-mail, queste informazioni forniscono visibilità agli esperti di marketing del team su ciò che potrebbe non funzionare e sugli aggiornamenti richiesti prima che possano essere utilizzati per la consegna.

Visualizza i dettagli del modello e-mail, ad esempio nome e descrizione. Queste impostazioni possono essere modificate. Fare clic all&#39;esterno della casella della descrizione per salvare automaticamente le modifiche.

Visualizza le proprietà del modello e-mail, ad esempio creato da, creato in data, aggiornato da ultimo in data e modificato da.

## Visualizza modello e-mail utilizzato da riferimenti

Nella pagina dei dettagli dei modelli e-mail, fai clic sulla scheda **[!UICONTROL Usato da]** per visualizzare i dettagli di dove questo modello e-mail viene utilizzato nelle e-mail tra percorsi di account.

Le e-mail in Journey Optimizer B2B Edition sono incorporate e create all’interno di percorsi, pertanto il percorso principale dell’e-mail che utilizza il modello viene visualizzato in riferimenti.

Fai clic sul collegamento per passare all’e-mail corrispondente dove viene utilizzato il modello e-mail.

Uscire dalla visualizzazione in qualsiasi momento facendo clic sulla freccia Indietro, che consente di tornare alla pagina dell&#39;elenco.

## Modifica modelli e-mail

Questa azione può essere intrapresa da:

* La pagina dei dettagli - Fai clic su **[!UICONTROL Modifica modello e-mail]**.
* Pagina dell&#39;elenco - Fai clic sui puntini di sospensione (...) accanto a un modello di e-mail e scegli **[!UICONTROL Modifica]**.

Questa azione ti porta alla pagina _Progetta il modello_ o alla pagina dell&#39;editor di contenuti visivi in base all&#39;ultimo stato salvato del modello e-mail. Da qui puoi modificare il contenuto del modello e-mail in base alle esigenze. Per informazioni sulle opzioni di modifica, consulta [Creare modelli e-mail](#create-email-templates).

## Modelli e-mail duplicati

Puoi duplicare un modello e-mail utilizzando uno dei seguenti metodi:

* Dai dettagli del modello e-mail a destra, espandi **[!UICONTROL Altro]** e fai clic su **[!UICONTROL Duplica]**.
* Dalla pagina di elenco dei _modelli di posta elettronica_, fai clic sui puntini di sospensione (...) accanto al modello e scegli **[!UICONTROL Duplica]**.

Nella finestra di dialogo, inserisci un nome utile (univoco) e una descrizione. Fai clic su **[!UICONTROL Duplica]** per completare l&#39;azione.

Il (nuovo) modello e-mail duplicato viene quindi visualizzato nell&#39;elenco _Modelli e-mail_.

## Elimina modelli e-mail

Una rimozione del modello e-mail non può essere annullata, pertanto controlla prima di avviare un’azione di eliminazione.

Puoi eliminare un modello e-mail utilizzando uno dei seguenti metodi:

* Dai dettagli del modello a destra, espandi **[!UICONTROL Altro]** e fai clic su **[!UICONTROL Elimina]**.
* Dalla pagina di elenco dei _modelli di posta elettronica_, fai clic sui puntini di sospensione (...) accanto al modello e scegli **[!UICONTROL Elimina]**.

Questa azione apre una finestra di dialogo di conferma. È possibile interrompere il processo facendo clic su **[!UICONTROL Annulla]** oppure su **[!UICONTROL Elimina]** per confermare la rimozione.

## Eseguire azioni in blocco

Dalla pagina di elenco dei modelli e-mail (Gestione contenuto > Modelli e-mail), seleziona più modelli alla volta selezionando la casella di controllo a sinistra. Quando selezioni più modelli, nella parte inferiore viene visualizzato un banner.

Puoi eseguire le seguenti azioni in blocco:

### Elimina modelli e-mail

Puoi eliminare fino a un massimo di 20 modelli alla volta.
Una finestra di dialogo di conferma consente di interrompere l’azione o confermare la rimozione dei modelli.

## Creare un messaggio e-mail da un modello salvato

Dalla schermata _Crea e-mail_, utilizza la sezione _Seleziona modello struttura_ per iniziare a creare il contenuto da un modello.

Per iniziare a creare i contenuti con uno dei modelli e-mail creati, procedi come segue:

1. Accedi al Designer di posta elettronica dalla pagina _Modifica contenuto_.

   Nella pagina _Crea messaggio e-mail_, la scheda _Modelli di esempio_ è selezionata per impostazione predefinita.

1. Per utilizzare un modello e-mail personalizzato, seleziona la scheda **[!UICONTROL Modelli salvati]**.

   In questa scheda viene visualizzato un elenco di tutti i modelli e-mail creati nella sandbox. Puoi ordinarli per nome, Ultima modifica e Ultima creazione.

1. Seleziona dall’elenco il modello desiderato.

   Dopo la selezione, viene visualizzata un&#39;anteprima del modello. In modalità anteprima puoi spostarti tra tutti i modelli di una categoria (campione o salvato, a seconda della selezione) utilizzando le frecce destra e sinistra.

1. Fai clic su [!UICONTROL Usa questo modello] in alto a destra.

1. Dalla finestra di progettazione del contenuto visivo, modifica il contenuto in base alle esigenze.
