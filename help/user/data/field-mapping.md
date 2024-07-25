---
title: Mappatura campo XDM
description: Esamina la mappatura dei campi tra lo schema XDM di AEP, il Marketo Engage e la Journey Optimizer B2B Edition.
exl-id: 8c65fdec-e32d-4ba8-be7b-48522cc3dace
source-git-commit: 7103e4f6666482a72511661dfaed1392d4eb16b1
workflow-type: tm+mt
source-wordcount: '576'
ht-degree: 19%

---

# Mappatura campo XDM

Il servizio di trasferimento dati (DTS) in è responsabile della sincronizzazione dei dati da Adobe Experience Platform a Journey Optimizer B2B Edition. DTS si basa sulle mappature tra i campi dello schema XDM Experience Platform e i relativi equivalenti nel Marketo Engage.

## Mappature campi predefiniti persona aziendale XDM

| Persona aziendale XDM | Nome visualizzato persona Marketo Engage | Nome visualizzato della persona B2B di AJO | Tipo XDM | Tipo Marketo | Descrizione XDM |
|------------------- |---------------------------------- |--------------------------- |-------- |------------ |--------------- |
| `workAddress.street1` | Indirizzo | N/D | stringa | testo | Informazioni stradali primarie, numero di appartamento, numero civico e nome della strada. |
| `workAddress.city ` | Città | Città | stringa | stringa | Il nome della città. |
| `b2b.companyName` | Nome della società | Azienda | stringa | stringa | Nome della società a cui è associata una persona aziendale. |
| `workAddress.country` | Paese | Paese | stringa | stringa | Il nome del territorio amministrato dal governo. A parte `xdm:countryCode`, questo è un campo in formato libero che può avere il nome del paese in qualsiasi lingua. |
| `person.birthDate` | Data di nascita | Data di nascita | stringa | data | La data completa di nascita di una persona.  DD/MM/YYYY |
| `workEmail.address` | Indirizzo e-mail | Indirizzo e-mail | stringa | e-mail | L&#39;indirizzo tecnico, ad esempio &#39;<name@domain.com>&#39;, come comunemente definito in RFC2822 e standard successivi. |
| `workEmail.status` | E-mail sospesa | E-mail sospesa | stringa | booleano | Un’indicazione relativa alla possibilità di utilizzare l’indirizzo e-mail. |
| `faxPhone.number` | Numero di fax | N/D | stringa | telefono | Numero di fax. |
| `person.name.firstName` | Nome | Nome | stringa | stringa | Il primo segmento del nome nell’ordine di scrittura più comunemente accettato nella lingua del nome. In molte culture questo è il nome personale o di battesimo preferito. Le proprietà firstName e lastName sono state introdotte per mantenere la compatibilità con i sistemi esistenti che modellano i nomi in modo semplificato, non semantico e non internazionalizzabile. È sempre preferibile utilizzare xdm:fullName. |
| `extendedWorkDetails.jobTitle` | Qualifica | Qualifica | stringa | stringa | Qualifica della persona. |
| `person.name.lastName` | Cognome | Cognome | stringa | stringa | L’ultimo segmento del nome nell’ordine di scrittura più comunemente accettato nella lingua del nome. In molte culture questo è il nome ereditario di famiglia, cognome, patronimico o matronimico. Le proprietà firstName e lastName sono state introdotte per mantenere la compatibilità con i sistemi esistenti che modellano i nomi in modo semplificato, non semantico e non internazionalizzabile. È sempre preferibile utilizzare xdm:fullName. |
| `b2b.personStatus` | Stato Lead | N/D | stringa | stringa | Campo che registra lo stato attuale di marketing/vendite della persona. |
| `b2b.isMarketingSuspended` | Marketing sospeso | N/D | booleano | booleano | Indica se il marketing è sospeso per la persona. |
| `b2b.marketingSuspendedCause` | Causa della sospensione del marketing | N/D | stringa | stringa | Se il marketing viene sospeso per la persona, questa proprietà fornisce il motivo. |
| `person.name.middleName` | Secondo nome | N/D | stringa | telefono | Secondi nomi, nomi alternativi o aggiuntivi forniti tra nome e cognome. |
| `mobilePhone.number` | Numero di telefono | Numero di telefono | stringa | telefono | Numero di telefono cellulare. |
| `workPhone.number` | Numero di telefono | Numero di telefono | stringa | telefono | Numero di telefono di lavoro. |
| `workAddress.postalCode` | Codice di avviamento postale | Codice di avviamento postale | stringa | stringa | Il codice postale della località. I codici postali non sono disponibili per tutti i paesi. In alcuni paesi, questa conterrà solo una parte del codice postale. |
| `person.name.courtesyTitle` | Formula di saluto | N/D | stringa | stringa | Normalmente un&#39;abbreviazione di un titolo, titolo onorifico o formula introduttiva di una persona. Il courtesyTitle viene utilizzato davanti al nome completo o al cognome nei testi di apertura. Ad esempio, Sig., Sig.na o Dott. |
| `workAddress.state` | Stato | Stato | stringa | stringa | Il nome dello Stato. Questo è un campo in formato libero. |
| `consents.marketing.email.val` | Annulla l&#39;iscrizione | Annulla l&#39;iscrizione | stringa | booleano | Se l&#39;annullamento dell&#39;abbonamento è vero (ad esempio, valore = 1), impostare `consents.marketing.email.val` come (n). Se l’annullamento dell’abbonamento è falso (ad esempio, valore = 0), imposta consents.marketing.email.val su null. |
| `consents.marketing.email.reason` | Motivo di annullamento dell&#39;iscrizione | Motivo di annullamento dell&#39;iscrizione | stringa | stringa |  |
| `b2b.companyWebsite` | Sito web | N/D | stringa | url | Sito web della società a cui è associata una persona aziendale. |
