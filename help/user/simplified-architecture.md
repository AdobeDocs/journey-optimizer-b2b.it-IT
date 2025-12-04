---
title: Configurazione semplificata dell'architettura
description: Configurare Journey Optimizer B2B edition con l'architettura semplificata. Configura schemi XDM, canali e-mail/SMS, azioni del percorso Marketo Engage e utenti.
feature: Setup, Administration
role: Admin, Data Engineer
hide: true
hidefromtoc: true
source-git-commit: d2f33c30dba1ce44842f41bd2dbbfada24a8ff9c
workflow-type: tm+mt
source-wordcount: '1363'
ht-degree: 6%

---

# Configurazione semplificata dell&#39;architettura

Adobe Journey Optimizer B2B Edition è ora disponibile utilizzando un’architettura semplificata. Grazie a questa architettura aggiornata, Journey Optimizer B2B Edition e Marketo Engage non si trovano più nello stesso sistema e nello stesso archivio di dati. Journey Optimizer B2B Edition riceve i dati solo da Adobe Experience Platform. Tuttavia, continua a fare affidamento su diritti di Marketo Engage e su alcune funzioni di configurazione per il provisioning e la configurazione del sistema.

L’architettura semplificata è la base per lo sviluppo di nuove funzionalità in Adobe Journey Optimizer B2B edition:

* **Unifica e ridimensiona facilmente i dati:** La nuova piattaforma supporta modelli di dati complessi, inclusi oggetti personalizzati, gruppi di acquisto ed eventi account. 

* **Connetti più istanze di Adobe Marketo Engage:** Gestisci e unifica i dati da più ambienti Adobe Marketo Engage in un&#39;unica posizione.

* **Protegge i tuoi dati:** Funzioni avanzate di privacy e sicurezza che aiutano a proteggere le informazioni dei tuoi clienti. (_In arrivo_)

* **Creato per il futuro:** Questo aggiornamento consente di apportare miglioramenti e innovazioni continui. 

Per gli ambienti per i quali è stato eseguito il provisioning per questa architettura, utilizza le seguenti linee guida per la configurazione.

## Spazi dei nomi e schemi

Per una panoramica, consulta [Spazi dei nomi B2B e schemi](https://experienceleague.adobe.com/en/docs/experience-platform/sources/connectors/adobe-applications/marketo/marketo-namespaces) nella documentazione di Experience Platform.

### Configurazione dell’ambiente

Imposta un ambiente Postman per supportare lo spazio dei nomi B2B e l’utility di generazione automatica dello schema.

* È possibile scaricare la raccolta di utilità di generazione automatica dello spazio dei nomi e dello schema e l&#39;ambiente dall&#39;[archivio GitHub](https://github.com/adobe/experience-platform-postman-samples/tree/master/Postman%20Collections/CDP%20Namespaces%20and%20Schemas%20Utility).

* Per informazioni sull&#39;utilizzo delle API di Experience Platform, inclusi i dettagli su come raccogliere i valori per le intestazioni richieste e leggere chiamate API di esempio, consulta la [guida introduttiva alle API di Experience Platform](https://experienceleague.adobe.com/it/docs/experience-platform/landing/platform-apis/api-guide).

* Per informazioni su come generare le credenziali per le API Experience Platform, consulta l&#39;esercitazione su [autenticazione e accesso alle API Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/landing/platform-apis/api-authentication).

* Per informazioni sulla configurazione di Postman per le API di Experience Platform, consulta i passaggi dettagliati in [Postman in Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/landing/platform-apis/postman).

Con una console per sviluppatori di Experience Platform e la configurazione di Postman, ora puoi iniziare ad applicare i valori di ambiente appropriati all’ambiente Postman.

### Eseguire gli script

Con la tua raccolta Postman e la configurazione dell&#39;ambiente, puoi eseguire lo script tramite l&#39;interfaccia Postman.

Nell&#39;interfaccia di Postman, selezionare la cartella principale dell&#39;utilità di generazione automatica, quindi selezionare **Esegui** dall&#39;intestazione superiore.

Quando viene visualizzata l&#39;interfaccia di Runner, assicurarsi che tutte le caselle di controllo siano selezionate, quindi selezionare **Esegui utilità di generazione automatica spazi dei nomi e schemi**.

In caso di esito positivo, la richiesta crea gli spazi dei nomi e gli schemi necessari per B2B.

## Selezione campo XDM

Puoi gestire i campi XDM disponibili in tutta l’applicazione nell’interfaccia utente di Journey Optimizer B2B edition. Questi campi consentono di semplificare l&#39;istanza esponendo solo i campi rilevanti per la creazione di **_percorsi_**, **_gruppi di acquisto_** o **_personalizzazioni e-mail_**.

### Classi XDM

#### Classi standard

Utilizza i passaggi seguenti per definire i campi per le classi XDM standard:

1. Passa a **[!UICONTROL Amministrazione] > [!UICONTROL Configurazioni]**.

1. Nel pannello di navigazione, seleziona **[!UICONTROL Classi XDM]**.

1. Seleziona la scheda **[!UICONTROL Standard]** per visualizzare le classi XDM disponibili:

   * Profilo individuale XDM

   * Account aziendale XDM

#### Campi gestiti

Definisci quali campi sono disponibili in tutta l’applicazione.

1. Fai clic sull&#39;icona _Altro menu_ (**...**) e seleziona **[!UICONTROL Modifica campi gestiti]**.

1. Rivedi l&#39;elenco dei campi disponibili (fai clic sull&#39;icona _Informazioni_ per i metadati del campo).

1. Selezionare i campi da includere e deselezionare le selezioni per i campi non necessari.

1. Utilizza il cursore **[!UICONTROL Mostra solo campi selezionati]** per rivedere le tue selezioni.

1. Fai clic su **[!UICONTROL Salva]**.

#### Campi aggiornabili

Scegli quali campi possono essere modificati tramite **[!UICONTROL Aggiorna profilo account]** o **[!UICONTROL Aggiorna profilo persona]** azioni di percorso.

1. Fai clic sull&#39;icona _Altro menu_ (**...**) e seleziona **[!UICONTROL Modifica campi aggiornabili]**.

1. Selezionare **[!UICONTROL Schema]** e quindi **[!UICONTROL Set di dati]**.

   Questi schemi e set di dati vengono forniti dalla tua organizzazione.

1. Rivedi l&#39;elenco dei campi aggiornabili (fai clic sull&#39;icona _Informazioni_ per i metadati).

   È possibile modificare solo i campi gestiti.

1. Selezionare i campi che si desidera rendere disponibili per l&#39;aggiornamento dai percorsi.

1. Fai clic su **Salva**

### Schemi relazionali

Seleziona [schemi relazionali](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/schema/relational) da utilizzare in **_decisioning di percorso_** e **_personalization_**. Attualmente, questi schemi sono destinati a casi di utilizzo con oggetti personalizzati. In futuro, gli schemi relazionali possono essere utilizzati anche per altri casi di utilizzo di oggetti.

1. Selezionare la scheda **[!UICONTROL Relazionale]**.

1. Fare clic su **[!UICONTROL Seleziona classe XDM relazionale]**.

   Attualmente, è supportato solo l’oggetto personalizzato account many-to-one.

1. Rivedi l&#39;elenco dei campi dello schema (fai clic sull&#39;icona _informazioni_ per visualizzare i metadati).

1. Selezionare i campi che si desidera includere.

1. Utilizza il cursore **[!UICONTROL Mostra solo campi selezionati]** per rivedere le tue selezioni.

1. Fai clic su **[!UICONTROL Salva]**.

>[!NOTE]
>
>Tieni presente che gli schemi relazionali devono avere le seguenti configurazioni:
>
><li>Comportamento: record
&gt; <li>Segmentazione: abilitata
&gt; <li>Tipo di relazione: molti-a-uno
&gt; <li>Schema di riferimento: <a href="https://experienceleague.adobe.com/it/docs/platform-learn/tutorials/schemas/create-schemas-for-b2b-data">Account B2B - Schema account aziendale XDM</a>
&gt; <li>Campi obbligatori: chiave primaria, chiave esterna e descrittore versione
&gt; <li>Set di dati associato: definito e mappato allo schema

### Eventi

Seleziona gli eventi esperienza da utilizzare in **_decisioning percorso_**.

1. Selezionare la scheda **[!UICONTROL Eventi]**.

1. Fai clic su **[!UICONTROL Seleziona evento esperienza]**.

1. Fai clic su **[!UICONTROL Seleziona tipo di evento]**, scegli il tipo di evento, fai clic su **[!UICONTROL Seleziona]**.

1. Fai clic su **[!UICONTROL Seleziona campi]**, scegli i campi necessari, quindi fai clic su **[!UICONTROL Seleziona]**.

1. Fai clic su **[!UICONTROL Salva]**.

## Configurazione e-mail

Per inviare e-mail da Journey Optimizer B2B edition, è necessario configurare quanto segue.  

[https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/get-started/email-protocols](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/get-started/email-protocols)

### Protocolli per il tracciamento e la consegna e-mail

1. [Crea record DNS per posta elettronica](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/get-started/email-protocols#create-dns-records-for-landing-pages-and-email)

1. [Configura SPF e DKIM](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/get-started/email-protocols#set-up-spf-and-dkim)

1. [Configura DMARC](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/get-started/email-protocols#set-up-dmarc)

1. [Configura record MX per il dominio](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/get-started/email-protocols#set-up-mx-records-for-your-domain)

1. [Aggiungere indirizzi IP in uscita ai inserisce nell&#39;elenco Consentiti di](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/get-started/email-protocols#outbound-ip-addresses)

1. Se devi condividere il pool IP dedicato, rivolgiti al team di recapito messaggi sulla fattibilità e sulla configurazione assistita.

### Configurazioni del canale e-mail

Nell’architettura semplificata, le impostazioni e-mail vengono configurate dall’applicazione Marketo Engage. Completa i passaggi di configurazione relativi all’e-mail:

* [https://experienceleague.adobe.com/en/docs/marketo/using/getting-started/initial-setup/setup-steps](https://experienceleague.adobe.com/en/docs/marketo/using/getting-started/initial-setup/setup-steps)

* [https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/admin/channels/configure-channels-emails](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/admin/channels/configure-channels-emails)

### Limiti di comunicazione

1. Nel menu di navigazione a sinistra, scegli **[!UICONTROL Amministrazione]** > **[!UICONTROL Canali]**.

1. Nel pannello di navigazione, seleziona **[!UICONTROL Limite di comunicazione]**.

1. Creare un set di regole del limite di comunicazione globale (questo set di regole viene creato per impostazione predefinita in ogni istanza di Journey Optimizer B2B edition).

   Se non viene creato il set di regole globale, non vi è alcun limite di comunicazione.

<!-- In the future, you can also add local communication limit rule sets (AJO B2C doc can be found here [https://experienceleague.adobe.com/en/docs/journey-optimizer/using/conflict-prioritization/capping-rules/rule-sets](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/conflict-prioritization/capping-rules/rule-sets). We may need a small update for our B2B version.) -->

### Limiti di comunicazione condivisa

Per impostazione predefinita, Journey Optimizer B2B edition e Marketo Engage dispongono di limiti di comunicazione indipendenti all’interno della nuova architettura.

Se desideri che l’istanza Marketo Engage condivida il limite di comunicazione impostato nell’istanza Journey Optimizer B2B edition, contatta il supporto Adobe per assistenza nella configurazione o apri un ticket di supporto. Su richiesta, il team di progettazione può abilitare la condivisione dei limiti di comunicazione tra Journey Optimizer B2B edition e una o più istanze di Marketo Engage.

Quando i limiti di comunicazione condivisa sono abilitati, puoi definire le regole in Journey Optimizer B2B edition ed estendere la condivisione di tali limiti ai codici Munchkin di Marketo. Per ulteriori informazioni, vedere [Limiti di comunicazione](./admin/configure-channels-emails.md#communication-limits)

<!-- internal info only 

Currently, the shared communication limit in the Marketo Engage instance must be set up through an API call.

For example, when:

* The munchkinId of the Journey Optimizer B2B Edition instance is `JKL-567-MNO`.
* The munchkinId of the Marketo Engage instance is `ABC-123-DEF` and it is in the SJ datacenter

The API request should look similar to the following:

```
curl --location --request POST 'http://sjrest2a.marketo.org/rest/v1/fm.json?_munchkinId=ABC-123-DEF&featureName=Mktmail%20Config&paramName=ajoB2bMappingMunchkinId&dataType=string&value=JKL-567-MNO'
```
-->

## Configurazione del canale SMS

Per informazioni dettagliate, consulta [_Configurazioni SMS_](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/admin/channels/configure-channels-sms).

## Azioni Marketo Engage da percorsi

È possibile configurare una o più istanze **_Marketo Engage_** remote da utilizzare con le azioni di percorso seguenti:

* Aggiungi a elenco Marketo
* Rimuovi dall’elenco Marketo
* Aggiungi alla campagna di richiesta Marketo

Completa i seguenti passaggi per configurare queste connessioni:

1. Passa a **[!UICONTROL Amministrazione] > [!UICONTROL Configurazioni]**.

1. Nel pannello di navigazione, seleziona **[!UICONTROL Classi XDM]**.

1. Seleziona la scheda **[!UICONTROL Integrazioni]**.

1. Fare clic su **[!UICONTROL Crea connessione]**.

1. Immetti **[!UICONTROL Nome]** e **[!UICONTROL Descrizione]**.

1. Selezionare **[!UICONTROL Aggiorna criterio]** per i record persona corrispondenti.

1. Immetti **[!UICONTROL Munchkin ID]**, **[!UICONTROL ID client]**, **[!UICONTROL Segreto client]** e fai clic su **[!UICONTROL Connetti a Marketo]**.

1. Fai clic su **[!UICONTROL Crea]**.

## Onboarding degli utenti

Consulta la pagina [Gestione utente](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/admin/user-management) per una panoramica.

### Gruppi di utenti esistenti

Se tutti gli utenti Journey Optimizer B2B edition esistenti hanno bisogno di accedere alla nuova architettura, utilizzare il gruppo di utenti Journey Optimizer B2B edition esistente. L’amministratore di sistema o l’amministratore di prodotto può eseguire i seguenti passaggi.

1. Crea un profilo di prodotto nel Marketo Engage dedicato.

1. Aggiungi un gruppo di utenti esistente al profilo di prodotto creato.

I profili concedono tutti i ruoli e le autorizzazioni già assegnati a quel gruppo di utenti, che devono già essere configurati affinché gli utenti possano accedere a Journey Optimizer B2B edition. Se solo un sottoinsieme di utenti deve accedere alla nuova architettura, completa i passaggi descritti di seguito. Ulteriori dettagli nella [documentazione corrente](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/admin/user-management).

### Crea un nuovo gruppo di utenti

1. Crea un profilo di prodotto nell’istanza dedicata di Marketo Engage.
1. Crea un gruppo di utenti per i nuovi utenti.
1. Seleziona e assegna i profili di prodotto richiesti al gruppo di utenti:

   * Profilo Marketo Engage creato
   * Profili Adobe Experience Platform
      * AEP-Default-All-Users
      * Raccolta dati di Adobe Experience Platform
      * Accesso a tutti i tipi di raccolta dati

1. Aggiungi gli utenti al gruppo di utenti.
1. Aggiungi un nuovo gruppo di utenti ai ruoli B2B edition di Journey Optimizer in Experience Platform.
