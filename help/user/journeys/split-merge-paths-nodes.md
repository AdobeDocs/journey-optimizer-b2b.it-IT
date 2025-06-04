---
title: Dividi e unisci percorsi
description: Scopri i tipi di nodo percorsi suddivisi e di unione che puoi utilizzare per orchestrare i percorsi di account in Journey Optimizer B2B edition.
feature: Account Journeys
role: User
exl-id: 563d6a85-504d-4c70-b075-8a9a9e88bd6b
source-git-commit: 9ad8ba495cdae4c88d9422f758ea912ca84e143c
workflow-type: tm+mt
source-wordcount: '2083'
ht-degree: 2%

---

# Dividere e unire i percorsi

Utilizza i nodi del percorso di unione e divisione nel percorso di account per orchestrare i percorsi di account in base alle condizioni definite per gli account o le persone. Puoi segmentare il pubblico del percorso o l’elenco degli account in base alle condizioni, definire un percorso con nodi di azione ed evento per ciascun segmento, quindi combinare i segmenti e continuare il percorso ulteriormente.

![Video](../../assets/do-not-localize/icon-video.svg){width="30"} [Guarda il video introduttivo](#overview-video)

Un nodo _Percorsi suddivisi_ definisce uno o più percorsi segmentati in base ai filtri account o persone.

>[!NOTE]
>
>Sono supportati un massimo di 25 percorsi.

## Dividere i percorsi per account

I percorsi suddivisi per account possono includere azioni ed eventi sia per account che per persone. Questi percorsi possono essere ulteriormente suddivisi.

_Come funziona un percorso di suddivisione per nodo account?_

* Ogni percorso aggiunto include un nodo finale con la possibilità di aggiungere nodi a ogni nodo edge.
* È possibile nidificare il percorso suddiviso per nodi di account (è possibile dividerlo più volte per account).
* La valutazione di ciascun percorso è dall&#39;alto verso il basso. Se un account corrisponde al primo e al secondo percorso, procede solo lungo il primo percorso.
* È possibile combinare due o più percorsi utilizzando un nodo di unione.
* Il nodo supporta la definizione di un percorso _[!UICONTROL Altri account]_, in cui è possibile aggiungere azioni o eventi per account che non corrispondono a uno dei segmenti o percorsi definiti.

![nodo Percorso - percorsi suddivisi per account](./assets/node-split-paths-account.png){width="700" zoomable="yes"}

### Condizioni del percorso dell’account

| Condizioni del percorso | Descrizione |
| --------------- | ----------- |
| Attributi dell’account | Attributi dal profilo dell’account, tra cui: <li>Entrate annuali <li>Città <li>Paese <li>Dimensione dipendente <li>Settore <li>Nome <li>Codice SIC <li>Stato |
| [!UICONTROL Filtri speciali] > [!UICONTROL Ha un gruppo di acquisto] | L’account non ha membri di gruppi di acquisto. Può essere valutato anche in base a uno o più dei seguenti criteri: <li>Interesse soluzione <li>Stato gruppo acquisti <li>Punteggio di completezza <li>Punteggio di coinvolgimento |

### Aggiungere un percorso di suddivisione per nodo account

1. Passa alla mappa del percorso.

1. Fare clic sull&#39;icona più ( **+** ) in un percorso e scegliere **[!UICONTROL Dividi percorsi]**.

   ![Aggiungi nodo percorso - percorsi suddivisi](./assets/add-node-split.png){width="300"}

1. Nelle proprietà del nodo a destra, scegli **[!UICONTROL Account]** per la suddivisione.

1. Per definire una condizione applicabile a _[!UICONTROL Percorso 1]_, fare clic su **[!UICONTROL Applica condizione]**.

   ![Dividi nodo percorso - aggiungi condizione](./assets/node-split-properties-apply-condition.png){width="500"}

1. Nell’editor delle condizioni, aggiungi uno o più filtri per definire il percorso di divisione.

   * Trascina e rilascia gli attributi del filtro dal menu di navigazione a sinistra e completa la definizione della corrispondenza.

   * Ottimizza le condizioni applicando la **[!UICONTROL logica filtro]** nella parte superiore. Scegli di soddisfare tutte le condizioni dell’attributo o qualsiasi condizione.

     ![Dividi nodo percorso - condizioni account filtro logica](./assets/node-split-conditions-accounts.png){width="700" zoomable="yes"}

   * Fai clic su **[!UICONTROL Fine]**.

1. Per aggiungere altri percorsi, fare clic su **[!UICONTROL Aggiungi percorso]** e ripetere i passaggi precedenti per aggiungere le condizioni applicabili al percorso.

   È inoltre possibile etichettare ogni percorso in base a queste condizioni o utilizzare le etichette predefinite.

1. Se necessario, riordinare i percorsi in base alla priorità desiderata per la suddivisione.

   Il filtro dei percorsi viene valutato in ordine decrescente. Ogni account procede lungo il primo percorso corrispondente.

   Fai clic sulle frecce su e giù in alto a destra di ciascuna scheda di percorsi per spostarla in alto o in basso nell’elenco dei percorsi.

   ![Dividi nodo percorso - riordina percorsi](./assets/node-split-reorder-paths-accounts.png){width="500" zoomable="yes"}

1. Abilita l&#39;opzione **[!UICONTROL Altri account]** per definire il percorso predefinito per gli account che non corrispondono ai segmenti/percorsi definiti.

   Se questa opzione non è abilitata, il percorso termina per i conti che non corrispondono a un segmento/percorso definito all’interno della suddivisione.

## Dividi percorsi per persone

I percorsi suddivisi per persone possono includere solo azioni persone. Questi percorsi non possono essere nuovamente suddivisi e uniti automaticamente.

_Come funziona un percorso diviso per nodo persone?_

* I nodi suddivisi per persone funzionano all&#39;interno di una combinazione di _nodo raggruppato_ split-merge. I percorsi suddivisi si uniscono automaticamente in modo che tutte le persone nel pubblico possano passare al passaggio successivo senza perdere il contesto dell’account.
* I nodi Dividi per persone non possono essere nidificati (non è possibile aggiungere un percorso diviso per le persone in un percorso che si trova in questo nodo raggruppato).
* La valutazione di ciascun percorso è dall&#39;alto verso il basso. Se una persona corrisponde per il primo e il secondo percorso, procede solo lungo il primo percorso.
* Il nodo supporta l&#39;utilizzo di _relazioni account-persona_, che consente di filtrare le persone in base al loro ruolo (ad esempio, collaboratore esterno o dipendente a tempo pieno) come definito nella relazione.
* Il nodo supporta la definizione di un percorso _[!UICONTROL Altre persone]_, in cui è possibile aggiungere azioni o eventi per le persone che non corrispondono a uno dei segmenti o percorsi definiti.

![nodo Percorso - percorsi suddivisi per persone](./assets/node-split-paths-people.png){width="700" zoomable="yes"}

### Condizioni del percorso delle persone

| Condizioni del percorso | Descrizione |
| --------------- | ----------- |
| [!UICONTROL Attributi della persona] | Attributi dal profilo della persona, tra cui: <li>Città</li><li>Paese</li><li>Data di nascita</li><li>Indirizzo e-mail</li><li>E-mail non valida</li><li>E-mail sospesa</li><li>Nome</li><li>Area dello stato dedotta</li><li>Posizione lavorativa</li><li>Cognome</li><li>Numero di telefono cellulare</li><li>Numero di telefono</li><li>Codice postale</li><li>Stato</li><li>Annulla l&#39;iscrizione</li><li>Motivo per annullamento abbonamento</li> |
| [!UICONTROL Cronologia attività] > [!UICONTROL E-mail] | Attività e-mail basate su condizioni valutate utilizzando uno o più messaggi e-mail selezionati di versioni precedenti nel percorso: <li>[!UICONTROL Collegamento selezionato nell&#39;e-mail] <li>E-mail aperta <li>E-mail consegnata <li>È stata inviata l&#39;e-mail <br>**[!UICONTROL Passa al filtro di inattività&#x200B;]**. Utilizzare questa opzione per filtrare in base alla mancanza di attività (una persona non aveva l&#39;attività e-mail). |
| [!UICONTROL Cronologia attività] > [!UICONTROL Messaggio SMS] | Attività SMS basate su condizioni valutate utilizzando uno o più messaggi SMS selezionati da in precedenza nel percorso: <li>[!UICONTROL Collegamento selezionato in SMS] <li>[!UICONTROL SMS non recapitato] <br>**[!UICONTROL Passa al filtro di inattività&#x200B;]**. Utilizzare questa opzione per filtrare in base all&#39;assenza di attività (una persona non aveva l&#39;attività SMS). |
| [!UICONTROL Cronologia attività] > [!UICONTROL Valore dati modificato] | Per un attributo persona selezionato, si è verificata una modifica del valore. Questi tipi di modifica includono: <li>Nuovo valore<li>Valore precedente<li>Motivo<li>Origine<li>Data di attività<li>Min numero di volte <br>**[!UICONTROL Passa al filtro di inattività&#x200B;]**. Utilizzare questa opzione per filtrare in base alla mancanza di attività (una persona non ha modificato il valore dei dati). |
| [!UICONTROL Cronologia attività] > [!UICONTROL Momento di interesse] | L’attività del momento di interesse definita nell’istanza di Marketo Engage associata. I vincoli includono: <li>Milestone<li>E-mail<li><br>**[!UICONTROL Passa al filtro di inattività&#x200B;]**. Utilizzare questa opzione per filtrare in base alla mancanza di attività (una persona non ha avuto un momento di interesse). |
| [!UICONTROL Cronologia attività] > [!UICONTROL Pagina Web visitata] | Attività della pagina web che per una o più pagine web gestite dall’istanza Marketo Engage associata. I vincoli includono: <li>Pagina Web (obbligatoria)<li>Data di attività<li>Indirizzo IP client <li>Querystring <li>Referrer <li>Agente utente <li>Motore di ricerca <li>Query di ricerca <li>URL personalizzato <li>Token <li>Browser <li>Piattaforma <li>Dispositivo <li>Min numero di volte <br>**[!UICONTROL Passa al filtro di inattività&#x200B;]**. Utilizzare questa opzione per filtrare in base alla mancanza di attività (una persona non ha visitato la pagina Web). |
| [!UICONTROL Filtri speciali] > [!UICONTROL Membro del gruppo di acquisto] | La persona è o non è un membro del gruppo di acquisto valutato in base a uno o più dei seguenti criteri: <li>Interesse soluzione</li><li>Stato gruppo acquisti</li><li>Punteggio di completezza</li><li>Punteggio di coinvolgimento</li><li>Ruolo</li> |
| [!UICONTROL Filtri speciali] > [!UICONTROL Membro dell&#39;elenco] | La persona è o non è membro di uno o più elenchi Marketo Engage. |
| [!UICONTROL Filtri speciali] > [!UICONTROL Membro del programma] | La persona è o non è membro di uno o più programmi Marketo Engage. |

### Condizioni del percorso account-persona

| Condizioni del percorso | Descrizione |
| --------------- | ----------- |
| [!UICONTROL Ruolo nell&#39;account] | Alla persona è o non è assegnata una mansione nell’account. Vincoli facoltativi: <li>Nome ruolo |

### Aggiungere un percorso suddiviso per nodo persone

>[!NOTE]
>
>Quando si dividono i percorsi in base alle persone, viene inserito automaticamente un nodo _Chiudi percorsi divisi_ per terminare la divisione. Un percorso suddiviso per persone consente solo _di eseguire un&#39;azione_ sui nodi persone.

1. Passa alla mappa del percorso.

1. Fare clic sull&#39;icona più ( **+** ) in un percorso e scegliere **[!UICONTROL Dividi percorsi]**.

   ![Aggiungi nodo percorso - percorsi suddivisi](./assets/add-node-split.png){width="300"}

1. Nelle proprietà del nodo a destra, scegli **[!UICONTROL Persone]** per la suddivisione.

1. Imposta gli **[!UICONTROL attributi utilizzati per le condizioni]**.

   * Scegli **[!UICONTROL Solo attributi persone]** per utilizzare le condizioni relative al profilo persona.
   * Scegliere **[!UICONTROL Solo attributi persona-account]** per utilizzare le condizioni relative all&#39;appartenenza al ruolo della persona all&#39;interno di un account.

1. Per definire una condizione applicabile a _[!UICONTROL Percorso 1]_, fare clic su **[!UICONTROL Applica condizione]**.

1. Nell’editor delle condizioni, aggiungi uno o più filtri per definire il percorso di divisione.

   * Trascina e rilascia uno degli attributi delle persone dalla navigazione a sinistra e completa la definizione della corrispondenza.

     >[!NOTE]
     >
     >Se hai dei campi persona personalizzati definiti nello schema del pubblico dell’account in Experience Platform, questi campi sono disponibili per l’utilizzo come attributi persona in determinate condizioni.

   * Ottimizza le condizioni applicando la **[!UICONTROL logica filtro]** nella parte superiore. Scegli di soddisfare tutte le condizioni dell’attributo o qualsiasi condizione.

     ![Dividi nodo percorso - condizioni logica filtro persona](./assets/node-split-conditions-people.png){width="700" zoomable="yes"}

   * Fai clic su **[!UICONTROL Fine]**.

1. Per aggiungere altri percorsi, fare clic su **[!UICONTROL Aggiungi percorso]** e ripetere i passaggi precedenti per aggiungere le condizioni applicabili al percorso.

   È inoltre possibile etichettare ogni percorso in base a queste condizioni o utilizzare le etichette predefinite.

1. Se necessario, riordinare i percorsi in base alla priorità desiderata per la suddivisione.

   Il filtro dei percorsi viene valutato in ordine decrescente. Ogni persona procede lungo il primo percorso che corrisponde a.

   Fai clic sulle frecce su e giù in alto a destra di ciascuna scheda di percorsi per spostarla in alto o in basso nell’elenco dei percorsi.

   ![Dividi nodo percorso - riordina percorsi](./assets/node-split-reorder-paths-people.png){width="500" zoomable="yes"}

1. Abilita l&#39;opzione **[!UICONTROL Altre persone]** per aggiungere un percorso predefinito per le persone che non corrispondono ai percorsi definiti.

   Se questa opzione non è abilitata, le persone che non corrispondono a un segmento/percorso definito si spostano oltre la divisione e procedono al passaggio successivo nel percorso.

   Quando hai definito le condizioni per ogni percorso per suddividere il pubblico a livello di persone, puoi aggiungere azioni che desideri eseguire sulle persone.

### Filtro attività

Per un percorso suddiviso per persone, puoi definire un percorso in base all’attività della persona relativa a:

* Messaggi e-mail da prima nel percorso
* Messaggi SMS da all’inizio del percorso
* Modifica del valore dei dati nel profilo della persona
* Un momento interessante (tracciato in Marketo Engage) associato a un’e-mail, una pagina web o un’attività cardine
* Visita a una pagina web tracciata in Marketo Engage

>[!BEGINSHADEBOX &quot;Filtro inattività&quot;]

Per ciascuno dei filtri _[!UICONTROL Cronologia attività]_, è possibile abilitare l&#39;opzione **[!UICONTROL Passa a filtro inattività]**. Questa opzione trasforma il filtro in una valutazione per l’assenza di quel tipo di attività. Ad esempio, se desideri creare un percorso per le persone che _**non hanno aperto**_ un&#39;e-mail da prima nel percorso, aggiungi il filtro _[!UICONTROL E-mail]_ > _[!UICONTROL E-mail aperta]_. Abilita l’opzione di inattività e specifica l’e-mail. È consigliabile utilizzare il vincolo _[!UICONTROL Data attività]_ per definire un periodo di tempo per l&#39;inattività.

![Condizione Dividi percorso per persona per l&#39;acquisto dell&#39;iscrizione al gruppo](./assets/node-split-people-condition-inactivity.png){width="700" zoomable="yes"}

>[!ENDSHADEBOX]

### Filtro appartenenza

Nella sezione _[!UICONTROL Filtri speciali]_ sono disponibili più filtri che è possibile utilizzare per valutare l&#39;appartenenza di una persona a un gruppo di acquisto o a un elenco di Marketo Engage. Ad esempio, se desideri creare un percorso per le persone che sono membri di un gruppo di acquisto e a cui è assegnato un ruolo particolare, aggiungi il filtro _[!UICONTROL Filtri speciali]_ > _[!UICONTROL Membro del gruppo di acquisto]_. Per il filtro, impostare l&#39;appartenenza come _true_, selezionare un _[!UICONTROL Interesse per la soluzione]_ associato a uno o più gruppi di acquisto e impostare il _[!UICONTROL Ruolo]_ che si desidera associare.

![Condizione Dividi percorso per persona per l&#39;acquisto dell&#39;iscrizione al gruppo](./assets/node-split-people-condition-buying-group-membership.png){width="700" zoomable="yes"}

>[!BEGINSHADEBOX &quot;Appartenenza all&#39;elenco Marketo Engage&quot;]

In Marketo Engage, _Campagne avanzate_ verifica l&#39;appartenenza ai programmi per assicurarsi che i lead non ricevano e-mail duplicate e non siano membri di più flussi di e-mail contemporaneamente. In Journey Optimizer B2B, puoi verificare che l’iscrizione all’elenco Marketo Engage sia una condizione per il percorso di suddivisione da parte delle persone, in modo da eliminare la duplicazione nelle attività di percorso.

Per utilizzare l&#39;appartenenza a un elenco in una condizione divisa, espandere **[!UICONTROL Filtri speciali]** e trascinare la condizione **[!UICONTROL Membro dell&#39;elenco]** nello spazio del filtro. Completa la definizione del filtro per valutare l’appartenenza a uno o più elenchi Marketo Engage.

![Condizione Dividi percorso in base alle persone per l&#39;iscrizione all&#39;elenco Marketo Engage](./assets/node-split-paths-conditions-people-member-of-list.png){width="700" zoomable="yes"}

>[!ENDSHADEBOX]

## Unisci percorsi

Aggiungi un nodo _Unisci percorsi_ per combinare diversi percorsi suddivisi per account nel percorso.

1. Passa alla mappa del percorso.

1. Fare clic sull&#39;icona più ( **+** ) in un percorso e scegliere **[!UICONTROL Dividi percorsi]**.

1. Fai clic sul nodo diviso per aprirne le proprietà a destra.

1. Fai clic su [!UICONTROL Aggiungi percorso] per creare tre percorsi.

1. Aggiungi una combinazione di azioni ed eventi a ciascun percorso.

1. Fai clic sull&#39;icona più ( **+** ) per uno di questi percorsi e scegli **[!UICONTROL Unisci]** dalle opzioni visualizzate.

   ![nodo Percorso - unisci percorsi](./assets/node-plus-icon-merge-paths.png){width="400"}

1. Nelle proprietà del nodo percorsi unione, seleziona i percorsi che desideri unire.

   ![nodo Percorso - unisci percorsi](./assets/node-merge-select-paths.png){width="600" zoomable="yes"}

   A questo punto, i percorsi vengono uniti in modo che gli account dei percorsi selezionati si combinino in un unico percorso che può continuare a progredire attraverso il percorso.

1. Se necessario, puoi annullare l’unione dei percorsi tornando alle proprietà del nodo percorsi unione e deselezionando la casella di controllo per tutti i percorsi che desideri rimuovere.

## Video di panoramica

>[!VIDEO](https://video.tv.adobe.com/v/3443231/?learn=on)
