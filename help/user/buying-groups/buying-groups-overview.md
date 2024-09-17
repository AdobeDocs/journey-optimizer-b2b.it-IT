---
title: Gruppi di acquisto
description: Scopri come acquistare i gruppi e i relativi componenti.
feature: Buying Groups
exl-id: ddcd7b62-6a76-4f5e-b6d3-a20944ca8332
source-git-commit: 8571e26a99a86e938bafbce7cea599a46441da8d
workflow-type: tm+mt
source-wordcount: '1193'
ht-degree: 5%

---


# Gruppi acquisti

Per le attività di vendita e marketing B2B, gli account sono fondamentali per qualsiasi strategia. A ogni account è associato un gruppo di persone, che possono essere dipendenti dell&#39;account o collaboratori esterni che lavorano con l&#39;account. Gli account sono gerarchici e prodotti diversi possono essere venduti a diversi livelli nella gerarchia. Ad esempio, Adobe Experience Platform potrebbe essere venduto a livello aziendale a un account di livello superiore, mentre Adobe Photoshop potrebbe essere venduto a un account che rappresenta una divisione o un reparto all’interno di un’organizzazione, ad esempio un reparto progettazione all’interno di un’azienda più grande.

![Diagramma ruoli account](assets/account-roles-diagram.png){width="800"}

Nell&#39;account potrebbe essere presente un sottoinsieme di persone che costituiscono il _gruppo di acquisto_. Queste sono le persone che alla fine prendono la decisione di acquisto, quindi hanno bisogno di particolare attenzione da parte dell’addetto al marketing e potrebbero aver bisogno di informazioni diverse da quelle delle altre persone associate all’account. I gruppi di acquisto possono comprendere un gruppo diverso di persone per diverse linee di prodotti o offerte. Ad esempio, un prodotto di cibersicurezza potrebbe in genere richiedere un Chief Information Officer o un Chief Security Officer e un rappresentante dell&#39;Ufficio legale per approvare un acquisto, ma un prodotto di tracciamento dei bug potrebbe in genere avere un VP of Engineering e un IT Director come membri del gruppo di acquisto.

![Video](../../assets/do-not-localize/icon-video.svg){width="30"} [Guarda la panoramica del video](#overview-video)

## Componenti chiave

Puoi aumentare l’efficacia del marketing creando, in Journey Optimizer B2B Edition, gruppi di acquisto che identifichino i membri mancanti negli elenchi degli account di destinazione in base alle soluzioni che i team di vendita sono responsabili della vendita. Prima che tu e il team Marketing iniziiate a creare i gruppi di acquisto, accertati di disporre dei componenti chiave definiti. Questi componenti sono fondamentali per raggiungere gli obiettivi e le finalità aziendali.

| Componente | Finalità |
| --------- | ------- |
| Interesse nella soluzione | Questo componente fornisce la risposta a: <ul><li>In qualità di organizzazione di marketing, cosa stai vendendo?</li><li>Quale prodotto o raccolta di prodotti intendi vendere?</li></ul>  **_Esempio:_** vendita incrociata del nuovo prodotto X a clienti esistenti |
| Pubblico dell’account | Questo componente fornisce la risposta a: <ul><li>A chi stai vendendo?</li><li>Qual è l’elenco degli account di destinazione?</li></ul> **_Esempio:_** segmento di conto definito da conti con prodotto Y che hanno ricavi superiori a 1M |
| Acquisto di modelli di ruolo del gruppo | Questo componente fornisce la risposta a: <ul><li>Quali ruoli esegui il targeting?</li><li>Quale insieme di regole viene utilizzato per determinare chi è assegnato ai ruoli del gruppo di acquisto?</li></ul>  **_Esempio:_** assegna una persona con titolo CMO al ruolo Responsabile delle decisioni |

## Flusso di lavoro gruppo acquisti

1. Creare gruppi di acquisto.

   Opzioni:
   * Usa [interesse soluzione](./solution-interests.md) e [modello ruolo](./buying-groups-role-templates.md)
   * Usa importazione di terze parti
   * Genera da IA/ML

1. Identifica le persone scomparse.

   Analizza il gruppo di acquisto utilizzando i filtri.

   **_Esempio:_** ruolo Responsabile delle decisioni mancante e punteggio di completezza &lt; 50

1. Completa le definizioni dei gruppi di acquisto.
<!--
   * Acquire missing people
   * Send to LinkedIn Destination
   * Enrich with Zoominfo -->

1. Utilizza in un percorso di account tramite l’interesse della soluzione associato.

## Visualizza gruppi di acquisto e componenti

Nella barra di navigazione a sinistra, espandi **[!UICONTROL Account]** e fai clic su **[!UICONTROL Gruppi di acquisto]**.

La pagina _[!UICONTROL Gruppi di acquisto]_ è organizzata in schede:

| Scheda | Descrizione |
| --- | ----------- |
| [!UICONTROL Panoramica] | Questa scheda è quella predefinita e visualizza il dashboard [Gruppi di acquisto](../dashboards/buying-groups-dashboard.md). |
| [!UICONTROL Sfoglia] | Questa scheda supporta le seguenti attività: <ul><li>Visualizza l&#39;elenco dei gruppi di acquisto esistenti. </li><li>Cerca per nome gruppo di acquisto. </li><li>Filtra per interesse della soluzione. </li><li>Espandere i dettagli del gruppo di acquisto. </li><li>Crea un gruppo di acquisto. Eliminare un gruppo di acquisto.</li></ul> |
| [!UICONTROL Interessi sulla soluzione] | Questa scheda supporta le seguenti attività: <ul><li>Visualizza l&#39;elenco dei gruppi di acquisto esistenti. </li><li>Cerca per nome gruppo di acquisto. </li><li>Accedere e modificare le proprietà di interesse della soluzione. </li><li>Crea un interesse per la soluzione. </li><li>Eliminare un interesse per la soluzione. </li><li>Visualizza ed elimina i processi del gruppo di acquisto. </li></ul> |
| [!UICONTROL Modelli di Ruoli] | Questa scheda supporta le seguenti attività: <ul><li>Visualizza l&#39;elenco dei modelli di ruoli esistenti. </li><li>Cerca per nome modello ruoli. </li><li>Consente di accedere e modificare le proprietà e le condizioni del modello di ruoli. </li><li>Crea un modello di ruoli. </li><li>Eliminare un modello di ruoli. </li></ul> |

## Ricerca e filtro gruppo di acquisto

Utilizza la scheda _[!UICONTROL Sfoglia]_ per visualizzare l&#39;elenco dei gruppi di acquisto. Puoi cercare per nome e filtrare l’elenco in base all’interesse della soluzione.

![Sfoglia gruppo acquisti](assets/buying-groups-browse.png){width="800" zoomable="yes"}

## Dettagli gruppo di acquisto

Per accedere ai dettagli di un gruppo di acquisto, fare clic sul nome del gruppo di acquisto nella scheda _[!UICONTROL Sfoglia]_.

![Dettagli gruppo di acquisto](assets/buying-group-details.png){width="600" zoomable="yes"}

### Punteggio di completezza del gruppo di acquisto

Il punteggio di completezza viene utilizzato per determinare se il gruppo di acquisto è completo, il che significa che ha i membri giusti assegnati ai ruoli ed è pronto per essere utilizzato in un percorso di account. Questo punteggio è una percentuale basata sul numero di ruoli all’interno del gruppo di acquisto e sul numero di ruoli assegnati con almeno un lead.

Ad esempio, se all’interno di un gruppo di acquisto sono presenti quattro ruoli e tre dei quattro ruoli sono assegnati ad almeno un lead, il gruppo di acquisto è completato al 75%.

Il punteggio di completezza del gruppo di acquisto viene ricalcolato ogni volta che un gruppo di acquisto viene creato o aggiornato.

### Punteggio di coinvolgimento del gruppo acquisti

Punteggio di coinvolgimento del gruppo di acquisto è un numero per determinare il coinvolgimento dei membri di un gruppo di acquisto, in base alle attività che eseguono. Per calcolare il punteggio viene utilizzata qualsiasi attività in entrata eseguita dai membri del gruppo di acquisto negli ultimi 30 giorni.

C’è un limite di frequenza giornaliero di 20 per ogni attività. Se un membro di un gruppo di acquisto esegue la stessa attività più di 20 volte al giorno, il numero massimo di attività è 20 e non un numero più alto.

Il punteggio visualizzato viene arrotondato. Ad esempio, un punteggio di 75,89999 viene visualizzato come 76.

#### Ponderazione

Gli utenti possono assegnare _ponderazione_ a ciascun ruolo nel modello dei ruoli per allocare ponderazioni diverse a un ruolo per calcolare il punteggio di coinvolgimento.

![Imposta la ponderazione per ogni ruolo nel modello di ruoli](./assets/roles-templates-weighting.png){width="700" zoomable="yes"}

Ogni livello di ponderazione si traduce in un valore, utilizzato per calcolare il punteggio di coinvolgimento:

* [!UICONTROL Bassa] = 20
* [!UICONTROL Non grave] = 40
* [!UICONTROL Normale] = 60
* [!UICONTROL Importante] = 80
* [!UICONTROL Vital] = 100

Un modello di ruoli con tre ruoli ponderati come _[!UICONTROL Vital]_, _[!UICONTROL Importante]_ e _[!UICONTROL Normale]_ viene convertito nelle seguenti percentuali ponderate:

| Ruolo | Ponderazione | Valore di sistema | Calcolo del valore | Percentuale |
|-------------- |--------- |------------- |------------------ |---------- |
|               |          |              |                   |           |
| Responsabile delle decisioni | Vitale | 100 | 100/240 | 41,67% |
| Influencer | Importante | 80 | 80/240 | 33,33% |
| Professionista | Normale | 60 | 60/240 | 25% |
|               | Totale | 240 |                   |           |

#### Esempio di calcolo

L’esempio seguente illustra il calcolo del punteggio di coinvolgimento utilizzando la percentuale di peso del ruolo delineata, il conteggio delle attività in entrata per ogni membro del gruppo di acquisto e un tetto giornaliero di 20 conteggi per ogni evento (se si è verificato più volte).

| Ruolo | Membro | Tipo di attività | Conteggio di ieri | Conteggio odierno | Calcolo | Punteggio totale |
|-------------- |--------- |-------------|-----------------|-------------|------|-----------|
|               |          |             |                 |             |      |           |
| Responsabile delle decisioni | Adam | Sito web visitato | 37 | 15 | 20 + 15 | 35 |
|               |          | E-mail selezionata | 1 | 1 | 1 + 1 | 2 |
|               |          |             |                 |             |      |           |
|               | Contrassegna | Sito web visitato | 5 | 3 | 5 + 3 | 8 |
|               |          | E-mail selezionata | 1 | 1 | 1 + 1 | 2 |
|               |          | Pub scaricato | 3 | 2 | 3 + 2 | 5 |
| **Punteggio totale decision maker** |         |             |                 |             |      | **52** |
|               |          |             |                 |             |      |           |
| Influencer | John | Sito web visitato | 19 | 9 | 19 + 9 | 28 |
| **Punteggio totale influencer** |         |             |                 |             |      | **28** |
|               |          |             |                 |             |      |           |
| Professionista | Bob | E-mail selezionata | 1 | 1 | 1 + 1 | 2 |
|               |          |             |                 |             |      |           |
|               | Paul | E-mail selezionata | 1 | 1 | 1 + 1 | 2 |
|               |          |             |                 |             |      |           |
|               | Calvin | E-mail selezionata | 1 | 1 | 1 + 1 | 2 |
|               |          | Sito web visitato | 1 | 7 | 1 + 7 | 8 |
|               |          | Pub scaricato | 1 | 2 | 1 + 2 | 3 |
| **Punteggio totale professionisti** |         |             |                 |             |      | **17** |

Il punteggio di coinvolgimento finale viene calcolato applicando la ponderazione per ciascuno dei punteggi dei ruoli:

| Ruolo | Punteggio totale mansione | % peso ruolo | Punteggio X peso % |
|-------------- |---------------- |------------- |---------------- |
| Responsabili decisionali | 52 | 41,67% | 21,67 |
| Influencer | 28 | 33,33% | 9,33 |
| Professionisti | 17 | 25% | 4,25 |
| **Punteggio di coinvolgimento finale** |                |             | **35,25** |

## Video introduttivo

>[!VIDEO](https://video.tv.adobe.com/v/3433078/?learn=on)
