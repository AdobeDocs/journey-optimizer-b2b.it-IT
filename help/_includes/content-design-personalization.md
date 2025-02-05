---
title: Authoring dei contenuti - personalizzazione
description: Sezione riutilizzata sull’utilizzo della personalizzazione per l’authoring dei contenuti
source-git-commit: 3791beb98068a56882bb0a96fbc6b192e85130bb
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 2%

---

# Authoring dei contenuti - personalizzazione

Journey Optimizer B2B edition utilizza una sintassi inline semplice che consente di creare espressioni con contenuto personalizzato racchiuso tra parentesi graffe `{}`. È possibile aggiungere più espressioni nello stesso contenuto o campo senza restrizioni.

Esempi:

* `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}`

* `Hello {{profile.person.name.fullName}}`

Durante l’elaborazione del contenuto, Journey Optimizer B2B edition sostituisce l’espressione con i dati contenuti nel database Experience Platform. Il primo esempio diventa _Hello John Doe_.

L’esempio seguente illustra i passaggi per personalizzare il contenuto utilizzando gli attributi lead/account e i token di sistema.

1. Seleziona il componente testo e fai clic sull&#39;icona _Aggiungi personalizzazione_ nella barra degli strumenti.

   ![Fare clic sull&#39;icona Personalizza](../assets/content-design-shared/visual-designer-personalize-icon.png){width="600"}

   Questa azione apre la finestra di dialogo _Modifica Personalization_.

1. Fare clic su **+** o **...** per aggiungere un token allo spazio vuoto.

   ![Creare testo personalizzato utilizzando token](../assets/content-design-shared/visual-designer-personalize-dialog.png){width="700" zoomable="yes"}

1. Fai clic su **[!UICONTROL Salva]**.
