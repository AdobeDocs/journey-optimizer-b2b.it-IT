---
title: Pagine di destinazione
description: 'Creazione, progettazione e pubblicazione di pagine di destinazione per percorsi di account: creazione da zero, importazione di HTML, aggiunta di moduli, personalizzazione del contenuto e collegamento dalle e-mail in Journey Optimizer B2B edition.'
feature: Landing Pages, Content
role: User
exl-id: 1a3b4519-e1c0-418a-979a-7ba3e5972edd
autotag-review: '2026-05-27T16:16:24.088Z'
TQID: 'https://experienceleague.adobe.com/zAr9SwPBHxU50gD1ZRdJQo3M-qL-BEO6R1UYq7hSG-8'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: e666e996-b2cf-4c45-8fc2-1c625212abab
subfeature_v2:
  - id: a96755d6-1f54-4f3f-a971-d31f83705ab7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: e9001ce2-5245-4a8e-8601-dd958009072f
source-git-commit: 508524bce6cdf1e5c4ad8c8916332666252472d1
workflow-type: tm+mt
source-wordcount: 1637
ht-degree: 2%

---

# Pagine di destinazione

Una pagina di destinazione è una pagina web indipendente in cui puoi indirizzare contatti e clienti dopo che hanno fatto clic su un elemento collegato in un’e-mail, un messaggio SMS o qualsiasi posizione digitale. Puoi incorporare queste pagine nei tuoi percorsi di account per consentire ai potenziali clienti e ai clienti di visualizzare i messaggi sul web e i progressi nei tuoi percorsi di account. Puoi creare, personalizzare e visualizzare in anteprima le pagine di destinazione nell’area di progettazione visiva della pagina di destinazione.

Casi d’uso comuni per le pagine di destinazione:

* Fornisci il consenso o la rinuncia alle comunicazioni di marketing o a un servizio specifico. Utilizza un collegamento a un elenco di destinazione in un’e-mail o in un’altra comunicazione.
* Raccogli il consenso prima di inviare le comunicazioni e invia un’e-mail di conferma in caso di consenso o rinuncia.
* Acquisisci o aggiorna i dati del profilo (profilatura progressiva, preferenze, registrazioni e scenari simili) utilizzando i moduli nelle pagine di destinazione.
* Indirizza le persone a informazioni specifiche per la campagna progettate per l’orchestrazione del percorso.
* Reindirizza le persone a un modulo web dedicato senza creare una pagina esterna al di fuori di Journey Optimizer B2B edition.

## Flusso di lavoro per pagina di destinazione

Per indirizzare i membri di un pubblico di percorso a una pagina web definita quando fanno clic su un collegamento specifico, crea una pagina di destinazione in Journey Optimizer B2B edition:

1. [Crea la pagina](./landing-pages-create-publish.md) - Seleziona un predefinito, imposta la pagina principale e aggiungi eventuali pagine secondarie richieste.
1. [Progettare il contenuto della pagina di destinazione](./landing-page-design.md) - Creare il contenuto della pagina utilizzando i componenti di progettazione visiva trascinati.
1. [Verifica e pubblica la pagina di destinazione](./landing-pages-create-publish.md) - Visualizza l&#39;anteprima della pagina, verifica il comportamento del modulo, quindi pubblica per renderla live.
1. [Collega alla pagina dal tuo percorso](#link-to-a-landing-page). Aggiungi l&#39;URL della pagina di destinazione a un&#39;azione e-mail, SMS o percorso in modo che i destinatari possano raggiungerla.

Ad esempio, puoi creare e progettare pagine di destinazione per indirizzare gli utenti a informazioni online. La pagina potrebbe includere un modulo in cui gli utenti possono dare il consenso o rinunciare alla ricezione delle comunicazioni. Oppure potrebbe essere l&#39;opportunità di abbonarsi a comunicazioni ricorrenti, come una newsletter.

Nello spazio di progettazione visiva puoi creare, personalizzare e visualizzare in anteprima le pagine di destinazione.

## Accedere e gestire le pagine di destinazione

Per accedere alle pagine di destinazione in Journey Optimizer B2B edition, vai alla navigazione a sinistra e fai clic su **[!UICONTROL Gestione contenuto]** > **[!UICONTROL Pagine di destinazione]**. Questa azione visualizza un elenco di tutte le pagine di destinazione create nell’istanza.

![Accedi alla libreria delle pagine di destinazione](./assets/landing-pages-list.png){width="800" zoomable="yes"}

L&#39;elenco è ordinato in base alla colonna _[!UICONTROL Modificato]_, con gli elementi aggiornati più di recente nella parte superiore. Fai clic sul titolo della colonna per passare da crescente a decrescente.

### Filtrare l’elenco delle pagine di destinazione

Per cercare una pagina di destinazione per nome, immetti una stringa di testo nella barra di ricerca per trovare una corrispondenza. Fai clic sull&#39;icona _Filtro_ ( ![Mostra o nascondi icona filtri](../assets/do-not-localize/icon-filter.svg) ) per visualizzare le opzioni di filtro disponibili e modificare le impostazioni per filtrare gli elementi visualizzati in base ai criteri specificati.

![Filtra le pagine di destinazione visualizzate](./assets/landing-pages-list-filtered.png){width="700" zoomable="yes"}

<!-- 
This is going away? ### Customize the column display

Customize the columns that you want to display in the table by clicking the _Customize table_ icon ( ![Customize table icon](../assets/do-not-localize/icon-column-settings.svg) ) at the top right. 

In the dialog, select the columns to display and click **[!UICONTROL Apply]**.

![Select the columns that you want to display](./assets/landing-pages-customize-table-dialog.png){width="300"} 
-->

### Stato e ciclo di vita della pagina di destinazione

Lo stato della pagina di destinazione determina la disponibilità del collegamento nei contenuti e-mail e SMS e le modifiche che puoi apportare.

| Stato | Descrizione |
| -------------------- | ----------- |
| Bozza | Quando crei una pagina di destinazione, questa si trova nello stato Bozza. Rimane in questo stato mentre definisci o modifichi il contenuto visivo e fino a quando non lo pubblichi come pagina in hosting. Azioni disponibili:<br/><ul><li>Modifica nome o descrizione<li>Modifica URL collegamento<li>Modifica nello spazio di progettazione visiva<li>Pubblica<li>Duplica<li>Elimina |
| Pubblicato | Quando pubblichi una pagina di destinazione, questa viene ospitata nell’istanza B2B edition di Journey Optimizer e diventa disponibile per il collegamento in un contenuto di e-mail o SMS. Azioni disponibili:<br/><ul><li>Modifica nome o descrizione<li>Modifica URL collegamento<li>Aggiungere un collegamento nel contenuto di un messaggio e-mail o SMS<li>Crea versione bozza<li>Duplica<li>Elimina |
| Pubblicato con bozza | Quando crei una bozza da una pagina di destinazione pubblicata, la versione pubblicata rimane e il contenuto della bozza può essere modificato nello spazio di progettazione visiva. Se pubblichi la bozza della versione, questa sostituisce la versione pubblicata corrente e il contenuto viene aggiornato nella pagina ospitata. Azioni disponibili:<br/><ul><li>Modifica nome o descrizione<li>Modifica URL collegamento<li>Aggiungere un collegamento nel contenuto di un messaggio e-mail o SMS<li>Modifica versione bozza in Visual Design Space<li>Pubblica versione bozza<li>Duplica<li>Elimina (elimina entrambe le versioni)<li>Elimina bozza (torna allo stato pubblicato) |

![Ciclo di vita stato pagina di destinazione](./assets/status-lifecycle-diagram.png){zoomable="yes"}

## Modificare una pagina di destinazione

Le modifiche apportate a una pagina di destinazione dipendono dal suo stato corrente:

* Quando una pagina di destinazione è in stato **_Bozza_**, puoi modificarne i dettagli, l&#39;URL e il contenuto visivo.
* Quando una pagina di destinazione si trova nello stato **_Pubblicato_**, puoi modificare la descrizione, ma non il nome. Per modificare il contenuto visivo, è necessario creare una versione bozza della pagina.
* Quando una pagina di destinazione è in stato **_Pubblicato con bozza_**, la modifica dei dettagli è limitata alla descrizione. Puoi anche modificare il contenuto visivo della versione bozza.

>[!BEGINTABS]

>[!TAB Bozza]

1. Dalla pagina di elenco _[!UICONTROL Pagine di destinazione]_, fai clic sul nome della pagina di destinazione per aprirla.

   Viene visualizzata un’anteprima del contenuto visivo, con i dettagli della pagina di destinazione a destra.

1. Modifica uno dei dettagli, ad esempio nome e descrizione.

   ![Dettagli per la pagina di destinazione con stato Bozza](./assets/landing-page-draft-details.png){width="700" zoomable="yes"}

1. Per apportare modifiche al contenuto nello spazio di progettazione visivo, fare clic su **[!UICONTROL Modifica pagina di destinazione]**.

   Utilizza gli strumenti di progettazione visiva secondo necessità:

   * [Aggiungere struttura e contenuto](./landing-page-design.md#structure-content-landing-page)
   * [Aggiungi Assets](./landing-page-design.md#add-assets)
   * [Spostarsi tra livelli, impostazioni e stili](./landing-page-design.md#navigate-the-layers-settings-and-styles)
   * [Personalizzazione dei contenuti](./landing-page-design.md#personalize-content)
   * [Modifica tracciamento URL collegato](./landing-page-design.md#edit-linked-url-tracking)

1. Fai clic su **[!UICONTROL Salva]** o **[!UICONTROL Salva e chiudi]** per tornare ai dettagli della pagina di destinazione.

1. Quando la pagina soddisfa i criteri e desideri renderla disponibile per la visualizzazione, fai clic su **[!UICONTROL Pubblica]**.

>[!TAB Pubblicato]

1. Dalla pagina di elenco _[!UICONTROL Pagine di destinazione]_, fare clic sul nome della pagina per aprirla.

   Viene visualizzata un’anteprima del contenuto visivo, con i dettagli della pagina di destinazione a destra.

1. Se necessario, modifica la descrizione.

   Per una pagina di destinazione pubblicata, tutti gli altri dettagli non possono essere modificati.

1. Se desideri aggiornare il contenuto, fai clic su **[!UICONTROL Modifica pagina di destinazione]** a destra.

   Fare clic su **[!UICONTROL Crea bozza versione]** nella finestra di dialogo per aprire la bozza versione nello spazio di progettazione visivo.

   ![Finestra di dialogo Crea bozza versione](./assets/landing-page-create-draft-version.png){width="300"}

   Utilizza gli strumenti di progettazione visiva secondo necessità:

   * [Aggiungere struttura e contenuto](./landing-page-design.md#structure-content-landing-page)
   * [Aggiungi Assets](./landing-page-design.md#add-assets)
   * [Spostarsi tra livelli, impostazioni e stili](./landing-page-design.md#navigate-the-layers-settings-and-styles)
   * [Personalizzazione dei contenuti](./landing-page-design.md#personalize-content)
   * [Modifica tracciamento URL collegato](./landing-page-design.md#edit-linked-url-tracking)

1. Fai clic su **[!UICONTROL Salva]** o **[!UICONTROL Salva e chiudi]** per tornare ai dettagli della pagina di destinazione.

1. Quando la bozza della pagina di destinazione soddisfa i criteri e desideri rendere le modifiche disponibili nella pagina pubblicata, fai clic su **[!UICONTROL Pubblica]**.

   Quando pubblichi la versione bozza, questa sostituisce la versione pubblicata corrente e il contenuto viene aggiornato per l’URL della pagina.

>[!TAB Pubblicato con bozza]

Quando apri la pagina di destinazione, viene visualizzata la versione bozza. Le schede nella parte superiore dello spazio di anteprima consentono di alternare la visualizzazione tra la versione pubblicata e quella bozza. Le bozze delle azioni e dei dettagli sono visualizzate a destra.

![Anteprima e dettagli della versione bozza della pagina di destinazione](./assets/landing-page-published-draft-details.png){width="700" zoomable="yes"}

Per aggiornare il contenuto:

1. Fai clic su **[!UICONTROL Modifica pagina di destinazione]** in alto a destra. Utilizza gli strumenti di progettazione visiva secondo necessità:

   * [Aggiungere struttura e contenuto](./landing-page-design.md#structure-content-landing-page)
   * [Aggiungi Assets](./landing-page-design.md#add-assets)
   * [Spostarsi tra livelli, impostazioni e stili](./landing-page-design.md#navigate-the-layers-settings-and-styles)
   * [Personalizzazione dei contenuti](./landing-page-design.md#personalize-content)
   * [Modifica tracciamento URL collegato](./landing-page-design.md#edit-linked-url-tracking)

1. Fai clic su **[!UICONTROL Salva]** o **[!UICONTROL Salva e chiudi]** per tornare ai dettagli della pagina di destinazione.

1. Quando la pagina della bozza soddisfa i criteri e desideri rendere disponibili le modifiche, fai clic su **[!UICONTROL Pubblica]**.

   Quando pubblichi la versione bozza, questa sostituisce la versione pubblicata corrente e il contenuto viene aggiornato nella pagina ospitata.

>[!ENDTABS]

## Duplicare una pagina di destinazione

Puoi duplicare una pagina di destinazione utilizzando uno dei seguenti metodi:

* Dalla pagina dell&#39;elenco _[!UICONTROL Pagina di destinazione]_, fare clic sull&#39;icona _Altro_ (**...**) accanto al nome della pagina di destinazione e scegli **[!UICONTROL Duplica]**.
* Nella parte superiore destra della pagina dei dettagli della pagina di destinazione, fare clic su **[!UICONTROL ... Altro]** e scegli **[!UICONTROL Duplicato]**.

![Duplica la pagina di destinazione](./assets/landing-page-details-duplicate-delete.png){width="600" zoomable="yes"}

Nella finestra di dialogo, inserisci un nome utile (univoco) e una descrizione (facoltativa). Fai clic su **[!UICONTROL Duplica]** per completare l&#39;azione.

![Immettere un nome e una descrizione per la pagina di destinazione duplicata](./assets/landing-page-duplicate-dialog.png){width="350"}

La pagina duplicata (nuova) viene quindi visualizzata nell&#39;elenco _Pagine di destinazione_.

## Eliminare una pagina di destinazione

Puoi eliminare una pagina di destinazione utilizzando uno dei seguenti metodi:

* Dalla pagina dell&#39;elenco _[!UICONTROL Pagina di destinazione]_, fare clic sull&#39;icona _Altro_ (**...**) accanto al nome della pagina di destinazione e scegliere **[!UICONTROL Elimina]**.
* Nella parte superiore destra della pagina dei dettagli della pagina di destinazione, fare clic su **[!UICONTROL ... Altro]** e scegliere **[!UICONTROL Elimina]**.

Questa azione apre una finestra di dialogo di conferma. È possibile interrompere il processo facendo clic su **[!UICONTROL Annulla]** oppure su **[!UICONTROL Elimina]** per confermare l&#39;eliminazione.

![Finestra di dialogo Elimina pagina di destinazione](./assets/landing-page-delete-dialog.png){width="400"}

## Collegamento a una pagina di destinazione

In qualità di addetto al marketing o Designer che crea contenuti per e-mail, frammenti e pagine, puoi incorporare collegamenti alle pagine di destinazione pubblicate (live) create nell’istanza di Journey Optimizer B2B edition.

1. Quando lavori nello spazio di progettazione visiva per un frammento, un’e-mail, una pagina di destinazione o un modello, seleziona una parte di testo, un componente pulsante o un componente immagine per il collegamento.

   Le opzioni **[!UICONTROL Collegamento]** sono visualizzate nel pannello di destra.

1. Per l&#39;opzione **[!UICONTROL Tipo]**, scegliere **[!UICONTROL Pagina di destinazione]**.

   ![Opzioni di collegamento per una pagina di destinazione](/help/assets/content-design-shared/content-design-link-settings.png){width="700" zoomable="yes"}

1. Per l&#39;opzione **[!UICONTROL Pagina di destinazione]**, fare clic sull&#39;icona _Seleziona pagina_ ( ![Mostra icona collegamenti](/help/assets/do-not-localize/icon-landing-page-select.svg) ).

1. Nella finestra di dialogo Seleziona pagina di destinazione, imposta **[!UICONTROL Origine pagina di destinazione]** come **[!UICONTROL Journey Optimizer B2B edition]**, seleziona la casella di controllo per la pagina di destinazione dall&#39;elenco delle pagine pubblicate e fai clic su **[!UICONTROL Seleziona]**.

   ![Opzioni di collegamento per una pagina di destinazione](/help/assets/content-design-shared/content-design-link-landing-page-select.png){width="600" zoomable="yes"}

1. Per l&#39;opzione **[!UICONTROL Target]**, scegliere il comportamento della destinazione di collegamento:

   * **[!UICONTROL Nessuno]** - Apre il collegamento utilizzando il comportamento predefinito del browser.
   * **[!UICONTROL Vuoto]** - Apre il collegamento in una nuova finestra o scheda.
   * **[!UICONTROL Autonomo]** - Apre il collegamento nello stesso frame.
   * **[!UICONTROL Elemento padre]** - Apre il collegamento nel frame padre.
   * **[!UICONTROL Top]** - Apre il collegamento nel corpo completo della finestra.

1. (Solo collegamento di testo) Per sottolineare il testo collegato, selezionare la casella di controllo **[!UICONTROL Sottolinea collegamento]**.

   Puoi impostare stili aggiuntivi per il testo del collegamento, incluso il colore del collegamento, selezionando la scheda **[!UICONTROL Stili]** nel pannello di destra.
