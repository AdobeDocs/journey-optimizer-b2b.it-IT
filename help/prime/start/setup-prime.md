---
title: Elenco di controllo per l'installazione
description: Completa le attività iniziali di configurazione per l’istanza Prime B2B di Journey Optimizer, inclusa la configurazione dell’accesso utente e l’infrastruttura di recapito messaggi e-mail.
autotag-review: '2026-06-12T23:06:52.179Z'
TQID: 'https://experienceleague.adobe.com/D8qXM-F4anA8IVYmdlaclUoxgTwqQptN36xYFpsuvHY'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: d6e625c1-468f-4d73-9f32-fd1edb87f96b
  - id: f467931a-9b22-4ca8-869f-adfbd64061ce
  - id: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2:
  - id: d270a788-eb1d-40ed-b74e-9158ed975b1f
  - id: f6df9def-cdf7-4728-9ec8-3f65716828c7
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: de83abd4ca48e2dfda8a1900f7c8074232bb9d8e
workflow-type: tm+mt
source-wordcount: 218
ht-degree: 11%

---

# Elenco di controllo per l’installazione

Completa queste attività per abilitare la funzionalità nell&#39;istanza [!DNL Journey Optimizer B2B Prime] con provisioning.

## Abilita accesso utente {#enable-user-access}

Una volta completato il provisioning e quando le sandbox sono associate, configura l&#39;accesso [!DNL Journey Optimizer B2B Edition] per il team e gli utenti.

<table>
<thead>
<tr>
<th colspan="2">Attività</th>
<th>Dettagli e istruzioni</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><strong>Fornisci l'accesso al prodotto e le autorizzazioni</strong> per gli utenti</td>
<td></td>
</tr>
<tr>
<td><img src="../../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casella di controllo per l'attività"/></td>
<td>Creazione di un profilo di prodotto Journey Optimizer B2B edition in Admin Console (solo configurazione una tantum/iniziale)</td>
<td><a href="./user-management.md#create-profile">Crea profilo</a></td>
</tr>
<tr>
<td><img src="../../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casella di controllo per l'attività"/></td>
<td>Aggiungere un gruppo di utenti in Admin Console</td>
<td><a href="./user-management.md#add-user-group">Aggiungi gruppo utenti</a></td>
</tr>
<tr>
<td><img src="../../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casella di controllo per l'attività"/></td>
<td>Modificare i ruoli incorporati o creare un ruolo personalizzato con le autorizzazioni del prodotto</td>
<td><a href="./user-management.md#edit-role-permissions">Modifica ruoli</a> <br/> <a href="./user-management.md#create-a-custom-role">Crea un ruolo personalizzato</a></td>
</tr>
<tr>
<td><img src="../../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casella di controllo per l'attività"/></td>
<td>Aggiungere utenti o gruppi ai ruoli in Adobe Experience Platform</td>
<td><a href="./user-management.md#add-users-to-a-role">Aggiungi utenti</a> <br/><a href="./user-management.md#add-user-groups-to-a-role">Aggiungi gruppi</a></td>
</tr>
</tbody>
</table>

## Recapitabilità delle e-mail {#email-deliverability}

Prima che gli esperti di marketing possano inviare e-mail dai percorsi, configura l’infrastruttura di invio per la tua organizzazione, inclusi la delega dei sottodomini, l’autenticazione e-mail e le impostazioni dei canali.

<table>
<thead>
<tr>
<th colspan="2">Attività</th>
<th>Dettagli e istruzioni</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><strong>Configurare il recapito messaggi e-mail e le impostazioni del canale</strong></td>
<td></td>
</tr>
<tr>
<td><img src="../../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casella di controllo per l'attività"/></td>
<td>Delegare un sottodominio ad Adobe (completamente delegato o CNAME)</td>
<td><a href="./admin/configuration-email-deliverability.md#delegate-fully-delegated">Delega completa</a> <br/> <a href="./admin/configuration-email-deliverability.md#delegate-cname">CNAME</a></td>
</tr>
<tr>
<td><img src="../../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casella di controllo per l'attività"/></td>
<td>Configurare DMARC per il sottodominio</td>
<td><a href="./admin/configuration-email-deliverability.md#configure-dmarc">Configurare DMARC</a></td>
</tr>
<tr>
<td><img src="../../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casella di controllo per l'attività"/></td>
<td>Revisione e assegnazione di un pool IP</td>
<td><a href="./admin/configuration-email-deliverability.md#review-ip-pool">Verifica pool IP</a></td>
</tr>
<tr>
<td><img src="../../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casella di controllo per l'attività"/></td>
<td>Creare una configurazione del canale e-mail</td>
<td><a href="./admin/configuration-email-deliverability.md#create-email-channel-configuration">Configurare il canale e-mail</a></td>
</tr>
</tbody>
