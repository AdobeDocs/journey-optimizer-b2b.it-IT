---
title: Percorsi account
description: Inizia a usare i percorsi account e scopri come gestirli utilizzando l’elenco Percorsi account.
feature: Account Journeys
role: User
exl-id: 5c22f11f-1967-4b55-8aee-16371173c040
source-git-commit: a67ab8268676050f0c5f34b94d4aebfd46aaf601
workflow-type: ht
source-wordcount: '1027'
ht-degree: 100%

---


# Percorsi account

Con i percorsi account puoi semplificare la generazione della domanda e la qualificazione dei gruppi acquisti e aumentare la domanda qualificata per i programmi di acquisizione, upselling/cross-selling e conservazione. Adatta i percorsi a ogni gruppo acquisti e membro del gruppo acquisti utilizzando il coinvolgimento automatizzato per e-mail, SMS, eventi e altro ancora.

Definisci un coinvolgimento basato sulle vendite che includa e-mail, SMS e altri percorsi account interni per coordinare le attività di marketing in entrata con le attività di vendita in uscita per ciascun membro del gruppo acquisti.

![Video](../../assets/do-not-localize/icon-video.svg){width="30"} [Guarda il video introduttivo](#overview-video)

## Introduzione a un percorso

Per iniziare a utilizzare i percorsi account:

1. [Crea un percorso](./create-publish-journey.md#create-an-account-journey).
1. [Aggiungi i nodi](./create-publish-journey.md#add-a-node) e [definisci il flusso del percorso](./create-publish-journey.md#add-and-delete-a-path) nella relativa mappa.
1. [Pubblica il percorso](./create-publish-journey.md#publish-an-account-journey).

## Accedere e sfogliare i percorsi account

Nella barra di navigazione a sinistra, espandi **[!UICONTROL Gestione account]** e fai clic su **[!UICONTROL Percorsi account]**.

Immetti il testo nello strumento _Ricerca_ nella parte superiore dell’elenco per filtrare l’elenco visualizzato in base al nome.

![Filtrare l’elenco dei percorsi account](./assets/account-journeys-list-search-filter.png){width="800" zoomable="yes"}

La pagina dell’elenco _[!UICONTROL Percorsi account]_ include le colonne riportate di seguito:

* [!UICONTROL Nome] (fai clic sul nome per aprire il percorso per la modifica)
* [!UICONTROL Stato]
* [!UICONTROL Descrizione]
* [!UICONTROL Creato da]
* [!UICONTROL Ultimo aggiornamento il]
* [!UICONTROL Ultimo aggiornamento effettuato da]
* [!UICONTROL Pubblicato il]
* [!UICONTROL Pubblicato da]

Puoi ordinare l’elenco in base allo _[!UICONTROL Stato]_ facendo clic sull’intestazione della colonna.

Puoi personalizzare le colonne visualizzate nella tabella facendo clic sull’icona _Personalizza tabella_ ( ![Personalizza tabella](../assets/do-not-localize/icon-column-settings.svg) ) nell’angolo in alto a destra. Seleziona o deseleziona le caselle di controllo nella finestra di dialogo e fai clic su **[!UICONTROL Applica]**.

![Scegliere le colonne da visualizzare nell’elenco dei percorsi account](./assets/account-journeys-list-columns.png){width="800" zoomable="yes"}

## Anatomia di un percorso account

Fai clic sul nome (visualizzato come collegamento) nell’elenco _[!UICONTROL percorsi account]_ per rivedere i dettagli, apportare modifiche ed eseguire azioni.

![Area di lavoro percorso account](./assets/account-journey-workspace.png){width="800" zoomable="yes"}

L’intestazione di ciascuna mappa del percorso account include:

* Nome del percorso
* Strumento di modifica per il nome del percorso ( ![icona Modifica](../assets/do-not-localize/icon-edit.svg) icona _Modifica_)
* Stato del percorso

Lo stato di un percorso può cambiare in base alle azioni applicate. In base allo stato di un percorso, alcune azioni sono/non sono disponibili nel lato destro dell’intestazione.

| Stato | Descrizione | Azioni disponibili |
| ------ | ----------- | ----------------- |
| _**Bozza**_ | Un percorso non pubblicato che può essere modificato. | <li>[Pubblica](./create-publish-journey.md#publish-an-account-journey)<li>[Duplica](#duplicate-journey) <li>[Elimina](#delete-journey) |
| _**Live**_ | Quando un percorso viene pubblicato, il relativo stato cambia da Bozza a Live. Se il percorso si trova in questo stato, non può più essere modificato. | <li>[Duplica](#duplicate-journey)<li>[Chiudi ai nuovi ingressi](#close-to-new-entries) <li>[Interrompi](#abort-journey) |
| _**Chiuso alle nuove voci**_ | Lo stato del percorso cambia da _Live_ a _Chiuso alle nuove voci_ quando fai clic su [!UICONTROL Chiudi alle nuove voci] nel menu di navigazione superiore. | <li>[Duplica](#duplicate-journey) <li>[Interrompi](#abort-journey) |
| _**Annullato**_ | Lo stato del percorso cambia da _Live_ o _Chiuso alle nuove voci_ quando interrompi un percorso. Un percorso interrotto non può essere riavviato. | <li>[Duplica](#duplicate-journey) <li>[Elimina](#delete-journey) |
| _**Completato**_ | Quando tutti gli account completano il percorso, lo stato cambia da _Live_ o _Chiuso ai nuovi ingressi_ a _Completato_. | <li>[Duplica](#duplicate-journey) <li>[Elimina](#delete-journey) |

## Gestisci percorsi

L’elenco _Percorsi account_ include tutti i percorsi nell’istanza di Journey Optimizer B2B Edition.

### Interrompi percorso

Se interrompi (arresti) un percorso live o pianificato, gli account nel percorso interrompono immediatamente l’avanzamento e non può verificarsi un ulteriore ingresso nel percorso. Un percorso interrotto non può essere riavviato.

>[!IMPORTANT]
>
>Quando il percorso account viene utilizzato in un altro percorso da un nodo _Esegui un’azione_ con l’azione _Aggiungi account a (altro) Percorso_, l’interruzione del percorso blocca l’azione da tale percorso.

1. Fai clic sul nome del percorso per aprirlo.

1. Fai clic sul menu **[!UICONTROL Altro...]** in alto a destra e scegli **[!UICONTROL Interrompi]**.

   ![Fai clic su Altro in alto a destra](./assets/account-journey-live-more-menu.png){width="450"}

1. Nella finestra di dialogo di conferma, fai clic su **[!UICONTROL Interrompi]**.

### Chiudi ai nuovi ingressi

Se chiudi un percorso live, gli account attualmente presenti nel percorso continuano ad avanzare in quel percorso e nessun ulteriore ingresso nel percorso è possibile. Un percorso chiuso non può essere riavviato, ma può essere duplicato.

>[!IMPORTANT]
>
>Quando il percorso account viene utilizzato in un altro percorso da un nodo _Esegui un’azione_ con l’azione _Aggiungi account a (altro) Percorso_, la chiusura del nodo ai nuovi ingressi blocca l’azione da tale percorso.

1. Fai clic sul nome del percorso per aprirlo.

1. Fai clic sul menu **[!UICONTROL Altro...]** in alto a destra e scegli **[!UICONTROL Chiudi ai nuovi ingressi]**.

1. Nella finestra di dialogo di conferma, fai clic su **[!UICONTROL Chiudi a nuovi ingressi]**.

### Duplica percorso

Un’azione di duplicazione è simile a una funzione di clonazione, ma un percorso duplicato non include le risorse dei contenuti del percorso create. Puoi duplicare i dettagli per il percorso account o solo un semplice _schema_ della struttura del flusso e del percorso.

1. Fai clic sull’icona _Altro_ (**...**) accanto al nome del percorso e scegli **[!UICONTROL Duplica]**.

   ![Fai clic sull’icona ... e scegli Duplica](./assets/account-journeys-list-more-menu.png){width="450"}

   A seconda dello stato del percorso account, puoi anche accedere all’azione di duplicazione dai dettagli o dalla mappa del percorso:

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

   Il percorso account duplicato viene aperto nella mappa del percorso, dove puoi impostare i dettagli e creare il contenuto del percorso in base alle esigenze.

### Elimina percorso

Utilizza un’azione di eliminazione per eliminare definitivamente un percorso. Non puoi eliminare un percorso live o pianificato.

1. Fai clic sull’icona _Altro_ (**...**) accanto al nome del percorso e scegli **[!UICONTROL Elimina]**.

   A seconda dello stato del percorso account, puoi anche accedere all’azione di eliminazione dai dettagli o dalla mappa del percorso:

   * Per un percorso in stato di bozza, fai clic sul menu **[!UICONTROL Altro...]** in alto a destra e scegli **[!UICONTROL Elimina]**.

   * Per altri stati del percorso, ad esempio _Completato_ o _Interrotto_, fai clic su **[!UICONTROL Elimina]** in alto a destra.

1. Nella finestra di dialogo di conferma, fai clic su **[!UICONTROL Elimina]**.

## Video di panoramica

>[!VIDEO](https://video.tv.adobe.com/v/3443215/?learn=on&captions=ita)
