---
title: Consenso alla messaggistica canale
description: Scopri come Journey Optimizer B2B edition legge le preferenze di consenso del profilo XDM di AEP e applica il consenso e la rinuncia al momento della consegna dei messaggi per i canali e-mail, SMS e WhatsApp.
feature: Setup, Channels
role: Admin, User
autotag-review: '2026-05-19T16:18:37.228Z'
TQID: 'https://experienceleague.adobe.com/-c0dJnpfiIcj0B5gViyEQ7E1Ws0BwP864OLF003rOjw'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: a4b836d9-ffdd-4df3-a62a-f78b830cf059id: f01b5556-e951-40ba-8625-2e3001864f2b
subfeature_v2: id: ff0c35fa-aa7e-4050-a37c-198fcacd09e6id: a22f05f6-0fcf-40c0-a70e-e13a3db185f7
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 8226114f1a34adf85437579ef17a50b80ccfa596
workflow-type: tm+mt
source-wordcount: 424
ht-degree: 1%

---

# Consenso alla messaggistica canale

Adobe Journey Optimizer B2B edition legge le preferenze di consenso per persona memorizzate nei profili XDM di Adobe Experience Platform e le applica al momento della consegna dei messaggi, come parte dei [controlli di governance](../admin/governance.md) dell&#39;app. Le persone che hanno rinunciato a un canale sono escluse dalla consegna prima che il contenuto venga inviato dal canale o dal provider di messaggistica a valle.

Le sezioni seguenti descrivono come Journey Optimizer B2B edition valuta il consenso al momento dell’invio dei messaggi per ogni canale supportato.

## E-mail {#email}

Journey Optimizer B2B edition valuta il seguente attributo XDM per il consenso e-mail durante l&#39;invio di messaggi sul [canale e-mail](../admin/configure-channels-emails.md):

| attributo XDM | `y` | `n` | Nessun valore |
| --- | --- | --- | --- |
| `consents.marketing.email.val` | Consenso accordato | Rinuncia | Consenso accordato |

Per il consenso e-mail, tieni presenti le seguenti considerazioni:

* Le persone che hanno rinunciato a livello globale all’e-mail possono ricevere e-mail contrassegnate come operative.
* Preferenze a livello di abbonamento non supportate.

Per esaminare l&#39;attività di annullamento dell&#39;iscrizione per le e-mail inviate, vedere il [Rapporto sulle prestazioni delle e-mail](../dashboards/email-performance-dashboard.md).

## SMS {#sms}

Journey Optimizer B2B edition valuta i seguenti attributi XDM per il consenso SMS durante l&#39;invio di messaggi tramite il [canale SMS](../admin/configure-channels-sms.md):

| attributo XDM | `y` | `n` | Nessun valore |
| --- | --- | --- | --- |
| `consents.marketing.sms.val` | Consenso accordato | Rinuncia | Rinuncia |
| `consents.marketing.subscriptions.<senderID>` | Consenso accordato | Rinuncia | Rinuncia |
| `consents.marketing.sms.subscriptions.<senderId>.subscribers.<phoneNumber>` | Consenso accordato | Rinuncia | Rinuncia |

Per il consenso SMS, tieni presenti le seguenti considerazioni:

* Quando un record principale (persona) viene escluso dagli SMS, viene escluso completamente e non viene passato ai provider SMS a valle.
* Quando disponibile, viene valutato il consenso a livello di abbonamento. La rinuncia globale viene utilizzata come fallback quando il consenso a livello di abbonamento non è disponibile.
* Le persone che hanno rinunciato agli SMS possono ancora ricevere messaggi contrassegnati come operativi.
* Se più record di lead condividono lo stesso numero di telefono, condividono lo stesso stato di consenso o rinuncia.

## WhatsApp {#whatsapp}

Journey Optimizer B2B edition valuta i seguenti attributi XDM per il consenso WhatsApp quando si inviano messaggi tramite un [canale WhatsApp](../admin/configure-channels-whatsapp.md) configurato:

| attributo XDM | `y` | `n` | Nessun valore |
| --- | --- | --- | --- |
| `consents.marketing.whatsApp.val` | Consenso accordato | Rinuncia | Rinuncia |
| `consents.idSpecific.Phone.<number>.marketing.whatsApp.val` | Consenso accordato | Rinuncia | Rinuncia |

Per il consenso WhatsApp, tieni presenti le seguenti considerazioni:

* Se il valore dell&#39;attributo WhatsApp globale (`consents.marketing.whatsApp.val`) è presente, viene utilizzato per la valutazione del consenso.
* Se il valore dell’attributo globale non è presente ma è presente una voce specifica del mittente, per la valutazione del consenso viene utilizzata la voce specifica del mittente.
* Se non è presente alcun valore per nessuno degli attributi, la persona viene considerata esclusa.

## Non supportato {#not-supported}

Le seguenti funzioni relative al consenso non sono attualmente supportate in Journey Optimizer B2B edition:

* Criteri di consenso di AEP
* Attributi di marketing preferiti (`consents.marketing.preferred`)
