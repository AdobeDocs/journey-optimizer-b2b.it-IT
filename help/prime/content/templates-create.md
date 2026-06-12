---
title: Creare modelli e-mail
description: 'Scopri come creare modelli e-mail in Journey Optimizer B2B Prime: progettare da zero, salvare un’e-mail da un percorso come modello o convertire un’immagine di progettazione in un modello e-mail.'
badgeBeta: label="Beta" type="informative" tooltip="Questa funzione fa parte di una versione beta limitata."
source-git-commit: 2f19137465c71f2292d37bea5786533b1df6e286
workflow-type: tm+mt
source-wordcount: '760'
ht-degree: 0%

---


# Creare modelli e-mail

È possibile creare un modello di posta elettronica in [!DNL Journey Optimizer B2B Edition Prime] in tre modi:

* **Progetta da zero**: crea un nuovo modello nella libreria di modelli utilizzando lo spazio di progettazione e-mail visiva.
* **Salva da e-mail di percorso** — Salva un messaggio e-mail creato in un percorso come modello riutilizzabile.
* **Converti un&#39;immagine** - Carica un&#39;immagine di progettazione e utilizza l&#39;intelligenza artificiale generativa per convertirla in un modello di e-mail modificabile.

>[!NOTE]
>
>In questa versione di Beta, sono supportati solo i modelli e-mail.

## Progettare un modello da zero {#design-from-scratch}

1. Passa a **[!UICONTROL Gestione contenuto]** > **[!UICONTROL Modelli]**.
1. Fare clic su **[!UICONTROL Crea modello]**.
1. Immettere un **[!UICONTROL nome modello]** e una **[!UICONTROL descrizione]** facoltativa.
1. Facoltativamente, aggiungi dei tag per categorizzare il modello.
1. Fai clic su **[!UICONTROL Crea]** per aprire lo spazio di progettazione delle e-mail.
1. Progetta il layout dell’e-mail utilizzando strutture e componenti di contenuto. Per un riferimento completo sugli strumenti disponibili, vedi [Creazione di e-mail](email-authoring.md).
1. È possibile configurare [il blocco del contenuto](template-content-locking.md) per limitare le parti che gli autori del modello possono modificare quando lo utilizzano in un percorso.
1. Fai clic su **[!UICONTROL Salva]**.

## Salvare un’e-mail di percorso come modello {#save-as-template}

Quando progetti un messaggio e-mail in un percorso che desideri riutilizzare, salvalo direttamente nella libreria di modelli dall’interno dello spazio di progettazione dell’e-mail.

1. Nell&#39;area di progettazione delle e-mail, apri il menu a discesa **[!UICONTROL Salva]** nella parte superiore dell&#39;editor.
1. Selezionare **[!UICONTROL Salva come modello di contenuto]**.
1. Immettere un **[!UICONTROL nome modello]** e una **[!UICONTROL descrizione]** facoltativa.
1. È possibile aggiungere tag e configurare [il blocco del contenuto](template-content-locking.md).
1. Fai clic su **[!UICONTROL Salva]**.

L’e-mail originale del percorso non subisce modifiche. Il modello salvato è disponibile nella libreria di modelli per tutti gli utenti nella sandbox.

## Convertire un’immagine in un modello {#image-to-template}

[!DNL Journey Optimizer B2B Edition Prime] può convertire un&#39;immagine statica, ad esempio un modello di Figma o Photoshop, in un modello di e-mail modificabile utilizzando l&#39;intelligenza artificiale generativa. Questo elimina la necessità di rigenerare manualmente i layout dai file di progettazione.

### Requisiti

Prima di iniziare:

* La tua organizzazione deve aver firmato l’addendum all’intelligenza artificiale generativa con Adobe.
* È necessario disporre dell&#39;autorizzazione **[!UICONTROL Genera contenuto]** oltre a **[!UICONTROL Gestisci modelli di contenuto]**.
* Il file di immagine deve soddisfare le seguenti specifiche:
   * Formato: JPEG (.jpg, .jpeg) o PNG (.png)
   * Dimensione massima file: 10 MB
   * Larghezza consigliata: 600-800 pixel
   * Immagine chiara e di alta qualità con testo leggibile ed elementi visivi distinti

>[!IMPORTANT]
>
>L’immagine non deve contenere dati personali (PII, personally identifiable information) né dati sensibili.

### Conversione di un’immagine

1. Passa a **[!UICONTROL Gestione contenuto]** > **[!UICONTROL Modelli]**.
1. Fare clic su **[!UICONTROL Converti immagine in modello]** nell&#39;intestazione.
1. Immettere un **[!UICONTROL nome modello]** e una **[!UICONTROL descrizione]** facoltativa.
1. Se necessario, seleziona un **[!UICONTROL tema marchio]** per applicare i colori, i font e la spaziatura del tuo marchio all&#39;output generato.
1. Carica l’immagine trascinandola e rilasciandola o nel browser dei file.
1. Verifica che l’immagine non contenga dati personali.
1. Rivedi e accetta le linee guida per gli utenti di Adobe Generative AI (solo per la prima volta).
1. Fare clic su **[!UICONTROL Converti]**.

   Generalmente la conversione viene completata entro cinque minuti. Immagini complesse o di grandi dimensioni possono richiedere fino a dieci minuti. Potete spostarvi, il processo continua in background.

1. Al termine della conversione, fai clic sul nome del modello per visualizzare in anteprima e modificare il contenuto generato.

>[!NOTE]
>
>Il risultato non viene visualizzato automaticamente. Aggiorna la pagina o torna alla libreria dei modelli per visualizzare il modello completato.

### Modifica dopo la conversione

Il modello convertito si apre nello spazio di progettazione delle e-mail come e-mail completamente modificabile. Utilizzare gli strumenti di progettazione standard per:

* Modifica il testo e aggiungi [token di personalizzazione](email-authoring.md#personalization).
* Aggiornare o sostituire immagini e aggiungere collegamenti.
* Regola colori, tipi di carattere e spaziatura.
* Aggiungere, rimuovere o ridisporre i componenti di contenuto.
* Configura [blocco contenuto](template-content-locking.md).

>[!IMPORTANT]
>
>L’intelligenza artificiale generativa produce un HTML statico basato sull’immagine visiva. Controlla tutto il testo per verificarne la precisione e aggiungi manualmente personalizzazione, contenuto dinamico e tracciamento dopo la conversione.

Al termine della conversione, il modello convertito viene salvato automaticamente nella libreria di modelli.

### Suggerimenti per ottenere risultati ottimali

Utilizza le seguenti linee guida per ottenere risultati migliori dalla conversione da immagine a modello:

**Prima della conversione:**

* Utilizza la versione con la massima risoluzione del file di progettazione.
* Progetta con larghezze e-mail standard (600-800 pixel) e includi il layout completo, dall’intestazione al piè di pagina, in una singola immagine.
* Assicuratevi di ottenere un contrasto sufficiente tra testo e sfondi e di utilizzare dimensioni dei caratteri leggibili.

**Progettazione per una conversione accurata:**

* Utilizzare layout semplici e ben strutturati con una netta separazione tra le sezioni.
* Segui i pattern e-mail standard: intestazione, corpo, inviti all’azione, piè di pagina, anziché progetti complessi a più livelli.
* Mantieni distinti gli elementi visivi in modo che l’intelligenza artificiale possa identificare correttamente i limiti strutturali.

**Dopo la conversione:**

* Prima di utilizzare il modello in un percorso, verifica il rendering tra client e dispositivi e-mail.
* Verifica l’allineamento con i colori del marchio, i font e le linee guida di stile.
* Rivedi e migliora l’accessibilità, incluso il testo alternativo dell’immagine.
