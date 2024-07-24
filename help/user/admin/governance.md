---
title: Funzioni di governance
description: Scopri le funzioni di governance attualmente disponibili in Journey Optimizer B2B Edition.
source-git-commit: 1353defe804947617a4d7489592d380bf372c7df
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 1%

---

# Funzioni di governance

In qualità di app Adobe Experience Platform integrata, Journey Optimizer B2B Edition utilizza diversi servizi e strumenti che ti consentono di controllare in modo affidabile i dati sull’esperienza raccolti per rispettare le tue pratiche aziendali, gli obblighi legali e i processi di sviluppo. Le sezioni seguenti forniscono un riepilogo di ciascuna di queste funzioni di governance.

## Privacy - RGPD

Journey Optimizer B2B Edition utilizza le funzioni di governance del Marketo Engage RGPD fornite dal servizio Privacy Service e Marketo Privacy Broker.

## Controllo degli accessi basato sul ruolo (RBAC)

Con Journey Optimizer B2B Edition e l’accesso a Adobe Admin Console, gli amministratori possono concedere a un utente le autorizzazioni per un tipo di entità (view-segments, manage-segments, manage-percorsi e così via). Questa funzionalità fa parte del framework di autorizzazioni unificate (UPF, Unified Permissions Framework) che consente a tutti i clienti di Adobe Experience Platform di definire e gestire ruoli e autorizzazioni per la propria organizzazione.

## Crittografia dei dati

**_Crittografia per i dati inattivi_** - Tutti i dati di account e profili di persona trasferiti da Adobe Experience Platform a Journey Optimizer B2B Edition sono crittografati per mantenere la conformità esistente da Experience Platform. Anche tutte le entità originarie di Journey Optimizer B2B Edition, come percorsi e gruppi di acquisto, sono crittografate.

**_Crittografia per i dati in transito_** (su una rete pubblica) - Tutte le API e le entità dell&#39;edizione B2B di Journey Optimizer sono crittografate in transito utilizzando TLS 1.2.

## Consenso/rinuncia

Consent opt-in/opt-out è una forma di governance in cui un profilo può rinunciare a un canale di comunicazione, come e-mail o SMS, e un profilo deve quindi essere escluso da tale canale di comunicazione.

Con Journey Optimizer B2B Edition, puoi creare e gestire casi d’uso di abbonamento/annullamento dell’abbonamento per e-mail e SMS. Queste preferenze di consenso sono memorizzate nel gruppo di campi del consenso del profilo XDM e vengono sincronizzate in e fuori da Journey Optimizer B2B Edition come parte del Data Sync Framework. Queste preferenze vengono utilizzate al momento della consegna per escludere i profili con rinuncia dalle consegne.

## Non ancora disponibile

Le seguenti funzioni di governance non sono ancora disponibili, ma sono incluse nella roadmap del prodotto:

* Applicazione etichetta di utilizzo dati (DULE) / criteri di utilizzo
* Igiene dei dati
* Ripristino del sandbox
* Criteri di consenso
* Controllo degli accessi a livello di campo (Field-Level Access Control, FLAC)
* Controllo dell&#39;accesso a livello di oggetto (OLAC)
* Crittografia CMK per i dati inattivi
* Servizio di audit della piattaforma
