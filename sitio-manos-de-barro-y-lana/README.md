Prompt: 
Simula ser un desarrollador web que cumple con los estandares W3C y WCAG 2.2. Necesito que hagas un codigo para un sitio web estatico usando solamente HTML y CSS. Esta prohibodp usar JavaScript o cualquier otro lenguaje. 
El objetivo del sitio web es para un emprendimiento que vende artesanias agrupadas en tres categorias: 1- tejidos, 2- ceramicas y 3- pinturas. 
Debes cumplir con estos requisitos de manera perfecta: 
Requisito 1 los archivos requeridos: devolveme el codigo para un archivo index.html y un archivo de estilos llamado estilosIA.css. Deben ser archivos separados. 
Requisito 2 la barra de navegacion: una barra de navegacion que debe mostrar una barra de navegacion con enlaces a informacion de contacto que lleve a una seccion con un formulario simple. Informacion de quien matiene el sitio, es decir una seccion tipo "Acerca de". Y una lista de articulos agrupados por categoria. 
Requisito 3 la interaccion debe ser estatica: El usuario debe poder elegir una categoría usando un menu desplegable, radio/ buttons o anclas  y al seleccionarla, se debe mostrar los articulos de esa categoria de la pagina. Todo esto debe resolverse solamente con HTML y CSS 
Requisito 4 el contenido de los articulos: genera informacion para al menos tres articulos por cada categoria, con un total de nueve articulos. 
Requisito 5 la estructura de directorios: simula que las imagenes y PDFs de cada articulo estan en una carpeta llamada "articulos", la cual tiene subclases para cada categoria. HTML puede apuntar a las rutas asi articulos/tejidos/articulo1.png (y articulo2.png)
Requisito 6 las imagenes representativas del ariculo: cada articulo debe mostrarse con una imagen representativa y un enlace a su informacion.
Requisito 7 el sitio debe ser si o si completamente responsivo. 

Rta: 
Listo. Algunas notas sobre cómo cumplí cada requisito:

Filtrado sin JS (Req. 3): son 4 input type="radio" (name="categoria") ocultos visualmente pero accesibles por teclado/lector de pantalla (técnica clip, no display:none), con <label> como pestañas. El truco :checked + combinador de hermanos generales (~) muestra el grupo de artículos correspondiente. Están declarados como hermanos directos dentro de #catalogo, antes de los tres div.articulos-grupo, para que el selector funcione.
Estructura de carpetas (Req. 5): todas las imágenes apuntan a articulos/{categoria}/articuloN.png y los PDFs a articulos/{categoria}/articuloN.pdf — tendrás que crear esa carpeta articulos/tejidos, articulos/ceramicas, articulos/pinturas con los archivos reales junto al index.html.
Accesibilidad WCAG 2.2: enlace "saltar al contenido", lang="es", foco visible (:focus-visible), texto alternativo descriptivo en cada imagen, enlaces con propósito claro (no dicen solo "PDF" sino qué artículo), formulario con <label for> asociados, contraste de color pensado para AA, y respeto de prefers-reduced-motion.
Responsivo (Req. 7): grid con auto-fit/minmax para las tarjetas, navegación en flex-wrap, y media queries en 48rem y 30rem para tablets/celulares.

Si querés, puedo generarte también las 9 imágenes/PDFs de muestra (placeholders) o adaptar la paleta de colores.

Mi Rta: si quiero que me generes las 9 imagenes/PDFs de muestra

Rta: 
El ZIP incluye todo, ya con la estructura de carpetas correcta:
sitio-manos-de-barro-y-lana/
├── index.html
├── estilosIA.css
└── articulos/
    ├── tejidos/
    │   ├── articulo1.png + articulo1.pdf
    │   ├── articulo2.png + articulo2.pdf
    │   └── articulo3.png + articulo3.pdf
    ├── ceramicas/  (mismos 3 pares)
    └── pinturas/   (mismos 3 pares)

Detalles:

Imágenes (PNG): son ilustraciones simples estilo vectorial (no fotos), dibujadas con la misma paleta de colores del sitio, para que combinen visualmente y sirvan de placeholder decente hasta que subas fotos reales de los productos.
PDFs: cada uno es una ficha técnica de una página con el nombre del artículo, categoría, descripción, materiales, dimensiones, cuidados y precio de referencia, incluyendo la imagen correspondiente.


