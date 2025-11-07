---
title: Qualificatore di vendita
description: Scopri come utilizzare l’applicazione Qualificatore di vendita per accelerare e gestire i percorsi.
feature: Account Journeys, AI Assistant
role: User
source-git-commit: 8fb86fe3434a5acdec6fd638fad571a0bc901884
workflow-type: tm+mt
source-wordcount: '1316'
ht-degree: 1%

---


# Qualificatore di vendita

>[!NOTE]
>Questa funzione è attualmente a disponibilità limitata e non è disponibile per tutti gli utenti.
>

Sales Qualifier è un&#39;applicazione aggiuntiva basata sull&#39;intelligenza artificiale per Adobe Journey Optimizer B2B edition che contiene il Account Qualification Agent ed è progettata per semplificare i flussi di lavoro per i rappresentanti di sviluppo aziendale (BDR, Business Development Representative). Il qualificatore di vendita automatizza i flussi di lavoro di qualificazione dei potenziali clienti, coinvolgimento degli acquirenti e coinvolgimento degli acquirenti su tutti i canali, riducendo il carico BDR manuale e accelerando la velocità della pipeline per le aziende B2B aziendali.
Utilizza il browser e i plug-in e-mail per accedere alle informazioni aziendali direttamente in CRM o Outlook.

Il qualificatore di vendita è incluso in AJO B2B ma è un’app separata all’interno di AEP Experience Cloud.

![Home page Qualificatore vendite](assets/home-screen.png)

## Agente Account Qualification

Il Account Qualification Agent (AQA) è il cuore del qualificatore di vendita. L’AQA utilizza l’intelligenza artificiale per leggere gli account e determinare quali sono pronti per il passaggio successivo.  Aiuta con la ricerca, la redazione delle e-mail e gli aggiornamenti del sistema CRM.

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

* Mostra i lead a cui sono stato assegnato senza alcun coinvolgimento
* Mostrami tutti i miei contatti che non fanno parte di alcun impegno autonomo
* Riepilogo dettagliato su `<company>`, incluso il gruppo di acquisto, i segnali di intenti recenti e il nostro impegno passato.

Puoi capire immediatamente quali account e lead sono più attivi e mostrano le intenzioni più elevate, in modo da concentrare la tua energia dove ha il maggior impatto.

Eseguire un&#39;iterazione nel percorso perfezionando le richieste per ottenere i risultati desiderati. Ad esempio:

* Crea un disegno e-mail di follow-up dal contesto, ad esempio chiamate o rapporti sui guadagni. Fino a 120 parole. Oggetto: Captivazione, con un tema chiave. Introduzione: hook con una citazione diretta da origini di contesto. Corpo: connettiti ai punti critici e alle proposte di valore. CTA: propone una breve chiamata per approfondire l’analisi.

* L’obiettivo di questa e-mail è quello di avviare una conversazione e rafforzare la credibilità. Redigi un&#39;e-mail sotto 120 parole con un tono consultivo ed empatico. Assicurati di evitare un approccio troppo familiare o di vendita e non utilizzare le frasi &quot;spera di stare bene&quot;, &quot;solo il check-in&quot; o &quot;per favore&quot;.

## Potenziali clienti

Questa finestra elenca tutti i lead a cui hai accesso. Controlla rapidamente elementi quali lo stato del lead e l’ultima attività.

![Visualizza tutti i lead nella tabella Lead](assets/prospects.png)

Fai clic sull&#39;icona Filtro ![icona Filtro](../assets/icon-filter.png) per filtrare in base allo stato del lead.

## Piani di coinvolgimento

Questa finestra fornisce dettagli su qualsiasi piano di coinvolgimento definito.

![Piani di coinvolgimento](assets/engagement-plans.png)

Per creare un nuovo piano di coinvolgimento, fare clic su **[!UICONTROL Crea piano di coinvolgimento]**.

1. Nella fase Dettagli, fornisci un nome e una descrizione facoltativa. Fai clic su **[!UICONTROL Salva e continua]**.
1. Nella fase Seleziona potenziali clienti selezionare i lead che devono appartenere a questo piano.
1. Nella fase Definisci cadenza, impostare i parametri per il piano.
1. Nella fase di anteprima, assicurati che tutto funzioni come previsto.

## Posta in uscita e-mail

Nel pannello Posta in uscita e-mail sono elencate tutte le e-mail automatizzate inviate.

## Prenotazioni riunioni

Questo pannello visualizza tutte le riunioni impostate tramite l&#39;automazione.

## Casella in entrata chat

Questo pannello visualizza tutti i thread di chat.

![Posta in arrivo chat](assets/chat-inbox.png)

Oltre a poter interagire con i client, puoi anche visualizzare un riepilogo del contatto e un riepilogo del thread, in modo da poter sapere rapidamente dove ti trovi nel thread.

## Integrazioni

Con le integrazioni, il Qualificatore di vendita può sfruttare i CRM e altre origini dati per arricchire i profili dei clienti e attingere alle attività di vendita:

* Integra con la tua casella di posta in arrivo per tenere traccia delle e-mail in arrivo rilevanti e contribuire a generare le risposte.
* Leggi e aggiorna i dati CRM, ad esempio Salesforce o Microsoft® Dynamics, ZoomInfo o Buildwidth.

![Qualificatore vendite per l&#39;integrazione Outlook](assets/outlook.png)

### Configurare una nuova integrazione

Per avviare una nuova integrazione, fai clic su **[!UICONTROL Crea integrazione]** in alto a destra.

![Dettagli integrazione](assets/integration-details.png)

Qui definiamo l’URL dell’integrazione e stabiliamo il payload da inviare.

1. Fornisci un nome univoco e una descrizione (facoltativa) per l’integrazione.
1. Imposta il campo URL sull’endpoint di autenticazione dell’integrazione del sito di integrazione.
1. In Parametri percorso impostare il metodo HTTP.
1. In Parametri intestazione, imposta le intestazioni HTTP da inviare. In genere, un oggetto JSON inviato e che richiede un’intestazione content-type.
1. In Parametri query, stabilisci tutti i parametri richiesti.
1. In Autenticazione, imposta le informazioni di accesso per il sito di integrazione.

   * Nessuna
   * OAuth 2.0
   * Chiave API
   * Autenticazione di base

1. Imposta i valori di limitazione e cache nella sezione di configurazione del payload.
1. In Configurazione payload, fai clic sull’icona della matita. Nella finestra di dialogo Incolla payload, incolla o immetti l’oggetto payload JSON.
   * Richiedi payload : Oggetto JSON contenente i dati per inviare il sito di integrazione.
   * Payload di risposta: la struttura dati che si prevede di ottenere in cambio.
1. Fai clic su [!UICONTROL Verifica connessione] per verificare che le impostazioni siano corrette.

Quando le impostazioni di connessione sono valide, fare clic su **[!UICONTROL Salva come bozza]**.

Quando sei di nuovo nella tabella delle integrazioni principali, seleziona l&#39;integrazione e fai clic su **[!UICONTROL Attiva]** per rendere attiva l&#39;integrazione oppure su **[!UICONTROL Salva come bozza]**.



#### Gestisci accesso

Puoi gestire l’accesso agli utenti e il tipo di dati condivisi con i diversi gruppi di utenti.

Fai clic su **[!UICONTROL Gestisci accesso]** per aprire la finestra di dialogo Gestisci accesso.

Questa finestra di dialogo elenca tutte le etichette stabilite dall’organizzazione. Seleziona le etichette da applicare a questa integrazione.

Se hai bisogno di una nuova etichetta, fai clic su **[!UICONTROL Crea etichetta]** e compila:

* Nome
* Nome intuitivo
* Descrizione

## Impostazioni rappresentative

Qui puoi immettere informazioni su di te: dati personali, impostazioni di e-mail e calendario e disponibilità della chat.

### Dettagli

Nella scheda Dettagli è possibile inserire informazioni personali:

![Impostazioni dettagli qualificatore vendite](assets/details.png)

### Impostazioni e-mail

Nella scheda Impostazioni e-mail, imposta le connessioni e-mail.

![Impostazioni e-mail](assets/email-settings.png)

#### Connessioni e-mail

Fai clic su **[!UICONTROL Connetti]** e segui la procedura di accesso di Microsoft.

#### Firma e-mail

Configura la firma e-mail utilizzata nelle e-mail generate automaticamente.

### Impostazioni calendario

Nella scheda Impostazioni calendario, imposta il tuo fuso orario e la disponibilità.

![Impostazioni calendario](assets/calendar-settings.png)

#### Connessione calendario

Fai clic su **[!UICONTROL Connetti]** e segui la procedura di accesso a Microsoft per integrare il calendario.

#### Email di conferma riunione

Quando un cliente conferma una riunione con te, riceve l’e-mail di conferma come risposta.
Utilizza queste impostazioni per definire l’oggetto e il corpo dell’e-mail.

#### Preferenze

Impostare la durata predefinita della riunione e l&#39;ora desiderata tra le riunioni back-to-back.

### Impostazioni chat

In questa scheda, imposta la disponibilità della chat live del fuso orario.

![Impostazioni chat](assets/chat-settings.png)

## Gestione dei rappresentanti

In questo pannello viene visualizzata una tabella di tutti i rappresentanti definiti e del relativo stato del calendario.

## Prestazioni riunione

Questo pannello presenta le analisi relative alle riunioni completate.

## Configurazione del plug-in Chrome

Il plug-in Chrome dell&#39;Assistente di intelligenza artificiale è disponibile in [Google Store](https://chromewebstore.google.com/detail/ai-assistant/hancbabllcmckehonngbdkhilocpdfji?authuser=0&hl=en).

Quando il plug-in viene installato in Chrome, il logo Adobe viene visualizzato nel mezzo a destra quando ti trovi su un sito integrato:

* Applicazioni web Adobe
* Salesforce
* Outlook
* Microsoft Dynamics e applicazioni web
* Applicazioni Google

## Modifica barra di navigazione a sinistra

Nella parte inferiore sinistra dell&#39;applicazione, fare clic su **[!UICONTROL Modifica]** per controllare quale delle icone è visibile nell&#39;area di navigazione. Puoi anche trascinarli e rilasciarli per riordinarli come desideri.

## Video dimostrativo

Il video seguente offre una breve dimostrazione dei Sales Qualifier e di Account Qualification Agent.

>[!VIDEO](https://video.tv.adobe.com/v/3476550)
