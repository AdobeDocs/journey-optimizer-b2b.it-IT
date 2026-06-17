---
title: Ascolta un nodo evento
description: 'Configurare Ascolta per i nodi di un evento in Journey Optimizer B2B edition Prime: imposta i trigger di evento, applica filtri facoltativi e avanza le persone quando si verificano attività o modifiche di dati.'
autotag-review: '2026-06-12T23:00:36.531Z'
TQID: 'https://experienceleague.adobe.com/SBEfrrIKSCnO5x1tGXQTz1EZryH0IKhQx4tuqVn78FI'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: a4b836d9-ffdd-4df3-a62a-f78b830cf059id: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2: id: d0031543-532c-4a26-8f90-01af2b91e6d0id: ba367494-9862-4596-bd6f-299c7e10a46bid: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 3368f815edc0ce817cb7ed371157b63fa548d848
workflow-type: tm+mt
source-wordcount: 233
ht-degree: 8%

---

# Ascolta un nodo evento

Aggiungi il nodo _Ascolta un evento_ per spostare il pubblico al passaggio successivo nel percorso in cui si verifica un evento.

## Trigger evento {#event-triggers}

Ottieni elenco da PM

## Filtri degli eventi {#event-filters}

Ottieni elenco aggiornato da PM

| Filtri | Descrizione |
| ------- | ----------- |
| Cronologia attività > E-mail | Attività e-mail in base a condizioni valutate utilizzando uno o più messaggi e-mail selezionati: <li>Collegamento cliccato nell’e-mail <li>E-mail aperta |
| Cronologia attività > Valore dati modificato | Per un attributo persona selezionato, si è verificata una modifica del valore. Questi tipi di modifica includono: <li>Nuovo valore <li>Valore precedente <li>Motivo <li>Origine <li>Data dell’attività <li> Min numero di volte |

## Aggiungere un nodo evento {#add-event-node}

1. Passa all’area di lavoro del percorso.

1. Fai clic sull&#39;icona più ( **+** ) in un percorso e scegli **[!UICONTROL Ascolta un evento]**.

   ![Fai clic sull&#39;icona Aggiungi nel percorso del percorso](./assets/person-journey-canvas-add-node.png){width="200"}

1. Nelle proprietà del nodo a destra, fai clic su **[!UICONTROL Aggiungi criterio evento]**.

1. Nella finestra di dialogo _[!UICONTROL Modifica evento]_, aggiungi gli eventi da attivare.

   ![Modifica evento - trigger evento](./assets/edit-event-triggers.png){width="600" zoomable="yes"}

1. (Facoltativo) Seleziona la scheda **[!UICONTROL Filtri]** nella finestra di dialogo e aggiungi i criteri di filtro per i trigger.

1. Fai clic su **[!UICONTROL Modifica evento]** e definisci i dettagli dell&#39;evento.

   ![Modifica evento - filtro eventi](./assets/edit-event-filters.png){width="600" zoomable="yes"}

1. Fai clic su **[!UICONTROL Salva]**.

<!--
1. If needed, set the **[!UICONTROL Timeout]** option to limit the time period to listen for the event.

   >[!NOTE]
   >
   >The journey ends after a timeout unless you define a timeout path, where you can add other nodes.

   Enable the **[!UICONTROL Timeout]** option and select the duration for which the journey waits for an event to occur before it times out.

   You can choose to end the path here or take a different course of action by setting another path. To create a new path in the journey where you can add actions and events applicable to accounts when the event does not occur, select the **[!UICONTROL Set timeout path]** check box.

   ![Journey event node - set timeout path](../../user/journeys/assets/node-event-timeout-set-path.png){width="700" zoomable="yes"}
-->

>[!NOTE]
>
>La funzionalità di timeout per Ascolta per un nodo evento non funziona al momento. È pianificata per una versione successiva.
