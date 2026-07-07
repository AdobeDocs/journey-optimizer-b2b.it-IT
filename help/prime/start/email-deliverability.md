---
title: Configurazione recapito e-mail
description: Configura la delega dei sottodomini, DMARC, SPF, DKIM e i pool IP per Journey Optimizer B2B Prime.
badgeBeta: label="Beta" type="informative" tooltip="Questa funzione fa parte di una versione beta limitata."
autotag-review: '2026-06-12T22:43:42.799Z'
TQID: 'https://experienceleague.adobe.com/RKZSQkjSRvHixOm2faRT5D-yB00IykXfPO06vvIUQ6k'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: d6e625c1-468f-4d73-9f32-fd1edb87f96bid: f01b5556-e951-40ba-8625-2e3001864f2bid: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2: id: d270a788-eb1d-40ed-b74e-9158ed975b1fid: ff0c35fa-aa7e-4050-a37c-198fcacd09e6
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: 4632a06ce5a17713fdcaecf6eac8c051bc984e28
workflow-type: tm+mt
source-wordcount: 1920
ht-degree: 1%

---

# Recapitabilità delle e-mail

Le informazioni seguenti sono destinate agli amministratori che configurano l’infrastruttura di invio per supportare gli addetti al marketing e i creatori di contenuti e-mail. Descrive le funzioni di recapito messaggi e come configurare i sottodomini, l’autenticazione e i pool IP. Per ulteriori informazioni sui canali e-mail, consulta i seguenti argomenti:

* Configurazione dei canali e-mail - [Configurazione del canale e-mail](../admin/email-channel-configuration.md)
* Creazione di e-mail - [Aggiungi e-mail ai percorsi](../marketing/email-channel.md)
* Progettazione di contenuti e-mail - [Authoring di contenuti e-mail](../content/email-authoring.md).

Il recapito messaggi e-mail in [!DNL Journey Optimizer B2B Prime] è il set di configurazioni di infrastruttura e autenticazione che consentono ai messaggi e-mail di raggiungere la casella in entrata del destinatario, non la cartella di posta indesiderata e non bloccati dagli ISP (provider di servizi Internet).

Utilizza i seguenti blocchi predefiniti, configurati da un amministratore, in genere nell’ordine seguente:

1. [Delega uno o più sottodomini](#subdomain-delegation) ad Adobe.
1. [Configura i record DMARC, SPF e DKIM](#dmarc-spf-dkim) in ciascun sottodominio.
1. [Conferma il pool IP](#ip-pools) utilizzato per inviare e-mail per il tuo sottodominio.
1. [Crea una o più configurazioni del canale e-mail](../admin/email-channel-configuration.md#create-email-channel-configuration) che associano un sottodominio, un pool IP e un&#39;identità mittente.

![Configurazione del recapito messaggi e-mail per Journey Optimizer B2B Prime](./assets/email-deliverability-diagram.svg){width="550" zoomable="yes"}

>[!TIP]
>
>Considera il recapito messaggi e la configurazione dei canali come un’attività amministratore una tantum. Una volta configurata, gli addetti al marketing e gli autori di e-mail non dovranno più visitarla.

## Limitazioni attuali {#limitations}

* **Il metodo di delega personalizzato** per la delega del sottodominio non è ancora disponibile. Utilizza Fully Delegated o CNAME. Per la versione GA è prevista la delega personalizzata.
* **Pool IP dedicati** non disponibili in Beta. L&#39;unica opzione è il pool IP condiviso. Gli IP dedicati vengono forniti in GA, inclusa la pianificazione del riscaldamento IP e la gestione dei record PTR.

## Concetti chiave {#key-concepts}

Prima di configurare l’e-mail, esamina i concetti seguenti che si applicano alle funzioni di consegna del canale e-mail:

| Concetto | Cosa significa in [!DNL Journey Optimizer B2B Prime] |
| ------- | ---------------------- |
| **_Sottodominio_** | Parte delegata del dominio di invio (ad esempio, `mail.contoso.com`) utilizzata per inviare messaggi di posta elettronica tramite Prime. I sottodomini isolano la reputazione di marketing B2B dalla posta aziendale o transazionale. |
| **_Pool IP_** | Un gruppo di indirizzi IP associati a uno o più sottodomini. In questa versione, Prime supporta un pool IP condiviso gestito da Adobe; i pool IP dedicati sono inclusi nella roadmap di GA. |
| **_Configurazione canale_** | Un set riutilizzabile di impostazioni di invio e-mail (identità del mittente, indirizzo di risposta, sottodominio, pool IP, tipo e-mail e tracciamento) da allegare alle azioni e-mail nei percorsi. Puoi avere più configurazioni di canale denominate per diversi marchi, business unit o tipi di invio. |

<!--

## Roles and permissions {#roles-permissions}

[!DNL Journey Optimizer B2B Prime] uses role-based access control (RBAC) for email features. Permissions are managed in the Adobe Admin Console (IMS) and synced at login. Product administrators assign granular permissions to product profiles, and then attach those product profiles to users.

Access to email functionality in [!DNL Journey Optimizer B2B Prime] is gated by two layers:

1. **Feature flag (LD).** A LaunchDarkly flag controls whether the entire feature is turned on for your organization. Email authoring and deliverability are gated by `dx_ajo_btob_channel_foundation`. Without this flag, the feature is hidden regardless of permissions.
2. **Functional permission.** A user-level permission that controls whether a specific user can read or write within a feature.

Most email features follow a `view-*` (read) and `manage-*` (write) pattern. A user needs the read permission to see a feature in the navigation, and the write permission to create, edit, or delete within it.

### Email authoring permissions {#email-authoring-permissions}

| Capability | Permission | What it allows |
| ---------- | ---------- | -------------- |
| **View emails** | `view-b2b-emails` | View the email list, open emails, view content (read-only). |
| **Create / edit / delete emails** | `manage-b2b-emails` | All read access plus create, edit, duplicate, and delete emails. Required to author email content within a journey. |
| **View templates** | `view-b2b-templates` | Browse and preview templates in the Templates gallery (read-only). |
| **Create / edit / delete templates** | `manage-b2b-templates` | All read access plus create, edit, and delete saved templates. |
| **View fragments** | `view-b2b-fragments` | Browse and preview visual fragments (read-only). |
| **Create / edit fragments** | `manage-b2b-fragments` | All read access plus create and edit visual fragments. |
| **Publish fragments** | `publish-b2b-fragments` | Publish a fragment so it becomes available to email authors across the organization. |
| **Manage shared assets and library items** | `manage-b2b-library-items` | Manage the underlying shared library used by templates, fragments, and emails. Often granted alongside the template/fragment manage permissions. |
| **Manage usage labels** | `manage-b2b-delete-usage-labels` | Manage data usage labels (DULE) attached to library items for governance. |
| **Manage packages** | `manage-b2b-packages` | Bundle and move templates, fragments, and emails between sandboxes. |
| **View assets (Marketo Design Studio assets in Prime)** | `view-b2b-assets` | Browse the asset picker and preview images. Read-only. |
| **Manage assets** | `manage-b2b-assets` | All read access plus future asset-management actions (Beta scope). |
| **Export message data** | `manage-b2b-message-export` | Export email-level message data and reports. |

Within a person journey, the **Send email** action requires `manage-b2b-person-journeys` (to add the action and activate the journey). A user with only email permissions can author content but cannot add an email to a journey.

### Email deliverability permissions {#email-deliverability-permissions}

Deliverability features (subdomains, DMARC, IP pools, suppression lists, allowed lists, IP warmup plans, and seed lists) are administrator-level configuration. They are governed by two permissions covering the entire **[!UICONTROL Channels]** > **[!UICONTROL Email settings]** area:

| Capability | Permission | What it allows |
| ---------- | ---------- | -------------- |
| **View email settings** | `view-b2b-email-settings` | View subdomains, PTR records, IP pools, suppression list, allowed list, IP warmup plans, and seed lists (read-only). |
| **Manage email settings** | `manage-b2b-email-settings` | All read access plus delegate subdomains, configure DMARC, manage suppression and allowed lists, manage IP warmup plans and seed lists. |

Some sub-features within Email settings are gated by additional LaunchDarkly flags — Suppression list (`enable-suppression`), Allowed list (`enable-allow-list`), Seed lists (`enable-seedlist-ui`). If a sub-feature is not visible in your organization, check with your Adobe representative on flag enablement.

### Channel configuration permissions {#channel-configuration-permissions}

Channel configurations sit under **[!UICONTROL Channels]** → **[!UICONTROL General settings]**. They tie deliverability primitives (subdomain, IP pool, sender identity) to a reusable object that journey authors reference. They are governed by a single permission:

| Capability | Permission | What it allows |
| ---------- | ---------- | -------------- |
| **Manage channel configurations** | `manage-b2b-channels-configurations` | View, create, edit, and delete email channel configurations. |

-->

## Delega dei sottodomini {#subdomain-delegation}

La delega dei sottodomini comunica a Internet che Adobe è autorizzato a inviare e-mail per conto di un sottodominio specifico (ad esempio, `mail.contoso.com`) del tuo dominio. La delega di un sottodominio dedicato, anziché del dominio principale, protegge la posta aziendale e offre i seguenti vantaggi:

* **Isolamento reputazione.** Gli invii di marketing sono tenuti separati dalla posta aziendale. Se la reputazione di marketing diminuisce, i messaggi aziendali e transazionali non subiranno modifiche.
* **Riscaldamento IP più veloce.** I sottodomini dedicati aiutano a stabilire più rapidamente una reputazione positiva del mittente con gli ISP.
* **Autenticazione moderna.** SPF, DKIM e DMARC possono essere configurati in modo pulito per sottodominio senza influire sugli altri flussi di posta.
* **Conformità.** Consente di soddisfare i requisiti di invio in blocco da Gmail, Yahoo e altri importanti ISP.

>[!NOTE]
>
>Ogni sottodominio in Prime può essere utilizzato solo da un prodotto Adobe. Non è possibile condividere lo stesso sottodominio di invio tra Prime e un altro prodotto, ad esempio Adobe Marketo Engage o Adobe Campaign, ma è necessario utilizzare sottodomini distinti.

### Metodi supportati {#supported-methods}

In questa versione di Beta, Prime supporta due dei tre metodi di delega dei sottodomini. Il terzo metodo (Delega personalizzata) si trova nella roadmap.

| Metodo | Quando utilizzare | Che cosa implica |
| ------ | ----------- | ---------------- |
| **Delega completa** | Consigliato | Delega l’autorità DNS completa per il sottodominio ad Adobe. Adobe crea e gestisce record MX, SPF, DKIM, DMARC, A e CNAME. Sovraccarico operativo minimo. Adobe gestisce le modifiche DNS per te. |
| **CNAME** | Per criteri con restrizioni | Mantieni l’autorità DNS al tuo fianco e crea record CNAME che puntano ai record gestiti da Adobe. Utilizzalo quando i criteri DNS della tua organizzazione non consentono la delega completa. Sei responsabile della gestione dei record DNS. |
| **Delega personalizzata** | Roadmap (GA) | Mantenere la piena proprietà dei certificati DNS e SSL. Offre il massimo controllo, inclusa la possibilità di utilizzare certificati personalizzati. Questa è la destinazione per la versione GA. |

### Delegare un sottodominio (metodo Fully Delegated) {#delegate-fully-delegated}

>[!PREREQUISITES]
>
>* Decidi su una convenzione di denominazione del sottodominio (ad esempio, `mail.contoso.com` per il marketing, `alerts.contoso.com` per le transazioni).
>* Conferma con il tuo team IT/DNS di poter delegare il sottodominio (record NS) ad Adobe.
>* Crea il nuovo sottodominio nel provider DNS, quindi attendi 24-48 ore per la propagazione DNS prima di delegare ad Adobe.
>* Conferma di disporre del ruolo di Amministratore in Prime.

1. Nella barra di navigazione a sinistra di [!DNL Adobe Journey Optimizer B2B Prime], espandi **[!UICONTROL Amministrazione]** e seleziona **[!UICONTROL Canali]**.
1. Nel pannello, espandi **[!UICONTROL Impostazioni e-mail]** e seleziona **[!UICONTROL Sottodomini]**.
1. Fare clic su **[!UICONTROL Configura sottodominio]**.
1. Immettere il nome completo del sottodominio, ad esempio `mail.contoso.com`.
1. Scegliere **[!UICONTROL Delega completa]** come metodo di delega.
1. Configurare DMARC per il sottodominio (vedere [DMARC, SPF e DKIM](#dmarc-spf-dkim)).

   Imposta almeno un record DMARC con un criterio di avvio di `none` per monitorare i report senza influire sulla consegna.

1. Esamina l’elenco dei record DNS da gestire in Adobe.

   In genere includono i record MX, SPF, DKIM, DMARC, A e CNAME (per il tracciamento e gli URL delle pagine mirror).

1. Scarica i record DNS come file CSV utilizzando il pulsante **[!UICONTROL Scarica record]**. Condividi questo file con il tuo team DNS.

1. Il team DNS aggiunge i record NS nella soluzione di hosting del dominio che delegano il sottodominio ad Adobe.

1. Dopo che il team DNS ha confermato la disponibilità dei record, tornare a [!DNL Journey Optimizer B2B Prime] e selezionare la casella di controllo che conferma la creazione dei record richiesti nel sito di hosting.

1. Fai clic su **[!UICONTROL Invia]** per avviare una serie di controlli di convalida (pre-convalida, MX, SPF, DKIM, DMARC, registrazione FBL).

1. Attendere che lo stato del sottodominio passi a **[!UICONTROL Operazione completata]**.

   Questa operazione richiede in genere alcuni minuti dopo il completamento della propagazione DNS.

>[!NOTE]
>
>Se la convalida non riesce, lo stato diventa **[!UICONTROL Non riuscito]** e [!DNL Journey Optimizer B2B Prime] viene visualizzato il motivo (ad esempio, record NS non trovato, record MX mancante o configurazione errata di DMARC). Correggi il problema DNS sottostante, quindi riprova l’invio.

### Delega un sottodominio (metodo CNAME) {#delegate-cname}

Utilizzare questo metodo solo se i criteri DNS dell&#39;organizzazione non consentono la delega completa. Con CNAME puoi mantenere i record DNS al tuo fianco.

1. Nella barra di navigazione a sinistra di [!DNL Adobe Journey Optimizer B2B Prime], espandi **[!UICONTROL Amministrazione]** e seleziona **[!UICONTROL Canali]**.
1. Nel pannello, espandi **[!UICONTROL Impostazioni e-mail]** e seleziona **[!UICONTROL Sottodomini]**.
1. Fare clic su **[!UICONTROL Configura sottodominio]**.
1. Immetti il nome completo del sottodominio.
1. Scegliere **[!UICONTROL CNAME]** come metodo di delega.
1. Configurare DMARC per il sottodominio ([DMARC, SPF e DKIM](#dmarc-spf-dkim)).
1. Esamina l’elenco dei record CNAME da generare. Questi puntano i componenti del sottodominio ai record gestiti da Adobe.
1. Scarica i record come CSV e condividili con il tuo team DNS.
1. Il team DNS aggiunge ogni record CNAME alla soluzione di hosting DNS.
1. Quando i record sono presenti e propagati, tornare a [!DNL Adobe Journey Optimizer B2B Prime] e confermare.
1. Fai clic su **[!UICONTROL Invia]**.
1. Attendere che lo stato raggiunga il **[!UICONTROL successo]**.

>[!IMPORTANT]
>
>Con CNAME, Adobe non può aiutarti a modificare, gestire o risolvere i problemi DNS per il sottodominio. Eventuali modifiche future, ad esempio l’aggiunta di un nuovo CNAME per un aggiornamento della funzione, devono essere apportate dal team DNS.

### Guardrail del sottodominio {#subdomain-guardrails}

* **Limite predefinito:** 10 sottodomini per organizzazione. Contatta il tuo rappresentante Adobe se ne hai bisogno di più (fino a 100 a seconda del contratto).
* **Propagazione DNS:** Consenti la propagazione globale delle modifiche per 24-48 ore. La convalida può non riuscire semplicemente perché il DNS non è ancora stato propagato.
* **Riutilizzo del sottodominio:** Un sottodominio già utilizzato da un altro prodotto Adobe (Marketo Engage, Adobe Campaign) non può essere riutilizzato in Prime.

## DMARC, SPF e DKIM {#dmarc-spf-dkim}

DMARC, SPF e DKIM sono standard di autenticazione e-mail. Assieme, dimostrano ai server di posta che il messaggio è stato effettivamente inviato per conto del dominio e non è stato oggetto di spoofing. Gli ISP moderni - Gmail, Yahoo, Microsoft - richiedono questi standard per i mittenti in blocco.

| Record | Sta per | Finalità |
| ------ | ---------- | ------- |
| **SPF** | Framework criteri mittente | Elenca gli IP del server di posta autorizzati a inviare messaggi dal dominio. I server di ricezione rifiutano la posta da indirizzi IP non inclusi nell&#39;elenco. Adobe crea e mantiene automaticamente il record SPF quando deleghi un sottodominio (completamente delegato). |
| **DKIM** | Posta identificata DomainKeys | Una firma crittografica aggiunta a ogni e-mail in uscita. Il server ricevente verifica la firma in base a una chiave pubblica pubblicata nel DNS. Adobe genera automaticamente le chiavi DKIM e i record DNS durante la delega del sottodominio. |
| **DMARC** | Autenticazione, reporting e conformità dei messaggi basati su dominio | Indica ai server riceventi cosa fare in caso di errore di SPF o DKIM e fornisce report sui risultati dell&#39;autenticazione. DMARC dispone di tre modalità di criteri: nessuno, quarantena e rifiuto. |

### Modalità criteri di DMARC {#dmarc-policy-modes}

| Policy | Azione | Quando utilizzare |
| ------ | ------ | ----------- |
| `none` | Monitoraggio | Il server ricevente non esegue alcuna operazione in caso di errore di DMARC, ma invia comunque un report. Utilizza questa opzione quando deleghi un sottodominio per la prima volta a confermare il funzionamento dell’autenticazione senza rischiare la perdita dei messaggi. |
| `quarantine` | Quarantena | Il server ricevente inserisce i messaggi di errore nella cartella di posta indesiderata. |
| `reject` | Rifiuta | Il server ricevente rifiuta i messaggi (non recapitati) che non superano l’autenticazione. Modalità più rigida. Consigliato quando si è sicuri della configurazione dell’autenticazione. |

### Configurare DMARC {#configure-dmarc}

DMARC è configurato al momento della delega del sottodominio, ma puoi anche aggiungere o aggiornare DMARC per un sottodominio già delegato.

1. Nella barra di navigazione a sinistra di [!DNL Adobe Journey Optimizer B2B Prime], espandi **[!UICONTROL Amministrazione]** e seleziona **[!UICONTROL Canali]**.

1. Nel pannello, espandi **[!UICONTROL Impostazioni e-mail]** e seleziona **[!UICONTROL Sottodomini]**.

1. Nell’elenco Sottodomini, individua il sottodominio e controlla la colonna Record di DMARC.

   Se manca un record, viene visualizzato un avviso.

1. Apri il sottodominio e scorri fino alla sezione del record DMARC.

   * Se nel dominio padre esiste già un record DMARC, [!DNL Journey Optimizer B2B Prime] recupera automaticamente i valori. Puoi tenerli o ignorarli.
   * Se non esiste alcun record, scegli **[!UICONTROL Gestisci con Adobe]** e Adobe crea e ospita il record DMARC.

1. Impostare i criteri: `none`, `quarantine` o `reject`. Iniziare con `none` a meno che non si disponga già di una postura DMARC matura nel dominio padre.

1. (Facoltativo) Configurare altri tag di DMARC (`sp` per il criterio del sottodominio, `pct` per la percentuale, `rua` e `ruf` per gli indirizzi di report).

1. Se si utilizza Completamente delegato, fare clic su **[!UICONTROL Salva]**.

   Adobe applica il record automaticamente. Se utilizzi CNAME, copia il record DNS e chiedi al tuo team DNS di aggiungerlo, quindi confermarlo in [!DNL Journey Optimizer B2B Prime].

1. Consenti fino a 48 ore per la propagazione DNS, quindi verifica che l’indicatore di stato DMARC nella pagina del sottodominio sia verde/integro.

>[!TIP]
>
>Inizia con `policy=none` per monitorare i rapporti di autenticazione, quindi passa a `quarantine` e infine a `reject` quando i rapporti mostrano un allineamento corretto di SPF e DKIM. Se si passa direttamente a `reject` senza monitoraggio, i messaggi legittimi potrebbero essere rifiutati.

## Pool IP {#ip-pools}

Un pool IP è un gruppo denominato di indirizzi IP utilizzati per inviare l’e-mail. I pool IP sono fondamentali per la reputazione del mittente: ogni pool ha la propria reputazione rispetto agli ISP, pertanto un problema relativo a un pool (ad esempio, un burst di marketing che attiva reclami di spam) non ne infligge un altro (ad esempio, conferme transazionali).

### Tipi di pool {#pool-types}

| Tipo di pool | Disponibilità | Descrizione |
| --------- | ------------ | ----------- |
| **Pool IP condiviso** | Disponibile in Beta | Un pool di indirizzi IP gestiti da Adobe e condivisi tra molti clienti. La reputazione viene mantenuta da Adobe in tutto il pool. Consigliato per volumi di e-mail da basso a medio e clienti che non desiderano gestire il riscaldamento dell’IP. |
| **Pool IP dedicato** | Roadmap (GA) | Uno o più indirizzi IP allocati esclusivamente alla tua organizzazione. Tu possiedi la reputazione. Consigliato per mittenti con volumi elevati. Include la pianificazione del riscaldamento IP e la gestione dei record PTR. |

### Revisione e assegnazione di un pool IP {#review-ip-pool}

In questa versione, viene eseguito il preprovisioning dei pool IP per la tua organizzazione. Assegna un pool IP durante la creazione di una configurazione del canale e-mail.

1. Nella barra di navigazione a sinistra di [!DNL Adobe Journey Optimizer B2B Prime], espandi **[!UICONTROL Amministrazione]** e seleziona **[!UICONTROL Canali]**.
1. Nel pannello, espandi **[!UICONTROL Impostazioni e-mail]** e seleziona **[!UICONTROL Pool IP]**.
1. Verificare che un pool IP con stato **[!UICONTROL Attivo]** sia disponibile per l&#39;organizzazione.
1. Passa il puntatore del mouse sul pool per visualizzare gli indirizzi IP e i relativi record PTR (DNS inverso).
1. Se la tua organizzazione dispone di più business unit o marchi, pianifica come utilizzare i pool IP (ad esempio, pool di marketing rispetto a pool di webinar) prima di creare configurazioni di canale.

>[!IMPORTANT]
>
>Non combinare il traffico di marketing e quello transazionale sullo stesso pool IP, anche quando il pool condiviso è disponibile. L’impostazione del tipo di e-mail nella configurazione del canale (Marketing vs. Transazionale) governa il comportamento di soppressione, ma le configurazioni del canale devono comunque utilizzare pool distinti, ove possibile.

<!--

### Frequently asked questions {#faq}

| Question | Answer |
| -------- | ------ |
| **Can I reuse the subdomain I already use in Marketo Engage?** | No. A subdomain can only be associated with one Adobe product at a time. Create a new subdomain (for example, mail2.contoso.com) for Prime. |
| **Why does my channel configuration show Failed?** | The most common reasons are: MX record validation failed (your subdomain DNS isn't fully configured); DMARC misalignment; or an IP pool that is in Processing and has never been associated with the selected subdomain. Open the configuration to see the specific reason. |
| **What happens if a personalization token has no value at send time?** | If you defined a fallback with the Handlebars `default` helper, the fallback is used. If not, the token resolves to an empty string. Prime warns you when a token has no fallback and the underlying attribute is not guaranteed by the audience definition. |
| **Can I personalize using account-level attributes?** | Not in this release. Personalization in Prime today supports profile attributes only. |
| **What's the maximum email size?** | 100 KB is the recommended best-practice cap for inbox rendering. Prime warns you in the editor if you exceed it. |
| **Can I migrate existing Marketo email templates into Prime?** | A guided self-serve migration tool — including Velocity-to-Handlebars conversion — is delivered at GA. In this release, you can manually rebuild templates or paste raw HTML. |
| **Will my updates to Marketo assets show up in Prime?** | No. Asset availability in Prime is based on a one-time copy from Marketo Design Studio. Re-uploaded or modified Marketo assets are not reflected in Prime today. Native asset upload and management within Prime is on the Beta roadmap. |

## Glossary {#glossary}

| Term | Definition |
| ---- | ---------- |
| **DKIM** | DomainKeys Identified Mail — cryptographic email signature. |
| **DMARC** | Domain-based Message Authentication, Reporting & Conformance. |
| **FBL** | Feedback Loop — a service ISPs offer to receive spam-complaint reports back to senders. |
| **Handlebars** | JavaScript templating language used in Prime for personalization expressions. |
| **IP pool** | Group of IP addresses used to send email. |
| **MX record** | Mail Exchange DNS record — directs incoming mail to the correct mail servers. |
| **NS record** | Name Server DNS record — used to delegate a subdomain. |
| **PTR record** | Pointer record — reverse DNS that maps an IP address back to a hostname. |
| **RBAC** | Role-Based Access Control. |
| **SPF** | Sender Policy Framework — DNS record listing authorized sending IPs. |
| **Subdomain delegation** | Granting Adobe authority over a portion of your domain (a subdomain) for sending email. |

-->


