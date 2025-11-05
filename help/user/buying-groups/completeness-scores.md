---
title: Punteggi di completezza per gruppi di acquisto
description: Calcola i punteggi di completezza dei gruppi di acquisto utilizzando le soglie basate sui ruoli, i requisiti dei membri personalizzabili e le impostazioni di completezza in Journey Optimizer B2B edition.
feature: Buying Groups
role: User
source-git-commit: 1ebc27a709e1b82029c22950897505f3945a507f
workflow-type: tm+mt
source-wordcount: '884'
ht-degree: 3%

---


# Punteggi di completezza {#completeness-scores}

>[!CONTEXTUALHELP]
>id="ajo-b2b_buying_group_completeness_score"
>title="Punteggio di completezza"
>abstract="I punteggi di completezza riflettono il livello di allineamento dell’iscrizione al gruppo di acquisto per un gruppo di acquisto pronto per le vendite."

Un punteggio di completezza è una percentuale che indica il livello di popolamento di un gruppo di acquisto con i membri richiesti nei ruoli definiti. Questi punteggi si basano sulle soglie dei membri del ruolo configurate nel modello dei ruoli e sul numero effettivo di membri assegnati a ciascun ruolo nel gruppo di acquisto. I punteggi risultanti aiutano gli addetti al marketing a valutare la fattibilità delle vendite e a identificare le lacune nella composizione del gruppo di acquisto. Il calcolo del punteggio viene eseguito automaticamente quando cambia l’iscrizione al gruppo di acquisto.

![Punteggi di completezza gruppo acquisti](./assets/buying-group-details-page-completeness-scores.png){width="800" zoomable="yes"}

Esistono due tipi di punteggi di completezza:

* **Punteggio di completezza del gruppo di acquisto** - Il punteggio di completezza del gruppo di acquisto è una percentuale compresa tra 0% e 100% e rappresenta la completezza complessiva del gruppo di acquisto in base ai calcoli di completezza a livello di ruolo.

  Il punteggio di completezza del gruppo di acquisto viene visualizzato nella pagina [Dettagli gruppo di acquisto](./buying-group-details.md). Questo punteggio fornisce una panoramica immediata per capire se il gruppo di acquisto dispone delle parti interessate necessarie per un coinvolgimento nelle vendite.

* **Punteggio di completezza ruolo** - Il punteggio di completezza ruolo è una percentuale per ogni singolo ruolo all&#39;interno di un gruppo di acquisto, in base al numero di membri assegnati a tale ruolo.

  Il punteggio di completezza del ruolo per ogni ruolo viene visualizzato nella pagina dei dettagli del gruppo di acquisto quando si modificano i ruoli e le impostazioni di completezza. Questi punteggi ti aiutano a identificare quali ruoli specifici richiedono ulteriori membri per raggiungere la soglia pronta per le vendite.

  Nella pagina dei dettagli vengono visualizzati i primi due punteggi di completezza dei ruoli, con un collegamento n_+ per gli eventuali ruoli aggiuntivi. Fai clic sul collegamento per visualizzare i punteggi aggiuntivi di completezza del ruolo.

I punteggi di completezza riflettono lo stato corrente di appartenenza al gruppo di acquisto e vengono aggiornati automaticamente quando i membri vengono aggiunti o rimossi. I punteggi visualizzati sono mostrati come percentuali intere (ad esempio, un punteggio del 66,67% viene visualizzato come 67%).

## Valutare la fattibilità

Adobe Journey Optimizer B2B edition offre agli esperti di marketing strumenti che garantiscono l&#39;allineamento dei gruppi di acquisto con processi decisionali reali. È possibile definire gruppi di acquisto completi utilizzando soglie di membri dei ruoli personalizzabili che riflettono la metodologia di vendita della propria organizzazione. Impostando requisiti membri minimi e massimi per ogni ruolo, si definiscono criteri chiari per definire cosa costituisce un gruppo di acquisto pronto per la vendita.

Il punteggio di completezza del gruppo di acquisto fornisce una misura accurata della preparazione alle vendite per il gruppo. Ad esempio, per completare un’opportunità per una soluzione specifica, potresti aver bisogno di almeno due decision maker, un influencer e almeno un professionista. Il calcolo del punteggio di completezza tiene conto di ciascuno di questi requisiti specifici del ruolo, fornendo una visualizzazione della preparazione complessiva del gruppo di acquisto.

## Misurare l’efficacia del percorso

La completezza dei gruppi di acquisto funge da indicatore di prestazioni chiave (KPI, Key Performance Indicator) per l&#39;efficacia del percorso. L’obiettivo per un percorso specifico può essere quello di aumentare la completezza dei gruppi di acquisto di una determinata percentuale o di raggiungere una soglia minima prima di attivare avvisi pronti per le vendite.

In un&#39;azienda di grandi dimensioni è possibile identificare una persona per ruolo. Tuttavia, quella persona potrebbe non essere il contatto giusto per la vendita, o potresti aver bisogno di più contatti per ruoli critici. Ad esempio, una grande organizzazione può disporre di diversi responsabili delle decisioni IT distribuiti tra reparti o unità aziendali. L’identificazione di un’entità con potere decisionale può non essere sufficiente per una vendita di un’impresa complessa.

Dopo aver analizzato la completezza del gruppo di acquisto corrente, è possibile regolare il numero di contatti necessario per ogni ruolo nel modello dei ruoli. Queste regolazioni consentono di regolare la strategia del gruppo di acquisto in base ai modelli reali e ai risultati di vendita.

<!-- ## Analyze audiences for journey optimization

Marketers can view the starting buying group completeness score of target account audiences to find the best performance indicators for a solution. This visibility enables marketers to:

* Determine if they need to adjust the completeness score requirements for each role to make journeys more effective.
* Identify which buying groups are closest to sales-ready status and prioritize them for acceleration campaigns.
* Segment buying groups by completeness score ranges and create tailored nurture strategies for different maturity levels.

>[!BEGINSHADEBOX]

The buying group completeness score is available to use for filtering in [journey split-path-by-account nodes](../journeys/split-merge-paths-nodes.md#account-path-filters) and for audience segmentation. Role completeness can be used to create personalized content that addresses specific gaps in buying group composition.

>[!ENDSHADEBOX] -->

## Calcolo di completezza ruolo {#role-completeness-calculation}

>[!CONTEXTUALHELP]
>id="ajo-b2b_buying_group_role_completeness_calculation"
>title="Calcolo di completezza ruolo"
>abstract="I punteggi di completezza dei ruoli vengono calcolati come percentuale in base al numero di membri assegnati a un ruolo."

Journey Optimizer B2B edition calcola il punteggio di completezza per ogni singolo ruolo del gruppo di acquisto come percentuale. Basare questo punteggio sul numero di membri assegnati al ruolo, rispetto al [numero richiesto nel modello di ruoli](./buying-groups-role-templates.md#change-the-completeness-score-settings) per il completamento.

Il calcolo di completezza del ruolo è una percentuale lineare compresa tra zero e la soglia specificata (membri richiesti):

* Se il numero di membri assegnati è **zero**, la completezza del ruolo è **0%**.
* Se il numero di membri assegnati è pari o superiore a **alla soglia**, la completezza del ruolo è pari a **100%**.
* Se il numero di membri assegnati è **compreso tra uno e la soglia**, la completezza viene calcolata in modo proporzionale.

### Formula di completezza del ruolo

La percentuale di completezza del ruolo viene calcolata utilizzando la formula seguente:

```text
Role Completeness % = ((Assigned Members - Threshold) / (Threshold)) × 100
```

Dove:

* `Assigned Members` = numero corrente di membri nel ruolo
* `Threshold` = Membri valore obbligatorio impostato nel modello dei ruoli

### Esempi di completezza del ruolo

Gli esempi seguenti illustrano i calcoli di completezza dei ruoli con diverse configurazioni di soglia:

| Ruolo | Membri obbligatori | Membri assegnati | Calcolo | Completezza ruolo |
|------|------------------|------------------|-------------|-------------------|
| Responsabile delle decisioni | 3 | 0 | Nessuna | 0% |
|  |  | 1 | 1/3 × 100 | 33% |
|  |  | 2 | 2/3 × 100 | 66% |
|  |  | 3 | Alla soglia | 100% |
|  |  | 4 | Al di sopra della soglia | 100% |
| Influencer | 5 | 0 | Nessuna | 0% |
|  |   | 1 | 1/5 × 100 | 20% |
|  |   | 2 | 2/5 × 100 | 40% |
|  |   | 3 | 3/5 × 100 | 60% |
|  |   | 4 | 4/5 × 100 | 80% |
|  |   | 5 | Alla soglia | 100% |
|  |   | 6 | Al di sopra della soglia | 100% |

## Calcolo di completezza del gruppo di acquisto {#buying-group-completeness-calculation}

Il punteggio di completezza del gruppo di acquisto aggrega i punteggi di completezza dei singoli ruoli. Questo calcolo fornisce una visione olistica della preparazione del gruppo di acquisto in tutti i ruoli definiti.

### Formula di completezza del gruppo di acquisto

La percentuale di completezza del gruppo di acquisto viene calcolata utilizzando la seguente formula:

```text
Buying Group Completeness % = Σ(Role Completeness %) / Number of defined roles
```

Dove:

* `Role Completeness %` = Percentuale di completezza ruolo individuale (0-100%)
* `Σ` = Somma per tutti i ruoli nel gruppo di acquisto

<!--

## Use completeness scores in journeys

Use buying group completeness scores and role-level completeness scores to optimize your account journeys and personalize engagement strategies.

### Split paths by completeness

Use completeness thresholds in [journey split-path-by-account nodes](../journeys/split-merge-paths-nodes.md#account-path-filters) to route buying groups through different journey paths based on their readiness. For example:

* **High completeness path** (≥70%) - Buying groups that are nearly sales-ready can be routed to sales teams or receive call-to-action campaigns
* **Medium completeness path** (40-69%) - Buying groups in active development receive nurture campaigns focused on filling specific role gaps
* **Low completeness path** (<40%) - Newly formed buying groups receive awareness and education content to build initial engagement

### Trigger actions based on completeness milestones

Set up journey events that trigger specific actions when buying groups reach completeness milestones. FOr example:

* Alert sales teams when a buying group reaches 70% completeness.
* Send a _stakeholder alignment_ campaign when completeness increases by 20% or more within a defined timeframe.
* Trigger an automated assessment when a buying group stalls at the same completeness level for an extended period.

By leveraging completeness scores throughout the journey, you create more targeted, efficient campaigns that align with the actual composition and maturity of your buying groups.

-->