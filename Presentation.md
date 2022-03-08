# Structures de données
Les langages de programmation disposent de structures de données natives. Selon les langages, les structures mises à disposition peuvent être différentes. Dans cet article, on listera les structures de données natives en JavaScript. On détaillera leurs propriétés et les façons de les utiliser voire de les combiner. Dans certains cas, on comparera ces structures avec celles d'autres langages.

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

### 3.1. Le type booléen (boolean)

Un booléen représente le résultat d'une assertion logique et peut avoir deux valeurs : `true` (pour le vrai logique) et `false` (pour le faux logique).  
> Visitez le lien [Boolean](https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Global_Objects/Boolean) pour plus de détails sur la représentation objet de ce type. 

### 3.2. Le type nul (null)
**Le type nul ne possède qu'une valeur : null.**   
> Visitez le lien [null](https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Global_Objects/null) et [Null](https://developer.mozilla.org/fr/docs/Glossary/Null) pour plus d'informations.

### 3.3. Le type indéfini (undefined)
**Une variable à laquelle on n'a pas affecté de valeur vaudra undefined.**  
> Voir [undefined](https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Global_Objects/undefined) et [Undefined](https://developer.mozilla.org/fr/docs/Glossary/undefined) pour plus d'informations.








