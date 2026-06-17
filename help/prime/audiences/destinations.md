---
title: Destinazioni
description: Scopri come collegare le destinazioni e attivare gli elenchi di persone statiche in Journey Optimizer B2B Prime per esportare i dati sul pubblico in pubblicità, e-mail e altre piattaforme di marketing.
autotag-review: '2026-06-17T18:30:02.442Z'
TQID: 'https://experienceleague.adobe.com/xO1p-VvIfv1KB77g0l2-fFRHQ0w2hy97vnG1QHpMw8c'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: aed878b8-11d0-487c-828b-d23b2051ec37id: beb5f4be-cec3-471a-9db6-831a77dd3ac9id: c8f3fb27-3167-48ac-a66a-fa4bc3f58dda
subfeature_v2: id: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 1cb68e8933d6b1abba3cc82f154344d1dde51818
workflow-type: tm+mt
source-wordcount: 289
ht-degree: 2%

---

# Destinazioni

Le destinazioni sono integrazioni predefinite che consentono di esportare i dati dell&#39;elenco di persone da [!DNL Adobe Journey Optimizer B2B Prime] a piattaforme di marketing esterne, quali reti pubblicitarie, provider di servizi di posta elettronica e sistemi CRM. In [!DNL Journey Optimizer B2B Prime], attivi [elenchi di persone statiche](./people-lists.md#static-list) (composti da record di persone Marketo Engage) nelle destinazioni in modo che tali tipi di pubblico siano disponibili per il targeting e il coinvolgimento nei canali a valle.

<!-- 
Does not align w/AEP info for Beta

Activating a static list to a destination follows a three-step process:

1. **Connect** — Authenticate and configure a connection to a destination platform.
1. **Map** — Select the static list and map its people attributes to the fields required by the destination.
1. **Schedule** — Define when and how often the list data is exported to the destination.

Destination activations reflect the membership state of the static list at the time of each synch.

## Destination types {#destination-types}

[!DNL Journey Optimizer B2B Prime] supports the following destination types for activating static people lists:

| Type | Description |
|--- |--- |
| Streaming | Real-time API-based connections that push audience membership updates to the destination as they occur. |
| File-based (batch) | Scheduled exports that deliver audience data as structured files to cloud storage or SFTP locations, which the destination platform then ingests. |

-->

## Collega una destinazione {#connect-destination}

1. Nella barra di navigazione a sinistra, espandi **[!UICONTROL Connessioni]** e seleziona **[!UICONTROL Destinazioni]**.

1. Nella scheda _[!UICONTROL Catalogo]_, individua il connettore del tipo di destinazione esterna.

   >[!TIP]
   >
   >È possibile trovare rapidamente il connettore immettendo il nome, ad esempio `LinkedIn`, nella casella di ricerca.

   ![Accedere ai tipi di connettore disponibili](./assets/destinations-catalog.png){width="800" zoomable="yes"}

1. Nella scheda del connettore, fai clic su **[!UICONTROL Configura nuova destinazione]**.

1. Seleziona **[!UICONTROL Nuovo account]** e immetti le credenziali del tuo account.

   ![Connetti un nuovo account di destinazione](./assets/destinations-configure-new.png){width="500"}

1. Fai clic su **[!UICONTROL Connetti alla destinazione]**.

   >[!IMPORTANT]
   >
   >A questo punto, **non** immettere i _[!UICONTROL dettagli di destinazione]_. È necessaria solo la connessione.

1. Rivedi le impostazioni delle azioni di marketing e governance dei dati, quindi fai clic su **[!UICONTROL Salva]**.

La destinazione connessa viene visualizzata nell&#39;elenco nella scheda _[!UICONTROL Sfoglia]_ ed è disponibile per l&#39;attivazione statica dell&#39;elenco.

## Attivare un elenco statico in una destinazione {#activate}

>[!NOTE]
>
>È possibile attivare solo [elenchi di persone statiche](./people-lists.md#static-list) nelle destinazioni in [!DNL Journey Optimizer B2B Prime]. [Gli elenchi dinamici](./people-lists.md#dynamic-lists) non sono idonei per l&#39;attivazione della destinazione.

1. Nella barra di navigazione a sinistra, espandere **[!UICONTROL Gestione marketing]**.

1. Sulla destra nell&#39;elenco delle risorse **[!UICONTROL Marketing]**, seleziona **[!UICONTROL Elenchi persone]**.

   ![Accedi agli elenchi di persone per gestire i tuoi tipi di pubblico](./assets/people-lists.png){width="800" zoomable="yes"}

1. Selezionare la scheda **[!UICONTROL Elenchi statici]**.

1. Individua l’elenco statico da attivare su una destinazione.

1. Fai clic sull&#39;icona _Attiva_ ( ![Attiva icona](../../assets/do-not-localize/icon-falco-activate-dest.svg) ) accanto al nome dell&#39;elenco statico.

1. Selezionare la casella di controllo per la connessione di destinazione configurata.

   ![Destinazioni configurate disponibili per l&#39;attivazione](./assets/static-list-activate-destination-select.png){width="600" zoomable="yes"}

1. Fai clic su **[!UICONTROL Salva]**.

<!--

This method not working for Beta

1. On the _[!UICONTROL Browse]_ tab, locate the destination you want to use for the activation and click the name to open it.

1. Select the **[!UICONTROL Activation data]** tab.

1. Click **[!UICONTROL Activate people lists]**.

1. Select the static people list you want to export and click **[!UICONTROL Next]**.

1. Map the people list attributes to the required fields of the destination schema and click **[!UICONTROL Next]**.

1. Set the export schedule:

   * **[!UICONTROL Frequency]** — Choose how often the list is exported (for example, daily or weekly).
   * **[!UICONTROL Start date]** — Set when the first export should run.

1. Review the activation summary and click **[!UICONTROL Finish]**.

The activation is created and the static list data is exported to the destination according to the defined schedule.

-->
