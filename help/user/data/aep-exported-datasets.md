---
title: Set di dati di Experience Platform esportati
description: Riferimento per i nomi dei set di dati Adobe Experience Platform e i percorsi dei campi chiave esportati da Adobe Journey Optimizer B2B Edition.
feature: Setup, Data Management
role: Admin
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
    internal-label: Journey Optimizer B2B Edition
  - id: edbd1a0e-46c8-49da-8c10-dba9ec80bba9
    internal-label: Experience Platform
feature_v2:
  - id: f2da1b69-6919-4386-a5d2-9c7b5c9033db
    internal-label: Data management
  - id: c8f3fb27-3167-48ac-a66a-fa4bc3f58dda
    internal-label: Integrations
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: d378ca77-2da1-4f39-ad92-1917fe974a38
    internal-label: Experienced
topic_v2:
  - id: df401a2a-327d-468c-a5e4-b7b7ccd071a0
    internal-label: Data integration
autotag-review: '2026-09-29T00:00:00.000Z'
source-git-commit: 801025ee02617d56fc8ab933b59385bca38f5097
workflow-type: tm+mt
source-wordcount: '4845'
ht-degree: 6%
---

# [!DNL Experience Platform] set di dati esportati

[!DNL Adobe Journey Optimizer B2B Edition] rende disponibili le informazioni su account, persona, gruppo di acquisto e percorso in [!DNL Adobe Experience Platform]. Un set di dati è una raccolta di record correlati. Un set di dati persona, ad esempio, descrive le persone, un set di dati di appartenenza collega le persone ad account o percorsi e un set di dati evento registra azioni quali l’apertura di un messaggio e-mail.

Utilizza questa guida per comprendere cosa contiene ogni set di dati, cosa significano i suoi campi e come si connettono i record correlati. I nomi dei set di dati seguono questo pattern:

**`AJOB2B-<datasetVersion>-<entity>`**

`<entity>` descrive le informazioni, ad esempio `person`, `account_relational` o `person_event`. `<datasetVersion>` identifica la versione delle definizioni dei campi del set di dati. I titoli delle sezioni mostrano i nomi documentati; l&#39;ambiente [!DNL Experience Platform] può contenere anche versioni precedenti.

Per le impostazioni dello spazio dei nomi e dello schema che supportano queste esportazioni, vedere [Spazi dei nomi e schemi B2B](./namespaces-schemas.md).

>[!NOTE]
>
>Adobe conserva le versioni precedenti dei set di dati per evitare di interrompere l’utilizzo esistente. Di conseguenza, nella sandbox potrebbero essere presenti più versioni dello stesso set di dati. Se non utilizzi più un set di dati precedente, puoi richiedere che Adobe lo rimuova. Prima di richiedere la rimozione, verifica che il set di dati non sia più in uso.

## Lettura di questa guida

- **Nome campo:** il nome esatto visualizzato in [!DNL Experience Platform]. Punta livelli separati all&#39;interno di un campo, ad esempio `consents.marketing.email.val`.
- **ID record:** identifica il record in tale set di dati.
- **Relazione:** assegna un nome al set di dati e al campo corrispondenti all&#39;identificatore. Ad esempio, `Matches AJOB2B-1_5_4-buying_group (_id)` significa che il campo si riferisce a `_id` di un gruppo di acquisto. Corrispondenza con l’identificatore completo; non abbreviarlo o tentare di ricrearlo.
- **Formato Adobe standard:** utilizza le definizioni dei campi condivisi di Adobe.
- **Formato record correlato:** organizza le informazioni come record che è possibile connettere utilizzando gli identificatori corrispondenti.

Ad esempio, `buying_group_member.buyingGroupID` corrisponde a `buying_group._id` e il suo `personID` corrisponde a `person_relational._id` o al set di dati della persona `personKey.sourceKey`. Questi collegamenti ti aiutano a capire chi appartiene a un gruppo di acquisto. [!DNL Experience Platform] non crea automaticamente rapporti o tipi di pubblico solo dai collegamenti.

Alcuni identificatori fanno riferimento a informazioni che non hanno set di dati separati in questa guida, ad esempio un programma di marketing. La colonna Relazione segnala questo problema invece di denominare un set di dati che non esiste qui.

`isDeleted` è `true` quando il record è contrassegnato come eliminato e `false` quando non lo è. Non trattarlo come un membro attivo generale o come un indicatore di consenso. `lastUpdatedDate` descrive l&#39;ultimo aggiornamento dei dati del record. Per gli eventi, utilizzare `timestamp` per capire quando si è verificata l&#39;attività. Un campo vuoto indica che le informazioni non sono disponibili o non sono applicabili a tale record.

I set di dati dei record correlati utilizzano la versione `1_5_4`. Se un campo non è attualmente popolato o richiede una gestione speciale, la sezione pertinente spiega la limitazione visibile al cliente.

Un pubblico è un gruppo di persone che soddisfano i criteri selezionati. La disponibilità per la creazione di tipi di pubblico dipende dalla configurazione di [!DNL Experience Platform] per la combinazione di informazioni in profili di persona. La presenza di un set di dati in [!DNL Experience Platform] non significa di per sé che sia disponibile per la segmentazione.

## Scelta di un set di dati

| Cosa vuoi capire | Set di dati da cercare |
|---|---|
| Persone e relative preferenze e-mail | `person` |
| Dettagli dell’account e dettagli di contatto della persona | `account_relational`, `person_relational` |
| Quali persone sono associate a un account | `account_member`, `account_person` |
| Gruppi di acquisto, relativi membri e modifiche di stato | `buying_group`, `buying_group_member`, `buying_group_event` |
| Percorsi di conti e conti partecipanti | `account_journey`, `account_journey_member`, `account_event` |
| Percorsi di persone e persone partecipanti | `person_journey`, `person_journey_member` |
| Passaggi all’interno di un percorso | `account_journey_node`, `person_journey_node`, `journey_node` |
| Attività relative a e-mail, web e altre persone supportate | `person_event`, `person_event_relational` |

Le sezioni seguenti forniscono i nomi completi dei set di dati e i dettagli dei campi. Un percorso descrive l’esperienza complessiva; un’iscrizione collega una persona o un account a quel percorso; un evento descrive qualcosa che è successo.

+++Diagramma relazioni entità

![Diagramma relazioni entità per i set di dati esportati in [!DNL Adobe Experience Platform]](./assets/ajo-b2b-data-model.svg)

+++

## `AJOB2B-1_5_1-person`

Ogni record descrive una persona, i suoi identificatori e le sue preferenze di e-mail marketing. Utilizzala per la generazione di rapporti a livello di persona e, laddove è configurato il profilo, per aiutare a creare tipi di pubblico.

**Formato:** Formato Adobe standard

| Nome campo | Relazione | Cosa ti dice |
|------------|-------------|-------------|
| `personID` | ID record | Identificatore della persona. Utilizza il valore completo per far corrispondere i record correlati. |
| `personKey.sourceID` |  | Identificatore della persona nel sistema connesso. |
| `personKey.sourceInstanceID` |  | Identificatore dell&#39;ambiente [!DNL Experience Platform] o dell&#39;account connesso. |
| `personKey.sourceType` |  | Nome del prodotto connesso. |
| `personKey.sourceKey` |  | Identificatore completo della persona utilizzato per far corrispondere i record correlati. |
| `identityMap` |  | Altri identificatori che consentono a [!DNL Experience Platform] di riconoscere la stessa persona nei dati connessi. |
| `consents.marketing.email.val` |  | Preferenza marketing e-mail: `n` indica una rinuncia; `y` indica che non è stata registrata alcuna rinuncia in questo campo. Questo campo da solo non stabilisce l’autorizzazione per inviare e-mail di marketing. |
| `consents.marketing.email.time` |  | Data e ora dell’ultimo aggiornamento della preferenza e-mail. |
| `consents.marketing.email.reason` |  | Motivo della rinuncia, se fornito (impostato solo se l’abbonamento è stato annullato). |
| `isDeleted` |  | Indica se il record della persona è contrassegnato come eliminato. |

>[!NOTE]
>
>La tua organizzazione può avere campi persona aggiuntivi oltre a quelli elencati qui.

Quando l&#39;organizzazione utilizza set di dati personali o account configurati, tali record possono includere anche `isDeleted`. Vedi [Set di dati di proprietà del cliente](#customer-owned-datasets).

## `AJOB2B-1_5_4-account_member`

Ogni record collega un account a una persona. Utilizza questo set di dati per segnalare quali persone sono associate a ciascun account; descrive la relazione anziché uno dei due profili.

**Formato:** Formato record correlati

| Nome campo | Relazione | Cosa ti dice |
|------------|-------------|-------------|
| `_id` | ID record | ID record relazione. |
| `accountID` | Corrisponde a `AJOB2B-1_5_4-account_relational` (`_id`) | Identificatore dell’account. |
| `personID` | Corrisponde a `AJOB2B-1_5_4-person_relational` (`_id`) | Identificatore della persona. |
| `isDeleted` |  | Indica se il record è contrassegnato come eliminato. |
| `lastUpdatedDate` |  | Ora ultima modifica. |

## `AJOB2B-1_5_4-buying_group`

Ogni record descrive un gruppo di acquisto associato a un account, inclusi il nome, lo stato, l&#39;interesse per la soluzione e i punteggi di coinvolgimento e completezza. La fase del gruppo di acquisto non è attualmente compilata.

**Formato:** Formato record correlati

| Nome campo | Relazione | Cosa ti dice |
|------------|-------------|-------------|
| `_id` | ID record | ID record gruppo di acquisto (utilizzare il valore completo). |
| `buyingGroupName` |  | Nome del gruppo di acquisto. |
| `engagementScore` |  | Punteggio di coinvolgimento. |
| `completenessScore` |  | Valutazione della completezza. |
| `accountID` | Corrisponde a `AJOB2B-1_5_4-account_relational` (`_id`) | Identificatore account correlato. |
| `solutionInterest` |  | Etichetta di interesse della soluzione. |
| `buyingGroupStatus` |  | Stato. |
| `buyingGroupStage` |  | Nome fase del gruppo di acquisto. |
| `isDeleted` |  | Indica se il record è contrassegnato come eliminato. |
| `lastUpdatedDate` |  | Ora ultima modifica. |

>[!NOTE]
>
>**Nota sulla disponibilità:** `buyingGroupStage` è attualmente vuoto. Non utilizzarlo per filtrare o raggruppare i gruppi di acquisto per fase.

## `AJOB2B-1_5_4-buying_group_member`

Ogni record collega una persona a un gruppo di acquisto e ne registra il ruolo. Utilizzala per segnalare la composizione del gruppo di acquisto e la copertura dei ruoli.

`isDeleted` non indica sempre se una persona è stata rimossa da un gruppo di acquisto. Non utilizzare questo solo campo per determinare l&#39;appartenenza corrente. Il nome del ruolo può essere vuoto se non sono disponibili informazioni sul ruolo.

**Formato:** Formato record correlati

| Nome campo | Relazione | Cosa ti dice |
|------------|-------------|-------------|
| `_id` | ID record | ID del record di appartenenza. |
| `buyingGroupID` | Corrisponde a `AJOB2B-1_5_4-buying_group` (`_id`) | Identificatore del gruppo di acquisto. |
| `personID` | Corrisponde a `AJOB2B-1_5_4-person_relational` (`_id`) | Identificatore della persona. |
| `buyingGroupMemberRole` |  | Nome del ruolo, se disponibile. |
| `isDeleted` |  | Indica se il record è contrassegnato come eliminato. |
| `lastUpdatedDate` |  | Ora ultima modifica. |

## `AJOB2B-1_5_4-account_journey`

Ogni record descrive un percorso di conti, con il nome, lo stato e le date di inizio e fine. Utilizzala per segnalare il ciclo di vita del percorso e lo stato degli account.

**Formato:** Formato record correlati

| Nome campo | Relazione | Cosa ti dice |
|------------|-------------|-------------|
| `_id` | ID record | ID record percorso (utilizzare il valore completo). |
| `accountJourneyName` |  | Nome percorso. |
| `accountJourneyStatus` |  | Stato (ad esempio bozza, live, finished). |
| `startDate` |  | Timestamp di inizio. |
| `endDate` |  | Timestamp di fine. |
| `isDeleted` |  | Indica se il record è contrassegnato come eliminato. |
| `lastUpdatedDate` |  | Ora ultima modifica. |

## `AJOB2B-1_5_4-account_journey_member`

Ogni record collega un account a un percorso di account. Utilizzalo per identificare e segnalare quali account partecipano a ciascun percorso.

**Formato:** Formato record correlati

| Nome campo | Relazione | Cosa ti dice |
|------------|-------------|-------------|
| `_id` | ID record | ID del record di appartenenza. |
| `accountID` | Corrisponde a `AJOB2B-1_5_4-account_relational` (`_id`) | Identificatore dell’account. |
| `journeyID` | Corrisponde a `AJOB2B-1_5_4-account_journey` (`_id`) | Identificatore del percorso di account. |
| `isDeleted` |  | Indica se il record è contrassegnato come eliminato. |
| `lastUpdatedDate` |  | Ora ultima modifica. |

## `AJOB2B-1_5_4-person_journey`

Ogni record descrive un percorso di persone, con il nome, lo stato e le date di inizio e fine. Utilizzala per segnalare il ciclo di vita e lo stato del percorso per i percorsi incentrati sulle persone.

**Formato:** Formato record correlati

| Nome campo | Relazione | Cosa ti dice |
|------------|-------------|-------------|
| `_id` | ID record | ID record percorso (utilizzare il valore completo). |
| `personJourneyName` |  | Nome percorso. |
| `personJourneyStatus` |  | Stato (ad esempio bozza, live, finished). |
| `startDate` |  | Timestamp di inizio. |
| `endDate` |  | Timestamp di fine. |
| `isDeleted` |  | Indica se il record è contrassegnato come eliminato. |
| `lastUpdatedDate` |  | Ora ultima modifica. |

## `AJOB2B-1_5_4-person_journey_member`

Ogni record descrive l&#39;appartenenza di una persona a un percorso, inclusi il nodo del percorso corrente, le date di iscrizione e appartenenza e il conteggio delle voci. Utilizzala per segnalare l’iscrizione, il reinserimento e l’avanzamento del percorso.

**Formato:** Formato record correlati

| Nome campo | Relazione | Cosa ti dice |
|------------|-------------|-------------|
| `_id` | ID record | ID del record di appartenenza. |
| `marketingProgramID` |  | Identificatore del programma di marketing a cui appartiene il percorso. |
| `personID` | Corrisponde a `AJOB2B-1_5_4-person_relational` (`_id`) | Identificatore della persona. |
| `journeyID` | Corrisponde a `AJOB2B-1_5_4-person_journey` (`_id`) | Identificatore percorso. |
| `journeyNodeID` | Corrisponde a `AJOB2B-1_5_4-person_journey_node` (`_id`) | Identificatore del nodo del percorso in cui si trova attualmente la persona. |
| `membershipDate` |  | Quando la persona è diventata membro del programma di marketing. |
| `lastEntryDate` |  | Data dell’ultimo accesso al percorso. |
| `reentryOpensAt` |  | Quando la persona può rientrare nel percorso. |
| `entryCount` |  | Numero di volte in cui la persona è entrata nel percorso. |
| `createdDate` |  | Data di creazione del record. |
| `updatedDate` |  | Data dell&#39;ultima modifica del record. |
| `isDeleted` |  | Indica se il record è contrassegnato come eliminato. |
| `lastUpdatedDate` |  | Ora ultima modifica. |

## `AJOB2B-1_5_4-account_journey_node`

Ogni record descrive un passaggio di un percorso, incluso il tipo di passaggio e il percorso a cui appartiene. Un nodo di percorso è un passaggio, ad esempio un inizio, un&#39;attesa o una decisione. Gli stessi passaggi possono essere visualizzati in `person_journey_node`; abbina `accountJourneyID` a un percorso di account prima di trattare un passaggio come specifico per l&#39;account.

**Formato:** Formato record correlati

| Nome campo | Relazione | Cosa ti dice |
|------------|-------------|-------------|
| `_id` | ID record | ID del record del nodo (utilizza il valore completo). |
| `accountJourneyID` | Corrisponde a `AJOB2B-1_5_4-account_journey` (`_id`) | Identificatore del percorso padre. |
| `uuid` |  | Identificatore aggiuntivo per il passaggio di percorso. |
| `journeyNodeTypeID` |  | Numero che identifica il tipo di passaggio del percorso. |
| `nodeType` |  | Etichetta che identifica il tipo di passaggio del percorso. |
| `isDeleted` |  | Indica se il record è contrassegnato come eliminato. |
| `createdDate` |  | Data di creazione del record. |
| `lastUpdatedDate` |  | Ora ultima modifica. |

## `AJOB2B-1_5_4-person_journey_node`

Ogni record descrive un passaggio di un percorso, incluso il tipo di passaggio e il percorso a cui appartiene. Gli stessi passaggi possono essere visualizzati in `account_journey_node`; abbina `personJourneyID` a un percorso di persone prima di trattare un passaggio come specifico per la persona.

**Formato:** Formato record correlati

| Nome campo | Relazione | Cosa ti dice |
|------------|-------------|-------------|
| `_id` | ID record | ID del record del nodo (utilizza il valore completo). |
| `personJourneyID` | Corrisponde a `AJOB2B-1_5_4-person_journey` (`_id`) | Identificatore del percorso padre. |
| `uuid` |  | Identificatore aggiuntivo per il passaggio di percorso. |
| `journeyNodeTypeID` |  | Numero che identifica il tipo di passaggio del percorso. |
| `nodeType` |  | Etichetta che identifica il tipo di passaggio del percorso. |
| `isDeleted` |  | Indica se il record è contrassegnato come eliminato. |
| `createdDate` |  | Data di creazione del record. |
| `lastUpdatedDate` |  | Ora ultima modifica. |

## `AJOB2B-1_5_4-account_event`

Ogni record acquisisce un evento di percorso dell’account: un account che viene aggiunto o rimosso da un percorso o che si sposta tra i nodi del percorso. Utilizzare `eventType` e `timestamp` per creare una sequenza temporale dell&#39;attività dell&#39;account; `buyingGroupID` è disponibile quando l&#39;evento è attribuito al gruppo di acquisto.

**Formato:** Formato record correlati

`eventType` fornisce informazioni sull&#39;evento. Le tabelle seguenti descrivono i campi per ogni tipo di attività.

`lastUpdatedDate` non è attualmente popolato per questi eventi. Utilizza `timestamp` per la data attività.

### Account aggiunto a un percorso (`account.addAccountToJourney`)

| Nome campo | Relazione | Cosa ti dice |
|------------|-------------|-------------|
| `_id` | ID record | Identificatore dell’attività. |
| `eventType` |  | `account.addAccountToJourney`. |
| `timestamp` |  | Quando si è verificata l’attività. |
| `accountID` | Corrisponde a `AJOB2B-1_5_4-account_relational` (`_id`) | Identificatore dell’account. |
| `journeyID` | Corrisponde a `AJOB2B-1_5_4-account_journey` (`_id`) | Identificatore percorso. |
| `journeyNodeID` | Corrisponde a `AJOB2B-1_5_4-account_journey_node` (`_id`) | Identificatore del nodo del percorso. |
| `buyingGroupID` | Corrisponde a `AJOB2B-1_5_4-buying_group` (`_id`) | Identificatore del gruppo di acquisto, quando l’aggiunta al percorso è attribuita al gruppo di acquisto. |
| `lastUpdatedDate` |  | Registra ora di aggiornamento. Attualmente vuoto; utilizza la marca temporale per la data dell’attività. |

### Account rimosso da un percorso (`account.removeAccountFromJourney`)

| Nome campo | Relazione | Cosa ti dice |
|------------|-------------|-------------|
| `_id` | ID record | Identificatore dell’attività. |
| `eventType` |  | `account.removeAccountFromJourney`. |
| `timestamp` |  | Quando si è verificata l’attività. |
| `accountID` | Corrisponde a `AJOB2B-1_5_4-account_relational` (`_id`) | Identificatore dell’account. |
| `journeyID` | Corrisponde a `AJOB2B-1_5_4-account_journey` (`_id`) | Identificatore percorso. |
| `journeyNodeID` | Corrisponde a `AJOB2B-1_5_4-account_journey_node` (`_id`) | Identificatore del nodo del percorso. |
| `buyingGroupID` | Corrisponde a `AJOB2B-1_5_4-buying_group` (`_id`) | Identificatore del gruppo di acquisto, quando la rimozione del percorso è attribuita al gruppo di acquisto. |
| `lastUpdatedDate` |  | Registra ora di aggiornamento. Attualmente vuoto; utilizza la marca temporale per la data dell’attività. |

### Account spostato tra i passaggi del percorso (`account.changeAccountJourneyNode`)

| Nome campo | Relazione | Cosa ti dice |
|------------|-------------|-------------|
| `_id` | ID record | Identificatore dell’attività. |
| `eventType` |  | `account.changeAccountJourneyNode`. |
| `timestamp` |  | Quando si è verificata l’attività. |
| `accountID` | Corrisponde a `AJOB2B-1_5_4-account_relational` (`_id`) | Identificatore dell’account. |
| `journeyID` | Corrisponde a `AJOB2B-1_5_4-account_journey` (`_id`) | Identificatore percorso. |
| `journeyNodeID` | Corrisponde a `AJOB2B-1_5_4-account_journey_node` (`_id`) | Identificatore del nodo del percorso. |
| `previousJourneyNodeID` | Fa riferimento a `AJOB2B-1_5_4-account_journey_node` (`_id`); i valori potrebbero non corrispondere | Identificatore del passaggio di percorso precedente. Questo valore potrebbe non corrispondere al record del passaggio corrispondente; non fare affidamento solo su di esso per collegare i record. |
| `buyingGroupID` | Corrisponde a `AJOB2B-1_5_4-buying_group` (`_id`) | Identificatore del gruppo di acquisto, quando la modifica del nodo è attribuita al gruppo di acquisto. |
| `lastUpdatedDate` |  | Registra ora di aggiornamento. Attualmente vuoto; utilizza la marca temporale per la data dell’attività. |

## `AJOB2B-1_5_4-buying_group_event`

Ogni record acquisisce una modifica allo stato di un gruppo di acquisto, incluso il nuovo stato e quando è stato modificato. Il campo new-stage non è attualmente popolato.

**Formato:** Formato record correlati

### Stato del gruppo di acquisto modificato (`buyingGroup.changeStatus`)

| Nome campo | Relazione | Cosa ti dice |
|------------|-------------|-------------|
| `_id` | ID record | Identificatore dell’attività. |
| `eventType` |  | `buyingGroup.changeStatus`. |
| `timestamp` |  | Quando si è verificata l’attività. |
| `buyingGroupID` | Corrisponde a `AJOB2B-1_5_4-buying_group` (`_id`) | Identificatore del gruppo di acquisto. |
| `newStatus` |  | Nuovo valore di stato. |
| `newStage` |  | Nuova fase del gruppo di acquisto. Attualmente vuoto. |
| `lastUpdatedDate` |  | Registra ora di aggiornamento. |

>[!NOTE]
>
>**Nota sulla disponibilità:** utilizza `newStatus` per segnalare le modifiche di stato. Non utilizzare `newStage` per segnalare le modifiche della fase perché è attualmente vuoto.

## `AJOB2B-1_5-person_event`

Ogni record descrive un evento web, e-mail o altro evento attività supportato a livello di persona. Utilizzare `eventType` e `timestamp` per analizzare il comportamento nel tempo, con dettagli specifici dell&#39;evento popolati solo per il tipo di evento corrispondente.

**Formato:** Formato Adobe standard

`eventType` ti dice cosa è successo. Le tabelle seguenti descrivono i campi per ogni tipo di attività. I dettagli che non si applicano a un evento sono vuoti.

### E-mail inviata (`directMarketing.emailSent`)

| Nome campo | Relazione | Cosa ti dice |
|------------|-------------|-------------|
| `_id` | ID record | Identificatore dell’attività. |
| `eventType` |  | `directMarketing.emailSent`. |
| `timestamp` |  | Quando si è verificata l’attività. |
| `personID` | Corrisponde a `AJOB2B-1_5_1-person` (`personID`) | Identificatore della persona. |
| `personKey.sourceID` |  | Identificatore della persona nel sistema connesso. |
| `personKey.sourceType` |  | Nome del prodotto connesso. |
| `personKey.sourceInstanceID` |  | Identificatore dell&#39;ambiente [!DNL Experience Platform] o dell&#39;account connesso. |
| `personKey.sourceKey` |  | Identificatore completo della persona utilizzato per far corrispondere i record correlati. |
| `directMarketing.emailSent.mailingKey.sourceID` |  | ID risorsa mailing. |
| `directMarketing.emailSent.mailingKey.sourceType` |  | Nome del prodotto connesso. |
| `directMarketing.emailSent.mailingKey.sourceInstanceID` |  | ID istanza. |
| `directMarketing.emailSent.mailingKey.sourceKey` |  | Identificatore completo del contenuto e-mail. |
| `directMarketing.emailSent.mailingName` |  | Nome mailing. |
| `_experience.journeyOrchestration.stepEvents.journeyID` | Corrisponde a `AJOB2B-1_5_4-person_journey` (`_id`) | ID percorso (se attribuito). |
| `_experience.journeyOrchestration.stepEvents.nodeID` | Corrisponde a `AJOB2B-1_5_4-person_journey_node` (`_id`) | ID nodo percorso (se attribuito). |

### E-mail consegnata (`directMarketing.emailDelivered`)

| Nome campo | Relazione | Cosa ti dice |
|------------|-------------|-------------|
| `_id` | ID record | Identificatore dell’attività. |
| `eventType` |  | `directMarketing.emailDelivered`. |
| `timestamp` |  | Quando si è verificata l’attività. |
| `personID` | Corrisponde a `AJOB2B-1_5_1-person` (`personID`) | Identificatore della persona. |
| `personKey.sourceID` |  | Identificatore della persona nel sistema connesso. |
| `personKey.sourceType` |  | Nome del prodotto connesso. |
| `personKey.sourceInstanceID` |  | Identificatore dell&#39;ambiente [!DNL Experience Platform] o dell&#39;account connesso. |
| `personKey.sourceKey` |  | Identificatore completo della persona utilizzato per far corrispondere i record correlati. |
| `directMarketing.mailingKey.sourceID` |  | ID risorsa mailing. |
| `directMarketing.mailingKey.sourceType` |  | Nome del prodotto connesso. |
| `directMarketing.mailingKey.sourceInstanceID` |  | ID istanza. |
| `directMarketing.mailingKey.sourceKey` |  | Identificatore completo del contenuto e-mail. |
| `directMarketing.mailingName` |  | Nome mailing. |
| `directMarketing.email` |  | Indirizzo e-mail. |
| `_experience.journeyOrchestration.stepEvents.journeyID` | Corrisponde a `AJOB2B-1_5_4-person_journey` (`_id`) | ID percorso (se attribuito). |
| `_experience.journeyOrchestration.stepEvents.nodeID` | Corrisponde a `AJOB2B-1_5_4-person_journey_node` (`_id`) | ID nodo percorso (se attribuito). |

### Annullamento iscrizione e-mail (`directMarketing.emailUnsubscribed`)

| Nome campo | Relazione | Cosa ti dice |
|------------|-------------|-------------|
| `_id` | ID record | Identificatore dell’attività. |
| `eventType` |  | `directMarketing.emailUnsubscribed`. |
| `timestamp` |  | Quando si è verificata l’attività. |
| `personID` | Corrisponde a `AJOB2B-1_5_1-person` (`personID`) | Identificatore della persona. |
| `personKey.sourceID` |  | Identificatore della persona nel sistema connesso. |
| `personKey.sourceType` |  | Nome del prodotto connesso. |
| `personKey.sourceInstanceID` |  | Identificatore dell&#39;ambiente [!DNL Experience Platform] o dell&#39;account connesso. |
| `personKey.sourceKey` |  | Identificatore completo della persona utilizzato per far corrispondere i record correlati. |
| `directMarketing.mailingKey.sourceID` |  | ID risorsa mailing. |
| `directMarketing.mailingKey.sourceType` |  | Nome del prodotto connesso. |
| `directMarketing.mailingKey.sourceInstanceID` |  | ID istanza. |
| `directMarketing.mailingKey.sourceKey` |  | Identificatore completo del contenuto e-mail. |
| `directMarketing.mailingName` |  | Nome mailing. |
| `directMarketing.email` |  | Indirizzo e-mail. |
| `_experience.journeyOrchestration.stepEvents.journeyID` | Corrisponde a `AJOB2B-1_5_4-person_journey` (`_id`) | ID percorso (se attribuito). |
| `_experience.journeyOrchestration.stepEvents.nodeID` | Corrisponde a `AJOB2B-1_5_4-person_journey_node` (`_id`) | ID nodo percorso (se attribuito). |

### E-mail aperta (`directMarketing.emailOpened`)

| Nome campo | Relazione | Cosa ti dice |
|------------|-------------|-------------|
| `_id` | ID record | Identificatore dell’attività. |
| `eventType` |  | `directMarketing.emailOpened`. |
| `timestamp` |  | Quando si è verificata l’attività. |
| `personID` | Corrisponde a `AJOB2B-1_5_1-person` (`personID`) | Identificatore della persona. |
| `personKey.sourceID` |  | Identificatore della persona nel sistema connesso. |
| `personKey.sourceType` |  | Nome del prodotto connesso. |
| `personKey.sourceInstanceID` |  | Identificatore dell&#39;ambiente [!DNL Experience Platform] o dell&#39;account connesso. |
| `personKey.sourceKey` |  | Identificatore completo della persona utilizzato per far corrispondere i record correlati. |
| `directMarketing.mailingKey.sourceID` |  | ID risorsa mailing. |
| `directMarketing.mailingKey.sourceType` |  | Nome del prodotto connesso. |
| `directMarketing.mailingKey.sourceInstanceID` |  | ID istanza. |
| `directMarketing.mailingKey.sourceKey` |  | Identificatore completo del contenuto e-mail. |
| `directMarketing.mailingName` |  | Nome mailing. |
| `directMarketing.email` |  | Indirizzo e-mail. |
| `_experience.journeyOrchestration.stepEvents.journeyID` | Corrisponde a `AJOB2B-1_5_4-person_journey` (`_id`) | ID percorso (se attribuito). |
| `_experience.journeyOrchestration.stepEvents.nodeID` | Corrisponde a `AJOB2B-1_5_4-person_journey_node` (`_id`) | ID nodo percorso (se attribuito). |
| `device.isMobileDevice` |  | Se un dispositivo mobile è stato registrato per l&#39;attività. |
| `device.model` |  | Informazioni sul dispositivo o sul client e-mail. |
| `environment.browserDetails.userAgent` |  | Informazioni sul browser o sul client e-mail. |
| `environment.operatingSystem` |  | Sistema operativo. |

### Collegamento e-mail selezionato (`directMarketing.emailClicked`)

| Nome campo | Relazione | Cosa ti dice |
|------------|-------------|-------------|
| `_id` | ID record | Identificatore dell’attività. |
| `eventType` |  | `directMarketing.emailClicked`. |
| `timestamp` |  | Quando si è verificata l’attività. |
| `personID` | Corrisponde a `AJOB2B-1_5_1-person` (`personID`) | Identificatore della persona. |
| `personKey.sourceID` |  | Identificatore della persona nel sistema connesso. |
| `personKey.sourceType` |  | Nome del prodotto connesso. |
| `personKey.sourceInstanceID` |  | Identificatore dell&#39;ambiente [!DNL Experience Platform] o dell&#39;account connesso. |
| `personKey.sourceKey` |  | Identificatore completo della persona utilizzato per far corrispondere i record correlati. |
| `directMarketing.mailingKey.sourceID` |  | ID risorsa mailing. |
| `directMarketing.mailingKey.sourceType` |  | Nome del prodotto connesso. |
| `directMarketing.mailingKey.sourceInstanceID` |  | ID istanza. |
| `directMarketing.mailingKey.sourceKey` |  | Identificatore completo del contenuto e-mail. |
| `directMarketing.mailingName` |  | Nome mailing. |
| `directMarketing.email` |  | Indirizzo e-mail. |
| `directMarketing.linkURL` |  | URL collegamento selezionato. |
| `_experience.journeyOrchestration.stepEvents.journeyID` | Corrisponde a `AJOB2B-1_5_4-person_journey` (`_id`) | ID percorso (se attribuito). |
| `_experience.journeyOrchestration.stepEvents.nodeID` | Corrisponde a `AJOB2B-1_5_4-person_journey_node` (`_id`) | ID nodo percorso (se attribuito). |
| `device.isMobileDevice` |  | Se un dispositivo mobile è stato registrato per l&#39;attività. |
| `device.model` |  | Informazioni sul dispositivo o sul client e-mail. |
| `environment.browserDetails.userAgent` |  | Informazioni sul browser o sul client e-mail. |
| `environment.operatingSystem` |  | Sistema operativo. |

### E-mail non recapitata (`directMarketing.emailBounced`)

| Nome campo | Relazione | Cosa ti dice |
|------------|-------------|-------------|
| `_id` | ID record | Identificatore dell’attività. |
| `eventType` |  | `directMarketing.emailBounced`. |
| `timestamp` |  | Quando si è verificata l’attività. |
| `personID` | Corrisponde a `AJOB2B-1_5_1-person` (`personID`) | Identificatore della persona. |
| `personKey.sourceID` |  | Identificatore della persona nel sistema connesso. |
| `personKey.sourceType` |  | Nome del prodotto connesso. |
| `personKey.sourceInstanceID` |  | Identificatore dell&#39;ambiente [!DNL Experience Platform] o dell&#39;account connesso. |
| `personKey.sourceKey` |  | Identificatore completo della persona utilizzato per far corrispondere i record correlati. |
| `directMarketing.mailingKey.sourceID` |  | ID risorsa mailing. |
| `directMarketing.mailingKey.sourceType` |  | Nome del prodotto connesso. |
| `directMarketing.mailingKey.sourceInstanceID` |  | ID istanza. |
| `directMarketing.mailingKey.sourceKey` |  | Identificatore completo del contenuto e-mail. |
| `directMarketing.mailingName` |  | Nome mailing. |
| `directMarketing.email` |  | Indirizzo e-mail. |
| `directMarketing.emailBouncedCode` |  | Categoria/codice di mancato recapito. |
| `directMarketing.emailBouncedDetails` |  | Testo dettagliato. |
| `_experience.journeyOrchestration.stepEvents.journeyID` | Corrisponde a `AJOB2B-1_5_4-person_journey` (`_id`) | ID percorso (se attribuito). |
| `_experience.journeyOrchestration.stepEvents.nodeID` | Corrisponde a `AJOB2B-1_5_4-person_journey_node` (`_id`) | ID nodo percorso (se attribuito). |

### E-mail non recapitate (`directMarketing.emailBouncedSoft`)

| Nome campo | Relazione | Cosa ti dice |
|------------|-------------|-------------|
| `_id` | ID record | Identificatore dell’attività. |
| `eventType` |  | `directMarketing.emailBouncedSoft`. |
| `timestamp` |  | Quando si è verificata l’attività. |
| `personID` | Corrisponde a `AJOB2B-1_5_1-person` (`personID`) | Identificatore della persona. |
| `personKey.sourceID` |  | Identificatore della persona nel sistema connesso. |
| `personKey.sourceType` |  | Nome del prodotto connesso. |
| `personKey.sourceInstanceID` |  | Identificatore dell&#39;ambiente [!DNL Experience Platform] o dell&#39;account connesso. |
| `personKey.sourceKey` |  | Identificatore completo della persona utilizzato per far corrispondere i record correlati. |
| `directMarketing.mailingKey.sourceID` |  | ID risorsa mailing. |
| `directMarketing.mailingKey.sourceType` |  | Nome del prodotto connesso. |
| `directMarketing.mailingKey.sourceInstanceID` |  | ID istanza. |
| `directMarketing.mailingKey.sourceKey` |  | Identificatore completo del contenuto e-mail. |
| `directMarketing.mailingName` |  | Nome mailing. |
| `directMarketing.email` |  | Indirizzo e-mail. |
| `directMarketing.emailBouncedCode` |  | Categoria/codice di mancato recapito. |
| `directMarketing.emailBouncedDetails` |  | Testo dettagliato. |
| `_experience.journeyOrchestration.stepEvents.journeyID` | Corrisponde a `AJOB2B-1_5_4-person_journey` (`_id`) | ID percorso (se attribuito). |
| `_experience.journeyOrchestration.stepEvents.nodeID` | Corrisponde a `AJOB2B-1_5_4-person_journey_node` (`_id`) | ID nodo percorso (se attribuito). |

### Pagina Web visualizzata (`web.webpagedetails.pageViews`)

| Nome campo | Relazione | Cosa ti dice |
|------------|-------------|-------------|
| `_id` | ID record | Identificatore dell’attività. |
| `eventType` |  | `web.webpagedetails.pageViews`. |
| `timestamp` |  | Quando si è verificata l’attività. |
| `personID` | Corrisponde a `AJOB2B-1_5_1-person` (`personID`) | Identificatore della persona. |
| `personKey.sourceID` |  | Identificatore della persona nel sistema connesso. |
| `personKey.sourceType` |  | Nome del prodotto connesso. |
| `personKey.sourceInstanceID` |  | Identificatore dell&#39;ambiente [!DNL Experience Platform] o dell&#39;account connesso. |
| `personKey.sourceKey` |  | Identificatore completo della persona utilizzato per far corrispondere i record correlati. |
| `web.webPageDetails.webPageKey.sourceID` |  | ID risorsa della pagina. |
| `web.webPageDetails.webPageKey.sourceType` |  | Nome del prodotto connesso. |
| `web.webPageDetails.webPageKey.sourceInstanceID` |  | ID istanza. |
| `web.webPageDetails.webPageKey.sourceKey` |  | Identificatore pagina completo. |
| `web.webPageDetails.name` |  | Nome pagina. |
| `web.webPageDetails.URL` |  | URL della pagina. |
| `web.webPageDetails.queryParameters` |  | Informazioni aggiuntive incluse in un indirizzo web. |
| `web.webPageDetails.webPageID` |  | ID pagina. |
| `environment.browserDetails.userAgent` |  | Informazioni sul browser o sul client e-mail. |
| `web.webReferrer.URL` |  | URL referrer. |

### Collegamento Web selezionato (`web.webinteraction.linkClicks`)

| Nome campo | Relazione | Cosa ti dice |
|------------|-------------|-------------|
| `_id` | ID record | Identificatore dell’attività. |
| `eventType` |  | `web.webinteraction.linkClicks`. |
| `timestamp` |  | Quando si è verificata l’attività. |
| `personID` | Corrisponde a `AJOB2B-1_5_1-person` (`personID`) | Identificatore della persona. |
| `personKey.sourceID` |  | Identificatore della persona nel sistema connesso. |
| `personKey.sourceType` |  | Nome del prodotto connesso. |
| `personKey.sourceInstanceID` |  | Identificatore dell&#39;ambiente [!DNL Experience Platform] o dell&#39;account connesso. |
| `personKey.sourceKey` |  | Identificatore completo della persona utilizzato per far corrispondere i record correlati. |
| `web.webInteraction.webInteractionKey.sourceID` |  | ID risorsa dell’interazione. |
| `web.webInteraction.webInteractionKey.sourceType` |  | Nome del prodotto connesso. |
| `web.webInteraction.webInteractionKey.sourceInstanceID` |  | ID istanza. |
| `web.webInteraction.webInteractionKey.sourceKey` |  | Identificatore di interazione completo. |
| `web.webInteraction.linkID` |  | ID collegamento. |
| `web.webInteraction.linkURL` |  | URL di destinazione. |
| `web.webPageDetails.queryParameters` |  | Informazioni aggiuntive incluse in un indirizzo web. |
| `web.webPageDetails.webPageID` |  | ID pagina. |
| `environment.browserDetails.userAgent` |  | Informazioni sul browser o sul client e-mail. |
| `web.webReferrer.URL` |  | URL referrer. |

### Modulo inviato (`web.formFilledOut`)

| Nome campo | Relazione | Cosa ti dice |
|------------|-------------|-------------|
| `_id` | ID record | Identificatore dell’attività. |
| `eventType` |  | `web.formFilledOut`. |
| `timestamp` |  | Quando si è verificata l’attività. |
| `personID` | Corrisponde a `AJOB2B-1_5_1-person` (`personID`) | Identificatore della persona. |
| `personKey.sourceID` |  | Identificatore della persona nel sistema connesso. |
| `personKey.sourceType` |  | Nome del prodotto connesso. |
| `personKey.sourceInstanceID` |  | Identificatore dell&#39;ambiente [!DNL Experience Platform] o dell&#39;account connesso. |
| `personKey.sourceKey` |  | Identificatore completo della persona utilizzato per far corrispondere i record correlati. |
| `web.fillOutForm.webFormKey.sourceID` |  | ID risorsa modulo. |
| `web.fillOutForm.webFormKey.sourceType` |  | Nome del prodotto connesso. |
| `web.fillOutForm.webFormKey.sourceInstanceID` |  | ID istanza. |
| `web.fillOutForm.webFormKey.sourceKey` |  | Identificatore modulo completo. |
| `web.fillOutForm.webFormID` |  | ID modulo. |
| `web.fillOutForm.webFormName` |  | Nome modulo. |
| `web.webPageDetails.queryParameters` |  | Informazioni aggiuntive incluse in un indirizzo web. |
| `web.webPageDetails.webPageID` |  | ID pagina. |
| `environment.browserDetails.userAgent` |  | Informazioni sul browser o sul client e-mail. |
| `web.webReferrer.URL` |  | URL referrer. |

### Momento di interesse registrato (`leadOperation.interestingMoment`)

| Nome campo | Relazione | Cosa ti dice |
|------------|-------------|-------------|
| `_id` | ID record | Identificatore dell’attività. |
| `eventType` |  | `leadOperation.interestingMoment`. |
| `timestamp` |  | Quando si è verificata l’attività. |
| `personID` | Corrisponde a `AJOB2B-1_5_1-person` (`personID`) | Identificatore della persona. |
| `personKey.sourceID` |  | Identificatore della persona nel sistema connesso. |
| `personKey.sourceType` |  | Nome del prodotto connesso. |
| `personKey.sourceInstanceID` |  | Identificatore dell&#39;ambiente [!DNL Experience Platform] o dell&#39;account connesso. |
| `personKey.sourceKey` |  | Identificatore completo della persona utilizzato per far corrispondere i record correlati. |
| `leadOperation.interestingMoment.date` |  | Data/ora del momento. |
| `leadOperation.interestingMoment.description` |  | Descrizione |
| `leadOperation.interestingMoment.source` |  | Nome del prodotto o della campagna correlata. |
| `leadOperation.interestingMoment.type` |  | Digita l’etichetta. |
| `_experience.journeyOrchestration.stepEvents.journeyID` | Corrisponde a `AJOB2B-1_5_4-person_journey` (`_id`) | ID percorso (se attribuito). |
| `_experience.journeyOrchestration.stepEvents.nodeID` | Corrisponde a `AJOB2B-1_5_4-person_journey_node` (`_id`) | ID nodo percorso (se attribuito). |

## `AJOB2B-1_5_4-journey_node`

Ogni record descrive un passaggio di percorso, il percorso a cui appartiene e il tipo di passaggio. Gli stessi passaggi possono essere visualizzati nei set di dati dei passaggi account e persona-percorso. Abbina `journeyID` al percorso appropriato. Non contare un passaggio più di una volta perché viene visualizzato in diversi set di dati.

**Formato:** Formato record correlati

| Nome campo | Relazione | Cosa ti dice |
|------------|-------------|-------------|
| `_id` | ID record | ID del record del nodo (utilizza il valore completo). |
| `journeyID` | Corrisponde a `AJOB2B-1_5_4-account_journey` o `AJOB2B-1_5_4-person_journey` (`_id`) | Identificatore del percorso padre. |
| `nodeType` |  | Tipo di passaggio di percorso, ad esempio inizio, fine, attesa o decisione. |
| `isDeleted` |  | Indica se il record è contrassegnato come eliminato. |
| `lastUpdatedDate` |  | Ora ultima modifica. |

## `AJOB2B-1_5_4-account_relational`

Ogni record descrive un account, inclusi i relativi campi personalizzati, quali dettagli sull&#39;organizzazione, ubicazione, dimensioni e ricavi. Utilizzare queste informazioni per aggiungere il contesto dell&#39;account ai report dei gruppi di acquisto e dei percorsi.

**Formato:** Formato record correlati

| Nome campo | Relazione | Cosa ti dice |
|------------|-------------|-------------|
| `_id` | ID record | ID del record dell’account (utilizza il valore completo). |
| `accountName` |  | Nome account. |
| `industry` |  | Classificazione di settore. |
| `country` |  | Paese. |
| `sicCode` |  | Codice di classificazione industriale standard. |
| `domainName` |  | Dominio web primario. |
| `primaryEmailDomain` |  | Dominio e-mail primario. |
| `street` |  | Indirizzo. |
| `city` |  | Città. |
| `state` |  | Stato o regione. |
| `postalCode` |  | CAP. |
| `region` |  | Area geografica. |
| `phoneNumber` |  | Numero di telefono |
| `logoUrl` |  | URL del logo dell’account. |
| `annualRevenue` |  | Entrate annuali. |
| `numberOfEmployees` |  | Numero di dipendenti. |
| `createdDate` |  | Data di creazione del record. |
| `sourceType` |  | Nome del sistema connesso che identifica l&#39;account. |
| `sourceInstanceID` |  | Identificatore dell&#39;organizzazione o dell&#39;account nel sistema connesso. |
| `sourceID` |  | Identificatore account nel sistema connesso. |
| `customAttributes` |  | Nomi e valori di campi personalizzati memorizzati insieme come testo. |
| `isDeleted` |  | Indica se il record è contrassegnato come eliminato. |
| `lastUpdatedDate` |  | Ora ultima modifica. |

## `AJOB2B-1_5_4-person_relational`

Ogni record descrive una persona, incluse le informazioni di contatto, i dettagli del processo, gli identificatori e i campi personalizzati. Utilizzala per aggiungere informazioni sulla persona ai rapporti su appartenenza, percorso e attività.

**Formato:** Formato record correlati

| Nome campo | Relazione | Cosa ti dice |
|------------|-------------|-------------|
| `_id` | ID record | Identificatore completo della persona utilizzato per far corrispondere i record correlati. |
| `email` |  | Indirizzo e-mail. |
| `firstName` |  | Nome. |
| `middleName` |  | Secondo nome. |
| `lastName` |  | Cognome. |
| `jobTitle` |  | Qualifica. |
| `personType` |  | Tipo di persona: contatto, potenziale cliente potenziale o lead in sospeso. |
| `isLead` |  | Se la persona è un lead. |
| `isAnonymous` |  | Indica se la persona è anonima. |
| `salutation` |  | Saluto o onorifico. |
| `phone` |  | Numero di telefono principale. |
| `mobile` |  | Numero di telefono cellulare. |
| `sourceType` |  | Nome del sistema connesso che identifica la persona, ad esempio [!DNL Marketo Engage]. |
| `sourceInstanceID` |  | Identificatore dell&#39;organizzazione o dell&#39;account nel sistema connesso. |
| `sourceID` |  | Identificatore della persona nel sistema connesso. |
| `identityNamespace` |  | Etichetta che identifica il tipo di identificatore persona aggiuntivo. |
| `identityValue` |  | Valore dell’identità secondaria. |
| `customAttributes` |  | Nomi e valori di campi personalizzati memorizzati insieme come testo. |
| `isDeleted` |  | Indica se il record è contrassegnato come eliminato. |
| `lastUpdatedDate` |  | Ora ultima modifica. |

## `AJOB2B-1_5_4-account_person`

Ogni record collega un profilo account a un profilo persona. Utilizzala per creare rapporti tra i set di dati del profilo account e persona.

**Formato:** Formato record correlati

| Nome campo | Relazione | Cosa ti dice |
|------------|-------------|-------------|
| `_id` | ID record | ID record relazione account-persona (utilizzare il valore completo). |
| `accountID` | Corrisponde a `AJOB2B-1_5_4-account_relational` (`_id`) | Identificatore account completo (riferimenti `account_relational._id`). |
| `personID` | Corrisponde a `AJOB2B-1_5_4-person_relational` (`_id`) | Identificatore persona completo (riferimenti `person_relational._id`). |
| `createdDate` |  | Quando è stata creata la relazione account-persona. |
| `isDeleted` |  | Indica se il record è contrassegnato come eliminato. |
| `lastUpdatedDate` |  | Ora ultima modifica. |

## `AJOB2B-1_5_4-person_event_relational`

Ogni record descrive un’attività della persona supportata, ad esempio la visualizzazione di una pagina web, l’interazione con un’e-mail o lo spostamento all’interno di un percorso. Utilizza `eventType` e `activityTypeID` per capire cosa è successo. Vengono compilati solo i dettagli relativi a quel tipo di attività.

**Formato:** Formato record correlati

Il seguente elenco di campi copre tutti i tipi di attività supportati. Un singolo record contiene solo i dettagli applicabili alla sua attività.

>[!NOTE]
>
>**Disponibilità:** alcune attività potrebbero avere un `_id` vuoto. Non presumere che ogni attività abbia un identificatore di record utilizzabile. Il set di dati non è una garanzia di una cronologia completa delle attività.

I dettagli del percorso (`journeyID`, `journeyNodeID`, `journeyStepID` e campi simili) vengono forniti per le attività del percorso (`person.journeyAdd`, `person.journeyRemove`, `person.journeyStart`, `person.journeyEnd`, `person.journeyNodeTransition`, `person.journeySplitNode`) e per `person.attributeChanged` attività associate a un passaggio di percorso &quot;Aggiorna profilo persona&quot;.

I campi di modifica degli attributi (`attributeName`, `attributeID`, `attributeNewValue`, `attributeOldValue`, `attributeChangeReason`) sono compilati solo per `person.attributeChanged`.

| Nome campo | Relazione | Cosa ti dice |
|------------|-------------|-------------|
| `_id` | ID record | Identificatore dell’attività, se disponibile. |
| `timestamp` |  | Quando si è verificata l’attività. |
| `eventType` |  | Etichetta attività. Valori: `web.webpagedetails.pageViews`, `web.formFilledOut`, `web.webinteraction.linkClicks`, `directMarketing.emailSent`, `directMarketing.emailDelivered`, `directMarketing.emailBounced`, `directMarketing.emailBouncedSoft`, `directMarketing.emailUnsubscribed`, `directMarketing.emailOpened`, `directMarketing.emailClicked`, `leadOperation.interestingMoment`, `person.attributeChanged`, `person.journeyAdd`, `person.journeyRemove`, `person.journeyStart`, `person.journeyEnd`, `person.journeyNodeTransition`, `person.journeySplitNode`. |
| `activityTypeID` |  | Codice attività. Utilizzala con `eventType` per distinguere le attività che condividono la stessa etichetta evento. |
| `personID` | Corrisponde a `AJOB2B-1_5_4-person_relational` (`_id`) | Identificatore completo della persona utilizzato per associare l’attività a un record della persona. |
| `journeyID` | Corrisponde a `AJOB2B-1_5_4-person_journey` (`_id`) | Identificatore percorso completo. Vuoto per le attività non associate a un percorso. |
| `journeyNodeID` | Corrisponde a `AJOB2B-1_5_4-person_journey_node` (`_id`) | Identificatore completo per fase del percorso. Vuoto per le attività non associate a un percorso. |
| `previousJourneyNodeID` | Corrisponde a `AJOB2B-1_5_4-person_journey_node` (`_id`) | Nodo percorso precedente (popolato per `person.journeyNodeTransition` e `person.journeySplitNode`). |
| `newJourneyNodeID` | Corrisponde a `AJOB2B-1_5_4-person_journey_node` (`_id`) | ID nodo percorso di destinazione (`person.journeyNodeTransition` e `person.journeySplitNode`). In genere è uguale a `journeyNodeID`. |
| `journeyStepID` |  | Identificatore della fase del percorso associata all’attività. |
| `journeyChoiceNumber` |  | Numero di scelta divisa per `person.journeySplitNode`. Registrato come numero intero. |
| `journeyEntryCount` |  | Numero di volte in cui questa persona è entrata nel percorso (popolato in eventi di aggiunta/avvio del percorso). Registrato come numero intero. |
| `journeyProgramID` | Questa guida non contiene set di dati separati per programmi di marketing | Identificatore del programma di marketing associato all’attività di percorso. |
| `activitySource` |  | Nome del prodotto o dell’azione associata all’attività. |
| `campaignID` |  | ID campagna [!DNL Marketo Engage] quando l&#39;attività è attribuita a una campagna. |
| `attributeName` |  | Nome del campo modificato (`person.attributeChanged` only). |
| `attributeID` |  | Identificatore del campo modificato (`person.attributeChanged` only). |
| `attributeNewValue` |  | Nuovo valore di campo, registrato come testo (`person.attributeChanged`). |
| `attributeOldValue` |  | Valore campo precedente, registrato come testo (`person.attributeChanged`). |
| `attributeChangeReason` |  | Etichetta del motivo della modifica (`person.attributeChanged` only). |
| `assetID` |  | Identificatore del contenuto dell’e-mail, della pagina o del modulo correlati. |
| `assetName` |  | Nome del contenuto correlato. |
| `recipientEmail` |  | Indirizzo e-mail del destinatario, se disponibile. Compilato solo per i codici attività **27** (mancati recapiti non permanenti) e **48** (mancati recapiti non permanenti e-mail di vendita); vuoto per altre attività e-mail. Per tali attività, cercare il record persona utilizzando `personID`. `assetName` identifica il contenuto dell&#39;e-mail, non l&#39;indirizzo del destinatario. |
| `bouncedCode` |  | Codice categoria di mancato recapito (solo emailBounce/emailBounceSoft). |
| `bouncedDetails` |  | Motivo dettagliato del mancato recapito (solo e-mailRimbalzato/e-mailRimbalzatoSoft). |
| `isMobileDevice` |  | Indica se un dispositivo mobile è stato registrato per l’apertura o il clic di un’e-mail. |
| `deviceModel` |  | Modello del dispositivo (solo e-mailOpened/e-mailClicked). |
| `operatingSystem` |  | Sistema operativo (solo e-mailOpened/e-mailClicked). |
| `userAgent` |  | Informazioni su browser o client e-mail, per aperture di e-mail, clic e attività web. |
| `clickedLinkUrl` |  | URL collegamento e-mail selezionato (solo e-mailSelezionato). |
| `webPageUrl` |  | URL della pagina Web (`web.webpagedetails.pageViews` only). |
| `queryParameters` |  | Informazioni aggiuntive in un indirizzo web, per le visualizzazioni di pagina, l’invio di moduli o i clic sui collegamenti web. |
| `webPageID` |  | ID pagina Web [!DNL Marketo Engage] (pageViews, formFilledOut, linkClicks). |
| `referrerUrl` |  | URL referente (pageViews, formFilledOut, linkClicks). |
| `formID` |  | ID modulo [!DNL Marketo Engage] (solo `web.formFilledOut`). |
| `linkID` |  | ID collegamento [!DNL Marketo Engage] (solo `web.webinteraction.linkClicks`). |
| `interestingMomentDate` |  | Data momento (`leadOperation.interestingMoment` only). |
| `interestingMomentDescription` |  | Descrizione a testo libero (solo interessantiMoment). |
| `interestingMomentSource` |  | Prodotto o campagna correlata (solo interessanteMoment). |
| `interestingMomentType` |  | Categoria/tipo (solo interessantiMoment). |
| `isDeleted` |  | Indica se il record è contrassegnato come eliminato. |
| `lastUpdatedDate` |  | Ora ultima modifica. |

### Riferimento campo per tipo di attività

Le tabelle seguenti mostrano i dettagli applicabili a ogni attività. Gli altri dettagli sono vuoti. Alcune attività condividono la stessa etichetta `eventType`: i codici 8 e 48 utilizzano entrambi `directMarketing.emailBounced`. Utilizza `activityTypeID` per distinguerli.

#### Pagina Web visualizzata (`web.webpagedetails.pageViews`) (tipo di attività 1)

| Nome campo | Relazione | Cosa ti dice |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | ID record: `_id`; `personID` corrisponde a `AJOB2B-1_5_4-person_relational` (`_id`) | Campi comuni. |
| `assetID` |  | ID pagina. |
| `assetName` |  | Nome pagina. |
| `webPageUrl` |  | URL della pagina. |
| `queryParameters` |  | Informazioni aggiuntive incluse in un indirizzo web. |
| `webPageID` |  | ID pagina Web [!DNL Marketo Engage]. |
| `referrerUrl` |  | URL referrer. |
| `userAgent` |  | Informazioni sul browser o sul client e-mail. |
| `isDeleted`, `lastUpdatedDate` |  | Campi comuni. |

#### Modulo inviato (`web.formFilledOut`) (tipo di attività 2)

| Nome campo | Relazione | Cosa ti dice |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | ID record: `_id`; `personID` corrisponde a `AJOB2B-1_5_4-person_relational` (`_id`) | Campi comuni. |
| `assetID` |  | ID modulo. |
| `assetName` |  | Nome modulo. |
| `formID` |  | ID modulo [!DNL Marketo Engage]. |
| `queryParameters` |  | Informazioni aggiuntive incluse in un indirizzo web. |
| `webPageID` |  | ID pagina Web [!DNL Marketo Engage]. |
| `referrerUrl` |  | URL referrer. |
| `userAgent` |  | Informazioni sul browser o sul client e-mail. |
| `isDeleted`, `lastUpdatedDate` |  | Campi comuni. |

#### Collegamento Web su cui è stato fatto clic (`web.webinteraction.linkClicks`) (tipo di attività 3)

| Nome campo | Relazione | Cosa ti dice |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | ID record: `_id`; `personID` corrisponde a `AJOB2B-1_5_4-person_relational` (`_id`) | Campi comuni. |
| `assetID` |  | ID interazione/collegamento. |
| `assetName` |  | URL di destinazione. |
| `linkID` |  | ID collegamento [!DNL Marketo Engage]. |
| `queryParameters` |  | Informazioni aggiuntive incluse in un indirizzo web. |
| `webPageID` |  | ID pagina Web [!DNL Marketo Engage]. |
| `referrerUrl` |  | URL referrer. |
| `userAgent` |  | Informazioni sul browser o sul client e-mail. |
| `isDeleted`, `lastUpdatedDate` |  | Campi comuni. |

#### E-mail inviata (`directMarketing.emailSent`) (tipi di attività 6, 39)

| Nome campo | Relazione | Cosa ti dice |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | ID record: `_id`; `personID` corrisponde a `AJOB2B-1_5_4-person_relational` (`_id`) | Campi comuni. |
| `assetID` |  | ID mailing. |
| `assetName` |  | Nome mailing. |
| `campaignID` |  | ID [!DNL Marketo Engage] della campagna, quando attribuito alla campagna. |
| `isDeleted`, `lastUpdatedDate` |  | Campi comuni. |

#### E-mail consegnata (`directMarketing.emailDelivered`) (tipi di attività 7, 45)

| Nome campo | Relazione | Cosa ti dice |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | ID record: `_id`; `personID` corrisponde a `AJOB2B-1_5_4-person_relational` (`_id`) | Campi comuni. |
| `assetID` |  | ID mailing. |
| `assetName` |  | Nome mailing. |
| `campaignID` |  | ID [!DNL Marketo Engage] della campagna, quando attribuito alla campagna. |
| `isDeleted`, `lastUpdatedDate` |  | Campi comuni. |

#### Annullamento iscrizione e-mail (`directMarketing.emailUnsubscribed`) (tipo di attività 9)

| Nome campo | Relazione | Cosa ti dice |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | ID record: `_id`; `personID` corrisponde a `AJOB2B-1_5_4-person_relational` (`_id`) | Campi comuni. |
| `assetID` |  | ID mailing. |
| `assetName` |  | Nome mailing. |
| `campaignID` |  | ID [!DNL Marketo Engage] della campagna, quando attribuito alla campagna. |
| `isDeleted`, `lastUpdatedDate` |  | Campi comuni. |

#### E-mail aperta (`directMarketing.emailOpened`) (tipi di attività 10, 40)

| Nome campo | Relazione | Cosa ti dice |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | ID record: `_id`; `personID` corrisponde a `AJOB2B-1_5_4-person_relational` (`_id`) | Campi comuni. |
| `assetID` |  | ID mailing. |
| `assetName` |  | Nome mailing. |
| `isMobileDevice` |  | Se un dispositivo mobile è stato registrato per l&#39;attività. |
| `deviceModel` |  | Modello del dispositivo. |
| `operatingSystem` |  | Sistema operativo. |
| `userAgent` |  | Informazioni sul browser o sul client e-mail. |
| `campaignID` |  | ID [!DNL Marketo Engage] della campagna, quando attribuito alla campagna. |
| `isDeleted`, `lastUpdatedDate` |  | Campi comuni. |

#### Clic sul collegamento e-mail eseguito (`directMarketing.emailClicked`) (tipi di attività 11, 41)

| Nome campo | Relazione | Cosa ti dice |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | ID record: `_id`; `personID` corrisponde a `AJOB2B-1_5_4-person_relational` (`_id`) | Campi comuni. |
| `assetID` |  | ID mailing. |
| `assetName` |  | Nome mailing. |
| `clickedLinkUrl` |  | URL collegamento selezionato. |
| `isMobileDevice` |  | Se un dispositivo mobile è stato registrato per l&#39;attività. |
| `deviceModel` |  | Modello del dispositivo. |
| `operatingSystem` |  | Sistema operativo. |
| `userAgent` |  | Informazioni sul browser o sul client e-mail. |
| `campaignID` |  | ID [!DNL Marketo Engage] della campagna, quando attribuito alla campagna. |
| `isDeleted`, `lastUpdatedDate` |  | Campi comuni. |

#### E-mail non recapitate (`directMarketing.emailBounced`): messaggio non recapitato (tipo di attività 8)

| Nome campo | Relazione | Cosa ti dice |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | ID record: `_id`; `personID` corrisponde a `AJOB2B-1_5_4-person_relational` (`_id`) | Campi comuni. |
| `assetID` |  | ID mailing. |
| `assetName` |  | Nome mailing. |
| `bouncedCode` |  | Codice categoria per mancato recapito. |
| `bouncedDetails` |  | Motivo dettagliato del mancato recapito. |
| `campaignID` |  | ID [!DNL Marketo Engage] della campagna, quando attribuito alla campagna. |
| `isDeleted`, `lastUpdatedDate` |  | Campi comuni. |

Questa attività condivide l&#39;etichetta `directMarketing.emailBounced` con il codice attività 48, ma `recipientEmail` è vuoto per il codice 8. Utilizza `activityTypeID` per distinguere i due.

#### E-mail non recapitate (`directMarketing.emailBounced`): messaggio e-mail di vendita non recapitato (tipo di attività 48)

| Nome campo | Relazione | Cosa ti dice |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | ID record: `_id`; `personID` corrisponde a `AJOB2B-1_5_4-person_relational` (`_id`) | Campi comuni. |
| `assetID` |  | ID mailing. |
| `assetName` |  | Nome mailing. |
| `recipientEmail` |  | Indirizzo e-mail del destinatario. |
| `bouncedCode` |  | Codice categoria per mancato recapito. |
| `bouncedDetails` |  | Motivo dettagliato del mancato recapito. |
| `campaignID` |  | ID [!DNL Marketo Engage] della campagna, quando attribuito alla campagna. |
| `isDeleted`, `lastUpdatedDate` |  | Campi comuni. |

#### E-mail non recapitate (`directMarketing.emailBouncedSoft`) (tipo di attività 27)

| Nome campo | Relazione | Cosa ti dice |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | ID record: `_id`; `personID` corrisponde a `AJOB2B-1_5_4-person_relational` (`_id`) | Campi comuni. |
| `assetID` |  | ID mailing. |
| `assetName` |  | Nome mailing. |
| `recipientEmail` |  | Indirizzo e-mail del destinatario. |
| `bouncedCode` |  | Codice categoria per mancato recapito. |
| `bouncedDetails` |  | Motivo dettagliato del mancato recapito. |
| `campaignID` |  | ID [!DNL Marketo Engage] della campagna, quando attribuito alla campagna. |
| `isDeleted`, `lastUpdatedDate` |  | Campi comuni. |

#### Momento di interesse registrato (`leadOperation.interestingMoment`) (tipo di attività 46)

| Nome campo | Relazione | Cosa ti dice |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | ID record: `_id`; `personID` corrisponde a `AJOB2B-1_5_4-person_relational` (`_id`) | Campi comuni. |
| `interestingMomentDate` |  | Data/ora del momento. |
| `interestingMomentDescription` |  | Descrizione a testo libero. |
| `interestingMomentSource` |  | Nome del prodotto o della campagna correlata. |
| `interestingMomentType` |  | Digita l’etichetta. |
| `isDeleted`, `lastUpdatedDate` |  | Campi comuni. |

`assetID` e `assetName` non sono compilati per questo tipo di attività.

#### Campo della persona modificato (`person.attributeChanged`) (tipo di attività 13)

Incluso solo quando la modifica è associata a un percorso, ad esempio un passaggio &quot;Aggiorna profilo persona&quot;. Le modifiche all&#39;esterno di un percorso non sono incluse.

| Nome campo | Relazione | Cosa ti dice |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | ID record: `_id`; `personID` corrisponde a `AJOB2B-1_5_4-person_relational` (`_id`) | Campi comuni. |
| `attributeName` |  | Nome del campo che è stato modificato. |
| `attributeID` |  | Identificatore del campo che è stato modificato. |
| `attributeNewValue` |  | Nuovo valore di campo, registrato come testo. |
| `attributeOldValue` |  | Valore di campo precedente, registrato come testo. |
| `attributeChangeReason` |  | Etichetta del motivo della modifica. |
| `journeyID` | Corrisponde a `AJOB2B-1_5_4-person_journey` (`_id`) | Identificatore percorso. |
| `journeyNodeID` | Corrisponde a `AJOB2B-1_5_4-person_journey_node` (`_id`) | Identificatore del nodo del percorso. |
| `journeyStepID` |  | Identificatore del passaggio di percorso. |
| `journeyProgramID` | Questa guida non contiene set di dati separati per programmi di marketing | ID programma percorso. |
| `activitySource` |  | Prodotto o azione associato all’attività. |
| `isDeleted`, `lastUpdatedDate` |  | Campi comuni. |

#### Persona aggiunta o avviata in un percorso (`person.journeyAdd`, `person.journeyStart`) (tipi di attività 182, 184)

| Nome campo | Relazione | Cosa ti dice |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | ID record: `_id`; `personID` corrisponde a `AJOB2B-1_5_4-person_relational` (`_id`) | Campi comuni. |
| `journeyID` | Corrisponde a `AJOB2B-1_5_4-person_journey` (`_id`) | Identificatore percorso. |
| `journeyNodeID` | Corrisponde a `AJOB2B-1_5_4-person_journey_node` (`_id`) | Identificatore del nodo del percorso. |
| `journeyStepID` |  | Identificatore del passaggio di percorso. |
| `journeyEntryCount` |  | Numero di volte in cui questa persona è entrata nel percorso. |
| `journeyProgramID` | Questa guida non contiene set di dati separati per programmi di marketing | ID programma percorso. |
| `activitySource` |  | Prodotto o azione associato all’attività. |
| `isDeleted`, `lastUpdatedDate` |  | Campi comuni. |

#### Persona rimossa da o terminata da un percorso (`person.journeyRemove`, `person.journeyEnd`) (tipi di attività 183, 185)

| Nome campo | Relazione | Cosa ti dice |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | ID record: `_id`; `personID` corrisponde a `AJOB2B-1_5_4-person_relational` (`_id`) | Campi comuni. |
| `journeyID` | Corrisponde a `AJOB2B-1_5_4-person_journey` (`_id`) | Identificatore percorso. |
| `journeyNodeID` | Corrisponde a `AJOB2B-1_5_4-person_journey_node` (`_id`) | Identificatore del nodo del percorso. |
| `journeyStepID` |  | Identificatore del passaggio di percorso. |
| `journeyProgramID` | Questa guida non contiene set di dati separati per programmi di marketing | ID programma percorso. |
| `activitySource` |  | Prodotto o azione associato all’attività. |
| `isDeleted`, `lastUpdatedDate` |  | Campi comuni. |

#### La persona ha seguito un ramo del percorso (`person.journeySplitNode`) (tipo di attività 186)

| Nome campo | Relazione | Cosa ti dice |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | ID record: `_id`; `personID` corrisponde a `AJOB2B-1_5_4-person_relational` (`_id`) | Campi comuni. |
| `journeyID` | Corrisponde a `AJOB2B-1_5_4-person_journey` (`_id`) | Identificatore percorso. |
| `journeyNodeID` | Corrisponde a `AJOB2B-1_5_4-person_journey_node` (`_id`) | Identificatore del nodo di percorso (nodo suddiviso). |
| `previousJourneyNodeID` | Corrisponde a `AJOB2B-1_5_4-person_journey_node` (`_id`) | Nodo in cui si trovava la persona prima della divisione. |
| `newJourneyNodeID` | Corrisponde a `AJOB2B-1_5_4-person_journey_node` (`_id`) | Nodo in cui la persona è stata spostata (in genere è uguale a `journeyNodeID`). |
| `journeyStepID` |  | Identificatore del passaggio di percorso. |
| `journeyChoiceNumber` |  | Quale ramo della divisione è stato acquisito. |
| `journeyProgramID` | Questa guida non contiene set di dati separati per programmi di marketing | ID programma percorso. |
| `activitySource` |  | Prodotto o azione associato all’attività. |
| `isDeleted`, `lastUpdatedDate` |  | Campi comuni. |

#### Persona spostata tra i passaggi del percorso (`person.journeyNodeTransition`) (tipo di attività 600)

| Nome campo | Relazione | Cosa ti dice |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | ID record: `_id`; `personID` corrisponde a `AJOB2B-1_5_4-person_relational` (`_id`) | Campi comuni. |
| `journeyID` | Corrisponde a `AJOB2B-1_5_4-person_journey` (`_id`) | Identificatore percorso. |
| `journeyNodeID` | Corrisponde a `AJOB2B-1_5_4-person_journey_node` (`_id`) | Identificatore del nodo del percorso corrente. |
| `previousJourneyNodeID` | Corrisponde a `AJOB2B-1_5_4-person_journey_node` (`_id`) | Nodo da cui è avvenuta la transizione della persona. |
| `newJourneyNodeID` | Corrisponde a `AJOB2B-1_5_4-person_journey_node` (`_id`) | Il nodo a cui è passata la persona (in genere è uguale a `journeyNodeID`). |
| `journeyStepID` |  | Identificatore del passaggio di percorso. |
| `journeyProgramID` | Questa guida non contiene set di dati separati per programmi di marketing | ID programma percorso. |
| `activitySource` |  | Prodotto o azione associato all’attività. |
| `isDeleted`, `lastUpdatedDate` |  | Campi comuni. |

## Set di dati di proprietà del cliente {#customer-owned-datasets}

La tua organizzazione può utilizzare i propri [!DNL Experience Platform] set di dati per account o persone. Una volta configurata, [!DNL Adobe Journey Optimizer B2B Edition] può aggiungere informazioni a tali set di dati anziché creare un altro set di dati account o persona.

I nomi e i campi disponibili dipendono dalla configurazione dell’organizzazione. Utilizza l’identificatore account o persona configurato per riconoscere i record corrispondenti. L&#39;utilizzo di record in questi set di dati non li rende automaticamente disponibili per i tipi di pubblico; la disponibilità dipende dalla configurazione di [!DNL Experience Platform].
