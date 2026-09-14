Simula ser un desarrollador web que cumple con los estándares W3C y WCAG 2.2. Necesito que hagas un código para un sitio web estático usando solamente HTML y CSS. Está prohibido usar JavaScript o cualquier otro lenguaje.

El objetivo del sitio web es para un emprendimiento que vende artesanías agrupadas en tres categorías: 1- tejidos, 2- cerámicas y 3- pinturas.

Debes cumplir con estos requisitos de manera perfecta:

Requisito 1 - Archivos requeridos: devolveme el código para un archivo index.html y un archivo de estilos llamado estilosIA.css. Deben ser archivos separados.

Requisito 2 - Barra de navegación: debe mostrar enlaces a información de contacto que lleve a una sección con un formulario simple. Información de quien mantiene el sitio, es decir una sección tipo "Acerca de". Y una lista de artículos agrupados por categoría.

Requisito 3 - Interacción estática: El usuario debe poder elegir una categoría usando un menú desplegable, radio buttons o anclas y al seleccionarla, se debe mostrar los artículos de esa categoría de la página. Todo esto debe resolverse solamente con HTML y CSS.

Requisito 4 - Contenido de los artículos: genera información para al menos tres artículos por cada categoría, con un total de nueve artículos.

Requisito 5 - Estructura de directorios: simula que las imágenes y PDFs de cada artículo están en una carpeta llamada "articulos", la cual tiene subclases para cada categoría. HTML puede apuntar a las rutas así articulos/tejidos/articulo1.png (y articulo2.png).

Requisito 6 - Imágenes representativas del artículo: cada artículo debe mostrarse con una imagen representativa y un enlace a su información.

Requisito 7 - Responsividad: el sitio debe ser sí o sí completamente responsivo.

Rta (Respuesta de la IA):
Listo. Algunas notas sobre cómo cumplí cada requisito:

Filtrado sin JS (Req. 3): son 4 input type="radio" (name="categoria") ocultos visualmente pero accesibles por teclado/lector de pantalla (técnica clip, no display:none), con <label> como pestañas. El truco :checked + combinador de hermanos generales (~) muestra el grupo de artículos correspondiente. Están declarados como hermanos directos dentro de #catalogo, antes de los tres div.articulos-grupo, para que el selector funcione.

Estructura de carpetas (Req. 5): todas las imágenes apuntan a articulos/{categoria}/articuloN.png y los PDFs a articulos/{categoria}/articuloN.pdf — tendrás que crear esa carpeta articulos/tejidos, articulos/ceramicas, articulos/pinturas con los archivos reales junto al index.html.

Accesibilidad WCAG 2.2: enlace "saltar al contenido", lang="es", foco visible (:focus-visible), texto alternativo descriptivo en cada imagen, enlaces con propósito claro (no dicen solo "PDF" sino qué artículo), formulario con <label for> asociados, contraste de color pensado para AA, y respeto de prefers-reduced-motion.

Responsivo (Req. 7): grid con auto-fit/minmax para las tarjetas, navegación en flex-wrap, y media queries en 48rem y 30rem para tablets/celulares.
i querés, puedo generarte también las 9 imágenes/PDFs de muestra (placeholders) o adaptar la paleta de colores.

Mi Rta:
Sí, quiero que me generes las 9 imágenes/PDFs de muestra.

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
