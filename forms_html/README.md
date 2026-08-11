# Exposición Súper Sencilla: Formularios HTML

---

##  ¿Qué es un Formulario HTML?
Es la herramienta que usa una página web para **pedirle datos al usuario** (como un registro, un inicio de sesión o una encuesta) y mandárselos a una computadora servidora para procesarlos.

> **Metáfora:** Es como una planilla en papel que llenas con lapicero y entregas en una ventanilla.

---

##  Las 3 Partes Clave

1. **`<form>`**: La caja grande que contiene todo.
   * `action`: ¿A dónde van los datos? (ej. `/guardar`)
   * `method`: ¿Cómo se envían? (`POST` para seguridad, `GET` para búsquedas).

2. **`<label>`**: El texto que le dice al usuario qué escribir.

3. **`<input>`**: El cuadro donde el usuario escribe o selecciona datos.
   * ¡Muy importante! Debe llevar el atributo **`name`** para que el servidor sepa qué dato recibe (ej: `name="nombre"`).

---

##  Ejemplo Breve y Fácil de Explicar

```html
<form action="/enviar" method="POST">

  <!-- Campo 1: Nombre -->
  <label for="nombre">Nombre:</label>
  <input type="text" id="nombre" name="usuario" placeholder="Tu nombre" required>

  <!-- Campo 2: Correo -->
  <label for="correo">Correo:</label>
  <input type="email" id="correo" name="email" required>

  <!-- Botón de Envío -->
  <button type="submit">Enviar Datos</button>

</form>
```

---

##  Guía para Explicar el Ejemplo (30 segundos)

1. **"Aquí abrimos la etiqueta `<form>`"**: Indica que todo lo que está dentro es parte del formulario que enviará datos por método `POST`.
2. **"Usamos `<label>` e `<input>` juntos"**: El `label` da la instrucción ("Nombre:") y el `input` crea la caja blanca donde el usuario escribe.
3. **"Atributos clave"**:
   * `type="text"` crea una caja para texto normal.
   * `type="email"` exige que sea un correo válido.
   * `name` identifica los datos al enviarse.
   * `required` hace obligatorio llenar el campo.
4. **"El botón `<button type="submit">`"**: Al hacer clic, envía la información.