---
title: Introduzione alla versione B2B di Journey Optimizer
description: In qualità di nuovo utente in Journey Optimizer B2B Edition, scopri le aree chiave per iniziare.
exl-id: 83f8e666-0b31-4323-9902-4fdf4446424c
source-git-commit: 7103e4f6666482a72511661dfaed1392d4eb16b1
workflow-type: tm+mt
source-wordcount: '623'
ht-degree: 8%

---

# Introduzione alla versione B2B di Journey Optimizer

Le funzioni e gli strumenti che desideri utilizzare in Adobe Journey Optimizer B2B Edition dipendono dal tuo ruolo all’interno del team.

In base all’organizzazione, gli amministratori possono definire diversi tipi di utenti e concedere loro l’accesso a determinate funzionalità a seconda delle loro autorizzazioni.

>[!BEGINTABS]

>[!TAB Avvio rapido amministratore]

Prima che il team possa iniziare a utilizzare le funzionalità di Adobe Journey Optimizer B2B Edition, sono necessari diversi passaggi per preparare l’ambiente. Esegui questi passaggi in modo che l’ingegnere dati e l’addetto al marketing possano iniziare a lavorare con Adobe Journey Optimizer B2B Edition.

In qualità di amministratore di sistema, devi comprendere i profili di prodotto e assegnare le autorizzazioni per l’amministrazione della sandbox e la configurazione dei canali. È inoltre necessario configurare le sandbox e gestirle per i profili di prodotto disponibili. Puoi quindi assegnare i membri del gruppo ai profili di prodotto. Queste funzionalità possono essere gestite dagli amministratori di prodotto che hanno accesso a Adobe Admin Console. [Ulteriori informazioni su Adobe Admin Console](https://helpx.adobe.com/it/enterprise/using/admin-console.html).

Per ulteriori informazioni sulla gestione degli accessi, consulta le pagine seguenti:

1. **Creare sandbox** per suddividere le istanze in ambienti virtuali separati e isolati. [Ulteriori informazioni](https://experienceleague.adobe.com/en/docs/experience-platform/sandbox/home#understanding-sandboxes)

1. **Configura il profilo di prodotto**. Un profilo di prodotto è un insieme di diritti unitari in Adobe Experience Platform che consentono agli utenti di accedere a determinate funzionalità o oggetti nell’interfaccia. [Ulteriori informazioni](../admin/user-management.md#create-the-marketo-engage-product-profile)

1. **Configura le autorizzazioni utente** per i profili di prodotto, incluse le sandbox, e concedi l&#39;accesso ai membri del gruppo assegnandoli a profili di prodotto diversi. Questa attività viene eseguita nell’Admin Console. [Ulteriori informazioni](../admin/user-management.md#create-a-user-group)

1. **Configura la consegna e-mail** in Marketo Engage, che consente al team di inviare contenuti e-mail dai percorsi di account. [Ulteriori informazioni](https://experienceleague.adobe.com/en/docs/marketo/using/getting-started/initial-setup/setup-steps#ensure-email-deliverability)

1. **Configurare i servizi SMS**. Imposta uno dei provider SMS di terze parti supportati che offre servizi di messaggistica di testo in modo indipendente e configura le credenziali dell’account in Adobe Journey Optimizer B2B Edition. [Ulteriori informazioni](../content/sms-authoring.md#create-a-new-api-credentials-for-an-sms-service-provider)

1. **Configura e abilita l&#39;utilizzo di Adobe Experience Manager Assets** per i team che utilizzano Assets come Cloud Service C per la gestione centralizzata delle risorse digitali. [Ulteriori informazioni](../admin/configure-aem-repositories.md)

>[!TAB Guida introduttiva per gli addetti al marketing]

In qualità di addetto al marketing o di _professionista del Percorso dell&#39;account_, sei responsabile della progettazione di percorsi e della creazione di contenuti. È possibile iniziare a utilizzare Adobe Journey Optimizer B2B Edition dopo che l’amministratore di sistema e il data engineer hanno preparato l’ambiente e concesso l’accesso.

Per configurare il primo percorso, aggiungere risorse e inviare contenuti, consulta le sezioni seguenti:

1. **Aggiungi tipi di pubblico dell&#39;account**. La versione B2B di Journey Optimizer consente di creare tipi di pubblico per l’account tramite definizioni di segmenti direttamente dall’applicazione e di sfruttarli nei percorsi dell’account. [Ulteriori informazioni](../audiences/account-audience-overview.md)

1. **Crea gruppi di acquisto**. Definisci i componenti chiave per il raggiungimento degli obiettivi e degli obiettivi aziendali e crea gruppi di acquisto che identifichino i membri per gli elenchi di account target. [Ulteriori informazioni](../buying-groups/buying-groups-overview.md)

1. **Creare e gestire le risorse**. Adobe Experience Manager Assets fornisce un archivio di risorse unico e centralizzato da utilizzare per compilare i messaggi. [Ulteriori informazioni](../content/assets-overview.md)

1. **Aggiungi modelli e-mail personalizzati e dinamici**. Sfrutta le funzionalità di personalizzazione e di contenuti dinamici della Journey Optimizer B2B Edition per adattare il messaggio al tuo pubblico. [Ulteriori informazioni](../content/email-templates.md)

1. **Progetta percorsi di account per offrire esperienze personalizzate e contestuali**. Journey Optimizer B2B Edition consente di creare casi di utilizzo di orchestrazione in tempo reale con dati contestuali archiviati in eventi o origini dati. Progetta scenari avanzati e in più passaggi basati sulle seguenti funzionalità:

   * Invia in tempo reale una consegna unitaria attivata quando viene ricevuto un evento, oppure in batch utilizzando il pubblico di Adobe Experience Platform.

   * Utilizza dati contestuali da eventi, informazioni da Adobe Experience Platform o dati da servizi API di terze parti.

   * Utilizza le azioni del canale integrate (e-mail e SMS) per inviare messaggi progettati in Journey Optimizer B2B Edition.

   * Nella finestra di progettazione del percorso, genera i casi d’uso in più passaggi, aggiungi condizioni e invia messaggi personalizzati.

[Ulteriori informazioni](../journeys/journey-overview.md)

>[!ENDTABS]
