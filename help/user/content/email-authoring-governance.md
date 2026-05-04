---
title: Autore da un modello gestito
description: 'Creazione di e-mail da modelli governati con contenuto bloccato: identifica le aree modificabili e lavora entro i vincoli di governance in Journey Optimizer B2B edition.'
feature: Email Authoring, Content
role: User
exl-id: 1af996a6-a010-4899-96e9-bad76f93865c
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: e666e996-b2cf-4c45-8fc2-1c625212abab
subfeature_v2: id: adfaa694-5e52-4b2d-8c6b-20a18ae4b51bid: e7bdffdc-2950-4be5-8c23-84240a995090
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adebid: f5c2a4bb-71ca-4d7e-8efd-442250e6ba48
autotag-review: '2026-03-30T22:35:16.900Z'
source-git-commit: 8fe8318d7e1c63cbaa2749fc3928eb0a12967bd9
workflow-type: tm+mt
source-wordcount: 277
ht-degree: 1%

---

# Autore da un modello gestito

I progettisti di contenuti possono abilitare [la governance (_il blocco del contenuto_)](./template-content-governance.md) durante la creazione di modelli di posta elettronica. Le funzioni di governance consentono di designare le parti della progettazione che non possono essere modificate quando vengono utilizzate in un percorso di conti. Quando [selezioni un modello salvato](./email-authoring.md#select-a-template) per creare un&#39;e-mail, lo spazio di progettazione visiva carica il modello in modo che tu possa utilizzarlo come base per l&#39;e-mail.

Se la governance del modello è abilitata, nel pannello delle proprietà a destra viene visualizzato un avviso. Puoi attivare le **[!UICONTROL aree modificabili evidenziate]** nella parte superiore dell&#39;area di lavoro per vedere quali componenti ed elementi di contenuto sono modificabili per l&#39;utilizzo nel percorso.

![Visualizzare le aree modificabili in un modello gestito](./assets/email-designer-governed-highlight.png){width="800" zoomable="yes"}

È inoltre possibile determinare gli elementi bloccati o modificabili utilizzando la _struttura di spostamento_. Fai clic sull&#39;icona _Struttura di navigazione_ ( ![Icona collegamento](../assets/do-not-localize/icon-navigation-tree.svg) ) a sinistra dell&#39;area di lavoro per visualizzare la struttura.

![Visualizzare le aree modificabili in un modello gestito](./assets/email-designer-governed-tree.png){width="600" zoomable="yes"}

Le icone indicano le impostazioni di blocco del contenuto applicate.

| Icona | Nome | Descrizione |
|------|------|-------------|
| ![Icona di sola lettura](../assets/do-not-localize/icon-tree-lock.svg) | Sola lettura | Il componente è bloccato e non può essere modificato. Se applicati al livello principale (_[!UICONTROL Corpo]_), tutti i componenti figlio sono bloccati e non possono essere modificati. |
| ![Icona modifica contenuto](../assets/do-not-localize/icon-tree-content-lock.svg) | Blocco del contenuto | Il blocco del contenuto viene applicato a livello di componente. |
| ![Icona Modificabile](../assets/do-not-localize/icon-edit.svg) | Modificabile | Il componente è completamente modificabile. Tuttavia, potrebbe non essere possibile eliminare l’elemento. |
| ![Icona modifica contenuto](../assets/do-not-localize/icon-tree-edit-text.svg) | Modificabile - solo contenuto | Il componente e lo stile sono statici, ma è possibile modificarne il contenuto (ad esempio testo o immagine). |
