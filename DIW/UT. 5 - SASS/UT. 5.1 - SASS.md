---
Título: UD. 5.1 - SASS
Autor: Javier Egea Blasco
Año: 24-25
Palabras clave: DAW, DIW
---  

<div align="center">
</br>
<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/9/96/Sass_Logo_Color.svg/480px-Sass_Logo_Color.svg.png" width=25%>
</div>
 
# 1. Introducción
<a href="https://sass-lang.com/">SASS</a> (Syntactically Awesome Stylesheet) es un preprocesador de CSS utilizado para traducir un código de **hojas de estilo no estándar** a un código CSS estándar e interpretable por la mayoría de navegadores. Fue creado por Hampton Catlin en 2006 y más tarde extendido por Natalie Weizenbaum.    
La principal utilidad de SASS es la de hacer más simple la escritura del código CSS y brindar utilidades que CSS no ofrece.

**Ventajas de utilizar Sass**
En proyectos grandes, las hojas de estilo suelen ser complejas y difíciles de mantener. Un preprocesador emplea funcionalidades que no existen en CSS y que facilitan la escritura y organización del código. Estas funcionalidades incluyen entre otros, variables, anidación de selectores, herencia de estilos y mixins, lo que permite un desarrollo más estructurado y eficiente.  
- **Variables.**
  De manera similar a cualquier lenguaje de programación, las variables permiten guardar información y emplearlas cuándo sea necesario.
  
- **Anidación de selectores.**
Usar anidamiento en Sass permite escribir el código CSS con la misma estructura visual que el HTML. De este modo, se simplifica el uso de los selectores y se ofrece a los programadores un formato más visual y jerarquizado para seleccionar elementos anidados.

- **Mixins.**
Los mixins son grupos de código, algo comparable a una función en otro lenguaje de programación, y permiten reutilizar secciones íntegras de código.

- **Herencia de estilos.**  
Mediante las herencias, es posible unificar declaraciones de estilo y compartirlas entre diferentes selectores. Una de las particularidades de las herencias en SASS es que las declaraciones heredadas solo se procesan si se utilizan, lo que asegura que el CSS final no contenga estilos innecesarios.

# 2. Otros preprocesadores de CSS: SCSS  
**SCSS (Sassy CSS) es una extensión de la sintaxis de Sass** que se distingue por su sintaxis: **utiliza corchetes en lugar de identaciones**. SCSS se diseñó de tal manera que un archivo CSS3 válido también es un archivo SCSS válido.  
Los archivos SCSS se almacenan con la extensión .scss.  
**Nota:** Al ser actualmente la sintaxis de Sass preferida nos centraremos en esta. No obstante, a lo largo de la unidad se darán tanto ejemplos de sintaxis Sass como de SCSS. 


# 2. Instalación y uso de SASS.
## 2.1 Instalación
Instrucciones de <a href="https://sass-lang.com/install/">**instalación**</a> de Sass.  
## 2.2 Uso de Sass
De una manera que recuerda a **Tailwind** necesitaremos compilar el código Sass (estilos.scss) a (estilos.css).  
Para ello podremos hacerlo desde la `CLI` con `sass input.scss output.css` o automaticamente con un **supervidor** ejecutando el comando `sass --watch input.scss output.css`. 
## 2.3 Ejercicio
Crear una carpeta dentro de la cual crearéis un archivo *.scss con el siguiente contenido:
```
$font-stack: Helvetica, sans-serif;
$primary-color: #333;

body {
  font: 100% $font-stack;
  color: $primary-color;
}
```
Ejecutar el comando `sass --watch archivo.scss archivo.css` y comprobar que se han generado 2 archivos con extensiones ***.css** y ***.css.map**

## 2.4 Archivo *.css.map
El archivo `map.css` es un archivo de mapa de fuentes (source map). Los mapas de fuentes ayudan a depurar el código CSS compilado al permitir que las herramientas de desarrollo del navegador mapeen las reglas CSS generadas de vuelta a las líneas correspondientes en los archivos SASS/SCSS originales.

**Propósito de un archivo** `.map.css`
- **Depuración:** Facilita identificar en qué parte del archivo SASS/SCSS se originó un estilo específico cuando se inspecciona un elemento en el navegador.
- **Desarrollo:** Ayuda a mantener la relación entre el CSS compilado y el código fuente, lo que resulta útil cuando se trabajan en proyectos grandes y complejos.

**Funcionamiento.**
El archivo `.map.css` se enlaza al archivo CSS compilado. El navegador utiliza este archivo para mostrar las fuentes originales al depurar el CSS, lo que simplifica la localización y corrección de errores.  

## 2.5 Ejercicio
Crear un archivo `index.html` y asociarle la hoja de estilos *.css.
Renderizar el archivo y con la herramienta de desarollo y comprobar que los estilos del documento están vinculados al archivo.sass . 
Comprobar igualmente que en el archivo *.css aparece el siguiente comentario:
```
/*# sourceMappingURL=styles.css.map */
```
Esto indica al navegador dónde encontrar el archivo de mapa de fuentes para vincular el código CSS compilado al código SCSS original.

# 3. Variables
Las variables permiten almacenar información reutilizable, el nombre de la variable debe empezar con $ y deben ser declaradas antes de utilizarse.  
Sass permite almacenar diferentes tipos de datos en variables, incluyendo:

**Colores:**
- **SCSS**  
```
$background-color: #ff5733;
```
- **Sass**
```
$background-color: #ff5733
```
<br></br>
**Números:**  
```
$base-margin: 16px;
```
<br></br>
**Cadenas de texto:**  
- **SCSS**
```
$font-family: 'Arial', sans-serif;
```
- **Sass**
```
$font-family: 'Arial', sans-serif
```
<br></br>
**Booleans:**
```
$is-responsive: true;
```
<br></br>
**Listas:**
```
$breakpoints: 320px, 480px, 768px, 1024px;
```
<br></br>
**Maps (Mapas asociativos):**  
- **SCSS**
```
$theme-colors: (
  "primary": #007bff,
  "secondary": #6c757d,
  "success": #28a745
);
```
- **Sass**
```
$theme-colors: (
  "primary": #007bff,
  "secondary": #6c757d,
  "success": #28a745
)
```

## 3.1 Ejercicio parte 1
**Implementación de Temas Claro y Oscuro en Sass**
Implementar un sistema de temas claro y oscuro utilizando variables en Sass para definir colores de fondo y de texto, y aplicarlos al `body` según la clase asignada.

- **Instrucciones:**
    - Crear variables en Sass para los **colores** de **fondo** y de **texto** del tema claro y oscuro , p.e.: `bg-light` y `text-dark`, `#ffffff`. 
    - Aplicar las variables de color:
      - Definir los estilos de `body` usando la clase `.light-theme` para aplicar los colores correspondientes al tema claro.
      - Define los estilos de `body` usando la clase `.dark-theme` para aplicar los colores correspondientes al tema oscuro.

Con la ayuda del siguiente código, comprobar que los estilos se aplican correctamente.
```
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Variables</title>
  <link rel="stylesheet" href="Estilos.css">  
</head>
<body class="light-theme"> 

  <header>
    <h1>Ejercicio de variables en Sass</h1>
    <button id="toggle-theme">Cambiar a Tema Oscuro</button>
  </header>

  <main>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Nobis quis a atque facilis iste asperiores iure repudiandae modi, placeat ullam eos soluta laboriosam recusandae velit est optio consequatur quasi officiis!</p>
  </main>

  <footer>
    <p>Pie de página</p>
  </footer>

  <script>
    // Función para alternar temas
    const toggleButton = document.getElementById('toggle-theme');
    toggleButton.addEventListener('click', () => {
      document.body.classList.toggle('light-theme');
      document.body.classList.toggle('dark-theme');
      
      // Cambiar el texto del botón según el tema activo
      if (document.body.classList.contains('light-theme')) {
        toggleButton.textContent = 'Cambiar a Tema Oscuro';
      } else {
        toggleButton.textContent = 'Cambiar a Tema Claro';
      }
    });
  </script>

</body>
</html>
```  
  
## 3.2 Ejercicio parte 2
Continuaremos sobre la base del ejercicio anterior y explotaremos la reutilizabilidad de las variables de Sass.
1. Definir un color primario `primary-color`, `#ff5733`.
2. Aplicar ese color como color de fondo del `header` del archivo anterior.
3. Aplicar ese color al **borde superior** del `footer` (2px)   


## 4 Anidación de selectores.
En CSS, los selectores relacionados deben escribirse de manera explícita, lo que puede llevar a un código repetitivo y difícil de mantener. 
**Ejemplo de una hoja de estilos CSS**
```
/* Estilos para el panel */
.panel {
  background-color: #f4f4f4;
  padding: 20px;
  border-radius: 8px;
}

/* Estilos para el título del panel */
.panel .panel-title {
  font-size: 1.5rem;
  font-weight: bold;
  color: #333;
}

/* Estilos para el contenido del panel */
.panel .panel-content {
  margin-top: 10px;
  font-size: 1rem;
  color: #666;
}

/* Estilos para el pie del panel */
.panel .panel-footer {
  display: flex;
  justify-content: flex-end;
}

/* Estilos para los botones dentro del pie del panel */
.panel .panel-footer button {
  background-color: #007bff;
  color: white;
  border: none;
  padding: 10px 15px;
  cursor: pointer;
}

.panel .panel-footer button:hover {
  background-color: #0056b3;
}
```

Una de las características de Sass es la capacidad de anidar selectores CSS de una manera que refleja la estructura jerárquica del HTML. Eso hace que el código CSS sea más legible y fácil de organizar. 


https://www.chucksacademy.com/es/topic/css-preprocessors/variables-in-sass


https://www.youtube.com/watch?v=MOstrhqpIsI&list=PLjwdMgw5TTLWVp8WUGheSrGnmEWIMk9H6&index=2

<Variables
Nesting
Partials
Modules
Mixins
Inheritance
Operators>
<https://www.youtube.com/watch?v=MOstrhqpIsI&list=PLjwdMgw5TTLWVp8WUGheSrGnmEWIMk9H6&index=2>
<https://www.youtube.com/watch?v=_kqN4hl9bGc&list=PL4cUxeGkcC9jxJX7vojNVK-o8ubDZEcNb>
<https://www.youtube.com/playlist?list=PLhSj3UTs2_yVyMlZyW-NAbgjtgAgLBzFP>


https://www.w3schools.com/sass/sass_variables.php
