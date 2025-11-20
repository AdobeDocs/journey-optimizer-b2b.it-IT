---
title: Seleziona eventi e campi esperienza
description: Seleziona i campi e gli eventi di Experience Platform per attivare il decisioning in tempo reale nei percorsi in base al comportamento del cliente.
feature: Setup, Integrations
role: Admin
badgeBeta: label="Beta" type="informative" tooltip="Questa funzione è attualmente in versione beta"
solution: Journey Optimizer B2B Edition, Experience Platform
exl-id: a7696d03-f4c4-4f64-8ef2-b15e59b59770
source-git-commit: 046d3648c5e482a69719d0095c297a766dd852ea
workflow-type: tm+mt
source-wordcount: '656'
ht-degree: 0%

---

# Seleziona eventi e campi esperienza

Gli amministratori possono selezionare [AEP Experience Events](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/classes/experienceevent){target="_blank"} specifici e i campi associati nello schema di unione Experience Event. Dopo la selezione, gli utenti possono configurare le regole di decisione per ascoltare tali eventi esperienza al fine di abilitare azioni di campagna dinamiche e mirate basate su dati di eventi in tempo quasi reale.

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
>Nella versione beta, non è possibile rimuovere gli eventi dall’elenco. Assicurati che ogni evento aggiunto sia destinato all’utilizzo da parte dell’organizzazione.

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

<!-- ## Overview video

>[!VIDEO](https://video.tv.adobe.com/v/3448637/?learn=on) -->