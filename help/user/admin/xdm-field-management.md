---
title: Gestione campi XDM
description: Utilizza la gestione dei campi XDM per controllare i dati disponibili per Journey Optimizer B2B edition.
feature: Data Management, Integrations
role: User
badgeBeta: label="Beta" type="informative" tooltip="Questa funzione è attualmente in versione beta limitata"
source-git-commit: de7f5620556a48fe6f12ed1c70e925e11ec770f1
workflow-type: tm+mt
source-wordcount: '1027'
ht-degree: 1%

---


# Gestione dei campi XDM

I campi Experience Data Model (XDM) sono elementi dello schema che forniscono dati all&#39;applicazione [!DNL Journey Optimizer B2B Edition]. Utilizza i campi XDM come filtri e vincoli in percorsi, gruppi di acquisto e funzioni, come la personalizzazione e-mail e il contenuto condizionale.

Gli schemi definiscono i campi in base alle classi XDM standard. Le classi XDM standard includono Profilo individuale, Account aziendale ed Evento esperienza. Gli schemi relazionali definiscono inoltre campi che consentono di modellare i dati strutturati in modo simile ai database relazionali tradizionali.

Gli schemi di Adobe Experience Platform (AEP) in genere contengono molti campi in gerarchie complesse. L’attraversamento degli alberi dello schema XDM richiede tempo. La gestione dei campi XDM semplifica la selezione dei campi visualizzando solo i campi rilevanti per ciascun percorso. Gli amministratori controllano quali campi vengono visualizzati dai creatori del percorso. Gli amministratori impostano inoltre i campi in sola lettura o modificabili. Queste azioni migliorano l&#39;efficienza durante la progettazione del percorso.

Gli amministratori che conoscono XDM e collaborano con data engineer o con le parti interessate alla modellazione dati di Customer Data Platform (CDP) B2B seguono le procedure descritte in questa guida.

>[!NOTE]
>[Gli schemi relazionali](https://experienceleague.adobe.com/it/docs/experience-platform/xdm/schema/relational#) sono disponibili per [!DNL Journey Optimizer B2B Edition] come versione limitata. Data Mirror e gli schemi relazionali sono disponibili per i titolari di licenze per campagne Journey Optimizer Orchestrated. Gli schemi relazionali sono disponibili anche come versione limitata per gli utenti di Customer Journey Analytics, a seconda della licenza e dell’abilitazione della funzione. Contatta il tuo rappresentante Adobe per accedere.

## Accesso alle classi XDM

Per aprire l&#39;area di gestione campi XDM, passa a **Configurazioni** > CONFIGURAZIONE > **Classi XDM**.

* Puoi aggiungere nuovi campi solo dopo che uno schema è utilizzato attivamente in un percorso.
* L’eliminazione, la ridenominazione o la modifica dei tipi di campo possono causare problemi di funzionalità del percorso. Presta attenzione durante la manipolazione degli schemi.
* Non rinominare o eliminare schemi o modificare le chiavi negli schemi relazionali.

>[!IMPORTANT]
>È possibile aggiornare la selezione dei campi in qualsiasi momento selezionando nuovi campi o deselezionando i campi non più necessari. Dopo aver pubblicato un percorso utilizzando questo schema, la struttura dello schema viene bloccata. L’eliminazione o la ridenominazione dello schema, l’aggiunta di nuovi campi o la modifica dei tipi di campo non sono supportate e potrebbero verificarsi errori di percorso.

## Classi standard

Nella scheda Classi standard è possibile modificare _Campi gestiti_ e _Campi aggiornabili_.

* I campi gestiti vengono visualizzati in percorsi, gruppi di acquisto e funzioni di personalizzazione.
* I campi aggiornabili fungono da vincoli per i nodi di percorso _Aggiorna profilo account_ e _Aggiorna profilo persona_.

![Scheda Classi standard che mostra i campi gestiti e aggiornabili per la configurazione della classe XDM](assets/xdm-standard.png){width="600" zoomable="yes"}

Per selezionare i campi dallo schema di unione per le classi XDM standard, effettua le seguenti operazioni:

1. Vai a **Amministrazione** > **Configurazioni** > **Classi XDM**.
1. Apri la scheda **Standard**. Scegliere una delle seguenti classi:

   * Profilo individuale XDM
   * Account aziendale XDM

Nella tabella vengono visualizzate le seguenti informazioni:

* Numero di campi gestiti
* Numero di campi aggiornabili
* Ora ultimo aggiornamento

Fare clic sul nome della classe per aprire la finestra di dialogo di selezione _Campi gestiti_.

![Finestra di dialogo per la selezione dei campi gestiti per le classi XDM standard che visualizzano le opzioni dei campi configurabili](assets/xdm-standard-managed-fields.png){width="600" zoomable="yes"}

1. Fare clic sul menu **...** per passare da _[!UICONTROL Campi gestiti]_ a _[!UICONTROL Campi aggiornabili]_. La finestra di dialogo elenca tutti i campi configurabili.
1. Seleziona fino a 100 campi per ogni classe XDM.
1. Fai clic su **[!UICONTROL Salva]** per confermare le tue selezioni.

Utilizza il filtro [!UICONTROL Mostra solo campi selezionati] per visualizzare solo i campi attivi.

Per _Campi aggiornabili_, è possibile accedere a una finestra di dialogo separata che consente di scegliere campi da altre origini dati:

1. Nel menu a discesa Set di dati, seleziona l’origine dati da configurare.
1. Modifica i campi dal set di dati selezionato.
1. Fai clic su **[!UICONTROL Salva]** per applicare le modifiche.

![Finestra di dialogo per selezionare campi aggiornabili dai set di dati nella configurazione dello schema XDM](assets/xdm-select-updateable.png){width="600" zoomable="yes"}

Il campo deve essere _Gestito_ prima di poter essere _Aggiornabile_. I _campi aggiornabili_ selezionati devono esistere nello schema fornito dall&#39;utente.

## Schemi relazionali

Gli schemi relazionali consentono di creare classi di dati personalizzate. Con l’accesso a più set di dati, puoi creare classi personalizzate in base alle tue esigenze di dati.
Utilizza gli schemi relazionali per le entità business, ad esempio acquisti, licenze e registrazioni di eventi, nelle decisioni del percorso e nella personalizzazione e-mail. Puoi selezionare fino a 50 schemi e 100 campi per schema.

![Scheda Schemi relazionali nell&#39;Editor schema che mostra i campi dell&#39;entità business per Adobe Journey Optimizer](assets/xdm-relational.png)

>[!NOTE]
>Questa funzione supporta attualmente i casi di utilizzo di oggetti personalizzati relativi all’account, con l’intenzione di supportare in futuro altri casi di utilizzo di oggetti preconfigurati.

Crea schemi relazionali utilizzando l&#39;Editor di schema in **Gestione dati** > **Schemi**.

I seguenti valori di configurazione devono essere inclusi durante la creazione di uno schema da utilizzare con [!DNL Journey Optimizer B2B Edition]:

* Comportamento: record
* Segmentazione: abilitata
* Tipo di relazione: molti-a-uno
* Schema di riferimento: account B2B
* Campi obbligatori: chiave primaria, chiave esterna e descrittore di versione
* Set di dati associato: definito e mappato allo schema

### Creare uno schema relazionale

Per selezionare i campi da utilizzare in [!DNL Journey Optimizer B2B Edition], eseguire la procedura seguente:

1. Vai a **Amministrazione** > **Configurazioni** > **Classi XDM**.
1. Apri la scheda **Relazionale** per visualizzare gli schemi.
1. Fai clic su **[!UICONTROL Seleziona schema XDM relazionale]**.

   * Nella versione beta, sono supportati solo _oggetti personalizzati account molti-a-uno_.

1. Seleziona uno schema relazionale e fai clic su **[!UICONTROL Avanti]**.

   * Nella versione beta non è possibile rimuovere uno schema dall’elenco dopo averlo selezionato.

1. Inserisci uno spazio dei nomi o utilizza lo spazio dei nomi predefinito. Fai clic su **[!UICONTROL Avanti]**.

   * È possibile impostare lo spazio dei nomi una sola volta e non è possibile annullare questa azione.

1. Esamina i campi dello schema relazionale. Fai clic sull&#39;icona ![Info](../assets/do-not-localize/icon-info-light.svg) [!UICONTROL Info] per visualizzare i metadati del campo.
1. Seleziona i campi da abilitare per percorsi e personalizzazione. La piattaforma seleziona automaticamente i seguenti campi obbligatori:

   * Chiave esterna
   * Chiave primaria
   * Descrittore versione

1. Utilizza il cursore [!UICONTROL Mostra solo campi selezionati] per visualizzare l&#39;anteprima delle selezioni.
1. Filtra i campi per nome utilizzando la barra di ricerca.
1. Fai clic su **[!UICONTROL Salva]**.

## Eventi

Utilizza Eventi di esperienza e i campi associati nelle decisioni del percorso. Puoi selezionare fino a 50 eventi e fino a 100 campi per evento.

![Scheda Eventi che mostra i campi di selezione e schema degli Eventi esperienza per percorsi e personalizzazione](assets/xdm-events.png){width="700" zoomable="yes"}

Fai clic sul nome di un evento per visualizzare i dettagli e modificare i campi configurati.

Per selezionare Eventi esperienza e campi schema, segui la procedura riportata di seguito:

1. Vai a **Amministrazione** > **Configurazioni** > **Classi XDM**.
1. Apri la scheda **Eventi**.
1. Per selezionare i campi per un evento, fare clic su **[!UICONTROL Seleziona evento esperienza]**.
1. Nella pagina Dettagli fare clic su **[!UICONTROL Seleziona tipo di evento]**.
1. Dall’elenco Evento, scegli l’evento.
1. Fai clic su **[!UICONTROL Seleziona]** per chiudere la finestra di dialogo.

   * Nella versione beta, non è possibile rimuovere gli eventi selezionati.

1. Fare clic su **[!UICONTROL Seleziona campi]**.
1. Utilizza il cursore [!UICONTROL Mostra solo campi selezionati] per visualizzare le selezioni correnti.
1. Selezionare i campi da utilizzare in [!DNL Journey Optimizer B2B Edition]. Fai clic su **[!UICONTROL Seleziona]** per chiudere la finestra di dialogo.
1. Fai clic su [!UICONTROL Salva].
