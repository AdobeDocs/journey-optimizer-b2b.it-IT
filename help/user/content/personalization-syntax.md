---
title: Sintassi di personalizzazione
description: Scopri la sintassi di personalizzazione basata su Handlebars in Journey Optimizer B2B edition, inclusi espressioni, helper, tipi letterali e regole di formattazione.
feature: Personalization, Content Design Tools
topic: Personalization
role: Developer
level: Intermediate
keywords: espressione, editor, sintassi, personalizzazione
source-git-commit: fee5bddcce11b3035da6ab93b18bcc7006b4b554
workflow-type: tm+mt
source-wordcount: '349'
ht-degree: 2%

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
  >La struttura degli attributi è definita in uno [schema XDM Adobe Experience Platform](https://experienceleague.adobe.com/it/docs/experience-platform/xdm/home){target="_blank"}.

* Gli identificatori possono essere qualsiasi carattere Unicode ad eccezione dei seguenti:

  ```
  Whitespace ! " # % & ' ( ) * + , . / ; < = > @ [ \ ] ^ ` { | } ~
  ```

* La sintassi fa distinzione tra maiuscole e minuscole.

* Le parole **true**, **false**, **null** e **undefined** sono consentite solo nella prima parte di un&#39;espressione di percorso.

* In Handlebars, i valori restituiti da {\{expression}\} sono _con escape HTML_. Se l&#39;espressione contiene `&`, l&#39;output con escape HTML restituito verrà generato come `&amp;`. Se non desiderate che Handlebars utilizzi il carattere escape per un valore, utilizzate il carattere +triple-stash_.

<!-- For example:

    If the value of the field `profile.person.name` is _Mark & Mary_, the `{\{profile.person.name}\}` value generates as `Mark &amp; Mary` and `{\{\{profile.person.name}}}` renders as `Mark & Mary`. -->

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

<!-- These block helpers are identified with a `#` preceding the helper name and require a matching closing `/`, of the same name. 

Blocks are expressions that have a block opening ( {\{# }\} ) and closing ( {\{/} } ). -->

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
