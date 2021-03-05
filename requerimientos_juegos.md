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

1. Principales
    a. Caminar a la derecha
    b. Caminar a la izquierda
    c. Saltar
    d. Agacharse
    e. Atacar

2. Secundarias
    a. Saltar y atacar
    b. Moverse y atacar
    c. Esperar
    d. Agacharse y atacar
    e. Saltar y moverse
    f. Agacharse y moverse

3. Enemigos
    a. Moverse a la derecha
    b. Moverse a la izquierda
    c. Moverse arriba
    d. Moverse abajo
    e. Atacar
    f. Saltar

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
   i. Ambiente 1. Edificios 2. Rascacielos 3. Calles
   ii. Interactivos 1. Nuevos bloques de código 2. Nuevos enemigos 3. Enemigos especiales 4. Terminal

7. Ciudad futurista
   a. Ambiente
   i. Moderno, estético, futuristico, TRON
   b. Objetos
  ii. Interactivos 1. Nuevos bloques de código 2. Nuevos enemigos 3. Enemigos especiales 4. Jefe Final

_(example)_

## Game Flow

1. El jugador comienza en una cueva (tutorial).
2. Tendrá que mover a su personaja a la derecha para poder salir de la cueva y progresar.
3. El jugador solo tendra acceso a dos comandos en el inicio del juego, caminar a la derecha y saltar. 
4. Para pasar de nivel el jugador devera interactuar con una terminal que le dara acceso al siguiente nivel. 
4. Conforme el jugador pase los niveles encontraraá nuevos comandos que le permitiran hacer nuevas acciones, como atacar, agacharse y moverse a la izquierda.
5. En niveles mas avanzados se ecnotrara con enemigos que trataran de impedir su paso, el jugador devera esquivarlos o atacarlos. 
6. Cuanco el jugador pase los niveles suficientes y se sienta comodo con los controles del juego se enfrentara con el enemigo final.
7. Despues de ganar el enfrentamiento contra el emnemigo final, el jugador habra completado el juego. 

# Development


## Abstract Classes / Components

```
1.	Personajes 
    a.	Jugador
    b.	Enemigos normales
    c.  Jefe Final
2.	Objetos
    a.  Bloques de códigos
    b.  Plataformas 
    c.  Obstáculos

## Derived Classes / Component Compositions

```
1.	Jugador
    a.  Costumización del personaje
2.	EnemigosNormales
    a.	EnemigoVolador1
    b.  EnemigoVolador2
    c.  EnemigoTerrestre1
    d.  EnemigoTerrestre2
3.  Jefe Final
    a.  EnemigoFinal
4.	Objetos
    a.	Bloques de códigos (agarrable, usable)
    b.	Plataformas (estaticas)
    c.	Obstáculos (barrera)

```

_(example)_

# Graphics

## Style Attributes

Empezando en la cueva, utilizaremos una paleta de colores limitada, queremos un ambiente oscuro. Mientras el jugador progresa por los niveles, utilizaremos colores más vivos como rojo, azúl y verde, y para el último nivel, queremos dar un ambiente más futurista, entonces utilizaremos una paleta con efecto neón para que el jugador tenga una experiencia más inmersiva. 

El estilo del arte será retro, de 64 bits ya que nos estamos inspirando en clásicos como Super Mario 64 o Sonic The Hedgehog.  


## Graphics Needed

```
Todo el arte es de tipo Pixel Art

1.	Characters
    a.	Tipo Humano
        i.	Jugador principal (idle, caminando, saltando y atacando)
        ii.	Enemigo Final (idle, caminando, saltando y atacando)
    b.	Otros
        i.	EnemigoVoldaor estilo bug (idle, volando)
        ii.	EnemigoTerrestre estilo big (idle, caminando)
2.	Bloques
    a.	Piedra
    b.	Ladrillos
    c.	Pasto
    d.	Metal
    e.	Calles
3.	Ambiente
    a.	Cueva
    b.	Bosque
    c.	Ciudad
    d.	Ciudad destruida
    e.	Ciudad futuristica
4.	Otros
    a.	Terminal con la que pasa el nivel el jugador
    b.	Terminal en la que programa el jugador
    c.	Cambiar los colores del personaje
```


# Sounds/Music

## Style Attributes


Queremos que la vibra del juego sea como si fuera un clásico, como si estuvieras jugando un juego que se hizo hace 30 años. Tendremos piezas para cada momento, si el jugador esta en medio de la acción pondremos efectos y música que hagan sinergia con lo que esta pasando. Si el jugador consigue una victoria, habrá música que lo relaje y lo haga sentir orgulloso y satisfecho de su progreso. 

Again, consistency is key. Define that consistency here. What kind of instruments do you want to use in your music? Any particular tempo, key? Influences, genre? Mood?

## Sounds Needed

```
1.	Effects
    a.	Pisadas del jugador
    b.	Sonido de salto
    c.	Sonido de caida
    d.	Sondio de attaque
    e.	Sonido de enemigo moviendose
2.	Feedback
    a.	Sonido de toma de daño
    b.	Sonido de muerte
    c.	Sonido de derrota
    d.	Sonido de victoria
    e.  Sonido de enemigo tomando daño 
    f.  Sonido de enemigo muriendo
```

_(example)_

## Music Needed

```
1.	Musica de 8bit
2.	Musica de victoria
3.	Musica de derrota
4.	Musica de batalla final
```

# Schedule

```
1.	Desarrollar el nivel principal
    a.	Animaciones
        i.	 Hacer que el personaje salte
        ii.	 Hacer que el personaje se mueva
        iii. Hacer que el personaje ataque
    b.	Nivel
        i.	Hacer los bloques en los que salta el personaje
        ii.	Hacer el ambiente del primer nivel
    
2.	Desarrollar bloques de comando
    a.	Implementar los bloques con el que el jugador controlará al personaje
    b.  Implementar un canvas en el que el jugador podra utilizar los bloques

3.	Desarrollo de enemigos
    a.  Animaciones
        i.   Hacer que el enemigo se mueva dependiendo de su clase
        ii.  Hacer que el enemigo ataque
    
4.	Desarrollar al enemigo final
    a.	Animaciones
        i. Hacer que el enemigo final se mueva solo
        ii. Hacer que el enemigo final ataque 
        iii. Hacer la animación cuando un enemigo es derrotado
    
    b. Batalla
        i. Hacer el diseño de la batalla final

5.	Diseñar niveles
6.  Diseñar sonidos
7.	Diseñar musica
```

