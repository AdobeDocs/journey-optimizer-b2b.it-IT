---
title: Content Credentials
description: Scopri in che modo Adobe Journey Optimizer B2B edition applica automaticamente Content Credentials alle immagini generate o modificate con strumenti di intelligenza artificiale generativi e cosa significa per i contenuti.
feature: Assets, Content
role: User
autotag-review: '2026-07-31T22:15:54.535Z'
TQID: 'https://experienceleague.adobe.com/9XCqPWz62uDDLFAyxARfD2jErYx2aOiOB5fAOGLLTbo'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: a65c8aea-b21a-41ce-9ed7-6b517a69fd0bid: bef5003b-cad2-4f40-bdb2-a80426d52ef5id: e666e996-b2cf-4c45-8fc2-1c625212abab
subfeature_v2: id: c8402946-ff35-44c5-ab98-74c1bba0975f
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: ad794b50f6c6f3b59e853e99f7983136ee098e18
workflow-type: tm+mt
source-wordcount: 913
ht-degree: 0%

---

# Content Credentials

Le organizzazioni di marketing si preoccupano più che mai della trasparenza dei contenuti, della divulgazione dell’intelligenza artificiale e della prevenzione della manomissione delle risorse. Content Authenticity Initiative (CAI) di Adobe crea strumenti conformi allo standard tecnico [Coalition for Content Provenance and Authenticity](https://c2pa.org/specifications/specifications/1.1/specs/C2PA_Specification.html#_trust_model) (C2PA). _Content Credentials_, metadati crittografati a prova di manomissione, possono aiutare i visualizzatori a comprendere la derivazione dei contenuti e garantire l&#39;integrità delle risorse del marchio. Queste informazioni includono:

* Emittente o firmatario: informazioni sull’entità o sulla società che ha emesso la firma digitale per certificare o firmare la risorsa.
* Data problema: la data in cui il Content Credential è stato applicato alla risorsa.
* Credito e utilizzo: informazioni sul produttore della risorsa, tra cui nome, handle di social media o altre informazioni relative all’identità.
* Processo: record di eventuali modifiche apportate alla risorsa.
* Dettagli dispositivo: informazioni sull’app o sul dispositivo utilizzato per creare o modificare la risorsa.
* Strumento di intelligenza artificiale utilizzato: se per modificare o creare la risorsa è stata utilizzata l’intelligenza artificiale generativa, è possibile includere il nome del modello utilizzato.
* Altre informazioni pertinenti: possono essere inclusi anche dati aggiuntivi per offrire più contesto sulla cronologia di una risorsa.

Per informazioni complete sulla cronologia delle risorse, puoi utilizzare lo strumento di ispezione [di Adobe Content Authenticity](https://contentauthenticity.adobe.com/inspect).

Content Credentials persiste con il file di immagine. Quando un&#39;immagine generata o modificata con IA generativa viene caricata o esportata da [!DNL Adobe Journey Optimizer B2B Edition], il relativo Content Credentials viene mantenuto.

>[!NOTE]
>
>Alcuni metodi di importazione di immagini nel contenuto, ad esempio l&#39;estrazione di un&#39;immagine da un PDF o da un&#39;origine incorporata (base64), potrebbero non mantenere il Content Credentials originale. In questi casi, non è possibile leggere Content Credentials dall’origine e non ne viene creato alcuno per il risultato.

>[!BEGINSHADEBOX]

## Persistenza di Content Credentials tramite canali {#channels}

Quando includi le immagini nell’e-mail o nei messaggi WhatsApp, viene mantenuto anche il Content Credentials per le immagini consegnate:

* **E-mail** - Quando utilizzi un&#39;azione di percorso _Invia e-mail_, aggiungi l&#39;immagine al contenuto dell&#39;e-mail dalla libreria _Assets_. Quando l’e-mail viene consegnata, il destinatario può scaricare l’immagine dal messaggio e il Content Credentials è intatto.
* **WhatsApp** - Aggiungi l&#39;immagine al modello di messaggio WhatsApp nel tuo account aziendale Meta. Puoi aggiungerlo direttamente dal tuo sistema o scaricare un file di immagine dalla libreria _Assets_. Utilizza il modello per un&#39;azione di percorso _Invia WhatsApp_. Quando il messaggio WhatsApp viene consegnato, il destinatario può scaricare l’immagine dal messaggio e il Content Credentials è intatto.

>[!ENDSHADEBOX]

## Azioni che interessano Content Credentials {#cc-workflows}

>[!INFO]
>
>Nuove leggi stanno emergendo sulla trasparenza generativa dell’intelligenza artificiale e Adobe sta lavorando per soddisfare i requisiti applicabili in tutte le giurisdizioni. Content Credentials è lo strumento di provenienza utilizzato da Adobe per soddisfare i requisiti di queste normative.

Quando si genera o si modifica un&#39;immagine con strumenti di intelligenza artificiale generativi in [!DNL Journey Optimizer B2B Edition], Content Credentials viene automaticamente associato all&#39;immagine e non è richiesta alcuna azione da parte dell&#39;utente.

### Generare un’immagine {#generate}

**_Esempio:_** Genera un&#39;immagine del banner per un&#39;e-mail da un prompt di testo che descrive l&#39;elemento visivo desiderato. Content Credentials sono associati all&#39;immagine generata.

Quando crei una nuova immagine da un prompt di testo, da un’immagine di riferimento o generi un’immagine simile, Content Credentials viene sempre associato.

### Ritagliare un’immagine {#crop}

**_Esempi:_**

* Ritagliare un&#39;immagine del banner generata per adattarla a una pagina Web. I Content Credentials vengono conservati attraverso il ritaglio.
* Utilizza una foto caricata come sfondo e-mail e ritagliala per adattarla allo schermo. Se la foto d’archivio non contiene informazioni generative sull’intelligenza artificiale, Content Credentials non viene creato.

Quando apportate una regolazione a un file di immagine, ad esempio per ritagliarlo nelle dimensioni richieste, il Content Credentials viene mantenuto solo se l&#39;immagine di origine ne disponeva già. Il ritaglio ricrea i pixel dell&#39;immagine, che in genere rimuove il Content Credential, quindi l&#39;Assistente AI legge l&#39;immagine dall&#39;immagine di origine prima del ritaglio, quindi la ricrea e la ricollega al risultato ritagliato. Il ritaglio stesso non aggiunge una nuova azione di IA generativa, ma mantiene quella esistente.

### Aggiungere una sovrapposizione di testo

**_Esempio:_** Produrre un titolo promozionale come sovrapposizione di testo su un&#39;immagine di sfondo generata per una pagina di destinazione. Il Content Credentials dell&#39;immagine di sfondo viene mantenuto.

Quando eseguite il rendering del testo generato sopra un&#39;immagine di sfondo, Content Credentials viene allegato all&#39;immagine risultante solo se l&#39;immagine di sfondo contiene già Content Credentials. Il rendering della sovrapposizione genera una nuova immagine, in modo che lo strumento di modifica delle immagini legga il Content Credentials dallo sfondo e lo ricolleghi al risultato. Il passaggio di sovrapposizione non aggiunge una nuova azione di IA generativa.

### Sovrapponi un&#39;immagine

**_Esempi:_**

* Crea un’intestazione e-mail combinando un’immagine di prodotto generata con uno sfondo generato. Il risultato porta Content Credentials che riflette entrambe le fonti di intelligenza artificiale generative.
* Combina due foto del marchio caricate in un&#39;unica immagine collage. Poiché nessuna delle immagini sorgente dispone di un’azione di intelligenza artificiale generativa, Content Credentials non viene creato.

Quando composite due o più immagini insieme e una qualsiasi delle immagini sorgente dispone di Content Credentials, l’immagine combinata le mantiene, unite in un singolo elemento di metadati Content Credentials. La composizione produce una nuova immagine dalle sorgenti, che normalmente rimuove quelle Content Credentials. Tuttavia, gli strumenti di modifica delle immagini leggono ciascuno prima di comporre, quindi creano un singolo elemento Content Credentials combinato che elenca tutte le sorgenti che hanno contribuito a un’azione di intelligenza artificiale generativa.

<!--

In [!DNL Adobe Journey Optimizer B2B Edition], you can see Content Credentials directly within the _Assets_ library. When you open the asset details, any image with Content Credentials (such as those created with GenAI services) shows the manifest details in a dedicated panel. If the asset is downloaded, published, or shared, the Content Credentials remain intact with the asset.

_To access Content Credentials:_

1. In the left navigation, expand **[!UICONTROL Content Management]** and select **[!UICONTROL Assets]**.

   This action opens a listing page with all the assets listed.

1. Navigate to a folder, and select the desired asset.

1. In the right panel, ??? where is it.

-->