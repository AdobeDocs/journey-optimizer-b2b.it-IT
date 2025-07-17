---
title: Rivedi il rapporto Spam
description: Scopri come controllare il punteggio di posta indesiderata in un rapporto spam dedicato che prevede se gli ISP o i provider di cassette postali lo considereranno o meno come spam.
feature: Email Authoring
level: Beginner
role: User
source-git-commit: 7992df497182b69c5103b603d69a70e1a40e903a
workflow-type: tm+mt
source-wordcount: '362'
ht-degree: 0%

---

# Rivedi il rapporto sulla posta indesiderata

Molti provider di posta in arrivo e la maggior parte dei sistemi aziendali utilizzano un processo di filtraggio dello spam. L’invio di e-mail che attivano questi filtri può influire notevolmente sul recapito messaggi. In Journey Optimizer B2B edition, puoi verificare il punteggio di posta indesiderata generato generando un rapporto Spam. Questo report utilizza [[!DNL SpamAssassin]](https://spamassassin.apache.org/) per testare l&#39;e-mail e consente di determinare se un messaggio può essere considerato come posta indesiderata dagli strumenti anti-spam. Puoi utilizzare le informazioni contenute nel rapporto per intraprendere azioni che migliorano il punteggio e il recapito dei contenuti dell’e-mail.

Quando rivedi le impostazioni delle e-mail o modifichi il contenuto, apri la pagina _[!UICONTROL Simula]_ e genera un _rapporto spam_ per rivedere il punteggio e gli elementi contrassegnati che possono attivare il filtro anti-spam.

1. Dalla pagina _[!UICONTROL Simula]_, fai clic su **[!UICONTROL Rapporto spam]** in alto a destra.

   ![Pulsante Report spam](./assets/email-spam-report-button.png){width="700" zoomable="yes"}

   Il processo di reporting analizza il contenuto dell’e-mail e genera un punteggio con un elenco delle regole di filtro attivate utilizzate per generare il punteggio. I fattori includono il layout del corpo, la struttura, le dimensioni dell’immagine, le parole chiave per la posta indesiderata e altri elementi. Per un elenco dei test di valutazione delle regole per gli elementi e-mail, consulta l&#39;[[!DNL SpamAssassin] elenco dei test](https://spamassassin.apache.org/old/tests_3_0_x.html).

1. Controlla i punteggi e le descrizioni di ogni elemento.

   >[!NOTE]
   >
   >Il punteggio spam viene calcolato tramite SpamAssassin e Adobe non è proprietaria delle regole o della logica di punteggio. Per ulteriori dettagli sul progetto open source [!DNL SpamAssassin], consulta la [[!DNL SpamAssassin] documentazione](https://cwiki.apache.org/confluence/display/SPAMASSASSIN/).

   Minore è il punteggio, minore è la probabilità che l’e-mail venga contrassegnata come spam.

   ![Punteggio positivo report spam](./assets/email-spam-report-positive.png){width="600" zoomable="yes"}

   Con un punteggio maggiore di 5, il rapporto include un avviso che segnala che alcuni messaggi possono essere bloccati o contrassegnati come spam al momento della ricezione. È consigliabile assicurarsi che il punteggio sia inferiore a 2.

   ![Punteggio nagativo report spam](./assets/email-spam-report-negative.png){width="600" zoomable="yes"}

1. Se all’interno del contenuto dell’e-mail sono presenti alcuni elementi che possono essere migliorati, modifica il contenuto per applicare gli aggiornamenti necessari.

1. Una volta completate le modifiche, torna alla pagina _[!UICONTROL Simula]_ e fai di nuovo clic su **[!UICONTROL Rapporto spam]** per verificare i miglioramenti risultanti nel punteggio.



