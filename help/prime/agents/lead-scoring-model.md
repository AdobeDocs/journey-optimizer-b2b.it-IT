---
title: Creare modelli di punteggio personalizzati
description: Crea, visualizza in anteprima e pubblica modelli personalizzati di punteggio del lead in Journey Optimizer B2B Prime utilizzando l’abilità Studio di punteggio nell’interfaccia chat dell’Assistente IA.
badgeBeta: label="Beta" type="informative" tooltip="Questa funzione è attualmente in versione beta limitata"
autotag-review: '2026-06-25T21:20:26.754Z'
TQID: 'https://experienceleague.adobe.com/-D5EaJ-3GQ5iwaE6hChscZGEdflKmZ3tdp6VUNuPjWk'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: bef5003b-cad2-4f40-bdb2-a80426d52ef5id: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2: id: ff10f619-348f-47e3-99bf-3ce4c817cf2cid: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: d8f352c636ebd8980614922099701de8f755e8e4
workflow-type: tm+mt
source-wordcount: 489
ht-degree: 2%

---

# Creare modelli di punteggio personalizzati

>[!CONTEXTUALHELP]
>id="ajo-b2b-prime_scoring_studio"
>title="Scoring Studio"
>abstract="Utilizza l’abilità Studio di valutazione per creare, configurare e pubblicare modelli di punteggio del lead personalizzati tramite l’interfaccia chat dell’Assistente AI."

L&#39;abilità [_Scoring Studio_](./skills.md#scoring-signals) in [!DNL Adobe Journey Optimizer B2B Prime] fornisce una soluzione di valutazione dei lead nativa per l&#39;intelligenza artificiale che consente di creare, configurare e pubblicare modelli di valutazione dei lead. Lo studio combina un flusso di lavoro basato su agenti con un&#39;interfaccia utente visiva: è possibile creare modelli di punteggio tramite prompt del linguaggio naturale nell&#39;interfaccia chat dell&#39;[Assistente IA](./chat-interface.md) o interagendo direttamente con i controlli dell&#39;interfaccia utente.

* **Abilità** - `scoring-studio`
* **Chiamata** - Utilizzare un comando barra per aprire Scoring Studio. Ad esempio: _&quot;open Scoring Studio.&quot;_
* **Legge/scrive in** - [!DNL Journey Optimizer B2B Prime] servizio di punteggio; legge [!DNL Marketo Engage] campi lead e tipi di attività

All’avvio, l’Assistente AI recupera automaticamente il contesto rilevante, inclusi i tipi di attività, i campi del lead, gli elenchi di persone e gli elenchi di punteggi esistenti, per motivare i suggerimenti nei dati.

![Studio punteggio avviato nell&#39;interfaccia chat dell&#39;Assistente di IA](./assets/scoring-studio.png){width="700" zoomable="yes"}

## Creare un modello di punteggio {#create-model}

Quando apri Scoring Studio, l’Assistente AI propone un modello di punteggio di esempio pertinente precompilato con un elenco statico e un set di attività con punteggio. Potete accettare questo punto iniziale suggerito o fornire un prompt personalizzato per definire un modello personalizzato.

### Anteprima del modello {#preview-model}

Dopo aver richiesto, l&#39;Assistente IA genera un&#39;anteprima del modello prima di apportare qualsiasi modifica. Le superfici di anteprima:

* Dimensioni punteggio in uso
* Attributi e attività con punteggio
* Elenchi statici o elenchi avanzati applicati come segmenti
* Riepilogo dell&#39;obiettivo del modello, del segmento di destinazione e dei segnali primari

Puoi rivedere l’anteprima e scegliere di creare il modello basato su di essa, oppure continuare a perfezionare attraverso la chat prima di finalizzare.

### Struttura del modello {#model-structure}

Il modello creato è organizzato in _dimensioni_ e _segnali_. Puoi configurare ogni segnale utilizzando il pannello delle proprietà nell’interfaccia utente:

* **Tipo di segnale**: basato su attività o su attributi
* **Attività o attributo**: l&#39;elemento specifico da valutare
* **Parametri segnale** — Impostazioni regolabili per il segnale

Puoi generare e configurare modelli interamente tramite l’agente utilizzando il linguaggio naturale oppure interagire direttamente con i controlli dell’interfaccia utente.

## Pubblicare un modello di punteggio {#publish-model}

Quando il modello viene finalizzato, indica all&#39;agente di pubblicarlo. Il processo di pubblicazione gestisce automaticamente quanto segue:

| Passaggio | Cosa succede |
|---|---|
| **Compilazione regola** | Tutte le regole di punteggio vengono compilate e convalidate |
| **Creazione attività punteggio** | Viene creata e configurata un’attività punteggio pianificata da eseguire ogni giorno |

Dopo la pubblicazione, puoi anche attivare un’esecuzione manuale per elaborare immediatamente i punteggi.

## Visualizzare i risultati del punteggio {#view-results}

Al termine dell&#39;esecuzione di un punteggio, i punteggi vengono scritti nuovamente in [!DNL Marketo Engage] tramite il processo di importazione del lead. Al termine dell&#39;importazione, i punteggi aggiornati possono essere verificati direttamente in [!DNL Marketo Engage].

Dopo ogni esecuzione, puoi visualizzare un riepilogo dei risultati che mostra:

* Quante persone hanno ottenuto un punteggio
* Le singole modifiche di punteggio per persona

È disponibile un registro di controllo per la revisione di ulteriori dettagli di esecuzione.
