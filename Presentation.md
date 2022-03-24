# Structures de données
Les langages de programmation disposent de structures de données natives. Selon les langages, les structures mises à disposition peuvent être différentes. Dans cet article, on listera les structures de données natives en JavaScript. On détaillera leurs propriétés et les façons de les utiliser voire de les combiner. Dans certains cas, on comparera ces structures avec celles d'autres langages.

-----

## 1. Un typage dynamique

JavaScript est un langage dont le __typage est faible et dynamique__ . Cela signifie qu'il n'est pas nécessaire de déclarer le type d'une variable avant de l'utiliser.  

Le type de la variable sera automatiquement déterminé lorsque le programme sera exécuté. Cela signifie également que la même variable pourra avoir différents types au cours de son existence :

```js
  var toto = 42;       // toto est un nombre
      toto = "machin"; // toto est une chaîne de caractères désormais
      toto = true;     // et maintenant, toto est un booléen
```

## 2. Les types de données
Le dernier standard ECMAScript définit 8 types de données :

 - Les 7 types **Primitifs** : 
    - Booléen (boolean)
    - Nul (null)
    - Indéfini (undefined)
    - Nombre (number)
    - BigInt (proposition pour ES2020)
    - Chaîne de caractères (String)
    - Symbole (Symbol, type introduit avec ECMAScript 6)
 - et le type **Objet**

## 3. Les valeurs primitives

Tous les types, sauf les objets, définissent des valeurs immuables (qu'on ne peut modifier). Ainsi, contrairement au `langage C`, les chaînes de caractères sont immuables en JavaScript. Les valeurs immuables pour chacun de ces types sont appelées « valeurs primitives ».

-----

### 3.1. Le type booléen (boolean)

Un booléen représente le résultat d'une assertion logique et peut avoir deux valeurs : `true` (pour le vrai logique) et `false` (pour le faux logique).  
> Visitez le lien [Boolean](https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Global_Objects/Boolean) pour plus de détails sur la représentation objet de ce type. 

-----

### 3.2. Le type nul (null)
**Le type nul ne possède qu'une valeur : null.**   
> Visitez le lien [null](https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Global_Objects/null) et [Null](https://developer.mozilla.org/fr/docs/Glossary/Null) pour plus d'informations.

-----

### 3.3. Le type indéfini (undefined)
**Une variable à laquelle on n'a pas affecté de valeur vaudra undefined.**  
> Voir [undefined](https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Global_Objects/undefined) et [Undefined](https://developer.mozilla.org/fr/docs/Glossary/undefined) pour plus d'informations.

-----

### 3.4. Le type nombre
ECMAScript possède deux types numériques natifs : `Number` et `BigInt` (cf. ci-après)  

Le type `Number` est géré pour représenter les nombres : [les nombres flottants à précision double, représentés sur 64 bits, selon le format IEEE 754](https://en.wikipedia.org/wiki/Double-precision_floating-point_format) (les nombres compris entre -(2^53 -1) et 2^53 -1).  

**Il n'y a donc pas de type à part pour représenter les nombres entiers.** En plus de sa capacité à représenter les nombres décimaux, le type nombre possède trois valeurs symboliques :  `+Infinity`, `-Infinity`, et [`NaN`](https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Global_Objects/NaN) (Not A Number en anglais, qui signifie « n'est pas un nombre »). 

Afin de vérifier que des valeurs sont supérieures/inférieures à `+/-Infinity`, on peut utiliser les constantes [Number.MAX_VALUE](https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Global_Objects/Number/MAX_VALUE) et [Number.MIN_VALUE](https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Global_Objects/Number/MIN_VALUE).  

À partir d'ECMAScript 6, on peut également vérifier si un nombre est/sera compris dans l'intervalle de représentation pour les nombres flottants à précision double en utilisant la méthode [`Number.isSafeInteger()`](https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Global_Objects/Number/isSafeInteger) ainsi que les valeurs [`Number.MAX_SAFE_INTEGER`](https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Global_Objects/Number/MAX_SAFE_INTEGER) et [`Number.MIN_SAFE_INTEGER`](https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Global_Objects/Number/MIN_SAFE_INTEGER).  

En dehors de cet intervalle et pour JavaScript, on considère que les nombres ne sont plus représentés correctement. On manipule alors une approximation de la valeur sous forme d'un nombre à virgule flottante à précision double.  

Le type nombre possède un seul entier pouvant être représenté de deux façons différentes : 0 qui peut être représenté par -0 et +0. ("0" étant un alias pour +0). En pratique, cela n'a généralement aucun impact et `+0 === -0` vaut bien `true`. Malgré tout, on peut observer certaines différences quand on divise par zéro :


```js
42 / +0
// Infinity

42 / -0
// -Infinity
```

Dans la plupart des cas, un nombre représente sa propre valeur, malgré tout les [opérateurs binaires](https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Operators) peuvent être utilisés pour représenter plusieurs valeurs booléennes grâce à un seul nombre (on parle alors de [masque de bits](https://fr.wikipedia.org/wiki/Masquage)). Ceci est généralement une mauvaise pratique (lisibilité, maintenabilité) bien que ça puisse être utile lorsqu'on souhaite minimiser le nombre de bits qu'on utilise.

-----

### 3.5. 


-----

***Le document est en cours de rédaction...***
