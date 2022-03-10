# tuto_15

## @showdialog

Le décompte musical!

## Étape 1

Supprime les blocs ``||basic:toujours||`` et ``||basic:au démarrage||``.

## Étape 2

Crée une ``||variables: variable||`` et donne lui le nom ``||variables:Temps||``.

Ajoute le bloc ``||variables: définir Temps à "4"||`` dans le bloc ``||input: lorsque le bout A est pressé||``.

```blocks

let Temps = 0
input.onButtonPressed(Button.A, function () {
    Temps = 4
})

```

## Étape 3

Ajoute le bloc ``||loops: répéter 3 fois||`` sous le bloc ``||variables: définir Nombre à "4"||``.

```blocks

let Temps = 0
input.onButtonPressed(Button.A, function () {
    Temps = 4
    for (let index = 0; index < 3; index++) {
    	
    }
})

```

## Étape 4

Ajoute le bloc ``||music: jouer ton Middle C pendant 1/4 temps||`` dans le bloc ``||loops: répéter 3 fois||``.

```blocks

let Temps = 0
input.onButtonPressed(Button.A, function () {
    Temps = 4
    for (let index = 0; index < 3; index++) {
        music.playTone(262, music.beat(BeatFraction.Quarter))
    }
})

```

## Étape 5

Ajoute le bloc ``||basic: montrer nombre||`` sous le bloc ``||music: jouer ton Middle C pendant 1/4 temps||``.

Ajoute le bloc ``||basic: pause (ms) 100||`` sous le bloc ``||basic: montrer nombre||``.

```blocks

let Temps = 0
input.onButtonPressed(Button.A, function () {
    Temps = 4
    for (let index = 0; index < 3; index++) {
        music.playTone(262, music.beat(BeatFraction.Quarter))
        basic.showNumber(0)
        basic.pause(100)
    }
})

```

## Étape 6

Ajoute le bloc ``||math: "0" - "0"||`` dans le bloc ``||basic: montrer nombre||``.

Remplace la valeur ``||math: 0 ||`` de gauche par le bloc ``||variables:Temps||``.

Remplace la valeur ``||math: 0 ||`` de droite par la valeur ``||math: 1 ||``. 

```blocks

let Temps = 0
input.onButtonPressed(Button.A, function () {
    Temps = 4
    for (let index = 0; index < 3; index++) {
        music.playTone(262, music.beat(BeatFraction.Quarter))
        basic.showNumber(Temps - 1)
        basic.pause(100)
    }
})

```

## Étape 7

Ajoute le bloc ``||variables: modifier Temps 1||`` sous le bloc ``||basic: pause (ms) 100)||``.

Remplace la valeur ``||variables: 1||`` par ``||variables: -1||`` dans le bloc ``||variables: modifier Temps de 1||``.

```blocks

let Temps = 4
for (let index = 0; index < 3; index++) {
    music.playTone(262, music.beat(BeatFraction.Quarter))
    basic.showNumber(Temps - 1)
    basic.pause(100)
    Temps += -1
}

```

## Étape 8

Ajoute le bloc ``||music: jouer ton Middle G pendant 1 temps||`` sous le bloc ``||loops: répéter 3 fois||``.

```blocks

let Temps = 0
input.onButtonPressed(Button.A, function () {
    Temps = 4
    for (let index = 0; index < 3; index++) {
        music.playTone(262, music.beat(BeatFraction.Quarter))
        basic.showNumber(Temps - 1)
        basic.pause(100)
        Temps += 1
    }
    music.playTone(392, music.beat(BeatFraction.Whole))
})

```
## Étape 9

Ajoute le bloc ``||basic:afficher texte "Hello!"||`` sous le bloc ``||music: jouer ton Middle G pendant 1 temps||``.

Remplace le texte ``||basic: Hello! ||`` par ``||basic: Go! ||``.

```blocks

let Temps = 0
input.onButtonPressed(Button.A, function () {
    Temps = 4
    for (let index = 0; index < 3; index++) {
        music.playTone(262, music.beat(BeatFraction.Quarter))
        basic.showNumber(Temps - 1)
        basic.pause(100)
        Temps += 1
    }
    music.playTone(392, music.beat(BeatFraction.Whole))
    basic.showString("Go!")
})


```

## Étape 10

Télécharge le programme dans le micro:bit.

Teste le programme!

Manipule le micro:bit. Que remarques-tu?