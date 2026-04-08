---
title: Configurazione azioni esterne
description: Scopri come sviluppatori, amministratori e addetti al marketing collaborano per implementare, configurare e utilizzare azioni esterne che collegano Journey Optimizer B2B edition a servizi esterni nei percorsi di account.
feature: Setup, Integrations
role: Admin, Developer
source-git-commit: 6d3967babc1bc868fde0c76ac9068e63156070cd
workflow-type: tm+mt
source-wordcount: '907'
ht-degree: 1%

---

# Configurazione azioni esterne

Le azioni esterne consentono ai percorsi di account in Journey Optimizer B2B edition di connettersi con i sistemi esterni direttamente dall’area di lavoro del percorso. Quando un pubblico di account raggiunge un nodo di azione esterna, il sistema effettua una chiamata in uscita asincrona a un servizio esterno configurato, trasmettendo i dati degli attributi di pubblico per account, persone o entrambi. Il servizio esterno elabora i dati e risponde utilizzando un callback, restituendo dati sul pubblico e metadati che possono essere utilizzati per guidare l’esecuzione del percorso.

Questa funzione supporta due tipi di nodo di percorso:

* **Azione esterna** - Chiama un servizio esterno e continua lungo un singolo percorso in uscita. Ideale per _integrazioni Fire-and-Dimenticate_, ad esempio per aggiornare un record CRM o attivare una notifica downstream.
* **Percorsi di suddivisione esterni** - Chiama un servizio esterno e valuta la risposta per instradare gli account lungo uno dei diversi percorsi definiti.

>[!NOTE]
>
>I servizi per le azioni esterne sono supportati solo per i percorsi di account. Questi tipi di nodo non sono disponibili per i percorsi di persone.

## Panoramica sull’implementazione

La configurazione delle azioni esterne richiede il coordinamento in tre ruoli in sequenza:

| | Ruolo | Attività |
| ---- | ---- | ---- |
| 1 | Sviluppatore | [Implementare e pubblicare il servizio esterno](#implement-service) |
| 2 | Amministratore | [Configura l&#39;azione in Journey Optimizer B2B edition](#configure-action) |
| 3 | Addetto marketing | [Aggiungere un nodo esterno a un percorso di account](#add-journey-node) |

## Implementare il servizio esterno {#implement-service}

Lo sviluppatore deve creare e pubblicare un servizio Web pubblico conforme all&#39;[interfaccia del provider di servizi Adobe Journey Optimizer B2B edition External Actions](https://developer.adobe.com/journey-optimizer-b2b-apis/).

>[!NOTE]
>
>La funzione di callback richiede un token Bearer. Per recuperarlo, imposta [le credenziali da server a server OAuth in Adobe Developer Console](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation) per la tua organizzazione IMS.

Dopo che il servizio è attivo, fornisci l’URL della specifica OpenAPI e le credenziali di autenticazione all’amministratore del prodotto responsabile della configurazione dell’azione.

## Configurare l’azione {#configure-action}

Un’azione deve essere configurata e attivata prima che gli addetti al marketing possano utilizzarla in un percorso. Le azioni vengono create nello stato _Bozza_ e le modifiche vengono salvate automaticamente. Rimane come bozza finché non la attivate.

>[!PREREQUISITES]
>
>Prima di aggiungere la configurazione, richiedi l’URL per la specifica OpenAPI e le credenziali di autenticazione allo sviluppatore.
>
>Per definire e attivare un&#39;azione esterna, è necessario disporre dell&#39;autorizzazione _[!UICONTROL Gestisci configurazioni amministratore B2B]_ [prodotto](./user-management.md#b2b-product-permissions).

1. Vai a **[!UICONTROL Amministrazione]** > **[!UICONTROL Configurazioni]**.

1. Fai clic su **[!UICONTROL Azioni esterne]** nel pannello intermedio.

   ![Accedere allo spazio di configurazione Azioni esterne](./assets/configuration-external-actions-list.png){width="800" zoomable="yes"}

1. Fai clic su **[!UICONTROL Crea azione]** in alto a destra.

1. Immetti l&#39;URL della specifica OpenAPI per il servizio esterno e fai clic su **[!UICONTROL Crea]**.

   ![Immettere l&#39;URL del servizio](./assets/configuration-external-actions-create-url.png){width="500"}

   >[!NOTE]
   >
   >Affinché questo passaggio abbia esito positivo, il servizio esterno deve essere attivo e raggiungibile.

1. Quando l&#39;URL viene risolto correttamente, esaminare i **[!UICONTROL Dettagli servizio]**.

   I dettagli del servizio vengono letti direttamente dalla specifica OpenAPI al momento della creazione dell’azione. Non è possibile modificare queste proprietà nella configurazione dopo la creazione.

   | Proprietà | Descrizione | Proprietà delle specifiche OpenAPI |
   | -------- | ----------- | --------------------- |
   | [!UICONTROL Nome] | Nome dell’azione | `info.title` |
   | [!UICONTROL Descrizione] | Descrizione dell’azione | `info.description` |
   | [!UICONTROL URL] | URL della specifica OpenAPI che definisce il servizio esterno | `servers.url` |

1. Immettere le credenziali di **[!UICONTROL Autenticazione]** per il servizio esterno (`components.securitySchemes`).

   >[!NOTE]
   >
   >I campi delle credenziali visualizzati dipendono dal meccanismo di autenticazione definito nel servizio esterno. I tipi supportati sono API Key, OAuth2 e HTTP Basic Authentication.

   ![Aggiungi le credenziali di autenticazione](./assets/configuration-external-actions-auth-credentials.png){width="600" zoomable="yes"}

   È possibile modificare le credenziali in base alle esigenze quando l&#39;azione configurata è nello stato _Bozza_ o _Attivo_.

1. Fai clic su **[!UICONTROL Avanti]**.

1. Imposta le proprietà **[!UICONTROL Configurations]** per definire il modo in cui l&#39;azione scambia i dati con il servizio esterno.

   >[!NOTE]
   >
   >Le proprietà contrassegnate come _Statiche_ non sono aggiornabili al momento della configurazione e si basano sulla definizione del servizio.

   * **[!UICONTROL Tipo di azione]** (_Statico_) - Tipo di nodo di percorso supportato:

      * [!UICONTROL Azione esterna] (`enableSplitPath` = false)
      * [!UICONTROL Percorso suddivisione azione esterna] (`enableSplitPath` = true)

     Non puoi modificare il tipo di azione dopo aver creato la configurazione dell’azione.

   * **[!UICONTROL Funzioni di accesso]** (_Static_) - (Solo percorso suddiviso azione esterna) Le variabili restituite dal servizio esterno sono disponibili come condizioni di percorso in un nodo di percorso suddiviso esterno. (`invocationPayloadDef.accessorsMetadata`)

   * **[!UICONTROL Contesto Percorso]** (_Statico_) - Ambito dei dati del pubblico inviati nella richiesta (`supportedEntityType`):

      * [!UICONTROL Account] - Invia solo gli account

      * [!UICONTROL Persone] - Invia solo persone

      * [!UICONTROL Persone nell&#39;account] - Invia account e persone correlate all&#39;account

   * **[!UICONTROL Campi in uscita]** - Mappa ogni campo della tabella su un [campo XDM](../admin/xdm-field-management.md). Questi campi vengono inviati nel corpo della richiesta al servizio esterno. Proprietà definizione servizio: `invocationPayloadDef.accountFields`, `invocationPayloadDef.fields`.

   ![Mappa i campi in uscita dell&#39;azione esterna](./assets/configuration-external-actions-fields.png){width="600" zoomable="yes"}

   * **[!UICONTROL Campi in ingresso]** - Mappa ogni campo della tabella su un [campo XDM aggiornabile](../admin/xdm-field-management.md#updatable-fields). Questi campi vengono compilati dalla risposta del servizio esterno. Proprietà definizione servizio: `callbackPayloadDef.accountFields`, `callbackPayloadDef.fields`. Aggiornabile dopo la creazione.

   * **[!UICONTROL Parametri intestazione]** - Immettere un valore per ogni riga da passare come intestazione HTTP nella richiesta. Proprietà definizione servizio: `invocationPayloadDef.headers`.

   * **[!UICONTROL Timeout]** - Immettere il numero di minuti di attesa per il richiamo del callback da parte del servizio esterno prima che la richiesta venga considerata non riuscita. Proprietà definizione servizio: `timeout`.

   * **[!UICONTROL Attributi globali]** - Immettere un valore per ogni riga da includere come campo statico nel corpo della richiesta. Proprietà definizione servizio: `invocationPayloadDef.globalAttributes`.

   ![Parametri di intestazione azione esterna, timeout e attributi globali](./assets/configuration-external-actions-header-timeout-global.png){width="600" zoomable="yes"}

1. Fai clic sulla _freccia Indietro_ per tornare all&#39;elenco e mantenere l&#39;azione nello stato _Bozza_.

   In alternativa, fare clic su **[!UICONTROL Attiva]** per modificare la configurazione dell&#39;azione allo stato _Attivo_. L’azione esterna configurata deve essere attiva per renderla disponibile per l’utilizzo nei percorsi di account.

## Aggiungere un nodo esterno a un percorso {#add-journey-node}

Dopo l&#39;attivazione di un&#39;azione, gli addetti al marketing possono aggiungere un nodo _[!UICONTROL Azione esterna]_ o _[!UICONTROL Percorso suddiviso esterno]_ a qualsiasi percorso di account. Per informazioni su come aggiungere e utilizzare questi nodi nell&#39;area di lavoro del percorso di account, vedere [Nodi esterni](../journeys/external-nodes.md).
