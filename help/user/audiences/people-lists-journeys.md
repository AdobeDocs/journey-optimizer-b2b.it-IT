---
title: Usa elenchi persone in Percorsi
description: Utilizzare gli elenchi persone per aggiungere o rimuovere persone in modo dinamico e per suddividere i percorsi di percorso in base all'appartenenza a un elenco in Journey Optimizer B2B Edition.
feature: Audiences, Person Journeys, Account Journeys
role: User
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
    internal-label: Journey Optimizer B2B Edition
feature_v2:
  - id: beb5f4be-cec3-471a-9db6-831a77dd3ac9
    internal-label: Audiences
  - id: a4b836d9-ffdd-4df3-a62a-f78b830cf059
    internal-label: Journeys
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: d00e9f03-e50b-4162-b143-0c0817c937c2
    internal-label: Customer journeys
source-git-commit: d713d57bddf2ac6f8cf7e7a7d163281f607d729c
workflow-type: tm+mt
source-wordcount: '829'
ht-degree: 0%
---

# Utilizzare gli elenchi di persone nei percorsi

È possibile incorporare [elenchi di persone](./people-lists.md) nei percorsi di account e nei percorsi di persone in diversi modi:

* **Gestisci un elenco statico da un percorso** - In un nodo _Esegui un&#39;azione_, utilizza l&#39;azione _[!UICONTROL Aggiungi all&#39;elenco persone]_ o _[!UICONTROL Rimuovi dall&#39;elenco persone]_ per aggiornare l&#39;appartenenza a un elenco di persone statiche durante lo spostamento delle persone nel percorso.
* **Indirizza le persone in base all&#39;appartenenza all&#39;elenco**. In un nodo _Percorsi suddivisi_, utilizzare il filtro _[!UICONTROL Elenco statico membri persona persone]_ o _[!UICONTROL Elenco dinamico membri persona persone]_ per creare un percorso per le persone che sono o non sono membri di un elenco.

Ad esempio, puoi creare un elenco di esclusione di membri del gruppo e partner e utilizzarlo per escludere tali persone da un percorso di apprendimento. Oppure puoi aggiungere persone a un elenco statico quando raggiungono un punto di qualificazione in un percorso e quindi utilizzare tale elenco per diramare persone in un percorso diverso.

## Crea un nodo di azione - Aggiungi all’elenco delle persone {#add-to-people-list}

**_Elenchi di persone statiche solo_**

All&#39;interno di un account o di un percorso di persone, aggiungi persone a un elenco di persone statiche utilizzando [a _Esegui un&#39;azione_ nodo](../journeys/action-nodes.md#people-actions).

Considera ad esempio un percorso di percorso in cui si invia un’e-mail e alcune persone si registrano a un webinar. Considera questa risposta un punto di qualificazione nel percorso. Una volta ottenuta la qualifica, desideri aggiungere queste persone a un elenco di persone statiche utilizzato da un altro percorso per suddividere le persone qualificate in un percorso diverso.

>[!NOTE]
>
>Se una persona è già presente nell’elenco durante l’esecuzione del nodo, l’azione viene ignorata.

1. Passa alla mappa del percorso.

1. Fai clic sull&#39;icona più ( **+** ) in un percorso e scegli **[!UICONTROL Esegui un&#39;azione]**.

1. (Solo percorsi di account) Seleziona l&#39;opzione _[!UICONTROL Azione su]_ **[!UICONTROL Persone]**.

1. Per _[!UICONTROL Azione sulle persone]_, scegli **[!UICONTROL Aggiungi all&#39;elenco delle persone]**.

1. Per **[!UICONTROL Seleziona elenco persone statiche]**, scegli l&#39;elenco di persone in cui desideri aggiungere persone.

   ![Seleziona Aggiungi a elenco persone](../journeys/assets/node-action-add-to-people-list.png){width="300"}

## Crea un nodo di azione - Rimuovi dall’elenco delle persone {#remove-from-people-list}

**_Elenchi di persone statiche solo_**

All&#39;interno di un account o di un percorso di persone, rimuovere le persone da un elenco di persone statiche utilizzando [a _Esegui un&#39;azione_ nodo](../journeys/action-nodes.md#people-actions).

Ad esempio, dopo la conversione di una persona, è necessario rimuoverla da un elenco statico. Questo elenco viene utilizzato per indirizzare le persone su un percorso di apprendimento in modo che non ricevano più comunicazioni di apprendimento.

>[!NOTE]
>
>Se una persona non è presente nell’elenco da cui è pianificata la rimozione, l’azione viene ignorata.

1. Passa alla mappa del percorso.

1. Fai clic sull&#39;icona più ( **+** ) in un percorso e scegli **[!UICONTROL Esegui un&#39;azione]**.

1. (Solo percorsi di account) Seleziona l&#39;opzione _[!UICONTROL Azione su]_ **[!UICONTROL Persone]**.

1. Per _[!UICONTROL Azione sulle persone]_, scegli **[!UICONTROL Rimuovi dall&#39;elenco delle persone]**.

1. Per **[!UICONTROL Seleziona elenco persone statiche]**, scegliere l&#39;elenco di persone da cui si desidera rimuovere le persone.

   ![Seleziona Rimuovi dall&#39;elenco persone](../journeys/assets/node-action-remove-from-people-list.png){width="300"}

## Dividi nodo percorsi - Elenco membri di persone {#split-paths-by-list-membership}

**_percorsi di account e persone_**

Utilizzare i filtri di appartenenza all&#39;elenco persone in un nodo [_Percorsi suddivisi_](../journeys/split-merge-paths-nodes.md) per indirizzare le persone in base al fatto che siano membri di un elenco persone. Sono disponibili due filtri:

| Filtro | Descrizione |
| ------ | ----------- |
| [!UICONTROL Utente dell&#39;elenco dinamico Persone] | L’utente è o non è membro di uno o più elenchi di persone dinamici. L&#39;appartenenza riflette le regole correnti dell&#39;elenco. |
| [!UICONTROL Elenco statico membri persona] | La persona è o non è membro di uno o più elenchi di persone statiche. |

Questi filtri sono disponibili in entrambi i tipi di percorso:

* **percorsi di persone** - In un nodo _Percorsi suddivisi_.
* **percorsi di account** - In un nodo _Percorsi suddivisi_ diviso da _[!UICONTROL Persone]_.

Per escludere membri e partner del team da un percorso di sviluppo, aggiungere il filtro _[!UICONTROL Elenco statico membri persona]_, impostare l&#39;operatore su `is not` e selezionare l&#39;elenco.

1. Passa alla mappa del percorso.

1. Fare clic sull&#39;icona più ( **+** ) in un percorso e scegliere **[!UICONTROL Dividi percorsi]**.

   ![Aggiungi nodo percorso - percorsi suddivisi](../journeys/assets/add-node-split.png){width="300" zoomable="no"}

1. (Solo per percorsi di account) Imposta il nodo per le condizioni persone.

   * Nelle proprietà del nodo a destra, scegli **[!UICONTROL Persone]** per la suddivisione.

   * Imposta **[!UICONTROL Attributi utilizzati per le condizioni]** su **[!UICONTROL Solo attributi persone]**.

   ![percorso account - nodo percorso suddiviso - attributi persone](../journeys/assets/node-split-path-account-journey-people-attributes.png){width="300" zoomable="no"}

1. Per definire una condizione per _[!UICONTROL Percorso 1]_, fare clic su **[!UICONTROL Applica condizione]**.

1. Nell&#39;editor delle condizioni, espandere la cartella _[!UICONTROL Filtri speciali]_ e trascinare il filtro **[!UICONTROL Elenco dinamico Persona membro di persone]** o **[!UICONTROL Elenco statico Persona membro di persone]** nell&#39;area di lavoro delle condizioni.

   ![Editor delle condizioni del percorso suddiviso con filtri per elenco Persona membro di persone](../accounts/assets/account-lists-person-journeys-split-path-filter.png){width="700" zoomable="yes"}

1. Per includere i membri dell&#39;elenco, impostare l&#39;appartenenza su `is`.

   Per escluderli, impostarli su `is not`.

1. Selezionare l&#39;elenco di persone da valutare.

   Immetti il testo nel campo per filtrare gli elenchi disponibili. È possibile selezionare solo gli elenchi di persone creati dall&#39;utente.

1. Affina le condizioni applicando la **[!UICONTROL logica filtro]** nella parte superiore.

   Puoi combinare i filtri di appartenenza agli elenchi con altri filtri di persone e scegliere di soddisfare tutte le condizioni o qualsiasi condizione.

1. Fai clic su **[!UICONTROL Fine]**.

Continua a configurare il nodo percorsi suddivisi come descritto in [_Aggiungi un percorso suddiviso per nodo persone_](../journeys/split-merge-paths-nodes.md#add-a-split-path-by-people-node). Per ulteriori informazioni sui filtri di appartenenza, vedere [_Filtro appartenenza_](../journeys/split-merge-paths-nodes.md#membership-filtering).
