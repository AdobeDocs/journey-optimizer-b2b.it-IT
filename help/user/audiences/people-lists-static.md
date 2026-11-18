---
title: Elenchi di persone statiche
description: Aggiungere e rimuovere membri per gli elenchi di persone statiche in Journey Optimizer B2B Edition.
feature: Audiences
role: User
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
    internal-label: Journey Optimizer B2B Edition
feature_v2:
  - id: beb5f4be-cec3-471a-9db6-831a77dd3ac9
    internal-label: Audiences
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: ff2b9b37-92e0-45fc-b853-379d44c08c89
    internal-label: Audience segmentation
source-git-commit: d713d57bddf2ac6f8cf7e7a7d163281f607d729c
workflow-type: tm+mt
source-wordcount: '462'
ht-degree: 2%
---

# Elenchi di persone statiche

Un [elenco persone](./people-lists.md) statico è una raccolta di profili di persone la cui appartenenza cambia solo quando si aggiungono o rimuovono persone. I filtri semplici che fanno riferimento agli attributi e alle attività delle persone definiscono l’iscrizione a un elenco statico. L&#39;appartenenza cambia solo quando si aggiungono o rimuovono membri. Puoi eseguire le seguenti operazioni:

* [Aggiungi persone](#static-list-add-members) applicando un set di filtri valutato una volta, quando lo applichi.
* Aggiungere e rimuovere persone tramite un account o un percorso di persone utilizzando le azioni [!UICONTROL Aggiungi all&#39;elenco persone] e [!UICONTROL Rimuovi dall&#39;elenco persone]. (Vedi [Utilizzare gli elenchi di persone nei percorsi](./people-lists-journeys.md))
<!-- * [Activate the list to a destination](#static-list-activate) to sync its membership downstream. -->

>[!NOTE]
>
>Le definizioni dei filtri elenco statici vengono applicate una sola volta, quando si aggiungono membri all&#39;elenco. Il filtro definito non è disponibile in seguito. Se desideri mantenere una definizione del pubblico coerente utilizzando i filtri, utilizza invece un [elenco dinamico](./people-lists-dynamic.md).

## Aggiungi membri {#static-list-add-members}

>[!NOTE]
>
>Se desideri che un elenco statico inizi vuoto, non applicare filtri. Un elenco statico vuoto è utile quando si prevede di aggiungere membri tramite percorsi.

1. Apri l&#39;elenco statico e fai clic su **[!UICONTROL Aggiungi persone]** in alto a destra.

   ![Aggiungi persone a un elenco di persone statiche](./assets/people-list-static-add-people.png){width="700" zoomable="yes"}

1. Nella finestra di dialogo _[!UICONTROL Aggiungi persone]_, definisci le regole per i profili qualificati trascinando i filtri dal pannello a sinistra.

   Filtra i profili utilizzando una qualsiasi combinazione di:

   * Cronologia delle attività
   * Campi persona abilitati per Experience Platform
   * Campi personalizzati
   * Dati di intento
   * Attributi della persona
   * Filtri speciali, ad esempio appartenenza al percorso

   I filtri sono nidificati nelle cartelle delle categorie. Espandere ogni cartella e scorrere i filtri disponibili oppure utilizzare il campo _Cerca_ nella parte superiore per individuare il filtro necessario. Per ogni filtro aggiunto:

   * Trascina il filtro dal pannello di sinistra allo spazio di definizione del filtro.
   * Completa la definizione della valutazione della corrispondenza.
   * Fai clic su **[!UICONTROL Aggiungi vincoli]** per perfezionare i criteri di corrispondenza.

   Ottimizza le condizioni applicando la **[!UICONTROL logica del filtro]** nella parte superiore. Puoi scegliere di soddisfare tutte le condizioni, qualsiasi condizione o definire una logica avanzata.

   ![Aggiungere filtri con vincoli per aggiungere persone all&#39;elenco statico](./assets/people-list-static-add-people-filters.png){width="800" zoomable="yes"}

1. Fai clic su **[!UICONTROL Fine]** per salvare le modifiche.

   Il sistema elabora la richiesta e visualizza un messaggio di conferma quando vengono aggiunte persone. Il tempo di elaborazione dipende dal numero di persone da valutare e dai criteri di filtro selezionati. Mentre l&#39;elenco continua a essere popolato, utilizzare **[!UICONTROL Aggiorna membri]** nel menu _[!UICONTROL Altro]_ per aggiornare l&#39;elenco.

   I membri qualificati vengono visualizzati nell&#39;elenco dopo un breve ritardo. Il set di filtri viene valutato una volta, pertanto le persone che in seguito corrispondono ai filtri non vengono aggiunte automaticamente. Puoi ripetere questa procedura in qualsiasi momento per aggiungere più persone all’elenco.

   ![Membri per un elenco di persone statiche](./assets/people-list-static-members.png){width="700" zoomable="yes"}

## Rimuovi membri {#static-list-remove-members}

È possibile rimuovere automaticamente le persone da un elenco statico tramite un percorso utilizzando l&#39;azione [!UICONTROL Rimuovi da elenco persone]. (Vedi [Utilizzare gli elenchi di persone nei percorsi](./people-lists-journeys.md))

<!--
TODO: Restore this section when the activate to a destination function is released.

## Activate to a destination {#static-list-activate}

Activating a static people list sends its membership to a connected destination, with ongoing sync instead of a one-time export. This is useful for paid media targeting, suppression, and downstream orchestration.

* The static list acts as a container for the people.
* The activation sends and syncs that membership to a destination.
* People added to the list later are propagated automatically.
* People removed later are deactivated automatically.

>[!PREREQUISITES]
>
>You must have one or more configured destinations for your [!DNL Journey Optimizer B2B Edition] sandbox before you can activate a static list to a destination. See [Destinations](./destinations.md).

1. Select the **[!UICONTROL Static lists]** tab.

1. Locate the static list that you want to activate, click the _More menu_ ( **...** ) icon next to the list, and choose **[!UICONTROL Activate to destination]**.

   ![Access the More menu for a static people list](./assets/people-lists-static-more-menu.png){width="450"}

   You can also open the static list and use the **[!UICONTROL More]** menu at the top right.

1. Select the check box for the configured destination connection.

   ![Configured destinations available for activation](./assets/people-list-activate-destination-select.png){width="600" zoomable="yes"}

1. Click **[!UICONTROL Save]**.

1. In the _[!UICONTROL Activate list to destination]_ dialog, click **[!UICONTROL Activate]** to confirm.

When activation completes, a confirmation message appears and the destination shows as **[!UICONTROL Active]** on the **[!UICONTROL Destinations]** tab of the list. You can activate a static list to more than one destination at a time. Membership syncs to all of them.

To review the destinations that a static list is activated to, open the list and select the **[!UICONTROL Destinations]** tab.

### Deactivate a destination {#deactivate-destination}

Remove a destination connection from a static list when you no longer want its membership synced downstream.

1. Open the static list and select the **[!UICONTROL Destinations]** tab.

1. Use the row action to remove the destination that you want to disconnect.

1. Confirm in the _[!UICONTROL Deactivate destination]_ dialog.

Deactivating removes the destination from the list. The people in the list are also removed from the connected destination audience.

-->
