---
title: IA generativa per i contenuti
description: Scopri come creare e-mail e pagine di destinazione personalizzate con IA generativa in [!DNL Journey Optimizer B2B Edition], incluse le best practice per richiedere conferma.
feature: AI Assistant, Generative AI, Content
level: Beginner
topic: Artificial Intelligence
role: User
exl-id: 36baf7f9-2fff-4c33-bca0-7d43ec48e74a
source-git-commit: ce4df9a2726cf842c088738521b3e5dd88dd768f
workflow-type: tm+mt
source-wordcount: '2506'
ht-degree: 2%

---

# IA generativa per i contenuti {#generative-ai-content}

>[!CONTEXTUALHELP]
>id="ajo_b2b_ai-generation-settings"
>title="Generazione di contenuti AI"
>abstract="Dopo aver creato il layout, puoi utilizzare strumenti di intelligenza artificiale generativi in [!DNL Journey Optimizer B2B Edition] per migliorare i contenuti. Questa funzione semplifica il processo di personalizzazione e miglioramento dei contenuti ottimizzandoli in base al prompt descrittivo."

>[!CONTEXTUALHELP]
>id="ajo_b2b_ai-generation-reference-context"
>title="Contenuto di riferimento"
>abstract="Utilizza _Contenuto di riferimento_ per caricare un file di risorse contenente contenuto che fornisce ulteriore contesto per l&#39;intelligenza artificiale generativa in [!DNL Journey Optimizer B2B Edition] o per selezionare un file caricato in precedenza. Questa opzione garantisce che tutti i materiali necessari siano disponibili per migliorare la qualità e la pertinenza dei contenuti generati."

>[!CONTEXTUALHELP]
>id="ajo_b2b_ai-generation-start"
>title="Termini di intelligenza artificiale generativi di Adobe"
>abstract="L’accesso a questa funzione è soggetto al consenso alle Linee guida per l’utente dell’IA generativa di Adobe Experience Cloud. Esamina l’eventuale output di questa funzione per verificarne la precisione e assicurati che sia appropriato per il tuo caso d’uso."
>additional-url="https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html" text="Linee guida per l’utente sull’intelligenza artificiale generativa di Adobe"

L&#39;intelligenza artificiale generativa per il contenuto in [!DNL Adobe Journey Optimizer B2B Edition], basata su Microsoft Azure OpenAI e Adobe Firefly, fornisce suggerimenti proattivi per la variazione dei contenuti per testo e immagini. Ottimizza l’impatto dei contenuti sperimentando con diversi titoli e immagini principali.

Utilizzare le funzionalità di intelligenza artificiale generativa per la creazione di contenuti in [!DNL Journey Optimizer B2B Edition] per sfruttare le funzionalità di intelligenza artificiale generativa di Adobe. Crea testo e immagini personalizzati per e-mail, messaggi SMS, pagine di destinazione e altro ancora. Quando si crea una campagna completa o si perfezionano semplicemente risorse specifiche, queste funzioni consentono di allineare i contenuti in modo semplice alle linee guida del marchio, risparmiando tempo prezioso.

<!--
Generate multiple variants and build an experiment to compare them. Leveraging Journey Optimizer Content Experiment, you can define multiple message treatments to measure which one performs best for your target audience. You can choose to vary the delivery content, or subject. The message audience is randomly allocated to each treatment to determine which one works best in terms of the specified metric. Learn more about Content Experiment in this section. -->

>[!IMPORTANT]
>
>Per accedere a queste funzionalità in [!DNL Journey Optimizer B2B Edition], è necessario disporre dell&#39;autorizzazione _[!UICONTROL Assistente AI]_ > _[!UICONTROL Genera contenuto]_. Per ulteriori informazioni su come un amministratore di prodotto può concedere le autorizzazioni per le funzionalità, vedere [Modifica ruoli per le autorizzazioni per il prodotto](../admin/user-management.md#edit-roles-for-product-permissions).

Gli strumenti di AI Assistant per la generazione di contenuti sono supportati con i seguenti tipi di risorse:

* [E-mail](../content/ai-assistant-emails.md)
* [!BADGE Beta] [Pagine di destinazione](../content/ai-assistant-landing-pages.md)

## Linee guida e limitazioni generali {#general-guidelines-and-limitations}

L&#39;utilizzo delle funzionalità di IA generativa è soggetto alle [linee guida per l&#39;utente di IA generativa di Adobe Experience Cloud](https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html){target="_blank"}. Con l&#39;impegno di Adobe per la trasparenza nell&#39;utilizzo degli strumenti di intelligenza artificiale generativi per la creazione di contenuti multimediali, Adobe applica [credenziali contenuto](https://helpx.adobe.com/firefly/web/get-started/learn-the-basics/content-credentials-overview.html){target="_blank"} a qualsiasi contenuto o progetto che include una risorsa generata da [!DNL Firefly] al momento del download o dell&#39;esportazione.

Rivedi le seguenti linee guida generali per l&#39;utilizzo di IA generativa per il contenuto in [!DNL Journey Optimizer B2B Edition]:

* Utilizza prompt ben definiti per il modello di intelligenza artificiale generativo per interpretare con precisione. L’obiettivo di marketing o la richiesta che fornisci influisce fortemente sulla qualità del contenuto generato.

* Carica i file di riferimento dei contenuti per ottenere contenuti precisi per il brand. In caso contrario, il contenuto si basa su informazioni disponibili pubblicamente. Il contenuto caricato può essere nei seguenti formati di file: PDF, JPEG, PNG o ZIP (contenenti i formati di file supportati). La dimensione massima per un file caricato è di 50 MB. È possibile utilizzare file più grandi o un numero elevato di immagini, ma questo aumenta il tempo di elaborazione.

* Utilizza un modello personalizzato o specifico per il brand per creare i contenuti delle e-mail. Si consigliano modelli e-mail con un massimo di 8-10 immagini.

* Assicurati di segnalare eventuali output problematici utilizzando le icone thumb up, thumb down o flag durante la selezione delle varianti.

## Best practice per l’intelligenza artificiale generativa {#generative-ai-prompting-guide}

>[!CONTEXTUALHELP]
>id="ajo_b2b_ai_content_prompt"
>title="Suggerimenti per i prompt"
>abstract="Esplora la documentazione di [!DNL Journey Optimizer B2B Edition] per scoprire come creare prompt efficaci che producono contenuti di marketing on-brand ad alta conversione."

Questa guida ti aiuta a strutturare le richieste, comunicare le intenzioni con chiarezza e garantire che l’intelligenza artificiale produca messaggi in linea con le linee guida del tuo marchio, le esigenze del pubblico e gli obiettivi della campagna.

Scopri come scrivere prompt efficaci che consentano all’Assistente AI di generare contenuti di marketing di alta qualità e personalizzati per i tuoi obiettivi.

### Utilizzare il framework CO-STAR {#costar-framework}

Per ottenere risultati ottimali con i contenuti generati, organizza le richieste utilizzando il framework CO-STAR. Questo approccio strutturato fornisce chiarezza per ciò che vi serve.

| Componente | Che cosa significa | Perché è importante |
| --- | ---- | ------ |
| **C - Contesto** | Informazioni sulla campagna, sul prodotto o sulla situazione | Comprensione per il quadro generale |
| **O - Obiettivo** | Il tuo obiettivo di marketing specifico | Guida gli obiettivi dei contenuti |
| **S - Stile** | Modalità di comunicazione | Imposta l&#39;approccio |
| **T - Tono** | Stile e voce emotivi | Forma l&#39;impatto del messaggio |
| **A - Pubblico** | Il pubblico di destinazione | Assicura che il messaggio risuoni con le persone giuste |
| **R - Requisiti** | Vincoli specifici o requisiti obbligatori | Definisce limiti ed elementi critici |

{style="table-layout:fixed"}

### Nozioni di base sulla richiesta {#key-takeaways}

<table style="table-layout: fixed; width: 100%; border: 0;">
<thead style="border: 0; background-color: #FFFFFF;">
<tr>
<th>Esegui</th>
<th>Non</th>
</tr>
</thead>
<tbody>
<tr style="border: 0;">
<td>
<ul><li>Utilizzare il framework CO-STAR per la struttura
<li>Chiarezza sui contenuti nuovi rispetto a quelli esistenti
<li>Fornire indicazioni specifiche sull’estrazione per l’utilizzo dei documenti
<li>Effettuare selezioni per il tono, la strategia e la lingua
<li>Corrispondenza tra obiettivi di marketing e funzionalità per tipi di contenuto
<li>Generare più varianti per il test A/B</ul>
</td>
<td>
<ul><li>Richiedere modifiche strutturali, stili o modifiche di immagini nei prompt
<li>Menziona tono/strategia nei prompt, se disponibile nelle opzioni
<li>Usa obiettivi vaghi come _promuove il prodotto_
<li>Richiedi selezioni elementi condizionali
<li>Prevista modifica del layout tramite prompt</ul>
</td>
</tr>
</tbody>
</table>

### Contenuto non supportato nei prompt

>[!TIP]
>
>Utilizzare gli strumenti di progettazione o [!DNL Adobe Express] per apportare modifiche visive o di immagine.

Le seguenti richieste sono **_non supportate_** e devono essere gestite tramite altri strumenti:

<table style="table-layout: fixed; border: 0;">
<thead style="border: 0; background-color: #FFFFFF">
<tr>
<th><img src="../../assets/do-not-localize/check-box-red.svg" alt="Croce rossa in uscita">  Modifiche alla struttura delle e-mail</th>
<th><img src="../../assets/do-not-localize/check-box-red.svg" alt="Croce rossa in uscita">  Modifiche allo stile visivo</th>
<th><img src="../../assets/do-not-localize/check-box-red.svg" alt="Croce rossa in uscita">  Operazioni di modifica delle immagini</th>
</tr>
</thead>
<tbody>
<tr style="border: 0;">
<td>
<ul>
<li>Selezione di sezioni specifiche da modificare</li>
<li>Eliminazione o clonazione di elementi</li>
<li>Selezioni condizionali</li>
<li>Aggiunta o rimozione di sezioni layout</li>
</ul>
</td>
<td>
<ul>
<li>Formattazione del testo (grassetto, corsivo, dimensione carattere)</li>
<li>Modifiche colore</li>
<li>Stile layout (bordi, spaziatura interna, margini)</li>
<li>Effetti visivi (ombre)</li>
</ul>
</td>
<td>
<ul>
<li>Modifiche di sfondo</li>
<li>Aggiunta di sovrapposizioni di testo o logo</li>
<li>Ritaglio o ridimensionamento delle immagini</li>
<li>Regolazioni colore</li>
<li>Sostituzione immagine</li>
</ul>
</td>
</tr>
</tbody>
</table>

### Lista di controllo qualità {#quality-checklist}

Prima di generare il contenuto, verifica quanto segue:

![Segno di spunta verde](../../assets/do-not-localize/check-box-green.svg){width="20"} **Cancella obiettivo**: indica chiaramente l&#39;azione, il prodotto/servizio, il valore e il contesto.

![Segno di spunta verde](../../assets/do-not-localize/check-box-green.svg){width="20"} **Pubblico di destinazione definito**: specifica il gruppo demografico, la mansione o il segmento.

![Segno di spunta verde](../../assets/do-not-localize/check-box-green.svg){width="20"} **Allineamento tipo di contenuto**: l&#39;obiettivo corrisponde al canale o al formato selezionato.

![Segno di spunta verde](../../assets/do-not-localize/check-box-green.svg){width="20"} **Controlla selezioni**: sono stati selezionati il tono, la strategia e le impostazioni locali, non includerli nel prompt.

![Segno di spunta verde](../../assets/do-not-localize/check-box-green.svg){width="20"} **Lo stato attivo del documento è specificato**: evidenzia il contenuto o le sezioni a cui fare riferimento.

![Segno di spunta verde](../../assets/do-not-localize/check-box-green.svg){width="20"} **Marchio applicato**: sono state selezionate le linee guida del marchio appropriate.

![Segno di spunta verde](../../assets/do-not-localize/check-box-green.svg){width="20"} **Ambito realistico**: evita richieste di modifiche di layout, stile o struttura.

### Obiettivi di marketing efficaci {#marketing-objectives}

Quando definisci gli obiettivi di marketing, assicurati che siano chiari, utilizzabili e misurabili. Evita istruzioni vaghe o generiche.

**Esempi di obiettivi validi:**

![Segno di spunta verde](../../assets/do-not-localize/check-box-green.svg){width="20"} &quot;Effettua le iscrizioni per la versione di prova gratuita di 30 giorni del nuovo dashboard di analisi basato sull&#39;intelligenza artificiale&quot;

![Segno di spunta verde](../../assets/do-not-localize/check-box-green.svg){width="20"} &quot;Genera lead per il webinar B2B su &quot;Riduzione dei costi cloud del 40%&quot; in programma dal 15 marzo&quot;

![Segno di spunta verde](../../assets/do-not-localize/check-box-green.svg){width="20"} &quot;Promuovi lo sconto limitato del 25% sugli abbonamenti premium, fino al 25 dicembre&quot;

**Esempi da evitare:**

![Croce rossa](../../assets/do-not-localize/check-box-red.svg){width="20"} &quot;Promuovi il prodotto&quot; (troppo vago)

![Croce rossa](../../assets/do-not-localize/check-box-red.svg){width="20"} &quot;Fai firmare le offerte alle persone&quot; (valore non chiaro)

![Croce rossa](../../assets/do-not-localize/check-box-red.svg){width="20"} &quot;E-mail sulle nuove funzioni&quot; (manca lo scopo)

#### Strutturare l&#39;obiettivo

Fornisci sempre contesto e proposta di valore per la produzione di contenuti rilevanti. Usa la formula seguente per scrivere obiettivi efficaci: **Azione + Prodotto/Servizio + Valore/Beneficio + Urgenza/Contesto**

**Esempi di obiettivi validi:**

![Segno di spunta verde](../../assets/do-not-localize/check-box-green.svg){width="20"} &quot;Incoraggia il download della nuova app mobile che aiuta gli utenti a tenere traccia di abitudini di vita sostenibili con consigli personalizzati ed ecocompatibili&quot;

![Segno di spunta verde](../../assets/do-not-localize/check-box-green.svg){width="20"} &quot;Promuovi la registrazione per il workshop esclusivo sulle tecniche avanzate di visualizzazione dei dati per i professionisti del marketing&quot;

![Segno di spunta verde](../../assets/do-not-localize/check-box-green.svg){width="20"} &quot;Partecipazione all&#39;evento di lancio del prodotto con il rivoluzionario assistente di scrittura AI che consente di risparmiare più di 5 ore a settimana&quot;

**Esempi da evitare:**

![Croce rossa](../../assets/do-not-localize/check-box-red.svg){width="20"} &quot;Annuncio nuova app&quot; (proposta di valore e contesto mancanti)

![Croce rossa](../../assets/do-not-localize/check-box-red.svg){width="20"} &quot;Invita le persone a iscriversi al workshop&quot; (manca specificità su pubblico e vantaggi)

![Croce rossa](../../assets/do-not-localize/check-box-red.svg){width="20"} &quot;Promuovi evento&quot; (nessuna azione, valore o urgenza chiari)

#### Esempio di prompt per tipo di canale {#channel-type-practices}

<table style="table-layout: auto; border: 0;">
<thead>
<tr style="border: 0;background-color: #FFFFFF;">
<th>Canale</th>
<th>Esempio</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>E-mail</strong></td>
<td>"Sviluppa i potenziali clienti aziendali presentando tre storie di successo dei clienti con metriche dettagliate sul ROI (Oracle: riduzione dei costi del 45%, Accenture: aumento del lead del 200%, Microsoft: risparmio di tempo del 60%). Responsabili IT di aziende con più di 1000 dipendenti"</td>
</tr>
<tr>
<td><strong>Pagine di destinazione</strong></td>
<td>"Converti i visitatori B2B in lead qualificati dimostrando come la soluzione di sicurezza aziendale impedisce il 99,9% degli attacchi informatici, con testimonianze Fortune 500 e audit di sicurezza gratuiti"</td>
</tr>
</tbody>
</table>

<!-- channels not yet supported
<tr>
<td><strong>SMS</strong></td>
<td>"Alert VIP customers about a 4-hour flash sale on premium electronics with 40% discount, limited to the first 100 customers"</td>
</tr>
<tr>
<td><strong>Push Notifications</strong></td>
<td>"Re-engage users who haven't opened the app in 7 days with personalized content recommendations based on their reading history"</td>
</tr> -->

<!-- Wait on more B2B specific examples

### Industry-specific approaches {#industry-approaches}

<table style="table-layout: fixed; border-collapse: collapse; border: 0;">
<thead>
<tr style="border: 0;background-color: #FFFFFF;">
<th>Industry</th>
<th>Example Prompt</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>B2B Technology</strong></td>
<td>"Demonstrate ROI and technical specifications while addressing security concerns for IT decision-makers evaluating our cloud infrastructure solution, emphasizing 99.9% uptime SLA, SOC 2 compliance, and 40% cost savings."</td>
</tr>
<tr>
<td><strong>E-commerce Retail</strong></td>
<td>"Create urgency around limited-stock holiday items while highlighting free shipping and easy returns for last-minute shoppers, emphasizing limited quantities (less than 50 remaining) and 24-hour shipping cutoff."</td>
</tr>
<tr>
<td><strong>Financial Services</strong></td>
<td>"Educate clients about investment portfolio diversification strategies while maintaining regulatory compliance, featuring certified financial advisor insights and risk disclaimers."</td>
</tr>
<tr>
<td><strong>Healthcare & Wellness</strong></td>
<td>"Promote preventive care benefits and annual health screenings while maintaining medical accuracy, featuring board-certified physician recommendations and patient privacy assurances."</td>
</tr>
<tr>
<td><strong>Education & Training</strong></td>
<td>"Emphasize career advancement outcomes and industry certifications while showcasing instructor expertise, highlighting 92% job placement rate and project-based curriculum."</td>
</tr>
<tr>
<td><strong>SaaS Platforms</strong></td>
<td>"Highlight time savings and automation benefits with specific metrics while addressing integration concerns, featuring average 25-hour weekly time savings and integration with 200+ popular tools."</td>
</tr>
</tbody>
</table>
 -->

### Nuovi contenuti e modifica di quelli esistenti {#new-vs-modify}

Indica chiaramente se la richiesta comporta la generazione di nuovo contenuto o l&#39;aggiornamento del materiale esistente. Questa distinzione è importante perché guida l’intelligenza artificiale nella selezione dell’approccio appropriato e garantisce un risultato più accurato e utile.

#### Creazione di nuovi contenuti

Applica questa strategia quando avvii campagne di marketing, riveli nuove soluzioni o avvii comunicazioni aggiornate/aggiornate. In questo modo il messaggio inizia forte e si allinea agli obiettivi.

**Come richiedere** ➤ Quando crei un nuovo contenuto, concentrati sul tuo obiettivo di marketing senza fare riferimento a contenuto esistente.

>[!BEGINSHADEBOX &quot;Esempi&quot;]

* **Versione di prova SaaS**: &quot;Lancia il nuovo software CRM per i proprietari di piccole imprese, evidenziando un risparmio di tempo del 50%, una qualificazione del lead più veloce del 90% e offrendo una prova gratuita di 30 giorni con onboarding personalizzato&quot;
* **Annuncio sulle funzionalità**: &quot;Annuncio di nuove funzionalità di integrazione API che riducono i tempi di sviluppo del 60% per i clienti aziendali, con targeting per i decision-maker tecnici&quot;
* **Promozione evento**: &quot;Registrazioni del webinar su &#39;Tendenze di marketing digitale 2024&#39; con la partecipazione di esperti di Google, Meta e Adobe, con particolare attenzione alle informazioni fruibili e alle postazioni limitate (massimo 500)&quot;

>[!ENDSHADEBOX]

#### Modifica del contenuto esistente

>[!TIP]
>
>Per le modifiche standard come elaborate, riepilogate o semplificate, selezionare **_Perfeziona_** invece di scrivere prompt personalizzati.

Invia una richiesta di modifica quando devi aggiornare, aggiornare o adattare le campagne di marketing correnti. Questo metodo supporta miglioramenti incrementali, garantendo che i messaggi rimangano pertinenti senza iniziare da zero.

**Come richiedere** ➤ Quando modifichi il contenuto esistente, specifica chiaramente ciò che desideri modificare e come modificarlo.

>[!BEGINSHADEBOX &quot;Esempi&quot;]

* **Aggiornamento della campagna**: &quot;Modifica l&#39;e-mail di avvio del programma per concentrarti sulle funzionalità di sicurezza aziendale anziché sui vantaggi generali in termini di produttività, indirizzando i responsabili delle decisioni IT con certificazioni di conformità&quot;
* **Audience Pivot**: &quot;Adatta l&#39;invito demo software per eseguire in modo specifico il targeting dell&#39;assistenza sanitaria, sostituendo esempi generici con casi di utilizzo dell&#39;assistenza sanitaria e vantaggi in termini di conformità HIPAA&quot;
* **Aggiornamento stagionale**: &quot;Aggiorna la campagna promozionale Q3 per lo shopping durante le vacanze Q4, cambiando l&#39;attenzione dal back-to-school al regalo per le vacanze con l&#39;enfasi della spedizione rapida&quot;

>[!ENDSHADEBOX]

## Impostazioni avanzate testo {#text-settings}

Oltre a utilizzare un prompt chiaro e ben formato, le impostazioni di testo negli strumenti di contenuto dell’Assistente AI includono impostazioni di testo che è possibile utilizzare per ottimizzare gli output generati.

>[!TIP]
>
>Utilizza le opzioni _[!UICONTROL Strategia di comunicazione]_ e _[!UICONTROL Tono]_ nelle _[!UICONTROL Impostazioni testo]_ invece di menzionare queste caratteristiche nel prompt.

### Tipi di strategie di comunicazione

La tua strategia di comunicazione determina il modo in cui presenterai il messaggio per massimizzare l’impatto. Diverse strategie funzionano meglio per diversi obiettivi, che tu stia costruendo l&#39;urgenza, stabilendo la fiducia, o guidando l&#39;azione immediata. Scegli la strategia che meglio si allinea agli obiettivi della campagna e alla mentalità del pubblico.

| **Strategia** | **Ottimo per** | **Stile messaggistica** | **Esempi** |
| ------------ | ------------ | ------------------- | ------------ |
| **Urgente** | Offerte sensibili al tempo, scadenze, azioni immediate | Crea una pressione immediata con un linguaggio basato sul tempo | <li>&quot;Agisci subito: l’offerta scade a mezzanotte&quot; <li>&quot;Registrati oggi stesso prima che gli spot si riempiono&quot; <li>&quot;La vendita flash da 48 ore inizia ora&quot; |
| **FOMO (paura di perdere)** | Offerte limitate, eventi, accesso esclusivo | Utilizza segnali di urgenza, scarsità e pressione temporale | <li>&quot;Mancano solo 24 ore! Scorte limitate al 40% di sconto&quot; <li>&quot;Ultima possibilità: domani il prezzo anticipato degli uccelli&quot; <li>&quot;Rimangono solo 100 punti beta&quot; |
| **Bozza social** | Trust-building, testimonianze, prodotti popolari | Sfrutta le esperienze altrui e la convalida | <li>&quot;Unisciti a oltre 50.000 clienti soddisfatti&quot; <li>&quot;Valutazione 4,9/5 stelle da parte di professionisti del settore&quot; <li>&quot;Affidabile per le aziende Fortune 500&quot; |
| **Scarsità** | Scorte limitate, rilasci esclusivi, articoli a forte domanda | Evidenzia la disponibilità e l&#39;esclusività limitate | <li>&quot;Ne rimangono solo 5 scorte&quot; <li>&quot;Edizione limitata: 100 unità disponibili&quot; <li>&quot;Rilascio esclusivo: primo arrivato, primo servito&quot; |
| **Incentivo** | Promozioni, programmi di premi, offerte speciali | Vantaggi e ricompense tangibili | <li>&quot;Sconto del 20% sul primo ordine&quot; <li>&quot;Guadagna punti doppio questo fine settimana&quot; <li>&quot;Spedizione gratuita per ordini superiori a $50&quot; |
| **Esclusività** | Prodotti Premium, esperienze VIP, offerte per soli membri | Utilizza il posizionamento premium e un linguaggio ad accesso speciale | <li>&quot;Invito esclusivo a un&#39;anteprima privata&quot; <li>&quot;L’appartenenza a un’élite sblocca le analisi avanzate&quot; <li>&quot;Unisciti a determinate aziende Fortune 500 che già ci utilizzano&quot; |
| **Gamification** | Campagne di coinvolgimento, programmi fedeltà, contenuti interattivi | Utilizza meccaniche di gioco e linguaggio di realizzazione | <li>&quot;Sblocca il tuo prossimo livello di premio&quot; <li>&quot;Sfide complete per guadagnare distintivi&quot; <li>&quot;Scala la classifica dei premi esclusivi&quot; |
| **Informativo** | Istruzione, ricerca, prodotti complessi, leadership di pensiero | Utilizza fatti, dati, informazioni e spiegazione | <li>&quot;5 informazioni dall’analisi di oltre 10.000 interazioni&quot; <li>&quot;Nuove ricerche rivelano 3 approcci rivoluzionari&quot; <li>&quot;Guida completa all’implementazione dell’intelligenza artificiale nel marketing&quot; |
| **Istruzione e approfondimenti** | Contenuti di apprendimento, tendenze del settore, best practice | Fornisce conoscenze preziose e soluzioni actionable | <li>&quot;Scopri tecniche avanzate con una guida esperta&quot; <li>&quot;Scopri 7 strategie utilizzate dai principali esperti di marketing&quot; <li>&quot;Scopri come ottimizzare il flusso di lavoro in 5 passaggi&quot; |

### Imposta il tono giusto {#tone}

Il tono determina il modo in cui il pubblico percepisce il messaggio e lo risponde. Seleziona sempre un tono che sia allineato alla voce del brand e all’area di visualizzazione del percorso di profili.

Rivedi le opzioni dei toni disponibili, tra cui quando ciascuno funziona al meglio ed esempi di contenuto che si adattano a ogni stile.

| Tonalità | Ideale per | Esempio di contenuto |
| ---- | ----- | ----- |
| Professionale | Comunicazioni B2B, annunci formali | &quot;Siamo lieti di annunciare la nostra partnership strategica...&quot; |
| Empatico | Assistenza clienti, argomenti sensibili | &quot;Capiamo quanto questo problema possa essere frustrante per te...&quot; |
| Umoristico | Campagne coinvolgenti, contenuti dal cuore leggero | &quot;Avvertenza: può causare gravi aumenti di produttività!&quot; |
| Eccitante | Lancio di prodotti, promozioni di eventi | &quot;Questo è il momento che stavi aspettando!&quot; |
| Ispirativo | Campagne motivazionali, scopo del brand | &quot;Insieme possiamo fare la differenza nel mondo...&quot; |
| Persuasivo | Campagne di vendita, conversioni | &quot;Non perdete questa opportunità limitata di...&quot; |
| Amichevole | Coinvolgimento del cliente, messaggi di benvenuto | &quot;Sono contento che tu sia qui con noi!&quot; |
| Formale | Comunicazioni legali, comunicazioni ufficiali | &quot;Questa è una notifica delle seguenti modifiche...&quot; |
| Scusante | Ripristino del servizio, risoluzione dei problemi | &quot;Bodea si scusa sinceramente per ogni disagio causato...&quot; |
| Assertivo | Contenuto di leadership, messaggistica autorevole | &quot;Ecco cosa devi fare in questo momento...&quot; |
| Narrazione | Racconti del brand, connessioni emotive | &quot;Tutto è iniziato con una semplice domanda...&quot; |
| Conversazionale | Campagne di sviluppo, creazione di relazioni | &quot;Parliamo di come questo programma può aiutarti...&quot; |

## Contenuto di riferimento ottimizzato {#reference-content}

>[!TIP]
>
>Se hai già caricato una risorsa tramite il menu **[!UICONTROL Contenuto di riferimento]**, non è necessario farvi riferimento nella richiesta. Il sistema utilizza automaticamente tutti i documenti selezionati.

I file di contenuto di riferimento forniscono informazioni fattuali che arricchiscono il contenuto generato con dettagli specifici e precisi. Quando carichi dei documenti, ad esempio brochure di prodotti o white paper, modifica la richiesta per specificare quali parti sono attive:

* **Anziché** _&quot;Utilizzare la brochure del prodotto&quot;_ **utilizzare** _&quot;Concentrarsi sulle funzionalità di sicurezza avanzate e sulle certificazioni di conformità, in particolare sulla conformità SOC 2 e sulla crittografia dei dati&quot;_

* **Anziché** _&quot;Fare riferimento ai casi di studio&quot;_ **utilizzare** _&quot;Evidenziare i risultati del ROI dai clienti del settore sanitario, in particolare la riduzione dei costi del 40% presso il Centro medico regionale&quot;_

* **Invece di** _&quot;Includi dettagli tecnici&quot;_ **devi utilizzare** _&quot;Enfatizzare le funzionalità di integrazione API e i vantaggi per gli sviluppatori, concentrandoti sugli endpoint REST API e sul 99,9% di uptime SLA&quot;_

### Ottimizzazione dei contenuti

Dopo la generazione del contenuto, utilizzare la funzionalità **_[!UICONTROL Perfeziona]_** per eseguire iterazioni e migliorarla con le opzioni seguenti:

* **[!UICONTROL Elaborare]** - L&#39;Assistente all&#39;intelligenza artificiale può aiutarti a espandere argomenti specifici, fornendo ulteriori dettagli per una migliore comprensione e coinvolgimento.

* **[!UICONTROL Riepiloga]** - Le informazioni lunghe possono sovraccaricare i visualizzatori di pagina. Utilizza l’Assistente AI per condensare i punti chiave in riepiloghi chiari e concisi che catturano l’attenzione e li incoraggiano a leggere ulteriormente.

* **[!UICONTROL Riformula]** - Riscrivi il messaggio conservandone il significato. Questa opzione consente di generare una formulazione alternativa, migliorare il flusso o regolare la formulazione senza modificare il messaggio principale.

* **[!UICONTROL Usa un linguaggio più semplice]**: semplifica la lingua, garantendo chiarezza e accessibilità a un pubblico più ampio.

* **[!UICONTROL Traduci]** - Traduci il testo in un&#39;altra lingua. Attualmente, l’inglese è l’unica lingua supportata.

* **[!UICONTROL Cambia tono]** - Regola il tono del messaggio in base allo stile di comunicazione, ad esempio rendendolo più amichevole, professionale, urgente o stimolante.

* **[!UICONTROL Modifica strategia di comunicazione]** - Modifica l&#39;approccio di messaggistica in base agli obiettivi, ad esempio la creazione di messaggi urgenti o l&#39;enfasi sull&#39;aspetto interessante.
