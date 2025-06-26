---
title: Linee guida sull’onboarding per amministratori e addetti al marketing
description: In qualità di nuovo amministratore o utente di Journey Optimizer B2B edition, scopri le aree chiave del processo di onboarding.
role: Admin, User
level: Beginner
exl-id: 83f8e666-0b31-4323-9902-4fdf4446424c
source-git-commit: d0bd2d5153b972df92ff42c6f1eebb25448b222f
workflow-type: tm+mt
source-wordcount: '685'
ht-degree: 84%

---

# Linee guida per l’onboarding

Le funzioni e gli strumenti che desideri utilizzare in Adobe Journey Optimizer B2B edition dipendono dal tuo ruolo all’interno del team. In base all’organizzazione, gli amministratori possono definire diversi tipi di utente e concedere loro l’accesso a determinate funzionalità in base alle autorizzazioni.

>[!TIP]
>
>Verifica anche i diritti delle licenze e la corrispondente [descrizione del prodotto](https://helpx.adobe.com/it/legal/product-descriptions/adobe-journey-optimizer-b2b.html){target="_blank"} sui guardrail delle prestazioni e le limitazioni statiche.

>[!BEGINTABS]

>[!TAB Amministratore]

Prima che il team possa iniziare a utilizzare le funzionalità di Adobe Journey Optimizer B2B Edition, sono necessari diversi passaggi per preparare l’ambiente. Esegui questi passaggi in modo che il tecnico dati e il marketer possano iniziare a utilizzare Adobe Journey Optimizer B2B Edition.

In qualità di Amministratore di sistema, devi comprendere i profili di prodotto e assegnare le autorizzazioni per l’amministrazione della sandbox e la configurazione dei canali. Devi anche configurare le sandbox e gestirle per i profili di prodotto disponibili. Potrai quindi assegnare membri del gruppo ai profili di prodotto. Gli amministratori di prodotto che hanno accesso a Adobe Admin Console possono gestire queste funzionalità. [Ulteriori informazioni su Adobe Admin Console](https://helpx.adobe.com/it/enterprise/using/admin-console.html).

Per ulteriori informazioni sulla gestione degli accessi, consulta le pagine seguenti:

1. **Creare sandbox** per suddividere le istanze in ambienti virtuali separati e isolati. [Ulteriori informazioni](https://experienceleague.adobe.com/it/docs/experience-platform/sandbox/home#understanding-sandboxes){target="_blank"}

1. **Rivolgiti al tuo data engineer** per pianificare e implementare l&#39;attivazione dei profili e del pubblico B2B. Esamina i progetti pubblicati e segui le linee guida in base alle tue esigenze. [Ulteriori informazioni](https://experienceleague.adobe.com/en/docs/blueprints-learn/architecture/b2b-activation/overview){target="_blank"}

1. **Impostare il profilo di prodotto**. Un profilo di prodotto è un set di diritti unitari in Adobe Experience Platform che consente agli utenti di accedere a determinate funzionalità o oggetti nell’interfaccia. [Ulteriori informazioni](../admin/user-management.md#create-the-marketo-engage-product-profile)

1. **Imposta le autorizzazioni utente** per i profili di prodotto, tra cui le sandbox, e concedi l’accesso ai membri del tuo gruppo assegnandoli a profili di prodotto diversi. Questa attività viene eseguita in Admin Console. [Ulteriori informazioni](../admin/user-management.md#create-a-user-group)

1. **Configura la consegna e-mail** in Marketo Engage, in modo da consentire al gruppo di inviare contenuto e-mail dai percorsi account. [Ulteriori informazioni](https://experienceleague.adobe.com/it/docs/marketo/using/getting-started/initial-setup/setup-steps#ensure-email-deliverability){target="_blank"}

1. **Configurare i servizi SMS**. Imposta uno dei provider di SMS terze parti supportati che offre servizi di SMS in modo indipendente e configura le credenziali dell’account in Adobe Journey Optimizer B2B Edition. [Ulteriori informazioni](../admin/configure-channels-sms.md)

1. **Configura e abilita l’utilizzo di Adobe Experience Manager Assets** per i gruppi che utilizzano Assets as a Cloud Service per la gestione centralizzata delle risorse digitali. [Ulteriori informazioni](../admin/configure-aem-repositories.md)

1. **Imposta le definizioni degli eventi esperienza di Adobe Experience Platform (AEP)** per i gruppi responsabili della creazione di percorsi account che ascoltano gli eventi esperienza AEP. [Ulteriori informazioni](../admin/configure-aep-events.md)

>[!TAB Addetto marketing]

In qualità di marketer, o di _professionista del percorso dell’account_, sei responsabile della progettazione di percorsi e della creazione di contenuti. Puoi iniziare a utilizzare Adobe Journey Optimizer B2B Edition dopo che l’amministratore di sistema e il tecnico dati hanno preparato l’ambiente e ti hanno concesso l’accesso.

Per impostare il primo percorso, aggiungere risorse e inviare contenuti, consulta le sezioni seguenti:

1. **Aggiungere pubblico all’account**. In Journey Optimizer B2B Edition puoi creare tipi di pubblico dell’account tramite le definizioni di segmento direttamente dall’applicazione e quindi utilizzarli nei percorsi account. [Ulteriori informazioni](../audiences/account-audience-overview.md)

1. **Creare gruppi acquisti**. Definisci i componenti chiave per raggiungere gli obiettivi e le finalità aziendali e crea gruppi acquisti che identificano i membri degli elenchi di account target. [Ulteriori informazioni](../buying-groups/buying-groups-overview.md)

1. **Creare e gestire le risorse**. Adobe Experience Manager Assets fornisce un archivio unico e centralizzato di risorse che puoi utilizzare per compilare i messaggi. [Ulteriori informazioni](../content/assets-overview.md)

1. **Aggiungere modelli e-mail personalizzati e dinamici**. Sfrutta le funzionalità di personalizzazione e per contenuti dinamici di Journey Optimizer B2B Edition per adattare il messaggio al tuo pubblico. [Ulteriori informazioni](../content/email-templates.md)

1. **Progetta i percorsi account per offrire esperienze personalizzate e contestuali**. Journey Optimizer B2B Edition consente di creare casi d’uso di orchestrazione in tempo reale sfruttando i dati contestuali archiviati negli eventi o nelle origini dati. Progetta scenari avanzati a più passaggi basati sulle seguenti funzionalità:

   * Invia una consegna unitaria in tempo reale attivata quando viene ricevuto un evento, oppure in batch, utilizzando i tipi di pubblico di Adobe Experience Platform.

   * Usa i dati contestuali da eventi, le informazioni da Adobe Experience Platform o i dati da servizi API di terze parti.

   * Utilizza le azioni del canale integrate (e-mail e SMS) per inviare messaggi progettati in Journey Optimizer B2B edition.

   * Nella mappa del percorso, genera i tuoi casi d’uso in più passaggi, aggiungi condizioni e invia messaggi personalizzati.

[Ulteriori informazioni](../journeys/journey-overview.md)

>[!ENDTABS]
