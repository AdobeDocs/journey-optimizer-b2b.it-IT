---
title: Gruppi acquisti
description: Migliora il marketing basato sugli account con gruppi di acquisto per identificare i responsabili delle decisioni chiave, tenere traccia dei punteggi di coinvolgimento e indirizzare gli account in Journey Optimizer B2B edition.
feature: Buying Groups
role: User
exl-id: ddcd7b62-6a76-4f5e-b6d3-a20944ca8332
source-git-commit: 6f141e08066097c3b5e991e27b6177148fad1fff
workflow-type: tm+mt
source-wordcount: '1194'
ht-degree: 73%

---


# Gruppi acquisti

Per le attività di vendita e marketing B2B, gli account sono fondamentali per qualsiasi strategia. A ogni account è associato un gruppo di persone, che possono essere dipendenti dell’account o collaboratori esterni che utilizzano l’account. Gli account sono gerarchici e prodotti diversi possono essere venduti a diversi livelli nella gerarchia. Ad esempio, Adobe Experience Platform potrebbe essere venduto a livello aziendale a un account di livello dirigenziale. Inoltre, Adobe Photoshop potrebbe essere venduto a un account che rappresenta una divisione o un reparto all’interno di un’organizzazione, ad esempio un reparto progettazione all’interno di un’azienda più grande.

![Diagramma ruoli account](assets/account-roles-diagram.png){width="800"}

Nell’account potrebbe essere presente un sottoinsieme di persone che costituiscono il _gruppo acquisti_. Queste persone alla fine prendono la decisione di acquisto, quindi hanno bisogno di particolare attenzione da parte del marketer e potrebbero aver bisogno di informazioni diverse da quelle delle altre persone associate all’account. I gruppi acquisti possono comprendere un gruppo diverso di persone per diverse linee di prodotti o offerte. Ad esempio, l’approvazione di un acquisto di un prodotto per la sicurezza informatica può richiedere un Chief Information Officer o un Chief Security Officer, e un rappresentante del reparto legale. Per un prodotto di tracciamento dei bug si possono includere tra i membri del gruppo acquisti un VP of Engineering e un direttore IT.

![Icona video](../../assets/do-not-localize/icon-video.svg){width="30"} [Guarda la panoramica video](#overview-video)

## Componenti principali

È possibile aumentare l&#39;efficacia del marketing creando gruppi di acquisto in Journey Optimizer B2B edition che identifichino i membri per gli elenchi degli account target per le soluzioni che i team di vendita sono responsabili della vendita. Prima di iniziare a creare i gruppi acquisti con il team di marketing, accertati di aver definito i componenti principali. Questi componenti sono fondamentali per raggiungere gli obiettivi e le finalità aziendali.

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

Per evitare di sovrascrivere erroneamente l&#39;assegnazione di un membro in un gruppo di acquisto, l&#39;elenco è nell&#39;ordine di precedenza seguito nel sistema per garantire un&#39;assegnazione accurata dei membri. Ad esempio, se un utente del reparto vendite aggiunge manualmente un membro al gruppo acquisti, nessun processo di manutenzione dovrà cambiare tale aggiunta. Seguendo l’ordine di precedenza, vengono applicati i seguenti scenari:

* Se un utente assegna manualmente un membro a un gruppo di acquisto seguito da un processo di manutenzione del gruppo di acquisto che rimuove lo stesso membro dal gruppo di acquisto, il processo di manutenzione **non rimuove** tale membro e non può sostituire l&#39;assegnazione manuale.
* Se un utente assegna manualmente un membro a un percorso di acquisto e questo viene seguito da un nodo attivato che rimuove lo stesso membro dal gruppo di acquisto, l&#39;azione del nodo **non rimuove** tale membro e non può sovrascrivere l&#39;assegnazione manuale.
* Se un nodo di azione del percorso attivato aggiunge un membro a un gruppo di acquisto e viene seguito da un processo di manutenzione del gruppo di acquisto che rimuove lo stesso membro dal gruppo di acquisto, il processo di manutenzione **non rimuove** tale membro e non può sostituire l&#39;assegnazione dell&#39;azione del percorso.

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

Il punteggio di completezza viene utilizzato per determinare se al gruppo di acquisto sono assegnati i membri giusti ai ruoli ed è pronto per essere utilizzato in un percorso di account. Questo punteggio è una percentuale basata sul numero di ruoli all’interno del gruppo acquisti e sul numero di ruoli assegnati con almeno un lead.

Ad esempio, se all’interno di un gruppo acquisti sono presenti quattro ruoli e tre di tali quattro ruoli sono assegnati ad almeno un lead, il gruppo acquisti è completo al 75%.

Il punteggio di completezza del gruppo acquisti viene ricalcolato ogni volta che un gruppo acquisti viene creato o aggiornato.

### Punteggio di coinvolgimento del gruppo acquisti {#engagement-score}

Il punteggio di coinvolgimento si basa sulle attività dei membri del gruppo di acquisto, sulle azioni ponderate e sui ruoli ponderati. Il punteggio risultante viene normalizzato all’interno del tenant/istanza per consentire un confronto coerente e ottenere informazioni fruibili.

Il calcolo del punteggio di coinvolgimento iniziale viene avviato non appena si crea il gruppo di acquisto e viene ricalcolato ogni giorno.

Per informazioni dettagliate sulle attività e sui calcoli dei punteggi di coinvolgimento, vedere [Punteggi di coinvolgimento](./engagement-scores.md).

## Video di panoramica

>[!VIDEO](https://video.tv.adobe.com/v/3433078/?learn=on)
