---
title: Snippet
description: Riutilizzo di note ed elementi visivi per annotare una funzione o una pagina applicata a una specifica edizione
source-git-commit: d0b2f91754ce3c5e38c6aa2c49c816fd46510403
workflow-type: tm+mt
source-wordcount: '451'
ht-degree: 0%

---

# Snippet

<!-- Content authoring steps for reuse -->

## Configurazione dati intento {#intent-data-note}

>[!NOTE]
>
>I dati intento vengono inclusi quando sono configurati per l’istanza Journey Optimizer B2B edition. È inoltre necessario creare uno o più percorsi di acquisto **o** pubblicati. Per ulteriori informazioni sul modello di rilevamento intento e su come inviare parole chiave, prodotti e categorie, vedere [Dati intento](../user/admin/intent-data.md).

## Note sulla licenza di AEM assets {#aem-assets-licensing-note}

>[!NOTE]
>
>Le licenze per AEM Assets as a Cloud Service e Dynamic Media sono prerequisiti per l’integrazione. Verificare che [Dynamic Media con API aperta](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/assets/dynamicmedia/dynamic-media-open-apis/dynamic-media-open-apis-overview){target="_blank"} sia abilitato.<br/>
>A seconda del contratto e della configurazione, è possibile accedere a Adobe Experience Manager Assets as a Cloud Service direttamente da Adobe Journey Optimizer B2B edition durante la progettazione di contenuti visivi.

## Passaggio Authoring dei contenuti - componenti - strutture {#structures-step}

1. Per iniziare la progettazione del contenuto, trascina un elemento dalle **[!UICONTROL Strutture]** e rilascialo nell&#39;area di lavoro.

   Aggiungi tutti gli elementi da _[!UICONTROL Strutture]_ necessari e modifica le impostazioni per ciascuno nel riquadro a destra.

   >[!TIP]
   >
   >Seleziona il componente _[!UICONTROL n:n column]_ per definire il numero di colonne desiderato (tra tre e 10). Puoi anche definire la larghezza di ciascuna colonna spostando le frecce sotto di essa.

   ![Trascina una struttura nell&#39;area di lavoro e regola le impostazioni](../assets/content-design-shared/content-design-add-structure.png){width="800" zoomable="yes"}

   Le dimensioni di ogni colonna non possono essere inferiori al 10% della larghezza totale del componente struttura. È possibile rimuovere solo colonne vuote.

## Authoring dei contenuti - componenti - passaggio contenuti {#contents-step}

1. Espandi la sezione **[!UICONTROL Contents]** e aggiungi tutti gli elementi necessari in uno o più componenti della struttura.

   ![Trascina un elemento di contenuto nell&#39;area di lavoro e regola le impostazioni](../assets/content-design-shared/content-design-add-content.png){width="800" zoomable="yes"}
   <!--
   reference to the contents elements--->

## Authoring dei contenuti - componenti - passaggio impostazioni {#settings-step}

1. Se necessario, puoi effettuare ulteriori personalizzazioni per ciascun componente nelle schede _[!UICONTROL Impostazioni]_ o _[!UICONTROL Stile]_.

   Ad esempio, puoi modificare lo stile del testo, la spaziatura interna o il margine di ciascun componente.

## Authoring dei contenuti - passaggio delle risorse {#assets-step}

1. Dal selettore _Risorsa_, puoi selezionare direttamente le risorse memorizzate nella libreria di risorse.

   Fai doppio clic sulla cartella che contiene le risorse. Trascina e rilascia gli elementi in un componente struttura.

   Per ulteriori informazioni sull&#39;utilizzo delle risorse del tipo di origine, vedere [Aggiungere risorse al contenuto](../user/content/assets-overview.md#use-assets-for-content-authoring).

   ![Trascina una risorsa Marketo Engage nell&#39;area di lavoro e regola le impostazioni](../assets/content-design-shared/content-design-add-asset.png){width="800" zoomable="yes"}

## Authoring dei contenuti - passaggio di personalizzazione {#personalization-step}

1. Inserisci campi di personalizzazione per personalizzare il contenuto da attributi di profili, iscrizioni di pubblico, attributi contestuali e altro ancora.

## Authoring dei contenuti - passaggio di abilitazione del contenuto della condizione {#dynamic-content-step}

1. Fai clic su **[!UICONTROL Abilita contenuto condizione]** per aggiungere contenuto dinamico e adattare il contenuto ai profili target in base alle regole condizionali.

## Authoring dei contenuti - passaggio di tracciamento dei collegamenti {#links-tracking-step}

1. Seleziona la scheda **[!UICONTROL Collegamenti]** dal riquadro a sinistra per visualizzare tutti gli URL del contenuto tracciato.

   Puoi modificare il _Tipo di tracciamento_ o _Etichetta_ e aggiungere tag se necessario.
