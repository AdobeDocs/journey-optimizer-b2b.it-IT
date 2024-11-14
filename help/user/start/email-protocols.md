---
title: Protocolli per il tracciamento e la consegna e-mail
description: Scopri come configurare i protocolli in Marketo Engage per l’utilizzo da parte di Journey Optimizer B2B edition per il tracciamento e le funzioni del canale e-mail.
feature: Setup
role: Admin
source-git-commit: a8ca8b99ddf33b4a64b42b751f7be798274d0084
workflow-type: tm+mt
source-wordcount: '1798'
ht-degree: 0%

---

# Protocolli per il tracciamento e la consegna e-mail

Adobe Journey Optimizer B2B edition sfrutta le funzioni del canale e-mail e il tracciamento degli eventi nel Marketo Engage. Per garantire che la consegna delle e-mail funzioni come previsto per le organizzazioni che utilizzano impostazioni restrittive del firewall o del server proxy, un amministratore di sistema deve aggiungere determinati domini e intervalli di indirizzi IP al inserisco nell&#39;elenco Consentiti di.

>[!NOTE]
>
>Se l’organizzazione sta già utilizzando l’istanza del Marketo Engage connesso per eseguire le operazioni di marketing, questi protocolli e configurazioni dovrebbero essere già in uso.

Accertati che i seguenti domini (incluso l’asterisco) siano aggiunti al elenco Consentiti per abilitare tutte le risorse di Marketo Engage e i socket web:

* `*.experience.adobe.com`
* `*.adobe.net`
* `*.marketo.com`
* `*.marketodesigner.com`
* `*.mktoweb.com`

Segui i passaggi seguenti per garantire il tracciamento e la consegna e-mail:

1. [Crea record DNS per ](#create-dns-records-for-landing-pages-and-email)
1. [Configurazione di SPF e DKIM](#set-up-spf-and-dkim)
1. [Configurare DMARC](#set-up-dmarc)
1. [Configurare i record MX per il dominio](#set-up-mx-records-for-your-domain)
1. [Aggiungere indirizzi IP in uscita ai inserisce nell&#39;elenco Consentiti di](#outbound-ip-addresses)

## Crea record DNS per <!-- landing pages and --> e-mail

La connessione di un record CNAME consente agli addetti al marketing di ospitare versioni web di e-mail, pagine di destinazione e blog con un branding coerente che migliora il traffico e le conversioni. Si consiglia vivamente di aggiungere i CNAME all’host del dominio principale affinché il Marketo Engage ospiti le risorse web incentrate sul marketing. In qualità di amministratore, devi collaborare con il team Marketing per pianificare e implementare un record CNAME per i collegamenti di tracciamento inclusi nelle e-mail inviate tramite il Marketo Engage.
<!-- As an administrator, you should work with your Marketing team to plan and implement two CNAME records. The first one is for landing page URLs, so that the landing pages appear in URLs that reflect your domain and not Adobe Marketo Engage (the actual host). The second one is for the tracking links that are included in the emails sent through Marketo Engage.

### Add the CNAME for landing pages

Add the landing page CNAME to your DNS record, so that `[YourLandingPageCNAME]` points to the unique account string that is assigned to your landing pages. Log in to your domain registrar's site and enter the landing page CNAME and account string. This entry usually involves three fields:

* Alias: Enter `[YourLandingPageCNAME]`
* Type: CNAME
* Point to: Enter `[MunchkinID].mktoweb.com`
-->

### Aggiungi il CNAME per i collegamenti di tracciamento e-mail

Aggiungi il CNAME e-mail in modo che `[YourEmailCNAME]` punti a `[MktoTrackingLink]`, che è il collegamento di tracciamento predefinito assegnato da quel Marketo Engage, nel formato:

`[YourEmailCNAME].[YourDomain].com` NEL CNAME `[MktoTrackingLink]`

Ad esempio:

`pages.abc.com IN CNAME mkto-a0244.com`

>[!NOTE]
>
>Il valore `[MktoTrackingLink]` deve essere il dominio di branding predefinito.

### Eseguire il provisioning del certificato SSL

Contatta il [supporto Adobe](https://experienceleague.adobe.com/home?lang=en&amp;support-tab=home#support){target="_blank"} per avviare il processo di provisioning di un certificato SSL.

Il completamento di questo processo può richiedere fino a tre giorni lavorativi.

## Configurazione di SPF e DKIM

Il team marketing deve fornire le informazioni DKIM (Domain Keys Identified Mail) da aggiungere al record di risorse DNS. Segui questi passaggi per configurare DKIM e SPF (Sender Policy Framework), quindi avvisa il team Marketing quando viene aggiornato.

1. Per impostare SPF, aggiungere la riga seguente alle voci DNS:

   ```
   [CompanyDomain] IN TXT v=spf1 mx ip4:[CorpIP]  
   include: mktomail.com ~all
   ```

   Se disponi già di un record SPF nella voce DNS, aggiungi semplicemente quanto segue:

   ```
   include: mktomail.com
   ```

   Sostituisci `CompanyDomain` con il dominio principale del tuo sito Web (ad esempio `company.com/`) e `CorpIP` con l&#39;indirizzo IP del tuo server di posta elettronica aziendale (ad esempio `255.255.255.255`). Se prevedi di inviare e-mail da più domini tramite il Marketo Engage, aggiungi questa riga per ciascun dominio (su una riga).

1. Per DKIM, crea record di risorse DNS per ciascun dominio.

   Aggiungi i record host e i valori TXT per ciascun dominio:

   `[DKIMDomain1]`: il record host è `[HostRecord1]` e il valore TXT è `[TXTValue1]`.

   `[DKIMDomain2]`: il record host è `[HostRecord2]` e il valore TXT è `[TXTValue2]`.

   Copia `HostRecord` e `TXTValue` per ciascun dominio DKIM dopo aver seguito le [istruzioni](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/email-marketing/deliverability/set-up-a-custom-dkim-signature){target="_blank"} nella documentazione del Marketo Engage. Puoi verificare i domini in Journey Optimizer B2B edition (vedi [SPF/DKIM](../admin/configure-channels-emails.md#spfdkim)).

## Configurare DMARC

DMARC (Domain-based Message Authentication, Reporting, and Conformance) è un protocollo di autenticazione utilizzato per aiutare le organizzazioni a proteggere il proprio dominio da utilizzi non autorizzati. Estende i protocolli di autenticazione esistenti, come SPF e DKIM, per informare i server destinatari sulle azioni da intraprendere in caso di errore di autenticazione nel dominio. DMARC è facoltativo, ma è vivamente consigliato perché contribuisce a proteggere il tuo marchio e la tua reputazione. I principali fornitori, come Google e Yahoo, hanno iniziato a richiedere l’utilizzo di DMARC per i mittenti in blocco a partire da febbraio 2024.

Affinché DMARC funzioni, è necessario disporre di almeno uno dei seguenti record TXT DNS:

* Un SPF valido
* Un record DKIM valido per il dominio FROM: (consigliato per Marketo Engage e Journey Optimizer B2B edition)

È inoltre necessario disporre di un record TXT DNS specifico di DMARC per il dominio `FROM:`. Facoltativamente, puoi definire un indirizzo e-mail che specifichi dove i rapporti di DMARC devono essere inviati all’interno della tua organizzazione per il monitoraggio dei rapporti.

### Esempio di flusso di lavoro DMARC

>[!TIP]
>
>È consigliabile implementare DMARC come _rollout lento_. Intensificare i criteri di DMARC da `p=none` a `p=quarantine` e quindi a `p=reject` per comprendere il potenziale impatto e impostare i criteri di DMARC in modo da ridurre l&#39;allineamento su SPF e DKIM.

Se ricevi rapporti di DMARC, devi effettuare le seguenti operazioni:

1. Utilizza `p=none` e analizza il feedback e i report che ricevi. I rapporti indicano al destinatario di non eseguire azioni nei confronti dei messaggi che non superano l’autenticazione e di inviare i rapporti e-mail al mittente.

   * Se l&#39;autenticazione dei messaggi legittimi non riesce, esaminare e risolvere i problemi con SPF/DKIM.

   * Determina se SPF o DKIM sono allineati e trasmette l’autenticazione per tutte le e-mail legittime.

   * Rivedi i rapporti per garantire che i risultati siano quelli previsti in base ai criteri SPF/DKIM.

1. Regolare il criterio su `p=quarantine`, che indica al server di posta elettronica ricevente di mettere in quarantena le e-mail che non riescono a eseguire l&#39;autenticazione (in genere inserendo tali messaggi nella cartella di posta indesiderata).

   Rivedi i rapporti per assicurarti che i risultati siano quelli previsti.

1. Se si è soddisfatti del comportamento dei messaggi al livello `p=quarantine`, è possibile modificare i criteri in (`p=reject`).

   Il criterio di rifiuto indica al destinatario di rifiutare (non recapitare) qualsiasi e-mail per il dominio che non supera l’autenticazione. Con questo criterio abilitato, solo i messaggi e-mail verificati come autenticati al 100% dal dominio hanno la possibilità di inserire messaggi nella casella in entrata.

   >[!CAUTION]
   >
   >Utilizza questo criterio con cautela e stabilisci se è appropriato per la tua organizzazione.

### Reportistica di DMARC

DMARC offre la possibilità di ricevere rapporti relativi alle e-mail che non superano SPF/DKIM. Esistono due diversi rapporti generati dai server ISP come parte del processo di autenticazione. I mittenti possono ricevere questi rapporti tramite i tag RUA/RUF nella propria policy DMARC.

* **Aggregate Reports (RUA)**: non contiene dati PII (personalmente identificabili) che potrebbero essere sensibili ai requisiti del GDPR (General Data Protection Regulation, Regolamento generale sulla protezione dei dati).

* **Rapporti forensi (RUF)** - Contengono indirizzi e-mail sensibili ai requisiti RGPD. Prima di implementare questo rapporto, verifica i criteri organizzativi per la gestione delle informazioni che devono essere conformi ai requisiti RGPD.

L’utilizzo principale di questi rapporti consiste nel ricevere una panoramica delle e-mail che vengono tentate di spoofing. Si tratta di rapporti altamente tecnici che è consigliabile digerire tramite uno strumento di terze parti.

### Esempio di record DMARC

* Record minimo nudo: `v=DMARC1; p=none`

* Record che reindirizza a un indirizzo e-mail per ricevere i report: `v=DMARC1; p=none;  rua=mailto:emaill@domain.com;  ruf=mailto:email@domain.com`

### Tag DMARC

I record DMARC contengono più componenti denominati _tag DMARC_. Ogni tag ha un valore che specifica un determinato aspetto di DMARC.

| Nome tag | Utilizzo di  | Funzione | Esempio | Valore predefinito |
|-----------|------------------------|-----------|----------|-----------------------------------|
| `v` | Obbligatorio | Specifica la versione. Esiste una sola versione, quindi ha un valore fisso di `v=DMARC1` | V=DMARC1 DMARC1 | DMARC1 |
| `p` | Obbligatorio | Specifica il criterio DMARC, che indica al destinatario di segnalare, mettere in quarantena o rifiutare un messaggio e-mail che non supera i controlli di autenticazione. | `p=none`, `p=quarantine` o `p=reject` | - |
| `fo` | Facoltativo | Consente al proprietario del dominio di specificare le opzioni di reporting. | `0`: Genera report se entrambi SPF e DKIM non riescono <br> `1` - Genera report se SPF o DKIM non riesce <br> `d` - Genera report se DKIM non riesce <br> `s` - Genera report se SPF non riesce | `1` (consigliato per i report DMARC) |
| `pct` | Facoltativo | Specifica la percentuale di messaggi soggetti a filtro. | `pct=20` | `100` |
| `rua` | Facoltativo (consigliato) | Indica dove vengono consegnati i rapporti aggregati. | `rua=mailto:aggrep@example.com` | - |
| `ruf` | Facoltativo (consigliato) | Indica dove vengono consegnati i rapporti forensi. | `ruf=mailto:authfail@example.com` | - |
| `sp` | Facoltativo | Specifica il criterio DMARC per i sottodomini del dominio padre. | `sp=reject` | - |
| `adkim` | Facoltativo | Specifica un allineamento rigido (`s`) o rilassato (`r`). L&#39;allineamento semplificato indica che il dominio viene utilizzato nella firma DKIM e può essere un sottodominio dell&#39;indirizzo `From:`. L&#39;allineamento rigido indica che il dominio viene utilizzato nella firma DKIM e deve corrispondere esattamente al dominio utilizzato nell&#39;indirizzo `From:`. | `adkim=r` | `r` |
| `aspf` | Facoltativo | Può essere rigido (`s`) o rilassato (`r`). La modalità semplificata indica che il dominio del percorso restituito può essere un sottodominio dell&#39;indirizzo `From:`. La modalità rigorosa indica che il dominio del percorso restituito deve corrispondere esattamente all&#39;indirizzo `From:`. | `aspf=r` | `r` |

Per informazioni dettagliate su DMARC e su tutte le sue opzioni, consulta [https://dmarc.org/](https://dmarc.org/){target="_blank"}.

### Implementazione DMARC per il Marketo Engage

Esistono due tipi di allineamento per DMARC:

* Allineamento **DKIM** (Domain Keys Identified Mail): il dominio specificato nell&#39;intestazione `From:` di un&#39;e-mail corrisponde alla firma DKIM. La firma DKIM contiene un valore `d=` in cui il dominio è specificato per la corrispondenza con il dominio intestazione `From:`.

  L’allineamento DKIM verifica se il mittente è autorizzato a inviare e-mail dal dominio e se nessun contenuto è stato modificato durante il transito e-mail. Per implementare DMARC allineato a DKIM:

   * Imposta DKIM per il dominio MAIL FROM del messaggio. Utilizza le [istruzioni](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/email-marketing/deliverability/set-up-a-custom-dkim-signature){target="_blank"} nella documentazione del Marketo Engage.

   * Configurare DMARC per il dominio DKIM MAIL FROM.

  >[!NOTE]
  >
  >L’allineamento DKIM è consigliato per il Marketo Engage.

* Allineamento **SPF** (Sender Policy Framework): il dominio nell&#39;intestazione `From:` deve corrispondere al dominio nell&#39;intestazione Return-Path:. Se entrambi i domini DNS sono uguali, SPF corrisponde (allinea) e restituisce un risultato positivo. Per implementare DMARC allineato a SPF:

   * Imposta il dominio Return-Path con marchio.

      * Configura il record SPF appropriato.
      * Modificare il record MX in modo che punti al record MX predefinito per il data center da cui viene inviata la posta

   * Configura DMARC per il dominio del percorso di ritorno a marchio.

  >[!NOTE]
  >
  >L&#39;allineamento rigoroso dell&#39;SPF non è supportato o consigliato per il Marketo Engage.

### IP dedicati e pool condiviso

Se invii messaggi tramite il Marketo Engage tramite un IP dedicato e non hai implementato un percorso di ritorno con marchio (o non sei sicuro di averlo), apri un ticket con [Supporto Adobe](https://experienceleague.adobe.com/home?lang=en&amp;support-tab=home#support){target="_blank"}.

Gli IP attendibili sono un pool condiviso di IP riservati agli utenti con volumi di dati inferiori che inviano meno di 75.000 messaggi al mese e non sono idonei per un IP dedicato. Tali utenti devono inoltre soddisfare i requisiti delle best practice.

* Se si invia posta tramite un Marketo Engage utilizzando un pool condiviso di IP, è possibile verificare se si è idonei per gli IP attendibili [candidandosi al programma intervallo di invio IP attendibili](https://na-sjg.marketo.com/lp/marketoprivacydemo/Trusted-IP-Sending-Range-Program.html){target="_blank"}. Il percorso di ritorno del marchio è incluso durante l’invio da IP attendibili del Marketo Engage. Se approvato per questo programma, contatta il supporto Adobe per impostare il percorso di ritorno del marchio.

* Se invii più di 100.000 messaggi al mese e desideri inviare e-mail tramite il Marketo Engage utilizzando IP condivisi, contatta il Team account di Adobe (il tuo account manager) per acquistare un IP dedicato.

## Configurare i record MX per il dominio

Un record MX ti consente di ricevere e-mail al dominio da cui stai inviando l’e-mail per elaborare le risposte e i risponditori automatici. Se invii dal dominio aziendale, è probabilmente già configurato. In caso contrario, in genere è possibile configurarlo per eseguire la mappatura sul record MX del dominio aziendale.

## Indirizzi IP in uscita

Per connessione in uscita si intende una connessione effettuata dal Marketo Engage a un server su Internet per conto dell&#39;utente. L&#39;organizzazione IT e alcuni partner/fornitori possono utilizzare i inserisce nell&#39;elenco Consentiti di per limitare l&#39;accesso ai server. In tal caso, devi fornire loro blocchi di indirizzi IP in uscita di Marketo Engage da aggiungere ai loro inserisce nell&#39;elenco Consentiti di indirizzi.

<!-- ### Webhooks

Marketo Engage webhooks are an outbound integration mechanism. When a Smart Campaign executes a _Call Webhook_ flow action, it makes an HTTP request to an external web service. If the web service publisher uses an allowlist on the firewall of the network where the external web service is located, the publisher must add the IP address blocks listed below to their allowlist. For more information, see [Create a webhook](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/additional-integrations/create-a-webhook){target="_blank"} and [Call Webhook](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/core-marketo-concepts/smart-campaigns/flow-actions/call-webhook){target="_blank"} in the Marketo Engage documentation.

### CRM sync

Marketo Engage Salesforce CRM Sync and Microsoft Dynamics Sync are integration mechanisms that make outbound HTTP requests to APIs published by your CRM vendor. Ensure that your IT organization does not block any of the IP address blocks below from accessing your CRM vendor APIs. For more information, see [Add an Existing Salesforce Field to the Marketo Sync](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/crm-sync/salesforce-sync/sfdc-sync-details/add-an-existing-salesforce-field-to-the-marketo-sync){target="_blank"} and [Understanding the Microsoft Dynamics Sync](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/crm-sync/microsoft-dynamics/understanding-the-microsoft-dynamics-sync){target="_blank"} in the Marketo Engage documentation. -->

## Blocchi di indirizzi IP in uscita

Gli elenchi seguenti coprono tutti i server di Marketo Engage che effettuano chiamate in uscita. Fare riferimento a questi elenchi per configurare un inserisco nell&#39;elenco Consentiti IP, un server, un firewall, un elenco di controllo di accesso, un gruppo di sicurezza o un servizio di terze parti per ricevere connessioni in uscita dal Marketo Engage.

| Blocco IP (notazione CIDR) | Indirizzo IP individuale |
| ------------------------ | --------------------- |
| <ul><li>`94.236.119.0/26`</li><li>`103.237.104.0/22`</li><li>`130.248.172.0/24`</li><li>`130.248.173.0/24`</li><li>`130.248.244.88/29`</li><li>`185.28.196.0/22`</li><li>`192.28.144.0/20`</li><li>`192.28.160.0/19`</li><li>`199.15.212.0/22`</li></ul> | <ul><li>`13.237.155.207`</li><li>`13.55.192.247`</li><li>`18.200.201.81`</li><li>`34.247.24.245`</li><li>`35.165.244.220`</li><li>`44.235.171.179`</li><li>`52.20.211.99`</li><li>`52.64.109.86`</li><li>`54.160.246.246`</li><li>`54.212.167.17`</li><li>`54.220.138.65`</li><li>`54.237.141.197`</li><li>`130.248.168.16`</li><li>`130.248.168.17`</li></ul> |
