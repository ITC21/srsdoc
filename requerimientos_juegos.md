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
   * Start
   * Level Select
   * Options
   * Credits
![Menu](/img/Menu.png)
2. Level Select
   * List of levels
   * Back
3. Game
   * Terminal
   * Blocks of code
   * Reset (Resets code blocks)
   * Play/Pause button
   * Indicator to current code block on execution
   * Level overview
![Primer Nivel C](/img/nivel1_cueva.jpg)
![Segundo Nivel C](/img/nivel2_cueva.jpg)
![Primer Nivel B](/img/nivel1_bosque.jpg)
![Juego](/img/Primer_nivel.png)
4. Game Over
   * Game Over
   * Cause of Death
   * Restart
   * Main Menu
5. Level Complete
   * Level number
   * Completion Time
   * Number of deaths
   * Next Level
   * Main Menu
6. In Game Menu
   * Options
   * Main Menu
7. Options
   * Volume level (slider)
   * Terminal Theme

## Controls

How will the player interact with the game? Will they be able to choose the controls? What kind of
in-game events are they going to be able to trigger, and how? (e.g. pressing buttons, opening doors, etc.)

El personaje podrá ser controlado por bloques de código, estos serán escogidos por el jugador. Como mencionamos antes, los comandos serían caminar a la derecha, a la izquierda, agacharse, saltar y por último atacar (Repetir para loops, opcional); escogiendo estos con el mouse.

## Mechanics

Are there any interesting mechanics? If so, how are you going to accomplish them? Physics,
algorithms, etc.


1. Principales
    * Derecha: caminar a la derecha.
    * Izquierda: caminar a la izquierda.
    * Saltar: salta moviendose a la derecha.
    * Agacharse: mientras se mueve se agacha.
    * Atacar: atacar a un enemigo.

2. Secundarias (Combinación de bloques para mejorar las mecanicas principales)
    * Saltar y atacar: atacar en el aire.
    * Moverse y atacar: atacar mientras caminas.
    * Esperar: esperar unos segundo en un lugar.
    * Agacharse y atacar: atacar mientras de deslizas.
    * Saltar y moverse: saltar mientras te mueves.
    * Agacharse y moverse: deslizarse hacia una dirección.

3. Enemigos
    * Moverse a la derecha
    * Moverse a la izquierda
    * Moverse arriba
    * Moverse abajo
    * Atacar
    * Saltar

4. Trampas
    * picos salientes
    * agujeros

# Level Design

(Note : These sections can safely be skipped if they’re not relevant, or you’d rather go about it another way. For most games, at least one of them should be useful. But I’ll understand if you don’t want to use them. It’ll only hurt my feelings a little bit.)

## Themes

1. Cueva (Tutorial)
    * Ambiente
        * Oscuro
        * tensión
    * Objetos
        * Antorchas
        * Piedras
   * Interactivos
        * Primeros pasos
        * Primer enemigo
        

2. Bosque y Pueblo
    * Ambiente
        * Más peligroso que la cueva, ya que hay más enemigos, más luz y más acción.
    * Objetos
        * Arboles 
        * Casas pequeñas
    * Interactivos 
        * Nuevos bloques de código 
        * Enemigos normales 
        * Enemigos especiales

3. Ciudad
    * Ambiente
        * Vértigo
        * adrenalina
        * peligro
        * rápidez
        * muerte
    * Objetos
        * Edificios 
        * Rascacielos 
        * Calles
    * Interactivos 
        * Combinación de bloques de codigo
        * Nuevos enemigos 
        * Enemigos especiales 

4. Ciudad futurista
    * Ambiente
        * Moderno
        * Estético
        * futuristico
        * TRON
    * Objetos
        * Edificios altos.
        * naves espaciales.
    * Interactivos 
        * Jefe Final

## Game Flow

1. El jugador comienza en una cueva (tutorial).
2. Tendrá que mover a su personaja a la derecha para poder salir de la cueva y progresar.
3. El jugador solo tendra acceso a dos comandos en el inicio del juego, caminar a la derecha y saltar. 
4. Para pasar de nivel el jugador devera interactuar con una terminal que le dara acceso al siguiente nivel. 
5. Conforme el jugador pase los niveles encontrará nuevos comandos que le permitiran hacer nuevas acciones, como atacar, agacharse y moverse a la izquierda.
6. En niveles mas avanzados se ecnotrara con enemigos que trataran de impedir su paso, el jugador devera esquivarlos o atacarlos. 
7. Cuando el jugador pase los niveles suficientes y se sienta comodo con los controles del juego se enfrentara con el enemigo final.
8. Despues de ganar el enfrentamiento contra el emnemigo final, el jugador habra completado el juego. 

# Development

## Abstract Classes / Components

1.	Personajes 
    * Jugador
        * PlayerMovement
    * Enemigos
2.	Objetos
    * Bloques de códigos
        * DragDrop
        * CodeSlot
        * command executed  
    * Obstáculos
3. Pantallas
    * SceneLoader
## Derived Classes / Component Compositions


1.	Jugador
    * Costumización del personaje
2.	EnemigosNormales
    * EnemigoVolador1
    * EnemigoVolador2
    * EnemigoTerrestre1
    * EnemigoTerrestre2
3.  Jefe Final
    * EnemigoFinal
4.	Objetos
    * Bloques de códigos (agarrable, usable)
    * Plataformas (estaticas)
    * Obstáculos (barrera)


# Graphics

## Style Attributes

Empezando en la cueva, utilizaremos una paleta de colores limitada, queremos un ambiente oscuro. Mientras el jugador progresa por los niveles, utilizaremos colores más vivos como rojo, azúl y verde, y para el último nivel, queremos dar un ambiente más futurista, entonces utilizaremos una paleta con efecto neón para que el jugador tenga una experiencia más inmersiva. 

El estilo del arte será retro, de 64 bits ya que nos estamos inspirando en clásicos como Super Mario 64 o Sonic The Hedgehog.  


## Graphics Needed


Todo el arte es de tipo Pixel Art

1.	Characters
    * Tipo Humano
        * Jugador principal (idle, caminando, saltando y atacando)
        * Enemigo Final (idle, caminando, saltando y atacando)
    * Otros
        * EnemigoVoldaor estilo bug (idle, volando)
        * EnemigoTerrestre estilo big (idle, caminando)
2.	Bloques
    * Piedra
    * Ladrillos
    * Pasto
    * Metal
    * Calles
3.	Ambiente
    * Cueva
    * Bosque
    * Ciudad
    * Ciudad destruida
    * Ciudad futuristica
4.	Otros
    * Terminal con la que pasa el nivel el jugador
    * Terminal en la que programa el jugador
    * Cambiar los colores del personaje

# Sounds/Music

## Style Attributes

Queremos que la vibra del juego sea como si fuera un clásico, como si estuvieras jugando un juego que se hizo hace 30 años. Tendremos piezas para cada momento, si el jugador esta en medio de la acción pondremos efectos y música que hagan sinergia con lo que esta pasando. Si el jugador consigue una victoria, habrá música que lo relaje y lo haga sentir orgulloso y satisfecho de su progreso. 

Again, consistency is key. Define that consistency here. What kind of instruments do you want to use in your music? Any particular tempo, key? Influences, genre? Mood?

## Sounds Needed


1.	Effects
    * Pisadas del jugador
    * Sonido de salto
    * Sonido de caida
    * Sondio de attaque
    * Sonido de enemigo moviendose
2.	Feedback
    * Sonido de toma de daño
    * Sonido de muerte
    * Sonido de derrota
    * Sonido de victoria
    * Sonido de enemigo tomando daño 
    * Sonido de enemigo muriendo

## Music Needed

1.	Musica de 8bit
2.	Musica de victoria
3.	Musica de derrota
4.	Musica de batalla final


# Schedule

1.	Desarrollar el nivel principal
    * Animaciones
        * Hacer que el personaje salte
        * Hacer que el personaje se mueva
        * Hacer que el personaje ataque
    * Nivel
        * Hacer los bloques en los que salta el personaje
        * Hacer el ambiente del primer nivel
    
2.	Desarrollar bloques de comando
    * Implementar los bloques con el que el jugador controlará al personaje
    * Implementar un canvas en el que el jugador podra utilizar los bloques

3.	Desarrollo de enemigos
    * Animaciones
        * Hacer que el enemigo se mueva dependiendo de su clase
        * Hacer que el enemigo ataque
    
4.	Desarrollar al enemigo final
    * Animaciones
        * Hacer que el enemigo final se mueva solo
        * Hacer que el enemigo final ataque 
        * Hacer la animación cuando un enemigo es derrotado
    
    * Batalla
        * Hacer el diseño de la batalla final

5.	Diseñar niveles
6.  Diseñar sonidos
7.	Diseñar musica


