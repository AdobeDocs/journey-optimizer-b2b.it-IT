---
title: Audience Agent B2B
description: Audience Agent B2B in Journey Optimizer B2B edition utilizza l’analisi intento e la mappatura persona per creare gruppi di acquisto e accelerare i flussi di lavoro di marketing B2B.
feature: Agentic AI, Audiences
role: User
exl-id: c1210912-66ba-4b5f-8f3b-96eb6280c926
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: beb5f4be-cec3-471a-9db6-831a77dd3ac9
  - id: bef5003b-cad2-4f40-bdb2-a80426d52ef5
subfeature_v2:
  - id: ff10f619-348f-47e3-99bf-3ce4c817cf2c
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: bbbea26f-9621-49eb-9ab8-e06fb3bbce8c
autotag-review: '2026-04-29T23:21:59.633Z'
source-git-commit: 97417ae1fcb017d4fcb7128e3fc0b61c829f867e
workflow-type: tm+mt
source-wordcount: 2500
ht-degree: 1%

---

# Audience Agent B2B

Basato su [Adobe Experience Platform Agent Orchestrator](https://experienceleague.adobe.com/it/docs/experience-cloud-ai/experience-cloud-ai/agents/agent-orchestrator), Audience Agent B2B è disponibile in Journey Optimizer B2B edition. L’utilizzo di questo agente migliora l’efficienza e l’efficacia nell’esplorazione e nella scalabilità dei tipi di pubblico, velocizzando la creazione di gruppi di acquisto e flussi di lavoro fluidi per l’attivazione del percorso:

* **_Assegna la priorità ai tipi di pubblico target in base all&#39;intento_**: associa utenti tipo in base all&#39;intento del prodotto per vari tipi di pubblico e semplifica la pianificazione delle campagne, riducendo il tempo impiegato per la convalida del pubblico.

* **_Sfrutta l&#39;intelligenza artificiale per rilevare e creare gruppi di acquisto_**: utilizza l&#39;intelligenza artificiale, dati strutturati e non strutturati e dati unificati di prime parti per semplificare l&#39;individuazione e la creazione di gruppi di acquisto.

![Audience Agent B2B in modalità a pagina intera](./assets/audience-agent-full.png){width="700" zoomable="yes"}

>[!PREREQUISITES]
>
>Per utilizzare Audience Agent B2B, sono necessarie definizioni e mappature di dati:<br/>
>
>* [Tassonomia/mappatura dei dati intento](../admin/intent-data.md)
>* [Tassonomia/mappatura campi XDM](#xdm-data-prerequisites)

## Funzionalità B2B di Audience Agent

| Area | Funzionamento | Valore aziendale |
| ---- | ------------ | -------------- |
| Analisi intento | <li> Misura l’intensità dell’intento del conto (ad esempio basso, medio e alto) per prodotti specifici. <li>Confronta le tendenze di interesse del prodotto nel tempo (ad esempio i prodotti più importanti negli ultimi _n_ giorni). <li>Identifica gli account che mostrano attivamente interesse per prodotti specifici. <li>Crea pattern di coinvolgimento che combinano l’attività dell’account con la copertura dell’utente. | <li>Aiuta i team a concentrarsi sugli account giusti al momento giusto. <li>Migliora la qualità della pipeline assegnando priorità agli account con segnali di acquisto autentici. <li>Consente un coinvolgimento proattivo prima che la concorrenza agisca. |
| Mappatura utente tipo | <li>Rileva e classifica gli utenti tipo principali in base all’intento del prodotto. <li>Identifica gli utenti tipo coinvolti nell’acquisto di uno o più prodotti. <li>Associa gli utenti tipo a ruoli funzionali (ad esempio _Champion_, _Decision Maker_ e _Influencer_) con giustificazione. <li>Convalida il motivo per cui una determinata persona è considerata un campione. | <li>Assicura che il sales team coinvolga veri decision-maker e influencer. <li>Riduce lo spreco di risorse sui contatti a basso impatto. <li>Aumenta i tassi di vincita allineando l’estensione con le dinamiche del potere dell’acquirente. |
| Valutazione gruppo acquisti | <li>Valuta le dimensioni del gruppo di acquisto (ad esempio, gruppi con più di _n_ membri). <li>Misura la copertura dell&#39;utente tra gli account (ad esempio, inferiore a _x_%). <li>Monitora la distribuzione dei ruoli e il gap di copertura all’interno dei gruppi di acquisto. <li>Evidenzia i clienti con i campioni identificati in recenti offerte. | <li>Mostra le lacune nella copertura che potrebbero bloccare le trattative. <li>Rafforza le strategie multithreading garantendo una rappresentazione completa dei ruoli. <li>Migliora il tracciamento dello stato delle opportunità di business tramite approfondimenti sul coinvolgimento a livello di gruppo. |
| Creazione di gruppi di acquisto e attuabilità | <li>Consigliare mappature da ruolo a persona in base ai modelli di ruolo e persona osservati. <li>Genera un modello di ruolo gruppo di acquisto per un prodotto specificato. <li>Supporta la personalizzazione dei modelli includendo o escludendo utenti tipo e ruoli specifici. <li>Verifica che i ruoli richiesti siano definiti prima della creazione dei gruppi di acquisto. | <li>Riduce l&#39;impegno manuale e il rischio di modelli di gruppi di acquisto incompleti. <li>Garantisce la convalida della copertura dei ruoli prima della creazione, riducendo il rischio di lacune nella copertura. <li>Trasforma gli insight dell’analisi in passaggi operativi immediati. |

## Limitazioni

Audience Agent B2B dipende dalla tassonomia di intento configurata, dalle mappature dei campi XDM e dai dati dell’evento esperienza. Gli insights sono meno affidabili quando i dati dell’opportunità sono incompleti, la tassonomia intento è mancante o non aggiornata oppure gli identificatori di profilo e account richiesti non sono mappati. Per il calcolo dell&#39;intento, l&#39;agente elabora solo gli eventi di esperienza seguenti: `directMarketing.emailClicked`, `directMarketing.emailOpened`, `directMarketing.emailUnsubscribed` e `web.webpagedetails.pageViews`.

## Esempi di prompt

Questi esempi di prompt illustrano alcuni dei modi in cui è possibile utilizzare l&#39;agente:

* Mostra la finestra di tendenza: meno recente e più recente aggiornata per l’intento di prodotto dell’account per prodotto.
* Per `<product>`, elenca i gruppi di acquisto con finalità di prodotto e punteggi.
* Per `<product>`, elenca gli utenti tipo e i ruoli con le relative metriche opportunità (tasso di vincita, tasso di iscrizione, conteggi).
* Per gli account in `<industry>`, qual è la copertura media degli utenti tipo per l&#39;account per `<product>`?
* Quali account hanno un intento basso per qualsiasi prodotto ma hanno ancora opportunità aperte (vale la pena nutrirsi)?
* Quali account hanno aggiunto nuovi segnali di intento per `<account_name>` questa settimana?
* Mostra gli utenti tipo associati a `<product>`.
* Mostra il ruolo per il consiglio di mappatura persona per `<product>`.
* Creare un modello di gruppo di acquisto per `<product>`.
* Creare un modello di gruppo di acquisto per `<product>` senza l&#39;utente tipo `<persona>` e rimuovere il ruolo `<role>`.

## Concetti

| Concetto | Spiegazione |
| ------- | ----------- |
| Rilevamento del pubblico | Dietro le quinte, l’agente osserva i segnali di intenti di prima parte basati su due cose: il grado di coinvolgimento delle persone con il tuo marchio e i tipi di persone che rappresentano. L’analisi considera gli ultimi 18 mesi di attività per rilevare l’intento del prodotto per tutti gli utenti dell’account, in particolare durante il periodo precedente alla chiusura di un’opportunità. Questa analisi aiuta l&#39;agente a evidenziare gli utenti tipo che hanno più probabilità di influenzare l&#39;operazione.<br/><br/>A volte gli account non dispongono di tutti i dati sulle opportunità in una forma perfetta, il che è corretto e l&#39;agente può ancora rilevare l&#39;intento del prodotto puramente dai pattern di coinvolgimento. |
| Utente tipo | Gli utenti tipo rappresentano i tipi di persone coinvolti all’interno di un account. L&#39;agente le crea osservando la qualifica professionale, la funzione e il livello di anzianità e quindi normalizzando tali informazioni in modo che siano coerenti tra i diversi account. In questo modo, invece di perderti in titoli confusi, puoi vedere rapidamente se stai raggiungendo decisori, influencer o ruoli di supporto. Le persone ti aiutano a capire chi mostra interesse, non solo quanto interesse ci sia. |
| Mappatura dei ruoli del gruppo di acquisto | Dopo aver mappato gli utenti tipo ai ruoli, li riunisci in un gruppo di acquisto, il team completo all’interno dell’account che molto probabilmente influenzerà o deciderà sull’acquisto. Ogni ruolo (ad esempio _decision maker_, _influencer_ o _champion_) aggiunge una parte dell&#39;immagine in modo da avere una visione chiara del comitato che guida l&#39;offerta.<br/><br/>L&#39;agente associa ogni persona identificata al ruolo che è più probabile che svolga per un prodotto specifico, in base alla qualifica professionale, alla funzione, all&#39;anzianità e agli altri attributi configurati. Mostra inoltre la copertura per ogni ruolo, in modo da poter vedere quali ruoli sono ben rappresentati e dove rimangono le lacune nella strategia di coinvolgimento. |
| Utilizzo dei dati sulle opportunità per rilevare l’utente tipo | Per darti una visione più accurata di chi è coinvolto e di dove stanno i loro interessi, l&#39;agente si avvicina alla classificazione personale e all&#39;intento del prodotto in base a quanto segue: <ul><li>Scenario del migliore dei casi: se puoi fornire dati come _Fase opportunità_, _Data chiusura opportunità_ e una chiara _Mappatura opportunità-prodotto_, l&#39;agente può classificare gli utenti tipo per prodotto.<li>Questa classificazione fornisce una comprensione precisa del coinvolgimento e degli interessi in tutto l’account. </ul>Ma l&#39;agente sa che i dati non sono sempre completi, il che va bene. Include i fallback intelligenti per mantenere le cose in movimento:<ul><li>L’agente analizza il volume delle attività, dando più peso a quelle recenti utilizzando il decadimento nel tempo.<li>Questa ponderazione consente all’agente di differenziare e classificare gli utenti tipo, anche senza dati completi sulle opportunità. </ul>Quando si tratta di collegare opportunità ai prodotti, ecco come l&#39;agente la gestisce:<ul><li>_Ideale_: fornire o aiutare l&#39;agente a creare la tabella di mapping.<li>_Se non disponibile_: l&#39;agente utilizza una corrispondenza fuzzy per connettere i punti.<li>_Nessun collegamento_: l&#39;agente deduce l&#39;intento del prodotto in base alle attività recenti precedenti alla data di chiusura.</ul>Questo approccio su più livelli garantisce che l’agente possa fornire informazioni significative, anche quando i dati non sono perfetti. |
| Analisi dell’opportunità | L’agente esamina i dati storici sulle opportunità per capire quali fattori prevedono più fortemente una vittoria, e a tal fine utilizza tre dimensioni principali:<ol><li>Tasso di successo: mostra con quale frequenza le offerte vengono chiuse correttamente quando sono coinvolti determinati utenti tipo. Se gli account con un pattern personale specifico (come un valutatore tecnico o un decision maker a livello di VP) tendono a convertirsi più spesso, il modello dà maggiore peso a tale pattern. Queste informazioni rappresentano una percentuale delle opportunità totali, ad esempio opportunità chiuse o realizzate.<li>Tasso di iscrizione: misura la frequenza con cui un tipo di utente viene visualizzato nelle opportunità per un determinato prodotto. Se alcuni utenti appaiono costantemente in offerte di successo, indica che svolgono un ruolo fondamentale nel processo di acquisto.<li>Influenza personale: quantifica il contributo di una determinata persona al risultato, non solo se è presente, ma anche il modo in cui il suo livello di coinvolgimento o attività è correlato alle vittorie.</ol>Insieme, questi segnali consentono di dedurre quali utenti tipo hanno l’impatto più forte sui risultati di acquisto, anche quando i dati sulle opportunità sono incompleti. Nel tempo, consente al sistema di individuare utenti tipo e pattern di alto impatto più predittivi del successo dell’offerta, che informano le finalità dell’account, la mappatura dell’utente e i consigli del gruppo di acquisto. |
| Intento | Quando qualcuno visita una pagina web o fa clic su un collegamento e-mail relativo a un prodotto, ciò indica che è interessato e si chiama _intento_.<br/><br/>L&#39;agente inizia con una tassonomia, che consiste essenzialmente in un elenco dei prodotti del cliente e delle parole chiave che li descrivono. Queste informazioni aiutano l&#39;agente a capire di cosa si tratta ogni contenuto o interazione.<br/><br/>L&#39;agente utilizza quindi tale tassonomia per etichettare l&#39;attività del visitatore, ad esempio a quali parole chiave o prodotti si riferiscono le loro azioni.<br/><br/>L&#39;agente esamina quindi il livello di coinvolgimento degli utenti, ad esempio quante pagine visitano o con quale frequenza interagiscono. Utilizza queste informazioni per calcolare il punteggio di intento individuale per parole chiave, prodotti o categorie di prodotti specifici. Inserisce ogni punteggio intento in _Alto_, _Medium_ o _Basso_ intento per indicare la forza di interesse. (Intento basso: `<=0.2`, Intento Medium: `0.2 < score <= 0.6`, Intento alto: `0.6 < score <= 1`)<br/><br/>Infine, l&#39;agente combina i punteggi di intento di tutte le persone della stessa società (account) per visualizzare l&#39;intento complessivo a livello di account, mostrando i prodotti o gli argomenti a cui l&#39;azienda sembra più interessata. |
| Ruoli che influenzano un gruppo di acquisto | Ogni gruppo di acquisto è composto da ruoli che contribuiscono in modo diverso alla decisione di acquisto, ad esempio _Decision Maker_, _Influencer_, _Champion_ e _End User_. Ogni ruolo ha un diverso grado di impatto.<br/><br/>I decision maker hanno la maggiore influenza e in genere controllano le approvazioni del budget. Influenzatori - Valutazione della forma e consigli. I promotori contribuiscono a creare un consenso interno, mentre gli utenti finali convalidano la conformità del prodotto.<br/><br/>Mostrandoti questi ruoli, l&#39;agente ti aiuta a capire chi sta guidando la decisione di acquisto, dove il tuo coinvolgimento è più forte e dove potrebbero esistere vuoti di copertura. Queste informazioni consentono di concentrarsi sui ruoli più importanti per questo prodotto. |
| Copertura di persone o ruoli | Per un determinato prodotto, esiste in genere un insieme di ruoli chiave e utenti tipo noti per influenzare l&#39;acquisto (_N_ utenti tipo o ruoli).<br/><br/>Per ogni account, l&#39;agente calcola la copertura controllando quanti di questi _N_ ruoli sono rappresentati da almeno una persona all&#39;interno dell&#39;account.<br/><br/>Se sono presenti tutti i _N_ ruoli, l&#39;account dispone di copertura completa. Se sono rappresentati solo alcuni ruoli, la copertura è parziale.<br/><br/>In termini semplici, il ruolo e la copertura dell&#39;utente misurano la completezza del gruppo di acquisto per un prodotto, in base all&#39;inclusione o meno di tutti i decisori, influencer e campioni importanti. |

## Prerequisiti per i dati XDM

Audience Agent fornisce informazioni approfondite sugli account che mostrano l’intento di prime parti per i prodotti e calcola gli utenti tipo e i ruoli in base ai dati definiti. Assicurati che i seguenti dati prerequisiti siano configurati per utilizzare le funzionalità di Audience Agent:

### Mappatura campo XDM

<table>
  <tbody>
    <tr>
      <th>Campo XDM</th>
      <th>Entità</th>
      <th>Definizione di business</th>
      <th>Dettagli aggiuntivi</th>
    </tr>
    <tr>
      <td>
        <p>
          <span>b2b.accountKey.sourceKey</span>
        </p>
      </td>
      <td>
        <p>
          <span>Profili</span>
        </p>
      </td>
      <td>Identificatore account, utilizzato nei join dei dati relativi a opportunità, evento e intento</td>
      <td rowspan="2">Analisi opportunità<br/>Esplorazione account<br/>
        <br/>
      </td>
    </tr>
    <tr>
      <td>
        <p>
          <span>b2b.personKey.sourceKey</span>
        </p>
      </td>
      <td>
        <p>
          <span>Profili</span>
        </p>
      </td>
      <td>Identificatore della persona, utilizzato nei join che coinvolgono i dati evento ai dati profilo</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>extendedWorkDetails.departments</span>
        </p>
      </td>
      <td>
        <p>
          <span> profili</span>
        </p>
      </td>
      <td>Reparto del profilo/persona</td>
      <td rowspan="5">
        <p>
          <br/>
        </p>
        <p>Mappatura personale</p>
      </td>
    </tr>
    <tr class="">
      <td>
        <p>
          <span>extendedWorkDetails.jobTitle</span>
        </p>
      </td>
      <td>
        <p>
          <span> profili</span>
        </p>
      </td>
      <td>Qualifica del profilo/persona utilizzato nel calcolo dell’utente tipo</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>nome.nome.nomeNome</span>
        </p>
      </td>
      <td>
        <p>
          <span >Profili</span>
        </p>
      </td>
      <td>Nome della persona, utilizzato da Audience Agent per visualizzare i nomi nell’interfaccia utente quando vengono soddisfatti i criteri</td>
    </tr>
    <tr class="">
      <td>
        <p>
          <span>nome.nome.nomeCompleto</span>
        </p>
      </td>
      <td>
        <p>
          <span> profili</span>
        </p>
      </td>
      <td>Nome completo della persona, utilizzato da Audience Agent per visualizzare i nomi nell’interfaccia utente quando vengono soddisfatti i criteri</td>
    </tr>
    <tr class="">
      <td>
        <p>
          <span>nome.cognome</span>
        </p>
      </td>
      <td>
        <p>
          <span> profili</span>
        </p>
      </td>
      <td>Cognome della persona, utilizzato da Audience Agent per visualizzare i nomi nell’interfaccia utente quando vengono soddisfatti i criteri</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>accountKey.sourceKey</span>
        </p>
      </td>
      <td>
        <p>
          <span> account</span>
        </p>
      </td>
      <td>Identificatore account, utilizzato nei join dei dati relativi a opportunità, evento e intento</td>
      <td>Analisi opportunità<br/>Esplorazione account</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>nomeAccount</span>
        </p>
      </td>
      <td>
        <p>
          <span>Account</span>
        </p>
      </td>
      <td>Nome dell’account utilizzato da Audience Agent da visualizzare nell’interfaccia utente quando vengono soddisfatti i criteri indicati nella query utente</td>
      <td rowspan="4">
        <p>
          <br/>
        </p>
        <p>
          <br/>
        </p>
        <p>
          <br/>
        </p>
        <p>Esplorazione account</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>
          <span>accountDescription</span>
        </p>
      </td>
      <td>
        <p>
          <span>Account</span>
        </p>
      </td>
      <td>Descrizione dell’account/azienda utilizzato da Audience Agent per applicare il filtro agli account in base alla query dell’utente nell’interfaccia utente </td>
    </tr>
    <tr>
      <td>
        <p>
          <span>accountOrganization.industry</span>
        </p>
      </td>
      <td>
        <p>
          <span> account</span>
        </p>
      </td>
      <td>Settore di account/azienda utilizzato da Audience Agent per applicare il filtro agli account in base alle query degli utenti nell’interfaccia utente </td>
    </tr>
    <tr>
      <td>
        <p>
          <span>accountBillingAddress.region</span>
        </p>
      </td>
      <td>
        <p>
          <span> account</span>
        </p>
      </td>
      <td>Indirizzo di fatturazione dell’account/azienda utilizzato da Audience Agent per applicare il filtro sugli account in base alla query dell’utente nell’interfaccia utente </td>
    </tr>
    <tr>
      <td>
        <p>
          <span>accountKey.sourceKey</span>
        </p>
      </td>
      <td>
        <p>
          <span>Opportunità</span>
        </p>
      </td>
      <td>Identificatore account, utilizzato nei join dei dati relativi a opportunità, evento e intento</td>
      <td rowspan="2">
        <p>Analisi opportunità<br/>Esplorazione account</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>
          <span>optionKey.sourceKey</span>
        </p>
      </td>
      <td>
        <p>
          <span>Opportunità</span>
        </p>
      </td>
      <td>Identificatore dell’opportunità, utilizzato nei join per i dati dell’account</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>NomeOpportunità</span>
        </p>
      </td>
      <td>
        <p>
          <span> opportunità</span>
        </p>
      </td>
      <td>Nome dell’opportunità utilizzata da Audience Agent </td>
      <td rowspan="5">
        <p>
          <br/>
        </p>
        <p>
          <br/>
        </p>
        <p>
          <br/>
        </p>
        <p>
          <br/>
        </p>
        <p>
          <br/>
        </p>
        <p>Analisi dell’opportunità</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>
          <span>isWon</span>
        </p>
      </td>
      <td>
        <p>
          <span>Opportunità</span>
        </p>
      </td>
      <td>Se l’opportunità è vinta (binario)</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>descrizione opportunità</span>
        </p>
      </td>
      <td>
        <p>
          <span>Opportunità</span>
        </p>
      </td>
      <td>Descrizione dell’opportunità utilizzata da Audience Agent </td>
    </tr>
    <tr>
      <td>
        <p>
          <span>importo opportunità</span>
        </p>
      </td>
      <td>
        <p>
          <span>Opportunità</span>
        </p>
      </td>
      <td>Importo di $ coinvolto nell’opportunità</td>
    </tr>
    <tr class="">
      <td>
        <p>
          <span>tipoOpportunità</span>
        </p>
      </td>
      <td>
        <p>
          <span>Opportunità</span>
        </p>
      </td>
      <td>Tipo di opportunità</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>faseOpportunità</span>
        </p>
      </td>
      <td>
        <p>
          <span> opportunità</span>
        </p>
      </td>
      <td>Fase dell’opportunità (vinta chiusa o persa chiusa o qualsiasi fase intermedia) </td>
      <td rowspan="4">
        <p>Analisi opportunità<br/>Esplorazione account</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>
          <span>actualCloseDate</span>
        </p>
      </td>
      <td>
        <p>
          <span>Opportunità</span>
        </p>
      </td>
      <td>Data effettiva di chiusura dell’opportunità</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>expectedCloseDate</span>
        </p>
      </td>
      <td>
        <p>
          <span> opportunità</span>
        </p>
      </td>
      <td>Data di chiusura prevista dell’opportunità</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>extSourceSystemAudit.createdDate</span>
        </p>
      </td>
      <td>
        <p>
          <span>Opportunità</span>
        </p>
      </td>
      <td>Data di creazione per questa opportunità</td>
    </tr>
  </tbody>
</table>

### Dati di tassonomia

Audience Agent sfrutta l’intento di prime parti rilevato in Journey Optimizer B2B edition:

1. Il calcolo dell&#39;intento richiede i dati della tassonomia (prodotti del cliente e parole chiave corrispondenti) da Clienti > Tassonomia
1. I dati di tassonomia vengono utilizzati per etichettare i dati evento (etichettatura delle risorse). Questi dati forniscono informazioni approfondite sulle parole chiave e i prodotti a cui i visitatori sono interessati in base ai loro dati evento > Etichettatura risorse 
1. Le risorse con etichetta (dati evento) vengono combinate con i comportamenti dei visitatori (numero di pagine visitate) per determinare l’intento di un visitatore a livello di parola chiave, prodotto e categoria di prodotto → calcolo dell’intento
1. I punteggi di intento a livello di profilo visitatore vengono aggregati a livello di account per determinare l’intento dell’account in una determinata parola chiave, prodotto e categoria di prodotto > Aggregazione account intento

I campi seguenti sono obbligatori oltre a [configurare la tassonomia intento](../admin/intent-data.md):

<table>
  <tbody>
    <tr>
      <th>Campo XDM</th>
      <th>Entità</th>
      <th>Definizione di business</th>
    </tr>
    <tr>
      <th>
        <br/>
      </th>
      <th>
        <br/>
      </th>
      <td>profilo della persona</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>_acp_system_metadata.primaryIdentity.namespace.code<br/>
          </span>
        </p>
      </td>
      <td>
        <p>
          <span>Profilo</span>
        </p>
      </td>
      <td>Consente di identificare un identificatore di persona (e-mail o b2b_person)</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>_acp_system_metadata.primaryIdentity.id
          </span>
        </p>
      </td>
      <td>
        <p>
          <span>Profilo</span>
        </p>
      </td>
      <td>namespace_id</td>
    </tr>
    <tr>
      <td>
        <ul>
          <li>keyword_id</li>
          <li>keyword_name</li>
          <li>product_id</li>
          <li>product_name</li>
          <li>product_category_id</li>
          <li>product_category_name</li>
        </ul>
      </td>
      <td>
        <p>
          <br/>
        </p>
      </td>
      <td>Utilizzato come tassonomia per etichettare le risorse (eventi di esperienza, come e-mail su cui è stato fatto clic, pagine web visitate)</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>timestamp</span>
        </p>
      </td>
      <td>
        <p>
          <span>Evento esperienza</span>
        </p>
      </td>
      <td>Utilizzato per il tempo necessario per ottenere la retrocompilazione e l’esecuzione incrementale</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>eventType</span>
        </p>
      </td>
      <td>
        <p>
          <span>Evento esperienza</span>
        </p>
      </td>
      <td>Ottieni il tipo di evento poiché l'agente elabora solo quattro eventi (<span>directMarketing.emailClicked, directMarketing.emailOpened, directMarketing.emailUnsubscscribe, web.webpagedetails.pageViews)</span>
      </td>
    </tr>
    <tr>
      <td>
        <p>
          <span>directMarketing.mailingName</span>
        </p>
      </td>
      <td>
        <p>
          <span>Evento esperienza</span>
        </p>
      </td>
      <td>Solo per riferimento/contabilità; informazioni sul nome della campagna</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>directMarketing.mailingKey.sourceID</span>
        </p>
      </td>
      <td>
        <p>
          <span>Evento esperienza</span>
        </p>
      </td>
      <td>Solo per riferimento/contabilità; informazioni sull’ID sorgente per il quale è indirizzata l’e-mail</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>directMarketing.mailingKey.sourceInstanceID<br/>
          </span>
        </p>
      </td>
      <td>
        <p>
          <span>Evento esperienza</span>
        </p>
      </td>
      <td>Solo per riferimento/contabilità: informazioni sull’istanza di origine per la quale è destinata l’e-mail</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>directMarketing.mailingKey.sourceKey<br/>
          </span>
        </p>
      </td>
      <td>
        <p>
          <span>Evento esperienza</span>
        </p>
      </td>
      <td>Utilizzato per recuperare il contenuto delle e-mail dal data center di Marketo Engage; è composto da (SourceID@SourceInstanceID.SourceType)</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>directMarketing.mailingKey.sourceType<br/>
          </span>
        </p>
      </td>
      <td>
        <p>
          <span>Evento esperienza</span>
        </p>
      </td>
      <td>Solo per riferimento/contabilità; informazioni sul tipo di sorgente o da dove ha avuto origine la sorgente </td>
    </tr>
    <tr>
      <td>
        <p>
          <span>web.webPageDetails<br/>
          </span>
        </p>
      </td>
      <td>
        <p>
          <span>Evento esperienza</span>
        </p>
      </td>
      <td>Informazioni sull’origine della visita della pagina web</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>web.webPageDetails.name<br/>
          </span>
        </p>
      </td>
      <td>
        <p>
          <span>Evento esperienza</span>
        </p>
      </td>
      <td>URL effettivo utilizzato per ottenere il contenuto</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>web.webPageDetails.queryParameters</span>
        </p>
      </td>
      <td>
        <p>
          <span>Evento esperienza</span>
        </p>
      </td>
      <td>Parametro di query aggiuntivo per l’URL utilizzato per recuperare il contenuto di destinazione </td>
    </tr>
    <tr>
      <td>
        <p>
          <span>web.webPageDetails.isPersonalizedURL</span>
        </p>
      </td>
      <td>
        <p>
          <span>Evento esperienza</span>
        </p>
      </td>
      <td>Solo per riferimento/contabilità</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>web.webPageDetails.webPageKey.sourceID<br/>
          </span>
        </p>
      </td>
      <td>
        <p>
          <span>Evento esperienza</span>
        </p>
      </td>
      <td>Solo per riferimento/contabilità; informazioni sull’ID sorgente per il quale è indirizzata l’e-mail</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>web.webPageDetails.webPageKey.sourceInstanceID<br/>
          </span>
        </p>
      </td>
      <td>
        <p>
          <span>Evento esperienza</span>
        </p>
      </td>
      <td>Solo per riferimento/contabilità; informazioni sull’istanza di origine per la quale è stato eseguito il targeting dell’e-mail</td>
    </tr>
    <tr class="">
      <td>
        <p>
          <span>web.webPageDetails.webPageKey.sourceKey<br/>
          </span>
        </p>
      </td>
      <td>
        <span>Evento esperienza</span>
      </td>
      <td>Solo per riferimento/contabilità; è composto da (SourceID@SourceInstanceID.SourceType)</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>web.webPageDetails.webPageKey.sourceType</span>
        </p>
      </td>
      <td>
        <span>Evento esperienza</span>
      </td>
      <td>Solo a fini di riferimento/contabilità; informazioni relative al tipo di fonte o alla provenienza</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>web.webPageDetails.webPageKey.URL</span>
        </p>
      </td>
      <td>
        <span>Evento esperienza</span>
      </td>
      <td>Utilizzato per recuperare l’URL effettivo se web.webPageDetails.name non lo contiene.</td>
    </tr>
  </tbody>
</table>
