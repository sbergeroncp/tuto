# tuto_12

## @showdialog

Compose une mélodie !

## Étape 1

Supprime le bloc ``||basic:toujours||``.

## Étape 2

Ajoute le bloc ``||music: régler le tempo à (bpm) 120 ||`` dans le bloc ``||basic: au démarrage||``.

```blocks

music.setTempo(120)

```

## Étape 3

Ajoute les blocs ``||music: jouer ton Middle pendant 1 temps ||`` dans le bloc ``||input: lorsque le bouton A est pressé||``.

Attention ! Plusieurs blocs sont différents.

```blocks

input.onButtonPressed(Button.A, function () {
    music.playTone(262, music.beat(BeatFraction.Whole))
    music.playTone(294, music.beat(BeatFraction.Whole))
    music.playTone(330, music.beat(BeatFraction.Whole))
    music.playTone(262, music.beat(BeatFraction.Whole))
})

```

## Étape 4

Ajoute la séquence de notes musicales dans le bloc ``||loops: répéter 2 fois ||``.

```blocks

input.onButtonPressed(Button.A, function () {
    for (let index = 0; index < 2; index++) {
        music.playTone(262, music.beat(BeatFraction.Whole))
        music.playTone(294, music.beat(BeatFraction.Whole))
        music.playTone(330, music.beat(BeatFraction.Whole))
        music.playTone(262, music.beat(BeatFraction.Whole))
    }
})

```

## Étape 5

Ajoute les blocs ``||music: jouer ton Middle pendant 1 temps ||`` sous le bloc ``||loops: répéter 2 fois ||``.

Attention ! Plusieurs blocs sont différents.

Attention ! La dernière note joue pendant 2 temps.

```blocks

input.onButtonPressed(Button.A, function () {
    for (let index = 0; index < 2; index++) {
        music.playTone(262, music.beat(BeatFraction.Whole))
        music.playTone(294, music.beat(BeatFraction.Whole))
        music.playTone(330, music.beat(BeatFraction.Whole))
        music.playTone(262, music.beat(BeatFraction.Whole))
    }
    music.playTone(330, music.beat(BeatFraction.Whole))
    music.playTone(349, music.beat(BeatFraction.Whole))
    music.playTone(392, music.beat(BeatFraction.Double))
})


```

## Étape 6

Ajoute la séquence de notes musicales dans le bloc ``||loops: répéter 2 fois ||``.

```blocks

input.onButtonPressed(Button.A, function () {
    for (let index = 0; index < 2; index++) {
        music.playTone(262, music.beat(BeatFraction.Whole))
        music.playTone(294, music.beat(BeatFraction.Whole))
        music.playTone(330, music.beat(BeatFraction.Whole))
        music.playTone(262, music.beat(BeatFraction.Whole))
    }
    for (let index = 0; index < 2; index++) {
        music.playTone(330, music.beat(BeatFraction.Whole))
        music.playTone(349, music.beat(BeatFraction.Whole))
        music.playTone(392, music.beat(BeatFraction.Double))
    }
})


```

## Étape 7

Continue à programmer la chanson.

Regarde attentivement l'indice, car il y a plusieurs notes à ajouter!

Bonne chance!

```blocks

input.onButtonPressed(Button.A, function () {
    for (let index = 0; index < 2; index++) {
        music.playTone(262, music.beat(BeatFraction.Whole))
        music.playTone(294, music.beat(BeatFraction.Whole))
        music.playTone(330, music.beat(BeatFraction.Whole))
        music.playTone(262, music.beat(BeatFraction.Whole))
    }
    for (let index = 0; index < 2; index++) {
        music.playTone(330, music.beat(BeatFraction.Whole))
        music.playTone(349, music.beat(BeatFraction.Whole))
        music.playTone(392, music.beat(BeatFraction.Double))
    }
    for (let index = 0; index < 2; index++) {
        music.playTone(392, music.beat(BeatFraction.Half))
        music.playTone(440, music.beat(BeatFraction.Half))
        music.playTone(392, music.beat(BeatFraction.Half))
        music.playTone(349, music.beat(BeatFraction.Half))
        music.playTone(330, music.beat(BeatFraction.Whole))
        music.playTone(262, music.beat(BeatFraction.Whole))
    }
    for (let index = 0; index < 2; index++) {
        music.playTone(262, music.beat(BeatFraction.Whole))
        music.playTone(196, music.beat(BeatFraction.Whole))
        music.playTone(262, music.beat(BeatFraction.Double))
    }
})
```

## Étape 7

Télécharge le programme dans le micro:bit.

Teste le programme! 

Relis les écouteurs au micro:bit avec des pinces alligators.