---
title: Qualificatore di vendita
description: Automatizzare la qualifica di potenziale cliente B2B e l'impegno con i qualificatori di vendita. Fornisce ricerche basate sull’intelligenza artificiale, bozza di e-mail, integrazione CRM e flussi di lavoro in uscita di IA per i BDR.
feature: Agentic AI, Sales Insights, Account Journeys
role: User
exl-id: cc590444-41df-44fe-830b-92241718ee81
autotag-review: '2026-06-05T16:42:16.451Z'
TQID: 'https://experienceleague.adobe.com/VNgs0cTpjCTG7JpFjFErnVMmRtR-gmw-iRRHZanZDUs'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: c8f3fb27-3167-48ac-a66a-fa4bc3f58dda
  - id: fc1ff3b2-6614-41ad-a113-de48597598fd
  - id: f979fe0e-02fe-4599-b492-7b3df1d4e7dc
subfeature_v2:
  - id: fe583b80-65a2-48c2-b4e1-9ea8fbac0a8a
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
  - id: fd2e3797-f2ea-4b36-a9af-52acf5e90513
source-git-commit: a5145b53d6b5c9462392f7c540a81b7d85abdd7b
workflow-type: tm+mt
source-wordcount: 6084
ht-degree: 1%

---

# Qualificatore di vendita

Sales Qualifier è un&#39;applicazione basata sull&#39;intelligenza artificiale che puoi utilizzare con Adobe Journey Optimizer B2B edition. Implementa Account Qualification Agent ed è progettato per semplificare i flussi di lavoro per i rappresentanti di sviluppo aziendale (BDR, Business Development Representative). Qualificatore di vendita automatizza i flussi di lavoro di qualificazione dei potenziali clienti, coinvolgimento degli acquirenti e coinvolgimento degli acquirenti su tutti i canali. Riduce il carico BDR manuale e accelera la velocità della pipeline per le aziende B2B aziendali.

I BDR possono utilizzare il browser e i plug-in e-mail per accedere alle informazioni aziendali direttamente in CRM o Outlook. Il video seguente offre una breve dimostrazione dei Sales Qualifier e di Account Qualification Agent.

>[!VIDEO](https://video.tv.adobe.com/v/3476569?captions=ita)

## Home dell’applicazione

Qualificatore di vendita è incluso in [!UICONTROL Journey Optimizer B2B edition], ma è un&#39;app separata all&#39;interno di Adobe Experience Platform.

![Qualificatore vendite nella schermata iniziale](./assets/home-screen.png){width="800" zoomable="yes"}

### Agente Account Qualification

Il Account Qualification Agent (AQA) è il nucleo del qualificatore di vendita. L’AQA utilizza l’intelligenza artificiale per leggere gli account e determinare quali sono pronti per il passaggio successivo. Aiuta nella ricerca, nella redazione di e-mail e nel contesto informato sul CRM quando la tua organizzazione ha connesso il CRM.

<!--
## Edit the left navigation bar

At the bottom left of the application, click the _Edit_ ( ![Edit icon](../assets/do-not-localize/icon-edit.svg) ) icon to control which elements are visible in the left navigation. You can also drag and drop them to reorder as you want.
-->

### Utilizzo di base dell’agente

Gli agenti di Adobe AI utilizzano _query in linguaggio naturale_, il che significa che utilizzano la stessa lingua nel prompt del testo utilizzata quando si parla con una persona. Più sei dettagliato, migliori saranno i risultati.

Utilizzando il linguaggio naturale, puoi chiedere all’agente di:

* `Tell me the latest financial results of Bodea`
* `Tell me more about hiring at TechNova`
* `Tell me about the new AI features in Bodea LumaSecure4`

Itera i flussi di lavoro in uscita perfezionando le richieste per ottenere i risultati necessari. Ad esempio:

* _Crea una bozza di disegno di un&#39;e-mail di follow-up dal contesto, ad esempio chiamate o rapporti sui guadagni._ Fino a 120 parole. Oggetto: Captivazione, con un tema chiave. Introduzione: inizia con una citazione diretta da origini di contesto. Corpo: connettiti ai punti critici e alle proposte di valore. CTA: propone una breve chiamata per approfondire l’analisi._

* _L&#39;obiettivo di questa e-mail è quello di avviare una conversazione e creare credibilità._ Redigi un&#39;e-mail sotto 120 parole con un tono consultivo ed empatico. Evita un approccio troppo familiare alle vendite e non usare le frasi &quot;spera di stare bene&quot;, &quot;solo per il check-in&quot; o &quot;per favore&quot;._

### Accesso ai prodotti e gruppi di utenti

L&#39;accesso alle funzioni Qualificatore di vendita viene gestito tramite due gruppi di utenti in Adobe Admin Console. Prima che gli utenti possano accedere all’applicazione, gli amministratori di prodotto devono configurare i gruppi durante l’onboarding.

#### Utenti qualificatore vendite

Gli utenti devono essere membri del gruppo di utenti `Sales Qualifier` per accedere all&#39;applicazione Sales Qualifier.

1. In Adobe Admin Console, creare un gruppo di utenti denominato `Sales Qualifier`.
1. Assegna al gruppo il profilo AEP **Default Production All Access**.
1. Aggiungere gli utenti che devono accedere al qualificatore vendite.

#### Amministratori qualificatori vendite

Gli amministratori che configurano [connessioni CRM](#integrations-and-crm), [Centro informazioni](#knowledge-center) e le impostazioni di rinuncia e-mail globali devono essere membri del gruppo di utenti `Sales Qualifier Admins`.

1. In Adobe Admin Console, creare un gruppo di utenti denominato `Sales Qualifier Admins`.
1. Aggiungere gli amministratori ai gruppi `Sales Qualifier` e `Sales Qualifier Admins`.

L&#39;appartenenza a entrambi i gruppi rende **[!UICONTROL Impostazioni amministratore]** visibili in **[!UICONTROL Amministrazione]** nella barra di navigazione a sinistra. Gli utenti standard possono utilizzare i campi, i filtri e la playbook configurati e il piè di pagina di rinuncia configurato viene applicato alle e-mail in uscita. Non possono modificare queste impostazioni.

>[!NOTE]
>
>I nomi dei gruppi di utenti devono corrispondere esattamente come mostrato nei passaggi precedenti.

## Potenziali clienti

Seleziona **[!UICONTROL Prospect]** nella barra di navigazione a sinistra per visualizzare un elenco dei lead a cui puoi accedere. L’elenco fornisce una rapida revisione delle informazioni, ad esempio lo stato del lead e l’ultima attività.

![Tabella dei potenziali clienti con lo stato del lead e l&#39;ultima attività per la gestione dei potenziali clienti](./assets/prospects.png){width="800" zoomable="yes"}

### Crea il tuo elenco di potenziali clienti

L’elenco dei potenziali clienti combina persone provenienti da più origini:

* **Prospettive originate da CRM** - Quando si connette un CRM, vengono automaticamente importati i lead di proprietà dell&#39;utente connesso. Consulta [Integrazioni e CRM](#integrations-and-crm).
* **Prospect importati** - Importa un elenco di lead da un file CSV.
* **Potenziali aggiunti manualmente** - Aggiungi una singola persona direttamente nell&#39;app.

Per aggiungere potenziali clienti non provenienti dal CRM:

1. Nella pagina **[!UICONTROL Prospect]**, selezionare **[!UICONTROL Aggiungi prospect]**.
1. Scegli **[!UICONTROL Importa CSV]** o **[!UICONTROL Aggiungi manualmente]**.

   * Per un’importazione CSV, carica il file e mappane le colonne su campi prospect.
   * Per aggiungere manualmente una persona, inserisci i relativi dettagli nel modulo.

1. Seleziona **[!UICONTROL Salva]**.

### Filtrare e trovare potenziali clienti

Seleziona l&#39;icona _Filtro_ ![Icona Filtro](../../assets/do-not-localize/icon_filter-outline.svg) per limitare l&#39;elenco. Puoi filtrare per:

* Stato lead
* Punteggio di coinvolgimento
* Momenti interessanti contrassegnati dal marketing
* Punteggio a stelle e punteggio di fiamma
* Offerte associate

Gli amministratori possono anche rendere disponibili come filtri i campi CRM mappati. In **[!UICONTROL Impostazioni amministratore]**, attivano **[!UICONTROL Filterable]** per i campi utilizzati dai rappresentanti per trovare potenziali clienti. Vedi [Mappa campi CRM](#map-crm-fields-inbound-mapping).

### Rivedi dettagli prospect

Seleziona un potenziale cliente per aprire il suo profilo. Rivedi i segnali importanti prima di contattare:

* **Elenco attività** - Un elenco cronologico delle attività del prospect, con un **riepilogo attività AI** nella parte superiore che evidenzia il comportamento più rilevante recente.
* **Visualizzazione sequenza temporale**: sequenza temporale visiva del coinvolgimento tra i canali.
* **Contenuto visualizzato** - Apre il contenuto effettivo visualizzato da un potenziale cliente, ad esempio una pagina Web o una risorsa, direttamente da un&#39;attività.

## Account

Seleziona **[!UICONTROL Account]** nella navigazione a sinistra per utilizzare gli account in cui effettui la vendita. Qualificatore di vendita riunisce dettagli, pipeline e coinvolgimento firmografici in modo da poter dare priorità all’impegno a livello di account.

La panoramica dell’account riassume elementi essenziali come ricavi, settore, dimensioni dell’azienda e sede centrale. Accanto a questi dettagli, ogni account affiora:

* **Opportunità aperte**: le opportunità aperte associate all&#39;account, originate dal CRM connesso, in modo da poter allineare l&#39;estensione con la pipeline attiva.
* **Membri principali coinvolti** - I contatti dell&#39;account con il coinvolgimento più recente, in modo da sapere a chi assegnare la priorità all&#39;interno del gruppo di acquisto.
* **Input CRM** - Campi account, opportunità e informazioni sul proprietario visualizzate dal CRM connesso. Per informazioni sul mapping dei dati, vedere [Integrazioni e CRM](#integrations-and-crm).

### Approfondimento account

Per iniziare un approfondimento, apri un account. Account Qualification Agent (AQA) assegna la priorità ai segnali più rilevanti per la strategia di vendita della tua organizzazione, in modo da capire rapidamente la posizione dell’account e decidere cosa fare dopo.

## Flussi di lavoro in uscita

>[!NOTE]
>
>I flussi di lavoro in uscita creati dagli amministratori di prodotto vengono condivisi con tutti gli utenti dell’organizzazione.

Un _flusso di lavoro in uscita_ è la struttura utilizzata dal qualificatore di vendita per eseguire una cadenza basata su obiettivi. Definisci un obiettivo di sensibilizzazione e criteri di targeting e l’intelligenza artificiale propone una cadenza multi-touch e scrive contenuti e-mail personalizzati per ogni potenziale cliente. Prima di attivare la registrazione, rivedi e approva ogni e-mail in modo che i messaggi vengano inviati solo durante la finestra configurata.

Un flusso di lavoro in uscita collega quattro elementi:

* **Obiettivo** - Il risultato desiderato dall&#39;estensione (ad esempio la prenotazione di una chiamata di individuazione o la registrazione di un evento guida).
* **Filtri di targeting** - Condizioni che determinano quali potenziali clienti sono idonei.
* **Cadenza dei punti di contatto** - Sequenza ordinata di passaggi, ciascuno in un giorno pianificato. I punti di contatto possono essere **e-mail**, **telefonate** o **LinkedInMails**.
* **Contenuto e-mail personalizzato** - Per ogni punto di contatto e-mail, l&#39;intelligenza artificiale crea il contenuto utilizzando il profilo del potenziale cliente, il contesto dell&#39;account, la cronologia del coinvolgimento e le notizie recenti.

L’obiettivo guida tutto a valle: l’intelligenza artificiale lo utilizza per suggerire filtri di targeting, progettare la cadenza, bozze di prompt dei punti di contatto e personalizzare la forma per ogni e-mail generata.

![Scheda Panoramica del flusso di lavoro in uscita](./assets/outbound-workflow-overview.png){width="800" zoomable="yes"}

### Concetti chiave

| Concetto | Descrizione |
| --- | --- |
| **Flusso di lavoro** | Un’attività in uscita riutilizzabile definita da un obiettivo, da filtri di targeting, cadenza e impostazioni. |
| **Obiettivo** | Cosa dovrebbe fare la sensibilizzazione. |
| **Punto di contatto** | Un passaggio nella cadenza (e-mail, chiamata telefonica o LinkedInMail), pianificato in relazione all’iscrizione. |
| **Prompt punto di contatto** | Le istruzioni che l’intelligenza artificiale segue durante la generazione del corpo e dell’oggetto dell’e-mail per un potenziale cliente: tono, lunghezza, focus e call to action. |
| **Cadenza** | La sequenza completa dei punti di contatto: quanti, in quale ordine e in quali giorni. |
| **Filtro di targeting** | Condizione che limita il flusso di lavoro a un sottoinsieme di potenziali clienti. |
| **Bozza** | Un’e-mail generata pronta per la revisione ma non ancora approvata. |
| **Motivazione** | La spiegazione dell’intelligenza artificiale di come ha scritto una determinata e-mail (quali segnali e fonti di dati ha utilizzato). |
| **Iscrizione** | Approvazione delle bozze di un potenziale cliente, che attiva la cadenza e mette in coda le e-mail da inviare durante la finestra di invio del flusso di lavoro. |

Le sezioni seguenti descrivono l’intero ciclo di vita: creazione di un flusso di lavoro nella procedura guidata, revisione delle e-mail generate, approvazione di potenziali clienti e gestione dei flussi di lavoro nel tempo.

### Creare un flusso di lavoro in uscita

La creazione del flusso di lavoro è una procedura guidata in cinque passaggi: **Obiettivo**, **Targeting**, **Generare punti di contatto**, **Impostazioni** e **Aggiungere potenziali clienti**. Ogni passaggio si basa sull’ultimo; l’obiettivo iniziale forma ogni decisione successiva.

1. Nel menu di navigazione a sinistra, seleziona **[!UICONTROL Flusso di lavoro in uscita]**.

1. Nella scheda **[!UICONTROL Sfoglia]**, fai clic su **[!UICONTROL + Crea flusso di lavoro]** nell&#39;angolo superiore destro.

#### Passaggio 1: definire l’obiettivo

L’obiettivo è l’input più importante: indica all’intelligenza artificiale come si presenta il successo e ancora il targeting, la cadenza e la generazione di e-mail.

1. Scegli **[!UICONTROL Inizia da zero]** per scrivere il tuo obiettivo oppure **[!UICONTROL Inizia da modello]** per utilizzare un modello salvato.

   ![Crea flusso di lavoro in uscita Avvia da zero](./assets/outbound-workflow-create-start-from-scratch.png){width="700" zoomable="yes"}

1. Scegli uno dei **[!UICONTROL obiettivi consigliati]** come punto di partenza oppure immetti un obiettivo personalizzato.

1. Fare clic su **[!UICONTROL Avanti: Targeting]**.

Gli obiettivi funzionano meglio quando indicano un **risultato concreto**, non solo un argomento. Per consentire all&#39;IA di lavorare di più con, utilizza un obiettivo come `Book a 15-minute discovery call with marketing leaders evaluating campaign automation` invece di `Promote campaign automation`.

#### Passaggio 2: configurare i filtri di targeting

I filtri di targeting definiscono quali potenziali clienti sono idonei. Quando si aggiungono i potenziali clienti in un secondo momento, nell&#39;elenco di selezione vengono visualizzati solo i potenziali clienti che corrispondono a questi filtri.

1. Fare clic sulla freccia rivolta verso il basso per visualizzare l&#39;elenco **[!UICONTROL Aggiungi un filtro]** e selezionare un filtro da applicare.

   ![Crea filtri di targeting flusso di lavoro in uscita](./assets/outbound-workflow-create-targeting-filter-list.png){width="700" zoomable="yes"}

1. Imposta i valori per il filtro.

1. Aggiungi altri filtri per restringere il pubblico.

   ![Crea flusso di lavoro in uscita Aggiunti filtri con valori](./assets/outbound-workflow-create-targeting-filters-values.png){width="600" zoomable="yes"}

1. Fai clic su **[!UICONTROL Avanti: genera punti di contatto]**.

#### Passaggio 3: generare e rivedere i punti di contatto

Dopo aver impostato il targeting, l&#39;IA crea la **_cadenza_**: analizza l&#39;obiettivo e il targeting, definisce la sequenza di punti di contatto e scrive un **_prompt dei punti di contatto_** per ogni passaggio. Viene visualizzata una cadenza in più passaggi con ogni punto di contatto in un giorno specifico. La cadenza può combinare i passaggi e-mail, telefonata e LinkedInMail.

![Cadenza punto di contatto generata dal flusso di lavoro in uscita e prompt](./assets/outbound-workflow-create-touchpoints.png){width="700" zoomable="yes"}

Per leggere il prompt, espandi un punto di contatto e-mail. Questa istruzione guida l&#39;intelligenza artificiale durante la scrittura dell&#39;e-mail di ogni prospect, inclusi il tono, la lunghezza, lo stato attivo e _call to action_.

**Rigenerare la cadenza**

Se la cadenza non è quella desiderata, fare clic su **[!UICONTROL Rigenera]** e immettere un&#39;istruzione di ottimizzazione. Ad esempio:

* `Make it 3 touchpoints across 2 weeks`
* `Lead with an executive briefing offer in the first email`
* `Add a nurture touch focused on a relevant case study`

L’intelligenza artificiale riscrive l’intera cadenza in base alle tue istruzioni.

Per regolare un singolo punto di contatto e-mail senza rigenerare l’intera cadenza, modifica il testo del prompt direttamente nella relativa area di testo.

**Usa un playbook nelle richieste**

Se la tua organizzazione ha creato un playbook nel [Centro conoscenze](#knowledge-center), puoi indirizzare l&#39;intelligenza artificiale per attingervi durante la scrittura delle e-mail. Nella richiesta, assegna un nome al documento e al contesto che desideri utilizzare con IA, ad esempio `Use the ABC positioning guide from the Knowledge Center and focus on the security value proposition`. Le e-mail generate riflettono quindi i messaggi presenti nel playbook.

Quando la cadenza e i prompt sono visualizzati a destra, fare clic su **[!UICONTROL Avanti: impostazioni]**.

Affinare i prompt dei punti di contatto prima che sia importante la generazione per potenziale cliente: questi prompt sono le istruzioni principali utilizzate dall’intelligenza artificiale per ogni potenziale cliente in un secondo momento. Il tempo trascorso qui viene proporzionato in tutte le e-mail generate.

#### Passaggio 4: configurare le impostazioni del flusso di lavoro

Il passaggio **Impostazioni** controlla come viene eseguito il flusso di lavoro.

![Impostazioni flusso di lavoro in uscita](./assets/outbound-workflow-create-settings.png){width="700" zoomable="yes"}

1. Rivedi il **[!UICONTROL nome flusso di lavoro]** e modificalo se vuoi un&#39;etichetta più chiara.
1. In **[!UICONTROL Numero massimo di potenziali clienti per flusso di lavoro]**, confermare il limite massimo per il numero di potenziali clienti che il flusso di lavoro può gestire contemporaneamente.
1. Imposta la **[!UICONTROL finestra di invio]** per le ore in cui le e-mail in uscita possono essere inviate.
1. Attiva **[!UICONTROL Salta fine settimana]** per spostare al giorno lavorativo successivo qualsiasi punto di contatto che cade in un weekend.
1. Per interrompere automaticamente i punti di contatto di follow-up quando un prospect registra una riunione, attivare **[!UICONTROL Pausa prenotazione riunione]**.
1. Verifica che il **[!UICONTROL Fuso orario]** corrisponda al tuo pubblico.
1. Fai clic su **[!UICONTROL Salva e aggiungi potenziali]**.

Il piè di pagina di rinuncia è configurato a livello globale da un amministratore e si applica alle e-mail in uscita indipendentemente dalle impostazioni del flusso di lavoro. Vedi [Sincronizzazione rinuncia globale](#global-opt-out-sync).

#### Passaggio 5: aggiungere potenziali clienti e avviare la generazione di e-mail

Il salvataggio apre la vista di selezione del prospect, già filtrata dal targeting del passaggio 2.

![Aggiungi prospect per flusso di lavoro in uscita](./assets/outbound-workflow-create-add-prospects.png){width="700" zoomable="yes"}

1. Rivedi l&#39;elenco.

   Le righe in genere includono il nome del potenziale cliente, l’account, l’e-mail, la qualifica professionale, lo stato del coinvolgimento e lo stato del potenziale cliente.

1. Regolare i filtri qui se è necessario espandere o restringere l’elenco.
1. Seleziona i potenziali clienti utilizzando le caselle di controllo.
1. Fai clic su **[!UICONTROL Avanti: controlla i punti di contatto]** per avviare la generazione di **e-mail per potenziale**.

L&#39;intelligenza artificiale genera e-mail personalizzate per ogni potenziale cliente selezionato per **ogni punto di contatto e-mail** nella cadenza. I punti di contatto Phone e LinkedInMail rimangono nella cadenza come passaggi pianificati. La generazione può essere eseguita in background. Utilizzare **[!UICONTROL Notify when ready]** se si desidera continuare il lavoro mentre viene completato.

Per ogni potenziale cliente, l’intelligenza artificiale combina ogni prompt dei punti di contatto con dati specifici del potenziale cliente (persona, account, cronologia del coinvolgimento, notizie recenti) per produrre l’oggetto e il corpo.

### Rivedere e perfezionare le e-mail generate

Al termine della generazione, nella vista dei dettagli del flusso di lavoro viene visualizzato un banner per la revisione delle bozze. La revisione è necessaria e non viene inviato nulla finché non ricevi l’approvazione.

![E-mail generate dalla revisione del flusso di lavoro in uscita](./assets/outbound-workflow-create-review-generated-emails.png){width="700" zoomable="yes"}

1. Nella visualizzazione dettagli flusso di lavoro, fare clic su **[!UICONTROL Rivedi bozze]** nel banner.
1. Il passaggio **[!UICONTROL Rivedi punti di contatto]** ha due schede:
   * **[!UICONTROL Pronto per la revisione]** - E-mail che hanno terminato la generazione.
   * **[!UICONTROL Generazione in corso]** - Messaggi di posta elettronica ancora in fase di scrittura.
1. Nell’elenco dei potenziali clienti a sinistra, fai clic su un nome per caricare i punti di contatto del potenziale cliente a destra.
1. Utilizzare la freccia (**>**) in un punto di contatto per espandere e leggere l&#39;oggetto e il corpo completi.

#### Leggere il ragionamento dell’intelligenza artificiale

Per ogni e-mail generata, **[!UICONTROL Reasoning]** spiega come l&#39;intelligenza artificiale ha creato il messaggio, inclusi segnali, attributi e origini che hanno modellato il contenuto e call to action. Esamina queste informazioni e convalida la personalizzazione prima di approvare.

![Motivo IA per l&#39;e-mail generato dal flusso di lavoro in uscita](./assets/outbound-workflow-create-review-generated-email-reasoning.png){width="600" zoomable="yes"}

#### Modifica direttamente le e-mail

Per le piccole modifiche (testo, tono, una singola frase):

1. Nel punto di contatto espanso, fai clic sull&#39;icona _Modifica_ per aprire l&#39;editor.
1. Modifica l&#39;oggetto o il corpo.
1. Fai clic su **[!UICONTROL Salva]**.

#### Ottimizzare le e-mail con l’intelligenza artificiale

Per modifiche più grandi (ristrutturazione, spostamento dell&#39;enfasi o riformattazione del messaggio), utilizza **[!UICONTROL Genera con IA]**. L’agente di IA riscrive l’e-mail mantenendo il contesto di personalizzazione.

1. Nell&#39;editor e-mail, fai clic su **[!UICONTROL Genera con IA]**.

   ![Ottimizzazione e-mail generata dal flusso di lavoro in uscita con IA](./assets/outbound-workflow-create-review-generated-email-edit-regenerate.png){width="600" zoomable="yes"}

1. Immettere un&#39;istruzione di cancellazione, ad esempio:
   * `Make it shorter and more direct. Keep it under 100 words.`
   * `Focus more on the prospect's role and how the solution helps them specifically.`
   * `Change the call-to-action to suggest a 15-minute introductory call instead.`
1. Rivedi la revisione e, se necessario, modificala manualmente.
1. Fai clic su **[!UICONTROL Salva]**.

>[!TIP]
>
>Modifica direttamente il testo e il tono della tuta. Utilizza _[!UICONTROL Genera con IA]_ per riscrivere l&#39;e-mail da zero.

### Approva e iscrivi potenziali clienti

L’approvazione attiva la cadenza per un potenziale cliente. Fino a quando un potenziale cliente non viene approvato e iscritto, il sistema non invia loro e-mail.

1. Nell’elenco a sinistra dei potenziali clienti, seleziona i potenziali clienti di cui hai rivisto e-mail e che sei pronto a inviare.
1. Fai clic su **[!UICONTROL Approva e iscrivi prospect]** (in basso a destra).

![Selezione e approvazione del flusso di lavoro in uscita](./assets/outbound-workflow-create-approve-enroll-prospects.png){width="700" zoomable="yes"}

Le e-mail approvate vengono inviate durante il flusso di lavoro **finestra di invio** nel **fuso orario** configurato, nel giorno pianificato di ogni punto di contatto relativo all&#39;iscrizione. I potenziali clienti che non approvi rimangono in **[!UICONTROL Pronti per la revisione]** fino a quando non agisci. Dopo l’approvazione, il flusso di lavoro viene eseguito in base alla cadenza definita.

### Gestire i flussi di lavoro esistenti

Nella pagina _[!UICONTROL Flusso di lavoro in uscita]_, la scheda **[!UICONTROL Sfoglia]** elenca tutti i flussi di lavoro. Ogni scheda mostra l’obiettivo, i punti di contatto configurati e le metriche delle prestazioni. Utilizzare questa visualizzazione per monitorare i flussi di lavoro attivi, tornare alle bozze che richiedono ancora una revisione o aprire un flusso di lavoro per aggiungere altri potenziali clienti.

### Best practice per i flussi di lavoro in uscita

* **Investire nell&#39;obiettivo.** Il targeting a valle, la cadenza e le e-mail riconducono tutti all’obiettivo. Obiettivi specifici e focalizzati sui risultati superano quelli vaghi.
* **Finalizza i prompt dei punti di contatto prima della generazione per singolo prospect.** Dopo la generazione in blocco, le modifiche vengono in genere apportate un prospect alla volta.
* **Usa il ragionamento come controllo qualità.** Se viene enfatizzato il segnale sbagliato (o se ne manca uno ovvio), modifica l’e-mail o visita nuovamente il prompt del punto di contatto e rigenera la cadenza.
* **Corrispondenza tra lo strumento di modifica e la modifica.** Modifiche dirette per la formulazione e il tono; **[!UICONTROL Generare con IA]** per la ristrutturazione o il riframing.
* **Approva solo ciò che hai rivisto.** Espandi i punti di contatto, leggi il contenuto e perfeziona eventualmente prima dell’iscrizione.

### Sincronizzazione rinuncia globale

Gli amministratori possono aggiungere a ogni e-mail in uscita un piè di pagina per l&#39;annullamento dell&#39;abbonamento leggero che utilizza il verbiage [!DNL Marketo] pre-approvato. Quando un prospect seleziona il collegamento di rinuncia, Sales Qualifier elimina definitivamente il prospect da ulteriori e-mail e sincronizza di nuovo lo stato di rinuncia al CRM connesso. Consulta [Configurare la rinuncia e-mail globale](#configure-global-email-opt-out).

## Posta in uscita e-mail

Nel pannello Posta in uscita e-mail sono elencate tutte le e-mail automatizzate inviate.

<!--
## Meeting bookings

This panel displays all meetings set up through automation.

## Chat inbox

This panel displays all your chat threads.

![Panel showing chat threads with contact and thread summaries for sales automation](assets/chat-inbox.png)

You can interact with clients, and see summaries for the contact and the thread so that you can quickly know where you are in the thread.

-->

## Attività

L&#39;area _Attività_ in Qualificatore vendite offre ai rappresentanti per lo sviluppo aziendale uno spazio dedicato per gestire ed elaborare le azioni del flusso di lavoro in uscita. Il motore del flusso di lavoro in uscita genera automaticamente attività che rappresentano le azioni specifiche che un BDR deve intraprendere con ogni potenziale cliente: telefonate, LinkedInMails e revisioni di e-mail.

L&#39;esperienza di gestione delle attività è una **coda di elaborazione**, non un elenco attività. È possibile aprire un&#39;attività, eseguire un&#39;azione, contrassegnarla come completata e passare a quella successiva senza uscire dalla pagina.

Seleziona **[!UICONTROL Attività]** nella barra di navigazione a sinistra per aprire la pagina completa delle attività. Questa pagina è l&#39;area di lavoro principale per l&#39;elaborazione delle attività una alla volta.

![Pagina Attività con coda attività e pannello dettagli](./assets/tasks.png){width="800" zoomable="yes"}

<!--
**Homepage feed** - The homepage displays a running feed of your most urgent tasks, with overdue items at the top followed by today's tasks. Each item in the feed has an "Open" button that takes you directly to that task in the Tasks page with the detail panel already loaded.
-->

### Tipi di attività

Tutte le attività sono associate ai passaggi del flusso di lavoro in uscita. Esistono tre tipi:

**Chiamata telefonica** — creata quando una cadenza raggiunge un passaggio di chiamata telefonica. Il pannello attività mostra i punti di intonazione generati dall’agente e un campo in linea per le note della chiamata.

**LinkedIn InMail** — Creato quando una cadenza raggiunge un passaggio LinkedInMail. Il pannello attività mostra un oggetto generato dall’intelligenza artificiale e un corpo del messaggio che puoi copiare e inviare all’esterno del prodotto.

**Revisione e-mail** — creata una volta che il sistema termina la generazione di e-mail personalizzate per un potenziale cliente iscritto a un flusso di lavoro. Esamina e approva le e-mail prima di iniziare l’uscita per quel potenziale cliente. Ogni potenziale cliente riceve un’attività di revisione e-mail separata; se iscrivi 10 potenziali clienti in un flusso di lavoro, al termine della generazione vengono visualizzate fino a 10 attività di revisione e-mail.

### Gestione attività

La pagina Attività è divisa in due pannelli:

* **A sinistra — Elenco attività:** La coda delle attività, ordinata e filtrata in base alle impostazioni di visualizzazione e ordinamento selezionate.
* **Destra — Pannello di lavoro attività:** Dettagli per l&#39;attività selezionata, incluse informazioni sul prospect, contesto del flusso di lavoro, contenuto specifico dell&#39;attività e controlli delle azioni.

Selezionando un’attività nel pannello di sinistra, i relativi dettagli vengono caricati nel pannello di destra senza uscire dalla pagina.

#### Controlli coda

Il pannello di lavoro include i controlli **Successivo** e **Precedente** per spostarsi nella coda attività in ordine. La coda rispetta tutte le impostazioni di ordinamento e filtro applicate all&#39;elenco. Pertanto, se stai eseguendo attività di telefonata scadute ordinate in base alla data di scadenza, _Successivo_ e _Precedente_ passano esattamente attraverso questo set.

Quando contrassegni un’operazione come completata, il pannello avanza automaticamente all’operazione successiva nella coda.

#### Note

Per le attività Phone Call (Chiamata telefonica) e LinkedInMail (InMail), nel pannello di lavoro è disponibile un campo delle note in linea. Le note vengono salvate automaticamente quando si fa clic in modo da non perderle quando si passa a un&#39;altra attività prima di contrassegnare quella corrente come completata.

#### Azioni attività

Per gestire le attività, utilizzare le azioni seguenti:

* **[!UICONTROL Contrassegna come completato]** - Azione primaria. Utilizza questa azione dopo aver eseguito l’attività: effettuato la chiamata, inviato InMail o rivisto e approvato le e-mail. Al completamento, l&#39;attività viene registrata come **Completata** e la coda avanza automaticamente.

* **[!UICONTROL Salta punto di contatto]** - Disponibile dal menu di overflow nel pannello di lavoro. Utilizza questa opzione quando non riesci a completare questo passaggio, ma il prospect rimane una destinazione valida nel flusso di lavoro.
  * Il prospect avanza al passaggio successivo nella cadenza. Le attività future vengono comunque generate nei tempi previsti.
  * Seleziona un motivo: *Informazioni contatto non valide*, *Intervallo non valido*, *Contenuto non rilevante* o *Altro* (con un campo a testo libero).
  * Lo stato dell&#39;attività è impostato su **Ignorato** e registrato con il motivo e la marca temporale.
  * Se questo è stato l’ultimo passaggio del flusso di lavoro, l’esecuzione del flusso di lavoro del prospect termina. L’attività è ancora registrata come Ignorata (non rimossa).

* **[!UICONTROL Rimuovi dal flusso di lavoro]** - Disponibile dal menu di overflow nel pannello di lavoro. Utilizzalo quando il prospect non appartiene più a questo flusso di lavoro.

  Quando rimuovi un prospect da un flusso di lavoro:
  * Tutte le attività in sospeso e future per quel prospect all’interno di questo flusso di lavoro vengono annullate.
  * Lo stato di iscrizione del prospect cambia in **Rimosso da BDR**.
  * Seleziona un motivo: *Società di sinistra*, *Duplicato*, *Adattamento errato*, *Già convertito* o *Altro* (con un campo di testo).
  * Viene visualizzata una finestra di dialogo di conferma: *&quot;Questa azione annullerà tutti i punti di contatto rimanenti per [Prospect] in [Nome flusso di lavoro]. Continuare?&quot;*
  * Lo stato dell&#39;attività è impostato su **Rimosso**. Anche tutte le attività di pari livello annullate sono contrassegnate come **Rimosse**.

>[!NOTE]
>
>I dati relativi al motivo di salto e rimozione vengono utilizzati nelle analisi, incluse le percentuali di salto dei canali, le percentuali di rimozione dei flussi di lavoro e i motivi principali. Questo consente di migliorare la qualità del flusso di lavoro e di informare l’analisi delle prestazioni nel tempo.

**Ignora automaticamente**

Le attività LinkedIn InMail e di telefonata stagnanti vengono ignorate automaticamente se rimangono incomplete per due giorni. Il salto automatico mantiene un potenziale cliente in movimento attraverso la cadenza senza arrestare l’esecuzione e non influisce sulla timeline dell’e-mail. I punti di contatto e-mail pianificati continuano a essere inviati come pianificato.

### Stato attività

Ogni attività si sposta nei seguenti stati:

| Stato | Descrizione |
|---|---|
| **In sospeso** | Creato, ma il passaggio precedente del flusso di lavoro non è ancora stato completato. Non visibile nell&#39;elenco delle attività. |
| **In arrivo** | Il passaggio precedente è completo, ma la data di scadenza è nel futuro. Visibile e actionable — puoi completarlo in anticipo se il momento è giusto. |
| **Open** | Scade oggi. Visibile e actionable. |
| **Scaduto** | Scaduto, non ancora completato. Visibile, actionable e contrassegnato visivamente. |
| **Completato** | Hai eseguito l’attività e l’hai contrassegnata come completata. |
| **Ignorato** | Hai saltato questo punto di contatto. Il prospect avanza nel flusso di lavoro. |
| **Rimosso** | Il prospect è stato rimosso dal flusso di lavoro. Tutte le attività di pari livello vengono annullate. |
| **Annullato** | Annullata dal sistema a causa di una modifica del flusso di lavoro o della rimozione di un potenziale cliente. |

### Visualizzazioni elenco

Utilizza le schede nella parte superiore dell’elenco delle attività per passare da una visualizzazione all’altra:

* **Oggi** *(impostazione predefinita)* — Attività in scadenza oggi che non sono state completate.

* **Scaduto** — Attività la cui data di scadenza è passata e sono ancora aperte. Risolvi prima queste attività.

* **Prossimo** — Attività con una data di scadenza futura in cui il passaggio precedente del flusso di lavoro è già stato completato. Queste attività sono visibili in anticipo, per consentirti di pianificare o agire prima al momento giusto (ad esempio, se sei già in contatto con un potenziale cliente). Viene visualizzata la data di scadenza pianificata in modo da conoscere la tempistica prevista.

* **Completato**: record di attività completate, ignorate o rimosse. Utile a scopo di revisione e audit.

### Filtraggio e ricerca

Sono disponibili diversi modi per filtrare l’elenco delle attività:

* Filtra per tipo di attività utilizzando un elenco a selezione multipla. Se si selezionano più tipi, le attività corrispondono a *any* dei tipi selezionati (ad esempio, Phone Call **or** Email Review).

* Filtra per stato attività. Se si selezionano più stati, vengono visualizzate le attività che corrispondono a uno qualsiasi degli stati selezionati.

* Filtra i gruppi utilizzando la logica **AND**. Ad esempio, `Type = Phone Call and Status = Overdue` mostra solo le attività di chiamata scadute.

Utilizzare la barra di ricerca per trovare le attività in base al nome del prospect, al nome della società o al nome del coinvolgimento. La ricerca viene applicata a fianco di qualsiasi filtro attivo. Solo corrispondenza testo: corrispondenze parziali esatte, nessuna ricerca fuzzy.

### Ordinamento

Utilizzare il controllo **Ordina per** per scegliere l&#39;ordine dell&#39;elenco attività. L&#39;ordinamento determina anche l&#39;ordine in cui i comandi Successivo e Precedente si spostano nella coda.

| Opzione di ordinamento | Comportamento |
|---|---|
| **Data scadenza (crescente)** *(predefinito)* | Prima la data di scadenza più vecchia. Le attività scadute vengono visualizzate prima delle attività odierne. |
| **Data scadenza (decrescente)** | Prima la data di scadenza più recente. |
| **Data creazione (più recente)** | Attività create più di recente. |
| **Data creazione (meno recente)** | Prima le attività create meno di recente. |
| **Tipo di attività** | Raggruppati per tipo nell&#39;ordine: → telefonata LinkedIn InMail → Email Review. All’interno di ciascun gruppo, in ordine crescente di data di scadenza. |

### Attività scadute

Un&#39;attività scade il giorno successivo alla data di scadenza se non è stata completata. Attività scadute:

* Sono visualizzati nella visualizzazione **Scaduto** e nella parte superiore del feed della home page.
* Sono contrassegnati visivamente con un contrassegno &quot;Scaduto&quot; nell’elenco delle attività.
* Rimanete completamente utilizzabili: potete completarli, saltarli o rimuoverli.

### Attività future

Le attività future vengono create nel momento in cui un potenziale cliente completa un passaggio del flusso di lavoro, anche se la scadenza del passaggio successivo è ancora nel futuro. Questa visibilità ti consente di accedere in anteprima a insight nella pipeline in modo da poter pianificare in anticipo o agire in anticipo quando si presenta l’opportunità.

Le attività future mostrano la data di scadenza pianificata, in modo da sapere sempre quando devono essere gestite. Il completamento anticipato di un&#39;attività è completamente supportato: il motore del flusso di lavoro registra la data di completamento effettiva e avanza normalmente il prospect.

### Completamento attività

Il completamento dell’attività non è limitato alla pagina Attività.

**Visualizzazione prospect coinvolti:** Le anteprime dei punti di contatto nella pagina di un prospect coinvolto includono un&#39;azione _Segna come completato_ insieme a un&#39;anteprima del contenuto e a un campo delle note facoltative. Il completamento di un’attività qui ne aggiorna immediatamente lo stato nella pagina Attività. Questa vista non attiva il comportamento di avanzamento automatico, ma è una superficie di visualizzazione e di azione, non una superficie di elaborazione della coda.

**Salesforce (plug-in CRM):** il plug-in Qualificatore vendite in Salesforce visualizza lo stato dell&#39;attività (in arrivo, in sospeso, completato, in ritardo, ignorato) nella scheda del flusso di lavoro in uscita. Nella versione corrente, la scheda CRM è **di sola lettura**. È possibile visualizzare lo stato dell&#39;attività ma è necessario completare le attività dall&#39;interno di Qualificatore vendite.

### Stati vuoti

* **Oggi senza attività:** Viene visualizzato un messaggio di _Sei stato contattato per oggi_. Se sono presenti le attività imminenti, verrà visualizzato un messaggio con il seguente messaggio: _Sono presenti [N] attività imminenti — visualizza_.
* **Attività scadute presenti:** Un prompt ti incoraggia a risolvere prima le attività scadute.

## Prenotazione riunione

Qualificatore vendite trasforma le conversazioni impegnate in riunioni prenotate senza uscire dal flusso in uscita. Quando si collega il calendario, Qualificatore vendite genera un collegamento di prenotazione personale che i potenziali clienti utilizzano per pianificare il tempo con l&#39;utente.

* **Collegamenti di prenotazione** - Configura la connessione e la disponibilità del calendario in [Impostazioni profilo](#profile-settings). Il collegamento di prenotazione può essere aggiunto alla firma e-mail in modo che venga visualizzato nelle e-mail in uscita.
* **Inserimento automatico in una cadenza** - Qualificatore vendite inserisce il collegamento di prenotazione nei punti appropriati in una cadenza, in modo che l&#39;invito a incontrarsi venga visualizzato quando è più rilevante. Potete sostituire manualmente il posizionamento.
* **Pausa prenotazione** - Quando un prospect registra una riunione, **[!UICONTROL Pausa prenotazione riunione]** interrompe automaticamente ulteriori follow-up. Consulta [Configurare le impostazioni del flusso di lavoro](#step-4-configure-workflow-settings).

Tieni traccia dei risultati della prenotazione nella sezione [Prestazioni](#performance).

## Centro conoscenze

Il _[!UICONTROL Centro conoscenze]_ consente a Account Qualification Agent (AQA) di accedere ai propri materiali di vendita, in modo che il qualificatore di vendita possa generare ricerche, approfondimenti sulle qualifiche e attività di divulgazione che riflettano le modalità di vendita dell&#39;organizzazione. La creazione e la gestione del playbook è un&#39;attività amministrativa.

![Centro conoscenze](./assets/integrations-knowledge-center.png){width="700" zoomable="yes"}

### Carica materiale promozionale

1. Nel menu di navigazione a sinistra, espandi **[!UICONTROL Amministrazione]** e seleziona **[!UICONTROL Impostazioni amministratore]**.
1. Seleziona **[!UICONTROL Centro informazioni]** in **[!UICONTROL Integrazioni]**.
1. Imposta **[!UICONTROL Nome società]** e **[!UICONTROL URL società]** utilizzati da Qualificatore vendite per eseguire ricerche nell&#39;azienda e nelle bozze di e-mail.
1. Carica giochi di vendita, profili cliente ideali (ICP), guide di posizionamento e altro materiale promozionale in formato PDF, PPTX o DOCX.

In ogni documento caricato viene visualizzato il relativo stato di elaborazione, ad esempio **[!UICONTROL Pronto]**, e la data dell&#39;ultimo aggiornamento.

### Creare un playbook

Dopo aver caricato i documenti, seleziona **[!UICONTROL Genera playbook]** per trasformarli in playbook.

>[!NOTE]
>
>L&#39;elaborazione di un playbook richiede circa 24 ore prima di essere pronto per l&#39;uso.

Quando il playbook è pronto, alimenta sia l&#39;impegno che l&#39;assistenza:

* **Messaggi e-mail in uscita** - Fai riferimento al playbook durante la generazione di e-mail assegnando un nome al documento e al contesto nel prompt. Consulta [Generare e rivedere i punti di contatto](#step-3-generate-and-review-touchpoints).
* **Assistente alle vendite per conversazioni** - Per estrarre dal playbook, puntare l&#39;assistente al Knowledge Center. Consulta [Assistente alle vendite per conversazioni](#conversational-sales-assistant).

## Assistente alle vendite per conversazioni

L&#39;Assistente alle vendite per conversazioni è un&#39;esperienza di chat in cui si pongono domande in linguaggio naturale e si ottengono risposte basate sul contesto di vendita. L’assistente si avvale di:

* La knowledge base interna, incluso qualsiasi playbook del [Centro conoscenze](#knowledge-center)
* Segnali CRM dal CRM connesso
* [!DNL Marketo] dati attività e coinvolgimento
* Ricerca web

Utilizza l’assistente per prepararti prima dell’attività di outreach, ad esempio per creare il posizionamento dell’account prima di una riunione. Per estrarre da un playbook costruito, puntare l&#39;assistente al Centro di conoscenza nella tua domanda. Ad esempio: `From the Knowledge Center, help me position our security solution for ABC Corp ahead of tomorrow's call.`

## Prestazioni

La sezione **[!UICONTROL Prestazioni]** mostra come sta andando il tuo outbound, in modo da poter vedere cosa sta funzionando e dove modificare.

### Prestazioni e-mail

Verifica il volume e l’efficacia dell’e-mail in uscita:

* E-mail inviate
* Tasso di apertura
* Tasso di clic
* Percentuale risposte

Qualificatore di vendita identifica le risposte fuori sede e i mancati recapiti con gli stati corrispondenti, in modo da poterli distinguere dagli impegni dei potenziali clienti.

### Prestazione prenotazione riunione

Le schede di stato per la prenotazione delle riunioni riassumono la posizione delle riunioni prenotate. Filtrare le schede per concentrarsi sulle riunioni e sugli stati che si desidera esaminare.

## Integrazioni e gestione delle relazioni con i clienti

Con le integrazioni, Qualificatore di vendita si connette al CRM in modo che i flussi di lavoro Account Qualification Agent (AQA) e in uscita condividano una visione coerente di lead, account, contatti, attività e proprietari in Salesforce o Microsoft Dynamics 365. Qualificatore di vendita legge i dati e le attività di vendita CRM per arricchire le informazioni e può riscrivere le attività di outreach registrate e lo stato di rinuncia. In caso contrario, non modifica i record CRM tramite questa connessione.

Le connessioni CRM, il mapping dei campi in entrata e la sincronizzazione delle attività sono configurate da un amministratore in **[!UICONTROL Amministrazione]** > **[!UICONTROL Impostazioni amministratore]** > **[!UICONTROL Connessioni CRM]**. Gli utenti standard utilizzano i dati e i filtri CRM configurati, ma non possono modificare queste impostazioni.

### MCP CRM e il plug-in incorporato

Qualificatore di vendita funziona con il tuo CRM in più di un modo:

* **Eseguire query sui dati CRM tramite MCP CRM**. Account Qualification Agent esegue query sui dati CRM in tempo reale tramite MCP CRM, in modo che le risposte e le informazioni riflettano lo stato corrente dei record.
* **Plug-in incorporato** - Il plug-in CRM incorporato presenta le informazioni principali [!DNL Marketo Sales Insights] (MSI) insieme ai nuovi dati agente, direttamente nel CRM. Dal plug-in, aggiungi un prospect a Sales Qualifier con un solo clic.
* **Sincronizzazione attività** - Quando un amministratore abilita **[!UICONTROL Sincronizzazione attività]**, le attività di outreach vengono sincronizzate con il sistema di gestione delle relazioni con i clienti, in modo che i rappresentanti possano visualizzare l&#39;attività Qualificatore vendite negli strumenti già utilizzati.

>[!IMPORTANT]
>
>L&#39;accesso a **[!UICONTROL Impostazioni amministratore]** richiede l&#39;appartenenza ai gruppi di utenti `Sales Qualifier` e `Sales Qualifier Admins`.

### Ambito di accesso CRM

Qualificatore di vendita legge le entità CRM necessarie e può riscrivere solo un set di dati definito. Le entità tipiche lette includono utenti, contatti, mappature del proprietario, lead, account, opportunità e attività. Il write-back è limitato alle attività di estensione registrate e allo stato di rinuncia. L’amministratore del sistema di gestione delle relazioni con i clienti prepara l’accesso API in Salesforce o Dynamics. Poi connetti Qualificatore di vendita, mappa i campi in entrata e scegli se sincronizzare le attività nell’app.

>[!NOTE]
>
>I passaggi delle credenziali seguenti descrivono l&#39;accesso in lettura agli oggetti CRM. Se abiliti la sincronizzazione delle attività o la rinuncia al write-back, rivolgiti al tuo amministratore del sistema di gestione delle relazioni con i clienti per concedere l’accesso in scrittura corrispondente richiesto dalla configurazione del sistema di gestione delle relazioni con i clienti.

### Prepara le credenziali nel CRM

Rivolgiti all’amministratore del sistema di gestione delle relazioni con i clienti prima di collegare il qualificatore vendite. Di seguito viene riepilogato ciò che in genere viene creato in ciascun sistema.

#### Microsoft Dynamics 365 (Dataverse/Power Platform)

1. In Azure Active Directory, registrare un&#39;applicazione (**[!UICONTROL Registrazioni app]**).

   Prendi nota dell&#39;**ID client** e dell&#39;**ID tenant** e crea un **Segreto client**.

1. Nel **[!UICONTROL centro di amministrazione di Power Platform]**, apri l&#39;ambiente e passa a **[!UICONTROL Impostazioni]** > **[!UICONTROL Utenti + autorizzazioni]** > **[!UICONTROL Utenti applicazioni]**.

1. Crea un utente dell’applicazione collegato a quell’app Azure AD.

1. Assegna un ruolo di sicurezza che consenta a **read** l&#39;accesso alle entità richieste da Qualificatore vendite, ad esempio lead, contatti, account, opportunità e attività.

   L’app richiede un ruolo di sicurezza con accesso in lettura ai dati.

**Informazioni da fornire durante la connessione a Dynamics:**

* ID client
* Segreto client
* ID tenant
* URL istanza Dynamics (URL organizzazione)

#### Salesforce

In Salesforce, [crea un&#39;app client esterna](https://help.salesforce.com/s/articleView?id=xcloud.create_a_local_external_client_app.htm&type=5) (o una _app connessa_) con OAuth abilitato e ambiti che consentono l&#39;accesso API a identità e dati, in base agli standard di sicurezza della tua organizzazione. L’utente che esegue l’integrazione deve disporre dell’accesso in lettura a oggetti quali lead, account, contatti, attività, eventi e opportunità. Per le attività amministrative è spesso necessario che un utente con **[!UICONTROL Gestione app collegate]** (tra le altre autorizzazioni) visualizzi una chiave consumer e un segreto dopo la creazione.

>[!PREREQUISITES]
>
>Per creare un’app client esterna, l’amministratore del prodotto deve verificare che siano abilitati i seguenti elementi (dal profilo o dal set di autorizzazioni):
>
>* Personalizza applicazione
>* Visualizza configurazione e configurazione
>* Modifica tutti i dati
>* Gestire le app collegate (importante)
>
>   Se _Gestisci app collegate_ non è abilitato, non sarà possibile visualizzare l&#39;ID client e il segreto client dopo aver creato l&#39;app client esterna.

Quando crei l’app client esterna, abilita OAuth e concedi le autorizzazioni. Abilita anche le seguenti credenziali client:

* Accedere al servizio URL di identità (ID, profilo, e-mail, indirizzo, telefono)
* Gestire i dati utente tramite API (API)
* Accedere a identificatori utente univoci (openid)

Dopo aver creato l’app, abilita di nuovo il flusso delle credenziali del client e utilizza l’e-mail di contatto come nome utente.  Quando le credenziali client sono abilitate, configurare un utente per _Esegui come_.

Assicurati che l’utente configurato abbia accesso in lettura ai seguenti oggetti:

* Lead
* Account
* Contatti
* Attività
* Eventi
* Opportunità
* OpportunityContactRoles
* OpportunityLineItems

**Informazioni da fornire per la connessione a Salesforce in Qualificatore vendite:**

* ID client (chiave consumer)
* Segreto client (segreto consumer)
* URL callback (come configurato nell&#39;app connessa)
* URL istanza Salesforce

>[!IMPORTANT]
>
>Non inviare i segreti del cliente tramite e-mail. Utilizza il canale sicuro approvato della tua organizzazione per condividere le credenziali con chi le inserisce in Qualificatore vendite.

### Connettersi al CRM

1. Accedi a Qualificatore di vendita e verifica che sia selezionato l’ambiente o la sandbox corretta.

1. Nel menu di navigazione a sinistra, espandi **[!UICONTROL Amministrazione]** e seleziona **[!UICONTROL Impostazioni amministratore]**.

1. Seleziona **[!UICONTROL connessioni CRM]** in **[!UICONTROL Integrazioni]**.

   Nella pagina sono visualizzate le schede per Salesforce e Microsoft Dynamics. Una connessione inattiva visualizza **[!UICONTROL Connessione]**. Una connessione configurata visualizza **[!UICONTROL Connesso]** e un&#39;azione **[!UICONTROL Gestisci]**.

   ![Impostazioni amministratore connessioni CRM con schede di connessione Salesforce e Dynamics](./assets/integrations-crm-connections.png){width="800" zoomable="yes"}

1. Fai clic su **[!UICONTROL Connetti]** per il sistema di gestione delle relazioni con i clienti utilizzato.

1. Immetti l&#39;ID client, i segreti, i valori tenant o callback e l&#39;**URL istanza** dal tuo amministratore CRM.

1. Dopo una connessione riuscita, verificare che nella scheda sia visualizzato **[!UICONTROL Connesso]**.

### Linee guida per l’URL dell’istanza

L&#39;**URL istanza** deve essere l&#39;URL di base dell&#39;ambiente utilizzato dal CRM per la configurazione dell&#39;API e dell&#39;integrazione, non un nome host di sola interfaccia utente.

**Salesforce**

1. Accedi e annota il sottodominio _Dominio personale_ dell&#39;organizzazione dalla barra degli indirizzi del browser (il valore `{{mydomain}}`).

1. Per Qualificatore di vendita, utilizzare il modulo canonico: `https://{{mydomain}}.my.salesforce.com` .

   **not** utilizza un URL `lightning.force.com` come URL istanza.

**Microsoft Dynamics 365**

1. Apri il CRM nel browser e copia l’URL di base dalla barra degli indirizzi.

   In genere è nel formato `https://{{org}}.crm.dynamics.com`.

### Mappa campi CRM (mappatura in entrata)

Dopo aver connesso il CRM, selezionare **[!UICONTROL Gestisci]** per la connessione e aprire **[!UICONTROL Mappatura in entrata]**. Il mapping in entrata controlla i campi CRM che il qualificatore vendite richiama nell&#39;applicazione.

1. Selezionare un gruppo di oggetti: **[!UICONTROL Contatto]**, **[!UICONTROL Prospect]** o **[!UICONTROL Account]**.
1. Selezionare **[!UICONTROL Aggiungi sezione]** e immettere un nome di sezione e una descrizione facoltativa.
1. Aggiungi i campi di gestione delle relazioni con i clienti alla sezione.

   Ogni riga di campo visualizza il relativo **[!UICONTROL Nome visualizzato]**, **[!UICONTROL Nome campo]** e **[!UICONTROL Tipo di dati]**.

1. Attiva **[!UICONTROL Filterable]** per ogni campo che deve essere disponibile come filtro nell&#39;elenco **[!UICONTROL Prospect]**.
1. Visualizza l’anteprima della mappatura e salvala.

I campi mappati vengono visualizzati nelle aree corrispondenti di Qualificatore di vendita:

* I campi Prospect e Contatto vengono visualizzati nella scheda **[!UICONTROL Persona]** per i prospect.
* I campi Conto vengono visualizzati nella vista Conto.
* I campi relativi all’opportunità vengono visualizzati nelle aree dell’opportunità dell’esperienza dell’account.

### Configurare la sincronizzazione delle attività (mappatura in uscita)

1. Da **[!UICONTROL connessioni CRM]**, selezionare **[!UICONTROL Gestisci]** per il CRM connesso.
1. Apri **[!UICONTROL Mappatura in uscita]**.
1. Attiva **[!UICONTROL Sincronizzazione attività]** per sincronizzare nuovamente le attività di distribuzione del qualificatore vendite con il CRM.

Quando la sincronizzazione delle attività è disattivata, il qualificatore vendite può continuare a utilizzare i dati CRM in entrata, ma non riscrive le attività di outreach nel CRM.

### Configurare la rinuncia e-mail globale

1. Nel menu di navigazione a sinistra, espandi **[!UICONTROL Amministrazione]** e seleziona **[!UICONTROL Impostazioni amministratore]**.
1. Seleziona **[!UICONTROL Impostazioni e-mail]** in **[!UICONTROL Conformità]**.
1. Attiva **[!UICONTROL Includi collegamento di rinuncia in ogni e-mail]** per aggiungere un piè di pagina per l&#39;annullamento dell&#39;iscrizione alle e-mail in uscita.
1. In **[!UICONTROL Modello per messaggi di rinuncia]** immettere il testo del piè di pagina. Includi il token `{{opt_out_link}}` in cui dovrebbe essere visualizzato il collegamento per l&#39;annullamento dell&#39;abbonamento cliccabile.
1. Salva le impostazioni.

Quando un prospect seleziona il collegamento, Sales Qualifier elimina definitivamente il prospect da ulteriori e-mail. Anche lo stato di rinuncia viene sincronizzato con il CRM connesso.

### Riferimento: parametri API di esempio

Il team di gestione delle relazioni con i clienti può utilizzare questi esempi per confermare che l’accesso in lettura restituisca i campi lead previsti.

**Dinamica (estratto in stile OData)**

```text
$select=fullname,_ownerid_value,leadid,emailaddress1,jobtitle,statuscode,createdon,modifiedon,statecode
$filter=_ownerid_value eq '<crmUserId>' [AND additional filters]
$expand=Lead_ActivityPointers(...),parentaccountid(...)
$orderby=modifiedon desc
```

**Salesforce (estratto SOQL)**

```sql
SELECT Id, Salutation, FirstName, LastName, Name, Title, Company, Email,
  LeadSource, Status, OwnerId, LastModifiedDate, LastActivityDate, CreatedDate,
  (SELECT Id, Subject, ActivityDate, Status FROM Tasks ORDER BY ActivityDate DESC LIMIT 1),
  (SELECT Id, Subject, ActivityDateTime FROM Events ORDER BY ActivityDateTime DESC LIMIT 1)
FROM Lead
WHERE OwnerId = '<crmUserId>' AND IsDeleted = false
ORDER BY LastModifiedDate DESC
```

## Impostazioni profilo

Le impostazioni del profilo specificano informazioni su di te, tra cui dati personali, e-mail, calendario e disponibilità della chat.

### Impostazioni e-mail

Nella scheda **[!UICONTROL Impostazioni e-mail]**, configura le connessioni e-mail.

![Scheda Impostazioni e-mail con le opzioni di connessione e la configurazione della firma e-mail](assets/email-settings.png)

* **[!UICONTROL Connessioni e-mail]** - Fare clic su **[!UICONTROL Connetti]** e seguire la procedura di accesso di Microsoft.

* **[!UICONTROL Firma e-mail]** - Configura la firma e-mail utilizzata nelle e-mail generate automaticamente. Aggiungi il collegamento [prenotazione riunione](#meeting-booking) alla firma in modo che i potenziali clienti possano pianificare con te gli orari.

### Configurazione calendario

Nella scheda **[!UICONTROL Configurazione calendario]**, imposta il tuo fuso orario e la tua disponibilità.

<!-- 
![Calendar settings tab showing time zone and availability options](assets/calendar-settings.png)
-->

* **[!UICONTROL Connessione calendario]** - Fai clic su **[!UICONTROL Connetti]** e segui la procedura di accesso a Microsoft per integrare il calendario.

* **[!UICONTROL E-mail di conferma riunione]** - Quando un cliente conferma una riunione con te, riceve l&#39;e-mail di conferma come risposta. Utilizza queste impostazioni per definire l’oggetto e il corpo dell’e-mail.

* **[!UICONTROL Preferenze]** - Imposta la durata predefinita della riunione e l&#39;intervallo tra le riunioni di back-to-back.

Se si disconnette il calendario:

* I collegamenti di prenotazione attivi sono effettivamente disabilitati.
* La pagina di prenotazione mostra uno stato amichevole, temporaneamente non disponibile.
* La riconnessione mantiene le impostazioni.

### Disponibilità del calendario

La disponibilità del calendario in Qualificatore di vendita si basa su due input:

* Calendario di lavoro connesso (Outlook o Gmail)
* Regole configurate per la disponibilità e il controllo orario in _Impostazioni calendario_.

Il qualificatore vendite legge lo stato di disponibilità dal calendario connesso, non dal contenuto completo dell’evento, e lo utilizza insieme alle regole configurate per decidere quali slot di prenotazione un potenziale cliente può visualizzare.

Puoi configurare:

* Ore lavorative per giorno della settimana
* Più blocchi al giorno (ad esempio: 9:00-12:00 e 1:00-5:00)
* Il tuo fuso orario
* Durata riunione
* Buffer prima/dopo le riunioni
* Avviso minimo
* Finestra di prenotazione

<!-- 
### Chat settings

In the **[!UICONTROL Chat settings]** tab, set your Timezone Live chat availability.

![Chat settings tab for configuring timezone and live chat availability](assets/chat-settings.png)

## Representative management

The _[!UICONTROL Representative management]_ panel displays the defined representatives and their calendar status.

## Meeting performance

This panel presents analytics around your completed meetings.
-->

<!--
 SHPHR-24341 remove section
## Set up the Chrome plugin

The AI Assistant Chrome plugin is available on the [Google Store](https://chromewebstore.google.com/detail/ai-assistant/hancbabllcmckehonngbdkhilocpdfji?authuser=0&hl=en).

When the plugin is installed in Chrome, the Adobe logo appears on the middle right when you are on an integrated site:

* Adobe web applications
* Salesforce
* Outlook
* Microsoft Dynamics and web applications
* Google applications 
-->
