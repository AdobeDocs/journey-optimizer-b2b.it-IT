---
title: Configurazioni SMS
description: Connetti i provider SMS come Sinch, Twilio e Infobip con le credenziali API per abilitare la messaggistica di testo nei percorsi Journey Optimizer B2B edition.
feature: Setup, Channels
role: Admin
exl-id: bd41a5ec-929f-489f-a757-0720c1b44ed2
source-git-commit: 9ed2d2a36dbdaf39c107a18632d951003c86197b
workflow-type: tm+mt
source-wordcount: '714'
ht-degree: 0%

---

# Configurazioni SMS

Adobe Journey Optimizer B2B edition invia messaggi di testo tramite provider di servizi SMS (o provider di gateway SMS). Prima di creare il messaggio SMS, configura il provider di servizi dalle impostazioni _Amministratore_.

## Provider del servizio gateway SMS

Adobe Journey Optimizer B2B edition attualmente si integra con provider di terze parti che offrono servizi di messaggistica di testo in modo indipendente. I provider supportati per i messaggi di testo sono Sinch, Twilio e Infobip.

Prima di configurare un canale SMS in Adobe Journey Optimizer B2B edition, è necessario creare un account con uno di questi provider per ottenere il token API e l’ID servizio. Queste credenziali sono necessarie per configurare la connessione tra Adobe Journey Optimizer B2B edition e il provider applicabile.

>[!IMPORTANT]
>
>L’utilizzo dei servizi di messaggistica di testo è soggetto a termini e condizioni aggiuntivi da parte del provider applicabile. In qualità di soluzioni di terze parti, Sinch, Twilio e Infobip sono disponibili per gli utenti di Adobe Journey Optimizer B2B edition tramite un’integrazione. Adobe non controlla e non è responsabile per i prodotti di terze parti. Per eventuali problemi o richieste di assistenza relativi ai servizi di messaggistica di testo (SMS), contatta il provider.

## Verifica una configurazione API SMS esistente

>[!NOTE]
>
>Le impostazioni descritte sono accessibili solo agli utenti con privilegi di amministratore SMS.

1. Nel menu di navigazione sinistro, espandere la sezione **[!UICONTROL Amministratore]** e fare clic su **[!UICONTROL Canali]**.

   ![Accedere alla configurazione delle credenziali API SMS](./assets/config-sms-api.png){width="800" zoomable="yes"}

1. Nel pannello di navigazione, seleziona **[!UICONTROL Credenziali API]**.

   Nella pagina sono elencate le configurazioni API disponibili per l’istanza.

1. Se necessario, fai clic sull&#39;icona _Filtro_ ( ![Mostra o nascondi icona filtri](../assets/do-not-localize/icon-filter.svg) ) e seleziona le opzioni per visualizzare l&#39;elenco delle credenziali API configurate dal provider di servizi SMS o dal creatore.

   ![Fai clic sull&#39;icona Filtro per perfezionare l&#39;elenco delle credenziali API](./assets/config-sms-api-filter.png){width="600" zoomable="yes"}

## Creare nuove credenziali API per un provider di servizi SMS

>[!BEGINTABS]

>[!TAB Sinch]

_Per configurare Sinch come provider SMS con Adobe Journey Optimizer B2B edition :_

1. Nella barra di navigazione a sinistra, espandere la sezione **[!UICONTROL Amministratore]** e fare clic su **[!UICONTROL Configurazione]**.

1. Fai clic su **[!UICONTROL Crea nuove credenziali API]** in alto a destra nell&#39;elenco delle _[!UICONTROL credenziali API]_.

1. Configura le credenziali API SMS:

   ![Configurare le credenziali API di Sinch SMS](./assets/config-sms-api-sinch.png){width="500"}

   * **[!UICONTROL Fornitore SMS]** - Scegliere `Sinch` come provider SMS.

   * **[!UICONTROL Nome]** - Immettere un nome per le credenziali API.

   * **[!UICONTROL ID servizio]** e **[!UICONTROL Token API]** - Accedi alla pagina API dal tuo account Sinch (puoi trovare le tue credenziali nella scheda SMS).

   Per ulteriori informazioni su come trovare queste informazioni per il tuo account Sinch, consulta la [documentazione per gli sviluppatori di Sinch](https://developers.sinch.com/docs/sms/getting-started/#2-get-credentials)

1. Fai clic su **[!UICONTROL Invia]** una volta completati i dettagli di configurazione delle credenziali API.

>[!TAB Twilio]

_Per configurare Twilio come provider SMS con Adobe Journey Optimizer B2B edition :_

1. Nella barra di navigazione a sinistra, espandere la sezione **[!UICONTROL Amministratore]** e fare clic su **[!UICONTROL Configurazione]**.

1. Fai clic su **[!UICONTROL Crea nuove credenziali API]** in alto a destra nell&#39;elenco delle _[!UICONTROL credenziali API]_.

1. Configura le credenziali API SMS:

   ![Configurare le credenziali API SMS Twilio](./assets/config-sms-api-twilio.png){width="500"}

   * **[!UICONTROL Fornitore SMS]** - Scegliere `Twilio` come provider SMS.

   * **[!UICONTROL Nome]** - Immettere un nome per la definizione delle credenziali API.

   * **[!UICONTROL SID account]** e **[!UICONTROL Token autenticazione]**. Per trovare le credenziali, accedi al riquadro _Informazioni account_ della pagina del dashboard di Twilio Console.

   Per ulteriori informazioni su come trovare queste informazioni per l&#39;account Twilio, visitare il [Centro assistenza Twilio](https://help.twilio.com/articles/14726256820123-What-is-a-Twilio-Account-SID-and-where-can-I-find-it-).

1. Fai clic su **[!UICONTROL Invia]** in alto a destra della pagina al completamento dei dettagli di configurazione delle credenziali API.

>[!TAB Informazioni]

_Per configurare Infobip come provider SMS con Adobe Journey Optimizer B2B edition :_

1. Nella barra di navigazione a sinistra, espandere la sezione **[!UICONTROL Amministratore]** e fare clic su **[!UICONTROL Configurazione]**.

1. Fai clic su **[!UICONTROL Crea nuove credenziali API]** in alto a destra nell&#39;elenco delle _[!UICONTROL credenziali API]_.

1. Configura le credenziali API SMS:

   ![Configurare le credenziali API di Infobip SMS](./assets/config-sms-api-infobip.png){width="500"}

   * **[!UICONTROL Fornitore SMS]** - Scegliere `Infobip` come provider SMS.

   * **[!UICONTROL Nome]** - Immettere un nome per la definizione delle credenziali API.

   * **[!UICONTROL URL di base API]** e **[!UICONTROL chiave API]**. Per trovare le credenziali, accedere alla home page dell&#39;interfaccia Web o alla pagina di gestione delle chiavi API per l&#39;account Infobip.

   Per ulteriori informazioni su come trovare queste informazioni per l&#39;account Infobip, vedere la [documentazione di Infobip](https://www.infobip.com/docs/api/_blank).

1. Fai clic su **[!UICONTROL Invia]** in alto a destra della pagina al completamento dei dettagli di configurazione delle credenziali API.

>[!ENDTABS]

Quando fai clic su _[!UICONTROL Invia]_, le credenziali vengono immediatamente convalidate e salvate, reindirizzandoti alla pagina dell&#39;elenco delle _[!UICONTROL credenziali API]_. Se le credenziali inviate non sono valide, il sistema visualizza un messaggio di errore nella pagina dell&#39;elenco. In questo caso, puoi scegliere di annullare la configurazione o di aggiornarla e inviarla nuovamente.
