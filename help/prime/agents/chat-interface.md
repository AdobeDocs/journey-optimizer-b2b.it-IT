---
title: Interfaccia chat
description: Utilizza il pannello chat Assistente IA in Journey Optimizer B2B Prime per creare programmi, percorsi ed elenchi utilizzando il linguaggio naturale o il menu con barra (/).
badgeBeta: label="Beta" type="informative" tooltip="Questa funzione è attualmente in versione beta limitata"
autotag-review: '2026-06-12T22:46:23.441Z'
TQID: 'https://experienceleague.adobe.com/XyBLmqv63kNBcw-Jo4hKvUKIn2la7kac7-kTbNEU5aE'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: bef5003b-cad2-4f40-bdb2-a80426d52ef5
  - id: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2:
  - id: d270a788-eb1d-40ed-b74e-9158ed975b1f
  - id: a30218bb-f80a-4410-8ac4-b039e99a15b4
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 29d33656b0bd05e9fdf2cbdeb1f6e89d13c3d20e
workflow-type: tm+mt
source-wordcount: 869
ht-degree: 1%

---

# Interfaccia chat

Il pannello chat è incorporato in [!DNL Adobe Journey Optimizer B2B Prime]. È qui che interagisci con gli agenti di intelligenza artificiale utilizzando un linguaggio semplice per creare programmi e percorsi, creare e confrontare elenchi di persone, indagare sui lead, configurare il punteggio e altro ancora.

Per aprire il pannello, seleziona l&#39;icona _Assistente AI_ nel menu di navigazione a sinistra. L’intestazione del pannello presenta quattro controlli:

| Controllo | Descrizione |
|---------|-------------|
| **Nuova conversazione** | Avvia una nuova chat (cancella il thread corrente). |
| **Cronologia conversazioni** | Apri le conversazioni precedenti in modo da poterne riaprire una. |
| **Scambia pannelli** | Sposta il pannello chat sull&#39;altro lato dell&#39;area di lavoro. |
| **Comprimi** | Nascondi il pannello per dare più spazio all’area di lavoro. |

Nella parte inferiore del pannello si trova la finestra di messaggio in cui è possibile:

* Aggiungi un messaggio e premi **Invio** per inviare (**MAIUSC+INVIO** inserisce una nuova riga).
* Allega un file utilizzando l&#39;icona _Allega_ (formati supportati: `.txt`, `.md`, `.csv`, `.json`, `.xlsx`, `.docx`, `.pdf`). Utilizza i caricamenti CSV e fogli di calcolo per avviare un’importazione di lead.

## Chiedi all’assistente AI

Ci sono due modi ugualmente validi per ottenere lavoro fatto — non è mai necessario utilizzare il menu barra.

**Lingua naturale** — Digita la richiesta nel modo in cui l&#39;hai detta a un collega:

* _&quot;Crea un percorso di benvenuto per le nuove iscrizioni di prova.&quot;_
* _&quot;Perché john@acme.com non è entrato in questo percorso?&quot;_
* _&quot;Confrontare gli elenchi &#39;Partecipanti al webinar Q3&#39; e &#39;Account organizzazione&#39;.&quot;_

L&#39;agente associa il testo all&#39;abilità appropriata dietro le quinte ed esegue il flusso di lavoro appropriato.

**Menu barra (/)**. Digitare `/` per aprire un menu di tutte le operazioni che l&#39;assistente può eseguire. Questa funzione è utile quando desideri scoprire le funzionalità o passare direttamente a un flusso di lavoro noto.

## Menu barra (/)

Utilizzare `/` all&#39;inizio della finestra di messaggio o dopo uno spazio per aprire il menu. Mentre si continua a digitare, l&#39;elenco filtra per nome, descrizione o ID, ad esempio `/journey` si limita ai comandi relativi al percorso.

Utilizza **/** per spostarti tra le voci, **Invio** o **Scheda** da selezionare e **Esc** da ignorare. Puoi anche fare clic direttamente su una voce.

Le voci di menu sono raggruppate in sezioni etichettate:

| Sezione | Contiene |
|---------|----------|
| **Analizza** | Ricerche diagnostiche di sola lettura (ad esempio, indagini lead, query intento). |
| **Convalida** | Flussi di lavoro di controllo qualità e audit. |
| **Build** | Flussi di lavoro di creazione (programmi, percorsi, elenchi, punteggio). |
| **Importa** | Importazione lead CSV. |
| **Altro** | Qualsiasi cosa che non rientri nelle categorie precedenti. |

Il menu elenca anche **connettori** (ad esempio, _Sfoglia Marketo_ apre una finestra di dialogo del selettore) e **collegamenti di navigazione** che ti portano a una schermata dell&#39;area di lavoro.

### Seleziona una voce di menu

Quando si seleziona un&#39;abilità o un agente dal menu, nella finestra di messaggio viene inserito un prompt iniziale da modificare. Il messaggio è **not** inviato automaticamente. Se ad esempio si seleziona _Pianifica campagne_, verrà visualizzato _&quot;Pianifica un nuovo programma Marketo per [nome campagna]. Caricherò la descrizione.&quot;_ Compila i segnaposto tra parentesi quadre e premi **Invio** per inviare.

I connettori aprono un modale invece di inserire testo. Le scelte rapide per la navigazione ti portano direttamente a quella schermata nell’area di lavoro.

>[!NOTE]
>
>Alcuni comandi sono visualizzati in grigio e contrassegnati come _In arrivo_. Questi sono gestiti da flag di funzione e non sono ancora attivi per il tuo account; selezionarne uno non fa nulla. Il set disponibile dipende dalle feature abilitate.

## Abilità

Un&#39;abilità è un flusso di lavoro in pacchetti che l&#39;agente è in grado di eseguire, ovvero i blocchi predefiniti del menu `/` e le richieste in linguaggio naturale. Ogni abilità riunisce istruzioni dettagliate e gli strumenti specifici necessari per un lavoro (ad esempio, &quot;pubblicare un percorso&quot;, &quot;confrontare elenchi di due persone&quot;, &quot;creare un modello di punteggio&quot;).

Aspetti chiave da conoscere sulle competenze:

* **Le abilità hanno ambito di prodotto.** In AJO B2B Prime troverai competenze AJO B2B (percorsi, elenchi di persone, punteggi, canali, ottimizzazione del tempo di invio e così via). Alcune competenze sono esclusivamente per Marketo e un paio lavorano in entrambi i prodotti (importazione di lead, conoscenza del prodotto). Le abilità sono visibili solo nel punto in cui ti trovi.
* **Non è necessario memorizzare i nomi delle abilità.** Descrivi il tuo obiettivo e l&#39;agente sceglie l&#39;abilità corrispondente. Il menu `/` è un collegamento più veloce e individuabile agli stessi flussi di lavoro.
* **Alcune abilità leggono solo, altre cambiano le cose.** Le abilità investigative e di reporting (ad esempio, analisi dei lead, query di intento, report sul tempo di invio) consentono di leggere solo i dati. Creare e configurare abilità (ad esempio, creazione di percorsi, punteggio) creare o modificare dati.

## Richieste di follow-up

Dopo le risposte dell&#39;assistente, viene spesso visualizzata una riga di prompt di follow-up selezionabili in base alle proprie esigenze, ad esempio dopo la creazione di un percorso potrebbe offrire _&quot;Pubblica questo percorso&quot;_ o _&quot;Aggiungi un passaggio di attesa&quot;_. Fai clic su uno per continuare senza digitare. Questi sono solo suggerimenti; puoi sempre digitare il tuo messaggio successivo.

## Suggerimenti

* **Specificare con gli identificatori.** Durante le indagini o le modifiche, includi l’indirizzo e-mail, il nome della persona, il nome del percorso o il nome dell’elenco in modo che l’agente agisca sulla risorsa giusta.
* **Utilizza `/` per esplorare.** Se non si è sicuri di ciò che l&#39;assistente può fare, aprire il menu `/` e scorrere le categorie.
* **Modifica il prompt iniziale.** La selezione di un&#39;abilità ti offre un modello — sostituisci i segnaposto `[bracketed]` prima dell&#39;invio.
* **Carica prima per le importazioni.** Per un’importazione di lead, allega prima il file CSV, quindi descrivi cosa desideri farne.
* **Avvia una nuova conversazione** quando si passa a un&#39;attività non correlata, in modo che il contesto precedente non influisca sulla nuova richiesta.
