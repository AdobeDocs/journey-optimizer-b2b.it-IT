---
title: Punteggio contenuto
description: 'Valuta il contenuto delle e-mail con il punteggio di allineamento del brand: convalida di colori, font, loghi e stile di scrittura in base alle linee guida del brand in Journey Optimizer B2B edition.'
badge: label="Beta" type="Informative"
feature: Content, Brand Identity
role: User
level: Beginner, Intermediate
exl-id: 686d5ce0-c597-48e1-a51f-e91e95a942d5
source-git-commit: 37e4a7976d716f24edf2c2e92cbfa4c149aa66ec
workflow-type: tm+mt
source-wordcount: '755'
ht-degree: 8%

---

# Punteggio del contenuto {#content-scoring}

La valutazione e il punteggio dei contenuti consentono di creare, esaminare e gestire contenuti conformi alle linee guida [definite nel marchio selezionato](./brands-manage-create.md#brand-definitions) e agli standard di qualità generali. L’esecuzione di una valutazione garantisce coerenza in termini di tono, messaggistica e identità visiva in tutte le campagne e-mail, fungendo anche da controllo di qualità prima che il contenuto venga pubblicato.

>[!AVAILABILITY]
>
>È necessario un [contratto utente](https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html){target="_blank"} prima di poter utilizzare le funzionalità basate sull&#39;intelligenza artificiale in Adobe Journey Optimizer B2B edition. Per ulteriori informazioni, contatta il tuo rappresentante Adobe.
>
>Consulta [Autorizzazioni relative al marchio](./brands-overview.md#brand-related-permissions) per informazioni su come gli amministratori di prodotto possono abilitare queste funzioni.

## Eseguire una valutazione

1. Dopo aver creato il contenuto dell&#39;e-mail, fai clic sull&#39;icona _Allineamento marchio_ ( ![Icona Allineamento marchio](../assets/do-not-localize/icon-brand-compliance.svg) ) a destra per aprire il pannello destro _Allineamento marchio_ nell&#39;area di progettazione e-mail.

   Il [marchio predefinito](./brands-manage-create.md#default-brand) è selezionato automaticamente.

   ![Accedere agli strumenti di allineamento del marchio](./assets/brands-alignment-sidebar.png){width="600" zoomable="yes"}

   Puoi fare clic sull&#39;icona _Schermo intero_ ( ![Icona Schermo intero](../assets/do-not-localize/icon-full-screen.svg) ) nella parte superiore del pannello per visualizzare gli strumenti di allineamento del brand in modalità a schermo intero.

1. Se necessario, fare clic sulla freccia del menu **[!UICONTROL Marchio]** (![Freccia giù](../assets/do-not-localize/icon-down-menu.svg) ) per scegliere un altro marchio pubblicato.

1. Fai clic su **[!UICONTROL Valuta punteggio]** per valutare l&#39;allineamento del contenuto con il brand selezionato.

   Il sistema valuta il contenuto in base alle linee guida del brand selezionato e visualizza il punteggio risultante.

   ![Punteggi di valutazione nel pannello di destra](./assets/brands-alignment-evaluation.png){width="600" zoomable="yes"}

## Punteggio di allineamento del brand {#brand-score}

>[!CONTEXTUALHELP]
>id="ajo-b2b_brand_score_overview"
>title="Selezione del brand"
>abstract="Seleziona il tuo brand per assicurarti che i contenuti siano realizzati in conformità con le linee guida, gli standard e l’identità specifici, mantenendo la coerenza e l’integrità del brand."

>[!CONTEXTUALHELP]
>id="ajo-b2b_brand_score"
>title="Punteggio di allineamento del brand"
>abstract="Il punteggio di allineamento del brand misura se il contenuto aderisce alle linee guida del brand per garantire coerenza in termini di colori, font, logo, immagini e stile di scrittura."

>[!CONTEXTUALHELP]
>id="ajo-b2b_brand_colors_score"
>title="Punteggio colori"
>abstract="Punteggio colori"

>[!CONTEXTUALHELP]
>id="ajo-b2b_brand_fonts_score"
>title="Punteggio font"
>abstract="Punteggio font"

>[!CONTEXTUALHELP]
>id="ajo-b2b_brand_logos_score"
>title="Punteggio logo"
>abstract="Punteggio logo"

>[!AVAILABILITY]
>
>Questa funzionalità è attualmente disponibile come versione beta pubblica.

Quando il brand è ben definito e pubblicato, valuta il punteggio di allineamento del brand direttamente all’interno dello spazio di progettazione e-mail per garantire che il contenuto sia allineato alle linee guida del brand:

Il punteggio viene calcolato in base alle violazioni identificate nel contenuto dell’e-mail valutato:

* 100 = Perfetto - Nessuna violazione trovata
* 80-99 = Buono - Solo violazioni minori
* 60-79 = Equo - Alcune violazioni significative
* Inferiore a 60 = Scarso - Violazioni gravi hanno bisogno di attenzione

Puoi esaminare i risultati della valutazione in modo più dettagliato per identificare le violazioni e migliorare i punteggi di allineamento delle categorie (_Alta_, _Medium_ e _Bassa_) e rivedere i dettagli.

Per lo **[!UICONTROL stile scrittura]** o il **[!UICONTROL contenuto visivo]**, fare clic sulla freccia _Espandi_ ( ![Espandi freccia](../assets/do-not-localize/icon-expand-right.svg) ) per visualizzare i dettagli per la valutazione.

![Dettagli di valutazione dell&#39;allineamento del brand](./assets/brands-alignment-evaluation-details.png){width="600" zoomable="yes"}

Fai clic sull&#39;icona _Schermo intero_ ( ![Icona Schermo intero per approfondimenti dettagliati](../assets/do-not-localize/icon-full-screen.svg) ) per visualizzare in dettaglio ogni punteggio di insight.

Seleziona una linea guida segnalata per visualizzare feedback e suggerimenti specifici.

![Dettagli di valutazione dell&#39;allineamento del brand in visualizzazione a schermo intero](./assets/brands-alignment-evaluation-details-full-screen.png){width="700" zoomable="yes"}

È possibile apportare modifiche al contenuto e fare clic su **[!UICONTROL Rivaluta punteggio]** per eseguire un&#39;altra valutazione e verificare la presenza di un risultato migliorato.

## Punteggio qualità contenuto {#quality-score}

>[!CONTEXTUALHELP]
>id="ajo-b2b_quality_score_overview"
>title="Qualità dei contenuti"
>abstract="Valuta la qualità generale dei contenuti per identificare potenziali problemi di leggibilità, coerenza ed efficacia dei contenuti. La valutazione della qualità è indipendente dalle linee guida del tuo marchio."

>[!NOTE]
>
>La valutazione della qualità dei contenuti è indipendente dalle linee guida del brand. Anche se viene selezionato un marchio, le relative linee guida non vengono applicate al controllo di qualità. La selezione del brand è pertinente solo per il punteggio di allineamento del brand.

Oltre all’allineamento del brand, puoi valutare la qualità generale dei contenuti per identificare potenziali problemi di leggibilità, coerenza ed efficacia dei contenuti, indipendentemente dalle linee guida del brand.

Scorri fino alla sezione **[!UICONTROL Qualità del contenuto]** per rivedere approfondimenti sulla qualità e consigli.

![Valutazione della qualità dei contenuti](./assets/content-scoring-quality-insights.png){width="600" zoomable="yes"}

Seleziona qualsiasi elemento contrassegnato per visualizzare feedback specifici e suggerimenti fruibili per il miglioramento. I punteggi si basano sulle seguenti categorie:

* **[!UICONTROL Efficacia di CTA]**: valuta il livello di efficacia del call-to-action nel motivare i lettori a intraprendere l&#39;azione desiderata.
* **[!UICONTROL Oggetto]**: valuta la chiarezza, la rilevanza e la qualità che attira l&#39;attenzione per incoraggiare l&#39;apertura delle e-mail.
* **[!UICONTROL Leggibilità]**: misura la facilità di comprensione del contenuto da parte dei lettori.
* **[!UICONTROL Controllo spam]**: identifica i trigger di posta indesiderata comuni che possono influire sul recapito messaggi.
* **[!UICONTROL Coerenza dei contenuti]**: assicura un flusso fluido dei contenuti e la loro permanenza nell&#39;argomento.
* **[!UICONTROL Correzione]**: verifica la presenza di problemi di ortografia, grammatica e chiarezza.

Fai clic sull&#39;icona _Schermo intero_ ( ![Icona Schermo intero per approfondimenti dettagliati](../assets/do-not-localize/icon-full-screen.svg) ) per una visualizzazione dettagliata del punteggio di qualità.

![Visualizzazione a schermo intero della valutazione della qualità dei contenuti](./assets/content-scoring-quality-full-screen.png){width="700" zoomable="yes"}

In base ai consigli, puoi modificare i contenuti per migliorarne la leggibilità, la coerenza e la qualità complessiva. Fai clic su **[!UICONTROL Rivaluta il punteggio]** dopo aver apportato modifiche per aggiornare il punteggio di qualità.
