---
title: Funzionalità per governance e privacy
description: Scopri le funzioni di governance attualmente disponibili in Journey Optimizer B2B edition.
feature: Setup
role: Admin
exl-id: 2845272b-987c-4a37-adf4-6ee5bfd59fc0
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: d6e625c1-468f-4d73-9f32-fd1edb87f96b
  - id: f2da1b69-6919-4386-a5d2-9c7b5c9033db
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
autotag-review: 2026-03-27T23:18:44.352Z
TQID: https://experienceleague.adobe.com/PwH34suDPc84nB9eiAWtrkVzsOw82RRGw4hrRogf9zE
source-git-commit: 6af5c69aac417f557472bdb80df9de7460e65f16
workflow-type: tm+mt
source-wordcount: 692
ht-degree: 0%

---

# Funzioni di governance e privacy

[!DNL Journey Optimizer B2B Edition] è un&#39;app Adobe Experience Platform integrata. Utilizza diversi strumenti e servizi che consentono di controllare i dati raccolti sull’esperienza in conformità con le pratiche aziendali, gli obblighi legali e i processi di sviluppo. Le sezioni seguenti forniscono un riepilogo di ciascuna di queste funzioni di governance.

## Privacy

Varie normative si applicano a [!DNL Journey Optimizer B2B Edition] utenti in possesso di dati per gli interessati in aree quali UE, California, Thailandia, Brasile e Nuova Zelanda. Le informazioni fornite in questa pagina non sono un parere legale e non garantiscono la conformità alle leggi applicabili.

### RGPD

Il Regolamento generale sulla protezione dei dati (RGPD) è la normativa sulla privacy dell&#39;Unione europea che armonizza e modernizza [i requisiti in materia di protezione dei dati](https://commission.europa.eu/law/law-topic/data-protection/data-protection-explained_en){target="_blank"} per i paesi dell&#39;UE.

[!DNL Journey Optimizer B2B Edition] utilizza la funzione esistente di governance RGPD di Experience Platform fornita da Privacy Service. Per informazioni sull&#39;invio e la gestione delle richieste di accesso ed eliminazione, vedere [_Gestione della privacy_](./privacy-management.md).

### CNIL

Il 14 aprile 2026 la Commission nationale de l&#39;informatique et des libertés (CNIL) [ha pubblicato una raccomandazione](https://cnil.fr/sites/default/files/2026-05/recommandation_tracking_pixels_emails.pdf) sull&#39;uso dei pixel di tracciamento nelle e-mail. La guida chiarisce quando è necessario il consenso ed evidenzia l’importanza di pratiche di consenso appropriate per il tracciamento dei pixel dell’e-mail. Questo criterio influisce su qualsiasi entità che invia e-mail agli abbonati con sede in Francia.

CNIL ha previsto un periodo di tre mesi dalla data della raccomandazione alle aziende di informare i propri destinatari e-mail della presenza dei pixel di tracciamento, del loro scopo e del diritto dei destinatari di rinunciare. Durante questo periodo di transizione, gli utenti di Marketo Engage devono informare i destinatari in merito al tracciamento dei pixel e, se necessario, fornire una rinuncia. CNIL dovrebbe iniziare le attività di applicazione dopo il 14 luglio 2026.

Mentre il CNIL e altre autorità di regolamentazione chiariscono le linee guida sui pixel di tracciamento e sui problemi correlati, Adobe monitora gli aggiornamenti e ti informa in merito alle modifiche alle funzionalità tecniche.

[!DNL Journey Optimizer B2B Edition] offre controlli che consentono di gestire il tracciamento delle aperture a livello di e-mail. Gli utenti sono responsabili della determinazione dei propri obblighi di conformità ai sensi degli orientamenti CNIL applicabili e di altre leggi. Per informazioni sull&#39;utilizzo di queste funzionalità per la gestione del tracciamento dell&#39;apertura delle e-mail, vedere [_Gestione del tracciamento delle e-mail_](../content/email-tracking-manage.md).

## Controllo degli accessi basato sul ruolo (RBAC)

Con Journey Optimizer B2B edition e l’accesso a Adobe Admin Console, gli amministratori possono concedere a un utente le autorizzazioni per un tipo di entità (view-segments, manage-segments, manage-percorsi e così via). Questa funzionalità fa parte del framework di autorizzazioni unificate (UPF, Unified Permissions Framework) che consente a tutti i clienti di Adobe Experience Platform di definire e gestire ruoli e autorizzazioni per la propria organizzazione.

## Crittografia dei dati

**_Crittografia per i dati inattivi_**: tutti i dati del profilo utente e dell&#39;account trasferiti da Adobe Experience Platform a Journey Optimizer B2B edition vengono crittografati per mantenere la conformità esistente da Experience Platform. Vengono crittografate anche tutte le entità originarie di Journey Optimizer B2B edition, ad esempio i percorsi e i gruppi di acquisto.

**_Crittografia per i dati in transito_** (su una rete pubblica): tutte le API e le entità di Journey Optimizer B2B edition sono crittografate in transito utilizzando TLS 1.2.

## Consenso/rinuncia

Journey Optimizer B2B edition legge le preferenze di consenso per persona memorizzate nei profili XDM di Adobe Experience Platform e le applica al momento della consegna dei messaggi per i canali e-mail, SMS e WhatsApp. Una persona che ha rinunciato a un canale è esclusa dalla consegna prima che il contenuto venga inviato dal canale o dal provider di messaggistica a valle.

Il consenso viene valutato al momento della consegna utilizzando i campi XDM del gruppo di campi Consenso profilo. Il comportamento predefinito del consenso varia a seconda del canale: per impostazione predefinita, l’e-mail ha acconsentito quando non è impostata alcuna preferenza, mentre per impostazione predefinita SMS e WhatsApp ha acconsentito.

Per informazioni dettagliate sugli attributi XDM valutati per ciascun canale e sui relativi comportamenti predefiniti, consulta [Preferenze di consenso](../content/channels-consent-preferences.md).

## Ripristino del sandbox

Il ripristino della sandbox è **non attualmente supportato** per Adobe Journey Optimizer B2B edition. Il ripristino o l&#39;eliminazione di una sandbox mappata a [!DNL Journey Optimizer B2B Edition] potrebbe causare una perdita permanente di dati e richiedere il provisioning di una nuova istanza.

## Non ancora disponibile

Le seguenti funzioni di governance non sono ancora disponibili:

* Applicazione etichetta di utilizzo dati (DULE) / criteri di utilizzo
* Igiene dei dati
* Criteri di consenso
* Controllo degli accessi a livello di campo (Field-Level Access Control, FLAC)
* Controllo dell&#39;accesso a livello di oggetto (OLAC)
* Crittografia CMK per i dati inattivi
* Servizio di audit della piattaforma
