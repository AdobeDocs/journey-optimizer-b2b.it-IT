---
title: '[!DNL Adobe Target] tipi di pubblico esterni'
description: Attiva i tipi di pubblico esterni a  [!DNL Adobe Target]  tramite percorsi di account. Personalizzare le esperienze web B2B e mantenere la coerenza tra le diverse piattaforme.
feature: Integrations, Audiences, Account Journeys
role: User, Admin
source-git-commit: 598546c62cb2d567f19b26f7f760aa43e4dd0bc9
workflow-type: tm+mt
source-wordcount: '695'
ht-degree: 1%

---

# [!DNL Adobe Target] tipi di pubblico esterni

Puoi attivare e personalizzare le esperienze per tipi di pubblico esterni in [!DNL Adobe Target] tramite percorsi di account. Utilizza questa integrazione per ottenere una personalizzazione avanzata e personalizzata che aumenti il coinvolgimento e per mantenere la coerenza tra le piattaforme in [!DNL Target] e [!DNL Journey Optimizer B2B Edition]. Questa coerenza garantisce che i team allineino e personalizzino i canali web per i gruppi di acquisto in tutto il percorso di acquirenti B2B.

Per attivare un pubblico esterno tramite Adobe Target, si tratta di un flusso di lavoro in due passaggi:

1. [Aggiungi a pubblico cliente esterno](#add-to-customer-external-audience-from-a-journey) da un percorso.
2. [Attiva il pubblico esterno](#activate-the-external-audience-to-target-as-a-destination) in [!DNL Target] come destinazione in Experience Platform.

## Aggiungi al pubblico esterno del cliente da un percorso

Nel tuo percorso, [aggiungi un _Esegui un&#39;azione_ nodo](../journeys/action-nodes.md) per eseguire l&#39;azione _[!UICONTROL Aggiungi al pubblico esterno]_. Le azioni sono in genere ciò che desideri che accada come risultato di un qualche tipo di trigger, ad esempio un evento o un’azione precedente. Il percorso esegue l’azione quando un account qualificato con profili di persona raggiunge il nodo.

>[!NOTE]
>
>Quando un account qualificato con profili persona raggiunge il nodo _Aggiungi al pubblico cliente esterno_ in un percorso pubblicato, possono essere necessarie fino a 48 ore perché tali profili si popolino nel pubblico esterno.

1. Con il nodo _Esegui un&#39;azione_ selezionato nell&#39;area di lavoro del percorso, scegli l&#39;opzione _[!UICONTROL Azione su]_ **[!UICONTROL Persone]**.

1. Per _[!UICONTROL Azione sulle persone]_, scegli **[!UICONTROL Aggiungi a pubblico cliente esterno]**.

   ![Nodo Percorso - Azione sulle persone - Aggiungi a pubblico cliente esterno](./assets/node-add-external-audience.png){width="550" zoomable="yes"}

1. Imposta il pubblico esterno dalle proprietà del nodo a destra.

   * Se sono già stati creati uno o più tipi di pubblico esterni, puoi scegliere **[!UICONTROL Seleziona pubblico esistente]** e [seleziona il pubblico che desideri utilizzare](#choose-an-external-audience).

   * Se desideri [creare un pubblico](#create-an-external-audience) da utilizzare per il nodo, scegli **[!UICONTROL Crea nuovo]**.

### Creare un pubblico esterno

1. Dopo aver scelto l&#39;opzione **[!UICONTROL Crea nuovo]** nelle proprietà del nodo, fai clic su **[!UICONTROL Crea pubblico cliente esterno]**.

   ![Azione sulle persone - Aggiungi a pubblico cliente esterno - Crea nuova opzione](./assets/node-add-external-audience-create-new-option.png){width="400"}

1. Nella finestra di dialogo, immetti un **[!UICONTROL Nome]** (obbligatorio) e una **[!UICONTROL Descrizione]** (facoltativo) per il nuovo pubblico.

   ![Finestra di dialogo Crea pubblico cliente esterno](./assets/create-external-customer-audience-dialog.png){width="400"}

1. Fai clic su **[!UICONTROL Crea]**.

   Il sistema crea il nuovo pubblico e visualizza un messaggio di conferma. Puoi quindi continuare a utilizzarlo come pubblico esistente per l’azione del nodo.

### Seleziona un pubblico esterno

1. Dopo aver scelto l&#39;opzione **[!UICONTROL Seleziona esistente]** nelle proprietà del nodo, fai clic su **[!UICONTROL Seleziona pubblico cliente esterno]**.

   ![Azione sulle persone - Aggiungi a pubblico cliente esterno - seleziona l&#39;opzione esistente](./assets/node-add-external-audience-select-existing-option.png){width="300"}

1. Nella finestra di dialogo _[!UICONTROL Aggiungi pubblico]_, seleziona il pubblico che desideri utilizzare.

   È possibile immettere testo nel campo _Ricerca_ per filtrare gli elementi visualizzati in modo che corrispondano al nome del pubblico.

   ![Azione sulle persone: aggiungi al pubblico esterno del cliente - finestra di dialogo Aggiungi pubblico](./assets/add-audience-dialog.png){width="700" zoomable="yes"}

1. Fai clic su **[!UICONTROL Aggiungi pubblico]**.

## Attivare il pubblico esterno su Target come destinazione

Per attivare il pubblico esterno in Adobe Target è necessario aver configurato [!DNL Adobe Target] come destinazione in [!DNL Real-time Customer Data Platform (RTCDP)]. Per ulteriori informazioni su questa configurazione, consulta la [documentazione di RTCDP](https://experienceleague.adobe.com/it/docs/platform-learn/tutorials/destinations/target/configure-the-target-destination){target="_blank"}.

>[!IMPORTANT]
>
>L’utilizzo dell’attivazione tramite un percorso richiede che l’implementazione di RTCDP utilizzi l’Indirizzo e-mail come identità.

Il processo di attivazione richiede l&#39;aggiunta di [!DNL Adobe Target] come pubblico esterno o destinazione esterna. Per iniziare, crea un pubblico [!DNL Target] nel generatore di pubblico. Puoi anche creare un pubblico segnaposto e aggiungere la funzione pubblico esterno.

>[!BEGINSHADEBOX]

![Icona autorizzazioni AEP](../../assets/do-not-localize/icon_permissions-outline.svg) Questi passaggi richiedono le seguenti autorizzazioni per il ruolo utente assegnato:

* **[!UICONTROL Experience Platform]** - Per la risorsa _[!UICONTROL Destinazioni]_: `Activate Destinations`, `Manage and Activate Dataset Destination` e `View Destination`
* **[!DNL Target]** - `Approver`

>[!ENDSHADEBOX]

1. In Experience Platform, vai a **[!UICONTROL Connessioni]** > **[!UICONTROL Destinazioni]** nel menu di navigazione a sinistra.

1. Fai clic sulla scheda **[!UICONTROL Sfoglia]**.

1. Individua la connessione di destinazione che desideri utilizzare per attivare i segmenti, fai clic sull&#39;icona _Altro menu_ ( **...** ) accanto al nome e scegli **[!UICONTROL Attiva pubblico]**.

   Immetti il testo nel campo _[!UICONTROL Ricerca]_ per filtrare le destinazioni visualizzate per una corrispondenza in base al nome.

   ![Experience Platform - destinazioni - sfoglia destinazioni Target - menu altro](./assets/aep-destinations-activate-target-audience.png){width="800" zoomable="yes"}

1. Nell&#39;elenco _[!UICONTROL Tipi di pubblico disponibili]_, seleziona il pubblico esterno e fai clic su **[!UICONTROL Avanti]**.

   ![Experience Platform - destinazioni - sfoglia destinazioni Target - menu altro](./assets/aep-destinations-activate-target-audience-available-audiences.png){width="700" zoomable="yes"}

1. Eseguire qualsiasi mapping di campi aggiuntivo alla destinazione (facoltativo) e fare clic su **[!UICONTROL Avanti]**.

1. Rivedi i nuovi parametri del pubblico e fai clic su **[!UICONTROL Fine]**.

   ![Experience Platform - destinazioni - attiva destinazione - revisione](./assets/aep-destinations-activate-target-audience-review.png){width="700" zoomable="yes"}

Al momento dell&#39;attivazione, puoi visualizzare il pubblico in [tipi di pubblico di Adobe Target](https://experienceleague.adobe.com/en/docs/target/using/audiences/create-audiences/audiences#use-list){target="_blank"} e utilizzarlo nelle attività di Adobe Target.

