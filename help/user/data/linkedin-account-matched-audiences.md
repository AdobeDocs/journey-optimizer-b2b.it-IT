---
title: Tipi di pubblico associati all’account LinkedIn
description: Scopri come collegare un account LinkedIn e attivare un flusso di dati per i gruppi di acquisto.
exl-id: d2303529-16c4-4b0b-b8c8-404dff8ec63d
source-git-commit: 9031191ead88652df95137a122f379b0ae2516a7
workflow-type: tm+mt
source-wordcount: '742'
ht-degree: 16%

---

# Tipi di pubblico associati all’account LinkedIn

Journey Optimizer B2B edition offre la possibilità di generare tipi di pubblico di LinkedIn Ad tramite i tipi di pubblico abbinati all’account ed è progettato per aiutarti a riempire ruoli vuoti nei gruppi di acquisto. Definendo un set di filtri per gruppi di acquisto, puoi mantenere un pubblico abbinato a LinkedIn per eseguire il targeting dei potenziali clienti che corrispondono ai parametri del gruppo di acquisto. Questa funzione sfrutta le destinazioni di Experience Platform per gestire alcuni aspetti dell’integrazione. È previsto un limite di dieci flussi di dati.

Prima di avviare un flusso di dati da Journey Optimizer B2B edition, è necessario disporre di almeno un&#39;istanza del connettore di destinazione [(Companies) LinkedIn MatchedIn Audience](https://experienceleague.adobe.com/it/docs/experience-platform/destinations/catalog/social/linkedin#connect){target="_blank"} con un account LinkedIn Campaign Manager configurato nell&#39;applicazione Experience Platform.

## Configurare una nuova connessione di account LinkedIn {#linkedin-destination-setup}

>[!CONTEXTUALHELP]
>id="ajo-b2b_linkedin_destination_setup"
>title="È richiesta la configurazione della destinazione LinkedIn"
>abstract="Invia account filtrati per gruppi acquisti a una destinazione LinkedIn per interagire con potenziali membri din un gruppo acquisti. Puoi creare fino a 10 flussi di dati per 10 diversi gruppi di account filtrati. Per iniziare a utilizzare questa funzione, devi prima aggiungere una destinazione LinkedIn."

1. In Experience Platform, vai a **[!UICONTROL Connessioni]** > **[!UICONTROL Destinazioni]** nel menu di navigazione a sinistra e seleziona la scheda **[!UICONTROL Catalogo]**.

1. Nel catalogo individuare il connettore **[!UICONTROL (Companies) LinkedIn Matched Audience]**.

   >[!TIP]
   >
   >È possibile trovare rapidamente il connettore immettendo `LinkedIn` nella casella di ricerca.

1. Nella scheda del connettore, fai clic sull&#39;icona _Altro_ (**...**) e scegli **[!UICONTROL Configura nuova destinazione]**.

   ![Accedi al connettore LinkedIn (Aziende) del pubblico corrispondente](./assets/aep-destinations-catalog-linkedin.png){width="800" zoomable="yes"}

1. Seleziona **[!UICONTROL Nuovo account]** e fai clic su **[!UICONTROL Connetti alla destinazione]**.

   ![Connetti un nuovo account LinkedIn](./assets/aep-destinations-catalog-linkedin-new-account.png){width="500"}

1. Immetti le credenziali di LinkedIn e accedi.

   Dopo l’autenticazione, l’account LinkedIn viene connesso come destinazione in Experience Platform.

   ![Viene visualizzata la conferma della connessione dell&#39;account](./assets/aep-destinations-catalog-linkedin-connected.png){width="400"}

   >[!IMPORTANT]
   >
   >A questo punto, **non** immettere i _[!UICONTROL dettagli di destinazione]_. È necessaria solo la connessione.

## Aggiorna i dettagli dell&#39;account

Il nome e la descrizione dell’account LinkedIn sono visibili per i gruppi di acquisto in Journey Optimizer B2B edition. È consigliabile aggiornare queste informazioni in modo che siano facilmente identificabili per gli addetti al marketing che lavorano con i gruppi di acquisto. Puoi modificare i dettagli dell’account nell’interfaccia utente di Experience Platform o Journey Optimizer B2B edition.

1. Vai a **[!UICONTROL Connessioni]** > **[!UICONTROL Destinazioni]** nella navigazione a sinistra e seleziona la scheda **[!UICONTROL Account]**.

1. Per il nuovo account creato, fare clic sul menu _Altro_ (**...**) e scegliere **[!UICONTROL Modifica dettagli]**.

   ![Modificare i dettagli dell’account](./assets/aep-destinations-accounts-edit-details.png){width="800" zoomable="yes"}

1. Nella finestra di dialogo, aggiorna il nome e la descrizione.

   ![Modifica nome e descrizione](./assets/destinations-linkedin-account-edit-details-dialog.png){width="500"}

1. Fai clic su **[!UICONTROL Salva]**.

## Attiva l&#39;account per i gruppi di acquisto

>[!NOTE]
>
>Se disponi già di dieci flussi di dati, non puoi crearne un altro. Se raggiungi il massimo, eliminane uno in Experience Platform prima di crearne uno nuovo in Journey Optimizer B2B edition.

1. In Journey Optimizer B2B edition, passa a **[!UICONTROL Account]** > **[!UICONTROL Gruppi acquisti]** nel menu di navigazione a sinistra.

1. Fai clic sulla scheda **[!UICONTROL Sfoglia]**.

1. Fai clic su **[!UICONTROL Attiva nella destinazione LinkedIn]** in alto a destra.

   ![Modificare i dettagli dell’account](./assets/activate-linkedin-destination.png){width="800" zoomable="yes"}

1. Assegna al flusso di dati un nome descrittivo e una descrizione (facoltativo).

   Dopo averlo salvato, al nome specificato per il flusso di dati viene aggiunto _AJOB2B_ per facilitare l&#39;identificazione del flusso di dati in Experience Platform.

1. Immetti l&#39;[ID account dell&#39;account LinkedIn Campaign Manager](https://www.linkedin.com/help/lms/answer/a424270).

   Puoi trovare l’ID account in base al nome nell’interfaccia utente di Campaign Manager.

   ![Aggiungi dettagli flusso di dati](./assets/destinations-linkedin-activate-details.png){width="700" zoomable="yes"}

1. Fai clic su **[!UICONTROL Seleziona i filtri del gruppo di acquisto]** e definisci i parametri del pubblico del tuo account.

   >[!IMPORTANT]
   >
   >Al momento, non è possibile modificare i filtri dopo l’attivazione del flusso di dati. Controlla nuovamente il lavoro prima di attivare il flusso di dati.

   ![Specifica il pubblico dell&#39;account filtrato in base ai gruppi di acquisto](./assets/destinations-linkedin-activate-buying-group-filters.png){width="400"}

   Per il **[!UICONTROL Punteggio di coinvolgimento]**, l’operatore `Between` è inclusivo, così come gli intervalli di percentuale. Ad esempio, 5.1 e 5 sono entrambi _tra_ 5 e 6.

   Le condizioni vuote vengono trattate come `Is Any`.

   Fai clic su **[!UICONTROL Salva]** per aggiungere i filtri specificati.

1. Fare clic su **[!UICONTROL Seleziona destinazione LinkedIn]** e scegliere la destinazione LinkedIn configurata che si desidera utilizzare.

   Al momento dell’attivazione, questa impostazione crea il flusso di dati utilizzando la configurazione di destinazione e un segmento virtuale corrispondente.

1. Controlla nuovamente le impostazioni e fai clic su **[!UICONTROL Attiva]** in alto a destra.

   Fai di nuovo clic su **[!UICONTROL Attiva]** nella finestra di dialogo di conferma.

   In Experience Platform viene visualizzato un banner con un collegamento al menu dei flussi di dati per consentirti di controllare il record del flusso di dati.

## Orchestrare il coinvolgimento di paid media

Puoi interagire con i membri dell’account tramite un canale multimediale a pagamento, ad esempio i tipi di pubblico di LinkedIn Ad, per acquisire, coltivare e qualificarli per le vendite. Utilizza un nodo _Esegui un&#39;azione_ in un percorso di account per automatizzare il coinvolgimento con i membri chiave di un account tramite un canale esterno che sia più adatto per i diversi membri dell&#39;account.

>[!VIDEO](https://video.tv.adobe.com/v/3448649/?learn=on)