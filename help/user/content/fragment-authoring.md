---
title: Authoring di frammenti
description: Scopri come creare frammenti di contenuto che possono essere riutilizzati per le e-mail e le progettazioni di modelli per migliorare l’efficienza e mantenere standard di progettazione e branding.
feature: Fragments, Content Design Tools
role: User
exl-id: d29754cf-6721-489c-bff8-cde034456db2
source-git-commit: 4a54548ad061fc778fae3bc4b8499f3716850e4a
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 14%

---

# Authoring dei frammenti

Dopo aver [creato un frammento](./fragments.md#create-fragments), utilizza l&#39;editor visivo per creare i componenti strutturali e di contenuto nel frammento.

## Aggiungere struttura e contenuto {#design-fragment}

>[!CONTEXTUALHELP]
>id="ajo-b2b_structure_components_fragment"
>title="Aggiungere i componenti Struttura"
>abstract="I componenti della struttura definiscono il layout del frammento. Per iniziare a progettare il contenuto del frammento, trascina un componente **Struttura** nell’area di lavoro."

>[!CONTEXTUALHELP]
>id="ajo-b2b_content_components_fragment"
>title="Informazioni sui componenti per contenuti"
>abstract="I componenti di contenuto sono segnaposto di contenuto vuoti che possono essere utilizzati per creare il layout di un frammento."

{{$include /help/_includes/content-design-components.md}}

## Aggiungere risorse

{{$include /help/_includes/content-design-assets.md}}

## Spostarsi tra livelli, impostazioni e stili

{{$include /help/_includes/content-design-navigation.md}}

## Personalizzazione dei contenuti

{{$include /help/_includes/content-design-personalization.md}}

## Abilita personalizzazione frammento

Quando un autore aggiunge un frammento a un [e-mail](./email-authoring.md#content-authoring---use-visual-fragments) o [modello e-mail](./email-template-authoring.md#content-authoring---use-visual-fragments), il contenuto del frammento è bloccato per impostazione predefinita. Eventuali modifiche apportate al frammento pubblicato vengono propagate automaticamente a tutte le risorse di contenuto in cui viene utilizzato il frammento. Quando imposti un parametro per un componente del frammento come modificabile, l’autore dell’e-mail o del modello può specificare un valore di campo personalizzato specifico per le sue esigenze. Questo flag di personalizzazione è limitato ai componenti visivi immagine, testo e pulsante.

Ad esempio, se progetti un banner riutilizzabile che include un pulsante cliccabile, puoi designare il parametro URL per il pulsante come modificabile. Gli autori delle e-mail possono quindi utilizzare un URL più specifico per la propria campagna e-mail. Con questi campi personalizzabili, gli addetti al marketing possono gestire e personalizzare contenuti riutilizzabili senza la necessità di creare blocchi di contenuto completamente nuovi o interrompere gli aggiornamenti ereditati dal frammento originale.

1. Nell’editor di contenuto visivo, seleziona l’immagine, il testo o l’elemento pulsante in cui desideri abilitare la personalizzazione.

1. Nei dettagli del componente a destra, seleziona la scheda **[!UICONTROL Campi modificabili]**.

1. Fai clic sull&#39;opzione **[!UICONTROL Abilita edizione]** e imposta i campi modificabili.

   ![Abilita campi modificabili per un componente immagine frammento](./assets/fragment-editable-fields-image.png){width="700" zoomable="yes"}

   Puoi abilitare la personalizzazione per i campi visualizzati, che dipendono dal tipo di componente e dai parametri definiti nel frammento.

   Cambia l’opzione in uno stato abilitato per ogni campo in cui desideri consentire la personalizzazione.

1. Fai clic su **[!UICONTROL Panoramica]** per esaminare tutti i campi modificabili e i relativi valori predefiniti.

   ![Esaminare i campi modificabili e i relativi valori predefiniti](./assets/fragment-editable-fields-image-overview.png){width="700" zoomable="yes"}

1. Salva le modifiche.

## Modifica tracciamento URL collegato

{{$include /help/_includes/content-design-links.md}}
