---
title: Funzioni Helper
description: Guida di riferimento per le funzioni di assistenza alla personalizzazione in Journey Optimizer B2B edition. Include sintassi ed esempi per stringhe, date, matematica e altro ancora.
feature: Personalization, Content Design Tools
topic: Personalization
role: Developer
level: Intermediate
keywords: espressione, editor, sintassi, personalizzazione
source-git-commit: fee5bddcce11b3035da6ab93b18bcc7006b4b554
workflow-type: tm+mt
source-wordcount: '4857'
ht-degree: 6%

---

# Funzioni Helper

Utilizza le funzioni helper nell’editor di personalizzazione per definire esperienze di contenuto personalizzate con precisione ed efficienza, manipolando i dati, eseguendo calcoli e formattando i contenuti. Esplora e sperimenta queste funzioni, operatori e collaboratori per scoprire come collaborano per aiutarti a creare percorsi personalizzati basati sui dati.

>[!AVAILABILITY]
>
>Sono disponibili funzioni di supporto per gli ambienti B2B edition di Joureny Optimizer con provisioning nell&#39;[architettura semplificata](../simplified-architecture.md).

## Funzioni di aggregazione

Utilizzare le funzioni di aggregazione per raggruppare più valori in modo da formare un singolo valore di riepilogo. È inoltre possibile utilizzare le funzioni array ed elenco per definire più facilmente le interazioni con array, elenchi e stringhe.

### media {#average}

Utilizzare la funzione `average` per restituire la media aritmetica di tutti i valori selezionati all&#39;interno dell&#39;array.

+++Sintassi

```sql
{%= average(array) %}
```

**Esempio**

L&#39;operazione seguente restituisce il prezzo medio di tutti gli ordini.

```sql
{%=average(orders.order.price)%}
```

+++

### conteggio {#count}

Utilizzare la funzione `count` per restituire il numero di elementi all&#39;interno dell&#39;array specificato.

+++Sintassi

```sql
{%= count(array) %}
```

**Esempio**

L&#39;operazione seguente restituisce il numero di ordini nell&#39;array.

```sql
{%= count(orders) %}
```

+++

### max {#max}

Utilizzare la funzione `max` per restituire il più grande di tutti i valori selezionati all&#39;interno dell&#39;array.

+++Sintassi

```sql
{%= max(array) %}
```

**Esempio**

L&#39;operazione seguente restituisce il prezzo più alto di tutti gli ordini.

```sql
{%=max(orders.order.price)%}
```

+++

### min {#min}

Utilizzare la funzione `min` per restituire il più piccolo di tutti i valori selezionati all&#39;interno dell&#39;array.

+++Sintassi

```sql
{%= min(array) %}
```

**Esempio**

L&#39;operazione seguente restituisce il prezzo più basso di tutti gli ordini.

```sql
{%=min(orders.order.price) %}
```

+++

### sum {#sum}

Utilizzare la funzione `sum` per restituire la somma di tutti i valori selezionati all&#39;interno dell&#39;array.

+++Sintassi

```sql
{%= sum(array) %}
```

**Esempio**

L&#39;operazione seguente restituisce la somma di tutti i prezzi degli ordini.

```sql
 {%=sum(orders.order.price)%}
```

+++

## Funzioni aritmetiche {#maths}

Utilizza le funzioni aritmetiche per eseguire calcoli di base sui valori.

### aggiungi {#add}

Utilizzare la funzione `+` (addizione) per trovare la somma di due espressioni di argomento.

+++Sintassi

```sql
{%= double + double %}
```

**Esempio**

L&#39;operazione seguente somma il prezzo di due prodotti diversi.

```sql
{%= product1.price + product2.price %}
```

+++

### moltiplicare {#multiply}

Utilizzare la funzione `*` (moltiplicazione) per trovare il prodotto di due espressioni di argomento.

+++Sintassi

```sql
{%= double * double %}
```

**Esempio**

L&#39;operazione seguente individua il prodotto dell&#39;inventario e il prezzo di un prodotto per trovare il valore lordo del prodotto.

```sql
{%= product.inventory * product.price %}
```

+++

### sottrarre {#substract}

Utilizzare la funzione `-` (sottrazione) per trovare la differenza tra due espressioni di argomento.

+++Sintassi

```sql
{%= double - double %}
```

**Esempio**

L&#39;operazione seguente rileva la differenza di prezzo tra due prodotti diversi.

```sql
{%= product1.price - product2.price %}
```

+++

### dividere {#divide}

Utilizzare la funzione `/` (divisione) per trovare il quoziente di due espressioni di argomento.

+++Sintassi

```sql
{%= double / double %}
```

**Esempio**

L&#39;operazione seguente consente di trovare il quoziente tra il totale dei prodotti venduti e il totale del denaro guadagnato per visualizzare il costo medio per articolo.

```sql
{%= totalProduct.price / totalProduct.sold %}
```

+++

### resto {#remainder}

Utilizzare la funzione `%` (resto) per trovare il resto dopo aver diviso le due espressioni di argomento.

+++Sintassi

```sql
{%= double % double %}
```

**Esempio**

L’operazione seguente verifica se l’età della persona è divisibile di cinque.

```sql
{%= person.age % 5 = 0 %}
```

+++

## Funzioni array ed elenco {#arrays}

Utilizzare queste funzioni per semplificare l&#39;interazione con array, elenchi e stringhe.

### countOnlyNull {#count-only-null}

Utilizzare la funzione `countOnlyNull` per contare il numero di valori Null in un elenco.

+++Sintassi

```sql
{%= countOnlyNull(array) %}
```

**Esempio**

```sql
{%= countOnlyNull([4,0,1,6,0,0]) %}
```

Restituisce 3.

+++

### countWithNull {#count-with-null}

Utilizzare la funzione `countWithNull` per contare tutti gli elementi di un elenco, inclusi i valori Null.

+++Sintassi

```sql
{%= countWithNull(array) %}
```

**Esempio**

```sql
{%= countOnlyNull([4,0,1,6,0,0]) %}
```

Restituisce 6.

+++

### distinct {#distinct}

Utilizzare la funzione `distinct` per ottenere valori da un array o da un elenco con valori duplicati rimossi.

+++Sintassi

```sql
{%= distinct(array) %}
```

**Esempio**

L&#39;operazione seguente specifica gli utenti che hanno effettuato ordini in più di un negozio.

```sql
{%= distinct(person.orders.storeId).count() > 1 %}
```

+++

### distinctCountWithNull {#distinct-count-with-null}

Utilizzare la funzione `distinctCountWithNull` per contare il numero di valori diversi in un elenco, inclusi i valori Null.

+++Sintassi

```sql
{%= distinctCountWithNull(array) %}
```

**Esempio**

```sql
{%= distinctCountWithNull([10,2,10,null]) %}
```

Restituisce 3.

+++

### testa {#head}

Utilizzare la funzione `head` per restituire il primo elemento di un array o di un elenco.

+++Sintassi

```sql
{%= head(array) %}
```

**Esempio**

L&#39;operazione seguente restituisce il primo dei primi cinque ordini con il prezzo più alto. Ulteriori informazioni sulla funzione `topN` sono disponibili nella sezione [first `n` in array](#first-n).

```sql
{%= head(topN(orders,price, 5)) %}
```

+++

### topN {#first-n}

La funzione `topN` ordina una matrice in ordine decrescente in base all&#39;espressione numerica specificata e restituisce i primi `N` elementi. Se la dimensione dell&#39;array è inferiore a `N`, restituisce l&#39;intero array ordinato.

+++Sintassi

```sql
{%= topN(array, value, amount) %}
```

| Argomento | Descrizione |
| --------- | ----------- |
| `{ARRAY}` | Matrice o elenco da ordinare. |
| `{VALUE}` | Proprietà utilizzata per ordinare l&#39;array o l&#39;elenco. |
| `{AMOUNT}` | Numero di elementi da restituire. |

**Esempio**

L&#39;operazione seguente restituisce i primi cinque ordini con il prezzo più basso.

```sql
{%= topN(orders,price, 5) %}
```

+++

### in {#in}

Utilizzare la funzione `in` per determinare se un elemento è membro di un array o di un elenco.

+++Sintassi

```sql
{%= in(value, array) %}
```

**Esempio**

L’operazione seguente definisce le persone il cui compleanno cade in marzo, giugno o settembre.

```sql
{%= in (person.birthMonth, [3, 6, 9]) %}
```

+++

### include {#includes}

Utilizzare la funzione `includes` per determinare se un array o un elenco contiene un elemento specifico.

+++Sintassi

```sql
{%= includes(array,item) %}
```

**Esempio**

L&#39;operazione seguente definisce le persone il cui colore preferito include il rosso.

```sql
{%= includes(person.favoriteColors,"red") %}
```

+++

### interseca {#intersects}

La funzione `intersects` viene utilizzata per determinare se due array o elenchi hanno almeno un membro comune.

+++Sintassi

```sql
{%= intersects(array1, array2) %}
```

**Esempio**

L&#39;operazione seguente definisce le persone i cui colori preferiti includono almeno uno rosso, blu o verde.

```sql
{%= intersects(person.favoriteColors,["red", "blue", "green"]) %}
```

+++

<!-- ## Intersection{#intersection}

The `intersection` function is used to determine the common members of two arrays or lists.

**Syntax**

```sql
intersection({ARRAY},{ARRAY})
```

**Example**

The following operation defines if person 1 and person 2 both have favorite colors of red, blue, and green.

```sql
intersection(person1.favoriteColors,person2.favoriteColors) = ["red", "blue", "green"]
```
-->

### bottomN {#last-n}

La funzione `bottomN` ordina una matrice in ordine crescente in base all&#39;espressione numerica specificata e restituisce i primi `N` elementi. Se la dimensione dell&#39;array è inferiore a `N`, restituisce l&#39;intero array ordinato.

+++Sintassi

```sql
{%= bottomN(array, value, amount) %}
```

| Argomento | Descrizione |
| --------- | ----------- | 
| `{ARRAY}` | Matrice o elenco da ordinare. |
| `{VALUE}` | Proprietà utilizzata per ordinare l&#39;array o l&#39;elenco. |
| `{AMOUNT}` | Numero di elementi da restituire. |

**Esempio**

L&#39;operazione seguente restituisce gli ultimi cinque ordini con il prezzo più alto.

```sql
{%= bottomN(orders,price, 5) %}
```

+++

### notIn {#notin}

Utilizzare la funzione `notIn` per determinare se un elemento non è un membro di un array o di un elenco.

>[!NOTE]
>
>La funzione `notIn` *also* assicura che nessuno dei due valori sia uguale a null. Pertanto, i risultati non sono una negazione esatta della funzione `in`.

+++Sintassi

```sql
{%= notIn(value, array) %}
```

**Esempio**

L’operazione seguente definisce le persone il cui compleanno non è in marzo, giugno o settembre.

```sql
{%= notIn(person.birthMonth ,[3, 6, 9]) %}
```

+++

### subsetOf {#subset}

Utilizzare la funzione `subsetOf` per determinare se un array specifico (array A) è un sottoinsieme di un altro array (array B). In altre parole, che tutti gli elementi nell&#39;array A sono elementi dell&#39;array B.

+++Sintassi

```sql
{%= subsetOf(array1, array2) %}
```

**Esempio**

L&#39;operazione seguente definisce le persone che hanno visitato tutte le loro città preferite.

```sql
{%= subsetOf(person.favoriteCities,person.visitedCities) %}
```

+++

### supersetOf {#superset}

Utilizzare la funzione `supersetOf` per determinare se un array specifico (array A) è un superset di un altro array (array B). In altre parole, l’array A contiene tutti gli elementi dell’array B.

+++Sintassi

```sql
{%= supersetOf(array1, array2) %}
```

**Esempio**

L’operazione seguente definisce le persone che hanno mangiato sushi e pizza almeno una volta.

```sql
{%= supersetOf(person.eatenFoods,["sushi", "pizza"]) %}
```

+++

## Funzioni data e ora {#date-time}

Utilizzare le funzioni di data e ora per eseguire operazioni di data e ora sui valori.

### addDays {#add-days}

La funzione `addDays` regola una data specificata di un numero specificato di giorni, utilizzando valori positivi per l&#39;incremento e valori negativi per la riduzione.

+++Sintassi

```sql
{%= addDays(date, number) %}
```

**Esempio**

* Input: `{%= addDays(stringToDate("2024-11-01T17:19:51Z"),10) %}`
* Output: `2024-11-11T17:19:51Z`

+++

### addHours {#add-hours}

La funzione `addHours` regola una data specificata di un numero specificato di ore, utilizzando valori positivi per l&#39;incremento e valori negativi per la riduzione.

+++Sintassi

```sql
{%= addHours(date, number) %}
```

**Esempio**

* Input: `{%= addHours(stringToDate("2024-11-01T17:19:51Z"),1) %}`
* Output: `2024-11-01T18:19:51Z`

+++

### addMinutes {#add-minutes}

La funzione `addMinutes` regola una data specificata di un numero specificato di minuti, utilizzando valori positivi per l&#39;incremento e valori negativi per la riduzione.

+++Sintassi

```sql
{%= addMinutes(date, number) %}
```

**Esempio**

* Input: `{%= addMinutes(stringToDate("2024-11-01T17:59:51Z"),10) %}`
* Output: `2024-11-01T18:09:51Z`

+++

### addMonths {#add-months}

La funzione `addMonths` regola una data specificata di un numero specificato di mesi, utilizzando valori positivi per l&#39;incremento e valori negativi per la riduzione.

+++Sintassi

```sql
{%= addMonths(date, number) %}
```

**Esempio**

* Input: `{%= addMonths(stringToDate("2024-11-01T17:19:51Z"),2) %}`
* Output: `2025-01-01T17:19:51Z`

+++

### addSeconds {#add-seconds}

La funzione `addSeconds` regola una data specificata di un numero specificato di secondi, utilizzando valori positivi per l&#39;incremento e valori negativi per la riduzione.

+++Sintassi

```sql
{%= addSeconds(date, number) %}
```

**Esempio**

* Input: `{%= addSeconds(stringToDate("2024-11-01T17:19:51Z"),10) %}`
* Output: `2024-11-01T17:20:01Z`

+++

### addYears {#add-years}

La funzione `addYears` regola una data specificata di un numero specificato di anni, utilizzando valori positivi per l&#39;incremento e valori negativi per la riduzione.

+++Sintassi

```sql
{%= addYears(date, number) %}
```

**Esempio**

* Input: `{%= addYears(stringToDate("2024-11-01T17:19:51Z"),2) %}`
* Output: `2026-11-01T17:19:51Z`

+++

### età {#age}

Utilizzare la funzione `age` per recuperare l&#39;età da una data specificata.

+++Sintassi

```sql
 {%= age(datetime) %}
```

<!--
**Example**

The following operation gets the value of the identity map for the key `example@example.com`.

```sql
 {%= age(datetime) %}
```
-->

+++

### ageInDays {#age-days}

La funzione `ageInDays` calcola il numero di giorni trascorsi tra la data specificata e la data corrente. Utilizza valori negativi per le date future e positivi per le date passate.

+++Sintassi

```sql
{%= ageInDays(date) %}
```

**Esempio**

currentDate = 2025-01-07T12:17:10.720122+05:30 (Asia/Calcutta)

* Input: `{%= ageInDays(stringToDate("2025-01-01T17:19:51Z"))%}`
* Output: `5`

+++

### ageInMonths {#age-months}

La funzione `ageInMonths` calcola il numero di mesi trascorsi tra la data specificata e la data corrente. Utilizza valori negativi per le date future e positivi per le date passate.

+++Sintassi

```sql
{%= ageInMonths(date) %}
```

**Esempio**

currentDate = 2025-01-07T12:22:46.993748+05:30(Asia/Calcutta)

* Input: `{%=ageInMonths(stringToDate("2024-01-01T00:00:00Z"))%}`
* Output: `12`

+++

### compareDates {#compare-dates}

La funzione `compareDates` confronta la prima data di input con l&#39;altra. Restituisce 0 se data1 è uguale a data2, -1 se data1 precede data2 e 1 se data1 segue data2.

+++Sintassi

```sql
{%= compareDates(date1, date2) %}
```

**Esempio**

* Input: `{%=compareDates(stringToDate("2024-12-02T00:00:00Z"), stringToDate("2024-12-03T00:00:00Z"))%}`
* Output: `-1`

+++

### convertZonedDateTime {#convert-zoned-date-time}

La funzione `convertZonedDateTime` converte una data/ora in un determinato fuso orario.

+++Sintassi

```sql
{%= convertZonedDateTime(dateTime, timezone) %}
```

**Esempio**

* Input: `{%=convertZonedDateTime(stringToDate("2019-02-19T08:09:00Z"), "Asia/Tehran")%}`
* Output: `2019-02-19T11:39+03:30[Asia/Tehran]`

+++

### currentTimeInMillis {#current-time}

Utilizzare la funzione `currentTimeInMillis` per recuperare il tempo corrente in millisecondi epoca.

+++Sintassi

```sql
{%= currentTimeInMillis() %}
```

<!--
**Example**

The following operation gets all the keys for the map `identityMap`.

```sql
{%= keys(identityMap) %}
```
-->

+++

### dateDiff {#date-diff}

Utilizzare la funzione `dateDiff` per recuperare la differenza tra due date in un numero di giorni.

+++Sintassi

```sql
{%= dateDiff(datetime,datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

+++

### dayOfMonth {#day-month}

`dayOfMonth` restituisce il numero che rappresenta il giorno del mese.

+++Sintassi

```sql
{%= dayOfMonth(datetime) %}
```

**Esempio**

* Input: `{%= dayOfMonth(stringToDate("2024-11-05T17:19:51Z")) %}`
* Output: `5`

+++

### DayOfWeek {#day-week}

Utilizzare la funzione `dayOfWeek` per recuperare il giorno della settimana.

+++Sintassi

```sql
{%= dayOfWeek(datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

+++

### dayOfYear {#day-year}

Utilizzare la funzione `dayOfYear` per recuperare il giorno dell&#39;anno.

+++Sintassi

```sql
{%= dayOfYear(datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

+++

### diffInSeconds {#diff-seconds}

La funzione `diffInSeconds` restituisce la differenza tra due date in secondi.

+++Sintassi

```sql
{%= diffInSeconds(endDate, startDate) %}
```

**Esempio**

* Input: `{%=diffInSeconds(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2024-11-01T17:19:01Z"))%}`
* Output: `50`

+++

### extractHours {#extract-hours}

La funzione `extractHours` estrae il componente Ora da un determinato timestamp.

+++Sintassi

```sql
{%= extractHours(date) %}
```

**Esempio**

* Input: `{%= extractHours(stringToDate("2024-11-01T17:19:51Z"))%}`
* Output: `17`

+++

### extractMinutes {#extract-minutes}

La funzione `extractMinutes` estrae il componente del minuto da un determinato timestamp.

+++Sintassi

```sql
{%= extractMinutes(date) %}
```

**Esempio**

* Input: `{%= extractMinutes(stringToDate("2024-11-01T17:19:51Z"))%}`
* Output: `19`

+++

### extractMonths {#extract-months}

La funzione `extractMonth` estrae il componente mese da un determinato timestamp.

+++Sintassi

```sql
{%= extractMonths(date) %}
```

**Esempio**

* Input: `{%=extractMonth(stringToDate("2024-11-01T17:19:51Z"))%}`
* Output: `11`

+++

### extractSeconds {#extract-seconds}

La funzione `extractSeconds` estrae il secondo componente da un determinato timestamp.

+++Sintassi

```sql
{%= extractSeconds(date) %}
```

**Esempio**

* Input: `{%=extractSeconds(stringToDate("2024-11-01T17:19:51Z"))%}`
* Output: `51`

+++

### formatDate {#format-date}

Utilizzare la funzione `formatDate` per formattare un valore di data e ora. Il formato deve essere un pattern Java `DateTimeFormat` valido.

+++Sintassi

```sql
{%= formatDate(datetime, format) %}
```

Dove la prima stringa è l’attributo data e il secondo valore è il modo in cui desideri che la data venga convertita e visualizzata.

>[!NOTE]
>
> Se un modello di data non è valido, la data viene riportata nel formato standard ISO.
>
> Puoi utilizzare le funzioni di formattazione della data Java riepilogate nella [documentazione di Oracle](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html){_blank}

**Esempio**

L&#39;operazione seguente restituisce la data nel formato seguente: MM/GG/AA.

```sql
{%= formatDate(profile.timeSeriesEvents._mobile.hotelBookingDetails.bookingDate, "MM/dd/YY") %}
```

+++

#### Caratteri pattern {#pattern-characters}

Alcune lettere di serie possono avere un aspetto simile, ma rappresentano concetti diversi.

| Pattern | Significato | Esempio (per `2023-12-31T10:15:30Z`) |
|---------|---------|--------------------------------------|
| `y` | Anno solare (anno standard) | `2023` |
| `Y` | Anno basato sulla settimana (ISO 8601). Può differire nei limiti dell&#39;anno. | `2024` (31 dicembre 2023 cade nella prima settimana del 2024) |
| `M` | Mese dell&#39;anno (1-12 o testo simile a `Jan`, `January`) | `12` o `Dec` |
| `m` | Minuto dell&#39;ora (0-59) | `15` |
| `d` | Giorno del mese (1-31) | `31` |
| `D` | Giorno dell’anno (1-366) | `365` |

#### Formattare la data con il supporto delle impostazioni internazionali {#format-date-locale}

È possibile utilizzare la funzione `formatDate` per formattare un valore di data e ora nella corrispondente rappresentazione sensibile alla lingua, ad esempio per le impostazioni locali desiderate. Il formato deve essere un pattern Java `DateTimeFormat` valido.

+++Sintassi

```sql
{%= formatDate(datetime, format, locale) %}
```

Dove la prima stringa è l’attributo data, il secondo valore corrisponde al modo in cui la data deve essere convertita e visualizzata e il terzo valore rappresenta le impostazioni locali in formato stringa.

>[!NOTE]
>
> Se un modello di data non è valido, la data viene riportata nel formato standard ISO.
>
> Puoi utilizzare le funzioni di formattazione della data Java come riepilogato nella [documentazione di Oracle](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html).
>
> Puoi utilizzare la formattazione e le impostazioni internazionali valide come riepilogato nella [documentazione di Oracle](https://docs.oracle.com/javase/8/docs/api/java/util/Locale.html) e nelle [impostazioni internazionali supportate](https://www.oracle.com/java/technologies/javase/jdk11-suported-locales.html).

**Esempio**

L&#39;operazione seguente restituisce la data nel formato seguente: MM/gg/AA e impostazioni internazionali FRANCE.

```sql
{%= formatDate(profile.timeSeriesEvents._mobile.hotelBookingDetails.bookingDate, "MM/dd/YY", "fr_FR") %}
```

+++

### getCurrentZonedDateTime {#get-current-zoned-date-time}

La funzione `getCurrentZonedDateTime` restituisce la data e l&#39;ora correnti con le informazioni sul fuso orario.

+++Sintassi

```sql
{%= getCurrentZonedDateTime() %}
```

**Esempio**

* Input: `{%= getCurrentZonedDateTime() %}`
* Output: `2024-12-06T17:22:02.281067+05:30[Asia/Kolkata]`

+++

### diffInHours {#hours-difference}

La funzione `diffInHours` restituisce la differenza tra due date in termini di ore.

+++Sintassi

```sql
{%= diffInHours(endDate, startDate) %}
```

**Esempio**

* Input: `{%= diffInHours(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2024-11-01T07:19:51Z"))%}`
* Output: `10`

+++

### diffInMinutes {#diff-minutes}

La funzione `diffInMinutes` restituisce la differenza tra due date in termini di minuti.

+++Sintassi

```sql
{%= diffInMinutes(endDate, startDate) %}
```

**Esempio**

* Input: `{%= diffInMinutes(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2024-11-01T16:19:51Z"))%}`
* Output: `60`

+++

### diffInMonths {#months-difference}

La funzione `diffInMonths` restituisce la differenza tra due date in termini di mesi.

+++Sintassi

```sql
{%= diffInMonths(endDate, startDate) %}
```

**Esempio**

* Input: `{%=diffInMonths(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2024-08-01T17:19:51Z"))%}`
* Output: `3`

+++

### setDays {#set-days}

Utilizzare la funzione `setDays` per impostare il giorno del mese per la data/ora specificata.

+++Sintassi

```sql
{%= setDays(datetime, day) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

+++

### setHours {#set-hours}

Utilizzare la funzione `setHours` per impostare l&#39;ora della data/ora.

+++Sintassi

```sql
{%= setHours(datetime, hour) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

+++

### toDateTime {#string-to-date-time}

La funzione `toDateTime` converte la stringa in data. In caso di input non valido, restituisce la data epoca come output.

+++Sintassi

```sql
{%= toDateTime(string, string) %}
```

**Esempio**

* Input: `{%=toDateTime("2024-11-01T17:19:51Z")%}`
* Output: `2024-11-01T17:19:51Z`

+++

### toUTC {#to-utc}

Utilizzare la funzione `toUTC` per convertire un datetime in UTC.

+++Sintassi

```sql
{%= toUTC(datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

+++

### truncateToStartOfDay {#truncate-day}

Utilizzare la funzione `truncateToStartOfDay` per modificare una data/ora specificata impostandola all&#39;inizio del giorno con ora 00:00.

+++Sintassi

```sql
{%= truncateToStartOfDay(date) %}
```

**Esempio**

* Input: `{%= truncateToStartOfDay(stringToDate("2024-11-01T17:19:51Z")) %}`
* Output: `2024-11-01T00:00Z`

+++

### truncateToStartOfQuarter {#truncate-quarter}

Utilizzare la funzione `truncateToStartOfQuarter` per troncare una data/ora al primo giorno del trimestre (ad esempio 1 gennaio, 1 aprile, 1 luglio, 1 ottobre) alle 00:00.

+++Sintassi

```sql
{%= truncateToStartOfQuarter(dateTime) %}
```

**Esempio**

* Input: `{%=truncateToStartOfQuarter(stringToDate("2024-11-01T17:19:51Z"))%}`
* Output: `2024-10-01T00:00Z`

+++

### truncateToStartOfWeek {#truncate-week}

La funzione `truncateToStartOfWeek` modifica una data/ora specificata impostandola all&#39;inizio della settimana (lunedì alle 00:00).

+++Sintassi

```sql
{%= truncateToStartOfWeek(dateTime) %}
```

**Esempio**

* Input: `{%= truncateToStartOfWeek(stringToDate("2024-11-19T17:19:51Z"))%} // tuesday`
* Output: `2024-11-18T00:00Z // monday`

+++

### truncateToStartOfYear {#truncate-year}

Utilizzare la funzione `truncateToStartOfYear` per modificare una data/ora specificata troncandola al primo giorno dell&#39;anno (1 gennaio) alle 00:00.

+++Sintassi

```sql
{%= truncateToStartOfYear(dateTime) %}
```

**Esempio**

* Input: `{%=truncateToStartOfYear(stringToDate("2024-11-01T17:19:51Z"))%}`
* Output: `2024-01-01T00:00Z`

+++

### weekOfYear {#week-of-year}

Utilizzare la funzione `weekOfYear` per recuperare la settimana dell&#39;anno.

+++Sintassi

```sql
{%= weekOfYear(datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

+++

### diffInYears {#diff-years}

Utilizzare la funzione `diffInYears` per restituire la differenza tra due date in termini di anni.

+++Sintassi

```sql
{%= diffInYears(endDate, startDate) %}: int
```

**Esempio**

* Input: `{%=diffInYears(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2019-10-01T17:19:51Z"))%}`
* Output: `5`

+++

## Funzioni dell&#39;operatore {#operators}

Utilizza le funzioni booleane e di confronto per eseguire valutazioni logiche.

### e {#and}

La funzione `and` viene utilizzata per creare una congiunzione logica.

+++Sintassi

```sql
{%= query1 and query2 %}
```

**Esempio**

L’operazione seguente restituisce tutte le persone con paese di origine (Francia) e anno di nascita (1985).

```sql
{%= profile.homeAddress.country = "France" and profile.person.birthYear = 1985 %}
```

+++

### oppure {#or}

La funzione `or` viene utilizzata per creare una disgiunzione logica.

+++Sintassi

```sql
{%= query1 or query2 %}
```

**Esempio**

L’operazione seguente restituisce tutte le persone con paese di origine (Francia) o anno di nascita (1985).

```sql
{%= profile.homeAddress.country = "France" or profile.person.birthYear = 1985 %}
```

+++

<!--
## Not{#not}

The `not` (or `!`) function is used to create a logical negation.

**Syntax**

```sql
not ({QUERY})
!({QUERY})
```

**Example**

The following operation will return all people who do not have their home country as Canada.

```sql
not (homeAddress.countryISO = "CA")
```
-->

### uguale a {#operator-equals}

La funzione `=` (è uguale a) controlla se un valore o un&#39;espressione è uguale a un altro valore o espressione.

+++Sintassi

```sql
{%= expression = value %}
```

**Esempio**

L&#39;operazione seguente verifica se il paese di residenza è la Francia.

```sql
{%= profile.homeAddress.country = "France" %}
```

+++

### non uguale {#notequal}

La funzione `!=` (diverso da) controlla se un valore o un&#39;espressione è **diverso** uguale a un altro valore o espressione.

+++Sintassi

```sql
{%= expression != value %}
```

**Esempio**

L&#39;operazione seguente verifica se l&#39;indirizzo del paese di origine non è la Francia.

```sql
{%= profile.homeAddress.country != "France" %}
```

+++

### maggiore di {#greaterthan}

Utilizzare la funzione `>` (maggiore di) per verificare se il primo valore è maggiore del secondo valore.

+++Sintassi

```sql
{%= expression1 > expression2 %}
```

**Esempio**

L&#39;operazione seguente definisce le persone nate rigorosamente dopo il 1970.

```sql
{%= profile.person.birthYear > 1970 %}
```

+++

### maggiore o uguale a {#greaterthanorequal}

Utilizzare la funzione `>=` (maggiore o uguale a) per verificare se il primo valore è maggiore o uguale al secondo valore.

+++Sintassi

```sql
{%= expression1 >= expression2 %}
```

**Esempio**

L&#39;operazione seguente definisce le persone nate nel 1970 o dopo di esso.

```sql
{%= profile.person.birthYear >= 1970 %}
```

+++

### minore di {#lessthan}

Utilizzare la funzione di confronto `<` (minore di) per verificare se il primo valore è minore del secondo valore.

+++Sintassi

```sql
{%= expression1 < expression2 %}
```

**Esempio**

L&#39;operazione seguente definisce le persone nate prima del 2000.

```sql
{%= profile.person.birthYear < 2000 %}
```

+++

### minore o uguale a{#lessthanorequal}

Utilizzare la funzione di confronto `<=` (minore o uguale a) per verificare se il primo valore è minore o uguale al secondo valore.

+++Sintassi

```sql
{%= expression1 <= expression2 %}
```

**Esempio**

L&#39;operazione seguente definisce le persone nate nel 2000 o prima.

```sql
{%= profile.person.birthYear <= 2000 %}
```

+++

## Funzioni dinamiche {#dynamic-helpers}

Utilizza le funzioni di assistenza dinamica per utilizzare valutazioni condizionali, iterazioni e assegnazioni di variabili per la personalizzazione dinamica.

### Valore di fallback predefinito {#default-value}

L&#39;helper `Default Fallback Value` viene utilizzato per restituire un valore di fallback predefinito se un attributo è vuoto o nullo. Questo meccanismo funziona per gli attributi del profilo e gli eventi di Percorso.

+++Sintassi

```sql
Hello {%=profile.personalEmail.name.firstName ?: "there" %}!
```

In questo esempio, il valore `there` viene visualizzato se l&#39;attributo `firstName` di questo profilo è vuoto o nullo.

+++

### if (condizioni) {#if-function}

L&#39;helper `if` viene utilizzato per definire un blocco condizionale.
Se la valutazione dell’espressione restituisce true, il blocco viene renderizzato, altrimenti viene saltato.

+++Sintassi

```sql
{%#if contains(account.accountOrganization.primaryEmailDomain, ".edu")%}
<a href="https://www.adobe.com/academia">Check out this link</a>
```

Dopo l&#39;helper `if`, è possibile immettere un&#39;istruzione `else` per specificare un blocco di codice da eseguire, se la stessa condizione è false.
L&#39;istruzione `elseif` specifica una nuova condizione da verificare se la prima istruzione restituisce false.


**Formato**

```sql
{
    {
        {%#if condition1%} element_1 
        {%else if condition2%} element_2 
        {%else%} default_element 
        {%/if%}
    }
}
```

<!-- 
**Examples**

* **Render different store links based on conditional expressions**

    ```sql
    {%#if profile.homeAddress.countryCode = "FR"%}
    <a href="https://www.somedomain.com/fr">Consultez notre catalogue</a>
    {%else%}
    <a href="https://www.somedomain.com/en">Checkout our catalogue</a>
    {%/if%}
    ```

* **Determine email address extension**

    ```sql
    {%#if contains(profile.personalEmail.address, ".edu")%}
    <a href="https://www.adobe.com/academia">Checkout our page for Academia personals</a>
    {%else if contains(profile.personalEmail.address, ".org")%}
    <a href="https://www.adobe.com/orgs">Checkout our page for Non Profits</a>
    {%else%}
    <a href="https://www.adobe.com/users">Checkout our page</a>
    {%/if%}
    ```

* **Add a conditional link**

    The following operation adds a link to the `www.adobe.com/academia` website for profiles with '.edu' email addresses only, the `www.adobe.com/org` website for profiles with '.org' email addresses, and the default URL `www.adobe.com/users` for all other profiles:

    ```sql
    {%#if contains(profile.personalEmail.address, ".edu")%}
    <a href="https://www.adobe.com/academia">Checkout our page for Academia personals</a>
    {%else if contains(profile.personalEmail.address, ".org")%}
    <a href="https://www.adobe.com/orgs">Checkout our page for Non Profits</a>
    {%else%}
    <a href="https://www.adobe.com/users">Checkout our page</a>
    {%/if%}
    ```

* **Conditional content based on audience membership**

    ```sql
    {%#if profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8b").status = "existing"%}
    Hi! Esteemed gold member. <a href="https://www.somedomain.com/gold">Checkout your exclusive perks </a>
    {%else if profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8c").status = "existing"%}
    Hi! Esteemed silver member. <a href="https://www.somedomain.com/silver">Checkout your exclusive perks </a>
    {%/if%}
    ```
-->

+++

### salvo {#unless}

Utilizzare l&#39;helper `unless` per definire un blocco condizionale. In opposizione all&#39;helper `if`, se la valutazione dell&#39;espressione restituisce false, viene eseguito il rendering del blocco.

+++Sintassi

```sql
{%#unless unlessCondition%} element_1 {%else%} default_element {%/unless%}
```

**Esempio**

Esegui il rendering di alcuni contenuti in base all’estensione dell’indirizzo e-mail:

```sql
{%#unless endsWith(account.accountOrganization.primaryEmailDomain}, ".edu")%}
Some Normal Content
{%else%}
Some edu specific content
{%/unless%}
```

+++

### ogni {#each}

Utilizza l&#39;helper `each` per eseguire l&#39;iterazione su un array.

La struttura helper è ```{{#each ArrayName}}``` YourContent `{{/each}}`

È possibile utilizzare la parola chiave `this` all&#39;interno del blocco per fare riferimento ai singoli elementi dell&#39;array. Utilizzare `{{@index}}` per eseguire il rendering dell&#39;indice dell&#39;elemento dell&#39;array.

+++Sintassi

```sql
{{#each profile.productsInCart}}
    <li>{{this.name}}</li>
{{/each}}
```

**Esempio**

```sql
{{#each profile.homeAddress.city}}
  {{@index}} : {{this}}<br>
{{/each}}
```

**Esempio**

Esegui il rendering di un elenco di prodotti che questo utente ha nel carrello:

```sql
{{#each profile.products as |product|}}
    <li>{{product.productName}} {{product.productRating}}</li>
{{/each}}
```

+++

### con {#with}

Utilizza l&#39;helper `with` per modificare il token di valutazione della parte modello.

+++Sintassi

```sql
{{#with profile.person.name}}
{{this.firstName}} {{this.lastName}}
{{/with}}
```

L&#39;helper `with` è utile anche per definire una variabile di collegamento.

**Esempio**

Utilizza `with` per l&#39;alias di nomi di variabili lunghi a nomi più brevi:

```sql
{{#with profile.person.name as |name|}}
 Hi {{name.firstName}} {{name.lastName}}!
 Checkout our trending products for today!
{{/with}}
```

+++

### let {#let}

La funzione `let` consente di archiviare un&#39;espressione come variabile da utilizzare successivamente in una query.

+++Sintassi

```sql
{% let variable = expression %} {{variable}}
```

**Esempio**

L&#39;esempio seguente consente di calcolare la somma totale dei prezzi dei prodotti nel carrello con prezzi compresi tra 100 e 1000.

```sql
{% let sum = 0%}
    {{#each profile.productsInCart as |p|}}
        {%#if p.price>100 and p.price<1000%}
            {%let sum = sum + p.price %}
        {%/if%}
    {{/each}}
{{sum}}
```

+++

## Metadati di esecuzione {#execution-metadata}

>[!AVAILABILITY]
>
>Questa funzionalità è a disponibilità limitata. Per ottenere l’accesso, contatta il tuo rappresentante Adobe.

Utilizzare `executionMetadata` per acquisire e archiviare coppie chiave-valore personalizzate in modo dinamico nel contesto di esecuzione del messaggio.

Con questa funzione, puoi aggiungere informazioni contestuali a qualsiasi azione nativa delle campagne o dei percorsi. Utilizzalo per esportare i dati contestuali di consegna in tempo reale verso sistemi esterni per vari scopi, come tracciamento, analisi, personalizzazione ed elaborazione a valle.

>[!NOTE]
>
>Le azioni personalizzate non supportano la funzione `executionMetadata`.

Ad esempio, puoi utilizzare l&#39;helper `executionMetadata` per aggiungere un ID specifico a ciascuna consegna inviata a ciascun profilo. Queste informazioni vengono generate durante il runtime e i metadati di esecuzione arricchiti possono quindi essere esportati per la riconciliazione a valle con una piattaforma di reporting esterna.

+++Sintassi

```
{{executionMetadata key="your_key" value="your_value"}}
```

In questa sintassi, `key` fa riferimento al nome dei metadati e `value` sono i metadati da mantenere.

**Come funziona**

Seleziona qualsiasi elemento dal contenuto del canale all&#39;interno di una campagna o di un percorso e, utilizzando l&#39;editor di personalizzazione, aggiungi l&#39;helper `executionMetadata` a questo elemento.

>[!NOTE]
>
>La funzione `executionMetadata` non è visibile quando viene visualizzato il contenuto stesso.

In fase di esecuzione, il valore dei metadati viene aggiunto al set di dati **[!UICONTROL Message Feedback Event]** esistente con la seguente aggiunta di schema:

```
"_experience": {
  "customerJourneyManagement": {
    "messageExecution": {
      "metadata": {
        "your_key": "your_value"
      }
    }
  }
}
```

>[!IMPORTANT]
>
>Esiste un limite massimo di 2 kb per le coppie chiave-valore per azione. Se viene superato il limite di 2 KB, il messaggio viene comunque recapitato, ma è possibile troncare qualsiasi coppia di valori chiave.

**Esempio**

```
{{executionMetadata key="firstName" value=profile.person.name.firstName}}
```

In questo esempio, supponendo `profile.person.name.firstName` = &quot;Alex&quot;, l&#39;entità risultante è:

```
{
  "key": "firstName",
  "value": "Alex"
}
```

+++

## Funzioni di mappatura {#maps}

Utilizza le funzioni mappa nella personalizzazione per semplificare l’interazione con le mappe.

### get {#get}

Utilizzare la funzione `get` per recuperare il valore di una mappa per una determinata chiave.

+++Sintassi

```sql
{%= get(map, string) %}
```

**Esempio**

L&#39;operazione seguente ottiene il valore della mappa di identità per la chiave `example@example.com`.

```sql
{%= get(identityMap,"example@example.com") %}
```

+++

### tasti {#keys}

Utilizzare la funzione `keys` per recuperare tutte le chiavi per una determinata mappa.

+++Sintassi

```sql
{%= keys(map) %}
```

**Esempio**

L&#39;operazione seguente recupera tutte le chiavi per la mappa `identityMap`.

```sql
{%= keys(identityMap) %}
```

+++

### valori {#values}

La funzione `values` viene utilizzata per recuperare tutti i valori di una determinata mappa.

+++Sintassi

```sql
{%= values(map) %}
```

**Esempio**

L&#39;operazione seguente recupera tutti i valori per la mappa `identityMap`.

```sql
{%= values(identityMap) %}
```

+++

## Funzioni matematiche {#math}

Scopri come utilizzare le funzioni matematiche nell’editor di personalizzazione.

### assoluto {#absolute}

Utilizzare la funzione `absolute` per convertire un numero nel relativo valore assoluto.

+++Sintassi

```sql
{%= absolute(int) %}: int
```

+++

### formatNumber {#format-number}

Utilizzare la funzione `formatNumber` per formattare qualsiasi numero nella relativa rappresentazione sensibile alla lingua.

Accetta un numero e una stringa che rappresenta la lingua e restituisce una stringa formattata del numero nella lingua desiderata.

+++Sintassi

```sql
{%= formatNumber(number/double,string) %}: string
```

Puoi utilizzare la formattazione e le impostazioni internazionali valide come riepilogato nella [documentazione di Oracle](https://docs.oracle.com/javase/8/docs/api/java/util/Locale.html) e nelle [impostazioni internazionali supportate](https://www.oracle.com/java/technologies/javase/jdk11-suported-locales.html){_blank}

**Esempio**

Questa query restituisce una stringa formattata in arabo corrispondente a 123456,789 come numero di input.

```sql
{%= formatNumber(123456.789, "ar_EG") %}
```

+++

### random {#random}

Utilizzare la funzione `random` per restituire un valore casuale compreso tra 0 e 1.

+++Sintassi

```sql
{%= random() %}: double
```

+++

### roundDown {#round-down}

Utilizzare la funzione `roundDown` per arrotondare un numero per difetto.

+++Sintassi

```sql
{%= roundDown(double) %}: double
```

+++

### roundUp {#round-up}

Utilizzare la funzione `roundUp` per arrotondare un numero per eccesso.

+++Sintassi

```sql
{%= roundUp(double) %}: double
```

+++

### toHexString {#to-hex-string}

La funzione `toHexString` converte qualsiasi numero nella relativa stringa esadecimale.

+++Sintassi

```sql
{%= toHexString(number) %}: string
```

**Esempio**

Questa query restituisce il valore esadecimale 158 come 9e.

```sql
{%= toHexString(158) %}
```

+++

### toInt {#to-int}

Utilizzare la funzione `toInt` per convertire i tipi (number, double, integer, long, float, short, byte, boolean, string) in un numero intero.

+++Sintassi

```sql
{%= toInt(<valueToConvert>) %}: integer
```

**Esempio**

Questa query restituisce il valore intero 42,6 come 42.

```sql
{%= toInt(42.6) %}: integer
```

+++

### toPercentage {#to-percentage}

Utilizzare la funzione `toPercentage` per convertire un numero in percentuale.

+++Sintassi

```sql
{%= toPercentage(double) %}: string
```

+++

### toPrecision {#to-precision}

Utilizzare la funzione `toPrecision` per convertire un numero con la precisione richiesta.

+++Sintassi

```sql
{%= toPrecision(double,int) %}: string
```

+++

### toString {#to-string}

La funzione `toString` converte qualsiasi numero nella relativa rappresentazione di stringa.

+++Sintassi

```sql
{%= toString(string) %}: string
```

**Esempio**

Questa query restituisce `"12"`.

```sql
{%= toString(12) %} 
```

+++

## Funzioni oggetto {#objects}

Funzioni oggetto per eseguire query sulle proprietà o sugli attributi dell&#39;oggetto.

### isNull {#isNull}

La funzione `isNull` determina se un riferimento a un oggetto non esiste.

+++Sintassi

```sql
{%= isNull(object) %}
```

**Esempio**

L&#39;operazione seguente verifica se l&#39;indirizzo dell&#39;abitazione della persona non esiste.

```sql
{%= isNull(person.homeAddress) %}
```

+++

### isNotNull {#isNotNull}

La funzione `isNotNull` determina se esiste un riferimento a un oggetto.

+++Sintassi

```sql
{%= isNotNull(object) %}
```

**Esempio**

L&#39;operazione seguente verifica se l&#39;indirizzo dell&#39;abitazione della persona esiste.

```sql
{%= isNotNull(person.homeAddress) %}
```

+++

## Funzioni stringa {#string-functions}

Scopri come utilizzare le funzioni stringa nell’editor di personalizzazione.

### CamelCase {#camelCase}

La funzione `camelCase` utilizza l&#39;iniziale maiuscola di ogni parola di una stringa.

+++Sintassi

```sql
{%= camelCase(string)%}
```

**Esempio**

La funzione seguente maiuscola la prima lettera di una parola nell’indirizzo stradale del profilo.

```sql
{%= camelCase(profile.homeAddress.street) %}
```

+++

### charCodeAt {#char-code-at}

La funzione `charCodeAt` restituisce il valore ASCII di un carattere, come la funzione `charCodeAt` in JavaScript. Come argomenti di input sono necessari una stringa e un numero intero (che definisce la posizione di un carattere) e viene restituito il valore ASCII corrispondente.

+++Sintassi

```sql
{%= charCodeAt(string,int) %}: int
```

**Esempio**

La funzione seguente restituisce il valore ASCII `o` (111).

```sql
{%= charCodeAt("some", 1)%}
```

+++

### concatena {#concate}

La funzione `concat` combina due stringhe in una.

+++Sintassi

```sql
{%= concat(string,string) %}
```

**Esempio**

La funzione seguente combina la città del profilo e il paese in una singola stringa.

```sql
{%= concat(profile.homeAddress.city,profile.homeAddress.country) %}
```

+++

### contiene {#contains}

Utilizzare la funzione `contains` per determinare se una stringa contiene una sottostringa specificata.

+++Sintassi

```sql
{%= contains(STRING_1, STRING_2, CASE_SENSITIVE) %}
```

| Argomento | Descrizione |
| --------- | ----------- |
| `STRING_1` | Stringa su cui eseguire il controllo. |
| `STRING_2` | Stringa da cercare nella prima stringa. |
| `CASE_SENSITIVE` | Un parametro opzionale per determinare se il controllo distingue tra maiuscole e minuscole. Valori possibili: true (predefinito) / false. |

**Esempi**

* La funzione seguente controlla se il nome del profilo contiene la lettera A (in maiuscolo o minuscolo). In caso contrario, restituisce `true`. In caso contrario, restituisce `false`.

  ```sql
  {%= contains(profile.person.name.firstName, "A", false) %}
  ```

* La query seguente determina, con distinzione tra maiuscole e minuscole, se l&#39;indirizzo e-mail della persona contiene la stringa `2010@gm`.

  ```sql
  {%= contains(profile.person.emailAddress,"2010@gm") %}
  ```

+++

### doesNotContain {#doesNotContain}

Utilizzare la funzione `doesNotContain` per determinare se una stringa non contiene una sottostringa specificata.

+++Sintassi

```sql
{%= doesNotContain(STRING_1, STRING_2, CASE_SENSITIVE)%}
```

| Argomento | Descrizione |
| --------- | ----------- |
| `STRING_1` | Stringa su cui eseguire il controllo. |
| `STRING_2` | Stringa da cercare nella prima stringa. |
| `CASE_SENSITIVE` | Un parametro opzionale per determinare se il controllo distingue tra maiuscole e minuscole. Valori possibili: true (predefinito) / false. |

**Esempio**

La query seguente determina, con distinzione tra maiuscole e minuscole, se l&#39;indirizzo e-mail della persona non contiene la stringa `2010@gm`.

```sql
{%= doesNotContain(profile.person.emailAddress,"2010@gm")%}
```

+++

### doesNotEndWith {#doesNotEndWith}

Utilizzare la funzione `doesNotEndWith` per determinare se una stringa non termina con una sottostringa specificata.

+++Sintassi

```sql
{%= doesNotEndWith(STRING_1, STRING_2, CASE_SENSITIVE)%}
```

| Argomento | Descrizione |
| --------- | ----------- |
| `{STRING_1}` | Stringa su cui eseguire il controllo. |
| `{STRING_2}` | Stringa da cercare nella prima stringa. |
| `{CASE_SENSITIVE}` | Un parametro opzionale per determinare se il controllo distingue tra maiuscole e minuscole. Valori possibili: true (predefinito) / false. |

**Esempio**

La query seguente determina, con distinzione tra maiuscole e minuscole, se l&#39;indirizzo e-mail dell&#39;utente non termina con `.com`.

```sql
doesNotEndWith(person.emailAddress,".com")
```

+++

### doesNotStartWith {#doesNotStartWith}

Utilizzare la funzione `doesNotStartWith` per determinare se una stringa non inizia con una sottostringa specificata.

+++Sintassi

```sql
{%= doesNotStartWith(STRING_1, STRING_2, CASE_SENSITIVE)%}
```

| Argomento | Descrizione |
| --------- | ----------- |
| `{STRING_1}` | Stringa su cui eseguire il controllo. |
| `{STRING_2}` | Stringa da cercare nella prima stringa. |
| `{CASE_SENSITIVE}` | Un parametro opzionale per determinare se il controllo distingue tra maiuscole e minuscole. Valori possibili: true (predefinito) / false. |

**Esempio**

La query seguente determina, con distinzione tra maiuscole e minuscole, se il nome della persona non inizia con `Joe`.

```sql
{%= doesNotStartWith(person.name,"Joe")%}
```

+++

### encode64 {#encode64}

Utilizzare la funzione `encode64` per codificare una stringa per conservare le informazioni personali (PI), ad esempio da includere in un URL.

+++Sintassi

```sql
{%= encode64(string) %}
```

+++

### endsWith {#endsWith}

Utilizzare la funzione `endsWith` per determinare se una stringa termina con una sottostringa specificata.

+++Sintassi

```sql
{%= endsWith(STRING_1, STRING_2, CASE_SENSITIVE) %}
```

| Argomento | Descrizione |
| --------- | ----------- |
| `{STRING_1}` | Stringa su cui eseguire il controllo. |
| `{STRING_2}` | Stringa da cercare nella prima stringa. |
| `{CASE_SENSITIVE}` | Un parametro opzionale per determinare se il controllo distingue tra maiuscole e minuscole. Valori possibili: true (predefinito) / false. |

**Esempio**

La query seguente determina, con distinzione tra maiuscole e minuscole, se l&#39;indirizzo e-mail dell&#39;utente termina con `.com`.

```sql
{%= endsWith(person.emailAddress,".com") %}
```

+++

### uguale a {#equals}

Utilizzare la funzione `equals` per determinare se una stringa è uguale alla stringa specificata, con distinzione tra maiuscole e minuscole.

+++Sintassi

```sql
{%= equals(STRING_1, STRING_2) %}
```

| Argomento | Descrizione |
| --------- | ----------- |
| `{STRING_1}` | Stringa su cui eseguire il controllo. |
| `{STRING_2}` | Stringa da confrontare con la prima stringa. |

**Esempio**

La query seguente determina, con distinzione tra maiuscole e minuscole, se il nome della persona è `John`.

```sql
{%=equals(profile.person.name,"John") %}
```

+++

### equalsIgnoreCase {#equalsIgnoreCase}

Utilizzare la funzione `equalsIgnoreCase` per determinare se una stringa è uguale alla stringa specificata, senza distinzione tra maiuscole e minuscole.

+++Sintassi

```sql
{%= equalsIgnoreCase(STRING_1, STRING_2) %}
```

| Argomento | Descrizione |
| --------- | ----------- |
| `{STRING_1}` | Stringa su cui eseguire il controllo. |
| `{STRING_2}` | Stringa da confrontare con la prima stringa. |

**Esempio**

La query seguente determina se il nome della persona è `John` senza distinzione tra maiuscole e minuscole.

```sql
{%= equalsIgnoreCase(profile.person.name,"John") %}
```

+++

### extractEmailDomain {#extractEmailDomain}

Utilizzare la funzione `extractEmailDomain` per estrarre il dominio di un indirizzo e-mail.

+++Sintassi

```sql
{%= extractEmailDomain(string) %}
```

**Esempio**

La query seguente estrae il dominio e-mail dell’indirizzo e-mail personale.

```sql
{%= extractEmailDomain(profile.personalEmail.address) %}
```

+++

### formatCurrency {#format-currency}

Utilizzare la funzione `formatCurrency` per convertire qualsiasi numero nella corrispondente rappresentazione della valuta sensibile alla lingua a seconda delle impostazioni locali passate come stringa nel secondo argomento.

+++Sintassi

```sql
{%= formatCurrency(number/double,string) %}: string
```

**Esempio**

Questa query restituisce £ 56,00

```sql
{%= formatCurrency(56L,"en_GB") %}
```

+++

### getUrlHost {#get-url-host}

Utilizzare la funzione `getUrlHost` per recuperare il nome host di un URL.

+++Sintassi

```sql
{%= getUrlHost(string) %}: string
```

**Esempio**

```sql
{%= getUrlHost("https://www.myurl.com/contact") %}
```

Restituisce &quot;www.myurl.com&quot;

+++

### getUrlPath {#get-url-path}

Utilizzare la funzione `getUrlPath` per recuperare il percorso dopo il nome di dominio di un URL.

+++Sintassi

```sql
{%= getUrlPath(string) %}: string
```

**Esempio**

```sql
{%= getUrlPath("https://www.myurl.com/contact.html") %}
```

Restituisce &quot;/contact.html&quot;

+++

### getUrlProtocol {#get-url-protocol}

Utilizzare la funzione `getUrlProtocol` per recuperare il protocollo di un URL.

+++Sintassi

```sql
{%= getUrlProtocol(string) %}: string
```

**Esempio**

```sql
{%= getUrlProtocol("https://www.myurl.com/contact.html") %}
```

Restituisce &quot;http&quot;

+++

### indexOf {#index-of}

Utilizzare la funzione `indexOf` per restituire la posizione della prima occorrenza del secondo parametro nel primo argomento. Restituisce -1 se non viene trovata alcuna corrispondenza.

+++Sintassi

```sql
{%= indexOf(STRING_1, STRING_2) %}: integer
```

| Argomento | Descrizione |
| --------- | ----------- |
| `{STRING_1}` | Stringa su cui eseguire il controllo. |
| `{STRING_2}` | Stringa da cercare nel primo parametro |

**Esempio**

```sql
{%= indexOf("hello world","world" ) %}
```

Restituisce 6.

+++

### IsEmpty {#isEmpty}

Utilizzare la funzione `isEmpty` per determinare se una stringa è vuota.

+++Sintassi

```sql
{%= isEmpty(string) %}
```

**Esempio**

La funzione seguente restituisce &quot;true&quot; se il numero di telefono cellulare del profilo è vuoto. Altrimenti restituisce `false`.

```sql
{%= isEmpty(profile.mobilePhone.number) %}
```

+++

### isNotEmpty {#is-not-empty}

Utilizzare la funzione `isNotEmpty` per determinare se una stringa non è vuota.

+++Sintassi

```sql
{= isNotEmpty(string) %}: boolean
```

**Esempio**

La funzione seguente restituisce &quot;true&quot; se il numero di telefono cellulare del profilo non è vuoto. Altrimenti restituisce `false`.

```sql
{%= isNotEmpty(profile.mobilePhone.number) %}
```

+++

### lastIndexOf {#last-index-of}

Utilizzare la funzione `lastIndexOf` per restituire la posizione (nel primo argomento) dell&#39;ultima occorrenza del secondo parametro. Restituisce -1 se non viene trovata alcuna corrispondenza.

+++Sintassi

```sql
{= lastIndexOf(STRING_1, STRING_2) %}: integer
```

| Argomento | Descrizione |
| --------- | ----------- |
| `{STRING_1}` | Stringa su cui eseguire il controllo. |
| `{STRING_2}` | Stringa da cercare nel primo parametro |

**Esempio**

```sql
{%= lastIndexOf("hello world","o" ) %}
```

Restituisce 7.

+++

### leftTrim {#leftTrim}

Utilizzare la funzione `leftTrim` per rimuovere gli spazi dall&#39;inizio di una stringa.

+++Sintassi

```sql
{%= leftTrim(string) %}
```

+++

### length {#length}

Utilizzare la funzione `length` per ottenere il numero di caratteri in una stringa o in un&#39;espressione.

+++Sintassi

```sql
{%= length(string) %}
```

**Esempio**

La funzione seguente restituisce la lunghezza del nome della città del profilo.

```sql
{%= length(profile.homeAddress.city) %}
```

+++

### mi piace {#like}

Utilizzare la funzione `like` per determinare se una stringa corrisponde a uno schema specificato.

+++Sintassi

```sql
{%= like(STRING_1, STRING_2) %}
```

| Argomento | Descrizione |
| --------- | ----------- |
| `{STRING_1}` | Stringa su cui eseguire il controllo. |
| `{STRING_2}` | Espressione da confrontare con la prima stringa. Per la creazione di un&#39;espressione sono supportati due caratteri speciali: `%` e `_`. <ul><li>`%` viene utilizzato per rappresentare zero o più caratteri.</li><li>`_` viene utilizzato per rappresentare esattamente un carattere.</li></ul> |

**Esempio**

La query seguente recupera tutte le città in cui vivono i profili contenenti il pattern `es`.

```sql
{%= like(profile.homeAddress.city, "%es%")%}
```

+++

### lowerCase {#lower}

Utilizzare la funzione `lowerCase` per convertire una stringa in lettere minuscole.

+++Sintassi

```sql
{%= lowerCase(string) %}
```

**Esempio**

Questa funzione converte il nome del profilo in lettere minuscole.

```sql
{%= lowerCase(profile.person.name.firstName) %}
```

+++

### matches {#matches}

Utilizzare la funzione `matches` per determinare se una stringa corrisponde a una specifica espressione regolare. Per ulteriori informazioni sui pattern corrispondenti nelle espressioni regolari, consulta [la documentazione di Oracle](https://docs.oracle.com/javase/8/docs/api/java/util/regex/Pattern.html).

+++Sintassi

```sql
{%= matches(STRING_1, STRING_2) %}
```

**Esempio**

La query seguente determina, senza distinzione tra maiuscole e minuscole, se il nome della persona inizia con `John`.

```sql
{%= matches(person.name.,"(?i)^John") %}
```

+++

### maschera {#mask}

Utilizzare la funzione `mask` per sostituire una parte di stringa con caratteri &quot;X&quot;.

+++Sintassi

```sql
{%= mask(string,integer,integer) %}
```

**Esempio**

La query seguente sostituisce la stringa &quot;123456789&quot; con caratteri &quot;X&quot;, ad eccezione del primo e dell’ultimo secondo carattere.

```sql
{%= mask("123456789",1,2) %}
```

La query restituisce `1XXXXXX89`.

+++

### md5 {#md5}

Utilizzare la funzione `md5` per calcolare e restituire l&#39;hash MD5 di una stringa.

+++Sintassi

```sql
{%= md5(string) %}: string
```

**Esempio**

```sql
{%= md5("hello world") %}
```

Restituisce &quot;5eb63bbbe01eeed093cb22bb8f5acdc3&quot;

+++

### notEqualTo {#notEqualTo}

Utilizzare la funzione `notEqualTo` per determinare se una stringa non è uguale alla stringa specificata.

+++Sintassi

```sql
{%= notEqualTo(STRING_1, STRING_2) %}
```

| Argomento | Descrizione |
| --------- | ----------- |
| `{STRING_1}` | Stringa su cui eseguire il controllo. |
| `{STRING_2}` | Stringa da confrontare con la prima stringa. |

**Esempio**

La query seguente determina, con distinzione tra maiuscole e minuscole, se il nome della persona non è `John`.

```sql
{%= notEqualTo(profile.person.name,"John") %}
```

+++

### notEqualWithIgnoreCase {#not-equal-with-ignore-case}

Utilizzare la funzione `notEqualWithIgnoreCase` per confrontare due stringhe ignorando la distinzione tra maiuscole e minuscole.

+++Sintassi

```sql
{= notEqualWithIgnoreCase(STRING_1,STRING_2) %}: boolean
```

| Argomento | Descrizione |
| --------- | ----------- |
| `{STRING_1}` | Stringa su cui eseguire il controllo. |
| `{STRING_2}` | Stringa da confrontare con la prima stringa. |

**Esempio**

La query seguente determina se il nome della persona non è `john`, senza distinzione tra maiuscole e minuscole.

```sql
{%= notEqualTo(profile.person.name,"john") %}
```

+++

### regexGroup {#regexGroup}

Utilizza la funzione `regexGroup` per estrarre informazioni specifiche, in base all&#39;espressione regolare fornita.

+++Sintassi

```sql
{%= regexGroup(STRING, EXPRESSION, GROUP) %}
```

| Argomento | Descrizione |
| --------- | ----------- |
| `{STRING}` | Stringa su cui eseguire il controllo. |
| `{EXPRESSION}` | Espressione regolare da confrontare con la prima stringa. |
| `{GROUP}` | Gruppo di espressioni con cui confrontare. |

**Esempio**

La query seguente estrae il nome di dominio da un indirizzo e-mail.

```sql
{%= regexGroup(emailAddress,"@(\\w+)", 1) %}
```

+++

### replace {#replace}

Utilizzare la funzione `replace` per sostituire una determinata sottostringa in una stringa con un&#39;altra sottostringa.

+++Sintassi

```sql
{%= replace(STRING_1,STRING_2,STRING_3) %}:string
```

| Argomento | Descrizione |
| --------- | ----------- |
| `{STRING_1}` | Stringa in cui deve essere sostituita la sottostringa. |
| `{STRING_2}` | Sottostringa da sostituire. |
| `{STRING_3}` | La sottostringa di sostituzione. |

**Esempio**

```sql
{%= replace("Hello John, here is your monthly newsletter!","John","Mark") %}
```

Restituisce `Hello Mark, here is your monthly newsletter!`

+++

### replaceAll {#replaceAll}

Utilizzare la funzione `replaceAll` per sostituire tutte le sottostringhe di un testo che corrisponde all&#39;espressione regex con la stringa di sostituzione letterale specificata. Regex gestisce in modo speciale `\` e `+` e tutte le espressioni regex seguono la strategia di escape di PQL. La sostituzione procede dall&#39;inizio della stringa alla fine, ad esempio sostituendo `aa` con `b` nella stringa `aaa` si ottiene `ba` anziché `ab`.

+++Sintassi

```sql
{%= replaceAll(string,string,string) %}
```

>[!NOTE]
>
> Se l&#39;espressione utilizzata come secondo argomento è un carattere regex speciale, utilizzare una doppia barra rovesciata (`//`).  I caratteri regex speciali sono: [., +, *, ?, ^, $, (, ), [,], {, }, |, \.]
> 
> Ulteriori informazioni sono disponibili nella [documentazione di Oracle](https://docs.oracle.com/javase/7/docs/api/java/util/regex/Pattern.html){_blank}.
>

+++

### rightTrim {#rightTrim}

La funzione `rightTrim` rimuove gli spazi dalla fine di una stringa.

+++Sintassi

```sql
{%= rightTrim(string) %}
```

+++

### sha256 {#sha256}

La funzione `sha256` calcola e restituisce l&#39;hash sha256 di una stringa.

+++Sintassi

```sql
{%= sha256(string) %} : string
```

**Esempio**

```sql
{%= sha256("Eliechxh")%}
```

Restituisce `0b0b207880b999adaad6231026abf87caa30760b6f326b21727b61139332257d`

+++

### split {#split}

Utilizzare la funzione `split` per dividere una stringa per un determinato carattere.

+++Sintassi

```sql
{%= split(string,string) %}
```

+++

### startsWith {#startsWith}

Utilizzare la funzione `startsWith` per determinare se una stringa inizia con una sottostringa specificata.

+++Sintassi

```sql
{%= startsWith(STRING_1, STRING_2, CASE_SENSITIVE) %}
```

| Argomento | Descrizione |
| --------- | ----------- |
| `{STRING_1}` | Stringa su cui eseguire il controllo. |
| `{STRING_2}` | Stringa da cercare nella prima stringa. |
| `{CASE_SENSITIVE}` | Un parametro opzionale per determinare se il controllo distingue tra maiuscole e minuscole. Per impostazione predefinita, è impostato su true. |

**Esempio**

La query seguente determina, con distinzione tra maiuscole e minuscole, se il nome della persona inizia con `Joe`.

```sql
{%= startsWith(person.name,"Joe") %}
```

+++

### stringToDate {#string-to-date}

La funzione `stringToDate` converte un valore stringa in un valore data-ora. Sono necessari due argomenti: la rappresentazione in forma di stringa di una data/ora e la rappresentazione in forma di stringa del formattatore.

+++Sintassi

```sql
{= stringToDate("date-time value","formatter" %}
```

**Esempio**

```sql
{= stringToDate("2023-01-10 23:13:26", "yyyy-MM-dd HH:mm:ss") %}
```

+++

### string_to_intero {#string-to-integer}

Utilizzare la funzione `string_to_integer` per convertire un valore stringa in un valore intero.

+++Sintassi

```sql
{= string_to_integer(string) %}: int
```

+++

### stringToNumber {#string-to-number}

Utilizzare la funzione `stringToNumber` per convertire una stringa in numero. In caso di input non valido, restituisce la stessa stringa come output.

+++Sintassi

```sql
{%= stringToNumber(string) %}: double
```

+++

### substr {#sub-string}

Utilizzare la funzione `substr` per restituire la sottostringa dell&#39;espressione stringa tra l&#39;indice iniziale e l&#39;indice finale.

+++Sintassi

```sql
{= substr(string, integer, integer) %}: string
```

+++

### titleCase {#titleCase}

Utilizzare la funzione `titleCase` per rendere maiuscole le prime lettere di ogni parola di una stringa.

+++Sintassi

```sql
{%= titleCase(string) %}
```

**Esempio**

Se la persona vive a Washington High Street, questa funzione restituisce `Washington High Street`.

```sql
{%= titleCase(profile.person.location.Street) %}
```

+++

### toBool {#to-bool}

Utilizzare la funzione `toBool` per convertire un valore di argomento in un valore booleano, a seconda del tipo.

+++Sintassi

```sql
{= toBool(string) %}: boolean
```

+++

### toDateTime {#to-date-time}

Utilizzare la funzione `toDateTime` per convertire la stringa in data. In caso di input non valido, restituisce la data epoca come output.

+++Sintassi

```sql
{%= toDateTime(string, string) %}: date-time
```

+++

### toDateTimeOnly {#to-date-time-only}

Utilizzare la funzione `toDateTimeOnly` per convertire un valore di argomento in un valore solo di data e ora. In caso di input non valido, restituisce la data epoca come output. Questa funzione accetta tipi di campo stringa, data, long e integer.

+++Sintassi

```sql
{%= toDateTimeOnly(string/date/long/int) %}: date-time
```

+++

### trim {#trim}

La funzione `trim` rimuove tutti gli spazi dall&#39;inizio e dalla fine di una stringa.

+++Sintassi

```sql
{%= trim(string) %}
```

+++

### upperCase {#upper}

La funzione `upperCase` converte una stringa in lettere maiuscole.

+++Sintassi

```sql
{%= upperCase(string) %}
```

**Esempio**

Questa funzione converte il cognome del profilo in lettere maiuscole.

```sql
{%= upperCase(profile.person.name.lastName) %}
```

+++

### urlDecode {#url-decode}

Utilizzare la funzione `urlDecode` per decodificare una stringa con codifica URL.

+++Sintassi

```sql
{%= urlDecode(string) %}: string
```

+++

### urlEncode {#url-encode}

Utilizzare la funzione `urlEncode` per codificare una stringa come URL.

+++Sintassi

```sql
{%= urlEncode(string) %}: string
```

+++
