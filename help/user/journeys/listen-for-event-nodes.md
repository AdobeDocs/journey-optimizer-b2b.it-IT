---
title: Ascolta un evento
description: 'Configurare i nodi evento per i trigger account e persone: ascolta le modifiche del gruppo di acquisto, i clic e-mail, i riempimenti di moduli ed eventi Experience Platform in Journey Optimizer B2B edition.'
feature: Account Journeys
role: User
exl-id: d852660b-f1da-4da0-86f0-85271f55b79f
source-git-commit: 2a676f3cbeb43616a75fa3fa6eb9106230b9fb40
workflow-type: tm+mt
source-wordcount: '1843'
ht-degree: 4%

---

# Ascoltare un evento

Aggiungi il nodo _Ascolta un evento_ per spostare il pubblico al passaggio successivo nel percorso in cui si verifica un evento.

![Video](../../assets/do-not-localize/icon-video.svg){width=&quot;30&quot;, vertical-align=&quot;middle&quot;} [Guarda il video introduttivo](#overview-video)

>[!NOTE]
>
>Per un percorso di account, non è possibile aggiungere questo tipo di nodo nel percorso suddiviso da persone.

## Eventi account

In un percorso di account, è possibile ascoltare un evento basato sull&#39;account quando si desidera spostare l&#39;account in avanti nel percorso in base agli eventi attivati dall&#39;attività dell&#39;account.

### Eventi e vincoli

| Evento | Vincoli |
| ----- | ----------- |
| [!UICONTROL L&#39;account ha avuto un momento interessante] | Tipo (E-mail, Milestone o Web)<br/>Vincoli aggiuntivi (facoltativo): <li>Descrizione</li><li>Origine</li><li>Data di attività</li> <br/>Timeout (facoltativo) |
| [!UICONTROL Modifica del valore dei dati dell&#39;account] | Attributo<br/>Vincoli aggiuntivi (facoltativo): <li>Nuovo valore</li><li>Valore precedente</li><li>Data di attività</li> <br/>Timeout (facoltativo) |
| [!UICONTROL Modifica in fase gruppo acquisti] | Interesse soluzione<br/>Vincoli aggiuntivi (facoltativo): <li>Nuova fase</li><li>Fase precedente</li><li>Data di attività</li><br/> Timeout (facoltativo) |
| [!UICONTROL Modifica dello stato del gruppo di acquisto] | Interesse soluzione<br/>Vincoli aggiuntivi (facoltativo): <li>Nuovo stato</li><li>Stato precedente</li><li>Data di attività</li><br/> Timeout (facoltativo) |
| [!UICONTROL Modifica del punteggio di completezza] | Interesse soluzione<br/>Vincoli aggiuntivi (facoltativo): <li>Nuovo punteggio</li><li>Punteggio precedente</li><li>Data di attività</li><br/> Timeout (facoltativo) |
| [!UICONTROL Modifica del punteggio di coinvolgimento] | Interesse soluzione<br/>Vincoli aggiuntivi (facoltativo): <li>Nuovo punteggio</li><li>Punteggio precedente</li><li>Data di attività</li><br/> Timeout (facoltativo) |

### Aggiungere un evento account

1. Passa alla mappa del percorso.

1. Fai clic sull&#39;icona più ( **+** ) in un percorso e scegli **[!UICONTROL Ascolta un evento]**.

1. Nelle proprietà del nodo a destra, scegliere **[!UICONTROL Account]** per il tipo di evento.

   ![Nodo Percorso - ascolta eventi sull&#39;account](./assets/node-listen-events-account.png){width="700" zoomable="yes"}

1. Seleziona un evento dall’elenco.

1. Fai clic su **[!UICONTROL Modifica evento]** e definisci i dettagli dell&#39;evento.

## Eventi persone

In un percorso di account, puoi ascoltare un evento basato sulle persone quando desideri spostare l’account in avanti nel percorso in base agli eventi attivati dall’attività delle persone. Puoi anche filtrare gli eventi in base agli attributi delle persone,

### Eventi e vincoli

| Tipo di input | Evento | Vincoli |
| ---------- | ----- | ----------- |
| Journey Optimizer B2B | [!UICONTROL Assegnato al gruppo di acquisto] | Interesse soluzione<br/><br/>Vincoli aggiuntivi (facoltativo): <li>Ruolo</li><li>Data di attività</li><br/>Timeout (facoltativo) |
| | [!UICONTROL Clic sul collegamento nell&#39;e-mail] | E-mail<br/><br/>Vincoli aggiuntivi (facoltativo): <li>Collegamento</li><li>ID collegamento</li><li>È un dispositivo mobile</li><li>Dispositivo</li><li>Piattaforma</li><li>Browser</li><li>Contenuto predittivo</li><li>È un’attività bot</li><li>Pattern di attività bot</li><li>Browser</li><li>Data di attività</li><li>Min numero di volte</li><br/>Timeout (facoltativo) |
| | [!UICONTROL Clic sul collegamento in SMS] | E-mail<br/><br/>Vincoli aggiuntivi (facoltativo): <li>Collegamento</li><li>Dispositivo</li><li>Piattaforma</li><li>Data di attività</li><li>Min numero di volte</li><br/>Timeout (facoltativo) |
| | [!UICONTROL Modifiche al valore dei dati] | Attributo persona<br/><br/>Vincoli aggiuntivi (facoltativo): <li>Nuovo valore</li><li>Valore precedente</li><li>Motivo</li><li>Origine</li><li>Data di attività</li><li>Min numero di volte</li><br/>Timeout (facoltativo) |
| | [!UICONTROL Apre l&#39;e-mail] | E-mail<br/><br/>Vincoli aggiuntivi (facoltativo): <li>Collegamento</li><li>ID collegamento</li><li>È un dispositivo mobile</li><li>Dispositivo</li><li>Piattaforma</li><li>Browser</li><li>Contenuto predittivo</li><li>È un’attività bot</li><li>Pattern di attività bot</li><li>Browser</li><li>Data di attività</li><li>Min numero di volte</li><br/>Timeout (facoltativo) |
| | [!UICONTROL Rimosso dal gruppo di acquisto] | Interesse soluzione<br/>Data di attività (facoltativo)<br/>Timeout (facoltativo) |
| | [!UICONTROL Il punteggio è cambiato] | Nome punteggio<br/><br/>Vincoli aggiuntivi (facoltativo):<li>Cambia</li><li>Nuovo punteggio</li><li>Urgenza</li><li>Priorità</li><li>Punteggio relativo</li><li>Urgenza relativa</li><li>Data di attività</li><li>Min numero di volte</li><br/>Timeout (facoltativo) |
| | [!UICONTROL Mancati recapiti SMS] | Messaggio SMS<br/><br/>Vincoli aggiuntivi (facoltativo): <li>Data di attività</li><li>Numero minimo di volte</li><br/>Timeout (facoltativo) |
| Marketo Engage | [!UICONTROL Pagina Web Visite] | Pagina Web <br/> Selezionare una o più pagine Marketo Engage da associare. <br/><br/>Ulteriori vincoli (facoltativi): <li>Querystring</li><li>Indirizzo IP client</li><li>Referrer</li><li>Agente utente</li><li>Motore di ricerca</li><li>Query di ricerca</li><li>Token</li><li>Browser</li><li>Piattaforma</li><li>Dispositivo</li><li>Data di attività</li> |
| | [!UICONTROL Compila modulo] | Modulo <br/> Selezionare uno o più moduli Marketo Engage da associare. <br/><br/>Ulteriori vincoli (facoltativi): <li>Data di attività</li><li>Querystring</li><li>Indirizzo IP client</li><li>Referrer</li><li>Agente utente</li><li>Piattaforma</li><li>Dispositivo</li><br/>Timeout (facoltativo) |
| Adobe Experience Platform | [!UICONTROL Definizione evento] | Tipo evento <br/><br/>Vincoli aggiuntivi (facoltativo): <li>Campi</li> <br/>Vincoli aggiuntivi (non supportati): <li>Data di attività</li><li>Min numero di volte</li><br/> Timeout (facoltativo) |

### Filtri per eventi Persone

| Filtri | Descrizione |
| ------------ | ----------- |
| [!UICONTROL Cronologia attività] > [!UICONTROL E-mail] | Attività e-mail basate su condizioni valutate utilizzando uno o più messaggi e-mail selezionati di versioni precedenti nel percorso: <li>[!UICONTROL Collegamento selezionato nell&#39;e-mail] <li>E-mail aperta <li>È stato recapitato tramite e-mail <li>E-mail inviata <!-- <br>**[!UICONTROL Switch to inactivity filter]** - Use this option to filter based on lack of activity (a person did not have the email activity).--> |
| [!UICONTROL Cronologia attività] > [!UICONTROL Messaggio SMS] | Attività SMS basate su condizioni valutate utilizzando uno o più messaggi SMS selezionati da in precedenza nel percorso: <li>[!UICONTROL Collegamento selezionato in SMS] <li>[!UICONTROL SMS non recapitato] <!--  <br>**[!UICONTROL Switch to inactivity filter]** - Use this option to filter based on lack of activity (a person did not have the SMS activity). --> |
| [!UICONTROL Cronologia attività] > [!UICONTROL Valore dati modificato] | Per un attributo persona selezionato, si è verificata una modifica del valore. Questi tipi di modifica includono: <li>Nuovo valore<li>Valore precedente<li>Motivo<li>Origine<li>Data di attività<li>Min numero di volte <!--  <br>**[!UICONTROL Switch to inactivity filter]** - Use this option to filter based on lack of activity (a person did not have a data value change). --> |
| [!UICONTROL Cronologia attività] > [!UICONTROL Momento di interesse] | L’attività del momento di interesse definita nell’istanza di Marketo Engage associata. I vincoli includono: <li>Milestone<li>E-mail<li>Web <!-- <br>**[!UICONTROL Switch to inactivity filter]** - Use this option to filter based on lack of activity (a person did not have an interesting moment).--> |
| [!UICONTROL Cronologia attività] > [!UICONTROL Pagina Web visitata] | Attività della pagina web che per una o più pagine web gestite dall’istanza Marketo Engage associata. I vincoli includono: <li>Pagina Web (obbligatoria)<li>Data di attività<li>Indirizzo IP client <li>Querystring <li>Referrer <li>Agente utente <li>Motore di ricerca <li>Query di ricerca <li>URL personalizzato <li>Token <li>Browser <li>Piattaforma <li>Dispositivo <li>Min numero di volte <!-- <br>**[!UICONTROL Switch to inactivity filter]** - Use this option to filter based on lack of activity (a person did not visit the web page). --> |
| [!UICONTROL Attributi della persona] | Attributi dal profilo della persona, tra cui: <li>Città <li>Paese <li>Data di nascita <li>Indirizzo e-mail <li>E-mail non valida <li>E-mail sospesa <li>Nome <li>Area dello stato dedotta<li>Posizione lavorativa <li>Cognome <li>Numero di telefono cellulare <li>Punteggio di coinvolgimento della persona <li>Numero di telefono <li>Codice postale <li>Stato <li>Annulla l&#39;iscrizione <li>Motivo per annullamento abbonamento |
| [!UICONTROL Filtri speciali] > [!UICONTROL Membro del gruppo di acquisto] | La persona è o non è un membro del gruppo di acquisto valutato in base a uno o più dei seguenti criteri: <li>Interesse soluzione</li><li>Stato gruppo acquisti</li><li>Punteggio di completezza</li><li>Punteggio di coinvolgimento</li><li>Ruolo</li> |
| [!UICONTROL Filtri speciali] > [!UICONTROL Membro dell&#39;elenco] | La persona è o non è membro di uno o più elenchi Marketo Engage. |
| [!UICONTROL Filtri speciali] > [!UICONTROL Membro del programma] | La persona è o non è membro di uno o più programmi Marketo Engage. |

### Aggiungere un evento persone

1. Passa alla mappa del percorso.

1. Fai clic sull&#39;icona più ( **+** ) in un percorso e scegli **[!UICONTROL Ascolta un evento]**.

1. Nelle proprietà del nodo a destra, scegli **[!UICONTROL Persone]** per il tipo di evento.

   ![nodo Percorso - ascolta eventi sulle persone](./assets/node-listen-events-people.png){width="700" zoomable="yes"}

1. Seleziona un evento dall’elenco.

1. Fai clic su **[!UICONTROL Modifica evento]** e definisci i dettagli dell&#39;evento.

### Ascolta un evento Marketo Engage

Se nell’istanza Marketo Engage connessa sono presenti pagine web, puoi attivare un evento in base a una visita o a nessuna visita a tali pagine web, nonché ai moduli Marketo Engage che non sono stati compilati.

1. Selezionare un nodo **[!UICONTROL Ascolta un evento]** nella mappa del percorso.

1. Nelle proprietà del nodo a destra, scegli **[!UICONTROL Persone]** per il tipo di evento.

1. Fai clic sulla freccia per il selettore **[!UICONTROL Seleziona evento persone]** e scorri il menu fino alla sezione **[!UICONTROL Marketo Engage]**.

1. Seleziona un tipo di attività Coinvolgimento nel mercato:

   * **[!UICONTROL Pagina Web Visite]**.
   * **[!UICONTROL Compila modulo]**

   ![Ascolta un evento esperienza](./assets/node-listen-events-people-me-event.png){width="700" zoomable="yes"}

1. Fai clic su **[!UICONTROL Modifica evento]** e definisci una o più pagine Web da associare ed eventuali vincoli aggiuntivi per l&#39;evento.

   * (Obbligatorio) Nella finestra di dialogo _[!UICONTROL Modifica evento]_, definisci il vincolo **[!UICONTROL Pagina Web]** o **[!UICONTROL Compila modulo]**. Utilizza **[!UICONTROL is]** (impostazione predefinita) per trovare corrispondenze in una o più pagine o moduli selezionati. Utilizza **[!UICONTROL is not]** per trovare una corrispondenza in tutte le visite/moduli di pagina, con l&#39;esclusione di una o più pagine/moduli selezionati. In alternativa, utilizza l&#39;operatore **[!UICONTROL is any]** per trovare corrispondenze in qualsiasi visita della pagina Web di Marketo Engage o modulo compilato.

   * (Facoltativo) Fare clic su **[!UICONTROL Aggiungi vincolo]** e scegliere il campo da utilizzare per il vincolo. Imposta l’operatore e il valore per il campo.

     ![Ascolta un evento esperienza](./assets/node-listen-events-people-me-event-edit-dialog.png){width="700" zoomable="yes"}

     È possibile ripetere questa azione per includere vincoli di campo aggiuntivi in base alle esigenze.

   * Se necessario, selezionare la scheda **[!UICONTROL Filtri]** per [aggiungere filtri per l&#39;evento](#add-a-filter-to-the-people-event).

   * Una volta definiti i vincoli e i filtri, fare clic su **[!UICONTROL Fine]**.

1. Se necessario, impostare l&#39;opzione **[!UICONTROL Timeout]** per limitare il periodo di tempo per l&#39;ascolto dell&#39;evento (vedere [Aggiungere un timeout a un nodo evento](#add-a-timeout-to-an-event-node)).

1. Nella mappa del percorso, aggiungi il nodo successivo da eseguire quando si verifica l’evento.

### Ascolta un evento esperienza

Gli amministratori possono selezionare [Adobe Experience Platform (AEP) Experience Events](https://experienceleague.adobe.com/it/docs/experience-platform/xdm/classes/experienceevent){target="_blank"}, che consentono agli addetti al marketing di creare percorsi di account e persone che reagiscono agli eventi in tempo reale. L’utilizzo degli eventi esperienza nei percorsi è un processo in due fasi:

1. Un amministratore [seleziona i tipi di evento e i campi di interesse](../admin/configure-aep-events.md#select-an-event) per renderli disponibili in percorsi.

2. In un percorso, aggiungi un nodo _Ascolta un evento_ e seleziona un tipo di evento Experience Platform per un evento basato su persone.

<!--
![Video](../../assets/do-not-localize/icon-video.svg){width="30", vertical-align="middle"} [Watch the video overview](../admin/configure-aep-events.md#overview-video) -->

_Per includere un evento esperienza nel percorso :_

1. Selezionare un nodo **[!UICONTROL Ascolta un evento]** nella mappa del percorso.

1. (Solo percorso di account) Nelle proprietà del nodo a destra, scegli **[!UICONTROL Persone]** per il tipo di evento.

1. Seleziona l’evento.

   Per un **_percorso di account_**, fare clic sulla freccia per il selettore **[!UICONTROL Seleziona evento persone]** e scorrere il menu fino alla sezione **[!UICONTROL Adobe Experience Platform]**.

   ![Ascolta un evento esperienza](./assets/node-listen-events-people-aep-events.png){width="700" zoomable="yes"}

   Per un percorso di persone, fare clic sulla freccia per il selettore **[!UICONTROL Seleziona evento]** e scegliere l&#39;evento.

1. Fare clic su **[!UICONTROL Modifica evento]** e definire uno o più vincoli per l&#39;evento.

   ![Modifica evento](./assets/node-listen-events-people-aep-events-edit.png){width="400" zoomable="yes"}

   I vincoli disponibili vengono definiti come campi gestiti per la configurazione dell’evento.

   * Fare clic su **[!UICONTROL Aggiungi vincolo]** e scegliere il campo che si desidera utilizzare per il vincolo.

   * Completare la condizione per il vincolo.

     È possibile utilizzare l&#39;operatore predefinito **[!UICONTROL is]** per far corrispondere uno o più valori di campo. In alternativa, è possibile utilizzare l&#39;operatore **[!UICONTROL is not]** per la corrispondenza su tutti i valori con l&#39;esclusione di uno o più valori specificati.

     ![Ascolta un evento esperienza](./assets/node-listen-events-people-aep-events-edit-dialog.png){width="700" zoomable="yes"}

   * Se necessario, selezionare la scheda **[!UICONTROL Filtri]** per [aggiungere filtri per l&#39;evento](#add-a-filter-to-the-people-event).

   * (Facoltativo) Fai clic su **[!UICONTROL Aggiungi vincolo]** e ripeti questi passaggi per includere eventuali vincoli di campo aggiuntivi.

   * Una volta definiti i vincoli e i filtri, fare clic su **[!UICONTROL Fine]**.

1. Se necessario, impostare l&#39;opzione **[!UICONTROL Timeout]** per limitare il periodo di tempo per l&#39;ascolto dell&#39;evento (vedere [Aggiungere un timeout a un nodo evento](#add-a-timeout-to-an-event-node)).

1. Nella mappa del percorso, aggiungi il nodo successivo da eseguire quando si verifica l’evento.

1. Completa i nodi rimanenti del percorso e [pubblicalo](./journeys-overview.md).

   Quando il percorso è attivo (pubblicato) e raggiunge il nodo _Ascolta un evento_, inizia l&#39;ascolto degli eventi AEP Experience.

### Aggiungere filtri all’evento persone

(Solo percorsi di account)

1. Dopo aver definito l&#39;evento, selezionare la scheda **[!UICONTROL Filtri]** nella finestra di dialogo _[!UICONTROL Modifica evento]_.

   ![Ascolta il nodo Evento da parte degli utenti - Seleziona la scheda Filtri per modificare l&#39;evento](./assets/node-listen-event-people-edit-event-filters.png){width="700" zoomable="yes"}

1. Aggiungi uno o più filtri per eseguire il targeting delle persone per l’evento.

   * Trascina uno dei [filtri persone](#people-event-filters) dalla navigazione a sinistra e completa la definizione della corrispondenza.

     >[!NOTE]
     >
     >Se hai dei campi persona personalizzati definiti nello schema del pubblico dell&#39;account in Experience Platform, questi campi sono disponibili anche in **[!UICONTROL Attributi]** da usare come attributi persona nei filtri.

   * Ottimizza il filtro applicando la **[!UICONTROL logica filtro]** nella parte superiore. Scegli di far corrispondere tutti i filtri o qualsiasi filtro.

     ![Filtri persona utilizzati in una definizione evento](./assets/node-split-conditions-people.png){width="700" zoomable="yes"}

   * Fai clic su **[!UICONTROL Fine]**.

## Aggiungere un timeout a un nodo evento

Se necessario, definisci il tempo di attesa dell’evento da parte del percorso. Il percorso termina dopo un timeout a meno che non si definisca un percorso di timeout in cui è possibile aggiungere altri nodi.

1. Abilita l&#39;opzione **[!UICONTROL Timeout]**.

1. Selezionare la durata per la quale il percorso attende che si verifichi un evento prima del timeout.

   Puoi scegliere di terminare il percorso qui o intraprendere un’azione diversa impostando un altro percorso.

1. Per creare un nuovo percorso nel percorso in cui è possibile aggiungere azioni ed eventi applicabili agli account quando l&#39;evento non si verifica, selezionare la casella di controllo **[!UICONTROL Imposta percorso di timeout]**.

   ![Nodo evento Percorso - imposta percorso timeout](./assets/node-event-timeout-set-path.png){width="700" zoomable="yes"}

<!-- ## Overview video

>[!VIDEO](https://video.tv.adobe.com/v/3443219/?learn=on) -->
