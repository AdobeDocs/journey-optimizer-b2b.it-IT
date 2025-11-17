---
title: Qualificatore di vendita
description: Automatizzare la qualifica di potenziale cliente B2B e l'impegno con i qualificatori di vendita. Fornisce ricerca basata sull’intelligenza artificiale, redazione di e-mail, integrazione CRM e piani di coinvolgimento per i BDR.
feature: AI Assistant, Sales Insights, Account Journeys
role: User
source-git-commit: dc6495a65b89cb3993c4b72706298181a3b555db
workflow-type: tm+mt
source-wordcount: '1290'
ht-degree: 1%

---


# Qualificatore di vendita

>[!NOTE]
>Questa funzione è attualmente a disponibilità limitata e non è disponibile per tutti gli utenti.
>

Sales Qualifier è un’applicazione aggiuntiva basata sull’intelligenza artificiale per Adobe Journey Optimizer B2B edition che contiene il Account Qualification Agent ed è progettata per semplificare i flussi di lavoro per i rappresentanti di sviluppo aziendale (BDR, Business Development Representative). Qualificatore di vendita automatizza i flussi di lavoro di qualificazione dei potenziali clienti, coinvolgimento degli acquirenti e coinvolgimento degli acquirenti su tutti i canali. Riduce il carico BDR manuale e accelera la velocità della pipeline per le aziende B2B aziendali.
Utilizza il browser e i plug-in e-mail per accedere alle informazioni aziendali direttamente in CRM o Outlook.

Sales Qualifier è incluso in Journey Optimizer B2B edition, ma è un&#39;app separata all&#39;interno di Experience Platform Experience Cloud.

![Home page Qualificatore vendite](assets/home-screen.png)

## Agente Account Qualification

Il Account Qualification Agent (AQA) è il cuore del qualificatore di vendita. L’AQA utilizza l’intelligenza artificiale per leggere gli account e determinare quali sono pronti per il passaggio successivo. Aiuta nella ricerca, nella redazione di e-mail e negli aggiornamenti CRM.

![Account Qualification Agent](assets/acc-qualification-agent.png)

* **Ricerca prospect**

  Effettua ricerche utilizzando il recupero e la visualizzazione automatici delle informazioni chiave sul potenziale cliente (come titolo del lavoro, impegni recenti, acquisto di iscrizioni al gruppo) per ottenere un quadro completo in pochi secondi.

* **Ricerca account**

  Eseguire ricerche sull&#39;account utilizzando il recupero automatico e la visualizzazione di informazioni dettagliate sull&#39;organizzazione di un potenziale cliente. Queste informazioni includono i dati vitali dell&#39;azienda, le notizie recenti, le priorità strategiche e i principali membri coinvolti.

* **E-mail bozza**

  Genera bozze e-mail sintetizzando le ricerche provenienti da approfondimenti di potenziali clienti e account per produrre contenuti e-mail singoli e personalizzati pertinenti in base all’obiettivo del BDR.

* **E-mail piano di coinvolgimento**

  Creare bozze e-mail del piano di coinvolgimento personalizzate per ogni passaggio di una cadenza di attività definita da BDR, garantendo che l’intera sequenza sia personalizzata

### Utilizzo di base

Gli agenti di IA per Adobe utilizzano _query in linguaggio naturale_, il che significa che utilizzano la stessa lingua nel prompt del testo come si farebbe nel parlare con una persona. Più sei dettagliato, migliori saranno i risultati.

Utilizzando il linguaggio naturale, puoi chiedere all’agente di:

* `Show me my assigned leads with no engagement yet`
* `Show me all my leads that are not part of any autonomous engagement`
* `Give me a detailed summary on Acme company, including their buying group, recent intent signals, and our past engagement.`

Puoi capire immediatamente quali account e lead sono più attivi e mostrano le intenzioni più alte, in modo da concentrare la tua energia dove ha il maggior impatto.

Eseguire un&#39;iterazione nel percorso perfezionando le richieste per ottenere i risultati desiderati. Ad esempio:

* Crea un disegno e-mail di follow-up dal contesto, ad esempio chiamate o rapporti sui guadagni. Fino a 120 parole. Oggetto: Captivazione, con un tema chiave. Introduzione: hook con una citazione diretta da origini di contesto. Corpo: connettiti ai punti critici e alle proposte di valore. CTA: propone una breve chiamata per approfondire l’analisi.

* L’obiettivo di questa e-mail è quello di avviare una conversazione e rafforzare la credibilità. Redigi un&#39;e-mail sotto 120 parole con un tono consultivo ed empatico. Assicurati di evitare un approccio troppo familiare o di vendita e non utilizzare le frasi &quot;spera di stare bene&quot;, &quot;solo il check-in&quot; o &quot;per favore&quot;.

## Potenziali clienti

Questa finestra elenca tutti i lead a cui hai accesso. Offre un controllo rapido su elementi quali lo stato del lead e l’ultima attività.

![Visualizza tutti i lead nella tabella Lead](assets/prospects.png)

Fai clic sull&#39;icona _Filtro_ ![Icona Filtro](../../assets/do-not-localize/icon_filter-outline.svg) per filtrare l&#39;elenco visualizzato in base allo stato del lead.

## Piani di coinvolgimento

Questa finestra fornisce dettagli su qualsiasi piano di coinvolgimento definito.

![Piani di coinvolgimento](assets/engagement-plans.png)

Per creare un nuovo piano di coinvolgimento, fare clic su **[!UICONTROL Crea piano di coinvolgimento]**.

1. Nella fase _Dettagli_, fornisci un nome e una descrizione facoltativa. Fai clic su **[!UICONTROL Salva e continua]**.
1. Nella fase _Seleziona potenziali_, seleziona i lead che devono appartenere a questo piano.
1. Nella fase _Definisci cadenza_, imposta i parametri per il piano.
1. Nella fase _Anteprima_, assicurati che tutto funzioni come previsto.

## Posta in uscita e-mail

Nel pannello Posta in uscita e-mail sono elencate tutte le e-mail automatizzate inviate.

## Prenotazioni riunioni

Questo pannello visualizza tutte le riunioni impostate tramite l&#39;automazione.

## Casella in entrata chat

Questo pannello visualizza tutti i thread di chat.

![Posta in arrivo chat](assets/chat-inbox.png)

È possibile interagire con i client e visualizzare i riepiloghi del contatto e del thread in modo da poter individuare rapidamente la posizione in cui si trova il thread.

## Integrazioni

Con le integrazioni, il Qualificatore di vendita può sfruttare i CRM e altre origini dati per arricchire i profili dei clienti e attingere alle attività di vendita:

* Integra con la tua casella di posta in arrivo per tenere traccia delle e-mail in arrivo rilevanti e contribuire a generare le risposte.
* Leggi e aggiorna i dati CRM, ad esempio Salesforce o Microsoft® Dynamics, ZoomInfo o Buildwidth.

![Qualificatore vendite per l&#39;integrazione Outlook](assets/outlook.png)

### Configurare una nuova integrazione

Per avviare una nuova integrazione, fai clic su **[!UICONTROL Crea integrazione]** in alto a destra.

![Dettagli integrazione](assets/integration-details.png)

Definisci l’URL dell’integrazione e stabilisci il payload da inviare:

1. Fornisci un nome univoco e una descrizione (facoltativa) per l’integrazione.
1. Imposta il campo URL sull’endpoint di autenticazione dell’integrazione del sito di integrazione.
1. In Parametri percorso impostare il metodo HTTP.
1. In Parametri intestazione, imposta le intestazioni HTTP da inviare. In genere, si tratta di un oggetto JSON inviato e richiede un’intestazione content-type.
1. In Parametri query, stabilisci tutti i parametri richiesti.
1. In Autenticazione, imposta le informazioni di accesso per il sito di integrazione.

   * Nessuna
   * OAuth 2.0
   * Chiave API
   * Autenticazione di base

1. Impostare i valori di limitazione e cache nella sezione **[!UICONTROL Configurazione payload]**.
   * Fai clic sull’icona della matita.
   * Nella finestra di dialogo _Incolla payload_, incolla o immetti l&#39;oggetto payload JSON.

      * **[!UICONTROL Payload della richiesta]** - Oggetto JSON contenente dati da inviare al sito di integrazione.
      * **[!UICONTROL Payload di risposta]** - Struttura di dati che si prevede venga restituita.

1. Fai clic su **[!UICONTROL Verifica connessione]** per verificare che le impostazioni siano corrette.

Quando le impostazioni di connessione sono valide, fare clic su **[!UICONTROL Salva come bozza]**.

Quando ritorni alla tabella principale _[!UICONTROL Integrazioni]_, seleziona l&#39;integrazione e fai clic su **[!UICONTROL Attiva]** per rendere attiva l&#39;integrazione. Se non sei pronto ad attivarlo, fai clic su **[!UICONTROL Salva come bozza]**.

#### Gestisci accesso

Puoi gestire l’accesso agli utenti e il tipo di dati condivisi con diversi gruppi di utenti.

Fai clic su **[!UICONTROL Gestisci accesso]** per aprire la finestra di dialogo _[!UICONTROL Gestisci accesso]_.

Questa finestra di dialogo elenca tutte le etichette stabilite per la tua organizzazione. Seleziona le etichette da applicare a questa integrazione.

Se hai bisogno di una nuova etichetta, fai clic su **[!UICONTROL Crea etichetta]** e immetti le informazioni dell&#39;etichetta:

* Nome
* Nome intuitivo
* Descrizione

## Impostazioni rappresentative

Le impostazioni del rappresentante specificano informazioni su di te, tra cui dati personali, impostazioni di e-mail e calendario e disponibilità della chat.

### Dettagli

Nella scheda **[!UICONTROL Dettagli]** è possibile immettere informazioni personali:

![Impostazioni dettagli qualificatore vendite](assets/details.png)

### Impostazioni e-mail

Nella scheda **[!UICONTROL Impostazioni e-mail]**, configura le connessioni e-mail.

![Impostazioni e-mail](assets/email-settings.png)

* **[!UICONTROL Connessioni e-mail]** - Fare clic su **[!UICONTROL Connetti]** e seguire la procedura di accesso di Microsoft.

* **[!UICONTROL Firma e-mail]** - Configura la firma e-mail utilizzata nelle e-mail generate automaticamente.

### Impostazioni calendario

Nella scheda **[!UICONTROL Impostazioni calendario]**, imposta il tuo fuso orario e la tua disponibilità.

![Impostazioni calendario](assets/calendar-settings.png)

* **[!UICONTROL Connessione calendario]** - Fare clic su **[!UICONTROL Connetti]** e seguire la procedura di accesso di Microsoft per integrare il calendario.

* **[!UICONTROL E-mail di conferma riunione]** - Quando un cliente conferma una riunione con te, riceve l&#39;e-mail di conferma come risposta. Utilizza queste impostazioni per definire l’oggetto e il corpo dell’e-mail.

* **[!UICONTROL Preferenze]** - Imposta la durata predefinita della riunione e l&#39;intervallo di tempo che desideri tra le riunioni back-to-back.

### Impostazioni chat

Nella scheda **[!UICONTROL Impostazioni chat]**, imposta la disponibilità della chat in tempo reale.

![Impostazioni chat](assets/chat-settings.png)

## Gestione dei rappresentanti

Il pannello _[!UICONTROL Gestione rappresentanti]_ visualizza i rappresentanti definiti e il relativo stato del calendario.

## Prestazioni riunione

Questo pannello presenta le analisi relative alle riunioni completate.

## Configurare il plug-in Chrome

Il plug-in Chrome dell&#39;Assistente di intelligenza artificiale è disponibile in [Google Store](https://chromewebstore.google.com/detail/ai-assistant/hancbabllcmckehonngbdkhilocpdfji?authuser=0&hl=en).

Quando il plug-in viene installato in Chrome, il logo Adobe viene visualizzato nel mezzo a destra quando ti trovi su un sito integrato:

* Applicazioni web Adobe
* Salesforce
* Outlook
* Microsoft Dynamics e applicazioni web
* Applicazioni Google

## Modifica la barra di navigazione a sinistra

Nella parte inferiore sinistra dell&#39;applicazione, fare clic su **[!UICONTROL Modifica]** per controllare quale delle icone è visibile nell&#39;area di navigazione. Puoi anche trascinarli e rilasciarli per riordinarli come desideri.

## Video dimostrativo

Il video seguente offre una breve dimostrazione dei Sales Qualifier e di Account Qualification Agent.

>[!VIDEO](https://video.tv.adobe.com/v/3476569?captions=ita)
