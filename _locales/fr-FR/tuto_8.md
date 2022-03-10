# Niveau 2

## @showdialog

Vrai ou faux ?

## Étape 1

Supprime les blocs ``||basic:au démarrage||`` et ``||basic:toujours||``.

## Étape 2

Ajoute le bloc ``||logic: si vrai alors sinon||`` dans le bloc ``||input: lorsque secouer||``.

```blocks

input.onGesture(Gesture.Shake, function () {
    if (true) {
    	
    } else {
    	
    }
})

```

## Étape 3

Remplace la valeur ``||logic: vrai ||`` dans le bloc ``||logic: si vrai alors sinon||`` par le bloc ``||math: choisir au hasard vrai ou faux||``.

```blocks

input.onGesture(Gesture.Shake, function () {
    if (Math.randomBoolean()) {
    	
    } else {
    	
    }
})

```

## Étape 4

Ajoute le bloc ``||basic: montrer l'icone||`` sous le bloc ``||logic: alors||``.

```blocks

input.onGesture(Gesture.Shake, function () {
    if (Math.randomBoolean()) {
        basic.showIcon(IconNames.Yes)
    } else {
    	
    }
})

```

## Étape 5

Ajoute le bloc ``||basic: montrer l'icone||`` sous le bloc ``||logic: sinon||``.

```blocks

input.onGesture(Gesture.Shake, function () {
    if (Math.randomBoolean()) {
        basic.showIcon(IconNames.Yes)
    } else {
        basic.showIcon(IconNames.No)
    }
})

```

## Étape 6

Ajoute le bloc ``||loops: répéter 2 fois||`` au-dessus du bloc ``||logic: si alors sinon||``.

```blocks

input.onGesture(Gesture.Shake, function () {
    for (let index = 0; index < 2; index++) {
    	
    }
    if (Math.randomBoolean()) {
        basic.showIcon(IconNames.Yes)
    } else {
        basic.showIcon(IconNames.No)
    }
})

```

## Étape 7

Ajoute les blocs ``||basic: montrer l'icone||`` dans le bloc ``||loops: répéter deux fois||``.

Regarde les icones dans l'indice.

```blocks

input.onGesture(Gesture.Shake, function () {
    for (let index = 0; index < 2; index++) {
        basic.showIcon(IconNames.Diamond)
        basic.showIcon(IconNames.SmallDiamond)
        basic.showIcon(IconNames.Chessboard)
    }
    if (Math.randomBoolean()) {
        basic.showIcon(IconNames.Yes)
    } else {
        basic.showIcon(IconNames.No)
    }
})

```

## Étape 8

Télécharge le programme dans le micro:bit.

Teste le programme !

Dis une affirmation et secoue le micro:bit.

Que remarques-tu ?
