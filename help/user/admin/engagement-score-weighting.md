---
title: Configurare la ponderazione dei punteggi di coinvolgimento
description: Crea modelli di punteggio di coinvolgimento personalizzati con attività ponderate per misurare con precisione l'impegno e l'intento del gruppo di acquisto in [!DNL Journey Optimizer B2B Edition].
feature: Setup, Engagement, Buying Groups
role: Admin
exl-id: 50d79d31-5ad8-41ed-a62b-4aa2ed9e837f
source-git-commit: ff635309749cfb7c065522a34b1228e71b144a9f
workflow-type: tm+mt
source-wordcount: '1373'
ht-degree: 0%

---

# Configurare la ponderazione del punteggio di coinvolgimento personalizzato

Un [punteggio di coinvolgimento del gruppo di acquisto](../buying-groups/engagement-scores.md) riflette il livello di coinvolgimento valutando varie attività registrate per i membri del gruppo di acquisto. Con la ponderazione del punteggio personalizzata, i team delle operazioni di marketing hanno la flessibilità di definire i propri modelli per la ponderazione delle attività. Un modello di punteggio personalizzato produce un riflesso più accurato della pipeline dando priorità ai comportamenti che segnalano più accuratamente l’intento di acquisto nel processo di vendita.

In qualità di amministratore, puoi definire più modelli di punteggio di coinvolgimento per la tua organizzazione, ma può essere attivo un solo modello alla volta. Puoi definire un modello di punteggio in base al peso applicato a ogni attività di punteggio del coinvolgimento.

>[!PREREQUISITES]
>
>Per definire e attivare un modello di ponderazione dei punteggi di coinvolgimento, è necessario disporre dell&#39;autorizzazione _[!UICONTROL Gestisci configurazioni amministratore B2B]_ [prodotto](./user-management.md#b2b-product-permissions).

## Accedere ai modelli di ponderazione dei punteggi di coinvolgimento

Apri l&#39;elenco di ponderazione del punteggio di coinvolgimento __ per visualizzare i modelli attivi, bozza e archiviati:

1. Nel menu di navigazione a sinistra, scegli **[!UICONTROL Amministrazione]** > **[!UICONTROL Configurazioni]**.

1. Fare clic su **[!UICONTROL Ponderazione punteggio coinvolgimento]** nel pannello intermedio per visualizzare l&#39;elenco dei modelli di punteggio.

   Da questa pagina è possibile [creare (duplicare)](#create-an-engagement-score-model), [attivare](#activate-a-score-model) e [modificare](#change-the-engagement-weighting-settings) i modelli di punteggio di coinvolgimento.

   ![Accedere ai modelli di punteggio di coinvolgimento definiti](./assets/configuration-engagement-scoring-list.png){width="800" zoomable="yes"}

   Nell&#39;elenco vengono visualizzati i modelli aggiornati più di recente nella parte superiore (ordinati per _[!UICONTROL Ultimo aggiornamento]_) e viene inclusa la possibilità di eseguire ricerche per _[!UICONTROL Nome]_.

   Puoi personalizzare la tabella visualizzata facendo clic sull&#39;icona _Impostazioni colonna_ ( ![Impostazioni colonna](../assets/do-not-localize/icon-column-settings.svg) ) nell&#39;angolo in alto a destra e selezionando o deselezionando le caselle di controllo della colonna.

   ![Colonne da visualizzare nell&#39;elenco di ponderazione dei punteggi di coinvolgimento](./assets/configuration-engagement-scoring-list-columns.png){width="300"}

1. Per accedere ai dettagli di un modello di punteggio di coinvolgimento, fai clic sul nome.

### Modello punteggio predefinito

Il sistema crea un modello di punteggio di coinvolgimento iniziale denominato _Modello di ponderazione attività 1_. Lo stato del modello e le attività di coinvolgimento dipendono dall&#39;architettura dei dati dell&#39;ambiente [!DNL Journey Optimizer B2B Edition]:

* **Architettura semplificata** (Beta): se l&#39;ambiente utilizza l&#39;[architettura semplificata](../simplified-architecture.md), le attività di coinvolgimento si basano su eventi Experience Platform standard e personalizzati. Il valore predefinito per tutte le attività è 0.

  ![Modello di ponderazione punteggio coinvolgimento predefinito per l&#39;architettura semplificata](./assets/configuration-engagement-scoring-model-default.png){width="600" zoomable="yes"}

* **Architettura standard** - Se l&#39;ambiente utilizza l&#39;architettura standard, l&#39;istanza [!DNL Marketo Engage] connessa è l&#39;origine dei dati dell&#39;attività di coinvolgimento. Il modello predefinito è attivo finché non crei una versione personalizzata e la attivi.

  ![Modello di ponderazione punteggio coinvolgimento predefinito per l&#39;architettura standard](./assets/configuration-engagement-scoring-model-default-me.png){width="600" zoomable="yes"}

Quando attivi un modello personalizzato, lo stato del modello attivo diventa _Archiviato_. Se decidi di ripristinare il modello di punteggio di coinvolgimento predefinito, puoi duplicare il modello predefinito originale e quindi attivarlo o utilizzarlo come punto di partenza per un altro modello personalizzato.

### Eliminare un modello 2D

È possibile eliminare una bozza di modello di punteggio di coinvolgimento se si decide di non attivarlo in futuro. Fai clic sull&#39;icona _Altro menu_ (***...***) accanto al nome del modello di punteggio bozza nell&#39;elenco e scegli **[!UICONTROL Elimina]**.

![Elimina modello punteggio bozza](./assets/configuration-engagement-scoring-model-more-delete.png){width="350"}

Nella finestra di dialogo di conferma, fai clic su **[!UICONTROL Elimina]**.

## Creare un modello di punteggio di coinvolgimento personalizzato

Per creare un modello di punteggio di coinvolgimento personalizzato, duplica il modello predefinito o un altro modello personalizzato già creato. Puoi duplicare il modello _Attivo_ corrente, un modello _Bozza_ o un modello _Archiviato_. Quindi, modifica il modello duplicato in base alle tue esigenze.

1. Fai clic sul nome del modello per aprire la pagina dei dettagli del modello e fai clic su **[!UICONTROL Duplica]** in alto a destra.

   ![Duplica il modello attivo](./assets/configuration-engagement-scoring-model-duplicate.png){width="600" zoomable="yes"}

   Puoi anche fare clic sull&#39;icona _Altro menu_ (***...***) accanto al nome del modello di punteggio nell&#39;elenco e scegliere **[!UICONTROL Duplica]**.

   ![Utilizzare il menu Altro per duplicare il modello attivo](./assets/configuration-engagement-scoring-model-more-duplicate.png){width="325"}

1. Nella finestra di dialogo _Duplica_, immetti un nome univoco per il modello duplicato e fai clic su **[!UICONTROL Duplica]**.

   ![Conferma la duplicazione del modello di punteggio](./assets/configuration-engagement-scoring-model-duplicate-dialog.png){width="500"}

   Il modello duplicato viene visualizzato nell&#39;elenco con lo stato _Bozza_. Fai clic sul nome per aprire i dettagli del modello di punteggio e apportare le modifiche.

### Modificare le impostazioni di ponderazione del coinvolgimento

Le impostazioni di spessore definiscono le bande che è possibile assegnare a ogni attività nel modello. Puoi modificare le fasce in modo che riflettano le strategie della tua organizzazione per valutare il coinvolgimento. Ad esempio, è possibile regolare la fascia di ponderazione _Normal_ a un valore di 65 se si desidera assegnare un valore più alto alle attività normali. In alternativa, è possibile aggiungere una fascia di ponderazione progettata per acquisire le attività comprese tra _Normal_ e _Importante_. In questo caso, puoi aggiungere una banda e etichettarla come _Significativa_ e assegnare un valore di fascia di peso pari a 75.

1. Nella pagina dei dettagli del modello di punteggio, fai clic su **[!UICONTROL Impostazioni peso coinvolgimento]** in alto.

   ![Accedere alle impostazioni relative al peso del coinvolgimento](./assets/configuration-engagement-scoring-model-weight-settings-button.png){width="600" zoomable="yes"}

1. Per ogni fascia di peso, regolare il nome o i valori in base alle proprie esigenze:

   * Modificare il nome nel campo _[!UICONTROL Fascia di ponderazione]_.
   * Immetti un nuovo valore. Puoi anche fare clic su **&plus;** o **−** per aumentare o diminuire il valore.

   ![Impostazioni peso coinvolgimento](./assets/configuration-engagement-scoring-model-weight-settings.png){width="500"}

1. Se necessario, aggiungere un&#39;altra fascia di ponderazione:

   Fare clic su **[!UICONTROL + Aggiungi banda di ponderazione]** in fondo all&#39;elenco. Questa azione consente di inserire una banda di ponderazione vuota nella parte inferiore dell&#39;elenco.

   Immettere il nome e impostare il valore per la banda. Utilizza un nome e un valore univoci.

1. Per rimuovere una fascia di ponderazione, fare clic sull&#39;icona _Elimina_ ( ![Icona Elimina](../assets/do-not-localize/icon-delete-outline.svg) ) per la riga della banda di ponderazione.

1. Al termine delle modifiche, fare clic su **[!UICONTROL Salva]**.

### Modificare la ponderazione delle attività

Ogni modello di punteggio include l’elenco completo delle attività di punteggio di coinvolgimento supportate.

+++Attività per architettura semplificata

Il modello predefinito per l’architettura semplificata include le attività tracciate di Experience Platform. Ogni attività ha un peso pari a zero (0) (non utilizzato) fino a quando non viene assegnato un peso. Tutte le attività hanno anche una frequenza massima giornaliera di 20, che non puoi modificare.

<table style="table-layout: fixed; width: 100%; border: 0;">
<tbody>
<tr style="border: 0;">
<td>
<ul><li>Clic su Advertising </li><li>Completamenti Advertising </li><li>Conversioni Advertising </li><li>Advertising federato </li><li>Primi quartili Advertising </li><li>Impression di Advertising </li><li>Midpoint Advertising </li><li>Avvio di Advertising </li><li>Terzi quartili Advertising </li><li>Tempo di riproduzione di Advertising </li><li>Chiusura applicazione </li><li>Avvio applicazione </li><li>Modifica cadenza campagna di coinvolgimento </li><li>Commerce Backoffice CreditMemo emessa </li><li>Ordine backoffice Commerce annullato </li><li>Ordine backoffice Commerce effettuato </li><li>Commerce Backoffice - Articoli ordine spediti </li><li>Spedizione backoffice Commerce completata </li><li>Pagamenti Commerce </li><li>Aggiunte a elenco prodotti Commerce (carrello) </li><li>Aperture dell’elenco dei prodotti Commerce (carrello) </li><li>Rimozioni da elenco prodotti Commerce (carrello) </li><li>Riapre l’elenco dei prodotti Commerce (carrello) </li><li>Visualizzazioni elenco prodotti Commerce (carrello) </li><li>Visualizzazioni prodotto Commerce </li><li>Acquisti Commerce </li><li>Salva per dopo Commerce </li><li>Ignora proposta di decisione </li><li>Visualizzazione delle proposte di decisione </li><li>Interazione della proposta di decisione </li></ul>
</td>
<td>
<ul><li>Invio di proposte di decisione </li><li>Trigger della proposta di decisione </li><li>Feedback sulla consegna </li><li>E-mail per marketing diretto non recapitata </li><li>E-mail di marketing diretto non recapitata morbida </li><li>E-mail per marketing diretto selezionata </li><li>E-mail per marketing diretto consegnata </li><li>E-mail per marketing diretto aperto </li><li>E-mail per marketing diretto inviata </li><li>E-mail per marketing diretto annullata </li><li>Messaggio in-app ignorato </li><li>È stato visualizzato il messaggio in-app </li><li>Il messaggio in-app è stato interagito con </li><li>Aggiunta operazione lead a campagna </li><li>Webhook chiamata operazione lead </li><li>Flusso campagna modifica operazione lead </li><li>Lead operazione Converti lead </li><li>Momento di interesse operazione lead </li><li>Lead operazione Unione Lead Lead </li><li>Lead operazione Nuovo lead </li><li>Fase ricavi operazione lead modificata </li><li>Punteggio operazione lead modificato </li><li>Stato operazione lead modificato nella progressione della campagna </li></ul>
</td>
<td>
<ul><li>Aggiunta operazione lead all'elenco </li><li>Operazione lead Rimuovi dall'elenco </li><li>Uscita posizione </li><li>Media adBreakComplete </li><li>Media adBreakStart </li><li>Media adComplete </li><li>Media adSkip </li><li>Media adStart </li><li>BitrateChange multimediale </li><li>BufferStart multimediale </li><li>ChapterComplete di contenuti multimediali </li><li>Capitolo multimedialeIgnora </li><li>ChapterStart per contenuti multimediali </li><li>Tracciamento personalizzato dei contenuti multimediali </li><li>Contenuto scaricato da contenuti multimediali </li><li>Errore supporto </li><li>Media pauseStart </li><li>Ping contenuti multimediali </li><li>Riproduzione file multimediali </li><li>Sessione multimediale completata </li><li>Media sessionEnd </li><li>Avvio sessione multimediale </li><li>Stati multimedialiAggiorna </li><li>Feedback messaggio </li><li>Dati rendering messaggi </li><li>Tracciamento messaggi </li><li>Aggiunta evento opportunità all’opportunità </li><li>Opportunità evento opportunità aggiornata </li><li>Evento opportunità Rimuovi dall’opportunità </li><li>Applicazione di tracciamento push aperta </li><li>Azione personalizzata tracciamento push </li><li>Modulo Web compilato </li><li>Clic sui collegamenti WebInteraction </li><li>Web Webpagedettagli Visualizzazioni pagina</li></ul>
</td>
</tbody>
</table>

+++

+++Attività per architettura standard

Il modello predefinito per l&#39;architettura standard include le attività tracciate [!DNL Marketo Engage] a cui è associato un peso predefinito. Quando si duplica questo modello, è possibile modificare la ponderazione in base alle proprie esigenze. Non è possibile modificare la frequenza massima giornaliera.

{{engagement-activities-me}}

+++

Per ogni attività nell’elenco, imposta il valore da assegnare a ogni occorrenza di attività. Fare clic sulla freccia rivolta verso il basso nel campo **[!UICONTROL Ponderazione]** e scegliere la fascia di ponderazione definita nelle impostazioni di ponderazione del coinvolgimento.

![Imposta ponderazione attività](./assets/configuration-engagement-scoring-model-set-activity-weighting.png){width="600" zoomable="yes"}

Se non desideri che il calcolo del punteggio di coinvolgimento utilizzi un’attività, imposta la ponderazione su un valore zero (0).

Le modifiche vengono salvate automaticamente.

## Attiva un modello di punteggio

Quando attivate un modello di punteggio bozza, questo sostituisce il modello attualmente attivo. Il modello attualmente attivo viene archiviato automaticamente.

1. Apri una bozza di modello di punteggio per visualizzare la pagina dei dettagli.

1. Fare clic su **[!UICONTROL Attiva]**.

1. Nella finestra di dialogo di conferma, fai clic su **[!UICONTROL Attiva]**.

   ![Attiva la finestra di conferma della ponderazione del punteggio di coinvolgimento](./assets/configuration-engagement-scoring-activate-dialog.png){width="400"}
