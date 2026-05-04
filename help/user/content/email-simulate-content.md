---
title: Anteprima e test del contenuto dell’e-mail
description: Visualizza un’anteprima delle e-mail con profili di test, controlla il rendering desktop e mobile, invia bozze ai destinatari e convalida la personalizzazione in Journey Optimizer B2B edition.
feature: Email Authoring
level: Beginner
role: User
exl-id: cf9d7716-b54d-430a-8102-72f9d35cc694
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: e666e996-b2cf-4c45-8fc2-1c625212ababid: f01b5556-e951-40ba-8625-2e3001864f2b
subfeature_v2: id: bd3c685c-6c92-4a4a-becb-535cc25215deid: ff0c35fa-aa7e-4050-a37c-198fcacd09e6
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: e0eb8757-182f-49f3-94a4-1587d16f5094
autotag-review: '2026-03-30T22:31:50.715Z'
source-git-commit: 8fe8318d7e1c63cbaa2749fc3928eb0a12967bd9
workflow-type: tm+mt
source-wordcount: 577
ht-degree: 7%

---

# Anteprima e test del contenuto dell’e-mail {#preview-simulate}

>[!CONTEXTUALHELP]
>id="ajo-b2b_email_preview_simulate"
>title="Controllare come viene eseguito il rendering del contenuto"
>abstract="Una volta definito il contenuto, puoi visualizzarne l’anteprima e verificare se viene riprodotto correttamente per il canale in uso."

Utilizza la funzione _Simula contenuto_ per visualizzare in anteprima il contenuto dell&#39;e-mail e inviare le consegne di prova a destinatari specifici. Per accedere alle funzionalità di anteprima e test, è necessario definire i campi e-mail obbligatori, tra cui _[!UICONTROL Nome mittente]_, _[!UICONTROL Indirizzo mittente]_, _[!UICONTROL Indirizzo destinatario risposta]_ e _[!UICONTROL Riga oggetto]_.

>[!IMPORTANT]
>
>Non puoi visualizzare l’anteprima del messaggio e-mail in presenza di errori. Controlla _Avvisi_ per assicurarti che non ci siano errori che bloccano le funzioni di anteprima. Gli avvisi non bloccano l’anteprima, ma è necessario indirizzarli prima di pubblicare il percorso che attiva la consegna e-mail.

## Visualizzare l’anteprima e-mail

Puoi accedere all&#39;anteprima del rendering dallo [spazio di progettazione e-mail](./email-authoring.md) o dal _[!UICONTROL Riepilogo]_ quando [apri un&#39;e-mail dall&#39;elenco e-mail](./emails-list.md#edit-emails).

1. Fai clic su **[!UICONTROL Simula contenuto]** in alto.

   ![Fai clic su Simula contenuto](assets/email-simulate-content.png){width="800" zoomable="yes"}

   >[!NOTE]
   >
   >Questo pulsante non è disponibile in caso di errori o se per l’e-mail non sono stati definiti campi obbligatori.

1. Nella pagina _[!UICONTROL Simula]_, seleziona un profilo persona nell&#39;elenco **[!UICONTROL Persone]** da utilizzare per il rendering dell&#39;e-mail.

   Nell’anteprima del contenuto, gli elementi personalizzati vengono compilati in base al profilo della persona selezionato.

   ![Seleziona un profilo persona per eseguire il rendering della simulazione](./assets/email-simulate-content-preview.png){width="800" zoomable="yes"}

   Se l&#39;elenco _[!UICONTROL Persone]_ a sinistra è vuoto, [aggiungi persone](#add-people-to-the-profiles-list) utilizzando i contatti dell&#39;istanza di Marketo Engage connessa.

   >[!TIP]
   >
   >È inoltre possibile utilizzare l&#39;[Integrazione rendering test Litmus](./email-test-rendering.md) per controllare il rendering dei messaggi di posta elettronica nei client desktop, mobili e basati su Web più diffusi.

## Regolare le opzioni di visualizzazione

Utilizza gli strumenti di visualizzazione per modificare l’anteprima in base al tipo di dispositivo o al livello di zoom:

* Seleziona l&#39;icona _Desktop_ ( ![Icona schermo del desktop](../../assets/do-not-localize/icon-device-desktop.svg) ) per visualizzare l&#39;anteprima utilizzando lo stile del desktop e le proporzioni.
* Seleziona l&#39;icona _Mobile_ ( ![icona di visualizzazione mobile](../../assets/do-not-localize/icon-device-mobile.svg) ) per visualizzare l&#39;anteprima utilizzando lo stile e le proporzioni del dispositivo mobile.
* Fare clic sulla freccia _Livello di zoom_ e selezionare una percentuale di zoom per verificare come cambia il contenuto in base al livello di zoom.

![Regola visualizzazione anteprima](assets/email-simulate-content-preview-display-options.png){width="600" zoomable="yes"}

## Inviare bozze

Una bozza è un messaggio di test consegnato che consente a te e ai membri del gruppo di rivedere un messaggio e-mail prima di inviarlo ai membri di un pubblico. I destinatari della bozza possono controllare il rendering, il contenuto, le impostazioni di personalizzazione e la configurazione dei messaggi. Puoi inviare bozze utilizzando un profilo di test selezionato.

1. Fai clic su **[!UICONTROL Invia bozza]** in alto a destra.

   ![Fai clic su Invia bozza](assets/email-simulate-content-preview-send-proof.png){width="500"}

1. Nella pagina _Invia bozza_ immettere l&#39;indirizzo di posta elettronica del primo destinatario.

1. Per ogni destinatario aggiuntivo che si desidera includere nella revisione, fare clic su **[!UICONTROL Aggiungi destinatario]** e immettere il relativo indirizzo di posta elettronica nel campo **[!UICONTROL Invia a]**.

   Puoi aggiungere fino a dieci destinatari per la consegna della bozza.

1. Per ogni destinatario, imposta il campo **[!UICONTROL Simula come]** selezionando un profilo di test da utilizzare per personalizzare il contenuto del messaggio.

   ![Aggiungere destinatari e impostare i profili di test](assets/email-simulate-content-preview-send-proof-recipients.png){width="700" zoomable="yes"}

1. Fai clic su **[!UICONTROL Invia bozza]**.

## Aggiungere persone all’elenco dei profili

1. Nella parte superiore dell&#39;elenco _[!UICONTROL Persone]_ fare clic su **[!UICONTROL Aggiungi persone]**.

   ![Regola visualizzazione anteprima](assets/email-simulate-content-add-people.png){width="500"}

1. Nella finestra di dialogo _[!UICONTROL Aggiungi persone per il test]_, immetti l&#39;indirizzo e-mail completo del contatto.

   Per aggiungere più contatti, immettere più indirizzi separati da una virgola.

1. Seleziona la casella di controllo per ogni contatto corrispondente che desideri aggiungere all’elenco dei profili di test.

   ![Regola visualizzazione anteprima](assets/email-simulate-content-add-people-addresses.png){width="700" zoomable="yes"}

1. Fai clic su **[!UICONTROL Aggiungi]** in alto a destra.
