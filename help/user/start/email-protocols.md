---
title: Configurazione per il tracciamento e la consegna e-mail
description: 'Configurare i protocolli di consegna e-mail: configura DNS, SPF, DKIM, DMARC e l’elenco Consentiti IP per garantire tracciamento e recapitabilità ottimali in Journey Optimizer B2B Edition.'
feature: Setup, Channels
role: Admin
exl-id: 3d56f147-ad0a-4686-b14e-375c2eca8806
source-git-commit: 944d2616fa21e7f8d2f8c439eaa2f5e529dacb84
workflow-type: tm+mt
source-wordcount: '2396'
ht-degree: 99%

---

# Configurazione per il tracciamento e la consegna e-mail

Adobe Journey Optimizer B2B edition sfrutta le funzioni del canale e-mail e il tracciamento degli eventi nell’istanza Marketo Engage allegata. Per garantire che la consegna delle e-mail funzioni come previsto per le organizzazioni che utilizzano impostazioni restrittive del firewall o del server proxy, un amministratore di sistema deve aggiungere determinati domini e intervalli di indirizzi IP all’elenco Consentiti.

>[!NOTE]
>
>Se la tua organizzazione sta già utilizzando l’istanza di Marketo Engage connessa per eseguire le operazioni di marketing, questi protocolli e configurazioni dovrebbero essere già in uso.

Assicurati che i seguenti domini (incluso l’asterisco) siano aggiunti all’elenco Consentiti per abilitare tutte le risorse Marketo Engage e i socket web:

* `*.experience.adobe.com`
* `*.adobe.net`
* `*.marketo.com`
* `*.marketodesigner.com`
* `*.mktoweb.com`

Segui i passaggi seguenti per garantire il tracciamento e la consegna e-mail:

1. [Creare record DNS per pagine di destinazione e e-mail](#create-dns-records-for-landing-pages-and-email)
1. [Configura SPF e DKIM](#set-up-spf-and-dkim)
1. [Configura DMARC](#set-up-dmarc)
1. [Configura i record MX per il dominio](#set-up-mx-records-for-your-domain)
1. [Aggiungi indirizzi IP in uscita all’elenco Consentiti](#outbound-ip-addresses)

>[!NOTE]
>
>I servizi di recapito messaggi e-mail e i servizi di consulenza sono offerte a pagamento separate da Adobe. Se hai bisogno o desideri il supporto del team di recapito messaggi per l’istanza di Journey Optimizer B2B edition, devi acquistare uno dei pacchetti Email Deliverability Services (Essentials, Enhanced o Plus) per tale istanza. Questo è indipendente da qualsiasi pacchetto di consegna su un’istanza Marketo Engage preesistente. I servizi di recapito messaggi sono collegati per istanza, non per organizzazione. Il supporto per il recapito messaggi in entrambe le istanze richiede due pacchetti di servizi di recapito messaggi separati. Ogni volta che viene fornito un nuovo IP per Journey Optimizer B2B edition, è necessario un nuovo pacchetto di Servizi di recapito messaggi per il riscaldamento dell’IP e il supporto continuo per il recapito messaggi.

## Creare record DNS per pagine di destinazione e e-mail

La connessione di un record CNAME consente ai marketer di ospitare versioni web di e-mail, pagine di destinazione e blog con un branding coerente che migliora il traffico e le conversioni. Si consiglia vivamente di aggiungere i CNAME all’host del dominio principale affinché Marketo Engage possa ospitare le risorse web incentrate sul marketing. In qualità di amministratore, devi collaborare con il team di marketing per pianificare e implementare un record CNAME per i collegamenti di tracciamento inclusi nelle e-mail inviate tramite Marketo Engage.

In qualità di amministratore, devi collaborare con il team Marketing per pianificare e implementare due record CNAME. Il primo è per gli URL delle pagine di destinazione, in modo che le pagine di destinazione vengano visualizzate in URL che riflettono il dominio e non Adobe Marketo Engage (l’host effettivo). Il secondo è per i collegamenti di tracciamento inclusi nelle e-mail inviate tramite Marketo Engage.

### Aggiungi il CNAME per le pagine di destinazione

Aggiungi il CNAME della pagina di destinazione al tuo record DNS, in modo che `[YourLandingPageCNAME]` punti alla stringa account univoca assegnata alle tue pagine di destinazione. Accedi al sito del tuo registrar di dominio e immetti il CNAME della pagina di destinazione e la stringa dell’account. Questa voce in genere include tre campi:

* Alias: immettere `[YourLandingPageCNAME]`
* Tipo: CNAME
* Puntare a: immettere `[MunchkinID].mktoweb.com`

### Aggiungere CNAME per i collegamenti di tracciamento e-mail

Aggiungi il CNAME e-mail in modo che `[YourEmailCNAME]` punti a `[MktoTrackingLink]`, che è il collegamento di tracciamento predefinito assegnato da Marketo Engage, nel formato:

`[YourEmailCNAME].[YourDomain].com` IN CNAME `[MktoTrackingLink]`

Ad esempio:

`pages.abc.com IN CNAME mkto-a0244.com`

>[!NOTE]
>
>Il valore `[MktoTrackingLink]` deve essere il [dominio di branding](../admin/configure-channels-emails.md#branding-domains) predefinito.

### Eseguire il provisioning del certificato SSL

Contatta il [supporto Adobe](https://experienceleague.adobe.com/home?lang=it&support-tab=home#support){target="_blank"} per avviare il processo di provisioning di un certificato SSL.

Il completamento di questo processo può richiedere fino a tre giorni lavorativi.

## Configura SPF e DKIM

Il team di marketing deve fornire le informazioni di DKIM (Domain Keys Identified Mail) da aggiungere al record di risorse DNS. Segui questi passaggi per configurare DKIM e SPF (Sender Policy Framework), quindi avvisa il team di marketing quando l’aggiornamento è completato.

Puoi utilizzare la stessa configurazione DKIM per l’istanza Marketo Engage di produzione e l’istanza B2B edition di Journey Optimizer associata. Nell’istanza allegata, crea lo stesso dominio esatto dell’istanza Marketo Engage. I valori del selettore e della crittografia non devono corrispondere. Dopo aver aggiunto il dominio all’istanza di Journey Optimizer B2B edition, apri un ticket di supporto Adobe per richiedere che la configurazione di DKIM sia condivisa dall’istanza di Marketo Engage alla nuova istanza. Specifica il prefisso Marketo Engage (Munchkin ID) e il nuovo prefisso Journey Optimizer B2B edition (Munchkin ID).

1. Per configurare SPF, aggiungi la riga seguente alle voci DNS:

   ```
   [CompanyDomain] IN TXT v=spf1 mx ip4:[CorpIP]  
   include: mktomail.com ~all
   ```

   Se disponi già di un record SPF nella voce DNS, aggiungi semplicemente quanto segue:

   ```
   include: mktomail.com
   ```

   Sostituisci `CompanyDomain` con il dominio principale del tuo sito web (ad esempio `company.com/`) e `CorpIP` con l’indirizzo IP del server di posta elettronica aziendale (ad esempio `255.255.255.255`). Se prevedi di inviare e-mail da più domini tramite Marketo Engage, aggiungi questa riga per ciascun dominio (su una sola riga).

1. Per DKIM, crea un record di risorse DNS per ciascun dominio.

   Aggiungi i record host e i valori TXT per ciascun dominio:

   `[DKIMDomain1]`: il record host è `[HostRecord1]` e il valore TXT è `[TXTValue1]`.

   `[DKIMDomain2]`: il record host è `[HostRecord2]` e il valore TXT è `[TXTValue2]`.

   Copia `HostRecord` e `TXTValue` per ciascun dominio DKIM dopo aver seguito le [istruzioni](https://experienceleague.adobe.com/it/docs/marketo/using/product-docs/email-marketing/deliverability/set-up-a-custom-dkim-signature){target="_blank"} nella documentazione di Marketo Engage. Puoi verificare i domini in Journey Optimizer B2B Edition (consulta [SPF/DKIM](../admin/configure-channels-emails.md#spfdkim)).

## Configura DMARC

DMARC (Domain-based Message Authentication, Reporting, and Conformance) è un protocollo di autenticazione utilizzato per aiutare le organizzazioni a proteggere il proprio dominio da utilizzi non autorizzati. Estende i protocolli di autenticazione esistenti, come SPF e DKIM, per informare i server destinatari sulle azioni da intraprendere in caso di errore di autenticazione nel dominio. Il protocollo DMARC è facoltativo, ma è vivamente consigliato perché contribuisce a proteggere il tuo marchio e la tua reputazione. I principali fornitori, come Google e Yahoo, hanno iniziato a richiedere l’utilizzo di DMARC per i mittenti in blocco a partire da febbraio 2024.

Affinché il protocollo DMARC funzioni, devi disporre di almeno uno dei seguenti record TXT DNS:

* Un SPF valido
* Un record DKIM valido per il dominio FROM: (consigliato per [!DNL Marketo Engage] e [!UICONTROL Journey Optimizer B2B edition])

Devi inoltre disporre di un record TXT DNS specifico di DMARC per il dominio `FROM:`. Facoltativamente, puoi definire un indirizzo e-mail che specifichi dove devono essere inviati i rapporti di DMARC per il monitoraggio all’interno della tua organizzazione.

### Esempio di flusso di lavoro DMARC

>[!TIP]
>
>È consigliabile implementare DMARC come _rollout lento_. Rafforza i criteri di DMARC da `p=none` a `p=quarantine` e quindi a `p=reject` per comprendere il potenziale impatto e impostare i criteri di DMARC per un allineamento più flessibile su SPF e DKIM.

Se ricevi report DMARC, devi effettuare le seguenti operazioni:

1. Utilizza `p=none` e analizza il feedback e i report che ricevi. I report indicano al destinatario di non eseguire azioni nei confronti dei messaggi che non superano l’autenticazione e inviano i rapporti e-mail al mittente.

   * Se l’autenticazione dei messaggi legittimi non riesce, esamina e risolvi i problemi con SPF/DKIM.

   * Determina se SPF o DKIM sono allineati e consentono l’autenticazione di tutte le e-mail legittime.

   * Esamina i report per assicurarti che i risultati corrispondano a quelli previsti in base ai criteri SPF/DKIM.

1. Regola il criterio su `p=quarantine`, che indica al server di posta elettronica ricevente di mettere in quarantena i messaggi che non riescono ad autenticarsi (in genere inserendo tali messaggi nella cartella spam).

   Esamina i report per assicurarti che i risultati siano quelli previsti.

1. Se il comportamento dei messaggi al livello `p=quarantine` ti soddisfa, puoi modificare il criterio in (`p=reject`).

   Il criterio di rifiuto indica al destinatario di non accettare (non recapitare) qualsiasi e-mail del dominio che non riesce ad autenticarsi. Con questa regola abilitata, solo l’e-mail verificata come autenticata al 100% dal tuo dominio ha la possibilità di venire inserita nella casella in entrata.

   >[!CAUTION]
   >
   >Utilizza questa regola con cautela e determina se è appropriata per la tua organizzazione.

### Reporting DMARC

DMARC offre la possibilità di ricevere rapporti relativi alle e-mail che non superano SPF/DKIM. Esistono due diversi report generati dai fornitori di servizi ISP come parte del processo di autenticazione. I mittenti possono ricevere questi report tramite i tag RUA/RUF nel proprio criterio DMARC.

* **Report aggregati (RUA):** non contengono PII (informazioni personali identificabili) che potrebbero essere sensibili secondo il GDPR (regolamento generale sulla protezione dei dati).

* **Report forensi (RUF)**: contengono indirizzi e-mail con dati sensibili secondo il GDPR. Prima di implementare questo report, verifica il criterio dell’organizzazione per la gestione delle informazioni che devono essere conformi al GDPR.

L’utilizzo principale di questi rapporti è quello di ricevere una panoramica delle e-mail che sono un tentativo di spoofing. Si tratta di report estremamente tecnici, che possono essere elaborati al meglio attraverso un strumento di terze parti.

### Esempio di record DMARC

* Record minimo accettabile: `v=DMARC1; p=none`

* Record diretto a un indirizzo e-mail per ricevere i report: `v=DMARC1; p=none;  rua=mailto:emaill@domain.com;  ruf=mailto:email@domain.com`

### Tag DMARC

I record DMARC contengono più componenti denominati _tag DMARC_. Ogni tag ha un valore che specifica un determinato aspetto di DMARC.

| Nome tag | Utilizzo | Funzione | Esempio | Valore predefinito |
|-----------|------------------------|-----------|----------|-----------------------------------|
| `v` | Obbligatorio | Specifica la versione. Esiste una sola versione, quindi ha un valore fisso di `v=DMARC1` | V=DMARC1 DMARC1 | DMARC1 |
| `p` | Obbligatorio | Specifica il criterio DMARC, che indica al destinatario di segnalare, mettere in quarantena o rifiutare un messaggio e-mail che non supera i controlli di autenticazione. | `p=none`, `p=quarantine` oppure `p=reject` | - |
| `fo` | Facoltativo | Consente al proprietario del dominio di specificare le opzioni di reporting. | `0`: genera report se sia SPF che DKIM falliscono <br> `1`: genera report se SPF o DKIM fallisce <br> `d`: genera report se DKIM fallisce <br> `s`: genera report se SPF fallisce | `1` (consigliato per i report DMARC) |
| `pct` | Facoltativo | Specifica la percentuale di messaggi sottoposti a filtro. | `pct=20` | `100` |
| `rua` | Facoltativo (consigliato) | Indica dove vengono consegnati i report aggregati. | `rua=mailto:aggrep@example.com` | - |
| `ruf` | Facoltativo (consigliato) | Indica dove vengono consegnati i report forensi. | `ruf=mailto:authfail@example.com` | - |
| `sp` | Facoltativo | Specifica il criterio DMARC per i sottodomini del dominio principale. | `sp=reject` | - |
| `adkim` | Facoltativo | Specifica un allineamento rigoroso (`s`) o più flessibile (`r`). L’allineamento più flessibile indica che il dominio viene utilizzato nella firma DKIM e può essere un sottodominio dell’indirizzo `From:`. L’allineamento rigoroso indica che il dominio viene utilizzato nella firma DKIM e deve corrispondere esattamente al dominio utilizzato nell’indirizzo `From:`. | `adkim=r` | `r` |
| `aspf` | Facoltativo | Può essere rigoroso (`s`) o più flessibile (`r`). La modalità più flessibile indica che il dominio Return-Path può essere un sottodominio dell’indirizzo `From:`. La modalità rigorosa indica che il dominio Return-Path deve corrispondere esattamente all’indirizzo `From:`. | `aspf=r` | `r` |

Per informazioni dettagliate su DMARC e su tutte le sue opzioni, consulta [https://dmarc.org/](https://dmarc.org/){target="_blank"}.

### Implementazione di DMARC per Marketo Engage

Esistono due tipi di allineamento per DMARC:

* Allineamento **DKIM** (Domain Keys Identified Mail): il dominio specificato nell’intestazione `From:` di un’e-mail corrisponde alla firma DKIM. La firma DKIM contiene un valore `d=` in cui il dominio è specificato per corrispondere al dominio di intestazione `From:`.

  L’allineamento DKIM convalida se il mittente è autorizzato a inviare e-mail dal dominio e verifica che non sia stato modificato alcun contenuto durante il transito e-mail. Per implementare DMARC allineato a DKIM:

   * Imposta DKIM per il dominio MAIL FROM del messaggio. Utilizza le [istruzioni](https://experienceleague.adobe.com/it/docs/marketo/using/product-docs/email-marketing/deliverability/set-up-a-custom-dkim-signature){target="_blank"} nella documentazione di Marketo Engage.

   * Configura DMARC per il dominio MAIL FROM DKIM.

  >[!NOTE]
  >
  >Per Marketo Engage è consigliato l’allineamento DKIM.

* Allineamento **SPF** (Sender Policy Framework): il dominio nell’intestazione `From:` deve corrispondere al dominio nell’intestazione di Return-Path. Se entrambi i domini DNS sono uguali, SPF corrisponde (si allinea) e restituisce un risultato positivo. Per implementare DMARC allineato a SPF:

   * Imposta il dominio Return-Path con brand.

      * Configura il record SPF appropriato.
      * Modifica il record MX in modo che punti al record MX predefinito per il data center da cui viene inviata l’e-mail.

   * Configura DMARC per il dominio di Return-Path con brand.

  >[!NOTE]
  >
  >L’allineamento rigoroso di SPF non è supportato o consigliato per Marketo Engage.

### IP dedicati e pool condiviso

Se invii messaggi tramite Marketo Engage con un IP dedicato e non hai implementato (o non hai la certezza di aver implementato) un Return-Path con brand, apri un ticket con il [supporto Adobe](https://experienceleague.adobe.com/home?lang=it&support-tab=home#support){target="_blank"}.

>[!BEGINSHADEBOX]

**Migrazione di IP dedicati a Journey Optimizer B2B Edition**

Se disponi di IP dedicati, la nuova istanza di Journey Optimizer B2B edition deve essere creata nella stessa area dell’istanza di Marketo Engage esistente. Se la nuova istanza si trova in un’area diversa, non è possibile condividere l’IP esistente. Se l&#39;area geografica corrisponde, aprire un ticket con [Supporto Adobe](https://experienceleague.adobe.com/home?lang=it&support-tab=home#support){target="_blank"} per richiedere la condivisione dell&#39;IP e dei gruppi di binding esistenti con la nuova istanza. Specifica il prefisso Marketo Engage (Munchkin ID) e il nuovo prefisso Journey Optimizer B2B edition (Munchkin ID).

Con questa richiesta, Adobe replica gli stessi IP, i gruppi di binding e i domini Return-Path configurati dell’istanza Marketo Engage esistente. Quando gli IP vengono condivisi tra l’istanza di Marketo Engage e Journey Optimizer B2B edition, entrambi li utilizzano contemporaneamente (un invio da Marketo Engage e un invio da Journey Optimizer B2B edition utilizzano gli stessi IP).

>[!ENDSHADEBOX]

Gli IP attendibili sono un pool condiviso di IP riservati agli utenti con bassi volumi, che inviano meno di 75.000 messaggi al mese, e non sono idonei per un IP dedicato. Tali utenti devono inoltre soddisfare i requisiti delle best practice.

* Se invii messaggi tramite Marketo Engage con un pool condiviso di IP, puoi verificare se hai i requisiti necessari per gli IP attendibili [richiedendo il programma di invio di intervalli IP attendibili](https://na-sjg.marketo.com/lp/marketoprivacydemo/Trusted-IP-Sending-Range-Program.html?lang=it){target="_blank"}. Il Return-Path con brand è incluso con l’invio da IP attendibili di Marketo Engage. Se ricevi l’approvazione per questo programma, contatta il supporto Adobe per impostare il Return-Path con brand.

* Se invii più di 100.000 messaggi al mese e desideri inviare e-mail tramite Marketo Engage utilizzando IP condivisi, contatta il team Adobe Account (il tuo account manager) per acquistare un IP dedicato.

I clienti del pool IP condiviso non hanno bisogno di configurazioni aggiuntive. Continui a utilizzare gli stessi pool IP e lo stesso dominio predefinito del percorso restituito di prima.



## Configura i record MX per il dominio

Un record MX ti consente di ricevere e-mail al dominio da cui stai inviando l’e-mail per elaborare le risposte e gli auto-responder. Se per l’invio utilizzi il dominio aziendale, probabilmente è già configurato. In caso contrario, in genere è possibile configurarlo per eseguire la mappatura sul record MX del dominio aziendale.

## Indirizzi IP in uscita

Una connessione in uscita è una connessione effettuata da Marketo Engage per tuo conto verso un server su Internet. L’organizzazione IT e alcuni partner/fornitori possono utilizzare gli elenchi Consentiti per limitare l’accesso ai server. In tal caso, devi fornire loro i blocchi di indirizzi IP in uscita di Marketo Engage da aggiungere ai loro elenchi Consentiti.

<!--
 ### Webhooks

Marketo Engage webhooks are an outbound integration mechanism. When a Smart Campaign executes a _Call Webhook_ flow action, it makes an HTTP request to an external web service. If the web service publisher uses an allowlist on the firewall of the network where the external web service is located, the publisher must add the IP address blocks listed below to their allowlist. For more information, see [Create a webhook](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/additional-integrations/create-a-webhook){target="_blank"} and [Call Webhook](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/core-marketo-concepts/smart-campaigns/flow-actions/call-webhook){target="_blank"} in the Marketo Engage documentation.

### CRM sync

Marketo Engage Salesforce CRM Sync and Microsoft Dynamics Sync are integration mechanisms that make outbound HTTP requests to APIs published by your CRM vendor. Ensure that your IT organization does not block any of the IP address blocks below from accessing your CRM vendor APIs. For more information, see [Add an Existing Salesforce Field to the Marketo Sync](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/crm-sync/salesforce-sync/sfdc-sync-details/add-an-existing-salesforce-field-to-the-marketo-sync){target="_blank"} and [Understanding the Microsoft Dynamics Sync](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/crm-sync/microsoft-dynamics/understanding-the-microsoft-dynamics-sync){target="_blank"} in the Marketo Engage documentation. 
-->

## Blocchi di indirizzi IP in uscita

Gli elenchi seguenti coprono tutti i server Marketo Engage che effettuano chiamate in uscita. Fai riferimento a questi elenchi per la configurazione di elenco IP Consentiti, firewall, elenco di controllo degli accessi, gruppo di sicurezza o servizio di terze parti per la ricezione di connessioni in uscita da Marketo Engage.

| Blocco IP (notazione CIDR) | Indirizzo IP individuale |
| ------------------------ | --------------------- |
| <ul><li>`94.236.119.0/26`</li><li>`103.237.104.0/22`</li><li>`130.248.172.0/24`</li><li>`130.248.173.0/24`</li><li>`130.248.244.88/29`</li><li>`185.28.196.0/22`</li><li>`192.28.144.0/20`</li><li>`192.28.160.0/19`</li><li>`199.15.212.0/22`</li></ul> | <ul><li>`13.237.155.207`</li><li>`13.55.192.247`</li><li>`18.200.201.81`</li><li>`34.247.24.245`</li><li>`35.165.244.220`</li><li>`44.235.171.179`</li><li>`52.20.211.99`</li><li>`52.64.109.86`</li><li>`54.160.246.246`</li><li>`54.212.167.17`</li><li>`54.220.138.65`</li><li>`54.237.141.197`</li><li>`130.248.168.16`</li><li>`130.248.168.17`</li></ul> |
