---
title: Punteggi intento
description: Scopri in che modo Journey Optimizer B2B edition calcola i punteggi di intento in base al coinvolgimento delle persone e alla rilevanza dei contenuti, e come i punteggi si aggregano per gli account.
feature: Dashboards, Intent, Intelligent Insights
role: User
autotag-review: '2026-09-11T14:56:32.307Z'
TQID: 'https://experienceleague.adobe.com/ajtUdNKafSoE1BC08imOpyflpDeAsXaQ3tdlbeYT6NU'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: f979fe0e-02fe-4599-b492-7b3df1d4e7dc
subfeature_v2:
  - id: e388c29d-df1e-4b47-ad27-1b14ae45776e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
  - id: eb30f47f-d87a-400f-8f78-63ce7979ff56
source-git-commit: 2da5c7bbbadde4bbb5df82a81398ecb970165da2
workflow-type: tm+mt
source-wordcount: 1445
ht-degree: 0%

---


# Punteggi intento {#intent-scores}

Un punteggio intento misura quanto una persona o un account sia interessato a una parola chiave, a un prodotto o a una categoria di prodotti. Adobe Journey Optimizer B2B edition calcola il punteggio utilizzando l’apprendimento automatico che misura la somiglianza nel significato, anziché con le regole manuali o con un sistema a punti fissi. Ogni punteggio è normalizzato da 0 a 1, con numeri più alti che indicano un intento più forte.

La rilevanza dei contenuti viene aggiornata all’incirca ogni 12 ore e i punteggi intento vengono ricalcolati quotidianamente. I punteggi vengono aggregati da parola chiave a prodotto e da persona a account. I punteggi delle finalità vengono visualizzati in [Intelligent Dashboard](../dashboards/intelligent-dashboard.md), nei [dettagli account](../accounts/account-details.md), [_dettagli gruppo acquisti_ pagina](../buying-groups/buying-group-details.md) e [dettagli persona](../accounts/person-details.md) pagine.

![Visualizzazione dati intento](../data/assets/intent-data-visualization.png){width="700" zoomable="yes"}

Nelle sezioni seguenti vengono illustrati i concetti fondamentali alla base del punteggio intento, il processo continuo che mantiene aggiornati i punteggi, la logica di calcolo alla base di ogni punteggio e le impostazioni configurabili.

## Concetti di base {#core-concepts}

Il rilevamento dell’intento misura con quale precisione una persona si impegna corrisponde ai tuoi prodotti e alle tue parole chiave, quindi pondera tale somiglianza in base al livello di coinvolgimento della persona. Questo modello è costituito da tre entità.

| Entità | Descrizione |
|--------|--------------|
| Persona | L’individuo che interagisce con il contenuto aprendo le e-mail, visitando le pagine web e coinvolgendo nel tempo. |
| Contenuti | Le e-mail e le pagine web con cui una persona si impegna. Altri formati, come webinar e campagne, vengono aggiunti nel tempo. |
| Tassonomia | La struttura delle parole chiave, dei prodotti e delle categorie di prodotti che rappresenta gli interessi che desideri misurare. |

### Tassonomia e aggiornamenti predefiniti {#taxonomy}

La tassonomia, le parole chiave, i prodotti e le categorie in base ai quali viene misurato l’intento sono disponibili per l’utilizzo senza alcuna configurazione richiesta.

Puoi rivedere e aggiornare i mapping della tassonomia in qualsiasi momento nella pagina _[!UICONTROL Mapping intento]_. Vedi [Dati intento](../admin/intent-data.md) per il processo di configurazione della tassonomia.

### Rilevanza dei contenuti {#content-relevance}

Journey Optimizer B2B edition traduce il contenuto e la tassonomia in una rappresentazione matematica del loro significato, quindi utilizza un modello di somiglianza per misurare quanto strettamente si allineano. I contenuti che corrispondono strettamente a una parola chiave o a un prodotto ricevono un punteggio di rilevanza elevato. I contenuti non correlati ricevono un punteggio basso.

Il modello di similarità è preformato sul linguaggio generale, quindi non è necessario alcun training specifico per il cliente per iniziare.

## Processo punteggio {#scoring-process}

Un processo continuo trasforma il coinvolgimento non elaborato in un punteggio intento finito. Ogni fase si basa su ciò che è stato prodotto nella fase precedente.

![Diagramma di flusso di cinque fasi di punteggio: acquisizione del coinvolgimento, estrazione del contenuto, punteggio di rilevanza, calcolo dell&#39;intento giornaliero e distribuzione del punteggio.](./assets/intent-scores-pipeline.svg){width="700"}

### Acquisizione del coinvolgimento {#engagement-capture}

Ogni punto di contatto significativo che una persona ha viene acquisito mentre accade e collegato al contenuto coinvolto.

* Le visite alle pagine, le aperture delle e-mail e i clic, l’invio di moduli e attività simili vengono registrati come eventi di coinvolgimento.
* Ogni elemento di contenuto univoco viene inoltre annotato in modo che possa essere analizzato nella fase successiva.
* **Frequenza di aggiornamento** - Continua, in base al coinvolgimento.

### Estrazione dei contenuti {#content-extraction}

Prima che il contenuto possa essere valutato per rilevanza, Journey Optimizer B2B edition estrae e legge il relativo testo.

* Per ogni nuovo contenuto, il sistema estrae il testo sottostante, sia che si trovi in una pagina web che in un messaggio e-mail.
* Alcuni tipi di attività, come i riempimenti di moduli, presentano già un proprio contenuto descrittivo e saltano questo passaggio.
* Il contenuto che non può essere recuperato, ad esempio un collegamento interrotto o rimosso, viene registrato ed escluso in futuro.
* **Frequenza di aggiornamento** - Quando viene individuato nuovo contenuto.

### Punteggio di rilevanza {#relevance-scoring}

Ogni risorsa viene valutata in base alla tassonomia, indipendentemente da chi vi si è impegnato.

* Ogni e-mail e pagina web viene analizzata e confrontata con le parole chiave, i prodotti e le categorie utilizzando il modello di somiglianza.
* Il risultato è un punteggio di rilevanza compreso tra 0 e 1 per quella risorsa rispetto a ciascuna parola chiave o prodotto correlato.
* **Frequenza di aggiornamento** - Ogni 12 ore.

### Calcolo intento giornaliero {#daily-intent-calculation}

Il coinvolgimento e la rilevanza dei contenuti si combinano in un punteggio intento giornaliero per persona, per parola chiave o per prodotto.

* Ogni tipo di attività ha un peso configurabile. Ad esempio, l’invio di un modulo può essere molto più importante della visualizzazione di una pagina.
* Le attività recenti sono più importanti delle attività precedenti, quindi i punteggi favoriscono le attività svolte da qualcuno questa settimana rispetto a quelle svolte un mese fa.
* Una misura di affidabilità riflette quanto coerente è stato il coinvolgimento di una persona, non solo il volume.
* **Frequenza aggiornamento** - Giornaliera.

### Consegna del punteggio {#score-delivery}

I punteggi giornalieri si aggregano, ricevono un livello intento e vengono consegnati alla dashboard.

* A ogni punteggio viene assegnato un livello di intento Alto, Medium o Basso.
* I punteggi sono collegati all’account corretto, in modo che i team di vendita e marketing possano vedere l’intento a livello di persona e di account.
* Vengono aggiornate solo le persone il cui livello di intento è stato modificato, pertanto la dashboard riflette l’ultimo spostamento significativo.
* **Frequenza aggiornamento** - Giornaliera.

## Logica di calcolo del punteggio {#score-calculation-logic}

Il calcolo è costituito da cinque livelli, ciascuno dei quali aggiunge più contesto ai dati di rilevanza e coinvolgimento non elaborati.

### Rilevanza dei contenuti per un argomento {#relevance-to-topic}

Ogni elemento di contenuto e ogni argomento, ovvero una parola chiave, un prodotto o una categoria, viene tradotto in una rappresentazione matematica del suo significato. I contenuti con un significato simile a un argomento sono più simili in questa rappresentazione. La rilevanza è una misura di vicinanza nel significato, non una corrispondenza esatta di parole.

### Ponderazione giornaliera del coinvolgimento {#engagement-weighting}

In un dato giorno, il punteggio di una persona è una media ponderata della rilevanza di tutto ciò con cui si è impegnata. Le attività di valore superiore contano per altre attività.

>[!BEGINSHADEBOX &quot;Esempio&quot;]

Una persona si impegna con tre contenuti in un giorno. Le visualizzazioni di pagina hanno un peso di uno e gli invii di moduli hanno un peso di cinque.

Poiché l’invio di un modulo conta cinque volte di più di una visualizzazione di pagina, influenza in modo significativo il punteggio giornaliero anche se hanno interagito con tre elementi in totale.

Il loro punteggio giornaliero risultante per quell&#39;argomento è circa 0,70 su una scala da 0 a 1.

>[!ENDSHADEBOX]

### Decadimento recente {#recency-decay}

Il punteggio di una persona riflette una combinazione degli ultimi diversi giorni, con l’attività recente pesata molto più pesantemente rispetto all’attività più vecchia. Dopo circa una settimana, le attività meno recenti hanno un impatto minimo, pertanto il punteggio riflette sempre l’interesse corrente. In pratica, una visita di oggi ha più peso di una di ieri, che supera quella di 10 giorni fa.

### Normalizzazione dei punteggi e livelli di intento {#normalization-intent-levels}

Ogni punteggio adeguato viene posizionato su una scala coerente da 0 a 1 relativa ad altre persone nella tua istanza, quindi inserito in un livello intento.

| Punteggio finale | Livello intento |
|-------------|--------------|
| Superiore a 0,6 | Alta |
| Da 0.2 a 0.6 | Canale |
| Inferiore a 0,2 | Bassa |

### Aggregazione punteggio {#score-aggregation}

I singoli punteggi vengono aggregati in modo da poter esaminare l’intento a livello rilevante per una decisione, non solo a livello granulare.

* **Parola chiave per il prodotto** - Punteggi calcolati a livello di parola chiave aggregati per mostrare interesse per un prodotto, non solo per un singolo termine di ricerca.
* **Persona all&#39;account** - Un punteggio di account aggrega tutti i punteggi delle persone, in modo da poter vedere quando un intero gruppo di acquisto mostra l&#39;intento.

![Diagramma che mostra l&#39;aggregazione dei punteggi delle parole chiave ai punteggi dei prodotti e l&#39;aggregazione dei punteggi delle persone ai punteggi degli account.](./assets/intent-scores-aggregation.svg){width="500"}

Utilizza la visualizzazione a livello di prodotto per vedere quali prodotti stanno aumentando di interesse in generale, piuttosto che quali singole parole chiave hanno una tendenza. Utilizza la visualizzazione a livello di account per vedere quando un intero gruppo di acquisto mostra un interesse maggiore insieme, anziché reagire a una singola persona coinvolta.

## Impostazioni configurabili {#configurable-settings}

La maggior parte della logica di punteggio è fissa per mantenere i risultati affidabili e comparabili nel tempo. L’amministratore del prodotto può personalizzare due impostazioni in base alle proprie esigenze:

* **Pesi delle attività** - Per applicare un impatto maggiore ai punteggi di intento, aumenta il peso delle attività di valore elevato, ad esempio una richiesta demo o una visita a una pagina di determinazione prezzi. Per escludere completamente un’attività, impostane il peso su zero, utile per azioni quali gli annullamenti dell’abbonamento che non contribuiscono all’intento. I pesi delle attività per il calcolo dell&#39;intento utilizzano lo stesso modello di ponderazione che genera anche [punteggi di coinvolgimento](../buying-groups/engagement-scores.md). Consulta [_Configurare la ponderazione del punteggio di coinvolgimento_](../admin/engagement-score-weighting.md) per modificare i pesi delle attività.

* **Mappature tassonomia** - Le parole chiave, i prodotti e le categorie su cui si basa il punteggio sono disponibili per l&#39;uso. Puoi rivederli e aggiornarli in qualsiasi momento nella pagina _[!UICONTROL Mappatura intento]_. Vedi [_Dati intento_](../admin/intent-data.md) per il processo di installazione.

Tutto il resto, compresi la rilevanza dei contenuti, il decadimento dell&#39;attività e le soglie _Alta_, _Medium_ e _Bassa_, è risolto in modo che i punteggi rimangano coerenti e comparabili nel tempo.

## Principi di assegnazione del punteggio {#scoring-principles}

Quando rivedi e agisci in base ai punteggi di intento, tieni presente i seguenti principi.

### Punteggio basato su modello {#model-driven}

Non vi sono assegnazioni di punti o regole di parole chiave da mantenere. Il modello apprende la rilevanza direttamente dal contenuto e dalla tassonomia, mantenendo coerente il punteggio con la crescita e le modifiche della libreria di contenuti, senza dover eseguire una configurazione continua.

### Punteggio relativo {#relative-scoring}

Un punteggio riflette il punto in cui una persona o un account si colloca tra gli altri contatti odierni e il sistema lo ricalcola quotidianamente in base alla popolazione corrente. Utilizza i punteggi per confrontare persone e account nella tua istanza, anziché come numero fisso e universale. I punteggi non sono direttamente confrontabili da un’azienda all’altra.

### Aggiornamento dei dati {#data-freshness}

La rilevanza dei contenuti viene aggiornata approssimativamente ogni 12 ore man mano che vengono visualizzati nuovi contenuti. I punteggi degli intenti vengono ricalcolati una volta al giorno, in modo che il dashboard rifletta ogni mattina l’attività del giorno precedente.
