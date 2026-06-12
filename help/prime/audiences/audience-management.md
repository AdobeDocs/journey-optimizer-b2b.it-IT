---
title: Gestione dell'audience
description: Pagina segnaposto per i tipi di pubblico.
autotag-review: '2026-06-12T22:47:10.727Z'
TQID: 'https://experienceleague.adobe.com/KWT9-Lr6358MQ0sLQyKAlb4SLERnBl-QQL7Cj1iXCZM'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: beb5f4be-cec3-471a-9db6-831a77dd3ac9
  - id: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2:
  - id: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: cb3217c9fd7beb712d0c61638d143b798010d2b7
workflow-type: tm+mt
source-wordcount: 442
ht-degree: 4%

---

# Gestione del pubblico

Come vengono riprodotti i tipi di pubblico in AJO B2B Prime?

Dall&#39;hub di gestione marketing, fare clic su **[!UICONTROL Elenchi persone]** nell&#39;area di navigazione a destra.

![Accedi agli elenchi di persone per gestire i tuoi tipi di pubblico](./assets/people-lists.png){width="800" zoomable="yes"}

Nella pagina sono disponibili due schede per la visualizzazione e la gestione di **[!UICONTROL elenchi dinamici]** e **[!UICONTROL elenchi statici]**. Fai clic sulla scheda per passare dalla visualizzazione a elenco a un tipo e viceversa.

Da questa pagina è possibile effettuare le seguenti operazioni:

* Creare nuovi elenchi dinamici e statici
* Cerca elenchi esistenti
* Vedi le informazioni sulla risorsa
* Elenchi di accesso per rivedere l&#39;iscrizione

<!--
## Audience Hub

The AI Audience Hub is a centralized, AI-driven starting point for all audience-related capabilities across AJO B2B. It is designed to accelerate first-time user success while progressively unlocking advanced intelligence, insights, and control for returning and power users.

The Hub acts as:

* A guided starting point for discovering, creating, and refining person lists, account lists, and buying groups

* A visibility layer for audience health, coverage, overlap, engagement patterns, and AI-driven insights

* A control center for audience governance, optimization, reuse, and readiness for activation across journeys and sales workflows

### High level structure

Prompt-based starting point - Quick Start prompts and freeform input to help users discover, create, or optimize audiences.

1. AI insights feed - Surfaces key audience signals such as overlap, gaps, saturation risk, and optimization opportunities.

1. Adaptive audience library - A personalized view of people lists, account lists, and buying groups that adapts based on usage, relevance, and activation.

1. Optimization and arbitration nudges - Guides users to refine, split, or reuse audiences before activation.

1. Audience visibility and reporting - High-level insight into audience health, engagement patterns, and usage across active journeys.


### Empty and Error States (High-Level)

No audiences / no data - Show Quick Start prompts to help first-time users create or import person lists

Low data or incomplete audience - Explain what's missing (e.g., insufficient contacts, missing persona coverage, or low engagement data) and suggest next steps.

AI insights unavailable - Provide a graceful fallback with a clear explanation, so users understand why insights aren't shown and what actions they can take manually.
-->

## Creare un elenco di persone


Per creare un nuovo elenco dinamico o statico:

1. Fai clic su **Crea elenco** in alto a destra della pagina _[!UICONTROL Elenchi persone]_.
1. Selezionare un programma come **[!UICONTROL Elemento padre]** per l&#39;elenco.
1. Immettere nell&#39;elenco **[!UICONTROL Nome]** e **[!UICONTROL Descrizione]** (facoltativo).
1. Scegli quindi elenca **[!UICONTROL Tipo]**:

   * **[!UICONTROL Statico]** - L&#39;appartenenza è determinata dai filtri qualificati valutati al momento della creazione dell&#39;elenco. L&#39;iscrizione all&#39;elenco non viene aggiornata a meno che non si qualifichino o non qualifichino manualmente i record.
***[!UICONTROL Dinamico]** - L&#39;appartenenza è determinata dinamicamente da filtri qualificati. L’iscrizione all’elenco si aggiorna automaticamente.

1. Fai clic su **[!UICONTROL Crea]**.

>[!NOTE]
>
>Eliminazione e duplicazione non sono attualmente supportate per gli elenchi di persone in questa versione di Beta.

## Elenchi statici

L’appartenenza a un elenco statico è definita da filtri semplici che fanno riferimento ad attributi e attività delle persone. L&#39;appartenenza non cambia a meno che non si qualifichino o non si qualifichino manualmente i membri.

### Aggiungi membri

1. Apri l&#39;elenco statico e fai clic su **[!UICONTROL Aggiungi persone]** in alto a destra.

1. Nella finestra di dialogo, definisci le regole per qualificare i lead trascinando i filtri da sinistra.

   Puoi filtrare le persone utilizzando qualsiasi combinazione di:

   * Cronologia delle attività
   * Attributi azienda
   * Attributi della persona
   * Filtri speciali, ad esempio appartenenza al Percorso

1. Per salvare le modifiche, fai clic su **[!UICONTROL Fine]**.

1. Selezionare la scheda **[!UICONTROL Membri]**.

   Dopo un breve periodo di tempo, i membri qualificati vengono visualizzati nell&#39;elenco.

### Rimuovi membri

1. Apri l&#39;elenco statico e fai clic su **[!UICONTROL Rimuovi persone]** in alto a destra.

1. Nella finestra di dialogo, aggiungi i filtri per far corrispondere i membri che desideri escludere.

1. Per salvare le modifiche, fai clic su **[!UICONTROL Fine]**.

1. Selezionare la scheda **[!UICONTROL Membri]**.

   Dopo un breve periodo di tempo, i membri squalificati lasciano la lista.

## Elenchi dinamici

L’appartenenza a un elenco dinamico viene definita utilizzando filtri semplici che fanno riferimento agli attributi e alle attività delle persone. L’iscrizione viene mantenuta automaticamente qualificando e squalificando i lead in base alla logica del filtro.

### Definire la logica di appartenenza

1. Apri l’elenco statico e seleziona la scheda Regole.

1. Fai clic su Modifica regole.

1. Nella finestra di dialogo, definisci le regole per qualificare i lead trascinando i filtri da sinistra.

   È possibile qualificare i lead per l&#39;elenco utilizzando qualsiasi combinazione di:

   * Cronologia delle attività
   * Attributi azienda
   * Attributi della persona
   * Filtri speciali, ad esempio appartenenza al Percorso

1. Per salvare le modifiche, fai clic su **[!UICONTROL Fine]**.

1. Selezionare la scheda **[!UICONTROL Membri]**.

   Dopo un breve periodo di tempo, i membri qualificati vengono visualizzati nell&#39;elenco.

Per aprire la pagina dei dettagli del profilo del lead in cui è possibile visualizzare le attività di riepilogo e recenti, fare clic sul nome di una persona nell&#39;elenco.