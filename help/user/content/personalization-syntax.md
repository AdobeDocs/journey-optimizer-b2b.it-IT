---
title: Sintassi di personalizzazione
description: Scopri la sintassi di personalizzazione basata su Handlebars in Journey Optimizer B2B edition, inclusi espressioni, helper, tipi letterali e regole di formattazione.
feature: Personalization, Content Design Tools
topic: Personalization
role: Developer
level: Intermediate
keywords: espressione, editor, sintassi, personalizzazione
exl-id: 91bbead6-aca0-4f39-9ab5-798b26ab81ee
autotag-review: '2026-05-27T16:18:02.498Z'
TQID: 'https://experienceleague.adobe.com/JWnXAAbCuZVLv4ZhWubpNsZ61xbYU7xtdOXkG9uoWis'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: e666e996-b2cf-4c45-8fc2-1c625212abab
subfeature_v2: id: bd3c685c-6c92-4a4a-becb-535cc25215de
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 955fac784a8f438ec2f9aaf66e9aaeefda58e2a7
workflow-type: tm+mt
source-wordcount: 361
ht-degree: 3%

---

# Sintassi di personalizzazione {#personalization-syntax}

Le espressioni nell&#39;editor [!DNL Journey Optimizer B2B Edition] [personalization](./personalization.md#personalization-editor) sono basate sulla sintassi del modello _Handlebars_. Utilizza un modello e un oggetto di input per generare HTML o altri formati di testo. I modelli Handlebars hanno l’aspetto di un testo normale con espressioni Handlebars incorporate.

Per ulteriori dettagli su Handlebars e sul suo funzionamento, consulta la [documentazione di HandlebarsJS](https://handlebarsjs.com/){target="_blank"}.

## Norme generali

Esempio di espressione semplice:

```
{{account.accountName}}
```

Dove:

* `account` è uno spazio dei nomi.
* `accountName` è un token composto da attributi.

  >[!NOTE]
  >
  >La struttura degli attributi è definita in uno [schema XDM Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/home){target="_blank"}.

* Gli identificatori possono essere qualsiasi carattere Unicode ad eccezione dei seguenti:

  ```
  Whitespace ! " # % & ' ( ) * + , . / ; < = > @ [ \ ] ^ ` { | } ~
  ```

* La sintassi fa distinzione tra maiuscole e minuscole.

* Le parole **true**, **false**, **null** e **undefined** sono consentite solo nella prima parte di un&#39;espressione di percorso.

* In Handlebars, i valori restituiti da {\{expression}\} sono _con escape HTML_. Se l&#39;espressione contiene `&`, l&#39;output con escape HTML restituito verrà generato come `&amp;`. Se non desiderate che Handlebars utilizzi il carattere escape per un valore, utilizzate il carattere +triple-stash_.

<!--
 For example:

    If the value of the field `profile.person.name` is _Mark & Mary_, the `{\{profile.person.name}\}` value generates as `Mark &amp; Mary` and `{\{\{profile.person.name}}}` renders as `Mark & Mary`. 
-->

* Per gli argomenti delle funzioni letterali, il parser del linguaggio del modello non supporta una singola barra rovesciata senza escape (`\`). Questo carattere deve essere preceduto da una barra rovesciata (`\`). Esempio:

  ```
  {%= regexGroup("abc@xyz.com","@(\\w+)", 1)%}
  ```

## Helper {#helpers-all}

Una funzione helper Handlebars è un semplice identificatore che può essere aggiunto con parametri. Ogni parametro è un&#39;espressione Handlebars. È possibile accedere a questi helper da qualsiasi contesto in un modello e-mail.

```sql
{{#each account.accountOrganization.annualRevenue.amount}}
    <li>{{this.name}}</li>
{{/each }}
```

<!--
 These block helpers are identified with a `#` preceding the helper name and require a matching closing `/`, of the same name.

Blocks are expressions that have a block opening ( {\{# }\} ) and closing ( {\{/} } ). 
-->

Per informazioni più dettagliate su queste funzioni, vedere [Funzioni helper](./personalization-helper-functions.md).

## Tipi letterali {#literal-types}

[!DNL Adobe Journey Optimizer B2B Edition] supporta i seguenti tipi letterali:

| Letterale | Definizione |
| ------- | ---------- |
| Stringa | Tipo di dati costituito da caratteri racchiusi tra virgolette doppie. <br>Esempi: `"prospect"`, `"jobs"`, `"articles"` |
| Booleano | Tipo di dati true o false. |
| Intero | Tipo di dati che rappresenta un numero intero. Può essere positivo, negativo o zero. <br>Esempi: `-201`, `0`, `412` |
| Array | Tipo di dati composto da un gruppo di altri valori letterali. Utilizza parentesi quadre per raggruppare e virgole per delimitare tra valori diversi. <br> **Nota:** non è possibile accedere direttamente alle proprietà degli elementi all&#39;interno di un array. <br> Esempi: `[1, 4, 7]`, `["US", "FR"]` |

>[!CAUTION]
>
>L&#39;utilizzo della variabile **xEvent** non è disponibile nelle espressioni di personalizzazione. Qualsiasi riferimento a xEvent genera errori di convalida.
