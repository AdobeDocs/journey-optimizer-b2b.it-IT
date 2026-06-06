---
title: Nodo percorso migliore successivo
description: Utilizza le decisioni basate sull’intelligenza artificiale per indirizzare le persone lungo il percorso di percorso più pertinente in base a prompt del linguaggio naturale, dati comportamentali e contesto del profilo in tempo reale in Journey Optimizer B2B edition.
feature: Account Journeys, AI Assistant
role: User
autotag-review: '2026-05-20T18:52:08.227Z'
TQID: 'https://experienceleague.adobe.com/idPaG-ZNnNwJjN8yVC3Ay1FZ2XPgtQgrSMNIus4fReI'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: a4b836d9-ffdd-4df3-a62a-f78b830cf059
subfeature_v2: id: ba367494-9862-4596-bd6f-299c7e10a46b
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: c4147b6e-073b-4d3c-9ab1-d60f2f4434ef
source-git-commit: 7cd6c4ecfbbd3a86b4f30d1b4fe6f06655a9c4f5
workflow-type: tm+mt
source-wordcount: 1912
ht-degree: 0%

---

# Nodo percorso migliore successivo

Il nodo _Percorso migliore successivo_ porta le decisioni sui percorsi suddivisi basati sull&#39;intelligenza artificiale direttamente nell&#39;area di lavoro del percorso. Invece di configurare le condizioni del filtro su un nodo [percorsi suddivisi](./split-merge-paths-nodes.md), descrivi l&#39;intento in linguaggio naturale e consenti al sistema di determinare il percorso più rilevante per ogni persona.

>[!NOTE]
>
>I nodi del percorso migliore successivo sono disponibili solo nei percorsi di persone. Non sono supportati nei percorsi di account.

Nell&#39;acquisto B2B, un profilo può apparire come un tipo di acquirente, ma il loro comportamento, i dati firmografici e il contesto di coinvolgimento rivelano una storia più sfumata. Il nodo del percorso migliore successivo valuta tale contesto per prendere una decisione di indirizzamento intelligente, consentendo al contempo di rivedere, modificare o ignorare eventuali consigli di IA prima di attivare il percorso.

L’intelligenza artificiale valuta ogni persona rispetto ai prompt dei percorsi definiti utilizzando una combinazione di input:

* **Cronologia del coinvolgimento** - Apertura dell&#39;e-mail, clic sui collegamenti, visite alle pagine Web e altri segnali comportamentali provenienti dal percorso corrente e da quelli precedenti
* **Segnali in tempo reale** - Eventi ad alto intento come riempimenti di moduli e visite di pagina per la determinazione dei prezzi
* **Attributi del profilo** - Dati demografici, titolo del processo, persona e dati firmografici
* **Attributi dell&#39;account** - Dati firmografici e tecnografici associati all&#39;account della persona

Quando una persona raggiunge il nodo, il sistema recupera il contesto del profilo, applica vincoli e utilizza un messaggio LLM per selezionare il percorso più adatto. Ogni decisione viene registrata con un punteggio di affidabilità e un ragionamento in linguaggio naturale per la trasparenza e l&#39;osservabilità.

Se nessun percorso corrisponde o se il prompt fa riferimento a dati non disponibili per un profilo, la persona viene indirizzata al percorso di fallback predefinito.

## Aggiungi un nodo percorso migliore successivo {#add-next-best-path-node}

1. Apri il percorso di persone e passa alla mappa del percorso.

1. Fai clic sull&#39;icona più ( **+** ) in un percorso e scegli **[!UICONTROL Percorso migliore successivo]**.

   ![Aggiungi nodo percorso - percorso migliore successivo](./assets/add-node-next-best-path.png){width="350" zoomable="no"}

   Il nodo viene aggiunto all’area di lavoro e il pannello di configurazione della suddivisione IA viene visualizzato a destra. Inizia con un percorso e un percorso predefinito _Altre persone_ per indirizzare le persone che non sono idonee per nessuno dei percorsi definiti.

   ![Nodo percorso migliore successivo](./assets/node-next-best-path-new.png){width="500"}

## Configurare i percorsi {#configure-paths}

Per ogni percorso, definisci un nome e un prompt in linguaggio naturale che descriva chi deve essere indirizzato lì. L’input del prompt sostituisce completamente l’interfaccia utente della condizione del filtro; non sono presenti condizioni di attributo da configurare.

1. Fare clic su **[!UICONTROL Aggiungi percorso]** per ogni percorso aggiuntivo che si desidera includere per il nodo.

   Per rimuovere un percorso, fare clic sull&#39;icona _Elimina_ ( ![Icona Elimina](../assets/do-not-localize/icon-delete-outline.svg) ) sulla scheda del percorso.

1. Per ogni scheda percorso nel pannello di destra:

   * Immetti un **[!UICONTROL Label]** che rifletta il pubblico o l&#39;intento per quel segmento.

   * Immetti un **[!UICONTROL Prompt]** in linguaggio naturale che descriva chi appartiene a questo percorso. Concentrati su intento e risultato, non su valori di attributo specifici.

     <!-- To get prompt ideas, click **[!UICONTROL Suggest prompts]**. The system provides several example prompts tailored to the path context that you can use as-is or adapt. -->

     ![Nodo percorso migliore successivo - percorsi di esempio](./assets/node-next-best-path-new.png){width="500"}

     **Esempio di richiesta di una suddivisione a tre percorsi:**

      * _Percorso 1 - Leader HR :_Identifica le persone con ruoli di leadership HR che hanno più probabilità di interagire con la gestione dei talenti e con il contenuto dell&#39;esperienza dei dipendenti.
      * _Path 2 - Technical Evaluators :_Identifica i soggetti tecnici che hanno maggiori probabilità di interagire con l&#39;architettura del prodotto, le integrazioni e il contenuto dell&#39;implementazione.
      * _Path 3 - Business Decision-Makers :_Identifica le parti interessate più propense a interagire con ROI, risultati aziendali e contenuti di case study.

1. Se necessario, riordina i percorsi per impostare l’ordine di priorità per la corrispondenza.

   Il filtro dei percorsi viene valutato in ordine decrescente. Ogni persona procede lungo il primo percorso che corrisponde a.

   Fai clic sulle frecce su e giù in alto a destra di ciascuna scheda di percorsi per spostarla in alto o in basso nell’elenco dei percorsi.

   ![Nodo percorso migliore successivo - riordina percorsi](./assets/node-next-best-path-reorder-paths.png){width="500"}

1. Rivedi il percorso predefinito (ultimo nell’elenco dei percorsi) e, se necessario, modifica l’etichetta.

   Il percorso predefinito viene utilizzato quando l’intelligenza artificiale non è in grado di assegnare una persona a un percorso definito o quando i dati pertinenti non sono disponibili. Quando un prompt fa riferimento a dati che non esistono nel set di dati per un determinato profilo, il sistema indirizza tale profilo al percorso predefinito e contrassegna lo spazio vuoto di dati.

### Controlli Human-in-the-loop {#human-in-the-loop}

Le raccomandazioni basate sull’intelligenza artificiale non sono vincolanti. Prima di attivare il percorso, puoi effettuare le seguenti operazioni:

* Modificate qualsiasi richiesta di percorso per perfezionare la logica di indirizzamento.
* Aggiungere, rimuovere o riordinare i percorsi.
* Se necessario, sovrascrivi i suggerimenti di IA con condizioni personalizzate.

Le assegnazioni di percorsi basate sull’intelligenza artificiale diventano effettive solo dopo la pubblicazione del percorso.

## Esempi di richiesta per caso d’uso {#examples}

Gli esempi seguenti mostrano come scrivere prompt dei percorsi efficaci nei casi d’uso comuni di marketing B2B. Utilizzali come punti di partenza e adatta la lingua per adattarsi al contesto del tuo percorso e ai dati del pubblico.

### Ricerca attiva e segnali di acquisto {#active-research}

+++Percorso 1: ricercatori attivi sui prodotti

_Identificare le persone che ricercano attivamente il software CRM. Cerca visite ripetute alla pagina del prodotto, coinvolgimento con contenuti di confronto, visite di ritorno frequenti e segnali di intento elevati di terze parti negli ultimi 30 giorni._

+++

+++Percorso 2: comportamento di confronto dei prezzi

_Identifica gli utenti che hanno visualizzato più volte le pagine di confronto dei prezzi o dei piani negli ultimi 14 giorni, in particolare gli utenti che si alternano tra le pagine di documentazione dei prezzi e delle funzionalità._

+++

+++Percorso 3: intento elevato, nessuna conversione

_Identifica i visitatori ad alto intento che si sono impegnati con demo di prodotti, pagine di prezzi o documentazione di integrazione negli ultimi 21 giorni, ma che non hanno inviato un modulo o convertito._

+++

+++Percorso 4: comportamento di checkout esitante

_Identifica gli utenti che hanno avviato i flussi di pagamento o di prenotazione demo ma non li hanno completati e che hanno restituito almeno una volta in seguito senza convertire._

+++

### Rischio di abbandono e fidelizzazione {#churn-retention}

+++Percorso 1: segnali di rischio di abbandono

_Identifica i clienti che mostrano segni di abbandono dovuti al calo dell&#39;utilizzo dei prodotti, alla frequenza di accesso ridotta, ai picchi dei ticket di supporto e al minore impegno nel marketing negli ultimi 60 giorni._

+++

+++Percorso 2 - Disattivazione degli utenti esperti

_Identifica gli utenti precedentemente coinvolti la cui velocità di coinvolgimento è diminuita significativamente negli ultimi 30 giorni rispetto alla linea di base cronologica._

+++

### Carenze tra istruzione e valutazione {#education-evaluation}

+++Percorso 1: ricerca sulla sequenza di determinazione prezzi

_Identifica gli utenti che hanno scaricato un ebook e poi hanno visitato la pagina dei prezzi entro 7 giorni, ma non hanno richiesto una demo._

+++

+++Percorso 2 - Webinar senza follow-up

_Identifica le persone che hanno partecipato a un webinar e successivamente sono tornate alle pagine dei prodotti ma che non hanno mai prenotato una demo o contattato le vendite._

+++

+++Percorso 3 - Valutazione basata sul confronto

_Identifica i visitatori che hanno visualizzato un articolo di confronto con un concorrente e poi hanno visitato la documentazione sull&#39;integrazione o sulla migrazione entro 14 giorni._

+++

### Sequenze di coinvolgimento e-mail {#email-engagement}

+++Percorso 1: si apre senza clic

_Identifica i lead che hanno aperto tre o più e-mail marketing entro 30 giorni senza aver mai fatto clic sul sito Web._

+++

+++Percorso 2: clic ma nessun coinvolgimento più approfondito

_Identifica gli utenti che hanno fatto clic da un messaggio e-mail a una pagina di prodotto ma non hanno esplorato ulteriori pagine o non sono tornati entro 7 giorni._

+++

### Modelli di prova e conversione {#trial-conversion}

+++Percorso 1: convertitori veloci

_Identificare i clienti che hanno effettuato l&#39;aggiornamento entro 30 giorni dall&#39;avvio di una prova e hanno mostrato un elevato coinvolgimento nel prodotto durante il periodo di prova._

+++

+++Percorso 2: utenti con versione di prova bloccata

_Identificare gli utenti della versione di valutazione che hanno effettuato l&#39;accesso durante la prima settimana ma hanno mostrato un&#39;attività minima in seguito e non hanno effettuato la conversione prima della scadenza della versione di valutazione._

+++

### Acquirenti multicanale {#multi-channel}

+++Percorso 1 - Convergenza organica e annuncio

_Identifica gli utenti che si sono prima impegnati tramite annunci a pagamento e successivamente hanno fatto ritorno tramite canali diretti o organici entro 14 giorni._

+++

+++Percorso 2: valutazione da evento a prodotto

_Identifica gli account che hanno partecipato a un evento virtuale o di persona e che successivamente hanno aumentato il comportamento di ricerca dei prodotti entro 30 giorni._

+++

+++Percorso 3: ricercatori social-to-site

_Identifica gli utenti che hanno a che fare con contenuti social e successivamente hanno visitato pagine ad alto intento come prezzi o prenotazioni demo._

+++

### Segnali di acquisto regionali {#regional-buying}

+++Percorso 1: picco in una regione specifica

_Identifica gli account in Nord America che mostrano un aumento dell&#39;attività di ricerca sui prodotti e segnali di intenti di terze parti elevati negli ultimi 30 giorni rispetto alla linea di base storica._

+++

+++Percorso 2 - La spinta dei mercati emergenti

_Identificare gli account in APAC in cui la velocità di coinvolgimento è aumentata in modo significativo negli ultimi 14 giorni, anche se il volume complessivo di coinvolgimento è ancora moderato._

+++

+++Percorso 3: interesse aziendale specifico per l’area geografica

_Identifica gli account di dimensioni Enterprise nell&#39;area EMEA che hanno a che fare con la conformità, la residenza dei dati o la documentazione sulla sicurezza negli ultimi 21 giorni._

+++

+++Tracciato 4 - Territorio poco penetrato

_Identificare gli account di elevata idoneità nelle aree di vendita assegnate che hanno mostrato segnali di intento ma che le vendite non hanno ancora contattato._

+++

### Segnali di timing comportamentale {#behavioral-timing}

+++Percorso 1 - Ricercatori al di fuori dell’orario di lavoro

_Identifica gli utenti che interagiscono ripetutamente con pagine di prodotti e prezzi al di fuori del normale orario di lavoro nel loro fuso orario locale._

+++

+++Percorso 2: finestra di ricerca compressa

_Identifica gli account che mostrano una densità di coinvolgimento insolitamente elevata in una breve finestra di 72 ore in più aree di prodotto._

+++

+++Percorso 3: picco attività fine trimestre

_Identificare gli account con un aumento dell&#39;attività nella fase di valutazione durante gli ultimi 30 giorni del trimestre fiscale._

+++

## Simulare decisioni prima della pubblicazione {#simulate}

Utilizza la simulazione per verificare in che modo l’intelligenza artificiale valuta i prompt rispetto a un pubblico reale prima che il percorso venga avviato. È disponibile solo quando il percorso è nello stato _Bozza_ e non ha alcun effetto sui percorsi pubblicati. Utilizzalo per convalidare la logica di indirizzamento e creare fiducia nei consigli di IA.

### Eseguire una simulazione {#run-simulation}

1. Seleziona il nodo del percorso migliore successivo e fai clic sull&#39;icona _Simula_ ( ![Simula icona](../../assets/do-not-localize/icon-simulate-outline.svg) ) nella parte superiore del pannello di destra.

   ![Percorso migliore successivo - fai clic sull&#39;icona di simulazione](./assets/node-next-best-path-simulate-select.png){width="500"}

1. Nella finestra di dialogo, scegli il pubblico da utilizzare per la simulazione:

   * **[!UICONTROL Elenchi persone originali]** - Utilizza il pubblico dal nodo del pubblico. Specifica una dimensione di esempio quando il pubblico completo supera la soglia di simulazione.
   * **[!UICONTROL Elenchi dinamici e statici]** - Utilizzare un elenco [!DNL Marketo Engage] statico o dinamico.
   * **[!UICONTROL Record di test]** - Utilizza i profili di test suggeriti dall&#39;intelligenza artificiale.

   ![Percorso migliore successivo - Simula - scegli il pubblico](./assets/node-next-best-path-simulate-dialog.png){width="300"}

   >[!NOTE]
   >
   >Se il pubblico selezionato supera la soglia di simulazione, il sistema esegue la simulazione su un campione di 100 profili. Un indicatore nell’interfaccia utente mostra che i risultati sono basati su campioni.
   >
   >Se il pubblico selezionato non è ancora materializzato, la simulazione viene bloccata. Un avviso in linea indica di materializzare prima il pubblico.

1. Fare clic su **[!UICONTROL Simula]**.

### Esamina risultati simulazione {#review-simulation-results}

Dopo l’esecuzione della simulazione, il pannello a destra mostra come i profili sono stati distribuiti su ciascun percorso e il ragionamento dell’intelligenza artificiale alla base di tali assegnazioni:

| Risultato | Descrizione |
| ------ | ----------- |
| **Profili** | Il numero di profili indirizzati al percorso. |
| **Dividere** | Percentuale di profili indirizzati al percorso. |
| **Affidabilità** | Livello di affidabilità AI per l’assegnazione del percorso. L’affidabilità riflette la freschezza dei dati, la forza e la coerenza del segnale e il successo storico di modelli di routing simili. |
| **Chiedi conferma** | Il prompt valutato per il percorso. |
| **Motivo IA** | Spiegazione in linguaggio naturale del motivo per cui i profili sono stati collettivamente assegnati a questo percorso. |

![Percorso migliore successivo - Simula - Risultati per il percorso](./assets/node-next-best-path-simulate-path-result.png){width="400"}

>[!NOTE]
>
>Quando i dati o l’ambito disponibili limitano una decisione, i risultati includono informazioni sulla limitazione. Ad esempio, quando un attributo obbligatorio non è presente nel set di dati, i risultati includono un indicatore esplicito che spiega in che modo i dati mancanti hanno influito sui risultati.

Utilizzare i risultati per perfezionare i prompt e verificare che il ciclo di produzione rifletta il risultato desiderato. È possibile modificare le richieste di percorso ed eseguire nuovamente la simulazione il numero di volte necessario prima di pubblicarla.

## Pubblicare e monitorare il percorso {#publish-and-monitor}

Dopo aver convalidato i risultati della simulazione:

1. Connetti il pubblico persone al nodo di ingresso percorso.

1. [Pubblica il percorso](./create-publish-journey.md#publish-a-journey).

Una volta che il percorso è attivo, il nodo del percorso migliore successivo viene eseguito al momento dell’esecuzione. Man mano che ogni persona raggiunge il nodo, l’intelligenza artificiale li valuta in tempo reale utilizzando i segnali più recenti e li indirizza al percorso più rilevante.

Per un percorso pubblicato, apri la mappa del percorso e seleziona il nodo del percorso migliore successivo per visualizzare la sezione **[!UICONTROL Risultati live]** nel pannello di destra. I risultati live mostrano:

* La distribuzione percentuale dei profili in ciascun percorso
* Punteggio di affidabilità per ogni assegnazione di percorso
* Ragionamento a livello di percorso e di profilo, con dettagli espandibili per i singoli profili

I risultati live sono disponibili anche nella console Percorso e tramite l&#39;[abilità Osservabilità Percorso](../agents/journey-agent.md#journey-observability-skill) nell&#39;hub AI.
