---
title: Esporta elenco account
description: Scopri come esportare l’elenco degli account in base al filtro dei gruppi di acquisto.
source-git-commit: c51ee8c8b58e8154c81f6a2ffada3f58a08eb6b4
workflow-type: tm+mt
source-wordcount: '253'
ht-degree: 0%

---

# Esporta elenco account

Utilizza la funzionalità _Esporta elenco account_ per esportare tutti gli account o un set di account in base al filtro definito. Il processo di esportazione genera un file CSV e invia l’URL del file memorizzato all’interno di una notifica Pulse. Puoi utilizzare questa funzione per spostare gli account in piattaforme di terze parti quando necessario.

1. In Journey Optimizer B2B edition, vai a **[!UICONTROL Account]** > **[!UICONTROL Gruppi di acquisto]** nel menu di navigazione a sinistra.

1. Selezionare la scheda **[!UICONTROL Sfoglia]**.

1. Fai clic su **[!UICONTROL Esporta account]** in alto a destra.

   ![Modifica dettagli account](./assets/export-accounts.png){width="800" zoomable="yes"}

1. Nella finestra di dialogo, definisci i parametri dei tipi di pubblico dell’account da esportare.

   ![Specificare il filtro del pubblico dell&#39;account](./assets/export-accounts-dialog.png){width="400"}

   Per il **[!UICONTROL Punteggio di coinvolgimento]**, l&#39;operatore `Between` è inclusivo, così come gli intervalli di percentuali. Ad esempio, 5.1 e 5 sono entrambi _tra_ 5 e 6.

   I parametri di filtro vuoti vengono trattati come `Is Any`.

1. Fai clic su **[!UICONTROL Esporta account]** per generare il file CSV utilizzando i filtri specificati.

1. Quando ricevi la notifica del completamento dell’esportazione, fai clic sul collegamento di notifica per accedere al file CSV.

   ![Fare clic sulla notifica per scaricare il file CSV dell&#39;elenco degli account esportati](./assets/export-accounts-notification.png){width="425"}

   >[!NOTE]
   >
   >Se disponi di un abbonamento per le notifiche e-mail configurato nelle preferenze dell’account utente di Adobe, potrebbe trattarsi di una notifica e-mail.

   La pagina dell&#39;applicazione viene reindirizzata alla scheda Sfoglia di _Gruppo acquisti_ e nella finestra di dialogo Salva file di sistema viene richiesto di salvare il file nel sistema. Se è necessario condividere i dati, è possibile utilizzare il sistema di condivisione file del team.
