---
title: Configurazione semplificata dell'architettura
description: Configurare Journey Optimizer B2B edition con l'architettura semplificata. Configura schemi XDM, canali e-mail/SMS, azioni del percorso Marketo Engage e utenti.
feature: Setup, Administration
role: Admin, Data Engineer
exl-id: 81232976-09d6-4e10-a034-5c193a63b7df
source-git-commit: 38d1794ed30a34dbb34dfaec2d3088bc3a4680ac
workflow-type: tm+mt
source-wordcount: '884'
ht-degree: 17%

---

# Configurazione semplificata dell&#39;architettura

Adobe Journey Optimizer B2B Edition è ora disponibile utilizzando un’architettura semplificata. Con questa architettura, Journey Optimizer B2B edition e Marketo Engage non si trovano più nello stesso sistema e nello stesso archivio dati. Journey Optimizer B2B Edition riceve i dati solo da Adobe Experience Platform. Tuttavia, continua a fare affidamento su adesioni a Marketo Engage e su alcune funzionalità di back-end, come la consegna e-mail, per il provisioning e la configurazione del sistema.

L’architettura semplificata è la base per lo sviluppo di nuove funzionalità in Journey Optimizer B2B edition:

* **Unifica e ridimensiona facilmente i dati:** La nuova piattaforma supporta modelli di dati complessi, inclusi oggetti personalizzati, gruppi di acquisto ed eventi account.

* **Connetti più istanze di Adobe Marketo Engage:** Gestisci e unifica i dati da più ambienti Marketo Engage in un&#39;unica posizione.

* **Protegge i tuoi dati:** Funzioni avanzate di privacy e sicurezza che aiutano a proteggere le informazioni dei tuoi clienti. (_In arrivo_)

* **Creato per il futuro:** Questo aggiornamento consente di apportare miglioramenti e innovazioni continui.

Per gli ambienti per i quali è stato eseguito il provisioning per questa architettura, utilizza le seguenti linee guida per la configurazione.

Utilizzare questo elenco di controllo per completare la configurazione di Journey Optimizer B2B edition sull&#39;architettura semplificata.

## &#x200B;1. Generare spazi dei nomi e schemi B2B

<table>
<thead>
<tr>
<th colspan="2">Attività</th>
<th>Dettagli e istruzioni</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><strong>Configurazione ambiente:</strong></td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casella di controllo"/></td>
<td>Scarica l’utility di generazione automatica dello spazio dei nomi e dello schema da GitHub.</td>
<td><a href="./data/namespaces-schemas.md#set-up-the-auto-generation-utility">Ulteriori informazioni</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casella di controllo"/></td>
<td>Raccogli le credenziali API di Experience Platform e le intestazioni richieste.</td>
<td><a href="https://experienceleague.adobe.com/it/docs/experience-platform/landing/platform-apis/api-guide">Ulteriori informazioni</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casella di controllo"/></td>
<td>Applica i valori dell’ambiente all’ambiente Postman.</td>
<td><a href="./data/namespaces-schemas.md#environment-values">Ulteriori informazioni</a></td>
</tr>
<tr>
<td colspan="2"><strong>Eseguire gli script:</strong></td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casella di controllo"/></td>
<td>Eseguire l'utilità di generazione <em>Spazi dei nomi e schemi</em> in Postman e confermare la creazione di spazi dei nomi e schemi.</td>
<td><a href="./data/namespaces-schemas.md#run-the-scripts">Ulteriori informazioni</a></td>
</tr>
</tbody>
</table>

## &#x200B;2. Configurare campi ed eventi XDM

<table>
<thead>
<tr>
<th colspan="2">Attività</th>
<th>Dettagli e istruzioni</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><strong>Classi XDM standard</strong>: configurare le classi XDM Individual Profile e XDM Business Account.</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casella di controllo"/></td>
<td>Seleziona i campi gestiti da esporre per percorsi, gruppi di acquisto e personalizzazione e-mail.</td>
<td><a href="./admin/xdm-field-management.md#standard-classes">Ulteriori informazioni</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casella di controllo"/></td>
<td>Modifica i campi aggiornabili per gli schemi.</td>
<td><a href="./admin/xdm-field-management.md#updatable-fields">Ulteriori informazioni</a></td>
</tr>
<tr>
<td colspan="2"><strong>Schemi relazionali</strong>: selezionare la classe XDM relazionale (oggetto personalizzato molti-a-uno account).</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casella di controllo"/></td>
<td>Assicurati che gli schemi abbiano i valori di configurazione richiesti.</td>
<td><a href="./admin/xdm-field-management.md#relational-schemas">Ulteriori informazioni</a></td>
</tr>
<tr>
<td colspan="2"><strong>Eventi</strong>: configura i tipi di evento e i campi di Experience Platform.</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casella di controllo"/></td>
<td>Configura ogni tipo di evento Experience Platform con campi da supportare nei percorsi decisionali/di suddivisione del percorso.</td>
<td><a href="./admin/configure-aep-events.md">Ulteriori informazioni</a></td>
</tr>
</tbody>
</table>

## &#x200B;3. Configurare il tracciamento e il recapito messaggi e-mail

Per inviare e-mail da [!DNL Journey Optimizer B2B Edition] sull&#39;architettura semplificata, configura il tracciamento e il recapito dei messaggi nell&#39;istanza di produzione [!DNL Marketo Engage] allegata e nell&#39;app [!DNL Journey Optimizer B2B Edition].

<table>
<thead>
<tr>
<th colspan="2">Attività</th>
<th>Dettagli e istruzioni</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><strong>Configurazione iniziale</strong> per l'istanza Marketo Engage allegata</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casella di controllo"/></td>
<td>Configurare un nuovo CNAME per il tracciamento dei collegamenti nei record DNS</td>
<td><a href="./start/email-protocols.md#create-dns-records-for-landing-pages-and-email">Ulteriori informazioni</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casella di controllo"/></td>
<td>Configurare i domini di branding per l’istanza Marketo Engage associata</td>
<td><a href="./start/branding-domains.md">Ulteriori informazioni</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casella di controllo"/></td>
<td>Configurare DKIM e SPF per l'istanza Marketo Engage associata</td>
<td><a href="./start/email-protocols.md#set-up-spf-and-dkim">Ulteriori informazioni</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casella di controllo"/></td>
<td>Configura DMARC</td>
<td><a href="./start/email-protocols.md#set-up-dmarc">Ulteriori informazioni</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casella di controllo"/></td>
<td>Configura i record MX per il dominio</td>
<td><a href="./start/email-protocols.md#set-up-mx-records-for-your-domain">Ulteriori informazioni</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casella di controllo"/></td>
<td>Aggiungere indirizzi IP in uscita ai inserisce nell'elenco Consentiti di</td>
<td><a href="./start/email-protocols.md#outbound-ip-addresses">Ulteriori informazioni</a></td>
</tr>
<tr>
<td colspan="2"><strong>Configurazione e-mail</strong> per l'istanza Marketo Engage allegata</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casella di controllo"/></td>
<td>Configura <em>Da e-mail</em> e <em>Da etichetta</em> (facoltativo)</td>
<td><a href="./start/email-setup.md#from-email-and-label">Ulteriori informazioni</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casella di controllo"/></td>
<td>Configura <em>Annulla sottoscrizione a HTML</em> e <em>Annulla sottoscrizione testo</em></td>
<td><a href="./start/email-setup.md#unsubscribe-messaging">Ulteriori informazioni</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casella di controllo"/></td>
<td>Configura <em>Visualizza come pagina Web HTML</em> e <em>Visualizza come testo pagina Web</em></td>
<td><a href="./start/email-setup.md#view-as-web-page">Ulteriori informazioni</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casella di controllo"/></td>
<td>Configura <em>Limiti di recupero oggetti personalizzati</em></td>
<td><a href="./start/email-setup.md#custom-object-retrieval-limits">Ulteriori informazioni</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casella di controllo"/></td>
<td>Configura <em>Opzioni intestazione personalizzate</em></td>
<td><a href="./start/email-setup.md#custom-header-options">Ulteriori informazioni</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casella di controllo"/></td>
<td>Configura filtro <em>Attività bot</em></td>
<td><a href="./start/email-setup.md#filter-email-bots">Ulteriori informazioni</a></td>
</tr>
<tr>
<td colspan="2"><strong>Configurazione del canale e-mail</strong> per Journey Optimizer B2B edition</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casella di controllo"/></td>
<td>Configura <em>Limiti di comunicazione</em> in Journey Optimizer B2B edition</td>
<td><a href="./admin/configure-channels-emails.md#communication-limits">Ulteriori informazioni</a></td>
</tr>
</tbody>
</table>

<!-- TBD for later 

<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Checkbox"/></td>
<td>Configure <em>Email CC Settings</em></td>
<td>[Learn more](TBD)</td>
</tr>

<tr>
<td colspan="2"><strong>Additional configurations</strong></td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Checkbox"/></td>
<td>Configure <em>Location Settings</em> for the attached Marketo Engage instance</td>
<td>< [Learn more](TBD)</td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Checkbox"/></td>
<td>Define and configure which Binding Groups / IPs to move over</td>
<td>[Learn more](TBD)</td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Checkbox"/></td>
<td>Test Email Send</td>
<td>[Learn more](TBD)</td>
</tr>
-->

## &#x200B;4. Configurare canali di contenuto aggiuntivi

Per supportare gli addetti al marketing nell’inclusione di altri canali nei loro percorsi, configura canali aggiuntivi.

<table>
<thead>
<tr>
<th colspan="2">Attività</th>
<th>Dettagli e istruzioni</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2">Configurazione del canale <strong>SMS</strong> per Journey Optimizer B2B edition.</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casella di controllo"/></td>
<td>Configura ogni account SMS che desideri supportare.</td>
<td><a href="./admin/configure-channels-sms.md">Ulteriori informazioni</a></td>
</tr>
<tr>
<td colspan="2"><strong>Configurazione del canale pagine di destinazione</strong> (Beta) per Journey Optimizer B2B edition.</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casella di controllo"/></td>
<td>Completa le impostazioni della pagina di destinazione per supportare gli esperti di marketing che creano e pubblicano queste pagine</td>
<td><a href="./admin/landing-page-settings.md">Ulteriori informazioni</a></td>
</tr>
<tr>
<td colspan="2">Configurazione del canale <strong>Web</strong> (Beta) per Journey Optimizer B2B edition</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casella di controllo"/></td>
<td>Configurare il sito Web aziendale per supportare Adobe Experience Platform Web SDK.</td>
<td><a href="https://experienceleague.adobe.com/it/docs/experience-platform/collection/js/js-overview">Ulteriori informazioni</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casella di controllo"/></td>
<td>Aggiungi le proprietà web tramite un URL in cui viene distribuito il contenuto.</td>
<td><a href="./admin/configure-channels-web.md">Ulteriori informazioni</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casella di controllo"/></td>
<td>Indica agli autori di esperienze web di installare l’estensione del browser Adobe Experience Cloud Visual Editing Helper.</td>
<td><a href="./content/web-experiences.md#install-the-visual-editing-helper-extension">Ulteriori informazioni</a></td>
</tr>
</tbody>
</table>

## &#x200B;5. Connetti l’istanza Marketo Engage per supportare le azioni di percorso (facoltativo)

Se prevedi di integrare le funzionalità di Journey Optimizer B2B edition con campagne e programmi in Marketo Engage, configura il supporto per le azioni di Marketo Engage. Queste azioni consentono ai team di marketing di coordinare le attività di marketing _basate sull&#39;account_ in Journey Optimizer B2B edition e _basate sul lead_ in Marketo Engage.

<table>
<thead>
<tr>
<th colspan="2">Attività</th>
<th>Dettagli e istruzioni</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><strong>Per ogni istanza di Marketo Engage</strong> per supportare le azioni di percorso</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casella di controllo"/></td>
<td>Creare il servizio personalizzato Marketo Engage</td>
<td><a href="./admin/marketo-actions-connect.md#create-the-marketo-engage-custom-service">Ulteriori informazioni</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casella di controllo"/></td>
<td>Aggiungere l’integrazione in Journey Optimizer B2B edition</td>
<td><a href="./admin/marketo-actions-connect.md#add-the-integration">Ulteriori informazioni</a></td>
</tr>
</tbody>
</table>

## &#x200B;6. Abilita accesso utente

Una volta completato il provisioning, le sandbox vengono associate e le attività di configurazione iniziali vengono completate, quindi puoi configurare l’accesso a Journey Optimizer B2B edition e Marketo Engage per il team e gli utenti.

<table>
<thead>
<tr>
<th colspan="2">Attività</th>
<th>Dettagli e istruzioni</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><strong>Fornisci l'accesso al prodotto e le autorizzazioni</strong> per gli utenti</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casella di controllo"/></td>
<td>Creare un profilo di prodotto Marketo Engage in Adobe Admin Console (solo per la nuova istanza di Marketo Engage)</td>
<td><a href="./admin/user-management.md#create-the-marketo-engage-product-profile">Ulteriori informazioni</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casella di controllo"/></td>
<td>Aggiungere un gruppo di utenti per il profilo</td>
<td><a href="./admin/user-management.md#add-a-user-group-for-the-profile">Ulteriori informazioni</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casella di controllo"/></td>
<td>Configurare i ruoli utente B2B</td>
<td><a href="./admin/user-management.md#b2b-built-in-roles">Ulteriori informazioni</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casella di controllo"/></td>
<td>Aggiungere utenti o gruppi ai ruoli</td>
<td><a href="./admin/user-management.md#add-users-to-a-role">Ulteriori informazioni</a></td>
</tr>
</tbody>
</table>
