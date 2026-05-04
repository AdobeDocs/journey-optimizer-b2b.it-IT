---
title: Rivedi il rapporto Spam
description: Genera rapporti di posta indesiderata con punteggio SpamAssassin per verificare se le e-mail attivano i filtri anti-spam e migliorano il recapito messaggi in Journey Optimizer B2B edition.
feature: Email Authoring
level: Beginner
role: User
exl-id: 0ab2a85c-fbab-4681-9964-74b7fd1d574f
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: c8f3fb27-3167-48ac-a66a-fa4bc3f58dda
  - id: f01b5556-e951-40ba-8625-2e3001864f2b
subfeature_v2:
  - id: ff0c35fa-aa7e-4050-a37c-198fcacd09e6
  - id: a7692144-1dc6-426f-b00f-fe187797f61d
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: beb7a3c1-66ab-4786-b879-7621375b3c40
autotag-review: '2026-03-30T22:30:57.478Z'
source-git-commit: 8fe8318d7e1c63cbaa2749fc3928eb0a12967bd9
workflow-type: tm+mt
source-wordcount: 364
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
