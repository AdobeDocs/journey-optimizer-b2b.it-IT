---
title: Test rendering e-mail
description: Test del rendering di e-mail su client desktop, mobili e web con integrazione Litmus per garantire la compatibilità della casella in entrata in Journey Optimizer B2B edition.
feature: Email Authoring, Integrations
level: Intermediate
role: User
exl-id: 26d87a56-6bd1-4d4a-8090-71f5b0a7e9f8
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: c8f3fb27-3167-48ac-a66a-fa4bc3f58ddaid: f01b5556-e951-40ba-8625-2e3001864f2bid: e666e996-b2cf-4c45-8fc2-1c625212abab
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: cad51180-f8ce-4cb7-aefc-437847b5d6d6
autotag-review: 2026-03-30T22:28:13.343Z
TQID: https://experienceleague.adobe.com/G9c2TdbEje4HgE82tKURAn-UYz5wB-9iLsT9805m1JI
source-git-commit: 9baf03a1ddc1733385b0398ffadde8f548c431cc
workflow-type: tm+mt
source-wordcount: 376
ht-degree: 5%

---

# Testare il rendering delle e-mail con Litmus

Per verificare le e-mail, puoi sfruttare un account aziendale [Litmus](https://www.litmus.com/email-testing){target="_blank"} di Journey Optimizer B2B edition. Con questa integrazione, puoi visualizzare in anteprima il rendering delle e-mail nei client e-mail più diffusi. Questo strumento ti aiuta a garantire che il contenuto delle e-mail si presenti in modo ottimale e funzioni come previsto in ogni casella in entrata.

>[!AVAILABILITY]
>
>Questa integrazione è disponibile solo per gli utenti di Journey Optimizer B2B edition con account Litmus Enterprise. Per ulteriori informazioni, vedere la pagina della soluzione [sul sito Web Litmus](https://www.litmus.com/solutions/esp/adobe-journey-optimizer){target="_blank"}.

1. Quando la progettazione delle e-mail è completa e pronta per essere testata, fai clic su **[!UICONTROL Simula contenuto]** nell&#39;area di progettazione delle e-mail.

1. Fai clic su **[!UICONTROL Rendering e-mail]** in alto a destra.

   ![Pulsante Rendering e-mail](./assets/email-simulate-render-button.png){width="700" zoomable="yes"}

   Se non hai ancora effettuato la connessione all’account Litmus da Journey Optimizer B2B edition, la pagina visualizzata offre un’opzione per avviare un account di prova o per connettersi all’account esistente.

1. Fai clic su **[!UICONTROL Connetti il tuo account Litmus]** in alto a destra oppure utilizza il collegamento all&#39;interno della pagina.

   ![Connetti il tuo account Litmus](./assets/email-simulate-render-litmus-connect.png){width="700" zoomable="yes"}

1. Immetti le credenziali del tuo account Litmus e fai clic su **[!UICONTROL Accedi]**.

1. Fai clic su **[!UICONTROL Connetti]** per confermare la connessione tra Litmus e Journey Optimizer B2B edition e inviare il contenuto dell&#39;e-mail per il rendering.

   >[!IMPORTANT]
   >
   >Quando connetti il tuo account Litmus con Journey Optimizer B2B edition, accetti che i messaggi di prova vengano inviati a Litmus. Questo contenuto viene quindi gestito all’interno di Litmus e non in Adobe. Di conseguenza, i criteri e-mail di conservazione dei dati di Litmus si applicano a tali e-mail, inclusi i dati di personalizzazione che possono essere inclusi nei messaggi di test.

1. Fai clic su **[!UICONTROL Esegui test]** in alto a destra per generare anteprime e-mail.

   ![Esegui un test di rendering Litmus](./assets/email-simulate-render-litmus-run-test.png){width="700" zoomable="yes"}

1. Verifica il contenuto delle e-mail nei client desktop, mobili e basati su web più diffusi.

   Fai clic sulla miniatura visualizzata per visualizzare i dettagli di qualsiasi test client sottoposto a rendering.

   ![Anteprime e-mail Litmus](./assets/email-simulate-render-litmus-previews.png){width="700" zoomable="yes"}

1. Al termine della revisione, fare clic sulla freccia indietro ( ![Mostra o nascondi icona filtri](../../assets/do-not-localize/icon_back-arrow.svg) ) in alto a sinistra per tornare alla pagina Simula contenuto.

   Puoi selezionare un altro profilo ed eseguire un altro test di rendering, oppure tornare allo spazio di progettazione delle e-mail per apportare le modifiche necessarie in base alla revisione.
