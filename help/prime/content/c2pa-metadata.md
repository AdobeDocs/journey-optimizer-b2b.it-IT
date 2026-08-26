---
title: Metadati C2PA
description: Scopri in che modo Adobe Journey Optimizer B2B Prime applica automaticamente i metadati C2PA alle immagini generate con l’intelligenza artificiale generativa e cosa significa per i contenuti.
feature: Assets, Content
role: User
badgeBeta: label="Beta" type="informative" tooltip="Questa funzione fa parte di una versione beta limitata."
autotag-review: '2026-07-31T22:31:06.899Z'
TQID: 'https://experienceleague.adobe.com/fBPnAmupve3xMSw5fZPQBDTUfr-rwiH2-R3wbKvox-E'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: a65c8aea-b21a-41ce-9ed7-6b517a69fd0b
  - id: e666e996-b2cf-4c45-8fc2-1c625212abab
  - id: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2:
  - id: d270a788-eb1d-40ed-b74e-9158ed975b1f
  - id: c8402946-ff35-44c5-ab98-74c1bba0975f
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: d0e408a3684289460bae729577870fc698c70a60
workflow-type: tm+mt
source-wordcount: 598
ht-degree: 0%

---

# Metadati C2PA

Le organizzazioni di marketing si preoccupano più che mai della trasparenza dei contenuti, della divulgazione dell’intelligenza artificiale e della prevenzione della manomissione delle risorse. Content Authenticity Initiative (CAI) di Adobe crea strumenti conformi allo standard tecnico [Coalition for Content Provenance and Authenticity](https://c2pa.org/specifications/specifications/1.1/specs/C2PA_Specification.html#_trust_model) (C2PA). _I metadati C2PA_ sono informazioni crittografate e in grado di evidenziare eventuali manomissioni che possono aiutare gli utenti a comprendere la derivazione dei contenuti e garantire l&#39;integrità delle risorse del marchio. Queste informazioni includono:

* Emittente o firmatario: informazioni sull&#39;entità o sulla società che ha emesso la firma digitale per certificare o firmare la risorsa.
* Data problema: la data in cui i metadati C2PA sono stati applicati alla risorsa.
* Credito e utilizzo: informazioni sul produttore della risorsa, tra cui nome, handle di social media o altre informazioni relative all&#39;identità.
* Processo - Registra eventuali modifiche apportate alla risorsa.
* Dettagli dispositivo — informazioni sull&#39;app o sul dispositivo utilizzato per creare o modificare la risorsa.
* Strumento di intelligenza artificiale utilizzato: se per creare la risorsa è stata utilizzata l’intelligenza artificiale generativa, è possibile includere il nome del modello utilizzato.
* Altre informazioni pertinenti: sono inclusi anche dati aggiuntivi per offrire maggiore contesto sulla cronologia di una risorsa.

Per informazioni complete sulla cronologia delle risorse, puoi utilizzare lo strumento di [ispezione di Adobe Content Authenticity](https://contentauthenticity.adobe.com/inspect).

I metadati C2PA persistono con il file di immagine. Quando un&#39;immagine generata o modificata con IA generativa viene caricata o esportata da [!DNL Adobe Journey Optimizer B2B Prime], i relativi metadati C2PA vengono conservati.

Per ulteriori dettagli sull&#39;allegato automatico dei metadati C2PA nelle applicazioni Adobe CX Enterprise, vedi [_Trasparenza dei contenuti di IA generativa_](https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/overview/content-transparency){target="_blank"} nella guida AI in CX Enterprise.

>[!NOTE]
>
>Alcuni metodi di importazione di immagini nel contenuto, ad esempio l&#39;estrazione di un&#39;immagine da un PDF o da un&#39;origine incorporata (base64), potrebbero non conservare i metadati C2PA originali. In questi casi, i metadati C2PA non possono essere letti dalla sorgente e non ne viene creato alcuno per il risultato.

>[!BEGINSHADEBOX]

## Persistenza dei metadati C2PA tramite canali {#channels}

Quando includi le immagini nelle e-mail o nei messaggi WhatsApp, vengono mantenuti anche i metadati C2PA per le immagini consegnate:

* **E-mail** - Quando utilizzi un&#39;azione di percorso _Invia e-mail_, aggiungi l&#39;immagine al contenuto dell&#39;e-mail dalla libreria _Assets_. Quando l’e-mail viene consegnata, il destinatario può scaricare l’immagine dal messaggio e i metadati C2PA sono intatti.
* **WhatsApp** - Aggiungi l&#39;immagine al modello di messaggio WhatsApp nel tuo account aziendale Meta. Puoi aggiungerlo direttamente dal sistema o scaricare un file immagine dalla libreria _Assets_. Utilizza il modello per un&#39;azione di percorso _Invia WhatsApp_. Quando il messaggio WhatsApp viene consegnato, il destinatario può scaricare l’immagine dal messaggio e i metadati C2PA sono intatti.

>[!ENDSHADEBOX]

## Generazione di immagini {#generate}

>[!INFO]
>
>Nuove leggi stanno emergendo sulla trasparenza generativa dell’intelligenza artificiale e Adobe sta lavorando per soddisfare i requisiti applicabili in tutte le giurisdizioni. I metadati C2PA sono lo strumento di provenienza utilizzato da Adobe per soddisfare i requisiti di queste normative.

Quando si utilizza l&#39;intelligenza artificiale generativa per creare un&#39;immagine per il contenuto dell&#39;e-mail in [!DNL Journey Optimizer B2B Prime], i metadati C2PA vengono automaticamente allegati all&#39;immagine generata e non è richiesta alcuna azione da parte dell&#39;utente. Gli strumenti di intelligenza artificiale generativi producono un elemento di metadati C2PA combinato per varianti di immagini con metadati esistenti, inclusa la sorgente originale.

>[!NOTE]
>
>[!DNL Journey Optimizer B2B Prime] non supporta attualmente le azioni di modifica manuale delle immagini. I flussi di lavoro dei metadati C2PA per queste azioni non sono al momento applicabili.
