---
title: Metadati C2PA
description: Scopri in che modo Adobe Journey Optimizer B2B edition applica automaticamente i metadati C2PA alle immagini generate o modificate con strumenti di intelligenza artificiale generativi e cosa significa per i contenuti.
feature: Assets, Content
role: User
autotag-review: '2026-07-31T22:15:54.535Z'
TQID: 'https://experienceleague.adobe.com/9XCqPWz62uDDLFAyxARfD2jErYx2aOiOB5fAOGLLTbo'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: a65c8aea-b21a-41ce-9ed7-6b517a69fd0b
  - id: bef5003b-cad2-4f40-bdb2-a80426d52ef5
  - id: e666e996-b2cf-4c45-8fc2-1c625212abab
subfeature_v2:
  - id: c8402946-ff35-44c5-ab98-74c1bba0975f
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: dd969d66eab5649ccb19fe6582dafe0b7304772c
workflow-type: tm+mt
source-wordcount: 913
ht-degree: 0%

---

# Metadati C2PA

Le organizzazioni di marketing si preoccupano più che mai della trasparenza dei contenuti, della divulgazione dell’intelligenza artificiale e della prevenzione della manomissione delle risorse. Content Authenticity Initiative (CAI) di Adobe crea strumenti conformi allo standard tecnico [Coalition for Content Provenance and Authenticity](https://c2pa.org/specifications/specifications/1.1/specs/C2PA_Specification.html#_trust_model) (C2PA). _I metadati C2PA_ sono informazioni crittografate e in grado di evidenziare eventuali manomissioni che consentono agli utenti di comprendere la derivazione dei contenuti e garantire l&#39;integrità delle risorse del marchio. Queste informazioni includono:

* Emittente o firmatario: informazioni sull’entità o sulla società che ha emesso la firma digitale per certificare o firmare la risorsa.
* Data problema: data in cui i metadati C2PA sono stati applicati alla risorsa.
* Credito e utilizzo: informazioni sul produttore della risorsa, tra cui nome, handle di social media o altre informazioni relative all’identità.
* Processo: record di eventuali modifiche apportate alla risorsa.
* Dettagli dispositivo: informazioni sull’app o sul dispositivo utilizzato per creare o modificare la risorsa.
* Strumento di intelligenza artificiale utilizzato: se per modificare o creare la risorsa è stata utilizzata l’intelligenza artificiale generativa, è possibile includere il nome del modello utilizzato.
* Altre informazioni pertinenti: possono essere inclusi anche dati aggiuntivi per offrire più contesto sulla cronologia di una risorsa.

Per informazioni complete sulla cronologia delle risorse, puoi utilizzare lo strumento di [ispezione di Adobe Content Authenticity](https://contentauthenticity.adobe.com/inspect).

I metadati C2PA persistono con il file di immagine. Quando un&#39;immagine generata o modificata con IA generativa viene caricata o esportata da [!DNL Adobe Journey Optimizer B2B Edition], i relativi metadati C2PA vengono conservati.

>[!NOTE]
>
>Alcuni metodi di importazione di immagini nel contenuto, ad esempio l&#39;estrazione di un&#39;immagine da un PDF o da un&#39;origine incorporata (base64), potrebbero non conservare i metadati C2PA originali. In questi casi, i metadati C2PA non possono essere letti dalla sorgente e non ne viene creato alcuno per il risultato.

>[!BEGINSHADEBOX]

## Persistenza dei metadati C2PA tramite canali {#channels}

Quando includi le immagini nelle e-mail o nei messaggi WhatsApp, vengono mantenuti anche i metadati C2PA per le immagini consegnate:

* **E-mail** - Quando utilizzi un&#39;azione di percorso _Invia e-mail_, aggiungi l&#39;immagine al contenuto dell&#39;e-mail dalla libreria _Assets_. Quando l’e-mail viene consegnata, il destinatario può scaricare l’immagine dal messaggio e i metadati C2PA sono intatti.
* **WhatsApp** - Aggiungi l&#39;immagine al modello di messaggio WhatsApp nel tuo account aziendale Meta. Puoi aggiungerlo direttamente dal tuo sistema o scaricare un file di immagine dalla libreria _Assets_. Utilizza il modello per un&#39;azione di percorso _Invia WhatsApp_. Quando il messaggio WhatsApp viene consegnato, il destinatario può scaricare l’immagine dal messaggio e i metadati C2PA sono intatti.

>[!ENDSHADEBOX]

## Azioni che influiscono sui metadati C2PA {#cc-workflows}

>[!INFO]
>
>Nuove leggi stanno emergendo sulla trasparenza generativa dell’intelligenza artificiale e Adobe sta lavorando per soddisfare i requisiti applicabili in tutte le giurisdizioni. I metadati C2PA sono lo strumento di provenienza utilizzato da Adobe per soddisfare i requisiti di queste normative.

Quando si genera o si modifica un&#39;immagine con strumenti di intelligenza artificiale generativi in [!DNL Journey Optimizer B2B Edition], i metadati C2PA vengono automaticamente associati all&#39;immagine e non è richiesta alcuna azione da parte dell&#39;utente.

### Generare un’immagine {#generate}

**_Esempio:_** Genera un&#39;immagine del banner per un&#39;e-mail da un prompt di testo che descrive l&#39;elemento visivo desiderato. I metadati C2PA vengono allegati all&#39;immagine generata.

Quando crei una nuova immagine da un prompt di testo, da un&#39;immagine di riferimento o generi un&#39;immagine simile, i metadati C2PA vengono sempre allegati.

### Ritagliare un’immagine {#crop}

**_Esempi:_**

* Ritagliare un&#39;immagine del banner generata per adattarla a una pagina Web. I metadati C2PA vengono conservati attraverso la coltura.
* Utilizza una foto caricata come sfondo e-mail e ritagliala per adattarla allo schermo. Se la foto d&#39;archivio non contiene informazioni generative sull&#39;intelligenza artificiale, i metadati C2PA non vengono creati.

Quando apportate una regolazione a un file di immagine, ad esempio per ritagliarlo nelle dimensioni richieste, i metadati C2PA vengono mantenuti solo se l&#39;immagine di origine ne disponeva già. Il ritaglio ricrea i pixel dell&#39;immagine, che in genere rimuove i metadati C2PA, pertanto l&#39;Assistente IA legge l&#39;immagine sorgente prima del ritaglio, quindi la ricrea e la ricollega al risultato ritagliato. Il ritaglio stesso non aggiunge una nuova azione di IA generativa, ma mantiene quella esistente.

### Aggiungere una sovrapposizione di testo

**_Esempio:_** Produrre un titolo promozionale come sovrapposizione di testo su un&#39;immagine di sfondo generata per una pagina di destinazione. I metadati C2PA dell’immagine di sfondo vengono conservati.

Quando eseguite il rendering del testo generato sopra un&#39;immagine di sfondo, i metadati C2PA vengono allegati all&#39;immagine risultante solo se l&#39;immagine di sfondo contiene già metadati C2PA. Il rendering della sovrapposizione produce una nuova immagine, in modo che lo strumento di modifica delle immagini legga i metadati C2PA dallo sfondo e li ricolleghi al risultato. Il passaggio di sovrapposizione non aggiunge una nuova azione di IA generativa.

### Sovrapponi un&#39;immagine

**_Esempi:_**

* Crea un’intestazione e-mail combinando un’immagine di prodotto generata con uno sfondo generato. Il risultato contiene metadati C2PA che riflettono entrambe le fonti di IA generative.
* Combina due foto del marchio caricate in un&#39;unica immagine collage. Poiché nessuna delle immagini sorgente dispone di un’azione di intelligenza artificiale generativa, i metadati C2PA non vengono creati.

Quando composite due o più immagini insieme e una qualsiasi delle immagini sorgente dispone di metadati C2PA, l&#39;immagine combinata la mantiene, unita in un unico elemento di metadati C2PA. La composizione produce una nuova immagine dalle sorgenti, che normalmente rimuove i metadati C2PA. Tuttavia, gli strumenti di modifica delle immagini leggono i metadati sorgente prima di effettuare la composizione, quindi creano un singolo elemento di metadati C2PA combinato che elenca tutte le sorgenti che hanno contribuito a un’azione di intelligenza artificiale generativa.

<!--

In [!DNL Adobe Journey Optimizer B2B Edition], you can see C2PA metadata directly within the _Assets_ library. When you open the asset details, any image with C2PA metadata (such as those created with GenAI services) shows the manifest details in a dedicated panel. If the asset is downloaded, published, or shared, the C2PA metadata remains intact with the asset.

_To access C2PA metadata:_

1. In the left navigation, expand **[!UICONTROL Content Management]** and select **[!UICONTROL Assets]**.

   This action opens a listing page with all the assets listed.

1. Navigate to a folder, and select the desired asset.

1. In the right panel, ??? where is it.

-->
