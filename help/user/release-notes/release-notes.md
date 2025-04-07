---
title: Note sulla versione
description: Note sulla versione più recente per l’edizione B2B di Adobe Journey Optimizer
exl-id: 7d3f1c26-d8a6-4065-a70f-5b30cb975dc8
source-git-commit: 228837741f3373ee2b8423515b7412564281f8ea
workflow-type: tm+mt
source-wordcount: '1818'
ht-degree: 9%

---

# Note sulla versione di Journey Optimizer B2B edition

Adobe Journey Optimizer B2B edition offre continuamente nuove funzioni, miglioramenti alle funzioni esistenti e correzioni di bug.

Journey Optimizer B2B edition è stato sviluppato in modalità nativa su [!DNL Adobe Experience Platform] e ne eredita le innovazioni e i miglioramenti più recenti. Ulteriori informazioni su queste modifiche nelle [Note sulla versione di Adobe Experience Platform](https://experienceleague.adobe.com/it/docs/experience-platform/release-notes/latest){target="_blank"}.

Rivedi la [descrizione del prodotto](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer-b2b.html){target="_blank"} per informazioni su adesioni, guardrail delle prestazioni e limitazioni.

## Note sulla versione 2025.3

**Data di rilascio**: mercoledì 1 aprile 2025

Questa versione include le nuove funzionalità e i miglioramenti seguenti:

| Tipo | Elemento | Descrizione |
| ---- | ---- | ----------- |
| Nuova funzionalità | Elenchi account | Ora puoi creare un elenco di account statico o dinamico per eseguire il targeting di account denominati in base a criteri definiti, ad esempio settore, posizione o dimensioni dell’azienda. <a href="../accounts/account-lists.md">Ulteriori informazioni</a> |
| Nuova funzionalità | I miei token per percorsi di account | Ora puoi definire un set di token personalizzati con valori specifici per il percorso di account. Questo set di token personalizzati si chiama _I miei token_ e uno qualsiasi di questi token personalizzati è destinato alla personalizzazione durante la creazione di e-mail di percorso. <a href="../content/personalization-my-tokens.md">Ulteriori informazioni</a> |
| Nuova funzionalità | Elimina fasi del gruppo di acquisto | È possibile eliminare il modello delle fasi del gruppo di acquisto quando si trova nello stato Bozza o Pubblicato. Se è pubblicato (in tempo reale), puoi eliminarlo solo se non è associato a un interesse per la soluzione. <a href="../buying-groups/buying-group-stages.md#delete-the-buying-group-stages-model">Ulteriori informazioni</a> |
| Miglioramento | Conteggi nodi percorsi | È stata migliorata la visibilità dei conteggi di appartenenza al percorso a livello di nodo. Utilizzare queste informazioni per convalidare la progressione dell&#39;account in un percorso. |

## Note sulla versione 2025.2

**Data di rilascio**: 11 marzo 2025

Questa versione include le nuove funzionalità e i miglioramenti seguenti:

| Tipo | Elemento | Descrizione |
| ---- | ---- | ----------- |
| Nuova funzionalità | Campi personalizzabili: frammenti di contenuto | In qualità di designer di frammenti di contenuto, puoi designare un parametro per un componente del frammento come modificabile. Questo consente all’autore del messaggio e-mail o del modello di specificare un valore di campo personalizzato specifico per le proprie esigenze. Questo flag di personalizzazione è limitato ai componenti visivi immagine, testo e pulsante. <a href="../content/fragment-authoring.md#enable-custom-fields">Ulteriori informazioni</a> |
| Nuova funzionalità | Ruoli incorporati B2B e autorizzazioni per il prodotto | Experience Platform ora include un set di ruoli incorporati (predefiniti) che puoi utilizzare per gestire l’accesso alle funzionalità dei prodotti B2B. <a href="../admin/user-management.md#b2b-built-in-roles">Ulteriori informazioni</a> <br/>Gli amministratori possono ora definire ruoli personalizzati in Adobe Experience Platform per includere le autorizzazioni per i prodotti Journey Optimizer B2B edition.  <a href="../admin/user-management.md#b2b-product-permissions">Ulteriori informazioni</a> |
| Nuova funzionalità | Tipi di duplicazione di percorso | Quando duplichi un percorso di account, puoi includere i dettagli del nodo, escluse le e-mail e i messaggi SMS creati in Journey Optimizer B2B edition. In alternativa, potete creare una copia di ossatura della struttura e dei flussi di tracciato, senza specificare i dettagli e le impostazioni del nodo. <a href="../journeys/journey-overview.md#duplicate-journey">Ulteriori informazioni</a> |
| Miglioramento | Altri quattro modelli e-mail di esempio | La libreria dei modelli e-mail di esempio ora include quattro modelli SecurFinacial come esempi di contenuto per coinvolgere di nuovo, informare, nutrire e fornire feedback |

## Note sulla versione 2025.1 {#Jan-2025}

**Data di rilascio**: 6 febbraio 2025

Questa versione include le nuove funzionalità e i miglioramenti seguenti:

| Tipo | Elemento | Descrizione |
| ---- | ---- | ----------- |
| Nuova funzionalità | Inoltro eventi esperienza | Gli amministratori possono configurare definizioni di eventi basate su Adobe Experience Platform (AEP). Queste configurazioni consentono agli addetti al marketing di creare percorsi di account che reagiscono agli eventi esperienza di AEP.  <a href="../admin/configure-aep-events.md">Ulteriori informazioni</a> |
| Nuova funzionalità | Destinazioni di media a pagamento | Qualifica le persone note per le campagne multimediali a pagamento da un percorso di account in modo da poterle coinvolgere ulteriormente su piattaforme pubblicitarie, come LinkedIn. Utilizza un nodo di percorsi suddivisi in un percorso di conti per segmentare i tipi di pubblico degli account in base a un comportamento specifico e identificare gli account che richiedono un coinvolgimento aggiuntivo. Quindi, aggiungi persone da tali account a un pubblico di clienti esterni tramite Real-time CDP a una destinazione di contenuti multimediali a pagamento supportata. <a href="../journeys/action-nodes.md#journey-optimizer-b2b-actions">Ulteriori informazioni</a> |
| Nuova funzionalità | Dashboard intelligente | Visualizza il progresso dei gruppi di acquisto attraverso i loro percorsi di account, comprese le informazioni generate dall’intelligenza artificiale per un’analisi più intelligente e una definizione precisa delle priorità degli account. <a href="../dashboards/intelligent-dashboard.md">Ulteriori informazioni</a> |
| Nuova funzionalità | Dettagli del gruppo di acquisto e dell’account | Visualizza informazioni a livello di gruppo di acquisto e di account per disporre di più dati contestuali e storici quando inizi a coinvolgere un cliente.<p>I dettagli del gruppo di acquisto includono qualsiasi intento di prime parti rilevato. <a href="../buying-groups/buying-group-details.md">Ulteriori informazioni</a><p>I conti dei dettagli account evidenziano l&#39;aumento del coinvolgimento rilevato intento, in modo da poter avvisare le vendite su account pronti per un impegno mirato alle vendite personalizzato.  <a href="../accounts/account-details.md">Ulteriori informazioni</a> |
| Nuova funzionalità | Panoramica sui percorsi | Quando si accede ai percorsi di account, la scheda Panoramica fornisce un&#39;istantanea completa dei percorsi di account attivi, con informazioni dettagliate sull&#39;avanzamento dell&#39;account utilizzando grafici a cerchi e a barre che categorizzano e quantificano i completamenti e le attività di coinvolgimento.  <a href="../dashboards/journeys-dashboard.md">Ulteriori informazioni</a> |
| Nuova funzionalità | Modifica delle immagini Adobe Express | Le azioni rapide di Adobe Express consentono di apportare semplici modifiche (ad esempio ritagliare e ridimensionare) alle immagini per conferire un aspetto più curato al contenuto. <a href="../content/image-edit-adobe-express.md#quick-actions-in-adobe-express">Ulteriori informazioni</a>  <p>Per un set più completo di strumenti di progettazione, questa integrazione consente di ottenere una licenza Adobe Express completa in Journey Optimizer B2B edition. Con questa configurazione, l’interfaccia utente completa di Adobe Express diventa accessibile all’interno dell’area di lavoro risorse locale. <a href="../content/image-edit-adobe-express.md#adobe-express-enterprise-license">Ulteriori informazioni</a> |
| Nuova funzionalità | Filtri intento per l’acquisto di ruoli di gruppo | Quando si inviano le parole chiave intento, il modello di rilevamento intento prevede una soluzione o un prodotto di interesse con sufficiente affidabilità in base all&#39;attività di un lead. <a href="../admin/intent-data.md">Ulteriori informazioni</a> <p>Questi dati di intento sono disponibili per definire le condizioni dei ruoli del gruppo di acquisto <a href="../buying-groups/buying-groups-role-templates.md#add-the-template-roles">Ulteriori informazioni</a> |
| Miglioramento | Supporto di eventi Marketo Engage in percorsi | Il nodo di percorso _Ascolta evento_ ora supporta due eventi Marketo Engage a livello di persone: _Visite alla pagina Web_ e _Compila modulo_. <a href="../journeys/listen-for-event-nodes.md#listen-for-marketo-engage-event">Ulteriori informazioni</a> |
| Miglioramento | Acquisto di filtri di gruppo per elenchi avanzati di Marketo Engage | Visualizza e crea elenchi avanzati con filtri per gruppi di acquisto in Marketo Engage. Questi filtri aggiunti ti consentono di eliminare e includere i membri del gruppo di acquisto in campagne e programmi Marketo Engage da percorsi di account in Journey Optimizer B2B edition. <a href="../buying-groups/marketo-engage-smart-list-buying-group-filters.md">Ulteriori informazioni</a> |
| Miglioramento | Filtro di iscrizione all’elenco Marketo Engage per percorsi e ruoli | In Journey Optimizer B2B, verifica l&#39;appartenenza all&#39;elenco Marketo Engage come condizione per un percorso _diviso da persone_ nodo per eliminare la duplicazione nelle attività di percorso. <a href="../journeys/split-merge-paths-nodes.md#add-a-split-path-by-people-node">Ulteriori informazioni</a> <p> Per l&#39;acquisto di modelli di ruoli di gruppo, utilizzare l&#39;appartenenza a un elenco come condizione del ruolo. <a href="../buying-groups/buying-groups-role-templates.md#add-the-template-roles">Ulteriori informazioni</a> |
| Miglioramento | Dashboard panoramica del coinvolgimento | Questa dashboard viene aggiornata per fornire una visione completa del coinvolgimento. Mostra metriche in tempo reale di account e interazioni individuali tramite grafici a cerchi istantanei e grafici a linee che rivelano le tendenze nel tempo. <a href="../dashboards/engagement-dashboard.md">Ulteriori informazioni</a> |


## Note sulla versione di ottobre 2024 {#Oct-2024}

**Data di rilascio**: 29 ottobre 2024

Questa versione include le nuove funzionalità e i miglioramenti seguenti:

| Tipo | Elemento | Descrizione |
| ---- | ---- | ----------- |
| Nuova funzionalità | Contenuto condizionale nei modelli e-mail | Personalizza il contenuto delle e-mail in base al comportamento del destinatario e alle caratteristiche del profilo, sia a livello di account che di lead. <p>Quando crei un’e-mail per il percorso di account nello spazio di progettazione visiva dell’e-mail, utilizza le regole condizionali per definire più varianti per qualsiasi componente di contenuto. <a href="../content/conditional-content.md">Ulteriori informazioni</a> |
| Nuova funzionalità | _Aggiungi all&#39;elenco_ e _Rimuovi dall&#39;elenco_ persone azioni in percorsi | Personalizza il contenuto delle e-mail in base al comportamento del destinatario e alle caratteristiche del profilo, sia a livello di account che di lead. <a href="../journeys/action-nodes.md">Ulteriori informazioni</a> |
| Nuova funzionalità | Governance dei contenuti e blocco dei componenti | Per garantire il rispetto delle progettazioni di contenuti approvate, utilizza le funzioni di governance dei contenuti per bloccare i componenti di contenuto dei modelli e-mail. Attivando la governance dei contenuti nel modello e-mail, gli esperti di marketing possono modificare solo gli elementi consentiti per mantenerli allineati alla strategia dei contenuti. <a href="../content/template-content-governance.md">Ulteriori informazioni</a> |
| Nuova funzionalità | Fasi del gruppo di acquisto | Quando definisci e pubblichi un modello di staging per gruppi di acquisto personalizzato, puoi tenere traccia della progressione del gruppo di acquisto attraverso le fasi del ciclo di vita del gruppo di acquisto. Utilizzare queste fasi per identificare le azioni migliori successive per i membri del gruppo di acquisto. Puoi configurare le regole di transizione e i nodi del percorso che determinano la progressione dell’area di visualizzazione e attivano le azioni in base alle modifiche. <a href="../buying-groups/buying-group-stages.md">Ulteriori informazioni</a> |
| Miglioramento | Nuovi modelli e-mail pronti all’uso | La libreria dei modelli di esempio ora include ulteriori modelli e-mail progettati per gli esperti di marketing B2B. Utilizza questi modelli di esempio come punto di partenza e aggiungi il tuo marchio e i tuoi messaggi. <a href="../content/email-templates.md#select-a-design-template">Ulteriori informazioni</a> |
| Miglioramento | Campi personalizzati come attributi persona | Se hai dei campi persona personalizzati definiti nello schema del pubblico dell’account in Experience Platform, questi campi sono disponibili per l’utilizzo come attributi persona in determinate condizioni. Utilizza questi attributi personalizzati in: <li>Modelli di ruoli <a href="../buying-groups/buying-groups-role-templates.md#add-the-template-roles">Ulteriori informazioni</a></li><li>Dividi percorsi per nodi percorso persone <a href="../journeys/split-merge-paths-nodes.md#add-a-split-path-by-people-node">Ulteriori informazioni</a></li> |
| Miglioramento | Impostazioni del canale e-mail | Le impostazioni e-mail sono ora visibili nell’interfaccia B2B edition di Journey Optimizer. Puoi rivedere rapidamente le configurazioni correnti e gli amministratori possono fare clic su _[!UICONTROL Modifica impostazioni]_ per passare direttamente alle impostazioni in Marketo Engage e aggiornarle in base ai requisiti della tua organizzazione. <a href="../admin/configure-channels-emails.md">Ulteriori informazioni</a> |

## Note sulla versione di settembre 2024 {#Sept-2024}

**Data di rilascio**: 7 ottobre 2024

Questa versione include le nuove funzionalità e i miglioramenti seguenti:

| Tipo | Elemento | Descrizione |
| ---- | ---- | ----------- |
| Miglioramento | Libreria risorse centrale | La _libreria di risorse centralizzata_ avanzata consente di utilizzare tutte le risorse immagine nell&#39;istanza di Marketo Engage, nelle aree di lavoro di Design Studio. Esistono guardrail integrati che impediscono le modifiche alle risorse Marketo Engage da Journey Optimizer B2B edition, nonché le operazioni di eliminazione e spostamento. Queste protezioni garantiscono la conservazione delle risorse di origine (Marketo Engage Design Studio) consentendo al tempo stesso la lettura e il riutilizzo senza interruzioni in Journey Optimizer B2B edition.<p>Per le risorse da utilizzare esclusivamente in Journey Optimizer B2B edition, un’area di lavoro specifica fornisce funzioni di gestione risorse complete. <a href="../content/marketo-engage-design-studio.md">Ulteriori informazioni</a> |
| Nuova funzionalità | Risorse utilizzate di recente | La home page dell&#39;app Journey Optimizer B2B edition ora include la sezione _[!UICONTROL Accesso recente]_, che fornisce un elenco delle risorse utilizzate più di recente dall&#39;addetto al marketing o dall&#39;amministratore. Puoi utilizzare questo elenco per passare direttamente alla risorsa su cui hai lavorato di recente senza passare attraverso una serie di pagine di risorse e senza effettuare ricerche. <p>L’elenco fornisce informazioni aggiuntive relative alla modifica, in modo da poter decidere quale delle risorse deve essere ulteriormente modificata dall’ultima sessione. Per le risorse e-mail, visualizza il percorso di account in cui viene utilizzata la risorsa e-mail. <a href="../home-page.md">Ulteriori informazioni</a> |
| Miglioramento | Nodo diviso percorso - riordina percorsi | Nei nodi di percorso suddivisi, il filtro dei percorsi viene valutato in ordine decrescente. Ogni persona o account procede lungo il primo percorso corrispondente. Per riordinare i percorsi definiti, fai clic sulle frecce in alto e in basso a destra di ciascuna scheda dei percorsi per spostarla in alto o in basso nell’elenco. <a href="../journeys/split-merge-paths-nodes.md#split-paths">Ulteriori informazioni</a> |
| Miglioramento | Nodo di suddivisione del percorso: attributi di condizione della cronologia attività aggiuntivi | Quando si utilizzano le condizioni per definire il filtro del percorso per un nodo suddiviso da persone, sono disponibili due attributi aggiuntivi: _E-mail aperta_ e _E-mail consegnata_. Queste aggiunte forniscono maggiore flessibilità per filtrare le persone nel percorso in base all’attività e-mail. <a href="../journeys/journey-nodes.md#split-paths">Ulteriori informazioni</a> |

## Note sulla versione di agosto 2024 {#Aug-2024}

**Data di rilascio**: 29 agosto 2024

Questa versione include le nuove funzionalità e i miglioramenti seguenti:

| Tipo | Elemento | Descrizione |
| ---- | ---- | ----------- |
| Nuova funzionalità | Tipi di pubblico associati all&#39;account LinkedIn | Genera tipi di pubblico di annunci LinkedIn tramite tipi di pubblico con corrispondenza dell’account, per aiutarti a riempire ruoli vuoti nei gruppi di acquisto. Definendo un set di filtri per gruppi di acquisto, puoi mantenere un pubblico abbinato a LinkedIn per eseguire il targeting dei potenziali clienti che corrispondono ai parametri del gruppo di acquisto. <p>Questa funzione sfrutta Destinazioni Experience Platform per gestire alcuni aspetti dell’integrazione. <a href="../data/linkedin-account-matched-audiences.md">Ulteriori informazioni</a> |
| Miglioramento | Ciclo di vita dello stato per i frammenti di contenuto visivo | I frammenti visivi vengono ora gestiti tramite un ciclo di vita dello stato. Lo stato del frammento determina la sua disponibilità per l’utilizzo in un messaggio e-mail o in un modello e-mail e le modifiche che puoi apportarvi. <p>Questo flusso di lavoro ottimizzato permette di gestire facilmente i contenuti riutilizzati in base al calendario delle comunicazioni e delle promozioni. <a href="../content/fragments.md#fragment-status-and-lifecycle">Ulteriori informazioni</a> |
