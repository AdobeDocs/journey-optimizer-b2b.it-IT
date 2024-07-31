---
title: Mappatura campo XDM
description: Esamina la mappatura dei campi tra lo schema XDM di AEP, il Marketo Engage e la Journey Optimizer B2B Edition.
exl-id: 8c65fdec-e32d-4ba8-be7b-48522cc3dace
source-git-commit: 838308621a27bcfc6425b8683f642a66f1fa6a7b
workflow-type: tm+mt
source-wordcount: '946'
ht-degree: 16%

---

# Mappatura campo XDM

Il servizio di trasferimento dati (DTS) è responsabile della sincronizzazione dei dati da Adobe Experience Platform a Journey Optimizer B2B Edition. DTS si basa sulle mappature tra i campi dello schema XDM Experience Platform e i relativi equivalenti nel Marketo Engage.

## Mappature campi predefiniti persona aziendale XDM

| [Persona aziendale XDM](https://github.com/adobe/xdm/blob/master/docs/reference/mixins/profile/b2b-person-details.schema.md) | Nome visualizzato XDM | Nome visualizzato Marketo Engage | Tipo XDM | Tipo Marketo | Descrizione XDM |
|------------------- |---------------------------------- |--------------------------- |-------- |------------ |--------------- |
| `b2b.companyName` | Nome della società | Nome della società | stringa | stringa | Nome della società a cui è associata una persona aziendale. |
| `b2b.companyWebsite` | Sito Web della società | Sito web | stringa | url | Sito web della società a cui è associata una persona aziendale. |
| `b2b.isMarketingSuspended` | Indicatore di sospensione del marketing | Marketing sospeso | booleano | booleano | Il valore indica se il marketing è sospeso per la persona. |
| `b2b.marketingSuspendedCause` | Causa della sospensione del marketing | Causa della sospensione del marketing | stringa | stringa | Se il marketing viene sospeso per la persona, questa proprietà fornisce il motivo. |
| `b2b.personStatus` | Stato della persona | Stato Lead | stringa | stringa | Campo che registra lo stato attuale di marketing/vendite della persona. |
| `consents.marketing.email.reason` | Motivo della rinuncia | Motivo di annullamento dell&#39;iscrizione | stringa | stringa | Motivo associato alla rinuncia e-mail. |
| `consents.marketing.email.val` | Annulla l&#39;iscrizione | Annulla l&#39;iscrizione | stringa | booleano | Se l&#39;annullamento dell&#39;abbonamento è vero (ad esempio, valore = 1), impostare `consents.marketing.email.val` come (n). Se l’annullamento dell’abbonamento è falso (ad esempio, valore = 0), imposta consents.marketing.email.val su null. |
| `extendedWorkDetails.jobTitle` | Qualifica | Qualifica | stringa | stringa | Qualifica della persona. |
| `faxPhone.number` | Numero | Numero di fax | stringa | telefono | Numero di fax. |
| `mobilePhone.number` | Numero | Numero di telefono | stringa | telefono | Numero di telefono cellulare associato alla persona. |
| `person.birthDate` | Data di nascita (AAAA-MM-GG) | Data di nascita | stringa | data | La data completa di nascita di una persona. DD/MM/YYYY |
| `person.name.courtesyTitle` | Titolo di cortesia | Formula di saluto | stringa | stringa | Normalmente un&#39;abbreviazione del titolo, titolo onorifico o formula di apertura di una persona. Il courtesyTitle viene utilizzato davanti al nome completo o al cognome nei testi di apertura. Ad esempio, Sig., Sig.ra o Dott. |
| `person.name.firstName` | Nome | Nome | stringa | stringa | Il primo segmento del nome nell’ordine scritto più comunemente accettato nella lingua del nome. In molte culture, è il nome personale o di battesimo preferito. Le proprietà firstName e lastName sono state introdotte per mantenere la compatibilità con i sistemi esistenti che modellano i nomi in modo semplificato, non semantico e non internazionalizzabile. L&#39;utilizzo di `xdm:fullName` è sempre preferibile. |
| `person.name.lastName` | Cognome | Cognome | stringa | stringa | L’ultimo segmento del nome nell’ordine scritto più comunemente accettato nella lingua del nome. In molte culture, è il cognome, il nome patronimico o matronimico ereditato. Le proprietà firstName e lastName sono state introdotte per mantenere la compatibilità con i sistemi esistenti che modellano i nomi in modo semplificato, non semantico e non internazionalizzabile. L&#39;utilizzo di `xdm:fullName` è sempre preferibile. |
| `person.name.middleName` | Secondo nome | Secondo nome | stringa | telefono | Secondi nomi, nomi alternativi o aggiuntivi forniti tra nome e cognome. |
| `workAddress.city ` | Città | Città | stringa | stringa | Il nome della città. |
| `workAddress.country` | Paese | Paese | stringa | stringa | Il nome del territorio amministrato dal governo. A parte `xdm:countryCode`, è un campo in formato libero che può avere il nome del paese in qualsiasi lingua. |
| `workAddress.postalCode` | Codice postale | Codice di avviamento postale | stringa | stringa | Il codice postale della località. I codici postali non sono disponibili per tutti i paesi. In alcuni paesi, contiene solo una parte del codice postale. |
| `workAddress.state` | Stato | Stato | stringa | stringa | Nome dello stato dell&#39;indirizzo. È un campo in formato libero. |
| `workAddress.street1` | Strada 1 | Indirizzo | stringa | testo | Informazioni stradali primarie, numero di appartamento, numero civico e nome della strada. |
| `workEmail.address` | Indirizzo | Indirizzo e-mail | stringa | e-mail | L&#39;indirizzo tecnico, ad esempio `<name@domain.com>`, come comunemente definito in RFC2822 e standard successivi. |
| `workEmail.status` | Stato | E-mail sospesa | stringa | booleano | Un’indicazione relativa alla possibilità di utilizzare l’indirizzo e-mail. |
| `workPhone.number` | Numero | Numero di telefono | stringa | telefono | Numero di telefono di lavoro. |

## Mappature campo predefinite dell’account aziendale XDM

| [Account aziendale XDM](https://github.com/adobe/xdm/blob/master/docs/reference/mixins/account/account-details.schema.md) | Nome visualizzato XDM | Nome visualizzato Marketo Engage | Tipo XDM | Tipo di Marketo Engage | Descrizione XDM |
|------------------- |---------------------------------- |--------------------------- |-------- |------------ |--------------- |
| `accountBillingAddress.city` | Città | Città | stringa | stringa | Il nome della città utilizzato nell’indirizzo di fatturazione. |
| `accountBillingAddress.country` | Paese | Paese | stringa | stringa | Nome del territorio amministrato dal governo utilizzato nell&#39;indirizzo di fatturazione. A parte `xdm:countryCode`, è un campo in formato libero che può avere il nome del paese in qualsiasi lingua. |
| `accountBillingAddress.postalCode` | Codice postale | Indirizzo Codice postale | stringa | stringa | Il codice postale dell’ubicazione dell’indirizzo di fatturazione. I codici postali non sono disponibili per tutti i paesi. In alcuni paesi, contiene solo una parte del codice postale. |
| `accountBillingAddress.region` | Area geografica | Area dell’indirizzo | stringa | stringa | La regione, la contea o la parte di distretto dell’indirizzo di fatturazione. |
| `accountBillingAddress.state` | Stato | Stato | stringa | stringa | Nome dello stato dell&#39;indirizzo di fatturazione. È un campo in formato libero. |
| `accountBillingAddress.street1` | Strada 1 | Strada 1 | stringa | stringa | Informazioni stradali primarie per l’indirizzo di fatturazione, che in genere includono il numero dell’appartamento, il numero civico e il nome della strada. |
| `accountName` | Nome | Nome | stringa | stringa | Nome della società. In questo campo sono consentiti fino a 255 caratteri. |
| `accountOrganization.annualRevenue.amount` | Entrata annuale | Entrata annuale | numero | valuta | Importo stimato delle entrate annuali dell’organizzazione. |
| `accountOrganization.industry` | Settore | Settore | stringa | stringa | Il settore è stato attribuito all’organizzazione. È un campo in formato libero ed è consigliabile utilizzare un valore strutturato per le query o utilizzare la proprietà `xdm:classifier`. |
| `accountOrganization.logoUrl` | URL logo | URL logo | stringa | stringa | Percorso da combinare con l&#39;URL di un&#39;istanza Salesforce (ad esempio, `https://yourInstance.salesforce.com/`) per generare un URL per richiedere l&#39;immagine del profilo del social network associata all&#39;account. L&#39;URL generato restituisce un reindirizzamento HTTP (codice 302) all&#39;immagine del profilo del social network dell&#39;account. |
| `accountOrganization.numberOfEmployees` | Numero di dipendenti | Numero dipendenti | intero | intero | Il numero di dipendenti dell&#39;organizzazione. |
| `accountOrganization.SICCode` | Codice SIC (Standard Industrial Classification) | Codice SIC (Standard Industrial Classification) | stringa | stringa | Il codice Standard Industrial Classification (SIC), che è un codice a quattro cifre che categorizza i settori a cui appartengono le aziende in base alle loro attività commerciali. |
| `accountOrganization.website` | URL sito Web | Nome dominio | stringa | stringa | L’URL del sito web dell’organizzazione. |
| `accountPhone.number` | N/D | Numero di telefono dell’account | stringa | stringa | Numero di telefono associato all’account. |
| `accountSourceType` | N/D | Tipo di origine | stringa | stringa | Tipo di Source per l’account. |
