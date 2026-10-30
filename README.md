# Informática Aplicada II

Guía didáctica para 1.er año (2.º semestre) de la Tecnicatura en Marketing, CETP-UTU, Plan 2019.
Ed. Téc. Laura Castro.

Los estudiantes, en equipos de 4, convierten la campaña de Publicidad en fotos, un spot de video, un sitio web y un plan de redes. Cada tema tiene un paso a paso y una entrega parcial. La defensa final es el **20 de noviembre**.

Todas las herramientas son online, gratis y no se instala nada: Photopea, Canva (o Clipchamp), YouTube, Google Sites, Google Drive, Docs y Sheets.

| Tema | Unidad del programa | Herramienta | Entrega |
| --- | --- | --- | --- |
| Tu campaña | Metodología y derechos de autor | Google Drive y Docs | — |
| Fotografía | 2. Fotografía digital | Celular, Photopea | E1 · Brief y kit fotográfico |
| Video | 1. Videos | Canva o Clipchamp, YouTube | E2 · Spot de video |
| Sitio web | 3. Marketing web | Google Sites | E3 · Sitio web de la campaña |
| Redes | 4. Redes sociales | Canva, Google Sheets | E4 · Plan de redes y licencias |
| Proyecto final | Evaluación | Todas | Campaña integrada y defensa |

## Archivos

- `index.html`: la guía completa, en un solo archivo.
- `README.md`: estas instrucciones.

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

La portada muestra sola cuál es la próxima entrega y cuántos días faltan.

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
  campoEntrega: 'entry.222222222'
};
```

Desde ahí, el botón **Entregar en Drive** de cada entrega abre el formulario con el equipo y la entrega ya cargados. Mientras `url` esté vacío, la guía avisa que el formulario todavía no está listo.

## Cómo guarda el avance

Las casillas "Lo leí", los pasos y las notas se guardan en el navegador de cada estudiante. No se envían a ningún lado. Si cambian de computadora, las marcas no aparecen, pero el trabajo está en el Drive del equipo.
