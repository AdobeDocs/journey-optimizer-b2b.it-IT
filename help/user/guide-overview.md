---
title: Documentazione di Adobe Journey Optimizer B2B Edition
description: 'Documentazione completa per Journey Optimizer B2B Edition: esplora le risorse disponibili per l’onboarding, la creazione di gruppi acquisti e di percorsi di account e la gestione dei contenuti.'
exl-id: 3d7b6c82-95c3-4d89-b3dc-7fd5b0aef615
autotag-review: 2026-03-27T22:18:45.397Z
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
    internal-label: Journey Optimizer B2B Edition
feature_v2:
  - id: f467931a-9b22-4ca8-869f-adfbd64061ce
    internal-label: Onboarding
TQID: https://experienceleague.adobe.com/BK-uFYGIZyqRNy4Gx-vJB-oy3q8zpjERIoJwBvgofUY
source-git-commit: 87bce853d68d03eabceccf02ba80a8077dce206d
workflow-type: tm+mt
source-wordcount: '1057'
ht-degree: 27%
---
# Documentazione di Adobe Journey Optimizer B2B Edition

[!DNL Adobe Journey Optimizer B2B Edition] è una prima applicazione di questo tipo che consente ai team di marketing e di vendita di orchestrare esperienze basate su account e qualificare gruppi di acquisto per prodotti specifici nell&#39;intero ciclo di vita del cliente. Utilizza l’intelligenza artificiale per coinvolgere e qualificare i gruppi di acquisto all’interno degli account di destinazione, aiutando i team a generare una pipeline di qualità superiore e a progettare migliori strategie di acquisizione, espansione e conservazione. Consente inoltre di condividere informazioni tra i team di vendita e marketing.

Questa documentazione fornisce informazioni per la masterizzazione dell&#39;applicazione. È progettato per gli addetti al marketing, i rappresentanti dello sviluppo aziendale, gli analisti di dati e gli amministratori operativi.

## Novità

Esaminare questo esempio delle ultime aggiunte e dei miglioramenti apportati all&#39;applicazione e alla documentazione [!DNL Journey Optimizer B2B Edition].

>[!BEGINTABS]

>[!TAB percorsi di persone]

Organizza attività di marketing basate su lead con percorsi di persone, che utilizzano i dati e il pubblico di [!DNL Adobe Experience Platform] per coinvolgere singole persone. I percorsi di persone ora supportano _Ascolta un evento_, azione esterna e nodi di percorsi suddivisi esterni e reinserimento del percorso. Utilizzali insieme a percorsi di account e gruppi di acquisto per orchestrare l’intero percorso di acquisto.

[!BADGE Ulteriori informazioni]{type=Informative url="/help/user/journeys/journeys-overview.md" tooltip="Informazioni sui percorsi di persone"}

>[!TAB Percorsi suddivisi variante]

Verifica le varianti all’interno di un percorso di account o persone assegnando account o persone a percorsi di percorso diversi in base alle percentuali definite. Nei percorsi di persone, l&#39;assegnazione è deterministica, quindi ogni persona segue sempre lo stesso percorso, che supporta gli esperimenti controllati.

[!BADGE Ulteriori informazioni]{type=Informative url="/help/user/journeys/variant-split-paths-nodes.md" tooltip="Scopri i percorsi di suddivisione delle varianti"}

>[!TAB Canale WhatsApp]

Quando sviluppatori e amministratori di prodotto configurano un’integrazione con un account Meta Business Manager, gli addetti al marketing possono includere messaggi WhatsApp come canale di contenuto nei percorsi di account utilizzando l’API Meta Cloud. WhatsApp si unisce a e-mail e SMS come canale disponibile per la distribuzione di contenuti di percorso direttamente ai membri dell’account.

[!BADGE Ulteriori informazioni]{type=Informative url="/help/user/admin/configure-channels-whatsapp.md" tooltip="Scopri il canale WhatsApp"}

>[!TAB Modelli di IA generativa]

I designer e-mail ora possono scegliere tra modelli standard [!DNL Firefly], modelli personalizzati [!DNL Firefly] addestrati su risorse specifiche del brand e modelli di immagini di terze parti approvati durante la generazione di immagini per il contenuto dell’e-mail. Questa selezione offre ai team il controllo su quale modello si adatta al loro specifico scenario di progettazione, dalle esigenze di contenuto generale ai casi d’uso con marchio o specializzati.

[!BADGE Ulteriori informazioni]{type=Informative url="/help/user/content/generative-ai-models.md" tooltip="Scopri la selezione del modello di IA generativa"}

>[!TAB Ottimizzazione del tempo di invio]

Per i nodi di azione _Invia e-mail_ in percorsi di persone, ora puoi utilizzare l&#39;ottimizzazione del tempo di invio per personalizzare il tempo di consegna delle e-mail. Il sistema prevede quando ogni persona è più probabile che interagisca e pianifica la consegna di conseguenza, anziché inviare contemporaneamente a tutti i destinatari.

[!BADGE Ulteriori informazioni]{type=Informative url="/help/user/content/email-send-time-optimization.md" tooltip="Scopri l’ottimizzazione dell’ora di invio"}

>[!TAB Percorso di rientro]

Ora puoi inviare più volte account o persone tramite un account o un percorso di persone. Il reinserimento prevede più scenari, ad esempio la rivalutazione dei criteri di qualificazione e dei flussi di lavoro di sviluppo riutilizzabili. Utilizzare le impostazioni di reinserimento per impostare criteri, limiti e tempi di attesa in modo che gli account o le persone possano riqualificarsi per il percorso in modo controllato.

[!BADGE Ulteriori informazioni]{type=Informative url="/help/user/journeys/journey-re-entry.md" tooltip="Informazioni sul rientro nel percorso"}

>[!ENDTABS]

## Inizia ad esplorare {#section-explore}

:::: landing-cards-container
:::
![icon](https://cdn.experienceleague.adobe.com/icons/list-check.svg?lang=it)

Note sulla versione più recente

Rimani aggiornato con le ultime note sulla versione, le nuove funzioni e i miglioramenti in [!DNL Adobe Journey Optimizer B2B Edition].

[Consulta le note sulla versione](./release-notes/release-notes.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg?lang=it)

Introduzione

Rivedi le linee guida per l&#39;onboarding di [!DNL Journey Optimizer B2B Edition] per amministratori e addetti al marketing.

[Amministratori](./setup-ultimate.md)
[Utenti](./start/get-started.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg?lang=it)

Gestione dei dati

Attiva gli schemi e i campi XDM che desideri utilizzare in [!DNL Adobe Journey Optimizer B2B Edition] e scopri come funzionano i relativi dati in [!DNL Adobe Experience Platform].

[Visualizza gestione campi XDM](./admin/xdm-field-management.md)
[Set di dati esportati](./data/aep-exported-datasets.md)
[Query set di dati](./data/aep-query-examples.md)
[Disponibilità dei dati e tempi di sincronizzazione](./data/data-availability-timing.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/envelope.svg?lang=it)

Canali di comunicazione

Configura e gestisci e-mail, SMS, WhatsApp e altri canali per interazioni personalizzate con i clienti.

[Configura canale e-mail](./admin/configure-channels-emails.md)
[Configurare il canale SMS](./admin/configure-channels-sms.md)
[Configura canale WhatsApp](./admin/configure-channels-whatsapp.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg?lang=it)

Creare un percorso

Progetta, gestisci, gestisci e ottimizza percorsi personalizzati di account e persone.

[Esplorare i percorsi](./journeys/journeys-overview.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/users.svg?lang=it)

Comprendere i gruppi di acquisto

Linee guida dettagliate sulla creazione, gestione e ottimizzazione dei gruppi di acquisto per un targeting efficace.

[Informazioni sui gruppi di acquisto](./buying-groups/buying-groups-overview.md)
:::

::::

<!--
:::
![icon](https://cdn.experienceleague.adobe.com/icons/image.svg?lang=it)

Design Content

Learn how to author and manage content for personalized customer experiences orchestrated through journeys.

[Explore Content Components](./content/content-components.md)
::: 
-->

## Panoramica dimostrazione

Scopri i componenti di un gruppo acquisti e comprendi le nozioni di base per la creazione di un percorso account.

>[!VIDEO](https://video.tv.adobe.com/v/3432054?quality=12)

## Esplora la documentazione

<table style="table-layout:auto">
  <tr style="border: 0;">
    <td>
      <img src="../assets/do-not-localize/icon-quick-start.svg" width="35px" alt="Introduzione"><br/>
      <strong>Introduzione</strong><br/><a href="home-page.md">Accesso e home page</a><br/><a href="./start/get-started.md">Guida all'onboarding</a> <br/><a href="./ai-coworker/ai-assistant-overview.md">Funzionalità AI</a>
    </td>
    <td>
      <img src="../assets/do-not-localize/icon_audience.svg" width="35px" alt="Gruppi acquisti"><br/>
      <strong>Gruppi acquisti</strong><br/><a href="./buying-groups/buying-groups-overview.md">Panoramica dei gruppi acquisti</a><br/><a href="./buying-groups/buying-groups-role-templates.md">Modelli di ruoli</a><br/><a href="./buying-groups/solution-interests.md">Soluzioni di interesse</a><br/><a href="./buying-groups/buying-groups-create.md">Creare gruppi acquisti</a>
    </td>
    <td>
      <img src="../assets/do-not-localize/icon-paths.svg" width="35px" alt="Percorsi account"><br/>
      <strong>Percorsi account</strong><br/><a href="./journeys/journeys-overview.md">Panoramica dei percorsi</a><br/><a href="./journeys/create-publish-journey.md#create-a-journey">Crea un percorso account</a><br/><a href="./journeys/journey-nodes.md">Nodi percorsi</a>
    </td>
  </tr>
  <tr style="border: 0;">
    <td>
      <img src="../assets/do-not-localize/icon-campaign.svg" width="35px" alt="Contenuto del percorso"><br/>
      <strong>Contenuto Percorso</strong><br/><a href="./content/add-email.md">Canale e-mail</a><br/><a href="./content/generate-content-emails.md">Genera contenuto e-mail</a><br/><a href="./content/genstudio-email-workflow.md">Esperienze e-mail GenStudio</a><br/><a href="./content/sms-authoring.md">Canale SMS</a>
    </td>
        <td>
      <img src="../assets/do-not-localize/icon_assets.svg" width="35px" alt="Gestione dei contenuti"><br/>
      <strong>Gestione dei contenuti</strong><br/><a href="./content/assets-overview.md">Panoramica di Assets</a><br/><a href="./content/email-templates.md">Modelli e-mail</a><br/><a href="./content/fragments.md">Frammenti visivi</a><br/><a href="./content/conditional-content.md">Contenuto condizionale</a><br/><a href="./content/brand-themes.md">Temi del marchio</a>
    </td>
    <td>
      <img src="../assets/do-not-localize/icon-offer.svg" width="35px" alt="Insight e dashboard"><br/>
      <strong>Approfondimenti</strong><br/><a href="./dashboards/intelligent-dashboard.md">Dashboard intelligente</a><br/><a href="./dashboards/engagement-dashboard.md">Dashboard di coinvolgimento</a><br/><a href="./dashboards/buying-groups-dashboard.md">Dashboard dei gruppi di acquisto</a><br/><a href="./dashboards/journeys-dashboard.md">Dashboard dei Percorsi</a><br/><a href="./buying-groups/incrm-insights.md">Approfondimenti in-CRM</a>
    </td>

</tr>
</table>

## Risorse aggiuntive

<table style="table-layout:fixed">
<tr><td><strong>Adobe Journey Optimizer B2B Edition</strong><br/>
<a href="https://experienceleague.adobe.com/it/docs/journey-optimizer-b2b-learn/tutorials/overview" target="_blank">Video e tutorial</a> - <a href="https://helpx.adobe.com/it/legal/product-descriptions/adobe-journey-optimizer-b2b.html" target="_blank">Descrizione del prodotto</a> <!-- - <a href="https://www.adobe.com/content/dam/cc/en/security/pdfs/AJO_SecurityOverview.pdf" target="_blank">Security overview (PDF)</a> - <a href="https://developer.adobe.com/journey-optimizer-apis/" target="_blank">APIs reference</a> - <a href="https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html?lang=it" target="_blank">Journey Optimizer Schema Dictionary</a> -->
</td>
<td><strong>Adobe Experience Platform</strong><br/>
<a href="https://experienceleague.adobe.com/it/docs/experience-platform/landing/home" target="_blank">Documentazione</a> - <a href="https://business.adobe.com/it/products/experience-platform/documentation-and-developer-resources.html" target="_blank">Risorse per sviluppatori</a>
</td></tr>
<tr><td><strong>Adobe Real-Time Customer Data Platform</strong><br/>
<a href="https://experienceleague.adobe.com/it/docs/experience-platform/rtcdp/home" target="_blank">Documentazione</a> - <a href="https://experienceleague.adobe.com/it/docs/platform-learn/getting-started-for-data-architects-and-data-engineers/overview" target="_blank">Esercitazioni per sviluppatori</a>
</td><td><strong>Adobe Marketo Engage</strong><br/>
<a href="https://experienceleague.adobe.com/it/docs/marketo/using/home" target="_blank">Documentazione utente</a> - <a href="https://experienceleague.adobe.com/it/docs/marketo-developer/marketo/home" target="_blank">Documentazione per sviluppatori</a>
</td>
</tr></table>

