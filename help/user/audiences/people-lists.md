---
title: Elenchi persone
description: Scopri gli elenchi di persone e come sfogliarli, visualizzarli, modificarli, eliminarli e utilizzarli in Journey Optimizer B2B Edition.
feature: Audiences
role: User
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
    internal-label: Journey Optimizer B2B Edition
feature_v2:
  - id: beb5f4be-cec3-471a-9db6-831a77dd3ac9
    internal-label: Audiences
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: ff2b9b37-92e0-45fc-b853-379d44c08c89
    internal-label: Audience segmentation
source-git-commit: d713d57bddf2ac6f8cf7e7a7d163281f607d729c
workflow-type: tm+mt
source-wordcount: '880'
ht-degree: 1%
---

# Elenchi di persone

In [!DNL Journey Optimizer B2B Edition], un elenco persone è una raccolta denominata di profili di persone che puoi riutilizzare nei tuoi percorsi. Invece di ricreare lo stesso set di filtri in ogni percorso, definisci il gruppo di persone una volta e fai riferimento a esso ovunque sia necessario. Ad esempio, utilizza un elenco di persone per escludere personale interno o clienti esistenti da un percorso di cura o per tenere traccia delle persone che hanno completato un passaggio in un percorso in modo che un altro percorso possa agire di conseguenza.

Esistono due tipi di elenchi di persone:

* **[!UICONTROL Statico]** - L&#39;appartenenza cambia solo quando si aggiungono o rimuovono esplicitamente delle persone. Puoi aggiungere persone applicando un set di filtri per compilare l’elenco in base ai dati persona correnti oppure aggiungere e rimuovere persone tramite un account o un percorso di persone. Vedi [Elenchi di persone statiche](./people-lists-static.md).
* **[!UICONTROL Dinamico]** - Definisci un set di regole (filtri) per la cura automatica dell&#39;elenco. L’elenco viene aggiornato in modo dinamico man mano che le persone diventano qualificate o squalificate per la definizione delle regole. Vedi [Elenchi di persone dinamiche](./people-lists-dynamic.md).

È possibile [utilizzare gli elenchi di persone nei percorsi di account e nei percorsi di persone](./people-lists-journeys.md) per suddividere i percorsi in base all&#39;appartenenza agli elenchi e per aggiungere o rimuovere persone dagli elenchi statici.

>[!NOTE]
>
>Gli elenchi Persone includono profili persona già sincronizzati e disponibili in [!DNL Journey Optimizer B2B Edition]. I profili non vengono letti direttamente dai tipi di pubblico [!DNL Adobe Experience Platform] durante la valutazione dell&#39;elenco.

## Accedere e sfogliare gli elenchi di persone {#access-browse}

Accedi agli elenchi delle persone dal menu di navigazione a sinistra per visualizzare, creare e gestire l’iscrizione agli elenchi.

>[!AVAILABILITY]
>
>Le seguenti autorizzazioni del prodotto controllano l’accesso agli elenchi di persone:
>
>* [!UICONTROL Gestisci elenchi persone B2B] - Visualizza, crea, modifica ed elimina gli elenchi di persone.
>* [!UICONTROL Visualizza elenchi di persone B2B] - Visualizza gli elenchi di persone e dei relativi membri (sola lettura).
>
>Per informazioni sull&#39;assegnazione delle autorizzazioni, vedere [Accesso utente e autorizzazioni](../admin/user-management.md#b2b-product-permissions).

* Nella barra di navigazione a sinistra, espandi **[!UICONTROL Account]** e seleziona **[!UICONTROL Elenchi persone]**.

* Seleziona **[!UICONTROL Elenchi dinamici]** o **[!UICONTROL Elenchi statici]** per passare da un tipo di elenco all&#39;altro.

* Immettere il testo nel campo _Ricerca_ nella parte superiore dell&#39;elenco per filtrare l&#39;elenco visualizzato in base al nome.

  ![Accedi agli elenchi di persone per gestire i tipi di pubblico a livello di persona](./assets/people-lists-browse-search.png){width="800" zoomable="yes"}

* Fai clic sull&#39;icona _Impostazioni colonna_ ( ![Icona Impostazioni colonna](../assets/do-not-localize/icon-column-settings-new.svg) ) nell&#39;angolo in alto a destra per selezionare o deselezionare le colonne visualizzate.

* Per modificare la larghezza di una colonna, trascinare il divisore tra le intestazioni di colonna.

Ogni scheda include le colonne **[!UICONTROL Nome]**, **[!UICONTROL Ultimo aggiornamento]**, **[!UICONTROL Aggiornato da]**, **[!UICONTROL Creato il]** e **[!UICONTROL Creato da]**. Fare clic sul nome dell&#39;elenco persone per visualizzarne i dettagli.

Da questa pagina è inoltre possibile:

* Creare nuovi elenchi dinamici e statici.
* Aprire un elenco e [rivedere i membri correnti](#view-list-members).
* Fai clic sull&#39;icona _Altre azioni_ ( **...** ) per un elenco e scegli di [modificarlo](#edit-list-properties) o [eliminarlo](#delete-people-list).

## Creare un elenco di persone {#create-people-list}

1. Fai clic su **[!UICONTROL Crea elenco]** in alto a destra della pagina _[!UICONTROL Elenchi persone]_.

   ![Finestra di dialogo Crea elenco persone](./assets/people-list-create-dialog.png){width="450"}

1. Immetti un **[!UICONTROL Nome]** (obbligatorio) e una **[!UICONTROL Descrizione]** (facoltativo) per l&#39;elenco.

   Il nome può contenere fino a 180 caratteri e deve essere univoco tra gli elenchi dello stesso tipo. La descrizione può contenere fino a 2.000 caratteri.

1. Scegli l&#39;elenco **[!UICONTROL Tipo]**:

   * [**[!UICONTROL Statico]**](./people-lists-static.md) - I filtri di qualificazione determinano l&#39;appartenenza quando vengono applicati all&#39;elenco. L&#39;iscrizione viene aggiornata solo quando si aggiungono manualmente persone o quando un percorso le aggiunge o le rimuove.
   * [**[!UICONTROL Dinamico]**](./people-lists-dynamic.md) - I filtri di qualificazione determinano l&#39;appartenenza in modo dinamico. L&#39;iscrizione viene aggiornata automaticamente.

1. Fai clic su **[!UICONTROL Crea]**.

   Il nuovo elenco persone viene aperto nella relativa pagina dei dettagli e viene aperto l’editor di filtri che consente di definire le persone per l’elenco. Per aggiungere persone a un elenco statico, applica uno o più filtri. Per un elenco dinamico, definisci le regole per l’iscrizione all’elenco.

## Visualizza membri elenco {#view-list-members}

Nella pagina dei dettagli di un elenco persone, l&#39;elenco **[!UICONTROL Membri]** visualizza le persone nell&#39;elenco. Il numero totale di persone nell’elenco viene visualizzato nella parte superiore della tabella.

La tabella dei membri include le colonne riportate di seguito.

* **[!UICONTROL Nome]**
* **[!UICONTROL Indirizzo e-mail]**
* **[!UICONTROL Qualifica]**
* **[!UICONTROL Società]**
* **[!UICONTROL Abbonamento annullato]**
* **[!UICONTROL Creato il]**
* **[!UICONTROL Ultima modifica]**

Per impostazione predefinita, il sistema ordina i membri in base a **[!UICONTROL Ultima modifica]**, mostrando prima le persone modificate più di recente. Puoi anche ordinare per **[!UICONTROL Nome]**, **[!UICONTROL Indirizzo e-mail]** o **[!UICONTROL Creato il]**.

* Per trovare un membro specifico, utilizzare il campo _Ricerca_. Puoi eseguire ricerche per nome, indirizzo e-mail o società.
* Per scegliere le colonne da visualizzare, fare clic sull&#39;icona _Impostazioni colonna_ e selezionare o deselezionare le caselle di controllo. La colonna _[!UICONTROL Name]_ è sempre visualizzata.
* Per visualizzare l&#39;appartenenza più recente, utilizzare il menu _[!UICONTROL Altro]_ per scegliere **[!UICONTROL Aggiorna membri]**.
* Per visualizzare ulteriori informazioni su una persona, fai clic sul nome della persona per aprire la pagina [dettagli persona](../accounts/person-details.md), in cui puoi visualizzare le attività di riepilogo e recenti.

## Modifica proprietà elenco persone {#edit-list-properties}

È possibile modificare il nome e la descrizione di un elenco di persone statiche o dinamiche.

1. Aprire la finestra di dialogo _[!UICONTROL Modifica elenco]_ utilizzando uno dei metodi seguenti:

   * Nella pagina _[!UICONTROL Elenchi persone]_, fai clic sull&#39;icona _Altre azioni_ ( **...** ) per l&#39;elenco e scegli **[!UICONTROL Modifica]**.
   * Nella pagina dei dettagli dell&#39;elenco fare clic su **[!UICONTROL Modifica proprietà elenco]**.

1. Aggiorna **[!UICONTROL Nome]** o **[!UICONTROL Descrizione]**.

1. Fai clic su **[!UICONTROL Salva]**.

## Eliminare un elenco di persone {#delete-people-list}

>[!IMPORTANT]
>
>L’eliminazione di un elenco di persone è permanente e non può essere annullata. Impossibile eliminare un elenco di persone in uso da un percorso attivo.

1. Eliminare l&#39;elenco utilizzando uno dei metodi seguenti:

   * Nella pagina _[!UICONTROL Elenchi persone]_ fare clic sull&#39;icona _Altre azioni_ ( **...** ) accanto al nome dell&#39;elenco e scegliere **[!UICONTROL Elimina]**.
   * Nella pagina dei dettagli dell&#39;elenco fare clic su **[!UICONTROL Elimina elenco]**.

1. Nella finestra di dialogo di conferma, fai clic su **[!UICONTROL Elimina]**.
