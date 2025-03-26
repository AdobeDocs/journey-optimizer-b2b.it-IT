---
title: Campi XDM
description: Esamina i campi attributo predefiniti sincronizzati tra Adobe Experience Platform e Journey Optimizer B2B edition.
exl-id: 8c65fdec-e32d-4ba8-be7b-48522cc3dace
source-git-commit: e2a802750ee221caf83989c5731e0daee64aa63e
workflow-type: tm+mt
source-wordcount: '1372'
ht-degree: 12%

---

# Campi XDM

I dati sul pubblico dell’account vengono memorizzati come attributi sia nelle classi XDM Business Account che XDM Business Person. I dati vengono periodicamente sincronizzati tra Adobe Experience Platform e Journey Optimizer B2B edition. Nelle sezioni seguenti sono elencati i set di attributi predefiniti.

>[!TIP]
>
>È possibile modellare le classi XDM Business Person e XDM Business Account in una relazione molti-a-molti utilizzando la classe XDM Business Account Person Relation come descritto nella [documentazione Experience Platform XDM](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/tutorials/relationship-b2b).

## Attributi di relazione della persona dell’account aziendale XDM

| [Proprietà](https://github.com/adobe/xdm/blob/master/docs/reference/mixins/profile/b2b-person-details.schema.md) | Nome visualizzato | Nome visualizzato B2B Journey Optimizer | Tipo di dati | Descrizione |
|------------------- |---------------------------------- |--------------------------- |-------- |--------------- |
| `personRoles` | Ruoli della persona | Ruolo | Array di stringhe | Array di ruoli associati alla persona nell&#39;account, ad esempio `owner, accountant, designer`. |

## Attributi persona aziendale XDM

>[!IMPORTANT]
>
>L&#39;attributo `workEmail.Address` è obbligatorio. Se è vuoto per un membro del pubblico dell’account, la persona non viene acquisita e viene omessa dai percorsi di account e dai gruppi di acquisto che fanno riferimento al pubblico.

| [Proprietà](https://github.com/adobe/xdm/blob/master/docs/reference/mixins/profile/b2b-person-details.schema.md) | Nome visualizzato | Nome visualizzato B2B Journey Optimizer | Tipo di dati | Descrizione |
|------------------- |---------------------------------- |--------------------------- |-------- |--------------- |
| `b2b.companyName` | Nome della società | Nome della società | Stringa | Nome della società a cui è associata una persona aziendale. |
| `b2b.companyWebsite` | Sito Web della società | Sito web | Stringa | Sito web della società a cui è associata una persona aziendale. |
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

| [Proprietà](https://github.com/adobe/xdm/blob/master/docs/reference/mixins/account/account-details.schema.md) | Nome visualizzato | Nome visualizzato B2B Journey Optimizer | Tipo di dati | Descrizione |
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

## Attributi dell’opportunità di business XDM

Inoltre, i dati sulle opportunità vengono memorizzati come attributi nella classe XDM Business Opportunity, che può essere associata alla classe XDM Business Account tramite una relazione molti-a-uno, come descritto [qui](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/tutorials/relationship-b2b#relationship-field).

| [Proprietà](https://github.com/adobe/xdm/blob/master/docs/reference/adobe/experience/marketo/opportunity-marketo.schema.md) | Nome visualizzato | Nome visualizzato B2B Journey Optimizer | Tipo di dati | Descrizione |
|------------------- |---------------------------------- |--------------------------- |-------- |--------------- |
| `expectedCloseDate` | Data di chiusura prevista | Data di chiusura prevista dell’opportunità | Stringa | Data prevista di chiusura dell’opportunità. |
| `expectedRevenue.amount` | Ricavi previsti | Ricavi totali previsti per l&#39;opportunità | Stringa | Ricavi calcolati in base all’importo e alla probabilità. |
| `fiscalQuarter` | Trimestre fiscale | Trimestre fiscale opportunità | Stringa | Trimestre fiscale di destinazione per l’opportunità. |
| `fiscalYear` | Anno fiscale | Anno fiscale opportunità | Stringa | L’anno fiscale previsto per l’opportunità. |
| `forecastCategory` | Categoria previsione | Categoria previsione opportunità | Stringa | Categoria di previsione determinata dal valore della fase dell&#39;opportunità. |
| `forecastCategoryName` | Nome categoria previsione | Nome categoria previsione opportunità | Stringa | Nome della categoria di previsione visualizzato nei rapporti per una particolare categoria di previsione. |
| `isClosed` | Flag chiuso | Opportunità chiusa | Stringa | Flag che indica se l’opportunità è chiusa. |
| `isWon` | Flag acquisizione | Opportunità vinta | Stringa | Flag che indica se l’opportunità è stata vinta. |
| `lastActivityDate` | Data ultima attività | Data dell’ultima attività | Stringa | Data dell’ultima attività dell’opportunità. |
| `leadSource` | Fonte Lead | Sorgente lead | Stringa | Source dell’opportunità, ad esempio Annuncio pubblicitario, Partner o Web. |
| `nextStep` | Passaggio successivo | Passaggio successivo dell’opportunità | Stringa | Descrizione dell&#39;attività successiva per la chiusura dell&#39;opportunità. |
| `opportunityAmount.amount` | Importo dell’opportunità | Importo totale dell’opportunità | Stringa | Importo totale stimato della vendita per l’opportunità. |
| `opportunityDescription` | Descrizione dell’opportunità | Descrizione dell’opportunità | Stringa | Informazioni aggiuntive per descrivere l&#39;opportunità, ad esempio possibili prodotti da vendere o acquisti precedenti effettuati dal cliente. |
| `opportunityName` | Nome opportunità | Nome opportunità | Stringa | Nome soggetto o descrittivo, ad esempio il nome dell’ordine o della società previsto per l’opportunità. |
| `opportunityQuantity` | Quantità opportunità | Quantità opportunità | Stringa | Totale di tutti i valori dei campi quantità per tutti i prodotti nell’elenco Prodotti correlato per l’opportunità. |
| `opportunityStage` | Fase dell’opportunità | Fase dell’opportunità | Stringa | Fase di vendita dell&#39;opportunità di aiutare il team di vendita nei loro sforzi per vincerla. |
| `opportunityType` | Tipo di opportunità | Tipo di opportunità | Stringa | Tipo assegnato all&#39;opportunità, ad esempio _Attività esistente _ o _Nuova attività_ |
| `probabilityPercentage` | Percentuale di probabilità | Percentuale di probabilità di opportunità | Stringa | Probabilità di chiusura dell&#39;opportunità, espressa in percentuale. |
