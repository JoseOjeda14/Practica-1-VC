## Práctica 1.

## Autores: José Miguel Ojeda Hernández y Yendey Morán Delgado

El primer paso necesario para realizar esta práctica fue importar los paquetes necesarios, correspondiendo a la celda Nº 1
Acontinuación vamos a explicar en que consiste cada Tarea.

## Tarea 1

La primera tarea consiste en analizar las diferencias a nivel de código entre nuestra solución y la generada por una inteligencia artificial para crear un tablero de ajedrez.
La segunda celda del documento contiene el código desarrollado por nosotros, al cual hemos añadido como funcionalidad extra una simulación de las piezas de ajedrez ubicadas en las dos filas superiores y las dos inferiores. Por otro lado, la tercera celda muestra la solución propuesta por la IA,Gemini Pro. Al comparar ambas versiones, se puede observar que la inteligencia artificial genera un código mucho más compacto, directo y con un menor uso de estructuras condicionales.

## Tarea 2

Esta segunda tarea consiste en generar un cuadro estilo Mondrian usando únicamente primitivas de la librería OpenCV, como líneas y rectángulos rellenos.

Lo primero que hacemos es inicializar el lienzo y cambiar todo el color de fondo a blanco para que se vea mejor la base. Después comenzamos con los pasos técnicos de la composición: usando la función cv2.rectangle, vamos poniendo rectángulos de colores primarios (rojos, azules y amarillos). Para ello calculamos sus coordenadas exactas y le indicamos un grosor de -1 para asegurarnos de que queden totalmente rellenos de color.

Ya con los bloques de color posicionados, finalizamos poniendo líneas negras con la función cv2.line, tanto verticales como horizontales y con un grosor de 3. Hacemos este paso al final a propósito para que las líneas se superpongan a los rectángulos.

## Tarea 3

La tercera tarea consiste en dibujar círculos sobre los píxeles más oscuros y más claros captados por la cámara del portátil. Además, hemos añadido una funcionalidad para detectar y marcar los píxeles con colores dominantes más cercanos al rojo, verde y azul, si se encuentran presentes en el fotograma.

A modo de resumen, los pasos realizados para llevar a cabo la tarea han sido los siguientes: en primer lugar, capturamos el vídeo de la cámara mediante un bucle continuo que lee fotograma a fotograma hasta que el usuario pulsa la tecla "ESC". Para optimizar el rendimiento, reescalamos cada fotograma a una resolución menor,dividiendo la imagen en celdas de 10x10.
A continuación, recorremos cada píxel de esta imagen reducida evaluando su luminosidad total y la predominancia de sus canales BGR para identificar los píxeles más claros y oscuros además de los píxeles más cercanos al rojo, verde y azul. Finalmente, trasladamos esas coordenadas de vuelta a su tamaño original y dibujamos los resultados directamente sobre el fotograma a color. Los puntos de mayor y menor luminosidad se representan con un círculo blanco, mientras que los puntos rojo, verde y azul se marcan utilizando el color exacto del píxel detectado.

## Tarea 4

Esta última tarea se trata de proponer un Pop Art usando la cámara del portátil. Para ello, nos hemos basado mayoritariamente en el estilo de Roy Lichtenstein con efecto de cómic y luego hemos cambiado tonos como en el ejemplo de Andy Warhol que usamos para aprender a realizar la tarea.

Lo primero que hacemos es capturar el vídeo y reducir la resolución a la mitad con la idea de optimizar el rendimiento. Después comenzamos con los pasos técnicos del estilo: Procesamos el fotograma aplicando una posterización para dejar los colores en tonos planos y extraemos los contornos por un filtro de suavizado y un umbral adaptativo para los trazos negros. Ya con el efecto de cómic, separamos los canales (BGR) y los reasignamos en cada uno de los cuatro cuadrantes.

La fuente principal utilizada fue esta web: https://www.wikiart.org/es/roy-lichtenstein, que contiene obras del artista para guiarnos.