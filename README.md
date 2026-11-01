# Informática Aplicada II

Guía didáctica para 1.er año (2.º semestre) de la Tecnicatura en Marketing, CETP-UTU, Plan 2019.
Ed. Téc. Laura Castro.

Los estudiantes, en equipos de 4, arman la campaña publicitaria digital de una marca: brief, fotos, spot de video, sitio web y plan de redes. Cada tema tiene un paso a paso y una entrega parcial. La defensa final es el **20 de noviembre**.

Todas las herramientas son online, gratis y no se instala nada: Photopea, Canva (o Clipchamp), YouTube, Google Sites (nivel básico), Wix (nivel intermedio), Google Drive, Docs y Sheets.

| Tema | Unidad del programa | Herramienta | Entrega |
| --- | --- | --- | --- |
| Tu campaña | Metodología y derechos de autor | Google Drive y Docs | — |
| Fotografía | 2. Fotografía digital | Celular, Photopea | E1 · Brief y kit fotográfico |
| Video | 1. Videos | Canva o Clipchamp, YouTube | E2 · Spot de video |
| Sitio web | 3. Marketing web | Google Sites (básico) · Wix (intermedio) | E3 · Sitio web de la campaña |
| Redes | 4. Redes sociales | Canva, Google Sheets | E4 · Plan de redes y licencias |
| Proyecto final | Evaluación | Todas | Campaña integrada y defensa |

## Archivos

- `index.html`: la guía completa, en un solo archivo.
- `README.md`: estas instrucciones.
- `.nojekyll`: le indica a GitHub Pages que publique los archivos tal cual.

## Publicar con GitHub Pages (todo desde la web)

1. En github.com, tocá **+ › New repository**. Nombre: `informatica-aplicada-ii`. Marcá **Public** y tocá **Create repository**.
2. En el repositorio vacío, tocá **uploading an existing file**. Arrastrá `index.html` y `README.md` y tocá **Commit changes**.
3. Andá a **Settings › Pages**. En **Branch** elegí `main` y la carpeta `/ (root)`, y tocá **Save**.
4. En uno o dos minutos la guía queda en `https://TU-USUARIO.github.io/informatica-aplicada-ii/`. Ese es el enlace para los estudiantes (CREA, WhatsApp del grupo).

## Cambiar las fechas de entrega

En GitHub, abrí `index.html`, tocá el lápiz (**Edit this file**) y buscá `var CALENDARIO`. Cambiá solo las fechas, con el formato año-mes-día, y tocá **Commit changes**:

```js
var CALENDARIO = {
  e1: '2026-11-04',   // Entrega 1 · Brief y kit fotográfico
  e2: '2026-11-10',   // Entrega 2 · Spot de video
  e3: '2026-11-13',   // Entrega 3 · Sitio web de la campaña
  e4: '2026-11-17',   // Entrega 4 · Plan de redes y registro de licencias
  final: '2026-11-20'    // Proyecto final · Campaña integrada y defensa
};
```

Cada tema muestra la fecha de su entrega en "Qué hacés en este tema".

## Plantillas: botón "Hacer mi copia"

La guía tiene 4 botones de plantilla: el brief y la ficha de fotos (Entrega 1, y el brief también en la parte 1.3), el guion del spot (Entrega 2) y la planilla de redes (Entrega 4). En cada entrega están en el recuadro **Antes de entregar**, justo arriba de **Cómo entregar**, con los pasos para hacer la copia, compartirla con el equipo y copiar el enlace para el formulario. Cada botón crea una copia en el Drive del estudiante.

1. Subí a tu Google Drive los archivos de la carpeta `plantillas` (`brief-de-la-campana.docx`, `ficha-de-fotos.docx`, `guion-del-spot.docx`, `planilla-de-redes.xlsx`).
2. Abrí cada uno y elegí **Archivo › Guardar como Documentos de Google** (o **Guardar como Hojas de cálculo de Google** para la planilla). Desde ahí trabajá con esa versión de Google.
3. **Compartir › Acceso general › Cualquier persona con el enlace › Lector**, y **Copiar enlace**.
4. En `index.html`, buscá `var PLANTILLAS` y pegá cada enlace entre las comillas:

```js
var PLANTILLAS = {
  brief: 'https://docs.google.com/document/d/…/edit?usp=sharing',
  fotos: 'https://docs.google.com/document/d/…/edit?usp=sharing',
  guion: 'https://docs.google.com/document/d/…/edit?usp=sharing',
  redes: 'https://docs.google.com/spreadsheets/d/…/edit?usp=sharing'
};
```

La guía convierte cada enlace en "Hacer una copia". Mientras un enlace esté vacío, el botón avisa que la plantilla todavía no está.

## Conectar el formulario de entregas (Google Forms)

1. Creá un formulario en forms.google.com con estas preguntas:
   - **Equipo e integrantes**: respuesta corta.
   - **Entrega**: desplegable con estas opciones, escritas exactamente así:
     - `Entrega 1 · Brief y kit fotográfico`
     - `Entrega 2 · Spot de video`
     - `Entrega 3 · Sitio web de la campaña`
     - `Entrega 4 · Plan de redes y registro de licencias`
     - `Proyecto final · Campaña integrada y defensa`
   - **Enlaces** (carpeta de Drive, video, sitio, planilla): párrafo.
   - **Archivos**: carga de archivos (pide iniciar sesión con Google; los archivos quedan en tu Drive).
2. En el formulario, tocá **⋮ › Obtener vínculo prefijado**. Escribí cualquier cosa en "Equipo", elegí una opción en "Entrega" y tocá **Obtener vínculo**. En el enlace copiado vas a ver dos números como `entry.123456789`.
3. En `index.html`, buscá `var FORMULARIO` y completá:

```js
var FORMULARIO = {
  url: 'https://docs.google.com/forms/d/e/XXXX/viewform',
  campoEquipo: 'entry.111111111',
  campoEntrega: 'entry.222222222',
  campoComentario: 'entry.333333333'   // ahí viaja el nivel elegido (Básico o Avanzado)
};
```

Desde ahí, el botón **Entregar en el formulario** de cada entrega abre el formulario con el equipo, la entrega y el nivel ya cargados (el nivel aparece en "Comentarios para la docente"). Mientras `url` esté vacío, la guía avisa que el formulario todavía no está listo.

## Cómo guarda el avance

Las casillas "Lo leí", los pasos, las notas y el estado de cada entrega se guardan en el navegador de cada estudiante. No se envían a ningún lado.

- **Para no borrar el avance de nadie:** actualizá siempre el mismo `index.html` en el mismo repositorio. No le cambies el nombre al repositorio ni crees uno nuevo: el avance está atado a la dirección del sitio.
- **Si cambian de computadora,** las marcas no aparecen en la otra. Lo entregado en el formulario no se pierde.
- Lo que entregaron en el formulario queda en tu Drive y no depende de la página.

## Cómo está organizada la guía

Una sola página con pestañas por tema. Fondo crema, azul tinta y un color por tema (azul, coral, mostaza, salvia), con letras Manrope (títulos) y DM Sans (texto). Los colores de texto están ajustados para leerse bien (contraste AA).

- **En la computadora:** a la izquierda, el panel **Recorrido** con los 6 temas, Ayuda y Glosario. Debajo de la barra, una línea coral muestra cuánto se leyó de la página.
- **Arriba:** el botón **Menú**, que abre el índice con los temas, sus partes y las entregas; los 6 temas con su punto de color, solo como decoración; y los enlaces **Ayuda** y **Glosario**.
- **Al comenzar la página:** el tamaño de la **Letra** y el modo oscuro.
- **Inicio:** una tarjeta con el lema «Una idea. Una campaña. Mil formas de comunicar.», el botón **Empezar por el tema 1** y **Elegí tu nivel**.
- **Cada entrega** se entrega desde la misma tarea: al final están el nombre del equipo (se escribe una sola vez), el botón **Entregar en el formulario** y la casilla **Ya la subimos**.
- **Cada tema** empieza con "Qué hacés en este tema". Las partes están numeradas y cada una termina con **Lo leí**. Al final está la entrega, con sus pasos para marcar.

## Entrega 1: tres caminos para las fotos

Cada equipo elige cómo consigue las fotos y la elección viaja sola al formulario, en "Comentarios para la docente" (por ejemplo: `Nivel: Básico · Camino B: fotos que ya tenían`).

- **A · Fotos nuevas:** las sacan ahora con el celular.
- **B · Fotos que ya tienen** de su emprendimiento real: eligen las mejores, las retocan y explican su luz y encuadre.
- **C · Imágenes con IA:** valen si lo dicen («imagen generada con IA») y anotan qué le pidieron. Si el producto es real, la foto del producto tiene que ser real.

Lo único que no vale es presentar una imagen de IA como foto propia. La regla está explicada en **Redes › Inteligencia artificial: usarla con honestidad**, con su hoja de **uso de IA** en el registro de licencias.

## Dos niveles (DUA)

Cada parte y cada entrega tiene un **nivel básico** y un **nivel intermedio**. Cada estudiante elige el suyo en el inicio o en **Mi nivel**, y lo puede cambiar cuando quiera.

- **Básico:** explicaciones cortas, paso a paso, y entregas con menos piezas. Cumple lo que pide el programa. El sitio web se hace en Google Sites.
- **Intermedio:** las explicaciones completas, la lista de pasos completa y desafíos extra. El sitio web se hace en **Wix** (gratis, varias páginas, SEO por página).
- Cada parte tiene dos pestañas, **Básico** e **Intermedio**, como en el curso de Diseño Web. Se abre en el nivel elegido y la otra pestaña muestra el otro nivel solo en esa parte.
- En cada entrega el equipo puede elegir un nivel distinto al general. Si ya habían marcado pasos de la lista completa, la entrega se abre en intermedio para que vean lo marcado.

Los dos niveles son una parte del Diseño Universal para el Aprendizaje. La guía también ofrece distintas formas de presentar la información (texto corto y completo, dibujos, tablas, glosario, letra grande), de hacer y entregar (niveles, herramientas a elegir, enlaces o archivos) y de motivarse (marca real, equipo, avance a la vista). Está explicado para los estudiantes en **Ayuda › Sobre esta guía**.
