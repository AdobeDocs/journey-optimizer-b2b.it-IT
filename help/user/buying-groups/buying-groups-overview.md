---
title: Gruppi acquisti
description: Scopri come i gruppi acquisti in Journey Optimizer B2B Edition possono aumentare l’efficacia del marketing tramite identificazione e targeting dei membri dei tuoi elenchi di account.
feature: Buying Groups
role: User
exl-id: ddcd7b62-6a76-4f5e-b6d3-a20944ca8332
source-git-commit: a2917ea8c389c35129a77d427528051be499addf
workflow-type: tm+mt
source-wordcount: '2170'
ht-degree: 98%

---


# Gruppi acquisti

Per le attività di vendita e marketing B2B, gli account sono fondamentali per qualsiasi strategia. A ogni account è associato un gruppo di persone, che possono essere dipendenti dell’account o collaboratori esterni che utilizzano l’account. Gli account sono gerarchici e prodotti diversi possono essere venduti a diversi livelli nella gerarchia. Ad esempio, Adobe Experience Platform potrebbe essere venduto a livello aziendale a un account di livello dirigenziale. Inoltre, Adobe Photoshop potrebbe essere venduto a un account che rappresenta una divisione o un reparto all’interno di un’organizzazione, ad esempio un reparto progettazione all’interno di un’azienda più grande.

![Diagramma ruoli account](assets/account-roles-diagram.png){width="800"}

Nell’account potrebbe essere presente un sottoinsieme di persone che costituiscono il _gruppo acquisti_. Queste persone alla fine prendono la decisione di acquisto, quindi hanno bisogno di particolare attenzione da parte del marketer e potrebbero aver bisogno di informazioni diverse da quelle delle altre persone associate all’account. I gruppi acquisti possono comprendere un gruppo diverso di persone per diverse linee di prodotti o offerte. Ad esempio, l’approvazione di un acquisto di un prodotto per la sicurezza informatica può richiedere un Chief Information Officer o un Chief Security Officer, e un rappresentante del reparto legale. Per un prodotto di tracciamento dei bug si possono includere tra i membri del gruppo acquisti un VP of Engineering e un direttore IT.

![Video](../../assets/do-not-localize/icon-video.svg){width="30"} [Guarda la panoramica video](#overview-video)

## Componenti principali

Puoi aumentare l’efficacia del marketing in Journey Optimizer B2B Edition creando gruppi acquisti che comprendano specifici membri dagli elenchi dei tuoi account target in base alle soluzioni gestite dai team di vendita. Prima di iniziare a creare i gruppi acquisti con il team di marketing, accertati di aver definito i componenti principali. Questi componenti sono fondamentali per raggiungere gli obiettivi e le finalità aziendali.

| Componente | Finalità |
| --------- | ------- |
| Soluzione di interesse | Questo componente fornisce la risposta alle domande seguenti: <ul><li>In qualità di organizzazione di marketing, cosa stai vendendo?</li><li>A quale prodotto o raccolta di prodotti è orientata la vendita?</li></ul>  **Esempio::_** cross-selling del nuovo prodotto X a clientela esistente |
| Pubblico dell’account | Questo componente fornisce la risposta alle domande seguenti: <ul><li>A chi stai vendendo?</li><li>Per quale elenco degli account intendi eseguire il targeting?</li></ul> **Esempio::_** segmento di account definito da account con prodotto Y per ricavi superiori a 1 milione |
| Modelli di ruoli del gruppo acquisti | Questo componente fornisce la risposta alle domande seguenti: <ul><li>Per quali ruoli intendi eseguire il targeting?</li><li>Quale insieme di regole viene utilizzato per determinare chi è assegnato ai ruoli del gruppo acquisti?</li></ul>  **Esempio::_** assegna una persona con titolo CMO al ruolo Responsabile delle decisioni |
| Fasi del gruppo acquisti | (Facoltativo) Questo componente fornisce la risposta alla domanda: In che modo il gruppo acquisti segue il percorso del successo o del fallimento? |

## Assegnazione membro

Esistono tre modi per assegnare o rimuovere i membri da un gruppo acquisti. I metodi di aggiunta e rimozione sono descritti ed elencati di seguito in ordine di precedenza. Il metodo più in alto ha la precedenza e non può essere sostituito da uno metodo di livello inferiore.

1. **_Azione manuale_**: azione manuale di aggiunta o rimozione di un membro eseguita da un utente del reparto vendite per il gruppo acquisti
2. **_Azione percorso_**: [nodi delle azioni del percorso per l’iscrizione al gruppo acquisti](../journeys/action-nodes.md#add-a-people-based-action) (_Assegna al gruppo acquisti_ o _Rimuovi dal gruppo acquisti_)
3. **_Processi di sistema_**: [creazione](../buying-groups/buying-groups-create.md#buying-group-creation-jobs) del gruppo acquisti e processi di manutenzione.

Affinché l’assegnazione dei membri in un gruppo acquisti non venga ignorata in modo errato, l’elenco rispecchia l’ordine di precedenza seguito nel sistema, per garantire l’assegnazione accurata dei membri. Ad esempio, se un utente del reparto vendite aggiunge manualmente un membro al gruppo acquisti, nessun processo di manutenzione dovrà cambiare tale aggiunta. Seguendo l’ordine di precedenza, vengono applicati i seguenti scenari:

* Se un utente assegna manualmente un membro a un gruppo acquisti e successivamente viene eseguito un processo di manutenzione del gruppo acquisti che prevede la rimozione dello stesso membro dal gruppo, il processo di manutenzione **non rimuove** tale membro e non può sostituire l’assegnazione manuale.
* Se un utente assegna manualmente un membro a un gruppo acquisti e, in seguito, un nodo di percorso attivato rimuove lo stesso membro dal gruppo, l’azione del nodo **non rimuove** tale membro e non può sovrascrivere l’assegnazione manuale.
* Se un nodo di azione del percorso attivato aggiunge un membro al gruppo acquisti e successivamente un processo di manutenzione del gruppo acquisti rimuove lo stesso membro dal gruppo, il processo di manutenzione **non rimuove** tale membro e non può sostituire l’assegnazione dell’azione del percorso.

## Flusso di lavoro del gruppo acquisti

1. Crea gruppi acquisti.

   * Definire la [soluzione di interesse](./solution-interests.md) e il [modello di ruoli](./buying-groups-role-templates.md)
   * [Crea il gruppo acquisti](./buying-groups-create.md#create-buying-groups) e assegna le [fasi del gruppo acquisti](./buying-group-stages.md).

1. Identifica le persone mancanti in base alla completezza.

   Analizza il gruppo acquisti utilizzando i filtri.

   **Esempio:_**: manca il ruolo Responsabile delle decisioni e il punteggio di completezza è &lt; 50

1. Completa le definizioni dei gruppi acquisti.
<!--
   * Acquire missing people
   * Send to LinkedIn Destination
   * Enrich with Zoominfo -->

1. Aggiungi le azioni del gruppo acquisti ai tuoi percorsi account.

## Visualizzare gruppi acquisti e componenti

Nella barra di navigazione a sinistra, espandi **[!UICONTROL Account]** e fai clic su **[!UICONTROL Gruppi acquisti]**.

La pagina _[!UICONTROL Gruppi acquisti]_ è organizzata in schede:

| Scheda | Descrizione |
| --- | ----------- |
| [!UICONTROL Panoramica] | Questa scheda è quella predefinita e mostra la dashboard [Gruppi acquisti](../dashboards/buying-groups-dashboard.md). |
| [!UICONTROL Sfoglia] | Questa scheda supporta le seguenti attività: <ul><li>Visualizzare l’elenco dei gruppi acquisti esistenti. </li><li>Ricerca per nome del gruppo acquisti. </li><li>Filtrare per soluzione di interesse. </li><li>Espandere i dettagli del gruppo acquisti. </li><li>Crea un gruppo acquisti. </li></ul> |
| [!UICONTROL Soluzioni di interesse] | Questa scheda supporta le seguenti attività: <ul><li>Visualizzare l’elenco dei gruppi acquisti esistenti. </li><li>Ricerca per nome del gruppo acquisti. </li><li>Accedere e modificare le proprietà di soluzione di interesse. </li><li>Creare una soluzione di interesse. </li><li>Eliminare una soluzione di interesse. </li><li>Visualizzare ed eliminare i processi del gruppo acquisti. </li></ul> |
| [!UICONTROL Modelli di ruoli] | Questa scheda supporta le seguenti attività: <ul><li>Visualizzare l’elenco dei modelli di ruoli esistenti. </li><li>Cercare per nome modello di ruoli. </li><li>Accedere e modificare le proprietà e le condizioni del modello di ruoli. </li><li>Creare un modello di ruoli. </li><li>Eliminare un modello di ruoli. </li></ul> |
| [!UICONTROL Fasi] | Questa scheda supporta le seguenti attività: <ul><li>Visualizzare il modello di fasi dei gruppi acquisti esistenti. </li><li>Accedere e modificare la bozza del modello di fasi del gruppo acquisti. </li><li>Crea il modello di fasi del gruppo acquisti. </li></ul> |

## Ricerca e filtro gruppo acquisti

Utilizza la scheda _[!UICONTROL Sfoglia]_ per accedere all’elenco di gruppi acquisti. Puoi effettuare una ricerca per nome e filtrare l’elenco in base alla soluzione di interesse.

![Pagina sfoglia gruppo acquisti](assets/buying-groups-browse.png){width="800" zoomable="yes"}

## Dettagli del gruppo acquisti

Per accedere ai dettagli di un gruppo acquisti, fai clic sul nome del gruppo acquisti nella scheda _[!UICONTROL Sfoglia]_. [Ulteriori informazioni](./buying-group-details.md)

![Dettagli del gruppo acquisti](assets/buying-group-details.png){width="600" zoomable="yes"}

### Punteggio di completezza del gruppo acquisti

Il punteggio di completezza viene utilizzato per determinare se il gruppo acquisti è completo, ovvero dispone dei membri giusti assegnati ai ruoli ed è pronto per essere utilizzato in un percorso dell’account. Questo punteggio è una percentuale basata sul numero di ruoli all’interno del gruppo acquisti e sul numero di ruoli assegnati con almeno un lead.

Ad esempio, se all’interno di un gruppo acquisti sono presenti quattro ruoli e tre di tali quattro ruoli sono assegnati ad almeno un lead, il gruppo acquisti è completo al 75%.

Il punteggio di completezza del gruppo acquisti viene ricalcolato ogni volta che un gruppo acquisti viene creato o aggiornato.

### Punteggio di coinvolgimento del gruppo acquisti {#engagement-score}

>[!CONTEXTUALHELP]
>id="ajo-b2b_buying_group_engagement_score"
>title="Punteggio di coinvolgimento"
>abstract="I punteggi di coinvolgimento determinano il livello di coinvolgimento dei membri del gruppo acquisti."

Il punteggio di coinvolgimento del gruppo acquisti è un numero utilizzato per determinare il coinvolgimento dei membri di un gruppo acquisti, in base alle attività che eseguono.

* Il calcolo del punteggio di coinvolgimento inizia non appena viene generato il gruppo acquisti.
* Per calcolare il punteggio viene utilizzata qualsiasi attività in entrata eseguita dai membri del gruppo acquisti negli ultimi 30 giorni.
* Con la finestra di 30 giorni e con la scadenza delle attività, il punteggio potrebbe diminuire.
* Per ogni attività è presente un limite di frequenza giornaliero di 20. Se un membro di un gruppo acquisti esegue la stessa attività più di 20 volte al giorno, il limite massimo dell’attività è 20 e non un numero più alto.
* Il punteggio visualizzato viene arrotondato. Ad esempio, un punteggio di 75,89999 viene visualizzato come 76.

+++Attività utilizzate per il punteggio

| Nome attività | Descrizione | Tipo di coinvolgimento | Frequenza massima giornaliera | Peso attività |
| --- | --- | --- | --- | --- |
| [!UICONTROL Visita la pagina web] | Un membro visita una pagina web | Web | 20 | 40 |
| [!UICONTROL Compila il modulo] | Un membro compila e invia un modulo in una pagina web | Web | 20 | 40 |
| [!UICONTROL Fai clic sul collegamento] | Un membro fa clic su un collegamento in una pagina web | Web | 20 | 40 |
| [!UICONTROL Apri e-mail] | Un membro apre un’e-mail | E-mail | 20 | 30 |
| [!UICONTROL Fai clic sull’e-mail] | Un membro fa clic su un collegamento in un’e-mail | E-mail | 20 | 30 |
| [!UICONTROL Apri e-mail vendite] | Un membro apre un’e-mail vendite | E-mail | 20 | 30 |
| [!UICONTROL Fai clic sull’e-mail vendite] | Un membro fa clic su un collegamento in un’e-mail vendite | E-mail | 20 | 30 |
| [!UICONTROL Momento interessante] | Un membro ha un momento interessante | Curato | 20 | 60 |
| [!UICONTROL Tocca notifica push] | Un membro riceve una notifica push | Dispositivi mobili | 20 | 30 |
| [!UICONTROL Attività sull’app mobile] | Un membro esegue un’attività su un’app mobile | Dispositivi mobili | 20 | 30 |
| [!UICONTROL Sessione dell’app mobile] | Un membro è attivo in una sessione dell’app mobile | Dispositivi mobili | 20 | 30 |
| [!UICONTROL Compila il modulo Annunci lead di Facebook] | Un membro compila e invia un modulo Annunci lead su una pagina Facebook | Social | 20 | 30 |
| [!UICONTROL Fai clic su Invito all’azione RTP] | Un membro fa clic su un invito all’azione personalizzato | Web | 20 | 60 |
| [!UICONTROL Visualizza messaggio in-app] | Un membro visualizza un messaggio in-app | Dispositivi mobili | 20 | 30 |
| [!UICONTROL Tocca messaggio in-app] | Un membro tocca un messaggio in-app | Dispositivi mobili | 20 | 30 |
| [!UICONTROL Abbonati SMS] | Un membro si abbona alle comunicazioni SMS | SMS | 20 | 90 |
| [!UICONTROL Rispondi all’e-mail vendite] | Un membro risponde a un&#39;e-mail vendite | E-mail | 20 | 30 |
| [!UICONTROL Impegnato con una finestra di dialogo] | Un membro interagisce con una finestra di dialogo Dynamic Chat | Chat | 20 | 90 |
| [!UICONTROL Interagito con il documento nella finestra di dialogo] | Un membro interagisce con un documento in una finestra di dialogo Dynamic Chat | Chat | 20 | 90 |
| [!UICONTROL Riunione pianificata nella finestra di dialogo] | Un membro pianifica un appuntamento in una finestra di dialogo di Dynamic Chat | Chat | 20 | 90 |
| [!UICONTROL Obiettivo finestra di dialogo raggiunto] | Un membro raggiunge un obiettivo in una finestra di dialogo Dynamic Chat |  | 20 | 90 |
| [!UICONTROL Ha risposto a un sondaggio nel webinar] | Un membro risponde a un sondaggio in un evento webinar | Chat | 20 | 90 |
| [!UICONTROL Invito all’azione selezionato nel webinar] | Un membro fa clic su un collegamento di invito all’azione in un evento webinar | Invito | 20 | 30 |
| [!UICONTROL Download di risorse nel webinar] | Un membro scarica un file o una risorsa in un evento webinar | Evento | 20 | 60 |
| [!UICONTROL Pone domande nel webinar] | Un membro pone domande in un evento webinar | Evento | 20 | 60 |
| [!UICONTROL Ha partecipato all’evento] | Un membro ha partecipato a un evento | Evento | 20 | 60 |
| [!UICONTROL Impegnato con un agente nella finestra di dialogo] | Un membro interagisce con un agente in una finestra di dialogo di Dynamic Chat | Chat | 20 | 90 |
| [!UICONTROL Collegamento selezionato nella chat nella finestra di dialogo] | Un membro fa clic su un collegamento in una finestra di dialogo di Dynamic Chat | Chat | 20 | 90 |
| [!UICONTROL Impegnato in un flusso conversazionale] | Un membro interagisce con un flusso conversazionale di Dynamic Chat | Chat | 20 | 90 |
| [!UICONTROL Riunione pianificata nel flusso conversazionale] | Un membro pianifica un appuntamento in un flusso conversazionale di Dynamic Chat | Chat | 20 | 90 |
| [!UICONTROL Obiettivo del flusso conversazionale raggiunto] | Un membro raggiunge un obiettivo in un flusso conversazionale di Dynamic Chat | Chat | 20 | 90 |
| [!UICONTROL Impegnato con il documento nel flusso conversazionale] | Un membro interagisce con un documento in un flusso conversazionale di Dynamic Chat | Chat | 20 | 90 |
| [!UICONTROL Impegnato con un agente nel flusso conversazionale] | Un membro interagisce con un agente in un flusso conversazionale di Dynamic Chat | Chat | 20 | 90 |
| [!UICONTROL Collegamento selezionato in una chat in un flusso conversazionale] | Un membro fa clic su un collegamento in un flusso conversazionale di Dynamic Chat | Chat | 20 | 90 |
| [!UICONTROL Fai clic sul collegamento in SMS V2] | Un membro fa clic su un collegamento in un messaggio SMS | SMS | 20 | 90 |

>[!NOTE]
>
>Le attività con punteggio di coinvolgimento sono registrate nel [registro attività per persona](https://experienceleague.adobe.com/it/docs/marketo/using/product-docs/core-marketo-concepts/smart-lists-and-static-lists/managing-people-in-smart-lists/locate-the-activity-log-for-a-person){target="_blank"} di Marketo Engage.

+++

#### Ponderazione {#engagement-score-weighting}

>[!CONTEXTUALHELP]
>id="ajo-b2b_buying_group_engagement_score_weighting"
>title="Ponderazione del punteggio di coinvolgimento"
>abstract="Utilizza la ponderazione per personalizzare il calcolo del punteggio di coinvolgimento."

Gli utenti possono assegnare _ponderazione_ a ogni ruolo nel modello [ruoli](./buying-groups-role-templates.md) per allocare ponderazioni diverse per un ruolo.

![Impostare la ponderazione per ogni ruolo nel modello di ruoli](./assets/roles-templates-weighting.png){width="700" zoomable="yes"}

Ogni livello di ponderazione si traduce in un valore, utilizzato per calcolare il punteggio di coinvolgimento:

* [!UICONTROL Insignificante] = 20
* [!UICONTROL Minore] = 40
* [!UICONTROL Normale] = 60
* [!UICONTROL Importante] = 80
* [!UICONTROL Fondamentale] = 100

Un modello di ruoli con tre ruoli ponderati come _[!UICONTROL Fondamentale]_, _[!UICONTROL Importante]_ e _[!UICONTROL Normale]_ viene convertito nelle seguenti percentuali ponderate:

| Ruolo | Ponderazione | Valore di sistema | Calcolo del valore | Percentuale |
|-------------- |--------- |------------- |------------------ |---------- |
|               |          |              |                   |           |
| Responsabile delle decisioni | Fondamentale | 100 | 100/240 | 41,76% |
| Influencer | Importante | 80 | 80/240 | 33,33% |
| Professionista | Normale | 60 | 60/240 | 25% |
|               | Totale | 240 |                   |           |

#### Esempio di calcolo

L’esempio seguente illustra il calcolo del punteggio di coinvolgimento utilizzando la percentuale di peso del ruolo delineata, il conteggio delle attività in entrata per ogni membro del gruppo acquisti e un limite giornaliero di 20 conteggi per ogni evento (se si è verificato più volte).

| Ruolo | Membro | Tipo di attività | Conteggio di ieri | Conteggio odierno | Calcolo | Punteggio totale |
|-------------- |--------- |-------------|-----------------|-------------|------|-----------|
|               |          |             |                 |             |      |           |
| Responsabile delle decisioni | Adam | Sito web visitato | 37 | 15 | 20 + 15 | 35 |
|               |          | E-mail cliccata | 1 | 1 | 1 + 1 | 2 |
|               |          |             |                 |             |      |           |
|               | Contrassegna | Sito web visitato | 5 | 3 | 5 + 3 | 8 |
|               |          | E-mail cliccata | 1 | 1 | 1 + 1 | 2 |
|               |          | Pub scaricato | 3 | 2 | 3 + 2 | 5 |
| **Punteggio totale responsabili delle decisioni** |         |             |                 |             |      | **52** |
|               |          |             |                 |             |      |           |
| Influencer | John | Sito web visitato | 19 | 9 | 19 + 9 | 28 |
| **Punteggio totale influencer** |         |             |                 |             |      | **28** |
|               |          |             |                 |             |      |           |
| Professionista | Bob | E-mail cliccata | 1 | 1 | 1 + 1 | 2 |
|               |          |             |                 |             |      |           |
|               | Paul | E-mail cliccata | 1 | 1 | 1 + 1 | 2 |
|               |          |             |                 |             |      |           |
|               | Calvin | E-mail cliccata | 1 | 1 | 1 + 1 | 2 |
|               |          | Sito web visitato | 1 | 7 | 1 + 7 | 8 |
|               |          | Pub scaricato | 1 | 2 | 1 + 2 | 3 |
| **Punteggio totale professionisti** |         |             |                 |             |      | **17** |

Il punteggio di coinvolgimento finale viene calcolato applicando la ponderazione per ciascuno dei punteggi dei ruoli:

| Ruolo | Punteggio totale ruolo | % peso ruolo | Punteggio X peso % |
|-------------- |---------------- |------------- |---------------- |
| Responsabili delle decisioni | 52 | 41,76% | 21,67 |
| Influencer | 28 | 33,33% | 9,33 |
| Professionisti | 17 | 25% | 4,25 |
| **Punteggio di coinvolgimento finale** |                |             | **35,25** |

## Video di panoramica

>[!VIDEO](https://video.tv.adobe.com/v/3452945/?learn=on&captions=ita)
