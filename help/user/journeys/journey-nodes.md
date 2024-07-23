---
title: Nodi del Percorso di account
description: Scopri i tipi di nodo che puoi utilizzare per creare i tuoi percorsi di account.
feature: Account Journeys
exl-id: 4edb87d9-cdf8-47a4-968b-6dc76d97b89c
source-git-commit: dc8301ba755aaf457b955ffbb9c6f0eff6d5a295
workflow-type: tm+mt
source-wordcount: '1544'
ht-degree: 0%

---

# Nodi del Percorso di account

Dopo aver [creato un percorso di account](journey-overview.md#create-an-account-journey) e [aggiunto il pubblico](journey-overview.md#add-the-account-audience-for-your-journey), crea il percorso utilizzando i nodi.

## Tipi di nodo

| Tipo di nodo | Funzione |
| --------- | ------- |
| [Pubblico account](journey-overview.md#add-the-account-audience-for-your-journey) | Pubblico dell&#39;account di input per il percorso. Questo nodo è sempre il primo e viene creato automaticamente per impostazione predefinita |
| [Azione sulle persone](#add-a-people-action) | Invia e-mail |
| | Modifica punteggio |
| | Assegna persona a gruppo di acquisto |
| | Rimuovi persona dal gruppo di acquisto |
| | Aggiungi a Marketo Campaign |
| | Crea momento di interesse lead |
| [Azione sugli account](#add-an-account-action) | Modifica valore dati |
| | Rimuovi account dal Percorso (corrente) |
| | Aggiungi account a (altro) Percorso |
| | Crea momento di interesse per l’account |
| | Aggiungi a elenco account Marketo (implicito) |
| [Eventi per persone](#add-a-people-event) | Modifiche al valore dei dati |
| | Modifica punteggio |
| | Apre l’e-mail |
| | Clic sul collegamento nell’e-mail |
| | Clic sul collegamento nella pagina web |
| | Assegnato al gruppo di acquisto |
| | Rimosso dal gruppo di acquisto |
| [Eventi per account](#add-an-account-event) | Modifica del valore dei dati dell’account |
| | Ha un momento interessante |
| [Dividi per persone](#add-a-split-path-by-people-node) | Attributi lead |
| | Valore dei dati modificato (ad esempio filtro sulla cronologia delle attività) |
| | E-mail aperta |
| | Collegamento selezionato nell’e-mail |
| | Collegamento selezionato nella pagina Web |
| | Ha avuto un momento interessante |
| | Membro del gruppo di acquisto |
| [Dividi per account](#add-a-split-path-by-account-node) | Modifica del valore dei dati dell’account (ad esempio filtro sulla cronologia delle attività) |
| [Attendi](#wait) | Disponibile a livello di account |
| [Unisci percorsi](#merge-paths) | |

## Esegui un&#39;azione

Esegui un’azione come inviare un’e-mail, modificare il punteggio e così via.

**Azione sugli account**: l&#39;azione viene applicata a tutte le persone che fanno parte degli account in questo percorso.

**Azione sulle persone**: l&#39;azione viene applicata a tutte le persone in questo percorso. Un&#39;azione sulle persone può essere utilizzata all&#39;interno del percorso suddiviso da persone o suddiviso da account.

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

## Dividere i percorsi

Dividi il pubblico in base alle condizioni del filtro.

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

>[!NOTE]
>
>Sono supportati un massimo di 25 percorsi.

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
>Quando dividi il pubblico per persone, puoi solo aggiungere azioni persone.

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

