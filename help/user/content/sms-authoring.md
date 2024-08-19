---
title: Authoring di SMS
description: Scopri come inviare messaggi di testo (SMS) ai clienti sui loro dispositivi mobili e come personalizzare e visualizzare in anteprima i messaggi in formato testo dall’editor SMS.
feature: SMS Authoring, Content
exl-id: bd648253-74de-4083-a37a-ab7ceaea2746
source-git-commit: eea4afcf352eeefbd5a67c4bfff6a4c2ec559319
workflow-type: tm+mt
source-wordcount: '1908'
ht-degree: 1%

---

# Authoring di SMS

Utilizza Adobe Journey Optimizer B2B Edition per inviare messaggi di testo (SMS) ai clienti sui loro dispositivi mobili. Puoi creare, personalizzare e visualizzare in anteprima i messaggi in formato testo dall’editor SMS.

## Configurazioni SMS

Adobe Journey Optimizer B2B Edition invia messaggi di testo tramite provider di servizi SMS (o provider di gateway SMS). Prima di creare il messaggio SMS, configura il provider di servizi dalle impostazioni _Amministratore_.

### Provider del servizio gateway SMS

Adobe Journey Optimizer B2B Edition si integra attualmente con provider di terze parti che offrono servizi di messaggistica di testo in modo indipendente. I provider supportati per i messaggi di testo sono Sinch, Twilio e Infobip.

Prima di configurare un canale SMS in Adobe Journey Optimizer B2B Edition, è necessario creare un account con uno di questi provider per ottenere il token API e l’ID servizio. Queste credenziali sono necessarie per configurare la connessione tra Adobe Journey Optimizer B2B Edition e il provider applicabile.

>[!IMPORTANT]
>
>L’utilizzo dei servizi di messaggistica di testo è soggetto a termini e condizioni aggiuntivi da parte del provider applicabile. In qualità di soluzioni di terze parti, Sinch, Twilio e Infobip sono disponibili per gli utenti di Adobe Journey Optimizer B2B Edition tramite un’integrazione. Adobe non controlla e non è responsabile per i prodotti di terze parti. Per eventuali problemi o richieste di assistenza relativi ai servizi di messaggistica di testo (SMS), contatta il provider.

### Verifica una configurazione API SMS esistente

>[!NOTE]
>
>Le impostazioni descritte sono accessibili solo agli utenti con privilegi di amministratore SMS.

Nella barra di navigazione a sinistra, espandere la sezione **[!UICONTROL Amministratore]** e fare clic su **[!UICONTROL Configurazione]**.

![Accedere alla configurazione delle credenziali API di AMA](./assets/config-sms-api.png){width="800" zoomable="yes"}

Nella pagina sono elencate le configurazioni API disponibili per l’istanza. Puoi filtrare le credenziali API visualizzate in base al provider di servizi SMS o al creatore.

![Fare clic sull&#39;icona del filtro per filtrare l&#39;elenco delle credenziali API](./assets/config-sms-api-filter.png){width="500"}

### Creare nuove credenziali API per un provider di servizi SMS

>[!BEGINTABS]

>[!TAB Sinch]

_Per configurare Sinch come provider SMS con Adobe Journey Optimizer B2B Edition:_

1. Nella barra di navigazione a sinistra, espandere la sezione **[!UICONTROL Amministratore]** e fare clic su **[!UICONTROL Configurazione]**.

1. Fai clic su **[!UICONTROL Crea nuove credenziali API]** in alto a destra nell&#39;elenco delle _[!UICONTROL credenziali API]_.

1. Configura le credenziali API SMS:

   ![Configurare le credenziali API di Sinch SMS](./assets/config-sms-api-sinch.png){width="500"}

   * **[!UICONTROL Fornitore SMS]** - Scegliere `Sinch` come provider SMS.

   * **[!UICONTROL Nome]** - Immettere un nome per le credenziali API.

   * **[!UICONTROL ID servizio]** e **[!UICONTROL Token API]** - Accedi alla pagina API dal tuo account Sinch (puoi trovare le tue credenziali nella scheda SMS).

   Per ulteriori informazioni su come trovare queste informazioni per il tuo account Sinch, consulta la [documentazione per gli sviluppatori di Sinch](https://developers.sinch.com/docs/sms/getting-started/#2-get-credentials)

1. Fai clic su **[!UICONTROL Invia]** una volta completati i dettagli di configurazione delle credenziali API.

>[!TAB Twilio]

_Per configurare Twilio come provider SMS con Adobe Journey Optimizer B2B Edition:_

1. Nella barra di navigazione a sinistra, espandere la sezione **[!UICONTROL Amministratore]** e fare clic su **[!UICONTROL Configurazione]**.

1. Fai clic su **[!UICONTROL Crea nuove credenziali API]** in alto a destra nell&#39;elenco delle _[!UICONTROL credenziali API]_.

1. Configura le credenziali API SMS:

   ![Configurare le credenziali API SMS Twilio](./assets/config-sms-api-twilio.png){width="500"}

   * **[!UICONTROL Fornitore SMS]** - Scegliere `Twilio` come provider SMS.

   * **[!UICONTROL Nome]** - Immettere un nome per la definizione delle credenziali API.

   * **[!UICONTROL SID account]** e **[!UICONTROL Token autenticazione]**. Per trovare le credenziali, accedi al riquadro _Informazioni account_ della pagina del dashboard di Twilio Console.

   Per ulteriori informazioni su come trovare queste informazioni per l&#39;account Twilio, visitare il [Centro assistenza Twilio](https://help.twilio.com/articles/14726256820123-What-is-a-Twilio-Account-SID-and-where-can-I-find-it-).

1. Fai clic su **[!UICONTROL Invia]** in alto a destra della pagina al completamento dei dettagli di configurazione delle credenziali API.

>[!TAB Informazioni]

_Per configurare Infobip come provider SMS con Adobe Journey Optimizer B2B Edition:_

1. Nella barra di navigazione a sinistra, espandere la sezione **[!UICONTROL Amministratore]** e fare clic su **[!UICONTROL Configurazione]**.

1. Fai clic su **[!UICONTROL Crea nuove credenziali API]** in alto a destra nell&#39;elenco delle _[!UICONTROL credenziali API]_.

1. Configura le credenziali API SMS:

   ![Configurare le credenziali API di Infobip SMS](./assets/config-sms-api-infobip.png){width="500"}

   * **[!UICONTROL Fornitore SMS]** - Scegliere `Infobip` come provider SMS.

   * **[!UICONTROL Nome]** - Immettere un nome per la definizione delle credenziali API.

   * **[!UICONTROL URL di base API]** e **[!UICONTROL chiave API]**. Per trovare le credenziali, accedere alla home page dell&#39;interfaccia Web o alla pagina di gestione delle chiavi API per l&#39;account Infobip.

   Per ulteriori informazioni su come trovare queste informazioni per l&#39;account Infobip, vedere la [documentazione di Infobip](https://www.infobip.com/docs/api/_blank).

1. Fai clic su **[!UICONTROL Invia]** in alto a destra della pagina al completamento dei dettagli di configurazione delle credenziali API.

>[!ENDTABS]

Quando fai clic su _[!UICONTROL Invia]_, le credenziali vengono immediatamente convalidate e salvate, reindirizzandoti alla pagina dell&#39;elenco delle _[!UICONTROL credenziali API]_. Se le credenziali inviate non sono valide, il sistema visualizza un messaggio di errore nella pagina dell&#39;elenco. In questo caso, puoi scegliere di annullare la configurazione o di aggiornarla e inviarla nuovamente.

## Aggiungere un’azione SMS in un percorso di account

Puoi impostare le consegne di messaggi di testo in un Percorso di account quando aggiungi un nodo _[!UICONTROL Esegui un&#39;azione]_ ed effettua le seguenti operazioni:

1. Per l&#39;azione _[!UICONTROL sulla destinazione]_, scegliere **[!UICONTROL Persone]**.

1. Per l&#39;_[!UICONTROL azione sulle persone]_, scegli **[!UICONTROL Invia SMS]**.

   ![Esegui un&#39;azione - Invia SMS](assets/journey-node-send-sms.png){width="800" zoomable="yes"}

1. Nella parte inferiore del pannello _[!UICONTROL Esegui un&#39;azione]_, fai clic su **[!UICONTROL Crea SMS]**.

1. Nella finestra di dialogo, immetti un **[!UICONTROL Nome]** univoco per l&#39;e-mail e una **[!UICONTROL riga Oggetto]**.

   ![Crea nuova finestra di dialogo SMS](assets/create-new-sms.png){width="500"}

## Creare il messaggio SMS

>[!IMPORTANT]
>
>**Gestione del consenso SMS**<br/>
><br/>
>In conformità agli standard e alle normative del settore, tutti i messaggi SMS di marketing devono consentire ai destinatari di annullare facilmente l’iscrizione alla ricezione di messaggi. A questo scopo, i destinatari di SMS possono rispondere con parole chiave di consenso e rinuncia. Tutte le parole chiave di consenso e rinuncia standard sono supportate e rispettate. Sono inoltre supportate e rispettate tutte le parole chiave personalizzate configurate per l’account del provider di servizi SMS.

1. Immetti il testo da inviare nel campo **[!UICONTROL Messaggio]**.

   Puoi creare un messaggio composto da un massimo di 1600 caratteri, ogni 160 caratteri vengono considerati come un singolo messaggio SMS.

1. **Personalizzare il messaggio di testo**.

   In qualsiasi momento durante la creazione del messaggio di testo, fai clic sull&#39;icona _Personalizza_ a destra della casella del messaggio di testo.

   ![Fai clic sull&#39;icona Personalizza per aggiungere token al messaggio](./assets/sms-message-personalize-icon.png){width="800" zoomable="yes"}

   La pagina visualizzata consente di accedere ai token di Adobe Marketo Engage Lead e System. Sono inclusi sia i token standard che quelli personalizzati. È possibile utilizzare la barra di ricerca per individuare il token desiderato oppure spostarsi nella struttura delle cartelle per trovare e selezionare uno dei token di sistema/lead.

   Posiziona il cursore nel punto del messaggio in cui desideri aggiungere il token. Aggiungere un token facendo clic sul simbolo più ( **+** ) accanto a esso. Se desideri aggiungere il token con un fallback (impostazione predefinita che viene visualizzata se il campo non è disponibile per un lead), fai clic sui puntini di sospensione ( **...** ) e scegli **[!UICONTROL Inserisci con testo di fallback]**.

   ![Fare clic sui puntini di sospensione per utilizzare un fallback per il token](./assets/sms-message-personalize-ellipsis-fallback.png){width="700" zoomable="yes"}

   Nella finestra di dialogo _[!UICONTROL Immetti valore di fallback]_, immetti il testo che viene visualizzato come fallback, quindi fai clic su **[!UICONTROL Aggiungi]**.

   ![Immettere il testo di fallback per il token](./assets/sms-message-personalize-fallback-text.png){width="400"}

   Una volta inseriti i token di personalizzazione, fai clic su **[!UICONTROL Salva]** per salvare le modifiche e tornare all&#39;area di lavoro di authoring SMS principale. Puoi continuare a modificare il messaggio con i token, in base alle esigenze.

1. **Aggiungi URL al messaggio di testo**.

   Dopo aver definito il contenuto, puoi aggiungere URL al messaggio facendo clic sull&#39;icona del _collegamento_.

   Questa azione apre una finestra di dialogo in cui puoi scegliere uno dei due tipi di URL da collegare:

   * **[!UICONTROL URL esterno]** - Questo tipo è qualsiasi URL esterno immesso nella casella di testo.
   * **[!UICONTROL Pagina di destinazione]** - Scegliere questa opzione per selezionare dall&#39;istanza di Marketo Engage una delle pagine di destinazione approvate di Adobe Marketo Engage Design Studio.

   La finestra di dialogo include anche le opzioni per i collegamenti URL:

   * **[!UICONTROL Abbrevia URL]** - Selezionare questa casella di controllo per _abbreviare_ l&#39;URL, necessario per il tracciamento. Per una pagina di destinazione, utilizza il sottodominio Marketo Engage per l’URL abbreviato. Viene visualizzato un esempio del formato URL abbreviato. L’URL effettivo viene creato quando l’SMS viene inviato al destinatario.

   * **[!UICONTROL Includi mkt_tok]** - Seleziona questa casella di controllo per tenere traccia dell&#39;attività rispetto a un utente.

   Una volta completate le opzioni di collegamento, fai clic su **[!UICONTROL Aggiungi]** per salvare le modifiche e aggiungere il collegamento URL al messaggio SMS.

## Impostare le proprietà di SMS

1. Nella sezione _[!UICONTROL Proprietà SMS]_, immetti un **[!UICONTROL Nome]** (obbligatorio, massimo 100 caratteri) e una **[!UICONTROL Descrizione]** (facoltativo, massimo 300 caratteri) per il messaggio.

   Ad Alpha, per questi campi sono consentiti caratteri numerici e speciali. I seguenti caratteri riservati sono **non consentiti**: `\`, `/`, `:`, `*`, `?`, `"`, `<`, `>` e `|`.

1. Scegli il tipo di SMS ****:

   * Utilizza `Marketing` per i messaggi di testo promozionali, che richiedono il consenso dell&#39;utente.
   * Utilizzare `Transactional` per i messaggi non commerciali, ad esempio la conferma di un ordine, le notifiche di reimpostazione della password o le informazioni di consegna.

1. Per la **[!UICONTROL configurazione SMS]**, scegli una delle configurazioni API predefinite.

   Questa impostazione determina il provider del servizio gateway SMS e l’account utilizzati per recapitare il messaggio.

1. Immettere il **[!UICONTROL numero mittente]** &#x200B;che si desidera utilizzare per le comunicazioni.

   ![Esegui un&#39;azione - Invia SMS](./assets/sms-properties.png){width="700" zoomable="yes"}

   Il numero del destinatario è sempre mappato al campo `Lead.mobilePhone` nel Marketo Engage.

## Simulare il contenuto del messaggio di testo {#preview-test}

>[!CONTEXTUALHELP]
>id="ajo-b2b_sms_preview_simulate"
>title="Controlla come viene eseguito il rendering del contenuto"
>abstract="Una volta definito il contenuto, puoi visualizzarne l’anteprima e verificare se il rendering è corretto per il canale in uso."

Una volta definito il contenuto del messaggio, puoi utilizzare i profili di test per simulare (visualizzare in anteprima) il contenuto. Se hai inserito dei contenuti personalizzati, puoi verificare come questi contenuti vengono visualizzati nel messaggio utilizzando i dati del profilo di test.

>[!IMPORTANT]
>
>Assicurati di salvare il messaggio SMS prima di procedere con la simulazione.

1. Fai clic su **[!UICONTROL Simula contenuto]** nella parte superiore dell&#39;area di lavoro di authoring SMS.

1. Dalla pagina _[!UICONTROL Simula contenuto]_, fare clic su **[!UICONTROL Aggiungi persone]**.

1. Utilizza la pagina _Simula contenuto_ per gestire i lead utilizzati per il tuo profilo di test.

   Nell&#39;elenco visualizzato è possibile cercare e aggiungere qualsiasi lead (fino a 10 lead alla volta) dal database dei lead di Marketo Engage.

   Per eseguire la ricerca, immettere l&#39;intero indirizzo di posta elettronica e premere _Invio_. Viene visualizzato il profilo di lead corrispondente per la selezione.

   L’anteprima viene aggiornata ai campi di personalizzazione per il profilo selezionato.

   Tutti i lead aggiunti vengono visualizzati a sinistra.

   Puoi gestire questo elenco aggiungendo più persone ed eliminando singoli lead dall’elenco dei profili (non li rimuove dal database).

1. Simula contenuto per un lead selezionato.

   Seleziona uno dei lead elencati a sinistra e l’anteprima SMS nella pagina aggiorna il lead corrispondente.

   Puoi anche selezionare un lead dal selettore sopra lo spazio di anteprima per aggiornare l’anteprima SMS sulla pagina per il lead corrispondente.

1. Per uscire dalla pagina _[!UICONTROL Simula contenuto]_ e tornare all&#39;area di lavoro di creazione SMS, fai clic su **[!UICONTROL Chiudi]** in alto a destra.

## Gestione del consenso SMS

Come requisito legale, è necessario dare ai destinatari la possibilità di annullare l’abbonamento alla ricezione di comunicazioni da un marchio e rispettare questa scelta. Il mancato rispetto di queste normative comporta rischi legali per il tuo marchio. Questa funzione ti aiuta anche a evitare l’invio di comunicazioni non richieste ai destinatari, che potrebbero essere contrassegnate come spam e danneggiare la tua reputazione.

Quando fornisci questa opzione, i destinatari di SMS possono rispondere con parole chiave di consenso e rinuncia. Sono supportate e rispettate tutte le parole chiave standard di consenso e rinuncia, nonché tutte le parole chiave personalizzate configurate nel provider di servizi SMS. Quando l’abbonamento viene annullato, i profili vengono rimossi automaticamente dal pubblico dei messaggi di marketing futuri.

Journey Optimizer B2B Edition consente di gestire la rinuncia nei messaggi SMS utilizzando la seguente logica:

* Per impostazione predefinita, se un lead ha rinunciato a ricevere comunicazioni dall’utente, il profilo corrispondente viene escluso dalle consegne SMS successive

* Questo consenso lead proveniente da origini diverse (ad esempio AEP o il provider di servizi SMS) viene sincronizzato con Journey Optimizer B2B Edition. Attualmente, supporta solo un singolo stato di consenso per lead a livello di istanza (un lead &quot;John Doe&quot; è abbonato o annullato da tutti gli SMS promozionali nell’istanza). Al momento non supporta il doppio consenso a livello di marchio/elenco di iscrizioni individuale.
