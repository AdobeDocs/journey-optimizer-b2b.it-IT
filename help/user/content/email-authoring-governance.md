---
title: Autore da un modello gestito
description: Scopri come utilizzare l’authoring delle e-mail con un modello gestito che contiene componenti di contenuto bloccati.
feature: Email Authoring, Content
source-git-commit: d7e2b7673b0a6709d2841893d87617e580b62298
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 1%

---

# Autore da un modello gestito

I progettisti di contenuti possono abilitare [la governance (_il blocco del contenuto_)](./template-content-governance.md) durante la creazione di modelli di posta elettronica. Le funzioni di governance consentono di designare le parti della progettazione che non possono essere modificate quando vengono utilizzate in un percorso di conti. Quando [selezioni un modello salvato](./email-authoring.md#select-a-template) per creare un&#39;e-mail, la finestra di progettazione visiva carica il modello in modo che tu possa utilizzarlo come base per l&#39;e-mail.

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
