---
title: Ascolta un evento
description: Scopri il tipo di nodo Ascolta per un evento che puoi utilizzare per orchestrare i percorsi di account in Journey Optimizer B2B edition.
feature: Account Journeys
role: User
exl-id: d852660b-f1da-4da0-86f0-85271f55b79f
source-git-commit: 4a54548ad061fc778fae3bc4b8499f3716850e4a
workflow-type: tm+mt
source-wordcount: '1373'
ht-degree: 8%

---

# Ascoltare un evento

Aggiungi il nodo _Ascolta un evento_ per spostare il pubblico al passaggio successivo nel percorso dell&#39;account quando si verifica un evento.

![Video](../../assets/do-not-localize/icon-video.svg){width="30"} [Guarda il video introduttivo](#overview-video)

>[!NOTE]
>
>Non è possibile aggiungere questo tipo di nodo nel percorso suddiviso da persone.

## Eventi account

Ascolta un evento basato sull’account quando desideri spostare l’account in avanti nel percorso in base agli eventi attivati dall’attività dell’account.

### Eventi e vincoli

| Evento | Vincoli |
| ----- | ----------- |
| L&#39;account ha avuto un momento interessante | Tipo (E-mail, Milestone o Web)<br/>Vincoli aggiuntivi (facoltativo): <li>Descrizione</li><li>Origine</li><li>Data di attività</li> <br/>Timeout (facoltativo) |
| Modifica il valore dei dati dell’account | Attributo<br/>Vincoli aggiuntivi (facoltativo): <li>Nuovo valore</li><li>Valore precedente</li><li>Data di attività</li> <br/>Timeout (facoltativo) |
| Modifica nella fase del gruppo di acquisto | Interesse soluzione<br/>Vincoli aggiuntivi (facoltativo): <li>Nuova fase</li><li>Fase precedente</li><li>Data di attività</li><br/> Timeout (facoltativo) |
| Modifica dello stato del gruppo acquisti | Interesse soluzione<br/>Vincoli aggiuntivi (facoltativo): <li>Nuovo stato</li><li>Stato precedente</li><li>Data di attività</li><br/> Timeout (facoltativo) |
| Modifica del punteggio di completezza | Interesse soluzione<br/>Vincoli aggiuntivi (facoltativo): <li>Nuovo punteggio</li><li>Punteggio precedente</li><li>Data di attività</li><br/> Timeout (facoltativo) |
| Modifica del punteggio di coinvolgimento | Interesse soluzione<br/>Vincoli aggiuntivi (facoltativo): <li>Nuovo punteggio</li><li>Punteggio precedente</li><li>Data di attività</li><br/> Timeout (facoltativo) |

### Aggiungere un evento account

1. Passa alla mappa del percorso.

1. Fai clic sull&#39;icona più ( **+** ) in un percorso e scegli **[!UICONTROL Ascolta un evento]**.

1. Nelle proprietà del nodo a destra, scegliere **[!UICONTROL Account]** per il tipo di evento.

   ![Nodo Percorso - ascolta eventi sull&#39;account](./assets/node-listen-events-account.png){width="700" zoomable="yes"}

1. Seleziona un evento dall’elenco.

1. Fai clic su **[!UICONTROL Modifica evento]** e definisci i dettagli dell&#39;evento.

## Eventi persone

Ascolta un evento basato sulle persone quando desideri spostare l’account in avanti nel percorso in base agli eventi attivati dall’attività delle persone.

### Eventi e vincoli

| Tipo di input | Evento | Vincoli |
| ---------- | ----- | ----------- |
| Journey Optimizer B2B | Assegnato al gruppo acquisti | Interesse soluzione<br/><br/>Vincoli aggiuntivi (facoltativo): <li>Ruolo</li><li>Data di attività</li><br/>Timeout (facoltativo) |
| | Fa clic sul collegamento nell’e-mail | E-mail<br/><br/>Vincoli aggiuntivi (facoltativo): <li>Collegamento</li><li>ID collegamento</li><li>È un dispositivo mobile</li><li>Dispositivo</li><li>Piattaforma</li><li>Browser</li><li>Contenuto predittivo</li><li>È un’attività bot</li><li>Pattern di attività bot</li><li>Browser</li><li>Data di attività</li><li>Min numero di volte</li><br/>Timeout (facoltativo) |
| | Clic sul collegamento nell’SMS | E-mail<br/><br/>Vincoli aggiuntivi (facoltativo): <li>Collegamento</li><li>Dispositivo</li><li>Piattaforma</li><li>Data di attività</li><li>Min numero di volte</li><br/>Timeout (facoltativo) |
| | Modifiche al valore dei dati | Attributo persona<br/><br/>Vincoli aggiuntivi (facoltativo): <li>Nuovo valore</li><li>Valore precedente</li><li>Motivo</li><li>Origine</li><li>Data di attività</li><li>Min numero di volte</li><br/>Timeout (facoltativo) |
| | Apre e-mail | E-mail<br/><br/>Vincoli aggiuntivi (facoltativo): <li>Collegamento</li><li>ID collegamento</li><li>È un dispositivo mobile</li><li>Dispositivo</li><li>Piattaforma</li><li>Browser</li><li>Contenuto predittivo</li><li>È un’attività bot</li><li>Pattern di attività bot</li><li>Browser</li><li>Data di attività</li><li>Min numero di volte</li><br/>Timeout (facoltativo) |
| | Rimosso dal gruppo acquisti | Interesse soluzione<br/>Data di attività (facoltativo)<br/>Timeout (facoltativo) |
| | Il punteggio è cambiato | Nome punteggio<br/><br/>Vincoli aggiuntivi (facoltativo):<li>Cambia</li><li>Nuovo punteggio</li><li>Urgenza</li><li>Priorità</li><li>Punteggio relativo</li><li>Urgenza relativa</li><li>Data di attività</li><li>Min numero di volte</li><br/>Timeout (facoltativo) |
| | Mancati recapiti SMS | Messaggio SMS<br/><br/>Vincoli aggiuntivi (facoltativo): <li>Data di attività</li><li>Numero minimo di volte</li><br/>Timeout (facoltativo) |
| Marketo Engage | Visite alla pagina web | Pagina Web <br/> Selezionare una o più pagine Marketo Engage da associare. <br/><br/>Ulteriori vincoli (facoltativi): <li>Querystring</li><li>Indirizzo IP client</li><li>Referrer</li><li>Agente utente</li><li>Motore di ricerca</li><li>Query di ricerca</li><li>Token</li><li>Browser</li><li>Piattaforma</li><li>Dispositivo</li><li>Data di attività</li> |
| | Compila modulo | Modulo <br/> Selezionare uno o più moduli Marketo Engage da associare.  <br/><br/>Ulteriori vincoli (facoltativi): <li>Data di attività</li><li>Querystring</li><li>Indirizzo IP client</li><li>Referrer</li><li>Agente utente</li><li>Piattaforma</li><li>Dispositivo</li><br/>Timeout (facoltativo) |
| Adobe Experience Platform | Definizione dell’evento | Tipo evento <br/><br/>Vincoli aggiuntivi (facoltativo): <li>Campi</li> <br/>Vincoli aggiuntivi (non supportati): <li>Data di attività</li><li>Min numero di volte</li><br/> Timeout (facoltativo) |

### Aggiungere un evento persone

1. Passa alla mappa del percorso.

1. Fai clic sull&#39;icona più ( **+** ) in un percorso e scegli **[!UICONTROL Ascolta un evento]**.

1. Nelle proprietà del nodo a destra, scegli **[!UICONTROL Persone]** per il tipo di evento.

   ![nodo Percorso - ascolta eventi sulle persone](./assets/node-listen-events-people.png){width="700" zoomable="yes"}

1. Seleziona un evento dall’elenco.

1. Fai clic su **[!UICONTROL Modifica evento]** e definisci i dettagli dell&#39;evento.

### Ascolta evento Marketo Engage

Se nell’istanza di Marketo Engage connessa sono state create pagine web, puoi attivare un evento in base a una visita o a nessuna visita alle pagine web di Marketo Engage, nonché ai moduli Marketo Engage che non sono stati compilati.

1. Selezionare un nodo **[!UICONTROL Ascolta un evento]** nella mappa del percorso.

1. Nelle proprietà del nodo a destra, scegli **[!UICONTROL Persone]** per il tipo di evento.

1. Fai clic sulla freccia per il selettore **[!UICONTROL Seleziona evento persone]** e scorri il menu fino alla sezione **[!UICONTROL Marketo Engage]**.

1. Seleziona un tipo di attività Coinvolgimento nel mercato:

   * **[!UICONTROL Pagina Web Visite]**.
   * **[!UICONTROL Compila modulo]**

   ![Ascolta un evento esperienza](./assets/node-listen-events-people-me-event.png){width="700" zoomable="yes"}

1. Fai clic su **[!UICONTROL Modifica evento]** e definisci una o più pagine Web da associare ed eventuali vincoli aggiuntivi per l&#39;evento.

   * (Obbligatorio) Nella finestra di dialogo _[!UICONTROL Modifica evento]_, definisci il vincolo del modulo **[!UICONTROL Pagina Web]** o Compila. Utilizza **[!UICONTROL is]** (impostazione predefinita) per trovare corrispondenze in una o più pagine o moduli selezionati. Utilizza **[!UICONTROL is not]** per trovare una corrispondenza in tutte le visite/moduli di pagina, con l&#39;esclusione di una o più pagine/moduli selezionati. In alternativa, utilizza **[!UICONTROL è qualsiasi]** da trovare in qualsiasi visita della pagina Web di Marketo Engage o modulo compilato.

   * (Facoltativo) Fare clic su **[!UICONTROL Aggiungi vincolo]** e scegliere il campo da utilizzare per il vincolo. Imposta l’operatore e il valore per il campo.

     ![Ascolta un evento esperienza](./assets/node-listen-events-people-me-event-edit-dialog.png){width="700" zoomable="yes"}

     È possibile ripetere questa azione per includere vincoli di campo aggiuntivi in base alle esigenze.

   * Una volta definiti i vincoli, fare clic su **[!UICONTROL Fine]**.

1. Se necessario, impostare l&#39;opzione **[!UICONTROL Timeout]** per limitare il periodo di tempo per l&#39;ascolto dell&#39;evento (vedere [Aggiungere un timeout a un nodo evento](#add-a-timeout-to-an-event-node)).

1. Nella mappa del percorso, aggiungi il nodo successivo da eseguire quando si verifica l’evento.

### Ascolta un evento esperienza

Gli amministratori possono configurare definizioni di eventi basate su Adobe Experience Platform (AEP), che consentono agli addetti al marketing di creare percorsi di account che reagiscono a [eventi esperienza AEP](https://experienceleague.adobe.com/it/docs/experience-platform/xdm/classes/experienceevent){target="_blank"}. L’utilizzo degli eventi di esperienza di AEP nei percorsi di account è un processo in due fasi:

1. [Crea e pubblica una definizione di evento AEP](../admin/configure-aep-events.md).

2. In un percorso di account, aggiungi un nodo _Ascolta un evento_ e seleziona una definizione di evento Experience Platform per un evento basato su persone.

![Video](../../assets/do-not-localize/icon-video.svg){width="30"} [Guarda la panoramica video](../admin/configure-aep-events.md#overview-video)

_Per includere un evento esperienza nel percorso:_

1. Selezionare un nodo **[!UICONTROL Ascolta un evento]** nella mappa del percorso.

1. Nelle proprietà del nodo a destra, scegli **[!UICONTROL Persone]** per il tipo di evento.

1. Fai clic sulla freccia per il selettore **[!UICONTROL Seleziona evento persone]** e scorri il menu fino alla sezione **[!UICONTROL Adobe Experience Platform]**.

   ![Ascolta un evento esperienza](./assets/node-listen-events-people-aep-events.png){width="700" zoomable="yes"}

1. Seleziona l’evento.

   Il tipo di evento viene visualizzato come vuoto nei dettagli del nodo.

   ![Modifica evento](./assets/node-listen-events-people-aep-events-edit.png){width="400" zoomable="yes"}

1. Fai clic su **[!UICONTROL Modifica evento]** e definisci i tipi di evento ed eventuali vincoli aggiuntivi per l&#39;evento.

   * (Obbligatorio) Nella finestra di dialogo _[!UICONTROL Modifica evento]_, definisci il tipo di evento. È possibile utilizzare l&#39;operatore predefinito **[!UICONTROL is]** per la corrispondenza su uno o più tipi di evento selezionati. In alternativa, è possibile utilizzare l&#39;operatore **[!UICONTROL is not]** per la corrispondenza in tutti i tipi di evento con l&#39;esclusione di uno o più tipi di evento selezionati.

   * (Facoltativo) Fare clic su **[!UICONTROL Aggiungi vincolo]** e scegliere il campo da utilizzare per il vincolo. Imposta l’operatore e il valore per il campo.

     ![Ascolta un evento esperienza](./assets/node-listen-events-people-aep-events-edit-dialog.png){width="700" zoomable="yes"}

     >[!NOTE]
     >
     >I vincoli per _data attività_ e _numero minimo di volte_ non sono supportati.

     È possibile ripetere questa azione per includere vincoli di campo aggiuntivi in base alle esigenze.

   * Una volta definiti i vincoli, fare clic su **[!UICONTROL Fine]**.

1. Se necessario, impostare l&#39;opzione **[!UICONTROL Timeout]** per limitare il periodo di tempo per l&#39;ascolto dell&#39;evento (vedere [Aggiungere un timeout a un nodo evento](#add-a-timeout-to-an-event-node)).

1. Nella mappa del percorso, aggiungi il nodo successivo da eseguire quando si verifica l’evento.

1. Completa i nodi rimanenti del percorso e [pubblicalo](./journey-overview.md).

   Quando il percorso è attivo (pubblicato) e raggiunge il nodo _Ascolta un evento_, inizia l&#39;ascolto degli eventi AEP Experience.

## Aggiungere un timeout a un nodo evento

Se necessario, definisci il tempo di attesa dell’evento da parte del percorso. Il percorso termina dopo un timeout a meno che non si definisca un percorso di timeout in cui è possibile aggiungere altri nodi.

1. Abilita l&#39;opzione **[!UICONTROL Timeout]**.

1. Selezionare la durata per la quale il percorso attende che si verifichi un evento prima del timeout.

   Puoi scegliere di terminare il percorso qui o intraprendere un’azione diversa impostando un altro percorso.

1. Per creare un nuovo percorso nel percorso in cui è possibile aggiungere azioni ed eventi applicabili agli account quando l&#39;evento non si verifica, selezionare la casella di controllo **[!UICONTROL Imposta percorso di timeout]**.

   ![Nodo evento Percorso - imposta percorso timeout](./assets/node-event-timeout-set-path.png){width="700" zoomable="yes"}

## Video di panoramica

>[!VIDEO](https://video.tv.adobe.com/v/3443242/?learn=on&captions=ita)
