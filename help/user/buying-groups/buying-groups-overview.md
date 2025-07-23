---
title: Gruppi acquisti
description: Scopri come i gruppi acquisti in Journey Optimizer B2B Edition possono aumentare l’efficacia del marketing tramite identificazione e targeting dei membri dei tuoi elenchi di account.
feature: Buying Groups
role: User
exl-id: ddcd7b62-6a76-4f5e-b6d3-a20944ca8332
source-git-commit: ada98f505aad848f958cf8325ed90d66692a6cac
workflow-type: tm+mt
source-wordcount: '2151'
ht-degree: 57%

---


# Gruppi acquisti

Per le attività di vendita e marketing B2B, gli account sono fondamentali per qualsiasi strategia. A ogni account è associato un gruppo di persone, che possono essere dipendenti dell’account o collaboratori esterni che utilizzano l’account. Gli account sono gerarchici e prodotti diversi possono essere venduti a diversi livelli nella gerarchia. Ad esempio, Adobe Experience Platform potrebbe essere venduto a livello aziendale a un account di livello dirigenziale. Inoltre, Adobe Photoshop potrebbe essere venduto a un account che rappresenta una divisione o un reparto all’interno di un’organizzazione, ad esempio un reparto progettazione all’interno di un’azienda più grande.

![Diagramma ruoli account](assets/account-roles-diagram.png){width="800"}

Nell’account potrebbe essere presente un sottoinsieme di persone che costituiscono il _gruppo acquisti_. Queste persone alla fine prendono la decisione di acquisto, quindi hanno bisogno di particolare attenzione da parte del marketer e potrebbero aver bisogno di informazioni diverse da quelle delle altre persone associate all’account. I gruppi acquisti possono comprendere un gruppo diverso di persone per diverse linee di prodotti o offerte. Ad esempio, un prodotto di cibersicurezza potrebbe in genere richiedere un Responsabile delle informazioni o un Responsabile della sicurezza e un rappresentante dell&#39;Ufficio legale per approvare un acquisto. Un prodotto di tracciamento dei bug può avere in genere un VP of Engineering e un direttore IT come membri del gruppo di acquisto.

![Video](../../assets/do-not-localize/icon-video.svg){width="30"} [Guarda la panoramica video](#overview-video)

## Componenti principali

È possibile aumentare l&#39;efficacia del marketing creando gruppi di acquisto in Journey Optimizer B2B edition che identificano i membri per gli elenchi di account di destinazione in base alle soluzioni che i team di vendita sono responsabili della vendita. Prima che tu e il team Marketing iniziiate a creare i gruppi di acquisto, accertati di disporre dei componenti chiave definiti. Questi componenti sono fondamentali per raggiungere gli obiettivi e le finalità aziendali.

| Componente | Finalità |
| --------- | ------- |
| Interesse della soluzione | Questo componente fornisce la risposta alle domande seguenti: <ul><li>In qualità di organizzazione di marketing, cosa stai vendendo?</li><li>Su quale prodotto o raccolta di prodotti stai puntando per la vendita?</li></ul>  **_Esempio:_** Vendita incrociata del nuovo prodotto X a clienti esistenti |
| Pubblico dell’account | Questo componente fornisce la risposta alle domande seguenti: <ul><li>A chi stai vendendo?</li><li>Qual è l’elenco degli account a cui stai puntando?</li></ul> **_Esempio:_** Segmento di conto definito da conti con prodotto Y che hanno ricavi superiori a 1M |
| Modelli di ruolo del gruppo acquisti | Questo componente fornisce la risposta alle domande seguenti: <ul><li>Di quali ruoli esegui il targeting?</li><li>Quale insieme di regole viene utilizzato per determinare chi è assegnato ai ruoli del gruppo acquisti?</li></ul>  **_Esempio:_** Assegna una persona con titolo CMO al ruolo Responsabile delle decisioni |
| Fasi del gruppo acquisti | (Facoltativo) Questo componente fornisce la risposta alla domanda: In che modo il gruppo acquisti segue il percorso del successo o del fallimento? |

## Assegnazione membro

Esistono tre modi per assegnare o rimuovere i membri da un gruppo di acquisto. Nell&#39;elenco seguente vengono descritti questi metodi di aggiunta e rimozione in ordine di precedenza. Il metodo più alto ha la precedenza più alta e uno più basso non può sovrascriverlo.

1. **_Azione manuale_**: azione manuale di aggiunta o rimozione di un membro eseguita da un utente di vendita per il gruppo di acquisto
2. **_Azione Percorso_** - Nodi azione [Percorso per l&#39;acquisto dell&#39;appartenenza al gruppo](../journeys/action-nodes.md#add-a-people-based-action) (_Assegna al gruppo Acquisti_ o _Rimuovi dal gruppo Acquisti_)
3. **_Processi di sistema_** - Acquisto del gruppo [creazione](../buying-groups/buying-groups-create.md#buying-group-creation-jobs) e processi di manutenzione.

Per garantire che l&#39;assegnazione dei membri in un gruppo di acquisto non venga ignorata in modo errato, l&#39;elenco è nell&#39;ordine di precedenza seguito nel sistema per garantire un&#39;assegnazione accurata dei membri. Ad esempio, quando un utente di vendita aggiunge manualmente un membro al gruppo di acquisto, non desidera che un processo di manutenzione modifichi tale aggiunta. Utilizzando l’ordine di precedenza, vengono applicati i seguenti scenari:

* Se un utente assegna manualmente un membro a un gruppo di acquisto seguito da un processo di manutenzione del gruppo di acquisto che rimuove lo stesso membro dal gruppo di acquisto, il processo di manutenzione **non rimuove** tale membro e non può sostituire l&#39;assegnazione manuale.
* Se un utente assegna manualmente un membro a un percorso di acquisto e questo viene seguito da un nodo attivato che rimuove lo stesso membro dal gruppo di acquisto, l&#39;azione del nodo **non rimuove** tale membro e non può sovrascrivere l&#39;assegnazione manuale.
* Se un nodo di azione del percorso attivato aggiunge un membro a un gruppo di acquisto e questo è seguito da un processo di manutenzione del gruppo di acquisto che rimuove lo stesso membro dal gruppo di acquisto, il processo di manutenzione **non rimuove** tale membro e non può sostituire l&#39;assegnazione dell&#39;azione del percorso.

## Flusso di lavoro del gruppo acquisti

1. Crea gruppi acquisti.

   * Definire l’[interesse della soluzione](./solution-interests.md) e il [modello di ruolo](./buying-groups-role-templates.md)
   * [Crea il gruppo acquisti](./buying-groups-create.md#create-buying-groups) e assegna le [fasi del gruppo acquisti](./buying-group-stages.md).

1. Identificare le persone scomparse per completezza.

   Analizza il gruppo acquisti utilizzando i filtri.

   **_Esempio:_** Ruolo Responsabile delle decisioni mancante e punteggio di completezza &lt; 50

1. Completa le definizioni dei gruppi acquisti.
<!--
   * Acquire missing people
   * Send to LinkedIn Destination
   * Enrich with Zoominfo -->

1. Aggiungi le azioni del gruppo di acquisto ai tuoi percorsi di account.

## Visualizzare gruppi acquisti e componenti

Nella barra di navigazione a sinistra, espandi **[!UICONTROL Account]** e fai clic su **[!UICONTROL Gruppi acquisti]**.

La pagina _[!UICONTROL Gruppi acquisti]_ è organizzata in schede:

| Scheda | Descrizione |
| --- | ----------- |
| [!UICONTROL Panoramica] | Questa scheda è quella predefinita e mostra la dashboard [Gruppi acquisti](../dashboards/buying-groups-dashboard.md). |
| [!UICONTROL Sfoglia] | Questa scheda supporta le seguenti attività: <ul><li>Visualizzare l’elenco dei gruppi acquisti esistenti. </li><li>Cerca in base al nome del gruppo di acquisto. </li><li>Filtrare per interesse della soluzione. </li><li>Espandere i dettagli del gruppo acquisti. </li><li>Crea un gruppo acquisti. </li></ul> |
| [!UICONTROL Interessi della soluzione] | Questa scheda supporta le seguenti attività: <ul><li>Visualizzare l’elenco dei gruppi acquisti esistenti. </li><li>Cerca in base al nome del gruppo di acquisto. </li><li>Accedere e modificare le proprietà di interesse della soluzione. </li><li>Creare un interesse della soluzione. </li><li>Eliminare un interesse della soluzione. </li><li>Visualizzare ed eliminare i processi del gruppo acquisti. </li></ul> |
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
| [!UICONTROL Visita pagina Web] | Un membro visita una pagina web | Web | 20 | 40 |
| [!UICONTROL Compila modulo] | Un membro compila e invia un modulo in una pagina Web | Web | 20 | 40 |
| [!UICONTROL Fai clic sul collegamento] | Un membro fa clic su un collegamento in una pagina Web | Web | 20 | 40 |
| [!UICONTROL Apri e-mail] | Un membro apre un messaggio e-mail | E-mail | 20 | 30 |
| [!UICONTROL Fai clic su E-mail] | Un membro fa clic su un collegamento in un messaggio e-mail | E-mail | 20 | 30 |
| [!UICONTROL Apri e-mail vendite] | Un membro apre un messaggio e-mail di vendita | E-mail | 20 | 30 |
| [!UICONTROL Fai clic su E-mail vendite] | Un membro fa clic su un collegamento in un messaggio e-mail di vendita | E-mail | 20 | 30 |
| [!UICONTROL Momento di interesse] | Un membro ha un momento interessante | Curato | 20 | 60 |
| [!UICONTROL Tocca Notifica Push] | Un membro riceve una notifica push | Dispositivi mobili | 20 | 30 |
| [!UICONTROL Attività app mobile] | Un membro esegue un&#39;attività su un&#39;app mobile | Dispositivi mobili | 20 | 30 |
| [!UICONTROL Sessione app mobile] | Un membro è attivo in una sessione di app mobile | Dispositivi mobili | 20 | 30 |
| [!UICONTROL Compila il modulo per gli annunci lead di Facebook] | Un membro compila e invia un modulo di annunci lead su una pagina Facebook | Social | 20 | 30 |
| [!UICONTROL Fare clic su Call to action RTP] | Un membro fa clic su un call to action personalizzato | Web | 20 | 60 |
| [!UICONTROL Visualizza Messaggio In-App] | Un membro visualizza un messaggio in-app | Dispositivi mobili | 20 | 30 |
| [!UICONTROL Tocca Messaggio In-App] | Un membro tocca un messaggio in-app | Dispositivi mobili | 20 | 30 |
| [!UICONTROL Sottoscrivi SMS] | Un membro si abbona alle comunicazioni SMS | SMS | 20 | 90 |
| [!UICONTROL Risposta all&#39;e-mail di vendita] | Un membro risponde a un&#39;e-mail di vendita | E-mail | 20 | 30 |
| [!UICONTROL Coinvolto con una finestra di dialogo] | Un membro si impegna con una finestra di dialogo Dynamic Chat | Chat | 20 | 90 |
| [!UICONTROL Interazione con il documento nella finestra di dialogo] | Un membro interagisce con un documento in una finestra di dialogo di Dynamic Chat | Chat | 20 | 90 |
| [!UICONTROL Riunione pianificata nella finestra di dialogo] | Un membro pianifica un appuntamento in una finestra di dialogo di Dynamic Chat | Chat | 20 | 90 |
| [!UICONTROL Obiettivo della finestra di dialogo raggiunto] | Un membro raggiunge un obiettivo in una finestra di dialogo Dynamic Chat |  | 20 | 90 |
| [!UICONTROL Ha risposto a un sondaggio nel webinar] | Un membro risponde a un sondaggio in un evento webinar | Chat | 20 | 90 |
| [!UICONTROL Clic su Call to action nel webinar] | Un membro fa clic su un collegamento di call-to-action in un evento webinar | Invito | 20 | 30 |
| [!UICONTROL Download di risorse nel webinar] | Un membro scarica un file o una risorsa in un evento webinar | Evento | 20 | 60 |
| [!UICONTROL Pone domande nel webinar] | Un membro fa domande in un evento webinar | Evento | 20 | 60 |
| [!UICONTROL Ha partecipato all&#39;evento] | Un membro ha partecipato a un evento | Evento | 20 | 60 |
| [!UICONTROL Coinvolto con un agente nella finestra di dialogo] | Un membro si impegna con un agente in una finestra di dialogo di Dynamic Chat | Chat | 20 | 90 |
| [!UICONTROL Collegamento selezionato in Chat nella finestra di dialogo] | Un membro fa clic su un collegamento in una finestra di dialogo di Dynamic Chat | Chat | 20 | 90 |
| [!UICONTROL Coinvolto con un flusso conversazionale] | Un membro partecipa a un flusso di conversazione Dynamic Chat | Chat | 20 | 90 |
| [!UICONTROL Riunione pianificata in flusso conversazionale] | Un membro pianifica un appuntamento in un flusso di conversazione Dynamic Chat | Chat | 20 | 90 |
| [!UICONTROL Obiettivo di flusso conversazionale raggiunto] | Un membro raggiunge un obiettivo in un flusso di conversazione Dynamic Chat | Chat | 20 | 90 |
| [!UICONTROL Interazione con il documento nel flusso conversazionale] | Un membro interagisce con un documento in un flusso conversazionale di Dynamic Chat | Chat | 20 | 90 |
| [!UICONTROL Coinvolto con un agente nel flusso conversazionale] | Un membro si impegna con un agente in un flusso di conversazione Dynamic Chat | Chat | 20 | 90 |
| [!UICONTROL Collegamento selezionato in Chat in Flusso conversazionale] | Un membro fa clic su un collegamento in un flusso di conversazione Dynamic Chat | Chat | 20 | 90 |
| [!UICONTROL Fai clic sul collegamento in SMS V2] | Un membro fa clic su un collegamento in un messaggio SMS | SMS | 20 | 90 |

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
