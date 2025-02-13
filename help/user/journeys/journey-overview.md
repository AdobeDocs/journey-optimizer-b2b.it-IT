---
title: Percorsi account
description: Scopri come creare e gestire i percorsi di account.
feature: Account Journeys
exl-id: 5c22f11f-1967-4b55-8aee-16371173c040
source-git-commit: d03e0e2d8070916d38bb956adff8dea3f3873aad
workflow-type: tm+mt
source-wordcount: '575'
ht-degree: 2%

---


# Percorsi di account

Crea ed esegui percorsi personalizzati per ogni gruppo di acquisto e membro del gruppo di acquisto utilizzando il coinvolgimento automatico per e-mail, SMS, eventi e altro ancora. Con i percorsi di account è possibile semplificare la generazione della domanda e la qualificazione dei gruppi di acquisto e aumentare la domanda qualificata per i programmi di acquisizione, upselling/cross-selling e fidelizzazione.

Definisci un coinvolgimento basato sulle vendite che includa e-mail, SMS e altri percorsi di account interni per coordinare le attività di marketing in entrata con le attività di vendita in uscita per ciascun membro del gruppo di acquisto.

![Video](../../assets/do-not-localize/icon-video.svg){width="30"} [Guarda il video introduttivo](#overview-video)

## Accedere e sfogliare i percorsi di account

1. Nella home page di Adobe Experience Platform, fare clic su Adobe Journey Optimizer B2B edition.

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

* **Pubblicazione** - È possibile pubblicare un percorso se non sono presenti errori di blocco. Quando viene pubblicato, lo stato del percorso cambia in _Live_. Se il percorso presenta errori, il pulsante viene oscurato con le informazioni sul contenuto: `Resolve errors before publishing`.
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

Per iniziare a usare i percorsi di account:

1. [Crea un percorso](./create-publish-journey.md#create-an-account-journey).
1. [Aggiungi i nodi](./create-publish-journey.md#add-a-node) e [definisci il flusso di percorso](./create-publish-journey.md#add-and-delete-a-path) nella mappa del percorso.
1. [Pubblica il percorso](./create-publish-journey.md#publish-an-account-journey).

## Video introduttivo

>[!VIDEO](https://video.tv.adobe.com/v/3443202/?learn=on)
