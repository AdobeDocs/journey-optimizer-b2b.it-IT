---
title: Nodi esterni
description: Scopri come utilizzare i nodi Azione esterna e Percorso suddiviso esterno nei percorsi di account per connettersi con servizi esterni e instradare account e persone in base alla risposta del servizio.
feature: Account Journeys, Integrations
role: User
exl-id: fc0d6baa-d2e9-4a28-9d78-c74b99282ec1
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: a4b836d9-ffdd-4df3-a62a-f78b830cf059id: c8f3fb27-3167-48ac-a66a-fa4bc3f58dda
subfeature_v2: id: c31bc6c7-76bc-467b-80c0-7315a4e3f6be
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
autotag-review: '2026-04-29T23:21:59.633Z'
source-git-commit: 7cd6c4ecfbbd3a86b4f30d1b4fe6f06655a9c4f5
workflow-type: tm+mt
source-wordcount: 866
ht-degree: 0%

---

# Nodi esterni

Utilizza nodi esterni per collegare il tuo percorso di account a un servizio esterno. Quando il pubblico di un account raggiunge uno di questi nodi, Journey Optimizer B2B edition invia in modo asincrono i dati degli attributi del pubblico al servizio esterno. Il servizio elabora i dati e risponde utilizzando un callback, restituendo informazioni sul pubblico e metadati utilizzati dal percorso per continuare.

>[!NOTE]
>
>I nodi di azione esterna sono disponibili solo nei percorsi di account. Non sono supportati nei percorsi di persone.
>
>Un amministratore deve [configurare e attivare l&#39;azione esterna](../admin/configure-external-actions.md) prima che gli addetti al marketing aggiungano e implementino questi nodi in un percorso.

Esistono due tipi di nodo di azione esterna:

* **[Azione esterna](#external-action)** - Chiama un servizio esterno e continua lungo un singolo percorso in uscita. Utilizzare questo nodo quando si desidera attivare un processo esterno senza logica di diramazione, ad esempio l&#39;aggiornamento di un record in un sistema esterno o l&#39;invio di un segnale a un servizio downstream.
* **[Percorsi di suddivisione esterni](#external-split-paths)** - Chiama un servizio esterno e valuta la risposta per instradare gli account lungo uno dei diversi percorsi definiti. Usa questo nodo quando il servizio esterno restituisce un valore, ad esempio un punteggio, un livello o una classificazione, che determina il passaggio successivo nel percorso.

## Nodo azione esterna {#external-action}

Il nodo _Azione esterna_ chiama un servizio esterno e continua lungo un singolo percorso in uscita, indipendentemente dal contenuto della risposta. Utilizzalo per le integrazioni in cui non è necessario alcun ramo dopo la chiamata esterna.

1. Passare alla mappa del percorso di account.

1. Fai clic sull&#39;icona più ( **+** ) in un percorso e scegli **[!UICONTROL Azione esterna]**.

   ![Aggiungi un nodo azione esterna](./assets/node-external-action.png){width="400"}

1. Nelle proprietà del nodo a destra, imposta il contesto **[!UICONTROL Azione su]** per l&#39;azione esterna:

   * Scegliere **[!UICONTROL Account]** per applicare l&#39;azione esterna a tutte le persone che fanno parte degli account nel percorso del nodo.
   * Scegliere **[!UICONTROL Persone]** per applicare una modifica a tutte le persone nel percorso del nodo.

1. Selezionare il **[!UICONTROL nome servizio]** esterno.

   ![Nodo azione esterna - seleziona servizio esterno](./assets/node-external-action-service-name.png){width="600" zoomable="yes"}

   L&#39;elenco include tutte le azioni esterne configurate attive e designate per il tipo _Azione esterna_ e il contesto.

1. Se il servizio dispone di attributi globali, immettere i valori richiesti nei campi visualizzati sotto il nome del servizio.

1. Continua a creare il percorso dai percorsi in uscita del nodo.

   Il percorso _[!UICONTROL Timeout o errore]_ viene creato automaticamente. Se il periodo di timeout (configurato nel servizio) scade prima che venga ricevuta una risposta, l’account o la persona procede lungo questo percorso. Lo stesso vale se si riceve una risposta di errore. Per gestire questi scenari, puoi aggiungere nodi di percorso a questo percorso oppure il percorso termina per il membro del pubblico.

## Nodo percorsi suddivisi esterni {#external-split-paths}

Il nodo Percorsi suddivisi esterni richiama un servizio esterno e utilizza la risposta per determinare quali account percorso seguire. Ogni percorso è definito da una condizione basata su una variabile (funzione di accesso) restituita dal servizio esterno. Il percorso valuta la risposta in base alle condizioni del percorso definito e indirizza ogni account lungo il primo percorso corrispondente. Le condizioni del percorso vengono valutate in ordine decrescente. Ogni account procede lungo il primo percorso la cui condizione corrisponde al valore restituito dal servizio esterno.

1. Passare alla mappa del percorso di account.

1. Fai clic sull&#39;icona più ( **+** ) in un percorso e scegli **[!UICONTROL Percorsi di suddivisione esterni]**.

   ![Aggiungi un nodo di percorso suddiviso esterno](./assets/node-external-split-path.png){width="400"}

1. Nelle proprietà del nodo a destra, scegli un **[!UICONTROL Dividi percorsi per]** tipo:

   * **[!UICONTROL Account]** - Per i percorsi suddivisi per account, è possibile aggiungere nodi account e persone all&#39;interno dei percorsi definiti.
   * **[!UICONTROL Persone]** - Per i percorsi suddivisi per persone, è possibile aggiungere solo nodi di azione persone all&#39;interno dei percorsi definiti. Una suddivisione basata sulle persone viene automaticamente chiusa con un nodo _[!UICONTROL Percorsi di unione]_ in modo che tutte le persone possano passare al passaggio successivo senza perdere il contesto dell&#39;account.

1. Selezionare **[!UICONTROL Nome servizio]**.

1. Se la configurazione del servizio contiene _attributi globali_, immettere i valori richiesti nei campi visualizzati sotto il nome del servizio.

1. Per _[!UICONTROL Percorso 1]_, definire la condizione di diramazione:

   * Per **[!UICONTROL Label]**, sostituire il valore predefinito con un&#39;etichetta più descrittiva.
   * Per **[!UICONTROL Selezionare la variabile]**, scegliere una funzione di accesso. Le funzioni di accesso sono valori restituiti dal servizio esterno e sono definiti al momento della configurazione dell&#39;azione.
   * Per **[!UICONTROL Selezionare l&#39;operatore]**, scegliere l&#39;operatore.
   * Per **[!UICONTROL Immettere i valori]**, immettere il valore da confrontare.

   ![Nodo percorso suddiviso esterno - impostare la condizione del percorso utilizzando una variabile del servizio](./assets/node-external-split-path-properties.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Le variabili di condizione disponibili e il contesto di percorso supportato (_Account_, _Persone_ o _Persone nell&#39;account_) sono determinati dalla configurazione dell&#39;azione esterna. Se il servizio o le variabili previsti non sono disponibili, contatta l’amministratore.

1. Per aggiungere altri percorsi, fai clic su **[!UICONTROL Aggiungi percorso]** e definisci una condizione per ciascuno di essi.

1. Continua a creare il percorso da ogni percorso in uscita del nodo.

   Il percorso _[!UICONTROL Timeout o errore]_ viene creato automaticamente. Se il periodo di timeout (configurato nel servizio) scade prima che venga ricevuta una risposta, l’account o la persona procede lungo questo percorso. Lo stesso vale se si riceve una risposta di errore. Per gestire questi scenari, puoi aggiungere nodi di percorso a questo percorso oppure il percorso termina per il membro del pubblico.

1. Per combinare due o più percorsi in base alle esigenze per _Dividi per account_, è possibile aggiungere un [nodo percorsi unione](./split-merge-paths-nodes.md#merge-paths).
