---
title: Decisioning IA
description: Comprendi le decisioni basate sull’intelligenza artificiale in Journey Optimizer B2B Prime, il livello di intelligence dietro il controllo del traffico del percorso, il percorso migliore successivo, l’ottimizzazione dell’ora di invio e altre funzionalità che sostituiscono le regole statiche con l’automazione basata sui risultati.
autotag-review: '2026-07-23T00:13:49.629Z'
TQID: 'https://experienceleague.adobe.com/vAu9C6Erjr-0TIJ18jQnR209Ed2xfLl9P3Nq2fPTs9c'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: a4b836d9-ffdd-4df3-a62a-f78b830cf059id: aed878b8-11d0-487c-828b-d23b2051ec37id: bef5003b-cad2-4f40-bdb2-a80426d52ef5
subfeature_v2: id: d270a788-eb1d-40ed-b74e-9158ed975b1fid: c3d6e661-d372-4e98-9fd9-eac771e7e4eeid: ff10f619-348f-47e3-99bf-3ce4c817cf2c
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 120afb1109e550fc65c2fc5a01680f2d7d2e2345
workflow-type: tm+mt
source-wordcount: 814
ht-degree: 2%

---


# Decisioning IA

Le decisioni basate sull’intelligenza artificiale sono il livello di intelligence che sta dietro a Adobe Journey Optimizer B2B Prime. Invece di pre-creare ogni ramo come regola statica, le decisioni basate sull’intelligenza artificiale valutano continuamente il contesto di un profilo, tra cui l’iscrizione al percorso, la cronologia del coinvolgimento, i punteggi di intento e il comportamento in tempo reale, per determinare l’azione o il percorso migliore successivo per quella persona.

Questa valutazione continua sposta l’orchestrazione da regole statiche verso un’automazione basata sui risultati: anziché definire in anticipo ogni condizione, descrivi il risultato desiderato e il sistema determina come raggiungerlo per ogni persona.

## Funzionalità {#capabilities}

Le decisioni di IA sono composte dalle seguenti funzionalità:

| Funzionalità | Cosa decide |
|---|---|
| [Controllo del traffico di Percorso](../marketing/journey-traffic-control.md) | In quale percorso una persona dovrebbe essere in questo momento. Quando una persona è idonea per più di un percorso, il controllo del traffico di percorso effettua un nuovo indirizzamento nel momento in cui il profilo o il comportamento cambia, anziché lasciarla su un percorso non più adatto. |
| [Percorso migliore successivo](../marketing/next-best-path.md) | Il percorso più adatto per una persona all’interno di un percorso. Invece delle condizioni di filtro hardcoding, descrivi l’intento nel linguaggio naturale, e il sistema indirizza ogni persona al percorso migliore al momento giusto. |
| [Ottimizzazione del tempo di invio](../marketing/email-send-time-optimization.md) | La finestra di invio migliore per ogni destinatario, in base al coinvolgimento storico, anziché una pianificazione fissa per tutti. |
| Contenuto contestuale | Varianti e-mail personalizzate generate automaticamente da una descrizione del contenuto, da utilizzare come singola risorsa e-mail personalizzata in pochi percorsi. _Disponibile a breve._ |
| [Brand Concierge](https://experienceleague.adobe.com/it/docs/brand-concierge/content/home){target="_blank"} | Indirizzamento e risposta conversazionali in tempo reale, ad esempio chat e assistenza in tempo reale. Brand Concierge richiede prodotti aggiuntivi. |

Alcune di queste funzionalità risolvono diversi problemi all’interno dello stesso percorso. Il controllo del traffico di percorso determina quale percorso ottiene la priorità quando più percorsi sono in competizione per coinvolgere la stessa persona contemporaneamente. Le altre funzionalità decidono cosa accade dopo che una persona è già in un percorso.

## Percorsi suddivisi e percorso migliore successivo {#split-paths-next-best-path}

[Percorsi suddivisi](../marketing/split-merge-paths-nodes.md) ti consentono di definire rami di percorso con condizioni di filtro esplicite: se un punteggio è superiore a una soglia, invia una persona in basso di un percorso, altrimenti invia un&#39;altra. Questa logica basata su regole è precisa e completamente controllabile, ma ogni nuova condizione richiede un nuovo ramo.

Il nodo [Percorso migliore successivo](../marketing/next-best-path.md) applica le decisioni di IA allo stesso problema. Invece di una soglia fissa, il modello valuta il coinvolgimento, l’utente tipo, l’interesse del prodotto e la fase di funnel insieme, prevede il risultato migliore per ogni persona e seleziona automaticamente il percorso ottimale.

## Input dati {#data-inputs}

Le decisioni basate sull’intelligenza artificiale si basano sulle seguenti categorie di dati:

| Categoria | Esempi |
|---|---|
| Demografico e firmografico | Qualifica, settore e dimensione società |
| Psicografico | Punteggio lead, urgenza e priorità |
| Coinvolgimento | Punteggio, livello, tendenza, ultima attività e canale |
| Intento | Intento di prodotto o parola chiave, raggruppato in contenitori alti, medi o bassi |
| Utente tipo | Ruolo nell’offerta, nella qualifica professionale e nella persona |

## Cadenza di valutazione {#evaluation-cadence}

Le decisioni basate su IA utilizzano due diversi programmi di valutazione. Il profilo sottostante di una persona viene ricalcolato in un batch notturno. La decisione stessa viene applicata in tempo reale a ogni interazione, utilizzando qualsiasi profilo notturno indichi. Quindi la parte continua del processo decisionale basato sull’intelligenza artificiale descrive il momento decisionale, non la frequenza di aggiornamento del profilo.

## Guardrail e regole {#guardrails-rules}

Le regole coprono solo le condizioni che qualcuno ha esplicitamente annotato. Quando la realtà cade al di fuori di quell&#39;albero, come un personaggio ibrido o una combinazione di segnali che nessuno aveva previsto, le regole non fanno nulla finché qualcuno non aggiunge un nuovo ramo. Il decisioning basato sull’intelligenza artificiale classifica ogni persona in modo continuo e restituisce un’azione migliore basata sull’affidabilità, in modo da gestire combinazioni per le quali non è stato esplicitamente programmato alcun risultato, e migliora man mano che si ottengono più risultati, cosa che una regola non fa mai.

Le regole sono spiegabili e immediate per l’auditing, mentre le decisioni basate sull’intelligenza artificiale sono basate su un punteggio di affidabilità anziché su un fattore deterministico. Per questo motivo, le regole rimangono lo strumento migliore quando:

* Non è mai necessario superare un limite di conformità rigido, ad esempio la soppressione dei contatti che hanno rinunciato.
* Volume o cronologia insufficienti per consentire a un modello di imparare da.
* Ogni decisione deve essere pienamente spiegabile su richiesta.

Le configurazioni più mature vengono eseguite insieme: regole come guardrail e decisioning di IA che gestiscono tutto nel mezzo.

## Vantaggi {#benefits}

* Meno complessità di percorso manuale, con meno rami di regole da mantenere.
* Esperienze più rilevanti senza la creazione di centinaia di regole.
* Maggiore efficienza delle qualifiche.
* Identificazione più rapida del miglior coinvolgimento successivo per ciascun profilo.

>[!BEGINSHADEBOX]

**Ambito futuro: contesto dell&#39;account e del gruppo di acquisto**

Non disponibile oggi in Journey Optimizer B2B Prime. Le decisioni basate sull’intelligenza artificiale sono pianificate per estendersi oltre il profilo individuale a:

* Contesto dell’account: segnali a livello di società e di account come input decisionale.
* Segnali del gruppo di acquisto: ruolo nell’affare, status di decision-maker o professionista e coinvolgimento aggregato in tutti coloro che sono coinvolti in una decisione di acquisto.
* Orchestrazione del percorso a livello di account: le decisioni su indirizzamento e contenuti prese per l’account o il gruppo di acquisto come unità, con il controllo del traffico di percorso coordinato tra le diverse persone coinvolte.

>[!ENDSHADEBOX]
