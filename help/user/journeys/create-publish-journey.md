---
title: Creare e pubblicare un Percorso
description: Crea percorsi di account e persone nell’area di lavoro visiva, aggiungi nodi azione ed evento, configura la pianificazione e pubblica per l’orchestrazione live in Journey Optimizer B2B Edition.
feature: Account Journeys
role: User
exl-id: f536b1a1-8dfe-437f-a84d-b66879529621
autotag-review: 2026-03-30T23:14:46.843Z
TQID: 'https://experienceleague.adobe.com/-emMaxlrae40JXP0tThacD3xA27d5OzO8tX6o-mOnfg'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
    internal-label: Journey Optimizer B2B Edition
feature_v2:
  - id: a4b836d9-ffdd-4df3-a62a-f78b830cf059
    internal-label: Journeys
subfeature_v2:
  - id: c31bc6c7-76bc-467b-80c0-7315a4e3f6be
    internal-label: Account Journeys
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: d00e9f03-e50b-4162-b143-0c0817c937c2
    internal-label: Customer journeys
source-git-commit: 9d5641659907d61be992ed218088a023a5211c56
workflow-type: tm+mt
source-wordcount: '1101'
ht-degree: 5%
---
# Creare e pubblicare un percorso

Per iniziare un nuovo percorso, create il percorso e quindi costruite i nodi e il flusso del percorso nella mappa del percorso.

![Video](../../assets/do-not-localize/icon-video.svg){width="30"} [Guarda il video introduttivo](#overview-video)

## Creare un percorso

In **[!UICONTROL Gestione Percorsi]** nella barra di navigazione a sinistra, selezionare il tipo di percorso che si desidera creare:

* **[!UICONTROL percorsi di account]**
* **[!UICONTROL percorsi di persone]**

_Per aggiungere un nuovo percorso :_

+++Percorso di account

1. Fai clic su **[!UICONTROL Crea Percorso di account]** in alto a destra nella pagina.

1. Nella finestra di dialogo, immetti un **[!UICONTROL Nome]** (obbligatorio) e una **[!UICONTROL Descrizione]** (facoltativo) univoci.

   ![Finestra di dialogo Crea Percorso di account](./assets/account-journey-create-dialog.png){width="400"}

1. Fai clic su **[!UICONTROL Crea]**.

+++

+++Percorso persone

1. Fai clic su **[!UICONTROL Crea Percorso]** in alto a destra della pagina.

1. Nella finestra di dialogo, immetti un **[!UICONTROL Nome]** (obbligatorio) e una **[!UICONTROL Descrizione]** (facoltativo) univoci.

   ![Finestra di dialogo Crea Percorso](./assets/person-journey-create-dialog.png){width="400"}

1. Fai clic su **[!UICONTROL Crea]**.

+++

## Componenti per la progettazione di percorsi

La mappa del percorso __ è la zona centrale nell&#39;area di lavoro del percorso. È in questa zona che puoi aggiungere nodi di percorso e configurarli. Fai clic su un nodo per aprire il relativo riquadro delle proprietà a destra dell’area di lavoro e impostarlo in base alla progettazione. Un percorso inizia sempre con un nodo di pubblico, in cui puoi definire l’input per il percorso:

* [Nodo pubblico account](./account-audience-nodes.md)
* [Nodo di pubblico della persona](./person-audience-nodes.md)

Dopo aver creato un percorso di account e aver aggiunto il pubblico, progetta il percorso utilizzando i nodi. La mappa del percorso fornisce un’area di lavoro in cui puoi creare casi di utilizzo del marketing B2B a più passaggi utilizzando i seguenti tipi di nodo per creare un percorso di account:

* [Intraprendere un’azione](./action-nodes.md)
* [Ascoltare un evento](./listen-for-event-nodes.md)
* [Suddividi percorsi](./split-merge-paths-nodes.md)
* [Percorsi suddivisi per variante](./variant-split-paths-nodes.md)
* [Prossimo percorso migliore](./next-best-path-node.md)
* [Attendere](./wait-nodes.md)
* [Unisci percorsi](./split-merge-paths-nodes.md)

## Guardrail

Per aiutarti a creare un percorso senza errori, sono presenti le seguenti protezioni:

* _Eliminazione di un nodo di percorso suddiviso_: l&#39;eliminazione di un nodo richiede l&#39;eliminazione di tutti i nodi successivi in ciascun percorso.
* _Eliminazione di un nodo di unione_: un nodo di unione può essere eliminato solo quando vi è un percorso connesso. Per eliminare un nodo di unione, lasciare selezionato un solo percorso.
* _Passaggio tra account e persone_: la modifica della selezione da account a persone comporta l&#39;eliminazione di tutti i nodi successivi in ogni percorso.

## Aggiungi un nodo

1. Passa alla mappa del percorso.

1. Fai clic sull&#39;icona più ( **+** ) sul percorso e scegli il tipo di nodo.

   ![Fai clic su + e scegli il tipo per aggiungere un nodo di percorso al percorso](./assets/node-add-menu.png){width="400" zoomable="no"}

   I tipi di nodo disponibili dipendono dal tipo di percorso e dal contesto del percorso. Per ulteriori informazioni, vedere [_Nodi di Percorso_](./journey-nodes.md).

1. Imposta le proprietà del nodo a destra.

   Le proprietà dipendono dal tipo di nodo.

## Etichettare un nodo {#label-a-node}

In [!DNL Adobe Journey Optimizer B2B Edition] ogni nodo della mappa di percorso visualizza il nome predefinito, ad esempio _Attendi_ o _Invia e-mail_. Aggiungi le etichette di visualizzazione per distinguere i nodi dello stesso tipo e identificare lo scopo di ciascun passaggio. Ad esempio, utilizza _un intervallo di 48 ore_ o _E-mail di benvenuto_.

Puoi aggiungere un’etichetta di visualizzazione a qualsiasi nodo in un percorso di account o in un percorso di persone.

1. Nella mappa del percorso, seleziona il nodo da etichettare.

1. Nelle proprietà del nodo, immettere il testo nel campo **[!UICONTROL Etichetta di visualizzazione]**.

   L’etichetta può contenere fino a 255 caratteri.

1. Fai clic all’esterno del campo per applicare l’etichetta.

   ![Aggiungi un&#39;etichetta di visualizzazione per distinguere il nodo all&#39;interno del percorso](./assets/node-display-label.png){width="500" zoomable="no"}

   L&#39;etichetta sostituisce il nome predefinito sul nodo nella mappa del percorso.

Per ripristinare il nome predefinito, cancellare il campo **[!UICONTROL Etichetta di visualizzazione]** e fare clic all&#39;esterno del campo.

Quando pubblichi il percorso, l’etichetta di visualizzazione per ciascun nodo viene salvata con il percorso pubblicato.

>[!NOTE]
>
>Le etichette di visualizzazione non sono disponibili per i nodi nei percorsi creati prima che questa funzionalità fosse disponibile.

Le etichette dei nodi sono disponibili nello schema `AJOB2B - 1.5.4 - journey node` e nel set di dati `AJOB2B-1_5_4-journey_node`. È possibile eseguire query sulle etichette in [!DNL Adobe Experience Platform] e utilizzarle per il reporting in [!DNL Adobe Customer Journey Analytics]. Per ulteriori informazioni sull&#39;esecuzione di query sui dati esportati, esaminare i [prerequisiti per la query del set di dati](../data/aep-query-examples.md#prerequisites).

## Eliminare un nodo

1. Passa alla mappa del percorso.

1. Nelle proprietà del nodo a destra, fai clic sull&#39;icona _Elimina_ ( ![Elimina icona](../assets/do-not-localize/icon-delete.svg) ).

1. Nella finestra di dialogo di conferma, fai clic su **[!UICONTROL Elimina]**.

## Aggiungere ed eliminare un percorso

1. Nella mappa del percorso, fai clic sull&#39;icona più ( **+** ) sul percorso e aggiungi il [nodo percorso diviso](./split-merge-paths-nodes.md#split-paths).

1. Nelle proprietà del nodo a destra, seleziona **[!UICONTROL Account]**.

1. Per aggiungere altri percorsi, fare clic su **[!UICONTROL Aggiungi percorso]**.

   Per ogni percorso creato nel percorso, nelle proprietà viene visualizzata una nuova scheda percorso.

1. Passa a uno dei percorsi nel percorso e aggiungi i nodi [action](./action-nodes.md) o [event](./listen-for-event-nodes.md) a tale percorso utilizzando l&#39;icona più.

1. Seleziona il nodo [split path](./split-merge-paths-nodes.md) per aprire le proprietà a destra.

   I percorsi con nodi non possono essere eliminati.

1. Per eliminare un percorso, è necessario eliminare prima tutti i nodi del percorso.

## Pianificare un percorso

Quando pubblichi un percorso, può iniziare immediatamente o in una data futura pianificata. La data di fine può essere un massimo di tre anni dalla data di inizio. Dopo la pubblicazione di un percorso (_Stato Live_), puoi aggiornare la data di fine del percorso ma non la data di inizio.

1. Passa alla mappa del percorso.

1. Pianifica il percorso facendo clic su **[!UICONTROL Impostazioni Percorso]** nell&#39;intestazione.

1. Nella finestra di dialogo, imposta le opzioni di pianificazione:

   * Scegli un tipo di pianificazione.

     Per attivare il percorso in fase di pubblicazione, scegliere **[!UICONTROL Immediatamente]**.

     Per attivare il percorso in una data futura, scegli **[!UICONTROL In una data specifica]** e fai clic sull&#39;icona _Calendario_ per selezionare la data.

     ![Finestra di dialogo impostazioni Percorso](./assets/account-journey-settings-dialog.png){width="400" zoomable="no"}

   * Specifica la **[!UICONTROL data di fine]** per il percorso. Può essere fino a tre anni dalla data di inizio (questo campo è obbligatorio per la pubblicazione).

1. Fai clic su **[!UICONTROL Salva]**.

   Quando sei pronto a pubblicare il tuo percorso, puoi rivedere queste impostazioni facendo clic su _[!UICONTROL Pubblica]_.

## Pubblicare un percorso

È possibile pubblicare un percorso se non sono presenti errori di blocco. Quando viene pubblicato, lo stato del percorso cambia in _Live_. Se il percorso presenta errori, il pulsante _[!UICONTROL Pubblica]_ è inattivo con le informazioni sul contenuto: `Resolve errors before publishing`.

>[!NOTE]
>
>Dopo la pubblicazione di un percorso di account, si verifica un ritardo di 24 ore per l&#39;inserimento degli account idonei nel percorso.

1. Nella parte superiore destra della mappa del percorso, fai clic su **[!UICONTROL Pubblica]**.

1. Nella finestra di dialogo _[!UICONTROL Rivedi impostazioni percorso]_, imposta le opzioni di avvio del percorso.

   Se hai già impostato le impostazioni di percorso per definire una pianificazione, controlla le impostazioni.

   Se è necessario impostare l&#39;attivazione del percorso, scegliere un tipo di pianificazione:

   * Per attivare il percorso in fase di pubblicazione, scegliere **[!UICONTROL Immediatamente]**.

   * Per attivare il percorso in una data futura, scegli **[!UICONTROL In una data specifica]** e fai clic sull&#39;icona _Calendario_ per selezionare la data.

1. Se necessario, specifica la **[!UICONTROL data di fine]** per il percorso.

   ![Finestra di dialogo impostazioni Percorso](./assets/journey-publish-dialog.png){width="400" zoomable="no"}

   Può essere fino a tre anni dalla data di inizio (questo campo è obbligatorio per la pubblicazione).

1. Fai clic su **[!UICONTROL Avanti]**.

1. Nella finestra di dialogo di conferma, fai clic su **[!UICONTROL Pubblica]**.

## Video di panoramica

>[!VIDEO](https://video.tv.adobe.com/v/3443204/?learn=on)
