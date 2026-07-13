---
title: Authoring di frammenti
description: 'Crea frammenti di contenuto riutilizzabili con strumenti di progettazione visiva: aggiungi struttura, risorse, personalizzazione, contenuto condizionale e tracciamento URL collegato per e-mail e modelli in Journey Optimizer B2B Prime.'
badgeBeta: label="Beta" type="informative" tooltip="Questa funzione fa parte di una versione beta limitata."
autotag-review: '2026-07-13T16:38:09.506Z'
TQID: 'https://experienceleague.adobe.com/Zn5L6Bc3x8SuGyjOPDdTWI-oxrrhk06a2f8ZvX2SN4s'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: aed878b8-11d0-487c-828b-d23b2051ec37
  - id: e666e996-b2cf-4c45-8fc2-1c625212abab
subfeature_v2:
  - id: e1663313-7961-4100-bea9-fa9f4edf8493
  - id: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 5206ed7bc0ce24e65700da28b023d76c68cb6419
workflow-type: tm+mt
source-wordcount: 215
ht-degree: 4%

---

# Authoring dei frammenti

Dopo aver [creato un frammento](./fragments.md#create-fragments), utilizza lo spazio di progettazione visiva per creare la struttura e i componenti di contenuto nel frammento.

## Aggiungere struttura e contenuto {#design-fragment}

{{$include /help/_includes/content-design-components-prime.md}}

## Aggiungere risorse {#add-assets}

Nello spazio di progettazione visiva, seleziona l&#39;icona _Assets_ ( ![icona Assets](../../assets/do-not-localize/icon-assets-me.svg) ) nella barra di navigazione a sinistra per sfogliare e selezionare le risorse immagine dalla libreria di risorse [!DNL Journey Optimizer B2B Prime].

Per i passaggi per selezionare, sostituire o caricare le risorse immagine, consulta [Utilizzare le risorse per l&#39;authoring dei contenuti](./digital-asset-management.md#assets-authoring).

## Spostarsi tra livelli, impostazioni e stili {#navigate-layers-settings-styles}

{{$include /help/_includes/content-design-navigation.md}}

## Personalizzazione dei contenuti {#personalize-content}

[!DNL Journey Optimizer B2B Prime] utilizza la sintassi Handlebars per la personalizzazione. I token vengono sostituiti al momento dell’invio con i valori dei dati di profilo di ciascun destinatario.

_Per aggiungere la personalizzazione :_

1. Seleziona il componente testo e fai clic sull&#39;icona _Aggiungi personalizzazione_ ( ![icona Personalizza](../../user/assets/do-not-localize/icon-personalize.svg) ) nella barra degli strumenti.
1. Nella finestra di dialogo di personalizzazione, sfoglia la struttura dello schema a sinistra e seleziona un attributo di profilo. L&#39;editor inserisce l&#39;espressione Handlebars corrispondente, ad esempio `{{profile.firstName}}`.
1. Aggiungere un valore di fallback per gestire i dati mancanti, se necessario, ad esempio `{{profile.firstName | default: "there"}}`.
1. Fai clic su **[!UICONTROL Conferma]** o **[!UICONTROL Inserisci]**. L’espressione viene visualizzata in linea nel campo.

Per informazioni dettagliate sugli strumenti e sulla sintassi dell&#39;editor espressioni, vedere [Editor Personalization](./personalization-expressions.md).

## Modifica tracciamento URL collegato {#edit-linked-url-tracking}

{{$include /help/_includes/content-design-links.md}}
