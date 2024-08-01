---
title: Nodi Percorso account
description: Scopri i tipi di nodo che puoi utilizzare per creare i tuoi percorsi di account.
feature: Account Journeys
exl-id: 4edb87d9-cdf8-47a4-968b-6dc76d97b89c
source-git-commit: 78d82aa8b3bb8b8d432eeb187d75e2354dbff3ee
workflow-type: tm+mt
source-wordcount: '1748'
ht-degree: 0%

---

# Nodi del Percorso di account

Dopo aver [creato un percorso di account](journey-overview.md#create-an-account-journey) e [aggiunto il pubblico](journey-overview.md#add-the-account-audience-for-your-journey), crea il percorso utilizzando i nodi. La mappa del percorso fornisce un’area di lavoro in cui puoi creare i tuoi casi d’uso di marketing B2B a più passaggi.

Crea il tuo percorso di account combinando i diversi nodi di azione, evento e orchestrazione come uno scenario multi-passaggio cross-channel. Ogni nodo di un percorso rappresenta un passaggio lungo un percorso logico.

## Nodo Pubblico account

Il nodo [Pubblico account](journey-overview.md#add-the-account-audience-for-your-journey) definisce il pubblico dell&#39;account di input (creato e gestito in Adobe Experience Platform) per il percorso. Questo nodo è sempre il primo e viene creato automaticamente per impostazione predefinita.

## Esegui un&#39;azione

Esegui un’azione come inviare un’e-mail, modificare il punteggio e così via.

**Azione sugli account**: l&#39;azione viene applicata a tutte le persone che fanno parte degli account in questo percorso.

**Azione sulle persone**: l&#39;azione viene applicata a tutte le persone in questo percorso. Un&#39;azione sulle persone può essere utilizzata all&#39;interno del percorso suddiviso da persone o suddiviso da account.

| Contesto del nodo | Funzione | Vincoli |
| ------------ | -------- | ----------- |
| [Persone](#add-a-people-action) | Assegna a gruppo di acquisto | Seleziona interesse soluzione<br/>Seleziona ruolo |
| | Rimuovi dal gruppo di acquisto | Seleziona interesse soluzione |
| | Inviare SMS | Creare un SMS |
| | Aggiungi alla campagna di richiesta Marketo Engage | Seleziona area di lavoro Marketo Engage<br/>Seleziona campagna di richiesta |
| | Cambia partizione persone nel Marketo Engage | Nuova partizione |
| | Momento di interesse della persona | Tipo<br/>Descrizione |
| | Modifica punteggio | Nome punteggio<br/>Modifica |
| | Invia e-mail | Crea nuova e-mail<br/>Seleziona e-mail da Marketo Engage |
| [Account](#add-an-account-action) | Invia avviso vendite | Seleziona interesse soluzione<br/>Invia e-mail a |
| | Aggiungi account a (altro) Percorso | Seleziona Percorso di account live |
| | Aggiorna stato gruppo acquisti | Interesse soluzione<br/>Stato (obbligatorio, massimo 50 caratteri) |
| | Rimuovi account dal Percorso (corrente) | Seleziona Percorso di account live |
| | Momento di interesse dell’account | Tipo (e-mail, milestone o web)<br/>Descrizione (facoltativo) |
| | Valore dati modifica account | Seleziona attributo<br/>Nuovo valore |

### Aggiungi un&#39;azione account

1. Passa all’editor di percorso.

1. Fai clic sull&#39;icona più ( **+** ) in un percorso e scegli **[!UICONTROL Esegui un&#39;azione]**.

   ![Aggiungi nodo percorso - percorsi suddivisi](./assets/add-node-action.png){width="400"}

1. Nelle proprietà del nodo a destra, scegliere **[!UICONTROL Account]** per l&#39;azione.

1. Seleziona un&#39;azione dall&#39;elenco e imposta i valori per l&#39;azione.

   ![nodo Percorso - eseguire un&#39;azione su un account](./assets/node-take-action-account.png){width="700" zoomable="yes"}

### Aggiungi un&#39;azione persone

1. Passa all’editor di percorso.

1. Fai clic sull&#39;icona più ( **+** ) in un percorso e scegli **[!UICONTROL Esegui un&#39;azione]**.

1. Nelle proprietà del nodo a destra, scegli **[!UICONTROL Persone]** per l&#39;azione.

1. Seleziona un&#39;azione dall&#39;elenco e imposta i valori per l&#39;azione.

![nodo Percorso - azione sulle persone](./assets/node-take-action-people.png){width="700" zoomable="yes"}

## Ascolta un evento

Porta il pubblico al passaggio successivo nel percorso quando si verifica un evento.

* Puoi anche definire il tempo che il percorso attende per questo evento. Il percorso termina dopo un timeout.
* Inoltre, puoi scegliere di aggiungere altri nodi nel percorso di timeout.

**Ascolta gli eventi sugli account**: se almeno una persona di un account attiva un evento, l&#39;account passa al passaggio successivo del percorso.

**Ascolta eventi sulle persone**: gli eventi sulle persone possono essere applicati solo su un percorso account; non è disponibile per un nodo suddiviso per persone.

| Contesto del nodo | Funzione | Vincoli |
| ------------ | -------- | ----------- |
| [Persone](#add-a-people-event) | Modifiche al valore dei dati | Attributo<br/>Vincoli aggiuntivi (facoltativo)<br/>Timeout (facoltativo) |
| | Clic sul collegamento nell’e-mail | E-mail<br/>Vincoli aggiuntivi (facoltativo)<br/>Timeout (facoltativo) |
| | Assegnato al gruppo di acquisto | Interesse soluzione<br/>Vincoli aggiuntivi (facoltativo)<br/>Timeout (facoltativo) |
| | Apre l’e-mail | E-mail<br/>Vincoli aggiuntivi (facoltativo)<br/>Timeout (facoltativo) |
| | Punteggio modificato | Nome punteggio<br/>Vincoli aggiuntivi (facoltativo)<br/>Timeout (facoltativo) |
| | Rimosso dal gruppo di acquisto | Interesse soluzione<br/>Data di attività (facoltativo)<br/>Timeout (facoltativo) |
| [Account](#add-an-account-event) | Modifica dello stato del gruppo acquisti | Interesse soluzione<br/>Vincoli aggiuntivi (facoltativo)<br/>Timeout (facoltativo) |
| | Modifica nel punteggio di completezza | Interesse soluzione<br/>Vincoli aggiuntivi (facoltativo)<br/>Timeout (facoltativo) |
| | L&#39;account ha avuto un momento interessante | Tipo<br/>Vincoli aggiuntivi (facoltativo)<br/>Timeout (facoltativo) |
| | Modifica nel punteggio di coinvolgimento | Interesse soluzione<br/>Vincoli aggiuntivi (facoltativo)<br/>Timeout (facoltativo) |
| | Modifica del valore dei dati dell’account | Attributo<br/>Vincoli aggiuntivi (facoltativo)<br/>Timeout (facoltativo) |

### Aggiungere un evento account

1. Passa all’editor di percorso.

1. Fai clic sull&#39;icona più ( **+** ) in un percorso e scegli **[!UICONTROL Ascolta un evento]**.

1. Nelle proprietà del nodo a destra, scegliere **[!UICONTROL Account]** per il tipo di evento.

   ![Nodo Percorso - ascolta eventi sull&#39;account](./assets/node-listen-events-account.png){width="700" zoomable="yes"}

1. Seleziona un evento dall’elenco.

1. Fai clic su **[!UICONTROL Modifica evento]** e definisci i dettagli dell&#39;evento.

### Aggiungere un evento persone

1. Passa all’editor di percorso.

1. Fai clic sull&#39;icona più ( **+** ) in un percorso e scegli **[!UICONTROL Ascolta un evento]**.

1. Nelle proprietà del nodo a destra, scegli **[!UICONTROL Persone]** per il tipo di evento.

   ![nodo Percorso - ascolta eventi sulle persone](./assets/node-listen-events-people.png){width="700" zoomable="yes"}

1. Seleziona un evento dall’elenco.

1. Fai clic su **[!UICONTROL Modifica evento]** e definisci i dettagli dell&#39;evento.

### Aggiungere un timeout a un nodo evento

Se necessario, definisci il tempo di attesa dell’evento da parte del percorso. Il percorso termina dopo il timeout.

1. Attiva/disattiva timeout.

1. Selezionare la durata per la quale il percorso attende che si verifichi un evento prima del timeout.

   Puoi scegliere di terminare il percorso qui o intraprendere un’azione diversa impostando un altro percorso.

1. Per creare un nuovo percorso nel percorso in cui è possibile aggiungere azioni ed eventi applicabili agli account quando l&#39;evento non si verifica, selezionare la casella di controllo **[!UICONTROL Imposta percorso di timeout]**.

   ![Nodo evento Percorso - imposta percorso timeout](./assets/node-event-timeout-set-path.png){width="700" zoomable="yes"}

## Dividi percorsi

Dividi il pubblico in base alle condizioni del filtro.

>[!NOTE]
>
>Sono supportati un massimo di 25 percorsi.

**Dividi percorsi per account**: i percorsi suddivisi per account possono includere azioni ed eventi sia per account che per persone e possono essere ulteriormente suddivisi.

_Come funziona un percorso di suddivisione per nodo account?_

* Quando aggiungi un nodo di percorso diviso e scegli _Account_, ogni percorso aggiunto include un nodo finale con la possibilità di aggiungere nodi a ogni nodo perimetrale.
* È possibile suddividere il percorso per account ripetutamente, ad esempio in modo nidificato. Un percorso diviso include un&#39;opzione che consente di non aggiungere il percorso predefinito.
* Gli account o le persone che non sono idonei per uno dei percorsi suddivisi non avanzano nel percorso.
* Questi percorsi possono essere combinati utilizzando un nodo di unione.

![nodo Percorso - percorsi suddivisi per account](./assets/node-split-paths-account.png){width="700" zoomable="yes"}

**Dividi percorsi per persone**: i percorsi suddivisi per persone possono includere solo azioni di persone e non possono essere suddivisi di nuovo. I percorsi si uniscono automaticamente.

_Come funziona un percorso diviso per nodo persone?_

* I nodi di suddivisione del percorso per persone sono nodi raggruppati. Si uniscono automaticamente in modo che tutte le persone nel pubblico possano passare al passaggio successivo senza perdere il contesto degli account a cui appartengono.
* Il percorso di divisione per le persone non può essere nidificato. Non è possibile aggiungere il percorso di divisione per le persone in un percorso che si trova in questo nodo raggruppato.
* Il percorso suddiviso include un&#39;opzione che consente di non aggiungere un percorso predefinito. Gli account/persone che non sono idonei non avanzano nel Percorso.

![nodo Percorso - percorsi suddivisi per persone](./assets/node-split-paths-people.png){width="700" zoomable="yes"}

| Contesto del nodo | Condizioni del percorso | Descrizione |
| ------------ | -------- | ----------- |
| [Persone](#add-a-split-path-by-people-node) | Attributi della persona | |
| | Valore dei dati modificato (ad esempio filtro sulla cronologia delle attività) | |
| | E-mail aperta | |
| | Collegamento selezionato nell’e-mail | |
| | Collegamento selezionato nella pagina Web | |
| | Ha avuto un momento interessante | |
| | Membro del gruppo di acquisto | |
| [Account](#add-a-split-path-by-account-node) | Modifica del valore dei dati dell’account (ad esempio filtro sulla cronologia delle attività) | |

### Aggiungere un percorso di suddivisione per nodo account

1. Passa all’editor di percorso.

1. Fare clic sull&#39;icona più ( **+** ) in un percorso e scegliere **[!UICONTROL Dividi percorsi]**.

   ![Aggiungi nodo percorso - percorsi suddivisi](./assets/add-node-split.png){width="300"}

1. Nelle proprietà del nodo a destra, scegli **[!UICONTROL Account]** per la suddivisione.

1. Per definire una condizione applicabile a _[!UICONTROL Percorso 1]_, fare clic su **[!UICONTROL Applica condizione]**.

   ![Dividi nodo percorso - aggiungi condizione](./assets/node-split-properties-apply-condition.png){width="500"}

1. Nell’editor delle condizioni, aggiungi uno o più filtri per definire il percorso di divisione.

   * Trascina e rilascia gli attributi del filtro dal menu di navigazione a sinistra e completa la definizione della corrispondenza.

   * Ottimizza le condizioni applicando la **[!UICONTROL logica filtro]** nella parte superiore. Scegli di soddisfare tutte le condizioni dell’attributo o qualsiasi condizione.

     ![Dividi nodo percorso - logica filtro condizioni](./assets/node-split-conditions.png){width="700" zoomable="yes"}

   * Fai clic su **[!UICONTROL Fine]**.

1. Per aggiungere altri percorsi, fare clic su **[!UICONTROL Aggiungi percorso]** e ripetere i passaggi precedenti per aggiungere le condizioni applicabili al percorso.

   È inoltre possibile etichettare ogni percorso in base a queste condizioni o utilizzare le etichette predefinite.

1. (Facoltativo) Aggiungi un percorso predefinito per gli account non qualificati per gli altri percorsi. In caso contrario, il percorso termina per questi account.

   ![Proprietà nodo percorso suddiviso - altri account](./assets/node-split-properties-other-accounts.png){width="700" zoomable="yes"}

### Aggiungere un percorso suddiviso per nodo persone

1. Passa all’editor di percorso.

1. Fare clic sull&#39;icona più ( **+** ) in un percorso e scegliere **[!UICONTROL Dividi percorsi]**.

   ![Aggiungi nodo percorso - percorsi suddivisi](./assets/add-node-split.png){width="300"}

1. Nelle proprietà del nodo a destra, scegli **[!UICONTROL Persone]** per la suddivisione.

1. Per definire una condizione applicabile a _[!UICONTROL Percorso 1]_, fare clic su **[!UICONTROL Applica condizione]**.

1. Nell’editor delle condizioni, aggiungi uno o più filtri per definire il percorso di divisione.

   * Trascina e rilascia gli attributi del filtro dal menu di navigazione a sinistra e completa la definizione della corrispondenza.

   * Ottimizza le condizioni applicando la **[!UICONTROL logica filtro]** nella parte superiore. Scegli di soddisfare tutte le condizioni dell’attributo o qualsiasi condizione.

   * Fai clic su **[!UICONTROL Fine]**.

1. Per aggiungere altri percorsi, fare clic su **[!UICONTROL Aggiungi percorso]** e ripetere i passaggi precedenti per aggiungere le condizioni applicabili al percorso.

   È inoltre possibile etichettare ogni percorso in base a queste condizioni o utilizzare le etichette predefinite.

1. Infine, puoi aggiungere un percorso predefinito per le persone non qualificate per i percorsi di cui sopra. In caso contrario, il percorso finirà per queste persone

Quando hai definito le condizioni per ogni percorso su cui stai suddividendo il pubblico a livello di persone, puoi aggiungere azioni che desideri eseguire su altre persone.

>[!NOTE]
>
>Quando dividi il pubblico per persone, puoi aggiungere solo azioni persone.

## Attendere

Attendi un certo periodo di tempo prima di passare al passaggio successivo.

1. Passa all’editor di percorso.

1. Fai clic sull&#39;icona più ( **+** ) in un percorso e scegli **[!UICONTROL Attendi]**.

1. Nelle proprietà del nodo a destra, imposta la **[!UICONTROL Durata]** di tempo di attesa prima che il percorso proceda al nodo successivo nel percorso.

![nodo Percorso - attendi](./assets/node-wait.png){width="700" zoomable="yes"}

## Unisci percorsi

Utilizzando questo nodo è possibile unire e separare percorsi diversi nel percorso.

1. Passa all’editor di percorso.

1. Fare clic sull&#39;icona più ( **+** ) in un percorso e scegliere **[!UICONTROL Dividi percorsi]**.

1. Fai clic sul nodo diviso per aprirne le proprietà a destra.

1. Fai clic su [!UICONTROL Aggiungi percorso] per creare tre percorsi.

1. Aggiungi una combinazione di azioni ed eventi a ciascun percorso.

1. Fai clic sull&#39;icona più ( **+** ) per uno di questi percorsi e scegli **[!UICONTROL Unisci]** dalle opzioni visualizzate.

   ![nodo Percorso - unisci percorsi](./assets/node-plus-icon-merge-paths.png){width="400"}

1. Nelle proprietà del nodo di unione, seleziona i percorsi che desideri unire.

   ![nodo Percorso - unisci percorsi](./assets/node-merge-select-paths.png){width="600" zoomable="yes"}

   Ora puoi vedere che i percorsi vengono uniti in modo che gli account dei percorsi selezionati si combinino in un unico percorso e possano continuare a progredire attraverso il percorso.

1. Se necessario, puoi annullare l’unione dei percorsi tornando alle proprietà del nodo di unione e deselezionando la casella di controllo di tutti i percorsi che desideri rimuovere.
