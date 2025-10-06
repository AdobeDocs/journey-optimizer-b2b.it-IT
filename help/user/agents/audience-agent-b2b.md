---
title: Audience Agent B2B
description: Audience Agent B2B in Percorsi OptimizerB2B Edition utilizza l’analisi intento e la mappatura persona per creare gruppi di acquisto e accelerare i flussi di lavoro di marketing B2B.
feature: Audiences, AI Assistant
role: User
source-git-commit: 7f1c1533c226a2626978ada221c7026bc3d1432b
workflow-type: tm+mt
source-wordcount: '417'
ht-degree: 0%

---

# Audience Agent B2B

Basato su [Adobe Experience Platform Agent Orchestrator](https://experienceleague.adobe.com/it/docs/experience-cloud-ai/experience-cloud-ai/agents/agent-orchestrator), Audience Agent B2B è disponibile in Journey Optimizer B2B edition. L’utilizzo di questo agente migliora l’efficienza e l’efficacia nell’esplorazione e nella scalabilità dei tipi di pubblico, velocizzando la creazione di gruppi di acquisto e flussi di lavoro fluidi per l’attivazione del percorso:

* **_Assegna la priorità ai tipi di pubblico di destinazione in base all&#39;intento_** - Assegna a più utenti tipo in base all&#39;intento del prodotto e semplifica la pianificazione delle campagne, riducendo il tempo impiegato per la convalida del pubblico.

* **_Sfrutta l&#39;intelligenza artificiale per rilevare i gruppi di acquisto_**. Utilizza l&#39;intelligenza artificiale, dati strutturati e non strutturati e dati unificati di prime parti per semplificare l&#39;individuazione e la creazione dei gruppi di acquisto.

![Audience Agent B2B in modalità a pagina intera](./assets/audience-agent-full.png){width="700" zoomable="yes"}

## Funzionalità di Audience Agent

| Area | Funzionamento | Valore aziendale |
| ---- | ------------ | -------------- |
| Analisi intento | <li> Misura l’intensità dell’intento del conto (ad esempio basso, medio e alto) per prodotti specifici. <li>Confronta le tendenze di interesse del prodotto nel tempo (ad esempio i prodotti più importanti negli ultimi _n_ giorni). <li>Identifica gli account che mostrano attivamente interesse per prodotti specifici. <li>Crea pattern di coinvolgimento che combinano l’attività dell’account con la copertura dell’utente. | <li>Aiuta i team a concentrarsi sugli account giusti al momento giusto. <li>Migliora la qualità della pipeline assegnando priorità agli account con segnali di acquisto autentici. <li>Consente un coinvolgimento proattivo prima che la concorrenza agisca. |
| Mappatura personale | <li>Rileva e classifica gli utenti tipo più importanti in base all’intento del prodotto. <li>Identifica gli utenti tipo coinvolti nell’acquisto di uno o più prodotti. <li>Mappare gli utenti tipo ai ruoli funzionali (Champion, Decision Maker, Influencer, ecc.) con giustificazione. <li>Convalida il motivo per cui una determinata persona è considerata un campione. | <li>Assicura che le vendite coinvolgano i veri decision-maker e i influencer. <li>Riduce lo spreco di risorse sui contatti a basso impatto. <li>Aumenta i tassi di vincita allineando l’estensione con le dinamiche del potere dell’acquirente. |
| Valutazione gruppo acquisti | <li>Valuta le dimensioni del gruppo di acquisto (ad esempio, gruppi con più di n membri). <li>Misura la copertura persona tra gli account (ad esempio, inferiore a x%). <li>Monitora la distribuzione dei ruoli e il gap di copertura all’interno dei gruppi di acquisto. <li>Evidenzia i clienti con i campioni identificati in recenti offerte. | <li>Mostra le lacune nella copertura che potrebbero bloccare le trattative. <li>Rafforza le strategie multithreading garantendo una rappresentazione completa dei ruoli. <li>Migliora il tracciamento dello stato delle opportunità di business tramite approfondimenti sul coinvolgimento a livello di gruppo. |

## Esempi di prompt

Questi esempi di prompt illustrano alcuni modi in cui è possibile utilizzare l&#39;agente:

* Mostra la finestra di tendenza: meno recente e più recente aggiornata per l’intento di prodotto dell’account per prodotto.
* Per `<product>`, elenca i gruppi di acquisto con finalità di prodotto e punteggi.
* Per `<product>`, elenca gli utenti tipo e i ruoli con le relative metriche opportunità (tasso di vincita, tasso di iscrizione, conteggi).
* Per gli account in `<industry>`, qual è la copertura media degli utenti tipo per l&#39;account per `<product>`?
* Quali account hanno un intento basso per qualsiasi prodotto ma hanno ancora opportunità aperte (vale la pena nutrirsi)?
* Quali account hanno aggiunto nuovi segnali di intento per `<account_name>` questa settimana?
