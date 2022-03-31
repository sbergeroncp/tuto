# tuto_7

## @showdialog

Affiche une image sur l'écran du micro:bit en fonction du niveau d'intensité lumineuse de la pièce.

## Étape 1

Supprime le bloc ``||basic:au démarrage||``.

## Étape 2

Crée une ``||variables: variable||`` et donne lui le nom ``||variables:Lumiere||``. (sans accent sur le "è")

Ajoute le bloc ``||variables: définir Lumiere à "0"||`` dans le bloc ``||basic: toujours||``.

```blocks

let Lumiere = 0
basic.forever(function () {
    Lumiere = 0
})

```

## Étape 3

Remplace la valeur ``||variables: 0||`` du bloc ``||variables: définir Lumiere ||`` par le bloc ``||input: niveau d'intensité lumineuse||``. 


```blocks

let Lumiere = 0
basic.forever(function () {
    Lumiere = input.lightLevel()
})

```

## Étape 4

Ajoute le bloc ``|| logic: si vrai alors sinon ||`` sous le bloc ``|| variables: définir Lumiere ||``.

```blocks

let Lumiere = 0
basic.forever(function () {
    Lumiere = input.lightLevel()
    if (true) {
    	
    } else {
    	
    }
})

```

## Étape 5

Remplace la valeur ``|| logic: vrai ||`` du bloc ``|| logic: si vrai alors sinon ||`` par le bloc ``|| logic: 0 < 0||``. 

```blocks

let Lumiere = 0
basic.forever(function () {
    Lumiere = input.lightLevel()
    if (0 < 0) {
    	
    } else {
    	
    }
})

```

## Étape 6

Remplace la valeur ``|| logic: 0 ||`` à la gauche du bloc ``|| logic: 0 < 0||`` par le bloc ``|| variables: Lumiere||``. 

Remplace la valeur ``|| logic: 0 ||`` à la droite du bloc ``|| logic: 0 < 0||`` par la valeur ``|| logic: 40 ||``.

Lorsque le niveau d'intensité lumieuse est sous 40 dans une pièce, il fait généralement sombre! 

Passe ta main au-dessous du micro:bit au besoin.

```blocks

let Lumiere = 0
basic.forever(function () {
    Lumiere = input.lightLevel()
    if (Lumiere < 40) {
    	
    } else {
    	
    }
})

```

## Étape 7

Ajoute le bloc ``|| basic: Montrer LEDs ||`` sous le bloc ``|| logic: si ||``.

Remplis les 25 cases pour activer toutes les LEDs du micro:bit.

Lorsque le niveau d'intensité lumineuse sera sous 40, l'image dessinée devrait s'afficher sur l'écran du micro:bit.

```blocks

let Lumiere = 0
basic.forever(function () {
    Lumiere = input.lightLevel()
    if (Lumiere < 40) {
        basic.showLeds(`
            # # # # #
            # # # # #
            # # # # #
            # # # # #
            # # # # #
            `)
    } else {
    	
    }
})

```

## Étape 8

Ajoute le bloc ``|| basic: montrer LEDs ||`` sous le bloc ``|| logic: sinon ||``.

Active seulement la LED centrale du micro:bit.

Lorsque le niveau d'intensité lumineuse sera au-dessus de 40, l'image dessinée devrait s'afficher sur l'écran du micro:bit.

```blocks

let Lumiere = 0
basic.forever(function () {
    Lumiere = input.lightLevel()
    if (Lumiere < 40) {
        basic.showLeds(`
            # # # # #
            # # # # #
            # # # # #
            # # # # #
            # # # # #
            `)
    } else {
        basic.showLeds(`
            . . . . .
            . . . . .
            . . # . .
            . . . . .
            . . . . .
            `)
    }
})

```

## Étape 9

Télécharge le programme dans le micro:bit.

Teste le programme!

Manipule le micro:bit. Que remarques-tu?
