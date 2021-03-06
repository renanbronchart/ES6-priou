# #5 spread, opérateur (...)

Le spread operator sert à eclater un tableau en liste finie de valeur.
Exemple:
```javascript
//pour la création de nouveaux tableaux
var arr1 = [0, 1, 2];
var arr2 = [3, 4, 5];
arr3 = [...arr1, ...arr2]; //  [0,1,2,3,4,5]
```
Sur ES5 **.concat** est utilisé pour concatener les tableaux.
Exemple:
```javascript
//pour la création de nouveaux tableaux avec .concat
var arr1 = [0, 1, 2];
var arr2 = [3, 4, 5];
arr3 = = arr1.concat(arr2);
```

# Utiliser la décomposition dans les objets
La décomposition d'objets permet de lier des variables à partir des différentes propriétés d’un objet.

```javascript
var array1 = { toto: 'Eric', x: 42 };
var array2 = { tata: 'Gaoussou', y: 13 };

var clone = { ...array }; // Object { toto: 'Eric', x: 42 }

var fusion = { ...array1, ...array2 }; // Object { toto: 'Eric', x: 42, tata: 'Gaoussou' y: 28 };
```

# Utiliser la décomposition dans les appels de fonction

Avec ES6, il est désormais possible de passer des arguments à une fonction avec le spread :

```javascript
function f(x, y, z) { }
var args = [0, 1, 2];
f(...args);
```

On peut également décomposer grâce à l'opérateur et l'opérateur peut donc utiliser plusieurs arguments :

```javascript
function f(v, w, x, y, z) { }
var args = [0, 1];
f(-1, ...args, 2, ...[3]);
```

