---
title: Assistente AI per il contenuto delle e-mail
description: 'Genera contenuti e-mail con l''Assistente AI: crea contenuto del messaggio, righe dell''oggetto e intestazioni anticipate con le risorse del marchio e il targeting del ruolo del gruppo di acquisto in [!DNL Journey Optimizer B2B Edition].'
feature: AI Assistant, Generative AI, Email Authoring
role: User
exl-id: b66d72e4-3afc-49ad-9bc2-bedc047ecca4
source-git-commit: c7c08dc1d9b041bfc83cf8b5766a953fa765f4c9
workflow-type: tm+mt
source-wordcount: '3591'
ht-degree: 0%

---

# Assistente AI per contenuti e-mail

Con l&#39;aumento della competitività del settore Marketing, i marchi sono alla ricerca di metodi efficienti per generare contenuti di forte impatto in modo rapido ed efficiente. L&#39;Assistente all&#39;intelligenza artificiale per l&#39;authoring delle e-mail in [!DNL Adobe Journey Optimizer B2B Edition] è la funzionalità di generazione di contenuti basata sull&#39;intelligenza artificiale di Adobe che rivoluziona il modo in cui gli esperti di marketing creano contenuti e-mail professionali e coerenti con il brand. Con modelli di intelligenza artificiale generativi avanzati e una profonda comprensione delle linee guida del brand, AI Assistant genera automaticamente contenuti personalizzati, coinvolgenti ed efficaci. Utilizza il tuo obiettivo di marketing e ottimizza i contenuti per stili, layout, toni e altro ancora. Ai Assistant rende la creazione e l’esecuzione di campagne di e-mail marketing intuitiva, semplice e senza problemi. L’aggiunta di questa funzionalità ai flussi di lavoro consente di risparmiare tempo, migliorare l’efficienza e ottenere risultati migliori.

Questa nuova funzionalità fornisce una generazione di contenuti basata su messaggi immediati per la generazione completa di e-mail o mirata all’interno dei componenti strutturali e-mail. Per le immagini, puoi generare nuove risorse immagine o semplicemente generare consigli dall’interno del catalogo delle immagini nella risorsa del marchio di input. Puoi anche utilizzare questa funzionalità per generare linee dell’oggetto e intestazioni preliminari ottimali in modo da influire sul tasso di apertura delle e-mail.

>[!IMPORTANT]
>
>Per accedere a queste funzionalità in Adobe Journey Optimizer B2B edition, è necessario disporre dell&#39;autorizzazione _[!UICONTROL Assistente AI]_ > _[!UICONTROL Genera contenuto]_. Per ulteriori informazioni su come un amministratore di prodotto può concedere le autorizzazioni per le funzionalità, vedere [Modifica ruoli per le autorizzazioni per il prodotto](../admin/user-management.md#edit-roles-for-product-permissions).

## Linee guida e limitazioni

Prima di iniziare a utilizzare questa funzionalità, rivedi le [linee guida e limitazioni](../ai-assistant/generative-ai-content.md#general-guidelines-and-limitations). [Per poter utilizzare le funzionalità di intelligenza artificiale in [!DNL Journey Optimizer B2B Edition] è inoltre necessario accettare l&#39;accordo utente](https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html){target="_blank"}. Per ulteriori informazioni, contatta il tuo rappresentante Adobe.

Con l&#39;impegno di Adobe di promuovere la trasparenza nell&#39;utilizzo degli strumenti di intelligenza artificiale generativi nella creazione di contenuti multimediali, Adobe applica [credenziali di contenuto](https://helpx.adobe.com/it/firefly/web/get-started/learn-the-basics/content-credentials-overview.html){target="_blank"} a qualsiasi contenuto o progetto che include una risorsa generata da Firefly al momento del download o dell&#39;esportazione.

Le limitazioni e le linee guida seguenti si applicano alle funzioni dell&#39;Assistente IA utilizzate per la generazione di contenuti e-mail in [!DNL Journey Optimizer B2B Edition]:

* L’inglese è l’unica lingua supportata.
* I contenuti generati potrebbero non essere accurati: condividi il tuo feedback in modo che i tecnici Adobe possano perfezionare i modelli.
* Puoi caricare più risorse di riferimento di contenuto, ma puoi sfruttarne una sola per una generazione specifica.
* Utilizza un modello personalizzato o specifico per il brand per generare contenuti per un’e-mail completa. Si consigliano modelli e-mail con un massimo di 8-10 immagini.
* Assicurati di segnalare eventuali output problematici utilizzando le icone thumb up, thumb down o flag quando selezioni le varianti generate.

## Input e impostazioni per la generazione di contenuti

Puoi generare contenuto completo per un messaggio e-mail o per i componenti selezionati nell’e-mail. Quando si utilizzano gli strumenti di Assistente AI per generare il contenuto necessario, è possibile fornire l’input, inclusi i prompt e il contenuto di riferimento, e le impostazioni per il testo e le immagini.

### Prompt

Utilizza prompt ben definiti per il modello di intelligenza artificiale generativo per interpretare con precisione. L’obiettivo/richiesta di marketing che fornisci influisce notevolmente sulla qualità del contenuto generato.

![Campo richiesta](./assets/gen-ai-prompt.png){width="320"}

Per ulteriori informazioni sulla creazione di prompt effettivi, vedere _[Best practice per i prompt](../ai-assistant/generative-ai-content.md#generative-ai-prompting-guide)_.

>[!BEGINSHADEBOX]

#### Libreria dei prompt

Un prompt efficace è essenziale per generare i contenuti migliori possibili. Se desideri assistenza per la creazione del prompt, fai clic sull&#39;icona _Libreria prompt_ ![Icona Libreria prompt](../assets/do-not-localize/icon-library.svg) per accedere a una libreria di idee prompt organizzate in base agli obiettivi. Immettere il testo nel campo di ricerca per trovare un prompt basato su una stringa di parole chiave.

![Assistente AI - Accesso alla libreria dei prompt](./assets/gen-ai-prompt-library.png){width="600" zoomable="no"}

Selezionare il prompt che meglio riflette gli obiettivi desiderati e fare clic su **[!UICONTROL Prova questo prompt]**. Nel campo _[!UICONTROL Chiedi conferma]_, sostituisci eventuali segnaposto (ad esempio `[Key Feature/Information]`) con i valori necessari che specificano il tuo marchio, la tua offerta, la tua campagna e i tuoi casi d&#39;uso.

>[!ENDSHADEBOX]

### Impostazioni testo

Espandi le **[!UICONTROL Impostazioni testo]** nel pannello di destra e imposta le opzioni per il testo generato.

* **[!UICONTROL Gruppo di acquisto]** - Scegli il [ruolo gruppo di acquisto](../buying-groups/buying-groups-role-templates.md) da utilizzare per il targeting dei messaggi. [!DNL Journey Optimizer B2B Edition] offre cinque ruoli standard di gruppo di acquisto B2B pronti all’uso. Ogni ruolo del gruppo di acquisto ha un oggetto di messaggistica distinto:

  | Ruolo | Stato attivo messaggistica |
  | ---- | --------------- |
  | Comitato esecutivo direttivo | Informazioni sul prodotto <br/>Prezzi <br/>Dettagli sull&#39;integrazione tecnica <br/>Caratteristiche e funzioni del prodotto |
  | Influencer | Prova di qualità <br/>Facilità di implementazione <br/>Competenze in materia <br/>Vantaggi competitivi |
  | Responsabile delle decisioni | Ritorno sull&#39;investimento <br/>Valore finanziario (RoI) <br/>Storie dei clienti |
  | Professionista | Facilità di utilizzo <br/>Funzionalità e funzionalità del prodotto <br/>Compatibilità del prodotto <br/>Facilità di integrazione del prodotto |
  | Campione | Contenuto educativo <br/>Contenuto leadership di pensiero <br/>Storie dei clienti |

* **[!UICONTROL Fase percorso marketing]** - Scegli la [fase gruppo acquisti](../buying-groups/buying-group-stages.md) da utilizzare per il targeting dei messaggi.
* **[!UICONTROL Strategia di comunicazione]** - Scegli lo stile di comunicazione più adatto al testo generato.
* **[!UICONTROL Lingua]** - Scegli la lingua del contenuto generato.
* **[!UICONTROL Tono]** - Il tono dovrebbe risuonare con il tuo pubblico. Ad esempio, puoi impostare il messaggio in modo che abbia un suono informativo, giocoso o persuasivo.

![Pannello Impostazioni testo che mostra le opzioni relative al gruppo di acquisto, alla fase del percorso marketing, alla strategia di comunicazione, alla lingua e al tono](./assets/gen-ai-text-settings.png){width="350" zoomable="yes"}

Fare clic sulla freccia sinistra per tornare alle _[!UICONTROL Impostazioni]_ principali.

### Impostazioni immagine

Per includere le immagini nel contenuto generato, espandi le **[!UICONTROL Impostazioni immagine]** nel pannello di destra e imposta le opzioni.

Per impostazione predefinita, l&#39;opzione **[!UICONTROL Generate images using AI]** è disabilitata. Abilita questa funzione e imposta le seguenti opzioni per includere le immagini generate nelle varianti di contenuto proposte:

<!-- * **[!UICONTROL Generative model]**: Select from available built-in models, custom Firefly models trained on your brand assets, or third-party image generation providers to create images that align with your specific needs and brand requirements. -->
* **[!UICONTROL Proporzioni]**: quando è selezionato un componente immagine, questa impostazione determina la larghezza e l&#39;altezza della risorsa. È possibile scegliere tra rapporti comuni quali 16:9, 4:3, 3:2 o 1:1 oppure immettere una dimensione personalizzata.
* **[!UICONTROL Tipo di contenuto]**: il tipo categorizza la natura dell&#39;elemento visivo, distinguendo tra diverse forme di rappresentazione visiva, come foto, grafica o grafica.
* **[!UICONTROL Intensità visiva]**: controlla l&#39;impatto dell&#39;immagine regolandone l&#39;intensità. Un&#39;impostazione più bassa (ad esempio 2) crea un aspetto più morbido e più contenuto, mentre un&#39;impostazione più alta (ad esempio 10) rende l&#39;immagine più vibrante e visivamente potente.
* **[!UICONTROL Colore e tono]**: l&#39;aspetto complessivo dei colori all&#39;interno di un&#39;immagine e l&#39;umore o l&#39;atmosfera che trasmette.
* **[!UICONTROL Illuminazione]**: lo stile di illuminazione utilizzato per l&#39;immagine, che ne forma l&#39;atmosfera ed evidenzia elementi specifici.
* **[!UICONTROL Composizione]**: disposizione degli elementi all&#39;interno della cornice di un&#39;immagine.

![Pannello impostazioni immagine che visualizza le opzioni Tipo di contenuto, Intensità visiva, Colore e tono, Illuminazione e Composizione](./assets/gen-ai-image-settings.png){width="350" zoomable="yes"}

Fare clic sulla freccia sinistra per tornare alle _[!UICONTROL Impostazioni]_ principali.

### Contenuto di riferimento

Carica le risorse di contenuto di riferimento per generare contenuti precisi per il brand. In caso contrario, il contenuto generato si basa su informazioni disponibili pubblicamente. Il contenuto di riferimento funge da origine per la generazione di contenuti e per i consigli sulle immagini. Per le linee guida e le best practice, consulta _[Contenuto di riferimento ottimizzato](../ai-assistant/generative-ai-content.md#reference-content)_.

Dalle impostazioni del **[!UICONTROL contenuto di riferimento]**, fare clic su **[!UICONTROL Carica file]** per aggiungere qualsiasi risorsa contenente contenuto da utilizzare per il contesto aggiuntivo.

![Carica il file da utilizzare per il contenuto di riferimento](./assets/gen-ai-reference-content-upload.png){width="350" zoomable="yes"}

Il file da caricare può essere nei seguenti formati: PDF, JPEG, PNG o file ZIP (contenenti i formati di file supportati). La dimensione massima per una risorsa marchio caricata è di 50 MB. È possibile utilizzare file più grandi o un numero elevato di immagini, ma questo aumenta il tempo di elaborazione.

Se desideri selezionare un file caricato in precedenza, espandi l&#39;elenco **[!UICONTROL Contenuto di riferimento caricato]** e abilita la risorsa da utilizzare per la generazione dei contenuti.

![Abilita il contenuto di riferimento esistente da utilizzare](./assets/gen-ai-reference-content-select.png){width="350" zoomable="yes"}

## Generare proprietà e-mail con l’Assistente IA

Quando [aggiungi un&#39;azione e-mail](./add-email.md#add-an-email-action-node-in-a-journey) a un percorso di account, definisci un set di proprietà e-mail utilizzate per inviare l&#39;e-mail. L&#39;Assistente AI può contribuire a migliorare il coinvolgimento e-mail generando il contenuto consigliato per l&#39;e-mail **_riga oggetto_** e **_preheader_**.

Quando crei un messaggio e-mail da un percorso o apri un messaggio e-mail esistente da un nodo del percorso, la pagina di anteprima e-mail viene visualizzata con le _[!UICONTROL proprietà e-mail]_ a destra. Nella scheda _[!UICONTROL Riepilogo]_ è possibile utilizzare gli strumenti di generazione dei contenuti dell&#39;Assistente IA per generare un oggetto, un preheader o entrambi.

>[!BEGINTABS]

>[!TAB Generazione riga oggetto]

I passaggi seguenti descrivono la sequenza di attività per l’utilizzo dell’Assistente AI per generare una riga dell’oggetto ottimizzata per l’e-mail:

1. Nel pannello _Riepilogo_ con la scheda _Dettagli_ selezionata, scorri verso il basso fino al campo **[!UICONTROL Oggetto]**.

1. Fare clic sull&#39;icona Assistente IA ( ![Icona di accesso Assistente IA](../../assets/do-not-localize/icon-gen-ai-email-properties.svg){width="30"} ) a destra del campo.

   ![Accesso all&#39;Assistente AI per la riga dell&#39;oggetto dell&#39;e-mail](./assets/email-properties-ai-assistant-subject-line-icon.png){width="600" zoomable="yes"}

   Viene visualizzata la finestra di dialogo _[!UICONTROL Genera riga oggetto]_ con le impostazioni di generazione per la riga dell&#39;oggetto dell&#39;e-mail.

1. (Obbligatorio) Nel campo **[!UICONTROL Prompt]**, inserisci una descrizione di ciò che desideri generare.

   Utilizza la [Libreria prompt](#prompt-library) per ottenere informazioni utili sulla creazione di un prompt valido.

1. (Facoltativo) Completa le impostazioni della guida al contenuto per fornire un input aggiuntivo per la generazione della preintestazione:

   * [**[!UICONTROL Impostazioni testo]**](#text-settings) - Fornire indicazioni per il contenuto di testo generato.
   * [**[!UICONTROL Contenuto di riferimento]**](#reference-content) - Fornisci la risorsa di contenuto che funge da origine per la generazione di contenuti.

1. Quando la richiesta e le impostazioni sono pronte, fare clic su **[!UICONTROL Genera]**.

   Le varianti generate vengono visualizzate nella finestra di dialogo.

   ![Assistente IA - varianti generate dalla riga dell&#39;oggetto dell&#39;e-mail](./assets/email-properties-ai-assistant-subject-line.png){width="600" zoomable="yes"}

1. Scorri il pannello Assistente AI e sfoglia le varianti generate per determinare quale sia la più adatta.

   Puoi [inviare un feedback](#submit-variation-feedback) per una variante generata facendo clic sull&#39;icona _Miniature in alto_, _Miniature in basso_ o _Contrassegna_ e scegliere il motivo che riepiloga meglio il tuo feedback.

1. Fai clic sull&#39;opzione **[!UICONTROL Perfeziona]** per accedere ad altre funzioni di personalizzazione:

   * **[!UICONTROL Riformula]** - Riscrivi il messaggio conservandone il significato. Questa opzione consente di generare una formulazione alternativa o di regolare la formulazione senza modificare il messaggio principale.

   * **[!UICONTROL Usa un linguaggio più semplice]**: semplifica la lingua, garantendo chiarezza e accessibilità a un pubblico più ampio.

   * **[!UICONTROL Traduci]** - Traduci il testo in un&#39;altra lingua. Attualmente, l’inglese è l’unica lingua supportata. Altre lingue sono pianificate per le versioni future.)

   * **[!UICONTROL Cambia tono]** - Regola il tono del messaggio in base allo stile di comunicazione, ad esempio rendendolo più amichevole, professionale, urgente o stimolante.

   * **[!UICONTROL Modifica strategia di comunicazione]** - Modifica l&#39;approccio di messaggistica in base agli obiettivi, ad esempio la creazione di messaggi urgenti o l&#39;enfasi sull&#39;aspetto interessante.

   ![Assistente IA - perfezionamento riga oggetto](./assets/email-properties-ai-assistant-subject-line-refine.png){width="600" zoomable="yes"}

1. Fai clic su **[!UICONTROL Seleziona]** per sostituire il testo dell&#39;oggetto con la variante selezionata e tornare alle proprietà dell&#39;e-mail.

>[!TAB Generazione preheader]

Un preheader e-mail è il breve testo di riepilogo che segue la riga dell’oggetto quando un’e-mail viene visualizzata nella casella in entrata. Si tratta di un elemento facoltativo per un’e-mail, ma rappresenta una grande opportunità per migliorare il coinvolgimento. I passaggi seguenti descrivono la sequenza di attività per l’utilizzo dell’Assistente AI per generare un preheader ottimizzato per l’e-mail:

1. Nel pannello _Riepilogo_ con la scheda _Dettagli_ selezionata, scorri verso il basso e seleziona la casella di controllo **[!UICONTROL Preheader]**.

   ![Accesso all&#39;Assistente AI per il preheader e-mail](./assets/email-properties-ai-assistant-preheader-icon.png){width="600" zoomable="yes"}

   Viene visualizzata la finestra di dialogo _[!UICONTROL Genera preintestazione]_ con le impostazioni di generazione per la preintestazione e-mail.

1. (Obbligatorio) Nel campo **[!UICONTROL Prompt]**, inserisci una descrizione di ciò che desideri generare.

   Utilizza la [Libreria prompt](#prompt-library) per ottenere informazioni utili sulla creazione di un prompt valido.

1. (Facoltativo) Completa le impostazioni della guida al contenuto per fornire un input aggiuntivo per la generazione della preintestazione:

   * [**[!UICONTROL Impostazioni testo]**](#text-settings) - Fornire indicazioni per il contenuto di testo generato.
   * [**[!UICONTROL Contenuto di riferimento]**](#reference-content) - Fornisci la risorsa di contenuto che funge da origine per la generazione di contenuti.

1. Quando la richiesta e le impostazioni sono pronte, fare clic su **[!UICONTROL Genera]**.

   Le varianti generate vengono visualizzate nella finestra di dialogo.

   ![Assistente IA - varianti generate dal preheader e-mail](./assets/email-properties-ai-assistant-preheader.png){width="600" zoomable="yes"}

1. Scorri il pannello Assistente AI e sfoglia le varianti generate per determinare quale sia la più adatta.

   Puoi [inviare un feedback](#submit-variation-feedback) per una variante generata facendo clic sull&#39;icona _Miniature in alto_, _Miniature in basso_ o _Contrassegna_ e scegliere il motivo che riepiloga meglio il tuo feedback.

1. Fai clic sull&#39;opzione **[!UICONTROL Perfeziona]** per accedere ad altre funzioni di personalizzazione:

   * **[!UICONTROL Riformula]** - Riscrivi il messaggio conservandone il significato. Questa opzione consente di generare una formulazione alternativa o di regolare la formulazione senza modificare il messaggio principale.

   * **[!UICONTROL Usa un linguaggio più semplice]**: semplifica la lingua, garantendo chiarezza e accessibilità a un pubblico più ampio.

   * **[!UICONTROL Traduci]** - Traduci il testo in un&#39;altra lingua. Attualmente, l’inglese è l’unica lingua supportata. Altre lingue sono pianificate per le versioni future.)

   * **[!UICONTROL Cambia tono]** - Regola il tono del messaggio in base allo stile di comunicazione, ad esempio rendendolo più amichevole, professionale, urgente o stimolante.

   * **[!UICONTROL Modifica strategia di comunicazione]** - Modifica l&#39;approccio di messaggistica in base agli obiettivi, ad esempio la creazione di messaggi urgenti o l&#39;enfasi sull&#39;aspetto interessante.

   ![Assistente IA - ottimizzazione preheader](./assets/email-properties-ai-assistant-preheader-refine.png){width="500" zoomable="yes"}

1. Fai clic su **[!UICONTROL Seleziona]** per sostituire il preheader con la variante selezionata e tornare alle proprietà e-mail.

>[!ENDTABS]

## Generare contenuti del corpo dell’e-mail con l’Assistente AI {#generative-ai-email-design}

Dopo aver [creato e personalizzato l&#39;e-mail](./email-authoring.md), utilizza l&#39;Assistente di intelligenza artificiale in [!DNL Journey Optimizer B2B Edition], basato sull&#39;intelligenza artificiale generativa, per elevare il contenuto del corpo dell&#39;e-mail al livello successivo.

Nell’area di progettazione delle e-mail, l’Assistente AI può aiutarti a ottimizzare l’impatto delle consegne generando l’intero corpo dell’e-mail, il contenuto di testo mirato e le immagini che risuonano con il tuo pubblico. Questa ottimizzazione delle campagne e-mail è progettata per produrre un coinvolgimento migliore. Selezionare _Assistente AI_ ( ![Attivazione/disattivazione del menu Assistente AI](../../assets/do-not-localize/icon-gen-ai-content.svg){width="25" zoomable="no"} ) per visualizzare gli strumenti di generazione del contenuto disponibili per la selezione del contenuto corrente.

![Attivazione/disattivazione dell&#39;Assistente IA nella finestra di progettazione e-mail](./assets/email-designer-ai-assistant-button.png){width="600" zoomable="yes"}

Utilizza i seguenti passaggi in base al tipo di generazione di contenuti e-mail che desideri utilizzare:

>[!BEGINTABS]

>[!TAB Generazione e-mail completa]

Segui questi passaggi per utilizzare l’Assistente all’intelligenza artificiale per la generazione completa di e-mail perfezionando un modello e-mail esistente:

1. Dopo [aver creato l&#39;e-mail](./add-email.md), fai clic su **[!UICONTROL Modifica contenuto e-mail]**.

1. Seleziona un modello.

   La generazione completa dei contenuti richiede un modello. Può essere un modello standard fornito da Adobe o un modello salvato. È inoltre possibile utilizzare l&#39;opzione _[!UICONTROL Importa HTML]_ per importare un modello.

   Per ulteriori informazioni sull&#39;utilizzo di un modello di posta elettronica, vedere _[Selezionare un modello](./email-authoring.md#select-a-template)_.

1. Nell&#39;area di progettazione delle e-mail, accedi al menu Assistente AI facendo clic sull&#39;icona ( ![Attiva/Disattiva il menu Assistente AI](../../assets/do-not-localize/icon-gen-ai-content.svg){width="25"} ) a destra.

   Le impostazioni dell&#39;Assistente AI a destra riflettono _Genera e-mail_.

   ![Assistente AI - Libreria di prompt per la generazione di contenuti e-mail](./assets/email-designer-ai-assistant-full.png){width="600" zoomable="yes"}

1. Seleziona il tuo **[!UICONTROL Marchio]** per assicurarti che il contenuto generato dall&#39;intelligenza artificiale sia allineato alle specifiche del tuo marchio.

   Se non sono presenti marchi pubblicati, fai clic su **[!UICONTROL Crea un marchio]** per definire le [linee guida per i marchi riutilizzabili](./brands-overview.md).

1. Nel campo **[!UICONTROL Prompt]** immettere una descrizione di ciò che si desidera generare.

   Utilizza la [Libreria prompt](#prompt-library) per ottenere informazioni utili sulla creazione di un prompt valido.

   >[!TIP]
   >
   >Se non hai ancora richiesto il contenuto generato, consulta le _[Best practice per la richiesta](../ai-assistant/generative-ai-content.md#generative-ai-prompting-guide)_.

1. Completa le impostazioni della guida ai contenuti per adattare il contenuto generato:

   * [**[!UICONTROL Impostazioni testo]**](#text-settings) - Fornire indicazioni per il contenuto di testo generato.
   * [**[!UICONTROL Impostazioni immagine]**](#image-settings) - Se desideri includere le immagini nel contenuto generato, abilita la generazione delle immagini e fornisci indicazioni.
   * [**[!UICONTROL Contenuto di riferimento]**](#reference-content) - Fornisci la risorsa di contenuto che funge da origine per la generazione di contenuti.

1. Quando la richiesta e le impostazioni sono pronte, fare clic su **[!UICONTROL Genera]**.

   Le varianti generate vengono visualizzate nel pannello di destra.

1. Sfoglia le varianti generate o fai clic sull&#39;icona _Schermo intero_ ( ![Icona Schermo intero](../assets/do-not-localize/icon-full-screen.svg) ) per aprire la finestra di dialogo _[!UICONTROL Genera e-mail]_.

   La finestra di dialogo fornisce spazio aggiuntivo per confrontare le varianti, regolare le impostazioni del testo e del contenuto di riferimento (se necessario) e rigenerare le varianti.

   Puoi anche perfezionare una variante applicando azioni di ottimizzazione e inviare feedback per le varianti generate. Consulta _[Anteprima e ottimizzazione dei contenuti](#preview-and-content-refinement)_ per ulteriori dettagli sull&#39;ottimizzazione delle varianti e sul feedback.

   ![Anteprima dell&#39;Assistente IA delle opzioni di ottimizzazione e variazione delle e-mail](./assets/email-designer-ai-assistant-full-refine.png){width="700" zoomable="yes"}

1. Fai clic su **[!UICONTROL Seleziona]** per sostituire il contenuto del modello con la variante selezionata e tornare allo spazio di progettazione delle e-mail.

   Puoi utilizzare gli strumenti di modifica e formattazione nell&#39;area di lavoro per modificare il contenuto generato, nonché le opzioni _[!UICONTROL Impostazioni]_ e _[!UICONTROL Stile]_ a destra.

>[!TAB Solo testo]

Per utilizzare l’Assistente IA per perfezionare o migliorare il contenuto del testo di un’e-mail esistente, effettua le seguenti operazioni:

1. Nell&#39;area di progettazione delle e-mail, seleziona un componente _Testo_ per eseguire il targeting del contenuto specifico.

1. Nella barra esterna del pannello di destra, seleziona l&#39;icona _Assistente AI_ ( ![Attiva/Disattiva il menu Assistente AI](../../assets/do-not-localize/icon-gen-ai-content.svg){width="25"} ).

   Le impostazioni a destra riflettono le impostazioni di generazione del contenuto per il componente testo.

1. Seleziona il tuo **[!UICONTROL Marchio]** per assicurarti che il contenuto generato dall&#39;intelligenza artificiale sia allineato alle specifiche del tuo marchio.

   Se non sono presenti marchi pubblicati, fai clic su **[!UICONTROL Crea un marchio]** per [definire le linee guida per i marchi riutilizzabili](./brands-overview.md).

1. Nel campo **[!UICONTROL Prompt]** immettere una descrizione di ciò che si desidera generare.

   ![Assistente AI - Impostazioni testo](./assets/email-designer-ai-assistant-text.png){width="600" zoomable="yes"}

   Utilizza la [Libreria prompt](#prompt-library) per ottenere informazioni utili sulla creazione di un prompt valido.

1. Completa le impostazioni della guida ai contenuti per adattare il contenuto generato:

   * [**[!UICONTROL Impostazioni testo]**](#text-settings) - Fornire indicazioni per il contenuto di testo generato.

   * [**[!UICONTROL Contenuto di riferimento]**](#reference-content) - Fornisci le risorse di contenuto che fungono da origine per la generazione del contenuto.

1. Quando la richiesta e le impostazioni sono pronte, fare clic su **[!UICONTROL Genera]**.

1. Sfoglia le varianti generate o fai clic sull&#39;icona _Schermo intero_ ( ![Icona Schermo intero](../assets/do-not-localize/icon-full-screen.svg) ) per aprire la finestra di dialogo _[!UICONTROL Genera testo]_.

   La finestra di dialogo fornisce spazio aggiuntivo per confrontare le varianti, regolare le impostazioni del testo e del contenuto di riferimento (se necessario) e rigenerare le varianti.

   Puoi anche perfezionare una variante applicando azioni di ottimizzazione e inviare feedback per le varianti generate. Consulta _[Anteprima e ottimizzazione dei contenuti](#preview-and-refine-the-content)_ per ulteriori dettagli sull&#39;ottimizzazione delle varianti e sul feedback.

   ![Anteprima dell&#39;Assistente di IA per le opzioni di modifica e perfezionamento del testo](./assets/email-designer-ai-assistant-text-refine.png){width="700" zoomable="yes"}

1. Quando hai il contenuto desiderato, fai clic su **[!UICONTROL Seleziona]** per sostituire il testo con la variante selezionata e tornare allo spazio di progettazione delle e-mail.

   Puoi utilizzare gli strumenti di modifica e formattazione nell&#39;area di lavoro per modificare il testo, nonché le opzioni _[!UICONTROL Impostazioni]_ e _[!UICONTROL Stile]_ a destra.

>[!TAB Solo immagine]

Segui questi passaggi per utilizzare l’Assistente IA per perfezionare o migliorare il contenuto dell’immagine per un’e-mail esistente:

1. Nell&#39;area di progettazione delle e-mail, seleziona un componente _Immagine_ per eseguire il targeting del contenuto specifico.

1. Nella barra esterna del pannello di destra, seleziona l&#39;icona _Assistente AI_ ( ![Attiva/Disattiva il menu Assistente AI](../../assets/do-not-localize/icon-gen-ai-content.svg){width="25"} ).

   Le impostazioni dell’Assistente AI a destra riflettono le impostazioni di generazione del componente immagine.

1. Seleziona il tuo **[!UICONTROL Marchio]** per assicurarti che il contenuto generato dall&#39;intelligenza artificiale sia allineato alle specifiche del tuo marchio.

   Se non sono presenti marchi pubblicati, fai clic su **[!UICONTROL Crea un marchio]** per [definire le linee guida per i marchi riutilizzabili](./brands-overview.md).

1. Immettere una descrizione nel campo **[!UICONTROL Prompt]**.

   ![Assistente AI - immettere un prompt per il componente immagine](./assets/email-designer-ai-assistant-image.png){width="600" zoomable="yes"}

   Utilizza la [Libreria prompt](#prompt-library) per ottenere informazioni utili sulla creazione di un prompt valido.

1. Completa le impostazioni della guida ai contenuti per adattare il contenuto generato:

   * [**[!UICONTROL Impostazioni immagine]**](#image-settings) - Se desideri includere le immagini nel contenuto generato, abilita la generazione delle immagini e utilizza le impostazioni di guida.

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

1. Evidenzia l&#39;immagine desiderata e fai clic su **[!UICONTROL Seleziona]** per sostituire l&#39;immagine o il segnaposto con l&#39;elemento selezionato e tornare allo spazio di progettazione e-mail.

   Puoi utilizzare gli strumenti di modifica e formattazione nell&#39;area di lavoro per modificare l&#39;immagine, nonché le opzioni _[!UICONTROL Impostazioni]_ e _[!UICONTROL Stile]_ a destra.

>[!ENDTABS]

## Anteprima e perfezionamento del contenuto {#refine-finalize}

Dopo aver generato le varianti di contenuto, puoi perfezionare i risultati per garantire che soddisfino esattamente i tuoi requisiti. Rivedi l’allineamento del brand, regola il tono e la lingua e prepara il contenuto per una bozza revisionabile. Puoi anche inviare feedback per una variante per aiutare ad addestrare l’Assistente AI e migliorare l’output futuro.

### Apri la visualizzazione a schermo intero

1. Dopo la generazione iniziale del contenuto, sfoglia le **[!UICONTROL Varianti]**.

1. Identifica la variante più adatta ai tuoi obiettivi e fai clic sull&#39;icona _Schermo intero_ ( ![Icona Schermo intero](../assets/do-not-localize/icon-full-screen.svg) ) per visualizzare la variante selezionata in modo più approfondito.

   ![Accedi alla finestra di dialogo di anteprima](./assets/gen-ai-preview-text-refine.png){width="700" zoomable="yes"}

1. Quando sei soddisfatto della variante selezionata, fai clic su **[!UICONTROL Seleziona]** per applicarla all&#39;area di lavoro.

### Perfezionare una variante

Fai clic sull&#39;opzione **[!UICONTROL Perfeziona]** per accedere a funzioni di personalizzazione aggiuntive per le varianti di e-mail e testo:

* **[!UICONTROL Elaborare]** - L&#39;Assistente all&#39;intelligenza artificiale può aiutarti a espandere argomenti specifici, fornendo ulteriori dettagli per una migliore comprensione e coinvolgimento.

* **[!UICONTROL Riepiloga]** - Le informazioni lunghe possono sovraccaricare i visualizzatori di pagina. Utilizza l’Assistente AI per condensare i punti chiave in riepiloghi chiari e concisi che catturano l’attenzione e li incoraggiano a leggere ulteriormente.

* **[!UICONTROL Riformula]** - Riscrivi il messaggio conservandone il significato. Questa opzione consente di generare una formulazione alternativa, migliorare il flusso o regolare la formulazione senza modificare il messaggio principale.

* **[!UICONTROL Usa un linguaggio più semplice]**: semplifica la lingua, garantendo chiarezza e accessibilità a un pubblico più ampio.

* **[!UICONTROL Traduci]** - Traduci il testo in un&#39;altra lingua. Attualmente, l’inglese è l’unica lingua supportata. Altre lingue sono pianificate per le versioni future.)

* **[!UICONTROL Cambia tono]** - Regola il tono del messaggio in base allo stile di comunicazione, ad esempio rendendolo più amichevole, professionale, urgente o stimolante.

* **[!UICONTROL Modifica strategia di comunicazione]** - Modifica l&#39;approccio di messaggistica in base agli obiettivi, ad esempio la creazione di messaggi urgenti o l&#39;enfasi sull&#39;aspetto interessante.

<!-- is this option coming back? * **[!UICONTROL Use as reference content]** - Select this option to use the variant as the reference content for generating other results. -->

![Perfeziona il menu visualizzando le opzioni per l&#39;ottimizzazione del contenuto](./assets/gen-ai-preview-text-refine.png){width="700" zoomable="yes"}

### Invia feedback variante

Fornisci un feedback per le varianti generate facendo clic sull&#39;icona _Miniature in alto_, _Miniature in basso_ o _Contrassegna_ e scegli il motivo per il quale riepiloga meglio il feedback.

![Assistente AI - visualizza in anteprima le varianti generate](./assets/gen-ai-preview-feedback-thumbs-up.png){width="700" zoomable="yes"}

### Verifica l’allineamento del brand (Beta)

<!-- Are we surfacing scoring here in the future, or will it be a separate post-creation task? 1. Click the percentage icon to view your **[!UICONTROL Brand Alignment Score]** and identify any misalignments with your brand. -->

La valutazione e il punteggio di allineamento del brand ti aiutano a garantire coerenza in termini di tono, messaggi e identità visiva nelle campagne e-mail, fungendo anche da controllo di qualità prima che il contenuto venga pubblicato. Una volta completato il contenuto dell&#39;e-mail, fai clic sull&#39;icona _Allineamento marchio_ ( ![Icona Allineamento marchio](../assets/do-not-localize/icon-brand-compliance.svg) ) a destra per aprire il pannello destro _Allineamento marchio_ nell&#39;area di progettazione e-mail.

![Accedere agli strumenti di allineamento del marchio](./assets/brands-alignment-sidebar.png){width="600" zoomable="yes"}

Per informazioni dettagliate, consulta [Convalidare l&#39;allineamento del brand](./brand-alignment.md#validate-your-brand-alignment)
