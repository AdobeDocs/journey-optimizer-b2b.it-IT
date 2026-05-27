---
title: Rapporto sulle prestazioni e-mail
description: Utilizza il rapporto sulle prestazioni delle e-mail in Journey Optimizer B2B edition per monitorare in un’unica vista unificata le metriche di invio, consegna, coinvolgimento e rinuncia in tutti i percorsi.
feature: Dashboards, Reporting
role: User
autotag-review: '2026-05-21T15:04:51.176Z'
TQID: 'https://experienceleague.adobe.com/hA63o9-2-atw0kRNFeEu6H449WmZ59CjL3uiVS7nEcA'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: a4b836d9-ffdd-4df3-a62a-f78b830cf059
  - id: f01b5556-e951-40ba-8625-2e3001864f2b
subfeature_v2:
  - id: ff0c35fa-aa7e-4050-a37c-198fcacd09e6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: 8226114f1a34adf85437579ef17a50b80ccfa596
workflow-type: tm+mt
source-wordcount: 833
ht-degree: 4%

---

# Rapporto sulle prestazioni delle e-mail

Il report **Prestazioni e-mail** offre agli addetti al marketing una visualizzazione unificata delle attività e-mail in tutti i percorsi in Adobe Journey Optimizer B2B edition. Aggrega le metriche di invio, consegna, coinvolgimento e rinuncia. Visualizzando sia i conteggi non elaborati che i tassi calcolati, puoi monitorare lo stato della campagna, confrontare le prestazioni delle e-mail e identificare immediatamente i problemi di recapito o coinvolgimento. Per le metriche a livello di percorso per i canali e-mail e SMS, consulta la [dashboard Percorsi di account](./journeys-dashboard.md).

## Accedere al rapporto

1. Nel menu di navigazione a sinistra, seleziona **[!UICONTROL Dashboard]**.
1. Seleziona la scheda **[!UICONTROL Prestazioni e-mail]** nella parte superiore del dashboard di reporting.

![Rapporto prestazioni e-mail](./assets/email-performance-dashboard.png){width="800" zoomable="yes"}

## Filtrare i dati

Fai clic sull&#39;icona _Filtro_ ( ![Icona Filtro](../assets/do-not-localize/icon-filter.svg) ) in alto a sinistra per filtrare la visualizzazione dei dati utilizzando i due tipi di filtro supportati. Questi filtri si applicano simultaneamente a tutti i pannelli:

* **[!UICONTROL Percorso]** - Filtra il report per visualizzare i dati per uno o più percorsi selezionati. Usa questo filtro per isolare le prestazioni per i percorsi rilevanti per la campagna o il programma.

* **Intervallo date** - Limita tutte le metriche alle e-mail inviate entro l&#39;intervallo di tempo specificato. Supporta intervalli predefiniti e un selettore di date personalizzato. Il selettore dell’intervallo di date si trova nell’angolo in alto a destra del dashboard.

![Filtri per Percorso e intervallo di date nella finestra di dialogo dei filtri](./assets/email-performance-filters.png){width="500"}

Quando modifichi i filtri nella finestra di dialogo dei filtri, fai clic su **[!UICONTROL Applica]**.

## Contare e valutare i grafici delle metriche

La sezione superiore del rapporto sulle prestazioni delle e-mail contiene due grafici a barre affiancati che forniscono un riepilogo visivo dello stato generale del programma e-mail nell’intervallo di date e nel percorso selezionati.

**Metriche conteggio** - Visualizza il volume assoluto dell&#39;attività e-mail. Ogni barra rappresenta il conteggio totale di un evento e-mail chiave in tutte le e-mail nell’ambito filtrato: Inviato, Consegnato, Aperto, Selezionato, Rifiutato e Annulla iscrizione.

**Metriche tasso** - Visualizza i tassi percentuali calcolati, consentendo di valutare la qualità del coinvolgimento e del recapito indipendentemente dal volume: tasso di consegna, tasso di apertura, tasso di clic, tasso di mancato recapito, tasso di clic per aprire e tasso di annullamento dell&#39;abbonamento.

Passa il puntatore del mouse sul grafico per visualizzare i dati numerici.

![Passa il puntatore del mouse sul grafico a barre. Numero visualizzato](./assets/email-performance-counts-hover.png){width="500"}

| Metrica | Tipo | Descrizione |
|--------|------|-------------|
| Inviato | Conteggio | Numero totale di messaggi e-mail inviati per la consegna. |
| Consegnati | Conteggio | Le e-mail sono state accettate dal server di posta del destinatario. |
| Apertura | Conteggio | Numero di e-mail consegnate aperte almeno una volta. |
| Clic | Conteggio | Numero di e-mail che hanno ricevuto almeno un clic di collegamento. |
| Mancato recapito | Conteggio | E-mail che non è stato possibile recapitare (mancati recapiti permanenti o non permanenti). |
| Iscrizioni annullate | Conteggio | Destinatari che hanno rinunciato tramite un collegamento di annullamento all’abbonamento nell’e-mail. |
| Percentuale di consegna | Tariffa | Consegnato ÷ inviato. Indica la percentuale di e-mail che hanno raggiunto le caselle in entrata. |
| Tasso di apertura | Tariffa | Aperto ÷ Consegnato. Misura il coinvolgimento del destinatario con le righe dell’oggetto. |
| Tasso di clic | Tariffa | Clic ÷ Consegnato. Misura il coinvolgimento di clic complessivo per e-mail consegnata. |
| Tasso di mancato recapito | Tariffa | ÷ non recapitate inviate. Evidenzia il recapito messaggi e elenca i problemi di integrità. |
| Percentuale di clic per apertura (CTOR) | Tariffa | Selezionato ÷ Aperto. Misura l’efficacia di contenuti e CTA tra i lettori coinvolti. |
| Tasso di annullamenti iscrizione | Tariffa | Annulla L’Abbonamento ÷ Consegnato. Pertinenza dei segnali e adattamento del pubblico. |

## Tabella delle prestazioni delle e-mail

Nella parte inferiore della pagina, una tabella dettagliata mostra le metriche per e-mail per ogni risorsa e-mail nell’ambito filtrato. Per impostazione predefinita, la tabella visualizza 10 righe per pagina.

La colonna **Annulla sottoscrizione %** è una metrica con priorità per il monitoraggio dell&#39;attività di rinuncia direttamente nella vista tabella.

| Colonna | Descrizione |
|--------|-------------|
| Nome e-mail | Nome della [risorsa e-mail](../content/add-email.md) configurata nel percorso. |
| Inviato | Totale invia per questa e-mail entro l’intervallo di date selezionato. |
| Consegnati | Numero di e-mail inviate correttamente ai server di posta dei destinatari. |
| % consegna | Consegnato ÷ Inviato, espresso come percentuale. |
| Aperti | Numero totale di eventi aperti registrati per questa e-mail. |
| Apri % | Apre ÷ Consegnato, espresso come percentuale. |
| Clic | Totale eventi clic collegamento per questa e-mail. |
| Fai clic su % | Clic ÷ consegnati, espressi come percentuale. |
| CTOR % | Percentuale di clic per apertura: clic ÷ aperture, espressa in percentuale. |
| E-mail non consegnate | Numero di e-mail non recapitate (mancati recapiti permanenti + non recapitati). |
| % mancato recapito | Mancato recapito ÷ Inviato, espresso come percentuale. |
| % annullamento abbonamento | Annulla L’Abbonamento ÷ Consegnato. Metrica prioritaria per monitorare l’integrità della rinuncia. |
| Prima attività | Timestamp del primo evento registrato (invio, apertura o clic) per questa e-mail nel periodo selezionato. |
| Ultima attività | Timestamp dell’evento registrato più recente per questa e-mail nel periodo selezionato. |

## Esportare i dati del rapporto

Il rapporto sulle prestazioni delle e-mail supporta l’esportazione dei dati per ulteriori analisi in strumenti esterni o per la condivisione dei risultati con le parti interessate. Puoi esportare i dati della tabella in formato CSV, compatibile con qualsiasi strumento di analisi dei dati o BI.

>[!CAUTION]
>
>Le esportazioni riflettono i filtri attualmente attivi. Assicurati che l’intervallo di date e i filtri di percorso siano impostati correttamente prima dell’esportazione per evitare dati incompleti nel file di output.

**_Per esportare i dati del report:_**

1. Imposta l&#39;intervallo di date in alto a destra e applica il filtro di **[!UICONTROL Percorso]** in base alle esigenze.
1. Fare clic sull&#39;icona del menu **...** nell&#39;angolo superiore destro del pannello Prestazioni e-mail e scegliere **[!UICONTROL Visualizza altro]**.
1. Fai clic su **[!UICONTROL Scarica CSV]** dal menu.

   ![Visualizza dati dettagliati e scarica CSV](./assets/email-performance-data-export.png){width="700" zoomable="yes"}

   Il file viene scaricato automaticamente nel percorso di download predefinito del browser.

1. Fai clic su **[!UICONTROL Chiudi]** per tornare al report delle prestazioni delle e-mail.
