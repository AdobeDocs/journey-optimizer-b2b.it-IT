---
title: Authoring dei contenuti - personalizzazione
description: Sezione riutilizzata sull’utilizzo della personalizzazione per l’authoring dei contenuti
source-git-commit: fee5bddcce11b3035da6ab93b18bcc7006b4b554
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 0%

---

# Authoring dei contenuti - personalizzazione

Journey Optimizer B2B edition utilizza una sintassi semplice in linea che consente di creare espressioni con contenuto personalizzato racchiuso tra parentesi graffe `{{}}`. È possibile aggiungere più espressioni nello stesso contenuto o campo senza restrizioni.

Ad esempio, è possibile aggiungere un&#39;espressione di personalizzazione come `Hello {{lead.firstName}} {{lead.lastName}}`. Durante l’elaborazione del contenuto, Journey Optimizer B2B edition sostituisce l’espressione con i dati contenuti nel database di Experience Platform. Il primo esempio diventa _Hello John Doe_.

Consulta [Personalizzazione dei contenuti](../user/content/personalization.md) per informazioni più complete sull&#39;utilizzo degli strumenti di personalizzazione in Journey Optimizer B2B edition.

>[!NOTE]
>
>Journey Optimizer B2B edition segue la sintassi _camel case_ per i token di personalizzazione nelle e-mail in modo che corrispondano alle altre applicazioni Adobe Experience Platform per un&#39;esperienza coerente. Questo formato di token è completamente compatibile con il linguaggio di modelli [Handlebars](https://handlebarsjs.com/guide/#what-is-handlebars){target="_blank"}. Tutti i token aggiunti prima di questa modifica vengono aggiornati automaticamente.

L’esempio seguente illustra i passaggi per personalizzare il contenuto utilizzando token di persona e di sistema. Riflette le modifiche disponibili per gli ambienti Journey Optimizer B2B edition per i quali è stato eseguito il provisioning nell&#39;[architettura semplificata](../user/simplified-architecture.md).

1. Seleziona il componente testo e fai clic sull&#39;icona _Aggiungi personalizzazione_ ( ![Aggiungi icona personalizzazione](../assets/do-not-localize/icon-personalization-field.svg) ) nella barra degli strumenti.

   ![Fare clic sull&#39;icona Personalizza](../assets/content-design-shared/visual-designer-personalize-icon.png){width="600"}

   Questa azione apre la finestra di dialogo _Modifica Personalization_.

1. Aggiungere un token facendo clic sul simbolo più ( **+** ) accanto a esso.

   Se desideri aggiungere il token con un fallback (testo predefinito che viene visualizzato quando tale campo non è disponibile per un lead), fai clic sull&#39;icona _Altro_ ( **...** ) e scegli **[!UICONTROL Inserisci con testo di fallback]**.

   ![Creare testo personalizzato utilizzando token](../assets/content-design-shared/visual-designer-personalize-dialog-handlebar.png){width="700" zoomable="yes"}

1. Aggiungi eventuali altri token o altro testo statico da includere.

1. Fai clic su **[!UICONTROL Salva]**.

   Lo script di personalizzazione viene visualizzato nello spazio di progettazione visiva. Puoi selezionarla per apportare modifiche quando necessario.

   ![Seleziona script di personalizzazione](../assets/content-design-shared/visual-designer-select-personalization-script.png){width="600"}
