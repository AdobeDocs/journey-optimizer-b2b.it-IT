---
title: Recapito messaggi e-mail e configurazione del canale
description: Configura la delega dei sottodomini, DMARC, SPF, DKIM, i pool IP e le configurazioni dei canali e-mail per Journey Optimizer B2B Prime.
autotag-review: '2026-06-12T22:43:42.799Z'
TQID: 'https://experienceleague.adobe.com/RKZSQkjSRvHixOm2faRT5D-yB00IykXfPO06vvIUQ6k'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: d6e625c1-468f-4d73-9f32-fd1edb87f96bid: f01b5556-e951-40ba-8625-2e3001864f2bid: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2: id: d270a788-eb1d-40ed-b74e-9158ed975b1fid: ff0c35fa-aa7e-4050-a37c-198fcacd09e6
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: 0a877cc1fc0dfd9c3d8271c8f7be6a5e34a69a9a
workflow-type: tm+mt
source-wordcount: 3095
ht-degree: 1%

---

# Recapito messaggi e-mail e configurazione dei canali

Le seguenti informazioni sono destinate agli amministratori che configurano l’infrastruttura di invio per supportare gli esperti di marketing e gli autori di e-mail. Descrive le funzioni di recapito messaggi, i ruoli e le autorizzazioni e come configurare sottodomini, autenticazione, pool IP e configurazioni dei canali.

Per informazioni dettagliate sulla creazione di e-mail e sull&#39;authoring del contenuto delle e-mail nello spazio di progettazione delle e-mail, consulta [Authoring e-mail](../content/email-authoring.md).

## Concetti chiave {#key-concepts}

Prima di configurare l’e-mail, esamina i concetti seguenti che si applicano alle funzioni di consegna del canale e-mail:

| Concetto | Che cosa significa in [!DNL Journey Optimizer B2B Edition] Prime |
| ------- | ---------------------- |
| **_Configurazione canale_** | Un set riutilizzabile di impostazioni di invio e-mail, tra cui identità del mittente, indirizzo di risposta, sottodominio, pool IP, tipo di e-mail (marketing o transazionale) e tracciamento, da allegare alle azioni e-mail nei percorsi. Puoi avere più configurazioni di canale denominate per diversi marchi, business unit o tipi di invio. |
| **_Sottodominio_** | Parte delegata del dominio di invio (ad esempio, `mail.contoso.com`) utilizzata per inviare messaggi di posta elettronica tramite Prime. I sottodomini isolano la reputazione di marketing B2B dalla posta aziendale o transazionale. |
| **_Pool IP_** | Un gruppo di indirizzi IP associati a uno o più sottodomini. In questa versione, Prime supporta un pool IP condiviso gestito da Adobe; i pool IP dedicati sono inclusi nella roadmap di GA. |

## Ruoli e autorizzazioni {#roles-permissions}

[!DNL Journey Optimizer B2B Edition] Prime utilizza il controllo degli accessi basato sul ruolo (RBAC) per le funzionalità di posta elettronica. Le autorizzazioni vengono gestite in Adobe Admin Console (IMS) e sincronizzate all’accesso. Gli amministratori di prodotto assegnano autorizzazioni granulari ai profili di prodotto, quindi associano tali profili di prodotto agli utenti.

L&#39;accesso alla funzionalità e-mail in [!DNL Journey Optimizer B2B Edition] Prime è gestito da due livelli:

1. **Flag di funzionalità (LD).** Un flag LaunchDarkly controlla se l’intera funzione è attivata per la tua organizzazione. L&#39;authoring e il recapito dei messaggi di posta elettronica sono gestiti da `dx_ajo_btob_channel_foundation`. Senza questo flag, la funzione è nascosta indipendentemente dalle autorizzazioni.
2. **Autorizzazione funzionale.** Autorizzazione a livello utente che controlla se un utente specifico può leggere o scrivere all’interno di una funzione.

La maggior parte delle funzionalità di posta elettronica seguono un pattern `view-*` (lettura) e `manage-*` (scrittura). Per visualizzare una funzionalità nella struttura di navigazione, l’utente deve disporre dell’autorizzazione di lettura e dell’autorizzazione di scrittura per crearla, modificarla o eliminarla.

### Autorizzazioni di authoring delle e-mail {#email-authoring-permissions}

| Funzionalità | Autorizzazione | Cosa consente |
| ---------- | ---------- | -------------- |
| **Visualizza e-mail** | `view-b2b-emails` | Visualizza l’elenco e-mail, apri le e-mail, visualizza il contenuto (sola lettura). |
| **Creare, modificare o eliminare le e-mail** | `manage-b2b-emails` | Accesso in lettura e creazione, modifica, duplicazione ed eliminazione di e-mail. Obbligatorio per creare contenuti e-mail all’interno di un percorso. |
| **Visualizza modelli** | `view-b2b-templates` | Sfoglia e visualizza in anteprima i modelli nella raccolta Modelli (sola lettura). |
| **Creare, modificare o eliminare modelli** | `manage-b2b-templates` | Accesso in lettura e creazione, modifica ed eliminazione di modelli salvati. |
| **Visualizza frammenti** | `view-b2b-fragments` | Sfoglia e visualizza in anteprima i frammenti visivi (sola lettura). |
| **Crea/modifica frammenti** | `manage-b2b-fragments` | Accesso in lettura e creazione e modifica di frammenti visivi. |
| **Pubblica frammenti** | `publish-b2b-fragments` | Pubblica un frammento in modo che diventi disponibile per gli autori e-mail in tutta l’organizzazione. |
| **Gestione di risorse condivise ed elementi della libreria** | `manage-b2b-library-items` | Gestisci la libreria condivisa sottostante utilizzata da modelli, frammenti ed e-mail. Spesso vengono concesse insieme alle autorizzazioni di gestione del modello/frammento. |
| **Gestione etichette di utilizzo** | `manage-b2b-delete-usage-labels` | Gestisci le etichette di utilizzo dati (DULE) allegate agli elementi della libreria per la governance. |
| **Gestisci pacchetti** | `manage-b2b-packages` | Crea bundle e sposta modelli, frammenti ed e-mail tra sandbox. |
| **Visualizzare le risorse (risorse di Marketo Design Studio in Prime)** | `view-b2b-assets` | Sfoglia il selettore delle risorse e visualizza le immagini in anteprima. Sola lettura. |
| **Gestire le risorse** | `manage-b2b-assets` | Accesso in lettura e future azioni di gestione delle risorse (ambito Beta). |
| **Esporta dati messaggio** | `manage-b2b-message-export` | Esporta dati e rapporti dei messaggi a livello di e-mail. |

All&#39;interno di un percorso di persone, l&#39;azione **Invia e-mail** richiede `manage-b2b-person-journeys` (per aggiungere l&#39;azione e attivare il percorso). Un utente con solo autorizzazioni e-mail può creare contenuti ma non può aggiungere un’e-mail a un percorso.

### Autorizzazioni di recapito messaggi e-mail {#email-deliverability-permissions}

Le funzioni di recapito messaggi (sottodomini, DMARC, pool IP, elenchi di soppressione, elenchi Consentiti, piani di riscaldamento IP ed elenchi di seed) sono configurazioni a livello di amministratore. Sono governati da due autorizzazioni che coprono l&#39;intera area **[!UICONTROL Canali]** > **[!UICONTROL Impostazioni e-mail]**:

| Funzionalità | Autorizzazione | Cosa consente |
| ---------- | ---------- | -------------- |
| **Visualizza impostazioni e-mail** | `view-b2b-email-settings` | Visualizzare sottodomini, record PTR, pool IP, elenco di soppressione, elenco Consentiti, piani di riscaldamento IP ed elenchi di seed (sola lettura). |
| **Gestione impostazioni e-mail** | `manage-b2b-email-settings` | Tutti gli accessi in lettura e i sottodomini delegati, configurano DMARC, gestiscono soppressione ed elenchi Consentiti, gestiscono i piani di riscaldamento IP e gli elenchi di seed. |

Alcune funzionalità secondarie nelle impostazioni e-mail sono gestite da flag LaunchDarkly aggiuntivi: elenco di soppressione (`enable-suppression`), Elenco Consentiti (`enable-allow-list`), elenchi seed (`enable-seedlist-ui`). Se una sottofunzione non è visibile nell’organizzazione, contatta il rappresentante Adobe per l’abilitazione del flag.

### Autorizzazioni di configurazione del canale {#channel-configuration-permissions}

Le configurazioni dei canali si trovano in **[!UICONTROL Canali]** → **[!UICONTROL Impostazioni generali]**. Legano le primitive di recapito dei messaggi (sottodominio, pool IP, identità del mittente) a un oggetto riutilizzabile a cui fanno riferimento gli autori del percorso. Sono disciplinati da un’unica autorizzazione:

| Funzionalità | Autorizzazione | Cosa consente |
| ---------- | ---------- | -------------- |
| **Gestione configurazioni canale** | `manage-b2b-channels-configurations` | Visualizza, crea, modifica ed elimina configurazioni del canale e-mail. |

## Panoramica sul recapito messaggi e-mail {#deliverability-overview}

Il recapito messaggi e-mail in [!DNL Journey Optimizer B2B Edition] Prime è il set di configurazioni di infrastruttura e autenticazione che consentono ai messaggi e-mail di raggiungere la casella in entrata del destinatario, non la cartella di posta indesiderata e non bloccati dagli ISP (provider di servizi Internet).

Utilizza i seguenti blocchi predefiniti, configurati da un amministratore, in genere nell’ordine seguente:

1. Delega uno o più sottodomini ad Adobe.
1. Configura i record DMARC, SPF e DKIM in ciascun sottodominio.
1. Conferma il pool IP che invierà l’e-mail per il tuo sottodominio.
1. Crea una o più configurazioni del canale e-mail che associano un sottodominio, un pool IP e un’identità del mittente.
1. Utilizza queste configurazioni di canale nelle azioni e-mail del percorso.

>[!TIP]
>
>Considera la configurazione del recapito messaggi come un’attività di amministratore una tantum per unità aziendale o marchio. Una volta configurata, gli addetti al marketing e gli autori di e-mail non dovranno più visitarla.

## Delega dei sottodomini {#subdomain-delegation}

La delega dei sottodomini comunica a Internet che Adobe è autorizzato a inviare e-mail per conto di un sottodominio specifico (ad esempio, `mail.contoso.com`) del tuo dominio. La delega di un sottodominio dedicato, anziché del dominio principale, protegge la posta aziendale e produce un

* **Isolamento reputazione.** Gli invii di marketing sono tenuti separati dalla posta aziendale. Se la reputazione di marketing diminuisce, i messaggi aziendali e transazionali non subiranno modifiche.
* **Riscaldamento IP più veloce.** I sottodomini dedicati aiutano a stabilire più rapidamente una reputazione positiva del mittente con gli ISP.
* **Autenticazione moderna.** SPF, DKIM e DMARC possono essere configurati in modo pulito per sottodominio senza influire sugli altri flussi di posta.
* **Conformità.** Consente di soddisfare i requisiti di invio in blocco da Gmail, Yahoo e altri importanti ISP.

>[!NOTE]
>
>Ogni sottodominio in Prime può essere utilizzato solo da un prodotto Adobe. Non è possibile condividere lo stesso sottodominio di invio tra Prime e un altro prodotto, ad esempio Adobe Marketo Engage o Adobe Campaign, ma è necessario utilizzare sottodomini distinti.

### Metodi supportati

Prime supporta due dei tre metodi di delega dei sottodomini in Alpha. Il terzo metodo (Delega personalizzata) si trova nella roadmap.

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

1. [!DNL Adobe Journey Optimizer B2B Edition] Prime, passa a **[!UICONTROL Amministrazione]** → **[!UICONTROL Canali]** → **[!UICONTROL Impostazioni e-mail]** → **[!UICONTROL Sottodomini]**.
1. Fare clic su **[!UICONTROL Configura sottodominio]**.
1. Immettere il nome completo del sottodominio, ad esempio `mail.contoso.com`.
1. Scegliere **[!UICONTROL Delega completa]** come metodo di delega.
1. Configurare DMARC per il sottodominio (vedere [DMARC, SPF e DKIM](#dmarc-spf-dkim)).

   Imposta almeno un record DMARC con un criterio di avvio di `none` per monitorare i report senza influire sulla consegna.

1. Esamina l’elenco dei record DNS da gestire in Adobe.

   In genere includono i record MX, SPF, DKIM, DMARC, A e CNAME (per il tracciamento e gli URL delle pagine mirror).

1. Scarica i record DNS come file CSV utilizzando il pulsante **[!UICONTROL Scarica record]**. Condividi questo file con il tuo team DNS.

1. Il team DNS aggiunge i record NS nella soluzione di hosting del dominio che delegano il sottodominio ad Adobe.

1. Dopo che il team DNS ha confermato la disponibilità dei record, tornare a [!DNL Journey Optimizer B2B Edition] Prime e selezionare la casella per confermare la creazione dei record richiesti nel sito di hosting.

1. Fai clic su **[!UICONTROL Invia]** per avviare una serie di controlli di convalida (pre-convalida, MX, SPF, DKIM, DMARC, registrazione FBL).

1. Attendere che lo stato del sottodominio passi a **[!UICONTROL Operazione completata]**.

   Questa operazione richiede in genere alcuni minuti dopo il completamento della propagazione DNS.

>[!NOTE]
>
>Se la convalida non riesce, lo stato cambia in **[!UICONTROL Non riuscito]** e [!DNL Journey Optimizer B2B Edition] Prime visualizza il motivo (ad esempio, record NS non trovato, record MX mancante o DMARC non configurato correttamente). Correggi il problema DNS sottostante, quindi riprova l’invio.

### Delega un sottodominio (metodo CNAME) {#delegate-cname}

Utilizzare questo metodo solo se i criteri DNS dell&#39;organizzazione non consentono la delega completa. Con CNAME puoi mantenere i record DNS al tuo fianco.

1. In [!DNL Adobe Journey Optimizer B2B Edition] Prime passare a **[!UICONTROL Amministrazione]** → **[!UICONTROL Canali]** → **[!UICONTROL Impostazioni e-mail]** → **[!UICONTROL Sottodomini]**.
1. Fare clic su **[!UICONTROL Configura sottodominio]**.
1. Immetti il nome completo del sottodominio.
1. Scegliere **[!UICONTROL CNAME]** come metodo di delega.
1. Configurare DMARC per il sottodominio ([DMARC, SPF e DKIM](#dmarc-spf-dkim)).
1. Esamina l’elenco dei record CNAME generati da Prime, che puntano i componenti del sottodominio ai record gestiti da Adobe.
1. Scarica i record come CSV e condividili con il tuo team DNS.
1. Il team DNS aggiunge ogni record CNAME alla soluzione di hosting DNS.
1. Una volta che i record sono presenti e propagati, torna a Prime e conferma. Fai clic su **[!UICONTROL Invia]**.
1. Attendere che lo stato raggiunga il **[!UICONTROL successo]**.

>[!IMPORTANT]
>
>Con CNAME, Adobe non può aiutarti a modificare, gestire o risolvere i problemi DNS per il sottodominio. Eventuali modifiche future, ad esempio l’aggiunta di un nuovo CNAME per un aggiornamento della funzione, devono essere effettuate dal team DNS.

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

### Modalità criteri di DMARC

| Policy | Azione | Quando utilizzare |
| ------ | ------ | ----------- |
| `none` | Monitoraggio | Il server ricevente non esegue alcuna operazione in caso di errore di DMARC, ma invia comunque un report. Utilizza questa opzione quando deleghi un sottodominio per la prima volta a confermare il funzionamento dell’autenticazione senza rischiare la perdita dei messaggi. |
| `quarantine` | Quarantena | Il server ricevente inserisce i messaggi di errore nella cartella di posta indesiderata. |
| `reject` | Rifiuta | Il server ricevente rifiuta i messaggi (non recapitati) che non superano l’autenticazione. Modalità più rigida. Consigliato quando si è sicuri della configurazione dell’autenticazione. |

### Configurare DMARC {#configure-dmarc}

DMARC è configurato al momento della delega del sottodominio, ma puoi anche aggiungere o aggiornare DMARC per un sottodominio già delegato.

1. Passa a **[!UICONTROL Amministrazione]** → **[!UICONTROL Canali]** → **[!UICONTROL Impostazioni e-mail]** → **[!UICONTROL Sottodomini]**.

1. Nell’elenco Sottodomini, individua il sottodominio e controlla la colonna Record di DMARC.

   Se manca un record, viene visualizzato un avviso.

1. Apri il sottodominio e scorri fino alla sezione del record DMARC.

   * Se nel dominio padre esiste già un record DMARC, [!DNL Journey Optimizer B2B Edition] Prime recupera i valori automaticamente. Puoi tenerli o ignorarli.
   * Se non esiste alcun record, scegli **[!UICONTROL Gestisci con Adobe]** e Adobe crea e ospita il record DMARC.

1. Impostare i criteri: `none`, `quarantine` o `reject`. Iniziare con `none` a meno che non si disponga già di una postura DMARC matura nel dominio padre.

1. (Facoltativo) Configurare altri tag di DMARC (`sp` per il criterio del sottodominio, `pct` per la percentuale, `rua` e `ruf` per gli indirizzi di report).

1. Se si utilizza Completamente delegato, fare clic su **[!UICONTROL Salva]**.

   Adobe applica il record automaticamente. Se utilizzi CNAME, copia il record DNS e chiedi al tuo team DNS di aggiungerlo, quindi confermarlo in [!DNL Journey Optimizer B2B Edition] Prime.

1. Consenti fino a 48 ore per la propagazione DNS, quindi verifica che l’indicatore di stato DMARC nella pagina del sottodominio sia verde/integro.

>[!TIP]
>
>Inizia con `policy=none` per monitorare i rapporti di autenticazione, quindi passa a `quarantine` e infine a `reject` quando i rapporti mostrano un allineamento corretto di SPF e DKIM. Se si passa direttamente a `reject` senza monitoraggio, i messaggi legittimi potrebbero essere rifiutati.

## Pool IP {#ip-pools}

Un pool IP è un gruppo denominato di indirizzi IP utilizzati per inviare l’e-mail. I pool IP sono fondamentali per la reputazione del mittente: ogni pool ha la propria reputazione rispetto agli ISP, pertanto un problema relativo a un pool (ad esempio, un burst di marketing che attiva reclami di spam) non ne infligge un altro (ad esempio, conferme transazionali).

### Tipi di pool

| Tipo di pool | Disponibilità | Descrizione |
| --------- | ------------ | ----------- |
| **Pool IP condiviso** | Disponibile in Alpha | Un pool di indirizzi IP gestiti da Adobe e condivisi tra molti clienti. La reputazione viene mantenuta da Adobe in tutto il pool. Consigliato per volumi di e-mail da basso a medio e clienti che non desiderano gestire il riscaldamento dell’IP. |
| **Pool IP dedicato** | Roadmap (GA) | Uno o più indirizzi IP allocati esclusivamente alla tua organizzazione. Tu possiedi la reputazione. Consigliato per mittenti con volumi elevati. Include la pianificazione del riscaldamento IP e la gestione dei record PTR. |

### Revisione e assegnazione di un pool IP {#review-ip-pool}

In questa versione, viene eseguito il preprovisioning dei pool IP per la tua organizzazione. Assegna un pool IP durante la creazione di una configurazione del canale e-mail.

1. Passare a **[!UICONTROL Amministrazione]** → **[!UICONTROL Canali]** → **[!UICONTROL Impostazioni e-mail]** → **[!UICONTROL Pool IP]**.
1. Verificare che un pool IP con stato **[!UICONTROL Attivo]** sia disponibile per l&#39;organizzazione.
1. Passa il puntatore del mouse sul pool per visualizzare gli indirizzi IP e i relativi record PTR (DNS inverso).
1. Se la tua organizzazione dispone di più business unit o marchi, pianifica come utilizzare i pool IP (ad esempio, pool di marketing rispetto a pool di webinar) prima di creare configurazioni di canale.

>[!IMPORTANT]
>
>Non combinare il traffico di marketing e quello transazionale sullo stesso pool IP, anche quando il pool condiviso è disponibile. L’impostazione del tipo di e-mail nella configurazione del canale (Marketing vs. Transazionale) governa il comportamento di soppressione, ma le configurazioni del canale devono comunque utilizzare pool distinti, ove possibile.

## Configurazioni del canale e-mail {#email-channel-configurations}

Una configurazione del canale è l’oggetto centrale che unisce l’identità del mittente, il sottodominio, il pool IP e le impostazioni di tracciamento. Le azioni e-mail nei percorsi fanno riferimento a una configurazione di canale per sapere come inviare il messaggio:

* **Canale:** E-mail.
* **Tipo di e-mail:** di marketing o transazionale. Questa impostazione determina se le regole di soppressione sono applicabili (Marketing le applica; Transazionale ignora la soppressione dei reclami spam per impostazione predefinita per i messaggi transazionali legittimi).
* **Parametri intestazione:** Da nome, Da e-mail, Nome risposta, E-mail risposta, E-mail errore.
* **Sottodominio:** Il sottodominio delegato utilizzato per l&#39;invio. Il Da e-mail deve utilizzare questo sottodominio.
* **Pool IP:** Pool IP utilizzato per recapitare il messaggio.
* **Tracciamento URL:** Attiva o disattiva il tracciamento dei clic e dei messaggi aperti; configura il dominio di tracciamento.
* **Tag:** Tag per organizzazione e ricerca.

### Creare una configurazione del canale e-mail {#create-email-channel-configuration}

>[!PREREQUISITES]
>
>* Almeno un sottodominio deve essere delegato e attivo.
>* È necessario assegnare almeno un pool IP all’organizzazione.
>* È necessario il ruolo di amministratore.

1. Passa a **[!UICONTROL Canali]** → **[!UICONTROL Impostazioni generali]** → **[!UICONTROL Configurazioni canale]**.
1. Fai clic su **[!UICONTROL Crea configurazione canale]**.
1. Immetti un Nome (ad esempio, &quot;Contoso B2B Marketing — North America&quot;) e una Descrizione facoltativa.
1. Seleziona il canale **[!UICONTROL E-mail]**.
1. Facoltativamente, seleziona i tag per categorizzare la configurazione.
1. Nella sezione **[!UICONTROL Tipo di e-mail]**, scegli Marketing o Transazionale.
1. Nella sezione **[!UICONTROL Sottodominio]**, seleziona un sottodominio delegato in precedenza.
1. Nella sezione **[!UICONTROL Pool IP]** selezionare un pool IP attivo. Puoi passare il cursore sugli IP per visualizzare i record PTR.
1. Configura i **[!UICONTROL parametri intestazione]**:
   * Dal nome (ad esempio, &quot;Contoso Marketing&quot;).
   * Da e-mail: deve utilizzare il sottodominio selezionato (ad esempio, `marketing@mail.contoso.com`).
   * Nome risposta e indirizzo e-mail di risposta: se questo campo viene lasciato vuoto, per impostazione predefinita viene utilizzato il campo Da.
   * E-mail di errore: indirizzo che riceve le notifiche di mancato recapito.
1. Abilita **[!UICONTROL Tracciamento URL]** e seleziona il dominio di tracciamento.
1. Fai clic su **[!UICONTROL Invia]**.
1. Prime esegue la convalida: stato del sottodominio, record MX, allineamento SPF/DKIM/DMARC, preparazione del pool IP, registrazione FBL. La configurazione si sposta attraverso l&#39;Elaborazione di bozze → → attiva.

>[!NOTE]
>
>Se la convalida non riesce, la configurazione passa allo stato **[!UICONTROL Non riuscito]**. Apri la configurazione per visualizzare il motivo dell’errore. Cause comuni sono errori di convalida dei record MX, IP nel pool che non corrispondono alla configurazione o disallineamento di DMARC. Risolvi e invia di nuovo.

### Modificare o eliminare una configurazione di canale {#edit-channel-configuration}

Puoi modificare le configurazioni di canale dopo la creazione, ma con un vincolo importante:

* **Impossibile modificare il canale.** Una configurazione è associata al relativo canale.

Quando modifichi una configurazione in uso:

* **Per i percorsi pubblicati:** la modifica viene applicata alla ricorrenza successiva o all&#39;esecuzione successiva. Le esecuzioni in volo continuano con le impostazioni precedenti.
* **Per i messaggi transazionali o in tempo reale:** le modifiche si propagano in circa cinque minuti.

Per eliminare una configurazione, rimuovi o aggiorna innanzitutto ogni azione e-mail che vi fa riferimento. [!DNL Journey Optimizer B2B Edition] Prime non elimina una configurazione attualmente utilizzata da un percorso attivo.

### Configurazioni multicanale {#multiple-channel-configurations}

La maggior parte delle organizzazioni B2B utilizza più configurazioni di canale per separare i marchi, le aree geografiche o i tipi di invio. Pattern comuni:

* Una configurazione marketing separata per unità aziendale (ad esempio, *BU-A Marketing*, *BU-B Marketing*).
* Una configurazione transazionale dedicata con Tipo e-mail = Transazionale per le notifiche di prodotti o contratti.
* Configurazioni specifiche per l&#39;area geografica che utilizzano sottodomini specifici dell&#39;area (ad esempio, `mail.eu.contoso.com`, `mail.us.contoso.com`) per l&#39;allineamento con gli ISP regionali e la conformità.

>[!TIP]
>
>Assegna alle configurazioni un nome chiaro e strutturato, ad esempio: *[Marchio] - [Regione] - [Tipo]*. Questo diventa critico una volta che hai una dozzina o più configurazioni.

### Limitazioni note {#known-limitations}

* **Il metodo di delega personalizzato** per la delega del sottodominio non è ancora disponibile. Utilizzare Fully Delegated o CNAME. La delega personalizzata è impostata per GA.
* **Pool IP dedicati** non disponibili in Alpha. L&#39;unica opzione è il pool IP condiviso. Gli IP dedicati vengono forniti in GA, inclusa la pianificazione del riscaldamento IP e la gestione dei record PTR.
* **L&#39;importazione di HTML tramite caricamento .html o .zip** è limitata in Alpha. L’importazione completa di HTML, che include l’editor di codice e l’area di lavoro visiva con visualizzazione doppia, la convalida e la conversione automatica in linea degli stili CSS, viene inviata in Beta.
* **Il caricamento di immagini native e DAM in Prime** (caricamento, organizzazione, modifica) si trovano nella roadmap di Beta. Utilizzare le risorse di Marketo Design Studio in questa versione. I ricaricamenti in Marketo non si riflettono in Prime.
* **I profili di test, Simula contenuto e Invia bozza** non sono disponibili in questa versione. Il rendering Litmus e i rapporti spam basati su SpamAssassin sono nella roadmap di Beta.
* **La personalizzazione a livello di account e i dati oggetto personalizzato** non sono disponibili in questa versione. Utilizza gli attributi del profilo.
* **Migrazione automatizzata Velocity-to-Handlebars** dei modelli Marketo esistenti viene spedito in GA.
* **Commenti e collaborazione alle e-mail** (commenti in linea, @mentions, flusso di lavoro di richiesta-revisione) vengono spediti nella versione Fast Follow-up.
* Le integrazioni **AEM Assets, Frammenti di contenuto AEM e Adobe Express** sono incluse nella roadmap di Fast Follow-up.

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
