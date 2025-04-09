---
title: Contenuto condizionale
description: Scopri come creare varianti di contenuto e applicare regole condizionali durante la creazione di contenuti e-mail per percorsi di account.
feature: Email Authoring, Content
exl-id: 7a789412-ea52-482f-8dc9-4a1599e85268
source-git-commit: 1351880505fcf656f94dc5d9e383337d83faeff4
workflow-type: tm+mt
source-wordcount: '1347'
ht-degree: 9%

---

# Contenuto condizionale

Il contenuto condizionale consente di adattare il contenuto delle e-mail in base alle regole condizionali. Queste regole vengono definite utilizzando gli attributi di profilo o gli eventi contestuali. Puoi creare regole condizionali nel generatore di regole e memorizzarle per riutilizzarle nei vari percorsi di account.

Per aggiungere contenuto condizionale ai messaggi di posta elettronica, Adobe Journey Optimizer consente di applicare le regole condizionali memorizzate nella libreria _Conditions_. Applica regole condizionali nello spazio di progettazione delle e-mail quando [crei un&#39;e-mail all&#39;interno di un percorso di account](./email-authoring.md).

## Aggiungere contenuto condizionale alle e-mail {#email-content}

>[!CONTEXTUALHELP]
>id="ajo-b2b_conditional_content"
>title="Contenuto condizionale"
>abstract="Utilizza le regole condizionali per creare più varianti di un componente di contenuto. Se non viene soddisfatta alcuna condizione durante l’invio del messaggio, verrà visualizzato il contenuto della variante predefinita."

>[!CONTEXTUALHELP]
>id="ajo-b2b_conditional_rule_select"
>title="Contenuto condizionale"
>abstract="Utilizza una regola condizionale salvata nella libreria o creane una nuova."

Quando crei un’e-mail per il percorso di account nello spazio di progettazione delle e-mail, utilizza le regole condizionali per definire più varianti per un componente di contenuto.

1. Seleziona un componente di contenuto e fai clic sull&#39;icona **[!UICONTROL Abilita contenuto condizionale]** nella barra degli strumenti del componente.

   Il componente è evidenziato in arancione per indicare che è attivato come componente condizionale. Il riquadro **[!UICONTROL Contenuto condizionale]** viene visualizzato a sinistra con _Variante predefinita_ e _Variante - 1.

   ![Abilitare il contenuto condizionale per il componente testo](./assets/conditions-enable.png){width="700" zoomable="yes"}{width=&quot;700&quot; zoomable=&quot;yes&quot;}

   Il contenuto originale selezionato e attivato è quello predefinito e si applica quando nessuna delle regole condizionali è soddisfatta per nessuna delle varianti definite.

   Da questo riquadro è possibile definire più varianti per il componente di contenuto selezionato utilizzando le regole condizionali.

1. Passa il puntatore del mouse sulla prima variante (_Variante - 1_) e fai clic sull&#39;icona _Seleziona condizione_ ( ![Icona condizione](../assets/do-not-localize/icon-select-condition.svg) ).

   ![Seleziona la condizione per la variante](./assets/conditions-variant-select.png){width="700" zoomable="yes"}{width=&quot;700&quot; zoomable=&quot;yes&quot;}

   Viene visualizzata la finestra di dialogo _[!UICONTROL Seleziona condizione]_ in cui è visualizzata la libreria delle condizioni.

   Se si desidera visualizzare i dettagli di una condizione per assicurarsi che sia ciò che si desidera, fare clic sull&#39;icona _Altro menu_ (**...**) e scegliere **[!UICONTROL Visualizza informazioni]**.

   ![Dettagli condizione di accesso alla libreria delle condizioni](assets/conditions-select-dialog.png){width="600" zoomable="yes"}{width=&quot;600&quot; zoomable=&quot;yes&quot;}

   Se la condizione necessaria non esiste, [creare una regola condizionale](#create-condition) facendo clic su **[!UICONTROL Crea nuovo]**.

1. Seleziona la regola condizionale e fai clic su **[!UICONTROL Seleziona]** per associarla alla variante.

   È possibile esaminare la condizione associata facendo clic sull&#39;icona del _menu_ Altro (**...**) relativa alla variante e scegliendo **[!UICONTROL Visualizza condizione]**.

   ![Visualizza la condizione associata alla variante](./assets/conditions-variant-view-condition.png){width="600" zoomable="yes"}{width=&quot;600&quot; zoomable=&quot;yes&quot;}

   Fai clic su X in alto a destra per chiudere la finestra a comparsa.

   ![Visualizza i dettagli per la condizione associata](./assets/conditions-info-popup.png){width="500"}{width=&quot;500&quot;}

1. Per una migliore leggibilità, rinominare la variante facendo clic sull&#39;icona _Altro menu_ (**...**) per la variante e scegliendo **[!UICONTROL Rinomina]**.

   Immetti un nome significativo per la variante che ti aiuti a identificare la variante e il relativo intento.

   ![Rinomina la variante](./assets/conditions-variant-rename.png){width="600" zoomable="yes"}{width=&quot;600&quot; zoomable=&quot;yes&quot;}

1. Con la variante selezionata nel riquadro sinistro, modificare il componente per modificarne l&#39;aspetto nel messaggio di posta elettronica quando la condizione è vera.

   In questo esempio, la variante del componente Testo utilizza una descrizione diversa in base al area geografica del destinatario.

   ![Modifica il componente per la variante](./assets/conditions-variant-component-edit.png){width="600" zoomable="yes"}{width=&quot;600&quot; zoomable=&quot;yes&quot;}

1. Se necessario, definire un&#39;altra variante facendo clic su **[!UICONTROL Aggiungi variante]**.

   Ripeti i passaggi da 2 a 5 per selezionare una condizione, rinominare la variante e modificare il componente per la variante.

   È possibile aggiungere tutte le varianti necessarie per il componente contenuto. Modificare la variante selezionata nel riquadro di sinistra in qualsiasi momento per verificare come appare il componente contenuto per la condizione.

   >[!IMPORTANT]
   >
   >Le contenuto condizionali vengono valutate rispetto alle regole associate nell&#39;ordine in cui sono elencate le varianti. Per il componente viene utilizzata la prima variante con una condizione che restituisce true.
   >
   >Se nessuna delle condizioni di variante definite viene considerata true durante l&#39;invio del messaggio e-mail, il componente contenuto viene visualizzato in base alla **[!UICONTROL variante]** predefinita.

1. Per eliminare una variante, fate clic sull&#39;icona del _menu_ Altro (**...**) relativa alla variante e scegliete **[!UICONTROL Elimina]**.

   Fai clic su **[!UICONTROL Elimina]** nella finestra di dialogo di conferma.

## Regole condizionali

Le regole condizionali sono un insieme di espressioni condizionali che possono essere valutate come true o false. Puoi utilizzare queste regole per determinare quale variante di contenuto visualizzare in un messaggio e-mail in base a vari filtri, ad esempio attributi di profilo o eventi contestuali.

Le regole condizionali vengono memorizzate nella libreria delle condizioni, dove sono disponibili per il riutilizzo in tutto il contenuto del percorso per l’organizzazione.
<!-- 

>[!NOTE]
>
>You need the [Manage Library Items](../administration/ootb-product-profiles.md) permission to save or delete conditional rules. Saved conditions are available for use by all users within an organization. -->

### Filtri condizione {#condition-filters}

| Tipo di condizione | Filtri | Descrizione |
| -------------- | ------- | ----------- |
| **Account** | Attributi account | Attributi del profilo account, tra cui: <li>Entrate annuali</li><li>Città</li><li>Paese</li><li>Dimensione del dipendente</li><li>Settore</li><li>Nome</li><li>Codice SIC</li><li>Stato</li> |
| | [!UICONTROL Filtri speciali] > [!UICONTROL Ha un gruppo di acquisto] | L’account non ha membri di gruppi di acquisto. Può essere valutato anche in base a uno o più dei seguenti criteri: <li>Interesse soluzione</li><li>Stato gruppo acquisti</li><li>Punteggio di completezza</li><li>Punteggio di coinvolgimento</li> |
| | [!UICONTROL Filtri speciali] > [!UICONTROL Ha opportunità] | L’account è o non è correlato a un’opportunità. Può essere valutato anche in base a uno o più dei seguenti attributi di opportunità: <li>Importo<li>Data di chiusura<li>Descrizione<li>Ricavi previsti<li>Trimestre fiscale<li>Anno fiscale<li>Categoria di previsione<li>Nome categoria previsione<li>È chiuso<li>È vinto</li><li>Data dell’ultima attività</li><li>Origine persona<li>Nome</li><li>Passaggio successivo</li><li>Probabilità<li>Quantità<li>Fase</li><li>Tipo |
| **Persona** | [!UICONTROL Cronologia attività] > [!UICONTROL E-mail] | Attività e-mail associate al percorso: <li>[!UICONTROL Collegamento selezionato nell&#39;e-mail]</li><li>Email aperta</li><li>E-mail recapitata</li><li>È stato inviato un messaggio e-mail</li> Queste condizioni vengono valutate utilizzando un messaggio e-mail selezionato in precedenza nel percorso. |
|  | [!UICONTROL Attributi della persona] | Attributi del profilo personale, tra cui: <li>Città</li><li>Paese</li><li>Data di nascita</li><li>Indirizzo e-mail</li><li>E-mail non valida</li><li>E-mail sospesa</li><li>Nome</li><li>Area dello stato dedotta</li><li>Posizione lavorativa</li><li>Cognome</li><li>Numero di cellulare</li><li>Numero di telefono</li><li>CAP</li><li>Stato</li><li>Annulla l&#39;iscrizione</li><li>Motivo per annullamento abbonamento</li> |
| | [!UICONTROL Filtri] speciali > [!UICONTROL iscritto di Buying Group] | La persona è o non è un membro del gruppo di acquisto valutata in base a uno o più dei seguenti criteri: <li>Interesse per la soluzione</li><li>Stato Gruppo di acquisto</li><li>Punteggio di completezza</li><li>Punteggio di coinvolgimento</li><li>Ruolo</li> |

<!-- 

| | [!UICONTROL Activity history] > [!UICONTROL Data Value Changed] | For a selected person attribute, a value change occurred. These change types include: <li>New value</li><li>Previous value</li><li>Reason</li><li>Source</li><li>Date of activity</li><li>Min. number of times</li> |
| | [!UICONTROL Activity history] > [!UICONTROL Had Interesting Moment] | Interesting moment activity that is defined in the associated Marketo Engage instance. Constraints include: <li>Milestone</li><li>Email</li><li>Web</li>|

| | [!UICONTROL Special filters] > [!UICONTROL Member of List] | The person is or is not a member of one or more Marketo Engage lists. |
| | [!UICONTROL Special filters] > [!UICONTROL Member of Program] | The person is or is not a member of one or more Marketo Engage programs. |
|  [People](#add-a-split-path-by-people-node) > [!UICONTROL Account-person attributes only] | Role in account attributes | The person is or is not assigned a role in the account. Optional constraints: <li>Enter a role name</li> | 
-->

### Creare una regola condizionale {#create-condition}

>[!CONTEXTUALHELP]
>id="ajo-b2b_conditions_rule_editor"
>title="Creare una condizione"
>abstract="Combina attributi ed eventi contestuali per creare regole che determinano la variante di contenuto da visualizzare nei messaggi e-mail."

Puoi accedere al generatore di regole condizionali dallo spazio di progettazione delle e-mail quando selezioni una condizione per una variante di componente.

1. Nella finestra di dialogo _[!UICONTROL Seleziona condizione]_, fai clic su **[!UICONTROL Crea nuova]** e scegli il tipo di condizione:

   * **[!UICONTROL Condizione persona]** - Scegliere questo tipo per generare la regola condizionale utilizzando gli attributi persona e gli eventi contestuali.
   * **[!UICONTROL Condizione account]** - Scegliere questo tipo per generare la regola condizionale utilizzando gli attributi dell&#39;account.

   ![Scegliere il tipo di condizione da creare](./assets/conditions-select-create-new.png){width="600" zoomable="yes"}{width=&quot;600&quot; zoomable=&quot;yes&quot;}

1. Crea la regola condizionale in base alle tue esigenze.

   Per ogni attributo o evento che desideri includere nella regola, trascina e rilascia l’elemento nell’area di lavoro della regola. Espandi il filtro e completa l’espressione.

   ![Completare l&#39;espressione per valutare](./assets/conditions-rule-add-attribute.png){width="600" zoomable="yes"}{width=&quot;600&quot; zoomable=&quot;yes&quot;}

   Se includi più di un filtro, imposta la **[!UICONTROL logica filtro]**:

   * **[!UICONTROL Applica tutti i filtri]** - La regola restituisce true se **tutti** i filtri sono true.
   * **[!UICONTROL Applica qualsiasi filtro]**. La regola restituisce true se **any** dei filtri è true.

1. A destra immettere **[!UICONTROL Nome]** e **[!UICONTROL Descrizione]** (facoltativo) per la regola.

   Utilizza un nome significativo e una descrizione utile per aiutare gli altri utenti dell’organizzazione a riutilizzarlo invece di creare un’altra condizione duplicata.

   ![Aggiungi un nome e una descrizione per la regola condizionale](./assets/conditions-rule-name-description.png){width="600" zoomable="yes"}{width=&quot;600&quot; zoomable=&quot;yes&quot;}

1. Al termine della regola condizionale, fare clic su **[!UICONTROL Salva]**.

   La regola condizionale viene salvata nella libreria e puoi selezionarla per la variante corrente. È incluso anche nella libreria per l’utilizzo da parte di qualsiasi altra variante di contenuto dinamico tra percorsi di account.

### Duplicare una regola

Le regole condizionali salvate nella libreria non possono essere modificate. Tuttavia, puoi duplicare una regola esistente e modificarla per crearne una nuova.

1. Fai clic sull&#39;icona _Altro menu_ (**...**) per la variante e scegli **[!UICONTROL Duplica]**.

   Nel generatore di regole viene aperto un duplicato della regola. Utilizza il duplicato come punto di partenza per la regola da generare.

   ![Usa un regola duplicato per creare quello che ti serve](./assets/conditions-rule-duplicate.png){width="600" zoomable="yes"}{width=&quot;600&quot; zoomable=&quot;yes&quot;}

1. Nel generatore di regole, modifica, aggiungi o elimina le condizioni in base alle tue esigenze.

1. Modifica il nome e la descrizione in modo che corrispondano allo scopo o agli elementi nella regola.

1. Al termine della regola condizionale, fare clic su **[!UICONTROL Salva]**.
