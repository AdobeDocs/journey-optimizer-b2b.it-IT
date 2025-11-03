---
title: Note sulla versione di Journey Optimizer B2B Edition
description: Scopri le funzioni, i miglioramenti e le correzioni di bug più recenti in Adobe Journey Optimizer B2B edition. Rimani aggiornato con nuove funzionalità e miglioramenti al prodotto.
role: User, Admin
exl-id: 7d3f1c26-d8a6-4065-a70f-5b30cb975dc8
source-git-commit: 74633474e8d0af1e976d007d75bf4db9906fe7d2
workflow-type: tm+mt
source-wordcount: '3644'
ht-degree: 81%

---

# Note sulla versione di Journey Optimizer B2B Edition

Adobe Journey Optimizer B2B Edition fornisce continuamente nuove funzioni, miglioramenti a quelle esistenti e correzioni di bug.

Journey Optimizer B2B Edition è costruito nativamente su [!DNL Adobe Experience Platform] e ne eredita le innovazioni e i miglioramenti più recenti. Ulteriori informazioni su queste modifiche sono disponibili nelle [note sulla versione di Adobe Experience Platform](https://experienceleague.adobe.com/it/docs/experience-platform/release-notes/latest){target="_blank"}.

Rivedi la [descrizione del prodotto](https://helpx.adobe.com/it/legal/product-descriptions/adobe-journey-optimizer-b2b.html){target="_blank"} per informazioni su diritti, guardrail delle prestazioni e limitazioni.

## Funzionalità di IA per l’agente

Nell’interfaccia di AI Assistant sono ora disponibili le seguenti funzionalità di IA per l’agente per Journey Optimizer B2B edition:

| Agente | Aggiornamento | Descrizione |
| ----- | ------ | ----------- |
| Creazione Agente Journey | Nuovo | L’agente di generazione del Percorso analizza, crea e crea congiuntamente percorsi in tempo reale, consentendo agli addetti al marketing di avviarsi più rapidamente, migliorare il coinvolgimento e aumentare i tassi di conversione. [Ulteriori informazioni](../agents/journey-agent.md) |
| Agente Audience | Nuovo | Audience Agent identifica e crea automaticamente i gruppi di acquisto utilizzando dati strutturati e non strutturati. Aiuta gli esperti di marketing a indirizzare le persone giuste in modo più rapido e preciso. [Ulteriori informazioni](../agents/audience-agent-b2b.md) |
| Account Qualification Agent | Nuovo | Scopri quali account sono pronti per la fase successiva utilizzando Account Qualification Agent nell’Assistente IA. Questo agente consente ai membri del team vendite di concentrarsi sugli account giusti presentando lead di alto valore e automatizzando i flussi di lavoro di qualificazione. [Ulteriori informazioni](../agents/account-qualification-agent.md) |

## Note sulla versione 2025.10

**Data di distribuzione**: sabato 31 ottobre 2025

| Tipo | Elemento | Descrizione |
| ---- | ---- | ----------- |
| Funzione | Modello dati relazionale | Sfrutta i dati relazionali collegati agli account B2B per filtrare gli account all’interno di un percorso di account o personalizzare il contenuto delle e-mail. Questi dati relazionali possono rappresentare entità aziendali reali come record di acquisto, registrazioni di eventi, licenze software, abbonamenti a servizi o prenotazioni. |
| Funzione | Attiva nella destinazione per percorsi | Utilizza la nuova azione _Attiva per l&#39;account aziendale_ per eseguire l&#39;attivazione direttamente alle aziende, anziché ai singoli utenti. (Limitato alle società LinkedIn per questa versione). |
| Funzione | Attivazione di più Marketo Engage | Configura le connessioni alle istanze Marketo Engage remote e utilizza tali connessioni per configurare le azioni Marketo Engage dai percorsi. Queste azioni, come l’aggiunta/rimozione di persone dagli elenchi o l’aggiunta di persone a una campagna di richieste, si applicano all’istanza di Marketo Engage designata. |
| Funzione | Temi del brand | Con i temi del brand, gli utenti non tecnici hanno ora la possibilità di creare contenuti riutilizzabili che si adattano a un marchio e a un linguaggio di progettazione specifici aggiungendo stili personalizzati sopra i modelli standard. [Ulteriori informazioni](../content/brand-themes.md) |
| Funzione | Modelli e-mail - Converti immagine in HTML | Ora puoi utilizzare i file di progettazione memorizzati come file di immagine JPG o PNG e generare automaticamente modelli e-mail. [Ulteriori informazioni](../content/email-template-image-convert.md) |
| Funzione | Mappatura utente tipo | Associa i membri dell’account con utenti tipo consolidati con il mapping degli attributi. [Ulteriori informazioni](../admin/persona-mapping.md) |
| Funzione | Informazioni sulle vendite per Salesforce e Dynamics | I membri del team vendite possono ora visualizzare i gruppi di acquisto in scadenza e le relative informazioni all’interno di un’integrazione Salesforce o Dynamics per identificare nuove opportunità. Sono inclusi i dettagli del gruppo di acquisto come fase, punteggio e membri correlati. |
| Miglioramento | Deduplicazione dell’eccesso di posta elettronica | Ora puoi abilitare la deduplicazione delle e-mail per garantire che la stessa e-mail non venga inviata più volte allo stesso indirizzo in un percorso. Gli indirizzi duplicati vengono bloccati finché il primo record con tale indirizzo e-mail non completa il percorso. |
| Miglioramento | Limiti di comunicazione | Il sistema ora rispetta i limiti di comunicazione combinati di Marketo Engage e Journey Optimizer B2B edition. |
| Miglioramento | Acquisto di processi di manutenzione del gruppo | La frequenza dei processi di manutenzione del gruppo di acquisto viene aggiornata da settimanale a giornaliera. |
| Miglioramento | Progressione del percorso account | Un collegamento _Ulteriori informazioni_ è visibile per la progressione del percorso per accedere ai conteggi e agli elenchi degli account. |

>[!NOTE]
>
>Queste modifiche iniziano la distribuzione il 31 ottobre 2025, con un rollout graduale di ciascuna funzione. Le date di rilascio di funzioni e miglioramenti sono soggette a modifiche.

### Architettura semplificata

Adobe Journey Optimizer B2B edition è ora disponibile utilizzando un’architettura semplificata. Con questa architettura aggiornata, Journey Optimizer B2B edition e Marketo Engage non si trovano più nello stesso sistema e nello stesso archivio dati. Journey Optimizer B2B edition riceve i dati solo da Adobe Experience Platform. Tuttavia, continua a fare affidamento su adesioni Marketo Engage e su alcune funzionalità di configurazione per il provisioning e la configurazione del sistema.

Questa architettura aggiornata offre diversi vantaggi:

* **Unifica e ridimensiona facilmente i dati**: la piattaforma aggiornata supporta modelli di dati complessi, inclusi oggetti personalizzati, gruppi di acquisto ed eventi dell&#39;account.
* **Connessione di più istanze di Adobe Marketo Engage**: gestione e unificazione dei dati da più ambienti Adobe Marketo Engage in un&#39;unica posizione.
* **Protezione dei dati**: le funzionalità avanzate di privacy e sicurezza consentono di proteggere le informazioni dei clienti.
* **Creato per il futuro**: questo aggiornamento imposta la tua organizzazione per continui miglioramenti e innovazioni.

<!-- hold for later release 

| Feature | Landing pages | You can now create and publish landing pages in Journey Optimizer B2B Edition to support your journeys and programs. _(Previously a Beta program feature.)_ [Learn more](../content/landing-pages.md) |
| Feature | Forms | You can now create and publish re-usable form components to enable data submission from landing pages that are created and published in Journey Optimizer B2B Edition. _(Previously a Beta program feature.)_ [Learn more](../content/forms.md) |

-->

## Note sulla versione 2025.9

**Data di distribuzione**: 30 settembre 2025

Questa versione include le seguenti nuove funzionalità e miglioramenti:

| Tipo | Elemento | Descrizione |
| ---- | ---- | ----------- |
| Funzione | Collaborazione sui contenuti delle e-mail | Ora puoi aggiungere commenti e collaborare con altri utenti di Journey Optimizer B2B Edition, nel contesto di una risorsa e-mail. Puoi menzionare i membri del gruppo in modo che ricevano una notifica e-mail con i dettagli del commento. La notifica è disponibile anche come notifica Pulse. [Ulteriori informazioni](../content/email-collaboration-tools.md) |
| Funzione | Modalità scura per la progettazione di e-mail | Lo spazio di progettazione delle e-mail ora include la possibilità di passare alla _modalità scura_. In modalità scura, puoi visualizzare in anteprima il contenuto dell’e-mail e definire impostazioni personalizzate da visualizzare in modo specifico per i destinatari che visualizzano le e-mail in modalità scura. [Ulteriori informazioni](../content/email-dark-mode.md) |
| Miglioramento | Percorsi - Dividere un percorso per numero di persone nel ruolo | Utilizza un percorso diviso per nodo di account per eseguire il targeting di un account con il numero di persone in uno o più ruoli del gruppo acquisti. Nel percorso puoi valutare la preparazione del gruppo acquisti per avvisi commerciali e altri tipi di coinvolgimento in base alla profondità del ruolo. [Ulteriori informazioni](../journeys/split-merge-paths-nodes.md#buying-group-filtering-for-accounts) |
| Miglioramento | Percorsi - Filtri persona per eventi | Utilizza i filtri persone per cogliere eventi relativi alle persone. Questi filtri includono la possibilità di eseguire il targeting per un ruolo specifico per un gruppo acquisti corrispondente. [Ulteriori informazioni](../journeys/listen-for-event-nodes.md#add-filters-to-the-people-event) |

>[!NOTE]
>
>Queste modifiche iniziano la distribuzione il 30 settembre 2025, con un rollout graduale di ciascuna funzione. Le date di rilascio di funzioni e miglioramenti sono soggette a modifiche.

## Note sulla versione 2025.8

**Data di distribuzione**: 26 agosto 2025

Questa versione include le seguenti nuove funzionalità e miglioramenti:

| Tipo | Elemento | Descrizione |
| ---- | ---- | ----------- |
| Funzione | Filtri del punteggio di coinvolgimento della persona per modelli di ruolo e percorsi | È ora possibile utilizzare il _Punteggio di coinvolgimento della persona_ come filtro nei modelli di Ruoli utilizzati per la creazione di gruppi acquisti e nei nodi di percorso con percorso suddiviso. [Ulteriori informazioni](../buying-groups/buying-groups-role-templates.md#add-the-template-roles) |
| Funzione | Configurazione dei ruoli personalizzati dei gruppi acquisti | Ora disponi della flessibilità di configurare ruoli personalizzati per i gruppi acquisti, per definire i ruoli specifici nei tuoi casi d’uso. [Ulteriori informazioni](../buying-groups/default-custom-roles.md) |
| Funzione | Configurazione della ponderazione del punteggio di coinvolgimento | Ora puoi assegnare pesi alle attività che influenzano il punteggio di coinvolgimento del gruppo acquisti. Questa funzione include la definizione di modelli di punteggio personalizzati e la modifica del modello attivo che influenza i calcoli del punteggio di coinvolgimento. [Ulteriori informazioni](../admin/engagement-score-weighting.md) |
| Miglioramento | Contenuto condizionale per frammenti | Ora puoi utilizzare gli strumenti del contenuto condizionale per la progettazione di frammenti visivi. [Ulteriori informazioni](../content/conditional-content.md) |
| Miglioramento | Aggiornamento del punteggio di coinvolgimento | La logica del punteggio di coinvolgimento del gruppo acquisti viene aggiornata per normalizzare i punteggi. Inoltre, puoi utilizzare i punteggi di coinvolgimento a livello di membro, nonché i punteggi di coinvolgimento collettivo per l’intero gruppo acquisti. [Ulteriori informazioni](../buying-groups/engagement-scores.md) |
| Miglioramento | Osservabilità attiva del percorso: account in ciascun nodo | Per un percorso di account attivo, puoi accedere a un elenco degli account che hanno raggiunto ciascun nodo account nel percorso. |

## Note sulla versione 2025.6

**Data di distribuzione**: 15 luglio 2025

Questa versione include le seguenti nuove funzionalità e miglioramenti:

| Tipo | Elemento | Descrizione |
| ---- | ---- | ----------- |
| Funzione | Integrazione con GenStudio for Performance Marketing | (Disponibilità limitata) Ora puoi integrare le esperienze e-mail di GenStudio for Performance Marketing con Journey Optimizer B2B Edition per migliorare l’efficienza del marketing e mantenere la coerenza del brand. Con questa integrazione, puoi combinare la creazione di contenuti basata sull’intelligenza artificiale di GenStudio con le funzionalità di orchestrazione avanzate di Journey Optimizer B2B Edition. [Ulteriori informazioni](../content/genstudio-email-workflow.md) |
| Funzione | Reporting sul rilevamento di spam | Per evitare i filtri anti-spam e assicurarti che i messaggi vengano recapitati alle caselle in entrata del pubblico, puoi generare un _rapporto spam_ direttamente nello spazio di progettazione delle e-mail. [Ulteriori informazioni](../content/email-spam-report.md) |
| Funzione | Pagina di dettagli sulle persone | Ora puoi fare clic sul nome di una persona visualizzato (come collegamento ipertestuale) nel Dashboard intelligente e nelle pagine dei dettagli del gruppo acquisti e  dell&#39;account. Questa azione apre la pagina dei dettagli della persona, con informazioni sul contatto, le sue attività e i gruppi acquisti più coinvolti. [Ulteriori informazioni](../accounts/person-details.md) |
| Funzione | Azioni per account e gruppi acquisti | Intraprendi azioni direttamente dalle pagine dei dettagli dell’account e del gruppo acquisti per un coinvolgimento puntuale e intenzionale. <li>Utilizza l’azione _Invia e-mail_ per inviare un’e-mail di Marketo Engage approvata ai contatti dell’account o ai membri del gruppo acquisti selezionati. [Ulteriori informazioni](../accounts/account-details.md#send-emails) <li>Dai dettagli del gruppo acquisti, le azioni includono anche _Assegna un nuovo membro_, _Rimuovi un membro_ e _Modifica un ruolo_. [Ulteriori informazioni](../buying-groups/buying-group-details.md#members-tab) |
| Funzione | Accesso dal CRM alle pagine dei dettagli | Ora puoi configurare collegamenti diretti alle pagine dei dettagli di Journey Optimizer B2B Edition per account, contatti e lead nel tuo strumento di gestione delle relazioni con i clienti (CRM), come Salesforce o Microsoft Dynamics. [Ulteriori informazioni](../accounts/crm-linking.md) |
| Funzione | Supporto per CSS personalizzati nella progettazione dei contenuti | Ora, nello spazio di progettazione, puoi aggiungere un CSS personalizzato durante l’authoring dei contenuti per e-mail e pagine di destinazione. [Ulteriori informazioni](../content/design-custom-css.md) |
| Funzione | Configurazione della mappatura delle parole chiave di intento | Per attivare e gestire il modello di rilevamento dell’intento, ora puoi caricare un foglio di calcolo per definire una categoria di mappatura dei dati intento. [Ulteriori informazioni](../admin/intent-data.md) |
| Miglioramento | Simulare il contenuto da riepilogo e-mail | È ora possibile accedere agli strumenti _Simula contenuto_ dal riepilogo dell’e-mail (dettagli e proprietà) quando viene aperto un messaggio dall’elenco E-mail. Questo si aggiunge alla possibilità di accedere a tali strumenti dallo spazio di progettazione delle e-mail. [Ulteriori informazioni](../content/email-simulate-content.md#display-the-email-preview) |
| Miglioramento | Visualizzazione del conteggio totale nell’elenco dei modelli di ruoli | La pagina dell’elenco _[!UICONTROL Modelli ruoli]_ è stata migliorata con la visualizzazione del conteggio totale accanto alla barra di ricerca. |

<!-- The following capabilities are currently available only for a set of program participants (Beta):

**Brand Kit with AI Assistant** - Maintain brand consistency across email assets by storing and managing brand assets. Add assets, such as colors, fonts, logos, themes, visual content, and compliance guidelines, and use them for your generative AI content creation. -->

## Note sulla versione 2025.5

**Data di distribuzione**: 3 giugno 2025

Questa versione include le seguenti nuove funzionalità e miglioramenti:

| Tipo | Elemento | Descrizione |
| ---- | ---- | ----------- |
| Funzione | Test delle e-mail con Litmus | Con un [account Litmus Enterprise](https://www.litmus.com/email-testing){target="_blank"}, ora puoi visualizzare in anteprima il rendering delle e-mail provenienti da Journey Optimizer B2B Edition nei client e-mail più diffusi. Questa integrazione ti consente di garantire che il contenuto delle e-mail si presenti in modo ottimale e funzioni come previsto in ogni casella in entrata dell’e-mail. [Ulteriori informazioni](../content/email-test-rendering.md) |
| Miglioramento | E-mail duplicata | Quando aggiungi un’e-mail per un nodo di percorso, ora puoi duplicare un’e-mail esistente. Modifica l’impostazione o il contenuto dell’e-mail duplicata oppure lasciala intatta.  [Ulteriori informazioni](../content/add-email.md#add-an-email-to-your-journey) |
| Miglioramento | Formato token Handlebar per e-mail | I token di personalizzazione per il contenuto delle e-mail ora utilizzano un formato aggiornato completamente compatibile con gli script Handlebar. Questo formato utilizza _camel case_ o trattini bassi, eliminando gli spazi. [Ulteriori informazioni](../content/email-authoring.md#content-authoring---personalization) |
| Miglioramento | Visualizzazione del conteggio totale per elenchi | Le pagine di elenco _[!UICONTROL Soluzioni di interesse]_ e _[!UICONTROL Percorsi account]_ sono state migliorate con la visualizzazione del conteggio totale accanto alla barra di ricerca. |

## Note sulla versione 2025.4

**Data di distribuzione**: 29 aprile 2025

Questa versione include le seguenti nuove funzionalità e miglioramenti:

| Tipo | Elemento | Descrizione |
| ---- | ---- | ----------- |
| Funzione | Elenchi account | Ora puoi creare un elenco account statico o dinamico per eseguire il targeting di account denominati in base a criteri definiti, ad esempio settore, posizione o dimensioni dell’azienda. <a href="../accounts/account-lists.md">Ulteriori informazioni</a> |
| Funzione | Orchestrazione dei percorsi dell’elenco account | Utilizza i nodi delle azioni di percorso per aggiungere e rimuovere account per gli elenchi di account statici. <a href="../accounts/account-lists-journeys.md#take-an-action-node---add-to-account">Ulteriori informazioni</a> |
| Miglioramento | Filtrare l’iscrizione al percorso in Marketo Engage | Utilizza gli elenchi account di Adobe Journey Optimizer B2B Edition per il pubblico del percorso, quindi utilizza il filtro _Membro di un elenco account_ negli elenchi avanzati di Marketo Engage. <a href="../accounts/account-lists-journeys.md#marketo-engage-program---member-of-account-list">Ulteriori informazioni</a> |
| Funzione | Filtri di inattività | Orchestra i percorsi in base all’inattività nelle campagne e nei programmi di Marketo Engage, inclusi inattività delle e-mail, momenti interessanti, modifiche al valore dei dati e pagine web visitate. <a href="../journeys/split-merge-paths-nodes.md#activity-filtering">Ulteriori informazioni</a> |
| Miglioramento | Filtro pagina web visitata | Orchestra i percorsi in base all’attività per le pagine web visitate associate a campagne e programmi di Marketo Engage. <a href="../journeys/split-merge-paths-nodes.md#people-path-filters">Ulteriori informazioni</a> |
| Miglioramento | Elenco di e-mail | Visualizza un elenco globale di e-mail attive e bozze per eseguirne la ricerca, la revisione e l’aggiornamento nei percorsi di account associati. <a href="../content/emails-list.md">Ulteriori informazioni</a> |

## Note sulla versione 2025.3

**Data di distribuzione**: 1 aprile 2025

Questa versione include le seguenti nuove funzionalità e miglioramenti:

| Tipo | Elemento | Descrizione |
| ---- | ---- | ----------- |
| Funzione | Duplicare i percorsi dell’account | È ora disponibile un’azione di duplica per i percorsi degli account. Puoi duplicare i dettagli per il percorso account o solo un semplice schema della struttura del flusso e del percorso. <a href="../journeys/journey-overview.md#duplicate-journey">Ulteriori informazioni</a> |
| Funzione | I miei token per percorsi account | Ora puoi definire un set di token personalizzati con valori specifici del percorso account. Questo set di token personalizzati si chiama _I miei token_ e uno qualsiasi di questi token personalizzati è destinato alla personalizzazione durante l’authoring e-mail del percorso. <a href="../content/personalization-my-tokens.md">Ulteriori informazioni</a> |
| Funzione | Elimina fasi del gruppo acquisti | È possibile eliminare il modello delle fasi del gruppo acquisti quando si trova nello stato Bozza o Pubblicato. Se è pubblicato (live), puoi eliminarlo solo se non è associato a una soluzione di interesse. <a href="../buying-groups/buying-group-stages.md#delete-the-buying-group-stages-model">Ulteriori informazioni</a> |
| Miglioramento | Conteggi nodi percorso | È stata migliorata la visibilità dei conteggi a livello di nodo per l’appartenenza a percorsi pubblicati. Nella _mappa del percorso_, i nodi mostrano il _[!UICONTROL Totale account inseriti]_. Quando selezioni e fai clic sul nodo dell’azione, i dettagli a destra includono anche _[!UICONTROL Account non ancora attivati su]_. E i dettagli dei nodi _Ascolta un evento_ includono _[!UICONTROL Account in questo passaggio]_. Utilizza queste informazioni per convalidare l’avanzamento dell’account nei tuoi percorsi live, completati e interrotti. |

## Note sulla versione 2025.2

**Data di distribuzione**: 11 marzo 2025

Questa versione include le seguenti nuove funzionalità e miglioramenti:

| Tipo | Elemento | Descrizione |
| ---- | ---- | ----------- |
| Funzione | Campi personalizzabili: frammenti di contenuto | Durante la progettazione di frammenti visivi, puoi designare parametri per un componente nel frammento come modificabili. Questa funzione consente all’autore del messaggio e-mail o del modello di specificare un valore di campo personalizzato che sia specifico per le proprie esigenze. Questo flag di personalizzazione è limitato ai componenti visivi immagine, testo e pulsante. <a href="../content/fragment-authoring.md#enable-fragment-customization">Ulteriori informazioni</a> |
| Funzione | Tipi di duplicazione di percorso | Quando duplichi un percorso account, puoi includere i dettagli del nodo, escluse le e-mail e i messaggi SMS creati in Journey Optimizer B2B Edition. In alternativa, puoi creare una copia semplificata della struttura e dei flussi di tracciato, senza specificare i dettagli e le impostazioni del nodo. <a href="../journeys/journey-overview.md#duplicate-journey">Ulteriori informazioni</a> |
| Miglioramento | Altri quattro modelli e-mail di esempio | La libreria dei modelli e-mail di esempio ora include quattro modelli SecurFinacial come esempi di contenuti di nuovo coinvolgimento, informazione, nurturing e feedback |

<!-- | Feature | B2B built-in roles and product permissions | Experience Platform now includes a set of built-in (default) roles that you can use to manage access to the B2B product capabilities. <a href="../admin/user-management.md#b2b-built-in-roles">Learn more</a> <br/>Administrators can now define custom roles in Adobe Experience Platform to include Journey Optimizer B2B Edition product permissions.  <a href="../admin/user-management.md#b2b-product-permissions">Learn more</a> | -->

## Note sulla versione 2025.1 {#Jan-2025}

**Data di distribuzione**: 6 febbraio 2025

Questa versione include le seguenti nuove funzionalità e miglioramenti:

| Tipo | Elemento | Descrizione |
| ---- | ---- | ----------- |
| Funzione | Inoltro degli eventi esperienza | Gli amministratori possono configurare definizioni di eventi basate su Adobe Experience Platform (AEP). Queste configurazioni consentono ai marketer di creare percorsi account che reagiscono agli eventi esperienza di AEP.  <a href="../admin/configure-aep-events.md">Ulteriori informazioni</a> |
| Funzione | Destinazioni dei paid media | Rendi idonee le persone note per le campagne di paid media da un percorso di account in modo da poterle coinvolgere ulteriormente su piattaforme pubblicitarie, come LinkedIn. Utilizza un nodo di percorso suddiviso per segmentare i tipi di pubblico degli account in base a un comportamento specifico e identificare quelli che richiedono un ulteriore coinvolgimento. In seguito, aggiungi le persone da tali account a un pubblico di clientela esterna tramite Real-time CDP a una destinazione di paid media supportata. <a href="../journeys/action-nodes.md#journey-optimizer-b2b-actions">Ulteriori informazioni</a> |
| Funzione | Dashboard intelligente | Visualizza il progresso dei gruppi acquisti attraverso i loro percorsi di account, comprese le informazioni generate dall’IA per un’analisi più intelligente e una definizione precisa delle priorità degli account. <a href="../dashboards/intelligent-dashboard.md">Ulteriori informazioni</a> |
| Funzione | Dettagli del gruppo acquisti e dell’account | Visualizza informazioni a livello di gruppo acquisti e di account per disporre di più dati contestuali e storici quando inizi a coinvolgere un cliente.<p>I dettagli del gruppo acquisti includono eventuali intenti di prime parti rilevati. <a href="../buying-groups/buying-group-details.md">Ulteriori informazioni</a><p>I dettagli dell’account evidenziano l’aumento nell’intento rilevato di coinvolgimento, in modo da poter avvisare il team vendite in merito agli account pronti per un coinvolgimento personalizzato orientato alla vendita.  <a href="../accounts/account-details.md">Ulteriori informazioni</a> |
| Funzione | Panoramica dei percorsi | Durante l’accesso ai percorsi degli account, la scheda Panoramica fornisce un’istantanea completa dei percorsi di account attivi, con informazioni dettagliate sull’avanzamento dell’account utilizzando grafici a cerchi e a barre che categorizzano e quantificano i completamenti e le attività di coinvolgimento.  <a href="../dashboards/journeys-dashboard.md">Ulteriori informazioni</a> |
| Funzione | Modifica delle immagini di Adobe Express | Le azioni rapide di Adobe Express consentono di apportare semplici modifiche (ad esempio ritagliare e ridimensionare) alle immagini per conferire un aspetto più curato al contenuto. <a href="../content/image-edit-adobe-express.md#quick-actions-in-adobe-express">Ulteriori informazioni</a>  <p>Per un set più completo di strumenti di progettazione, questa integrazione consente di ottenere una licenza Adobe Express completa in Journey Optimizer B2B Edition. Con questa configurazione, l’interfaccia utente completa di Adobe Express diventa accessibile all’interno dell’area di lavoro locale delle risorse. <a href="../content/image-edit-adobe-express.md#adobe-express-enterprise-license">Ulteriori informazioni</a> |
| Funzione | Filtri intento per ruoli di gruppi acquisti | Nell’invio di parole chiave di intento, il modello di rilevamento intento prevede una soluzione o un prodotto di interesse con sufficiente affidabilità in base all’attività di un lead. <a href="../admin/intent-data.md">Ulteriori informazioni</a> <p>Questi dati di intento sono disponibili per definire le condizioni dei ruoli del gruppo acquisti <a href="../buying-groups/buying-groups-role-templates.md#add-the-template-roles">Ulteriori informazioni</a> |
| Miglioramento | Supporto di eventi Marketo Engage nei percorsi | Il nodo del percorso _Ascolta evento_ ora supporta due eventi Marketo Engage a livello di persone: _Visite alla pagina web_ e _Compila il modulo_. <a href="../journeys/listen-for-event-nodes.md#listen-for-marketo-engage-event">Ulteriori informazioni</a> |
| Miglioramento | Filtri del gruppo acquisti per elenchi avanzati di Marketo Engage | Visualizza e crea elenchi avanzati con filtri del gruppo acquisti in Marketo Engage. Questi filtri aggiunti consentono di eliminare e includere i membri del gruppo acquisti in campagne e programmi Marketo Engage da percorsi di account in Journey Optimizer B2B Edition. <a href="../buying-groups/marketo-engage-smart-list-buying-group-filters.md">Ulteriori informazioni</a> |
| Miglioramento | Filtro di iscrizione all’elenco Marketo Engage per percorsi e ruoli | In Journey Optimizer B2B, verifica l’iscrizione all’elenco Marketo Engage come condizione per un nodo di _percorso suddiviso da persone_ per eliminare la duplicazione nelle attività di percorso. <a href="../journeys/split-merge-paths-nodes.md#add-a-split-path-by-people-node">Ulteriori informazioni</a> <p> Per i modelli dei ruoli del gruppo acquisti, utilizza l’iscrizione all’elenco come condizione del ruolo. <a href="../buying-groups/buying-groups-role-templates.md#add-the-template-roles">Ulteriori informazioni</a> |
| Miglioramento | Dashboard panoramica del coinvolgimento | Questa dashboard viene aggiornata per fornire una visione completa del coinvolgimento. Mostra metriche in tempo reale di interazioni tra account e singoli individui tramite grafici a cerchi istantanei e grafici a linee che rivelano le tendenze nel tempo. <a href="../dashboards/engagement-dashboard.md">Ulteriori informazioni</a> |

## Versioni del 2024

Espandi i seguenti elenchi per le funzioni e i miglioramenti di Journey Optimizer B2B Edition rilasciati nel 2024.

+++Note sulla versione di ottobre 2024

**Data di distribuzione**: 29 ottobre 2024

Questa versione include le seguenti nuove funzionalità e miglioramenti:

| Tipo | Elemento | Descrizione |
| ---- | ---- | ----------- |
| Funzione | Contenuto condizionale nelle e-mail | Personalizza il contenuto delle e-mail in base al comportamento del destinatario e alle caratteristiche del profilo, sia a livello di account che di lead. <p>Quando crei un’e-mail per il percorso dell’account nello spazio di progettazione visiva dell’e-mail, utilizza le regole condizionali per definire più varianti per qualsiasi componente di contenuto. <a href="../content/conditional-content.md">Ulteriori informazioni</a> |
| Funzione | Azioni delle persone _Aggiungi all’elenco_ e _Rimuovi dall’elenco_ in percorsi | Personalizza il contenuto delle e-mail in base al comportamento del destinatario e alle caratteristiche del profilo, sia a livello di account che di lead. <a href="../journeys/action-nodes.md">Ulteriori informazioni</a> |
| Funzione | Governance dei contenuti e blocco dei componenti | Per garantire il rispetto delle progettazioni di contenuti approvate, utilizza le funzioni di governance dei contenuti per bloccare i componenti di contenuto dei modelli e-mail. Attivando la governance dei contenuti nel modello e-mail, i marketer possono modificare solo gli elementi consentiti per mantenerli allineati alla strategia dei contenuti. <a href="../content/template-content-governance.md">Ulteriori informazioni</a> |
| Funzione | Fasi del gruppo acquisti | Quando definisci e pubblichi un modello di staging personalizzato per gruppi acquisti, puoi tenere traccia della progressione del gruppo acquisti attraverso le sue fasi del ciclo di vita. Utilizza queste fasi per identificare le prossime azioni migliori per i membri del gruppo acquisti. Puoi configurare le regole di transizione e i nodi del percorso che determinano la progressione delle fasi e attivano le azioni in base alle modifiche. <a href="../buying-groups/buying-group-stages.md">Ulteriori informazioni</a> |
| Miglioramento | Nuovi modelli e-mail pronti all’uso | La libreria dei modelli di esempio ora include ulteriori modelli e-mail progettati per i marketer B2B. Utilizza questi modelli di esempio come punto di partenza e aggiungi il branding e la messaggistica. <a href="../content/email-templates.md#select-a-design-template">Ulteriori informazioni</a> |
| Miglioramento | Campi personalizzati come attributi persona | Se hai dei campi persona personalizzati definiti nello schema del pubblico dell’account in Experience Platform, questi campi sono disponibili per l’utilizzo come attributi persona in determinate condizioni. Utilizza questi attributi personalizzati in: <li>Modelli di ruoli: <a href="../buying-groups/buying-groups-role-templates.md#add-the-template-roles">ulteriori informazioni</a></li><li>Dividi percorsi per nodi percorso persone: <a href="../journeys/split-merge-paths-nodes.md#add-a-split-path-by-people-node">ulteriori informazioni</a></li> |
| Miglioramento | Impostazioni del canale e-mail | Le impostazioni delle e-mail sono ora visibili nell’interfaccia di Journey Optimizer B2B Edition. Puoi rivedere rapidamente le configurazioni correnti e gli amministratori possono fare clic su _[!UICONTROL Modifica impostazioni]_ per passare direttamente alle impostazioni in Marketo Engage e aggiornarle in base ai requisiti dell’organizzazione. <a href="../admin/configure-channels-emails.md">Ulteriori informazioni</a> |

+++

+++Note sulla versione di settembre 2024

**Data di distribuzione**: 7 ottobre 2024

Questa versione include le seguenti nuove funzionalità e miglioramenti:

| Tipo | Elemento | Descrizione |
| ---- | ---- | ----------- |
| Miglioramento | Libreria di risorse centrale | La _libreria di risorse centrale_ avanzata consente di utilizzare tutte le risorse immagine nell’istanza di Marketo Engage, nelle aree di lavoro di Design Studio. Esistono guardrail incorporati che impediscono le modifiche alle risorse Marketo Engage da Journey Optimizer B2B Edition, nonché le operazioni di eliminazione e spostamento. Queste protezioni garantiscono la conservazione delle risorse di origine (Marketo Engage Design Studio) consentendo al tempo stesso la lettura e il riutilizzo senza interruzioni in Journey Optimizer B2B Edition.<p>Per le risorse da utilizzare esclusivamente in Journey Optimizer B2B Edition, un’area di lavoro specifica fornisce funzioni di gestione risorse complete. <a href="../content/marketo-engage-design-studio.md">Ulteriori informazioni</a> |
| Funzione | Risorse con accesso recente | La pagina Home dell’app Journey Optimizer B2B Edition ora include la sezione _[!UICONTROL Accesso recente]_, che fornisce un elenco delle risorse utilizzate più di recente dall’addetto marketing o dall’amministratore. Puoi utilizzare questo elenco per passare direttamente alla risorsa su cui hai lavorato di recente senza passare attraverso una serie di pagine di risorse e di ricerche. <p>L’elenco fornisce informazioni aggiuntive relative alla modifica, in modo da poter decidere quale delle risorse deve essere ulteriormente modificata dall’ultima sessione. Per le risorse e-mail, l’elenco visualizza il percorso dell’account in cui viene utilizzata la risorsa e-mail. <a href="../home-page.md">Ulteriori informazioni</a> |
| Miglioramento | Nodo del percorso suddiviso: riordinare percorsi | Nei nodi del percorso suddivisi, il filtro dei percorsi viene valutato in ordine decrescente. Ogni persona o account procede lungo il primo percorso corrispondente. Per riordinare i percorsi definiti, fai clic sulle frecce su e giù, in alto a destra di ciascuna scheda del percorso, per spostarlo in alto o in basso nell’elenco. <a href="../journeys/split-merge-paths-nodes.md#split-paths">Ulteriori informazioni</a> |
| Miglioramento | Nodo del percorso suddiviso: attributi di condizione della cronologia dell’attività aggiuntiva | Quando si utilizzano le condizioni per definire il filtro del percorso di un nodo suddiviso secondo le persone, sono disponibili due attributi aggiuntivi: _E-mail aperta_ e _E-mail consegnata_. Queste aggiunte forniscono maggiore flessibilità per filtrare le persone nel percorso in base all’attività e-mail. <a href="../journeys/journey-nodes.md#split-paths">Ulteriori informazioni</a> |

+++

+++Note sulla versione di agosto 2024

**Data di distribuzione**: 29 agosto 2024

Questa versione include le seguenti nuove funzionalità e miglioramenti:

| Tipo | Elemento | Descrizione |
| ---- | ---- | ----------- |
| Funzione | Tipi di pubblico associati all’account LinkedIn | Genera tipi di pubblico LinkedIn Ad tramite tipi di pubblico associati all’account, per aiutarti a riempire ruoli vuoti nei gruppi acquisti. Definendo un set di filtri di gruppi acquisti, puoi mantenere un pubblico associato a LinkedIn per eseguire il targeting dei potenziali clienti che corrispondono ai parametri del gruppo acquisti. <p>Questa funzione sfrutta le destinazioni di Experience Platform per gestire alcuni aspetti dell’integrazione. <a href="../data/linkedin-account-matched-audiences.md">Ulteriori informazioni</a> |
| Miglioramento | Ciclo di vita dello stato per i frammenti di contenuto visivo | I frammenti visivi vengono ora gestiti tramite un ciclo di vita dello stato. Lo stato del frammento determina la sua disponibilità per l’utilizzo in un messaggio o in un modello e-mail e le modifiche che puoi apportarvi. <p>Questo flusso di lavoro ottimizzato permette di gestire facilmente i contenuti riutilizzati in base al calendario delle comunicazioni e delle promozioni. <a href="../content/fragments.md#fragment-status-and-lifecycle">Ulteriori informazioni</a> |

+++
