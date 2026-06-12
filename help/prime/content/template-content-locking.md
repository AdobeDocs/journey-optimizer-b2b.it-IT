---
title: Blocco del contenuto per i modelli e-mail
description: Utilizza le impostazioni di governance in Journey Optimizer B2B Prime per bloccare il contenuto nei modelli e-mail a livello di struttura o di componente, controllando cosa possono modificare gli autori di e-mail.
badgeBeta: label="Beta" type="informative" tooltip="Questa funzione fa parte di una versione beta limitata."
source-git-commit: 2f19137465c71f2292d37bea5786533b1df6e286
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 0%

---


# Blocco del contenuto per i modelli e-mail

Il blocco del contenuto consente agli autori dei modelli di definire regole di governance che limitano le parti di un modello e-mail che possono essere modificate quando il modello viene utilizzato in un percorso. In questo modo i team del marchio e di conformità possono proteggere gli elementi chiave del design, ad esempio intestazioni, loghi e contenuti legali, e al contempo consentire ai team di marketing di personalizzare il messaggio all’interno della struttura approvata.

>[!NOTE]
>
>Il blocco dei contenuti è una funzione di governance a livello di editor. Controlla gli elementi che gli autori possono modificare nello spazio di progettazione delle e-mail, ma non impedisce le modifiche effettuate tramite l’API.

Solo gli utenti con l&#39;autorizzazione **[!UICONTROL Gestisci modelli di contenuto]** possono configurare le impostazioni di governance.

## Modalità di governance {#modes}

Quando abiliti la governance su un modello, seleziona una delle due modalità seguenti:

| Modalità | Descrizione |
| ---- | ----------- |
| **[!UICONTROL Blocco dei contenuti]** | Bloccare selettivamente strutture o componenti specifici. Le aree sbloccate rimangono modificabili dagli autori. |
| **[!UICONTROL Sola lettura]** | Blocca l&#39;intero modello. Gli autori possono applicarlo a un’e-mail ma non possono modificarne alcuna parte del contenuto. |

## Abilita governance {#enable}

1. Apri il modello nell’area di progettazione delle e-mail.
1. Nella barra a destra, fai clic sul componente **[!UICONTROL Body]** per selezionarlo.
1. Attiva **[!UICONTROL Governance]**.
1. Dal menu a discesa della modalità, selezionare **[!UICONTROL Blocco contenuto]** o **[!UICONTROL Sola lettura]**.

Se hai selezionato **[!UICONTROL Blocco contenuto]**, continua con il blocco di singoli elementi.

### Bloccare una struttura {#lock-structure}

1. Nell’area di lavoro, seleziona la struttura (layout colonne) da proteggere.
1. Nella barra a destra, abilita l&#39;interruttore **[!UICONTROL Blocca struttura]**.

Tutto il contenuto nidificato all’interno di una struttura bloccata viene bloccato automaticamente. Per consentire a un componente specifico all&#39;interno di una struttura bloccata di rimanere modificabile, seleziona il componente e abilita **[!UICONTROL Modificabile]** nella barra a destra.

### Bloccare un componente {#lock-component}

All’interno di una struttura modificabile, puoi bloccare singoli componenti di contenuto.

1. Seleziona il componente nell’area di lavoro.
1. Nella barra a destra, abilita l&#39;interruttore **[!UICONTROL Blocca contenuto]**.

### Consenti aggiunte di contenuto {#allow-additions}

Quando si utilizza la modalità **[!UICONTROL Blocco contenuto]**, è possibile consentire agli autori di aggiungere nuovi contenuti al modello mantenendo gli elementi bloccati protetti:

1. Abilita **[!UICONTROL Consenti aggiunta contenuto]**.
1. Scegli se gli autori possono aggiungere sia strutture che componenti di contenuto oppure solo componenti di contenuto.

## Identificare gli elementi bloccati {#identify}

La **[!UICONTROL struttura di navigazione]** nella barra a sinistra mostra icone di lucchetto e matita per consentire agli autori di identificare rapidamente ciò che possono e non possono modificare:

* Un&#39;icona **lucchetto** indica un elemento bloccato.
* Un&#39;icona di **matita** indica un elemento modificabile.

Gli elementi bloccati sono indicati visivamente nell’area di lavoro quando un autore apre il modello.

## Considerazioni

Le impostazioni di governance vengono salvate con il modello. Qualsiasi e-mail creata da un modello gestito eredita la relativa configurazione di blocco al momento dell’applicazione. L’aggiornamento delle impostazioni di governance su un modello non influisce sulle e-mail create in precedenza da esso.
