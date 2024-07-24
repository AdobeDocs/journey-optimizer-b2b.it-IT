---
title: Gestione degli utenti
description: Scopri come assegnare i membri del gruppo ai profili di prodotto della versione B2B di Journey Optimizer.
feature: Setup
roles: Admin
source-git-commit: dcd8ab2820d60654e8970944054142fc296ed54f
workflow-type: tm+mt
source-wordcount: '883'
ht-degree: 1%

---

# Gestione degli utenti

Dopo aver completato il provisioning e aver associato le sandbox, completa i passaggi seguenti per fornire a team e utenti l’accesso all’edizione B2B di Adobe Journey Optimizer.

1. [Creare un profilo di prodotto di Marketo Engage](#marketo-engage-profile) nell&#39;Admin Console (solo nuova istanza di Marketo Engage).
1. [Creare un gruppo di utenti](#create-user-group) nell&#39;Admin Console.
1. [Crea un ruolo](#create-role) nelle autorizzazioni AEP.
1. [Aggiungi utenti](#add-users) nell&#39;Admin Console.

In qualità di amministratore, puoi completare queste attività in Adobe Admin Console, che è una posizione centrale per amministrare e gestire le licenze e gli utenti dei prodotti Adobe. Nell’Admin Console, puoi creare e gestire gli utenti in un’unica posizione invece che all’interno delle varie soluzioni individuali. Per ulteriori informazioni sulle funzioni e le funzionalità della pagina [Panoramica dell&#39;Admin Console](https://helpx.adobe.com/it/enterprise/using/admin-console.html), fare riferimento a.

## Accedere all’Admin Console

Prima di poter utilizzare l’Admin Console per amministrare gli utenti del team, è necessario assicurarsi di poter accedere all’Admin Console e di disporre delle autorizzazioni appropriate.

1. In qualità di amministratore di sistema, come parte del processo di onboarding dovresti ricevere più e-mail da Adobe.

   Cerca l’e-mail di benvenuto con le informazioni sul nome dell’organizzazione a cui hai accesso.

1. Fai clic sul collegamento **[!UICONTROL Inizia]** nell&#39;e-mail di benvenuto per passare all&#39;Admin Console.

   Se non riesci a trovare l&#39;e-mail, apri un browser per accedere direttamente all&#39;Admin Console all&#39;indirizzo [https://adminconsole.adobe.com](https://adminconsole.adobe.com).

1. Accedi con il tuo Adobe ID.

   Dopo aver effettuato l’accesso, viene visualizzata la pagina Panoramica di Adobe Admin Console.

1. Se hai accesso a più organizzazioni, assicurati di aver effettuato l’accesso all’organizzazione corretta.

   Per modificare l’organizzazione, fai clic sul nome dell’organizzazione nell’angolo in alto a destra e scegli l’organizzazione a cui desideri accedere.

1. Dalla scheda Utenti, seleziona Amministratori per verificare di essere uno degli amministratori di sistema.

1. Effettua la ricerca immettendo e-mail, nome utente, nome o cognome Adobe ID.

   * Se l’accesso è configurato correttamente, la ricerca restituisce il record.

   * Se il valore nella colonna **[!UICONTROL RUOLO AMMINISTRATORE]** mostra `System`, l&#39;amministratore di sistema è tu o l&#39;utente visualizzato.

## Creare il profilo di prodotto Marketo Engage {#marketo-engage-profile}

Quando consenti l’accesso a una soluzione di Adobe agli utenti, non devi necessariamente concedere loro l’accesso completo. I profili di prodotto consentono a ciascuna soluzione di disporre di un proprio set di autorizzazioni utente. Utilizza l’Admin Console per assegnare profili di prodotto.

>[!NOTE]
>
>Questi passaggi possono essere eseguiti solo da un amministratore di Admin Console o da un amministratore di prodotto di Marketo Engage.

1. Accedi a [https://adminconsole.adobe.com](https://adminconsole.adobe.com).

1. Scegliete Prodotti > Marketo Engage.

1. Fai clic su Nuovo profilo e immetti un nome di profilo di prodotto, ad esempio _Utente standard_.

1. Fai clic su Avanti > Salva

## Creare un gruppo di utenti {#create-user-group}

Un gruppo di utenti è una raccolta di utenti a cui viene concesso un set condiviso di autorizzazioni. Puoi aggiungere o rimuovere utenti nel gruppo di utenti. Le autorizzazioni del gruppo rimangono invariate mentre gli utenti all’interno del gruppo cambiano.

>[!NOTE]
>
>Questi passaggi possono essere eseguiti solo da un amministratore di Admin Console.

1. Accedi a [https://adminconsole.adobe.com](https://adminconsole.adobe.com).

1. Scegliere **[!UICONTROL Utenti]** > **[!UICONTROL Gruppi utenti]** > **[!UICONTROL Nuovo gruppo utenti]**.

1. Immetti un nome per il gruppo di utenti, ad esempio _Utenti standard_ e fai clic su **[!UICONTROL Salva]**.

1. Fai clic sul gruppo di utenti appena creato.

1. Fai clic su **[!UICONTROL Profili di prodotto assegnati]** > **[!UICONTROL Assegna profilo]**.

1. Seleziona i seguenti prodotti:
   * [!UICONTROL Marketo Engage - Utente standard]
   * [!UICONTROL Adobe Experience Platform - AEP-Default-All-Users]
   * [!UICONTROL Raccolta dati Adobe Experience Platform - Predefinito]
   * [!UICONTROL Accesso a tutti gli elementi della raccolta dati]

1. Fai clic su **[!UICONTROL Salva]**.

## Creare un ruolo nelle autorizzazioni AEP {#create-role}

Le autorizzazioni sono diritti unitari che ti consentono di definire le autorizzazioni assegnate a un profilo di prodotto. Ogni autorizzazione viene riunita in una funzionalità, ad esempio percorsi o gruppi di acquisto, che rappresenta le diverse funzionalità o oggetti di Journey Optimizer B2B Edition.

_Autorizzazioni_ è l&#39;area di Adobe Experience Platform in cui gli amministratori possono definire i ruoli utente e i criteri di accesso per gestire le autorizzazioni di accesso per funzionalità e oggetti all&#39;interno di un&#39;applicazione di prodotto. In questa app, puoi creare e gestire i ruoli, nonché assegnare le autorizzazioni per le risorse desiderate per tali ruoli. Le autorizzazioni ti consentono inoltre di gestire le etichette, le sandbox e gli utenti associati a un ruolo specifico.

>[!NOTE]
>
>Per completare i passaggi seguenti, devi essere un amministratore di prodotto per Adobe Experience Platform.

1. Vai a [experience.adobe.com](https://experience.adobe.com/).

1. Seleziona **[!UICONTROL Autorizzazioni]**.

   >[!NOTE]
   >
   >Se Autorizzazioni non è visualizzato, potrebbe essere necessario fare clic su Visualizza tutto e selezionarlo dalle applicazioni disponibili.

1. Seleziona **[!UICONTROL Ruoli]** nell&#39;area di navigazione a sinistra e seleziona **[!UICONTROL Crea ruolo]**.

1. Nella finestra di dialogo _[!UICONTROL Crea nuovo ruolo]_, immettere un nome per il ruolo, ad esempio _Utente standard_, e una descrizione (facoltativa).

1. Fai clic su **[!UICONTROL Conferma]**.

1. Seleziona le sandbox.

1. Aggiungi le autorizzazioni profilo:

   * Nell&#39;elenco _[!UICONTROL Risorse]_ a sinistra, individuare l&#39;elemento **[!UICONTROL Gestione profili]** e fare clic sull&#39;icona più (**+**) per aggiungere l&#39;attributo.

   * Per l’attributo, aggiungi le seguenti autorizzazioni:
      * [!UICONTROL Visualizza segmenti]
      * [!UICONTROL Gestisci segmenti]
      * [!UICONTROL Visualizza profili]
      * [!UICONTROL Gestisci profili]
      * [!UICONTROL Visualizza profilo B2B]
      * [!UICONTROL Gestisci profilo B2B]

1. Fai clic su **[!UICONTROL Salva]** in alto a destra.

1. Scegliere **[!UICONTROL Gruppi utenti]** > **[!UICONTROL Aggiungi gruppi]**.

1. Seleziona la casella di controllo accanto al gruppo di utenti creato in precedenza nell’Admin Console.

1. Fai clic su **[!UICONTROL Salva]**.

## Aggiungere utenti nell’Admin Console

>[!NOTE]
>
>Questi passaggi possono essere eseguiti solo da un amministratore di Admin Console o da un amministratore di prodotto.

1. Vai a [https://adminconsole.adobe.com](https://adminconsole.adobe.com).

1. Fare clic su **[!UICONTROL Aggiungi utenti]**.

1. Aggiungi ogni utente:

   * Immetti l’indirizzo e-mail, il nome e il cognome dell’utente.
   * Fare clic su [!UICONTROL Gruppi utenti].
   * Seleziona il gruppo di utenti creato in precedenza.

1. Fare clic su **[!UICONTROL Applica]**.

1. Fai clic su **[!UICONTROL Salva]**.
