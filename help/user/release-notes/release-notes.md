---
title: Note sulla versione
description: Note sulla versione più recente per l’edizione B2B di Adobe Journey Optimizer
exl-id: 7d3f1c26-d8a6-4065-a70f-5b30cb975dc8
source-git-commit: 18a9f073f5c898d01c075611c6808d192d71dbc7
workflow-type: tm+mt
source-wordcount: '895'
ht-degree: 9%

---

# Note sulla versione di Journey Optimizer B2B edition

Adobe Journey Optimizer B2B edition offre continuamente nuove funzioni, miglioramenti alle funzioni esistenti e correzioni di bug.

Journey Optimizer B2B edition è stato sviluppato in modalità nativa su [!DNL Adobe Experience Platform] e ne eredita le innovazioni e i miglioramenti più recenti. Ulteriori informazioni su queste modifiche nelle [Note sulla versione di Adobe Experience Platform](https://experienceleague.adobe.com/it/docs/experience-platform/release-notes/latest){target="_blank"}.

Rivedi la [descrizione del prodotto](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer-b2b.html){target="_blank"} per informazioni su adesioni, guardrail delle prestazioni e limitazioni.

## Note sulla versione di ottobre 2024 {#Oct-2024}

**Data di rilascio**: 29 ottobre 2024

Questa versione include le nuove funzionalità e i miglioramenti seguenti:

| Tipo | Elemento | Descrizione |
| ---- | ---- | ----------- |
| Nuova funzionalità | Contenuto condizionale nei modelli e-mail | Personalizza il contenuto delle e-mail in base al comportamento del destinatario e alle caratteristiche del profilo, sia a livello di account che di lead. <p>Quando crei un’e-mail per il percorso di account in e-mail designer, utilizza le regole condizionali per definire più varianti per qualsiasi componente di contenuto. <a href="../content/conditional-content.md">Ulteriori informazioni</a> |
| Nuova funzionalità | _Aggiungi all&#39;elenco_ e _Rimuovi dall&#39;elenco_ persone azioni in percorsi | Personalizza il contenuto delle e-mail in base al comportamento del destinatario e alle caratteristiche del profilo, sia a livello di account che di lead. <a href="../journeys/journey-nodes.md#action-nodes">Ulteriori informazioni</a> |
| Nuova funzionalità | Governance dei contenuti e blocco dei componenti | Per garantire il rispetto delle progettazioni di contenuti approvate, utilizza le funzioni di governance dei contenuti per bloccare i componenti di contenuto dei modelli e-mail. Attivando la governance dei contenuti nel modello e-mail, gli esperti di marketing possono modificare solo gli elementi consentiti per mantenerli allineati alla strategia dei contenuti. <a href="../content/template-content-governance.md">Ulteriori informazioni</a> |
| Nuova funzionalità | Fasi del gruppo di acquisto | Quando definisci e pubblichi un modello di staging per gruppi di acquisto personalizzato, puoi tenere traccia della progressione del gruppo di acquisto attraverso le fasi del ciclo di vita del gruppo di acquisto. Utilizzare queste fasi per identificare le azioni migliori successive per i membri del gruppo di acquisto. Puoi configurare le regole di transizione e i nodi del percorso che determinano la progressione dell’area di visualizzazione e attivano le azioni in base alle modifiche. <a href="../buying-groups/buying-group-stages.md">Ulteriori informazioni</a> |
| Miglioramento | Nuovi modelli e-mail pronti all’uso | La libreria dei modelli di esempio ora include ulteriori modelli e-mail progettati per gli esperti di marketing B2B. Utilizza questi modelli di esempio come punto di partenza e aggiungi il tuo marchio e i tuoi messaggi. <a href="../content/email-templates.md#select-a-design-template">Ulteriori informazioni</a> |
| Miglioramento | Campi personalizzati come attributi persona | Se nello schema di pubblico dell’account di Experience Platform sono definiti campi persona personalizzati, questi campi sono disponibili anche per l’utilizzo come attributi persona in determinate condizioni. Utilizza questi attributi personalizzati in: <li>Modelli di ruoli <a href="../buying-groups/buying-groups-role-templates.md#add-the-template-roles">Ulteriori informazioni</a></li><li>Dividi percorsi per nodi percorso persone <a href="../journeys/journey-nodes.md#add-a-split-path-by-people-node">Ulteriori informazioni</a></li> |
| Miglioramento | Impostazioni del canale e-mail | Le impostazioni e-mail sono ora visibili nell’interfaccia B2B edition di Journey Optimizer. Puoi rivedere rapidamente le configurazioni correnti e gli amministratori possono fare clic su _[!UICONTROL Modifica impostazioni]_ per passare direttamente alle impostazioni nel Marketo Engage e aggiornarle in base ai requisiti della tua organizzazione. <a href="../admin/configure-channels-emails.md">Ulteriori informazioni</a> |

## Note sulla versione di settembre 2024 {#Sept-2024}

**Data di rilascio**: 7 ottobre 2024

Questa versione include le nuove funzionalità e i miglioramenti seguenti:

| Tipo | Elemento | Descrizione |
| ---- | ---- | ----------- |
| Miglioramento | Libreria risorse centrale | La _libreria di risorse centralizzata_ avanzata consente di utilizzare tutte le risorse immagine nell&#39;istanza di Marketo Engage, nelle aree di lavoro di Design Studio. Esistono guardrail integrati che impediscono le modifiche alle risorse di Marketo Engage da Journey Optimizer B2B edition, nonché le operazioni di eliminazione e spostamento. Queste protezioni garantiscono che le risorse di origine (Marketo Engage Design Studio) vengano mantenute e consentono la lettura e il riutilizzo senza interruzioni in Journey Optimizer B2B edition.<p>Per le risorse da utilizzare esclusivamente in Journey Optimizer B2B edition, un’area di lavoro specifica fornisce funzioni di gestione risorse complete. <a href="../content/marketo-engage-design-studio.md">Ulteriori informazioni</a> |
| Nuova funzionalità | Risorse utilizzate di recente | La home page dell&#39;app Journey Optimizer B2B edition ora include la sezione _[!UICONTROL Accesso recente]_, che fornisce un elenco delle risorse utilizzate più di recente dall&#39;addetto al marketing o dall&#39;amministratore. Puoi utilizzare questo elenco per passare direttamente alla risorsa su cui hai lavorato di recente senza passare attraverso una serie di pagine di risorse e senza effettuare ricerche. <p>L’elenco fornisce informazioni aggiuntive relative alla modifica, in modo da poter decidere quale delle risorse deve essere ulteriormente modificata dall’ultima sessione. Per le risorse e-mail, visualizza il percorso di account in cui viene utilizzata la risorsa e-mail. <a href="../home-page.md">Ulteriori informazioni</a> |
| Miglioramento | Nodo diviso percorso - riordina percorsi | Nei nodi di percorso suddivisi, il filtro dei percorsi viene valutato in ordine decrescente. Ogni persona o account procede lungo il primo percorso corrispondente. Per riordinare i percorsi definiti, fai clic sulle frecce in alto e in basso a destra di ciascuna scheda dei percorsi per spostarla in alto o in basso nell’elenco. <a href="../journeys/journey-nodes.md#split-paths">Ulteriori informazioni</a> |
| Miglioramento | Nodo di suddivisione del percorso: attributi di condizione della cronologia attività aggiuntivi | Quando si utilizzano le condizioni per definire il filtro del percorso per un nodo suddiviso da persone, sono disponibili due attributi aggiuntivi: _E-mail aperta_ e _E-mail consegnata_. Queste aggiunte forniscono maggiore flessibilità per filtrare le persone nel percorso in base all’attività e-mail. <a href="../journeys/journey-nodes.md#split-paths">Ulteriori informazioni</a> |

## Note sulla versione di agosto 2024 {#Aug-2024}

**Data di rilascio**: 29 agosto 2024

Questa versione include le nuove funzionalità e i miglioramenti seguenti:

| Tipo | Elemento | Descrizione |
| ---- | ---- | ----------- |
| Nuova funzionalità | Pubblico con account linkedIn corrispondente | Genera tipi di pubblico di LinkedIn Ad tramite tipi di pubblico corrispondenti all’account per aiutarti a riempire i ruoli vuoti nei gruppi di acquisto. Definendo un set di filtri per gruppi di acquisto, puoi mantenere un pubblico abbinato a LinkedIn per eseguire il targeting dei potenziali clienti che corrispondono ai parametri del gruppo di acquisto. <p>Questa funzione sfrutta Destinazioni Experience Platform per gestire alcuni aspetti dell’integrazione. <a href="../data/linkedin-account-matched-audiences.md">Ulteriori informazioni</a> |
| Miglioramento | Ciclo di vita dello stato per i frammenti di contenuto visivo | I frammenti visivi vengono ora gestiti tramite un ciclo di vita dello stato. Lo stato del frammento determina la sua disponibilità per l’utilizzo in un messaggio e-mail o in un modello e-mail e le modifiche che puoi apportarvi. <p>Questo flusso di lavoro ottimizzato permette di gestire facilmente i contenuti riutilizzati in base al calendario delle comunicazioni e delle promozioni. <a href="../content/fragments.md#fragment-status-and-lifecycle">Ulteriori informazioni</a> |
