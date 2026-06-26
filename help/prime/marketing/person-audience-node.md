---
title: Nodo Percorso pubblico persona
description: Configura il nodo del pubblico della persona in Journey Optimizer B2B per specificare quali profili inserire in un percorso utilizzando elenchi di persone dinamici o tipi di pubblico basati su eventi.
badgeBeta: label="Beta" type="informative" tooltip="Questa funzione è attualmente in versione beta limitata"
autotag-review: '2026-06-16T21:21:01.614Z'
TQID: 'https://experienceleague.adobe.com/pk1NGg3M67oRieuCOZFdaguKl2bVkiZyEPVnJDTUBJs'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: a4b836d9-ffdd-4df3-a62a-f78b830cf059id: beb5f4be-cec3-471a-9db6-831a77dd3ac9id: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2: id: ba367494-9862-4596-bd6f-299c7e10a46bid: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 263e15040990a48475ffdd2b0b25d1cb557d5abf
workflow-type: tm+mt
source-wordcount: 225
ht-degree: 4%

---

# Nodo di pubblico della persona

Il nodo _audience persona_ specifica i profili di persona che entrano nel percorso. Quando [crei un percorso di persone](./person-journeys.md), il percorso inizia sempre con un nodo di pubblico di persone che ne definisce l&#39;input. Il nodo del pubblico della persona può avere uno dei due tipi di input del pubblico: un elenco dinamico di persone o un trigger di evento.

Se l&#39;elenco di persone dinamiche necessario per il percorso di persone non esiste già, [creare l&#39;elenco di persone](../audiences/people-lists.md#create-a-people-list) e quindi configurare il nodo di pubblico Persona.

_Per configurare il pubblico di percorso :_

1. Fai clic sul nodo **[!UICONTROL Pubblico persona]**.

   Questa azione visualizza le proprietà del nodo a destra.

   ![Nodo percorso di pubblico della persona](./assets/person-audience-node-properties.png){width="500" zoomable="yes"}

1. Utilizza una delle seguenti opzioni di configurazione del pubblico per il pubblico della persona:

   * **[!UICONTROL Elenco dinamico]** - Utilizza un elenco di persone dinamico basato su regole. Le regole di elenco vengono valutate in fase di runtime del percorso per qualificare i membri del percorso. Le persone che in seguito vengono escluse dall’elenco dinamico non vengono rimosse dal percorso. Vedi _[Elenchi dinamici](../audiences/people-lists.md#dynamic-lists)_.

   * **[!UICONTROL Pubblico evento]** - Utilizza un pubblico evento per definire il pubblico percorso in base agli eventi qualificanti. Definisci i membri del pubblico utilizzando il filtro del profilo della persona e attiva l’immissione del percorso utilizzando i criteri degli eventi. Consulta _[Tipi di pubblico basati su eventi](../audiences/event-based-audiences.md)_.

