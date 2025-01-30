---
title: Funzioni di governance
description: Scopri le funzioni di governance attualmente disponibili in Journey Optimizer B2B edition.
exl-id: 2845272b-987c-4a37-adf4-6ee5bfd59fc0
source-git-commit: 3198ba223125c95263d8dcf5ee8cb285a888a26a
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 0%

---

# Funzioni di governance

Journey Optimizer B2B edition è un’app Adobe Experience Platform integrata. Utilizza diversi strumenti e servizi che consentono di controllare i dati raccolti sull’esperienza in conformità con le pratiche aziendali, gli obblighi legali e i processi di sviluppo. Le sezioni seguenti forniscono un riepilogo di ciascuna di queste funzioni di governance.

## Privacy - RGPD

Journey Optimizer B2B edition utilizza le funzioni Marketi Engage di governance RGPD offerte dal servizio Privacy Service e Marketo Privacy Broker.

## Controllo degli accessi basato sul ruolo (RBAC)

Con Journey Optimizer B2B edition e l’accesso a Adobe Admin Console, gli amministratori possono concedere a un utente le autorizzazioni per un tipo di entità (view-segments, manage-segments, manage-percorsi e così via). Questa funzionalità fa parte del framework di autorizzazioni unificate (UPF, Unified Permissions Framework) che consente a tutti i clienti di Adobe Experience Platform di definire e gestire ruoli e autorizzazioni per la propria organizzazione.

## Crittografia dei dati

**_Crittografia per i dati inattivi_** - Tutti i dati degli account e dei profili di persona trasferiti da Adobe Experience Platform a Journey Optimizer B2B edition sono crittografati per mantenere la conformità esistente da Experience Platform. Vengono crittografate anche tutte le entità originarie di Journey Optimizer B2B edition, ad esempio i percorsi e i gruppi di acquisto.

**_Crittografia per i dati in transito_** (su una rete pubblica) - Tutte le API e le entità di Journey Optimizer B2B edition sono crittografate in transito utilizzando TLS 1.2.

## Consenso/rinuncia

Il consenso opt-in/opt-out è una forma di governance in cui un profilo può rinunciare a un canale di comunicazione, come e-mail o SMS, e un profilo viene quindi escluso dal canale di comunicazione.

Con Journey Optimizer B2B edition, puoi creare e gestire casi d’uso di abbonamento/annullamento dell’abbonamento per i tuoi messaggi e-mail e SMS. Queste preferenze di consenso sono memorizzate nel gruppo di campi del consenso del profilo XDM e vengono sincronizzate in e fuori da Journey Optimizer B2B edition come parte del Data Sync Framework. Queste preferenze vengono utilizzate al momento della consegna per escludere i profili con rinuncia dalle consegne.

## Ripristino del sandbox

Il ripristino della sandbox è **non attualmente supportato** per Adobe Journey Optimizer B2B edition. Il ripristino o l’eliminazione di una sandbox mappata su Journey Optimizer B2B edition può causare la perdita permanente di dati in Journey Optimizer B2B edition e richiedere il provisioning di una nuova istanza di Journey Optimizer B2B edition.

## Non ancora disponibile

Le seguenti funzioni di governance non sono ancora disponibili:

* Applicazione etichetta di utilizzo dati (DULE) / criteri di utilizzo
* Igiene dei dati
* Criteri di consenso
* Controllo degli accessi a livello di campo (Field-Level Access Control, FLAC)
* Controllo dell&#39;accesso a livello di oggetto (OLAC)
* Crittografia CMK per i dati inattivi
* Servizio di audit della piattaforma
