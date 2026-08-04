---
title: Utenti tipo derivati
description: Utilizza utenti tipo derivati in Journey Optimizer B2B Prime per eseguire il targeting degli elenchi di persone e dei percorsi di percorso. Scopri le mappature persona predefinite e il filtro Persona derivata.
badgeBeta: label="Beta" type="informative" tooltip="Questa funzione è attualmente in versione beta limitata"
autotag-review: '2026-06-23T22:01:21.605Z'
TQID: 'https://experienceleague.adobe.com/OZ4GDkaqg9a5Aikic-m-f0MtHSpc3BO0h41fTAL1Rww'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: a4b836d9-ffdd-4df3-a62a-f78b830cf059id: beb5f4be-cec3-471a-9db6-831a77dd3ac9id: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2: id: d270a788-eb1d-40ed-b74e-9158ed975b1fid: c3d6e661-d372-4e98-9fd9-eac771e7e4ee
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 22de56a75a61ff2bf4345bcb09371b4c639206ba
workflow-type: tm+mt
source-wordcount: 639
ht-degree: 2%

---

# Utenti tipo derivati

La classificazione Persona trasforma i dati grezzi dei clienti in acquirenti semantici, comprendendo che l’intelligenza artificiale può utilizzare per generare contesto e favorire decisioni personalizzate su ogni canale e percorso. Questo profilo unificato consente di:

* _Diramazione di Percorso_ - Dividi percorsi route lead per persona, profondità di coinvolgimento e ruolo
* _Arbitrato Percorso_ - Determina il percorso di sviluppo a cui appartiene un lead in questo momento, evitando conflitti di messaggi tra programmi concorrenti
* _Personalizzazione dei contenuti_ - Contenuti con narrazioni specifiche per il ruolo (&quot;per un dirigente&quot; o &quot;per un professionista&quot;)
* _Contesto qualificatore vendite_ - I rappresentanti dello sviluppo commerciale (BDR) ricevono un riepilogo a schermo singolo che mostra l&#39;identità dell&#39;individuo, i suoi interessi e la sua fase corrente nel percorso di acquirenti

## Utenti tipo predefiniti {#default-ersonas}

Per la versione Beta di Journey Optimizer B2B Prime, i seguenti utenti tipo predefiniti sono definiti in base all’attributo titolo del processo:

| Utente tipo | Qualifiche |
| ------- | ---------- |
| [!UICONTROL CXO / EVP] | CEO, CIO, CTO, CMO, CFO, Executive Vice President of Strategy |
| [!UICONTROL SVP / VP] | SVP marketing, VP vendite, SVP operazioni, VP prodotto, VP IT |
| [!UICONTROL Responsabile / Manager senior] | Senior Marketing Manager, IT Manager, Operations Manager, Sales Manager, HR Manager |
| [!UICONTROL Collaboratore individuale] | Responsabile dell’account, ingegnere software, specialista di marketing, rappresentante del successo dei clienti |
| [!UICONTROL Analista] | Analista aziendale, analista dati, analista ricerche di mercato, analista finanziario, analista operazioni |
| [!UICONTROL Sviluppatore] | Sviluppatore front-end, sviluppatore back-end, sviluppatore full-stack, sviluppatore app mobile, ingegnere DevOps |
| [!UICONTROL Personale professionale] | Specialista delle risorse umane, Consulente legale, Responsabile per la conformità, Project Manager, Specialista di approvvigionamento |
| [!UICONTROL Consulente] | Consulente di gestione, consulente IT, consulente di processo aziendale, consulente di marketing |
| [!UICONTROL Altro] | Specialista di settore, consulente indipendente, consulente freelance, esperto in materia |

>[!NOTE]
>
>Nella prossima versione di Disponibilità generale, puoi modificare uno qualsiasi di questi utenti tipo predefiniti in base alle esigenze della tua organizzazione. Supporterà anche le definizioni e la mappatura personalizzate dei tipi di pubblico.

## Filtra per persona derivata {#derived-persona-filter}

[!DNL Journey Optimizer B2B Prime] deriva un utente tipo per ogni record persona valutando gli attributi del record rispetto agli utenti tipo definiti. È possibile utilizzare il risultato dedotto, ovvero _Persona derivata_, come filtro durante la definizione del pubblico per un elenco di persone o per la segmentazione in un percorso di persone.

Il filtro _[!UICONTROL Persona derivata]_ viene visualizzato nel pannello dei filtri nella categoria **[!UICONTROL Attributi persona]**.

### Elenchi di persone {#people-lists}

Quando gestisci i membri in un [elenco di persone statiche](./people-lists.md#static-lists) o definisci le regole per un [elenco di persone dinamiche](./people-lists.md#dynamic-lists), puoi filtrare per _Persona derivata_ per eseguire il targeting di tutte le persone i cui attributi corrispondono a un utente tipo specifico configurato.

![Filtro utente tipo derivato per un elenco di persone](./assets/derived-persona-filter-people-list.png){width="750" zoomable="yes"}

**Elenco statico — Aggiungi membri**

1. Apri l&#39;elenco statico e fai clic su **[!UICONTROL Aggiungi persone]** in alto a destra.

1. Nella finestra di dialogo del filtro, espandi **[!UICONTROL Attributi persone]** e trascina **[!UICONTROL Persona derivata]** nell&#39;area di lavoro.

1. Nella condizione del filtro, scegli **[!UICONTROL is]** e seleziona uno o più utenti tipo dall&#39;elenco.

1. Fai clic su **[!UICONTROL Fine]** per applicare il filtro e qualificare le persone corrispondenti nell&#39;elenco.

**Elenco dinamico - Imposta regole di appartenenza**

1. Apri l&#39;elenco dinamico e seleziona la scheda **[!UICONTROL Regole]**.

1. Fai clic su **[!UICONTROL Modifica regole]**.

1. Nella finestra di dialogo del filtro, espandi **[!UICONTROL Attributi persone]** e trascina **[!UICONTROL Persona derivata]** nell&#39;area di lavoro.

1. Nella condizione del filtro, scegli **[!UICONTROL is]** e seleziona uno o più utenti tipo dall&#39;elenco.

1. Fai clic su **[!UICONTROL Fine]** per salvare la regola.

   L’iscrizione viene aggiornata automaticamente quando i record delle persone vengono valutati in base alla regola.

### Percorsi di persone {#person-journeys}

Quando configuri la segmentazione per un percorso di persone in un nodo [_Percorsi suddivisi_](../marketing/split-merge-paths-nodes.md), puoi utilizzare un utente tipo derivato come filtro del profilo persona per controllare quali persone entrano nel percorso del percorso.

![Filtro utente tipo derivato per una condizione di percorso diviso](./assets/derived-persona-filter-split-path.png){width="750" zoomable="yes"}

1. Fare clic sul nodo **[!UICONTROL Percorsi suddivisi]** nell&#39;area di lavoro del percorso.

1. Nel pannello delle proprietà del nodo a destra, fai clic su **[!UICONTROL Applica condizione]** o **[!UICONTROL Modifica condizione]** per un percorso.

1. Nella finestra di dialogo del filtro, espandi **[!UICONTROL Attributi persone]** e trascina **[!UICONTROL Persona derivata]** nell&#39;area di lavoro.

1. Nella condizione del filtro, scegli **[!UICONTROL is]** e seleziona uno o più utenti tipo dall&#39;elenco.

1. Fai clic su **[!UICONTROL Fine]** per salvare il filtro per il percorso.

