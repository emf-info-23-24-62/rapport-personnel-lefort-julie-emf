<h1>🤔 RP - 323 - Programmation fonctionnelle</h1>

>[!TIP]
>**Référence Javascript:** <https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference>  
>**Tester du code JS** : <https://runjs.app/play>  
>**Convertir en PDF** : <https://marketplace.visualstudio.com/items?itemName=manuth.markdown-converter>

<h1>Table des matières</h1>

- [Introduction](#introduction)
- [Opérateurs javascript super-cooool 😎](#opérateurs-javascript-super-cooool-)
  - [opérateur `?:`](#opérateur-)
  - [opérateur `??`](#opérateur--1)
  - [opérateur `??=`](#opérateur--2)
  - [opérateur de décomposition 'spread' `...`](#opérateur-de-décomposition-spread-)
  - [Déstructuration](#déstructuration)
- [Date et Heure](#date-et-heure)
  - [Obtenir la date et/ou heure actuelle](#obtenir-la-date-etou-heure-actuelle)
- [Math](#math)
  - [`Math.PI` - la constante π](#mathpi---la-constante-π)
  - [`Math.abs()` - la |valeur absolue| d'un nombre](#mathabs---la-valeur-absolue-dun-nombre)
  - [`Math.pow()` - élever à une puissance](#mathpow---élever-à-une-puissance)
  - [`Math.min()` - plus petite valeur](#mathmin---plus-petite-valeur)
  - [`Math.max()` - plus grande valeur](#mathmax---plus-grande-valeur)
  - [`Math.ceil()` - arrondir à la prochaine valeur entière la plus proche](#mathceil---arrondir-à-la-prochaine-valeur-entière-la-plus-proche)
  - [`Math.floor()` - arrondir à la précédente valeur entière la plus proche](#mathfloor---arrondir-à-la-précédente-valeur-entière-la-plus-proche)
  - [`Math.round()` - arrondir à la valeur entière la plus proche](#mathround---arrondir-à-la-valeur-entière-la-plus-proche)
  - [`Math.trunc()` - supprime la virgule et retourne la partie entière d'un nombre](#mathtrunc---supprime-la-virgule-et-retourne-la-partie-entière-dun-nombre)
  - [`Math.sqrt()` - la raçine carrée d'un nombre](#mathsqrt---la-raçine-carrée-dun-nombre)
  - [`Math.random()` - générer un nombre aléatoire entre 0.0 (compris) et 1.0 (non compris)](#mathrandom---générer-un-nombre-aléatoire-entre-00-compris-et-10-non-compris)
- [JSON](#json)
  - [`JSON.stringify()` - transformer un objet Javascript en JSON](#jsonstringify---transformer-un-objet-javascript-en-json)
  - [`JSON.parse()` - transformer du JSON en objet Javascript](#jsonparse---transformer-du-json-en-objet-javascript)
- [Chaînes de caractères](#chaînes-de-caractères)
  - [`split()` - un ciseau qui coupe une chaîne là où un caractère apparaît et produit un tableau](#split---un-ciseau-qui-coupe-une-chaîne-là-où-un-caractère-apparaît-et-produit-un-tableau)
  - [`trim()`, `trimStart()` et `trimEnd()` - épuration des espaces en trop dans une chaîne (trimming)](#trim-trimstart-et-trimend---épuration-des-espaces-en-trop-dans-une-chaîne-trimming)
  - [`padStart()` et `padEnd()` - aligner le contenu dans une chaîne de caractères](#padstart-et-padend---aligner-le-contenu-dans-une-chaîne-de-caractères)
- [Console](#console)
  - [`console.log()` - Afficher un message sur la console](#consolelog---afficher-un-message-sur-la-console)
  - [`console.info()`, `warn()` et `error()` - Afficher un message sur la console (filtrables)](#consoleinfo-warn-et-error---afficher-un-message-sur-la-console-filtrables)
  - [`console.table()` - Afficher tout un tableau ou un objet sur la console](#consoletable---afficher-tout-un-tableau-ou-un-objet-sur-la-console)
  - [`console.time()`, `timeLog()` et `timeEnd()` - Chronométrer une durée d'exécution](#consoletime-timelog-et-timeend---chronométrer-une-durée-dexécution)
- [Tableaux](#tableaux)
  - [`forEach` - parcourir les éléments d'un tableau](#foreach---parcourir-les-éléments-dun-tableau)
  - [`entries()` - parcourir les couples index/valeurs d'un tableau](#entries---parcourir-les-couples-indexvaleurs-dun-tableau)
  - [`in` - parcourir les clés d'un tableau](#in---parcourir-les-clés-dun-tableau)
  - [`of` - parcourir les valeurs d'un tableau](#of---parcourir-les-valeurs-dun-tableau)
  - [`find()` - premier élément qui satisfait une condition](#find---premier-élément-qui-satisfait-une-condition)
  - [`findIndex()` - premier index qui satisfait une condition](#findindex---premier-index-qui-satisfait-une-condition)
  - [`indexOf()` et `lastIndexOf()` - premier/dernier élément qui correspond](#indexof-et-lastindexof---premierdernier-élément-qui-correspond)
  - [`push()`, `pop()`, `shift()` et `unshift()` - ajouter/supprime au début/fin dans un tableau](#push-pop-shift-et-unshift---ajoutersupprime-au-débutfin-dans-un-tableau)
  - [`slice()` - ne conserver que certaines lignes d'un tableau](#slice---ne-conserver-que-certaines-lignes-dun-tableau)
  - [`splice()` - supprimer/insérer/remplacer des valeurs dans un tableau](#splice---supprimerinsérerremplacer-des-valeurs-dans-un-tableau)
  - [`concat()` - joindre deux tableaux](#concat---joindre-deux-tableaux)
  - [`join()` - joindre des chaînes de caractères](#join---joindre-des-chaînes-de-caractères)
  - [`keys()` et `values()` - les clés/valeurs d'un objet](#keys-et-values---les-clésvaleurs-dun-objet)
  - [`includes()` - vérifier si une valeur est présente dans un tableau](#includes---vérifier-si-une-valeur-est-présente-dans-un-tableau)
  - [`every()` et `some()` - vérifier si plusieurs valeurs sont toutes/quelques présentes dans un tableau](#every-et-some---vérifier-si-plusieurs-valeurs-sont-toutesquelques-présentes-dans-un-tableau)
  - [`fill()` - remplir un tableau avec des valeurs](#fill---remplir-un-tableau-avec-des-valeurs)
  - [`flat()` - aplatir un tableau](#flat---aplatir-un-tableau)
  - [`sort()` - pour trier un tableau](#sort---pour-trier-un-tableau)
  - [`map()` - tableau avec les résultats d'une fonction](#map---tableau-avec-les-résultats-dune-fonction)
  - [`filter()` - tableau avec les éléments passant un test](#filter---tableau-avec-les-éléments-passant-un-test)
  - [`groupBy()` - regroupe les éléments d'un tableau selon un règle](#groupby---regroupe-les-éléments-dun-tableau-selon-un-règle)
  - [`flatMap()` - chaînage de map() et flat()](#flatmap---chaînage-de-map-et-flat)
  - [`reduce()` et `reduceRight()` - réduire un tableau à une seule valeur](#reduce-et-reduceright---réduire-un-tableau-à-une-seule-valeur)
  - [`reverse()` - inverser l'ordre du tableau](#reverse---inverser-lordre-du-tableau)
- [Techniques](#techniques)
  - [\`\`(backticks) - pour des expressions intelligentes](#backticks---pour-des-expressions-intelligentes)
  - [`new Set()` - pour supprimer les doublons](#new-set---pour-supprimer-les-doublons)
- [Fonctions](#fonctions)
  - [Déclaration de fonction](#déclaration-de-fonction)
  - [Fonctions immédiatement invoquées (IIFE)](#fonctions-immédiatement-invoquées-iife)
- [Conclusion](#conclusion)

<svg height="12" width="100%" style="padding-top:2em;padding-bottom:1em">
  <rect y="5" width="100%" height="5" fill="#7191B8"/>
</svg>

# Introduction

> Votre introduction avec notamment les objectifs opérationnels du module.

# Opérateurs javascript

## opérateur `?:`

> L'expression `question?valeur1:valeur2` retournera `valeur1` si `question` vaut `true` sinon elle retournera `valeur2`.

```javascript
const age = 15;
const resultat = age >= 18 ? 'majeur' : 'mineur'; // 'mineur'
```

## opérateur `??`

Cet opérateur logique se nomme l'opérateur de "coalescence des nuls".

> Renvoie son opérande de droite lorsque son opérande de gauche vaut `null` ou `undefined` et qui renvoie son opérande de gauche sinon.

```javascript
const foo1 = null ?? 'default'; // "default"
const foo2 = 0 ?? 42; // 0
```

>[!CAUTION]
>Contrairement à l'opérateur logique OU (`||`), l'opérande de gauche sera également renvoyé s'il s'agit d'une valeur équivalente à `false` et pas seulement `null` et `undefined`.
>
>⚠️ En d'autres termes **ATTENTION** ‼️ lors de l'utilisation de `||` pour fournir une valeur par défaut à une variable, car on peut rencontrer des comportements inattendus lorsqu'on considère certaines valeurs comme correctes et utilisables (par exemple une chaine vide `''` ou `0`) ‼️

```javascript
const foo3 = 0 || 42; // 42 => ATTENTION !
const foo4 = 1 || 42; // 1
const foo5 = null || 'salut !'; // 'salut !'
const foo6 = '' || 'salut !'; // 'salut !' => ATTENTION !
```

## opérateur `??=`

Cet opérateur logique se nomme l'opérateur d'affectation de "coalescence des nuls", également connu sous le nom d'opérateur affectation logique nulle.

> Évalue l'opérande de droite et l'attribue à gauche **UNIQUEMENT si l'opérande de gauche est nulle** (`null` ou `undefined`).

```javascript
const a = { duration: 50 };
a.duration ??= 10; // pas fait
a.speed ??= 25; // fait => { duration: 50, speed: 25 }
```

## opérateur de décomposition 'spread' `...`

L'opérateur de décomposition spread `...` permet de décomposer un itérable (comme un tableau) en en ses éléments distincts. Cela permet de rapidement copier tout ou une partie d'un tableau existant dans un autre tableau ou d'en extraire facilement des parties.

```javascript
// Combiner des valeurs existantes dans un nouveau tableau
const numbersOne = [1, 2, 3];
const numbersTwo = [4, 5, 6];
const numbersCombined = [...numbersOne, ...numbersTwo];

// Extraire uniquement ce qui est utile d'un tableau
const numbers = [1, 2, 3, 4, 5, 6];
const [one, two, ...rest] = numbers;

// Mariage d'objets avec mise à jour :-)
const myVehicle = {
    brand: 'Ford',
    model: 'Mustang',
    color: 'red',
};
const updateMyVehicle = {
    type: 'car',
    year: 2021,
    color: 'yellow',
};
const myUpdatedVehicle = { ...myVehicle, ...updateMyVehicle };
```

## Déstructuration

L'opérateur de décomposition spread `...` sert aussi à isoler certains éléments afin de les utiliser ensuite, et de **mettre le reste** d'un coup ailleurs.

```javascript
const valeurs = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
const [a, b, ...c] = valeurs;
console.log(a); // 1
console.log(b); // 2
console.log(c); // [3, 4, 5, 6, 7, 8, 9, 10]
```

<svg height="12" width="100%" style="padding-top:2em;padding-bottom:1em">
  <rect y="5" width="100%" height="5" fill="#7191B8"/>
</svg>

# Date et Heure

Lien vers la documentation officielle : [https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Global_Objects/Date](https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Global_Objects/Date)

## Obtenir la date et/ou heure actuelle

```javascript
const maintenant = new Date(); // Obtenir l'un comme l'autre

console.log(maintenant.toLocaleDateString()); // ex: "06.06.2025"
console.log(maintenant.toLocaleTimeString()); // ex: "15:23:42"

const jour = maintenant.getDate();
const mois = maintenant.getMonth() + 1; // Attention : janvier = 0
const annee = maintenant.getFullYear();
const heure = maintenant.getHours();
const minute = maintenant.getMinutes();
const seconde = maintenant.getSeconds();
console.log(`${jour}/${mois}/${annee} - ${heure}h${minute}`);

// Au format ISO (standard international)
console.log(maintenant.toISOString()); // ex: "2025-06-06T13:23:42.123Z"
```

<svg height="12" width="100%" style="padding-top:2em;padding-bottom:1em">
  <rect y="5" width="100%" height="5" fill="#7191B8"/>
</svg>

# Math

Lien vers la documentation officielle : [https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Global_Objects/Math](https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Global_Objects/Math)

## `Math.PI` - la constante π

Représente la constante Pi (environ 3.14159)

```javascript
console.log(Math.PI);

// Resultat
3.141592653589793
```

## `Math.abs()` - la \|valeur absolue\| d'un nombre

Retourne la valeur absolue d'un nombre (pas de valeur négative)

```javascript
function difference(a, b) {
  return Math.abs(a - b);
}

console.log(difference(3, 5));

// Resultat
2
```

## `Math.pow()` - élever à une puissance

Permet d'élever un nombre à une puissance. Le premier nombre est l'indice et le 2eme est l'exposant

```javascript
console.log(Math.pow(7, 3));

// Resultat
343
```

## `Math.min()` - plus petite valeur

Renvoie la plus petite valeur d'une collection

```javascript
console.log(Math.min(2, 3, 1));

// Resultat
1
```

## `Math.max()` - plus grande valeur

Renvoie la plus grande valeur d'une collection

```javascript
console.log(Math.max(2, 3, 1));

// Resultat
3
```

## `Math.ceil()` - arrondir à la prochaine valeur entière la plus proche

Arrondit à la valeur entière la plus proche, mais seulement vers le haut

```javascript
console.log(Math.ceil(7.004));

// Resultat
8
```

## `Math.floor()` - arrondir à la précédente valeur entière la plus proche

Arrondit à la valeur entière la plus proche, mais seulement vers le bas

```javascript
console.log(Math.floor(7.95));

// Resultat
7
```

## `Math.round()` - arrondir à la valeur entière la plus proche

Permet d'arrondir un nombre à la valeur entière la plus proche.  
Exemple pour calculer une note d'école arrondie:

```javascript
Math.round((48 / 52) * 5 + 1)

// Resultat
6
```

## `Math.trunc()` - supprime la virgule et retourne la partie entière d'un nombre

```javascript
Math.trunc(13.37)

// Résultat
13
```

## `Math.sqrt()` - la raçine carrée d'un nombre

Fais la racine carrée d'un nombre

```javascript
Math.sqrt(4)

// Resultat 
2
```

## `Math.random()` - générer un nombre aléatoire entre 0.0 (compris) et 1.0 (non compris)

Génère une valeur aléatoire entre 0.0 et 1, peut ensuite être adaptée pour renvoyer d'autres valeurs

```javascript
function getRandomInt(max) {
  return Math.floor(Math.random() * max);
}

console.log(getRandomInt(3));
// Resultat
1, 2 ou 3

```

<svg height="12" width="100%" style="padding-top:2em;padding-bottom:1em">
  <rect y="5" width="100%" height="5" fill="#7191B8"/>
</svg>

# JSON

Lien vers la documentation officielle : [https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Global_Objects/JSON](https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Global_Objects/JSON)

## `JSON.stringify()` - transformer un objet Javascript en JSON

Convertit une valeur JavaScript en une chaîne JSON, en remplaçant éventuellement les valeurs si une fonction de remplacement est spécifiée ou en incluant éventuellement uniquement les propriétés spécifiées si un tableau de remplacement est spécifié.

```javascript
console.log(JSON.stringify({ x: 5, y: 6 }));

// Résultat
{"x":5,"y":6}

```

## `JSON.parse()` - transformer du JSON en objet Javascript

Analyse une chaîne JSON et construit la valeur ou l'objet JavaScript correspondant. Une fonction de restauration optionnelle peut être fournie pour effectuer une transformation sur l'objet résultant avant son renvoi.  
```javascript
const json = '{"result":true, "count":42}';
const obj = JSON.parse(json);

console.log(obj.count);

console.log(obj.result);

// Résultat
42
true
```

<svg height="12" width="100%" style="padding-top:2em;padding-bottom:1em">
  <rect y="5" width="100%" height="5" fill="#7191B8"/>
</svg>

# Chaînes de caractères

Lien vers la documentation officielle : [https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Global_Objects/String](https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Global_Objects/String)

## `split()` - un ciseau qui coupe une chaîne là où un caractère apparaît et produit un tableau

Permet de séparer un string json en fonction du charatère spécifié et renvoie un nouveau tableau. 

```javascript
const str = "The quick brown fox jumps over the lazy dog.";

const words = str.split(" ");
console.log(words[3]);

// Résultat
fox
```

## `trim()`, `trimStart()` et `trimEnd()` - épuration des espaces en trop dans une chaîne (trimming)

Description à faire par vos soins...

```javascript
A FAIRE PAR VOS SOINS...
SIMPLE, DROIT AU BUT, UTILE, STYLE PENSE-BÊTE
```

## `padStart()` et `padEnd()` - aligner le contenu dans une chaîne de caractères

Description à faire par vos soins...

```javascript
A FAIRE PAR VOS SOINS...
SIMPLE, DROIT AU BUT, UTILE, STYLE PENSE-BÊTE
```

<svg height="12" width="100%" style="padding-top:2em;padding-bottom:1em">
  <rect y="5" width="100%" height="5" fill="#7191B8"/>
</svg>

# Console

Lien vers la documentation officielle : [https://developer.mozilla.org/fr/docs/Web/API/console](https://developer.mozilla.org/fr/docs/Web/API/console)

## `console.log()` - Afficher un message sur la console

```javascript
console.log('Coucou !'); // Coucou !
```

## `console.info()`, `warn()` et `error()` - Afficher un message sur la console (filtrables)

Description à faire par vos soins...

```javascript
A FAIRE PAR VOS SOINS...
SIMPLE, DROIT AU BUT, UTILE, STYLE PENSE-BÊTE
```

## `console.table()` - Afficher tout un tableau ou un objet sur la console

Description à faire par vos soins...

```javascript
A FAIRE PAR VOS SOINS...
SIMPLE, DROIT AU BUT, UTILE, STYLE PENSE-BÊTE
```

## `console.time()`, `timeLog()` et `timeEnd()` - Chronométrer une durée d'exécution

Description à faire par vos soins...

```javascript
A FAIRE PAR VOS SOINS...
SIMPLE, DROIT AU BUT, UTILE, STYLE PENSE-BÊTE
```

<svg height="12" width="100%" style="padding-top:2em;padding-bottom:1em">
  <rect y="5" width="100%" height="5" fill="#7191B8"/>
</svg>

# Tableaux

Lien vers la documentation officielle : [https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Global_Objects/Array](https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Global_Objects/Array)

## `forEach` - parcourir les éléments d'un tableau

Description à faire par vos soins...

```javascript
A FAIRE PAR VOS SOINS...
SIMPLE, DROIT AU BUT, UTILE, STYLE PENSE-BÊTE
```

## `entries()` - parcourir les couples index/valeurs d'un tableau

Description à faire par vos soins...

```javascript
A FAIRE PAR VOS SOINS...
SIMPLE, DROIT AU BUT, UTILE, STYLE PENSE-BÊTE
```

## `in` - parcourir les clés d'un tableau

Description à faire par vos soins...

```javascript
A FAIRE PAR VOS SOINS...
SIMPLE, DROIT AU BUT, UTILE, STYLE PENSE-BÊTE
```

## `of` - parcourir les valeurs d'un tableau

Description à faire par vos soins...

```javascript
A FAIRE PAR VOS SOINS...
SIMPLE, DROIT AU BUT, UTILE, STYLE PENSE-BÊTE
```

## `find()` - premier élément qui satisfait une condition

Description à faire par vos soins...

```javascript
A FAIRE PAR VOS SOINS...
SIMPLE, DROIT AU BUT, UTILE, STYLE PENSE-BÊTE
```

## `findIndex()` - premier index qui satisfait une condition

Description à faire par vos soins...

```javascript
A FAIRE PAR VOS SOINS...
SIMPLE, DROIT AU BUT, UTILE, STYLE PENSE-BÊTE
```

## `indexOf()` et `lastIndexOf()` - premier/dernier élément qui correspond

Description à faire par vos soins...

```javascript
A FAIRE PAR VOS SOINS...
SIMPLE, DROIT AU BUT, UTILE, STYLE PENSE-BÊTE
```

## `push()`, `pop()`, `shift()` et `unshift()` - ajouter/supprime au début/fin dans un tableau

Description à faire par vos soins...

```javascript
A FAIRE PAR VOS SOINS...
SIMPLE, DROIT AU BUT, UTILE, STYLE PENSE-BÊTE
```

## `slice()` - ne conserver que certaines lignes d'un tableau

Description à faire par vos soins...

```javascript
A FAIRE PAR VOS SOINS...
SIMPLE, DROIT AU BUT, UTILE, STYLE PENSE-BÊTE
```

## `splice()` - supprimer/insérer/remplacer des valeurs dans un tableau

Description à faire par vos soins...

```javascript
A FAIRE PAR VOS SOINS...
SIMPLE, DROIT AU BUT, UTILE, STYLE PENSE-BÊTE
```

## `concat()` - joindre deux tableaux

Description à faire par vos soins...

```javascript
A FAIRE PAR VOS SOINS...
SIMPLE, DROIT AU BUT, UTILE, STYLE PENSE-BÊTE
```

## `join()` - joindre des chaînes de caractères

Description à faire par vos soins...

```javascript
A FAIRE PAR VOS SOINS...
SIMPLE, DROIT AU BUT, UTILE, STYLE PENSE-BÊTE
```

## `keys()` et `values()` - les clés/valeurs d'un objet

Description à faire par vos soins...

```javascript
A FAIRE PAR VOS SOINS...
SIMPLE, DROIT AU BUT, UTILE, STYLE PENSE-BÊTE
```

## `includes()` - vérifier si une valeur est présente dans un tableau

Description à faire par vos soins...

```javascript
A FAIRE PAR VOS SOINS...
SIMPLE, DROIT AU BUT, UTILE, STYLE PENSE-BÊTE
```

## `every()` et `some()` - vérifier si plusieurs valeurs sont toutes/quelques présentes dans un tableau

Description à faire par vos soins...

```javascript
A FAIRE PAR VOS SOINS...
SIMPLE, DROIT AU BUT, UTILE, STYLE PENSE-BÊTE
```

## `fill()` - remplir un tableau avec des valeurs

Description à faire par vos soins...

```javascript
A FAIRE PAR VOS SOINS...
SIMPLE, DROIT AU BUT, UTILE, STYLE PENSE-BÊTE
```

## `flat()` - aplatir un tableau

Description à faire par vos soins...

```javascript
A FAIRE PAR VOS SOINS...
SIMPLE, DROIT AU BUT, UTILE, STYLE PENSE-BÊTE
```

## `sort()` - pour trier un tableau

Permet de trier les objets du tableau par odre alphabétique ou ordre croissant pour les chiffres. 

```javascript
// Code
const months = ["March", "Jan", "Feb", "Dec"];
months.sort();
console.log(months);

const array = [1, 30, 4, 21, 100000];
array.sort();
console.log(array);

// Résultat 
Array ["Dec", "Feb", "Jan", "March"]
Array [1, 100000, 21, 30, 4]
```

## `map()` - tableau avec les résultats d'une fonction

Permet de gérer l'affichage de données (tableaux, JSON, etc.)

```javascript
// Données
const dataMotos = [
    {
        marque: "Honda",
        modeles: [
            { nom: "CB750 Four", annee: 1969, prix: 12000, puissance: 67, couple: 60 },
            { nom: "Africa Twin CRF1100L", annee: 2020, prix: 15000, puissance: 102, couple: 105 },
            { nom: "CBR1000RR Fireblade", annee: 2024, prix: 23000, puissance: 218, couple: 113 },
            { nom: "Gold Wing", annee: 2024, prix: 33000, puissance: 126, couple: 170 },
        ]
    }, ... ]

//Code
function actionM1() {
    const resultat = dataMotos.map((moto) => moto.marque);

    afficherObjet(resultat);
}

//Résultat
[
   "Honda",
   "Yamaha",
   "Ducati",
   "BMW",
   "Harley-Davidson"
]
```

## `filter()` - tableau avec les éléments passant un test

Permet de filtrer des données afin d'obtenir seulement celles dont on a besoin

```javascript
// Données
const dataVilles = [
    // FRIBOURG (FR)
    { ville: "Fribourg", canton: "FR", habitants: 39000 },
    { ville: "Bulle", canton: "FR", habitants: 24400 },
    { ville: "Villars-sur-Glâne", canton: "FR", habitants: 12500 },
    ... ]
// Code
function actionF2() {

    const resultat = dataVilles.filter(ville => ville.habitants > 10000 && ville.habitants < 25000 && ville.canton === "FR");

    afficherObjet(resultat);
}

// Résultat
[
   {
      "ville": "Bulle",
      "canton": "FR",
      "habitants": 24400
   },
   {
      "ville": "Villars-sur-Glâne",
      "canton": "FR",
      "habitants": 12500
   }
]
```

## `groupBy()` - regroupe les éléments d'un tableau selon un règle

Description à faire par vos soins...

```javascript
// Code
const inventory = [
  { name: "asparagus", type: "vegetables", quantity: 9 },
  { name: "bananas", type: "fruit", quantity: 5 },
  { name: "goat", type: "meat", quantity: 23 },
  { name: "cherries", type: "fruit", quantity: 12 },
  { name: "fish", type: "meat", quantity: 5 },
];

const result = Object.groupBy(inventory, ({ quantity }) =>
  quantity < 6 ? "restock" : "sufficient",
);

// Resultat
Array [Object { name: "bananas", type: "fruit", quantity: 5 }, Object { name: "fish", type: "meat", quantity: 5 }]
```

## `flatMap()` - chaînage de map() et flat()

Permet de créer un nouveau tableau à partir du résultat d'un traitement d'élément. 

```javascript
// Code
const resultat = dataMotos.flatMap((moto) => moto.modeles.map((modele) => `${moto.marque} / ${modele.nom}`)).sort();

// Résultat
[
   "BMW / K1600GTL",
   "BMW / R nineT",
   "BMW / R1250GS",
   "BMW / S1000RR",
   ...
]
```

## `reduce()` et `reduceRight()` - réduire un tableau à une seule valeur

Exécute une fonction décrite par l'utilisateur sur chaque élément du tableau et retourne une seule valeur à la fin.  
`reduceRight()` permet de faire la même chose, mais de droite à gauche (`reduce` le fait de gauche à droite).

```javascript
// Code
const resultat = dataEvaluations.reduce((petit, note) => (note.date < petit.date ? { ...note } : petit), dataEvaluations[0]);

    afficherObjet(resultat.date);

// Resultat

```

## `reverse()` - inverser l'ordre du tableau

Description à faire par vos soins...

```javascript
A FAIRE PAR VOS SOINS...
SIMPLE, DROIT AU BUT, UTILE, STYLE PENSE-BÊTE
```

<svg height="12" width="100%" style="padding-top:2em;padding-bottom:1em">
  <rect y="5" width="100%" height="5" fill="#7191B8"/>
</svg>

# Techniques

## ``(backticks) - pour des expressions intelligentes

Description à faire par vos soins...

```javascript
A FAIRE PAR VOS SOINS...
SIMPLE, DROIT AU BUT, UTILE, STYLE PENSE-BÊTE
```

## `new Set()` - pour supprimer les doublons

Crée un nouveau tableau sans doublon.

```javascript
// Code
const resultat = [...new Set(dataEvaluations.map((e) => e.nom + ' ' + e.prenom))].sort();
    afficherObjet(resultat);

// Resultat 
[
   "D'ŒUF John",
   "FICE Eddy",
   "HARONI Mac",
   "NISSENS Remy",
   "RIQUE Théo",
   "TARISTE Guy",
   "TERNET Alain",
   "TERRIEUR Alain",
   "TERRIEUR Alex",
   "VOYANTE Claire"
]
```

<svg height="12" width="100%" style="padding-top:2em;padding-bottom:1em">
  <rect y="5" width="100%" height="5" fill="#7191B8"/>
</svg>

# Fonctions

## Déclaration de fonction

**Standard**

```javascript
function doStuff(a, b, c) {
    return a + b + c;
}
```

**Sous forme d'expression de fonction**

```javascript
const doStuff = function (a, b, c) {
    return a + b + c;
};
```

**Sous forme d'expression de fonction anonyme**

```javascript
const doStuff = (a, b, c) => {
    return a + b + c;
};
```

**Sous forme raccourcie**

S'il n'y a qu'un seul argument et que son corps n'a qu'une seule expression, on peut omettre le return et le corps de la fonction :

```javascript
const doStuff = (a) => `Salut ${a} !`;
```

## Fonctions immédiatement invoquées (IIFE)

IIFE = Immediately Invoked Function Expressions.

Ces fonctions sont définies et **exécutées immédiatement**. Elles sont souvent utilisées pour créer un **contexte isolé** ou encapsuler du code sans polluer l’espace global.

```javascript
(function(){ ... })()
```

ou

```javascript
(() => { ... })()
```

# Conclusion

## Ce que j'ai appris  

## Mes points forts

## Mes points faibles

