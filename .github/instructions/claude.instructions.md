---
applyTo: "**/*.md"
source-git-commit: d36cfd513df3d363a7bd74b5e09b774426e50b9b
workflow-type: tm+mt
source-wordcount: '5166'
ht-degree: 1%
---

# Documentazione di Adobe Experience League: istruzioni del codice Claude

Stai assistendo un autore tecnico nell&#39;archivio della documentazione pubblica di Adobe Experience League (`journey-optimizer-b2b.en`). Ogni elemento di contenuto che crei, modifichi o rivedi DEVE rispettare tutte le regole riportate di seguito. In caso di dubbi sulla terminologia, consultare i wiki a cui si fa riferimento utilizzando lo strumento MCP di influenza (`mcp__adobe-wiki-confluence`).

&#x200B;---

## &#x200B;1. Voce, tono e stile

### Scrittura incentrata sull&#39;utente

Centra l’utente, non la funzione. Scrivere ciò che l&#39;utente può **fare**, non ciò che la funzione fa.

- Usa la seconda persona (&quot;tu&quot;) e l&#39;umore imperativo per le istruzioni.
- Usa &quot;tu&quot; quando parli al pubblico di se stessi, non di &quot;utenti&quot;. &quot;Utenti&quot; è accettabile quando si fa riferimento a un ruolo (ad esempio, un amministratore che gestisce gli utenti).
- EVITA &quot;La funzione X consente di...&quot; o &quot;La funzione X consente di...&quot;. Metti l’utente come soggetto o usa umore imperativo.
  - Scorretto: &quot;L’API server può essere utilizzata sui server&quot;.
  - Corretto: &quot;Utilizzare l&#39;API server sui server&quot;.
  - Non valido: &quot;I campi calcolati consentono la creazione di valori...&quot;
  - Corretto: &quot;Utilizzare i campi calcolati per creare i valori...&quot;
- Presta attenzione a &quot;puoi&quot;. È appropriato, ma può essere usato in modo eccessivo, creando frasi ripetitive o peggiori.
- Utilizza &quot;seleziona&quot; per scegliere le opzioni da un elenco o evidenziare il testo. Utilizzare &quot;clic&quot; solo per azioni esplicite del mouse. Evitare di denominare il tipo di controllo (pulsante, collegamento) a meno che non sia necessario per la disambiguazione.
- Utilizzare &quot;Apri&quot; / &quot;Chiudi&quot; per le applicazioni e le principali finestre o pannelli.
- Utilizza &quot;Lascia&quot; per uscire da un sito o da un’esperienza (ad esempio, &quot;Lascia Report Builder&quot;).
- Utilizza &quot;vai a&quot; o &quot;passa a&quot; per la navigazione.
- Utilizzare &quot;Riproduci video&quot; e non &quot;Guarda video&quot;. Non tutti stanno guardando.
- Utilizzare &quot;Visualizza&quot;, &quot;Mostra&quot; o &quot;Vai a tutti&quot; e non &quot;Vedi tutti&quot;. Non tutti stanno vedendo.
- Utilizzare &quot;accesso&quot; / &quot;disconnessione&quot;, non &quot;accesso&quot; / &quot;disconnessione&quot;.
- Evita di usare &quot;al fine di&quot;. Utilizza invece &quot;per&quot;.
- Evita di utilizzare. Utilizza invece &quot;use&quot;.
- Evita aggettivi vaghi come &quot;veloce&quot; o &quot;facile&quot;. Sii preciso: &quot;Questo processo in genere richiede 5 minuti&quot;.
- Evita avverbi deboli: molto, estremamente, incredibilmente.

### Struttura frase e paragrafo

- Target ≤20 parole per frase (la guida per l’authoring riporta un massimo di ≤35). Un pensiero per frase.
- Paragrafi: max 125 parole, idealmente ≤100. Max 4-5 frasi. Nessuna parete di testo.
- Usa la voce attiva. Evita costruzioni passive e nominalizzazioni (ad esempio, utilizza &quot;crea&quot; e non &quot;creazione&quot;).
- Utilizza una semplice struttura soggetto-verbo-oggetto.
- Evita soggetti falsi (&quot;È...&quot;, &quot;Ci sono...&quot;).
- Utilizza la stessa parola in modo coerente. Non ruotare i sinonimi.
- Nessun esempio di umorismo, gergo, gergo o cultura specifica (localizzare bene).
- Utilizza la virgola di Oxford negli elenchi di tre o più elementi.
- Scrivi i numeri interi da zero a nove; utilizza le cifre per i numeri da 10 in poi.
- Nessun punto e virgola. Utilizza invece un punto e una nuova frase.

### Scannabilità

- I lettori devono comprendere l’ambito dell’articolo solo da titolo, intestazioni e didascalie.
- Max 2-5 sottosezioni per sezione.
- Target 7 passaggi per attività; 10 è il massimo pratico. Suddividere le procedure più lunghe in sottoattività.
- Max 8 elementi per elenco puntato.
- Utilizzare le tabelle per semplificare la scansione degli elenchi di termini/definizioni.
- Il contenuto deve avere un punteggio inferiore al grado 10 in un test di leggibilità (dopo aver rimosso sostantivi e titoli appropriati).

### Scrittura per individuazione IA

Gli assistenti e gli strumenti di ricerca basati su intelligenza artificiale fanno emergere sempre più contenuti Experience League nelle risposte generate.

- Inserire i termini chiave (nomi di prodotto, nomi di funzionalità, attività) nel corpo del testo e nel testo del collegamento, non solo nelle immagini o nelle tabelle complesse. I sistemi di intelligenza artificiale si basano su testo leggibile.
- Scrivi titoli e primi paragrafi chiari e autonomi. Gli strumenti di intelligenza artificiale spesso li estraggono in isolamento; devono avere senso senza il contesto circostante.
- Mantieni le frasi brevi e dirette. La prosa concisa è più facile per l’intelligenza artificiale analizzare e citare con precisione.
- Utilizza formati strutturati (passaggi numerati, punti elenco brevi, intestazioni di tipo definizione) per procedure e confronti. La struttura consente all’intelligenza artificiale di identificare la risposta corretta.
- Includi sinonimi o termini alternativi al primo utilizzo (ad esempio, &quot;ECID (Experience Cloud ID)&quot;) per migliorare il recupero per varie frasi di query.
- Assicurati che i campi dei metadati (titolo, descrizione, tag delle funzioni) siano completi e precisi.

&#x200B;---

## &#x200B;2. Sintassi di Adobe Markdown (Experience League)

### Frontmatter (obbligatorio per ogni file)

```yaml
---
title: Title Case Title Here
description: Learn how to... or Learn about... (150-160 chars, sentence case).
---
```

Campi facoltativi aggiuntivi utilizzati in questo repository: `solution`, `type`, `role`, `exl-id`. Corrispondenza con il pattern dei file esistenti.

**IMPORTANTE:** NON aggiungere `exl-id` durante la creazione di una nuova pagina. Viene generato automaticamente al momento della pubblicazione. Solo i campi `exl-id` che esistono già nelle pagine esistenti devono essere conservati.

**Regole metadati titolo:**

- Tutte iniziali maiuscole (solo in Experience League che utilizza le iniziali maiuscole).
- Massimo 60 caratteri (inglese). Il sistema aggiunge automaticamente `| Adobe Experience Platform`. Fattore in lunghezza.
- NON aggiungere il nome della pipe o del prodotto. Viene aggiunto automaticamente.
- Considerala come la versione SEO del nome della pagina (ciò che gli utenti cercano).
- Titolo del concetto: frase sostantiva (ad esempio, &quot;Rapporto visualizzazioni pagina&quot;).
- Titolo attività: frase verbale (ad esempio, &quot;Creare un segmento per le visualizzazioni di pagina&quot;).
- Gli acronimi non sono approvati dal Marketing per la maggior parte degli usi, ma un uso limitato è accettabile per SEO, voci di sommario, metadati di descrizione e intestazioni in cui la lunghezza è un problema.

**Regole metadati descrizione:**

- Frase. Da 150 a 160 caratteri idealmente; 160 max.
- Da una a due frasi concise. La prima frase riassume; la seconda è una call to action.
- Inizia le descrizioni dei concetti con &quot;Ulteriori informazioni su...&quot; o &quot;Comprendere...&quot;.
- Inizia le descrizioni delle attività con &quot;Scopri come...&quot; o un verbo imperativo.
- NON iniziare con il nome del prodotto. Inizia con un verbo per SEO (Search Engine Optimization).
- NON copiare il primo paragrafo letteralmente (scopo diverso).
- Se un campo di metadati inizia con un tag `[!DNL]` o &grave;&grave;, racchiudere l&#39;intero valore del campo tra virgolette o la convalida non riesce.

### Intestazioni

- `#` = H1 (titolo articolo, uno per pagina). `##` = sezioni principali H2. `###` = H3, ecc.
- NON saltare i livelli delle intestazioni (ad es., non saltare da H2 a H4).
- Target ≤5 parole. Massimo 69 caratteri (inglese).
- Riga vuota prima di AND dopo ogni intestazione.
- Ogni titolo deve essere seguito da almeno una frase del corpo del testo. NON sovrapporre MAI due intestazioni o inserire una nota, un elenco o una tabella direttamente sotto un&#39;intestazione senza prima un paragrafo.
- ID di ancoraggio personalizzati: `## Section title {#section-id}` (lettere minuscole, trattini, senza punti).
- Evita nomi di ancoraggio in conflitto con JavaScript/CSS: ricerca, risultati, contenuto, intestazione, piè di pagina, navigazione, barra laterale, paginazione, ecc.
- NON inserire badge o elementi Markdown all’interno del testo dell’intestazione.
- NON utilizzare titoli astratti di una sola parola come &quot;Panoramica&quot; o &quot;Introduzione&quot;. Descrivi sempre l’argomento della panoramica o dell’introduzione.
- NON numerare gli H1. Per i tutorial, utilizza il &quot;Passaggio 1: ...&quot; nelle sottorubriche anziché negli ancoraggi numerati.
- Maiuscole/minuscole per tutte le intestazioni (ad eccezione dei nomi corretti e degli elementi dell’interfaccia utente).
- Intestazioni del concetto: sostantivi e frasi sostantive (ad esempio, &quot;Panoramica sulla segmentazione&quot;).
- Intestazioni delle attività: verbi imperativi (ad esempio, &quot;Creare un flusso di lavoro di targeting&quot;). Evita i gerundi (forme-ing).
- Evita di comunicare i verbi con -ment o -ion (usa &quot;Crea una roadmap&quot; e non &quot;Creazione di una roadmap&quot;).
- Mantenere la struttura del titolo parallela all&#39;interno delle sezioni.
- Nessun ID di ancoraggio titolo duplicato in un documento.
- Se un&#39;intestazione include numeri, specificare un ID titolo esplicito che non inizi con un numero, ad esempio `## Release notes for 2016 {#release-notes-2016}`.

### Collegamenti

- Riferimenti incrociati interni: percorsi relativi alla radice che iniziano con `/help/`: `[link text](/help/path/to/file.md)`
- Collegamenti profondi agli ancoraggi: `[text](/help/path/to/file.md#anchor-id)`
- Collegamenti esterni (all&#39;esterno dell&#39;archivio): `https://` URL assoluti. Si aprono automaticamente in una nuova scheda.
- Apri esplicitamente in una nuova scheda: aggiungi `{target="_blank"}` (da utilizzare per i collegamenti tra guide).
- Collegamenti di riferimento (con stile `[1]: url`): funzionano solo con URL assoluti.
- NON aggiungere lo stesso file più volte in un sommario.
- Evita URL non elaborati nel corpo del testo. Utilizza sempre testo di collegamento descrittivo.
- Non utilizzare mai &quot;fai clic qui&quot; o &quot;collega&quot; come testo di collegamento. Gli assistenti vocali visualizzano i collegamenti fuori contesto e non sono in grado di distinguere più istanze &quot;click here&quot;.
- Il testo del collegamento deve rendere chiara la destinazione da sola.
- Per ulteriori informazioni sugli elenchi di riferimenti incrociati, utilizzare un sottotitolo `More help on this topic` con un elenco puntato.

### Immagini

- Sintassi: `![alt text](path/to/image.png)`
- Ridimensiona: `{width="300"}` o `{width="50%"}`
- Allinea: `{align="center"}` o `{align="right"}`
- Zoomable: `{zoomable="yes"}`
- Visualizzazione modale: `{modal="regular"}`. NON combinare con un collegamento.
- Larghezza consigliata: da 640 a 2000 px. Dimensione massima del file: si consigliano 5 MB; limite rigido di 100 MB. Massimo 100 immagini per articolo.
- Le immagini vengono inserite in una sottocartella `assets/` relativa al file markdown.
- Le immagini che NON devono essere localizzate vanno in una sottocartella `do-not-localize/`.
- Acquisisci sempre gli screenshot utilizzando il tema **Light** nell&#39;interfaccia utente del prodotto Experience Cloud, non il tema scuro.
- NON mostrare i dati dei clienti nelle schermate.
- NON documentare le interfacce di terze parti nelle schermate. Collega invece alla documentazione di terze parti.
- NON utilizzare le schermate solo per tenere traccia dell’avanzamento attraverso le schermate o mostrare elementi ovvi dell’interfaccia utente.
- NON includere illustrazioni di icone facilmente identificabili più di una volta per articolo
- NON utilizzare immagini di codice. Utilizza invece i blocchi di codice.
- NON utilizzare il solo colore per trasmettere le informazioni (non accessibile per gli utenti non vedenti).
- NON utilizzare immagini animate che lampeggiano più di tre volte al secondo (rischio di convulsioni).
- Assicurati che le immagini presentino un buon contrasto e siano chiare.
- Linee guida per le dimensioni dei pixel nelle schermate: 2000 px max per le immagini di grandi dimensioni, 672 px per le immagini di medie dimensioni, 300 px per le immagini di piccole dimensioni, 30-35 px per le icone.
- Per le didascalie: utilizzare #EB1000 HEX rosso, spessore linea 3 px, raggio angolo 8 px.

### Testo alternativo

Il testo alternativo viene indicizzato da Google e letto dagli assistenti vocali. Scrivilo sempre con attenzione.

- Descrivi cosa mostra l’immagine, non solo il nome dello schermo.
- Utilizza frasi complete con grammatica e punteggiatura appropriate.
- Includi testo rilevante dall’immagine.
- Usa parole intere, non abbreviazioni. Gli assistenti vocali scrivono le abbreviazioni.
- NON iniziare con &quot;Questa immagine mostra...&quot;. È sufficiente descrivere direttamente il contenuto.
- Il testo alternativo di solito non è necessario per le immagini puramente decorative, ma lo fornisce in caso di dubbi.

| Testo alternativo valido | Evita |
|---|---|
| Schermata di Audience Builder che mostra i filtri demografici per area geografica ed età selezionati. | Generatore di pubblico |
| Seleziona un&#39;estensione dal catalogo delle estensioni. | Libreria delle estensioni |

### Video

- Sintassi: `>[!VIDEO](https://video.tv.adobe.com/v/xxxxx/?quality=12&learn=on)`
- Aggiungi `?quality=12&learn=on` alla fine di tutti gli URL video per una migliore riproduzione.
- I video NON devono essere riprodotti automaticamente. Non aggiungere `?autoplay=true` nella documentazione.
- Fornisci sempre un testo alternativo, una trascrizione o un collegamento alle istruzioni scritte: &quot;Per le istruzioni scritte, consulta [collegamento].&quot;
- Utilizza didascalie significative.
- Abilitare le trascrizioni con `{transcript=true}` nei singoli video o aggiungere `auto-video-transcripts: true` a `TOC.md` per un&#39;intera guida.

### Note e avvertenze

```markdown
>[!NOTE]
>
>Note content here.

>[!TIP]
>
>Tip content here.

>[!IMPORTANT]
>
>Important content here.

>[!WARNING]
>
>Warning content here.

>[!CAUTION]
>
>Caution content here.
```

Tipi aggiuntivi: `[!ADMIN]`, `[!AVAILABILITY]`, `[!PREREQUISITES]`, `[!INFO]`, `[!ERROR]`, `[!SUCCESS]`.

Regole di sintassi CRITICHE:
- Deve essere presente una riga `>` vuota tra la riga del tag e il contenuto.
- Ogni riga di continuazione deve iniziare con `>`.
- La sintassi Blockquote (`>` senza tag) è supportata, ma viene eseguita come blockquote normale. NON utilizzarlo in presenza di callout con stile.
- NON aggiungere commenti all’interno di componenti di blocco come gli elenchi puntati, in particolare gli elenchi puntati nidificati. Il commento può modificare il rendering dell’elenco.

### Schede

```markdown
>[!BEGINTABS]

>[!TAB Tab label]

Tab content here.

>[!TAB Another tab]

More content.

>[!ENDTABS]
```

- NON nidificare le schede.
- NON nidificare i set di schede all’interno degli elenchi.
- I titoli delle schede non possono essere formattati in grassetto o corsivo.
- La ricerca nella pagina (Ctrl+F) non trova contenuto nelle schede nascoste.

### Sezioni comprimibili

```markdown
+++Click to expand
Content here.

* Bullet one
* Bullet two

+++
```

- Aggiungi righe vuote sopra e sotto gli elenchi e i blocchi di codice all’interno di elementi comprimibili.
- NON nidificare sezioni comprimibili all&#39;interno di sezioni comprimibili.
- Le intestazioni all&#39;interno di elementi comprimibili sono consentite ma non consigliate.
- Nota: Trova nella pagina (Ctrl+F) rileva il testo compresso in Chrome ma non in Safari.

### Scatole ombreggiate

```markdown
>[!BEGINSHADEBOX "Optional Title"]

Content with gray background.

>[!ENDSHADEBOX]
```

### Blocchi di codice

- In linea: singoli backtick `` `code` ``. Da utilizzare per nomi di cookie, nomi di file, valori, parametri, comandi e URL di esempio che non devono essere convalidati.
- Blocchi delimitati: tre apici retroversi con identificatore del linguaggio (abilita l’evidenziazione della sintassi e un pulsante Copia).
- Attributi facoltativi: `{line-numbers="true"}`, `{start-line="7"}`, `{highlight="11-13, 16"}`
- I blocchi di codice NON sono localizzati. Non è necessario aggiungere DNL o UICONTROL al loro interno.
- Utilizza gli apici retroversi (non le virgolette) per il codice, i nomi di file, i parametri e il testo digitato.
- NON utilizzare immagini di codice. Utilizza sempre blocchi di codice.

### Distintivi

- In linea: `[!BADGE Beta]{type=Informative}`
- Metadati (sopra H1): `badgePremium: label="Premium" type="Positive"`
- Tipi: `Informative` (blu), `Positive` (verde), `Negative` (rosso), `Neutral` (grigio scuro), `Caution` (giallo)
- Massimo 2 badge nei metadati per articolo.
- NON inserire badge nei titoli.
- NON utilizzare i badge per informazioni che diventano rapidamente obsolete (ad esempio, &quot;Nuovo&quot;).
- Le etichette dei badge sono localizzate. Tienili concisi.
- Per il badge beta, utilizzare solo frontmatter `badgeBeta`. NON inserire un badge in linea in H1.
- Se desideri che un URL del badge venga aperto in una nuova scheda, aggiungi `newtab=true` alla sintassi del badge.

### Elenchi

- Utilizza `*` o `-` in modo coerente all&#39;interno di un singolo articolo. Controlla la convenzione del file esistente. La combinazione di marcatori causa un errore di convalida.
- Per gli elenchi numerati, utilizzare `1.` per ogni elemento. GitHub/EDS effettua correttamente la numerazione automatica.
- Elenchi puntati: quando l’ordine non è importante. Elenchi numerati: per passaggi e procedure ordinate.
- Per una procedura in un solo passaggio, utilizzare un punto elenco (`*`) anziché `1.`.
- Mantieni brevi le voci elenco. Di solito una frase o meno.
- Utilizza i periodi per le frasi complete; ometti i periodi per le voci a parola singola o a frase incompleta (applica la regola in modo coerente all’interno di un elenco).
- NON terminare le voci di elenco con punti e virgola, virgole o combinazioni come &quot;and&quot; o &quot;or&quot; se gli elementi sono intesi per essere letti come serie semplice.
- Tutte le voci dell&#39;elenco devono essere grammaticalmente parallele.
- Rientra contenuto nidificato: 3 spazi per gli elenchi numerati, 2 per gli elenchi puntati.
- Circonda gli elenchi con righe vuote.
- NON utilizzare elenchi di attività (caselle di controllo `- [ ]` in stile GitHub). Non sono supportati in Experience League.

### Tabelle

- Utilizza tabelle markdown standard.
- Per i layout complessi (celle unite, bordi disattivati), è consentito HTML `<table>`.
- Tabelle surround con linee vuote.
- Utilizza `{style="table-layout:auto"}` per le tabelle con larghezza automatica quando necessario.
- Evita le schermate nelle celle della tabella. Nelle celle è possibile utilizzare icone o miniature di piccole dimensioni.

### Evidenziazione della funzione di anteprima

Utilizza un’estensione per il contenuto di anteprima in linea e un div per il contenuto di anteprima con più paragrafi:

```markdown
<span class="preview">This feature is in limited availability.</span>
```

```markdown
<div class="preview">

Multiple paragraphs of preview content here.

</div>
```

### Snippet e include

```markdown
{{$include /path/to/snippet.md}}
```

Da utilizzare per blocchi di contenuto riutilizzabili condivisi tra più articoli.

### Caratteri speciali

- Esci dai caratteri speciali nel corpo del testo con una barra rovesciata: `\#`, `\*`, `\[`, `\]`.
- Utilizzare le entità HTML per le parentesi: `&lt;`, `&gt;`, `&amp;`.
- Utilizzare le entità HTML per i simboli speciali: `&reg;`, `&mdash;`, `&ndash;`.

### Commenti

Utilizzare i commenti di HTML per la bozza di testo o le note per altri autori:

```markdown
<!-- This is a comment. Not rendered in the published doc. -->
```

I commenti SONO visibili agli utenti che modificano su GitHub.com. NON includere informazioni riservate nei commenti.

NON aggiungere commenti all’interno di componenti di blocco come gli elenchi puntati (in particolare quelli nidificati). I commenti possono interrompere il rendering dell’elenco. Nei file TOC.md, non commentare le righe al centro dell&#39;elenco, ma spostare i commenti alla fine del file.

### Azioni da tastiera

Assegna il grassetto a ogni singolo tasto in una scelta rapida da tastiera: **cmd** + **shift** + **p**.

### Denominazione di file e cartelle

- Nomi di file Markdown: in minuscolo con trattini. Nessun carattere maiuscolo, carattere di sottolineatura, punto o spazio.
- Utilizzare i tag descrittivi: `create-calculated-metric.md`, `calculated-metric-overview.md`. Evitare nomi file vuoti come `overview.md` o `introduction.md` a meno che IA non richieda un nome fisso.
- Evitare nomi di file in conflitto con JavaScript/CSS: `metadata.md`, `search.md`.
- Nomi file risorsa: preferiti in minuscolo; lettere maiuscole e caratteri di sottolineatura consentiti ma non consigliati.

&#x200B;---

## &#x200B;3. Tag di localizzazione (CRITICO)

Applica sempre i tag di localizzazione. La traduzione automatica viene eseguita automaticamente a ogni commit in main.

### `[!DNL Product Name]`: non localizzare

Usare per i nomi di prodotto di marca che devono rimanere in inglese.

**Applica a:**
- Nomi prodotti Adobe: `[!DNL Analytics]`, `[!DNL Target]`, `[!DNL Campaign]`, `[!DNL Experience Platform]`
- Nomi di prodotti di terze parti: `[!DNL Mozilla Firefox]`, `[!DNL Workfront]`
- Nomi funzionali che potrebbero confondere la traduzione: `[!DNL Pass]`, `[!DNL Campaign]`
- Operatori booleani utilizzati come termini logici: `[!DNL AND]`, `[!DNL OR]`

**NON applicare a:**
- URL, nomi di file o nomi di directory
- Blocchi di codice (non localizzati per impostazione predefinita)
- Acronimi (rimani automaticamente in inglese)
- Termini già presenti nel database Do Not Translate

**Nel testo del collegamento:** Rimuovere le parentesi per evitare problemi di rendering. Usa `[Adobe](https://www.adobe.com)` e non `[[!DNL Adobe]](https://www.adobe.com)`.

### `[!UICONTROL Label]`: Controlli interfaccia utente

Utilizza per gli elementi dell’interfaccia: opzioni, campi, schede, pagine, menu, pulsanti e nomi delle funzioni così come vengono visualizzati nell’interfaccia utente. Questo è il tag più importante per la qualità della traduzione. Consideralo obbligatorio nelle procedure.

**Applica a:**
- Ogni elemento dell’interfaccia utente cliccabile nei passaggi della procedura (obbligatorio)
- Nomi di funzioni ed elementi di navigazione come mostrato nel prodotto
- Nomi di pagina, opzioni, campi e schede come etichettati nell’interfaccia

**Formattazione:**
- Grassetto nei passaggi e nella navigazione: `Select **[!UICONTROL Destinations]** from the left navigation.`
- Il corsivo è accettabile nel testo concettuale (senza passaggi) per maggiore chiarezza.
- Nelle tabelle di HTML: utilizzare `<span class="uicontrol">term</span>` anziché &grave;&grave;.
- Nel testo del collegamento: rimuovi le parentesi quadre.

**Maiuscole:** Corrispondenza esatta con l&#39;interfaccia.

**NON applicare a:**
- Termini generici utilizzati concettualmente: &quot;segmento&quot;, &quot;metrica&quot;, &quot;campagna&quot; (solo tag quando si fa riferimento esplicito all’elemento dell’interfaccia utente)
- Frasi lunghe (a meno che il nome dell’elemento dell’interfaccia utente non sia una frase lunga)
- Blocchi di codice o acronimi
- Descrizioni delle icone. Utilizza il nome visualizzato al passaggio del mouse o la descrizione comando dell’icona, se disponibile; non assegnare tag a descrizioni generiche come &quot;icona a forma di matita&quot;

### `[!DNL]`: Escludere intere sezioni

Racchiudi il contenuto che deve rimanere in inglese per tutte le lingue:

```markdown
>[!DNL]
>
>Content that must not be translated.
```

Non necessario all’interno di blocchi di codice. Questi non sono localizzati per impostazione predefinita.

### Dove è possibile e non è possibile utilizzare i tag

**Può essere utilizzato in:** paragrafi, elenchi, intestazioni, tabelle, badge, testo alternativo e metadati.

**Impossibile utilizzare in:** blocchi di codice, acronimi.

**Regola metadati:** Se un campo metadati (titolo o descrizione) inizia con un tag `[!DNL]` o &grave;&grave;, racchiudere l&#39;intero valore del campo tra virgolette o la convalida non riuscirà.

&#x200B;---

## &#x200B;4. Struttura delle informazioni e tipi di contenuto

### Tre tipi di contenuto: mantenili separati

- **Concetto**: cosa e perché. Introduzioni, panoramiche, informazioni di base. Utilizza intestazioni sostantivo/sostantivo.
- **Attività**: Come. Procedure dettagliate. Utilizza i titoli dei verbi imperativi. Sempre preceduta da un concetto.
- **Riferimento**: campi, parametri, opzioni, codici di errore. Utilizzare le tabelle. Raccogliere con altro materiale di riferimento.

### Struttura dell’articolo

- Apri con contesto concettuale che orienta il lettore.
- Quindi spostarsi sulle attività e fare riferimento al materiale.
- Rispondi a una domanda mirata per pagina. Non troppo ampio, non troppo stretto.
- Pagina del concetto con pagine delle attività secondarie (multipagina), oppure sottotitoli H1 Concetto + H2 attività (pagina singola).
- Per collegare i termini di ricerca, introduce una volta i sinonimi o i nomi precedenti (ad esempio, &quot;ECID (Experience Cloud ID)&quot;).

### Passaggi

- Ogni passaggio è un singolo comando: una frase completa con un punto (o due punti se si introduce un sottoelenco).
- I passaggi iniziano sempre con un verbo o con l’obiettivo prima dell’azione: &quot;Per eseguire il rapporto, seleziona Esegui&quot;.
- Combina piccole azioni che si verificano nella stessa posizione nell’interfaccia utente in un unico passaggio quando la frase rimane chiara.
- Target 7 passaggi per attività; 10 è il massimo pratico. Dividi le attività più lunghe in sottoattività.
- Utilizzare un singolo punto elenco (non `1.`) per una procedura che include un solo passaggio.
- NON utilizzare i titoli come passaggi nella documentazione del prodotto. Per i tutorial lunghi su più pagine, utilizza i sottotitoli di stile &quot;Passaggio 1: ...&quot; quando necessario.
- Posizionare le informazioni sul passaggio (testo esplicativo) rientrate su una nuova riga dopo il passaggio.
- Posiziona le schermate rientrate dopo il passaggio o l’azione che causa la visualizzazione della schermata.
- Ripeti i nomi delle pagine, delle schede o dei pannelli nei passaggi in modo che i lettori sappiano dove si trovano.

### File TOC (TOC.md)

- Tutte le voci sono indicate in lettere maiuscole e minuscole, ad eccezione dei nomi e degli elementi dell’interfaccia utente.
- Voci di concetto: sostantivi e frasi sostantive.
- Voci di attività: verbi imperativi (non gerundi).
- Mantieni le voci parallele.
- Ogni intestazione di sezione nel sommario deve avere un ID di ancoraggio valido: `+ Processing rules {#processing-rules}`
- Un&#39;intestazione di sezione (padre) nel sommario non può essere un collegamento. Deve avere un ID di ancoraggio.
- NON aggiungere lo stesso file più volte in un sommario.
- NON commentare le righe al centro di un elenco sommario. Spostare i commenti alla fine del file.

### Nascondere i file dalla navigazione

Utilizzare il metodo **V2** per tutte le nuove operazioni. Metodo V1 obsoleto.

**V2 (corrente): `{hide-from-toc}` in TOC.md**

Posiziona `{hide-from-toc}` direttamente in `TOC.md` prima dell&#39;articolo o della sezione che desideri nascondere. NON aggiungerlo all’articolo frontmatter.

```
+ {hide-from-toc} [Article title](filename.md)
+ {hide-from-toc} Section name {#section-id}
  + [Nested article](nested.md)
```

- Gli articoli nascosti rimangono accessibili tramite URL diretto.
- Una sezione le cui voci sono tutte nascoste scompare dalla navigazione a sinistra.

**V1 (obsoleto): `hidefromtoc: yes` in frontmatter**

```yaml
hidefromtoc: yes
```

NON utilizzarlo nelle nuove pagine. L&#39;articolo deve comunque essere visualizzato in `TOC.md` per essere pubblicato, ma non verrà visualizzato nel menu di navigazione a sinistra.

**Nascondi dai motori di ricerca: `hide: yes` in frontmatter**

```yaml
hide: yes
```

Questo esclude la pagina sia dalla ricerca esterna che da quella interna. L&#39;impostazione di `hide: yes` imposta automaticamente `index: no`. Usare questo elemento in aggiunta a `{hide-from-toc}` quando si desidera nascondere una pagina sia dalla navigazione che dalla ricerca.

&#x200B;---

## &#x200B;5. Terminologia e branding

Origine autorevole: [wiki sulla terminologia di AEP rivolto all&#39;utente](https://wiki.corp.adobe.com/spaces/DMSArchitecture/pages/1230620427/Adobe+Experience+Platform+User-Facing+Terminology). Consultare sempre tramite lo strumento MCP di Confluenza (`mcp__adobe-wiki-confluence`) per l&#39;ultima versione.

### Nomi di prodotto

Utilizza sempre questi moduli esatti. Includi &quot;Adobe&quot; al primo riferimento in una guida; puoi rilasciarlo nelle menzioni successive in cui la policy lo consente.

NON anteporre &quot;the&quot; ai nomi dei prodotti, a meno che il nome ufficiale non lo contenga.
- Risposta corretta: &quot;Introduzione all&#39;Assistente AI&quot;.
- Errato: &quot;Introduzione all’Assistente AI&quot;.

| Corretto | NON usare MAI |
|---|---|
| Adobe Experience Platform | AEP, AXP, Adobe XP, Adobe Cloud Platform |
| Experience Platform (riferimento secondario) | Platform (da sola, a meno che il contesto non sia univoco) |
| Adobe Real-Time CDP | RTCDP, ARTCDP |
| Real-Time CDP (secondario) | Real-time CDP (&quot;t&quot; minuscola) |
| Adobe Real-Time Customer Data Platform | — |
| Profilo cliente in tempo reale | Profilo cliente in tempo reale, Profilo unificato |
| Adobe Journey Optimizer | AJO |
| Adobe Journey Optimizer B2B Edition | AJO B2B |
| Adobe Marketo Optimizer | AMO |
| Adobe Marketo Engage | Marketo (non può essere usato come aggettivo) |
| Adobe Customer Journey Analytics | CJA |
| Customer Journey Analytics (secondario) | — |
| Adobe Real-Time CDP Collaboration | RTCDP Collaboration, RTCDP Collab, Collab |
| Connessioni Adobe Real-Time CDP | Connessioni RTCDP, Connessioni AEP, Connessioni (da sole) |
| Adobe Experience Platform Edge Network | Platform Edge Network, Platform Edge, Adobe Experience Edge |
| Tag (nome prodotto) | Launch (obsoleto) |
| Gestione delle decisioni | Offer Decisioning (solo parentesi: &quot;precedentemente Offer Decisioning&quot;) |
| flusso di dati (una parola, lettere minuscole) | datastreaming, configurazione edge |
| Analysis Workspace | analysis workspace, workspace, Workspace |
| Adobe AI | Sensei (obsoleto) |
| Adobe GenAI | — |
| Adobe GenStudio for Performance Marketing | — |

**&quot;Real-Time&quot;** utilizza sempre il capitale R e il capitale T quando fanno parte del nome di un prodotto (Real-Time CDP, Real-Time Customer Profile, Real-Time Customer Data Platform).

**Edizioni**: &quot;edizioni&quot; è in lettere minuscole genericamente; &quot;Edizione&quot; è in lettere maiuscole come parte del nome di un&#39;edizione di prodotto (ad esempio, &quot;Adobe Real-Time CDP B2C Edition&quot;).

**Abbreviazioni nelle comunicazioni esterne**: NON abbreviare i nomi dei prodotti nella documentazione visualizzata dall&#39;utente. Nella documentazione non sono presenti AEP, CJA, AJO o RTCDP. Eccezioni limitate: gli acronimi possono comparire tra parentesi al primo utilizzo quando facilitano l’ottimizzazione SEO (Search Engine Optimization), oppure nelle voci del sommario, nei metadati della descrizione e nelle intestazioni in cui la lunghezza è un problema.

### Terminologia funzionale e concettuale

| Corretto | NON usi |
|---|---|
| inoltro eventi | inoltro lato server, Launch Server Side |
| INSERISCO NELL&#39;ELENCO CONSENTITI DI | whitelist |
| INSERISCO NELL&#39;ELENCO BLOCCATI DI / | blacklist |
| principale/replica OPPURE primario/secondario (server) | master/slave |
| principale (ramo GitHub) | principale |
| hacker etico | hacker con cappello bianco |
| remarketing | retargeting |
| gruppo di campi | mixin (obsoleto), estensioni, mixin |
| scadenza automatica dei dati | TTL, time-to-live, scadenza |
| sandbox non di produzione | staging (come nome di ambiente) |
| definizione del segmento | segmento (solo, quando significa la definizione) |
| ID (maiuscole sempre) | ID |
| acquisizione/acquisizione/acquisizione | onboarding (per aggiungere dati a Platform) |
| set di dati/set di dati | File di dati, file di set di dati |
| controllo degli accessi | autorizzazioni (per la funzione Platform) |
| widget | scheda metrica (obsoleto) |
| variabile segnaposto | variabile fittizia |
| non disponibile / bloccato / disattivato / disattivato | disattivato |
| verifica di coerenza | controllo di integrità |
| incorporato | nativo (come sinonimo di integrato) |
| priorità alta | unghie obbligatorie |
| legacy | clausola di salvaguardia |
| principale/principale/sorgente | master (come descrittore) |

**Uso delle maiuscole specifico per Analytics:**
- I nomi dei pannelli sono minuscoli: vuoto, attribuzione, sperimentazione, figura a mano libera (eccezione: &quot;area di lavoro Percorso&quot;)
- I nomi delle visualizzazioni sono in minuscolo: barra, ciambella, istogramma, linea, mappa ad albero, testo

### Termini solo interni: NON utilizzare MAI in documenti rivolti al pubblico

Questi termini vengono visualizzati in Jira, wiki e discussioni interne, ma non devono mai essere visualizzati nella documentazione:

| Termine interno | Utilizza invece |
|---|---|
| AEP | Adobe Experience Platform |
| PALMO | gestione sandbox/controllo degli accessi |
| BIOME | environment |
| Idrato/idratazione | crea/popola |
| Profilo unificato | Profilo cliente in tempo reale |
| Staging (ambiente) | sandbox non di produzione |
| DTM | Tag |
| Tenant | Organizzazione IMS |
| CRUD | crea, leggi, aggiorna ed elimina (scrivi) |
| Sifone, BSO, Ethos | nomi di codice interni, mai esterni |
| Luppolo | termine interno RGPD/controllo degli accessi |
| Ritmo | termine pubblicitario non rivolto all&#39;utente |
| Pipeline | termine dell’infrastruttura Adobe interna |

&#x200B;---

## &#x200B;6. Linguaggio inclusivo e accessibilità

### Principi linguistici inclusivi

- Utilizza termini indipendenti dal genere: &quot;rappresentante commerciale&quot; non &quot;venditore&quot;, &quot;moderatore&quot; non &quot;presidente&quot;.
- Preferisci la seconda persona (&quot;tu&quot;) per evitare i pronomi di genere.
- Utilizza singolarmente &quot;loro&quot; per una persona il cui genere è sconosciuto. NON usi lui/lei o lui/i.
- Includere nomi di culture non bianche in esempi (ad esempio, Ayesha, Ibrahim, Vignesh, Quynh). NON usare solo nomi culturalmente bianchi (John, Bill, Karen, Amy).
- NON confondere il sesso (maschile/femminile) con il sesso (uomo/donna).
- Capitalizzare le nazionalità, i popoli, le razze (diverse da &quot;bianchi&quot;, secondo lo Stylebook di AP), e le tribù.
- Usa il linguaggio personalizzato: &quot;persone che usano la tecnologia per l&#39;accessibilità&quot;, non &quot;disabili&quot;.
- Evita eufemismi come &quot;diversamente abili&quot;. Evita i descrittori usati come sostantivi: &quot;il cieco&quot;, &quot;il sordo&quot;.
- Evita termini che riflettono l&#39;identità (appropriazione culturale): spirito animale, sherpa, pow wow, guru, ninja, tribù.

### Terminologia non inclusiva da evitare

| Utilizzo | Non |
|---|---|
| INSERISCO NELL&#39;ELENCO CONSENTITI / ELENCO BLOCCATI DI / DI | whitelist/blacklist |
| principale/replica OPPURE principale/secondario | master/slave |
| principale (ramo Git) | principale |
| priorità alta | unghie obbligatorie |
| variabile segnaposto | variabile fittizia |
| non disponibile / bloccato / disattivato / disattivato | disattivato |
| verifica di coerenza | controllo di integrità |
| incorporato | nativo (come sinonimo) |
| autorità/esperto | guru/ninja |
| membri del gruppo | membri della tua tribù |
| riunione | Pow wow / Circolare i carri |
| modello di ruolo / spirito affine | spirito animale |
| guida | Sherpa |
| legacy | clausola di salvaguardia |
| impresa inutile | marcia della morte |
| ridicolo/incompetente/imprevedibile | stupido / zoppo / pazzo |
| hacker etico/non etico | hacker cappello bianco / cappello nero |
| Riproduci video | Guarda il video |
| Visualizza/Mostra/Vai a tutti | Vedi tutto |

### Accessibilità: descrizione dell’interfaccia utente

NON descrivere gli elementi dell&#39;interfaccia utente in base al colore o alla posizione dello schermo. Il colore non funziona per gli utenti o gli assistenti vocali non vedenti. La posizione dello schermo non è affidabile con le tecnologie assistive.

**Usa linguaggio cronologico, non linguaggio spaziale:**

| Utilizzo | Non |
|---|---|
| Primo, Successivo, Finale | Sopra, sotto |
| Nella barra dei menu | A sinistra |
| Prima/Dopo | Nella parte superiore/inferiore dello schermo |

**Descrivere le operazioni dei controlli e non il loro aspetto:**

| Utilizzo | Non |
|---|---|
| Seleziona ricerca | Fare clic sull&#39;icona della lente di ingrandimento |
| Modifica | Icona della matita |
| Attivato/Disattivato | Commuta/commuta/attiva |
| Menu | Cassetto laterale |
| Immetti l’e-mail | Digita il tuo indirizzo email |
| Salva | Pulsante Salva |
| Annulla | Chiudi |

NON usare il solo colore per trasmettere le informazioni. Associare sempre il colore al testo o alla forma.

### Accessibilità: testo alternativo

- Descrivi cosa mostra l’immagine, non solo il nome dello schermo.
- Utilizza frasi complete con grammatica e punteggiatura appropriate.
- Includi testo rilevante dall’immagine.
- Usa parole intere, non abbreviazioni. Gli assistenti vocali scrivono le abbreviazioni ad alta voce.
- Le immagini che trasmettono informazioni indipendenti dal testo circostante DEVONO contenere testo alternativo.
- Le immagini puramente decorative possono omettere il testo alternativo, ma è buona prassi includerlo.
- Testare le immagini con un simulatore di daltonismo quando il colore viene utilizzato per trasmettere significato.
- NON utilizzare immagini animate che lampeggiano più di tre volte al secondo (rischio di convulsioni).

### Accessibilità: collegamenti

- Non utilizzare mai &quot;fai clic qui&quot; o &quot;collega&quot; come testo di collegamento.
- Cancellare la destinazione dal solo testo del collegamento.
  - Corretto: &quot;Consulta i prerequisiti di RTCDP nella Guida utente di RTCDP&quot;.
  - Scorretto: &quot;Fare clic qui per i prerequisiti&quot;.

### Accessibilità: video

- I video NON devono essere riprodotti automaticamente.
- Fornisci sempre un testo alternativo, una trascrizione o un collegamento per le istruzioni scritte.
- Includi didascalie significative in tutti i video.
- Se possibile, collegarsi alle istruzioni scritte: &quot;Per istruzioni scritte, vedere [collegamento].&quot;

&#x200B;---

## &#x200B;7. Controllo ortografia e punteggiatura

### Controllo ortografia inglese americano

| Utilizzo | Non |
|---|---|
| colore | colore |
| riconoscere | riconoscere |
| licenza | licenza |
| durante | durante |
| scadenza | scadenza |
| contatore | contatore |
| tra | tra |

### Regole di punteggiatura

- Le virgolette di chiusura vanno oltre le virgole e i punti.
- Riserva le virgolette per le persone. Non citare le stringhe dell’interfaccia utente (utilizza UICONTROL e il grassetto nei passaggi).
- Usa il corsivo per i termini utilizzati come termini (non virgolette): *profilo*, non &quot;profilo&quot;.
- Utilizzare i backtick per codice, parametri, nomi di file e testo digitato: `datasetId`.
- Grassetto: solo per gli elementi dell’interfaccia utente nelle procedure (con UICONTROL) e per i termini chiave alla prima introduzione. Le linee guida in grassetto sono accettabili nei layout delle domande frequenti che non utilizzano domande a livello di intestazione.
- Corsivo: per enfasi, parole straniere, termini definiti o nomi concettuali in testo non di passaggio.
- Grassetto + corsivo combinati: `***text***`.
- NON utilizzare regole orizzontali (`---` o `***`). Non sono supportati in Experience League.
- NON utilizzare trattini (—), trattini (-) o trattini in prosa. Riformula invece la frase. I trattini sono consentiti solo negli aggettivi composti visualizzati nell’interfaccia utente, nei nomi dei file e nel codice.
- Due punti: utilizza per introdurre un elenco. Usa l&#39;iniziale maiuscola dopo due punti quando segue una frase intera (o la parola è un nome proprio).
- Nessun punto e virgola. Utilizza invece un punto e una nuova frase.

&#x200B;---

## &#x200B;8. SEO e reperibilità

- Includi i termini di ricerca (parole chiave) nei primi paragrafi.
- Usa i termini cercati dai lettori. Includi i sinonimi e i nomi dei termini precedenti, se utili.
- Parole chiave nei titoli: includono i nomi delle funzioni, gli elementi dell’interfaccia e l’attività in esecuzione.
- Il testo alternativo nelle immagini viene indicizzato da Google. Rendilo descrittivo e significativo.
- Evita di inserire termini essenziali solo in tabelle o immagini complesse (non indicizzati in modo affidabile da IA o ricerca).
- Metadati di descrizione: utilizza il linguaggio naturale con parole chiave. NON comprimere parole chiave casuali. Google può abbassare di livello il contenuto per il riempimento delle parole chiave.
- Mantieni i campi dei metadati (titolo, descrizione, tag delle funzioni) completi e precisi. Le superfici di individuazione utilizzano i metadati per filtrare e classificare i risultati prima di leggere il contenuto della pagina.

&#x200B;---

## &#x200B;9. Convenzioni relative a file e repository

- È necessario specificare un valore per ogni file `.md`.
- Le immagini vengono inserite in una sottocartella `assets/` relativa al file markdown.
- Le immagini che non devono essere localizzate vanno in una sottocartella `do-not-localize/`.
- I file sommario (`TOC.md`) definiscono la struttura di spostamento a sinistra. Aggiornale quando aggiungi o rimuovi pagine.
- Utilizzare i collegamenti relativi alla directory principale (`/help/...`) per i riferimenti incrociati tra documenti in questo repository.
- Per i collegamenti ai documenti esterni a questo archivio, utilizza `https://experienceleague.adobe.com/it...` URL assoluti.
- Denominazione ramo: nessun prefisso del nome utente. Utilizzare il numero del ticket Jira e una barra del titolo (ad esempio, `PLAT-12345-Update-Guardrail-Limits`). Denomina sia la filiale che il titolo PR utilizzando lo stesso formato.
- I componenti discreti (intestazioni, blocchi di codice delimitati, elenchi) devono essere circondati da righe vuote.
- Un solo H1 (`#`) per documento. La prima linea dopo la parte anteriore deve essere la H1.

&#x200B;---

## &#x200B;10. Controlla elenco di controllo

Durante la revisione o la modifica della documentazione, verifica ogni elemento riportato di seguito.

**Voce e stile**

- [ ] voce incentrata sull&#39;utente. No &quot;consente di&quot;, &quot;consente di&quot;
- [ ] &quot;tu&quot; utilizzato al posto di &quot;utenti&quot; quando si rivolge direttamente al pubblico
- [ ] Seconda persona e umore imperativo nelle procedure
- [ ] voce attiva in tutto
- [ ] frasi target ≤20 parole
- [ ] Nessun aggettivo vago (&quot;veloce&quot;, &quot;facile&quot;). Sostituire con descrizioni precise.
- [ ] I termini chiave vengono visualizzati nel corpo del testo (non solo nelle immagini o nelle tabelle) per l&#39;individuazione IA

**Struttura e intestazioni**
- [ ] Titoli: maiuscole/minuscole, ≤5 parole/69 caratteri, seguiti dal corpo del testo, senza intestazioni sovrapposte
- [ ] Nessun livello di intestazione ignorato
- [ ] Le intestazioni del concetto sono frasi sostantive; le intestazioni delle attività sono verbi imperativi
- [ ] Target 7 passaggi per attività; massimo 10. Le procedure in un unico passaggio utilizzano un punto elenco, non `1.`
- [ ] Max 8 elementi per elenco puntato

**Terminologia**
- [ ] Correzione dei nomi e dei moduli dei prodotti (sezione 5)
- [ ] Nessun termine obsoleto: mixin, TTL, Offer Decisioning, Launch, Unified Profile, Real-time (t minuscolo), Sensei
- [ ] Nessun termine solo interno: AEP, PALM, BIOME, idrato, staging, DTM, tenant, pipeline
- [ ] Nessun termine non inclusivo: whitelist, blacklist, master/slave, controllo di sanità, fittizio, grigio, nativo, guru, ninja, spirito animale, sherpa, marcia della morte, pow wow, tribù
- [ ] No &quot;il&quot; prima dei nomi di prodotto (ad esempio, non &quot;il Adobe Experience Platform&quot;)

**Tag di localizzazione**
- [ ] &grave;&grave; su tutti i nomi di elementi dell&#39;interfaccia utente; grassetto nei passaggi
- [ ] `[!DNL]` su tutti i nomi di prodotti e terze parti
- [ ] operatori booleani con tag: `[!DNL AND]`, `[!DNL OR]`
- [ ] Nessun tag nei blocchi di codice
- [ ] I campi di metadati che iniziano con un tag sono racchiusi tra virgolette

**Sintassi Markdown**
- [ ] Sintassi corretta dell&#39;ammonizione (riga `>` vuota tra tag e contenuto)
- [ ] Gli elenchi utilizzano marcatori coerenti; gli elenchi numerati utilizzano `1.` per ogni elemento
- [ ] Nessun elenco attività (`- [ ]`)
- [ ] Nessuna regola orizzontale (`---` tra i contenuti)
- [ ] righe vuote che circondano intestazioni, blocchi di codice, elenchi e tabelle
- [ ] Nessuna immagine di codice. Utilizza i blocchi di codice.
- [ ] schermate utilizzano tema chiaro; nessun dato cliente; nessuna interfaccia utente di terze parti

**Accessibilità**
- [ ] Testo alt.: frasi complete, parole intere, descrive il contenuto (non solo il nome dello schermo)
- [ ] Nessun linguaggio direzionale/spaziale: nessun &quot;sopra&quot;, &quot;sotto&quot;, &quot;a sinistra&quot;, &quot;in alto a destra&quot;
- [ Il testo del collegamento ] descrive la destinazione. Nessun &quot;clic qui&quot;
- [ ] video non impostati per la riproduzione automatica; sono state fornite trascrizioni o alternative scritte
- [ ] Nessun colore utilizzato da solo per trasmettere le informazioni

**File e collegamenti**

- [ ] Argomento necessario: titolo (maiuscolo, ≤60 caratteri), descrizione (da 150 a 160 caratteri)
- [ ] Nessun URL vuoto nel corpo del testo. Utilizza sempre testo di collegamento descrittivo.
- [ ] collegamenti interni relativi alla radice; collegamenti assoluti per riferimenti cross-repo
- [ ] I nomi dei file sono in minuscolo con trattini; dettagli descrittivi (non nudi `overview.md`)
- [ ] immagini in `assets/`; immagini non localizzate in `do-not-localize/`

&#x200B;---

## &#x200B;11. Riferimenti esterni

Utilizza lo strumento MCP corretto in base al tipo di risorsa:

- **Ticket e problemi Jira** (`jira.corp.adobe.com`): utilizza lo strumento MCP Jira aziendale (`mcp__corp-jira`)
- **Wiki / Pagine di influenza** (`wiki.corp.adobe.com`): utilizzare lo strumento MCP di influenza (`mcp__adobe-wiki-confluence`)
- **Experience League pubblico / pagine Web**: usa WebFetch

**Pagine wiki interne (utilizzare lo strumento Confluence MCP):**
- **Wiki sulla terminologia**: https://wiki.corp.adobe.com/spaces/DMSArchitecture/pages/1230620427/Adobe+Experience+Platform+User-Facing+Terminology
- **Guida allo stile della piattaforma**: https://wiki.corp.adobe.com/spaces/DMSArchitecture/pages/1938986972/Platform+style+guide
- **Guida all&#39;accessibilità e all&#39;inclusività**: https://wiki.corp.adobe.com/spaces/DMSArchitecture/pages/2234798784/Writing+for+accessibility+and+inclusivity
- **Guida contestuale ai popover**: https://wiki.corp.adobe.com/spaces/DMSArchitecture/pages/2575057078/How+to+add+contextual+help+popovers+to+the+Experience+Platform+documentation+and+UI

**Pubblico (utilizzare WebFetch):**
- **Panoramica sulla localizzazione**: https://experienceleague.adobe.com/en/docs/authoring-guide/using/authoring/localization/localization-overview
- **Riferimento tag di localizzazione**: https://experienceleague.adobe.com/en/docs/authoring-guide/using/authoring/localization/localize
- **Sintassi markdown Experience League**: https://experienceleague.adobe.com/en/docs/authoring-guide/using/markdown/markdown-syntax
- **Scheda di riferimento Markdown**: https://experienceleague.adobe.com/en/docs/authoring-guide/using/markdown/cheatsheet
- **Riferimento stile note sulla versione**: https://experienceleague.adobe.com/it/docs/experience-platform/release-notes/latest

**Clone locale:**
- **Archivio guida all&#39;authoring:** seleziona la guida all&#39;authoring di Adobe Experience League o la relativa documentazione pubblica.
