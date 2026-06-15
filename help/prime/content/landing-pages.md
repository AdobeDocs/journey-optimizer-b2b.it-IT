---
title: Pagine di destinazione
description: 'Creazione, progettazione e pubblicazione di pagine di destinazione per percorsi di persone: creazione da zero, importazione di HTML, aggiunta di moduli, personalizzazione del contenuto e collegamento dalle e-mail in Journey Optimizer B2B Prime.'
autotag-review: '2026-06-12T22:53:39.337Z'
TQID: 'https://experienceleague.adobe.com/BvtB0i5CzlVutPA6HAzZy-Gfymw7ppZwthyBauyciLc'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: e666e996-b2cf-4c45-8fc2-1c625212ababid: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2: id: a96755d6-1f54-4f3f-a971-d31f83705ab7id: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 21f0ab524176df40128212fef920e10b06b5c317
workflow-type: tm+mt
source-wordcount: 2180
ht-degree: 4%

---

# Pagine di destinazione

Una pagina di destinazione è una pagina web indipendente in cui puoi indirizzare contatti e clienti dopo che hanno fatto clic su un elemento collegato in un’e-mail, un messaggio SMS o qualsiasi posizione digitale. Puoi incorporare queste pagine nei tuoi percorsi per consentire ai potenziali clienti e ai clienti di visualizzare i messaggi sul web e i progressi compiuti nei tuoi percorsi. Puoi creare, personalizzare e visualizzare in anteprima le pagine di destinazione nell’area di progettazione visiva della pagina di destinazione.

Casi d’uso comuni per le pagine di destinazione:

* Fornisci il consenso o la rinuncia alle comunicazioni di marketing o a un servizio specifico. Utilizza un collegamento a un elenco di destinazione in un’e-mail o in un’altra comunicazione.
* Raccogli il consenso prima di inviare le comunicazioni e invia un’e-mail di conferma in caso di consenso o rinuncia.
* Acquisisci o aggiorna i dati del profilo (profilatura progressiva, preferenze, registrazioni e scenari simili) utilizzando i moduli nelle pagine di destinazione.
* Indirizza le persone a informazioni specifiche per la campagna progettate per l’orchestrazione del percorso.
* Reindirizza le persone a un modulo web dedicato senza creare una pagina esterna al di fuori di Journey Optimizer B2B Prime.

<!-- 
## Landing page workflow

To direct members of a journey audience to a defined web page when they click a specific link, create a landing page in Journey Optimizer B2B Edition: 


1. [Create the page](./landing-pages-create-publish.md) - Select a preset, set up the primary page, and add any required subpages.
1. [Design the landing page content](./landing-page-design.md) - Build the page content using drag-and-drop visual design components.
1. [Test the landing page](./landing-pages-create.md) - Preview the page, test form behavior, and then publish to make it live.
1. [Link to the page from your journey](#link-to-a-landing-page) - Add the landing page URL to an email, SMS, or journey action so that recipients can reach it.


For example, you can create and design landing pages to direct your users to online information. The page could include a form where they can opt in or opt out from receiving your communications. Or it could be an opportunity to subscribe to a recurring communications, such as a newsletter. 

You can create, personalize, and preview landing pages in the visual design space.
-->

## Accedere e gestire le pagine di destinazione {#access-manage-landing-pages}

Per accedere alle pagine di destinazione in Journey Optimizer B2B Prime, vai alla navigazione a sinistra e fai clic su **[!UICONTROL Gestione contenuto]** > **[!UICONTROL Pagine di destinazione]**. Questa azione visualizza un elenco di tutte le pagine di destinazione create nell’istanza.

L&#39;elenco è ordinato in base alla colonna _[!UICONTROL Modificato]_, con gli elementi aggiornati più di recente nella parte superiore. Fai clic sul titolo della colonna per passare da crescente a decrescente.

### Filtrare l’elenco delle pagine di destinazione {#filter-list}

Per cercare una pagina di destinazione per nome, immetti una stringa di testo nella barra di ricerca per trovare una corrispondenza. Fai clic sull&#39;icona _Filtro_ ( ![Mostra o nascondi icona filtri](../../user/assets/do-not-localize/icon-filter.svg) ) per visualizzare le opzioni di filtro disponibili e modificare le impostazioni per filtrare gli elementi visualizzati in base ai criteri specificati.

![Filtra le pagine di destinazione visualizzate](./assets/landing-pages-list-filtered.png){width="800" zoomable="yes"}

<!-- 
This is going away? ### Customize the column display

Customize the columns that you want to display in the table by clicking the _Customize table_ icon ( ![Customize table icon](../assets/do-not-localize/icon-column-settings.svg) ) at the top right. 

In the dialog, select the columns to display and click **[!UICONTROL Apply]**.

![Select the columns that you want to display](./assets/landing-pages-customize-table-dialog.png){width="300"} 
-->

### Stato e ciclo di vita della pagina di destinazione {#landing-page-status}

Lo stato della pagina di destinazione determina la disponibilità del collegamento nei contenuti e-mail e SMS e le modifiche che puoi apportare.

| Stato | Descrizione |
| -------------------- | ----------- |
| Bozza | Quando crei una pagina di destinazione, questa si trova nello stato Bozza. Rimane in questo stato mentre definisci o modifichi il contenuto visivo e fino a quando non lo pubblichi come pagina in hosting. Azioni disponibili:<br/><ul><li>Modifica nome o descrizione</li><li>Modifica URL collegamento</li><li>Modifica nello spazio di progettazione visiva</li><li>Pubblica</li><li>Duplica</li><li>Elimina</li></ul> |
| Pubblicato | Quando pubblichi una pagina di destinazione, questa viene ospitata sull’istanza Prime B2B di Journey Optimizer e diventa disponibile per il collegamento in un contenuto di un messaggio e-mail o SMS. Azioni disponibili:<br/><ul><li>Modifica nome o descrizione</li><li>Modifica URL collegamento</li><li>Aggiungere un collegamento nel contenuto di un messaggio e-mail o SMS</li><li>Crea versione bozza</li><li>Duplica</li><li>Elimina</li></ul> |
| Pubblicato con bozza | Quando crei una bozza da una pagina di destinazione pubblicata, la versione pubblicata rimane e il contenuto della bozza può essere modificato nello spazio di progettazione visiva. Se pubblichi la bozza della versione, questa sostituisce la versione pubblicata corrente e il contenuto viene aggiornato nella pagina ospitata. Azioni disponibili:<br/><ul><li>Modifica nome o descrizione</li><li>Modifica URL collegamento</li><li>Aggiungere un collegamento nel contenuto di un messaggio e-mail o SMS</li><li>Modifica versione bozza in Visual Design Space</li><li>Pubblica versione bozza</li><li>Duplica</li><li>Elimina (elimina entrambe le versioni)</li><li>Elimina bozza (torna allo stato pubblicato)</li></ul> |

<!-- ![Landing page status lifecycle](./assets/status-lifecycle-diagram.png){zoomable="yes"} -->

## Creare una pagina di destinazione {#create-landing-page}

>[!CONTEXTUALHELP]
>id="ajo-b2b-prime_lp_create"
>title="Definire e configurare la pagina di destinazione"
>abstract="Per creare una pagina di destinazione, devi selezionare un predefinito; configurare la pagina principale e le pagine secondarie; e infine verificare la pagina prima di pubblicarla."

Per indirizzare i membri del pubblico di un percorso di persone a una pagina Web definita quando fanno clic su un collegamento specifico, creare una pagina di destinazione in [!DNL Journey Optimizer B2B Prime]. Selezionare un predefinito, configurare la pagina principale e le eventuali pagine secondarie, [verificare la pagina](#test-landing-page) e pubblicarla.

>[!IMPORTANT]
>
>Prima di creare la prima pagina di destinazione, completa la relativa configurazione. Ciò include la configurazione di un sottodominio per ospitare le pagine di destinazione e la definizione di almeno un predefinito che specifica il sottodominio e le altre impostazioni del canale. Quando crei la pagina di destinazione, selezioni un predefinito. Per la configurazione dell&#39;amministratore, vedere [Configurazione della pagina di destinazione](../admin/configuration-presets-landing-pages.md).
>
>Per i casi di utilizzo relativi all&#39;acquisizione dei dati, crea un [modulo](./forms.md) prima di incorporarlo in una pagina di destinazione.

Per creare una pagina di destinazione, effettua le seguenti operazioni:

1. Vai alla navigazione a sinistra e seleziona **[!UICONTROL Gestione contenuto]** > **[!UICONTROL Pagine di destinazione]**.

1. Nell&#39;elenco delle pagine di destinazione fare clic su **[!UICONTROL Crea pagina di destinazione]**.

1. Immetti un **[!UICONTROL Titolo]** (obbligatorio) e una **[!UICONTROL Descrizione]** (facoltativo).

   Criteri di titolo e descrizione:

   * **Titolo** — Massimo 100 caratteri. Deve essere univoco (senza distinzione tra maiuscole e minuscole).
   * **Descrizione** — Massimo 300 caratteri.
   * Sono consentiti caratteri Alpha, numerici e speciali.
   * I caratteri riservati sono **_non consentiti_**: `\ / : * ? " < > |`

1. Seleziona un **[!UICONTROL predefinito]**.

   Un amministratore [crea i predefiniti per le pagine di destinazione](../admin/configuration-presets-landing-pages.md#lp-presets) per definire il sottodominio e altre impostazioni utilizzate per le pagine di destinazione. Seleziona un predefinito, quindi fai clic su **[!UICONTROL Visualizza predefinito]** per rivederne le impostazioni e confermare che corrispondono ai requisiti della pagina di destinazione.

1. Fai clic su **[!UICONTROL Crea]**.

   Viene visualizzata la pagina principale e le relative proprietà. Scopri come [configurare le impostazioni della pagina principale](#configure-primary-page).

1. Per aggiungere una pagina secondaria, ad esempio una pagina di ringraziamento o di errore, fare clic sull&#39;icona **+**.

   Puoi aggiungere fino a due pagine secondarie per pagina di destinazione.

Dopo aver configurato e progettato la pagina principale e le eventuali pagine secondarie, [verifica la pagina di destinazione](#test-landing-page) prima di pubblicarla.

>[!CAUTION]
>
>Non puoi accedere alla pagina di destinazione copiando e incollando l’URL definito in un browser web, anche se la pagina è pubblicata. Eseguire il test della pagina utilizzando la funzione di anteprima come descritto in [Eseguire il test della pagina di destinazione](#test-landing-page).

## Configurare la pagina principale {#configure-primary-page}

>[!CONTEXTUALHELP]
>id="ajo-b2b-prime_lp_primary_page"
>title="Definire le impostazioni della pagina principale"
>abstract="Definisci la pagina principale, che viene visualizzata immediatamente quando un destinatario fa clic sul collegamento della pagina di destinazione, ad esempio da un’e-mail o da un sito web."

>[!CONTEXTUALHELP]
>id="ajo-b2b-prime_lp_access_settings"
>title="Definire l’URL della pagina di destinazione"
>abstract="In questa sezione, definisci un URL univoco per la pagina di destinazione. La prima parte dell’URL richiede la configurazione precedente di un sottodominio della pagina di destinazione come parte del predefinito selezionato."

La pagina principale è quella che viene visualizzata immediatamente quando un destinatario fa clic sul collegamento della pagina di destinazione, ad esempio da un’e-mail o da un sito web.

Per definire le impostazioni della pagina principale, effettuare le seguenti operazioni:

1. Modifica il **[!UICONTROL Nome pagina]** in base alle tue esigenze, che per impostazione predefinita è _Pagina principale_.

1. Definisci la parte finale dell’URL della pagina.

   Il predefinito selezionato determina la prima parte dell’URL. Un amministratore configura il sottodominio [della pagina di destinazione](../admin/configuration-presets-landing-pages.md#lp-subdomains) come parte del predefinito.

   >[!CAUTION]
   >
   >L’URL della pagina di destinazione deve essere univoco.
   >
   >Non puoi accedere alla pagina di destinazione copiando e incollando questo URL in un browser web, anche se la pagina è pubblicata. Eseguire il test utilizzando la funzione di anteprima come descritto in [Verificare la pagina di destinazione](#test-landing-page).

1. Se desideri una pagina di destinazione anonima, disabilita l&#39;opzione **[!UICONTROL Richiedi utenti identificati]**.

1. Fai clic sull&#39;icona _Calendario_ per impostare la **[!UICONTROL scadenza pagina]**.

   Dopo aver selezionato una data di scadenza, scegli l’azione alla scadenza della pagina:

   * **[!UICONTROL URL di reindirizzamento]** - Immettere l&#39;URL della pagina da utilizzare come reindirizzamento.
   * **[!UICONTROL Errore del browser]** - Immettere il testo dell&#39;errore da visualizzare al posto della pagina.

## Verificare la pagina di destinazione {#test-landing-page}

>[!CONTEXTUALHELP]
>id="ajo-b2b-prime_preview_lp_profiles"
>title="Visualizzare l’anteprima e testare la pagina di destinazione"
>abstract="Dopo aver definito le impostazioni e il contenuto della pagina di destinazione, utilizza i profili di test per visualizzare l’anteprima della pagina."

Una volta definiti le impostazioni e il contenuto della pagina di destinazione, puoi utilizzare i profili di test per visualizzare l’anteprima della pagina. Se hai inserito [contenuto personalizzato](email-authoring.md#personalization), puoi controllare come questo contenuto viene visualizzato nella pagina di destinazione utilizzando i dati del profilo di test.

>[!PREREQUISITES]
>
>Per visualizzare in anteprima e verificare le pagine di destinazione, devi disporre dell&#39;autorizzazione **[!UICONTROL Pubblica messaggi]** e di un set di dati definito contenente i profili di test.

1. Fai clic su **[!UICONTROL Anteprima e test]** per aprire la selezione del profilo di test.

   >[!NOTE]
   >
   >È inoltre possibile utilizzare **[!UICONTROL Simula contenuto]** nello spazio di progettazione visiva.

1. Dalla schermata _[!UICONTROL Simula]_, seleziona un profilo di test.

   Se i profili necessari non sono elencati, fare clic su **[!UICONTROL Gestisci profili di test]** per utilizzare un indirizzo di posta elettronica del profilo di test noto e aggiungerlo all&#39;elenco.

   +++Aggiungere profili di test

   Per **[!UICONTROL Spazio dei nomi identità]**, fai clic sull&#39;icona _Seleziona_ ( ![Seleziona icona](../../user/assets/do-not-localize/icon-select-data.svg) ) e scegli lo spazio dei nomi `Email` da utilizzare per testare i profili.

   Nel campo **[!UICONTROL Valore identità]** immettere l&#39;indirizzo di posta elettronica per identificare il profilo di test e fare clic su **[!UICONTROL Aggiungi profilo]**. Puoi ripetere questa operazione per aggiungere più profili.

   Fai clic sulla freccia indietro in alto a sinistra per tornare alla pagina _[!UICONTROL Simula]_.

   +++

1. Seleziona **[!UICONTROL Apri anteprima]** per verificare la pagina di destinazione.

   L’anteprima della pagina di destinazione viene visualizzata in una nuova scheda. I dati del profilo di test selezionati sostituiscono gli elementi personalizzati.

1. Seleziona altri profili di test per visualizzare in anteprima il rendering per ogni variante della pagina di destinazione.

## Modificare una pagina di destinazione {#edit-landing-page}

Le modifiche apportate a una pagina di destinazione dipendono dal suo stato corrente:

* Quando una pagina di destinazione è in stato **_Bozza_**, puoi modificarne i dettagli, l&#39;URL e il contenuto visivo.
* Quando una pagina di destinazione si trova nello stato **_Pubblicato_**, puoi modificare la descrizione, ma non il nome. Per modificare il contenuto visivo, è necessario creare una versione bozza della pagina.
* Quando una pagina di destinazione è in stato **_Pubblicato con bozza_**, la modifica dei dettagli è limitata alla descrizione. Puoi anche modificare il contenuto visivo della versione bozza.

>[!BEGINTABS]

>[!TAB Bozza]

1. Dalla pagina di elenco _[!UICONTROL Pagine di destinazione]_, fai clic sul nome della pagina di destinazione per aprirla.

   Viene visualizzata un’anteprima del contenuto visivo, con i dettagli della pagina di destinazione a destra.

1. Modifica uno dei dettagli, ad esempio nome e descrizione.

   <!-- ![Details for landing page with Draft status](./assets/landing-page-draft-details.png){width="700" zoomable="yes"} -->

1. Per apportare modifiche al contenuto nello spazio di progettazione visivo, fare clic su **[!UICONTROL Modifica pagina di destinazione]**.

1. Fai clic su **[!UICONTROL Salva]** o **[!UICONTROL Salva e chiudi]** per tornare ai dettagli della pagina di destinazione.

1. Quando la pagina soddisfa i criteri e desideri renderla disponibile per la visualizzazione, fai clic su **[!UICONTROL Pubblica]**.

>[!TAB Pubblicato]

1. Dalla pagina di elenco _[!UICONTROL Pagine di destinazione]_, fare clic sul nome della pagina per aprirla.

   Viene visualizzata un’anteprima del contenuto visivo, con i dettagli della pagina di destinazione a destra.

1. Se necessario, modifica la descrizione.

   Per una pagina di destinazione pubblicata, tutti gli altri dettagli non possono essere modificati.

1. Se desideri aggiornare il contenuto, fai clic su **[!UICONTROL Modifica pagina di destinazione]** a destra.

   Fare clic su **[!UICONTROL Crea bozza versione]** nella finestra di dialogo per aprire la bozza versione nello spazio di progettazione visivo.

1. Fai clic su **[!UICONTROL Salva]** o **[!UICONTROL Salva e chiudi]** per tornare ai dettagli della pagina di destinazione.

1. Quando la bozza della pagina di destinazione soddisfa i criteri e desideri rendere le modifiche disponibili nella pagina pubblicata, fai clic su **[!UICONTROL Pubblica]**.

   Quando pubblichi la versione bozza, questa sostituisce la versione pubblicata corrente e il contenuto viene aggiornato per l’URL della pagina.

>[!TAB Pubblicato con bozza]

Quando apri la pagina di destinazione, viene visualizzata la versione bozza. Le schede nella parte superiore dello spazio di anteprima consentono di alternare la visualizzazione tra la versione pubblicata e quella bozza. Le bozze delle azioni e dei dettagli sono visualizzate a destra.

<!-- ![Preview and details for the landing page draft version](./assets/landing-page-published-draft-details.png){width="700" zoomable="yes"} -->

Per aggiornare il contenuto:

1. Fai clic su **[!UICONTROL Modifica pagina di destinazione]** in alto a destra.

1. Fai clic su **[!UICONTROL Salva]** o **[!UICONTROL Salva e chiudi]** per tornare ai dettagli della pagina di destinazione.

1. Quando la pagina della bozza soddisfa i criteri e desideri rendere disponibili le modifiche, fai clic su **[!UICONTROL Pubblica]**.

   Quando pubblichi la versione bozza, questa sostituisce la versione pubblicata corrente e il contenuto viene aggiornato nella pagina ospitata.

>[!ENDTABS]

## Duplicare una pagina di destinazione {#duplicate-landing-page}

Puoi duplicare una pagina di destinazione utilizzando uno dei seguenti metodi:

* Dalla pagina dell&#39;elenco _[!UICONTROL Pagina di destinazione]_, fare clic sull&#39;icona _Altro_ (**...**) accanto al nome della pagina di destinazione e scegli **[!UICONTROL Duplica]**.
* Nella parte superiore destra della pagina dei dettagli della pagina di destinazione, fare clic su **[!UICONTROL ... Altro]** e scegli **[!UICONTROL Duplicato]**.

<!-- ![Duplicate the landing page](./assets/landing-page-details-duplicate-delete.png){width="600" zoomable="yes"} -->

Nella finestra di dialogo, inserisci un nome utile (univoco) e una descrizione (facoltativa). Fai clic su **[!UICONTROL Duplica]** per completare l&#39;azione.

<!-- ![Enter a name and description for the duplicated landing page](./assets/landing-page-duplicate-dialog.png){width="350"} -->

La pagina duplicata (nuova) viene quindi visualizzata nell&#39;elenco _Pagine di destinazione_.

## Eliminare una pagina di destinazione {#delete-landing-page}

Puoi eliminare una pagina di destinazione utilizzando uno dei seguenti metodi:

* Dalla pagina dell&#39;elenco _[!UICONTROL Pagina di destinazione]_, fare clic sull&#39;icona _Altro_ (**...**) accanto al nome della pagina di destinazione e scegliere **[!UICONTROL Elimina]**.
* Nella parte superiore destra della pagina dei dettagli della pagina di destinazione, fare clic su **[!UICONTROL ... Altro]** e scegliere **[!UICONTROL Elimina]**.

Questa azione apre una finestra di dialogo di conferma. È possibile interrompere il processo facendo clic su **[!UICONTROL Annulla]** oppure su **[!UICONTROL Elimina]** per confermare l&#39;eliminazione.

<!-- ![Delete landing page dialog](./assets/landing-page-delete-dialog.png){width="400"} -->

## Collegamento a una pagina di destinazione {#link-to-landing-page}

In qualità di addetto al marketing o creativo che produce e-mail, frammenti e contenuti di pagina, puoi incorporare collegamenti alle pagine di destinazione pubblicate (live) create nell’istanza Prime B2B di Journey Optimizer.

1. Quando lavori nello spazio di progettazione visiva per un frammento, un’e-mail, una pagina di destinazione o un modello, seleziona una parte di testo, un componente pulsante o un componente immagine per il collegamento.

   Le opzioni **[!UICONTROL Collegamento]** sono visualizzate nel pannello di destra.

1. Per l&#39;opzione **[!UICONTROL Tipo]**, scegliere **[!UICONTROL Pagina di destinazione]**.

   <!-- ![Link options for a landing page](/help/assets/content-design-shared/content-design-link-settings.png){width="700" zoomable="yes"} -->

1. Per l&#39;opzione **[!UICONTROL Pagina di destinazione]**, fare clic sull&#39;icona _Seleziona pagina_ ( ![Mostra icona collegamenti](../../user/assets/do-not-localize/icon-landing-page-select.svg) ).

1. Nella finestra di dialogo Seleziona pagina di destinazione, imposta **[!UICONTROL Origine pagina di destinazione]** come **[!UICONTROL Journey Optimizer B2B edition]**, seleziona la casella di controllo per la pagina di destinazione dall&#39;elenco delle pagine pubblicate e fai clic su **[!UICONTROL Seleziona]**.

   <!-- ![Link options for a landing page](/help/assets/content-design-shared/content-design-link-landing-page-select.png){width="600" zoomable="yes"} -->

1. Per l&#39;opzione **[!UICONTROL Target]**, scegliere il comportamento della destinazione di collegamento:

   * **[!UICONTROL Nessuno]** - Apre il collegamento utilizzando il comportamento predefinito del browser.
   * **[!UICONTROL Vuoto]** - Apre il collegamento in una nuova finestra o scheda.
   * **[!UICONTROL Autonomo]** - Apre il collegamento nello stesso frame.
   * **[!UICONTROL Elemento padre]** - Apre il collegamento nel frame padre.
   * **[!UICONTROL Top]** - Apre il collegamento nel corpo completo della finestra.

1. (Solo collegamento di testo) Per sottolineare il testo collegato, selezionare la casella di controllo **[!UICONTROL Sottolinea collegamento]**.

   Puoi impostare stili aggiuntivi per il testo del collegamento, incluso il colore del collegamento, selezionando la scheda **[!UICONTROL Stili]** nel pannello di destra.
