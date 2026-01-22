---
title: Nodi del pubblico della persona
description: Configura i nodi di pubblico personale con segmenti o tipi di pubblico basati su eventi per definire punti di ingresso del percorso di persone per l’orchestrazione mirata in Journey Optimizer B2B edition.
feature: Audiences
role: User
badgeBeta: label="Beta" type="informative" tooltip="Questa funzione è attualmente in versione beta limitata"
source-git-commit: f5170767a6df14874fab5de203264a5a5e3e245a
workflow-type: tm+mt
source-wordcount: '707'
ht-degree: 0%

---

# Nodi del percorso di pubblico della persona

Il nodo _audience persona_ specifica i profili di persona che entrano nel percorso. Quando [crei un percorso di persone](./create-publish-journey.md#create-a-journey), il percorso inizia sempre con un nodo di pubblico di persone che ne definisce l&#39;input. Il nodo del pubblico della persona può avere uno dei due tipi di input del pubblico: segmenti CDP o appartenenza basata su eventi. Non è possibile combinare definizioni di pubblico basate su segmenti e eventi.

Utilizza una delle seguenti opzioni di input per il nodo percorso di pubblico persona:

* **Pubblico profilo** - Utilizza i tipi di pubblico dei segmenti definiti in un CDP. Tutti i profili idonei per il pubblico vengono aggiunti come membri al percorso. I nuovi profili qualificati per il segmento vengono aggiunti al percorso durante le [attività di acquisizione profilo](#profile-ingestion) giornaliere. Se un profilo non è più idoneo per il segmento, verrà rimosso **_non_** dal percorso.

* **Pubblico evento** - Utilizza eventi qualificati per definire il pubblico. Questi eventi sono definiti nella configurazione del nodo e devono utilizzare [eventi XDM configurati nelle impostazioni di amministrazione](../admin/configure-aep-events.md). Sono supportati fino a 10 eventi per l’iscrizione a un pubblico basato su eventi. Un profilo è idoneo immediatamente per il percorso successivo al primo evento corrispondente rilevato dal suo profilo.

  >[!NOTE]
  >
  >Gli eventi non possono essere combinati con gli attributi di profilo per limitare le definizioni di pubblico. Sono previsti miglioramenti per ovviare a questo limite nelle versioni future.

## Acquisizione profilo

In Journey Optimizer B2B edition, un’attività di acquisizione notturna del pubblico mantiene i profili sincronizzati con Experience Platform. Anche se i percorsi di persone basati su eventi possono qualificare profili che non fanno parte di un profilo o di un pubblico di account acquisito/in uso da Journey Optimizer B2B edition, ciò si traduce in profili acquisiti che rimangono non aggiornati a meno che non facciano parte di un pubblico utilizzato da un percorso di persone, un percorso di account o un gruppo di acquisto. Se un profilo viene acquisito e successivamente aggiunto a un pubblico, viene eseguita l’unione di profili e il profilo rimane sincronizzato con Experience Platform. Sono previsti miglioramenti alla sincronizzazione dei dati del profilo per le versioni future.

Un nuovo profilo creato acquisito da un percorso di persone basato su eventi potrebbe non disporre delle informazioni di profilo aggiornate al momento dell’acquisizione. Ad esempio, se un profilo viene creato tramite un evento di compilazione del modulo e un percorso di persone lo acquisisce dall’evento di compilazione del modulo, i dati inviati nel modulo potrebbero non essere ancora sincronizzati con il profilo al momento in cui il percorso lo ha acquisito. Il risultato potrebbe essere costituito da dati incompleti per la personalizzazione (ad esempio nel contenuto dell’e-mail). Sono previsti miglioramenti alla sincronizzazione dei dati di questo evento profilo per le versioni future.

I percorsi di persone basati su eventi possono qualificare profili ancora anonimi/senza indirizzi e-mail e contenenti solo ECID. Si verifica più comunemente quando si dispone di una logica di qualificazione per l’attività della pagina web. Una logica di pubblico eccessivamente ampia basata su eventi potrebbe portare l’istanza a raggiungere il limite di 40 milioni di profili, se troppi profili sono idonei. Limita il possibile ambito del pubblico per evitare questo scenario.

>[!IMPORTANT]
>
>Durante il programma beta corrente, l’utilizzo ideale dei percorsi di persone consiste nel qualificare solo i profili di cui esegui il targeting anche nei percorsi di account e nelle definizioni dei gruppi di acquisto. Questo utilizzo assicura che il profilo completo rimanga sincronizzato con Experience Platform.

## Impostare il pubblico per il nodo del pubblico della persona

1. Fai clic sul nodo **[!UICONTROL Pubblico persona]**.

   Questa azione visualizza le proprietà del nodo a destra.

   ![Nodo percorso di pubblico della persona](./assets/person-journey-person-audience-node.png){width="700" zoomable="yes"}

1. Scegliere il tipo di input per le persone che accedono al percorso:

   * **[!UICONTROL Pubblico profilo]**

     Scegli l&#39;opzione _[!UICONTROL Pubblico profilo]_. Quindi, fai clic su **[!UICONTROL Aggiungi pubblico profilo]**.

     Nella finestra di dialogo _[!UICONTROL Aggiungi pubblico]_, seleziona un segmento di pubblico creato in precedenza. Quindi, fai clic su **[!UICONTROL Aggiungi pubblico]**.

     ![Selezionare un pubblico di profilo per il nodo](./assets/node-person-audience-add-audience-dialog.png){width="700" zoomable="yes"}

   * **[!UICONTROL Pubblico evento]**

     Scegliere l&#39;opzione _[!UICONTROL Pubblico evento]_. Quindi fare clic su **[!UICONTROL Aggiungi criteri evento]**.

     Nella finestra di dialogo _[!UICONTROL Modifica criteri evento]_, aggiungi uno o più eventi da utilizzare per la qualifica di membro del pubblico. Per ogni evento aggiunto, fare clic su **[!UICONTROL Aggiungi vincolo]** per scegliere un attributo evento per una corrispondenza. Impostare la valutazione da utilizzare per una corrispondenza. Puoi aggiungere più vincoli per far corrispondere l’evento.

     ![Aggiungere eventi e criteri di corrispondenza per qualificare un profilo persona](./assets/node-person-audience-edit-event-criteria-dialog.png){width="700" zoomable="yes"}

     Una volta definiti i criteri dell&#39;evento, fare clic su **[!UICONTROL Salva]**.

     Per ulteriori informazioni sulla configurazione per gli eventi supportati dal percorso, vedi [Gestione eventi esperienza](../admin/configure-aep-events.md#manage-experience-events).
