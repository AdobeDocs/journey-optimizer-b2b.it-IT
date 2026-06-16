---
title: Crea un nodo azione
description: Placeholder
autotag-review: '2026-06-12T22:58:21.806Z'
TQID: 'https://experienceleague.adobe.com/uR-WvNz3gA6V7yyN3RRXH-MggrmGb1qvu1CBhMZRuAc'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: a4b836d9-ffdd-4df3-a62a-f78b830cf059id: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2: id: af7eab5e-3580-4254-9f56-3c20b4f6ef42id: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: bf2854a777f62ba2f74f79942ee3336b6e8ab9dd
workflow-type: tm+mt
source-wordcount: 197
ht-degree: 2%

---

# Crea un nodo di azione

In un percorso di persone, utilizza un’azione sulle persone quando desideri applicare una modifica a tutte le persone nel percorso del nodo. Per un percorso di account, questo tipo di nodo può essere utilizzato all’interno del percorso di suddivisione da persone o dal percorso di suddivisione da account.

## Azioni e vincoli

| Azione | Vincoli |
| ------ | ---------- |
| **[!UICONTROL Invia e-mail]** | <li>Crea e-mail <li>Ottimizzazione del tempo di invio (facoltativo) |
| **[!UICONTROL Modifica valore dati]** | <li>Seleziona attributo persona <li>Imposta nuovo valore |

## Aggiungi un nodo azione {#add-an-action-node}

1. Passa alla mappa del percorso.

1. Fai clic sull&#39;icona più ( **+** ) in un percorso e scegli **[!UICONTROL Esegui un&#39;azione]**.

1. Nelle proprietà del nodo a destra, seleziona un’azione dall’elenco e imposta i valori per l’azione.

<!-- ![Person journey node - take an action](./assets/node-take-action-people.png){width="700" zoomable="yes"} -->

+++[!UICONTROL Invia e-mail]

Utilizza questa azione per inviare un messaggio e-mail. Dopo aver creato l&#39;e-mail per il nodo, puoi progettare, personalizzare e visualizzare in anteprima i messaggi e-mail nello spazio di progettazione e-mail (consulta [Authoring e-mail](../content/email-authoring.md)).

<!-- ![Take an action - Send email](./assets/node-action-send-email-from-marketo.png){width="300"} -->

Puoi utilizzare [Ottimizzazione del tempo di invio](../marketing/email-send-time-optimization.md) per personalizzare la tempistica di consegna delle e-mail prevedendo quando è più probabile che ogni profilo sia coinvolto.

<!--
>[!NOTE]
>
>You can use email deduplication in account journeys to ensure that the same email is not sent multiple times to the same email address within a journey. For more information, see [Email deduplication](../content/email-deduplication.md).
-->

+++

+++[!UICONTROL Modifica valore dati]

Utilizzare questa azione per modificare il valore di un attributo di profilo persone nel database. Selezionare l&#39;attributo e quindi impostare il nuovo valore.

<!-- ![Take an action - Update person profile](./assets/node-action-update-person-profile.png){width="300"} -->

+++
