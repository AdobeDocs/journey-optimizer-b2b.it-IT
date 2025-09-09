---
title: Token personalizzati per E-mail Personalization
description: 'Creazione e gestione di token personalizzati per la personalizzazione dinamica dei messaggi e-mail: definisci le variabili di testo e numero per i percorsi di account in Journey Optimizer B2B edition.'
feature: Personalization, Content, Email Authoring
role: User
exl-id: 05d4f446-6348-4555-9c46-316c2857f01d
source-git-commit: 79012352c3ae4e2f3d38b632b1f523d262f74f96
workflow-type: tm+mt
source-wordcount: '603'
ht-degree: 2%

---

# Token personalizzati per la personalizzazione delle e-mail

La personalizzazione del contenuto utilizza i token come segnaposto o variabili che vengono compilate al momento della generazione dell’artefatto di contenuto. I token di personalizzazione standard sono disponibili per e-mail, pagine di destinazione, frammenti e modelli. Puoi anche definire un set di token personalizzati con valori specifici per il percorso di conti. Questo set di token personalizzati si chiama _I miei token_ e uno qualsiasi di questi token personalizzati è destinato alla personalizzazione quando si creano [e-mail di percorso](./email-authoring.md#content-authoring---personalization).

Oltre a _I miei token_, specifici del percorso di account, puoi utilizzare qualsiasi token standard (integrato) per la personalizzazione delle e-mail.

## Gestisci i miei token {#my-tokens}

I _Token personali_ sono variabili personalizzate create o modificate per un percorso di account in stato Bozza. Questo set di token personalizzati supporta attualmente le definizioni dei token di testo e numerici.

Quando aggiungi un token personalizzato a un&#39;e-mail, questo viene visualizzato come `{{my.TokenName}}`. Ad esempio, potresti avere `{{my.EventDate}}` o `{{my.WebinarSpeaker}}` token creati per gestire il contenuto delle e-mail relative ai prossimi webinar.

_Per accedere ai token personalizzati per un percorso di account :_

1. Aprire il percorso di conti provvisori.

1. Fai clic sul menu **[!UICONTROL Altro...]** in alto a destra e scegli **[!UICONTROL I miei token]**.

   ![Fai clic su Altro in alto a destra](../journeys/assets/account-journey-draft-more-menu.png){width="450"}

   Nella pagina _Token personali_ sono elencati tutti i token personalizzati definiti per il percorso.

   ![Token personali](./assets/my-tokens-list-page.png){width="700" zoomable="yes"}

### Creare un token

1. Nella pagina _[!UICONTROL Token personali]_, fai clic su **[!UICONTROL Crea]** e scegli il tipo di token che desideri definire:

   * **[!UICONTROL Testo]** - Utilizzare questo tipo per definire un token con un valore stringa di testo di base.

   * **[!UICONTROL Numero]** - Utilizzare questo tipo per definire un token con un valore numerico.

1. Nella finestra di dialogo, immetti **[!UICONTROL Nome]** e **[!UICONTROL Valore]** per il token.

   ![Immettere un nome e un valore per il token di testo](./assets/my-tokens-create-text-token-dialog.png){width="400"}

   Non è possibile utilizzare spazi o caratteri speciali nel nome del token. È possibile utilizzare _Camel Case_, ad esempio `EventType`, per utilizzare un nome composto da più parole facilmente identificabile.

   Se si definisce un token _Number_, il valore può contenere solo caratteri numerici. È possibile utilizzare un valore decimale.

   ![Immettere un nome e un valore per il token numerico](./assets/my-tokens-create-number-token-dialog.png){width="400"}

1. Fai clic su **[!UICONTROL Aggiungi]**.

### Modificare un token

Mentre il percorso di account rimane nello stato Bozza, puoi modificare qualsiasi token definito.

1. Nella pagina _[!UICONTROL Token personali]_, fai clic sull&#39;icona _Altre azioni_ (**...**) accanto al nome del token e scegli **[!UICONTROL Modifica]**.

   ![Menu altre azioni token](./assets/my-tokens-more-actions.png){width="430"}

1. Nella finestra di dialogo, modifica **[!UICONTROL Nome]** e **[!UICONTROL Valore]** come necessario per il percorso.

   ![Modifica il nome e il valore del token](./assets/my-tokens-edit-text-token-dialog.png){width="400"}

1. Fai clic su **[!UICONTROL Modifica]**.

### Eliminare un token

Puoi eliminare un token personalizzato dall&#39;elenco _Token personali_, ma devi accertarti che non sia attualmente utilizzato nel contenuto dell&#39;e-mail del percorso.

1. Nella pagina _[!UICONTROL Token personali]_, fai clic sull&#39;icona _Altre azioni_ (**...**) accanto al nome del token e scegli **[!UICONTROL Elimina]**.

1. Nella finestra di dialogo di conferma, fai clic su **[!UICONTROL Elimina]**.

## Utilizzare token personalizzati nel contenuto

Quando crei contenuti e-mail per il percorso di account, puoi utilizzare uno qualsiasi dei token dell&#39;elenco _Token personali_ quando utilizzi gli strumenti di personalizzazione nell&#39;area di progettazione visiva.

1. Seleziona il componente testo e fai clic sull&#39;icona _Aggiungi personalizzazione_ ( ![Aggiungi icona personalizzazione](../../assets/do-not-localize/icon-personalization-field.svg) ) nella barra degli strumenti.

   ![Fai clic sull&#39;icona Aggiungi personalizzazione](./assets/email-personalize-text.png){width="600"}

   Questa azione apre la finestra di dialogo _Modifica Personalization_. La finestra di dialogo include una cartella _[!UICONTROL I miei token]_ nella libreria _[!UICONTROL Token di Personalization]_ se sono stati definiti token personalizzati per il percorso di account.

1. Espandi la cartella **[!UICONTROL I miei token]**, quindi fai clic su **+** o **...** per aggiungere uno dei tuoi token personalizzati allo spazio vuoto.

   Se necessario, puoi aggiungere altro testo statico.

   ![Crea testo personalizzato con i miei token](./assets/personalization-edit-dialog-my-tokens.png){width="700" zoomable="yes"}

1. Fai clic su **[!UICONTROL Salva]**.
