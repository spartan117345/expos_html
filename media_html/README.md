# Guía de Medios en HTML: Video, Audio y Complementos

Este documento proporciona una referencia técnica sobre cómo integrar y gestionar contenido multimedia utilizando los estándares de HTML5.

---

## 1. Implementación de Video (`<video>`)

El elemento `<video>` es el estándar para mostrar películas o clips de video en una página web.

### Ejemplo de Código Básico

```html
<video width="320" height="240" controls>
  <source src="pelicula.mp4" type="video/mp4">
  <source src="pelicula.ogg" type="video/ogg">
  Tu navegador no soporta la etiqueta de video.
</video>
```

* **Atributos recomendados:** Es aconsejable incluir siempre `width` (ancho) y `height` (alto) para evitar que la página parpadee mientras el video se carga.
* **Controles:** El atributo `controls` añade botones esenciales como reproducción, pausa y volumen.

### Autoplay y Restricciones

* El atributo `autoplay` inicia el video automáticamente.
* En navegadores basados en Chromium, el inicio automático suele estar bloqueado a menos que se añada el atributo `muted` (silenciado).

---

## 2. Formatos de Video y Tipos de Medios

HTML soporta principalmente tres formatos de video, cada uno con su correspondiente tipo de medio (MIME):

| Formato | Tipo de Medio (MIME) | Soporte en Navegadores |
| :--- | :--- | :--- |
| **MP4** | `video/mp4` | Compatible con Edge, Chrome, Firefox, Safari y Opera. |
| **WebM** | `video/webm` | Compatible con Edge, Chrome, Firefox, Safari y Opera. |
| **Ogg** | `video/ogg` | Compatible con Edge, Chrome, Firefox y Opera *(No Safari)*. |

> **Nota:** El navegador cargará automáticamente el primer formato que reconozca dentro de la lista de etiquetas `<source>`.

---

## 3. Audio, YouTube y Complementos

Además del video, el estándar HTML contempla otras formas de integración de medios:

* **Audio:** Se utiliza el elemento `<audio>` para integrar sonidos o música.
* **YouTube:** Permite la inserción de videos directamente desde la plataforma de YouTube.
* **Complementos (Plug-ins):** Se gestionan habitualmente mediante la etiqueta `<object>` para definir recursos externos o funcionalidades adicionales.

---

## 4. Referencia de Etiquetas Multimedia

| Etiqueta | Descripción |
| :--- | :--- |
| `<video>` | Define un video o película. |
| `<audio>` | Define contenido de sonido. |
| `<source>` | Define múltiples recursos para que el navegador elija el más compatible. |
| `<track>` | Define pistas de texto (como subtítulos) para el reproductor. |

---

## 5. Control mediante JavaScript (DOM)

El DOM (*Modelo de Objetos del Documento*) permite interactuar con los elementos de video mediante programación:

* Es posible utilizar métodos como `play()` y `pause()`.
* Permite consultar y modificar propiedades para ajustar el volumen y la duración del contenido.
* Notifica cambios de estado mediante eventos (como cuando el video comienza a reproducirse o se detiene).