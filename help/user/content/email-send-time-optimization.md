---
title: Ottimizzazione dell’ora di invio delle e-mail
description: L’ottimizzazione del tempo di invio (STO) in Adobe Journey Optimizer personalizza la consegna e-mail per i percorsi di persone. Scopri come abilitare l’STO e migliorare il coinvolgimento.
feature: Person Journeys, Channels
role: User
source-git-commit: 55cfcd3b4ee777ee8945ea9a1cd1429625ee61c3
workflow-type: tm+mt
source-wordcount: '483'
ht-degree: 0%

---

# Ottimizzazione dell’ora di invio delle e-mail

Utilizza la funzione di ottimizzazione del tempo di invio per personalizzare la tempistica di consegna delle e-mail per [percorsi di persone](../journeys/journeys-overview.md) prevedendo quando è più probabile che ogni profilo sia coinvolto. Invece di un tempo di invio fisso, STO utilizza segnali storici di coinvolgimento e-mail per pianificare la consegna al momento ottimale per ogni destinatario, migliorando il coinvolgimento complessivo.

STO analizza il coinvolgimento storico di ciascun profilo utilizzando un modello di linguaggio di grandi dimensioni. Prevede e classifica i potenziali tempi di invio, quindi pianifica la consegna al momento più alto nella finestra di ottimizzazione.

## Disponibilità e ambito correnti

L’ottimizzazione dell’ora di invio è attualmente supportata per:

* **Tipo di Percorso**: Percorsi di persone
* **Canale**: e-mail
* **Configurazione**: _Invia e-mail_ nodo azione
* **Generazione rapporti**: Assistente IA tramite l&#39;abilità Osservabilità Percorso

  Informazioni approfondite sulle prestazioni, come l’utilizzo, l’incremento del coinvolgimento e i confronti STO e non-STO, sono disponibili tramite query in linguaggio naturale nell’Assistente IA.

>[!BEGINSHADEBOX]

Ci sono molti **_miglioramenti futuri_** pianificati per STO:

* Supporto per _Percorsi di account_
* Configurazione STO globale nell&#39;area _[!UICONTROL Amministratore]_
* Abilitazione STO a livello di percorso
* Divisioni di test/controllo configurabili
* Un dashboard dedicato per la generazione di rapporti STO

>[!ENDSHADEBOX]

## Configurazione

Puoi configurare l&#39;ottimizzazione dell&#39;ora di invio quando [aggiungi un _[!UICONTROL Esegui un&#39;azione]_ nodo](../journeys/action-nodes.md) a un percorso di persone.

1. Per _[!UICONTROL Seleziona azione]_, scegli **[!UICONTROL Invia e-mail]**.

1. Utilizza l&#39;interruttore **[!UICONTROL Ottimizzazione dell&#39;ora di invio]** per abilitare la funzione.

1. Impostare le opzioni STO per specificare la finestra e la distribuzione dei test:

   * **[!UICONTROL Invia entro]** - Questo valore determina la finestra di ottimizzazione (in giorni), che è l&#39;intervallo di tempo in cui è possibile recapitare le e-mail. Ad esempio, per un webinar che si svolge in cinque giorni, puoi impostare una finestra di quattro o cinque giorni. STO seleziona il tempo di invio migliore previsto per ciascun profilo all’interno di questa finestra.

   * **STO / Distribuzione fissa** - STO crea automaticamente una _suddivisione test e controllo_ per suddividere i profili idonei tra i tempi di invio ottimizzati e quelli fissi. La suddivisione consente un confronto diretto delle prestazioni. (I miglioramenti futuri sono pianificati per consentire percentuali di suddivisione personalizzate).

   >[!NOTE]
   >
   >I profili con una solida cronologia di coinvolgimento vengono suddivisi in gruppi di controllo e di test in modo uniforme per misurare l’impatto dell’operazione STO. Per garantire risultati statisticamente affidabili, la suddivisione tra STO e non STO è limitata tra il 30% e il 70%. Questo aiuta a evitare che le coorti più piccole distorcano i risultati e garantisce confronti significativi.

   ![Invia nodo del percorso di posta elettronica - Opzioni di ottimizzazione del tempo di invio](./assets/email-node-send-time-optimization.png){width="700" zoomable="no"}

1. Subito dopo il nodo _[!UICONTROL Invia e-mail]_, [aggiungi un nodo _Attendi_](../journeys/wait-nodes.md).

   Un nodo di attesa deve seguire immediatamente un’azione e-mail abilitata per STO. L’aggiunta di questo nodo assicura che i profili rimangano nel percorso fino a quando la finestra di ottimizzazione completa non viene cancellata e tutti gli invii dell’STO non vengono completati. Se si omette questo nodo, il sistema contrassegna la configurazione come non valida.

1. Dopo aver completato il resto del percorso di persone, procedi alla [pubblicazione](../journeys/create-publish-journey.md#publish-a-journey).

## Informazioni su STO

Gli approfondimenti STO vengono forniti tramite l&#39;_Assistente AI_ utilizzando l&#39;[_abilità di osservabilità_](../agents/journey-agent.md#journey-observability-skill) di Journey Agent. Puoi eseguire query sull’utilizzo, sulle metriche di coinvolgimento, sui risultati di test/controlli, sulle prestazioni dei nodi e sull’impatto complessivo del percorso.
