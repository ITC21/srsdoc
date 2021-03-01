# Code Jumpers

> Documeto del videojuego

# Tabla de Contenidos

- [Game Design](#game-design)
  - [Summary](#summary)
  - [Gameplay](#gameplay)
  - [Mindset](#mindset)
- [Technical](#technical)
  - [Screens](#screens)
  - [Controls](#controls)
  - [Mechanics](#mechanics)
- [Level Design](#level-design)
  - [Themes](#themes)
  - [Game Flow](#game-flow)
- [Development](#development)
  - [Abstract Classes / Components](#abstract-classes--components)
  - [Derived Classes / Component Compositions](#derived-classes--component-compositions)
- [Graphics](#graphics)
  - [Style Attributes](#style-attributes)
  - [Graphics Needed](#graphics-needed)
- [Sounds/Music](#soundsmusic)
  - [Style Attributes](#style-attributes-1)
  - [Sounds Needed](#sounds-needed)
  - [Music Needed](#music-needed)
- [Schedule](#schedule)

# Game Design

## Summary

Un platformer 2D en el cual los jugadores tendrán un acercamiento a la carrera de ITC el cuál tiene como objetivo motivarlos para que la escogan cuando entren a la Universidad.

## Gameplay

La manera en la que se juega el videojuego es mediante una terminal. Al inicio de cada nivel el jugador podrá visualizar todo el nivel que se encuentra por delante, el objetivo es que el jugador programe los movimientos del personaje para que este pueda pasar el nivel. El jugador pasara de nivel cuando logre llegar a la meta, pero se encontrará con obstáculos que tendrá que saltar y esquivar, así como enemigos que atacaran al personaje. Los controles que el jugador podrá acceder desde la terminal serán limitados a: caminar a la derecha, caminar a la izquierda, atacar, agacharse y saltar. El jugador tendrá que planear el camino de su personaje y programar sus movimientos para que pueda pasar de nivel.

## Mindset

What kind of mindset do you want to provoke in the player? Do you want them to feel powerful, or
weak? Adventurous, or nervous? Hurried, or calm? How do you intend to provoke those emotions?

Queremos que el jugador vaya recorriendo los niveles y sienta que cada vez va aprendiendo más y más conceptos relacionados con software. En cuanto al juego, mientras más progreso tenga, podrá acceder a más mecánicas lo que le dará una sensación de mayor poder. Nuestra intención es que se sienta atraído a los temas que se ven en la carrera y vea que puede resolver problemas estudiando esta ingeniería.

# Technical

## Screens

1. Title Screen
   a. Start
   b. Level Select
   c. Options
   d. Credits
   e. Quit
2. Level Select
   a. List of levels
   b. Back
3. Game
   a. Terminal
   a. Blocks of code
   b. Reset (Resets code blocks)
   c. Play/Pause button
   d. Indicator to current code block on execution
   c. Level overview
4. Game Over
   a. Game Over
   b. Cause of Death
   d. Restart
   e. Main Menu
5. Level Complete
   a. Level number
   b. Completion Time
   c. Number of deaths
   d. Next Level
   e. Main Menu
6. In Game Menu
   a. Options
   b. Main Menu
7. Options
   a. Volume level (slider)
   b. Terminal Theme

## Controls

How will the player interact with the game? Will they be able to choose the controls? What kind of
in-game events are they going to be able to trigger, and how? (e.g. pressing buttons, opening doors, etc.)

El personaje podrá ser controlado por bloques de código, estos serán escogidos por el jugador. Como mencionamos antes, los comandos serían caminar a la derecha, a la izquierda, agacharse, saltar y por último atacar (Repetir para loops, opcional); escogiendo estos con el mouse.

## Mechanics

Are there any interesting mechanics? If so, how are you going to accomplish them? Physics,
algorithms, etc.

- El jugador podrá defenderse de un enemigo especial que son los "bugs", estos afectan las acciones del personaje, atacándolos con bloques de código.

# Level Design

(Note : These sections can safely be skipped if they’re not relevant, or you’d rather go about it another way. For most games, at least one of them should be useful. But I’ll understand if you don’t want to use them. It’ll only hurt my feelings a little bit.)

## Themes

1. Cueva (Tutorial)

   > a. Ambiente
   >
   > > i. Oscuro, tensión

b. Objetosa
i. Ambiente

1. Torchas
2. Piedras
   ii. Interactivos
3. Primeros pasos
4. Primer enemigo

5. Bosque y Pueblo
   a. Ambiente
   i. Más peligroso que la cueva ya que hay más enemigos, más luz, más acción
   b. Objetos
   i. Ambiente 1. Arboles 2. Casas pequeñas
   ii. Interactivos 1. Nuevos bloques de código 2. Enemigos normales 3. Enemigos especiales

6. Ciudad
   a. Ambiente
   i. Vértigo, adrenalina, peligro, rápidez, muerte
   b. Objetos
   i. Ambiente 1. Edificios 2. Rascacielos 3.
   ii. Interactivos 1. Guards 2. Giant rats 3. Chests

7. Ciudad futurista
   a. Ambiente
   i. Blanco, edificios grandes, más dificultad
   b. Objetos
   i. Ambiente 1. Rodents 2. Torches 3. Suits of armor
   ii. Interactivos 1. Guards 2. Giant rats 3. Chests

_(example)_

## Game Flow

```
1.	Player starts in forest
2.	Pond to the left, must move right
3.	To the right is a hill, player jumps to traverse it (“jump” taught)
4.	Player encounters castle - door’s shut and locked
5.	There’s a window within jump height, and a rock on the ground
6.	Player picks up rock and throws at glass (“throw” taught)
7.	… etc.
```

(example)

# Development

## Abstract Classes / Components

```
1.	BasePhysics
    a.	BasePlayer
    b.	BaseEnemy
    c.	BaseObject
2.	BaseObstacle
3.	BaseInteractable
```

_(example)_

## Derived Classes / Component Compositions

```
1.	BasePlayer
    a.	PlayerMain
    b.	PlayerUnlockable
2.	BaseEnemy
    a.	EnemyWolf
    b.	EnemyGoblin
    c.	EnemyGuard (may drop key)
    d.	EnemyGiantRat
    e.	EnemyPrisoner
3.	BaseObject
    a.	ObjectRock (pick-up-able, throwable)
    b.	ObjectChest (pick-up-able, throwable, spits gold coins with key)
    c.	ObjectGoldCoin (cha-ching!)
    d.	ObjectKey (pick-up-able, throwable)
4.	BaseObstacle
    a.	ObstacleWindow (destroyed with rock)
    b.	ObstacleWall
    c.	ObstacleGate (watches to see if certain buttons are pressed)
5.	BaseInteractable
    a.	InteractableButton
```

_(example)_

# Graphics

## Style Attributes

What kinds of colors will you be using? Do you have a limited palette to work with? A post-processed HSV map/image? Consistency is key for immersion.

What kind of graphic style are you going for? Cartoony? Pixel-y? Cute? How, specifically? Solid, thick outlines with flat hues? Non-black outlines with limited tints/shades? Emphasize smooth curvatures over sharp angles? Describe a set of general rules depicting your style here.

    Well-designed feedback, both good (e.g. leveling up) and bad (e.g. being hit), are great for teaching the player how to play through trial and error, instead of scripting a lengthy tutorial. What kind of visual feedback are you going to use to let the player know they’re interacting with something? That they *can* interact with something?

## Graphics Needed

```
1.	Characters
    a.	Human-like
        i.	Goblin (idle, walking, throwing)
        ii.	Guard (idle, walking, stabbing)
        iii.	Prisoner (walking, running)
    b.	Other
        i.	Wolf (idle, walking, running)
        ii.	Giant Rat (idle, scurrying)
2.	Blocks
    a.	Dirt
    b.	Dirt/Grass
    c.	Stone Block
    d.	Stone Bricks
    e.	Tiled Floor
    f.	Weathered Stone Block
    g.	Weathered Stone Bricks
3.	Ambient
    a.	Tall Grass
    b.	Rodent (idle, scurrying)
    c.	Torch
    d.	Armored Suit
    e.	Chains (matching Weathered Stone Bricks)
    f.	Blood stains (matching Weathered Stone Bricks)
4.	Other
    a.	Chest
    b.	Door (matching Stone Bricks)
    c.	Gate
    d.	Button (matching Weathered Stone Bricks)
```

_(example)_

_(Note : If you’re soloing you might not need to define this part, as you can just use the Derived_
_Classes + Themes section as a reference. It’s up to you.)_

# Sounds/Music

## Style Attributes

Again, consistency is key. Define that consistency here. What kind of instruments do you want to use in your music? Any particular tempo, key? Influences, genre? Mood?

Stylistically, what kind of sound effects are you looking for? Do you want to exaggerate actions with lengthy, cartoony sounds (e.g. mario’s jump), or use just enough to let the player know something happened (e.g. mega man’s landing)? Going for realism? You can use the music style as a bit of a reference too.
Remember, auditory feedback should stand out from the music and other sound effects so the player hears it well. Volume, panning, and frequency/pitch are all important aspects to consider in both music and sounds - so plan accordingly!

## Sounds Needed

```
1.	Effects
    a.	Soft Footsteps (dirt floor)
    b.	Sharper Footsteps (stone floor)
    c.	Soft Landing (low vertical velocity)
    d.	Hard Landing (high vertical velocity)
    e.	Glass Breaking
    f.	Chest Opening
    g.	Door Opening
2.	Feedback
    a.	Relieved “Ahhhh!” (health)
    b.	Shocked “Ooomph!” (attacked)
    c.	Happy chime (extra life)
    d.	Sad chime (died)
```

_(example)_

## Music Needed

```
1.	Slow-paced, nerve-racking “forest” track
2.	Exciting “castle” track
3.	Creepy, slow “dungeon” track
4.	Happy ending credits track
5.	Rick Astley’s hit #1 single “Never Gonna Give You Up”
```

_(example)_

_(Note : Again, if you’re soloing you might be able to / want to skip this section. It’s up to you.)_

# Schedule

(what is a schedule, i don’t even. list is good enough, right? if not add some dates i guess)

```
1.	develop base classes
    a.	base entity
        i.	base player
        ii.	base enemy
        iii.	base block
    b.	base app state
        i.	game world
        ii.	menu world
2.	develop player and basic block classes
    a.	physics / collisions
3.	find some smooth controls/physics
4.	develop other derived classes
    a.	blocks
        i.	moving
        ii.	falling
        iii. breaking
        iv.	cloud
    b.	enemies
        i. soldier
        ii.	rat
        iii. etc.
5.	design levels
a.	introduce motion/jumping
b.	introduce throwing
c.	mind the pacing, let the player play between lessons
6.	design sounds
7.	design music
```

_(example)_
