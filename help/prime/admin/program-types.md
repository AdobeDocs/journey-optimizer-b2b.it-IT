---
title: Tipi di programmi
description: Creazione e gestione di tipi di programmi che definiscono attributi e flussi di stato dei membri per i programmi in Journey Optimizer B2B Prime.
badgeBeta: label="Beta" type="informative" tooltip="Questa funzione è attualmente in versione beta limitata"
autotag-review: '2026-06-23T19:10:36.949Z'
TQID: 'https://experienceleague.adobe.com/gDNLfcAICFtF7M-cB1zJjLih5kL6nUlpYA5zb1aQJv0'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: aed878b8-11d0-487c-828b-d23b2051ec37
  - id: d6e625c1-468f-4d73-9f32-fd1edb87f96b
subfeature_v2:
  - id: f6df9def-cdf7-4728-9ec8-3f65716828c7
  - id: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: ad5a67d291ffef797bb93f8b06f1bd8657efb67f
workflow-type: tm+mt
source-wordcount: 401
ht-degree: 2%

---

# Tipi di programmi

I tipi di programmi definiscono aspetti importanti dei [programmi](../marketing/programs.md) e dei relativi membri e distinguono tra diversi tipi di programmi di marketing. Ogni tipo di programma definisce le seguenti proprietà, che vengono ereditate per i programmi che utilizzano il tipo di programma:

* **Attributi** - Gli attributi descrivono gli aspetti importanti del tipo di programma, ad esempio le date degli eventi e gli attributi di posizione.

* **Flusso di stato del programma** - Ogni stato viene assegnato a un passaggio nel tipo di programma (ad esempio 1, 2 o 3). I membri di un programma possono passare solo da uno stato con lo stesso numero di passaggio (ad esempio, da _Non mostrato_ a _Partecipato_) o a uno stato con un numero di passaggio superiore (ad esempio, da _Invitato_ a _Registrato_).

  Gli stati del programma si escludono a vicenda e sono lineari, pertanto una persona può avere un solo valore di stato per programma. Durante la progettazione degli stati, pensa a quali stati desideri consentire il movimento tra. Ad esempio, se un utente non viene visualizzato per un webinar ma dispone di un&#39;opzione per partecipare in un secondo momento a un evento on demand, può avere lo stesso numero di stato o deve impostarlo su un numero di stato superiore in modo che un membro del programma possa avanzare.

>[!NOTE]
>
>Se un tipo di programma è utilizzato da almeno un programma, non può essere modificato.

_Per definire un tipo di programma personalizzato :_

1. Nella barra di navigazione a sinistra di [!DNL Adobe Journey Optimizer B2B Prime], espandi **[!UICONTROL Amministrazione]** e seleziona **[!UICONTROL Tipi di programma]**.

   ![Accedere all&#39;elenco dei tipi di programma](./assets/program-types-list.png){width="800" zoomable="yes"}

1. Fai clic su **[!UICONTROL Crea tipo]** in alto a destra.

1. Immetti un **[!UICONTROL Nome]** univoco (obbligatorio) e **[!UICONTROL Descrizione]** (facoltativo).

   ![Crea tipo di programma](./assets/program-type-create.png){width="600" zoomable="yes"}

   >[!TIP]
   >
   >L’inclusione di una descrizione è una best practice e rende la libreria dei tipi di programma più gestibile.

1. Fare clic su **[!UICONTROL Crea tipo]**.

1. Aggiungi **[!UICONTROL Attributi]** per il tipo di programma.

   Per ogni attributo che si desidera aggiungere:

   * Fare clic su **[!UICONTROL Aggiungi attributo]**.
   * Scegli il **[!UICONTROL nome API]** e immetti il **[!UICONTROL nome visualizzato]**.
   * Fai clic su **[!UICONTROL Salva]**.

   ![Attributi del tipo di programma](./assets/program-type-attributes.png){width="600" zoomable="yes"}

1. Definisci i passaggi per **[!UICONTROL Stati programma]**.

   Definisci ogni passaggio da includere nel flusso:

   * Fai clic su **[!UICONTROL Aggiungi passaggio]**.
   * Immettere un nome di stato.
   * (Facoltativo) Fai clic su **[!UICONTROL Aggiungi stato]** e immetti un nome di stato aggiuntivo da includere per il passaggio.

   Selezionare la casella di controllo **[!UICONTROL Contrassegna come completata]** per ogni passaggio che si desidera monitorare come esecuzione di un programma completata.

   ![Stati del tipo di programma](./assets/program-type-statuses.png){width="600" zoomable="yes"}

1. Fai clic su **[!UICONTROL Fine]** per salvare le modifiche e tornare all&#39;elenco dei tipi di programma.