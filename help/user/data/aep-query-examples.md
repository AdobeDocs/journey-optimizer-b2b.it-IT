---
title: Query set di dati
description: Scopri come utilizzare gli esempi di query SQL in Query Service per analizzare i dati di account, gruppi di acquisto, persone e percorsi esportati da Adobe Journey Optimizer B2B Edition.
feature: Reporting, Data Management
role: Admin, Developer
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
    internal-label: Journey Optimizer B2B Edition
  - id: edbd1a0e-46c8-49da-8c10-dba9ec80bba9
    internal-label: Experience Platform
feature_v2:
  - id: f2da1b69-6919-4386-a5d2-9c7b5c9033db
    internal-label: Data management
level_v2:
  - id: d378ca77-2da1-4f39-ad92-1917fe974a38
    internal-label: Experienced
topic_v2:
  - id: df401a2a-327d-468c-a5e4-b7b7ccd071a0
    internal-label: Data integration
source-git-commit: 6db81a0b993f450a3ff448dcb4c417e3e81ec70a
workflow-type: tm+mt
source-wordcount: '844'
ht-degree: 1%
---

# Query set di dati

Trovare esempi di query SQL pronti all&#39;uso per l&#39;analisi dei dati di account, persona, gruppo di acquisto e percorso esportati da [!DNL Adobe Journey Optimizer B2B Edition] in [!DNL Adobe Experience Platform]. Per creare report su account, gruppi di acquisto, coinvolgimento e-mail e attività di percorso, eseguire le query in [!DNL Query Service].

Per le descrizioni dei set di dati e dei campi utilizzati in queste query, vedere [Set di dati esportati](./aep-exported-datasets.md).

## Prerequisiti {#prerequisites}

Prima di eseguire qualsiasi query in questa pagina, verificare di disporre dei seguenti elementi:

* **Accesso a [!DNL Query Service]:** Devi avere accesso a [Query Service](https://experienceleague.adobe.com/it/docs/experience-platform/query/home){target="_blank"} nella tua sandbox [!DNL Experience Platform].
* **Set di dati disponibili:** Le query hanno come destinazione i [!DNL Journey Optimizer B2B Edition] set di dati esportati. Nella sandbox, vai a **[!UICONTROL Set di dati]** e verifica che i set di dati esistano e contengano dati.
* **Valori dei campi dello schema:** Assicurarsi che i campi nelle query contengano valori nello schema corrispondente. I campi vuoti non restituiscono alcun risultato e non generano errori.

>[!NOTE]
>
>Negli esempi vengono utilizzati nomi di tabella brevi, ad esempio `account_table` e `person_activity_table`. Sostituisci ogni nome di tabella con il nome del set di dati corrispondente nella sandbox. Se il nome di un set di dati contiene trattini, racchiuderlo tra virgolette doppie. Sostituire i valori segnaposto, ad esempio `Example Company` e `PASTE_COMPLETE_JOURNEY_ID_HERE`, con i valori dell&#39;ambiente.

## Eseguire una query {#run}

Per eseguire un esempio in questa pagina:

1. In [!DNL Experience Platform], selezionare **[!UICONTROL Query Service]** > **[!UICONTROL Query]**.
1. Incolla l’esempio nell’editor delle query, quindi sostituisci i nomi delle tabelle e i valori dei segnaposto.
1. Seleziona **[!UICONTROL Esegui]**.

Gli esempi che filtrano per data utilizzano gli ultimi 30 giorni. Per modificare l&#39;intervallo di tempo, modificare il valore `INTERVAL '30' DAY`.

## Scegli una query

Utilizzare la tabella seguente per scegliere una query per l&#39;attività di reporting.

| Io voglio | Vai a |
|---|---|
| Esamina nomi di account, settori e ubicazioni | [Rivedi dettagli account](#account-details) |
| Confronta gruppi di acquisto per impegno | [Confronta impegno gruppo acquisti](#buying-group-engagement) |
| Trovare le persone associate a un account | [Trova persone in un account](#account-people) |
| Tracciare le modifiche allo stato del gruppo di acquisto | [Rivedi modifiche stato gruppo acquisti](#buying-group-status-changes) |
| Trovare le persone che hanno fatto clic su un’e-mail | [Trovare persone che hanno fatto clic su un&#39;e-mail](#email-clicks) |
| Confronta le attività recenti per tipo | [Confronta attività persona recente](#person-activity) |
| Confronta percorsi di account per dimensione | [Confronta i conteggi account per percorso](#account-journey-counts) |
| Elencare gli account in un percorso | [Elenca account in un percorso](#journey-accounts) |
| Tracciare l’attività giornaliera del percorso di account | [Tracciare l&#39;attività giornaliera dell&#39;account](#account-daily-activity) |
| Esaminare la cronologia di un account in un percorso | [Rivedi la sequenza temporale di un percorso di account](#account-timeline) |
| Confronta percorsi di persone per dimensione e stato | [Confronta conteggi persone per percorso](#person-journey-counts) |
| Elencare le persone in un percorso | [Elenca persone in un percorso](#journey-people) |
| Scopri le persone in un percorso | [Confronta conteggi persone per passaggio](#person-step-counts) |
| Tracciare le attività recenti del percorso di persone | [Tracciare le attività di percorso recenti](#person-journey-activity) |
| Esaminare la storia di una persona in un percorso | [Rivedi la sequenza temporale di un percorso di persone](#person-timeline) |

## Query di account e gruppi di acquisto

Utilizzare queste query per esaminare gli account, i gruppi di acquisto e le persone disponibili per il reporting.

### Rivedi dettagli account {#account-details}

Rivedi i nomi dei conti, i settori, le sedi e le dimensioni aziendali per comprendere i conti disponibili per la generazione dei rapporti.

```sql
SELECT
a._id AS accountID,
a.accountName,
a.industry,
a.country,
a.numberOfEmployees
FROM account_table a
WHERE a.isDeleted = FALSE
ORDER BY a.accountName
LIMIT 100;
```

### Confrontare il coinvolgimento del gruppo di acquisto {#buying-group-engagement}

Confronta i gruppi di acquisto in base al punteggio di coinvolgimento registrato, oltre alla completezza e all’interesse per la soluzione.

```sql
SELECT
bg._id AS buyingGroupID,
bg.buyingGroupName,
bg.engagementScore,
bg.completenessScore,
bg.solutionInterest,
bg.buyingGroupStatus
FROM buying_group_table bg
WHERE bg.isDeleted = FALSE
ORDER BY bg.engagementScore DESC NULLS LAST, bg.buyingGroupName
LIMIT 100;
```

### Trovare persone in un account {#account-people}

Trova le persone e le mansioni associate a un account per comprenderne i contatti. Sostituisci `Example Company` con un nome account dalla sandbox.

```sql
SELECT DISTINCT
a._id AS accountID,
a.accountName,
p._id AS personID,
p.firstName,
p.lastName,
p.email,
p.jobTitle
FROM account_member_table m
JOIN account_table a ON m.accountID = a._id
JOIN person_table p ON m.personID = p._id
WHERE m.isDeleted = FALSE
AND a.isDeleted = FALSE
AND p.isDeleted = FALSE
AND a.accountName = 'Example Company'
ORDER BY p.lastName, p.firstName
LIMIT 100;
```

### Rivedi modifiche stato gruppo di acquisto {#buying-group-status-changes}

Esamina le modifiche dello stato del gruppo di acquisto negli ultimi 30 giorni per capire come cambiano i gruppi nel tempo.

```sql
SELECT
bg._id AS buyingGroupID,
bg.buyingGroupName,
e.timestamp AS changedAt,
e.newStatus
FROM buying_group_event_table e
JOIN buying_group_table bg ON e.buyingGroupID = bg._id
WHERE bg.isDeleted = FALSE
AND e.eventType = 'buyingGroup.changeStatus'
AND e.timestamp >= CURRENT_TIMESTAMP - INTERVAL '30' DAY
AND e.timestamp < CURRENT_TIMESTAMP
ORDER BY e.timestamp DESC
LIMIT 100;
```

## Query di coinvolgimento della persona

Utilizza queste query per rivedere il coinvolgimento e-mail e altre attività di persona registrate.

### Trovare le persone che hanno fatto clic su un’e-mail {#email-clicks}

Per rivedere il coinvolgimento nelle e-mail recenti, identifica le persone con clic e-mail registrati negli ultimi 30 giorni.

```sql
SELECT DISTINCT
p._id AS personID,
p.firstName,
p.lastName,
p.email
FROM person_activity_table e
JOIN person_table p ON e.personID = p._id
WHERE e.isDeleted = FALSE
AND p.isDeleted = FALSE
AND e.eventType = 'directMarketing.emailClicked'
AND e.timestamp >= CURRENT_TIMESTAMP - INTERVAL '30' DAY
AND e.timestamp < CURRENT_TIMESTAMP
ORDER BY p.lastName, p.firstName
LIMIT 100;
```

### Confronta attività persona recente {#person-activity}

Confronta i tipi di attività registrati e il numero di persone coinvolte per comprendere il coinvolgimento recente.

```sql
SELECT
e.eventType,
COUNT(*) AS recordedRows,
COUNT(DISTINCT e.personID) AS distinctPeople
FROM person_activity_table e
WHERE e.isDeleted = FALSE
AND e.personID IS NOT NULL
AND e.personID <> ''
AND e.timestamp >= CURRENT_TIMESTAMP - INTERVAL '30' DAY
AND e.timestamp < CURRENT_TIMESTAMP
GROUP BY e.eventType
ORDER BY recordedRows DESC
LIMIT 100;
```

## Query del percorso di account

Utilizzare queste query per analizzare i percorsi di account. Sostituire `PASTE_COMPLETE_JOURNEY_ID_HERE` con il valore `_id` del percorso di account e `PASTE_COMPLETE_ACCOUNT_ID_HERE` con il valore `_id` dell&#39;account.

### Confronta conteggi account per percorso {#account-journey-counts}

Confronta i percorsi di account in base allo stato e al numero di appartenenze registrate per vedere quali percorsi hanno le popolazioni di account più grandi.

```sql
SELECT
j._id AS journeyID,
j.accountJourneyName,
j.accountJourneyStatus,
COUNT(DISTINCT m.accountID) AS accountsWithRecordedMembership
FROM account_journey_table j
LEFT JOIN account_journey_member_table m
ON m.journeyID = j._id
AND m.isDeleted = FALSE
AND m.accountID <> ''
WHERE j.isDeleted = FALSE
GROUP BY j._id, j.accountJourneyName, j.accountJourneyStatus
ORDER BY accountsWithRecordedMembership DESC, j.accountJourneyName
LIMIT 100;
```

### Elencare account in un percorso {#journey-accounts}

Esaminare i conti associati a un determinato percorso, incluse le relative industrie e i paesi.

```sql
SELECT DISTINCT
a._id AS accountID,
a.accountName,
a.industry,
a.country
FROM account_journey_member_table m
JOIN account_table a ON m.accountID = a._id
WHERE m.isDeleted = FALSE
AND a.isDeleted = FALSE
AND m.journeyID = 'PASTE_COMPLETE_JOURNEY_ID_HERE'
ORDER BY a.accountName, accountID
LIMIT 100;
```

### Tracciare l’attività giornaliera dell’account {#account-daily-activity}

Tieni traccia di aggiunte, rimozioni e modifiche ai passaggi dell’account giornaliero per comprendere l’attività in un percorso negli ultimi 30 giorni.

```sql
SELECT
CAST(e.timestamp AS DATE) AS activityDate,
e.eventType,
COUNT(*) AS recordedRows,
COUNT(DISTINCT e.accountID) AS distinctAccounts
FROM account_activity_table e
WHERE e.journeyID = 'PASTE_COMPLETE_JOURNEY_ID_HERE'
AND e.accountID IS NOT NULL
AND e.accountID <> ''
AND e.eventType IN (
'account.addAccountToJourney',
'account.removeAccountFromJourney',
'account.changeAccountJourneyNode'
)
AND e.timestamp >= CURRENT_TIMESTAMP - INTERVAL '30' DAY
AND e.timestamp < CURRENT_TIMESTAMP
GROUP BY CAST(e.timestamp AS DATE), e.eventType
ORDER BY activityDate DESC, e.eventType
LIMIT 100;
```

### Revisione della sequenza temporale di un percorso di account {#account-timeline}

Esamina la cronologia recente del percorso di un account esaminandone gli eventi registrati e i passaggi del percorso.

```sql
SELECT
e.timestamp AS activityAt,
e.eventType,
e.journeyNodeID,
n.nodeType,
e.previousJourneyNodeID,
e.buyingGroupID
FROM account_activity_table e
LEFT JOIN account_journey_node_table n
ON e.journeyNodeID = n._id
AND e.journeyID = n.accountJourneyID
AND n.isDeleted = FALSE
WHERE e.accountID = 'PASTE_COMPLETE_ACCOUNT_ID_HERE'
AND e.journeyID = 'PASTE_COMPLETE_JOURNEY_ID_HERE'
AND e.timestamp >= CURRENT_TIMESTAMP - INTERVAL '30' DAY
AND e.timestamp < CURRENT_TIMESTAMP
ORDER BY e.timestamp DESC
LIMIT 100;
```

## Query del percorso di persone

Utilizzare queste query per analizzare i percorsi di persone. Sostituisci `PASTE_COMPLETE_JOURNEY_ID_HERE` con il valore `_id` del percorso di persone e `PASTE_COMPLETE_PERSON_ID_HERE` con il valore `_id` della persona.

### Confronta conteggi persone per percorso {#person-journey-counts}

Confrontare i percorsi di persone in base al numero di iscrizioni registrate, allo stato e alle date per comprenderne le dimensioni e il ciclo di vita.

```sql
SELECT
j._id AS journeyID,
j.personJourneyName,
j.personJourneyStatus,
j.startDate,
j.endDate,
COUNT(DISTINCT m.personID) AS peopleWithRecordedMembership
FROM person_journey_table j
LEFT JOIN person_journey_member_table m
ON m.journeyID = j._id
AND m.isDeleted = FALSE
AND m.personID <> ''
WHERE j.isDeleted = FALSE
GROUP BY
j._id,
j.personJourneyName,
j.personJourneyStatus,
j.startDate,
j.endDate
ORDER BY peopleWithRecordedMembership DESC, j.personJourneyName
LIMIT 100;
```

### Elencare persone in un percorso {#journey-people}

Controlla chi è associato a un percorso, quando è entrato per l’ultima volta e con quale frequenza.

```sql
SELECT DISTINCT
m.personID,
p.firstName,
p.lastName,
p.email,
m.membershipDate,
m.lastEntryDate,
m.entryCount,
m.reentryOpensAt,
m.journeyNodeID
FROM person_journey_member_table m
LEFT JOIN person_table p
ON m.personID = p._id
AND p.isDeleted = FALSE
WHERE m.isDeleted = FALSE
AND m.personID IS NOT NULL
AND m.personID <> ''
AND m.journeyID = 'PASTE_COMPLETE_JOURNEY_ID_HERE'
ORDER BY m.lastEntryDate DESC NULLS LAST, m.personID
LIMIT 100;
```

### Confronta conteggi persone per passaggio {#person-step-counts}

Scopri come le persone vengono distribuite nei passaggi registrati nelle loro appartenenze al percorso.

```sql
SELECT
m.journeyNodeID,
n.nodeType,
COUNT(DISTINCT m.personID) AS peopleWithRecordedStep
FROM person_journey_member_table m
LEFT JOIN person_journey_node_table n
ON m.journeyNodeID = n._id
AND m.journeyID = n.personJourneyID
AND n.isDeleted = FALSE
WHERE m.isDeleted = FALSE
AND m.personID IS NOT NULL
AND m.personID <> ''
AND m.journeyID = 'PASTE_COMPLETE_JOURNEY_ID_HERE'
GROUP BY m.journeyNodeID, n.nodeType
ORDER BY peopleWithRecordedStep DESC, m.journeyNodeID
LIMIT 100;
```

### Tracciare le attività di percorso recenti {#person-journey-activity}

Confronta gli inizi, le fine e le transizioni registrati del percorso per comprendere l’attività della persona in un percorso negli ultimi 30 giorni.

```sql
SELECT
e.eventType,
COUNT(*) AS recordedRows,
COUNT(DISTINCT e.personID) AS distinctPeople
FROM person_activity_table e
WHERE e.isDeleted = FALSE
AND e.journeyID = 'PASTE_COMPLETE_JOURNEY_ID_HERE'
AND e.personID IS NOT NULL
AND e.personID <> ''
AND e.eventType IN (
'person.journeyAdd',
'person.journeyRemove',
'person.journeyStart',
'person.journeyEnd',
'person.journeyNodeTransition',
'person.journeySplitNode'
)
AND e.timestamp >= CURRENT_TIMESTAMP - INTERVAL '30' DAY
AND e.timestamp < CURRENT_TIMESTAMP
GROUP BY e.eventType
ORDER BY recordedRows DESC, e.eventType
LIMIT 100;
```

### Rivedere la sequenza temporale di un percorso di persone {#person-timeline}

Analizza la cronologia recente del percorso di una persona, incluse le transizioni dei passaggi, le scelte divise e gli aggiornamenti del profilo attribuiti dal percorso.

```sql
SELECT
e.timestamp AS activityAt,
e.eventType,
e.journeyNodeID,
e.previousJourneyNodeID,
e.newJourneyNodeID,
e.journeyChoiceNumber,
e.journeyEntryCount,
e.attributeName,
e.attributeOldValue,
e.attributeNewValue
FROM person_activity_table e
WHERE e.isDeleted = FALSE
AND e.personID = 'PASTE_COMPLETE_PERSON_ID_HERE'
AND e.journeyID = 'PASTE_COMPLETE_JOURNEY_ID_HERE'
AND e.timestamp >= CURRENT_TIMESTAMP - INTERVAL '30' DAY
AND e.timestamp < CURRENT_TIMESTAMP
ORDER BY e.timestamp DESC
LIMIT 100;
```
