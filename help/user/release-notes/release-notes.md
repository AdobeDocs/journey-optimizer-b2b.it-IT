---
title: Note sulla versione di Journey Optimizer B2B Edition
description: Scopri le funzioni e i miglioramenti più recenti di Adobe Journey Optimizer B2B Edition.
role: User, Admin
exl-id: 7d3f1c26-d8a6-4065-a70f-5b30cb975dc8
source-git-commit: dbb1c0d57f3d0b9818dc284047bda9562cfb40f6
workflow-type: tm+mt
source-wordcount: '2166'
ht-degree: 96%

---

# Note sulla versione di Journey Optimizer B2B Edition

Adobe Journey Optimizer B2B Edition fornisce continuamente nuove funzioni, miglioramenti a quelle esistenti e correzioni di bug.

Journey Optimizer B2B Edition è costruito nativamente su [!DNL Adobe Experience Platform] e ne eredita le innovazioni e i miglioramenti più recenti. Ulteriori informazioni su queste modifiche sono disponibili nelle [note sulla versione di Adobe Experience Platform](https://experienceleague.adobe.com/it/docs/experience-platform/release-notes/latest){target="_blank"}.

Rivedi la [descrizione del prodotto](https://helpx.adobe.com/it/legal/product-descriptions/adobe-journey-optimizer-b2b.html){target="_blank"} per informazioni su diritti, guardrail delle prestazioni e limitazioni.

## Note sulla versione 2025.5

**Data di distribuzione**: 3 giugno 2025

Questa versione include le seguenti nuove funzionalità e miglioramenti:

| Tipo | Elemento | Descrizione |
| ---- | ---- | ----------- |
| Funzione | Test delle e-mail con Litmus | Con un account [Litmus Enterprise](https://www.litmus.com/email-testing){target="_blank"}, ora puoi visualizzare in anteprima il rendering delle e-mail nei client e-mail più diffusi da Journey Optimizer B2B edition. Questa integrazione ti aiuta a garantire che il contenuto delle e-mail si presenti in modo ottimale e funzioni come previsto in ogni casella in entrata e-mail. [Ulteriori informazioni](../content/email-test-rendering.md) |
| Miglioramento | E-mail duplicata | Quando aggiungi un’e-mail per un nodo di percorso, ora puoi duplicare un’e-mail esistente. Modifica l’impostazione o il contenuto dell’e-mail duplicata oppure lasciala intatta.  [Ulteriori informazioni](../content/add-email.md#add-an-email-to-your-journey) |
| Miglioramento | Formato token Handlebar per e-mail | I token di personalizzazione per il contenuto delle e-mail ora utilizzano un formato aggiornato completamente compatibile con gli script Handlebar. Questo formato utilizza _camel case_ o trattini bassi, eliminando gli spazi. [Ulteriori informazioni](../content/email-authoring.md#content-authoring---personalization) |
| Miglioramento | Visualizzazione del conteggio totale per elenchi | Le pagine di elenco _[!UICONTROL Interessi della soluzione]_ e _[!UICONTROL Percorsi account]_ sono state migliorate con la visualizzazione del conteggio totale accanto alla barra di ricerca. |

## Note sulla versione 2025.4

**Data di distribuzione**: 29 aprile 2025

Questa versione include le seguenti nuove funzionalità e miglioramenti:

| Tipo | Elemento | Descrizione |
| ---- | ---- | ----------- |
| Funzione | Elenchi account | Ora puoi creare un elenco account statico o dinamico per eseguire il targeting di account denominati in base a criteri definiti, ad esempio settore, posizione o dimensioni dell’azienda. <a href="../accounts/account-lists.md">Ulteriori informazioni</a> |
| Funzione | Orchestrazione dei percorsi dell’elenco account | Utilizza i nodi delle azioni di percorso per aggiungere e rimuovere account per gli elenchi di account statici. <a href="../accounts/account-lists-journeys.md#take-an-action-node---add-to-account">Ulteriori informazioni</a> |
| Miglioramento | Filtrare l’iscrizione al percorso in Marketo Engage | Utilizza gli elenchi account di Adobe Journey Optimizer B2B Edition per il pubblico del percorso, quindi utilizza il filtro _Membro di un elenco account_ negli elenchi avanzati di Marketo Engage. <a href="../accounts/account-lists-journeys.md#marketo-engage-program---member-of-account-list">Ulteriori informazioni</a> |
| Funzione | Filtri di inattività | Orchestra i percorsi in base all’inattività nelle campagne e nei programmi di Marketo Engage, inclusi inattività delle e-mail, momenti interessanti, modifiche al valore dei dati e pagine web visitate. <a href="../journeys/split-merge-paths-nodes.md#activity-filtering">Ulteriori informazioni</a> |
| Miglioramento | Filtro pagina web visitata | Orchestra i percorsi in base all’attività per le pagine web visitate associate a campagne e programmi di Marketo Engage. <a href="../journeys/split-merge-paths-nodes.md#people-path-conditions">Ulteriori informazioni</a> |
| Miglioramento | Elenco di e-mail | Visualizza un elenco globale di e-mail attive e bozze per eseguirne la ricerca, la revisione e l’aggiornamento nei percorsi di account associati. <a href="../content/emails-list.md">Ulteriori informazioni</a> |

## Note sulla versione 2025.3

**Data di distribuzione**: 1 aprile 2025

Questa versione include le seguenti nuove funzionalità e miglioramenti:

| Tipo | Elemento | Descrizione |
| ---- | ---- | ----------- |
| Funzione | Duplicare i percorsi dell’account | È ora disponibile un’azione di duplica per i percorsi degli account. Puoi duplicare i dettagli per il percorso account o solo un semplice schema della struttura del flusso e del percorso. <a href="../journeys/journey-overview.md#duplicate-journey">Ulteriori informazioni</a> |
| Funzione | I miei token per percorsi account | Ora puoi definire un set di token personalizzati con valori specifici del percorso account. Questo set di token personalizzati si chiama _I miei token_ e uno qualsiasi di questi token personalizzati è destinato alla personalizzazione durante l’authoring e-mail del percorso. <a href="../content/personalization-my-tokens.md">Ulteriori informazioni</a> |
| Funzione | Elimina fasi del gruppo acquisti | È possibile eliminare il modello delle fasi del gruppo acquisti quando si trova nello stato Bozza o Pubblicato. Se è pubblicato (live), puoi eliminarlo solo se non è associato a un interesse della soluzione. <a href="../buying-groups/buying-group-stages.md#delete-the-buying-group-stages-model">Ulteriori informazioni</a> |
| Miglioramento | Conteggi nodi percorso | È stata migliorata la visibilità dei conteggi a livello di nodo di appartenenza al percorso pubblicati. Nella _mappa del percorso_, i nodi mostrano il _[!UICONTROL Totale account inseriti]_. Quando selezioni e fai clic sul nodo dell’azione, i dettagli a destra includono anche _[!UICONTROL Account non ancora attivati su]_. E i dettagli dei nodi _Ascolta un evento_ includono _[!UICONTROL Account in questo passaggio]_. Utilizza queste informazioni per convalidare l’avanzamento dell’account nei tuoi percorsi live, completati e interrotti. |

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
| Funzione | Destinazioni dei paid media | Rendi idonee le persone note per le campagne di paid media da un percorso di account in modo da poterle coinvolgere ulteriormente su piattaforme pubblicitarie, come LinkedIn. Utilizza un nodo di percorso suddiviso in un percorso di account per segmentare i tipi di pubblico degli account in base a un comportamento specifico e identificare quelli che richiedono un ulteriore coinvolgimento. In seguito, aggiungi le persone da tali account a un pubblico di clientela esterna tramite Real-time CDP a una destinazione di paid media supportata. <a href="../journeys/action-nodes.md#journey-optimizer-b2b-actions">Ulteriori informazioni</a> |
| Funzione | Dashboard intelligente | Visualizza il progresso dei gruppi di acquisto attraverso i loro percorsi di account, comprese le informazioni generate dall’intelligenza artificiale per un’analisi più intelligente e una definizione precisa delle priorità degli account. <a href="../dashboards/intelligent-dashboard.md">Ulteriori informazioni</a> |
| Funzione | Dettagli del gruppo di acquisto e dell’account | Visualizza informazioni a livello di gruppo di acquisto e di account per disporre di più dati contestuali e storici quando inizi a coinvolgere un cliente.<p>I dettagli del gruppo di acquisto includono qualsiasi intento di prime parti rilevato. <a href="../buying-groups/buying-group-details.md">Ulteriori informazioni</a><p>Gli account dei dettagli evidenziano l’aumento nell’intento rilevato di coinvolgimento, in modo da poter avvisare le vendite su account pronti per un coinvolgimento mirato alle vendite personalizzate.  <a href="../accounts/account-details.md">Ulteriori informazioni</a> |
| Funzione | Panoramica dei percorsi | Durante l’accesso ai percorsi degli account, la scheda Panoramica fornisce un’istantanea completa dei percorsi di account attivi, con informazioni dettagliate sull’avanzamento dell’account utilizzando grafici a cerchi e a barre che categorizzano e quantificano i completamenti e le attività di coinvolgimento.  <a href="../dashboards/journeys-dashboard.md">Ulteriori informazioni</a> |
| Funzione | Modifica delle immagini di Adobe Express | Le azioni rapide di Adobe Express consentono di apportare semplici modifiche (ad esempio ritagliare e ridimensionare) alle immagini per conferire un aspetto più curato al contenuto. <a href="../content/image-edit-adobe-express.md#quick-actions-in-adobe-express">Ulteriori informazioni</a>  <p>Per un set più completo di strumenti di progettazione, questa integrazione consente di ottenere una licenza Adobe Express completa in Journey Optimizer B2B Edition. Con questa configurazione, l’interfaccia utente completa di Adobe Express diventa accessibile all’interno dell’area di lavoro locale delle risorse. <a href="../content/image-edit-adobe-express.md#adobe-express-enterprise-license">Ulteriori informazioni</a> |
| Funzione | Filtri intento per ruoli di gruppo di acquisto | Nell’invio di parole chiave di intento, il modello di rilevamento intento prevede una soluzione o un prodotto di interesse con sufficiente affidabilità in base all’attività di un lead. <a href="../admin/intent-data.md">Ulteriori informazioni</a> <p>Questi dati di intento sono disponibili per definire le condizioni dei ruoli del gruppo di acquisto <a href="../buying-groups/buying-groups-role-templates.md#add-the-template-roles">Ulteriori informazioni</a> |
| Miglioramento | Supporto di eventi Marketo Engage nei percorsi | Il nodo del percorso _Ascolta evento_ ora supporta due eventi Marketo Engage a livello di persone: _Visite alla pagina web_ e _Compila il modulo_. <a href="../journeys/listen-for-event-nodes.md#listen-for-marketo-engage-event">Ulteriori informazioni</a> |
| Miglioramento | Filtri del gruppo di acquisto per elenchi avanzati di Marketo Engage | Visualizza e crea elenchi avanzati con filtri del gruppo di acquisto in Marketo Engage. Questi filtri aggiunti consentono di eliminare e includere i membri del gruppo di acquisto in campagne e programmi Marketo Engage da percorsi di account in Journey Optimizer B2B Edition. <a href="../buying-groups/marketo-engage-smart-list-buying-group-filters.md">Ulteriori informazioni</a> |
| Miglioramento | Filtro di iscrizione all’elenco Marketo Engage per percorsi e ruoli | In Journey Optimizer B2B, verifica l’iscrizione all’elenco Marketo Engage come condizione per un nodo di _percorso suddiviso da persone_ per eliminare la duplicazione nelle attività di percorso. <a href="../journeys/split-merge-paths-nodes.md#add-a-split-path-by-people-node">Ulteriori informazioni</a> <p> Per i modelli dei ruoli del gruppo di acquisto, utilizza l’iscrizione all’elenco come condizione del ruolo. <a href="../buying-groups/buying-groups-role-templates.md#add-the-template-roles">Ulteriori informazioni</a> |
| Miglioramento | Dashboard panoramica del coinvolgimento | Questa dashboard viene aggiornata per fornire una visione completa del coinvolgimento. Mostra metriche in tempo reale di interazioni tra account e singoli individui tramite grafici a cerchi istantanei e grafici a linee che rivelano le tendenze nel tempo. <a href="../dashboards/engagement-dashboard.md">Ulteriori informazioni</a> |

## Versioni del 2024

Espandi i seguenti elenchi per le funzioni e i miglioramenti di Journey Optimizer B2B Edition rilasciati nel 2024.

+++Note sulla versione di ottobre 2024

**Data di distribuzione**: 29 ottobre 2024

Questa versione include le seguenti nuove funzionalità e miglioramenti:

| Tipo | Elemento | Descrizione |
| ---- | ---- | ----------- |
| Funzione | Contenuto condizionale nei modelli e-mail | Personalizza il contenuto delle e-mail in base al comportamento del destinatario e alle caratteristiche del profilo, sia a livello di account che di lead. <p>Quando crei un’e-mail per il percorso dell’account nello spazio di progettazione visiva dell’e-mail, utilizza le regole condizionali per definire più varianti per qualsiasi componente di contenuto. <a href="../content/conditional-content.md">Ulteriori informazioni</a> |
| Funzione | Azioni delle persone _Aggiungi all’elenco_ e _Rimuovi dall’elenco_ in percorsi | Personalizza il contenuto delle e-mail in base al comportamento del destinatario e alle caratteristiche del profilo, sia a livello di account che di lead. <a href="../journeys/action-nodes.md">Ulteriori informazioni</a> |
| Funzione | Governance dei contenuti e blocco dei componenti | Per garantire il rispetto delle progettazioni di contenuti approvate, utilizza le funzioni di governance dei contenuti per bloccare i componenti di contenuto dei modelli e-mail. Attivando la governance dei contenuti nel modello e-mail, i marketer possono modificare solo gli elementi consentiti per mantenerli allineati alla strategia dei contenuti. <a href="../content/template-content-governance.md">Ulteriori informazioni</a> |
| Funzione | Fasi del gruppo acquisti | Quando definisci e pubblichi un modello di staging per gruppi di acquisto personalizzato, puoi tenere traccia della progressione del gruppo di acquisto attraverso le sue fasi del ciclo di vita. Utilizza queste fasi per identificare le prossime azioni migliori per i membri del gruppo di acquisto. Puoi configurare le regole di transizione e i nodi del percorso che determinano la progressione delle fasi e attivano le azioni in base alle modifiche. <a href="../buying-groups/buying-group-stages.md">Ulteriori informazioni</a> |
| Miglioramento | Nuovi modelli e-mail pronti all’uso | La libreria dei modelli di esempio ora include ulteriori modelli e-mail progettati per i marketer B2B. Utilizza questi modelli di esempio come punto di partenza e aggiungi il branding e la messaggistica. <a href="../content/email-templates.md#select-a-design-template">Ulteriori informazioni</a> |
| Miglioramento | Campi personalizzati come attributi persona | Se hai dei campi persona personalizzati definiti nello schema del pubblico dell’account in Experience Platform, questi campi sono disponibili per l’utilizzo come attributi persona in determinate condizioni. Utilizza questi attributi personalizzati in: <li>Modelli di ruoli: <a href="../buying-groups/buying-groups-role-templates.md#add-the-template-roles">ulteriori informazioni</a></li><li>Dividi percorsi per nodi percorso persone: <a href="../journeys/split-merge-paths-nodes.md#add-a-split-path-by-people-node">ulteriori informazioni</a></li> |
| Miglioramento | Impostazioni del canale e-mail | Le impostazioni delle e-mail sono ora visibili nell’interfaccia di Journey Optimizer B2B Edition. Puoi rivedere rapidamente le configurazioni correnti e gli amministratori possono fare clic su _[!UICONTROL Modifica impostazioni]_ per passare direttamente alle impostazioni in Marketo Engage e aggiornarle in base ai requisiti dell’organizzazione. <a href="../admin/configure-channels-emails.md">Ulteriori informazioni</a> |

+++

Note sulla versione di settembre 2024

**Data di distribuzione**: 7 ottobre 2024

Questa versione include le seguenti nuove funzionalità e miglioramenti:

| Tipo | Elemento | Descrizione |
| ---- | ---- | ----------- |
| Miglioramento | Libreria di risorse centrale | La _libreria di risorse centrale_ avanzata consente di utilizzare tutte le risorse immagine nell’istanza di Marketo Engage, nelle aree di lavoro di Design Studio. Esistono guardrail integrati che impediscono le modifiche alle risorse Marketo Engage da Journey Optimizer B2B Edition, nonché le operazioni di eliminazione e spostamento. Queste protezioni garantiscono la conservazione delle risorse di origine (Marketo Engage Design Studio) consentendo al tempo stesso la lettura e il riutilizzo senza interruzioni in Journey Optimizer B2B Edition.<p>Per le risorse da utilizzare esclusivamente in Journey Optimizer B2B Edition, un’area di lavoro specifica fornisce funzioni di gestione risorse complete. <a href="../content/marketo-engage-design-studio.md">Ulteriori informazioni</a> |
| Funzione | Risorse con accesso recente | La pagina Home dell’app Journey Optimizer B2B Edition ora include la sezione _[!UICONTROL Accesso recente]_, che fornisce un elenco delle risorse utilizzate più di recente dall’addetto marketing o dall’amministratore. Puoi utilizzare questo elenco per passare direttamente alla risorsa su cui hai lavorato di recente senza passare attraverso una serie di pagine di risorse e di ricerche. <p>L’elenco fornisce informazioni aggiuntive relative alla modifica, in modo da poter decidere quale delle risorse deve essere ulteriormente modificata dall’ultima sessione. Per le risorse e-mail, l’elenco visualizza il percorso dell’account in cui viene utilizzata la risorsa e-mail. <a href="../home-page.md">Ulteriori informazioni</a> |
| Miglioramento | Nodo del percorso suddiviso: riordinare percorsi | Nei nodi del percorso suddivisi, il filtro dei percorsi viene valutato in ordine decrescente. Ogni persona o account procede lungo il primo percorso corrispondente. Per riordinare i percorsi definiti, fai clic sulle frecce su e giù, in alto a destra di ciascuna scheda del percorso, per spostarlo in alto o in basso nell’elenco. <a href="../journeys/split-merge-paths-nodes.md#split-paths">Ulteriori informazioni</a> |
| Miglioramento | Nodo del percorso suddiviso: attributi di condizione della cronologia dell’attività aggiuntiva | Quando si utilizzano le condizioni per definire il filtro del percorso di un nodo suddiviso secondo le persone, sono disponibili due attributi aggiuntivi: _E-mail aperta_ e _E-mail consegnata_. Queste aggiunte forniscono maggiore flessibilità per filtrare le persone nel percorso in base all’attività e-mail. <a href="../journeys/journey-nodes.md#split-paths">Ulteriori informazioni</a> |

+++

Note sulla versione di agosto 2024

**Data di distribuzione**: 29 agosto 2024

Questa versione include le seguenti nuove funzionalità e miglioramenti:

| Tipo | Elemento | Descrizione |
| ---- | ---- | ----------- |
| Funzione | Tipi di pubblico associati all’account LinkedIn | Genera tipi di pubblico LinkedIn Ad tramite tipi di pubblico associati all’account, per aiutarti a riempire ruoli vuoti nei gruppi di acquisto. Definendo un set di filtri di gruppi di acquisto, puoi mantenere un pubblico associato a LinkedIn per eseguire il targeting dei potenziali clienti che corrispondono ai parametri del gruppo di acquisto. <p>Questa funzione sfrutta le destinazioni di Experience Platform per gestire alcuni aspetti dell’integrazione. <a href="../data/linkedin-account-matched-audiences.md">Ulteriori informazioni</a> |
| Miglioramento | Ciclo di vita dello stato per i frammenti di contenuto visivo | I frammenti visivi vengono ora gestiti tramite un ciclo di vita dello stato. Lo stato del frammento determina la sua disponibilità per l’utilizzo in un messaggio o in un modello e-mail e le modifiche che puoi apportarvi. <p>Questo flusso di lavoro ottimizzato permette di gestire facilmente i contenuti riutilizzati in base al calendario delle comunicazioni e delle promozioni. <a href="../content/fragments.md#fragment-status-and-lifecycle">Ulteriori informazioni</a> |

+++
