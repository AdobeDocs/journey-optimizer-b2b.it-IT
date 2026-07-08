---
title: Gestire il tracciamento delle aperture delle e-mail
description: Disattiva il tracciamento delle aperture delle e-mail per una singola e-mail, oppure acquisisci le preferenze di tracciamento di una persona e utilizza un percorso suddiviso per inviare varianti e-mail di tracciamento e non tracciamento.
feature: Account Journeys, Channels
topic: Content Management
role: User
level: Beginner, Intermediate
autotag-review: '2026-07-08T00:02:50.497Z'
TQID: 'https://experienceleague.adobe.com/LIutoajlpVQTeJP2y4i0Wv7H-WqGj-c-LVsOGfin384'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: a4b836d9-ffdd-4df3-a62a-f78b830cf059
  - id: d6e625c1-468f-4d73-9f32-fd1edb87f96b
  - id: e666e996-b2cf-4c45-8fc2-1c625212abab
  - id: f01b5556-e951-40ba-8625-2e3001864f2b
subfeature_v2:
  - id: ff0c35fa-aa7e-4050-a37c-198fcacd09e6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
source-git-commit: 61481d57fb8eca805d9a9bc545124aed568b5416
workflow-type: tm+mt
source-wordcount: 860
ht-degree: 0%

---

# Gestire il tracciamento delle aperture delle e-mail

Puoi disabilitare il tracciamento aperto per una singola e-mail, oppure acquisire le preferenze di tracciamento di ciascuna persona in Adobe Experience Platform e utilizzare un percorso suddiviso per indirizzare le persone alle varianti e-mail di tracciamento e non tracciamento.

>[!BEGINSHADEBOX &quot;Linee guida CNIL sui pixel di tracciamento e-mail&quot;]

Il 14 aprile 2026 la *Commission Nationale de l&#39;Informatique et des Libertés* (CNIL) ha pubblicato una [raccomandazione sull&#39;uso dei pixel di tracciamento nelle e-mail](https://www.cnil.fr/sites/default/files/2026-04/recommandation-pixels_de_suivi.pdf). La guida chiarisce quando è necessario il consenso ed evidenzia l’importanza di pratiche di consenso appropriate per il tracciamento dei pixel dell’e-mail. Questo criterio potrebbe influire sulle pratiche di invio per qualsiasi entità che distribuisce e-mail agli abbonati con sede in Francia.

Un pixel di tracciamento e-mail è un’immagine trasparente 1x1 incorporata nel HTML di un’e-mail. Quando il client e-mail del destinatario carica l’immagine, il pixel invia un ping a un server che registra dati quali marca temporale, tipo di dispositivo, client e-mail e, a volte, un indirizzo IP per la posizione approssimativa. Tale registro viene quindi associato al record di un destinatario, consentendo agli addetti al marketing di sapere se un’e-mail è aperta.

Le funzionalità del prodotto [!UICONTROL Journey Optimizer B2B edition] qui descritte sono blocchi predefiniti che, configurati e gestiti in modo appropriato, possono supportare un&#39;implementazione conforme. Ciascun cliente è responsabile della determinazione e del rispetto degli obblighi derivanti dalla legge applicabile.

>[!ENDSHADEBOX]

## Disattiva il tracciamento per una singola e-mail {#disable-tracking-single-email}

Utilizza questa opzione quando desideri che un’e-mail specifica non riporti mai l’attività aperta, indipendentemente da chi la riceve.

1. Dal nodo del percorso sulla destra, apri l’e-mail.

1. Nelle proprietà dell&#39;e-mail, seleziona la casella di controllo **[!UICONTROL Disattiva tracciamento aperto]**.

   ![Disabilita tracciamento apertura e-mail](./assets/email-tracking-disable-all.png){width="500" zoomable="yes"}

   Consulta [Definire le impostazioni e-mail](./add-email.md#define-the-email-settings) per l&#39;elenco completo delle proprietà e-mail.

## Segmentare le persone tracciando le preferenze {#segment-people-tracking-preference}

Se desideri consentire a ogni persona di scegliere se tenere traccia delle aperture dei messaggi e-mail, acquisisci tale preferenza come attributo di persona in Adobe Experience Platform (AEP). Puoi utilizzare questo campo in un [modulo pagina di destinazione](./forms.md) in modo che i tuoi contatti abbiano l&#39;opportunità di rinunciare al tracciamento delle aperture delle e-mail. Potrai quindi utilizzare un nodo _Percorsi suddivisi_ nei tuoi percorsi per indirizzare le persone che eseguono il tracciamento e non lo seguono a diverse varianti di e-mail. Questo ti consente di rispettare una rinuncia individuale senza disabilitare il tracciamento aperto per tutti.

Il flusso di lavoro è suddiviso in tre parti:

1. [Aggiungi un campo personalizzato per la preferenza di tracciamento](#add-custom-field-tracking-preference) in AEP e invia una comunicazione di rinuncia con un collegamento a un modulo.
1. [Aggiungi un percorso suddiviso per il tracciamento della rinuncia](#add-split-path-tracking) nel percorso.
1. [Configura le varianti di e-mail di tracciamento e non di tracciamento](#configure-tracking-and-non-tracking-email-variants) per ciascun percorso.

### Aggiungi un campo personalizzato per la preferenza di tracciamento {#add-custom-field-tracking-preference}

>[!NOTE]
>
>L’aggiunta e la mappatura di campi XDM personalizzati è un’attività di amministrazione di Adobe Experience Platform. Per completare questo passaggio, rivolgiti al tuo amministratore AEP o al team di progettazione dati.

1. In AEP, apri lo schema utilizzato per il tuo profilo Persona B2B (ad esempio, _Persona B2B_).

1. Sotto l&#39;ID tenant, individua o crea un gruppo di campi per i campi di gestione del consenso della tua organizzazione (ad esempio, `consents`).

1. Aggiungere un campo al gruppo di campi, ad esempio un campo booleano denominato `emailTracking`, per indicare se la persona ha acconsentito al tracciamento delle aperture.

1. Immettere il nome del campo e il nome visualizzato, impostare il tipo, assegnarlo al gruppo di campi e fare clic su **[!UICONTROL Applica]**.

1. Fai clic su **[!UICONTROL Salva]** per salvare le modifiche allo schema.

   ![Aggiungi il campo emailTracking al gruppo di campi di consenso dello schema di AEP](./assets/email-tracking-xdm-field-aep-schema.png){width="800" zoomable="yes"}

1. Rendi il campo disponibile in [!DNL Journey Optimizer B2B Edition] selezionandolo come _Campo gestito_ per la classe [!UICONTROL Profilo individuale XDM] in [Gestione campi XDM](../admin/xdm-field-management.md#managed-fields).

   ![Seleziona emailTracking come campo gestito nella gestione dei campi XDM](./assets/email-tracking-xdm-field-select.png){width="450"}

   In questo modo il campo è disponibile come condizione nei nodi del percorso diviso.

### Aggiungi un percorso di suddivisione per il tracciamento della rinuncia {#add-split-path-tracking}

Aggiungi un [_Dividi percorsi per persone_ nodo](../journeys/split-merge-paths-nodes.md#split-paths-by-people) al percorso e definisci un percorso per ogni valore di preferenza di tracciamento.

1. Aggiungi un nodo **[!UICONTROL Percorsi suddivisi]** e scegli **[!UICONTROL Persone]** per la suddivisione.

1. Per il primo percorso, applicare una condizione utilizzando il campo delle preferenze di tracciamento personalizzato (ad esempio, `emailTracking` è `true`) per identificare le persone che consentono il tracciamento aperto.

   ![Condizione percorso diviso - aggiungi il campo di tracciamento e-mail come true](./assets/email-tracking-condition-true.png){width="700" zoomable="yes"}

1. Aggiungere un secondo percorso e applicare la condizione inversa (`emailTracking` è `false`) per identificare le persone che hanno rinunciato al tracciamento.

   Per i passaggi generali sull&#39;aggiunta di percorsi, l&#39;applicazione di condizioni e il riordinamento dei percorsi, vedere [Aggiungere un percorso diviso per nodo persone](../journeys/split-merge-paths-nodes.md#add-a-split-path-by-people-node).

   ![Dividi percorso per persone - condizioni di attivazione e disattivazione del tracciamento e-mail](./assets/email-tracking-split-paths.png){width="500" zoomable="yes"}

### Configurare le varianti e-mail di tracciamento e non di tracciamento {#configure-tracking-and-non-tracking-email-variants}

Aggiungi un nodo azione [_[!UICONTROL Invia e-mail &#x200B;]_](./add-email.md) a ogni percorso in modo che ogni persona riceva la variante e-mail che corrisponde alle proprie preferenze di tracciamento.

1. Nel percorso abilitato per il tracciamento, aggiungi un&#39;azione **[!UICONTROL Invia e-mail]** e seleziona o crea l&#39;e-mail come di consueto, lasciando **[!UICONTROL Disabilita tracciamento aperto]** cancellato nelle proprietà e-mail.

1. Nel percorso di rinuncia, aggiungi un&#39;azione **[!UICONTROL Invia e-mail]** utilizzando la stessa e-mail o un&#39;e-mail duplicata, quindi seleziona la casella di controllo **[!UICONTROL Disattiva tracciamento aperto]** nelle proprietà dell&#39;e-mail a destra.

   ![E-mail per tracciamento fuori percorso - disabilita tracciamento aperto](./assets/email-tracking-disable.png){width="600" zoomable="yes"}

1. [Pubblica il percorso](../journeys/create-publish-journey.md#publish-a-journey).

   Le persone vengono instradate automaticamente alla variante e-mail che corrisponde al valore del campo delle preferenze di tracciamento e gli eventuali aggiornamenti apportati alle loro preferenze vengono rispecchiati alla successiva immissione nel percorso.
