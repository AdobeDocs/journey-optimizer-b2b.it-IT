---
title: Abilità dell’Assistente AI
description: 'Esaminare le competenze di AI Assistant in Journey Optimizer B2B Prime: flussi di lavoro combinati per programmi, percorsi, tipi di pubblico, punteggio, contenuti e ottimizzazione del tempo di invio.'
badgeBeta: label="Beta" type="informative" tooltip="Questa funzione è attualmente in versione beta limitata"
autotag-review: '2026-06-24T23:55:36.649Z'
TQID: 'https://experienceleague.adobe.com/iIi07OBWKxxa-oW-A6VrlkoTS02kmCx8kfMaCe-C-4o'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: bef5003b-cad2-4f40-bdb2-a80426d52ef5id: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2: id: ff10f619-348f-47e3-99bf-3ce4c817cf2cid: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 9433a1e86767e4504cb238ba8f3fae6e5c098a86
workflow-type: tm+mt
source-wordcount: 565
ht-degree: 6%

---

# Competenze dell’assistente AI

Un _skill_ è un flusso di lavoro integrato che l&#39;agente è in grado di eseguire, ovvero i blocchi predefiniti del menu `/` e le richieste in linguaggio naturale. Ogni abilità riunisce istruzioni dettagliate e gli strumenti specifici necessari per un lavoro (ad esempio, &quot;pubblicare un percorso&quot;, &quot;confrontare elenchi di due persone&quot;, &quot;creare un modello di punteggio&quot;).

>[!NOTE]
>
>Ogni abilità viene classificata a seconda che muti lo stato [!DNL Journey Optimizer B2B Prime] o [!DNL Marketo Engage] (**Scrivi**), solo le query/analisi/genera (**Leggi**) o ha funzioni di query + mutazione (**Leggi+Scrivi**).

## Programmi e pianificazione {#programs-planning}

| Abilità | Funzionamento | Accesso | Superficie del prodotto | Impatto/flusso di dati |
|---|---|---|---|---|
| `falco-program-creation` | Creazione del programma [!DNL Journey Optimizer B2B Prime] end-to-end: programma, sottocartelle, token, elenchi, percorsi. | Scrittura | [!DNL Journey Optimizer B2B Prime] | Legge e scrive [!DNL Journey Optimizer B2B Prime] |
| `adapt-program` | Genera storie di migrazione da [!DNL Marketo Engage] programmi per l&#39;adattamento [!DNL Journey Optimizer B2B Prime]. | Lettura | [!DNL Journey Optimizer B2B Prime] | Legge [!DNL Marketo Engage], scrive [!DNL Journey Optimizer B2B Prime] |
| `folder-creation` | Crea cartelle organizzative nella struttura ad albero delle risorse. | Scrittura | [!DNL Journey Optimizer B2B Prime] | Legge e scrive [!DNL Journey Optimizer B2B Prime] |
| `program-creation` *(Programmi di compilazione)* | Crea programmi Marketo da una descrizione della campagna. | Scrittura | [!DNL Marketo Engage] | Legge e scrive [!DNL Marketo Engage] |
| `program-planning` *(Pianificare Campagne)* | Trasforma i resoconti in documenti di configurazione/implementazione. | Lettura | [!DNL Marketo Engage] | Legge [!DNL Marketo Engage] |
| `program-qa` *(Convalida Programmi)* | Convalidare/controllare i programmi (solo regole, piano di test o descrizione). | Lettura | [!DNL Marketo Engage] | Legge [!DNL Marketo Engage] |

## Percorsi {#journeys}

| Abilità | Funzionamento | Accesso | Prodotto | Back-end (flusso di dati) |
|---|---|---|---|---|
| `journey-creation` | Creazione e modifica di percorsi di persone dal linguaggio naturale. | Scrittura | [!DNL Journey Optimizer B2B Prime] | Legge e scrive [!DNL Journey Optimizer B2B Prime] |
| `journey-edit-dates` | Modifica la data di inizio/fine di un percorso senza pubblicazione. | Scrittura | [!DNL Journey Optimizer B2B Prime] | Legge e scrive [!DNL Journey Optimizer B2B Prime] |
| `journey-publish` | Pubblicare/avviare/pianificare percorsi di persone. | Scrittura | [!DNL Journey Optimizer B2B Prime] | Legge e scrive [!DNL Journey Optimizer B2B Prime] |
| `journey-stop` | Interrompi, chiudi, interrompi, interrompi o uccidi percorsi. | Scrittura | [!DNL Journey Optimizer B2B Prime] | Legge e scrive [!DNL Journey Optimizer B2B Prime] |
| `journey-reentry` | Configura reinserimento: consenti/non consentiti, arresto del sistema, numero massimo di voci. | Scrittura | [!DNL Journey Optimizer B2B Prime] | Legge e scrive [!DNL Journey Optimizer B2B Prime] |
| `journey-trafficcontrol` | Esegui una simulazione di controllo del traffico che mostra l’instradamento del profilo. | Lettura | [!DNL Journey Optimizer B2B Prime] | Legge [!DNL Journey Optimizer B2B Prime] (simulazione) |
| `journey-observability` | Avanzamento debug/monitoraggio: percorsi, tempistica, divisioni, blocchi, permanenza. | Lettura | [!DNL Journey Optimizer B2B Prime] | Legge [!DNL Journey Optimizer B2B Prime] + [!DNL Marketo Engage] (controllo elenco statico) |

## Pubblico e persone {#audiences-people}

| Abilità | Funzionamento | Accesso | Prodotto | Back-end (flusso di dati) |
|---|---|---|---|---|
| `audience-creation` | Adattare uno smartlist [!DNL Marketo Engage], creare un elenco di persone o aggiungere/aggiornare regole. | Scrittura | [!DNL Journey Optimizer B2B Prime] | Legge [!DNL Marketo Engage] + legge/scrive [!DNL Journey Optimizer B2B Prime] |
| `people-list-comparison` | Confrontare gli elenchi di due persone e visualizzare i membri sovrapposti. | Lettura | [!DNL Journey Optimizer B2B Prime] | Legge [!DNL Journey Optimizer B2B Prime] |
| `import-leads` | Controllare la qualità dei dati CSV e confermare le importazioni in [!DNL Marketo Engage]. | Lettura e scrittura | Entrambi | Legge e scrive [!DNL Marketo Engage] |
| `lead-investigation` *(Indagare sui lead)* | Analizzare l’attività, il punteggio, la qualifica e il ciclo di vita di un lead. | Lettura | [!DNL Marketo Engage] | Legge [!DNL Marketo Engage] |

## Contenuto e canali {#content-channels}

| Abilità | Funzionamento | Accesso | Prodotto | Back-end (flusso di dati) |
|---|---|---|---|---|
| `content-personalization` | Sfoglia/visualizza in anteprima i modelli e modifica il contenuto/genera varianti. | Lettura e scrittura | [!DNL Journey Optimizer B2B Prime] | Legge e scrive [!DNL Journey Optimizer B2B Prime] |
| `asset-tokens` | CRUD del token completo su programmi/cartelle/percorsi. | Lettura e scrittura | [!DNL Journey Optimizer B2B Prime] | Legge e scrive [!DNL Journey Optimizer B2B Prime] |
| `fcs-channels` | Ricerche per canale e CRUD + pubblicazione/interruzione/eliminazione. | Lettura e scrittura | [!DNL Journey Optimizer B2B Prime] | Legge e scrive [!DNL Journey Optimizer B2B Prime] |

## Punteggio e segnali {#scoring-signals}

| Abilità | Funzionamento | Accesso | Prodotto | Back-end (flusso di dati) |
|---|---|---|---|---|
| `scoring-studio` | Elencare/ottenere modelli di punteggio e generarli/pubblicarli. | Lettura e scrittura | [!DNL Journey Optimizer B2B Prime] | Legge e scrive [!DNL Journey Optimizer B2B Prime] (servizio di punteggio); legge [!DNL Marketo Engage] campi/tipi di attività lead |
| `engagementconfiguration` | Mostra la configurazione del coinvolgimento e modifica/aggiorna i pesi. | Lettura e scrittura | [!DNL Journey Optimizer B2B Prime] | Legge e scrive [!DNL Journey Optimizer B2B Prime] |
| `intentconfiguration` | Mostra la configurazione intento e imposta/aggiorna i pesi. | Lettura e scrittura | [!DNL Journey Optimizer B2B Prime] | Legge e scrive [!DNL Journey Optimizer B2B Prime] |
| `intent-query` | Eseguire query e spiegare i punteggi di intento per persona/segmento/elenco. | Lettura | [!DNL Journey Optimizer B2B Prime] | Legge [!DNL Journey Optimizer B2B Prime] |

## Ottimizzazione dell’ora di invio {#sto}

| Abilità | Funzionamento | Accesso | Prodotto | Back-end (flusso di dati) |
|---|---|---|---|---|
| `send-time-optimization` | Controlla lo stato STO e abilita/disabilita su un nodo e-mail. | Lettura e scrittura | [!DNL Journey Optimizer B2B Prime] | Legge e scrive [!DNL Journey Optimizer B2B Prime] |
| `send-time-report` | Recupera/visualizza il rapporto sulle prestazioni STO. | Lettura | [!DNL Journey Optimizer B2B Prime] | Legge [!DNL Journey Optimizer B2B Prime] |

## Conoscenza {#knowledge}

| Abilità | Funzionamento | Accesso | Prodotto | Back-end (flusso di dati) |
|---|---|---|---|---|
| `product-knowledge` | Rispondi alle domande pratiche/concettuali dalla documentazione di [!DNL Journey Optimizer B2B Prime] su Experience League. | Lettura | Entrambi | Legge i documenti esterni — nessun dato di prodotto |

## Back-end incrociato {#cross-backend}

Queste abilità si estendono su più back-end:

- **`adapt-program`** — `gather_program_assets` legge [!DNL Marketo Engage] (`get_program`, `get_smart_campaign`, `list_emails`), quindi scrive tramite `falcomcp_create_journey` — cross-backend classico.
- **`audience-creation`** - legge [!DNL Marketo Engage] elenchi smart (`get_smart_list` / `get_smart_campaign`), quindi scrive [!DNL Journey Optimizer B2B Prime] elenchi di persone.
- **`journey-observability`** - [!DNL Journey Optimizer B2B Prime] letture più `check_lead_in_marketo_static_list` [!DNL Marketo Engage] lette.
- **`scoring-studio`** - legge [!DNL Marketo Engage] tipi di campi/attività lead insieme al servizio di punteggio [!DNL Journey Optimizer B2B Prime].

Tutti gli strumenti `falco-mcp_*` e percorsi/token/scoring/STO/FCS hanno raggiunto [!DNL Journey Optimizer B2B Prime] servizi; gli strumenti CSV/program/lead hanno raggiunto [!DNL Marketo Engage].
