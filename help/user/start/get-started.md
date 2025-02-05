---
title: Introduzione a Journey Optimizer B2B edition
description: In qualità di nuovo utente in Journey Optimizer B2B Edition, scopri le aree chiave per iniziare.
exl-id: 83f8e666-0b31-4323-9902-4fdf4446424c
source-git-commit: b403ff764c002796953956379e33fec6eb8c0611
workflow-type: tm+mt
source-wordcount: '664'
ht-degree: 10%

---

# Introduzione a Journey Optimizer B2B edition

Le funzioni e gli strumenti che desideri utilizzare in Adobe Journey Optimizer B2B edition dipendono dal tuo ruolo all’interno del team.

In base all’organizzazione, gli amministratori possono definire diversi tipi di utenti e concedere loro l’accesso a determinate funzionalità a seconda delle loro autorizzazioni.

>[!TIP]
>
>Controlla anche i diritti delle licenze e la corrispondente [descrizione del prodotto](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer-b2b.html){target="_blank"} sui guardrail delle prestazioni e le limitazioni statiche.

>[!BEGINTABS]

>[!TAB Avvio rapido amministratore]

Prima che il team possa iniziare a utilizzare le funzioni di Adobe Journey Optimizer B2B edition, sono necessari diversi passaggi per preparare l’ambiente. Esegui questi passaggi in modo che l’ingegnere dati e l’addetto al marketing possano iniziare a lavorare con Adobe Journey Optimizer B2B edition.

In qualità di amministratore di sistema, devi comprendere i profili di prodotto e assegnare le autorizzazioni per l’amministrazione della sandbox e la configurazione dei canali. È inoltre necessario configurare le sandbox e gestirle per i profili di prodotto disponibili. Puoi quindi assegnare i membri del gruppo ai profili di prodotto. Queste funzionalità possono essere gestite dagli amministratori di prodotto che hanno accesso a Adobe Admin Console. [Ulteriori informazioni su Adobe Admin Console](https://helpx.adobe.com/it/enterprise/using/admin-console.html).

Per ulteriori informazioni sulla gestione degli accessi, consulta le pagine seguenti:

1. **Creare sandbox** per suddividere le istanze in ambienti virtuali separati e isolati. [Ulteriori informazioni](https://experienceleague.adobe.com/en/docs/experience-platform/sandbox/home#understanding-sandboxes)

1. **Configura il profilo di prodotto**. Un profilo di prodotto è un insieme di diritti unitari in Adobe Experience Platform che consentono agli utenti di accedere a determinate funzionalità o oggetti nell’interfaccia. [Ulteriori informazioni](../admin/user-management.md#create-the-marketo-engage-product-profile)

1. **Configura le autorizzazioni utente** per i profili di prodotto, incluse le sandbox, e concedi l&#39;accesso ai membri del gruppo assegnandoli a profili di prodotto diversi. Questa attività viene eseguita nell’Admin Console. [Ulteriori informazioni](../admin/user-management.md#create-a-user-group)

1. **Configura la consegna e-mail** in Marketo Engage, che consente al team di inviare contenuti e-mail dai percorsi di account. [Ulteriori informazioni](https://experienceleague.adobe.com/en/docs/marketo/using/getting-started/initial-setup/setup-steps#ensure-email-deliverability)

1. **Configurare i servizi SMS**. Imposta uno dei provider SMS di terze parti supportati che offre servizi di messaggistica di testo in modo indipendente e configura le credenziali dell’account in Adobe Journey Optimizer B2B edition. [Ulteriori informazioni](../admin/configure-channels-sms.md)

1. **Configura e abilita l&#39;utilizzo di Adobe Experience Manager Assets** per i team che utilizzano Assets as a Cloud Service per la gestione centralizzata delle risorse digitali. [Ulteriori informazioni](../admin/configure-aem-repositories.md)

1. **Configura le definizioni degli eventi di esperienza di Adobe Experience Platform (AEP)** per i team responsabili della creazione di percorsi di account che ascoltano gli eventi di esperienza di AEP. [Ulteriori informazioni](../admin/configure-aep-events.md)

>[!TAB Guida introduttiva per gli addetti al marketing]

In qualità di addetto al marketing o di _professionista del Percorso dell&#39;account_, sei responsabile della progettazione di percorsi e della creazione di contenuti. È possibile iniziare a lavorare con Adobe Journey Optimizer B2B edition dopo che l’amministratore di sistema e il data engineer hanno preparato l’ambiente e concesso l’accesso.

Per configurare il primo percorso, aggiungere risorse e inviare contenuti, consulta le sezioni seguenti:

1. **Aggiungi tipi di pubblico dell&#39;account**. Journey Optimizer B2B edition consente di creare tipi di pubblico per l’account tramite definizioni di segmenti direttamente dall’applicazione e di sfruttarli nei percorsi dell’account. [Ulteriori informazioni](../audiences/account-audience-overview.md)

1. **Crea gruppi di acquisto**. Definisci i componenti chiave per raggiungere gli obiettivi e le finalità aziendali e crea gruppi di acquisto che identifichino i membri per gli elenchi di account di destinazione. [Ulteriori informazioni](../buying-groups/buying-groups-overview.md)

1. **Creare e gestire le risorse**. Adobe Experience Manager Assets fornisce un archivio di risorse unico e centralizzato da utilizzare per compilare i messaggi. [Ulteriori informazioni](../content/assets-overview.md)

1. **Aggiungi modelli e-mail personalizzati e dinamici**. Sfrutta le funzionalità di personalizzazione e contenuti dinamici di Journey Optimizer B2B edition per adattare il messaggio al tuo pubblico. [Ulteriori informazioni](../content/email-templates.md)

1. **Progetta percorsi di account per offrire esperienze personalizzate e contestuali**. Journey Optimizer B2B edition consente di applicare l’orchestrazione in tempo reale per diversi casi d’uso, sfruttando i dati contestuali provenienti da eventi o origini dati. Progetta scenari avanzati e in più passaggi basati sulle seguenti funzionalità:

   * Invia in tempo reale una consegna unitaria attivata quando viene ricevuto un evento, oppure in batch utilizzando il pubblico di Adobe Experience Platform.

   * Utilizza dati contestuali da eventi, informazioni da Adobe Experience Platform o dati da servizi API di terze parti.

   * Utilizza le azioni del canale integrate (e-mail e SMS) per inviare messaggi progettati in Journey Optimizer B2B edition.

   * Nella finestra di progettazione del percorso, genera i casi d’uso in più passaggi, aggiungi condizioni e invia messaggi personalizzati.

[Ulteriori informazioni](../journeys/journey-overview.md)

>[!ENDTABS]
