---
source-git-commit: 1b4d8ad802265b537eb09439cfe34b97a3e61448
workflow-type: tm+mt
source-wordcount: '474'
ht-degree: 0%
---
# Istruzioni archivio GitHub Copilot

Quando le indicazioni generali nelle istruzioni Claude copiate sono in conflitto con le convenzioni specifiche per l’archivio o le istruzioni specifiche per il task, segui le istruzioni specifiche per l’archivio o per il task.

## Finalità

Utilizza queste istruzioni dell’archivio per lavorare con la documentazione in questo archivio. Le modifiche sono concise, tecnicamente accurate e allineate agli standard della documentazione di Adobe Experience League.

## Scrivi nello stile di documentazione dell’archivio

- Preferisci un linguaggio chiaro, diretto e incentrato sull&#39;utente.
- Mantieni le frasi brevi e digitalizzabili.
- Preferisci un linguaggio specifico e actionable al testo di marketing o di riempimento.
- Evita sezioni standard come &quot;Argomenti correlati&quot;, &quot;Domande frequenti&quot; o blocchi di riepilogo generici, a meno che non siano esplicitamente richiesti.
- Utilizza i collegamenti incrociati nel contesto invece dei blocchi di navigazione di fine pagina.
- Non aggiungere un elenco di riferimenti o una sezione &quot;Argomenti correlati&quot; alla fine di un articolo. Inserisci i collegamenti correlati pertinenti nel contenuto e spiega in che modo ogni destinazione si relaziona all’argomento corrente.
- Non utilizzare un linguaggio spaziale come &quot;sotto&quot; o &quot;sopra&quot; per descrivere l&#39;ordine dei documenti; utilizzare invece &quot;dopo&quot;, &quot;precedente&quot; o &quot;nella sezione successiva&quot;.

## Regole di denominazione della documentazione esterna

- Non utilizzare gli acronimi di prodotto Adobe nella documentazione esterna.
- La prima menzione dei nomi dei prodotti Adobe deve utilizzare il nome completo del prodotto, incluso &quot;Adobe&quot; quando appropriato.
- Utilizza i tag DNL per i nomi dei prodotti nel contenuto, ad esempio:
  - [!DNL Adobe Experience Platform]
  - [!DNL Adobe Journey Optimizer B2B Edition]
  - [!DNL Experience Platform]
  - [!DNL Journey Optimizer B2B Edition]
- Sostituisci i riferimenti solo acronimi come &quot;AEP&quot; e &quot;AJO B2B&quot; con i loro nomi completi di prodotto nella documentazione rivolta all’utente.
- Quando un prodotto viene introdotto per la prima volta, scrivi il nome completo. Le menzioni successive possono utilizzare il nome del prodotto più breve senza l’acronimo e mantenere il tag DNL quando il nome del prodotto viene visualizzato nell’interfaccia utente o nel testo della documentazione.
- Applica questi termini in modo coerente nel titolo della pagina, nel primo paragrafo e in tutte le etichette o collegamenti incrociati visibili ai lettori.

## Convenzioni di denominazione specifiche per l’archivio

- Utilizza &quot;Adobe Journey Optimizer B2B Edition&quot; per il nome del prodotto nei documenti rivolti all’utente.
- Utilizza &quot;Adobe Experience Platform&quot; per il nome della piattaforma nei documenti rivolti all’utente.
- Utilizza il nome del prodotto nella sua forma completa sulla prima menzione e quindi mantieni riferimenti successivi brevi e coerenti.
- Per i riferimenti ai set di dati, mantieni i nomi e gli ID dei set di dati effettivi esattamente come appaiono nel contratto di origine, anche quando includono prefissi legacy come `AJOB2B-`.

## Linee guida per la formattazione e il markdown

- Scrivi un Markdown valido al gusto di GitHub.
- Mantieni le intestazioni concise e descrittive.
- Utilizzare le tabelle solo quando aiutano i lettori a eseguire la scansione dei dettagli tecnici.
- Utilizza collegamenti relativi per riferimenti locali al repository.
- Mantieni i blocchi di codice e i percorsi dei campi esatti e copiabili.
- Evita riferimenti ridondanti ai prodotti nelle intestazioni, se il titolo della pagina li indica già.

## Elenco di controllo di convalida prima del completamento

- Assicurati che nei contenuti rivolti agli utenti non siano presenti acronimi per i prodotti Adobe.
- Assicurati che le prime menzioni utilizzino il nome completo del prodotto.
- Assicurati che i nomi dei prodotti siano contrassegnati con [!DNL ...] dove richiesto dallo stile dell&#39;archivio.
- Assicurati che il documento eviti problemi di linguaggio boilerplate e di linguaggio spaziale.
- Assicurati che il contenuto tecnico rimanga accurato e che i collegamenti incrociati nel contesto siano mantenuti.
