---
title: Crea un nodo azione
description: Placeholder
autotag-review: '2026-06-12T22:58:21.806Z'
TQID: 'https://experienceleague.adobe.com/uR-WvNz3gA6V7yyN3RRXH-MggrmGb1qvu1CBhMZRuAc'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: a4b836d9-ffdd-4df3-a62a-f78b830cf059id: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2: id: af7eab5e-3580-4254-9f56-3c20b4f6ef42id: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 0a877cc1fc0dfd9c3d8271c8f7be6a5e34a69a9a
workflow-type: tm+mt
source-wordcount: 821
ht-degree: 2%

---

# Crea un nodo di azione

In un percorso di persone, utilizza un’azione sulle persone quando desideri applicare una modifica a tutte le persone nel percorso del nodo.

## Azioni e vincoli {#actions}

| Azione | Vincoli |
| ------ | ----------- |
| **[!UICONTROL Attiva nella destinazione]** | <li>Seleziona o crea un elenco statico <li>Se l’elenco non ha una destinazione attivata, attiva l’elenco |
| **[!UICONTROL Aggiungi persona al Percorso]** | <li>Seleziona un percorso pianificato o live <li>I criteri di pubblico del percorso target non vengono applicati |
| **[!UICONTROL Aggiungi all&#39;elenco]** | <li>Crea un nuovo elenco statico o selezionane uno esistente |
| **[!UICONTROL Aggiungi a elenco Marketo]** | <li>Seleziona un elenco statico in Marketo Engage |
| **[!UICONTROL Modifica valore dati]** | <li>Seleziona attributo persona <li>Imposta nuovo valore |
| **[!UICONTROL Modifica dati programma]** | <li>Seleziona attributo del programma <li>Imposta nuovo valore |
| **[!UICONTROL Modifica stato programma]** | <li>Seleziona programma<li>Seleziona nuovo stato |
| **[!UICONTROL Rimuovi dall&#39;elenco]** | <li>Seleziona elenco statico <li>Ignora la persona se non ne è attualmente membro |
| **[!UICONTROL Rimuovi dall&#39;elenco Marketo]** | <li>Seleziona un elenco statico in Marketo Engage <li>Ignora la persona se non ne è attualmente membro |
| **[!UICONTROL Rimuovi persona dal Percorso]** | <li>Seleziona un percorso live <li>Ignora la persona se non è attualmente membro del percorso target |
| **[!UICONTROL Richiedi campagna Marketo]** | <li>Seleziona una campagna Marketo Engage |
| **[!UICONTROL Invia e-mail]** | <li>Creare, modificare o utilizzare un’e-mail personalizzata con IA <li>Ottimizzazione del tempo di invio (facoltativo) |
| **[!UICONTROL Invia WhatsApp]** | <li>Seleziona un messaggio WhatsApp |

## Aggiungi un nodo azione {#add-an-action-node}

1. Passa all’area di lavoro del percorso.

1. Fai clic sull&#39;icona più ( **+** ) in un percorso e scegli **[!UICONTROL Esegui un&#39;azione]**.

   ![Fai clic sull&#39;icona Aggiungi nel percorso del percorso](./assets/person-journey-canvas-add-node.png){width="200"}

1. Nelle proprietà del nodo a destra, seleziona un’azione dall’elenco e imposta i valori per l’azione.

+++Attiva nella destinazione

Utilizza questa azione per attivare le persone nelle destinazioni di Experience Platform direttamente dal tuo percorso. Seleziona la destinazione e immetti un nome di pubblico per identificare il pubblico attivato nella destinazione.

![Esegui un&#39;azione - Attiva nella destinazione](./assets/person-action-node-activate-to-destination.png){width="450"}

+++

+++[!UICONTROL Aggiungi persona al Percorso]

Utilizza questa azione per aggiungere persone ad altri percorsi pianificati o live. Le persone aggiunte tramite questa azione vengono aggiunte immediatamente al pubblico del percorso target; i criteri di pubblico del percorso non vengono applicati.

![Esegui un&#39;azione - Aggiungi persona al percorso](./assets/person-action-node-add-to-journey.png){width="450"}

+++

+++[!UICONTROL Aggiungi all&#39;elenco]

Utilizza questa azione per aggiungere persone a un elenco statico in Journey Optimizer B2B Prime.

![Esegui un&#39;azione - Aggiungi all&#39;elenco](./assets/person-action-node-add-to-list.png){width="450"}

Scegliere una delle opzioni seguenti:

* **[!UICONTROL Crea]** — crea una nuova risorsa elenco statica e aggiungi persone. L’elenco è immediatamente disponibile per l’utilizzo da parte di altre risorse in Journey Optimizer B2B Prime.
* **[!UICONTROL Seleziona]** — seleziona una risorsa elenco statico esistente in cui si desidera aggiungere persone che raggiungono il nodo.

+++

+++[!UICONTROL Aggiungi a elenco Marketo]

Utilizzare questa azione per aggiungere persone a un elenco statico in Marketo Engage.

![Esegui un&#39;azione - Aggiungi a elenco Marketo](./assets/person-action-node-add-to-marketo-list.png){width="450"}

+++

+++[!UICONTROL Modifica valore dati]

Utilizzare questa azione per aggiornare il valore di un attributo in un record persona. Selezionare l&#39;attributo e impostare il nuovo valore.

>[!TIP]
>
>Per cancellare il valore di un attributo, impostare il valore su `NULL`.

![Azione - Modifica valore dati](./assets/person-action-node-change-data-value.png){width="450"}

+++

+++[!UICONTROL Modifica dati programma]

Utilizzare questa azione per aggiornare il valore di un attributo di programma. Selezionare l&#39;attributo del programma e impostare il nuovo valore.

![Azione - Cambia dati programma](./assets/person-action-node-change-program-data.png){width="450"}

+++

+++[!UICONTROL Modifica stato programma]

Utilizzare questa azione per modificare lo stato di una persona in un programma Marketo Engage. Selezionare il programma e quindi il nuovo stato.

![Azione - Modifica stato programma](./assets/person-action-node-change-status-program.png){width="450"}

+++

+++[!UICONTROL Rimuovi dall&#39;elenco]

Utilizza questa azione per rimuovere persone da un elenco statico in Journey Optimizer B2B Prime. Se una persona non è attualmente membro dell’elenco, l’azione viene ignorata per tale persona.

![Esegui un&#39;azione - Rimuovi dall&#39;elenco](./assets/person-action-node-remove-from-list.png){width="450"}

+++

+++[!UICONTROL Rimuovi dall&#39;elenco Marketo]

Utilizzare questa azione per rimuovere persone da un elenco statico in Marketo Engage. Se una persona non è attualmente membro dell’elenco, l’azione viene ignorata per tale persona.

![Esegui un&#39;azione - Rimuovi dall&#39;elenco di Marketo](./assets/person-action-node-remove-from-marketo-list.png){width="450"}

+++

+++[!UICONTROL Rimuovi persona dal Percorso]

Utilizza questa azione per rimuovere persone da altri percorsi di persone live. La persona viene immediatamente rimossa dal percorso target e non vengono intraprese ulteriori azioni nei suoi confronti. Se una persona non è attualmente membro del percorso target, l’azione viene ignorata per tale persona.

![Azione - Rimuovi persona dal percorso](./assets/person-action-node-remove-from-journey.png){width="450"}

+++

+++[!UICONTROL Richiedi campagna Marketo]

Utilizza questa azione per aggiungere persone a una campagna di richieste in un’istanza di Marketo Engage connessa. Seleziona la campagna Marketo Engage da richiedere.

![Azione - Richiedi campagna Marketo](./assets/person-action-node-request-marketo-campaign.png){width="450"}

+++

+++[!UICONTROL Invia e-mail]

Utilizza questa azione per inviare un’e-mail alle persone che hanno prestato il consenso. Le persone che hanno annullato l’abbonamento, sono state inserite nell’elenco Bloccati, hanno sospeso l’e-mail o il marketing saltano questa azione.

![Azione - Invia e-mail](./assets/person-action-node-send-email.png){width="450"}

Puoi creare un’e-mail, modificare un’e-mail esistente o utilizzare un’e-mail personalizzata con IA. Per informazioni sulla creazione e la modifica delle e-mail, consulta [Canale e-mail](../marketing/email-channel.md).

Puoi utilizzare [Ottimizzazione del tempo di invio](../marketing/email-send-time-optimization.md) per personalizzare la tempistica di consegna delle e-mail prevedendo quando è più probabile che ogni profilo sia coinvolto.

+++

+++[!UICONTROL Invia WhatsApp]

Utilizza questa azione per inviare un messaggio WhatsApp. Puoi creare, personalizzare e visualizzare in anteprima i messaggi WhatsApp nello spazio di progettazione visivo (vedi [Authoring WhatsApp](../content/whatsapp-authoring.md)).

![Esegui un&#39;azione - Invia WhatsApp](./assets/person-action-node-send-whatsapp.png){width="450"}

+++
