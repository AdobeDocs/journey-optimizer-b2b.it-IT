---
title: Informazioni in-CRM
description: Accedi ai gruppi di acquisto di Journey Optimizer B2B edition direttamente in Salesforce. I membri del team di vendita possono visualizzare i dati sul coinvolgimento e identificare le opportunità di vendita grazie a In-CRM Insights.
feature: Sales Insights, Buying Groups
role: User
source-git-commit: de7f5620556a48fe6f12ed1c70e925e11ec770f1
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 0%

---


# Informazioni in-CRM

In-CRM Insights è un’applicazione basata su web che si integra in Salesforce, consentendoti di accedere ai gruppi di acquisto Journey Optimizer B2B edition direttamente all’interno di Salesforce. Identifica le opportunità di incremento del coinvolgimento e del potenziale di vendita.

L&#39;applicazione In-CRM Insights è disponibile nel pacchetto [Marketo Sales Insights](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/marketo-sales-insight/msi-for-salesforce/installation/install-marketo-sales-insight-package-in-salesforce-appexchange).

## Autorizzazioni

Per accedere all&#39;applicazione, gli utenti devono avere l&#39;appartenenza a un ruolo con l&#39;autorizzazione **Sales Insights:View Sales Insights** .

Se desideri limitare un gruppo di utenti a InCRM-Insights, utilizza le seguenti linee guida per creare un ruolo personalizzato specifico per InCRM-Insights:

* Crea un ruolo personalizzato con solo il set di autorizzazioni **Approfondimenti vendite:View Approfondimenti vendite**.
* Crea un nuovo gruppo di utenti, senza aggiungere profili di prodotto.
* Crea un altro gruppo di utenti e aggiungi un profilo di prodotto AEP oppure aggiungi un profilo AEP esistente al gruppo di utenti appena creato.
* Assegnare i nuovi gruppi di utenti al nuovo ruolo e aggiungere nuovi utenti ai nuovi gruppi di utenti.

## Utilizzo di informazioni in-CRM

L’applicazione In-CRM Insights è disponibile in Salesforce tramite l’App Launcher.

1. Fai clic sul modulo di avvio app in Salesforce.
1. Selezionare o cercare `Journey Optimizer B2B Edition`.
1. Nella scheda visualizzata, accedi con le credenziali di Adobe.
1. Scegli una sandbox che ospiti i tuoi Percorsi di account.

I gruppi di acquisto sono caricati e disponibili. I dati sono di sola lettura tramite In-CRM Insights.

>[!NOTE]
>
>Per accedere a Informazioni in-CRM è necessaria l&#39;appartenenza al ruolo di prodotto [Utente vendite B2B](../admin/user-management.md#b2b-built-in-roles).

Dopo aver selezionato un gruppo di acquisto, puoi sfogliare i [dettagli gruppo](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/accounts/sales-experience/buying-group-details#), proprio come in Journey Optimizer B2B edition.
