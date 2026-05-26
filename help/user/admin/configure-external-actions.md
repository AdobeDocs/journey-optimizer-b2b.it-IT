---
title: Configurazione azioni esterne
description: Scopri come sviluppatori, amministratori e addetti al marketing collaborano per implementare, configurare e utilizzare azioni esterne che collegano Journey Optimizer B2B edition a servizi esterni nei percorsi di account.
feature: Setup, Integrations
role: Admin, Developer
exl-id: 226fbf23-7df2-4fd7-b5a4-2057a417a261
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: d6e625c1-468f-4d73-9f32-fd1edb87f96b
  - id: c8f3fb27-3167-48ac-a66a-fa4bc3f58dda
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
autotag-review: '2026-04-29T23:21:59.633Z'
source-git-commit: effa8e2a45ecc5afbaa5a3f75437735bef89a400
workflow-type: tm+mt
source-wordcount: 1306
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

   Affinché questo passaggio abbia esito positivo, il servizio esterno deve essere attivo e raggiungibile. In caso di errore di convalida, nella finestra di dialogo viene visualizzato un messaggio che descrive l’errore e un suggerimento per risolverlo. Per ulteriori informazioni, vedere [_Risoluzione dei problemi_](#troubleshooting).

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

### Risoluzione dei problemi {#troubleshooting}

Quando si immette l&#39;URL della specifica OpenAPI per il servizio esterno e si fa clic su **[!UICONTROL Crea]**, il sistema esegue la convalida del servizio. Quando viene rilevato un errore, nella finestra di dialogo viene visualizzato un messaggio che descrive l’errore.

![Messaggio di errore di convalida del servizio URL azione esterna](./assets/configuration-external-actions-create-url-error.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Per molti dei seguenti errori è necessario rivolgersi allo sviluppatore che ha creato e pubblicato il servizio Web pubblico per risolvere il problema.

#### Dettagli errore di convalida

| Errore visualizzato | Perché è successo | Cosa fare |
|---|---|---|
| `This URL is already used by another external action` | Questo URL della specifica è già registrato per un&#39;altra azione nell&#39;organizzazione. | Utilizza un URL di specifica diverso o elimina l’azione esistente che lo utilizza già. |
| `An action with this name already exists` | `info.title` nella specifica corrisponde a un&#39;azione già esistente | Modificare il titolo nel campo `info.title` della specifica in modo che sia univoco. |
| `Duplicate operation ID found in the specification` | Due o più operazioni nella specifica condividono lo stesso `operationId`. | Assegna a ogni operazione un `operationId` univoco. |
| `Field in the specification exceeds the maximum allowed length` | Un campo di testo nella specifica (ad esempio un titolo o una descrizione) è troppo lungo. | Abbreviare il campo contrassegnato. |
| `The entity type value is invalid` | Valore non riconosciuto per un&#39;estensione `x-` specifica per Adobe per il tipo di entità | Correggi il tipo di entità in un valore supportato. Per informazioni sulle opzioni valide, consulta la [documentazione per sviluppatori](https://developer.adobe.com/journey-optimizer-b2b-apis/). |
| `The provided document is not a valid OpenAPI specification` | La specifica non può essere analizzata strutturalmente. | Convalida le specifiche in base allo schema OpenAPI 3.0 e correggi eventuali problemi. |
| `Required OpenAPI field is missing` | Un campo OpenAPI standard richiesto è assente (ad esempio `info` o `paths`). | Aggiungi il campo mancante. |
| `Required endpoint is missing from the specification` | Un endpoint richiesto da Adobe Journey Optimizer B2B edition non è definito nelle specifiche. | Aggiungi l’endpoint richiesto. Consulta la [documentazione per gli sviluppatori](https://developer.adobe.com/journey-optimizer-b2b-apis/) per cui sono necessari endpoint. |
| `Required extension field is missing` | Manca un campo di estensione Adobe `x-` richiesto nelle specifiche. | Aggiungi il campo di estensione mancante come descritto nella documentazione. |
| `Security schemes are missing from the specification` | Nessun `securitySchemes` definito nella specifica in `components`. | Definire almeno uno schema di protezione. |
| `Multiple authentication types are not supported` | La specifica definisce più schemi di autenticazione. | Aggiorna la specifica per utilizzare un singolo tipo di autenticazione. |
| `The authentication type is not supported` | Il tipo di schema di protezione utilizzato (ad esempio `oauth2` o `openIdConnect`) non è supportato. | Passa a un tipo di autenticazione supportato. Per informazioni sulle opzioni supportate, consulta la documentazione per gli sviluppatori. |
| `The OpenAPI version is not supported` | Mancata corrispondenza delle versioni a livello di specifica | Aggiorna la specifica per utilizzare OpenAPI 3.0.x. |
| `An unexpected error occurred` | È stato riscontrato un problema non classificato nella specifica. | Controllare la presenza di eventuali anomalie nelle specifiche e riprovare. Se l’errore persiste, contatta il supporto tecnico. |

<!--
## Errors you'll see if something goes wrong with the request itself

This error appears below the URL field (not in the alert banner) and means there was a network problem or an unexpected server response — not a problem with your URL or spec.

| What you'll see | Why it happened | What to do |
|---|---|---|
| `Failed to create external action. Please try again.` | A network error occurred or the server returned an unexpected response | Check your connection and try again. If it keeps happening, contact support |
-->

## Aggiungere un nodo esterno a un percorso {#add-journey-node}

Dopo l&#39;attivazione di un&#39;azione, gli addetti al marketing possono aggiungere un nodo _[!UICONTROL Azione esterna]_ o _[!UICONTROL Percorso suddiviso esterno]_ a qualsiasi percorso di account. Per informazioni su come aggiungere e utilizzare questi nodi nell&#39;area di lavoro del percorso di account, vedere [Nodi esterni](../journeys/external-nodes.md).
