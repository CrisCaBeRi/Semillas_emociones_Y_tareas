# Documentación Página web Fundación Semillas 

> <img src="https://user-images.githubusercontent.com/108433878/199076739-3d45b99a-fc46-4fb9-87a9-26e80780e708.png" alt="drawing" width="200" />

Desarrollado por: **Kevin Steven Arias Arias Duarte, Cristian Camilo Betancourt Rincon, Jonathan David Sánchez**  

Página realizada con HTML y Css utilizando el IDE Visual Studio Code.

* La Fundación Semillas, que ofrece diplomados en sostenibilidad del medio ambiente, desea saber el estado de ánimo sus alumnos, además de querer suministrarles una herramienta de fácil manejo, donde puedan organizar las tareas diarias propuestas por la institución.

* Para ello, plantea que se desarrolle una aplicación web con varios dashboard, que muestren indicadores sobre las emociones que un alumno puede llegar a sentir durante el desarrollo de la formación por cada actividad que realizan.


*Para el desarrollo se utilizo el principio del mobile first, partiendo de una vista inicial de 320 px hasta 424 px para vista móvil. De 425 a 768 px para vista tablet y de 768 a full 4k 2560 px para desktop.*

### Extensiones utilizadas: 
* Live server
* Html format
* Html preview
* Htmls Snippets
* Html CSS Support.


## Estructura principal: 
```bash
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="./styles/styles.css">
    <link rel="shortcut icon" href="./assets/logoSGreen.png" type="image/x-icon">    
    <title>Fundación Semillas</title>
</head>
 ```
> ## *Nota*
> * Se define la etiqueta Lang = es para mejorar los servicios de automatización y para que se reconozca el lenguaje utilizado. 
> * Se integran las etiquetas de compatibilidad preestablecidas del navegador X UA compatible. 
> * Le linkea el documento con la pagina de css que va a alterar directamente el contenido. <link reel= “stylesheet”>
> * Se genera el titulo que se va a mostrar en la pestaña con <title>
> * Se adjunta el icono que se muestra en la pestaña con <link reel =”icon” 

  **Vista de la pestaña y el logo de la fundación** 
 > *![image](https://user-images.githubusercontent.com/108433878/199104384-17f4ee89-5e9f-4d8b-96c2-cf548bbb1573.png)

## Header: 
```bash
<header>        
        <nav class="hamburguesa">
            <div class="nav_container">
                <div class="imagen_header">
                    <img src="./assets/logoSWhite_1.svg" alt="Logo empresa" width="20%">
                </div>
                <label for="menu" class="nav_label">
                    <hr>
                    <hr>
                    <hr>                    
                </label>
                <input type="checkbox" name="" id="menu" class="nav_input">
                <div class="nav_menu">
                    <a href="" class="nav_item">Administrador </a>
                    <a href="" class="nav_item">Formador</a>
                    <a href="" class="nav_item">Alumno</a>                    
                </div>
            </div>
        </nav>
    </header>
 ```
> ## *Nota*
> * Se crea la clase hamburguesa que cumple las funciones de menú desplegable y alberga la imagen del logo. 
> * Se genera un contenedro con hr que cumplira las funciones del botón de menú o hamburguesa.  
> * Se crea un input type que funcionara con acciones (checked) para desplegar el menú. 
> * Se crea el contenedor nav_menu que posee las etiquetas <a> encargadas de cumplir la función de hipervínculos. 

## CSS header 

```bash
.menu2 {
  display: none;}

.nav_container {
  display: flex;
  align-items: center;
  justify-content: space-between;}

.nav_item {
  color: white;
  text-decoration: none;}

.nav_label {
  width: 9vh;
  display: block;
  cursor: pointer;}

.nav_label hr {
  border-radius: 5px;
  padding-bottom: 3px;
  background-color: white;
  border-color: white;
  margin-bottom: 7px;}

.nav_menu {
  z-index: 1;
  position: fixed;
  top: 80px;
  bottom: 0px;
  background-color: #009458;
  width: 100%;
  left: 0;
  display: flex;
  justify-content: space-evenly;
  flex-direction: column;
  align-items: center;
  clip-path: circle(0 at center);
  transition: 1s;
  font-family: 'Dosis', sans-serif;
  font-size: 25px;}

.nav_input {
  display: none;}

.nav_input:checked+.nav_menu {
  clip-path: circle(100% at center);}

.hamburguesa {
  padding: 10px 10px 10px 40px;
  width: 100%;
  background-color: #009458;
  display: flex;
  justify-content: space-between;}
 ```
> ## *Nota*
> * Se selecciona la clase .menu2 (que es el menú utlizado en la version desktop y tablet) y se oculta por medio de un display none.
> * Se selecciona la clase .nav_container, nav_label hr y nav_item. Luego, se utiliza flexbox para darle ubicación a los elementos que contiene la clase padre. Adicionalmente, se le dan las características especifícas de forma a los hr encargados de ser el menú desplegable de hambruguesa.   
> * Para la clase nav_menu se generan los estilos y ubicaciones correspondientes mediante flexbox y la propiedad de background color. Se utiliza l propiedad z-index para darle una ubicación principal cuando el menú de hamburguesa se despliegue.Por otra parte, la propiedad clip-path se utiliza para generar la animación de despliegue del menú. 
> * La clase .nav_input se oculta ya que solo interesa la funcionalidad de input checkbox. Luego, seleccionando su acción de :checked se utiliza clip path para disparar la animación del circulo desplegable cuando se active el checkbox.
> *  Para la clase .hamburguesa, se genera una ubicación mediante el padding para alejar el contenido de los bordes y se genera un ancho del 100% para que el contenido no se altere.

## menu2: 
```bash
    <div class="menu2">       
        <div class="imagen_headermenu">
            <img src="./assets/logoSWhite_1.svg" alt="Logo empresa" width="">
        </div>            
        
        <div class="botones"> 
            <button>Administradores</button>
            <button>Formadores</button>
            <button>Alumnos</button>
        </div>
    </div>
 ```
> ## *Nota*
> * Se crea la clase menu2 que alberga el menu correspondiente a la vista desktop (solo visible en resolución 504 +).
> * Posee los mismos elementos de imagen que el menú de hamburguesa. 
> * Se crea la clase botones que agrega los tres botones correspondientes al menú desplegable, esta vez, funcionaran como un menú norman (sin vista desplegable).  


## CSS menu2

```bash
@media (min-width: 425px) {

  /* Sección Header */
  header {
    display: none;}

  .menu2 {
    display: flex;
    height: 80px;
    background-color: #009458;
    padding: 10px;}

  .imagen_headermenu {
    display: flex;
    padding-left: 20px;
    padding-right: 10px;}


  .botones {
    width: 100%;
    display: flex;
    align-items: center;
    margin-left: 25px;
    margin-right: 50px;}

  .botones button {
    color: #009458;
    font-size: 80%;
    padding: 5px;}

  .menu2 button {
    border-radius: 35px;
    height: 70%;
    margin-right: 15px;}

  button:nth-child(2),
  button:nth-child(3) {
    width: 28%;}

  button:nth-child(3) {
    margin-right: 25px;}

  .botones button:first-of-type {
    width: 38%;}
 ```
> ## *Nota*
> * Se oculta el menú de hamburguesa en el header mediante display: none. 
> * Se empieza a trabajar en el media query de tablet para menu2 que se muestra mediante el display flex ya que se encontraba oculto y se le dan las propiedades de color y espcio mediante background-color y padding. 
> * Se altera la posicion de la imagen de logo mediante padding rigut y left en la clase .imagen_headermenu. 
> * A la clase .botones que algerga las etiquetas button se le indican un contenido total del 100% y un margin izquierdo de 25 y derecho de 50 para lograr la ubicación espacial deseada. 
> * A las clase .menu2 en su etiqueta button se le indica un alto total de 70% mediante heigth y se redondean los bordes de los botones con border radius.  
> * Para las propuedades de boton adicionales en nth (2 y 3) se les genera un width específico para que ocupen sus dimensiones exactas.


## person: 
```bash
         <section class="container">
            <div class="person">
                <div class="container_ficha">
                    <img src="./assets/fotoperfil.PNG" alt="" class="imagen_persona" width="65%">      
                    <div class="nombre_persona">
                        <h2>Jackie-chan</h2>
                    </div>                
                </div> 
                <h4>Información del estudiante</h4>
                <div class="informacion_estudiante"> 
                    <h2>Información del estudiante</h2>                         
                    <div class="info_izq">                
                        <p>Jackie Orlando Chan Zapata</p>
                        <h4>Nombre</h4>
                        <p>27</p>
                        <h4>Edad</h4>
                        <p>China</p>
                        <h4>Nacionalidad</h4>
                        <p>1.015.462.428</p>
                        <h4>Identificación</h4>
                    </div>
                    <div class="info_der">
                            <p>Calle 22 # 33-45</p>
                            <h4>Dirección de residencia</h4>
                            <p>chanshei@semillas.co</p>
                            <h4>Correo electrónico</h4>
                            <p>3123678965</p>
                            <h4>Número de contacto</h4>
                            <div class="img_logosc">
                                <img src="./assets/whatsapp.svg">
                                <img src="./assets/gmail.svg" alt="" >
                                <img src="./assets/zoom.svg" alt="" > 
                            </div>
                    </div> 
                </div>
 ```
> ## *Nota*
> * La sección general "container" se trae desde el documento original. Se empieza a trabajar con la clase person, que albergará todo el contenido correspondiente a la ficha de información del estudiante. 
> * Se crea la clase container_ficha dentro de person. Esta etiqueta posee el contenido de imagen correspondeinte a la foto de perfil. Luego, se encuentra la clase nombre_persona que posee el h2 correspondiente al nombre del estudiante.
> * Fuera de los divs, se encuentra una etiqueta h4 que funciona como subtitulo correspondiente "Información del estudiante", se maneja duplicado dentro de la siguiente clase de informacion_estudiante ya que se necesita posicionar de forma diferente en las vistas de tablet y desktop. 
> * Se crea la clase padre informacion_estudiante que alberga dos contenedores de info_izq e info_der para posicionar los elementos uno al lado del otro en la hoja de estilos, dentro de ellas se crean las etiquetas p y h4 para información y subtitulos. En la clase img_logosc se alamcenana las imagenes de redes sociales. 


## CSS person

```bash
.person {
  margin: 0 2% 0 2%;
  padding: 15px;
  background-color: #d9efe6;
  border-radius: 15px;
  box-shadow: 0px 2px 2px 0px grey;}

.container_ficha {
  display: flex;
  flex-direction: column;
  align-items: center;}

.imagen_persona {
  clip-path: polygon(20% 0%, 80% 0%, 100% 50%, 80% 100%, 20% 100%, 0% 50%);
  margin-bottom: 20px;}

.nombre_persona {
  background-color: #009458;
  border-radius: 15px;
  padding: 0 20px 0 20px;
  text-align: center;
  margin-bottom: 20px;
  color: white;}

.person {
  font-family: 'Dosis', sans-serif;
  font-weight: 200;
  font-size: 16px;}

.nombre_persona h2 {
  font-family: 'Dosis', sans-serif;
  font-weight: 200;}

.informacion_estudiante {
  display: grid;
  grid-template-columns: 55% 45%;
  padding: 5px;
  gap: 5px;
  word-wrap: break-word;}

.info_der {
  padding-top: 20px;}

.informacion_estudiante h3 {
  font-size: 16px;
  margin-bottom: 15px;}

.informacion_estudiante h4 {
  font-size: 14px;
  margin-bottom: 10px;}

.informacion_estudiante p {
  font-size: 15px;}
 ```
 
> ## *Nota*
> * Para la clase .person se crean las pripiedades de margin para limitar el crecimiento del contenedor antes del borde y un padding para alejar el contenido de los bordes. Adicionalmente, se genera un background suave para diferenciar el espacio de la tarjeta, se leda un borde redonadeado con border radius y unas sobras de caja para contrastar con el fondo.
> * La clase .container ficha se crea para posicionar en columna el contenido, por ende se utiliza la propiedad display flex y flex direction column. 
> * La clase .imagen persona utiliza la propiedad de clip path para generar un poligono con la imagen del estudiante. 
> * .nombre_persona utiliza las propiedades de background color para contrastar en verde con el fondo, un borde redondeado de 15px y un espaciado de padding. 
> * Para .person .nombre_persona y la clase .información de estudiante, se utilizan las propiedades de fuente para letra y el tamaño. 
> * En informacion_estudiante se crean dos espacios utilizando grid en donde se ubica la informacion del estudiante contenida en info_Der e info_izq. 

## faces: 
```bash
          <div class="faces">            
                    <div class="face1">
                        <div id="cara">
                            <div class="ojos">
                                <div class="ojo_i">                       
                                </div>
                                <div class="ojo_d">
                                </div>
                            </div>
                            <div class="boca"></div>                
                        </div>
                        <h2>60%</h2>
                        <p>Aprobación</p>
                    </div>
                    <hr>
                    <div class="face2">
                        <div id="cara">
                            <div class="ojos">
                                <div class="ojo_i">                 
                                </div>
                                <div class="ojo_d">
                                </div>
                            </div>
                            <div class="boca"></div>
                        </div>
                        <h2>20%</h2>
                        <p>Pasivo</p>    
                    </div>
                    <hr>
                    <div class="face3">
                        <div id="cara">
                            <div class="ojos">
                                <div class="ojo_i">                            
                                </div>
                                <div class="ojo_d">
                                </div>
                            </div>
                            <div class="boca"></div>
                        </div>
                        <h2>20%</h2>
                        <p>Detractor</p>
                    </div>
 ```
> ## *Nota*
> * Se crea la clase padre de faces que alberga tres container diferentes. Cada uno representa un cara (aprobacion, Pasivo y detractor).
> * Cada container posee un container específico para cada parte de la cara sea el ovalo de la cabeza, ojo izquierdo, derecho y boca, esto con el fin de moldear las partes den css para generar una cara feliz, una de conforme y otra de desaprobación.





## CSS faces

```bash
.faces {
  width: 100%;
  height: 180px;
  border-radius: 15px;
  box-shadow: 0px 2px 2px 0px grey;
  display: flex;
  justify-content: space-around;
  background-color: white;}

.face1,
.face2,
.face3 {
  padding-top: 30px;
  display: flex;
  flex-direction: column;
  align-items: center;}

.face1 {
  padding-left: 10px;}

.face3 {
  padding-right: 10px;}

.face2 {
  padding-left: 15px;
  padding-right: 15px;}

#cara {
  width: 50px;
  height: 50px;
  border-radius: 50%;
  border: solid 4px #009458;
  margin-bottom: 10px;}

.face1,
.face2,
.face3 {
  transform: scale(var(--escala, 1));
  transition: transform 0.25s;}

.face1:hover,
.face2:hover,
.face3:hover {
  --escala: 1.1;
  cursor: pointer;}

.faces hr {
  margin-top: 10px;
  margin-bottom: 10px;
  border: 1px solid grey;}

.ojos {
  display: flex;
  align-items: center;
  justify-content: space-around;}

.ojo_i {
  margin-top: 8px;
  margin-left: 3px;
  width: 10px;
  height: 10px;
  border-radius: 50%;
  background-color: #009458;}

.ojo_d {
  margin-top: 8px;
  margin-right: 3px;  
  width: 10px;
  height: 10px;
  border-radius: 50%;
  background-color: #009458;}

.boca {
  transform: translate(50%, 100%);
  height: 10px;
  width: 20px;
  border-radius: 0 0 150px 150px;
  background-color: #009458;}

.face1 h2 {
  color: #009458;}

.face2 #cara {
  border: solid 4px #fab005;}

.face2 .ojo_i {
  background-color: #fab005;}

.face2 .ojo_d {
  background-color: #fab005;}

.face2 .boca {
  border-radius: 150px 150px 150px 150px;
  background-color: #fab005;
  transform: translate(50%, 200%);
  height: 5px;}

.face2 h2 {
  color: #fab005;}

.face3 #cara {
  border: solid 4px red;}

.face3 .ojo_i {
  background-color: red;}

.face3 .ojo_d {
  background-color: red;}

.face3 .boca {
  border-radius: 150px 150px 0px 0px;
  background-color: red;
  transform: translate(50%, 80%);
  height: 10px;}

.face3 h2 {
  color: red;}

.faces p {
  font-size: 18px;
  margin-top: 10px;}

.informacion_estudiante h2 {
  display: none;}
 ```
> ## *Nota*
> * El container .faces se modifica para que tenga un ancho del 100% y un alto de 180px. 
> * Par las clases de cara .face1 &2,3, utilizadas como contenedores de las figuras, se genera un espaciado de contenido y una ubicacion utilizando flexbox. 
> * Luego se toma cada clase .face1 &2,3 de nuevo y se les da una padding específico para cada una. 
> * Al id #cara se le genera un tamaño específico de 50 px horizontal y vertical para hacer un círculo. 
> * Luego se les da una animación a las caras utilizado el transform scale que generará un efecto de zoom. 
> * Para las clases de ojos y boca, se genera el tamaño específico y la forma utlizando border radius con propiedades diferentes. 
> * En los elementos adicionales solo se modifican los colores para generar una compatibilidad de paleta de colores.  

### Vista por MediaQuery

**Mobile**

![image](https://user-images.githubusercontent.com/108433878/199125792-af4a3cda-0105-4332-a16a-8ad9ce1f0d15.png)

**Tablet & Desktop** 

![image](https://user-images.githubusercontent.com/108433878/199126879-b5d86263-b1e0-4321-90e5-0f91545be695.png)


## Sección cursos:
```bash
         <div class="satisfaction">
                <div class="satisfaction__container">
                    <div class="satisfaction__container--title">
                        <h2>Satisfacción por diplomado</h2>
                    </div>
                    <div class="satisfaction__container--porcentajes">
                        <div class="satisfaction__container--linear1"></div>
                        <p class="satisfaction__container--cien">100%</p>
                        <div class="satisfaction__container--linear2"></div>
                        <p class="satisfaction__container--cincuenta">50%</p>
                        <div class="satisfaction__container--linear3"></div>
                        <p class="satisfaction__container--c">0%</p>
                    </div>
                    <div class="satisfaction__container--linebackground">
                        <div class="satisfaction__container--barras">
                            <div class="satisfaction__container--barra1">
                                <div class="satisfaction__container--mini-barra1"></div>
                            </div>
                            <div class="satisfaction__container--barra2">
                                <div class="satisfaction__container--mini-barra2"></div>
                            </div>
                            <div class="satisfaction__container--barra3">
                                <div class="satisfaction__container--mini-barra3"></div>
                            </div>
                            <div class="satisfaction__container--barra4">
                                <div class="satisfaction__container--mini-barra4"></div>
                            </div>
                            <div class="satisfaction__container--barra5">
                                <div class="satisfaction__container--mini-barra5"></div>
                            </div>
                        </div>
                        <div class="satisfaction__container--textos">
                            <p class="satisfaction__container--biologia">Biologia</p>
                            <p class="satisfaction__container--economia">Economía circular</p>
                            <p class="satisfaction__container--quimica">Química</p>
                            <p class="satisfaction__container--ecologia">Ecología</p>
                            <p class="satisfaction__container--ingieneria">Ingienería ambiental</p>
                        </div>
                    </div>
                </div>
            </div>
 ```
 > ## *Nota*
 > * En esta sección de cursos, planeamos crear un carrusel para los cursos y que sea parte de la animación, pero solo esto se pueden ver en la version tablet y mobile. Adentro de las tarjetas de cada curso, hay una barra de progreso con una otra animación, moviendose de izquierda a derecha.
```bash
    .courses{
    width: 100%;
    height: 89vh;
    display: flex;
    justify-content: flex-start;
    margin: 0;
    padding-top: 15px;
  }
  
  
  .courses__container{
    display: flex;
    animation: cambio 20s infinite;
  }
  
  
  @keyframes cambio{
    0%{margin-left: 0;}
    20%{margin-left: 0;}
  
    25%{margin-left: -190%;}
    45%{margin-left: -190%;}
  
    50%{margin-left: -190%;}
    70%{margin-left: -190%;}
  
    75%{margin-left: 190%;}
    100%{margin-left: 190%;}
  }
 ```
 > * En el padre puse una posición relativa para que cada tarjeta y mantuvieran en la misma posición, pero que se apoyara con el "display: flex" y un "justify-content: center" para llevarlos a la mitad y un "aling items: center" para alienalos y un "overflow: scroll" para que tenga suficiente espacio para moverse.

 > * Para la animación del carrusel usamos la propiedad llamada "animation" dandole un nombre "cambio", con 20 segundos de transición y que sea infinito, pero así por si solo no se moverá, ya que no le estamos diciendo que hacer. Para ello se utiliza un "keyframe" llamandolo con una "@" y con el nombre de la animación, que en este caso se llama "cambio", dandole unos porcentajes con un "margin-left" para que se corrieran a la izquiera, pero como al principio lo puse en negativo, primero se moverá a la derecha, despues a la izquierda y terminando en el centro.

```bash
    .courses__information--barra{
  margin-top: 10px;
  position: relative;
  border: 1px solid #C2C2C2;
  border-top-right-radius: 25px;
  border-bottom-right-radius: 25px;
  background-color: #C2C2C2;
}


.courses__information--barra div{
  width: 0;
  padding: 20px;
  position: relative;
  border: 1px solid #009458;
  border-top-right-radius: 25px;
  border-bottom-right-radius: 25px;
  background-color: #009458;
}


.courses__information--mini-barra{
  animation: biologia-barra 2s forwards;
}


@keyframes biologia-barra{
  100%{
    width: 55%;
  }
}
 ```
 
> * En la segunda animación de progreso del curso, le puse una clase "courses__information--barra" para darle los estilos correspondientes, luego llamando a esa clase, con el "div" que es el hijo, le puse la misma "position: relative" al padre, para que sea paralelo, con sus propios estilos para identificarlos. Ya con el nombre de la clase del hijo "courses__information--mini-barra" le puse la animación llamado por cada curso, ejemplo: biologia-barra, con 2 segundos de movimiento y "fowards" este ultivo valor, permite moverse por medio de fotogramas. Después llame la propiedad "@keyframe" con el nombre de la animación "biologia-barra" y le dije que se moviera el 55% del fotograma total en el ancho del padre "courses__information--barra". Con esto permitió que se moviera de izquierda a derecha.

## Sección satisfacción:

> * Para esta sección la animación se encuentra de abajo hacia arriba en cada uno de los cursos que el estudiante ha cursado.
```bash
    .container-title{
    width: fit-content;
    height: 60px;
    border-radius: 15px;
    border-top-left-radius: 20px;
    border-bottom-left-radius: 20px;
    border-bottom-right-radius: 20px;
    margin: 5% 5% 0;
    background: linear-gradient(30deg, #009458 90%, transparent 20%);
    display: flex;
    align-items: center;
    }
```

> * El titulo, hice un "border-radius" normal, pero para que quedara con esa linea cortada, utilice el "background: linear-gradient(30deg, #009458 90%, transparent 20%);" esa transpariencia de 20% hizo que se empezará a difuminar en esa esquina.

```bash
.satisfaction__container--cien{
  position: absolute;
  top: 15%;
  left: 15px;
  font-family: 'Dosis', sans-serif;
  color: black;
}
```

> * Ya para las barras verticales y darle posicionamiento de lineas, textos y barras, tuve que darle un ancho al padre de 100% "satisfaction", para que despues al hijo del hijo otro ancho de 70% para las barras "satisfaction__container--barras" y darle un "position: absolute", para darle libertad en moverse y poder ubicarlo.