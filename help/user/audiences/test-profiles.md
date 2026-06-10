---
title: Profili di test
description: Scopri come creare profili di test da utilizzare con il test e l’anteprima dei contenuti in Journey Optimizer B2B edition.
feature: Audiences
role: Admin
level: Intermediate
autotag-review: '2026-05-29T18:38:56.987Z'
TQID: 'https://experienceleague.adobe.com/7HMk9y8XhI6ONurF341d46oxkWj8dgnUdnWTylUu4pw'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: beb5f4be-cec3-471a-9db6-831a77dd3ac9
  - id: f2da1b69-6919-4386-a5d2-9c7b5c9033db
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
source-git-commit: 59fb0015ada5e28e5575cf57159c9be44bc66f18
workflow-type: tm+mt
source-wordcount: 843
ht-degree: 2%

---

# Profili di test {#test-profiles}

I profili di test sono necessari per [visualizzare in anteprima e verificare il contenuto della pagina di destinazione](../content/landing-pages-create-publish.md#test-landing-page) in Journey Optimizer B2B edition. Puoi definire un set di profili di test creando uno schema, creando il set di dati e caricando un file CSV.

<!--
>[!NOTE]
>
>[!DNL Journey Optimizer B2B Edition] allows testing different variants of your content by previewing it and sending proofs using sample input data uploaded from a CSV or JSON file, or added manually. 
-->

La creazione di un profilo di test è simile alla creazione di profili regolari in [!DNL Adobe Experience Platform]. Per ulteriori informazioni, consulta la [documentazione del profilo cliente in tempo reale](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=it){target="_blank"}.


## Creare uno schema {#create-schema}

Per creare i profili, è innanzitutto necessario creare uno schema in [!DNL Journey Optimizer B2B Edition].

1. Espandi **[!UICONTROL Gestione dati]** nel menu di navigazione a sinistra, seleziona **[!UICONTROL Schemi]**, quindi fai clic su **[!UICONTROL Crea schema]** in alto a destra.

   ![Menu Schemi con pulsante Crea schema](./assets/create-schema.png){width="800" zoomable="yes"}

1. Seleziona **[!UICONTROL Standard]** come opzione di creazione dello schema.

1. Seleziona un tipo di schema, ad esempio **[!UICONTROL Manuale]**, quindi fai clic su **[!UICONTROL Seleziona]**.

   ![Selezione del tipo di schema con opzione di creazione manuale selezionata](./assets/create-schema-options.png){width="500"}

1. Seleziona un tipo di schema, ad esempio **[!UICONTROL Profilo individuale]**, quindi fai clic su **[!UICONTROL Avanti]**.

   ![Selezione del tipo di schema con l&#39;opzione Profilo individuale](./assets/create-schema-individual-profile.png){width="700" zoomable="yes"}

1. Immettere un nome (obbligatorio) e una descrizione (facoltativo) per lo schema e fare clic su **[!UICONTROL Fine]**.

   ![Aggiungi nome e descrizione per lo schema](./assets/create-schema-name-description.png){width="700" zoomable="yes"}

   Viene visualizzata la struttura dello schema, con il pannello _[!UICONTROL Composizione]_ a sinistra.

1. Nella sezione **[!UICONTROL Gruppi di campi]**, fai clic su **[!UICONTROL Aggiungi]** e seleziona i gruppi di campi appropriati.

   Utilizza lo strumento di ricerca per individuare e selezionare il gruppo di campi **[!UICONTROL Dettagli test profilo]**.

   ![Cerca gruppi di campi esistenti e seleziona Dettagli test profilo](./assets/create-schema-field-groups-profile-test-details.png){width="700" zoomable="yes"}

   Al termine, fare clic su **[!UICONTROL Aggiungi gruppi di campi]** per visualizzare l&#39;elenco dei gruppi di campi nella schermata di panoramica dello schema.

   Ripetere questo passaggio per aggiungere altri gruppi di campi da utilizzare per i profili di test, ad esempio **[!UICONTROL Dettagli contatto persona]** e **[!UICONTROL Dettagli contatto lavoro]**.

1. Nell’elenco dei campi, fai clic sul campo che desideri definire come identità primaria.

1. Nel riquadro di destra _[!UICONTROL Proprietà campo]_, controllare le opzioni **[!UICONTROL Identità]** e **[!UICONTROL Identità primaria]** e selezionare uno spazio dei nomi.

   Se desideri che l&#39;identità primaria sia un indirizzo e-mail, scegli lo spazio dei nomi **[!UICONTROL E-mail]**.

   ![Elenco campi schema per la selezione dell&#39;identità primaria](./assets/create-schema-primary-identity.png){width="700" zoomable="yes"}

   Fare clic su **[!UICONTROL Applica]**.

1. Selezionare lo schema e abilitare l&#39;opzione **[!UICONTROL Profilo]** nel riquadro **[!UICONTROL Proprietà schema]**.

   ![Riquadro proprietà schema con opzione di profilo abilitata](assets/create-schema-profile-enable.png){width="700" zoomable="yes"}

1. Fai clic su **[!UICONTROL Salva]**.

Per ulteriori informazioni sulla creazione dello schema, consulta la [documentazione XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/resources/schemas.html#prerequisites){target="_blank"}.

>[!IMPORTANT]
>
>Quando crei o sostituisci un set di dati per l&#39;acquisizione del profilo di test, accertati che allo schema sia applicato il descrittore di identità corretto applicato al campo di identità primaria (`/personID`) per lo spazio dei nomi previsto. Se il descrittore di identità è mancante o non è configurato correttamente, i profili acquisiti in questo set di dati potrebbero non essere contrassegnati come profili di test (`testProfile = true`), anche se il processo di acquisizione viene completato correttamente.
>
>Se i profili di test non vengono contrassegnati correttamente dopo l’acquisizione:
>
>1. Esamina lo schema associato al set di dati.
>1. Verifica che il campo dell’identità primaria presenti il descrittore di identità corretto per il tuo spazio dei nomi.
>1. Se manca il descrittore, aggiorna lo schema per aggiungere il descrittore di identità e riacquisire i dati.

## Creare un set di dati {#create-dataset}

Dopo aver creato lo schema, crea il set di dati utilizzato per importare i profili. Per ulteriori informazioni sulla creazione di set di dati, consulta la [documentazione di Catalog Service](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html#getting-started){target="_blank"}.

1. In _[!UICONTROL Gestione dati]_ nel menu di navigazione a sinistra, seleziona **[!UICONTROL Set di dati]**.

1. In alto a destra, fai clic su **[!UICONTROL Crea set di dati]**.

   ![Menu Set di dati con pulsante Crea set di dati](./assets/create-dataset.png){width="800" zoomable="yes"}

1. Scegli **[!UICONTROL Crea set di dati dallo schema]**.

   ![Crea set di dati dall&#39;opzione dello schema](./assets/create-dataset-options.png){width="500"}

1. Seleziona lo schema creato in precedenza e fai clic su **[!UICONTROL Avanti]**.

1. Scegli un nome e fai clic su **[!UICONTROL Fine]**.

   ![Finestra di dialogo Nome e completamento set di dati](./assets/create-dataset-name.png){width="700" zoomable="yes"}

1. Nel pannello a destra, abilita l&#39;opzione **[!UICONTROL Profilo]**.

## Creare profili di test utilizzando un file CSV {#create-test-profiles-csv}

In [!DNL Adobe Experience Platform] puoi creare profili caricando un file CSV contenente i diversi campi del profilo nel set di dati. Questo è il metodo più semplice.

1. Crea un semplice file CSV utilizzando un software per fogli di calcolo.

1. Aggiungi una colonna per ogni campo obbligatorio.

   Assicurarsi di aggiungere il campo dell&#39;identità primaria (`personID`, ad esempio) e il campo `testProfile` impostato su `true`.

1. Aggiungi una riga per profilo e i valori per ciascun campo.

   ![File CSV con dati del profilo di test di esempio](./assets/test-profile-csv-data-values.png){width="600" zoomable="yes"}

1. Salva il foglio di calcolo come file csv, assicurandoti che le virgole siano utilizzate come separatori.

1. In [!DNL Adobe Experience Platform], passa a **[!UICONTROL Flussi di lavoro]**.

1. Scegli **[!UICONTROL Mappa CSV a schema XDM]** e fai clic su **[!UICONTROL Avvia]**.

   ![Opzione di flusso di lavoro per mappatura CSV su schema XDM](./assets/aep-workflows-data-ingestion.png){width="800" zoomable="yes"}

1. Selezionare il set di dati da utilizzare per l&#39;importazione e fare clic su **[!UICONTROL Avanti]**.

   ![Schermata di selezione del set di dati per l&#39;importazione CSV](./assets/aep-workflows-data-map-csv.png){width="700" zoomable="yes"}

1. Fai clic su **[!UICONTROL Scegli i file]** e seleziona il file CSV, oppure trascina e rilascia il file dal sistema.

   Al termine del caricamento del file, fare clic su **[!UICONTROL Avanti]**.

   ![Caricamento di file e dati di esempio](./assets/aep-workflows-data-map-file-upload.png){width="700" zoomable="yes"}

1. Mappa i campi CSV di origine ai campi dello schema, quindi fai clic su **[!UICONTROL Fine]**.

   ![Interfaccia di mappatura campi CSV con campi di origine e di destinazione](./assets/aep-workflows-data-mapping.png){width="700" zoomable="yes"}

   Viene avviata l’importazione dei dati. Lo stato passa da _Elaborazione_ a _Operazione completata_.

1. In alto a destra, fai clic su **[!UICONTROL Anteprima set di dati]** e verifica che i profili di test aggiunti al set di dati siano corretti.

   ![Anteprima set di dati con profili di test importati](./assets/aep-workflows-data-preview-test.png){width="700" zoomable="yes"}

   I profili di test possono quindi essere utilizzati per [verificare il contenuto della pagina di destinazione](../content/landing-pages-create-publish.md#test-landing-page).

>[!NOTE]
>
>Per ulteriori informazioni sull&#39;importazione di dati CSV, consulta la [documentazione sull&#39;acquisizione dei dati](https://experienceleague.adobe.com/docs/experience-platform/ingestion/tutorials/map-a-csv-file.html#tutorials){target="_blank"}.

<!--
## Create test profiles using API calls {#create-test-profiles-api}

You can also create test profiles via API calls. Learn more in [[!DNL Adobe Experience Platform] documentation](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html){target="_blank"}.

You must use a Profile schema that contains the **[!UICONTROL Profile test details]** field group. The `testProfile` flag is part of this field group.
When creating a profile, make sure you pass the value: `testProfile = true`.

You can also update an existing profile to change its `testProfile` flag to `true`.

Here is an example of an API call to create a test profile:

```bash
curl -X POST \
'https://dcs.adobedc.net/collection/xxxxxxxxxxxxxx' \
-H 'Cache-Control: no-cache' \
-H 'Content-Type: application/json' \
-H 'Postman-Token: xxxxx' \
-H 'cache-control: no-cache' \
-H 'x-api-key: xxxxx' \
-H 'x-gw-ims-org-id: xxxxx' \
-d '{
"header": {
"msgType": "xdmEntityCreate",
"msgId": "xxxxx",
"msgVersion": "xxxxx",
"xactionid":"xxxxx",
"datasetId": "xxxxx",
"imsOrgId": "xxxxx",
"source": {
"name": "Postman"
},
"schemaRef": {
"id": "https://example.adobe.com/mobile/schemas/xxxxx",
"contentType": "application/vnd.adobe.xed-full+json;version=1"
}
},
"body": {
"xdmMeta": {
"schemaRef": {
"contentType": "application/vnd.adobe.xed-full+json;version=1"
}
},
"xdmEntity": {
"_id": "xxxxx",
"_mobile":{
"ECID": "xxxxx"
},
"testProfile":true
}
}
}'
```
-->
