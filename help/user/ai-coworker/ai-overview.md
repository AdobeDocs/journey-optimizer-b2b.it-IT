---
title: Funzionalità di intelligenza artificiale in Journey Optimizer B2B Edition
description: 'Accelera i flussi di lavoro con le funzionalità di intelligenza artificiale: scopri le nozioni di prodotto, aiuto per la risoluzione dei problemi e informazioni operative per Journey Optimizer B2B Edition.'
feature: AI Assistant
role: User, Admin
level: Beginner
exl-id: 52ff66d2-1969-4e2c-985a-c75e613368de
autotag-review: '2026-06-05T16:05:30.499Z'
TQID: 'https://experienceleague.adobe.com/4bXkOzwadjZVzhedVO6oQEEV1biaWMZFHEuqey74qek'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
    internal-label: Journey Optimizer B2B Edition
feature_v2:
  - id: bef5003b-cad2-4f40-bdb2-a80426d52ef5
    internal-label: AI Assistant
subfeature_v2:
  - id: eb7448d0-50e6-41cc-83e2-a84cd2413491
    internal-label: Operational Insights
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: bbbea26f-9621-49eb-9ab8-e06fb3bbce8c
    internal-label: Artificial intelligence
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
    internal-label: Privacy
source-git-commit: c2d3ba94927361f7695e901ef9071bdd4ded8f7d
workflow-type: tm+mt
source-wordcount: '858'
ht-degree: 7%
---
# Funzionalità di intelligenza artificiale in Journey Optimizer B2B Edition

Utilizza le funzionalità di intelligenza artificiale in [!DNL Adobe Journey Optimizer B2B Edition] per generare contenuti, esplorare le conoscenze del prodotto e acquisire informazioni operative.

>[!IMPORTANT]
>
>Per poter utilizzare le funzionalità di intelligenza artificiale in [!DNL Journey Optimizer B2B Edition] è necessario un accordo per le [linee guida utente](https://www.adobe.com/it/legal/licenses-terms/adobe-gen-ai-user-guidelines.html){target="_blank"}. Questo contratto contiene anche il contratto beta pubblico, in modo da poter utilizzare funzioni basate sull’intelligenza artificiale aggiuntive durante il rollout.

+++Visualizza l&#39;interfaccia del contratto utente

![Prima pagina del contratto utente.](./assets/user-agreement-1.png)

![Ultima pagina del contratto utente.](./assets/user-agreement-2.png)

+++

## Usa l&#39;app [!DNL Coworker] {#coworker-app}

Utilizza l&#39;interfaccia dell&#39;app [!DNL CX Enterprise Coworker] per tutti i flussi di lavoro di chat diversi dalla generazione di contenuti. Poni le tue domande sul prodotto, esplora le informazioni operative e utilizza [abilità di percorso](../agents/journey-agent.md) e [abilità di pubblico per account B2B e persone](../agents/audience-agent-b2b.md). La generazione dei contenuti rimane disponibile in [!DNL Journey Optimizer B2B Edition].

Per istruzioni su come aprire l&#39;app, avviare le conversazioni e utilizzare le funzionalità di chat, vedere la [guida all&#39;interfaccia di CX Coworker](https://experienceleague.adobe.com/it/docs/coworker/content/chat/ui-guide){target="_blank"}.

Considera il tipo di richiesta di informazioni necessario prima di inviare una query di chat [!DNL Coworker].

### Conoscenza del prodotto

Per conoscenza del prodotto si intendono i concetti e gli argomenti contenuti nella documentazione di [!DNL Journey Optimizer B2B Edition] in [!DNL Adobe Experience League]. Le domande relative alla conoscenza del prodotto possono essere ulteriormente specificate nei seguenti sottogruppi:

| Conoscenza del prodotto | Esempi |
| --- | --- |
| Apprendimento puntato | <li>Che cos’è un gruppo di acquisto? <li> Mostrami un esempio di modello per ruoli di gruppo di acquisto? |
| Ricerca aperta | <li>Quali sono i passaggi per creare gruppi di acquisto? <li>Come si utilizzano i campi personalizzati nei modelli di ruolo di un gruppo di acquisto? |
| Risoluzione dei problemi | <li>Perché non sono stati creati gruppi di acquisto per il mio percorso? <li>Perché non riesco a trovare gli Eventi esperienza da ascoltare nel percorso? |

### Insight operativi

_Informazioni operative_ fa riferimento alle risposte che [!DNL Coworker] genera sugli oggetti metadati (attributi, pubblico dell&#39;account, flussi di dati, set di dati, destinazioni, percorsi di account, schemi, origini, modelli di gruppi di acquisto e interessi delle soluzioni). Queste informazioni includono conteggi, ricerche e impatto sulla derivazione. Non esaminano i dati all’interno della sandbox.

* Quale pubblico dell’account ha la dimensione di pubblico più grande e qual è tale dimensione?
* Quanti tipi di pubblico dell’account non sono mai stati utilizzati in alcun percorso?
* Quali percorsi attivi utilizzano l&#39;interesse della soluzione _x_?

Puoi porre a [!DNL Coworker] domande sulle tue informazioni operative nei seguenti domini:

| Dominio | Metadati supportati | Metadati non supportati |
| --- | --- | --- |
| Attributi/campi | <li>Ricerca nome attributo <li>Attributo: relazione schema <li>Attributo: relazione set di dati <li>Attributo: relazione pubblico <li>Attributo - relazione di destinazione | <li>Classe attributo <li>Audit <li>Stato obsoleto <li>Etichette <li>Valore memorizzato negli attributi |
| Tipi di pubblico dell&#39;account <br><br>**_Note:_** Nel contesto [!DNL Journey Optimizer B2B Edition], la chat di [!DNL Coworker] può rispondere solo alle domande del pubblico per i tipi di pubblico dell&#39;account. Nel contesto [!DNL Adobe Experience Platform], la chat di [!DNL Coworker] può rispondere alle domande solo per il pubblico di tipo Persona. | <li>Conteggio del pubblico <li>Tipo di pubblico (in streaming o in batch) <li>Date di creazione/modifica <li>Stato attivazione <li>Conteggio membri <li>Pubblico duplicato <li>Ricerca per nome e ID | <li>Sovrapposizioni del pubblico <li>Attivazione pubblico <li>Audit <li>Crea/modifica <li>Etichette <li>Tendenze delle qualifiche dei membri |
| Flussi di dati | <li>Conteggi dei flussi di dati <li>Stato del flusso di dati <li>Flusso di dati: relazione set di dati <li>Flusso di dati - relazione di origine | <li>Creazione/modifica <li>Relazioni flusso di dati-batch <li>Acquisisci conteggio profili |
| Set di dati | <li>Conteggio set di dati <li>Stato abilitazione profilo <li>Data di creazione/modifica <li>Set di dati: relazione schema <li>Set di dati: relazione pubblico <li>Set di dati: relazione attributo <li>Set di dati: relazione flusso di dati <li>Ricerca nome <li>Ricerca per nome e ID | <li>Audit <li>Creato da <li>Set di dati: relazione batch <li>Creazione/modifica del set di dati <li>Dimensione set di dati <li>Numero di profili <li>Numero di righe <li>Ricerca di valori |
| Destinazioni | <li>Conteggi di destinazione configurati <li>Destinazione - Relazione pubblico <li>Relazione attributo di destinazione | <li>Configurazione account <li>Informazioni sulle credenziali dell&#39;account <li>Profili univoci attivati |
| Percorsi (Percorsi di account) | <li>Conteggio <li>Ricerca per nome e ID <li>Stato del percorso <li>Date di creazione/modifica | <li>Attributi - Relazioni percorso <li>Audit <li>Creazione/modifica <li>Creato da |
| Schemi | <li>Conteggi schema <li>Data di creazione/modifica <li>Schema - relazione attributo <li>Schema: relazione tra set di dati <li>Schema: relazione pubblico <li>Stato abilitazione profilo <li>Ricerca nome <li>Ricerca per nome e ID | <li>Audit <li>Creazione/modifica <li>Creato da <li>Gruppi di campi <li>Identità <li>Spazi dei nomi identità <li>Etichette <li>Numero di profili |
| Origini | <li>Conteggi account <li>Stato account <li>Flussi di dati attivi/inattivi per ogni account <li>Connettore Source - relazione flusso di dati <li>Account Source - relazione flusso di dati | <li>Informazioni sulle credenziali dell’account <li>Configurazione accountMetriche di acquisizione dati <li>Numero di profilesSource - relazioni batch |
| Modello per gruppo di acquisto | <li>Conteggi <li>Stato <li>Ruoli <li>Ricerca per nome e ID | <li>Regole ruolo |
| Interesse soluzione | <li>Conteggi <li>Stato <li>Interesse soluzione - Relazione modello gruppo di acquisto <li>Ricerca per nome e ID | <li>Interesse soluzione - Relazione tra gruppo di acquisto |

{style="table-layout:fixed"}

Per le domande sulle informazioni operative, le risposte potrebbero non riflettere lo stato corrente dell’interfaccia utente. I dati che supportano queste domande vengono aggiornati una volta ogni 24 ore. Ad esempio, le modifiche apportate dagli utenti in [!DNL Adobe Real-Time Customer Data Platform] durante il giorno vengono sincronizzate con gli archivi dati di notte e quindi diventano disponibili per le domande degli utenti al mattino. Per informazioni su dati specifici relativi agli oggetti, accedi a una sandbox.

### Privacy, sicurezza e governance

La chat di [!DNL Coworker] in [!DNL Journey Optimizer B2B Edition] dà priorità a privacy, sicurezza e governance. Rivedi le seguenti informazioni per scoprire le funzionalità incentrate sulla fiducia dei clienti che puoi aspettarti dalla chat di [!DNL Coworker]:

* [!DNL Coworker] oggi non utilizza dati personali, nemmeno a scopo di formazione.

* Puoi visualizzare un registro di 30 giorni delle tue interazioni precedenti con la chat di [!DNL Coworker].

* [!DNL Coworker] si basa sui dati specifici della sandbox e sulla documentazione pubblica di Adobe quando risponde ai prompt. I dati non sono condivisi tra sandbox diverse.

* Le richieste che fornisci alla chat di [!DNL Coworker] non sono condivise con altri clienti.

## Passaggi successivi

Con una conoscenza generale della chat di [!DNL Coworker], procedere all&#39;attivazione e all&#39;utilizzo durante i flussi di lavoro. Per ulteriori informazioni, consulta la seguente documentazione:

* [Abilita accesso alle funzionalità AI](./enable-ai-access.md)
* [Guida alle domande](./question-guidance.md)
* [Guida all’interfaccia di CX Coworker](https://experienceleague.adobe.com/it/docs/coworker/content/chat/ui-guide){target="_blank"}
