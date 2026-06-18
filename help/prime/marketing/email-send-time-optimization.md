---
title: Ottimizzazione dell’ora di invio delle e-mail
description: L’ottimizzazione dell’ora di invio (STO) in Adobe Journey Optimizer B2B Prime personalizza la consegna e-mail per i percorsi di persone. Scopri come abilitare l’STO e migliorare il coinvolgimento.
autotag-review: '2026-06-17T20:52:02.535Z'
TQID: 'https://experienceleague.adobe.com/wlxhS7E8DnbThm5ge-wzTkMcn-eBzFUXfw3ZGrfcRHA'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: a4b836d9-ffdd-4df3-a62a-f78b830cf059
  - id: bef5003b-cad2-4f40-bdb2-a80426d52ef5
  - id: f01b5556-e951-40ba-8625-2e3001864f2b
  - id: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2:
  - id: d270a788-eb1d-40ed-b74e-9158ed975b1f
  - id: ff0c35fa-aa7e-4050-a37c-198fcacd09e6
source-git-commit: 951d9ceaa95656952e36b6d8f238348b08c796ca
workflow-type: tm+mt
source-wordcount: 403
ht-degree: 0%

---

# Ottimizzazione dell’ora di invio delle e-mail

Utilizza la funzione di ottimizzazione del tempo di invio per personalizzare la tempistica di consegna delle e-mail per [percorsi di persone](./person-journeys.md) prevedendo quando è più probabile che ogni profilo sia coinvolto. Invece di un tempo di invio fisso, STO utilizza segnali storici di coinvolgimento e-mail per pianificare la consegna al momento ottimale per ogni destinatario, migliorando il coinvolgimento complessivo.

STO analizza il coinvolgimento storico di ciascun profilo utilizzando un modello di linguaggio di grandi dimensioni. Prevede e classifica i potenziali tempi di invio, quindi pianifica la consegna al momento più alto nella finestra di ottimizzazione.

<!-- Performance insights, such as usage, engagement lift, and STO vs. non-STO comparisons, are available through natural language queries in the AI Assistant. -->

>[!BEGINSHADEBOX]

Ci sono molti **_miglioramenti futuri_** pianificati per STO:

* Configurazione STO globale nell&#39;area _[!UICONTROL Amministratore]_
* Abilitazione STO a livello di percorso
* Divisioni di test/controllo configurabili

>[!ENDSHADEBOX]

## Configurazione {#configuration}

Puoi configurare l&#39;ottimizzazione dell&#39;ora di invio quando [aggiungi un _[!UICONTROL Esegui un&#39;azione]_ nodo](./action-nodes.md) a un percorso di persone e scegli l&#39;azione **[!UICONTROL Invia e-mail]**.

1. Selezionare il nodo _Invia e-mail_ azione di percorso.

1. Nelle proprietà del nodo a destra, abilita l&#39;opzione **[!UICONTROL Ottimizzazione dell&#39;ora di invio]**.

   ![Invia nodo del percorso di posta elettronica - Opzioni di ottimizzazione del tempo di invio](./assets/email-node-send-time-optimization.png){width="450" zoomable="no"}

1. Per specificare la distribuzione della finestra e del test, impostare le opzioni STO:

   * **[!UICONTROL Invia entro]** - Questo valore determina la finestra di ottimizzazione (in giorni), che è l&#39;intervallo di tempo in cui è possibile recapitare le e-mail. Ad esempio, per un webinar che si svolge in cinque giorni, puoi impostare una finestra di quattro o cinque giorni. STO seleziona il tempo di invio migliore previsto per ciascun profilo all’interno di questa finestra.

   * **STO / Distribuzione fissa** - STO crea automaticamente una _suddivisione test e controllo_ per suddividere i profili idonei tra i tempi di invio ottimizzati e quelli fissi. La suddivisione consente un confronto diretto delle prestazioni. (I miglioramenti futuri sono pianificati per consentire percentuali di suddivisione personalizzate).

   >[!NOTE]
   >
   >I profili con una solida cronologia di coinvolgimento vengono suddivisi in gruppi di controllo e di test in modo uniforme per misurare l’impatto dell’operazione STO. Per garantire risultati statisticamente affidabili, la suddivisione tra STO e non STO è limitata tra il 30% e il 70%. Questo aiuta a evitare che le coorti più piccole distorcano i risultati e garantisce confronti significativi.

1. Subito dopo il nodo _[!UICONTROL Invia e-mail]_, [aggiungi un nodo _Attendi_](./wait-nodes.md).

   Un nodo di attesa deve seguire immediatamente un’azione e-mail abilitata per STO. L’aggiunta di questo nodo assicura che i profili rimangano nel percorso fino a quando la finestra di ottimizzazione completa non viene cancellata e tutti gli invii dell’STO non vengono completati. Se si omette questo nodo, il sistema contrassegna la configurazione come non valida.

1. Dopo aver completato il resto del percorso di persone, procedi alla [pubblicazione](./person-journeys.md#publish).

## Reporting


