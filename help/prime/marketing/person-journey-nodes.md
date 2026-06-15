---
title: Aggiungi nodi Percorso
description: Pagina Segnaposto per i nodi del percorso di persone.
autotag-review: '2026-06-12T23:02:52.147Z'
TQID: 'https://experienceleague.adobe.com/sTnrOvrGIrgboPqOMrrkUvNU1y6zZJX42zEJxuUInKQ'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: a4b836d9-ffdd-4df3-a62a-f78b830cf059
  - id: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2:
  - id: d270a788-eb1d-40ed-b74e-9158ed975b1f
  - id: ba367494-9862-4596-bd6f-299c7e10a46b
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 2f4929e4fadeee87b9e31298d2a1de269fc007d5
workflow-type: tm+mt
source-wordcount: 1137
ht-degree: 2%

---

# Aggiungere nodi di percorso

Dopo aver creato un percorso di persone, aggiungi il pubblico e crea il percorso utilizzando i nodi. La mappa del percorso fornisce un’area di lavoro in cui puoi creare i tuoi casi d’uso di marketing B2B a più passaggi.

Il nodo _[!UICONTROL Pubblico persona]_ è automaticamente il primo nodo del percorso. Dopo aver selezionato il pubblico, crea il percorso combinando i diversi nodi di azione, evento ed eliminazione come uno scenario multi-passaggio tra canali. Ogni nodo di un percorso rappresenta un passo lungo un percorso logico.

## Nodo di pubblico della persona

Il nodo audience persona specifica i record di persona che entrano nel percorso. Quando crei un percorso di persone, il percorso inizia sempre con un nodo del pubblico di persone che ne definisce l’input.

1. Fai clic sul nodo per selezionarlo.
1. Nel pannello delle proprietà del nodo a destra, utilizza una delle seguenti opzioni di input per il nodo del percorso di pubblico della persona:

   * **[!UICONTROL Elenco dinamico]** - Utilizza un elenco di persone dinamico basato su regole. Le regole di elenco vengono valutate in fase di runtime del percorso per qualificare i membri del percorso. Le persone che in seguito vengono escluse dall’elenco dinamico non vengono rimosse dal percorso.

   * **[!UICONTROL Elenco statico]** - Utilizza un elenco statico di persone come membro del percorso. L’appartenenza all’elenco corrente viene valutata in fase di runtime del percorso per qualificare i membri per il percorso. Le persone che vengono successivamente rimosse dall’elenco statico non vengono rimosse dal percorso.

## Nodi azione Persone

In un percorso di persone, utilizza un’azione sulle persone quando desideri applicare una modifica a tutte le persone nel percorso del nodo. Per un percorso di account, questo tipo di nodo può essere utilizzato all’interno del percorso di suddivisione da persone o dal percorso di suddivisione da account.

### Azioni e vincoli

| Azione | Vincoli |
| ------ | ---------- |
| **[!UICONTROL Invia e-mail]** | <li>Crea e-mail <li>Ottimizzazione del tempo di invio (facoltativo) |
| **[!UICONTROL Modifica valore dati]** | <li>Seleziona attributo persona <li>Imposta nuovo valore |

### Aggiungi un nodo azione {#add-an-action-node}

1. Passa alla mappa del percorso.

1. Fai clic sull&#39;icona più ( **+** ) in un percorso e scegli **[!UICONTROL Esegui un&#39;azione]**.

1. Nelle proprietà del nodo a destra, seleziona un’azione dall’elenco e imposta i valori per l’azione.

<!-- ![Person journey node - take an action](./assets/node-take-action-people.png){width="700" zoomable="yes"} -->

+++[!UICONTROL Invia e-mail]

Utilizza questa azione per inviare un messaggio e-mail. Dopo aver creato l&#39;e-mail per il nodo, puoi progettare, personalizzare e visualizzare in anteprima i messaggi e-mail nello spazio di progettazione e-mail (consulta [Authoring e-mail](../content/email-authoring.md)).

<!-- ![Take an action - Send email](./assets/node-action-send-email-from-marketo.png){width="300"} -->

Puoi utilizzare [Ottimizzazione del tempo di invio](../marketing/email-send-time-optimization.md) per personalizzare la tempistica di consegna delle e-mail prevedendo quando è più probabile che ogni profilo sia coinvolto.

<!--
>[!NOTE]
>
>You can use email deduplication in account journeys to ensure that the same email is not sent multiple times to the same email address within a journey. For more information, see [Email deduplication](../content/email-deduplication.md).
-->

+++

+++[!UICONTROL Modifica valore dati]

Utilizzare questa azione per modificare il valore di un attributo di profilo persone nel database. Selezionare l&#39;attributo e quindi impostare il nuovo valore.

<!-- ![Take an action - Update person profile](./assets/node-action-update-person-profile.png){width="300"} -->

+++

## Nodi evento

Aggiungi il nodo _Ascolta un evento_ per spostare il pubblico al passaggio successivo nel percorso in cui si verifica un evento.

### Filtri per eventi Persone

| Filtri | Descrizione |
| ------- | ----------- |
| Cronologia attività > E-mail | Attività e-mail in base a condizioni valutate utilizzando uno o più messaggi e-mail selezionati: <li>Collegamento cliccato nell’e-mail <li>E-mail aperta |
| Cronologia attività > Valore dati modificato | Per un attributo persona selezionato, si è verificata una modifica del valore. Questi tipi di modifica includono: <li>Nuovo valore <li>Valore precedente <li>Motivo <li>Origine <li>Data dell’attività <li> Min numero di volte |

### Aggiungere un nodo evento

1. Passa alla mappa del percorso.

1. Fai clic sull&#39;icona più ( **+** ) in un percorso e scegli **[!UICONTROL Ascolta un evento]**.

1. Nelle proprietà del nodo a destra, scegli **[!UICONTROL Persone]** per il tipo di evento.

   <!-- ![Journey node - listen to events on people](./assets/node-listen-events-people.png){width="700" zoomable="yes"} -->

1. Seleziona un evento dall’elenco.

1. Fai clic su **[!UICONTROL Modifica evento]** e definisci i dettagli dell&#39;evento.

>[!NOTE]
>
>La funzionalità di timeout per Ascolta un nodo evento non funziona al momento e verrà abilitata in una fase successiva.

## Dividere i nodi dei percorsi

Utilizza i nodi suddivisi per segmentare le persone in base alle condizioni definite. Crea percorsi per l’elenco dei tipi di pubblico in base alle condizioni, definisci ogni percorso con nodi di azione ed evento per il segmento, quindi combina i percorsi e continua il percorso.

Un nodo Percorsi suddivisi definisce uno o più percorsi segmentati in base ai filtri delle persone.

<!-- A split based on a people filter is automatically closed with a merge paths node so that all people can move forward to the next step. Split by people paths can include only people actions. These paths cannot be split again and automatically join back. _not currently true_ -->


_&#x200B;**Funzionamento di un percorso suddiviso per nodo persone**&#x200B;_

* La valutazione di ciascun percorso è dall&#39;alto verso il basso. Se una persona corrisponde per il primo e il secondo percorso, procede solo lungo il primo percorso.
* Il nodo supporta la definizione di un percorso _Altre persone_, in cui è possibile aggiungere azioni o eventi per le persone che non corrispondono a uno dei segmenti o percorsi definiti.

### Filtri corrispondenti

Per ogni percorso definito per il nodo, utilizza i seguenti tipi di filtro per far corrispondere le persone in base a una o più condizioni:

* Cronologia attività: puoi definire un percorso in base all’attività della persona in relazione a:

   * Messaggi e-mail
   * Modifica del valore dei dati

* Attributi persona: consente di definire una condizione in base agli attributi di una persona, ad esempio paese, qualifica o appartenenza a un elenco.

### Aggiungere un nodo di percorsi suddivisi

<!--
>[!NOTE]
>
>When you split paths by people, a _Close split paths_ node is automatically inserted to end the split. A split-by-people path allows only _Take an action_ on people nodes.
-->

1. Passa alla mappa del percorso.

1. Fare clic sull&#39;icona più ( **+** ) in un percorso e scegliere **[!UICONTROL Dividi percorsi]**.

   <!-- ![Add journey node - split paths](./assets/add-node-split.png){width="300" zoomable="no"} -->

1. Per definire una condizione applicabile a _[!UICONTROL Percorso 1]_, fare clic su **[!UICONTROL Applica condizione]**.

1. Nell’editor delle condizioni, aggiungi uno o più filtri per definire il percorso di divisione.

   * Trascina e rilascia uno dei filtri persone dalla navigazione a sinistra e completa la definizione della corrispondenza.

   * Ottimizza le condizioni applicando la **[!UICONTROL logica filtro]** nella parte superiore. Scegli di soddisfare tutte le condizioni o una condizione qualsiasi.

     <!-- ![Split path node - conditions person filter logic](./assets/node-split-conditions-people.png){width="700" zoomable="yes"} -->

   * Fai clic su **[!UICONTROL Fine]**.

1. Per aggiungere altri percorsi, fare clic su **[!UICONTROL Aggiungi percorso]** e ripetere i passaggi precedenti per aggiungere le condizioni applicabili al percorso.

   È inoltre possibile etichettare ogni percorso in base a queste condizioni o utilizzare le etichette predefinite.

1. Se necessario, riordinare i percorsi in base alla priorità desiderata per la suddivisione.

   Il filtro dei percorsi viene valutato in ordine decrescente. Ogni persona procede lungo il primo percorso che corrisponde a.

   Fai clic sulle frecce su e giù in alto a destra di ciascuna scheda di percorsi per spostarla in alto o in basso nell’elenco dei percorsi.

   <!-- ![Split path node - reorder paths](./assets/node-split-reorder-paths-people.png){width="500" zoomable="yes"} -->

1. Abilita l&#39;opzione **[!UICONTROL Altre persone]** per aggiungere un percorso predefinito per le persone che non corrispondono ai percorsi definiti.

   Se questa opzione non è abilitata, le persone che non corrispondono a un segmento/percorso definito si spostano oltre la divisione e procedono al passaggio successivo nel percorso.

Dopo aver definito le condizioni per ogni percorso, puoi aggiungere nodi di evento o azione da applicare alle persone presenti in un percorso.

## Unisci percorsi nodi

1. Passa alla mappa del percorso e individua il nodo dei percorsi suddivisi con due o più percorsi.

   Ogni percorso deve avere una combinazione di azioni ed eventi su ogni percorso.

1. Fai clic sull&#39;icona più ( **+** ) alla fine di uno di questi percorsi e scegli **[!UICONTROL Unisci percorsi]** dalle opzioni visualizzate.

   <!-- ![Journey node - merge paths](./assets/node-plus-icon-merge-paths.png){width="400" zoomable="no"} -->

1. Nelle proprietà del nodo a destra, seleziona i percorsi che desideri unire.

   <!-- ![Journey node - merge paths](./assets/node-merge-select-paths.png){width="600" zoomable="yes"} -->

   A questo punto, i percorsi vengono uniti in modo che le persone dei percorsi selezionati si combinino in un singolo percorso che può continuare a progredire attraverso il percorso.

1. Se necessario, puoi annullare l’unione dei percorsi tornando alle proprietà del nodo percorsi unione e deselezionando la casella di controllo per tutti i percorsi che desideri rimuovere.
