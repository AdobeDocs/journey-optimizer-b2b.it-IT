---
title: Nodo Percorso pubblico persona
description: Pagina Segnaposto per percorsi di persone.
autotag-review: '2026-06-16T21:21:01.614Z'
TQID: 'https://experienceleague.adobe.com/pk1NGg3M67oRieuCOZFdaguKl2bVkiZyEPVnJDTUBJs'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: a4b836d9-ffdd-4df3-a62a-f78b830cf059id: beb5f4be-cec3-471a-9db6-831a77dd3ac9id: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2: id: ba367494-9862-4596-bd6f-299c7e10a46bid: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 1cb68e8933d6b1abba3cc82f154344d1dde51818
workflow-type: tm+mt
source-wordcount: 197
ht-degree: 0%

---

# Nodo di pubblico della persona

Il nodo _audience persona_ specifica i profili di persona che entrano nel percorso. Quando [crei un percorso di persone](./person-journeys.md), il percorso inizia sempre con un nodo di pubblico di persone che ne definisce l&#39;input. Il nodo del pubblico della persona può avere uno dei due tipi di input del pubblico: un elenco di persone statiche o un elenco di persone dinamiche.

Se l&#39;elenco di persone necessario per il percorso di persone non esiste già, [creare l&#39;elenco di persone](../audiences/people-lists.md#create-a-people-list) e quindi configurare il nodo Pubblico persona.

## Impostare il pubblico

1. Fai clic sul nodo **[!UICONTROL Pubblico persona]**.

   Questa azione visualizza le proprietà del nodo a destra.

   ![Nodo percorso di pubblico della persona](./assets/person-audience-node-properties.png){width="500" zoomable="yes"}

1. Utilizza una delle seguenti opzioni di configurazione del pubblico per il pubblico della persona:

   * **[!UICONTROL Elenco dinamico]** - Utilizza un elenco di persone dinamico basato su regole. Le regole di elenco vengono valutate in fase di runtime del percorso per qualificare i membri del percorso. Le persone che in seguito vengono escluse dall’elenco dinamico non vengono rimosse dal percorso.

   * **[!UICONTROL Pubblico evento]** - Utilizza un pubblico evento per definire il pubblico percorso in base agli eventi qualificanti. Definisci i membri del pubblico utilizzando il filtro del profilo della persona e attiva l’immissione del percorso utilizzando i criteri degli eventi.

## Definire un pubblico per un evento

Aggiungi quando le informazioni provengono da PM.

