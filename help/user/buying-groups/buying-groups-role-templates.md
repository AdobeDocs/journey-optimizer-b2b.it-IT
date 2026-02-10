---
title: Acquisto di modelli di mansione per gruppi
description: Crea modelli di ruolo con assegnazione automatica condizionale per identificare i responsabili decisionali e le parti interessate per l’acquisto di gruppi in Journey Optimizer B2B edition.
feature: Buying Groups
role: User
exl-id: 9206356e-e9cf-486c-8982-c7d893222413
source-git-commit: bd6dff55621943dc349b47b99f24afefe5b9a514
workflow-type: tm+mt
source-wordcount: '1329'
ht-degree: 4%

---

# Modelli di ruoli del gruppo acquisti

In un mercato B2B, le decisioni di acquisto sono solitamente prese da più individui. Tali persone partecipano al processo decisionale in base al loro ruolo all’interno dell’organizzazione. Crea modelli di ruolo Gruppo acquisti contenenti un gruppo di definizioni di ruolo in base a ciascun tipo di offerta di prodotto o caso di utilizzo dell’account.

![Video](../../assets/do-not-localize/icon-video.svg){width="30"} [Guarda il video introduttivo](#overview-video)

## Accedere e sfogliare i modelli di ruolo

1. Nel menu di navigazione a sinistra, fai clic su **[!UICONTROL Gruppi di acquisto]**.

1. Nella pagina _[!UICONTROL Gruppi di acquisto]_, seleziona la scheda **[!UICONTROL Modelli ruoli]**.

   ![Scheda Modelli ruoli](assets/roles-templates-tab.png){width="800" zoomable="yes"}

   La scheda fornisce un elenco di inventario di tutti i modelli di ruoli esistenti e visualizza le seguenti informazioni in formato colonna:

   * [!UICONTROL Nome]
   * [!UICONTROL Stato]
   * [!UICONTROL Data di creazione]
   * [!UICONTROL Creato da]
   * [!UICONTROL Ultimo aggiornamento]
   * [!UICONTROL Ultimo aggiornamento effettuato da]
   * [!UICONTROL Pubblicato il]
   * [!UICONTROL Pubblicato da]

   Per impostazione predefinita, l&#39;elenco è ordinato in base all&#39;_[!UICONTROL Ultimo aggiornamento]_. Tutti i modelli di ruoli hanno lo stato `Draft` o `Live`.

1. Per filtrare l’elenco per nome, utilizza il campo di ricerca nella parte superiore dell’elenco.

   Immettere i primi caratteri del nome per ridurre l&#39;elenco visualizzato agli elementi corrispondenti.

   ![Modelli di ruoli filtrati per stringa di ricerca](assets/roles-templates-search.png){width="700" zoomable="yes"}

## Creare un modello di ruoli

1. Dalla scheda _[!UICONTROL Modelli ruoli]_, fai clic su **[!UICONTROL Crea modello]** nell&#39;angolo in alto a destra.

1. Nella finestra di dialogo, immetti un **[!UICONTROL Nome]** (obbligatorio) e una **[!UICONTROL Descrizione]** (facoltativo) univoci per il modello.

   ![Finestra di dialogo Crea modello ruoli](assets/roles-template-create-dialog.png){width="400"}

1. Fai clic su **[!UICONTROL Crea]**.

### Aggiungere i ruoli modello

Dopo aver creato il modello, questo viene aperto nell&#39;area di lavoro e viene richiesto di aggiungere i ruoli. Per impostazione predefinita, viene visualizzata la prima scheda ruolo.

Ogni ruolo definito per il modello utilizza un set di filtri, o _condizioni_, per determinare i membri assegnati al ruolo. Utilizzare i tipi di filtro seguenti per definire le condizioni per un ruolo:

| Tipo | Condizione |
| ---- | --------- |
| Attributi della persona | <li>Indirizzo e-mail <li>E-mail non valida <li>E-mail sospesa <li>Numero di fax <li>Nome <li>Area dello stato dedotta <li>Posizione lavorativa <li>Cognome <li>Secondo nome <li>Numero di telefono cellulare <li>Punteggio di coinvolgimento della persona <li>Numero di telefono <li>Codice postale <li>Stato <li>Annulla l&#39;iscrizione <li>Motivo per annullamento abbonamento |
| Filtri speciali | <li>Membro dell&#39;elenco <li>Membro del programma |
| Dati di intento | <li>Intento categoria <li>Intento prodotto <li>Intento parola chiave<br/>[Informazioni sui dati intento](../admin/intent-data.md) |

1. Per la prima scheda ruolo, definisci le proprietà del ruolo.

   * Scegliere il **[!UICONTROL Ruolo gruppo acquisti]** dall&#39;elenco.

     Sei ruoli predefiniti: `Decision Maker`, `Influencer`, `Practitioner`, `Executive Steering Committee`, `Champion` e `Other`. L&#39;elenco include anche i [ruoli personalizzati definiti nell&#39;elenco _Ruoli_](./default-custom-roles.md#custom-roles).

     ![Elenco ruoli gruppo acquisti](./assets/roles-template-create-roles-list.png){width="700" zoomable="yes"}

   * Imposta **[!UICONTROL Ponderazione]** per il ruolo, utilizzato per calcolare il punteggio di coinvolgimento.

     Il valore di ciascuna opzione viene convertito in percentuale per il calcolo del punteggio: [!UICONTROL Trivial] = 20, [!UICONTROL Minor] = 40, [!UICONTROL Normal] = 60, [!UICONTROL Importante] = 80, e [!UICONTROL Vital] = 100.

     Ad esempio, un modello di ruolo con ruoli che utilizzano Vital, Importante e Normale viene quindi convertito come 100/240, 80/240, 60/240.

   * **[!UICONTROL Aggiungi condizioni per l&#39;assegnazione automatica]** - Selezionare questa casella di controllo per aggiungere condizioni per l&#39;assegnazione automatica dei membri al gruppo di acquisto che soddisfano la condizione. Se la casella di controllo non è selezionata, l’aggiunta di condizioni NON è richiesta.

   * **[!UICONTROL Necessario per il punteggio di completezza]** - Selezionare questa casella di controllo per il ruolo se si desidera che sia un requisito per il calcolo di un punteggio di completezza.

1. Fare clic su **[!UICONTROL Aggiungi condizione]** e definire la regola condizionale per il ruolo.

   * Nella finestra di dialogo _[!UICONTROL Condizione]_, espandi l&#39;elenco di **[!UICONTROL Attributi persona]** e individua un attributo che desideri utilizzare per corrispondere al ruolo. Trascinalo a destra e rilascialo nello spazio del filtro.

     ![Attributo trascinamento condizione aggiunta modello ruoli](assets/roles-template-role-attribute.png){width="700" zoomable="yes"}

     >[!NOTE]
     >
     >Se hai dei campi persona personalizzati definiti nello schema del pubblico dell’account in Experience Platform, questi campi sono disponibili per l’utilizzo come attributi persona in determinate condizioni.

   * Utilizza l’attributo per creare un filtro corrispondente utilizzando uno o più valori.

     Nell’esempio seguente, l’attributo Job title viene utilizzato per identificare una corrispondenza per Decision Maker. Qualsiasi valore per il titolo che inizia con `Director` o `Sr Director` restituisce true per la condizione.

     ![Esempio di condizione del modello dei ruoli che utilizza il titolo del processo](assets/roles-template-condition-example-job-title.png){width="700" zoomable="yes"}

   * Se necessario, aggiungi un altro attributo e una condizione che perfeziona ulteriormente i criteri per una corrispondenza al ruolo.

   * Fai clic su **[!UICONTROL Fine]**.

1. Per ogni ruolo aggiuntivo che si desidera includere per il modello, fare clic su **[!UICONTROL Aggiungi un altro ruolo]** e ripetere i passaggi 1 e 2 per definire il ruolo.

   ![Modello ruoli con più ruoli definiti](assets/roles-template-multiple-roles.png){width="700" zoomable="yes"}

>[!BEGINSHADEBOX &quot;Appartenenza all&#39;elenco Marketo Engage&quot;]

In Marketo Engage, _Campagne avanzate_ verifica l&#39;appartenenza ai programmi per assicurarsi che i lead non ricevano e-mail duplicate e non siano membri di più flussi di e-mail contemporaneamente. In Journey Optimizer B2B, puoi verificare la presenza dell’iscrizione all’elenco Marketo Engage come condizione per il modello dei ruoli, in modo da eliminare le duplicazioni nell’iscrizione al gruppo di acquisto e nelle attività di percorso.

Per utilizzare l&#39;appartenenza a un elenco come condizione del ruolo, espandere **[!UICONTROL Filtri speciali]** e trascinare la condizione **[!UICONTROL Membro dell&#39;elenco]** nello spazio del filtro. Quindi completa la definizione del filtro per valutare l’appartenenza a uno o più elenchi Marketo Engage.

![Condizione del modello dei ruoli per l&#39;appartenenza all&#39;elenco di Marketo Engage](assets/roles-template-conditions-member-of-list.png){width="700" zoomable="yes"}
<br/>

>[!NOTE]
>
>**Funzionalità obsolete**</br></br>
>
>Con l&#39;[architettura semplificata](../simplified-architecture.md) per Journey Optimizer B2B edition, il filtro in base all&#39;appartenenza a un elenco o a un programma in un&#39;istanza di Marketo Engage non è supportato.

>[!ENDSHADEBOX]

Le modifiche vengono salvate automaticamente nello stato _Bozza_. Se non sei pronto per pubblicare il modello di ruoli, fai clic sulla freccia sinistra (indietro) nella parte superiore della pagina e torna all&#39;elenco _[!UICONTROL Modelli di ruoli]_.

### Modificare le impostazioni del punteggio di completezza

Per impostazione predefinita, la completezza di un ruolo viene definita come un membro assegnato al ruolo. Se si desidera utilizzare la completezza del gruppo di acquisto come indicatore della fattibilità o del successo <!-- journey decisioning coming later-->, è possibile utilizzare queste impostazioni per allineare il punteggio al numero di membri per ruolo necessario per chiudere un&#39;opportunità.

Ad esempio, la chiusura di un&#39;offerta per la soluzione _X_ richiede l&#39;identificazione e il coinvolgimento di più responsabili delle decisioni di marketing, in quanto la soluzione verrebbe utilizzata da più team di marketing in un&#39;organizzazione. In questo caso, desideri aumentare la soglia per calcolare un gruppo di acquisto _completo_ richiedendo almeno due responsabili delle decisioni di marketing.

Per informazioni dettagliate sul punteggio di completezza e sui calcoli, consulta [Punteggi di completezza](./completeness-scores.md).

1. Nella parte in alto a destra della pagina dei modelli dei ruoli, fare clic su **[!UICONTROL Impostazioni punteggio di completezza]**.

   ![Modello ruoli - pulsante Impostazioni punteggio di completezza](./assets/buying-group-details-edit-roles-completeness-settings.png){width="700" zoomable="yes"}

1. Nella finestra di dialogo, modifica il valore **[!UICONTROL Membri richiesti]** per ogni ruolo definito in base alle esigenze.

   È possibile immettere il valore oppure fare clic su **&amp;plus;** o **−** per aumentare o diminuire il valore.

   ![Modello ruoli - pulsante Impostazioni punteggio di completezza](./assets/buying-group-details-edit-roles-completeness-settings-dialog.png){width="450"}

1. Fai clic su **[!UICONTROL Salva]**.

### Pubblicare il modello di ruoli

Se il modello è pronto per l&#39;uso, fai clic su **[!UICONTROL Pubblica]** in alto a destra.

La pubblicazione del modello imposta lo stato su _Live_ e lo rende disponibile per l&#39;associazione a un interesse per la soluzione. Per pubblicare il modello dei ruoli deve essere presente almeno un ruolo definito.

## Modificare un modello di ruoli bozza

Quando un modello di ruoli si trova nello stato _Bozza_, è possibile continuare a modificare i ruoli definiti. Tutte le modifiche apportate vengono salvate automaticamente.

Modifica le impostazioni nell&#39;intestazione della scheda ruolo, inclusi il ruolo del gruppo di acquisto, la ponderazione, l&#39;assegnazione automatica e il requisito del punteggio di completezza.

![Modifica proprietà ruolo gruppo acquisti](./assets/roles-template-role-properties.png){width="600"}

### Modificare le condizioni per un ruolo

Per modificare la condizione/logica di filtro per uno qualsiasi dei ruoli, fai clic sull&#39;icona _Modifica_ ( ![Icona Modifica](../assets/do-not-localize/icon-edit.svg) ) in alto a destra nella scheda ruolo. Questa azione apre l&#39;area di lavoro _[!UICONTROL Condizioni]_ in cui è possibile modificare un filtro esistente, aggiungerne o rimuoverne uno o modificare la logica del filtro.

### Eliminare una scheda ruolo

Se desideri rimuovere un ruolo dal modello, fai clic sull&#39;icona _Elimina_ ( ![Elimina icona](../assets/do-not-localize/icon-delete.svg) ) nella scheda ruolo.

### Impostare la priorità per i ruoli

È possibile riordinare i ruoli all’interno del modello, che determina la priorità per l’assegnazione dei lead a un ruolo. Sulla destra di ogni scheda ruolo è visualizzato un controller **[!UICONTROL Priority]**. Fai clic sulla freccia _Su_ o _Giù_ a destra per spostare la scheda Ruolo verso l&#39;alto o verso il basso nella priorità.

![Modifica priorità ruolo](./assets/roles-template-role-priority.png){width="700"}

## Eliminare un modello di ruoli

Puoi eliminare un modello di ruoli se si trova nello stato _Bozza_.

1. Selezionare il modello di ruoli dall&#39;elenco per aprirlo.

1. Fai clic su **[!UICONTROL Elimina]** in alto a destra.

   ![Modifica priorità ruolo](./assets/roles-template-delete.png){width="700"}

1. Nella finestra di dialogo, fai clic su **[!UICONTROL Elimina]** per confermare.

## Video di panoramica

>[!VIDEO](https://video.tv.adobe.com/v/3433079/?learn=on)
