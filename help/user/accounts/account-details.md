---
title: Dettagli account
description: Visualizza gli approfondimenti dell’account con riepiloghi IA IA, rilevamento intento, analisi della copertura dei contatti e comunicazioni e-mail in Journey Optimizer B2B edition.
feature: Account Insights
role: User
exl-id: 12be33de-0a43-43d9-90b8-fe4411a50599
source-git-commit: 2a676f3cbeb43616a75fa3fa6eb9106230b9fb40
workflow-type: tm+mt
source-wordcount: '639'
ht-degree: 5%

---

# Dettagli dell’account

Quando si fa clic sul nome di un account in un punto qualsiasi di Journey Optimizer B2B edition, viene visualizzata la pagina _Dettagli account_. Questa pagina fornisce informazioni utili sull’account, inclusi i riepiloghi generativi di IA. Sono inoltre disponibili [azioni](#account-actions) che è possibile eseguire per i contatti associati all&#39;account.

![Accedi ai dettagli dell&#39;account](./assets/account-details.png){width="700" zoomable="yes"}

Utilizza la scheda **[!UICONTROL Panoramica]** per esaminare le informazioni sull&#39;account e la scheda **[!UICONTROL Contatti]** per accedere a un elenco dei contatti dell&#39;account.

## Scheda [!UICONTROL Panoramica]

La pagina dei dettagli dell’account è composta da tre sezioni principali:

### Panoramica dell’account

![Panoramica account](./assets/details-page-account-overview.png){zoomable="yes"}

La sezione Panoramica account include le seguenti informazioni sull&#39;account:

* Nome account
* Numero di persone nell’account
* Settore
* Opportunità aperte
* I tre percorsi di account più recenti in cui l&#39;account è attualmente in uso (fare clic sul nome del percorso per aprire la [panoramica percorso](../journeys/journeys-overview.md))
* Riepilogo IA generativo dell’account, che include informazioni sui principali gruppi di acquisto coinvolti.

### Dati di intento

In Journey Optimizer B2B edition, il modello di rilevamento intento (Intent Detection) prevede una soluzione o un prodotto di interesse con sufficiente affidabilità in base all’attività di contatto dell’account. L’intento dei contatti del conto può essere interpretato come la probabilità di avere interesse in un prodotto.

{{intent-data-note}}

![Dati intento - Dettagli account](./assets/intent-data-panel.png){width="700" zoomable="yes"}

* Livelli di intento
* Tipi di segnale di intento: parole chiave, prodotto e soluzione


### Copertura contatti

![Copertura contatti account](./assets/details-page-contact-coverage.png){width="800" zoomable="yes"}

Nella sezione _[!UICONTROL Copertura dei contatti]_ viene visualizzato il numero di contatti dell&#39;account con un ruolo specifico associato a un interesse della soluzione. L’assegnazione del ruolo e dell’interesse nella soluzione si basa sul modello dei ruoli del gruppo di acquisto. Fare clic su una cella per visualizzare i dettagli seguenti:

* Descrizione, nel formato seguente: _x persone hanno il ruolo y per l&#39;interesse della soluzione z_
* Colonne
* Nome
* Account
* Posizione lavorativa
* Gruppo acquisti
* Punteggio di coinvolgimento della persona
* Ultima attività
* Dettagli

Fai clic sull&#39;icona _Filtro_ ( ![Icona Filtro](../assets/do-not-localize/icon-filter.svg) ) in alto a sinistra per filtrare la visualizzazione dei dati utilizzando uno dei seguenti attributi:

* Soluzione di interesse
* Periodo di tempo

### Sovrapposizione contatti

![Sovrapposizione contatti account](./assets/details-page-contact-overlap.png){width="800" zoomable="yes"}

Nella sezione _[!UICONTROL Sovrapposizione contatti]_ vengono visualizzati i contatti dell&#39;account che fanno parte di più gruppi di acquisto in seguito all&#39;associazione a diversi interessi della soluzione. Queste informazioni sono sotto forma di una tabella con le seguenti colonne:

* Nome
* Posizione lavorativa
* Account
* Soluzione di interesse

Fai clic su _Informazioni_ ( ![Icona informazioni](../assets/do-not-localize/icon-info.svg) ) accanto al nome del contatto per visualizzare una tabella con i dettagli seguenti:

* Gruppo di acquisto (fare clic sul nome per aprire [dettagli gruppo di acquisto](../buying-groups/buying-group-details.md))
* Ruolo
* Soluzione di interesse
* Intento prodotto (se [configurato](../admin/intent-data.md))
* Prodotto

Fai clic sull&#39;icona _Filtro_ ( ![Icona Filtro](../assets/do-not-localize/icon-filter.svg) ) in alto a sinistra per filtrare la visualizzazione dei dati utilizzando uno dei seguenti attributi:

* Soluzione di interesse
* Ruoli

## Scheda [!UICONTROL Contatti]

Seleziona la scheda **[!UICONTROL Contatti]** per visualizzare un elenco di tutte le persone associate all&#39;account, che viene sincronizzato in Experience Platform. Ogni contatto elencato include il nome, l’indirizzo e-mail e il punteggio di coinvolgimento.

![Dettagli account - Scheda Contatti](./assets/account-details-contacts-tab.png){width="700" zoomable="yes"}

## Invia e-mail

Puoi inviare un’e-mail approvata dall’addetto al marketing a uno o più contatti selezionati (fino a 50 alla volta) o a tutti i contatti dell’account. L’elenco delle e-mail disponibili è limitato alle e-mail approvate dall’istanza di Marketo Engage connessa.

>[!BEGINTABS]

>[!TAB Tutti i contatti account]

1. Dalla scheda _[!UICONTROL Panoramica]_, fai clic su **[!UICONTROL Invia e-mail]** in alto a destra.

   ![Dettagli account - Seleziona e-mail](../accounts/assets/account-details-send-email.png){width="700" zoomable="yes"}

1. Nella finestra di dialogo _[!UICONTROL Invia e-mail]_, seleziona l&#39;area di lavoro di Marketo Engage, quindi seleziona la casella di controllo per l&#39;e-mail che desideri inviare.

   ![Selezionare un&#39;e-mail da inviare ai membri del gruppo di acquisto](../accounts/assets/account-details-send-email-dialog.png){width="700" zoomable="yes"}

1. Fai clic su **[!UICONTROL Invia]**.

>[!TAB Contatti selezionati]

1. Nella scheda _[!UICONTROL Contatti]_ selezionare le caselle di controllo relative ai contatti ai quali si desidera inviare l&#39;e-mail.

1. In alto a destra o nella barra di selezione in basso, fai clic su **[!UICONTROL Invia e-mail]**.

   ![Scheda Membri - Invia e-mail](../accounts/assets/account-details-send-email-selections.png){width="700" zoomable="yes"}

1. Nella finestra di dialogo _[!UICONTROL Invia e-mail]_, seleziona l&#39;area di lavoro di Marketo Engage, quindi seleziona la casella di controllo per l&#39;e-mail che desideri inviare.

   ![Selezionare un&#39;e-mail da inviare ai membri del gruppo di acquisto](../accounts/assets/account-details-send-email-dialog.png){width="700" zoomable="yes"}

1. Fai clic su **[!UICONTROL Invia]**.

>[!ENDTABS]
