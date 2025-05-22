---
title: Gruppi acquisti
description: Scopri come i gruppi acquisti in Journey Optimizer B2B Edition possono aumentare l’efficacia del marketing tramite identificazione e targeting dei membri dei tuoi elenchi di account.
feature: Buying Groups
role: User
exl-id: ddcd7b62-6a76-4f5e-b6d3-a20944ca8332
source-git-commit: d1130841ed3c560208bc93c53a54169f9b0b94aa
workflow-type: ht
source-wordcount: '1778'
ht-degree: 100%

---


# Gruppi acquisti

Per le attività di vendita e marketing B2B, gli account sono fondamentali per qualsiasi strategia. A ogni account è associato un gruppo di persone, che possono essere dipendenti dell’account o collaboratori esterni che utilizzano l’account. Gli account sono gerarchici e prodotti diversi possono essere venduti a diversi livelli nella gerarchia. Ad esempio, Adobe Experience Platform potrebbe essere venduto a livello aziendale a un account di livello dirigenziale. Inoltre, Adobe Photoshop potrebbe essere venduto a un account che rappresenta una divisione o un reparto all’interno di un’organizzazione, ad esempio un reparto progettazione all’interno di un’azienda più grande.

![Diagramma ruoli account](assets/account-roles-diagram.png){width="800"}

Nell’account potrebbe essere presente un sottoinsieme di persone che costituiscono il _gruppo acquisti_. Queste persone alla fine prendono la decisione di acquisto, quindi hanno bisogno di particolare attenzione da parte del marketer e potrebbero aver bisogno di informazioni diverse da quelle delle altre persone associate all’account. I gruppi acquisti possono comprendere un gruppo diverso di persone per diverse linee di prodotti o offerte. Ad esempio, un prodotto per la sicurezza informatica potrebbe in genere richiedere un Chief Information Officer o un Chief Security Officer e un rappresentante dell’Ufficio legale per approvare un acquisto, ma un prodotto di tracciamento dei bug potrebbe in genere interessare un VP of Engineering e un direttore IT come membri del gruppo di acquisto.

![Video](../../assets/do-not-localize/icon-video.svg){width="30"} [Guarda la panoramica video](#overview-video)

## Componenti principali

Puoi aumentare l’efficacia del marketing in Journey Optimizer B2B Edition creando gruppi acquisti che identificano i membri mancanti negli elenchi dei tuoi account target in base alle soluzioni che i team di vendita devono vendere. Prima che tu e il team di marketing iniziate a creare i gruppi acquisti, accertati di aver definito i componenti principali. Questi componenti sono fondamentali per raggiungere gli obiettivi e le finalità aziendali.

| Componente | Finalità |
| --------- | ------- |
| Interesse della soluzione | Questo componente fornisce la risposta alle domande seguenti: <ul><li>In qualità di organizzazione di marketing, cosa stai vendendo?</li><li>Su quale prodotto o raccolta di prodotti stai puntando per la vendita?</li></ul>  **_Esempio:_** cross-selling del nuovo prodotto X a clientela esistente |
| Pubblico dell’account | Questo componente fornisce la risposta alle domande seguenti: <ul><li>A chi stai vendendo?</li><li>Qual è l’elenco degli account a cui stai puntando?</li></ul> **_Esempio:_** segmento di account definito da account con prodotto Y che hanno ricavi superiori a 1 milione |
| Modelli di ruolo del gruppo acquisti | Questo componente fornisce la risposta alle domande seguenti: <ul><li>Di quali ruoli esegui il targeting?</li><li>Quale insieme di regole viene utilizzato per determinare chi è assegnato ai ruoli del gruppo acquisti?</li></ul>  **_Esempio:_** assegna una persona con titolo CMO al ruolo Responsabile delle decisioni |
| Fasi del gruppo acquisti | (Facoltativo) Questo componente fornisce la risposta alla domanda: In che modo il gruppo acquisti segue il percorso del successo o del fallimento? |

## Flusso di lavoro del gruppo acquisti

1. Crea gruppi acquisti.

   * Definire l’[interesse della soluzione](./solution-interests.md) e il [modello di ruolo](./buying-groups-role-templates.md)
   * [Crea il gruppo acquisti](./buying-groups-create.md#create-buying-groups) e assegna le [fasi del gruppo acquisti](./buying-group-stages.md).

1. Identifica le figure mancanti.

   Analizza il gruppo acquisti utilizzando i filtri.

   **_Esempio:_** manca il ruolo Responsabile delle decisioni e il punteggio di completezza è &lt; 50

1. Completa le definizioni dei gruppi acquisti.
<!--
   * Acquire missing people
   * Send to LinkedIn Destination
   * Enrich with Zoominfo -->

1. Utilizza il gruppo acquisti per i percorsi account.

## Visualizzare gruppi acquisti e componenti

Nella barra di navigazione a sinistra, espandi **[!UICONTROL Account]** e fai clic su **[!UICONTROL Gruppi acquisti]**.

La pagina _[!UICONTROL Gruppi acquisti]_ è organizzata in schede:

| Scheda | Descrizione |
| --- | ----------- |
| [!UICONTROL Panoramica] | Questa scheda è quella predefinita e mostra la dashboard [Gruppi acquisti](../dashboards/buying-groups-dashboard.md). |
| [!UICONTROL Sfoglia] | Questa scheda supporta le seguenti attività: <ul><li>Visualizzare l’elenco dei gruppi acquisti esistenti. </li><li>Cercare per nome gruppo acquisti. </li><li>Filtrare per interesse della soluzione. </li><li>Espandere i dettagli del gruppo acquisti. </li><li>Crea un gruppo acquisti. </li></ul> |
| [!UICONTROL Interessi della soluzione] | Questa scheda supporta le seguenti attività: <ul><li>Visualizzare l’elenco dei gruppi acquisti esistenti. </li><li>Cercare per nome gruppo acquisti. </li><li>Accedere e modificare le proprietà di interesse della soluzione. </li><li>Creare un interesse della soluzione. </li><li>Eliminare un interesse della soluzione. </li><li>Visualizzare ed eliminare i processi del gruppo acquisti. </li></ul> |
| [!UICONTROL Modelli di ruolo] | Questa scheda supporta le seguenti attività: <ul><li>Visualizzare l’elenco dei modelli di ruolo esistenti. </li><li>Cercare per nome modello di ruoli. </li><li>Accedere e modificare le proprietà e le condizioni del modello di ruoli. </li><li>Creare un modello di ruoli. </li><li>Eliminare un modello di ruoli. </li></ul> |
| [!UICONTROL Fasi] | Questa scheda supporta le seguenti attività: <ul><li>Visualizzare il modello di fasi dei gruppi acquisti esistenti. </li><li>Accedere e modificare la bozza del modello di fasi del gruppo acquisti. </li><li>Crea il modello di fasi del gruppo acquisti. </li></ul> |

## Ricerca e filtro gruppo acquisti

Utilizza la scheda _[!UICONTROL Sfoglia]_ per accedere all’elenco di gruppi acquisti. Puoi effettuare una ricerca per nome e filtrare l’elenco in base all’interesse della soluzione.

![Pagina sfoglia gruppo acquisti](assets/buying-groups-browse.png){width="800" zoomable="yes"}

## Dettagli del gruppo acquisti

Per accedere ai dettagli di un gruppo acquisti, fai clic sul nome del gruppo acquisti nella scheda _[!UICONTROL Sfoglia]_. [Ulteriori informazioni](./buying-group-details.md)

![Dettagli del gruppo acquisti](assets/buying-group-details.png){width="600" zoomable="yes"}

### Punteggio di completezza del gruppo acquisti

Il punteggio di completezza viene utilizzato per determinare se il gruppo acquisti è completo, ovvero dispone dei membri giusti assegnati ai ruoli ed è pronto per essere utilizzato in un percorso dell’account. Questo punteggio è una percentuale basata sul numero di ruoli all’interno del gruppo acquisti e sul numero di ruoli assegnati con almeno un lead.

Ad esempio, se all’interno di un gruppo acquisti sono presenti quattro ruoli e tre di tali quattro ruoli sono assegnati ad almeno un lead, il gruppo acquisti è completo al 75%.

Il punteggio di completezza del gruppo acquisti viene ricalcolato ogni volta che un gruppo acquisti viene creato o aggiornato.

### Punteggio di coinvolgimento del gruppo acquisti

Il punteggio di coinvolgimento del gruppo acquisti è un numero utilizzato per determinare il coinvolgimento dei membri di un gruppo acquisti, in base alle attività che eseguono.

* Il calcolo del punteggio di coinvolgimento inizia non appena viene generato il gruppo acquisti.
* Per calcolare il punteggio viene utilizzata qualsiasi attività in entrata eseguita dai membri del gruppo acquisti negli ultimi 30 giorni.
* Con la finestra di 30 giorni e con la scadenza delle attività, il punteggio potrebbe diminuire.
* Per ogni attività è presente un limite di frequenza giornaliero di 20. Se un membro di un gruppo acquisti esegue la stessa attività più di 20 volte al giorno, il numero massimo di attività è 20 e non un numero più alto.
* Il punteggio visualizzato viene arrotondato. Ad esempio, un punteggio di 75,89999 viene visualizzato come 76.

+++Attività utilizzate per il punteggio

| Nome attività | Descrizione | Tipo di coinvolgimento | Frequenza massima giornaliera | Peso attività |
| --- | --- | --- | --- | --- |
| Registrati a un evento | Registra a un evento associato a una campagna | Evento | 20 | 60 |
| Partecipa a un evento | Partecipa a un evento della campagna | Evento | 20 | 90 |
| Apri e-mail | Apre un’email | E-mail | 20 | 30 |
| Fai clic sull’e-mail | Fa clic su un collegamento in un messaggio e-mail | E-mail | 20 | 30 |
| Apri e-mail vendite | Apre un’e-mail vendite | E-mail | 20 | 30 |
| Fai clic sull’e-mail vendite | Fa clic su un collegamento in un messaggio e-mail vendite | E-mail | 20 | 30 |
| Momento interessante | Ha un momento interessante | Curato | 20 | 60 |
| Tocca Notifica push | Riceve una notifica push | Dispositivi mobili | 20 | 30 |
| Attività sull’app mobile | Esegue un’attività su un’app mobile | Dispositivi mobili | 20 | 30 |
| Sessione dell’app mobile | È attivo nella sessione dell’app mobile | Dispositivi mobili | 20 | 30 |
| Compila il modulo Annunci lead di Facebook | Compila e invia un modulo Annunci lead su una pagina Facebook | Social | 20 | 30 |
| Fai clic su Invito all’azione RTP | Fa clic su un invito all’azione personalizzato | Web | 20 | 60 |
| Visualizza messaggio in-app | Visualizza un messaggio in-app | Dispositivi mobili | 20 | 30 |
| Tocca messaggio in-app | Tocca un messaggio in-app | Dispositivi mobili | 20 | 30 |
| Abbonati SMS | Si abbona alle comunicazioni SMS | SMS | 20 | 90 |
| Rispondi all’e-mail vendite | Risponde a un’e-mail vendite | E-mail | 20 | 30 |
| Impegnato con una finestra di dialogo | Interagisce con una finestra di dialogo Dynamic Chat | Chat | 20 | 90 |
| Interagito con il documento nella finestra di dialogo | Interagisce con un documento in una finestra di dialogo Dynamic Chat | Chat | 20 | 90 |
| Riunione pianificata nella finestra di dialogo | Pianifica un appuntamento in una finestra di dialogo di Dynamic Chat | Chat | 20 | 90 |
| Obiettivo finestra di dialogo raggiunto | Raggiunge un obiettivo in una finestra di dialogo Dynamic Chat |  | 20 | 90 |
| Ha risposto a un sondaggio nel webinar | Risponde a un sondaggio in un evento webinar | Chat | 20 | 90 |
| Invito all’azione selezionato nel webinar | Fa clic su un collegamento di invito all’azione in un evento webinar | Invito | 20 | 30 |
| Download di risorse nel webinar | Scarica un file o una risorsa in un evento webinar | Evento | 20 | 60 |
| Pone domande nel webinar | Pone domande in un evento webinar | Evento | 20 | 60 |
| Ha partecipato all’evento | Ha partecipato a un evento | Evento | 20 | 60 |
| Impegnato con un agente nella finestra di dialogo | Interagisce con un agente in una finestra di dialogo di Dynamic Chat | Chat | 20 | 90 |
| Collegamento selezionato nella chat nella finestra di dialogo | Fa clic su un collegamento in una finestra di dialogo di Dynamic Chat | Chat | 20 | 90 |
| Impegnato in un flusso conversazionale | Interagisce con un flusso conversazionale di Dynamic Chat | Chat | 20 | 90 |
| Riunione pianificata nel flusso conversazionale | Pianifica un appuntamento in un flusso conversazionale di Dynamic Chat | Chat | 20 | 90 |
| Obiettivo del flusso conversazionale raggiunto | Raggiunge un obiettivo in un flusso conversazionale di Dynamic Chat | Chat | 20 | 90 |
| Impegnato con il documento nel flusso conversazionale | Interagisce con un documento in un flusso conversazionale di Dynamic Chat | Chat | 20 | 90 |
| Impegnato con un agente nel flusso conversazionale | Interagisce con un agente in un flusso conversazionale di Dynamic Chat | Chat | 20 | 90 |
| Collegamento selezionato in una chat in flusso conversazionale | Fa clic su un collegamento in un flusso conversazionale di Dynamic Chat | Chat | 20 | 90 |
| Fai clic sul collegamento in SMS V2 | Fa clic su un collegamento in un messaggio SMS | SMS | 20 | 90 |

>[!NOTE]
>
>Le attività con punteggio di coinvolgimento sono registrate nel [registro attività per persona](https://experienceleague.adobe.com/it/docs/marketo/using/product-docs/core-marketo-concepts/smart-lists-and-static-lists/managing-people-in-smart-lists/locate-the-activity-log-for-a-person){target="_blank"} di Marketo Engage.

+++

#### Ponderazione

Gli utenti possono assegnare la _ponderazione_ a ciascun ruolo nel modello dei ruoli per allocare pesi diversi a un ruolo e calcolare il punteggio di coinvolgimento.

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

L’esempio seguente illustra il calcolo del punteggio di coinvolgimento utilizzando la percentuale di peso del ruolo delineata, il conteggio delle attività in entrata per ogni membro del gruppo acquisti e un tetto giornaliero di 20 conteggi per ogni evento (se si è verificato più volte).

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

>[!VIDEO](https://video.tv.adobe.com/v/3433078/?learn=on)
