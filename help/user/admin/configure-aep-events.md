---
title: Seleziona eventi e campi esperienza
description: Seleziona i campi e gli eventi di Experience Platform per attivare il decisioning in tempo reale nei percorsi in base al comportamento del cliente.
feature: Setup, Integrations
role: Admin
badgeBeta: label="Beta" type="informative" tooltip="Questa funzione è attualmente in versione beta"
solution: Journey Optimizer B2B Edition, Experience Platform
exl-id: a7696d03-f4c4-4f64-8ef2-b15e59b59770
source-git-commit: cefd98099bf6524d1d559a47d502990852de1468
workflow-type: tm+mt
source-wordcount: '1463'
ht-degree: 7%

---

# Seleziona eventi e campi esperienza

Gli amministratori possono selezionare [AEP Experience Events](https://experienceleague.adobe.com/it/docs/experience-platform/xdm/classes/experienceevent){target="_blank"} specifici e i campi associati nello schema di unione Experience Event. Dopo la selezione, gli utenti possono configurare le regole di decisione per ascoltare tali eventi esperienza al fine di abilitare azioni di campagna dinamiche e mirate basate su dati di eventi in tempo quasi reale.

<!-- ![Video](../../assets/do-not-localize/icon-video.svg){width="30"} [Watch the video overview](#overview-video) -->
L’utilizzo degli eventi di esperienza di AEP nei percorsi è un processo in due fasi:

1. Un amministratore [aggiunge eventi esperienza AEP e campi](#add-an-event) nelle configurazioni di Journey Optimizer B2B edition.

2. In un percorso, un addetto marketing aggiunge un nodo _Ascolta un evento_ e [seleziona un evento esperienza](../journeys/listen-for-event-nodes.md#listen-for-an-experience-event).

   * Seleziona l&#39;evento da utilizzare nel nodo.
   * Seleziona i campi da utilizzare come vincoli.

>[!BEGINSHADEBOX]

## Linee guida e limitazioni

Quando selezioni gli eventi per raggiungere gli obiettivi organizzativi, tieni presente quanto segue:

* Puoi selezionare fino a 50 eventi e fino a 100 campi per evento.

* I percorsi possono ascoltare gli eventi esperienza acquisiti utilizzando le funzionalità di streaming di Experience Platform, come Web SDK o API HTTP.

* Puoi utilizzare gli eventi esperienza a scopo decisionale all’interno di un percorso, ma non vengono mantenuti. Pertanto, non puoi sfruttare un record storico di eventi esperienza in Journey Optimizer B2B edition.

* Quando utilizzi un evento esperienza e pubblichi il percorso, puoi aggiungere altri campi, ma non puoi rimuovere i campi precedentemente selezionati.

* Puoi fare riferimento a un evento esperienza in più percorsi o utilizzarne uno più di una volta nello stesso percorso.

>[!ENDSHADEBOX]

## Gestire gli eventi esperienza

1. Nel menu di navigazione a sinistra, scegli **[!UICONTROL Amministrazione]** > **[!UICONTROL Configurazioni]**.

1. Fai clic su **[!UICONTROL Classi XDM]** nel pannello intermedio, quindi fai clic sulla scheda **[!UICONTROL Eventi]** per visualizzare l&#39;elenco degli eventi disponibili.

   ![Accedi agli eventi esperienza selezionati](./assets/configurations-xdm-classes-events.png){width="800" zoomable="yes"}

   La tabella è ordinata in base alla colonna _[!UICONTROL Ultimo aggiornamento]_, con gli eventi aggiornati più di recente nella parte superiore per impostazione predefinita.

   Da questa pagina è possibile [selezionare](#add-an-event) e [modificare](#edit-an-event) eventi da utilizzare nei percorsi.

   Per accedere ai dettagli di un evento selezionato, fai clic sul nome dell’evento.

### Filtrare l’elenco degli eventi

Immetti il testo nel campo _[!UICONTROL Ricerca]_ per filtrare gli eventi visualizzati in base a una corrispondenza con il nome dell&#39;evento.

![Filtra l&#39;elenco degli eventi selezionati per nome](./assets/configurations-xdm-classes-events-search.png){width="600" zoomable="yes"}

### Aggiungi un evento

Per rendere disponibile un evento esperienza per un nodo _Ascolta un evento_ in un percorso, selezionare l&#39;evento e i campi supportati.

>[!NOTE]
>
>Nella versione beta, non è possibile rimuovere gli eventi dall’elenco. Assicurati che ogni evento aggiunto sia quello che la tua organizzazione intende utilizzare.

1. Fai clic su **[!UICONTROL Seleziona evento esperienza]** in alto a destra.

   Viene visualizzata la pagina dei dettagli dell’evento. Da questa pagina, puoi scegliere il tipo di evento e i campi.

   ![Dettagli evento per un nuovo evento](./assets/configurations-xdm-classes-events-select-new.png){width="700" zoomable="yes"}

1. Scegli il tipo di evento.

   * Fare clic su **[!UICONTROL Seleziona tipo di evento]**.

   * Nella finestra di dialogo, scegli il tipo di evento.

     Utilizza il campo _[!UICONTROL Ricerca]_ per filtrare l&#39;elenco visualizzato in base al nome. Utilizza il cursore **[!UICONTROL Mostra solo campi selezionati]** per rivedere le selezioni correnti.

     ![Finestra di dialogo Seleziona tipo di evento](./assets/configurations-xdm-classes-select-event-type-dialog.png){width="450" zoomable="yes"}

   * Fai clic su **[!UICONTROL Seleziona]**.

1. Scegli uno o più campi per il tipo di evento.

   * Fare clic su **[!UICONTROL Seleziona campi]**.

   * Nella finestra di dialogo, seleziona i campi che desideri utilizzare come vincoli per gli eventi corrispondenti.

     Utilizza il campo _[!UICONTROL Ricerca]_ per filtrare l&#39;elenco visualizzato in base al nome. Utilizza il cursore **[!UICONTROL Mostra solo campi selezionati]** per rivedere le selezioni correnti.

     ![Finestra di dialogo Seleziona campi](./assets/configurations-xdm-classes-select-fields-dialog.png){width="450" zoomable="yes"}

   * Fai clic su **[!UICONTROL Seleziona]**.

1. Nella pagina dei dettagli dell&#39;evento, fare clic su **[!UICONTROL Salva]**.

L&#39;evento salvato viene visualizzato nell&#39;elenco della scheda _[!UICONTROL Eventi]_.

### Modificare un evento

Modifica i dettagli dell’evento per modificare i campi.

1. Fai clic sul nome dell&#39;evento oppure fai clic sull&#39;icona _Altro menu_ ( **...** ) e scegli **[!UICONTROL Modifica]**.

   ![Fare clic sull&#39;icona Altro](./assets/configurations-xdm-classes-events-more-menu.png){width="500" zoomable="yes"}

1. Fai clic su **[!UICONTROL Modifica campi]** per aggiungere altri campi o rimuovere selezioni esistenti nella finestra di dialogo _[!UICONTROL Seleziona campi]_.

1. Fai clic su **[!UICONTROL Seleziona]** per salvare le selezioni.

### Rimuovere un evento

>[!NOTE]
>
>Per il rilascio Beta di questa funzione, non è possibile rimuovere un evento dall’elenco degli eventi selezionati. La rimozione degli eventi è pianificata per la versione GA.

## Eventi e campi

Per [!DNL Journey Optimizer B2B Edition], alcune attività a livello di persone vengono acquisite come [!DNL Experience Platform] eventi esperienza. Questi eventi vengono memorizzati in un set di dati di sistema che utilizza lo schema XDM Experience Event e include gruppi di campi specifici per il percorso. È possibile utilizzare questi eventi in [!UICONTROL Journey Optimizer B2B edition] come qualsiasi altro evento esperienza.

Ogni evento espone un set definito di campi che possono essere utilizzati nel percorso _Ascolta un evento_ nodi (decisioning basato sugli eventi). Esamina i tipi di evento disponibili e i relativi campi per determinare quale evento e campi utilizzare in questi nodi di percorso:

### E-mail inviata

Questo evento tiene traccia di quando un’e-mail di marketing è stata inviata a una persona.

Tipo evento: `directMarketing.emailSent`

+++Campi

| Nome visualizzato | Percorso |
| ------------ | ---- |
| Identificatore | `_id` |
| Tipo di evento | `eventType` |
| Marca temporale | `timestamp` |
| ID persona | `personID` |
| ID sorgente della persona | `personKey.sourceID` |
| Tipo di origine della persona | `personKey.sourceType` |
| ID istanza sorgente della persona | `personKey.sourceInstanceID` |
| Chiave sorgente della persona | `personKey.sourceKey` |
| ID origine e-mail | `directMarketing.emailSent.mailingKey.sourceID` |
| Tipo di origine e-mail | `directMarketing.emailSent.mailingKey.sourceType` |
| ID istanza origine e-mail | `directMarketing.emailSent.mailingKey.sourceInstanceID ` |
| Chiave sorgente e-mail | `directMailing.emailSent.mailingKey.sourceKey` |
| Nome mailing | `directMarketing.emailSent.mailingName` |
| ID PERCORSO | `_experience.journeyOrchestration.stepEvents.journeyID` |
| ID nodo | `_experience.journeyOrchestration.stepEvents.nodeID` |

+++

### E-mail consegnata

Questo evento tiene traccia di quando un’e-mail è stata recapitata correttamente al servizio e-mail di un utente.

Tipo evento: `directMarketing.emailDelivered `

+++Campi

| Nome visualizzato | Percorso |
| ------------ | ---- |
| Identificatore | `_id` |
| Tipo di evento | `eventType` |
| Marca temporale | `timestamp` |
| ID persona | `personID` |
| ID sorgente della persona | `personKey.sourceID` |
| Tipo di origine della persona | `personKey.sourceType` |
| ID istanza sorgente della persona | `personKey.sourceInstanceID` |
| Chiave sorgente della persona | `personKey.sourceKey` |
| ID origine mailing | `directMarketing.mailingKey.sourceID` |
| Tipo di origine mailing | `directMarketing.mailingKey.sourceType` |
| ID istanza sorgente mailing | `directMarketing.mailingKey.sourceInstanceID` |
| Chiave sorgente mailing | `directMarketing.mailingKey.sourceKey` |
| Nome mailing | `directMarketing.mailingName` |
| ID PERCORSO | `_experience.journeyOrchestration.stepEvents.journeyID` |
| ID nodo | `_experience.journeyOrchestration.stepEvents.nodeID` |

+++

### E-mail aperta

Questo evento tiene traccia di quando una persona ha aperto un’e-mail di marketing.

Tipo evento: `directMarketing.emailOpened`

+++Campi

| Nome visualizzato | Percorso |
| ------------ | ---- |
| Identificatore | `_id` |
| Tipo di evento | `eventType` |
| Marca temporale | `timestamp` |
| ID persona | `personID` |
| ID sorgente della persona | `personKey.sourceID` |
| Tipo di origine della persona | `personKey.sourceType` |
| ID istanza sorgente della persona | `personKey.sourceInstanceID` |
| Chiave sorgente della persona | `personKey.sourceKey` |
| ID origine mailing | `directMarketing.mailingKey.sourceID` |
| Tipo di origine mailing | `directMarketing.mailingKey.sourceType` |
| ID istanza sorgente mailing | `directMarketing.mailingKey.sourceInstanceID` |
| Chiave sorgente mailing | `directMarketing.mailingKey.sourceKey` |
| Nome mailing | `directMarketing.mailingName` |
| È un dispositivo mobile | `device.isMobileDevice` |
| Modello dispositivo | `device.model` |
| Agente utente | `environment.browserDetails.userAgent` |
| Sistema operativo | `environment.operatingSystem` |
| ID PERCORSO | `_experience.journeyOrchestration.stepEvents.journeyID` |
| ID nodo | `_experience.journeyOrchestration.stepEvents.nodeID` |

+++

### E-mail cliccata

Questo evento tiene traccia di quando una persona ha fatto clic su un collegamento in un’e-mail di marketing.

Tipo evento: `directMarketing.emailClicked`

+++Campi

| Nome visualizzato | Percorso |
| ------------ | ---- |
| Identificatore | `_id` |
| Tipo di evento | `eventType` |
| Marca temporale | `timestamp` |
| ID persona | `personID` |
| ID sorgente della persona | `personKey.sourceID` |
| Tipo di origine della persona | `personKey.sourceType` |
| ID istanza sorgente della persona | `personKey.sourceInstanceID` |
| Chiave sorgente della persona | `personKey.sourceKey` |
| ID origine mailing | `directMarketing.mailingKey.sourceID` |
| Tipo di origine mailing | `directMarketing.mailingKey.sourceType` |
| ID istanza sorgente mailing | `directMarketing.mailingKey.sourceInstanceID` |
| Chiave sorgente mailing | `directMarketing.mailingKey.sourceKey` |
| Nome mailing | `directMarketing.mailingName` |
| URL collegamento | `directMarketing.linkURL` |
| È un dispositivo mobile | `device.isMobileDevice` |
| Modello | `device.model` |
| Agente utente | `environment.browserDetails.userAgent` |
| Sistema operativo | `environment.operatingSystem` |
| ID PERCORSO | `_experience.journeyOrchestration.stepEvents.journeyID` |
| ID nodo | `_experience.journeyOrchestration.stepEvents.nodeID` |

+++

### E-mail non recapitata

Questo evento tiene traccia di quando un’e-mail inviata a una persona non viene recapitata.

Tipo evento: `directMarketing.emailBounced`

+++Campi

| Nome visualizzato | Percorso |
| ------------ | ---- |
| Identificatore | `_id` |
| Tipo di evento | `eventType` |
| Marca temporale | `timestamp` |
| ID persona | `personID` |
| ID sorgente della persona | `personKey.sourceID` |
| Tipo di origine della persona | `personKey.sourceType` |
| ID istanza sorgente della persona | `personKey.sourceInstanceID` |
| Chiave sorgente della persona | `personKey.sourceKey` |
| ID origine mailing | `directMarketing.mailingKey.sourceID` |
| Tipo di origine mailing | `directMarketing.mailingKey.sourceType` |
| ID istanza sorgente mailing | `directMarketing.mailingKey.sourceInstanceID` |
| Chiave sorgente mailing | `directMarketing.mailingKey.sourceKey` |
| Nome mailing | `directMarketing.mailingName` |
| E-mail | `directMarketing.email` |
| Codice e-mail non recapitate | `directMarketing.emailBouncedCode` |
| Dettagli e-mail non recapitate | `directMarketing.emailBouncedDetails` |
| ID PERCORSO | `_experience.journeyOrchestration.stepEvents.journeyID` |
| ID nodo | `_experience.journeyOrchestration.stepEvents.nodeID` |

+++

### E-mail non recapitata temporaneamente

Questo evento tiene traccia dei mancati recapiti non permanenti di un’e-mail a una persona.

Tipo evento: `directMarketing.emailBouncedSoft`

+++Campi

| Nome visualizzato | Percorso |
| ------------ | ---- |
| Identificatore | `_id` |
| Tipo di evento | `eventType` |
| Marca temporale | `timestamp` |
| ID persona | `personID` |
| ID sorgente della persona | `personKey.sourceID` |
| Tipo di origine della persona | `personKey.sourceType` |
| ID istanza sorgente della persona | `personKey.sourceInstanceID` |
| Chiave sorgente della persona | `personKey.sourceKey` |
| ID origine mailing | `directMarketing.mailingKey.sourceID` |
| Tipo di origine mailing | `directMarketing.mailingKey.sourceType` |
| ID istanza sorgente mailing | `directMarketing.mailingKey.sourceInstanceID` |
| Chiave sorgente mailing | `directMarketing.mailingKey.sourceKey` |
| Nome mailing | `directMarketing.mailingName` |
| E-mail | `directMarketing.email` |
| Codice e-mail non recapitate | `directMarketing.emailBouncedCode` |
| Dettagli e-mail non recapitate | `directMarketing.emailBouncedDetails` |
| ID PERCORSO | `_experience.journeyOrchestration.stepEvents.journeyID` |
| ID nodo | `_experience.journeyOrchestration.stepEvents.nodeID` |

+++

### Annullamento iscrizione e-mail

Questo evento tiene traccia di quando una persona ha annullato l’abbonamento a un’e-mail di marketing.

Tipo evento: `directMarketing.emailUnsubscribed `

+++Campi

| Nome visualizzato | Percorso |
| ------------ | ---- |
| Identificatore | `_id` |
| Tipo di evento | `eventType` |
| Marca temporale | `timestamp` |
| ID persona | `personID` |
| ID sorgente della persona | `personKey.sourceID` |
| Tipo di origine della persona | `personKey.sourceType` |
| ID istanza sorgente della persona | `personKey.sourceInstanceID` |
| Chiave sorgente della persona | `personKey.sourceKey` |
| ID origine mailing | `directMarketing.mailingKey.sourceID` |
| Tipo di origine mailing | `directMarketing.mailingKey.sourceType` |
| ID istanza sorgente mailing | `directMarketing.mailingKey.sourceInstanceID` |
| Chiave sorgente mailing | `directMarketing.mailingKey.sourceKey` |
| Nome mailing | `directMarketing.mailingName` |
| ID PERCORSO | `_experience.journeyOrchestration.stepEvents.journeyID` |
| ID nodo | `_experience.journeyOrchestration.stepEvents.nodeID` |

+++

### Visita pagina web

Questo tipo di evento è il metodo standard per contrassegnare l’hit come visualizzazione di pagina.

Tipo evento: `web.webpagedetails.pageViews`

+++Campi

| Nome visualizzato | Percorso |
| ------------ | ---- |
| Identificatore | `_id` |
| Tipo di evento | `eventType` |
| Marca temporale | `timestamp` |
| ID persona | `personID` |
| ID sorgente della persona | `personKey.sourceID` |
| Tipo di origine della persona | `personKey.sourceType` |
| ID istanza sorgente della persona | `personKey.sourceInstanceID` |
| Chiave sorgente della persona | `personKey.sourceKey` |
| ID sorgente della pagina web | `web.webPageDetails.webPageKey.sourceID` |
| Tipo di origine della pagina Web | `web.webPageDetails.webPageKey.sourceType` |
| ID istanza sorgente pagina web | `web.webPageDetails.webPageKey.sourceInstanceID` |
| Chiave sorgente della pagina web | `web.webPageDetails.webPageKey.sourceKey` |
| Nome pagina Web | `web.webPageDetails.name` |
| URL della pagina web | `web.webPageDetails.URL` |
| Parametri di query della pagina web | `web.webPageDetails.queryParameters` |
| ID pagina web | `web.webPageDetails.webPageID` |
| Agente utente | `environment.browserDetails.userAgent` |
| URL referrer | `web.webReferrer.URL` |

+++

### Modulo compilato

Questo evento tiene traccia di quando una persona ha compilato un modulo su una pagina web.

Tipo evento: `web.formFilledOut`

+++Campi

| Nome visualizzato | Percorso |
| ------------ | ---- |
| Identificatore | `_id` |
| Tipo di evento | `eventType` |
| Marca temporale | `timestamp` |
| ID persona | `personID` |
| ID sorgente della persona | `personKey.sourceID` |
| Tipo di origine della persona | `personKey.sourceType` |
| ID istanza sorgente della persona | `personKey.sourceInstanceID` |
| Chiave sorgente della persona | `personKey.sourceKey` |
| ID origine modulo web | `web.fillOutForm.webFormKey.sourceID` |
| Tipo di origine modulo Web | `web.fillOutForm.webFormKey.sourceType` |
| ID istanza origine modulo Web | `web.fillOutForm.webFormKey.sourceInstanceID` |
| Chiave origine modulo Web | `web.fillOutForm.webFormKey.sourceKey` |
| ID modulo web | `web.fillOutForm.webFormID` |
| Nome modulo web | `web.fillOutForm.webFormName` |
| Parametri di query della pagina web | `web.webPageDetails.queryParameters` |
| ID pagina web | `web.webPageDetails.webPageID` |
| Agente utente | `environment.browserDetails.userAgent` |
| URL referrer | `web.webReferrer.URL` |

+++

### Collegamento web su cui è stato fatto clic

L&#39;evento segnala che il Web SDK ha registrato automaticamente un clic di collegamento.

Tipo evento: `web.webinteraction.linkClicks`

+++Campi

| Nome visualizzato | Percorso |
| ------------ | ---- |
| Identificatore | `_id` |
| Tipo di evento | `eventType` |
| Marca temporale | `timestamp` |
| ID persona | `personID` |
| ID sorgente della persona | `personKey.sourceID` |
| Tipo di origine della persona | `personKey.sourceType` |
| ID istanza sorgente della persona | `personKey.sourceInstanceID` |
| Chiave sorgente della persona | `personKey.sourceKey` |
| ID sorgente dell’interazione web | `web.webInteraction.webInteractionKey.sourceID` |
| Tipo di origine dell’interazione web | `web.webInteraction.webInteractionKey.sourceType` |
| ID dell’istanza sorgente dell’interazione web | `web.webInteraction.webInteractionKey.sourceInstanceID` |
| Chiave sorgente dell’interazione web | `web.webInteraction.webInteractionKey.sourceKey` |
| ID collegamento interazione web | `web.webInteraction.linkID` |
| URL collegamento interazione web | `web.webInteraction.linkURL` |
| Parametri di query della pagina web | `web.webPageDetails.queryParameters` |
| ID pagina web | `web.webPageDetails.webPageID` |
| Agente utente | `environment.browserDetails.userAgent` |
| URL referrer | `web.webReferrer.URL` |

+++

### Momento interessante

Questo evento tiene traccia di quando è stato registrato un momento interessante per una persona.

Tipo evento: `leadOperation.interestingMoment `

+++Campi

| Nome visualizzato | Percorso |
| ------------ | ---- |
| Identificatore | `_id` |
| Tipo di evento | `eventType` |
| Marca temporale | `timestamp` |
| ID persona | `personID` |
| ID sorgente della persona | `personKey.sourceID` |
| Tipo di origine della persona | `personKey.sourceType` |
| ID istanza sorgente della persona | `personKey.sourceInstanceID` |
| Chiave sorgente della persona | `personKey.sourceKey` |
| Data momento | `leadOperation.interestingMoment.date` |
| Descrizione momento | `leadOperation.interestingMoment.description` |
| Sorgente momento | `leadOperation.interestingMoment.source` |
| Tipo di momento | `leadOperation.interestingMoment.type` |
| ID PERCORSO | `_experience.journeyOrchestration.stepEvents.journeyID` |
| ID nodo | `_experience.journeyOrchestration.stepEvents.nodeID` |

+++

<!-- ## Overview video

>[!VIDEO](https://video.tv.adobe.com/v/3448637/?learn=on) -->