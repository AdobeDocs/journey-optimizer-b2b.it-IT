---
title: Destinazioni
description: Scopri le autorizzazioni richieste, le destinazioni supportate e come collegare una destinazione in Journey Optimizer B2B Prime per attivare elenchi di persone statici per le piattaforme pubblicitarie e social.
badgeBeta: label="Beta" type="informative" tooltip="Questa funzione è attualmente in versione beta limitata"
autotag-review: '2026-06-17T18:30:02.442Z'
TQID: 'https://experienceleague.adobe.com/xO1p-VvIfv1KB77g0l2-fFRHQ0w2hy97vnG1QHpMw8c'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: aed878b8-11d0-487c-828b-d23b2051ec37
  - id: beb5f4be-cec3-471a-9db6-831a77dd3ac9
  - id: c8f3fb27-3167-48ac-a66a-fa4bc3f58dda
subfeature_v2:
  - id: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 7a954ba7ade748d5d51cae82a0cddb64449fa2a2
workflow-type: tm+mt
source-wordcount: 655
ht-degree: 8%

---

# Destinazioni

Le destinazioni sono integrazioni predefinite che ti consentono di inviare [elenchi di persone statiche](./people-lists.md#static-lists) da [!DNL Journey Optimizer B2B Prime] a piattaforme pubblicitarie o social esterne, ad esempio un pubblico della campagna LinkedIn, un pubblico di Google Customer Match o un pubblico personalizzato di Facebook. L’attivazione di un elenco statico in una destinazione mantiene sincronizzata l’appartenenza: quando le persone vengono aggiunte o rimosse dall’elenco, vengono aggiunte o rimosse in modo corrispondente dal pubblico di destinazione e, per estensione, da qualsiasi campagna creata dal pubblico.

Esistono due modi per attivare le persone in una destinazione connessa:

* **Da un elenco statico** - Attiva un elenco statico esistente direttamente dalla scheda **_[!UICONTROL Elenchi persone]_**. Vedi [Attiva in una destinazione](./people-lists.md#static-list-activate).
* **Da un percorso di persone** — Aggiungi un&#39;azione **_[!UICONTROL Attiva nella destinazione]_** a un percorso di percorso in modo che chiunque raggiunga tale nodo venga aggiunto a un elenco e inviato alla destinazione. Vedere [_Aggiungere un nodo azione_](../marketing/action-nodes.md#add-an-action-node).

>[!BEGINSHADEBOX]

## Autorizzazioni richieste {#required-permissions}

La funzionalità di destinazione completa richiede l&#39;abilitazione delle seguenti autorizzazioni [!DNL Adobe Experience Platform].

| Categoria | Autorizzazione | Obbligatorio |
|--- |--- |--- |
| Sandbox | Accesso alla sandbox _(abilitato per impostazione predefinita)_ | Sì |
| Dashboard | Visualizza dashboard standard | Sì |
| Dashboard | Gestione dashboard standard | Sì |
| Destinazioni | Visualizza destinazioni | Sì |
| Destinazioni | Gestire le destinazioni | Sì |
| Destinazioni | Attivare le destinazioni | Sì |
| Destinazioni | Attiva segmento senza mappatura | Sì |
| Destinazioni | Gestire e attivare la destinazione del set di dati | Sì |
| Destinazioni | Authoring delle destinazioni | Sì |
| Governance dei dati | Visualizza criteri di utilizzo dati | Sì |
| Governance dei dati | Gestire i criteri di utilizzo dei dati | Sì |
| Acquisizione dei dati | Visualizza origini | Sì |
| Acquisizione dei dati | Gestisci origini | Sì |
| Gestione profilo | Visualizza impostazioni profilo | Sì |
| Gestione profilo | Gestione impostazioni profilo | Sì |

>[!ENDSHADEBOX]

## Destinazioni supportati {#supported-destinations}

Prima di poter attivare un elenco statico, è necessario che nel catalogo delle destinazioni esista una destinazione. Nella barra di navigazione a sinistra, espandi **[!UICONTROL Connessioni]** e seleziona **[!UICONTROL Destinazioni]**. [!DNL Journey Optimizer B2B Prime] supporta attualmente le seguenti destinazioni:

* **[!UICONTROL Google Customer Match]** (Advertising)
* **[!UICONTROL Pubblico personalizzato Facebook]** (Social)
* **[!UICONTROL Pubblico collegato]** (Social)

![Accedere ai tipi di connettore disponibili](./assets/destinations-catalog.png){width="800" zoomable="yes"}

>[!NOTE]
>
>Questo catalogo non è il catalogo completo delle [!DNL Adobe Experience Platform] destinazioni. Se si accede alle destinazioni direttamente da [!DNL Experience Platform], verrà visualizzato un catalogo più grande, ma solo queste destinazioni sono attualmente disponibili per l&#39;attivazione in [!DNL Journey Optimizer B2B Prime]. Altre destinazioni sono pianificate per le versioni future.

## Configurare una destinazione {#set-up-destination}

Ogni scheda di destinazione supportata mostra **[!UICONTROL Configura nuova destinazione]**. La configurazione di una destinazione è un prerequisito per l&#39;attivazione.

1. Nella scheda del connettore, fai clic su **[!UICONTROL Configura nuova destinazione]**.

1. Selezionare **[!UICONTROL Account esistente]** o **[!UICONTROL Nuovo account]** e immettere i dettagli dell&#39;account, ad esempio il nome e la descrizione.

   ![Connetti un nuovo account di destinazione](./assets/destinations-configure-new.png){width="500"}

1. Fai clic su **[!UICONTROL Connetti alla destinazione]**.

   Un flusso OAuth consente di accedere all’account corrispondente: LinkedIn, Google o Facebook.

   >[!IMPORTANT]
   >
   >A questo punto, **non** immettere i _[!UICONTROL dettagli di destinazione]_. È necessaria solo la connessione.

1. Completa la mappatura dei campi obbligatori tra gli attributi delle persone e i campi richiesti dalla destinazione.

1. Rivedi le impostazioni delle azioni di marketing e governance dei dati, quindi fai clic su **[!UICONTROL Salva]**.

Per i passaggi di installazione completi, vedere [Creare una nuova connessione di destinazione](https://experienceleague.adobe.com/it/docs/experience-platform/destinations/ui/connect-destination){target="_blank"} nella documentazione di [!DNL Experience Platform].

Una volta configurata, la destinazione è disponibile per l&#39;attivazione ovunque sia possibile selezionare una destinazione in [!DNL Journey Optimizer B2B Prime].

## Attivazione e sincronizzazione {#activation-sync}

L’attivazione è guidata dall’appartenenza statica all’elenco, con una sincronizzazione bidirezionale tra l’elenco e il pubblico di destinazione:

* L’aggiunta di una persona all’elenco statico la attiva sulla destinazione entro 24 ore, aggiungendola al pubblico di destinazione e, successivamente, a qualsiasi campagna feed dal pubblico.
* La rimozione di una persona dall’elenco statico la disattiva dalla destinazione, poiché viene rimossa dal pubblico di destinazione e da qualsiasi campagna connessa.
* Lo stesso elenco può essere attivato su più destinazioni contemporaneamente; l’appartenenza si sincronizza con tutte le destinazioni.

>[!TIP]
>
>Per eseguire una campagna LinkedIn su un segmento, attiva l’elenco statico di tali persone nella destinazione LinkedIn Matched Audience. Tutti gli utenti dell&#39;elenco vengono aggiunti al pubblico corrispondente in LinkedIn, dove una campagna può indirizzarli e il pubblico rimane automaticamente aggiornato quando l&#39;elenco cambia.
