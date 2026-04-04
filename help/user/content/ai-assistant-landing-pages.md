---
title: Assistente AI per il contenuto della pagina di destinazione
description: 'Generare contenuti di pagina di destinazione con AI Assistant: crea testo e immagini di pagina con le risorse di riferimento e il targeting del ruolo di gruppo di acquisto in Journey Optimizer B2B edition.'
feature: Generative AI, Landing Pages, Content
badgeBeta: label="Beta" type="informative" tooltip="Questa funzione è attualmente in versione beta limitata"
topic: Artificial Intelligence
role: User
level: Beginner
exl-id: d1e818fb-7450-4c13-bc6c-24da5fb71285
source-git-commit: 859656dc4e355be0d9efe9414ad93404970d6e73
workflow-type: tm+mt
source-wordcount: '2700'
ht-degree: 1%

---

# Assistente AI per il contenuto della pagina di destinazione {#generative-full-content}

L&#39;Assistente all&#39;intelligenza artificiale per il contenuto delle pagine di destinazione in [!DNL Adobe Journey Optimizer B2B Edition] utilizza le funzionalità di generazione dei contenuti basate sull&#39;intelligenza artificiale di Adobe e rivoluziona il modo in cui gli addetti al marketing creano contenuti professionali e coerenti con il marchio nelle pagine di destinazione. Con modelli di intelligenza artificiale generativi avanzati e una profonda comprensione delle linee guida del brand, AI Assistant genera automaticamente contenuti personalizzati, coinvolgenti ed efficaci. Utilizza il tuo obiettivo di marketing e ottimizza i contenuti per stili, layout, toni e altro ancora. AI Assistant rende la creazione e l’esecuzione di campagne e programmi più intuitiva, semplice e senza problemi. L’aggiunta di questa funzionalità ai flussi di lavoro consente di risparmiare tempo, migliorare l’efficienza e ottenere risultati migliori.

Puoi generare esperienze di contenuto complete per le pagine di destinazione, inclusi testo e immagini. Questa robusta funzionalità consente di creare contenuti coinvolgenti e on-brand che si connettono al pubblico.

>[!NOTE]
>
>Questa funzionalità è disponibile nella versione Beta e soggetta a modifiche senza preavviso.

>[!IMPORTANT]
>
>Per accedere a queste funzionalità in [!DNL Journey Optimizer B2B Edition], è necessario disporre dell&#39;autorizzazione _[!UICONTROL Assistente AI]_ > _[!UICONTROL Genera contenuto]_. Per ulteriori informazioni su come un amministratore di prodotto può concedere le autorizzazioni per le funzionalità, vedere [Modifica ruoli per le autorizzazioni per il prodotto](../admin/user-management.md#edit-roles-for-product-permissions).

## Linee guida e limitazioni

Prima di iniziare a utilizzare questa funzionalità, controlla le [linee guida e limitazioni](../ai-assistant/generative-ai-content.md#general-guidelines-and-limitations). Per poter utilizzare le funzionalità di intelligenza artificiale in [!DNL Journey Optimizer B2B Edition] è inoltre necessario accettare il [Contratto utente](https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html){target="_blank"}. Per ulteriori informazioni, contatta il tuo rappresentante Adobe.

Con l&#39;impegno di Adobe di promuovere la trasparenza nell&#39;utilizzo degli strumenti di intelligenza artificiale generativi nella creazione di contenuti multimediali, Adobe applica [credenziali di contenuto](https://helpx.adobe.com/firefly/web/get-started/learn-the-basics/content-credentials-overview.html){target="_blank"} a qualsiasi contenuto o progetto che include una risorsa generata da Firefly al momento del download o dell&#39;esportazione.

Le limitazioni e le linee guida seguenti si applicano alle funzioni dell&#39;Assistente IA utilizzate per la generazione del contenuto della pagina di destinazione in [!DNL Journey Optimizer B2B Edition]:

* L’inglese è l’unica lingua supportata.
* I contenuti generati potrebbero non essere accurati: condividi il tuo feedback in modo che i tecnici Adobe possano perfezionare i modelli.
* Puoi caricare più risorse di riferimento di contenuto, ma puoi sfruttarne una sola per una generazione specifica.
* Utilizza un modello personalizzato o specifico per il brand per generare contenuti per una pagina di destinazione completa. Si consigliano modelli di pagina di destinazione con un massimo di 8-10 immagini.
* Assicurati di segnalare eventuali output problematici utilizzando le icone thumb up, thumb down o flag quando selezioni le varianti generate.

## Input e impostazioni per la generazione di contenuti

Puoi generare contenuto completo per una pagina di destinazione o per i componenti selezionati nella pagina. Quando si utilizzano gli strumenti di Assistente AI per generare il contenuto necessario, è possibile fornire l’input, inclusi i prompt e il contenuto di riferimento, e le impostazioni per il testo e le immagini.

### Prompt

Utilizza prompt ben definiti per il modello di intelligenza artificiale generativo per interpretare con precisione. L’obiettivo/richiesta di marketing che fornisci influisce notevolmente sulla qualità del contenuto generato.

![Campo richiesta](./assets/gen-ai-prompt.png){width="320"}

Per ulteriori informazioni sulla creazione di prompt effettivi, vedere _[Best practice per i prompt](../ai-assistant/generative-ai-content.md#generative-ai-prompting-guide)_.

>[!BEGINSHADEBOX]

**Libreria di richieste**

Un prompt efficace è essenziale per generare i contenuti migliori possibili. Se desideri assistenza per la creazione del prompt, fai clic sull&#39;icona _Libreria prompt_ ![Icona Libreria prompt](../assets/do-not-localize/icon-library.svg) per accedere a una libreria di idee prompt organizzate in base agli obiettivi. Immettere il testo nel campo di ricerca per trovare un prompt basato su una stringa di parole chiave.

![Assistente AI - Accesso alla libreria dei prompt](./assets/gen-ai-prompt-library.png){width="600" zoomable="no"}

Selezionare il prompt che meglio riflette gli obiettivi desiderati e fare clic su **[!UICONTROL Prova questo prompt]**. Nel campo _[!UICONTROL Chiedi conferma]_, sostituisci eventuali segnaposto (ad esempio `[Key Feature/Information]`) con i valori necessari che specificano il tuo marchio, la tua offerta, la tua campagna e i tuoi casi d&#39;uso.

>[!ENDSHADEBOX]

### Impostazioni testo

Espandi le **[!UICONTROL Impostazioni testo]** nel pannello di destra e imposta le opzioni per il testo generato.

* **[!UICONTROL Gruppo di acquisto]** - Scegli il [ruolo gruppo di acquisto](../buying-groups/buying-groups-role-templates.md) da utilizzare per il targeting dei messaggi.
* **[!UICONTROL Fase percorso marketing]** - Scegli la [fase gruppo acquisti](../buying-groups/buying-group-stages.md) da utilizzare per il targeting dei messaggi.
* **[!UICONTROL Strategia di comunicazione]** - Scegli lo stile di comunicazione più adatto al testo generato.
* **[!UICONTROL Lingua]** - Scegli la lingua del contenuto generato.
* **[!UICONTROL Tono]** - Il tono dovrebbe risuonare con il tuo pubblico. Ad esempio, puoi impostare il messaggio in modo che abbia un suono informativo, giocoso o persuasivo.

![Pannello Impostazioni testo che mostra le opzioni relative al gruppo di acquisto, alla fase del percorso marketing, alla strategia di comunicazione, alla lingua e al tono](./assets/gen-ai-text-settings.png){width="350" zoomable="yes"}

Fare clic sulla freccia sinistra per tornare alle _[!UICONTROL Impostazioni]_ principali.

### Impostazioni immagine

Per includere le immagini nel contenuto generato, espandi le **[!UICONTROL Impostazioni immagine]** nel pannello di destra e imposta le opzioni.

Per impostazione predefinita, l&#39;opzione **[!UICONTROL Generate images using AI]** è disabilitata. Abilita questa funzione e imposta le seguenti opzioni per includere le immagini generate nelle varianti di contenuto proposte:

* **[!UICONTROL Modello generativo]**: seleziona dal modello fornito da Adobe pronto per l’uso, dal modello partner per funzionalità specializzate o dai modelli personalizzati configurati addestrati sulle risorse del tuo marchio. Per ulteriori informazioni sui modelli generativi, consulta _[Modelli di intelligenza artificiale generativa per l&#39;allineamento del brand](generative-ai-models.md)_.
* **[!UICONTROL Proporzioni]**: quando è selezionato un componente immagine, questa impostazione determina la larghezza e l&#39;altezza della risorsa. È possibile scegliere tra rapporti comuni quali 16:9, 4:3, 3:2 o 1:1 oppure immettere una dimensione personalizzata.
* **[!UICONTROL Tipo di contenuto]**: il tipo categorizza la natura dell&#39;elemento visivo, distinguendo tra diverse forme di rappresentazione visiva, come foto, grafica o grafica.
* **[!UICONTROL Intensità visiva]**: controlla l&#39;impatto dell&#39;immagine regolandone l&#39;intensità. Un&#39;impostazione più bassa (ad esempio 2) crea un aspetto più morbido e più contenuto, mentre un&#39;impostazione più alta (ad esempio 10) rende l&#39;immagine più vibrante e visivamente potente.
* **[!UICONTROL Colore e tono]**: l&#39;aspetto complessivo dei colori all&#39;interno di un&#39;immagine e l&#39;umore o l&#39;atmosfera che trasmette.
* **[!UICONTROL Illuminazione]**: lo stile di illuminazione utilizzato per l&#39;immagine, che ne forma l&#39;atmosfera ed evidenzia elementi specifici.
* **[!UICONTROL Composizione]**: disposizione degli elementi all&#39;interno della cornice di un&#39;immagine.

![Pannello Impostazioni immagine che visualizza le opzioni Modello generativo, Tipo di contenuto, Intensità visiva, Colore e tono, Illuminazione e Composizione](./assets/gen-ai-image-settings.png){width="350" zoomable="yes"}

Fare clic sulla freccia sinistra per tornare alle _[!UICONTROL Impostazioni]_ principali.

### Contenuto di riferimento

Carica le risorse di contenuto di riferimento per generare contenuti precisi per il brand. In caso contrario, il contenuto generato si basa su informazioni disponibili pubblicamente. Il contenuto di riferimento funge da origine per la generazione di contenuti e per i consigli sulle immagini. Per le linee guida e le best practice, consulta _[Contenuto di riferimento ottimizzato](../ai-assistant/generative-ai-content.md#reference-content)_.

Dalle impostazioni del **[!UICONTROL contenuto di riferimento]**, fare clic su **[!UICONTROL Carica file]** per aggiungere qualsiasi risorsa contenente contenuto da utilizzare per il contesto aggiuntivo.

![Carica il file da utilizzare per il contenuto di riferimento](./assets/gen-ai-reference-content-upload.png){width="350" zoomable="yes"}

Il file da caricare può essere nei seguenti formati: PDF, JPEG, PNG o file ZIP (contenenti i formati di file supportati). La dimensione massima per una risorsa marchio caricata è di 50 MB. È possibile utilizzare file più grandi o un numero elevato di immagini, ma questo aumenta il tempo di elaborazione.

Se desideri selezionare un file caricato in precedenza, espandi l&#39;elenco **[!UICONTROL Contenuto di riferimento caricato]** e abilita la risorsa da utilizzare per la generazione dei contenuti.

![Abilita il contenuto di riferimento esistente da utilizzare](./assets/gen-ai-reference-content-select.png){width="350" zoomable="yes"}

## Utilizzare gli strumenti di intelligenza artificiale generativi {#gen-ai-tools}

Per iniziare a generare il contenuto, apri l’editor di contenuti per la pagina di destinazione e accedi agli strumenti di intelligenza artificiale generativi nella barra esterna del pannello di destra. Selezionare _Assistente AI_ ( ![Assistente AI per la selezione del contenuto](../../assets/do-not-localize/icon-gen-ai-content.svg){width="25" zoomable="no"} ) per visualizzare gli strumenti di generazione del contenuto disponibili per la selezione del contenuto corrente.

Utilizza i passaggi seguenti in base al tipo di generazione del contenuto della pagina di destinazione che desideri utilizzare:

>[!BEGINTABS]

>[!TAB Pagina intera]

Segui questi passaggi per utilizzare l’Assistente AI per la generazione di pagine di destinazione complete, perfezionando un modello di pagina di destinazione esistente:

1. Dopo [aver creato la pagina di destinazione](./landing-pages.md#create-a-landing-page), fai clic su **[!UICONTROL Modifica pagina di destinazione]**.

1. Seleziona un modello.

   La generazione completa dei contenuti richiede un modello. Può essere un modello standard fornito da Adobe o un modello salvato. È inoltre possibile utilizzare l&#39;opzione _[!UICONTROL Importa HTML]_ per importare un modello.

   Per ulteriori informazioni sull&#39;utilizzo di un modello di pagina di destinazione, vedere _[Selezionare un modello salvato o di esempio](./landing-pages.md#select-a-saved-or-sample-template)_.

1. Nella barra esterna del pannello di destra, seleziona l&#39;icona _Assistente AI_ ( ![Assistente AI per attivazione/disattivazione contenuti](../../assets/do-not-localize/icon-gen-ai-content.svg){width="25" zoomable="no"} ).

   ![Attivazione/disattivazione dell&#39;Assistente IA nello spazio di progettazione della pagina di destinazione](./assets/gen-ai-full-landing-page-ai-panel.png){width="600" zoomable="yes"}

   Le impostazioni dell’Assistente AI a destra riflettono le impostazioni di generazione per l’intera pagina di destinazione.

1. (Beta) Seleziona il tuo **[!UICONTROL marchio]** per assicurarti che il contenuto generato dall&#39;intelligenza artificiale sia in linea con le specifiche del tuo marchio.

   Se non sono presenti marchi pubblicati, fai clic su **[!UICONTROL Crea un marchio]** per definire le [linee guida per i marchi riutilizzabili](./brands-overview.md).

1. Nel campo **[!UICONTROL Prompt]** immettere una descrizione di ciò che si desidera generare.

   Utilizza la [Libreria prompt](#prompt-library) per ottenere informazioni utili sulla creazione di un prompt valido.

   ![Assistente AI - Libreria prompt per la generazione del contenuto della pagina di destinazione](./assets/email-designer-ai-assistant-full.png){width="600" zoomable="yes"}

   >[!TIP]
   >
   >Se non hai ancora richiesto il contenuto generato, consulta le _[Best practice per la richiesta](../ai-assistant/generative-ai-content.md#generative-ai-prompting-guide)_.

1. Completa le impostazioni della guida ai contenuti per adattare il contenuto generato:

   * [**[!UICONTROL Impostazioni testo]**](#text-settings) - Fornire indicazioni per il contenuto di testo generato.
   * [**[!UICONTROL Impostazioni immagine]**](#image-settings) - Se desideri includere le immagini nel contenuto generato, abilita la generazione delle immagini e fornisci indicazioni.
   * [**[!UICONTROL Contenuto di riferimento]**](#reference-content) - Fornisci la risorsa di contenuto che funge da origine per la generazione di contenuti.

1. Quando la richiesta e le impostazioni sono pronte, fare clic su **[!UICONTROL Genera]**.

1. Scorri verso il basso nel pannello Assistente AI e sfoglia le varianti generate per determinare quale sia la più adatta.

   * Fai clic sull&#39;icona _Schermo intero_ ( ![Icona Schermo intero](../assets/do-not-localize/icon-full-screen.svg) ) per aprire la finestra di dialogo _[!UICONTROL Genera pagina di destinazione]_

   * Se necessario, utilizza le [azioni di ottimizzazione](#refine-a-variation) per ottimizzare la variante in modo che soddisfi esattamente i tuoi requisiti.

   * [Invia feedback](#submit-variation-feedback) per le varianti generate facendo clic sull&#39;icona _Pollice in alto_, _Pollice in basso_ o _Contrassegna_ e scegliendo il motivo che riepiloga meglio il feedback.

1. Fai clic su **[!UICONTROL Seleziona]** per sostituire il contenuto del modello con la variante selezionata e tornare allo spazio di progettazione della pagina di destinazione.

   Puoi utilizzare gli strumenti di modifica e formattazione nell&#39;area di lavoro per modificare il contenuto generato, nonché le opzioni _[!UICONTROL Impostazioni]_ e _[!UICONTROL Stile]_ a destra.

>[!TAB Solo testo]

Per utilizzare l’Assistente AI per perfezionare o migliorare il contenuto del testo di una pagina di destinazione esistente, effettua le seguenti operazioni:

1. Nello spazio di progettazione della pagina di destinazione, seleziona un componente _Testo_ per eseguire il targeting del contenuto specifico.

1. Nella barra esterna del pannello di destra, seleziona l&#39;icona _Assistente AI_ ( ![Assistente AI per attivazione/disattivazione contenuti](../../assets/do-not-localize/icon-gen-ai-content.svg){width="25" zoomable="no"} ).

   ![Attivazione/disattivazione dell&#39;Assistente IA nello spazio di progettazione della pagina di destinazione](./assets/email-designer-ai-assistant-button.png){width="600" zoomable="yes"}

   Le impostazioni a destra riflettono le impostazioni di generazione del contenuto per il componente testo.

1. (Beta) Seleziona il tuo **[!UICONTROL marchio]** per assicurarti che il contenuto generato dall&#39;intelligenza artificiale sia in linea con le specifiche del tuo marchio.

   Se non sono presenti marchi pubblicati, fai clic su **[!UICONTROL Crea un marchio]** per [definire le linee guida per i marchi riutilizzabili](./brands-overview.md).

1. Nel campo **[!UICONTROL Prompt]** immettere una descrizione di ciò che si desidera generare.

   ![Assistente AI - Impostazioni testo](./assets/email-designer-ai-assistant-text.png){width="600" zoomable="yes"}

   Utilizza la [Libreria prompt](#prompt-library) per ottenere informazioni utili sulla creazione di un prompt valido.

1. Completa le impostazioni della guida ai contenuti per adattare il contenuto generato:

   * [**[!UICONTROL Impostazioni testo]**](#text-settings) - Fornire indicazioni per il contenuto di testo generato.

   * [**[!UICONTROL Contenuto di riferimento]**](#reference-content) - Fornisci le risorse di contenuto che fungono da origine per la generazione del contenuto.

1. Quando la richiesta e le impostazioni sono pronte, fare clic su **[!UICONTROL Genera]**.

1. Scorri verso il basso nel pannello Assistente AI e sfoglia le varianti generate per determinare quale sia la più adatta.

   * Fai clic sull&#39;icona _Schermo intero_ ( ![Icona Schermo intero](../assets/do-not-localize/icon-full-screen.svg) ) per aprire la finestra di dialogo _[!UICONTROL Genera testo]_

   * Se necessario, utilizza le [azioni di ottimizzazione](#refine-a-variation) per ottimizzare la variante in modo che soddisfi esattamente i tuoi requisiti.

   * [Invia feedback](#submit-variation-feedback) per le varianti generate facendo clic sull&#39;icona _Pollice in alto_, _Pollice in basso_ o _Contrassegna_ e scegliendo il motivo che riepiloga meglio il feedback.

1. Quando hai il contenuto desiderato, fai clic su **[!UICONTROL Seleziona]** per sostituire il testo con la variante selezionata e tornare allo spazio di progettazione della pagina di destinazione.

   Puoi utilizzare gli strumenti di modifica e formattazione nell&#39;area di lavoro per modificare il testo, nonché le opzioni _[!UICONTROL Impostazioni]_ e _[!UICONTROL Stile]_ a destra.

>[!TAB Solo immagine]

Per utilizzare l’Assistente AI per perfezionare o migliorare il contenuto dell’immagine per una pagina di destinazione esistente, effettua le seguenti operazioni:

1. Nello spazio di progettazione della pagina di destinazione, seleziona un componente _Immagine_ per eseguire il targeting del contenuto specifico.

1. Nella barra esterna del pannello di destra, seleziona l&#39;icona _Assistente AI_ ( ![Assistente AI per attivazione/disattivazione contenuti](../../assets/do-not-localize/icon-gen-ai-content.svg){width="25" zoomable="no"} ).

   ![Attivazione/disattivazione dell&#39;Assistente IA nello spazio di progettazione della pagina di destinazione](./assets/email-designer-ai-assistant-button.png){width="600" zoomable="yes"}

   Le impostazioni dell’Assistente AI a destra riflettono le impostazioni di generazione del componente immagine.

1. (Beta) Seleziona il tuo **[!UICONTROL marchio]** per assicurarti che il contenuto generato dall&#39;intelligenza artificiale sia in linea con le specifiche del tuo marchio.

   Se non sono presenti marchi pubblicati, fai clic su **[!UICONTROL Crea un marchio]** per [definire le linee guida per i marchi riutilizzabili](./brands-overview.md).

1. Immettere una descrizione nel campo **[!UICONTROL Prompt]**.

   ![Assistente AI - Impostazioni testo](./assets/email-designer-ai-assistant-image.png){width="600" zoomable="yes"}

   Utilizza la [Libreria prompt](#prompt-library) per ottenere informazioni utili sulla creazione di un prompt valido.

1. Completa le impostazioni della guida ai contenuti per adattare il contenuto generato:

   * [**[!UICONTROL Impostazioni immagine]**](#image-settings) - Se desideri includere le immagini nel contenuto generato, abilita la generazione delle immagini e fornisci indicazioni.

   * [**[!UICONTROL Contenuto di riferimento]**](#reference-content) - Fornisci le risorse di contenuto che fungono da origine per la generazione del contenuto.

1. Quando si è soddisfatti della richiesta e delle impostazioni, fare clic su **[!UICONTROL Genera]**.

   L’Assistente AI elabora la richiesta e genera le immagini più adatte in base al prompt e ad altri input.

   >[!IMPORTANT]
   >
   >Se nel contenuto di riferimento non sono presenti immagini o non sono presenti immagini rilevanti per il prompt di input, l&#39;output è vuoto.

1. Sfoglia le varianti generate o fai clic sull&#39;icona _Schermo intero_ ( ![Icona Schermo intero](../assets/do-not-localize/icon-full-screen.svg) ) per aprire la finestra di dialogo _[!UICONTROL Genera immagine]_.

   La finestra di dialogo fornisce spazio aggiuntivo per confrontare le varianti, regolare le impostazioni dell’immagine e del contenuto di riferimento (se necessario) e rigenerare le varianti.

   Puoi selezionare una variante e fare clic su **[!UICONTROL Genera simile]** per generare altre immagini simili alla variante selezionata. Oppure fai clic su **[!UICONTROL Modifica in Adobe Express]** per apportare modifiche all&#39;immagine. Consulta [Azioni rapide in Adobe Express](./image-edit-adobe-express.md#quick-actions-in-adobe-express) per ulteriori informazioni sull&#39;utilizzo di Adobe Express per perfezionare le immagini.

   ![Anteprima dell&#39;Assistente di IA per le opzioni di modifica e perfezionamento del testo](./assets/email-designer-ai-assistant-image-refine.png){width="700" zoomable="yes"}

   Puoi anche [inviare feedback](#submit-variation-feedback) per le varianti generate.

1. Evidenzia l&#39;immagine desiderata e fai clic su **[!UICONTROL Seleziona]** per sostituire l&#39;immagine o il segnaposto con l&#39;elemento selezionato e tornare allo spazio di progettazione della pagina di destinazione.

   Puoi utilizzare gli strumenti di modifica e formattazione nell&#39;area di lavoro per modificare l&#39;immagine, nonché le opzioni _[!UICONTROL Impostazioni]_ e _[!UICONTROL Stile]_ a destra.

>[!ENDTABS]

## Anteprima e ottimizzazione dei contenuti {#refine-finalize}

Dopo aver generato le varianti di contenuto, puoi perfezionare i risultati per garantire che soddisfino esattamente i tuoi requisiti. Rivedi l’allineamento del brand, regola il tono e la lingua e prepara il contenuto per una bozza revisionabile. Puoi anche inviare feedback per una variante per aiutare ad addestrare l’Assistente AI e migliorare l’output futuro.

### Apri la visualizzazione a schermo intero

1. Dopo la generazione iniziale del contenuto, sfoglia le **[!UICONTROL Varianti]**.

1. Identifica la variante più adatta ai tuoi obiettivi e fai clic sull&#39;icona _Schermo intero_ ( ![Icona Schermo intero](../assets/do-not-localize/icon-full-screen.svg) ) per aprire la finestra di dialogo.

   ![Accedi alla finestra di dialogo Genera](./assets/gen-ai-preview-text-refine.png){width="700" zoomable="yes"}

1. Quando sei soddisfatto della variante selezionata, fai clic su **[!UICONTROL Seleziona]** per applicarla all&#39;area di lavoro.

### Perfezionare una variante

Fai clic sull&#39;opzione **[!UICONTROL Perfeziona]** per accedere a funzioni di personalizzazione aggiuntive per le varianti di testo e pagina di destinazione:

* **[!UICONTROL Elaborare]** - L&#39;Assistente all&#39;intelligenza artificiale può aiutarti a espandere argomenti specifici, fornendo ulteriori dettagli per una migliore comprensione e coinvolgimento.

* **[!UICONTROL Riepiloga]** - Le informazioni lunghe possono sovraccaricare i visualizzatori di pagina. Utilizza l’Assistente AI per condensare i punti chiave in riepiloghi chiari e concisi che catturano l’attenzione e li incoraggiano a leggere ulteriormente.

* **[!UICONTROL Riformula]** - Riscrivi il messaggio conservandone il significato. Questa opzione consente di generare una formulazione alternativa, migliorare il flusso o regolare la formulazione senza modificare il messaggio principale.

* **[!UICONTROL Usa un linguaggio più semplice]**: semplifica la lingua, garantendo chiarezza e accessibilità a un pubblico più ampio.

* **[!UICONTROL Traduci]** - Traduci il testo in un&#39;altra lingua. Attualmente, l’inglese è l’unica lingua supportata.

* **[!UICONTROL Cambia tono]** - Regola il tono del messaggio in base allo stile di comunicazione, ad esempio rendendolo più amichevole, professionale, urgente o stimolante.

* **[!UICONTROL Modifica strategia di comunicazione]** - Modifica l&#39;approccio di messaggistica in base agli obiettivi, ad esempio la creazione di messaggi urgenti o l&#39;enfasi sull&#39;aspetto interessante.

<!-- * **[!UICONTROL Use as reference content]** - Select this option to use the variant as the reference content for generating other results. -->

![Perfeziona il menu visualizzando le opzioni per l&#39;ottimizzazione del contenuto](./assets/gen-ai-preview-text-refine.png){width="700" zoomable="yes"}

### Invia feedback variante

Fornisci un feedback per le varianti generate facendo clic sull&#39;icona _Miniature in alto_, _Miniature in basso_ o _Contrassegna_ e scegli il motivo per il quale riepiloga meglio il feedback.

![Assistente AI - visualizza in anteprima le varianti generate](./assets/gen-ai-preview-feedback-thumbs-up.png){width="700" zoomable="yes"}

### Verifica l’allineamento del brand (Beta)

<!-- Are we surfacing scoring here in the future, or will it be a separate post-creation task? 1. Click the percentage icon to view your **[!UICONTROL Brand Alignment Score]** and identify any misalignments with your brand. -->

La valutazione e il punteggio dell’allineamento del brand ti aiutano a garantire coerenza in termini di tono, messaggi e identità visiva nelle campagne, fungendo anche da controllo di qualità prima che il contenuto venga pubblicato. Una volta completato il contenuto della pagina di destinazione, fai clic sull&#39;icona _Allineamento marchio_ ( ![Icona Allineamento marchio](../assets/do-not-localize/icon-brand-compliance.svg) ) a destra per aprire il pannello destro _Allineamento marchio_ nell&#39;area di progettazione della pagina di destinazione.

![Accedere agli strumenti di allineamento del marchio](./assets/brands-alignment-sidebar.png){width="600" zoomable="yes"}

Per informazioni dettagliate, consulta [Convalidare l&#39;allineamento del brand](./brand-alignment.md#validate-your-brand-alignment)
