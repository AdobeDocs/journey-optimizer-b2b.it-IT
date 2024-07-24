---
title: Mappatura campo XDM
description: Esamina la mappatura dei campi tra lo schema XDM di AEP, il Marketo Engage e la Journey Optimizer B2B Edition.
source-git-commit: af287825508b2372f51aa8ea629cc6eda0a50b35
workflow-type: tm+mt
source-wordcount: '559'
ht-degree: 17%

---

# Mappatura campo XDM

Il servizio di trasferimento dati (DTS) in è responsabile della sincronizzazione dei dati da Adobe Experience Platform a Journey Optimizer B2B Edition. DTS si basa sulle mappature tra i campi dello schema XDM Experience Platform e i relativi equivalenti nel Marketo Engage.

## Mappature campi predefiniti persona aziendale XDM

| Persona aziendale XDM | Nome visualizzato persona Marketo Engage | Nome visualizzato della persona B2B di AJO | Tipo XDM | Tipo Marketo | Descrizione XDM |
|------------------- |---------------------------------- |--------------------------- |-------- |------------ |--------------- |
| `workAddress.street1` | Indirizzo | ? | stringa | text | Informazioni stradali primarie, numero di appartamento, numero civico e nome della strada. |
| `workAddress.city ` | Città | Città | stringa | stringa | Il nome della città. |
| `b2b.companyName` | Nome della società | ? | stringa | stringa | Nome della società a cui è associata una persona aziendale. |
| `workAddress.country` | Paese | Paese | stringa | stringa | Il nome del territorio amministrato dal governo. A parte `xdm:countryCode`, questo è un campo in formato libero che può avere il nome del paese in qualsiasi lingua. |
| `person.birthDate` | Data di nascita | Data di nascita | stringa | data | La data completa di nascita di una persona.  DD/MM/YYYY |
| `workEmail.address` | Indirizzo e-mail | Indirizzo e-mail | stringa | e-mail | L&#39;indirizzo tecnico, ad esempio &#39;<name@domain.com>&#39;, come comunemente definito in RFC2822 e standard successivi. |
| `workEmail.status` | E-mail sospesa | E-mail sospesa | stringa | booleano | Un’indicazione relativa alla possibilità di utilizzare l’indirizzo e-mail. |
| `faxPhone.number` | Numero di fax | ? | stringa | telefono | Numero di fax. |
| `person.name.firstName` | Nome | Nome | stringa | stringa | Il primo segmento del nome nell’ordine di scrittura più comunemente accettato nella lingua del nome. In molte culture questo è il nome personale o di battesimo preferito. Le proprietà firstName e lastName sono state introdotte per mantenere la compatibilità con i sistemi esistenti che modellano i nomi in modo semplificato, non semantico e non internazionalizzabile. È sempre preferibile utilizzare xdm:fullName. |
| `extendedWorkDetails.jobTitle` | Qualifica | Qualifica | stringa | stringa | Qualifica della persona. |
| `person.name.lastName` | Cognome | Cognome | stringa | stringa | L’ultimo segmento del nome nell’ordine di scrittura più comunemente accettato nella lingua del nome. In molte culture questo è il nome ereditario di famiglia, cognome, patronimico o matronimico. Le proprietà firstName e lastName sono state introdotte per mantenere la compatibilità con i sistemi esistenti che modellano i nomi in modo semplificato, non semantico e non internazionalizzabile. È sempre preferibile utilizzare xdm:fullName. |
| `b2b.personStatus` | Stato Lead | ? | stringa | stringa | Campo che registra lo stato attuale di marketing/vendite della persona. |
| `b2b.isMarketingSuspended` | Marketing sospeso | ? | booleano | booleano | Indica se il marketing è sospeso per la persona. |
| `b2b.marketingSuspendedCause` | Causa della sospensione del marketing | ? | stringa | stringa | Se il marketing viene sospeso per la persona, questa proprietà fornisce il motivo. |
| `person.name.middleName` | Secondo nome | ? | stringa | telefono | Secondi nomi, nomi alternativi o aggiuntivi forniti tra nome e cognome. |
| `mobilePhone.number` | Numero di telefono | Numero di telefono | stringa | telefono | Numero di telefono cellulare. |
| `workPhone.number` | Numero di telefono | Numero di telefono | stringa | telefono | Numero di telefono di lavoro. |
| `workAddress.postalCode` | Codice postale | Codice postale | stringa | stringa | Il codice postale della località. I codici postali non sono disponibili per tutti i paesi. In alcuni paesi, questa conterrà solo una parte del codice postale. |
| `person.name.courtesyTitle` | Formula di saluto | ? | stringa | stringa | Normalmente un&#39;abbreviazione di un titolo, titolo onorifico o formula introduttiva di una persona. Il courtesyTitle viene utilizzato davanti al nome completo o al cognome nei testi di apertura. Ad esempio, Sig., Sig.na o Dott. |
| `workAddress.state` | Stato | Stato | stringa | stringa | Il nome dello Stato. Questo è un campo in formato libero. |
| `consents.marketing.email.val` | Annulla l&#39;iscrizione | Annulla l&#39;iscrizione | stringa | booleano | Se l&#39;annullamento dell&#39;abbonamento è vero (ad esempio, valore = 1), impostare `consents.marketing.email.val` come (n). Se l’annullamento dell’abbonamento è falso (ad esempio, valore = 0), imposta consents.marketing.email.val su null. |
| `consents.marketing.email.reason` | Motivo di annullamento dell&#39;iscrizione | Motivo di annullamento dell&#39;iscrizione | stringa | stringa |  |
| `b2b.companyWebsite` | Sito web | ? | stringa | url | Sito web della società a cui è associata una persona aziendale. |

