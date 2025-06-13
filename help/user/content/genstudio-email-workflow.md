---
title: Creazione di contenuti e-mail con GenStudio for Performance Marketing
description: Scopri come effettuare l’integrazione con i flussi di lavoro di GenStudio per semplificare la progettazione dell’esperienza e-mail.
feature: Email Authoring, Content, Integrations
topic: Content Supply Chain
level: Intermediate
role: User
badge: label="Disponibilità limitata" type="Informative"
exl-id: 13f45e8f-9d49-4ec2-90ef-689475c629f1
source-git-commit: 82bfb3b425bc7a3931b5ce8b925b860ef70d11fe
workflow-type: tm+mt
source-wordcount: '786'
ht-degree: 8%

---

# Creazione di contenuti e-mail con GenStudio for Performance Marketing {#genstudio-workflow}

>[!CONTEXTUALHELP]
>id="ajo-b2b_genstudio_button"
>title="Utilizzare un modello creato con GenStudio"
>abstract="Utilizza l’integrazione diretta con Adobe GenStudio for Performance Marketing per importare un modello GenStudio ottimizzato con la tecnologia dell’intelligenza artificiale di Adobe."

>[!AVAILABILITY]
>
>L’integrazione di GenStudio in [!DNL Adobe Journey Optimizer B2B Edition] attualmente non può essere utilizzata con le offerte che includono il componente aggiuntivo **Healthcare Shield** o **Privacy and Security Shield**.
>
>Questa integrazione è disponibile solo per il canale e-mail.

Per migliorare l’efficienza del flusso di lavoro e mantenere la coerenza del marchio, puoi combinare le esperienze di GenStudio for Performance Marketing con l’orchestrazione e-mail di Adobe Journey Optimizer B2B edition. Questo flusso di lavoro esteso consente di sfruttare gli strumenti di creazione dei contenuti basati sull’intelligenza artificiale di GenStudio per espandere e massimizzare le comunicazioni e-mail tramite i percorsi di account.

Ad esempio, un esperto di marketing tecnico che utilizza Journey Optimizer B2B edition per sviluppare e automatizzare comunicazioni e-mail per account chiave può collaborare con un esperto di marketing delle prestazioni che crea contenuti utilizzando GenStudio. Con questo flusso di lavoro, entrambi possono collaborare per combinare contenuti on-brand da GenStudio all’automazione del marketing basata sull’account Journey Optimizer B2B edition, fornendo e-mail coinvolgenti mirate a gruppi di acquisto specifici e incentivando le vendite.

>[!BEGINSHADEBOX]

## Funzionalità di generazione dei contenuti GenStudio

[Adobe GenStudio for Performance Marketing](https://business.adobe.com/it/products/genstudio-for-performance-marketing.html){target="_blank"} è un&#39;applicazione IA-first generativa che consente ai team di marketing di creare annunci ed e-mail personalizzati e di grande impatto, conformi agli standard del marchio e ai criteri aziendali. Sfruttando la tecnologia di intelligenza artificiale Adobe, fornisce una suite completa di strumenti che semplificano le complessità della creazione e della gestione dei contenuti in modo che i creativi possano concentrarsi sull’innovazione.

![Video](../../assets/do-not-localize/icon-video.svg){width="30"} [Crea e-mail marketing sul marchio](https://experienceleague.adobe.com/it/docs/genstudio-for-performance-marketing-learn/tutorials/creating-experiences/creating-on-brand-emails){target="_blank"}

Ulteriori informazioni sulle funzionalità di GenStudio for Performance Marketing nella [documentazione](https://experienceleague.adobe.com/it/docs/genstudio-for-performance-marketing/user-guide/home){target="_blank"}

>[!ENDSHADEBOX]

## Esporta HTML da Journey Optimizer B2B edition

In primo luogo, in Journey Optimizer B2B edition, esporta HTML da un’e-mail che include le linee guida del tuo marchio.

1. In Journey Optimizer B2B edition, accedi al contenuto dell’e-mail nello spazio di progettazione visiva.

1. Dal menu _[!UICONTROL Altro ...]_ nella parte superiore dello spazio di progettazione delle e-mail, scegli **[!UICONTROL Esporta HTML]**.

   ![Fare clic su Altro e scegliere Esporta HTML](./assets/email-export-html.png){width="600"}

   Questa azione genera un file .zip scaricato contenente i file HTML e i file immagine.

## Utilizzare il HTML esportato in GenStudio for Performance Marketing

GenStudio for Performance Marketing riconosce alcuni elementi all’interno del HTML e-mail importato quando sono identificati con un nome di campo riconosciuto. Aggiungi i nomi dei campi nel HTML esportato utilizzando la sintassi Handlebars in cui è necessario GenStudio for Performance Marketing per generare un determinato tipo di contenuto.

| Campo | Content type (Tipo di contenuto) |
| ----------------- | ------------------------- |
| `{{pre_header}}` | Preheader |
| `{{headline}}` | Titolo |
| `{{sub_headline}}` | Sottotitolo |
| `{{body}}` | Corpo del testo |
| `{{cta}}` | Call to action (pulsante) |
| `{{image}}` | Immagine |
| `{{link}}` | Call to action sull&#39;immagine |

### Creare il modello

Utilizza il file HTML per creare un modello in GenStudio for Performance Marketing.

Per informazioni dettagliate sul caricamento di un modello di HTML in GenStudio in Adobe GenStudio for Performance Marketing, consulta [Aggiungere un modello](https://experienceleague.adobe.com/it/docs/genstudio-for-performance-marketing/user-guide/content/templates/use-templates#add-a-template) nella documentazione di GenStudio for Performance Marketing.

Quando carichi il HTML esportato come modello, GenStudio for Performance Marketing analizza il file HTML per individuare i campi riconosciuti. Utilizza l’anteprima per rivedere gli elementi del modello e confermare che li hai identificati correttamente con i nomi dei campi riconosciuti.

### Generare esperienze e-mail

In GenStudio for Performance Marketing, utilizza il modello per creare diverse varianti di esperienza e-mail e salvarle.

Per informazioni dettagliate sulla generazione di esperienze e-mail con marchio, consulta [Creare un&#39;esperienza e-mail](https://experienceleague.adobe.com/it/docs/genstudio-for-performance-marketing/user-guide/create/create-email-experience) nella documentazione di GenStudio for Performance Marketing.

## Aggiungere esperienze e-mail generate a Journey Optimizer B2B edition

>[!NOTE]
>
>L’integrazione GenStudio for Performance Marketing è disponibile solo per la creazione di e-mail e non per la creazione di modelli e-mail.

Per utilizzare le varianti e-mail di GenStudio create dal file di HTML e-mail di Journey Optimizer B2B edition esportato, effettua le seguenti operazioni:

1. In Journey Optimizer B2B edition, [aggiungi un&#39;e-mail](./add-email.md) a un percorso di account utilizzando un nodo _[!UICONTROL Esegui un&#39;azione]_.

   * Per l&#39;azione _[!UICONTROL sulla destinazione]_, scegliere **[!UICONTROL Persone]**.

   * Per _[!UICONTROL Azione sulle persone]_, scegli **[!UICONTROL Invia e-mail]**.

     ![Esegui un&#39;azione - invia un&#39;e-mail](./assets/journey-node-send-email.png){width="700" zoomable="yes"}

   * Per _[!UICONTROL Origine e-mail]_, scegli **[!UICONTROL Crea nuova e-mail]** per creare l&#39;e-mail in modo nativo in Journey Optimizer B2B edition.

1. Nella pagina _Crea e-mail_, seleziona **[!UICONTROL Importa HTML]**.

1. Nella finestra di dialogo _[!UICONTROL Importa e-mail]_, fai clic su **[!UICONTROL Adobe GenStudio for Performance Marketing]**.

   ![Importa HTML da GenStudio for Performance Marketing](./assets/email-import-html-genstudio.png){width="500" zoomable="yes"}

1. Sfoglia le esperienze pubblicate.

   Puoi filtrare le esperienze in base a diversi criteri, ad esempio _Modello_ e _Creato da_.

   ![Importa HTML da GenStudio for Performance Marketing](./assets/email-import-select-gen-studio-experience.png){width="600" zoomable="yes"}

1. Seleziona un&#39;esperienza e fai clic su **[!UICONTROL Utilizza]** per iniziare a creare il contenuto delle e-mail.

   >[!NOTE]
   >
   >Le esperienze GenStudio create da un modello Journey Optimizer B2B edition o Marketo Engage vengono importate direttamente nello spazio di progettazione e-mail. Le esperienze create senza un modello Journey Optimizer B2B edition vengono importate in modalità di compatibilità.

1. Utilizza i [contenuti e-mail e strumenti di personalizzazione](./email-authoring.md) per modificare l&#39;e-mail in base alle esigenze e salvarla.

   ![Importa HTML da GenStudio for Performance Marketing](./assets/email-imported-experience.png){width="800" zoomable="yes"}
