---
title: Attivare Marketo Engage per supportare le azioni di Percorso
description: Attiva le connessioni Marketo Engage per supportare le azioni di percorso in modo che gli addetti al marketing possano coordinare le campagne tra Marketo Engage e Journey Optimizer B2B edition.
feature: Integrations, Audiences, Buying Groups
role: User, Admin
source-git-commit: 9b77570ddb9b416251f38db51a57507a935a526a
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 1%

---


# Attivare le istanze Marketo Engage per supportare le azioni

Le azioni Marketo Engage sono _azioni basate sulle persone_ che ti consentono di coordinare l&#39;orchestrazione marketing _basata sull&#39;account_ tra Journey Optimizer B2B edition e le attività di marketing _basate sui lead_ in Marketo Engage. Utilizza queste azioni per orchestrare l’iscrizione all’elenco statico e inserire le persone nelle campagne.

Per utilizzare le azioni di percorso di Marketo Engage, un amministratore crea innanzitutto un [servizio personalizzato](https://experienceleague.adobe.com/en/docs/marketo-developer/marketo/rest/custom-services){target="_blank"} in Marketo Engage, che fornisce le credenziali necessarie per l&#39;autenticazione. L’amministratore di prodotto per Journey Optimizer B2B edition utilizza quindi le credenziali per creare una connessione a Marketo Engage. Gli utenti di Journey Optimizer B2B edition possono quindi fare riferimento alla connessione per configurare azioni di Marketo Engage nei percorsi di account <!-- person and -->, ad esempio aggiungendo o rimuovendo persone dagli elenchi di Marketo Engage o aggiungendole a campagne di richiesta.

## Configurare una connessione Marketo Engage {#external-marketo-configure}

>[!CONTEXTUALHELP]
>id="ajo-b2b_marketo-configure-connections"
>title="Connessioni Marketo Engage esterne"
>abstract="Gli amministratori di prodotto possono configurare le connessioni alle istanze Marketo Engage esterne, rendendole disponibili per le azioni di percorso."

Completa le seguenti attività per configurare un’istanza Marketo Engage esterna da utilizzare con le azioni di percorso.

### Creare il servizio personalizzato Marketo Engage

1. Accedi a Marketo Engage come amministratore e [crea un servizio personalizzato](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/additional-integrations/create-a-custom-service-for-use-with-rest-api){target="_blank"}.
1. Copia i seguenti valori da utilizzare per la connessione Journey Optimizer B2B edition:

   * ID Munchkin
   * ID client
   * Segreto client

La visibilità delle risorse nell&#39;area di lavoro di Marketo Engage, ad esempio elenchi e campagne, è disciplinata dalle autorizzazioni per il ruolo [assegnate nel servizio personalizzato](https://experienceleague.adobe.com/en/docs/marketo-developer/marketo/rest/custom-services#permission-list){target="_blank"}. Gli addetti al marketing possono utilizzare la stessa connessione più volte all’interno di un percorso e utilizzare diverse connessioni Marketo Engage all’interno dello stesso percorso.

### Aggiungere l’integrazione

![Aggiungi dettagli integrazione](assets/integration-connection-details.png){width="800" zoomable="yes"}

1. In Journey Optimizer B2B edition, passa a **[!UICONTROL Amministrazione]** > **[!UICONTROL Configurazioni]**.
1. Selezionare la scheda **[!UICONTROL Integrazioni]**.
1. Fare clic su **[!UICONTROL Crea una connessione]**.
1. Immettere un **[!UICONTROL Nome]** (obbligatorio) e **[!UICONTROL Descrizione]** (facoltativo).
1. Selezionare il criterio di aggiornamento utilizzato per applicare un&#39;azione a un record persona corrispondente.

   Quando viene eseguita un&#39;azione per l&#39;istanza di Marketo Engage connessa, il _criterio di aggiornamento_ selezionato determina i record persona in Marketo Engage per selezionare se esistono più identificatori nel profilo persona unificato.

   * **[!UICONTROL Aggiorna tutti i record corrispondenti]**
   * **[!UICONTROL Aggiorna solo il record corrispondente più vecchio]**
   * **[!UICONTROL Aggiorna solo il record corrispondente più recente]**

   >[!NOTE]
   >
   >Le persone procedono attraverso il percorso indipendentemente da una corrispondenza, tranne quando si verifica un errore.

1. Immetti l’ID Munchkin, l’ID client e il Segreto client per il servizio creato nell’istanza Marketo Engage esterna.
1. Fare clic su **[!UICONTROL Connetti a Marketo]**.
1. Fai clic su **[!UICONTROL Crea]**.

## Utilizzare la connessione in un&#39;azione di percorso

Quando un addetto al marketing utilizza un’azione Marketo Engage in un percorso, può configurare il nodo utilizzando il nome della connessione.

Con l&#39;integrazione completata, le azioni Marketo Engage sono disponibili da **Azioni in:** nelle proprietà del nodo.

![Elenco azioni di Marketo](assets/marketo-actions-list.png){width="800" zoomable="yes"}