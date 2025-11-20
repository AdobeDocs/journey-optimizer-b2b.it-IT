---
title: Attivare Marketo Engage per supportare le azioni di Percorso
description: Attiva le connessioni Marketo Engage per supportare le azioni di percorso in modo che gli addetti al marketing possano coordinare le campagne tra Marketo Engage e Journey Optimizer B2B edition.
feature: Integrations, Audiences, Buying Groups
role: User, Admin
source-git-commit: de7f5620556a48fe6f12ed1c70e925e11ec770f1
workflow-type: tm+mt
source-wordcount: '397'
ht-degree: 1%

---


# Attivare le istanze Marketo Engage per supportare le azioni

Le azioni Marketo Engage sono _azioni basate sulle persone_ che ti consentono di coordinare l&#39;orchestrazione marketing _basata sull&#39;account_ tra Journey Optimizer B2B edition e le attività di marketing _basate sui lead_ in Marketo Engage. Utilizza queste azioni per orchestrare l’iscrizione all’elenco statico e inserire le persone nelle campagne.

Per utilizzare le azioni di Marketo Engage, un amministratore crea innanzitutto un [servizio personalizzato](https://experienceleague.adobe.com/it/docs/marketo-developer/marketo/rest/custom-services#) in Marketo Engage, che fornisce le credenziali necessarie per l&#39;autenticazione.
Quindi, un amministratore di prodotto per Journey Optimizer B2B edition crea una connessione a Marketo Engage immettendo le credenziali.
Gli utenti di Journey Optimizer B2B edition possono quindi fare riferimento alla connessione per configurare azioni di Marketo Engage nei percorsi di account <!-- Person and -->, ad esempio aggiungendo o rimuovendo persone dagli elenchi di Marketo Engage o aggiungendole a campagne di richiesta.

La visibilità delle risorse nell’area di lavoro di Marketo Engage, ad esempio elenchi e campagne, è disciplinata dalle autorizzazioni per il ruolo assegnate nel servizio personalizzato.

La stessa connessione può essere utilizzata più volte all’interno di un percorso e diverse connessioni Marketo Engage possono coesistere in un singolo percorso.

Quando viene eseguita un’azione, utilizza i Criteri di selezione per determinare quali record di persone in Marketo Engage devono essere selezionati per verificare se nel profilo di persona unificato sono presenti più identificatori. Le opzioni includono la scelta dei record Marketo Engage più vecchi, più recenti o tutti quelli corrispondenti. Le persone procedono attraverso il percorso indipendentemente da una corrispondenza, tranne quando si verifica un errore.

## Configurare una connessione Marketo Engage

Configurare un&#39;istanza remota di Marketo Engage da utilizzare con le azioni del percorso Marketo Engage.

### Creare il servizio personalizzato Marketo Engage

1. Accedi a Marketo Engage come amministratore e crea un servizio personalizzato.
1. Registra i seguenti valori da utilizzare per la connessione:

   * ID Munchkin
   * ID client
   * Segreto client

### Aggiungere l’integrazione

![Aggiungi dettagli integrazione](assets/integration-connection-details.png)

1. In Journey Optimizer B2B edition, passa a **Amministrazione** > **Configurazioni**.
1. Selezionare la scheda **Integrazioni**.
1. Fare clic su **[!UICONTROL Crea una connessione]**.
1. Immettere un nome (obbligatorio) e una descrizione (facoltativo).
1. Selezionare un **criterio di selezione** per i record persona corrispondenti.
1. Immetti l&#39;ID Munchkin, l&#39;ID client e il segreto client.
1. Fare clic su **[!UICONTROL Connetti a Marketo]**.
1. Fai clic su **[!UICONTROL Crea]**.

Quando un addetto al marketing utilizza un’azione Marketo Engage in un percorso, può configurare il nodo utilizzando il nome della connessione.

Con l&#39;integrazione completata, le azioni Marketo Engage sono disponibili da **Azioni in:** nelle proprietà del nodo.

![Elenco azioni di Marketo](assets/marketo-actions-list.png)