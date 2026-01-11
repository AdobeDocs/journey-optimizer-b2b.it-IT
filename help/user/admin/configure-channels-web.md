---
title: Configurazioni del canale web
description: Scopri come configurare le impostazioni del canale web per definire le proprietà web e le regole di corrispondenza delle pagine per la distribuzione dei contenuti in Journey Optimizer B2B edition.
feature: Setup, Channels
role: Admin
badgeBeta: label="Beta" type="informative" tooltip="Questa funzione è attualmente in versione beta limitata"
source-git-commit: 2f9b007df233cf8a233c3646bf691b7cff139f86
workflow-type: tm+mt
source-wordcount: '1064'
ht-degree: 0%

---

# Configurazioni del canale web

Una configurazione web è una proprietà web identificata da un URL in cui viene distribuito il contenuto. Può corrispondere a un singolo URL di pagina o a più pagine, in modo che le esperienze web possano fornire modifiche in una o più pagine web. Queste configurazioni sono necessarie affinché gli addetti al marketing possano [aggiungere nodi di azioni di personalizzazione Web nei percorsi](../content/web-experiences.md#create-a-web-experience) e [progettare le modifiche dell&#39;esperienza](../content/web-experience-design.md) per una campagna.

>[!BEGINSHADEBOX]

**Prerequisiti**

Per utilizzare i canali Web, il sito Web deve avere [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/it/docs/experience-platform/collection/js/js-overview) (`alloy.js`) implementato per l&#39;identificazione dei visitatori e la distribuzione dei contenuti. Verificare che la versione di Adobe Experience Platform Web SDK sia 2.16 o successiva.

La configurazione del canale web in Journey Optimizer B2B edition richiede le [autorizzazioni](../admin/user-management.md#b2b-product-permissions) seguenti:

* _[!UICONTROL Configurazioni canale]_ > _[!UICONTROL Gestione predefiniti messaggi]_ - Necessario per creare, aggiornare ed eliminare configurazioni canale web.
* _[!UICONTROL Configurazioni canale]_ > _[!UICONTROL Visualizza predefiniti messaggi]_ - Necessario per visualizzare le configurazioni del canale web.

>[!ENDSHADEBOX]

## Creare una configurazione del canale web

1. Nel menu di navigazione a sinistra, vai a **[!UICONTROL Amministrazione]** > **[!UICONTROL Canali]**.

1. In _[!UICONTROL Web]_ nel pannello di navigazione, seleziona **[!UICONTROL Configurazioni canale]**.

   ![Accedi alle configurazioni del canale web](./assets/config-web-channels.png){width="800" zoomable="yes"}

1. Fai clic su **[!UICONTROL Crea configurazione canale]** in alto a destra.

1. Immetti un **[!UICONTROL Nome]** (obbligatorio) e una **[!UICONTROL Descrizione]** (facoltativo) per la configurazione.

   >[!NOTE]
   >
   >I nomi devono iniziare con una lettera (A-Z) e possono contenere solo caratteri alfanumerici. È inoltre possibile utilizzare il carattere di sottolineatura `_`, il punto `.` e il trattino `-`.

1. Nella sezione **[!UICONTROL Impostazioni Web]** selezionare una delle opzioni seguenti:

   * **[!UICONTROL Pagina singola]** - Se desideri applicare le modifiche solo a una pagina singola, immetti o seleziona un **[!UICONTROL URL pagina]**.

     ![Selezione dell&#39;URL di una pagina per la configurazione di un canale Web a pagina singola](./assets/config-web-channel-create-single-page.png){width="600" zoomable="yes"}

   * **[!UICONTROL Regola di corrispondenza pagine]** - Per eseguire il targeting di più URL che corrispondono alla stessa regola, genera una [regola di corrispondenza pagine](#build-a-pages-matching-rule) e immetti un **[!UICONTROL URL predefinito per l&#39;authoring e l&#39;anteprima]**.

1. Fai clic su **[!UICONTROL Invia]** per salvare le modifiche.

Dopo aver salvato la configurazione, questa si trova nello stato _Bozza_ ed è disponibile per gli addetti al marketing quando utilizzano un canale web nei propri percorsi. Puoi continuare a modificare la configurazione finché rimane nello stato di bozza. È inoltre possibile eliminare una bozza di configurazione del canale Web facendo clic sull&#39;icona _Altro_ (**...**) accanto al nome e scegliendo **[!UICONTROL Elimina]**.

Non appena il canale web viene utilizzato in un percorso, passa allo stato _Attivo_. In questo stato, puoi modificare il nome e la descrizione della configurazione. Non è possibile modificare le impostazioni Web o eliminare la configurazione.

## Regole di corrispondenza pagine {#pages-matching-rule}

Durante la creazione di una configurazione Web, puoi generare una _[!UICONTROL regola di corrispondenza pagine]_ per eseguire il targeting di più URL che corrispondono alla stessa regola. Queste regole ti consentono di applicare le stesse modifiche al contenuto in più pagine.

Ad esempio, puoi applicare le modifiche a un banner principale in un intero sito web o aggiungere un’immagine superiore visualizzata in tutte le pagine dei prodotti.

### Creare una regola

1. Quando [crei una configurazione del canale Web](#create-a-web-channel-configuration), scegli **[!UICONTROL Regola di corrispondenza pagine]**.

1. Definisci i criteri per i campi **[!UICONTROL Dominio]** e **[!UICONTROL Pagina]** utilizzando i diversi operatori in ogni sezione per generare la regola.

   +++Operatori di dominio

   Utilizza i seguenti operatori per i domini corrispondenti in base al valore stringa immesso:

   | Operatore | Descrizione | Esempi |
   | --- | --- | --- |
   | [!UICONTROL Uguale a] | Corrispondenza esatta del dominio. | |
   | [!UICONTROL Inizia con] | Corrisponde a tutti i domini (inclusi i sottodomini) che iniziano con la stringa immessa. | `Starts with: dev` corrisponde a tutti i domini e i sottodomini che iniziano con `dev`, ad esempio `dev.example.com`, `dev.products.example.com` e `developer.example.com` |
   | [!UICONTROL Termina con] | Corrisponde a tutti i domini (inclusi i sottodomini) che terminano con la stringa immessa. | `Ends with: example.com` rileva tutti i domini e i sottodomini che terminano con `example.com`, ad esempio `stage.example.com`, `prod.example.com` e `myexample.com` |
   | [!UICONTROL Corrispondenza con caratteri jolly] | Consente di definire una corrispondenza con caratteri jolly al centro della stringa, ad esempio `dev.*.example.com`. Le regole di convalida richiedono che il valore contenga un solo carattere jolly (asterisco) quando l&#39;operatore _corrisponde al carattere jolly_. | `Wildcard matching: dev.*.example.com` corrisponde a domini come `dev.products.example.com`, `dev.mytest.products.example.com` e `dev.blog.example.com` |
   | [!UICONTROL Qualsiasi] | Corrisponde a tutti i domini. È utile quando si esegue il test di un particolare percorso tra domini diversi. | |

   +++

   +++Operatori di percorso

   Utilizza i seguenti operatori per associare i percorsi in base al valore stringa immesso:

   | Operatore | Descrizione | Esempi |
   | --- | --- | --- |
   | [!UICONTROL Uguale a] | Corrispondenza esatta del percorso. | |
   | [!UICONTROL Inizia con] | Corrisponde a tutti i percorsi (inclusi i percorsi secondari) che iniziano con la stringa. | |
   | [!UICONTROL Termina con] | Corrisponde a tutti i percorsi (inclusi i percorsi secondari) che terminano con la stringa. | |
   | [!UICONTROL Qualsiasi] | Corrisponde a tutti i percorsi. È utile quando esegui il targeting di tutti i percorsi sotto uno o più domini. | |
   | [!UICONTROL Corrispondenza con caratteri jolly] | Consente di definire un carattere jolly interno nel percorso, ad esempio `/products/*/detail`. Il carattere jolly `*` nel componente percorso corrisponde a qualsiasi sequenza di caratteri fino al primo carattere `/`.  E `/*/` corrisponde a qualsiasi sequenza di caratteri (inclusi i percorsi secondari). | `Wildcard matching: /products/*/detail` corrisponde a percorsi come `example.com/products/yoga/detail`, `example.com/products/surf/detail`, `example.com/products/tennis/detail` e `example.com/products/yoga/pants/detail` |
   | [!UICONTROL Contiene] | Il valore viene convertito in un carattere jolly, ad esempio `*mystring*`, e corrisponde a tutti i percorsi che contengono la sequenza di caratteri. | `Contains: product` corrisponde a tutti i percorsi che contengono la stringa `product`, ad esempio `example.com/products`, `example.com/yoga/perfproduct`, `example.com/surf/productdescription` e `example.com/home/product/page` |

   +++

   Ad esempio, per supportare le modifiche al contenuto in tutte le pagine della soluzione _LumaSecure_ del sito Web _Bodea_, selezionare **[!UICONTROL Dominio]** > **[!UICONTROL Inizia con]** > `bodea` e **[!UICONTROL Pagina]** > **[!UICONTROL Contiene]** > `lumasecure`.

   ![Definizione di una regola di corrispondenza pagine per una configurazione del canale Web](./assets/config-web-channel-pages-matching-rules.png){width="600" zoomable="yes"}

1. Se il tuo caso d&#39;uso richiede più regole, fai clic su **[!UICONTROL Aggiungi un&#39;altra regola di pagina]** e ripeti il passaggio precedente.

   * Puoi definire fino a 10 regole.

   * Utilizza gli operatori **[!UICONTROL Or]** o **[!UICONTROL Exclude]** tra le diverse regole.

     _[!UICONTROL Or]_ è l&#39;operatore predefinito per la definizione di più regole ed è utile per aggiungere più definizioni di criteri che possono trovare corrispondenza.

     _[!UICONTROL Escludi]_ è utile quando una delle pagine che corrispondono alla regola definita non deve essere sottoposta a targeting. Ad esempio, è possibile eseguire il targeting di tutte le `bodea.com` pagine che contengono `lumasecure`, ma escludendo le pagine di blog (ad esempio `bodea.com/blogs/lumasecure/latest-release`).

   ![Regole di corrispondenza pagine con esclusione](./assets/config-web-channel-pages-matching-rules-exclude.png){width="600" zoomable="yes"}

1. Immetti l&#39;**[!UICONTROL URL predefinito per l&#39;authoring e l&#39;anteprima]**.

   Questo passaggio assicura che le pagine generate o associate dalla regola abbiano un URL designato sia per la progettazione del contenuto dell’esperienza web che per l’anteprima.

## Duplicare un canale web

Puoi duplicare una configurazione di canale web esistente e modificarla per creare un nuovo canale web basato su uno esistente. Non è possibile modificare una configurazione di canale web attivo salvata nella libreria.

1. Fai clic sull&#39;icona _Altro menu_ (**...**) per la variante e scegli **[!UICONTROL Duplica]**.

   ![Fai clic sull&#39;icona altro menu per duplicare una configurazione di canale web esistente](./assets/config-web-channels-more-menu.png){width="450"}

   Questa azione crea un canale web duplicato con `_Copy_nnn` aggiunto al nome.

1. Fai clic sul nome del canale web duplicato per modificare i parametri.

   * Modifica il nome e la descrizione in modo che corrispondano allo scopo o agli elementi nella regola.
   * Se necessario, modifica l’URL della pagina singola.
   * Se necessario, modifica la regola di corrispondenza delle pagine in base alle tue esigenze.

1. Al termine della configurazione, fare clic su **[!UICONTROL Invia]**.
