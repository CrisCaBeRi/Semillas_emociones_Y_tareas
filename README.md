# Semillas_emociones_Y_tareas
Desarrollo de un dashboard para la fundación "Semillas".



# Sección cursos:
En esta sección de cursos, planeamos crear un carrusel para los cursos y que sea parte de la animación, pero solo esto se pueden ver en la version tablet y mobile.
Adentro de las tarjetas de cada curso, hay una barra de progreso con una otra animación, moviendose de izquierda a derecha.


En el padre puse una posición relativa para que cada tarjeta y mantuvieran en la misma posición, pero que se apoyara con el "display: flex" y un "justify-content: center"
para llevarlos a la mitad y un "aling items: center" para alienalos y un "overflow: scroll" para que tenga suficiente espacio para moverse.


Para la animación del carrusel usamos la propiedad llamada "animation" dandole un nombre "cambio", con 20 segundos de transición y que sea infinito, pero así
por si solo no se moverá, ya que no le estamos diciendo que hacer. Para ello se utiliza un "keyframe" llamandolo con una "@" y con el nombre de la animación, que en
este caso se llama "cambio", dandole unos porcentajes con un "margin-left" para que se corrieran a la izquiera, pero como al principio lo puse en negativo, primero
se moverá a la derecha, despues a la izquierda y terminando en el centro.


En la segunda animación de progreso del curso, le puse una clase "courses__information--barra" para darle los estilos correspondientes, luego llamando a esa clase, con el
"div" que es el hijo, le puse la misma "position: relative" al padre, para que sea paralelo, con sus propios estilos para identificarlos. Ya con el nombre de la clase del
hijo "courses__information--mini-barra" le puse la animación llamado por cada curso, ejemplo: biologia-barra, con 2 segundos de movimiento y "fowards" este ultivo valor,
permite moverse por medio de fotogramas.
Después llame la propiedad "@keyframe" con el nombre de la animación "biologia-barra" y le dije que se moviera el 55% del fotograma total en el ancho del padre "courses__information--barra". Con esto permitió que se moviera de izquierda a derecha.


# Sección satisfacción:
Para esta sección la animación se encuentra de abajo hacia arriba en cada uno de los cursos que el estudiante ha cursado, se tiene que actualizar la pagina y estar en esta
sección para verlas, siempre y cuendo se encuentren en mobile o tablet.


El titulo, hice un "border-radius" normal, pero para que quedara con esa linea cortada, utilice el "background: linear-gradient(30deg, #009458 90%, transparent 20%);"
esa transpariencia de 20% hizo que se empezará a difuminar en esa esquina.


Ya para las barras verticales y darle posicionamiento de lineas, textos y barras, tuve que darle un ancho al padre de 100% "satisfaction", para que despues al hijo del hijo 
otro ancho de 70% para las barras "satisfaction__container--barras" y darle un "position: absolute", para darle libertad en moverse y poder ubicarlo.