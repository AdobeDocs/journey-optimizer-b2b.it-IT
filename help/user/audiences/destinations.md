---
title: Destinazioni
description: Scopri le destinazioni di Experience Platform supportate e come connettere una destinazione per attivare gli elenchi di persone statiche in Journey Optimizer B2B Edition.
feature: Audiences, Integrations
role: User
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
    internal-label: Journey Optimizer B2B Edition
feature_v2:
  - id: beb5f4be-cec3-471a-9db6-831a77dd3ac9
    internal-label: Audiences
  - id: c8f3fb27-3167-48ac-a66a-fa4bc3f58dda
    internal-label: Integrations
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
source-wordcount: '629'
ht-degree: 4%
---

# Destinazioni

Le destinazioni sono integrazioni predefinite che ti consentono di inviare [membri dell&#39;elenco di persone statiche](./people-lists-static.md) e tipi di pubblico del percorso di account alle piattaforme social. L&#39;attivazione di un elenco statico in una destinazione mantiene sincronizzata l&#39;appartenenza. Man mano che le persone vengono aggiunte o rimosse dall’elenco, vengono aggiunte o rimosse dal pubblico di destinazione e, per estensione, da qualsiasi campagna creata dal pubblico.

Esistono tre modi per attivare le persone in una destinazione connessa:

* **Da un elenco statico** - Attiva un elenco statico esistente direttamente dalla scheda **_[!UICONTROL Elenchi persone]_**. Vedi [_Attiva in una destinazione_](./people-lists-static.md#static-list-activate).
* **Da un percorso di account** - Aggiungi un nodo azione **_[!UICONTROL Attiva nella destinazione]_** a un percorso di percorso in modo che gli account idonei vengano attivati nella destinazione quando raggiungono tale nodo. Vedi [_Attiva o disattiva da una destinazione_](../journeys/action-nodes.md#activate-deactivate-destination).
* **Da un gruppo di acquisto** - Per riempire ruoli vuoti nei gruppi di acquisto, puoi attivare un pubblico LinkedIn corrispondente per eseguire il targeting dei potenziali clienti che corrispondono ai parametri del gruppo di acquisto. Vedi [_LinkedIn Account MatchedAudience_s](../data/linkedin-account-matched-audiences.md#activate-buying-group).

>[!BEGINSHADEBOX]

## Autorizzazioni richieste {#required-permissions}

La funzionalità di destinazione completa richiede le seguenti autorizzazioni [!DNL Adobe Experience Platform].

| Categoria | Autorizzazione |
|--- |--- |--- |
| Sandbox | Accesso alla sandbox |
| Dashboard | Visualizza dashboard standard |
| Dashboard | Gestione dashboard standard |
| Destinazioni | Visualizza destinazioni |
| Destinazioni | Gestire le destinazioni |
| Destinazioni | Attivare le destinazioni |
| Destinazioni | Attiva segmento senza mappatura |
| Destinazioni | Gestire e attivare la destinazione del set di dati |
| Destinazioni | Authoring delle destinazioni |
| Governance dei dati | Visualizza criteri di utilizzo dati |
| Governance dei dati | Gestire i criteri di utilizzo dei dati |
| Acquisizione dei dati | Visualizza origini |
| Acquisizione dei dati | Gestisci origini |
| Gestione profilo | Visualizza impostazioni profilo |
| Gestione profilo | Gestione impostazioni profilo |

>[!ENDSHADEBOX]

## Destinazioni supportati {#supported-destinations}

Prima di poter attivare un elenco statico, è necessario che nel catalogo delle destinazioni esista una destinazione. Nella barra di navigazione a sinistra, espandi **[!UICONTROL Connessioni]** e seleziona **[!UICONTROL Destinazioni]**. [!DNL Journey Optimizer B2B Edition] attualmente supporta la destinazione **[!UICONTROL Tipi di pubblico collegati]** (social). Vedi [_Tipi di pubblico corrispondenti all&#39;account LinkedIn_](../data/linkedin-account-matched-audiences.md) in

<!-- 
the following destinations:

* **[!UICONTROL Google Customer Match]** (Advertising)
* **[!UICONTROL Facebook Custom Audience]** (Social)
* **[!UICONTROL LinkedIn Matched Audience]** (Social)

![Access the available connector types](./assets/destinations-catalog.png){width="800" zoomable="yes"}

-->

>[!NOTE]
>
>Il catalogo visualizzato non è il catalogo completo delle [!DNL Adobe Experience Platform] destinazioni. Se si accede alle destinazioni direttamente da [!DNL Experience Platform], verrà visualizzato un catalogo più grande, ma solo queste destinazioni sono attualmente disponibili per l&#39;attivazione in [!DNL Journey Optimizer B2B Edition]. Altre destinazioni sono pianificate per le versioni future.

## Imposta una destinazione {#set-up-destination}

Ogni scheda di destinazione supportata mostra **[!UICONTROL Configura nuova destinazione]**. La configurazione di una destinazione è un prerequisito per l&#39;attivazione.

1. Nella scheda del connettore, fai clic su **[!UICONTROL Configura nuova destinazione]**.

   ![Configura una nuova destinazione](./assets/destinations-configure-new.png){width="500"}

1. Selezionare **[!UICONTROL Account esistente]** o **[!UICONTROL Nuovo account]** e immettere i dettagli dell&#39;account, ad esempio il nome e la descrizione.

1. Fai clic su **[!UICONTROL Connetti alla destinazione]**.

   Un flusso OAuth consente di accedere all’account corrispondente: LinkedIn, Google o Facebook.

   >[!IMPORTANT]
   >
   >A questo punto, non immettere i _[!UICONTROL Dettagli destinazione]_. È necessaria solo la connessione.

1. Completa la mappatura dei campi obbligatori tra gli attributi delle persone e i campi richiesti dalla destinazione.

1. Rivedi le impostazioni delle azioni di marketing e governance dei dati, quindi fai clic su **[!UICONTROL Salva]**.

Per i passaggi di installazione completi, vedere [Creare una nuova connessione di destinazione](https://experienceleague.adobe.com/it/docs/experience-platform/destinations/ui/connect-destination){target="_blank"} nella documentazione di [!DNL Experience Platform].

Una volta configurata, la destinazione è disponibile per l&#39;attivazione ovunque sia possibile selezionare una destinazione in [!DNL Journey Optimizer B2B Edition].

## Attivazione e sincronizzazione {#activation-sync}

L’attivazione è guidata dall’appartenenza statica all’elenco, con una sincronizzazione bidirezionale tra l’elenco e il pubblico di destinazione:

* L’aggiunta di una persona all’elenco statico la attiva sulla destinazione entro 24 ore, aggiungendola al pubblico di destinazione e, successivamente, a qualsiasi campagna feed dal pubblico.
* La rimozione di una persona dall’elenco statico la disattiva dalla destinazione. Vengono rimossi dal pubblico di destinazione e da qualsiasi campagna connessa.
* Lo stesso elenco può essere attivato su più destinazioni contemporaneamente. L&#39;appartenenza viene sincronizzata con tutti i membri.

>[!TIP]
>
>Per eseguire una campagna LinkedIn su un segmento, attiva l’elenco statico di tali persone nella destinazione LinkedIn Matched Audience. Tutti gli utenti dell&#39;elenco vengono aggiunti al pubblico corrispondente in LinkedIn, dove una campagna può indirizzarli e il pubblico rimane automaticamente aggiornato quando l&#39;elenco cambia.
