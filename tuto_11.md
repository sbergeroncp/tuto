# tuto_11

## @showdialog

Une boussole pour s'orienter!

## @showdialog

Voici les points cardinaux importants sur une boussole.

![Atelier](https://cdn.sanity.io/images/ajwvhvgo/production/c1ba4627f246bc638f48cd51afb80342fd1db540-2019x1878.png?w=653&q=80&fit=max&auto=format)

## Étape 1

Supprime le bloc ``||basic:au démarrage||``.

## Étape 2

Crée une ``||variables: variable||`` et donne lui le nom ``||variables:Degres||``. (sans accent sur le "é")

Ajoute le bloc ``||variables: définir Degres à "0"||`` dans le bloc ``||basic: toujours||``.

```blocks

let Degres = 0
basic.forever(function () {
    Degres = 0
})

```

## Étape 3

Remplace la valeur ``||variables: 0 ||`` dans le bloc ``||variables: définir Degres||`` par le bloc ``||input: direction de la boussole||``.


```blocks

let Degres = 0
basic.forever(function () {
    Degres = input.compassHeading()
})

```

## Étape 4

Ajoute le bloc ``||logic: si vrai alors sinon si||`` sous le bloc ``||variables: définir Degres||``.

Ajoute 5 conditions en tout en appuyant sur le bouton ``||logic: +||``.

```blocks

let Degres = 0
basic.forever(function () {
    Degres = input.compassHeading()
    if (true) {
    	
    } else if (false) {
    	
    } else if (false) {

    } else if (false) {

    } else {
    	
    }
})

```

## Étape 5

Ajoute le bloc ``||logic: "0" = "0"||`` dans le bloc ``||logic: si||``.

```blocks

let Degres = 0
basic.forever(function () {
    Degres = input.compassHeading()
    if (0 < 0) {
    	
    } else if (false) {
    	
    } else if (false) {

    } else if (false) {
    	
    } else {
    	
    }
})

```

## Étape 6

Remplace la valeur ``||logic: 0 ||`` de gauche du bloc ``||logic: "0" = "0"||`` par le bloc ``||variables:Degres||``.

Remplace la valeur ``||logic: 0 ||`` de droite du bloc ``||logic: "0" = "0"||`` par la valeur ``||logic: 45 ||``.

La valeur 45 représente la coordonnée nord-est.

```blocks

let Degres = 0
basic.forever(function () {
    Degres = input.compassHeading()
    if (Degres < 45) {
    	
    } else if (false) {

    } else if (false) {

    } else if (false) {
    	
    } else {
    	
    }
})

```

## Étape 7

Ajoute le bloc ``||basic: afficher le texte||`` sous le bloc ``||logic: si Degres < 45||``.

Remplace ``||basic: Hello ||`` du bloc ``||basic: afficher le texte||`` par la lettre ``||basic: N ||``.

```blocks

let Degres = 0
basic.forever(function () {
    Degres = input.compassHeading()
    if (Degres < 45) {
        basic.showString("Hello")
    } else if (false) {

    } else if (false) {

    } else if (false) {
    	
    } else {
    	
    }
})

```

## Étape 8

Ajoute le bloc ``||basic: afficher le texte||`` sous le dernier bloc ``||logic: sinon||``.

Remplace ``||basic: Hello ||`` du bloc ``||basic: afficher le texte||`` par la lettre ``||basic: N ||``.

```blocks

let Degres = 0
basic.forever(function () {
    Degres = input.compassHeading()
    if (Degres < 45) {
        basic.showString("N")
    } else if (false) {

    } else if (false) {
    	
    } else if (false) {
    	
    } else {
        basic.showString("N")
    }
})

```

## @showdialog

Oups! Les étapes pour programmer les autres points cardinaux ont disparu.

Programme le micro:bit pour qu'il puisse afficher les autres points cardinaux.

La valeur < 45 représente le point cardninal ``||input: nord||``. La valeur < 135 représente le point cardninal ``||input: est||``.

La valeur < 225 représente le point cardninal ``||input: sud||``. La valeur < 315 représente le point cardninal ``||input: ouest||`` .

## Étape 8

Télécharge le programme dans le micro:bit.

Tu devras sans doute calibrer la boussole avant de l'utiliser.

Tourne le microbit doucement dans tous les sens pour activer toutes les LEDs de l'écran.

Teste le programme ! 

Quel bâtiment et/ou lieu retrouve-t-on au nord de l'école ? au sud ? à l'est ? à l'ouest ?