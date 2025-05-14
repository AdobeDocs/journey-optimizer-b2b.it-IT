---
title: Aggiungere un messaggio e-mail al Percorso
description: Scopri come aggiungere, definire e ottimizzare azioni e-mail in Adobe Journey Optimizer B2B. Migliora i tuoi percorsi di account con comunicazioni e-mail mirate.
feature: Email Authoring, Content
source-git-commit: 6517a953692a56bd31c5b0f2fa5f15f40c6743b5
workflow-type: tm+mt
source-wordcount: '963'
ht-degree: 0%

---

# Aggiungi un messaggio e-mail al percorso

Utilizza Adobe Journey Optimizer B2B edition per inviare messaggi e-mail ai clienti tramite percorsi di account. Puoi scegliere di creare, personalizzare e visualizzare in anteprima i messaggi nello spazio di progettazione delle e-mail. In alternativa, puoi scegliere di inviare un’e-mail già definita nell’istanza di Marketo Engage connessa.

>[!NOTE]
>
>Se invii un’e-mail per la prima volta, assicurati che il canale e-mail sia configurato dall’interno di Adobe Marketo Engage. Per ulteriori informazioni, consulta [Protocolli per il tracciamento e la consegna e-mail](../start/email-protocols.md).

## Aggiungere un nodo di azione e-mail in un percorso

Puoi impostare le consegne e-mail in un percorso quando [aggiungi un _[!UICONTROL Esegui un&#39;azione]_ nodo](../journeys/action-nodes.md) ed esegui le seguenti operazioni:

1. Per l&#39;azione _[!UICONTROL sulla destinazione]_, scegliere **[!UICONTROL Persone]**.

1. Per _[!UICONTROL Azione sulle persone]_, scegli **[!UICONTROL Invia e-mail]**.

1. Per l&#39;_[!UICONTROL origine e-mail]_, scegliere la modalità di origine dell&#39;e-mail da inviare.

   ![Esegui un&#39;azione - invia un&#39;e-mail](assets/journey-node-send-email.png){width="700" zoomable="yes"}

   * Scegli **[!UICONTROL Crea nuova e-mail]** per creare l&#39;e-mail in modo nativo in Journey Optimizer B2B edition.

     Questa opzione consente di gestire il contenuto delle e-mail in modo nativo in Journey Optimizer B2B edition. Fai clic su **[!UICONTROL Crea e-mail]** per aprire la finestra di dialogo _Crea nuova e-mail_. È possibile creare una nuova risorsa di contenuto e-mail<!-- or duplicate an existing email content asset-->.

     Nella finestra di dialogo, immetti un **[!UICONTROL Nome]** univoco per l&#39;e-mail e una **[!UICONTROL Riga oggetto]**, quindi fai clic su **[!UICONTROL Crea]**.

     ![Crea nuova finestra di dialogo e-mail - nuova e-mail](assets/create-new-email-no-duplicate.png){width="400"}

     Nella sezione _[!UICONTROL Proprietà e-mail]_ della pagina del contenuto e-mail, i campi _[!UICONTROL Da e-mail]_ e _[!UICONTROL Rispondi all&#39;indirizzo]_ sono già configurati. È possibile immettere valori per i campi _[!UICONTROL Da nome]_ e _[!UICONTROL Descrizione]_ (facoltativo).

     Definisci le [impostazioni](#define-the-email-settings) dell&#39;e-mail e fai clic su **[!UICONTROL Modifica contenuto e-mail]** per [progettare il contenuto](./email-authoring.md).

     <!-- +++New email {#new-email}
     When you want to create an email using an empty canvas or an email template, use the _[!UICONTROL New email]_ option. 

     1. In the dialog, choose **[!UICONTROL New email]**.

     1. Enter a unique **[!UICONTROL Name]** for the email and a **[!UICONTROL Subject line]**.

        ![Create new email dialog - new email](assets/create-new-email.png){width="400"}

     1. Click **[!UICONTROL Create]**.

       In the _[!UICONTROL Email properties]_ section of the email content page, the _[!UICONTROL From email]_ and _[!UICONTROL Reply to address]_ fields are already configured. You can enter values for the _[!UICONTROL From name]_ and _[!UICONTROL Description]_ (optional) fields.

     1. Click **[!UICONTROL Edit email]** to define the email [settings](#define-the-email-settings) and design the [content](./email-authoring.md).

     +++

     +++Duplicate existing email {#duplicate-email}
     When you want to create an email using an existing email from the current journey or from another journey, use the Duplicate existing journey option. You can make changes to the duplicated email according to your objective for the journey node.

     1. In the dialog, choose **[!UICONTROL Duplicate existing email]**.

     1. For **[!UICONTROL Existing email to duplicate]**, click the _Select email_ icon and select the email you want to duplicate and use for the journey node.

      You can filter the list of emails by entering a text string in the search field to match the email name.

      ![Select email](assets/create-new-email-duplicate-select-email.png){width="600" zoomable="yes"}

      Select the checkbox for the email that you want to duplicate and click **[!UICONTROL Select]**. 

     1. Enter a unique **[!UICONTROL Name]** for the email and a **[!UICONTROL Subject line]**.

        ![Create new email dialog - duplciate existing email](assets/create-new-email.png){width="400"}

     1. Click **[!UICONTROL Create]**.

        In the _[!UICONTROL Email properties]_ section of the email content page, the _[!UICONTROL From email]_ and _[!UICONTROL Reply to address]_ fields are already configured. You can enter values for the _[!UICONTROL From name]_ and _[!UICONTROL Description]_ (optional) fields.

     1. If needed, click **[!UICONTROL Edit email]** to modify the email [settings](#define-the-email-settings) and [content](./email-authoring.md).

     +++
   —>
   * Scegli **[!UICONTROL Seleziona e-mail da Adobe Marketo Engage]** per utilizzare una delle e-mail precreate in Marketo Engage e inviarla come parte del percorso.

     ![Seleziona e-mail Marketo Engage](./assets/email-select-marketo.png){width="500" zoomable="yes"}

     Con questa opzione, il nodo è impostato e il contenuto dell’e-mail non necessita di ulteriori definizioni nel percorso.

## Definire le impostazioni e-mail

Con la scheda **[!UICONTROL Dettagli]** selezionata nel pannello _Riepilogo_ a destra, scorri verso il basso per visualizzare e impostare le opzioni e-mail.

![Impostazioni e-mail](./assets/email-summary-details-settings.png){width="600" zoomable="yes"}

| Opzione | Descrizione |
| ------ | ----------- |
| [!UICONTROL Da nome] | Nome del mittente utilizzato nell’intestazione dell’e-mail. Immettere il nome del mittente che si desidera venga visualizzato al destinatario. Fai clic sull&#39;icona _Personalizza_ ( ![Icona Personalizza](../assets/do-not-localize/icon-personalize.svg) ) per utilizzare un token di personalizzazione nel campo. |
| [!UICONTROL Da e-mail] | Indirizzo del mittente utilizzato nell’intestazione dell’e-mail. Il valore predefinito viene popolato dalle [impostazioni di consegna del canale e-mail](../admin/configure-channels-emails.md#delivery-settings). Fai clic sull&#39;icona _Personalizza_ ( ![Icona Personalizza](../assets/do-not-localize/icon-personalize.svg) ) per utilizzare un token di personalizzazione nel campo. |
| [!UICONTROL Indirizzo di risposta] | Indirizzo del mittente utilizzato nell’intestazione dell’e-mail. Il valore predefinito viene popolato dalle [impostazioni di consegna del canale e-mail](../admin/configure-channels-emails.md#delivery-settings) ([!UICONTROL Da etichetta]). Inserisci l’indirizzo e-mail che desideri compilare se il destinatario utilizza la funzione di risposta (può essere diverso o uguale all’indirizzo del mittente). Fai clic sull&#39;icona _Personalizza_ ( ![Icona Personalizza](../assets/do-not-localize/icon-personalize.svg) ) per utilizzare un token di personalizzazione nel campo. |
| [!UICONTROL Oggetto] | Testo visualizzato nel campo oggetto dell’e-mail. Il valore predefinito viene compilato dal testo immesso nella finestra di dialogo _[!UICONTROL Crea nuova e-mail]_. Se necessario, puoi modificare il testo. Fai clic sull&#39;icona _Personalizza_ ( ![Icona Personalizza](../assets/do-not-localize/icon-personalize.svg) ) per utilizzare un token di personalizzazione nel campo.<!-- Click the AI Assistant button ( ![AI Assistant icon](../../assets/do-not-localize/icon-gen-ai.svg){width="30" zoomable="no"} ) to generate the subject line based on the current email content.--> |
| [!UICONTROL E-mail operativa] | Seleziona la casella di controllo se desideri che l’e-mail sia operativa. Le e-mail operative sono escluse dagli elenchi di rinuncia/annullamento dell’iscrizione e dai limiti di comunicazione. Seleziona questa opzione solo se il destinatario non può considerare il messaggio e-mail come un messaggio commerciale non richiesto (SPAM). |
| [!UICONTROL Includi visualizzazione come pagina Web] | Seleziona la casella di controllo per includere un collegamento a una pagina web generata dal contenuto del messaggio e-mail. I messaggi e-mail hanno funzionalità più limitate rispetto alle pagine web, quindi è utile per JavaScript, CSS esteso e moduli. Il testo utilizzato per generare il collegamento è configurato nelle [impostazioni di consegna del canale e-mail](../admin/configure-channels-emails.md#delivery-settings) ([!UICONTROL Visualizza come pagina Web HTML] e [!UICONTROL Visualizza come testo della pagina Web]). |
| [!UICONTROL Disabilita tracciamento aperto] | Seleziona la casella di controllo se non desideri tenere traccia dell’attività di apertura delle e-mail. Con la funzione disattivata, i conteggi delle attività aperte e-mail vengono incrementati solo quando una persona univoca apre l’e-mail. Puoi [gestire il tracciamento per i collegamenti al contenuto delle e-mail](./email-authoring.md#content-authoring---link-tracking) durante la progettazione del contenuto del corpo dell&#39;e-mail. |
| [!UICONTROL Preheader] | Selezionare la casella di controllo per includere una preintestazione. Un preheader è il breve testo di riepilogo che viene visualizzato dopo la riga dell’oggetto in alcuni client e-mail. In genere fornisce un breve riepilogo dell’e-mail ed è in genere una singola frase. Immettere il testo di riepilogo nel campo<!-- , or click the AI Assistant button ( ![AI Assistant icon](../../assets/do-not-localize/icon-gen-ai.svg){width="30" zoomable="no"} ) to generate summary text based on the current email content -->. |
| [!UICONTROL Campi utilizzati come indirizzi CC] | Se disponibili, selezionare fino a 25 campi Lead o Società configurati in Marketo Engage utilizzando il tipo `Email`. |

## Controllare gli avvisi

Durante la progettazione del contenuto dei messaggi e-mail, gli avvisi vengono visualizzati nell’interfaccia (in alto a destra della pagina) quando mancano le impostazioni chiave. Se non trovi questo pulsante, non sono stati rilevati problemi.

![Avvisi e-mail](./assets/email-alerts.png){width="600" zoomable="yes"}

È possibile rilevare due tipi di avvisi:

* **_Avvisi_** che fanno riferimento a consigli e best practice, ad esempio:

   * `The opt-out link is not present in the email body`: è consigliabile aggiungere un collegamento di annullamento all&#39;abbonamento nel corpo dell&#39;e-mail.

     >[!NOTE]
     >
     >I messaggi e-mail in stile marketing devono includere un collegamento di rinuncia, che non è necessario per i messaggi transazionali.

   * `Text version of HTML is empty`: non dimenticare di definire una versione testuale del corpo dell&#39;e-mail, che viene utilizzata quando non è possibile visualizzare il contenuto HTML.

   * `Empty link is present in email body`: verificare che tutti i collegamenti presenti nel messaggio di posta elettronica siano corretti.

   * `Email size has exceeded the limit of 100KB`: per una consegna ottimale, assicurati che la dimensione dell&#39;e-mail non superi i 100 KB.

* **_Errori_** che impediscono di testare o attivare il percorso o la campagna finché non vengono risolti, ad esempio:

   * `The subject line is missing`: l&#39;oggetto dell&#39;e-mail è obbligatorio.

   * `The email version of the message is empty`: questo errore viene visualizzato quando il contenuto dell&#39;e-mail non è stato configurato.
