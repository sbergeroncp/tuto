# tuto_14

## @showdialog

Crée une boule de neige à l'aide du micro:bit.

## Étape 1

Supprime les blocs ``||basic:au démarrage||`` et ``||basic:toujours||``.


## Étape 2

Crée trois nouvelles fonctions à l'aide du bloc ``||functions: Créer une fonction||``.

Nomme les fonctions : neige1, neige2 et neige3.

```blocks

function neige1 () {
	
}
function neige2 () {
	
}
function neige3 () {
	
}

```

## Étape 3

Ajoute le bloc ``||functions: appel neige1||`` dans le bloc ``||input: lorsque le bouton A est pressé||``.

Ajoute le bloc ``||functions: appel neige2||`` sous le bloc ``||functions: appel neige1||``.

Ajoute le bloc ``||functions: appel neige3||`` sous le bloc ``||functions: appel neige2||``.

```blocks

input.onButtonPressed(Button.A, function () {
    neige1()
    neige2()
    neige3()
})
function neige1 () {
	
}
function neige2 () {
	
}
function neige3 () {
	
}

```

## Étape 4

Ajoute le bloc ``||led: allumer x / y||`` dans le bloc ``||functions: fonction neige1||``.

```blocks

function neige1 () {
    led.plot(0, 0)

```

## @showdialog

Voici les coordonnées x,y des LEDs sur l'écran du micro:bit.

Le but est d'allumer et/ou d'éteindre uniquement les LED aux coordonnées 0 à 4 pour x et y. 

Autrement dit, uniquement les LED à l'intérieur de la boule de neige.

![Atelier](https://pxt.azureedge.net/blob/dcab173218997aba45eb174b25cb128e3172bbb1/static/courses/csintro/coordinates/microbit-led-coords.png)


## Étape 5

Ajoute le bloc ``||math: choisir au hasard||`` à la valeur ``||math: x||`` et ``||math: y||`` dans le bloc ``||led: allumer x / y||``.

Modifie les valeurs de x (0 et 4) et de y (0 et 4).

```blocks

function neige1 () {
    led.plot(randint(0, 4), randint(0, 4))
}

```

## Étape 6

Ajoute le bloc ``||basic: pause (ms) 100||`` sous le bloc ``||led: allumer x / y||``.

```blocks

function neige1 () {
    led.plot(randint(0, 4), randint(0, 4))
    basic.pause(100)
}

```

## Étape 7

Ajoute le bloc ``||led: éteindre x / y||`` sous le bloc ``||basic: pause (ms) 100||``.

Ajoute le bloc ``||math: choisir au hasard||`` dans la valeur ``||math: x||`` et ``||math: y||`` du bloc ``||led: éteindre x / y||``.

Modifie les valeurs de ``||math: x||`` (0 et 4) et ``||math: y||`` (0 et 4).

```blocks

function neige1 () {
    led.plot(randint(0, 4), randint(0, 4))
    basic.pause(100)
    led.unplot(randint(0, 4), randint(0, 4))
}

```

## Étape 8

Ajoute le bloc ``||loops: répéter 3 fois||`` dans le bloc ``||input: lorsque le bouton A est pressé||``.

Et ajoute le bloc ``||functions: appel neige1||`` , le bloc ``||functions: appel neige2||`` et le bloc ``||functions: appel neige3||`` dans la boucle.

```blocks

input.onButtonPressed(Button.A, function () {
    for (let index = 0; index < 3; index++) {
        neige1()
        neige2()
        neige3()
    }
})
function neige1 () {
	
}
function neige2 () {
	
}
function neige3 () {
	
}


```

## Étape 9

Duplique les mêmes étapes pour le bloc ``||functions: fonction neige2||`` et le bloc ``||functions: fonction neige3||``.

## Étape 10

Ajoute le bloc ``||basic: effacer l'écran||`` sous le bloc ``||input: lorsque le bouton B est pressé||``.

```blocks

input.onButtonPressed(Button.B, function () {
    basic.clearScreen()
})

```

## Étape 11

Télécharge le programme dans le micro:bit.

Teste le programme!

Que remarques-tu ?