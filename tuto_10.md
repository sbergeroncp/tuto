# tuto_10

## @showdialog

Roche, papier, ciseau... allumettes!

## Étape 1

Supprime les blocs ``||basic:au démarrage||`` et ``||basic:toujours||``.

## Étape 2

Crée une ``||variables: variable||`` et donne lui le nom ``||variables:Main||``.

Ajoute le bloc ``||variables: définir Main à "0"||`` dans le bloc ``||input: lorsque secouer||``.

```blocks

let Main = 0
input.onGesture(Gesture.Shake, function () {
    Main = 0
})

```

## Étape 3

Remplace la valeur ``||variables: 0||`` dans le bloc ``||variables: définir Main à||`` par le bloc ``||math: choisir au hasard de "0" à "10"||``.

Remplace les valeurs ``||math: 0||`` et ``||math: 10||`` dans le bloc ``||math: choisir au hasard de "0" à "10"||`` par les valeurs ``||math: 1||`` et ``||math: 3||``.

```blocks

let Main = 0
input.onGesture(Gesture.Shake, function () {
    Main = randint(1, 3)
})

```

## Étape 4

Ajoute le bloc ``||logic: si vrai alors||`` sous le bloc ``||variables: définir Main à||``.

```blocks

let Main = 0
input.onGesture(Gesture.Shake, function () {
    Main = randint(1, 3)
    if (true) {
    	
    }
})

```

## Étape 5

Remplace le bloc ``||logic: vrai||`` par le bloc ``||logic: "0" = "0"||`` dans le bloc ``||logic: si alors||``.

```blocks

let Main = 0
input.onGesture(Gesture.Shake, function () {
    Main = randint(1, 3)
    if (0 == 0) {
    	
    }
})

```

## Étape 6

Remplace la valeur ``||logic: 0||`` de gauche du bloc ``||logic: "0" = "0"||`` par le bloc ``||variables:Main||``.

Remplace la valeur ``||logic: 0||`` de droite du bloc ``||logic: "0" = "0"||`` par la valeur ``||logic: 1||``.

La valeur 1 représente les ``||logic: ciseaux||``.

```blocks

let Main = 0
input.onGesture(Gesture.Shake, function () {
    Main = randint(1, 3)
    if (Main == 1) {
    	
    }
})

```

## Étape 7

Ajoute le bloc ``||basic: montrer l'icône||`` sous le bloc ``||logic: si alors ||``.

Ajoute le bloc ``||basic: pause (ms) 2000||`` sous le bloc ``||basic: montrer l'icône||``.

Ajoute le bloc ``||basic: effacer l'écran||`` sous le bloc ``||basic: pause (ms) 2000||``.

```blocks

let Main = 0
input.onGesture(Gesture.Shake, function () {
    Main = randint(1, 3)
    if (Main == 1) {
        basic.showIcon(IconNames.Scissors)
        basic.pause(2000)
        basic.clearScreen()
    }
})

```

## Étape 8

Ajoute le bloc ``||basic: pause (ms) 1000||`` sous le bloc ``||input: lorsque secouer||``.

```blocks

let Main = 0
input.onGesture(Gesture.Shake, function () {
    basic.pause(1000)
    Main = randint(1, 3)
    if (Main == 1) {
        basic.showIcon(IconNames.Scissors)
        basic.pause(2000)
        basic.clearScreen()
    }
})

``` 

## Étape 9

Oups! Les étapes pour programmer la roche, le papier et les allumettes ont disparu.

Programme le micro:bit pour qu'il puisse afficher les autres éléments du jeu.

La valeur 1 représente les ``||logic: ciseaux||``. 

La valeur 2 représente la ``||logic: roche||``.

La valeur 3 représente le ``||logic: papier||``. 



## Étape 10

Télécharge le programme dans le micro:bit.

Teste le programme avec une autre équipe!

Es-tu capable d'ajouter à la séquence de programmation une autre valeur ? La valeur 4 pourrait représenter les ``||logic: allumettes||`` .