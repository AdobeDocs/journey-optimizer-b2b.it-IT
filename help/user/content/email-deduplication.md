---
title: Deduplica e-mail
description: Scopri come utilizzare la deduplicazione delle e-mail nei percorsi di account per impedire che la stessa e-mail venga inviata più volte allo stesso indirizzo e-mail.
feature: Account Journeys, Channels
topic: Content Management
role: User
level: Beginner, Intermediate
keywords: e-mail, deduplicazione, percorso, duplicato
exl-id: 93107acd-1cb2-4316-acfc-e32ab1e065ae
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: a4b836d9-ffdd-4df3-a62a-f78b830cf059
  - id: f01b5556-e951-40ba-8625-2e3001864f2b
subfeature_v2:
  - id: ff0c35fa-aa7e-4050-a37c-198fcacd09e6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
autotag-review: '2026-03-30T22:08:16.582Z'
source-git-commit: 8fe8318d7e1c63cbaa2749fc3928eb0a12967bd9
workflow-type: tm+mt
source-wordcount: 343
ht-degree: 1%

---

# Deduplicazione e-mail

Utilizza la deduplicazione delle e-mail nei percorsi di account per garantire che la stessa e-mail non venga inviata più volte allo stesso indirizzo e-mail all’interno di un percorso. Quando abiliti questa funzione, gli indirizzi e-mail duplicati vengono bloccati fino a quando il primo record con tale indirizzo e-mail non completa il percorso. Al termine di un percorso di account, una persona può qualificarsi per ricevere nuovamente le e-mail come parte di un nuovo account che accede al percorso.

## Quando utilizzare la deduplicazione e-mail

Esistono due scenari chiave in cui è necessario considerare l’abilitazione della deduplicazione delle e-mail:

* **L&#39;indirizzo e-mail non è utilizzato come identità in Real-Time CDP**. Lo stesso indirizzo e-mail potrebbe essere visualizzato in più profili di persona. Se tali profili duplicati sono idonei per lo stesso percorso e desideri impedire l’invio dell’e-mail più di una volta, abilita questa funzione.

* **Singola persona associata a più account** - Se il modello dati di Real-Time CDP consente a una singola persona di essere associata a più account e si desidera evitare di inviare la stessa e-mail due volte a tale persona quando più account (inclusi profili con lo stesso indirizzo e-mail) sono idonei per lo stesso percorso, abilitare questa funzione.

>[!NOTE]
>
>La deduplicazione delle e-mail si applica a livello di percorso. Se una persona con lo stesso indirizzo e-mail si qualifica per percorsi diversi, può comunque ricevere e-mail da ogni percorso.

## Abilitare la deduplicazione delle e-mail per un percorso

Per abilitare la deduplicazione delle e-mail per un percorso di account:

1. Apri un percorso di account.

1. Fai clic su **[!UICONTROL Altro]** (**...**) nell&#39;angolo superiore destro dell&#39;area di lavoro percorso.

   ![Area di lavoro di Percorso con menu Altro espanso che mostra l&#39;opzione Deduplicazione e-mail](./assets/email-deduplication-more-menu.png){width="450"}

1. Scegli **[!UICONTROL Deduplicazione e-mail]**.

1. Nella finestra di dialogo, seleziona la casella di controllo **[!UICONTROL Deduplicazione e-mail]**.

   ![Finestra di dialogo Deduplicazione e-mail con attivazione/disattivazione abilitata](./assets/email-deduplication-dialog.png){width="400"}

1. Fai clic su **[!UICONTROL Salva]**.

Quando la deduplicazione e-mail è abilitata, il percorso controlla ogni indirizzo e-mail prima di inviarlo. Se un record con lo stesso indirizzo e-mail è già stato inserito in quel nodo di percorso, la nuova voce viene bloccata fino a quando il primo record non completa il percorso.
