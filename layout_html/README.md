# HTML Layout Elements y Técnicas de Maquetación

## 1. ¿Qué es un HTML Layout?
Las páginas web suelen organizar su contenido en múltiples columnas o secciones organizadas (encabezado, menú, contenido principal, pie de página). Un layout (o maquetación) es la estructura visual que organiza estos elementos en la pantalla.

## 2. Elementos Semánticos de Layout en HTML5
HTML5 introdujo etiquetas específicas que le dan significado a la estructura del sitio web, mejorando el SEO y la accesibilidad:

- `<header>`: Define un encabezado para un documento o sección.
- `<nav>`: Define un conjunto de enlaces de navegación.
- `<section>`: Define una sección en un documento.
- `<article>`: Define contenido independiente y autónomo (ej. un post de blog).
- `<aside>`: Define contenido a un lado del contenido principal (ej. una barra lateral).
- `<footer>`: Define un pie de página para un documento o sección.
- `<details>`: Define detalles adicionales que el usuario puede abrir y cerrar.
- `<summary>`: Define un encabezado visible para el elemento `<details>`.

## 3. Técnicas de Maquetación en CSS
Para organizar estos elementos semánticos en la pantalla se utilizan principalmente 4 técnicas:

1. **CSS Frameworks:** Uso de librerías externas como Bootstrap o Tailwind CSS.
2. **CSS Float Property:** Técnica tradicional (antigua) usando `float` y `clear`.
3. **CSS Flexbox (Recomendado para 1D):** Diseñado para maquetar elementos en una sola dimensión (fila o columna). Ajusta el tamaño de los elementos dinámicamente.
4. **CSS Grid (Recomendado para 2D):** Diseñado para maquetar elementos en dos dimensiones (filas y columnas al mismo tiempo).