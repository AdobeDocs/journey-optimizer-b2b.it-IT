---
title: Elenchi di persone dinamiche
description: Definisci le regole di iscrizione e duplica gli elenchi di persone dinamiche in Journey Optimizer B2B Edition.
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
source-git-commit: 734966636b6d2addf014905431fa755f6fe92ee6
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 2%
---

# Elenchi di persone dinamiche

Un [elenco persone](./people-lists.md) dinamico è una raccolta di profili persona definita da regole (filtri). L’appartenenza a un elenco dinamico viene definita utilizzando filtri semplici che fanno riferimento agli attributi e alle attività della persona. L’appartenenza viene mantenuta automaticamente in quanto i profili si qualificano e squalificano in base alla logica del filtro.

Non è possibile aggiungere o rimuovere singoli utenti da un elenco dinamico. Per modificare l&#39;appartenenza all&#39;elenco, aggiornare le relative regole. Se è necessario gestire l&#39;appartenenza manualmente o tramite un percorso, utilizzare un [elenco statico](./people-lists-static.md).

## Imposta regole di appartenenza {#set-membership-rules}

>[!NOTE]
>
>Un elenco dinamico senza regole non ha membri. Per popolare l’elenco, aggiungi almeno un filtro.

1. Apri l&#39;elenco dinamico e seleziona la scheda **[!UICONTROL Regole]**.

1. Fai clic su **[!UICONTROL Modifica regole]**.

   ![Regole di accesso per la creazione di un elenco di persone dinamico](./assets/people-list-dynamic-rules-edit.png){width="700" zoomable="yes"}

1. Nella finestra di dialogo _[!UICONTROL Modifica regole]_, definisci le regole per i profili qualificati trascinando i filtri dal pannello a sinistra.

   Qualifica i profili per l’elenco utilizzando una qualsiasi combinazione di:

   * Cronologia delle attività
   * [!DNL Experience Platform] campi persona abilitati
   * Campi personalizzati
   * Dati di intento
   * Attributi della persona
   * Filtri speciali, ad esempio appartenenza al percorso

   Per ogni filtro aggiunto, fare clic su **[!UICONTROL Aggiungi vincoli]** per perfezionare i criteri corrispondenti. Ottimizza le condizioni applicando la **[!UICONTROL logica del filtro]** nella parte superiore. Puoi scegliere di soddisfare tutte le condizioni, qualsiasi condizione o definire una logica avanzata.

   ![Aggiungere filtri con vincoli per popolare l&#39;elenco dinamico](./assets/people-list-dynamic-rules-edit-filter.png){width="700" zoomable="yes"}

1. Fai clic su **[!UICONTROL Fine]** per salvare le modifiche.

   La scheda **[!UICONTROL Regole]** visualizza i filtri e la logica di filtro per l&#39;elenco e la scheda **[!UICONTROL Membri]** viene aggiornata per riflettere l&#39;appartenenza aggiornata. Per trovare i requisiti del pubblico più aggiornati, utilizzare **[!UICONTROL Aggiorna membri]** nel menu **[!UICONTROL Altro]**.

1. Selezionare la scheda **[!UICONTROL Membri]**.

   I membri qualificati vengono visualizzati nell&#39;elenco dopo un breve ritardo.

   ![Membri generati per un elenco persone dinamico](./assets/people-list-dynamic-members.png){width="700" zoomable="yes"}

>[!NOTE]
>
>Per modificare le regole dell’elenco in qualsiasi momento, puoi ripetere questi passaggi. L’appartenenza all’elenco viene aggiornata in base ai filtri salvati.

<!--

## Duplicate a dynamic list {#duplicate-dynamic-list}

Duplicating a dynamic list replicates its membership filtering so that you can reuse it in a different context.

1. In the _[!UICONTROL Dynamic lists]_ tab, click the _More menu_ ( **...** ) icon next to the list and choose **[!UICONTROL Duplicate]**.

1. Enter a unique **[!UICONTROL Name]** (required) and a **[!UICONTROL Description]** (optional).

   By default, the dialog appends `_copy` to the name of the originating list. Enter a different unique name as needed.

   ![Duplicate list dialog](./assets/people-list-duplicate-dialog.png){width="375"}

1. Click **[!UICONTROL Duplicate]**.
-->
