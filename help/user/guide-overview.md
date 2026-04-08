---
title: Documentazione di Adobe Journey Optimizer B2B Edition
description: 'Documentazione completa per Journey Optimizer B2B Edition: esplora le risorse disponibili per l’onboarding, la creazione di gruppi acquisti e di percorsi di account e la gestione dei contenuti.'
exl-id: 3d7b6c82-95c3-4d89-b3dc-7fd5b0aef615
source-git-commit: 0e79785bd8baf3914127cc650b8e503a8d461a3d
workflow-type: tm+mt
source-wordcount: '917'
ht-degree: 29%

---

# Documentazione di Adobe Journey Optimizer B2B Edition

[!DNL Adobe Journey Optimizer B2B Edition] è una prima applicazione di questo tipo che consente ai team di marketing e di vendita di orchestrare esperienze basate su account e qualificare gruppi di acquisto per prodotti specifici nell&#39;intero ciclo di vita del cliente. Utilizza l’intelligenza artificiale per coinvolgere e qualificare i gruppi di acquisto all’interno degli account di destinazione, aiutando i team a generare una pipeline di qualità superiore e a progettare migliori strategie di acquisizione, espansione e conservazione. Consente inoltre di condividere informazioni tra i team di vendita e marketing.

Questa documentazione fornisce informazioni per la masterizzazione dell&#39;applicazione. È progettato per gli addetti al marketing, i rappresentanti dello sviluppo aziendale, gli analisti di dati e gli amministratori operativi.

## Novità

Esaminare questo esempio delle ultime aggiunte e dei miglioramenti apportati all&#39;applicazione e alla documentazione [!DNL Journey Optimizer B2B Edition].

>[!BEGINTABS]

>[!TAB Agenti AI]

Con [Experience Platform Agent Orchestrator](https://experienceleague.adobe.com/it/docs/experience-cloud-ai/experience-cloud-ai/home#agent-orchestrator){target="_blank"}, l&#39;interfaccia dell&#39;Assistente di intelligenza artificiale può richiamare automaticamente agenti specializzati per ottenere le risposte e le informazioni corrette. Agent Orchestrator ricorda la cronologia delle conversazioni consentendoti di fare riferimento alle domande precedenti in modo naturale, senza dover ripetere il contesto, e combina gli insight provenienti da più agenti per fornire risposte chiare e unificate. Nel contesto [!DNL Journey Optimizer B2B Edition] sono disponibili tre agenti appositamente creati per attività e domini B2B specifici:

* [Audience Agent B2B](./agents/audience-agent-b2b.md)
* [Journey Agent B2B](./agents/journey-agent.md)
* [Agente Account Qualification](./agents/sales-qualifier.md#account-qualification-agent)

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

Ora puoi inviare account/persone più volte tramite un flusso di lavoro di percorso dell’account. Il reinserimento prevede più scenari, ad esempio la rivalutazione dei criteri di qualificazione e dei flussi di lavoro di sviluppo riutilizzabili. Utilizzare le impostazioni di reinserimento per impostare criteri, limiti e tempi di attesa in modo che gli account possano essere riqualificati per il percorso in modo controllato.

[!BADGE Ulteriori informazioni]{type=Informative url="/help/user/journeys/journey-re-entry.md" tooltip="Informazioni sul rientro nel percorso"}

>[!TAB Temi marchio]

Con i temi, i designer non tecnici hanno la possibilità di creare linee guida per la progettazione di contenuti e-mail riutilizzabili, in linea con un marchio e uno stile specifici. I temi consentono agli addetti al marketing di sfruttare le e-mail visivamente accattivanti e coerenti con il brand in modo più rapido e con meno sforzo, e di fornire opzioni di personalizzazione avanzate per esigenze di progettazione univoche.

[!BADGE Ulteriori informazioni]{type=Informative url="/help/user/content/brand-themes.md" tooltip="Scopri i temi del brand"}

>[!TAB Mappatura persona]

Gli addetti al marketing possono definire profili dettagliati che includono informazioni di base, responsabilità, punti critici e canali di comunicazione preferiti. Con queste definizioni, gli amministratori possono configurare gli utenti tipo in base agli attributi della persona in [!DNL Journey Optimizer B2B Edition] in modo che i modelli di ruolo possano utilizzare condizioni di ruolo semplificate e coerenti per acquisire tali utenti tipo.

[!BADGE Ulteriori informazioni]{type=Informative url="/help/user/admin/persona-mapping.md" tooltip="Scopri la mappatura personale"}

>[!ENDTABS]

## Inizia ad esplorare {#section-explore}

:::: landing-cards-container
:::
![icon](https://cdn.experienceleague.adobe.com/icons/list-check.svg?lang=it)

Note sulla versione più recente

Rimani aggiornato con le note sulla versione più recente, le nuove funzioni e i miglioramenti apportati in Adobe Journey Optimizer B2B edition.

[Consulta le note sulla versione](./release-notes/release-notes.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg?lang=it)

Introduzione

Consulta le linee guida per l’onboarding di Journey Optimizer B2B edition per amministratori e addetti al marketing.

[Introduzione](./start/get-started.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg?lang=it)

Configurare i campi XDM

Implementa le configurazioni di sistema per attivare gli schemi e i campi XDM da utilizzare in Adobe Journey Optimizer B2B edition.

[Visualizza gestione campi XDM](./admin/xdm-field-management.md)
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

Creazione di un Percorso di account

Progetta, gestisci, gestisci e ottimizza percorsi di account personalizzati.

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
      <strong>Introduzione</strong><br/><a href="home-page.md">Accesso e pagina Home</a><br/><a href="./start/get-started.md">Guida all’onboarding</a> <br/><a href="./ai-assistant/ai-assistant-overview.md">Assistente IA</a>
    </td>
    <!--
    <td>
      <img src="../assets/do-not-localize/icon-configure.svg" width="35px"><br/>
      <strong>Configuration<br/>administration</strong><br/><a href="using/configuration/channel-surfaces.md">Channel surfaces</a> - <a href="using/configuration/about-data-sources-events-actions.md">Configure journeys</a>  - <a href="using/administration/permissions-overview.md">Access control</a> - <a href="using/administration/sandboxes.md">Sandboxes management</a>
    </td> -->
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
      <strong>Contenuto del percorso</strong><br/><a href="./content/add-email.md">Canale e-mail</a><br/><a href="./content/ai-assistant-emails.md">Assistente IA per e-mail</a><br/><a href="./content/genstudio-email-workflow.md">Esperienze e-mail di GenStudio</a><br/><a href="./content/sales-alert-email.md">E-mail di avviso vendite</a><br/><a href="./content/sms-authoring.md">Canale SMS</a>
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
<tr><td><strong>Adobe Journey Optimizer B2B edition</strong><br/>
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

