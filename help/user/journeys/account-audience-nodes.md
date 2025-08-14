---
title: Nodi del pubblico dell’account
description: Scopri il tipo di nodo del pubblico di account che puoi utilizzare per definire l’input per i percorsi di account in Journey Optimizer B2B edition.
feature: Account Journeys, Audiences, Account Lists
role: User
exl-id: 288ac5a8-79ed-4654-8ac1-83da2af04f2c
source-git-commit: 82553c9ee6205e0ad47cc5a56112590471c03d0e
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 0%

---


# Nodi del percorso di pubblico dell’account

Il nodo Pubblico account specifica gli account che entrano nel percorso. Quando [crei un percorso di account](./journey-overview.md#create-an-account-journey), il percorso inizia sempre con un nodo di pubblico dell&#39;account che ne definisce l&#39;input.

Utilizzare una delle opzioni di input seguenti per questo nodo di percorso:

* **[Pubblico account](../audiences/account-audience-overview.md)**: il pubblico dell&#39;account rappresenta il pubblico di base che viene sincronizzato dal servizio di segmentazione di Experience Platform.
* **[Elenco account](../accounts/account-lists.md)**: l&#39;elenco account è una raccolta di account denominati utilizzati per l&#39;orchestrazione del percorso di destinazione. Un elenco di conti esegue il targeting dei conti denominati utilizzando criteri definiti, ad esempio settore, ubicazione o dimensione società.

## Impostare il pubblico per il nodo del pubblico dell’account

1. Fai clic sul nodo **[!UICONTROL Pubblico account]**. Questa azione visualizza le proprietà del nodo a destra.

   ![Nodo percorso di destinatari account](./assets/account-journey-account-audience-node.png){width="700" zoomable="yes"}

1. Scegliere il tipo di input per i conti che entrano nel percorso:

   * **[!UICONTROL Pubblico account]**

     Scegli l’opzione Pubblico dell’account. Quindi, fai clic su **[!UICONTROL Aggiungi pubblico account]**.

     Nella finestra di dialogo _[!UICONTROL Aggiungi pubblico]_, seleziona un segmento di pubblico creato in precedenza. Quindi, fai clic su **[!UICONTROL Aggiungi pubblico]**.

     ![Selezionare un segmento di pubblico per il nodo](./assets/node-audience-add-dialog.png){width="700" zoomable="yes"}

   * **[!UICONTROL Elenco account]**

     Scegliere l&#39;opzione dell&#39;elenco dei conti. Fare clic su **[!UICONTROL Aggiungi elenco account]**.

     Nella finestra di dialogo _[!UICONTROL Seleziona elenco account live]_, seleziona un elenco account pubblicato. Quindi fare clic su **[!UICONTROL Salva]**.

     ![Seleziona un elenco di account live per il nodo](./assets/account-journey-account-audience-select-account-list.png){width="700" zoomable="yes"}

     Per ulteriori informazioni sulla creazione e la pubblicazione di elenchi di account, vedere [Elenchi di account](../accounts/account-lists.md).

## Creare un segmento di pubblico

1. Nel menu di navigazione a sinistra, seleziona **[!UICONTROL Account]** > **[!UICONTROL Tipi di pubblico]**.

1. Fai clic su **[!UICONTROL Crea pubblico]** nell&#39;angolo superiore destro.

   ![Crea un segmento di pubblico](./assets/audiences-list-create.png){width="800" zoomable="yes"}

1. Segui i passaggi descritti nella [Guida al servizio di segmentazione](https://experienceleague.adobe.com/it/docs/experience-platform/segmentation/types/account-audiences){target="_blank"}.
