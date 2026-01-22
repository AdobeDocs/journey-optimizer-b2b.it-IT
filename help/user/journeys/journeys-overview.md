---
title: Gestione dei percorsi
description: 'Semplifica la generazione della domanda con i percorsi: crea, pubblica, gestisci il coinvolgimento dei gruppi di acquisto tramite e-mail, SMS ed eventi in Journey Optimizer B2B edition.'
feature: Account Journeys
role: User
exl-id: 5c22f11f-1967-4b55-8aee-16371173c040
source-git-commit: 6511f40329df34db665ed6f971fa20670be0ae32
workflow-type: tm+mt
source-wordcount: '1521'
ht-degree: 44%

---


# Gestione dei percorsi

In Journey Optimizer B2B edition, i percorsi sono account automatizzati a più passaggi e piani di marketing basati su lead che orchestrano esperienze personalizzate tra canali in risposta a coinvolgimento, eventi di business o campagne pianificate. Definisci un coinvolgimento basato sulle vendite che includa e-mail, SMS e altro ancora in per coordinare il marketing in entrata con le attività di vendita in uscita per ogni membro del gruppo di acquisto.

Journey Optimizer B2B edition supporta due tipi di percorso:

* **percorsi di account** - Semplifica la generazione della domanda e la qualificazione dei gruppi di acquisto e genera una domanda più qualificata per i programmi di acquisizione, upselling/cross-selling e fidelizzazione. Adatta i percorsi a ogni gruppo acquisti e membro del gruppo acquisti utilizzando il coinvolgimento automatizzato per e-mail, SMS, eventi e altro ancora.

  ![Video](../../assets/do-not-localize/icon-video.svg){width="30"} [Guarda il video introduttivo sul percorso di account](#overview-video)

* **percorsi di persone** - (Beta) Orchestrazione di marketing basato su lead tramite dati e tipi di pubblico di Experience Platform. Con i percorsi di persone, le operazioni di marketing non si basano su Marketo Engage o su soluzioni alternative per le catene di strumenti Adobe Campaign/B2C, in modo che possano funzionare con i casi di utilizzo B2B.

  Se utilizzato insieme a percorsi di account e gruppi di acquisto, un percorso di persone può fornire agli addetti al marketing la possibilità di applicare l’orchestrazione completa al percorso di acquisto.

  +++Limitazioni attuali per i percorsi di persone

  Esistono limitazioni che potrebbero bloccare alcuni casi d’uso o causare difficoltà nella creazione di percorsi di persone. Molti problemi sono il risultato dell’implementazione iniziale del programma beta, che sarà affrontata in futuro.

   * Gli eventi non possono essere combinati con gli attributi di profilo per limitare le definizioni di pubblico.
   * Il contesto dell’evento che qualifica un profilo per un percorso non può essere utilizzato per la personalizzazione o l’orchestrazione.
   * Al momento i percorsi non possono avere sia un criterio di immissione evento che un criterio di immissione segmento profilo.
   * I listener di eventi non possono ascoltare più eventi.
   * Al momento i nodi di attesa non dispongono di una suite completa di opzioni per i criteri di uscita relativi al giorno della settimana o all’ora del giorno.
   * L’editor e-mail fa erroneamente riferimento a funzionalità e attributi disponibili solo per i Percorsi di account
   * Il supporto per i token di percorso personalizzati (_I miei token_) non è ancora disponibile.
   * Aggiungi e rimuovi da nodi del percorso di persone non è attualmente disponibile da nessuno dei tipi di percorso.
   * Impossibile utilizzare la cronologia eventi per l&#39;orchestrazione o la personalizzazione.
   * Gli oggetti correlati (ad esempio account, gruppo di acquisto, opportunità e oggetti personalizzati) non possono essere utilizzati per l’orchestrazione o la personalizzazione.
   * I canali web, SMS e della piattaforma di annunci non sono attualmente supportati.

  +++

## Introduzione a un percorso

Per iniziare a usare il primo percorso:

1. [Crea un percorso](./create-publish-journey.md#create-a-journey).
1. [Aggiungi i nodi](./create-publish-journey.md#add-a-node) e [definisci il flusso del percorso](./create-publish-journey.md#add-and-delete-a-path) nella relativa mappa.
1. [Pubblica il percorso](./create-publish-journey.md#publish-a-journey).

## Accedere ai percorsi e sfogliarli

>[!BEGINTABS]

>[!TAB percorsi di account]

Nella barra di navigazione a sinistra, espandi **[!UICONTROL Gestione Percorsi]** e fai clic su **[!UICONTROL percorsi account]**.

Immetti il testo nello strumento _Ricerca_ nella parte superiore dell’elenco per filtrare l’elenco visualizzato in base al nome.

![Filtrare l’elenco dei percorsi account](./assets/account-journeys-list-search-filter.png){width="800" zoomable="yes"}

>[!TAB percorsi di persone (Beta)]

[!BADGE Beta]{type=Informative tooltip="Disponibile come funzione beta sull’architettura semplificata"}

Nella barra di navigazione a sinistra, espandi **[!UICONTROL Gestione Percorsi]** e fai clic su **[!UICONTROL percorsi di persone]**.

Immettere il testo nello strumento _Ricerca_ nella parte superiore dell&#39;elenco per filtrare l&#39;elenco visualizzato in base al nome.

![Filtra l&#39;elenco dei percorsi di persone](./assets/person-journeys-list-search-filter.png){width="800" zoomable="yes"}

>[!ENDTABS]

### Colonne elenco percorso

La pagina dell&#39;elenco percorsi include le colonne riportate di seguito.

* [!UICONTROL Nome] (fai clic sul nome per aprire il percorso per la modifica)
* [!UICONTROL Stato]
* [!UICONTROL Data di creazione]
* [!UICONTROL Creato da]
* [!UICONTROL Ultimo aggiornamento]
* [!UICONTROL Ultimo aggiornamento effettuato da]
* [!UICONTROL Pubblicato il]
* [!UICONTROL Pubblicato da]
* [!UICONTROL Data di inizio]
* [!UICONTROL Data di fine]

Puoi ordinare l&#39;elenco in base a _[!UICONTROL Stato]_, _[!UICONTROL Data di creazione]_ o _[!UICONTROL Ultimo aggiornamento]_ facendo clic sull&#39;intestazione della colonna.

Per personalizzare (mostrare/nascondere) le colonne visualizzate nella tabella, fare clic sull&#39;icona _Personalizza tabella_ ( ![Personalizza tabella](../assets/do-not-localize/icon-column-settings.svg) ) nell&#39;angolo superiore destro. Seleziona o deseleziona le caselle di controllo nella finestra di dialogo e fai clic su **[!UICONTROL Applica]**.

![Selezionare le colonne da visualizzare nell&#39;elenco percorsi](./assets/account-journeys-list-columns.png){width="800" zoomable="yes"}

### Stato del percorso

Lo stato di un percorso può cambiare in base alle azioni applicate. In base allo stato di un percorso, alcune azioni sono/non sono disponibili nel lato destro dell’intestazione.

| Stato | Descrizione | Azioni disponibili |
| ------ | ----------- | ----------------- |
| _&#x200B;**Bozza**&#x200B;_ | Un percorso non pubblicato che può essere modificato. | <li>[Pubblica](./create-publish-journey.md#publish-a-journey)<li>[Duplica](#duplicate-journey) <li>[Elimina](#delete-journey) |
| _&#x200B;**Live**&#x200B;_ | Lo stato del percorso cambia da _Bozza_ a _Live_ quando viene pubblicato un percorso. Se il percorso si trova in questo stato, non può più essere modificato. | <li>[Duplica](#duplicate-journey)<li>[Chiudi ai nuovi ingressi](#close-to-new-entries) <li>[Interrompi](#abort-journey) |
| _&#x200B;**Chiuso alle nuove voci**&#x200B;_ | Lo stato del percorso cambia da _Live_ a _Chiuso alle nuove voci_ quando fai clic su [!UICONTROL Chiudi alle nuove voci] nel menu di navigazione superiore. | <li>[Duplica](#duplicate-journey) <li>[Interrompi](#abort-journey) |
| _&#x200B;**Annullato**&#x200B;_ | Lo stato del percorso cambia da _Live_ o _Chiuso alle nuove voci_ quando interrompi un percorso. Un percorso interrotto non può essere riavviato. | <li>[Duplica](#duplicate-journey) <li>[Elimina](#delete-journey) |
| _&#x200B;**Completato**&#x200B;_ | Quando tutti i membri del pubblico dell&#39;account o della persona in un percorso completano il percorso, lo stato cambia da _Live_ o _Closed to new entries_ a _Finished_. | <li>[Duplica](#duplicate-journey) <li>[Elimina](#delete-journey) |

## Mappe percorso

Fare clic sul nome (visualizzato come collegamento) nell&#39;elenco percorsi per esaminare i dettagli, apportare modifiche ed eseguire azioni.

![Area di lavoro percorso account](./assets/account-journey-workspace.png){width="800" zoomable="yes"}

L’intestazione di ciascuna mappa del percorso include:

* Nome del percorso
* Strumento di modifica per il nome del percorso ( ![icona Modifica](../assets/do-not-localize/icon-edit.svg) icona _Modifica_)
* [Stato](#journey-status) del percorso

Dalla mappa del percorso, puoi [Aggiungere i nodi](./create-publish-journey.md#add-a-node) e [definire il flusso di percorso](./create-publish-journey.md#add-and-delete-a-path).

## Azioni percorso

La pagina dell’elenco percorsi include tutti i percorsi di account o persone nell’istanza Journey Optimizer B2B edition. Dalla pagina dell’elenco, puoi applicare una serie di azioni a un percorso.

### Interrompi percorso

Se interrompi un percorso live o pianificato, gli account o le persone nel percorso interrompono immediatamente i loro progressi e non può accadere alcun ulteriore ingresso nel percorso. Un percorso interrotto non può essere riavviato.

>[!IMPORTANT]
>
>Quando il percorso viene utilizzato in un altro percorso da un nodo _Esegui un&#39;azione_ con l&#39;azione _[!UICONTROL Aggiungi account a (altro) Percorso]_, l&#39;interruzione del percorso blocca tale azione in tale percorso.

1. Fai clic sul nome del percorso per aprirlo.

1. Fai clic sul menu **[!UICONTROL Altro...]** in alto a destra e scegli **[!UICONTROL Interrompi]**.

   ![Fai clic su Altro in alto a destra](./assets/account-journey-live-more-menu.png){width="450"}

1. Nella finestra di dialogo di conferma, fai clic su **[!UICONTROL Interrompi]**.

### Chiudi ai nuovi ingressi

Se chiudi un percorso live, gli account attualmente presenti nel percorso continuano ad avanzare in quel percorso e nessun ulteriore ingresso nel percorso è possibile. Un percorso chiuso non può essere riavviato, ma può essere duplicato.

>[!IMPORTANT]
>
>Quando il percorso viene utilizzato in un altro percorso da un nodo _Esegui un&#39;azione_ con l&#39;azione _[!UICONTROL Aggiungi account a (altro) Percorso]_, la chiusura del nodo alle nuove voci blocca l&#39;azione da tale percorso.

1. Fai clic sul nome del percorso per aprirlo.

1. Fai clic sul menu **[!UICONTROL Altro...]** in alto a destra e scegli **[!UICONTROL Chiudi ai nuovi ingressi]**.

1. Nella finestra di dialogo di conferma, fai clic su **[!UICONTROL Chiudi a nuovi ingressi]**.

### Duplicare un percorso

Un’azione di duplicazione è simile a una funzione di clonazione, ma un percorso duplicato non include le risorse dei contenuti del percorso create. Puoi duplicare i dettagli per il percorso o solo una semplice _ossatura_ della struttura del flusso e del percorso.

>[!NOTE]
>
>Questa azione non è attualmente disponibile per percorsi di persone.

1. Fai clic sull’icona _Altro_ (**...**) accanto al nome del percorso e scegli **[!UICONTROL Duplica]**.

   ![Fai clic sull’icona ... e scegli Duplica](./assets/account-journeys-list-more-menu.png){width="450"}

   A seconda dello stato del percorso, puoi anche accedere all’azione duplicata dai dettagli del percorso o dalla mappa del percorso:

   * Per un percorso in stato di bozza, fai clic sul menu **[!UICONTROL Altro...]** in alto a destra e scegli **[!UICONTROL Duplica]**.

   * Per tutti gli altri stati del percorso, fai clic su **[!UICONTROL Duplica]** in alto a destra.

     ![Fai clic su Duplica in alto a destra](./assets/account-journey-duplicate-button.png){width="450"}

1. Nella finestra di dialogo _Duplica percorso_, imposta **[!UICONTROL Nome]** e **[!UICONTROL Descrizione]** per il nuovo percorso.

   Per impostazione predefinita, la finestra di dialogo utilizza il nome del percorso duplicato a cui è stato aggiunto __copia_. Immetti un altro nome univoco per il percorso, in base alle esigenze.

   ![Finestra di dialogo Duplica percorso](./assets/account-journey-duplicate-dialog.png){width="400"}

1. Scegli il **[!UICONTROL Tipo]** di duplicazione:

   * **[!UICONTROL Duplicazione parziale del contenuto]**: utilizza questo tipo per copiare tutto ciò che si trova nel percorso, esclusi i messaggi e-mail o SMS creati. I nodi che fanno riferimento a un messaggio e-mail o SMS di Marketo Engage rimangono completamente intatti.

   * **[!UICONTROL Duplica senza dettagli]**: utilizza questo tipo per copiare solo la struttura e i percorsi dei nodi. Tutte le impostazioni del nodo e le condizioni del percorso non sono definite (impostazione predefinita), pertanto puoi riutilizzare il flusso di base con diverse impostazioni di pubblico, azioni e segmentazione del percorso. Tutti i nodi _Attendi_ utilizzano il valore predefinito di cinque giorni.

1. Fai clic su **[!UICONTROL Duplica]**.

   Il percorso duplicato viene aperto nella mappa del percorso, dove è possibile impostare i dettagli e creare il contenuto del percorso in base alle esigenze.

### Eliminare un percorso

Utilizza un’azione di eliminazione per eliminare definitivamente un percorso. Non puoi eliminare un percorso live o pianificato.

1. Fai clic sull’icona _Altro_ (**...**) accanto al nome del percorso e scegli **[!UICONTROL Elimina]**.

   A seconda dello stato del percorso, puoi anche accedere all’azione di eliminazione dai dettagli del percorso o dalla mappa del percorso:

   * Per un percorso in stato di bozza, fai clic sul menu **[!UICONTROL Altro...]** in alto a destra e scegli **[!UICONTROL Elimina]**.

   * Per altri stati del percorso, ad esempio _Completato_ o _Interrotto_, fai clic su **[!UICONTROL Elimina]** in alto a destra.

1. Nella finestra di dialogo di conferma, fai clic su **[!UICONTROL Elimina]**.

## Rivedere l’avanzamento degli account

Per un percorso di account pubblicato che si trova nello stato _Live_, _Chiuso alle nuove voci_, _Interrotto_ o _Completato_, puoi aprire la mappa del percorso per esaminare la progressione dell&#39;account per i nodi del percorso. Ogni nodo sulla mappa mostra il numero di account che hanno raggiunto quel nodo e, per i percorsi live, il numero di account che si trovano attualmente a quel nodo.

![Informazioni sull’avanzamento degli account attraverso i nodi del percorso](./assets/node-account-progression-observability.png){width="400"}

Quando selezioni il nodo, fai clic sul numero per visualizzare un elenco di account che sono entrati nel nodo o che si trovano attualmente a quel passaggio del percorso.

![Informazioni sull’avanzamento degli account attraverso i nodi del percorso](./assets/node-accounts-entered-list.png){width="700" zoomable="yes"}

## Video introduttivo sul percorso di account {#overview-video}

>[!VIDEO](https://video.tv.adobe.com/v/3443215/?captions=ita&learn=on)
