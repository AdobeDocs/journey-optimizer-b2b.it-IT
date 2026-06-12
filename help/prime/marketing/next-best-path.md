---
title: Nodo percorso migliore successivo
description: Utilizza il nodo Migliore percorso successivo in Journey Optimizer B2B Prime per l’instradamento del percorso basato sull’intelligenza artificiale con prompt in linguaggio naturale, simulazione del percorso, punteggi di affidabilità e risultati del percorso suddiviso in tempo reale.
badgeBeta: label="Beta" type="informative" tooltip="Questa funzione è attualmente in versione beta limitata"
source-git-commit: 2f19137465c71f2292d37bea5786533b1df6e286
workflow-type: tm+mt
source-wordcount: '2205'
ht-degree: 0%

---

# Nodo percorso migliore successivo

In Journey Optimizer B2B Prime, il nodo *Next best path* porta le decisioni sui percorsi suddivisi basati su intelligenza artificiale direttamente nell&#39;area di lavoro del percorso. Invece di configurare le condizioni del filtro su un nodo [percorsi suddivisi](./split-merge-paths-nodes.md), descrivi l&#39;intento in linguaggio naturale e consenti al sistema di determinare il percorso più rilevante per ogni persona.

Nell&#39;acquisto B2B, un profilo può apparire come un tipo di acquirente, ma il loro comportamento, i dati firmografici e il contesto di coinvolgimento rivelano una storia più sfumata. Il nodo del percorso migliore successivo valuta tale contesto per prendere una decisione di indirizzamento intelligente, consentendo al contempo di rivedere, modificare o ignorare eventuali consigli di IA prima di attivare il percorso.

## Decisioning del percorso {#path-decisioning}

È possibile passare da un intento all&#39;attivazione in tre passaggi.

* **Passaggio 1: definizione dei percorsi** — Aggiungere un nodo Percorso migliore successivo nel percorso, assegnare un nome a ciascun percorso e scrivere un prompt in linguaggio naturale che descriva chi deve avanzare lungo il percorso. È possibile aggiungere o rimuovere percorsi in qualsiasi momento.

* **Passaggio 2: simulare** — Selezionare un pubblico di esempio ed eseguire una simulazione. Puoi visualizzare i conteggi dei profili per percorso, i punteggi di affidabilità e il ragionamento dell’intelligenza artificiale in modo da poter convalidare la logica prima di attivare.

  >[!NOTE]
  >
  >La simulazione viene eseguita solo sui dati di esempio e non influisce mai sull’esecuzione del percorso live.

* **Passaggio 3: attiva** — pubblica il percorso in base al pubblico reale. L’intelligenza artificiale valuta ogni persona in fase di runtime, assegna il percorso di adattamento migliore in tempo reale e un fallback predefinito assicura che nessuno raggiunga un vicolo cieco.

### Input di decisioning IA {#ai-decisioning-inputs}

Quando una persona raggiunge il nodo, il sistema recupera il contesto del profilo, applica vincoli e utilizza un messaggio LLM per selezionare il percorso più adatto. L’IA valuta ogni persona utilizzando una combinazione dei seguenti input:

* **Cronologia del coinvolgimento** - Apertura dell&#39;e-mail, clic sui collegamenti, visite alle pagine Web e altri segnali comportamentali provenienti dal percorso corrente e da quelli precedenti
* **Segnali in tempo reale** - Eventi ad alto intento come riempimenti di moduli e visite di pagina per la determinazione dei prezzi
* **Attributi del profilo** - Dati demografici, titolo del processo, persona e dati firmografici
* **Attributi dell&#39;account** - Dati firmografici e tecnografici associati all&#39;account della persona

### Creazione contesto IA {#ai-context-building}

Alla base della decisione di indirizzamento, l’intelligenza artificiale costruisce un livello dedotto per ciascun profilo. Combina dati demografici e firmografici, dettagli dell’account e segnali comportamentali (come dettagli dell’utente tipo, intento di problema e intento di prodotto) in un riepilogo contestuale per quella persona. Utilizzando questo contesto arricchito, l’intelligenza artificiale può indirizzare ogni persona al percorso ottimale e fornire sia un punteggio di affidabilità che il ragionamento in linguaggio naturale alla base di ogni decisione.

Ogni decisione viene registrata con un punteggio di affidabilità e un ragionamento in linguaggio naturale per la trasparenza e l&#39;osservabilità.

Se nessun percorso corrisponde o se il prompt fa riferimento a dati non disponibili per un profilo, la persona viene indirizzata al percorso di fallback predefinito.

## Aggiungi un nodo percorso migliore successivo {#add-node}

1. Apri il percorso di persone e passa alla mappa del percorso.

1. Fai clic sull&#39;icona più ( **+** ) in un percorso e scegli **Percorso migliore successivo**.

   Il nodo viene aggiunto all’area di lavoro e il pannello di configurazione con suddivisione IA si apre a destra. Inizia con un percorso e un percorso predefinito *Altre persone* per indirizzare le persone che non sono idonee per nessuno dei percorsi definiti.

## Configurare i percorsi {#configure-paths}

Per ogni percorso, definisci un nome e un prompt in linguaggio naturale che descriva chi deve essere indirizzato lì. L’input del prompt sostituisce completamente l’interfaccia utente della condizione del filtro; non sono presenti condizioni di attributo da configurare.

1. Fare clic su **Aggiungi percorso** per ogni percorso aggiuntivo che si desidera includere.

   Per rimuovere un percorso, fare clic sull&#39;icona *Elimina* nella scheda del percorso.

1. Per ogni scheda percorso nel pannello di destra:

   * Immetti un **Label** che rifletta il pubblico o l&#39;intento per quel segmento.

   * Immetti un **Prompt** in linguaggio naturale che descriva chi appartiene a questo percorso. Concentrati su intento e risultato, non su valori di attributo specifici.

     **Esempio di richiesta di una suddivisione a tre percorsi:**

      * *Percorso 1 - Responsabili HR:* Identificare le persone con ruoli di leadership HR che hanno più probabilità di interagire con la gestione dei talenti e con il contenuto dell&#39;esperienza dei dipendenti.
      * *Percorso 2 - Valutatori tecnici:* Identifica i soggetti tecnici che hanno più probabilità di interagire con l&#39;architettura del prodotto, le integrazioni e il contenuto dell&#39;implementazione.
      * *Percorso 3 - Responsabili delle decisioni aziendali:* Identifica le parti interessate più propense a interagire con il ROI, i risultati aziendali e il contenuto del caso aziendale.

1. Se necessario, riordina i percorsi per impostare l’ordine di priorità per la corrispondenza.

   Il filtro dei percorsi viene valutato in ordine decrescente. Ogni persona procede lungo il primo percorso che corrisponde a. Fai clic sulle frecce su e giù in alto a destra di ciascuna scheda del percorso per spostarla in alto o in basso nell’elenco.

1. Rivedi il percorso predefinito (ultimo nell’elenco dei percorsi) e, se necessario, modifica l’etichetta.

   Il percorso predefinito viene utilizzato quando l’intelligenza artificiale non è in grado di assegnare una persona a un percorso definito o quando i dati pertinenti non sono disponibili. Quando un prompt fa riferimento a dati che non esistono nel set di dati per un determinato profilo, il sistema indirizza tale profilo al percorso predefinito e contrassegna lo spazio vuoto di dati.

>[!BEGINSHADEBOX]

**Controlli Human-in-the-loop**

Le raccomandazioni basate sull’intelligenza artificiale non sono vincolanti. Prima di attivare il percorso, puoi effettuare le seguenti operazioni:

* Modificate qualsiasi richiesta di percorso per perfezionare la logica di indirizzamento.
* Aggiungere, rimuovere o riordinare i percorsi.
* Se necessario, sovrascrivi i suggerimenti di IA con condizioni personalizzate.

Le assegnazioni di percorsi basate sull’intelligenza artificiale diventano effettive solo dopo la pubblicazione del percorso.

>[!ENDSHADEBOX]

## Esempi di richiesta per caso d’uso {#prompt-examples}

Gli esempi seguenti mostrano come scrivere prompt dei percorsi efficaci nei casi d’uso comuni di marketing B2B. Utilizzali come punti di partenza e adatta la lingua per adattarsi al contesto del tuo percorso e ai dati del pubblico.

+++Ricerca attiva e segnali di acquisto

**Percorso 1 - Ricercatori prodotti attivi**
*Identificare le persone che ricercano attivamente il software CRM. Cerca visite ripetute alla pagina del prodotto, coinvolgimento con contenuti di confronto, visite di ritorno frequenti e segnali di intento elevati di terze parti negli ultimi 30 giorni.*

**Percorso 2 - Comportamento di confronto prezzi**
*Identifica gli utenti che hanno visualizzato più volte le pagine di confronto dei prezzi o dei piani negli ultimi 14 giorni, in particolare quelli che si alternano tra le pagine di documentazione dei prezzi e delle funzionalità.*

**Percorso 3 - Intento elevato, nessuna conversione**
*Identifica i visitatori ad alto intento che si sono impegnati con demo di prodotti, pagine di prezzi o documentazione di integrazione negli ultimi 21 giorni, ma che non hanno inviato un modulo o convertito.*

**Percorso 4: comportamento di estrazione esitante**
*Identifica gli utenti che hanno avviato i flussi di pagamento o di prenotazione demo ma non li hanno completati e che hanno restituito almeno una volta in seguito senza convertirli.*

+++

+++Rischio di abbandono e fidelizzazione

**Percorso 1 - Segnali di rischio di abbandono**
*Identifica i clienti che mostrano segni di abbandono dovuti al calo dell&#39;utilizzo dei prodotti, alla frequenza di accesso ridotta, ai picchi dei ticket di supporto e al minore impegno nel marketing negli ultimi 60 giorni.*

**Percorso 2 - Disattivazione degli utenti esperti**
*Identifica gli utenti precedentemente coinvolti la cui velocità di coinvolgimento è diminuita significativamente negli ultimi 30 giorni rispetto alla linea di base cronologica.*

+++

+++Carenze tra istruzione e valutazione

**Percorso 1 - Ricerca nella sequenza di determinazione prezzi**
*Identifica gli utenti che hanno scaricato un ebook e poi hanno visitato la pagina dei prezzi entro 7 giorni, ma non hanno richiesto una demo.*

**Percorso 2 - Webinar senza follow-up**
*Identifica le persone che hanno partecipato a un webinar e successivamente sono tornate alle pagine dei prodotti ma che non hanno mai prenotato una demo o contattato le vendite.*

**Percorso 3 - Valutazione basata sul confronto**
*Identifica i visitatori che hanno visualizzato un articolo di confronto con un concorrente e poi hanno visitato la documentazione sull&#39;integrazione o sulla migrazione entro 14 giorni.*

+++

+++Sequenze di coinvolgimento e-mail

**Percorso 1 - Si apre senza clic**
*Identifica i lead che hanno aperto tre o più e-mail marketing entro 30 giorni senza aver mai fatto clic sul sito Web.*

**Percorso 2: clic effettuato, ma nessun coinvolgimento più approfondito**
*Identifica gli utenti che hanno fatto clic da un messaggio e-mail a una pagina di prodotto ma non hanno esplorato ulteriori pagine o non sono tornati entro 7 giorni.*

+++

+++Modelli di prova e conversione

**Percorso 1 - Convertitori veloci**
*Identificare i clienti che hanno effettuato l&#39;aggiornamento entro 30 giorni dall&#39;avvio di una prova e hanno mostrato un elevato coinvolgimento nel prodotto durante il periodo di prova.*

**Percorso 2 - Versione di prova degli utenti bloccati**
*Identificare gli utenti della versione di valutazione che hanno effettuato l&#39;accesso durante la prima settimana ma hanno mostrato un&#39;attività minima in seguito e non hanno effettuato la conversione prima della scadenza della versione di valutazione.*

+++

+++Acquirenti multicanale

**Percorso 1 - Convergenza organica e annuncio**
*Identifica gli utenti che hanno iniziato a utilizzare gli annunci a pagamento e successivamente hanno fatto ritorno tramite canali diretti o organici entro 14 giorni.*

**Percorso 2 - Valutazione da evento a prodotto**
*Identificare gli account che hanno partecipato a un evento di persona o virtuale e successivamente hanno aumentato il comportamento di ricerca dei prodotti entro 30 giorni.*

**Percorso 3 - Ricercatori da social-to-site**
*Identifica gli utenti che hanno a che fare con contenuti social e successivamente hanno visitato pagine ad alto intento come prezzi o prenotazioni dimostrative.*

+++

+++Segnali di acquisto regionali

**Percorso 1 - Incremento in una regione specifica**
*Identifica gli account in Nord America che mostrano un aumento dell&#39;attività di ricerca sui prodotti e segnali di intenti di terze parti elevati negli ultimi 30 giorni rispetto alla linea di base storica.*

**Percorso 2: slancio dei mercati emergenti**
*Identificare gli account in APAC in cui la velocità di coinvolgimento è aumentata in modo significativo negli ultimi 14 giorni, anche se il volume complessivo di coinvolgimento è ancora moderato.*

**Percorso 3: interesse aziendale specifico per l&#39;area geografica**
*Identifica gli account di dimensioni Enterprise nell&#39;area EMEA che hanno a che fare con la conformità, la residenza dei dati o la documentazione sulla sicurezza negli ultimi 21 giorni.*

**Percorso 4 - Territorio poco penetrato**
*Identificare gli account di elevata idoneità nelle aree di vendita assegnate che hanno mostrato segnali di intento ma che le vendite non hanno ancora contattato.*

+++

+++Targeting del pubblico del webinar

**Percorso 1 - Leader HR interessati all’intelligenza artificiale**
*Identificare le persone che hanno partecipato a siti HR (shrm.org, hbr.org/topic/human-resource-management), interessate a Journey Optimizer negli ultimi 30 giorni, che probabilmente parteciperanno a un webinar su &quot;IA in HR Operations&quot;. Dovrebbero inoltre aver mostrato un certo interesse per i prodotti AI.*

**Percorso 2: professionisti della finanza interessati all’intelligenza artificiale**
*Identificare le persone che hanno partecipato a siti di finanza (wsj.com/finance, investopedia.com), interessate a Marketo negli ultimi 30 giorni, che probabilmente parteciperanno a un webinar su &quot;AI in Financial Planning&quot;. Dovrebbero inoltre aver mostrato un certo interesse per i prodotti AI.*

**Percorso 3: professionisti del rischio e della ricerca interessati all’intelligenza artificiale**
*Identificare le persone che hanno partecipato a siti di ricerca/rischio (mckinsey.com/capabilities/risk-and-resilience, forrester.com/research), interessate a GenStudio negli ultimi 30 giorni, che probabilmente parteciperanno a un webinar su &quot;IA in Risk Management&quot;. Dovrebbero inoltre aver mostrato un certo interesse per i prodotti AI.*

+++

+++Segnali di timing comportamentale

**Percorso 1 - Ricercatori fuori orario**
*Identifica gli utenti che interagiscono ripetutamente con pagine di prodotti e prezzi al di fuori del normale orario di lavoro nel loro fuso orario locale.*

**Percorso 2 - Finestra di ricerca compressa**
*Identifica gli account che mostrano una densità di coinvolgimento insolitamente elevata in una breve finestra di 72 ore in più aree di prodotto.*

**Percorso 3: picco attività fine trimestre**
*Identificare gli account con un aumento dell&#39;attività nella fase di valutazione durante gli ultimi 30 giorni del trimestre fiscale.*

+++

## Simulare decisioni prima della pubblicazione {#simulate}

Utilizza la simulazione per verificare in che modo l’intelligenza artificiale valuta i prompt rispetto a un pubblico reale prima che il percorso venga avviato. La simulazione è disponibile solo quando il percorso è nello stato *Bozza* e non ha alcun effetto sui percorsi pubblicati.

### Eseguire una simulazione {#run-simulation}

1. Seleziona il successivo nodo del percorso migliore e fai clic sull&#39;icona *Simula* nella parte superiore del pannello di destra.

1. Nella finestra di dialogo, scegli il pubblico da utilizzare per la simulazione:

   * **[!UICONTROL Elenchi persone originali]** - Utilizza il pubblico dal nodo del pubblico. Specifica una dimensione di esempio quando il pubblico completo supera la soglia di simulazione.
   * **[!UICONTROL Elenchi dinamici e statici]** - Utilizzare un elenco statico o dinamico di Marketo Engage.
   * **[!UICONTROL Record di test]** - Utilizza i profili di test suggeriti dall&#39;intelligenza artificiale.

   >[!NOTE]
   >
   >* Se il pubblico selezionato supera la soglia di simulazione, il sistema esegue la simulazione su un campione di 100 profili. Un indicatore nell’interfaccia utente mostra che i risultati sono basati su campioni.
   >* Se il pubblico selezionato non è ancora materializzato, la simulazione viene bloccata. Un avviso in linea indica di materializzare prima il pubblico.

1. Fare clic su **[!UICONTROL Simula]**.

### Esamina risultati simulazione {#review-results}

Dopo l’esecuzione della simulazione, il pannello a destra visualizza la distribuzione dei profili su ciascun percorso e il ragionamento di intelligenza artificiale alla base di tali assegnazioni:

| Risultato | Descrizione |
|---|---|
| **Profili** | Il numero di profili indirizzati al percorso. |
| **Dividere** | Percentuale di profili indirizzati al percorso. |
| **Affidabilità** | Livello di affidabilità AI per l’assegnazione del percorso. L’affidabilità riflette la freschezza dei dati, la forza e la coerenza del segnale e il successo storico di modelli di routing simili. |
| **Chiedi conferma** | Il prompt valutato per il percorso. |
| **Motivo IA** | Spiegazione in linguaggio naturale del motivo per cui i profili sono stati collettivamente assegnati a questo percorso. |

>[!NOTE]
>
>Quando i dati o l’ambito disponibili limitano una decisione, i risultati includono informazioni sulla limitazione. Ad esempio, quando un attributo obbligatorio non è presente nel set di dati, i risultati includono un indicatore esplicito che spiega in che modo i dati mancanti hanno influito sui risultati.

Utilizzare i risultati per perfezionare i prompt e verificare che il ciclo di produzione rifletta il risultato desiderato. È possibile modificare le richieste di percorso ed eseguire nuovamente la simulazione il numero di volte necessario prima di pubblicarla.

## Pubblicare e monitorare il percorso {#publish-monitor}

Dopo aver convalidato i risultati della simulazione:

1. Connetti il pubblico persone al nodo di ingresso percorso.

2. [Pubblica il percorso](./journeys-overview.md).

Una volta che il percorso è attivo, il nodo del percorso migliore successivo viene eseguito al momento dell’esecuzione. Man mano che ogni persona raggiunge il nodo, l’intelligenza artificiale li valuta in tempo reale utilizzando i segnali più recenti e li indirizza al percorso più rilevante.

Per un percorso pubblicato, apri la mappa del percorso e seleziona il nodo del percorso migliore successivo per visualizzare la sezione **_[!UICONTROL Risultati live]_** nel pannello di destra. I risultati live mostrano:

* La distribuzione percentuale dei profili in ciascun percorso
* Punteggio di affidabilità per ogni assegnazione di percorso
* Ragionamento a livello di percorso e di profilo, con dettagli espandibili per i singoli profili

I risultati live sono disponibili anche nella console del Percorso e attraverso l’abilità Osservabilità del Percorso nell’hub AI.