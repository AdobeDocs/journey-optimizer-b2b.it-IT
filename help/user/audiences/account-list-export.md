---
title: Esportare l’elenco account
description: Scopri come esportare l’elenco account in base al filtro dei gruppi acquisti.
feature: Account Lists
role: User
exl-id: 3ec8e8fd-1bc2-4efa-840f-f06520099060
source-git-commit: 4a54548ad061fc778fae3bc4b8499f3716850e4a
workflow-type: ht
source-wordcount: '253'
ht-degree: 100%

---

# Esportare l’elenco account

Utilizza la funzione _Esporta elenco account_ per esportare tutti gli account o un set di account in base al filtro definito. Il processo di esportazione genera un file CSV e invia l’URL del file memorizzato all’interno di una notifica Pulse. Puoi utilizzare questa funzione per spostare gli account in piattaforme di terze parti quando necessario.

1. In Journey Optimizer B2B edition, passa a **[!UICONTROL Account]** > **[!UICONTROL Gruppi acquisti]** nel menu di navigazione a sinistra.

1. Fai clic sulla scheda **[!UICONTROL Sfoglia]**.

1. Fai clic su **[!UICONTROL Esporta account]** in alto a destra.

   ![Modificare i dettagli dell’account](./assets/export-accounts.png){width="800" zoomable="yes"}

1. Nella finestra di dialogo, definisci i parametri dei tipi di pubblico dell’account da esportare.

   ![Specificare il filtro del pubblico dell’account](./assets/export-accounts-dialog.png){width="400"}

   Per il **[!UICONTROL Punteggio di coinvolgimento]**, l’operatore `Between` è inclusivo, così come gli intervalli di percentuale. Ad esempio, 5.1 e 5 sono entrambi _tra_ 5 e 6.

   I parametri di filtro vuoti vengono trattati come `Is Any`.

1. Fai clic su **[!UICONTROL Esporta account]** per generare il file CSV utilizzando i filtri specificati.

1. Quando ricevi la notifica del completamento dell’esportazione, fai clic sul collegamento di notifica per accedere al file CSV.

   ![Fare clic sulla notifica per scaricare il file CSV dell’elenco degli account esportati](./assets/export-accounts-notification.png){width="425"}

   >[!NOTE]
   >
   >Se disponi di un abbonamento per le notifiche e-mail configurato nelle preferenze dell’account utente di Adobe, potrebbe trattarsi di una notifica e-mail.

   La pagina dell’applicazione reindirizza alla scheda Sfoglia del _Gruppo acquisti_ e la finestra di dialogo del sistema per il salvataggio del file, richiede di salvare tale file nel sistema. Se è necessario condividere i dati, è possibile utilizzare il sistema di condivisione file del team.
