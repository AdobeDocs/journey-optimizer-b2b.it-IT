---
title: Canale e-mail
description: 'Aggiungi nodi di azione e-mail ai percorsi di account: crea nuove e-mail o utilizza e-mail esistenti di Marketo Engage per comunicazioni mirate in Journey Optimizer B2B edition.'
feature: Email Authoring, Account Journeys
role: User
autotag-review: '2026-06-18T20:30:25.418Z'
TQID: 'https://experienceleague.adobe.com/K3OZnLvtSdwSq6AT4JlRQ62t32d6smIJ4K9EEnK-QUc'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: a4b836d9-ffdd-4df3-a62a-f78b830cf059id: f01b5556-e951-40ba-8625-2e3001864f2bid: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2: id: ff0c35fa-aa7e-4050-a37c-198fcacd09e6id: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 0a877cc1fc0dfd9c3d8271c8f7be6a5e34a69a9a
workflow-type: tm+mt
source-wordcount: 881
ht-degree: 2%

---

# Canale e-mail

[!DNL Adobe Journey Optimizer B2B Prime] offre agli esperti di marketing B2B un&#39;esperienza moderna di creazione e consegna di e-mail di livello enterprise. Questa versione introduce strumenti di progettazione delle e-mail riprogettati e un set completo di controlli per la consegna delle e-mail.

>[!NOTE]
>
>Se invii un&#39;e-mail per la prima volta, assicurati che il canale e-mail [e-mail e il recapito messaggi](../admin/configuration-email-deliverability.md) siano configurati.

## Panoramica del canale e-mail {#overview}

* **Configurazioni del canale e-mail** - Gestisci l&#39;identità del mittente, il comportamento della risposta, i tipi di messaggi di marketing e transazionali e il tracciamento.
* **Controlli per il recapito messaggi e-mail** - Configura il tuo canale di recapito messaggi e-mail, inclusa la delega del sottodominio (metodi Fully Delegated e CNAME), la configurazione automatica di DMARC, SPF/DKIM e il supporto del pool IP condiviso.
* **Azione Invia e-mail** - Da un percorso, aggiungi un nodo di azione _Invia e-mail_, inclusa la personalizzazione tramite gli attributi del profilo (sintassi Handlebars).
* **Strumenti di progettazione delle e-mail mediante trascinamento visivo** - Progetta il contenuto delle e-mail con strutture, componenti di contenuto, temi, supporto in modalità scura e frammenti visivi riutilizzabili.
* **Risorse di Marketo Design Studio**: scegli immagini e risorse da una copia unica della libreria di risorse Marketo Engage direttamente nell&#39;area di lavoro delle e-mail.
* **Modelli e frammenti riutilizzabili**: consente di salvare intestazioni, piè di pagina, CTA e layout e-mail comuni e riutilizzarli in percorsi diversi.
* **RBAC (Role-Based Access Control)**: applica autorizzazioni granulari per la creazione, la modifica, l&#39;approvazione e l&#39;invio di e-mail.

## Concetti chiave {#key-concepts}

Prima di creare e-mail per percorsi di persone e contenuti e-mail, esamina i seguenti concetti:

| Concetto | In [!DNL Journey Optimizer B2B Prime] Prime |
| ------- | ---------------------- |
| **_Spazio di progettazione e-mail_** | L’area di lavoro visiva e gli strumenti di progettazione utilizzati per comporre il contenuto delle e-mail. Include componenti di layout drag-and-drop, modelli, frammenti, temi e un editor di personalizzazione. |
| **_Modello_** | Layout e-mail riutilizzabile disponibile per la creazione di un nuovo messaggio e-mail. Può essere un modello di esempio integrato fornito da Adobe o un modello personalizzato creato dal team. |
| **_Frammento visivo_** | Blocco di contenuto riutilizzabile (ad esempio intestazione, piè di pagina, CTA, dichiarazione di non responsabilità legale) che può essere inserito in più e-mail. L’aggiornamento di un frammento propaga la modifica a ogni e-mail che lo utilizza. |
| **_Tema_** | Predefinito di stile riutilizzabile (colori, composizione tipografica, spaziatura, stili di pulsante) applicato a un messaggio e-mail. |
| **_Token Personalization_** | Un&#39;espressione Handlebars, ad esempio `{{profile.firstName}}`, è stata risolta in fase di invio utilizzando i dati del profilo di ogni destinatario. |
| **_Invia azione e-mail_** | Nodo di azione del percorso che utilizza una configurazione di canale e contenuti e-mail per inviare un messaggio e-mail. |

## Aggiungere un messaggio e-mail da un percorso

Per inviare e-mail da un percorso, aggiungi un nodo _Esegui un&#39;azione_ e configuralo per inviare e-mail.

1. Nell&#39;area di lavoro del percorso fare clic sull&#39;icona **+** e selezionare **[!UICONTROL Esegui un&#39;azione]**.

1. Nelle proprietà del nodo a destra, imposta l&#39;azione su **[!UICONTROL Invia e-mail]**.

   ![Azione - Invia e-mail](./assets/person-action-node-send-email.png){width="450"}

1. Scegli l’origine dell’e-mail:

   * **Crea/modifica e-mail** - Scegliere questa opzione per definire il contenuto dell&#39;e-mail, inclusi l&#39;oggetto, le informazioni sul mittente e il corpo dell&#39;e-mail nell&#39;area di progettazione e-mail.

   * **[!UICONTROL Utilizza un&#39;e-mail personalizzata con IA]** - Scegli questa opzione per perfezionare un&#39;e-mail generata con IA nell&#39;area di progettazione e-mail. Queste e-mail sono ottimizzate in modo che i client di posta in arrivo assistiti da AI inseriscano nelle offerte e nelle chiamate all’azione i riepiloghi e le risposte.

1. Fai clic su **[!UICONTROL Crea e-mail]**.

1. Nella finestra di dialogo _[!UICONTROL Crea e-mail]_, immetti un **[!UICONTROL Nome]** univoco (obbligatorio) e una **[!UICONTROL Descrizione]** (facoltativo).

1. Fai clic su **[!UICONTROL Crea]**.

## Definire le proprietà e le azioni dell’e-mail

1. Con il nodo _[!UICONTROL Invia e-mail]_ selezionato nell&#39;area di lavoro del percorso, fai clic su **[!UICONTROL Modifica e-mail]** nelle proprietà del nodo a destra.

<!-- Staging environment broken -->

per l&#39;e-mail e una **[!UICONTROL riga oggetto]**.

Verrà aperta la scheda **[!UICONTROL Azioni]** in cui è possibile selezionare o creare la configurazione di posta elettronica da utilizzare.

1. (Facoltativo) Seleziona un set di regole nelle Regole aziendali per applicare le regole di limitazione all’azione e-mail.

È possibile utilizzare l&#39;opzione di ottimizzazione del tempo di invio [Send](./email-send-time-optimization.md) per prevedere il momento migliore per inviare il messaggio in modo da massimizzare il coinvolgimento in base alle percentuali storiche di apertura e clic. Scopri come

Seleziona il pulsante Modifica contenuto e crea il contenuto come desiderato utilizzando E-mail Designer.

Torna all’area di lavoro del percorso. Se necessario, completa il flusso di percorso trascinando altre azioni o eventi.

Per ulteriori informazioni su come creare, configurare e pubblicare un percorso, consulta questa pagina.


### Definire le impostazioni e-mail {#email-settings}

Configura le impostazioni nella scheda **[!UICONTROL Dettagli]** del pannello di riepilogo dei nodi.

| Impostazione | Descrizione |
| ------- | ----------- |
| **[!UICONTROL Da nome]** | Nome del mittente visualizzato nell’intestazione dell’e-mail. Supporta i token di personalizzazione. |
| **[!UICONTROL Da e-mail]** | Indirizzo e-mail del mittente. Impostazioni predefinite dalla configurazione del canale. Supporta la personalizzazione. |
| **[!UICONTROL Indirizzo di risposta]** | Indirizzo che riceve risposte dai destinatari. Supporta la personalizzazione. |
| **[!UICONTROL Oggetto]** | Riga dell’oggetto dell’e-mail. Modificabile dal valore immesso al momento della creazione. |
| **[!UICONTROL Dominio di branding]** | Dominio utilizzato per l’invio specifico per il brand. |
| **[!UICONTROL IP dedicato]** | Indirizzo IP specifico per il tracciamento del recapito messaggi. |
| **[!UICONTROL E-mail operativa]** | Quando questa opzione è abilitata, ignora la soppressione di rinuncia e annullamento dell’abbonamento. Da utilizzare solo per messaggi operativi legittimi. |
| **[!UICONTROL Includi visualizzazione come pagina Web]** | Genera un collegamento a una pagina web per il contenuto dell’e-mail. |
| **[!UICONTROL Disabilita tracciamento aperto]** | Impedisce il tracciamento dell’attività di apertura delle e-mail. |
| **[!UICONTROL Preheader]** | Testo di riepilogo breve visualizzato dopo la riga dell&#39;oggetto nelle anteprime della casella in entrata. |
| **[!UICONTROL Indirizzi CC]** | Aggiungi fino a 25 campi e-mail lead o azienda per riceverne una copia. |

### Controllare gli avvisi {#alerts}

[!DNL Journey Optimizer B2B Prime] rileva problemi nell&#39;angolo in alto a destra dell&#39;editor e-mail. Risolvi tutti gli errori prima di attivare il percorso; gli avvisi sono solo consigli.

**Errori** (impedisce l&#39;attivazione del percorso):

* Il nome del mittente è vuoto
* Riga oggetto mancante
* Il contenuto dell’e-mail è vuoto

**Avvisi** (consigli):

* Il collegamento di rinuncia non è presente nel corpo dell’e-mail
* La versione testo di HTML è vuota
* Sono stati rilevati collegamenti vuoti
* L&#39;e-mail supera i 100 K
