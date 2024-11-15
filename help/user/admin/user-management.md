---
title: Gestione utente
description: Scopri come assegnare i membri del gruppo ai profili di prodotto di Journey Optimizer B2B edition.
feature: Setup
roles: Admin
exl-id: ddbdc6a5-49bc-46cd-8d9b-1d37223dffe2
source-git-commit: 97a9932a8a2a1c7a37dcc110b59cee70a61b5763
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Gestione degli utenti

Dopo aver completato il provisioning e aver associato le sandbox, completa i passaggi seguenti per fornire al team e agli utenti l’accesso a Adobe Journey Optimizer B2B edition.

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

   Dopo aver effettuato l&#39;accesso, viene visualizzata la pagina _Panoramica_ di Adobe Admin Console.

1. Se hai accesso a più organizzazioni, assicurati di aver effettuato l’accesso all’organizzazione corretta.

   Per modificare l’organizzazione, fai clic sul nome dell’organizzazione nell’angolo in alto a destra e scegli l’organizzazione a cui desideri accedere.

1. Seleziona **[!UICONTROL Amministratori]** dalla scheda _[!UICONTROL Utenti]_ per verificare di essere un amministratore di sistema.

   ![Panoramica Admin Console - fare clic su Amministratori](./assets/admin-console-overview-administrators.png){width="700" zoomable="yes"}

1. Effettua la ricerca immettendo e-mail, nome utente, nome o cognome Adobe ID.

   * Se l’accesso è configurato correttamente, la ricerca restituisce il record.

   * Se il valore nella colonna **[!UICONTROL RUOLO AMMINISTRATORE]** mostra `System`, l&#39;amministratore di sistema è tu o l&#39;utente visualizzato.

## Creare il profilo di prodotto Marketo Engage {#marketo-engage-profile}

Quando consenti l’accesso a una soluzione Adobe agli utenti, non devi necessariamente concedere loro l’accesso completo. I profili di prodotto consentono a ciascuna soluzione di disporre di un proprio set di autorizzazioni utente. Utilizza l’Admin Console per assegnare profili di prodotto.

Per ulteriori informazioni sull&#39;utilizzo dei profili di prodotto per i diritti utente, consulta [Gestire i profili di prodotto per gli utenti aziendali](https://helpx.adobe.com/it/enterprise/using/manage-product-profiles.html){target="_blank"} nella documentazione di Admin Console.
<!--
>[!BEGINSHADEBOX]

When you add a user to the Marketo Engage product profile, they are subsequently added to the _Standard User_ role within the Default workspace of the Marketo Engage subscription. This role grants them all _Standard User_ permissions for Marketo Engage in that workspace. Currently, all Journey Optimizer B2B Edition users are required to be Marketo Engage users. A Marketo Engage administrator can restrict access by updating the permissions for the _Standard User_ role or by moving the user to a different Marketo Engage user role with more restrictive permissions.

For more information about managing these permissions within Marketo Engage, see [Managing User Roles and Permissions](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/users-and-roles/managing-user-roles-and-permissions){target="_blank"} in the Marketo Engage documentation.

>[!ENDSHADEBOX]-->

>[!NOTE]
>
>Un amministratore di Admin Console o un amministratore di prodotto di Marketo Engage può eseguire questi passaggi.

1. Accedi a [https://adminconsole.adobe.com](https://adminconsole.adobe.com).

1. Selezionare la scheda **[!UICONTROL Prodotti]**.

1. Apri l’istanza Market Engage in cui desideri aggiungere il profilo e fai clic su Nuovo profilo.

   ![Admin Console - Istanza Marketo Engage - Nuovo profilo](./assets/admin-console-marketo-engage-instance-new-profile.png){width="700" zoomable="yes"}

1. Immettere un nome di profilo prodotto, ad esempio _Utente standard_.

1. Fai clic su **Avanti** e quindi su **Salva**.

## Creare un gruppo di utenti {#create-user-group}

Un gruppo di utenti è una raccolta di utenti a cui viene concesso un set condiviso di autorizzazioni. Puoi aggiungere o rimuovere utenti nel gruppo di utenti. Le autorizzazioni del gruppo rimangono invariate mentre gli utenti all’interno del gruppo cambiano.

Per ulteriori informazioni sulle modalità di utilizzo dei gruppi di utenti per gestire le autorizzazioni, vedi [Gestione dei gruppi di utenti](https://helpx.adobe.com/it/enterprise/using/user-groups.html){target="_blank"} nella documentazione di Admin Console.

>[!NOTE]
>
>Un amministratore di Admin Console può eseguire questi passaggi.

1. Accedi a [https://adminconsole.adobe.com](https://adminconsole.adobe.com).

1. Selezionare la scheda **[!UICONTROL Utenti]**.

1. Scegliere **[!UICONTROL Gruppi utenti]** nel menu di navigazione a sinistra.

1. Fai clic su **[!UICONTROL Nuovo gruppo utenti]** in alto a destra.

1. Immetti un nome per il gruppo di utenti, ad esempio _Utenti standard_ e fai clic su **[!UICONTROL Salva]**.

1. Fai clic sul gruppo di utenti appena creato.

1. Seleziona la scheda **[!UICONTROL Profili di prodotto assegnati]** e fai clic su **[!UICONTROL Assegna profilo]**.

1. Fai clic su **+** e aggiungi ogni istanza dei seguenti prodotti:

   * [!UICONTROL Marketo Engage]
   * [!UICONTROL Adobe Experience Platform - AEP-Default-All-Users]
   * [!UICONTROL Raccolta dati di Adobe Experience Platform]
   * [!UICONTROL Accesso a tutti gli elementi della raccolta dati]

   ![Admin Console - user-group - aggiungi prodotti](./assets/admin-console-user-group-add-products.png){width="700" zoomable="yes"}

1. Fai clic su **[!UICONTROL Salva]**.

## Creare un ruolo nelle autorizzazioni AEP {#create-role}

Le autorizzazioni sono diritti unitari che ti consentono di definire le autorizzazioni assegnate a un profilo di prodotto. Ogni autorizzazione viene riunita in una funzionalità, ad esempio percorsi o gruppi di acquisto, che rappresenta le diverse funzionalità o oggetti di Journey Optimizer B2B edition.

Nell&#39;area _Autorizzazioni_ di Adobe Experience Platform gli amministratori possono definire ruoli utente e criteri di accesso per gestire le autorizzazioni di accesso per funzionalità e oggetti all&#39;interno di un&#39;applicazione di prodotto. In questa app, puoi creare e gestire i ruoli, nonché assegnare le autorizzazioni per le risorse desiderate per tali ruoli. Le autorizzazioni ti consentono inoltre di gestire le etichette, le sandbox e gli utenti associati a un ruolo specifico.

Per ulteriori informazioni, vedi [Gestione delle autorizzazioni per un ruolo](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/abac/permissions-ui/permissions){target="_blank"} nella documentazione di Experience Platform.

>[!NOTE]
>
>Per completare i passaggi seguenti, devi essere un amministratore di prodotto per Adobe Experience Platform.

1. Vai a [experience.adobe.com](https://experience.adobe.com/).

1. Nel pannello _[!UICONTROL Accesso rapido]_, seleziona **[!UICONTROL Autorizzazioni]**.

   >[!NOTE]
   >
   >Se non trovi _[!UICONTROL Autorizzazioni]_, potresti dover fare clic su **[!UICONTROL Visualizza tutto]** e selezionarlo dalle applicazioni disponibili.

   ![Experience Platform - autorizzazioni di accesso](./assets/aep-permissions.png){width="700" zoomable="yes"}

1. Seleziona **[!UICONTROL Ruoli]** nell&#39;area di navigazione a sinistra e seleziona **[!UICONTROL Crea ruolo]**.

1. Nella finestra di dialogo _[!UICONTROL Crea nuovo ruolo]_, immetti un nome per il ruolo, ad esempio _AJO B2B_, e una descrizione (facoltativa).

1. Fai clic su **[!UICONTROL Conferma]**.

1. Seleziona le sandbox.

   ![Experience Platform - aggiungi sandbox per il nuovo ruolo](./assets/aep-permissions-role-sandboxes.png){width="700" zoomable="yes"}

1. Aggiungi le autorizzazioni profilo:

   * Nell&#39;elenco _[!UICONTROL Risorse]_ a sinistra, individuare l&#39;elemento **[!UICONTROL Gestione profili]** e fare clic sull&#39;icona più (**+**) per aggiungere l&#39;attributo.

   * Per l’attributo, aggiungi le seguenti autorizzazioni:
      * [!UICONTROL Visualizza segmenti]
      * [!UICONTROL Gestisci segmenti]
      * [!UICONTROL Visualizza profili]
      * [!UICONTROL Gestisci profili]
      * [!UICONTROL Visualizza profilo B2B]
      * [!UICONTROL Gestisci profilo B2B]

   ![Experience Platform - aggiungi profili per il nuovo ruolo](./assets/aep-permissions-role-profiles.png){width="700" zoomable="yes"}

1. Fai clic su **[!UICONTROL Salva]** in alto a destra.

1. Vai ai dettagli del ruolo e seleziona la scheda **[!UICONTROL Gruppi di utenti]**.

1. Fare clic su **[!UICONTROL Aggiungi gruppi]**.

   ![Experience Platform - aggiungi profili per il nuovo ruolo](./assets/aep-permissions-role-add-groups.png){width="700" zoomable="yes"}

1. Seleziona la casella di controllo accanto al gruppo di utenti creato in precedenza nell’Admin Console.

1. Fai clic su **[!UICONTROL Salva]**.

## Aggiungere utenti al gruppo nell&#39;Admin Console

>[!NOTE]
>
>Un amministratore di Admin Console o un amministratore di prodotto può eseguire questi passaggi.

Per informazioni sulla gestione degli utenti, vedi [utenti Admin Console](https://helpx.adobe.com/it/enterprise/using/user-groups.html) nella documentazione di Admin Console.

1. Vai a [https://adminconsole.adobe.com](https://adminconsole.adobe.com).

1. In _[!UICONTROL Collegamenti rapidi]_, fare clic su **[!UICONTROL Aggiungi utenti]**.

1. Aggiungi ogni utente:

   * Immetti l’indirizzo e-mail, il nome e il cognome dell’utente.

     ![Experience Platform - aggiungi profili per il nuovo ruolo](./assets/admin-console-add-users.png){width="600" zoomable="yes"}

   * Per **[!UICONTROL Gruppi utenti]**, fare clic su **+**.

   * Seleziona il gruppo di utenti creato in precedenza.

   * Fare clic su **[!UICONTROL Applica]**.

1. Fai clic su **[!UICONTROL Salva]**.
