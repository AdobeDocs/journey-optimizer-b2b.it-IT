---
title: Authoring di e-mail
description: Utilizza gli strumenti di progettazione delle e-mail in Journey Optimizer B2B Prime, tra cui modelli e-mail, frammenti, personalizzazione, modalità scura e convalida.
autotag-review: '2026-06-12T22:51:19.543Z'
TQID: 'https://experienceleague.adobe.com/-mtyiJ98caCTuTKaZbzYrYKiQoxolq-hMw7p5h7bNpY'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: e666e996-b2cf-4c45-8fc2-1c625212abab
  - id: f01b5556-e951-40ba-8625-2e3001864f2b
  - id: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2:
  - id: e7bdffdc-2950-4be5-8c23-84240a995090
  - id: ff0c35fa-aa7e-4050-a37c-198fcacd09e6
  - id: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: cb3217c9fd7beb712d0c61638d143b798010d2b7
workflow-type: tm+mt
source-wordcount: 2775
ht-degree: 1%

---

# Authoring di e-mail

In [!DNL Adobe Journey Optimizer B2B Prime], lo spazio di progettazione delle e-mail fornisce un&#39;area di lavoro visiva in cui gli addetti al marketing compongono le e-mail. Gli strumenti di progettazione delle e-mail nei pannelli sinistro e superiore (strutture, componenti di contenuto, modelli, frammenti e altro ancora) supportano la creazione da zero con il trascinamento della selezione. Puoi anche scegliere di iniziare da un modello, incollare HTML non elaborati o assemblare messaggi da frammenti visivi riutilizzabili.

>[!IMPORTANT]
>
>Per informazioni sulla configurazione da parte dell&#39;amministratore di sottodomini, autenticazione, pool IP e canali e-mail, vedere [Recapito messaggi e-mail e configurazione dei canali](../admin/configuration-email-deliverability.md).

In [!DNL Journey Optimizer B2B Prime], ogni e-mail è associata a un&#39;azione _[!UICONTROL Invia e-mail]_ in un percorso. L’intero flusso di lavoro dalla progettazione del percorso alla definizione dell’e-mail avviene in un’esperienza continua. Quando [aggiungi un _Invia e-mail_ nodo](../marketing/person-journey-nodes.md#add-an-action-node) a un percorso di persone, fai clic su **[!UICONTROL Crea e-mail]** per avviare il processo di progettazione del contenuto dell&#39;e-mail.

Questa azione avvia lo spazio di progettazione delle e-mail, in cui puoi scegliere come progettare le e-mail tra le seguenti opzioni:

* [Progetta il tuo messaggio e-mail da zero](#design-your-email-from-scratch) utilizzando l&#39;interfaccia di progettazione visiva. Crea il componente layout e-mail per componente trascinando la selezione su un’area di lavoro vuota. Questo metodo è ideale per creare nuovi modelli o e-mail una tantum.

* [Importa HTML](#html) nell&#39;editor di codice o lavora fianco a fianco con l&#39;area di lavoro visiva.

  <!-- Full HTML import workflow with .html and .zip uploads is on the Beta roadmap. -->

* [Selezionare un modello esistente](#select-a-template) da un elenco di modelli di posta elettronica predefiniti o personalizzati. Questo metodo è ideale per i casi di utilizzo di e-mail ripetibili.

<!-- * Upload a design prototype (JPG, PNG, PDF, or Figma export) and have AI Assitant convert it into a responsive HTML email. (Image to HTML (Img2HTML) -->

## Strumenti di progettazione e-mail

* **Barra degli strumenti superiore:** Salva, Indietro, Passa all&#39;editor di codice, controlli di anteprima.
* **Barra a sinistra:** strutture (layout colonne), contenuto (testo, pulsante, immagine, divisore, social, HTML), frammenti, modelli, struttura di navigazione (gerarchia DOM dell&#39;e-mail).
* **Area di lavoro centrale:** editor WYSIWYG con anteprima desktop e mobile.
* **Barra a destra:** impostazioni e stili per il componente attualmente selezionato, incluse le proprietà del contenuto, lo sfondo, il bordo, la spaziatura interna e la personalizzazione.

## Best practice per la progettazione e-mail {#design-best-practices}

L’aderenza alle best practice HTML e CSS consente di garantire un rendering coerente tra i client e-mail.

| Approccio | Linee guida |
| -------- | -------- |
| **Consigliato** | Layout statici basati su tabelle · Tabelle HTML e tabelle nidificate · Larghezze dei modelli di 600-800 px · CSS in linea semplice · Font Web-safe |
| **Usare con cautela** | Immagini di sfondo (supporto client limitato) · Font web personalizzati (definiscono sempre un font di fallback) · Layout di dimensioni superiori a 800 px · Mappe immagine |
| **Evita** | JavaScript, iframe o Flash · Audio o video incorporati · HTML Form · Layout basati su Div |

>[!NOTE]
>
>Il contenuto dell’e-mail deve inoltre soddisfare i requisiti di accessibilità digitale applicabili. Strutturare le intestazioni in modo logico, fornire testo alternativo per tutte le immagini e verificare il contrasto dei colori in modalità chiara e scura.

## Creare un messaggio e-mail da un percorso {#email-from-journey}

1. Fai clic sul pulsante **[!UICONTROL Modifica e-mail]** per procedere al passaggio di configurazione dell&#39;e-mail.
1. Nella schermata successiva, seleziona una configurazione di canale creata in precedenza dal menu a discesa **[!UICONTROL Configurazione e-mail]**. Sono elencate solo le configurazioni attive.
1. Inserisci un Etichetta per l’azione (visibile nell’area di lavoro del percorso) e un nome e-mail interno.
1. Immettere la riga Oggetto.
1. Facoltativamente, attiva **[!UICONTROL Abilita tracciamento URL]** per questo nodo e-mail.
1. Fai clic su **[!UICONTROL Modifica contenuto]** per aprire lo spazio di progettazione delle e-mail.

### Schermata Modifica contenuto {#edit-content-screen}

Da questa schermata puoi confermare i dettagli del mittente (ereditati dalla configurazione del canale), impostare l’oggetto e aprire lo spazio di progettazione dell’e-mail per creare il corpo. Il preheader è configurato nello spazio di progettazione e-mail (vedi [Impostazione del preheader](#preheader)).

* **Da nome, Da e-mail, Ccn:** Ereditato dalla configurazione del canale. Sola lettura in questa schermata.
* **Riga oggetto:** Obbligatorio. Personalization è supportato.
* **Modifica corpo dell&#39;e-mail:** Apre lo spazio di progettazione e-mail.

>[!NOTE]
>
>La dimensione dell’e-mail non può superare i 100 KB per best practice ISP. Se superi questo limite, Prime ti avvisa nell’editor. Gli errori (oggetto mancante, corpo mancante, configurazione del canale eliminata) impediscono l’attivazione del percorso finché non vengono risolti.

## Progettazione da zero {#design-from-scratch}

### Passaggio per passaggio: creare un messaggio e-mail da zero {#build-from-scratch}

1. Dal nodo e-mail del percorso, fare clic su **[!UICONTROL Modifica contenuto]** → **[!UICONTROL Modifica corpo e-mail]**.
1. Nella schermata Crea e-mail, fai clic su **[!UICONTROL Progetta da zero]**.
1. Fai clic su **[!UICONTROL Conferma]** per aprire un&#39;area di lavoro vuota.
1. Dalla barra a sinistra, trascina una **[!UICONTROL colonna]** (1-colonna, 1:1, 2:2, n:n colonna) nell&#39;area di lavoro.
1. Trascina i componenti **[!UICONTROL Contenuto]** nelle colonne della struttura: Testo, Pulsante, Immagine, Divisore, Social, HTML.
1. Fai clic su un componente nell’area di lavoro per selezionarlo. La barra a destra mostra le schede Impostazioni e Stili.
1. Utilizza la scheda **[!UICONTROL Impostazioni]** per configurare le opzioni specifiche del componente (contenuto di testo, origine immagine, URL pulsante).
1. Utilizza la scheda **[!UICONTROL Stili]** per configurare spaziatura, bordo, sfondo, carattere e colore.
1. Utilizza l&#39;icona **[!UICONTROL Struttura di navigazione]** nella barra a sinistra per spostarti tra i componenti in un messaggio e-mail profondamente nidificato.
1. Passa da Desktop a Anteprima mobile utilizzando le icone nella barra degli strumenti superiore.
1. Fai clic su **[!UICONTROL Salva]** (oppure utilizza il menu a discesa Salva per visualizzare altre opzioni di salvataggio).
1. Fai clic su **[!UICONTROL Indietro]** per tornare alle proprietà dell&#39;e-mail.

### Componenti contenuto disponibili {#content-components}

| Componente | Descrizione |
| --------- | ----------- |
| **Testo** | Testo formattato (grassetto, corsivo, dimensione carattere, colore, allineamento, elenchi, collegamenti). |
| **Pulsante** | CTA cliccabile. Supporta colore di sfondo, bordo, spaziatura interna, comportamento al passaggio del mouse e URL personalizzati. |
| **Immagine** | Inserisci da Marketo Design Studio (selettore risorse). Supporta il testo alternativo, l&#39;allineamento, il collegamento e il tracciamento dei clic. |
| **Divisore** | Regola orizzontale con spessore e colore configurabili. |
| **Social** | Icone di social media preformattate con configurazione del collegamento. |
| **HTML** | Blocco Raw HTML per contenuti avanzati. Utile per incorporare markup codificati a mano. |

### Strutture e layout di colonna {#structures}

Le strutture definiscono la griglia di colonne dell’e-mail. Le strutture disponibili includono: 1 colonna, 1:1 (due colonne uguali), 1:2 / 2:1 (due colonne asimmetriche), 1:1:1 (tre colonne uguali) e n:n (più colonne personalizzate). Utilizza le strutture per controllare il modo in cui il contenuto viene riversato sui dispositivi mobili: per impostazione predefinita, la maggior parte delle strutture si riduce a una colonna singola su schermi stretti.

>[!TIP]
>
>Semplifica la struttura delle e-mail. I layout a due o tre colonne forniscono un rendering coerente tra i client e-mail (in particolare Outlook e Gmail). Le strutture annidate in profondità possono presentare un rendering imprevedibile.

### Impostazione della preintestazione {#preheader}

Il preheader è lo snippet di testo mostrato dopo la riga dell&#39;oggetto nelle anteprime della casella in entrata. In Prime, il preheader viene configurato nell’area di lavoro visiva nell’area di progettazione dell’e-mail, non nella schermata delle proprietà dell’e-mail accanto alla riga dell’oggetto.

1. Apri l’e-mail nello spazio di progettazione e-mail.
1. Nell’area di lavoro, individua l’area di preintestazione nella parte superiore del corpo dell’e-mail.
1. Fare clic sull&#39;area di testo preintestazione e inserire la copia preintestazione.
1. Applicare i token di formattazione e personalizzazione in base alle esigenze utilizzando i controlli RTF.
1. Fai clic su **[!UICONTROL Salva]**.

>[!TIP]
>
>Mantieni il preheader tra 40 e 100 caratteri. Deve essere complementare all’oggetto (non ripetuto) e fornire al destinatario un motivo in più per aprire l’e-mail.

## Utilizzo dei modelli {#templates}

I modelli sono layout e-mail riutilizzabili. Accelerano la creazione di e-mail, impongono la coerenza del marchio e semplificano la collaborazione tra team.

### Tipi di modelli

* **Modelli di esempio (preconfigurati).** Circa 20 modelli già pronti che coprono casi d’uso comuni (sensibilizzazione basata sull’account, inviti a eventi, formazione, annunci di prodotti). Disponibile immediatamente per ogni cliente.
* **Modelli salvati (personalizzati).** Modelli creati dal team: creati da zero in **[!UICONTROL Gestione contenuto]** → **[!UICONTROL Modelli]** o salvati da un&#39;e-mail esistente utilizzando l&#39;opzione &quot;Salva come modello&quot;.

### Creare un messaggio e-mail da un modello {#create-from-template}

1. Dal nodo e-mail del percorso, fare clic su **[!UICONTROL Modifica contenuto]** → **[!UICONTROL Modifica corpo e-mail]**.
1. Nella schermata Crea e-mail, la scheda **[!UICONTROL Modelli di esempio]** è selezionata per impostazione predefinita.
1. Sfoglia la galleria. Utilizza la casella di ricerca per filtrare per nome o categoria.
1. Passa alla scheda **[!UICONTROL Modelli salvati]** per visualizzare i modelli creati dal team.
1. Fai clic sulla miniatura di un modello per visualizzarne l’anteprima.
1. Fare clic su **[!UICONTROL Usa questo modello]** per applicarlo. Il contenuto del modello viene aperto nell’area di lavoro nello spazio di progettazione delle e-mail.
1. Personalizzare testo, immagini e collegamenti. La struttura ereditata dal modello può essere modificata come un’e-mail originale.
1. Fai clic su **[!UICONTROL Salva]** → **[!UICONTROL Indietro]** per tornare alle proprietà dell&#39;e-mail.

### Creare un modello riutilizzabile {#create-reusable-template}

1. Passa a **[!UICONTROL Gestione contenuto]** → **[!UICONTROL Modelli]**.
1. Fare clic su **[!UICONTROL Crea modello]**.
1. Immettere un nome e una descrizione. Seleziona **[!UICONTROL E-mail]** come canale.
1. Fai clic su **[!UICONTROL Crea]**. Lo spazio di progettazione e-mail viene aperto per la modifica.
1. Crea il modello da zero, da un modello esistente o incollando HTML.
1. Abilitare facoltativamente **[!UICONTROL Impostazioni di governance]**:
   * Consenti modifica struttura e contenuto: controlla se gli autori delle e-mail possono modificare la struttura del modello o solo il relativo contenuto.
   * Blocca componenti specifici: rendi i singoli componenti di sola lettura quando vengono utilizzati in un messaggio e-mail.
1. Fai clic su **[!UICONTROL Salva]**. Il modello è ora disponibile per tutti gli utenti nella raccolta Modelli salvati.

### Salvare un’e-mail come modello {#save-as-template}

1. Apri un’e-mail esistente nello spazio di progettazione e-mail.
1. Nel menu a discesa **[!UICONTROL Salva]**, fai clic su **[!UICONTROL Salva come modello]**.
1. Immettere un nome e una descrizione.
1. Facoltativamente, configura le impostazioni di governance.
1. Fai clic su **[!UICONTROL Salva]**.

>[!NOTE]
>
>I modelli salvati e il relativo contenuto e-mail sono indipendenti. La modifica di un modello non aggiorna retroattivamente le e-mail create da esso. Per propagare le modifiche in più e-mail, utilizza frammenti visivi invece di modelli.

## Frammenti visivi {#visual-fragments}

Un frammento visivo è un blocco di contenuto riutilizzabile, come intestazione, piè di pagina, CTA, dichiarazione di non responsabilità legale e set di collegamenti social, che può essere inserito in molte e-mail. Quando aggiorni un frammento, la modifica si propaga automaticamente a ogni e-mail che lo utilizza. I frammenti sono il metodo consigliato per applicare la coerenza del brand e centralizzare gli aggiornamenti dei contenuti.

### Creare un frammento visivo {#create-fragment}

1. Passa a **[!UICONTROL Gestione contenuto]** → **[!UICONTROL Frammenti]**.
1. Fare clic su **[!UICONTROL Crea frammento]**.
1. Seleziona **[!UICONTROL Frammento visivo]** come tipo. Immettere un nome e una descrizione.
1. Fai clic su **[!UICONTROL Crea]**. Lo spazio di progettazione e-mail viene aperto per la modifica.
1. Trascina strutture e componenti di contenuto nell’area di lavoro per creare il frammento (ad esempio, una struttura a 1 colonna con un’immagine del logo, un’intestazione e un elenco di collegamenti di navigazione).
1. (Facoltativo) Contrassegna i campi come **[!UICONTROL Modificabili]** per renderli personalizzabili in base all&#39;utilizzo:
   * Seleziona un componente, quindi apri la sezione **[!UICONTROL Campi modificabili]** nella barra a destra.
   * Aggiungi campi con valori predefiniti (ad esempio, un campo origine immagine con un URL logo predefinito e un campo di testo con un titolo predefinito).
   * Gli autori di e-mail che utilizzano il frammento possono ignorare questi campi senza interrompere la struttura del frammento.
1. Fai clic su **[!UICONTROL Salva]**.

### Inserire un frammento in un messaggio e-mail {#insert-fragment}

1. Apri l’e-mail nello spazio di progettazione e-mail.
1. Nella barra a sinistra, fai clic su **[!UICONTROL Frammenti]**.
1. Cerca il frammento desiderato.
1. Trascina il frammento nell’area di lavoro nella posizione desiderata.
1. Se il frammento dispone di campi modificabili, configura i valori nella barra a destra.
1. Fai clic su **[!UICONTROL Salva]**.

>[!TIP]
>
>Utilizza i frammenti per qualsiasi contenuto che deve rimanere coerente tra le e-mail: intestazione del brand, piè di pagina legale, barra dei collegamenti social, blocco per annullare l’abbonamento. Quando il team legale aggiorna la liberatoria, cambi un frammento e ogni e-mail viene aggiornata.

## Personalizzazione {#personalization}

Prime utilizza la sintassi Handlebars per la personalizzazione. I token vengono sostituiti al momento dell’invio con i valori dei dati di profilo di ciascun destinatario.

### Dove puoi personalizzare

* **Oggetto**: punto di personalizzazione più comune.
* **Preheader** — impostato nell&#39;area di lavoro visiva; supporta i token di attributi di profilo.
* **Testo del corpo dell&#39;e-mail**: nomi e altri attributi di profilo inseriti in linea.
* **URL pulsante** — aggiungi parametri per destinatario.

>[!NOTE]
>
>In questa versione sono disponibili solo gli attributi del profilo nell’editor di Personalization.

### Inserire un token di personalizzazione {#insert-token}

1. Nell’area di progettazione e-mail (o nella schermata delle proprietà e-mail per la riga dell’oggetto), fai clic sul campo in cui desideri inserire un token.
1. Fai clic sull&#39;icona di personalizzazione (spesso etichettata **[!UICONTROL Apri finestra di dialogo per personalizzazione]** o **[!UICONTROL Aggiungi espressione]**).
1. Nella finestra di dialogo di personalizzazione, sfoglia la struttura dello schema a sinistra. Sono elencati gli attributi del profilo (nome, cognome, e-mail, titolo del processo e altri campi del profilo).
1. Seleziona un attributo. Prime inserisce l&#39;espressione Handlebars corrispondente, ad esempio `{{profile.firstName}}`.
1. Aggiungere un valore di fallback per gestire i dati mancanti: `{{profile.firstName | default: "there"}}`.
1. Fai clic su **[!UICONTROL Conferma]** o **[!UICONTROL Inserisci]**. L’espressione viene visualizzata in linea nel campo.

### Pattern di personalizzazione comuni {#personalization-patterns}

Utilizza espressioni Handlebars come le seguenti (la personalizzazione utilizza la stessa sintassi descritta in [Procedura dettagliata: inserire un token di personalizzazione](#insert-token)):

* **`{{profile.lastName}}`** - Inserire il cognome del destinatario.
* **`{{profile.jobTitle}}`** — Fare riferimento al titolo del processo del destinatario nella copia del corpo.
* **`{{profile.firstName}}, ready to take the next step?`** - Combina token e testo statico in linea.

Per un saluto di nome con un fallback quando manca il valore, utilizza l&#39;helper `default` come mostrato nei passaggi di personalizzazione precedenti (ad esempio, nome con `"there"` predefinito).

### Handlebars Helpers {#handlebars-helpers}

Oltre a `default`, l&#39;editor di personalizzazione include helper Handlebars incorporati per logica condizionale, trasformazione del testo e formattazione della data. Utilizza il browser delle funzioni dell’editor per esplorare gli helper disponibili e inserirli con la sintassi corretta.

>[!TIP]
>
>Nello spazio di progettazione delle e-mail, digita `{{` direttamente in qualsiasi campo di testo per attivare un elenco a discesa di completamento automatico in linea contenente gli attributi di profilo disponibili. Non è necessario aprire la finestra di dialogo di personalizzazione completa per gli inserimenti rapidi.

### Espressioni basate sull’intelligenza artificiale {#ai-personalization}

L’Assistente IA nell’editor di personalizzazione può generare espressioni Handlebars da una descrizione in linguaggio semplice, spiegare cosa fa un’espressione esistente e identificare potenziali problemi. Utilizzala per accelerare l’authoring delle espressioni, in particolare per gli helper per la logica condizionale o la formattazione della data.

## Aggiunta di risorse da Marketo Design Studio {#marketo-assets}

Prime rende disponibili le risorse esistenti di Marketo Design Studio nell’area di progettazione delle e-mail. Puoi sfogliare e inserire queste immagini nelle e-mail direttamente dal selettore delle risorse.

>[!IMPORTANT]
>
>La disponibilità delle risorse in Prime si basa su una **copia occasionale** delle risorse da Marketo Design Studio. Il nuovo caricamento o la modifica di risorse in Marketo dopo la copia iniziale **non** si rifletterà in Prime. In questa versione non sono supportati neanche i caricamenti di immagini direttamente in Prime. La gestione nativa delle risorse digitali in Prime, tra cui caricamento, navigazione delle cartelle, ricerca e modifica delle immagini, fa parte dell’ambito di Beta.

### Tipi di file supportati {#asset-file-types}

* **Supporto completo (visibile nel selettore, incorporabile in linea):** JPG, PNG, GIF, WebP.
* **Accessibile con attenzione:** SVG (con un avviso che alcuni client di posta elettronica non eseguono il rendering di SVG).
* **Non supportato in questa versione:** TIFF, PDF, DOCX, XLSX, PPTX, CSS, JS, HTML, TXT, file binari, PSD, AI, INDD.

### Inserire un&#39;immagine da Marketo Design Studio {#insert-image}

1. Nell&#39;area di progettazione delle e-mail, trascina un componente di contenuto **[!UICONTROL Immagine]** nell&#39;area di lavoro oppure fai clic su un&#39;immagine esistente per sostituirla.
1. Nella barra a destra, fai clic su **[!UICONTROL Marketo Engage Assets]**.
1. Viene aperto il selettore risorse. Sfoglia cartelle o cerca per nome file.
1. Seleziona la risorsa desiderata.
1. Fai clic su **[!UICONTROL Seleziona]**. L’immagine viene inserita nell’e-mail dalla copia della risorsa disponibile in Prime.
1. Nella barra a destra, configura:
   * Testo alternativo (consigliato per l’accessibilità e per i client che bloccano le immagini per impostazione predefinita).
   * Allineamento
   * Destinazione collegamento - rende l&#39;immagine cliccabile.
1. Fai clic su **[!UICONTROL Salva]**.

## Modalità scura {#dark-mode}

Il rendering in modalità scura è supportato tramite le query multimediali CSS `prefers-color-scheme`. Gli strumenti di progettazione delle e-mail includono un’anteprima in modalità scura e opzioni per definire uno stile personalizzato per i client e-mail di supporto, che consente di verificare che il testo rimanga leggibile, che i loghi siano visibili e che i colori del brand resistano su sfondi scuri.

Per istruzioni dettagliate sull&#39;anteprima, sulla configurazione delle impostazioni della modalità scura personalizzata, sul supporto client e-mail e sulle best practice per i test, consulta [Modalità scura per il contenuto delle e-mail](./email-dark-mode.md).

## Convalida del contenuto delle e-mail {#validation}

Prima di poter attivare il percorso, il contenuto dell’e-mail deve essere valido. Prime genera avvisi a livello di contenuto nell’e-mail e nell’area di lavoro del percorso. Questa sezione descrive gli avvisi che potresti visualizzare e come risolverli.

### Avvisi di contenuto comuni e come risolverli {#content-alerts}

| Avviso | Che cosa significa | Come risolvere |
| ----- | ------------- | -------------- |
| **Riga oggetto mancante** | Il campo Oggetto è vuoto. | Apri l’e-mail e immetti un oggetto nella schermata Modifica contenuto. I token Personalization sono consentiti, ma il campo non può essere vuoto. |
| **Il corpo dell&#39;email è vuoto** | L’area di lavoro nell’area di progettazione e-mail non ha contenuto. | Fai clic su **[!UICONTROL Modifica corpo dell&#39;e-mail]** per aprire lo spazio di progettazione e-mail. Trascina nell’area di lavoro almeno un componente Struttura e uno Contenuto, quindi fai clic su Salva. |
| **Configurazione canale non selezionata** | Non è stata scelta alcuna configurazione e-mail per il nodo e-mail. | Nella schermata delle proprietà e-mail, seleziona una configurazione del canale attivo dal menu a discesa **[!UICONTROL Configurazione e-mail]**. |
| **Configurazione canale eliminata** | La configurazione di canale selezionata in precedenza è stata eliminata o non è più attiva. | Apri le proprietà e-mail e seleziona un’altra configurazione del canale attivo. Se non ne è disponibile alcuna, un amministratore deve crearne o riattivarne una. |
| **La dimensione dell&#39;e-mail supera i 100 KB** | La dimensione totale dell’e-mail (HTML, CSS in linea, contenuto codificato) supera il limite di 100 KB previsto per le best practice ISP. | Riduci la dimensione dell’e-mail: sostituisci immagini in linea di grandi dimensioni con immagini ospitate esternamente da Marketo Design Studio, rimuovi i file CSS in linea non utilizzati, semplifica le strutture nidificate. |
| **Token di personalizzazione non risolto** | Un token Handlebars fa riferimento a un attributo di profilo senza fallback e l’attributo potrebbe non essere presente per alcuni destinatari. | Aggiungere un fallback utilizzando l&#39;helper Handlebars `default` come descritto in [Personalization](#personalization). In alternativa, limita il pubblico di percorso ai profili in cui l’attributo è garantito. |
| **Immagine non caricata** | Un componente immagine fa riferimento a una risorsa che non è più disponibile. | Fai clic sull’immagine, apri il selettore risorse e riseleziona la risorsa da Marketo Design Studio. |

### Rivedere e risolvere gli avvisi {#resolve-alerts}

1. Apri il percorso contenente il nodo e-mail. I nodi e-mail con avvisi non risolti sono contrassegnati da un contrassegno rosso nell’area di lavoro.
1. Fai clic sul nodo e-mail per aprire la barra delle proprietà.
1. Rivedi la sezione **[!UICONTROL Avvisi]** nella barra delle proprietà. Ogni avviso è collegato al campo o alla schermata in cui è possibile risolvere il problema.
1. Risolvi ogni avviso di volta in volta: ad esempio, inserisci un oggetto mancante, seleziona una configurazione di canale o apri lo spazio di progettazione e-mail per correggere il contenuto.
1. Dopo aver risolto tutti gli avvisi, fai clic su **[!UICONTROL Salva]** nel nodo e-mail.
1. Conferma che il badge rosso sul nodo e-mail si cancelli.

>[!NOTE]
>
>Gli avvisi devono essere cancellati prima che il percorso possa procedere. Gli avvisi non sono di blocco, ma devono essere rivisti (ad esempio, un’e-mail che utilizza un token senza un fallback potrebbe restituire con valori vuoti per alcuni destinatari).
