---
title: Gestione campi XDM
description: Utilizza la gestione dei campi XDM per controllare i dati disponibili per Journey Optimizer B2B edition.
feature: Data Management, Integrations
role: User
badgeBeta: label="Beta" type="informative" tooltip="Questa funzione è attualmente in versione beta limitata"
source-git-commit: 046d3648c5e482a69719d0095c297a766dd852ea
workflow-type: tm+mt
source-wordcount: '989'
ht-degree: 1%

---


# Gestione dei campi XDM

I campi Experience Data Model (XDM) sono elementi dello schema che forniscono dati all&#39;applicazione [!DNL Journey Optimizer B2B Edition]. Utilizza i campi XDM come filtri e vincoli in percorsi, gruppi di acquisto e funzioni, come la personalizzazione e-mail e il contenuto condizionale.

Gli schemi definiscono i campi in base alle classi XDM standard. Le classi XDM standard includono Profilo individuale, Account aziendale ed Evento esperienza. Gli schemi relazionali definiscono inoltre campi che consentono di modellare i dati strutturati in modo simile ai database relazionali tradizionali.

Gli schemi di Adobe Experience Platform (AEP) in genere contengono molti campi in gerarchie complesse. L’attraversamento degli alberi dello schema XDM richiede tempo. La gestione dei campi XDM semplifica la selezione dei campi visualizzando solo i campi rilevanti per ciascun percorso. Gli amministratori controllano quali campi vengono visualizzati dai creatori del percorso. Gli amministratori impostano inoltre i campi in sola lettura o modificabili. Queste azioni migliorano l&#39;efficienza durante la progettazione del percorso.

Gli amministratori che conoscono XDM e collaborano con data engineer o con le parti interessate alla modellazione dati di Customer Data Platform (CDP) B2B devono utilizzare le procedure riportate in questa pagina.

>[!NOTE]
>[Gli schemi relazionali](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/schema/relational#) sono disponibili per [!DNL Journey Optimizer B2B Edition] come versione limitata. Data Mirror e gli schemi relazionali sono disponibili per i titolari di licenze per campagne Journey Optimizer Orchestrated. Gli schemi relazionali sono disponibili anche come versione limitata per gli utenti di Customer Journey Analytics, a seconda della licenza e dell’abilitazione della funzione. Contatta il tuo rappresentante Adobe per accedere.

## Accedere alle classi XDM

1. Nel menu di navigazione a sinistra, scegli **[!UICONTROL Amministrazione]** > **[!UICONTROL Configurazione]**.

1. Fai clic su **[!UICONTROL Classi XDM]** nel pannello intermedio.

   * Utilizza le schede **[!UICONTROL Standard]** e **[!UICONTROL Relazionale]** per aggiungere nuovi campi e renderli disponibili in Journey Optimizer B2B edition.

   * Utilizza la scheda **Eventi** per [selezionare eventi esperienza AEP specifici e i campi associati](./configure-aep-events.md) da utilizzare per i nodi evento di percorso.

## Selezioni campi

>[!IMPORTANT]
>
>È possibile aggiornare la selezione dei campi in qualsiasi momento selezionando nuovi campi o deselezionando i campi non più necessari. Quando pubblichi un percorso utilizzando questo schema, blocchi la struttura dello schema. L’eliminazione o la ridenominazione dello schema, l’aggiunta di nuovi campi o la modifica dei tipi di campo non sono supportate e potrebbero verificarsi errori di percorso.

Per effettuare le selezioni dei campi, attenersi alla seguente linea guida:

* Puoi aggiungere nuovi campi solo dopo che uno schema è utilizzato attivamente in un percorso.
* L’eliminazione, la ridenominazione o la modifica dei tipi di campo possono causare problemi di funzionalità del percorso. Presta attenzione durante la manipolazione degli schemi.
* Non rinominare o eliminare schemi o modificare le chiavi negli schemi relazionali.

### Classi standard

Nella scheda _[!UICONTROL Standard]_ è possibile modificare _Campi gestiti_ e _Campi aggiornabili_ per le classi standard:

* I campi gestiti vengono visualizzati in percorsi, gruppi di acquisto e funzioni di personalizzazione.
* I campi aggiornabili fungono da vincoli per i nodi di percorso _Aggiorna profilo account_ e _Aggiorna profilo persona_.

![Scheda Classi standard che mostra la configurazione della classe XDM](assets/xdm-standard.png){width="600" zoomable="yes"}

L’elenco include due classi:

* **[!UICONTROL Profilo individuale XDM]**
* **[!UICONTROL Account aziendale XDM]**

Le informazioni sulla classe visualizzate includono:

* Numero di campi gestiti
* Numero di campi aggiornabili
* Ora ultimo aggiornamento

Per selezionare i campi dallo schema di unione per le classi XDM standard, fai clic sul nome della classe per aprire la finestra di dialogo di selezione _Campi gestiti_ oppure fai clic sull&#39;icona _Altro menu_ ( **...** ) per scegliere tra _[!UICONTROL Campi gestiti]_ e _[!UICONTROL Campi aggiornabili]_.

![Fare clic sull&#39;icona Altro per scegliere tra campi gestiti e campi aggiornabili](./assets/xdm-classes-standard-more-menu.png){width="550" zoomable="yes"}

>[!NOTE]
>
>Un campo deve essere _Gestito_ prima di poter essere _Aggiornabile_. I _campi aggiornabili_ selezionati devono esistere nello schema fornito dall&#39;utente.

#### Campi gestiti

Quando si sceglie **[!UICONTROL Campi gestiti]**, nella finestra di dialogo _Seleziona campi_ sono elencati tutti i campi configurabili.

1. Seleziona fino a 100 campi per ogni classe XDM.

   Utilizza il campo _[!UICONTROL Ricerca]_ per filtrare l&#39;elenco visualizzato in base al nome. Utilizza il cursore **[!UICONTROL Mostra solo campi selezionati]** per rivedere le selezioni correnti.

   ![Finestra di dialogo per la selezione dei campi gestiti per le classi XDM standard che visualizzano le opzioni dei campi configurabili](assets/xdm-standard-managed-fields.png){width="450" zoomable="yes"}

1. Fai clic su **[!UICONTROL Salva]** per confermare le tue selezioni.

#### Campi aggiornabili

Quando si sceglie **[!UICONTROL Campi aggiornabili]**, la finestra di dialogo _Seleziona campi_ consente di scegliere campi da altre origini dati.

1. Per **[!UICONTROL Set di dati]**, selezionare l&#39;origine dati che si desidera configurare.
1. Modifica i campi dal set di dati selezionato.

   ![Finestra di dialogo per selezionare campi aggiornabili dai set di dati nella configurazione dello schema XDM](./assets/xdm-select-updateable.png){width="450" zoomable="yes"}

1. Fai clic su **[!UICONTROL Salva]** per applicare le modifiche.

### Schemi relazionali

Gli schemi relazionali consentono di creare classi di dati personalizzate. Con l’accesso a più set di dati, puoi creare classi personalizzate in base alle tue esigenze di dati. Utilizza gli schemi relazionali per le entità business, ad esempio acquisti, licenze e registrazioni di eventi, nelle decisioni del percorso e nella personalizzazione e-mail. Puoi selezionare fino a 50 schemi e 100 campi per schema.

>[!NOTE]
>
>Questa funzione supporta attualmente casi di utilizzo di oggetti personalizzati relativi all’account, con piani per supportare più casi di utilizzo di oggetti preconfigurati in futuro.

Puoi creare schemi relazionali utilizzando l&#39;editor schema (vai a **[!UICONTROL Gestione dati]** > **[!UICONTROL Schemi]** nel menu di navigazione a sinistra).

Durante la creazione di uno schema da utilizzare con [!DNL Journey Optimizer B2B Edition], sono necessari i seguenti valori di configurazione:

* Comportamento: record
* Segmentazione: abilitata
* Tipo di relazione: molti-a-uno
* Schema di riferimento: account B2B
* Campi obbligatori: chiave primaria, chiave esterna e descrittore di versione
* Set di dati associato: definito e mappato allo schema

Per selezionare i campi dello schema relazionale da utilizzare in [!DNL Journey Optimizer B2B Edition]:

1. Seleziona la scheda **[!UICONTROL Relazionale]** per visualizzare gli schemi.

   ![Scheda Schemi relazionali nell&#39;Editor schema che mostra i campi dell&#39;entità business per Adobe Journey Optimizer B2B edition](assets/xdm-relational.png){width="600" zoomable="yes"}

1. Fai clic su **[!UICONTROL Seleziona schema XDM relazionale]**.

   >[!NOTE]
   >
   >In questa versione beta sono supportati solo _Oggetti personalizzati account molti-a-uno_.

1. Seleziona uno schema relazionale e fai clic su **[!UICONTROL Avanti]**.

   >[!NOTE]
   >
   >In questa versione beta non è possibile rimuovere uno schema dall’elenco dopo averlo selezionato.

   ![Selezionare uno schema relazionale nella finestra di dialogo](./assets/xdm-classes-relational-select-schema-dialog.png){width="500" zoomable="yes"}

1. Inserisci uno spazio dei nomi o utilizza lo spazio dei nomi predefinito. Fai clic su **[!UICONTROL Avanti]**.

   È possibile impostare lo spazio dei nomi una sola volta e non è possibile annullare questa azione.

   ![Spazio dei nomi predefinito nella finestra di dialogo Crea spazio dei nomi](./assets/xdm-classes-relational-create-namespace.png){width="400" zoomable="yes"}

1. Esamina i campi dello schema relazionale.

   Fai clic sull&#39;icona _Info_ ![Info](../assets/do-not-localize/icon-info-light.svg) per visualizzare i metadati del campo.

1. Seleziona i campi da abilitare per percorsi e personalizzazione.

   La piattaforma seleziona automaticamente i seguenti campi obbligatori:

   * Chiave esterna
   * Chiave primaria
   * Descrittore versione

   Utilizza il campo _[!UICONTROL Ricerca]_ per filtrare l&#39;elenco visualizzato in base al nome. Utilizza il cursore **[!UICONTROL Mostra solo campi selezionati]** per rivedere le selezioni correnti.

   ![Selezionare i campi per lo schema relazionale nella finestra di dialogo](./assets/xdm-classes-relational-select-schema-fields.png){width="500" zoomable="yes"}

1. Fai clic su **[!UICONTROL Salva]**.
