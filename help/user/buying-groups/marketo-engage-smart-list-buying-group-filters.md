---
title: Acquisto di filtri per gruppi in Marketo Engage
description: Filtra i lead acquistando l’iscrizione al gruppo negli elenchi avanzati di Marketo Engage con vincoli come il punteggio di completezza per ottimizzare le campagne e il punteggio di lead.
feature: Buying Groups, Integrations
role: User
exl-id: b137e787-808e-4d36-8e8b-a1c7b999f8a2
source-git-commit: 204b293d3bc526b139f68766ed45ff549a74ed34
workflow-type: tm+mt
source-wordcount: '540'
ht-degree: 1%

---

# Filtri per gruppi acquisti in Marketo Engage

>[!IMPORTANT]
>
>**Funzionalità obsolete**</br></br>
>
>Con l&#39;[architettura semplificata](../simplified-architecture.md) per Journey Optimizer B2B edition, i filtri dei gruppi di acquisto non sono più disponibili in un&#39;istanza di Marketo Engage connessa.</br></br>
>
>In alternativa, puoi creare un elenco statico per ogni interesse della soluzione e quindi [utilizzare l&#39;azione _Aggiungi all&#39;elenco di Marketo_](../journeys/action-nodes.md#marketo-engage-actions) da un nodo di percorso. Questa azione aggiunge i membri del gruppo di acquisto a un particolare elenco statico in un’istanza di Marketo Engage connessa. Quindi, utilizza l’elenco statico incentrato sugli interessi della soluzione per un filtro elenco avanzato.

In qualità di addetto al marketing, potresti voler eliminare le campagne in Marketo Engage per gli utenti che fanno parte di gruppi di acquisto in Journey Optimizer B2B edition. Puoi anche informare i flussi di lavoro di valutazione dei lead in Marketo Engage utilizzando informazioni sui lead associati ai gruppi di acquisto. Ad esempio:

* Questo lead fa parte di un gruppo di acquisto?
* Il gruppo di acquisto è completo e coinvolto?

Se queste condizioni sono vere, puoi scegliere di valutare il lead in modo più alto. In caso contrario, puoi scegliere di non contrassegnarlo come lead qualificato per il marketing (MQL).

Nell&#39;istanza di Marketo Engage connessa a Journey Optimizer B2B edition, è possibile utilizzare il filtro _[!UICONTROL Membro del gruppo di acquisto]_ negli elenchi smart per identificare questi lead in base alla strategia della campagna.

1. Dopo aver [creato un elenco avanzato in Marketo Engage](https://experienceleague.adobe.com/it/docs/marketo/using/product-docs/core-marketo-concepts/smart-lists-and-static-lists/creating-a-smart-list/create-a-smart-list){target="_blank"}, selezionare la scheda **[!UICONTROL Elenco avanzato]** per aprire l&#39;editor di filtri.

1. Nell&#39;elenco dei filtri a destra, scorri verso il basso ed espandi la cartella **[!UICONTROL Filtri speciali]**.

1. Fare clic sul filtro **[!UICONTROL Membro del gruppo di acquisto]** e trascinarlo nell&#39;area di definizione del filtro.

   ![Aggiungere il filtro Membro del gruppo di acquisto all&#39;elenco smart](./assets/me-member-of-buying-group-filter-add.png){width="700" zoomable="yes"}

1. Impostare l&#39;opzione _[!UICONTROL Membro del gruppo di acquisto]_ su **[!UICONTROL true]** o **[!UICONTROL false]**.

   Questo vincolo è obbligatorio per la definizione.

1. (Facoltativo) Aggiungi altri vincoli relativi al gruppo di acquisto al filtro in base alla modalità di identificazione dei lead per l’elenco avanzato.

   * Fai clic su **[!UICONTROL Aggiungi vincolo]** in alto a destra nella scheda del filtro.

     ![Seleziona un altro vincolo](./assets/me-member-of-buying-group-filter-add-constraint.png){width="700" zoomable="yes"}

   * Selezionare il vincolo da aggiungere, ad esempio _Punteggio di completezza_ o _Interesse soluzione_.

   * Impostare la valutazione da utilizzare per una corrispondenza.

     Per un punteggio, puoi utilizzare una corrispondenza esatta o un intervallo superiore o inferiore al numero immesso.

     Per escludere i membri rimossi da un gruppo di acquisto, utilizzare il vincolo _[!UICONTROL Rimosso]_ impostato su `false`. È inoltre possibile includere in modo esplicito i membri rimossi nell&#39;elenco smart impostando il vincolo su `true`.

     Per un articolo discreto, ad esempio gli interessi della soluzione definiti in Journey Optimizer B2B edition, è possibile selezionare uno o più articoli per l&#39;elenco.

     ![Selezionare un valore per il vincolo dall&#39;elenco](./assets/me-member-of-buying-group-filter-constraint-list.png){width="600" zoomable="yes"}

     Seleziona il primo e fai di nuovo clic sul selettore per aprire la finestra di dialogo _[!UICONTROL Selezione di più valori]_.

     ![Selezionare più valori per il vincolo](./assets/me-member-of-buying-group-filter-constraint-multiple-value.png){width="500" zoomable="yes"}

     Spostare gli elementi rimanenti verso destra e fare clic su **[!UICONTROL OK]** quando si dispone dell&#39;elenco di elementi che si desidera utilizzare per il vincolo.

   * Ripetete queste azioni per aggiungere tutti i vincoli necessari.

   ![Filtro Membro del gruppo di acquisto con più vincoli](./assets/me-member-of-buying-group-filter-constraints-complete.png){width="600" zoomable="yes"}
