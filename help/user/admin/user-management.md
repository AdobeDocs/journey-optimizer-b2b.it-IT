---
title: Gestione utente
description: Scopri come assegnare i membri del gruppo ai profili di prodotto di Journey Optimizer B2B edition.
feature: Setup
roles: Admin
exl-id: ddbdc6a5-49bc-46cd-8d9b-1d37223dffe2
source-git-commit: 44a3bb6d986726dbbd9d2854e4fce321eac56824
workflow-type: tm+mt
source-wordcount: '1311'
ht-degree: 1%

---

# Gestione degli utenti

Dopo aver completato il provisioning e aver associato le sandbox, completa i passaggi seguenti per fornire al team e agli utenti l’accesso a Adobe Journey Optimizer B2B edition.

1. [Creare un profilo di prodotto di Marketo Engage](#marketo-engage-profile) nell&#39;Admin Console (solo nuova istanza di Marketo Engage).
1. [Creare un gruppo di utenti](#create-user-group) nell&#39;Admin Console.
1. [Modifica ruoli predefiniti](#edit-roles) o [crea un ruolo personalizzato](#create-a-custom-role) con autorizzazioni Journey Optimizer B2B edition.
1. [Aggiungi utenti](#add-users) o [gruppi](#add-user-groups-to-a-role) ai ruoli.

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

1. Aprire l&#39;istanza di Marketo Engage in cui si desidera aggiungere il profilo e fare clic su **[!UICONTROL Nuovo profilo]**.

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

## Aggiungere utenti a un gruppo

>[!NOTE]
>
>Un amministratore di Admin Console può eseguire questi passaggi.

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

## Modifica ruoli per le autorizzazioni prodotto {#edit-roles}

Le autorizzazioni sono diritti unitari che ti consentono di definire le autorizzazioni assegnate a un profilo di prodotto. Ogni autorizzazione viene riunita in una funzionalità, ad esempio percorsi o gruppi di acquisto, che rappresenta le diverse funzionalità o oggetti di Journey Optimizer B2B edition.

Nell&#39;area _Autorizzazioni_ di Adobe Experience Platform gli amministratori possono definire ruoli utente e criteri di accesso per gestire le autorizzazioni di accesso per funzionalità e oggetti all&#39;interno di un&#39;applicazione di prodotto. In questa app, puoi creare e gestire i ruoli, nonché assegnare le autorizzazioni per le risorse desiderate per tali ruoli. Le autorizzazioni ti consentono inoltre di gestire le sandbox e gli utenti associati a un ruolo specifico.

Per ulteriori informazioni sulle autorizzazioni per i ruoli in Experience Platform, vedi [Gestione delle autorizzazioni per un ruolo](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/abac/permissions-ui/permissions){target="_blank"} nella documentazione di Experience Platform.
<!-- 
### B2B product permissions

The following permissions govern access to Journey Optimizer B2B Edition capabilities:

| Category | Description | Permissions |
| -------- | ----------- | ---------- |
| B2B Account Lists | Configure, manage, view, and publish permissions for B2B account lists. These permissions include actions such as add, remove, import, and delete accounts from account lists. | <li>Manage B2B Account Lists |
| B2B Admin Configurations | Configure, manage, and view permissions for B2B administrative configurations. These permissions include digital asset management connections, asset repositories, and events. | <li>Manage B2B Admin Configurations |
| B2B Assets | Configure, manage, and view permissions for B2B assets. These permissions include emails, SMS, landing pages, fragments, templates, and images. | <li>Manage B2B Assets <li>Manage B2B Templates <li>Manage B2B Fragments|
| B2B Buying Groups | Configure, manage, and view permissions for B2B buying groups. These permissions include solution interests, roles templates, and buying group status. | <li>Manage B2B Buying Groups |
| B2B Channel Configurations | Configure, manage, and view permissions for B2B channel configurations. These permissions include settings for communication limits, API credentials, and security settings. | <li>Manage B2B Channels Configurations |
| B2B Dashboards |Configure and view permissions for B2B dashboards. These permissions include account engagement, buying group stages, surging accounts, and contact coverage. | <li>Manage B2B Dashboards |
| B2B Journeys | Configure manage, view, and publish permissions for B2B journeys. These permissions include account and person actions, event listeners, and split paths | <li>Manage B2B Journeys |

### B2B built-in roles

When your organization has the Journey Optimizer B2B Edition product provisioned, Experience Platform includes a set of built-in (default) roles that you can use to manage access to the product capabilities:

| Role | Permissions |
| ---- | ----------- |
| B2B Journey Manager | <li>Manage B2B Journeys <li>Manage B2B Buying Groups <li>Manage B2B Account Lists <li>View B2B Intelligent Dashboard <li>View B2B Insights Dashboard |
| B2B Channel Manager | <li>Manage B2B Assets <li>Manage B2B Templates <li>Manage B2B Fragments |
| B2B System Administrator | <li>Manage B2B Channels Configurations <li>Manage B2B Admin Configurations |
| B2B Sales User | <li>View Intelligent Dashboard |

### Edit role permissions

For built-in or custom roles, you can decide at any time to add or delete permissions. If you modify a default or custom role, it impacts every user assigned to the role.

In the following example, you want to add permissions related to the B2B Journeys resource for users assigned to the B2B Channel Manager role. This change enables users for that role to manage account journeys also.

>[!NOTE]
>
>An Admin Console system administrator can perform these steps.

_To change the permissions for a role:_

1. Go to [experience.adobe.com](https://experience.adobe.com/).

1. In the _[!UICONTROL Quick access]_ panel, select **[!UICONTROL Permissions]**.

   >[!NOTE]
   >
   >If you don't see _[!UICONTROL Permissions]_, you may need to click **[!UICONTROL View all]** and select it from the available applications.

   ![Experience Platform - access Permissions](./assets/aep-permissions.png){width="700" zoomable="yes"}

1. Select **[!UICONTROL Roles]** in the left navigation.

1. Click the **_B2B Channel Manager_** role name.

1. In the details page, click **[!UICONTROL Edit]** at the top right.

   ![Experience Platform - edit the role](./assets/aep-permissions-role-edit.png){width="700" zoomable="yes"}

   In the role editor, the _[!UICONTROL Resources]_ menu displays the list of resources that apply to the Experience Cloud - Platform powered applications products.

   You can enter _B2B_ in the search tool to filter the list for the B2B product permissions. 
   
1. Click the _Add_ icon (**+**) for the B2B Journeys resource.

   ![Experience Platform - edit the role](./assets/aep-permissions-role-edit-b2b-journeys-add.png){width="700" zoomable="yes"}

1. In the _[!UICONTROL B2B Journeys]_ permissions card, select **[!UICONTROL Manage B2B Account Journeys]**.

1. Click **[!UICONTROL Save]**.

   ![Experience Platform - edit the role](./assets/aep-permissions-role-edit-b2b-journeys-done.png){width="700" zoomable="yes"}

1. Click **[!UICONTROL Close]** to return to the details page. -->

### Aggiungere utenti a un ruolo

>[!NOTE]
>
>Un amministratore di Admin Console può eseguire questi passaggi.

1. Apri i dettagli del ruolo e seleziona la scheda **[!UICONTROL Utenti]**.

   Questa scheda visualizza un elenco di tutti gli utenti assegnati al ruolo.

1. Fare clic su **[!UICONTROL Aggiungi utenti]**.

   ![Experience Platform - aggiungi utenti al ruolo](./assets/aep-permissions-role-add-users.png){width="700" zoomable="yes"}

1. Nella finestra di dialogo _[!UICONTROL Aggiungi utenti]_, individua e seleziona gli utenti che desideri aggiungere al ruolo.

   * Puoi usare lo strumento di ricerca per filtrare l’elenco degli utenti.

   * Selezionare la casella di controllo per ogni utente.

   ![Experience Platform - Finestra di dialogo Aggiungi utenti](./assets/aep-permissions-role-add-users-dialog.png){width="600" zoomable="yes"}

1. Dopo aver selezionato tutti gli utenti che desideri aggiungere, fai clic su **[!UICONTROL Salva]**.

### Aggiungere gruppi di utenti a un ruolo

>[!NOTE]
>
>Un amministratore di Admin Console può eseguire questi passaggi.

Per informazioni sulla gestione degli utenti, vedi [utenti Admin Console](https://helpx.adobe.com/it/enterprise/using/user-groups.html) nella documentazione di Admin Console.

1. Apri i dettagli del ruolo e seleziona la scheda **[!UICONTROL Gruppi di utenti]**.

   Questa scheda visualizza un elenco di tutti i gruppi di utenti assegnati al ruolo.

1. Fare clic su **[!UICONTROL Aggiungi gruppi]**.

   ![Experience Platform - aggiungi utenti al ruolo](./assets/aep-permissions-role-add-groups.png){width="700" zoomable="yes"}

1. Nella finestra di dialogo _[!UICONTROL Aggiungi gruppi]_, individua e seleziona i gruppi da aggiungere al ruolo.

   * Puoi usare lo strumento di ricerca per filtrare l’elenco dei gruppi di utenti.

   * Seleziona la casella di controllo per ogni gruppo di utenti.

   ![Experience Platform - Finestra di dialogo Aggiungi gruppi](./assets/aep-permissions-role-add-groups-dialog.png){width="600" zoomable="yes"}

1. Dopo aver selezionato tutti gli utenti che desideri aggiungere, fai clic su **[!UICONTROL Salva]**.

## Creare un ruolo personalizzato

>[!NOTE]
>
>Un amministratore di Admin Console può eseguire questi passaggi.

1. Seleziona **[!UICONTROL Ruoli]** nell&#39;area di navigazione a sinistra e seleziona **[!UICONTROL Crea ruolo]**.

1. Nella finestra di dialogo _[!UICONTROL Crea nuovo ruolo]_, immetti un nome per il ruolo, ad esempio _B2B Marketers_, e una descrizione (facoltativa).

1. Fai clic su **[!UICONTROL Conferma]**.

1. Seleziona le sandbox.

   ![Experience Platform - aggiungi sandbox per il nuovo ruolo](./assets/aep-permissions-role-sandboxes.png){width="700" zoomable="yes"}

1. Aggiungi le autorizzazioni profilo:

   * Nell&#39;elenco _[!UICONTROL Risorse]_ a sinistra, individuare l&#39;elemento **[!UICONTROL Gestione profili]** e fare clic sull&#39;icona _Aggiungi_ (**+**) per aggiungere l&#39;attributo.

   * Per l’attributo, aggiungi le seguenti autorizzazioni:
      * [!UICONTROL Visualizza segmenti]
      * [!UICONTROL Gestisci segmenti]
      * [!UICONTROL Visualizza profili]
      * [!UICONTROL Gestisci profili]
      * [!UICONTROL Visualizza profilo B2B]
      * [!UICONTROL Gestisci profilo B2B]

   ![Experience Platform - aggiungi profili per il nuovo ruolo](./assets/aep-permissions-role-profiles.png){width="700" zoomable="yes"}

1. Aggiungere autorizzazioni prodotto B2B:

   Consulta l&#39;elenco delle [autorizzazioni prodotto B2B](#b2b-product-permissions) per determinare quali funzionalità prodotto desideri per il ruolo.

   Nell&#39;elenco _[!UICONTROL Risorse]_ a sinistra, individuare gli elementi **[!UICONTROL B2B]** e fare clic sull&#39;icona _Aggiungi_ (**+**) per aggiungere ogni attributo che si desidera abilitare per il ruolo.

   È possibile immettere _B2B_ nello strumento di ricerca per filtrare l&#39;elenco delle autorizzazioni per il prodotto B2B.

1. Fai clic su **[!UICONTROL Salva]** in alto a destra.

1. Vai ai dettagli del ruolo e seleziona la scheda **[!UICONTROL Gruppi di utenti]**.

1. Fare clic su **[!UICONTROL Aggiungi gruppi]**.

   ![Experience Platform - aggiungi profili per il nuovo ruolo](./assets/aep-permissions-role-add-groups.png){width="700" zoomable="yes"}

1. Seleziona la casella di controllo accanto al gruppo di utenti creato in precedenza nell’Admin Console.

1. Fai clic su **[!UICONTROL Salva]**.
