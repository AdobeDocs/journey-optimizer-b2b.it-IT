---
title: Percorsi persona
description: Pagina Segnaposto per percorsi di persone.
autotag-review: '2026-06-12T23:03:17.139Z'
TQID: 'https://experienceleague.adobe.com/MhkAuypbebo-n9uwxFPUKbNgyHijaTnaVsqhs9-lXC0'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: a4b836d9-ffdd-4df3-a62a-f78b830cf059id: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2: id: ba367494-9862-4596-bd6f-299c7e10a46b
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: cb3217c9fd7beb712d0c61638d143b798010d2b7
workflow-type: tm+mt
source-wordcount: 683
ht-degree: 21%

---

# Percorsi persona

In Journey Optimizer B2B edition Prime, i percorsi di persone sono piani di marketing basati su lead automatizzati e a più passaggi, che utilizzano dati Marketo Engage per orchestrare esperienze personalizzate tra i canali in risposta a coinvolgimento, eventi di business o campagne pianificate.

Per iniziare a usare il percorso in prima persona:

1. Crea un percorso di persone.
1. Aggiungi i nodi e definisci il flusso di percorso nella mappa del percorso.
1. Pubblica il percorso.

## Accedere e sfogliare percorsi di persone

Nel menu di navigazione a sinistra, espandi **[!UICONTROL Gestione marketing]** e seleziona **[!UICONTROL percorsi di persone]**.

È possibile immettere testo nello strumento _Ricerca_ nella parte superiore dell&#39;elenco per filtrare l&#39;elenco visualizzato in base al nome.

### Colonne elenco percorso

La pagina dell&#39;elenco percorsi include le colonne riportate di seguito.

Nome (fai clic sul nome per aprire la mappa del percorso da modificare)
Stato
Data di creazione
Creato da
Ultimo aggiornamento
Ultimo aggiornamento di
Pubblicato
Pubblicato da
Data di inizio
Data di fine

È possibile ordinare l&#39;elenco in base a Stato, Data di creazione o Ultimo aggiornamento facendo clic sull&#39;intestazione della colonna.

Per personalizzare (mostrare/nascondere) le colonne visualizzate nella tabella, fai clic sull’icona Personalizza tabella ( ) nell’angolo in alto a destra. Seleziona o deseleziona le caselle di controllo nella finestra di dialogo e fai clic su Applica.

### Stato del percorso

Lo stato di un percorso può cambiare in base alle azioni applicate. In base allo stato di un percorso, alcune azioni sono/non sono disponibili nel lato destro dell’intestazione.

| Stato | Descrizione | Azioni disponibili |
| ------ | ----------- | ----------------- |
| Bozza | Un percorso non pubblicato che può essere modificato. | <li>Pubblica <li>Duplica <li>Elimina |
| Live | Lo stato del percorso cambia da Bozza a In tempo reale quando viene pubblicato un percorso. Se il percorso si trova in questo stato, non può più essere modificato. | <li>Duplica |
| Terminato | Quando tutti i membri del pubblico account o persona in un percorso completano il percorso, lo stato cambia da Live o Closed (Chiuso) a Finished (Completato). | <li>Duplica <li>Elimina |

## Creazione di un percorso di persone

1. Fai clic su **[!UICONTROL Crea Percorso]** in alto a destra nell&#39;elenco dei percorsi.

1. Nella finestra di dialogo, immetti un **[!UICONTROL Nome]** (obbligatorio) e una **[!UICONTROL Descrizione]** (facoltativo) univoci.

<!-- 
   ![Create Journey dialog](./assets/person-journey-create-dialog.png){width="400"}
-->

1. Fai clic su **[!UICONTROL Crea]**.

### Progettazione percorso

La mappa del percorso __ è la zona centrale nell&#39;area di lavoro del percorso. È dove puoi aggiungere nodi di percorso e configurarli. Fai clic su un nodo per aprirne le proprietà nel pannello a destra del layout e impostarle in base al design. Un percorso di persone inizia sempre con un nodo _[!UICONTROL Pubblico persona]_, in cui puoi definire l&#39;input per il percorso.

<!--
   ![Journey map for newly created journey](./assets/person-journey-create-dialog.png){width="400"}
-->

Dopo aver creato un percorso di persone e aver aggiunto il pubblico di tale persona, crea il percorso utilizzando i nodi. La mappa del percorso fornisce un’area di lavoro in cui puoi creare casi di utilizzo B2B a più passaggi utilizzando i seguenti tipi di nodo per creare il percorso:

* [Intraprendere un’azione](./action-nodes.md)
* [Ascoltare un evento](./listen-for-event-nodes.md)
* [Attendere](./wait-nodes.md)
* [Suddividi percorsi](./split-merge-paths-nodes.md)
* [Prossimo percorso migliore](./next-best-path.md)
* [Unisci percorsi](./split-merge-paths-nodes.md)


## Gestione dei percorsi



## Mappa del percorso

Fare clic sul nome (visualizzato come collegamento) nell&#39;elenco percorsi per esaminare i dettagli, apportare modifiche ed eseguire azioni.

L’intestazione di ciascuna mappa del percorso include:

Nome del percorso
Strumento di modifica per il nome del percorso (icona Modifica )
Stato del percorso
Dalla mappa del percorso, puoi Aggiungere i nodi e definire il flusso di percorso.

### Azioni percorso

La pagina dell’elenco percorsi include tutti i percorsi di account o persone nell’istanza Journey Optimizer B2B edition. Dalla pagina dell’elenco, puoi applicare una serie di azioni a un percorso.



#### Duplicare un percorso

Un’azione di duplicazione è simile a una funzione di clonazione, ma un percorso duplicato non include le risorse dei contenuti del percorso create. Potete duplicare i dettagli del percorso o semplicemente una semplice ossatura della struttura del flusso e del percorso.

NOTA

Fare clic sull&#39;icona Altro (...) accanto al nome del percorso e scegliere Duplica.

A seconda dello stato del percorso, puoi anche accedere all’azione duplicata dai dettagli del percorso o dalla mappa del percorso:

Per un percorso 2D, fate clic sul menu Altro... in alto a destra e scegliete Duplica.
Per tutti gli altri stati del percorso, fare clic su Duplica in alto a destra.
Nella finestra di dialogo Duplica Percorso impostare il nome e la descrizione per il nuovo percorso.
Per impostazione predefinita, nella finestra di dialogo viene utilizzato il nome del percorso duplicato a cui è stato aggiunto _copy. Immettere un altro nome univoco per il percorso, in base alle esigenze.

Scegli il tipo di duplicazione:
Duplicazione parziale dei contenuti: utilizza questo tipo di dati per copiare tutto ciò che si trova nel percorso, escluse le e-mail o i messaggi SMS creati. I nodi che fanno riferimento a un messaggio e-mail o SMS di Marketo Engage sono completamente intatti.
Duplica senza dettagli: utilizza questo tipo per copiare solo la struttura e i percorsi dei nodi. Tutte le impostazioni del nodo e le condizioni del percorso non sono definite (impostazione predefinita), pertanto puoi riutilizzare il flusso di base con diverse impostazioni di pubblico, azioni e segmentazione del percorso. Tutti i nodi Wait (Attesa) utilizzano il valore predefinito di cinque giorni.
Fare clic su Duplica.
Il percorso duplicato viene aperto nella mappa del percorso, dove è possibile impostare i dettagli e creare il contenuto del percorso in base alle esigenze.

Eliminare un percorso

Utilizza un’azione di eliminazione per eliminare definitivamente un percorso. Non puoi eliminare un percorso live o pianificato.

Fare clic sull&#39;icona Altro (...) accanto al nome del percorso e scegliere Elimina.
A seconda dello stato del percorso, puoi anche accedere all’azione di eliminazione dai dettagli del percorso o dalla mappa del percorso:

Per un percorso 2D, fate clic sul menu Altro... in alto a destra e scegliete Elimina.
Per altri stati del percorso, ad esempio Finito o Interrotto, fare clic su Elimina in alto a destra.
Nella finestra di dialogo di conferma, fai clic su Elimina.






