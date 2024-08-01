---
title: Percorsi di account
description: Scopri come creare e gestire i percorsi di account.
feature: Account Journeys
exl-id: 5c22f11f-1967-4b55-8aee-16371173c040
source-git-commit: 78d82aa8b3bb8b8d432eeb187d75e2354dbff3ee
workflow-type: tm+mt
source-wordcount: '1125'
ht-degree: 1%

---


# Percorsi di account

Definisci un coinvolgimento basato sulle vendite che includa e-mail, SMS e altri percorsi di account interni per coordinare le attività di marketing in entrata con le attività di vendita in uscita per ciascun membro del gruppo di acquisto.

## Accedere e sfogliare i percorsi di account

1. Nella home page di Adobe Experience Platform, fare clic su Adobe Journey Optimizer B2B Edition.

1. Nel menu di navigazione a sinistra, fai clic su **[!UICONTROL percorsi di account]**.

   ![Accedi a percorsi di account](./assets/account-journey-browse.png){width="800" zoomable="yes"}

   La pagina percorsi visualizzati include le colonne riportate di seguito.

   * [!UICONTROL Nome] (fare clic sul nome per aprire il percorso di account per la modifica)
   * [!UICONTROL Stato]
   * [!UICONTROL Descrizione]
   * [!UICONTROL Creato da]
   * [!UICONTROL Ultimo aggiornamento:]
   * [!UICONTROL Ultimo aggiornamento eseguito da]
   * [!UICONTROL Pubblicato il]
   * [!UICONTROL Pubblicato da]

Questa tabella include la possibilità di eseguire ricerche per nome e Creato da. Ordinamento non disponibile.

Puoi personalizzare la tabella visualizzata facendo clic sull&#39;icona _Colonne_ nell&#39;angolo in alto a destra e selezionando o deselezionando le caselle di controllo.

![Scegliere le colonne da visualizzare nell&#39;elenco dei percorsi di account](./assets/account-journeys-list-columns.png){width="800" zoomable="yes"}

## Anatomia di un percorso di account

Fare clic sul nome (visualizzato come collegamento) nell&#39;elenco _[!UICONTROL percorsi di account]_ per esaminare i dettagli, apportare modifiche ed eseguire azioni.

![Area di lavoro percorso account](./assets/account-journey-workspace.png){width="800" zoomable="yes"}

L’intestazione dell’editor di ciascun percorso di account include:

* Nome percorso
* Possibilità di modificare il nome (_Modifica_ icona)
* Stato del percorso

Nell’intestazione sono disponibili le seguenti azioni:

* **Publish** - È possibile pubblicare un percorso se non sono presenti errori di blocco. Quando viene pubblicato, lo stato di un Percorso cambia in _Live_. Se il percorso presenta errori, il pulsante viene oscurato con le informazioni sul contenuto: `Resolve errors before publishing`.
* **Duplicato** - Questa azione è simile a una funzione clone, ma il percorso duplicato non include risorse.
* **Chiudi alle nuove voci** - Se chiudi un percorso, gli account attualmente nel percorso continuano il loro percorso nel percorso e non può verificarsi alcun ulteriore ingresso nel percorso. Impossibile riavviare un percorso chiuso. È possibile duplicare un percorso chiuso.
* **Interrompi** - Se interrompi un percorso, gli account nel percorso interrompono immediatamente l&#39;avanzamento e non può verificarsi un ulteriore ingresso nel percorso. Impossibile riavviare un percorso arrestato. Se blocchi i nuovi ingressi senza fermare l&#39;avanzamento delle persone, puoi decidere di chiudere il percorso.
* **Elimina** - Questa azione elimina definitivamente il percorso.

Lo stato di un Percorso cambia in base alle azioni applicate. In base allo stato di un percorso, alcune azioni sono/non sono disponibili nell’intestazione.

| Stato | Descrizione | Azioni disponibili |
| ------ | ----------- | ----------------- |
| _**Bozza**_ | Percorso non pubblicato modificabile. | <ul><li>Pubblica</li><li>Duplica </li><li>Elimina </li></ul> |
| _**Live**_ | Lo stato del percorso cambia da Bozza a In tempo reale quando viene pubblicato un percorso. In questo stato, non è più modificabile. | <ul><li>Duplica </li><li>Chiudi alle nuove voci </li><li>Interrompi </li></ul> |
| _**Chiuso alle nuove voci**_ | Lo stato del percorso cambia da _Live_ a _Chiuso alle nuove voci_ quando fai clic su [!UICONTROL Chiudi alle nuove voci] nella navigazione superiore. | <ul><li>Duplica </li><li>Interrompi </li></ul> |
| _**Interrotto**_ | Lo stato del percorso cambia da _Live_ o _Chiuso alle nuove voci_ quando si interrompe un percorso. Un percorso interrotto non può essere riavviato. | <ul><li>Duplica </li><li>Elimina </li></ul> |
| _**Completato**_ | Quando tutti gli account di un percorso completano il percorso, lo stato cambia da Live (Live) o Closed (Chiuso) a Finished (Finito). | <ul><li>Duplica </li><li>Elimina </li></ul> |

## Introduzione a un percorso

Per iniziare a utilizzare un percorso di account, crea il percorso e quindi costruisci i nodi e il flusso del percorso nell’editor di percorso.

### Creazione di un percorso di account

1. Nel menu di navigazione a sinistra, fai clic su **[!UICONTROL percorsi di account]**.

1. Fai clic su **[!UICONTROL Crea Percorso di account]** in alto a destra nella pagina.

1. Nella finestra di dialogo, immetti un **[!UICONTROL Nome]** (obbligatorio) e una **[!UICONTROL Descrizione]** (facoltativo) univoci.

   ![Finestra di dialogo Crea Percorso di account](./assets/account-journey-create-dialog.png){width="400"}

1. Fai clic su **[!UICONTROL Crea]**.

### Aggiungere il pubblico dell’account per il percorso

Un percorso di account inizia sempre con Pubblico account, in cui puoi aggiungere input al percorso.

1. Fai clic sul nodo **[!UICONTROL Pubblico account]** per visualizzare le proprietà del nodo a destra.

   ![Nodo pubblico account](./assets/account-journey-account-audience-node.png){width="700" zoomable="yes"}

1. Fai clic su **[!UICONTROL Aggiungi pubblico account]**.

   Per selezionare un segmento di pubblico selezionato in precedenza, fai clic su _[!UICONTROL Aggiungi pubblico]_.

1. Per creare un nuovo segmento di pubblico, seleziona **[!UICONTROL Tipi di pubblico per l&#39;account]** nell&#39;area di navigazione a sinistra.

1. Fai clic su **[!UICONTROL Crea pubblico]** e segui i passaggi descritti nella [guida del servizio di segmentazione](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/account-audiences){target="_blank"}.

### Elementi di base di un percorso

L&#39;area di lavoro _percorso_ è la zona centrale nella finestra di progettazione del percorso. È in questa zona che puoi aggiungere nodi di percorso e configurarli. Fai clic su un nodo per aprire il relativo riquadro delle proprietà a destra dell’area di lavoro e impostarlo in base alla progettazione.

Puoi creare il percorso utilizzando uno dei seguenti tipi di nodo:

* [Ascolta un evento](journey-nodes.md#listen-for-an-event)
* [Esegui un&#39;azione](journey-nodes.md#take-an-action)
* [Dividere i percorsi](journey-nodes.md#split-paths)
* [Attendere](journey-nodes.md#wait)
* [Unisci percorsi](journey-nodes.md#merge-paths)

### Parapetti

Per facilitare la creazione di un percorso senza che si verifichino errori, sono presenti le seguenti barre di protezione:

* _Eliminazione di un nodo di percorso suddiviso_: non è possibile eliminare un nodo senza eliminare tutti i nodi successivi in ciascun percorso.
* _Eliminazione di un nodo di unione_: un nodo di unione può essere eliminato solo quando vi è un percorso connesso. Per eliminare un nodo di unione, lasciare selezionato un solo percorso.
* _Passaggio tra account e persone_: non è possibile modificare la selezione da account a persone senza eliminare tutti i nodi successivi in ogni percorso.

### Aggiungi un nodo

1. Passa all’editor di percorso.

1. Fai clic sull&#39;icona più ( **+** ) sul percorso e seleziona il tipo di nodo.

1. Imposta le proprietà del nodo a destra.

### Eliminare un nodo

1. Passa all’editor di percorso.

1. Nelle proprietà del nodo a destra, fai clic sull&#39;icona _Elimina_ (cestino).

1. Nella finestra di dialogo di conformazione, fare clic su **[!UICONTROL Elimina]**.

### Aggiungere ed eliminare un percorso

1. Passa all’editor di percorso.

1. Fai clic sull&#39;icona più ( **+** ) sul percorso e aggiungi il nodo del percorso diviso.

1. Nelle proprietà del nodo a destra, seleziona **[!UICONTROL Account]**.

1. Per aggiungere altri percorsi, fare clic su **[!UICONTROL Aggiungi percorso]**.

   Per ogni percorso creato nel percorso, nelle proprietà viene visualizzata una nuova scheda percorso.

1. Passa a uno dei percorsi nel percorso e aggiungi nodi azione o evento a questo percorso utilizzando l’icona più.

1. Selezionate il nodo del percorso di [PROD143]e per aprire le proprietà a destra.

   Non è possibile eliminare i percorsi che contengono nodi.

1. Per eliminare questi percorsi, è necessario eliminare prima tutti i nodi del percorso.

### Pianificare un percorso

Quando pubblichi un percorso, può iniziare immediatamente o in una data futura pianificata. La data di fine può essere un massimo di tre anni dalla data di inizio. Dopo la pubblicazione di un percorso (_Stato Live_), puoi aggiornare la data di fine del percorso ma non la data di inizio.

1. Passa all’editor di percorso.

1. Pianifica il percorso facendo clic su [!UICONTROL Impostazioni Percorso] nell&#39;intestazione.

1. Nella finestra di dialogo, imposta le opzioni di pianificazione:

   * Scegli un tipo di pianificazione.

     Per attivare il percorso in fase di pubblicazione, scegliere **[!UICONTROL Immediatamente]**.

     Per attivare il percorso in una data futura, scegli **[!UICONTROL In una data specifica]** e fai clic sull&#39;icona _Calendario_ per selezionare la data.

     ![Finestra di dialogo impostazioni Percorso](./assets/account-journey-settings-dialog.png){width="400" zoomable="no"}

   * Specifica la **[!UICONTROL data di fine]** per il percorso. Può essere fino a tre anni dalla data di inizio (questo campo è obbligatorio).

1. Fai clic su **[!UICONTROL Salva]**.

   Quando sei pronto a pubblicare il tuo percorso, puoi rivedere queste impostazioni facendo clic su _[!UICONTROL Publish]_.
