---
title: Campi XDM
description: Esamina i campi attributo predefiniti sincronizzati tra Adobe Experience Platform e Journey Optimizer B2B edition.
feature: Data Management, Integrations
role: User
exl-id: 8c65fdec-e32d-4ba8-be7b-48522cc3dace
source-git-commit: 9ad8ba495cdae4c88d9422f758ea912ca84e143c
workflow-type: tm+mt
source-wordcount: '1004'
ht-degree: 13%

---

# Campi XDM

I dati sul pubblico dell’account vengono memorizzati come attributi sia nelle classi XDM Business Account che XDM Business Person. I dati vengono periodicamente sincronizzati tra Adobe Experience Platform e Journey Optimizer B2B edition. Nelle sezioni seguenti sono elencati i set di attributi predefiniti.

>[!TIP]
>
>È possibile modellare le classi XDM Business Person e XDM Business Account in una relazione molti-a-molti utilizzando la classe XDM Business Account Person Relation come descritto nella [documentazione Experience Platform XDM](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/tutorials/relationship-b2b){target="_blank"}.

## Attributi di relazione della persona dell’account aziendale XDM

| [Proprietà](https://github.com/adobe/xdm/blob/master/docs/reference/mixins/profile/b2b-person-details.schema.md){target="_blank"} | Nome visualizzato | Nome visualizzato B2B Journey Optimizer | Tipo di dati | Descrizione |
|------------------- |---------------------------------- |--------------------------- |-------- |--------------- |
| `personRoles` | Ruoli della persona | Ruolo | Array di stringhe | Array di ruoli associati alla persona nell&#39;account, ad esempio `owner, accountant, designer`. |

## Attributi persona aziendale XDM

>[!IMPORTANT]
>
>L&#39;attributo `workEmail.Address` è obbligatorio. Se è vuoto per un membro del pubblico dell’account, la persona non viene acquisita e viene omessa dai percorsi di account e dai gruppi di acquisto che fanno riferimento al pubblico.

| [Proprietà](https://github.com/adobe/xdm/blob/master/docs/reference/mixins/profile/b2b-person-details.schema.md){target="_blank"} | Nome visualizzato | Nome visualizzato B2B Journey Optimizer | Tipo di dati | Descrizione |
|------------------- |---------------------------------- |--------------------------- |-------- |--------------- |
| `b2b.isMarketingSuspended` | Indicatore di sospensione del marketing | Marketing sospeso | Booleano | Il valore indica se il marketing è sospeso per la persona. |
| `b2b.marketingSuspendedCause` | Causa della sospensione del marketing | Causa della sospensione del marketing | Stringa | Se il marketing viene sospeso per la persona, questa proprietà fornisce il motivo. |
| `b2b.personStatus` | Stato della persona | Stato Lead | Stringa | Campo che registra lo stato attuale di marketing/vendite della persona. |
| `consents.marketing.email.reason` | Motivo della rinuncia | Motivo di annullamento dell&#39;iscrizione | Stringa | Motivo associato alla rinuncia e-mail. |
| `consents.marketing.email.val` | Annulla l&#39;iscrizione | Annulla l&#39;iscrizione | Stringa | Se l&#39;annullamento dell&#39;abbonamento è vero (ad esempio, valore = 1), impostare `consents.marketing.email.val` come (n). Se l&#39;annullamento dell&#39;abbonamento è falso (ad esempio, valore = 0), impostare `consents.marketing.email.val` come null. |
| `extendedWorkDetails.jobTitle` | Qualifica | Qualifica | Stringa | Qualifica della persona. |
| `faxPhone.number` | Numero | Numero di fax | Stringa | Numero di fax. |
| `mobilePhone.number` | Numero | Numero di telefono | Stringa | Numero di telefono cellulare associato alla persona. |
| `person.birthDate` | Data di nascita (AAAA-MM-GG) | Data di nascita | Stringa | La data completa di nascita di una persona. DD/MM/YYYY |
| `person.name.courtesyTitle` | Titolo di cortesia | Formula di saluto | Stringa | Normalmente un&#39;abbreviazione del titolo, titolo onorifico o formula di apertura di una persona. Il courtesyTitle viene utilizzato davanti al nome completo o al cognome nei testi di apertura. Ad esempio, Sig., Sig.ra o Dott. |
| `person.name.firstName` | Nome | Nome | Stringa | Il primo segmento del nome nell’ordine scritto più comunemente accettato nella lingua del nome. In molte culture, è il nome personale o di battesimo preferito. Le proprietà firstName e lastName sono state introdotte per mantenere la compatibilità con i sistemi esistenti che modellano i nomi in modo semplificato, non semantico e non internazionalizzabile. L&#39;utilizzo di `xdm:fullName` è sempre preferibile. |
| `person.name.lastName` | Cognome | Cognome | Stringa | L’ultimo segmento del nome nell’ordine scritto più comunemente accettato nella lingua del nome. In molte culture, è il cognome, il nome patronimico o matronimico ereditato. Le proprietà firstName e lastName sono state introdotte per mantenere la compatibilità con i sistemi esistenti che modellano i nomi in modo semplificato, non semantico e non internazionalizzabile. L&#39;utilizzo di `xdm:fullName` è sempre preferibile. |
| `person.name.middleName` | Secondo nome | Secondo nome | Stringa | Secondi nomi, nomi alternativi o aggiuntivi forniti tra nome e cognome. |
| `workAddress.city ` | Città | Città | Stringa | Il nome della città. |
| `workAddress.country` | Paese | Paese | Stringa | Il nome del territorio amministrato dal governo. A parte `xdm:countryCode`, è un campo in formato libero che può avere il nome del paese in qualsiasi lingua. |
| `workAddress.postalCode` | Codice postale | Codice di avviamento postale | Stringa | Il codice postale della località. I codici postali non sono disponibili per tutti i paesi. In alcuni paesi, contiene solo una parte del codice postale. |
| `workAddress.state` | Stato | Stato | Stringa | Nome dello stato dell&#39;indirizzo. È un campo in formato libero. |
| `workAddress.street1` | Strada 1 | Indirizzo | Stringa | Informazioni stradali primarie, numero di appartamento, numero civico e nome della strada. |
| `workEmail.address` | Indirizzo | Indirizzo e-mail | Stringa | **Campo obbligatorio** <br/>Indirizzo tecnico, ad esempio `<name@domain.com>`, come comunemente definito in RFC2822 e standard successivi. |
| `workEmail.status` | Stato | E-mail sospesa | Stringa | Un’indicazione relativa alla possibilità di utilizzare l’indirizzo e-mail. |
| `workPhone.number` | Numero | Numero di telefono | Stringa | Numero di telefono di lavoro. |

## Attributi dell’account aziendale XDM

>[!IMPORTANT]
>
>L&#39;attributo `accountName` è obbligatorio. Se è vuoto per un account in un pubblico di account, l’account non viene acquisito e viene omesso dai percorsi di account e dai gruppi di acquisto che fanno riferimento al pubblico.

| [Proprietà](https://github.com/adobe/xdm/blob/master/docs/reference/mixins/account/account-details.schema.md){target="_blank"} | Nome visualizzato | Nome visualizzato B2B Journey Optimizer | Tipo di dati | Descrizione |
|------------------- |---------------------------------- |--------------------------- |-------- |--------------- |
| `accountBillingAddress.city` | Città | Città | Stringa | Il nome della città utilizzato nell’indirizzo di fatturazione. |
| `accountBillingAddress.country` | Paese | Paese | Stringa | Nome del territorio amministrato dal governo utilizzato nell&#39;indirizzo di fatturazione. A parte `xdm:countryCode`, è un campo in formato libero che può avere il nome del paese in qualsiasi lingua. |
| `accountBillingAddress.postalCode` | Codice postale | Indirizzo Codice postale | Stringa | Il codice postale dell’ubicazione dell’indirizzo di fatturazione. I codici postali non sono disponibili per tutti i paesi. In alcuni paesi, contiene solo una parte del codice postale. |
| `accountBillingAddress.region` | Area geografica | Area dell’indirizzo | Stringa | La regione, la contea o la parte di distretto dell’indirizzo di fatturazione. |
| `accountBillingAddress.state` | Stato | Stato | Stringa | Nome dello stato dell&#39;indirizzo di fatturazione. È un campo in formato libero. |
| `accountBillingAddress.street1` | Strada 1 | Strada 1 | Stringa | Informazioni stradali primarie per l’indirizzo di fatturazione, che in genere includono il numero dell’appartamento, il numero civico e il nome della strada. |
| `accountName` | Nome | Nome | Stringa | **Campo obbligatorio** <br/>Nome dell&#39;azienda. In questo campo sono consentiti fino a 255 caratteri. |
| `accountOrganization.annualRevenue.amount` | Ricavi annuali | Ricavi annuali | Numero | Importo stimato delle entrate annuali dell’organizzazione. |
| `accountOrganization.industry` | Settore | Settore | Stringa | Il settore è stato attribuito all’organizzazione. È un campo in formato libero ed è consigliabile utilizzare un valore strutturato per le query o utilizzare la proprietà `xdm:classifier`. |
| `accountOrganization.logoUrl` | URL logo | URL logo | Stringa | Percorso da combinare con l&#39;URL di un&#39;istanza di Salesforce (ad esempio, `https://yourInstance.salesforce.com/`) per generare un URL per richiedere l&#39;immagine del profilo del social network associata all&#39;account. L&#39;URL generato restituisce un reindirizzamento HTTP (codice 302) all&#39;immagine del profilo del social network dell&#39;account. |
| `accountOrganization.numberOfEmployees` | Numero di dipendenti | Numero dipendenti | Intero | Il numero di dipendenti dell&#39;organizzazione. |
| `accountOrganization.SICCode` | Codice SIC (Standard Industrial Classification) | Codice SIC (Standard Industrial Classification) | Stringa | Il codice SIC (Standard Industrial Classification) è un codice a quattro cifre che categorizza i settori a cui appartengono le aziende in base alle loro attività commerciali. |
| `accountOrganization.website` | URL sito Web | Nome dominio | Stringa | L’URL del sito web dell’organizzazione. |
| `accountPhone.number` | N/D | Numero di telefono dell’account | Stringa | Numero di telefono associato all’account. |
| `accountSourceType` | N/D | Tipo di origine | Stringa | Tipo di Source per l’account. |

<!-- ## XDM Business Opportunity attributes

Additionally, opportunity data is stored as attributes in the XDM Business Opportunity class, which can be associated with the XDM Business Account class through a many-to-one relationship, as described in the [Exerience Platform documentation](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/tutorials/relationship-b2b#relationship-field){target="_blank"}.

|[Property](https://github.com/adobe/xdm/blob/master/docs/reference/adobe/experience/marketo/opportunity-marketo.schema.md){target="_blank"} |Display name |Journey Optimizer B2B display name |Data type |Description |
|------------------- |---------------------------------- |--------------------------- |-------- |--------------- |
|`expectedCloseDate` | Expected Close Date  | Expected opportunity close date   | String | Expected date of closure for the opportunity.   |
|`expectedRevenue.amount` | Expected Revenue  | Total opportunity expected revenue   | String | Calculated revenue based on the Amount and Probability.   |
|`fiscalQuarter` | Fiscal Quarter   | Opportunity fiscal quarter  | String | The targeted fiscal quarter for the opportunity.   |
|`fiscalYear` | Fiscal Year   | Opportunity fiscal year   | String | The targeted fiscal year for the opportunity.   |
|`forecastCategory`|Forecast Category | Opportunity Forecast category | String | Forecast Category determined by the opportunity Stage value. |
|`forecastCategoryName`|Forecast Category Name | Opportunity forecast category name | String | Forecast category name that is displayed in reports for a particular forecast category. |
|`isClosed` | Closed Flag  | Opportunity closed   | String | Flag that indicates if the opportunity is closed.   |
|`isWon` | Won Flag  | Opportunity won   | String | Flag that indicates if the opportunity is won.  |
|`lastActivityDate` | Last Activity Date  | Last activity date   | String | Last activity date for the opportunity.  |
|`leadSource` | Lead Source  | Lead source   | String | Source of the opportunity, such as Advertisement, Partner, or Web.   |
|`nextStep` | Next Step  | Opportunity next step   | String | Description of the next task for closing the opportunity.   |
|`opportunityAmount.amount` | Opportunity Amount  | Total Opportunity Amount | String | Estimated total sale amount for the opportunity.   |
|`opportunityDescription` | Opportunity Description   | Opportunity description  |String  | Additional information to describe the opportunity, such as possible products to sell or past purchases from the customer. |
|`opportunityName` | Opportunity Name   | Opportunity name |String  | Subject or descriptive name, such as the expected order or company name, for the opportunity. |
|`opportunityQuantity` | Opportunity Quantity  | Opportunity quantity   | String | Total of all quantity field values for all products in the related Products list for the opportunity.   |
|`opportunityStage` | Opportunity Stage   | Opportunity stage   | String | Sales stage of the opportunity to aid the sales team in their efforts to win it.  |
|`opportunityType` | Opportunity Type   | Opportunity type   | String | Type assigned to the opportunity, such as _Existing Business_ or _New Business_  |
|`probabilityPercentage` | Probability Percentage  | Opportunity probability percentage  | String | Likelihood of closing the opportunity, stated as a percentage.  |
 -->