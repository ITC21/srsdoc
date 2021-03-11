# STEAMEATE

# Tabla de contenido

- [Introducción](#Introducción)
  - [Propósito](#Propósito)
  - [Alcance](#Alcance)
  - [Definiciones y Acrónimos](#Definicios-y-Acrónimos)
- [Descripción General](#Descripción-general)
  - [Clases de usuarios](#Clases-de-usuarios)
  - [Asumciones y Dependencias](#Asumciones-y-Dependencias)
- [Características del Sistema y Requerimientos](#Características-y-requerimientos)
  - [Requerimientos funcionales](#Requerimientos-funcionales)
  - [Requerimientos de la Interface externa](#Requerimientos-de-Interface-externo)
  - [Requerimientos no funcionales](#Requerimientos-no-funcionales)
- [Screens](#screens)
  - [Wireframes](#wireframes)
- [Referencias](#Referencias)

_Tabla de contenido generada usando el plugin Markdown de VSCode: [Markdown TOC](https://marketplace.visualstudio.com/items?itemName=AlanWalk.markdown-toc)_

# Introducción

STEAM Es una asociación sin fines de lucro que está liderando un movimiento regional que impulsa la Educación y el talento STEAM, los emplos del futuro y la innovación, con visión social e incluyente.

Desarrollaremos un aplicación web que dentro tenga un videojuego de plataforma para que las personas entre 18-19 años puedan tomar una decisión más informada sobre que carreras STEAM hay y porque deberían elegir una.

## Propósito

Nuestro propósito es quitar el miedo y los esterotipos que conlleva estudiar una carrera STEAM. Queremos que los estudiantes tomen una decisión informada respecto a su futuro con ayuda del videojuego que desarrollaremos.

## Alcance

Desarrollaremos una applicación web que dentro contenga un videojuego. La applicación web se implementará con JavaScript, HTML y CSS la cual tiene el objetivo de ser visualizada en cualquier dispositivo electrónico. Utilizaremos la plataforma de desarrollo <em>Unity</em> junto con el lenguaje C# para hacer el videojuego. Por último utilizaremos MySQL para ir recabando los medidores STEAM solicitados por la OSF.

<strong>Beneficios: </strong>

<ul>
<li>Personas entre 18 y 19 años (alumnos de preparotoria) podrán conocer las carreras STEAM (carreras del futuro)</li>
<li>Mediante el videojuego, conocerán caracteristicas sobre alguna carrera de su interés y podrán eliminar ciertos estereotipos ligados a esta.</li>
<li>STEAM podrá conocer los intereses de las personas con las que trabaje, con estos datos podrá tomar mejor decisiones sobre como ayudarlos.</li>
<li>Incluir a más mujeres en carreras como alguna de las ingenierías ya que actualmente no hay un porcentaje equilibrado entre los estudiantes</li>
</ul>

## Definiciones y Acrónimos

<ul>
<li>STEAM: Science Technology Engineering Arts and Mathematics</li>
<li>JavaScript: Es un lenguaje de programación o de secuencias de comandos que te permite implementar funciones complejas en páginas web [1]</li>
<li>HTML: Es un lenguaje de marcado que se utiliza para el desarrollo de páginas de Internet. Se trata de la siglas que corresponden a HyperText Markup Language, es decir, Lenguaje de Marcas de Hipertexto [2]</li>
<li>CSS: Es el lenguaje de estilos utilizado para describir la presentación de documentos HTML o XML [3]</li>
<li>C#: Es un lenguaje de programación desarrollado por Microsoft, orientado a objetos, que ha sido diseñado para compilar diversas aplicaciones que se ejecutan en .NET Framework. Se trata de un lenguaje simple, eficaz y con seguridad de tipos [4] </li>
<li>MySQL: Es un sistema de gestión de bases de datos relacionales de código abierto (RDBMS, por sus siglas en inglés) con un modelo cliente-servidor. [5] </li>
</ul>

# Descripción General

Nuestra applicación web será una adición a la página existente de STEAM. El videojuego lo realizaremos desde cero tomando inspiraciones de otras piezas.

## Clases de usuarios

<ul>
<li>Usuario: Cualquier persona que accese a la página web y pruebe el videojuego </li>
<li>Administrador: Este usuario tiene el control sobre los usuarios que hay, además de poder ver los indicadores STEAM que recolecta el videojuego</li>
</ul>

## Asumciones y Dependencias


<ul>

<li>Usuarios: </li>

<ul>
<li>Realizar la implementación dentro de la página para que las personas puedan crear sus usuarios o inciar sesión</li>
<li>Encriptación de los datos personales de los usuarios para proteger contraseñas o mails</li>
<li>Realizar una interfaz para representar y visualizar los indicadores STEAM</li>
</ul>

</ul>

# Características del Sistema y Requerimientos


## Requerimientos funcionales

<h2>Página Web:</h2>
<ol>
<li>Registrar usuarios que no hayan entrado a la pagina anteriormente</li>
<li>Iniciar sesión para usuarios que haya entrado a la pagina</li>
<li>Desplegar información sobre la carrera de ITC y porque un alumno debería de considerar estudiarla</li>
<li>Mostrar en un apartado el videojuego</li>
<li>Conexión a una base de datos</li>
<li>Recolectar los indicadores STEAM</li>
<li>Realizar la visualización de Datos de los indicadores</li>
<li>Devolver indicadores a los usuarios que sean administradores</li>
</ol>

<h2>Videojuego: </h2>
<ol>
<li>Cargar y obtener la información de usuarios que hayan jugado anteriormente</li>
<li>Mostrar un menú donde se muestre el puntaje de jugadores con partidas previas</li>
<li>Explicar las mecánicas del juego al inicio</li>
<li>Mostrar elementos como el jugador, barra de vida, escenario, enemigos, puntaje actual u otros con los que el jugador pueda interactuar.</li>
<li>Desplegar un apartado donde aparezcan las hábilidades (bloques de código) con las que el jugador cuenta al momento de pausar el juego y mostrar una descripción breve de que es lo que hace cada habilidad</li>
<li>Desplegar información que sea relevante para el jugador ya que esta puede ser necesaria para alguna mecánica o progresar en la historia</li>
<li>Mostrar el puntaje de su partida</li>
<li>Detectar cuando el jugador perdió (Barra de vida vacía o fuera del área jugable)</li>
<li>Detectar cuando el jugador pasa de nivel y/o gana la partida</li>
</ol>

## Requerimientos de la Interface externa

There are several types of interfaces you may have requirements for, including:

- User
- Hardware
- Software
- Communications

## Requerimientos no funcionales


# Screens

Identifying the individual screens (for an app), or pages (for a website) are where a product’s shape starts to become clear. They are a distillation of the user stories into a set of distinct sections that satisfy the needs and behaviors identified so far. The process of outlining an application’s screens may also highlight any requirements or considerations that have been overlooked up to this point.

This has the dual purpose of both contributing to a more accurate vision of the product early on, and serving as a jumping-off point for the time when designers do get involved.

## Wireframes

Wireframes are simple page layouts that outline the size and placement of elements, and features on a page. They are generally devoid of color, font styles, logos or any design elements.

Wireframing is probably the most time-consuming step of this process and for some simple projects, it may be overkill. For complex projects where serious design thinking needs to happen, wireframes are an indispensable tool.

Here are some popular tools for wireframing:

- https://marvelapp.com/
- https://balsamiq.com/
- https://jetstrap.com/
- https://www.fluidui.com/
- https://ninjamock.com/
- https://www.justinmind.com/
- https://moqups.com/

# Referencias

<ol>
<li>https://developer.mozilla.org/es/docs/Learn/JavaScript/First_steps/Qu%C3%A9_es_JavaScript</li>
<li>https://codigofacilito.com/articulos/que-es-html    </li>
<li>https://developer.mozilla.org/es/docs/Web/CSS</li>
<li>https://openwebinars.net/blog/que-es-c-introduccion/</li>
<li>https://www.hostinger.mx/tutoriales/que-es-mysql/</li>
</ol>
