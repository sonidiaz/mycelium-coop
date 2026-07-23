# mycelium-coop

Sitio web de Mycelium Coop. Es una página simple: todo el contenido y el diseño viven en un único archivo, [index.html](index.html).

## Guía para el propietario del proyecto: cómo actualizar el sitio con ayuda de la IA

Esta guía está pensada para una persona sin conocimientos de programación. No requiere instalar Git ni configurar ningún servidor. El trabajo combina el sitio [github.com](https://github.com) (desde el navegador, para descargar y subir el archivo) con la aplicación de Claude instalada en el ordenador (para editarlo).

### Requisito previo

Tener acceso al repositorio de GitHub `sonidiaz/mycelium-coop`. Si no se tiene acceso, solicitar a quien administre el repositorio que agregue al usuario como colaborador.

### Paso 1: Descargar el archivo desde GitHub

1. Ingresar a [github.com](https://github.com) y entrar al repositorio `sonidiaz/mycelium-coop`.
2. Hacer clic en el archivo [index.html](index.html) para abrirlo.
3. Usar la opción para descargarlo (el ícono de descarga o "Download raw file") y guardarlo en el ordenador, en una carpeta fácil de encontrar (por ejemplo, "Escritorio").

### Paso 2: Pedir el cambio a la aplicación de Claude

1. Abrir la aplicación de Claude en el ordenador.
2. Adjuntar a la conversación el archivo `index.html` descargado en el paso anterior.
3. Describir el cambio deseado con palabras simples. Por ejemplo:

   > "Cambia el título principal de la portada por 'Liderazgo regenerativo para tiempos de cambio'"

   > "Agrega un nuevo testimonio en la sección correspondiente, a nombre de Juana Pérez, con el siguiente texto: ..."

   > "El botón de contacto no funciona, revísalo"

4. Pedirle a Claude que entregue el archivo `index.html` completo y actualizado, y guardarlo en el ordenador (conservando el mismo nombre de archivo).

### Paso 3: Revisar el cambio antes de publicarlo

1. Ubicar el archivo `index.html` guardado en el paso anterior y abrirlo con doble clic (se abre directamente en el navegador).
2. Verificar que el sitio se vea como se espera. Si algo no resulta satisfactorio, continuar la conversación con Claude indicando el ajuste necesario y volver a guardar el archivo actualizado.

### Paso 4: Subir el cambio a GitHub

1. Ingresar nuevamente a [github.com](https://github.com), al repositorio `sonidiaz/mycelium-coop`.
2. Abrir el archivo [index.html](index.html) y usar el ícono con forma de lápiz ("Edit this file") o la opción "Add file" > "Upload files" para reemplazarlo por la nueva versión.
3. Escribir una breve descripción del cambio realizado en el campo de mensaje de confirmación (commit).
4. Confirmar la subida directamente sobre la rama principal (`main`).

### Buenas prácticas

- **Conservar el nombre del archivo** (`index.html`) exactamente igual al subir la nueva versión.
- **Pedir cambios de a uno por vez.** Resulta más fácil revisarlos y, si algo sale mal, más fácil identificar qué lo causó.
- **Revisar siempre el archivo en el navegador antes de publicarlo**, abriéndolo localmente con doble clic.
- **Si algo sale mal luego de subir el cambio**, GitHub conserva el historial de versiones del archivo: se puede acceder a él desde la vista del archivo ("History") y recuperar una versión anterior.
- **No compartir contraseñas** con nadie; el acceso a GitHub y a la aplicación de Claude se realiza siempre mediante inicio de sesión personal.

## Guía para subir o actualizar imágenes

Las imágenes del sitio se guardan en la carpeta `img`, tanto en la copia local como en el servidor. El proceso es similar al utilizado para actualizar `index.html`, con la diferencia de que las imágenes se suben directamente a esa carpeta, sin pasar por la aplicación de Claude.

### Preparar la imagen

- Elegir un nombre de archivo simple, sin espacios, tildes ni caracteres especiales (por ejemplo: `equipo-2026.jpg`, no `Equipo Nuevo (2026).jpg`).
- Formatos recomendados: `.jpg`, `.png` o `.webp`.

### Caso A: Reemplazar una imagen ya existente

1. Ingresar a [github.com](https://github.com), al repositorio `sonidiaz/mycelium-coop`, y entrar a la carpeta `img`.
2. Usar "Add file" > "Upload files" y arrastrar la nueva imagen, **con exactamente el mismo nombre de archivo** que la que se quiere reemplazar.
3. Escribir una breve descripción en el mensaje de confirmación (commit) y confirmar sobre la rama principal (`main`).
4. Como el nombre del archivo no cambia, no es necesario modificar `index.html`: el sitio va a mostrar la nueva imagen automáticamente.

### Caso B: Agregar una imagen nueva

1. Subir la imagen a la carpeta `img` en GitHub, siguiendo los mismos pasos que en el Caso A (con un nombre de archivo nuevo, que todavía no exista en esa carpeta).
2. Abrir la aplicación de Claude en el ordenador y adjuntar el archivo `index.html` (descargado como se indica en el Paso 1 de la guía anterior).
3. Pedirle a Claude que incorpore la imagen, indicando el nombre de archivo y dónde debe aparecer. Por ejemplo:

   > "Agrega la imagen img/equipo-2026.jpg como foto de portada en la sección 'Nuestro equipo'"

4. Pedirle a Claude que entregue el `index.html` completo y actualizado, y guardarlo en el ordenador.
5. Subir el `index.html` actualizado a GitHub siguiendo el Paso 4 de la guía anterior.

### Cómo revisar la imagen antes de publicarla

Para poder ver la imagen al abrir `index.html` localmente con doble clic, la carpeta `img` con esa imagen debe estar guardada en el ordenador, en la misma carpeta que el archivo `index.html` (por ejemplo, ambos dentro de "Escritorio"). Si la imagen no se descargó localmente, el sitio funcionará igual una vez publicado en GitHub, pero no se va a ver en la vista previa local.

### Buenas prácticas para imágenes

- **Optimizar el tamaño del archivo antes de subirlo** (idealmente menos de 500 KB por imagen), para que el sitio cargue rápido. Se le puede pedir ayuda a Claude para comprimir o redimensionar una imagen.
- **No reutilizar un nombre de archivo para una imagen distinta** a menos que se quiera reemplazarla intencionalmente.
- **Revisar el historial de la carpeta `img` en GitHub** ("History") si es necesario recuperar una imagen anterior.
