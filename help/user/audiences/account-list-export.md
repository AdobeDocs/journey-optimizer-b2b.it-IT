---
title: Esportazione di account
description: Esporta elenchi di account filtrati in CSV per piattaforme di terze parti con gruppi acquisti e filtri di punteggio di coinvolgimento in Journey Optimizer B2B edition.
feature: Audiences
role: User
exl-id: 3ec8e8fd-1bc2-4efa-840f-f06520099060
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: e935834c-48b7-43d8-b754-a815196a1b05
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
autotag-review: 2026-03-30T19:51:33.392Z
TQID: https://experienceleague.adobe.com/fvkVLjO9oIF7hOuoqdSS-jU4wAvsrPnKp1fIabH-Ewk
source-git-commit: 9baf03a1ddc1733385b0398ffadde8f548c431cc
workflow-type: tm+mt
source-wordcount: 261
ht-degree: 100%

---

# Esportazione di account

Utilizza la funzione _Esporta account_ per esportare tutti gli account o un set di account in base al filtro definito. Il processo di esportazione genera un file CSV e invia l’URL del file memorizzato all’interno di una notifica Pulse. Puoi utilizzare questa funzione per spostare gli account in piattaforme di terze parti quando necessario.

1. In Journey Optimizer B2B edition, passa a **[!UICONTROL Account]** > **[!UICONTROL Gruppi acquisti]** nel menu di navigazione a sinistra.

1. Fai clic sulla scheda **[!UICONTROL Sfoglia]**.

1. Fai clic su **[!UICONTROL Esporta account]** in alto a destra.

   ![Modificare i dettagli dell’account](./assets/export-accounts.png){width="800" zoomable="yes"}

1. Nella finestra di dialogo, definisci i parametri dei tipi di pubblico di account da esportare.

   ![Specificare il filtro per pubblico di account](./assets/export-accounts-dialog.png){width="400"}

   Per il **[!UICONTROL Punteggio di coinvolgimento]**, l’operatore `Between` è inclusivo, così come gli intervalli di percentuale. Ad esempio, 5.1 e 5 sono entrambi _tra_ 5 e 6.

   I parametri di filtro vuoti vengono trattati come `Is Any`.

1. Fai clic su **[!UICONTROL Esporta account]** per generare il file CSV utilizzando i filtri specificati.

1. Quando ricevi la notifica del completamento dell’esportazione, fai clic sul collegamento di notifica per accedere al file CSV.

   ![Fare clic sulla notifica per scaricare il file CSV dell’elenco degli account esportati](./assets/export-accounts-notification.png){width="425"}

   >[!NOTE]
   >
   >Se disponi di un abbonamento per le notifiche e-mail configurato nelle preferenze dell’account utente di Adobe, potrebbe trattarsi di una notifica e-mail.

   La pagina dell’applicazione reindirizza alla scheda Sfoglia del _Gruppo acquisti_ e la finestra di dialogo del sistema per il salvataggio del file, richiede di salvare tale file nel sistema. Se è necessario condividere i dati, è possibile utilizzare il sistema di condivisione file del team.
