---
title: Reinserimento percorso
description: Controlla quando e con quale frequenza gli account o le persone possono reinserire lo stesso account o percorso di persone.
feature: Account Journeys
role: User
level: Intermediate
exl-id: e5153125-6d5b-4835-bd19-c9b7ce67e46a
autotag-review: '2026-08-14T19:11:15.391Z'
TQID: 'https://experienceleague.adobe.com/BabVdaLaAwER8tEQLOAjChwyy4WI2Cle19-Uu-varIc'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
    internal-label: Journey Optimizer B2B Edition
feature_v2:
  - id: a4b836d9-ffdd-4df3-a62a-f78b830cf059
    internal-label: Journeys
subfeature_v2:
  - id: c31bc6c7-76bc-467b-80c0-7315a4e3f6be
    internal-label: Account Journeys
  - id: ba367494-9862-4596-bd6f-299c7e10a46b
    internal-label: Person Journeys
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
topic_v2:
  - id: d00e9f03-e50b-4162-b143-0c0817c937c2
    internal-label: Customer journeys
source-git-commit: 07717d3ba2d67a61e3dcfa4693e2ee2e151e78da
workflow-type: tm+mt
source-wordcount: '667'
ht-degree: 1%
---
# Reinserimento percorso

Quando abiliti il reinserimento per un percorso, puoi controllare quando e con quale frequenza un account o una persona può reinserirsi nello stesso percorso. Utilizzare le impostazioni di reinserimento per impostare criteri, limiti e tempi di attesa in modo che gli account o le persone possano riqualificarsi per il percorso in modo controllato.

Un account o una persona può riqualificarsi per un percorso quando sono soddisfatte le seguenti condizioni:

* L&#39;account o la persona rientra nel numero di rientri consentiti per il percorso.
* L’account o la persona ha raggiunto la soglia del tempo di attesa (il tempo minimo di attesa prima della riqualificazione).
* L&#39;account o la persona non è attualmente nel percorso.

## Abilita reinserimento per un percorso

È possibile abilitare il reinserimento e modificare le impostazioni di reinserimento quando il percorso è in stato _Bozza_.

>[!BEGINTABS]

>[!TAB percorso account]

1. Aprire il percorso di conti provvisori.

1. Fai clic sul menu **[!UICONTROL Altro...]** in alto a destra e scegli **[!UICONTROL Rientro]**.

   ![Fai clic su Altro in alto a destra in un percorso di account](./assets/account-journey-draft-more-menu.png){width="450"}

1. Nella finestra di dialogo _[!UICONTROL Rientro Percorso]_, attiva l&#39;opzione **[!UICONTROL Abilita rientro]**.

   Quando la funzione è attivata, vengono visualizzate le opzioni per la temporizzazione, il ritardo e i limiti.

   ![Finestra di dialogo di reinserimento Percorso per un percorso di account con funzionalità abilitata](./assets/journey-re-entry-dialog-enabled.png){width="450"}

1. Per **[!UICONTROL Intervallo di rientro]**, scegliere la modalità di calcolo dell&#39;attesa:

   * **[!UICONTROL Attesa dalla fine del percorso]** - Il periodo di attesa inizia quando l&#39;account esce o completa il percorso. Ad esempio, &quot;30 giorni dopo il completamento del percorso, l’account può reinserirsi.&quot;

   * **[!UICONTROL Attesa dall&#39;inizio del percorso]** - Il periodo di attesa si basa sul momento in cui l&#39;account è entrato per la prima volta nel percorso. Ad esempio, &quot;30 giorni dopo l’inizio del percorso, l’account può rientrare.&quot;

1. Imposta il **[!UICONTROL ritardo rientro]**, che è la durata dell&#39;attesa in ore o giorni.

   Questa impostazione determina quanto tempo un account deve attendere dopo essere uscito o aver avviato il percorso prima di poter rientrare.

1. Per definire il numero massimo di volte in cui un account può entrare nel percorso, impostare il **[!UICONTROL limite di ingresso]**.

   Quando un account raggiunge il limite, non è più idoneo per l’ingresso fino a quando il limite non viene reimpostato o il percorso non viene ripubblicato con un nuovo limite.

   Questo limite si applica per ogni account di quel percorso.

1. Fai clic su **[!UICONTROL Salva]**.

>[!TAB percorso di persone]

1. Aprire il percorso di persone in bozza.

1. Fai clic sul menu **[!UICONTROL Altro...]** in alto a destra e scegli **[!UICONTROL Impostazioni reinserimento]**.

   ![Fai clic su Altro in alto a destra nel percorso di persone](./assets/person-journey-draft-more-menu.png){width="450"}

1. Nella finestra di dialogo _[!UICONTROL Rientro Percorso]_, attiva l&#39;opzione **[!UICONTROL Abilita rientro]**.

   Quando la funzione è attivata, vengono visualizzate le opzioni per la temporizzazione, il ritardo e i limiti.

   ![Finestra di dialogo di rientro Percorso per un percorso di persone con funzionalità abilitata](./assets/person-journey-re-entry-dialog.png){width="450"}

1. Per **[!UICONTROL Intervallo di rientro]**, scegliere la modalità di calcolo dell&#39;attesa:

   * **[!UICONTROL Attesa dalla fine del percorso]** - Il periodo di attesa inizia quando la persona esce dal percorso o lo completa. Ad esempio, &quot;30 giorni dopo che la persona ha completato il percorso, può rientrare.&quot;

   * **[!UICONTROL Attesa dall&#39;inizio del percorso]** - Il periodo di attesa si basa su quando la persona è entrata per la prima volta nel percorso. Ad esempio, &quot;30 giorni dopo l’inizio del percorso, la persona può rientrare.&quot;

1. Imposta il **[!UICONTROL ritardo rientro]**, che è la durata dell&#39;attesa in ore o giorni.

   Questa impostazione determina quanto tempo una persona deve attendere dopo l’uscita o l’avvio del percorso prima di poter rientrare.

1. Per definire il numero massimo di accessi al percorso consentito a una persona, impostare il **[!UICONTROL limite di ingressi]**.

   Quando una persona raggiunge il limite, non è più idonea per l’ingresso fino a quando il limite non viene reimpostato o il percorso viene ripubblicato con un nuovo limite.

   Questo limite si applica a persona per quel percorso.

1. Fai clic su **[!UICONTROL Salva]**.

>[!ENDTABS]

## Progressione e attività

Per un account o un percorso di persone pubblicato, nell&#39;area di lavoro del percorso viene visualizzato [progressione](./journeys-overview.md#review-account-progression) per i nodi del percorso. Ogni nodo visualizza il numero di account o persone che devono raggiungere il nodo e, per i percorsi live, il numero attualmente presente in tale nodo. Ogni volta che un account o una persona viene reinserito in un percorso, viene conteggiato come voce distinta.

<!-- 
You can see how many times accounts have entered the journey. ?? 

When you drill in to [account details](../accounts/account-details.md), the account activity shows each time the account entered the journey. It includes explicit activity and a recurrence count so that you can see re-entries clearly.
-->
