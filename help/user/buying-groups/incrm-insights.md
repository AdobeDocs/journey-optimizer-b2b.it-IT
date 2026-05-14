---
title: Informazioni in-CRM
description: Accedi ai gruppi di acquisto di Journey Optimizer B2B edition direttamente in CRM. I membri del team di vendita possono visualizzare i dati sul coinvolgimento e identificare le opportunità di vendita grazie a In-CRM Insights.
feature: Sales Insights, Buying Groups
role: User
exl-id: c55a1fce-2ddc-481b-9f60-5e67a4bf9633
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: afadf741-c5fe-42cd-8013-23bb6ff2d1bcid: fc1ff3b2-6614-41ad-a113-de48597598fdid: c8f3fb27-3167-48ac-a66a-fa4bc3f58dda
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: e1e0219c-f879-479f-8427-888ed2a6e9c2
autotag-review: 2026-03-30T21:40:22.011Z
TQID: https://experienceleague.adobe.com/HfypAUMJxZyWaQlkknyxUn63x5uVqcfJU-pzXcDWYBs
source-git-commit: 9baf03a1ddc1733385b0398ffadde8f548c431cc
workflow-type: tm+mt
source-wordcount: 483
ht-degree: 1%

---

# Informazioni in-CRM

[!DNL In-CRM Insights] è un&#39;applicazione basata su Web che si integra in Salesforce e Microsoft Dynamics 365, consentendo l&#39;accesso a [!DNL Journey Optimizer B2B Edition] gruppi di acquisto direttamente all&#39;interno del CRM. Riunisce le fonti di dati sulle vendite, facilitando l&#39;identificazione delle opportunità di incremento del coinvolgimento e del potenziale di vendita.

## Installazione

Il processo di installazione include:

* Configurazione di autorizzazioni utente e gruppi
* Installazione del pacchetto software
* Accesso tramite CRM

### Impostare le autorizzazioni

Gli utenti che installano il software devono disporre delle autorizzazioni necessarie per installare i pacchetti Salesforce.

Per accedere all&#39;applicazione, gli utenti devono avere un ruolo con l&#39;autorizzazione **Sales Insights:View Sales Insights**.

Se si desidera limitare gli utenti solo a [!DNL In-CRM Insights]:

1. Crea un [ruolo personalizzato](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/accounts/buying-groups/default-custom-roles#create-a-custom-role) e assegnagli l&#39;autorizzazione **Sales Insights: View Sales Insights**.
1. Crea un nuovo [gruppo utenti](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/admin/user-management#create-user-group).
1. Aggiungi un profilo di prodotto Experience Platform al gruppo.

### Installare il pacchetto

Per installare il pacchetto In-CRM Insights, segui i passaggi per Salesforce o Microsoft Dynamics.

#### Salesforce

1. Scarica il pacchetto di installazione di [In-CRM Insights](https://experience.adobe.com/solutions/OneAdobe-sales-workflow-optimizer-sales-insight-ui/install/sales-insight?crm=salesforce).
1. Dopo l&#39;accesso, si viene reindirizzati alla pagina di installazione del pacchetto.
1. Selezionare l&#39;opzione **[!UICONTROL Installa per tutti gli utenti]** e fare clic su **[!UICONTROL Installa]**.

   ![Installare il pacchetto Approfondimenti in-CRM](assets/incrm-install-sf.png){width=500}

1. Approva l&#39;accesso di terze parti nella finestra di dialogo, quindi fai clic su **[!UICONTROL Continua]**.
1. Al termine dell&#39;installazione, fare clic su **[!UICONTROL Fine]**.

   Ora è elencato nella pagina **Pacchetti installati** e **Journey Optimizer B2B edition** è elencato nell&#39;Utilità di avvio app.

   ![Informazioni in-CRM configurate in Salesforce](assets/in-crm-install-sf-done.png){width=800 zoomable="yes"}

#### MS Dynamics

1. Scarica il pacchetto di installazione di [In-CRM Insights](https://experience.adobe.com/solutions/OneAdobe-sales-workflow-optimizer-sales-insight-ui/install/sales-insight?crm=dynamics).
1. Passare alla [porta Power Apps](https://make.powerapps.com/){target=_blank}.
1. Dopo aver effettuato l&#39;accesso, selezionare l&#39;ambiente per il pacchetto, quindi passare a **[!UICONTROL Soluzioni]** dal menu a sinistra.
1. Fare clic su **[!UICONTROL Importa soluzione]**.
1. Individua e carica il pacchetto di installazione, quindi fai clic su **[!UICONTROL Avanti]**.
1. Verificare i dettagli del pacchetto e fare clic su **[!UICONTROL Avanti]**.
1. In _Variabili di ambiente_, verificare che il valore sia impostato su `prod` (non modificare il valore) e fare clic su **[!UICONTROL Importa]**.
1. Al termine dell&#39;installazione, nella barra di navigazione a sinistra vengono visualizzati **[!UICONTROL Journey Optimizer B2B edition]** > **[!UICONTROL Buying groups]**.

   ![Informazioni in-CRM disponibili in Microsoft Dynamics](assets/incrm-ms-install-done.png){width=800 zoomable="yes"}

## Visualizza i gruppi di acquisto

Segui le istruzioni per accedere al tuo account Adobe. I gruppi di acquisto sono caricati e disponibili per la visualizzazione.

Dopo aver selezionato un gruppo di acquisto, puoi sfogliare i [dettagli gruppo](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/accounts/sales-experience/buying-group-details#). È lo stesso dei dati e delle informazioni visualizzati in Journey Optimizer B2B edition, ma i dati sono di sola lettura tramite [!DNL In-CRM Insights].
