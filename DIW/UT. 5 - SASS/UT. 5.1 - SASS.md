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
 
# 1. Introducción: Preprocesador de estilos Sass
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

# 3. Frameworks compatibles con Sass
<a href="https://getbootstrap.com/">**Bootstrap**</a> es uno de los frameworks frontend más populares y utiliza SASS como preprocesador para sus estilos. Esto nos permite personalizar fácilmente los estilos de Bootstrap utilizando variables y funciones de SASS.

<a href="https://bulma.io/">**Bulma**</a> es otro framework CSS que utiliza SASS como preprocesador. Al igual que Bootstrap, nos permite personalizar fácilmente los estilos de Bulma con características avanzadas de SASS.

<a href="https://gulpjs.com/">**Gulp**</a> es una herramienta de automatización de tareas que puede integrarse fácilmente con SASS. Podemos usar Gulp para compilar automáticamente nuestros archivos SASS, minificar y combinar nuestros estilos, entre otras tareas útiles.



# 4. Instalación y uso de SASS.
## 4.1 Instalación
Instrucciones de <a href="https://sass-lang.com/install/">**instalación**</a> de Sass.  
## 4.2 Uso de Sass
De una manera que recuerda a **Tailwind** necesitaremos compilar el código Sass (estilos.scss) a (estilos.css).  
Para ello podremos hacerlo desde la `CLI` con `sass input.scss output.css` o automáticamente con un **supervidor** ejecutando el comando `sass --watch input.scss output.css`. 
## 4.3 Ejercicio
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

## 4.4 Archivo *.css.map
El archivo `map.css` es un archivo de mapa de fuentes (source map). Los mapas de fuentes ayudan a depurar el código CSS compilado al permitir que las herramientas de desarrollo del navegador mapeen las reglas CSS generadas de vuelta a las líneas correspondientes en los archivos SASS/SCSS originales.

**Propósito de un archivo** `.map.css`
- **Depuración:** Facilita identificar en qué parte del archivo SASS/SCSS se originó un estilo específico cuando se inspecciona un elemento en el navegador.
- **Desarrollo:** Ayuda a mantener la relación entre el CSS compilado y el código fuente, lo que resulta útil cuando se trabajan en proyectos grandes y complejos.

**Funcionamiento.**
El archivo `.map.css` se enlaza al archivo CSS compilado. El navegador utiliza este archivo para mostrar las fuentes originales al depurar el CSS, lo que simplifica la localización y corrección de errores.  

## 4.5 Ejercicio
Crear un archivo `index.html` y asociarle la hoja de estilos *.css.
Renderizar el archivo y comprobar que los estilos del documento están vinculados al archivo.scss . 
Comprobar igualmente que en el archivo *.css aparece el siguiente comentario:
```
/*# sourceMappingURL=styles.css.map */
```
Esto indica al navegador dónde encontrar el archivo de mapa de fuentes para vincular el código CSS compilado al código SCSS original.

# 5. Variables
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

## 5.1 Ejercicio parte 1
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
  <meta name="viewport" ="width=device-width, initial-scale=1.0">
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
        toggleButton.text = 'Cambiar a Tema Oscuro';
      } else {
        toggleButton.text = 'Cambiar a Tema Claro';
      }
    });
  </script>

</body>
</html>
```  
  
## 5.2 Ejercicio parte 2
Continuaremos sobre la base del ejercicio anterior y explotaremos la reutilizabilidad de las variables de Sass.
1. Definir un color primario `primary-color`, `#ff5733`.
2. Aplicar ese color como color de fondo del `header` del archivo anterior.
3. Aplicar ese color al **borde superior** del `footer` (2px)
   
## 5.3 Utilización, operaciones y funciones sobre variables
**Utilización de variables**  
Para utilizar una variable dentro de un selector usaremos la notacion `#{$variable}`.
```
$medium: 768px;

@media only screen and min-width: #{$medium} {
    .btn {
        background: $blue;
    }
}
```
**Operaciones sobre variables**  
También se pueden realizar operaciones matemáticas sobre variables. 
```
$padding: 20px;

.btn {
    padding: $padding / 2;
}
```
**Funciones sobre variables**  
Para terminar, también es posible utilizar funciones que podremas aplicar a nuestras variables.  
<a href="https://sass-lang.com/documentation/modules/">**Listado módulos Sass**</a>  
Para poder usar las funciones de los módulos, previamente deberemos importarlos con la directiva `@use`  
```
@use 'sass:color';

$primary: gray;

.btn {
    background: $primary;

    &:hover {
        background: darken($primary, 10);
    }
}
```
Ejemplo de función que permite extraer valores de una variable **mapa** (diccionario).
```
@use "sass:map";

$theme-colors: (
  "primary": #007bff,
  "secondary": #6c757d,
  "success": #28a745
);

.realizado {
    background-color: map-get($map: $theme-colors, $key: success);
}
```

# 6 Anidación de selectores
En CSS, los selectores relacionados deben escribirse de manera explícita, lo que puede llevar a un código repetitivo y difícil de mantener. 
Una de las características de Sass es la capacidad de anidar selectores CSS de una manera que refleja la estructura jerárquica del HTML. Eso hace que el código CSS sea más legible y fácil de organizar.

## 6.1 Sintaxis de Sass para los anidamientos de estilos
En Sass, el anidamiento **se realiza simplemente escribiendo las reglas dentro de otras reglas**.  
Esto refleja la jerarquía de los elementos HTML como lo podemos ver a continuación donde:
  1. `nav` contiene un `ul`
  2. `ul`contiene un `li`
  3. `li` contiene un `a`.

```scss
nav {
  background-color: #333;
  
  ul {
    list-style-type: none;
    
    li {
      display: inline-block;
      padding: 10px;
      
      a {
        color: white;
        text-decoration: none;
      }
    }
  }
}
```
  
## 6.2 Uso del selector padre `&`
El símbolo `&` (Ampersand) se utiliza para hacer referencia al selector padre en una regla anidada. Esto es útil para aplicar pseudo-clases, pseudo-elementos o variantes del selector.  
  
**Ejemplo con pseudo clases y pseudo-elementos**  
- `&:hover` Se refiere a button:hover. El botón cambia de color cuando está en hover.
- `&.active` Se refiere a button.active. Permite aplicar los estilos de la clase `active` a un botón.
- `&::after` Hace referencia a `a::after`. Crea un contenido después de clicar el enlace.
```
SCSS
button {
  background-color: #007bff;
  color: white;
  
  &:hover {
    background-color: #0056b3;
  }
  
  &.active {
    background-color: #28a745;
  }
}

a {
  color: blue;
  
  &:hover {
    color: darkblue;
  }
  
  &::after {
    content: ' (link)';
    font-style: italic;
  }
}
```
```
CSS
button {
  background-color: #007bff;
  color: white;
}

button:hover {
  background-color: #0056b3;
}

button.active {
  background-color: #28a745;
}

a {
  color: blue;
}

a:hover {
  color: darkblue;
}

a::after {
  content: ' (link)';
  font-style: italic;
}
```
  
## 6.3 Anidamiento con combinadores
El anidamiento puede incluir combinadores de selección como `>`, `+`, `~`, y un espacio (para descendientes). Esto permite especificar la relación entre los elementos de manera jerárquica.

**Ejemplo con combinadores.**
- `> p` selecciona los elementos `p` que son hijos directos de `div`.
- `p + ul` selecciona un `ul` que está inmediatamente después de un `p`.
- `p ~ div` selecciona todos los `div` que siguen a un `p` en el mismo nivel de jerarquía.
>Archivo.scss
```
div {
  background-color: lightblue;
  
  > p {
    font-weight: bold;
  }
  
  p + ul {
    margin-top: 10px;
  }
  
  p ~ div {
    border: 1px solid gray;
  }
}
```
>Archivo.css
```
div {
  background-color: lightblue;
}
div > p {
  font-weight: bold;
}
div p + ul {
  margin-top: 10px;
}
div p ~ div {
  border: 1px solid gray;
}

/*# sourceMappingURL=estilos.css.map */
```  

## 6.4 Anidamiento de media queries:
También se pueden anidar las reglas de media queries para hacer que los estilos sean responsivos.

**Ejemplo:**
```
.container {
  width: 100%;
  
  @media (min-width: 768px) {
    width: 80%;
  }

  @media (min-width: 1024px) {
    width: 60%;
  }
}
```

## 6.5 Buenas prácticas de Sass
Es recomendable no anidar demasiado profundamente, ya que puede hacer que el CSS sea difícil de mantener y puede generar reglas de estilo muy específicas difíciles de sobrescribir.  
  
**Ejemplo de anidamiento excesivo.**
```
.container {
  .section {
    .article {
      .title {
        font-size: 2rem;
      }
    }
  }
}
```
  
## 6.6 Tarea RA3CEh
Convertir la hoja de estilos siguiente a SCSS.
```
.panel {
  border: 1px solid #ddd;
  padding: 20px;
}
.panel .panel-header {
  background-color: #f5f5f5;
}
.panel .panel-header h2 {
  margin: 0;
  color: #333;
}
.panel .panel-body {
  margin-top: 20px;
}
.panel .panel-body p {
  color: #666;
}
.panel .panel-footer {
  background-color: #f5f5f5;
  text-align: right;
}
.panel .panel-footer button {
  background-color: #007bff;
  color: white;
}
.panel .panel-footer button:hover {
  background-color: #0056b3;
}
```


# 7 Directivas @import, @use y @forward  
La directiva **@import** se utiliza para importar **otras hojas de estilo dentro de la hoja de estilo principal**, lo que permite modularizar los estilos, organizarlos en diferentes archivos y mantener el código más limpio y manejable.  
Desde `Sass 1.23.0`, el uso de `@import` está desaconsejado, se recomienda usar `@use` y `@forward`.  
  
Las directivas **`@use`** y **`@forward`** son características de **Sass** (desde Sass 1.23.0) y reemplazanan la directiva **`@import`**. 

## 7.1 Importación de módulos con @use
**@use** permite importar y cargar un archivo Sass de manera más controlada y eficiente que la antigua `@import` permitiendo, entre otras, evitar la duplicación de reglas.
- **Sintaxis.**
```
@use "path/to/module";
```

- **Características de `@use`:**
    - **Carga el archivo solo una vez**, incluso si se importa en múltiples archivos.
    - **Las variables, mixins y funciones** importadas son "namespaced", es decir, agrupadas bajo el nombre del archivo, lo que ayuda a evitar conflictos de nombres.
    - **Naming (espacios de nombres)**: Cuando usamos `@use`, las variables, mixins y funciones del archivo importado se agrupan bajo un prefijo que se deriva del nombre del archivo. Por ejemplo, si importamos el archivo `_colors.scss`, las variables dentro de este archivo estarán accesibles como `colors.$primary`, `colors.$secondary`, etc.

**Ejemplo:**
- Archivo Estilos.scss
```
@use "./estilosAdicionales/_flex";

// tema claro
$bg-light: #ffffff;
$text-light: #000000;

// tema oscuro
$bg-dark: #333333;
$text-dark: #ffffff;

body.light-theme {
  background-color: $bg-light;
  color: $text-light;  
}

body.dark-theme {
  background-color: $bg-dark;
  color: $text-dark;
}

$primary-color: #ff5733;

header {
  background-color: $primary-color;
}

footer {
  border-top: 1px solid $primary-color;
}
```

- **Archivo _flex.scss**
```
#formulario {
    display: flex;
    flex-direction: column;
    align-items: center;               
}

input {
    width: 45vw;
    margin: 5px;
}

textarea {
    width: 45vw;
}

main {
    display: flex;
    flex-direction: column;
    align-items: center;
    border: 2px solid blue;     
    margin: 10px; 
    width: 60vw;      
}

body {
    display: flex;
    flex-direction: column;
    align-items: center;
}
```
- **Archivo index.html**
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
    <p>Utilización de la directiva @use para añadir estilos desde hoja de estilos adicional.</p>
    <form id="formulario" action="form">
      <label>Nombre</label>
      <input type="text">
      <label>Email</label>
      <input type="">
      <label>Mensaje</label>
      <input type="text">
      <textarea cols="10" rows="5"></textarea>
      <input type="submit" value="Enviar">
    </form>

  </main>

  <footer>
    <p>Pie de página</p>
  </footer>

  <script>
    // Función para alternar entre el tema claro y oscuro
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

## 7.2 Ejercicio 
Montar el ejemplo anterior y comprobar como el estilo de <`form`> se actualiza al usar la directiva @use.

**Nota:**  
En el ejemplo:
- Por convención se pone un `guión bajo` delante de la hoja de estilos a la que se hace referencia.
- El guión bajo indica que el archivo es **un archivo de estilos parcial**, es decir, un archivo que **no se compila directamente** en un archivo CSS independiente, sino que **se incluye y compila en otros archivos**.

## 7.3 Alias
Se puede usar un alias para un archivo importado con `@use` para hacer más cortos los nombres de las variables o mixins que estamos usando.

**Modificación del ejemplo anterior.**
- **Archivo _flex.scss**
```
#formulario {
    display: flex;
    flex-direction: column;
    align-items: center;               
}

input {
    width: 45vw;
    margin: 5px;
}

textarea {
    width: 45vw;
}

main {
    display: flex;
    flex-direction: column;
    align-items: center;
    border: 2px solid blue;     
    margin: 10px; 
    width: 60vw;      
}

body {
    display: flex;
    flex-direction: column;
    align-items: center;
}

// tema claro
$bg-light: #ffffff;
$text-light: #000000;

// tema oscuro
$bg-dark: #333333;
$text-dark: #ffffff;
```
- **Archivo Estilos.scss**
```
@use "./estilosAdicionales/_flex" as flex;

body.light-theme {
  background-color: flex.$bg-light;
  color: flex.$text-light;
}

body.dark-theme {
  background-color: flex.$bg-dark;
  color: flex.$text-dark;
}

$primary-color: #ff5733;

header {
  background-color: $primary-color;
}

footer {
  border-top: 1px solid $primary-color;
}
```
  
## 7.4 Reexportación de módulos con @forward 
La directiva `@forward` se utiliza para **reenviar** todo o parte de un módulo (archivo Sass) a otros archivos. Esto permite que un archivo Sass se convierta en un "paso intermedio" que reexporta el contenido de otros archivos, lo que facilita la creación de bibliotecas o colecciones de módulos reutilizables.
La directiva @forward, **solo sirve para reexportar variables, mixins, y funciones de un archivo a otro**, de forma que otros archivos puedan importar las funcionalidades desde un único punto central.

**Ejemplo.**
- **Archivo Estilos.scss**
```
@use "./estilosAdicionales/flex" as flex;

body.light-theme {
  background-color: flex.$bg-light;
  color: flex.$text-light;
}

body.dark-theme {
  background-color: flex.$bg-dark;
  color: flex.$text-dark;
}

$primary-color: #ff5733;

header {
  background-color: $primary-color;
}

footer {
  border-top: 1px solid $primary-color;
}
```
- **Archivo _variables.scss**
```
// _variables.scss
// Tema claro
$bg-light: #ffffff;
$text-light: #000000;

// Tema oscuro
$bg-dark: #000000;
$text-dark: #ffffff;
```
- **Archivo flex.scss**
```
@forward "../forwarded/variables"; 

#formulario {
    display: flex;
    flex-direction: column;
    align-items: center;
}

input {
    width: 45vw;
    margin: 5px;
}

textarea {
    width: 45vw;
}

main {
    display: flex;
    flex-direction: column;
    align-items: center;
    border: 2px solid blue;
    margin: 10px;
    width: 60vw;
}

body {
    display: flex;
    flex-direction: column;
    align-items: center;
}
```

## 7.5 Ejercicio
Montar el ejemplo anterior para entender mejor la directiva @forward.

**Nota:**
En el ejemplo:
- **@use**: Se utiliza para **importar un archivo Sass en otro** y poder utilizar sus variables, mixins y funciones.
- **@forward**: Se utiliza para **reexportar contenido de un archivo Sass a otro**. Sirve para crear puntos de acceso centralizados o módulos de estilo que otros archivos pueden importar.
- **@forward no carga el archivo** en sí, sino que expone su contenido para que otros archivos puedan usarlo al importar el archivo que contiene @forward.

**Características clave de `@forward`:**
- **Reexportar módulos**: `@forward` reexporta todas o algunas partes de un módulo a otros archivos que lo necesiten, **sin necesidad de hacer un `@use` de cada archivo individualmente**.
- **Control de lo que se reexporta**: Se puede usar `@forward` con selección para excluir o incluir ciertas variables, mixins o funciones.

**Ejemplo de `@forward` con control de lo que se reexporta:**
```
// _colors.scss
$primary: #ff5733;
$secondary: #333333;
$tertiary: #ffffff;
```
```
// _index.scss
@forward "colors" with $primary, $secondary;
```
En este caso, el archivo `_index.scss` solo reexportará las variables `$primary` y `$secondary`, excluyendo `$tertiary`.

## 7.6 Resumen de @use y @forward
- **`@use`**: Importa un archivo Sass de manera controlada, evitando la duplicación de código y proporcionando un espacio de nombres para las variables y mixins.
- **`@forward`**: Reexporta un archivo Sass a otros archivos, permitiendo que esos archivos accedan a su contenido de forma organizada.  
Ambas directivas son fundamentales para trabajar de manera eficiente con Sass en proyectos grandes y permiten una gestión más limpia de los estilos.

# 8. Mixins
## 8.1 Definición de un mixin.
Los **mixins** son bloques que agrupan estilos CSS que pueden ser utilizados y reutilizados en otros lugares del proyecto de una página web, lo que evita tener que reescribirlos cada vez que sea necesario emplearlos. Además, un **mixin** también puede recibir parámetros (como si fuera una función de un lenguaje de programación), los que permite obtener varias salidas (estilos CSS), personalizadas a las necesidades del proyecto.

## 8.2 Sintaxis de un mixin
Un *mixin* se define con la directiva `@mixin` seguida del nombre del mixin. Es una buena práctica emplear nombres descriptivos y claros.

```
// Definición del mixin
@mixin button-styles {
  padding: 10px 20px;
  border: none;
  border-radius: 4px;
  background-color: #3498db;
  color: #fff;
  cursor: pointer;

  &:hover {
    background-color: #2980b9;
  }
}
```

>**Ejercicio**
>Crear un archivo `*.scss` y compilarlo. Observar el contenido del archivo `*.css` generado.

## 8.3 Uso de un mixin
Para incluir un **mixin** en un selector, se utiliza la directiva `@include`.

```
.button {
  @include button-styles;
}
```
>**Ejercicio**
>Completar el archivo `*.scss` creado anteriormente, compilarlo y observar el contenido del archivo `*.css`.

## 8.4 Mixins con Parámetros
Los **mixins** pueden aceptar uno o más parámetros para permitir la personalización de los estilos. 

```
@mixin border-radius($radius) {
    -webkit-border-radius: $radius;
       -moz-border-radius: $radius;
            border-radius: $radius;
}

@mixin botonCompleto($radius, $fontSize, $color) {
    font-size: $fontSize;
    border-radius: $radius;
    color: $color;
}
  
#box {
    @include border-radius(12px);
}

.button {
    margin-top: 10px;
    @include border-radius(6px);    
}

.btn {
    margin-top: 10px;
    @include botonCompleto(6px,20px,blue);    
}
```
```
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Instanciar @mixin</title>
  <link rel="stylesheet" href="estilos.css">  
</head>
<body class="light-theme">

  <header>
    <h1>Ejercicio de declaración de mixins</h1>
    <button id="box">Click 1</button>
  </header>

  <main>
    <section>
      <button class="button">Mixin de 1 parametro</button>
    </section>
    <section>
      <button class="btn">Mixin de varios parametros</button>
    </section>    
  </main>

  <footer>
    <h1>Fin del ejercicio</h1>    
  </footer>
  
</body>
</html>
```

## 8.5 Mixins con Parámetros Predeterminados
También se pueden definir parámetros predeterminados, dado el caso de instanciar un mixin sin pasarle parte, o ningun valor. 

```
@mixin box-shadow($x: 0, $y: 0, $blur: 5px, $color: rgba(0, 0, 0, 0.3)) {
  box-shadow: $x $y $blur $color;
}

.card {
  @include box-shadow(2px, 2px);
}
```
>**Ejercicio**
>¿Cual será el *.css resultante del ejemplo anterior?

## 8.7 Directiva @content dentro de un @mixin
**@content** actúa como un marcador de posición dentro de un **@mixin**. Ese marcador será reemplazado por el código proporcionado al invocar el @mixin con @include. 
```
//definicion del mixin con la directica @content
@mixin card-style {
    padding: 20px;
    border: 1px solid #ccc;
    background-color: #f9f9f9;    
    @content; // Se insertará contenido aquí cuando se use el mixin
}
//invocar el mixin y pasarle codigo adicional
.container {
    @include card-style {
        color: #333; //código adicional
        font-size: 14px; //código adicional
    }
}
```

## 8.8 Ejercicio
- **Mixin de media queries**
**Parte 1**  
Escribe un código en SCSS que defina un `mixin` llamado `media-query`
Ese `mixin` permitirá aplicar diferentes estilos CSS basados en el dispositivo `$device` (phone o tablet). 
El `mixin` debe aceptar un parámetro que determine si se trata de un teléfono o una tableta y aplicar el `@content` correspondiente dentro de una consulta de medios (`@media`) con un ancho máximo de 900px o 1200px, respectivamente. 
En el caso de no pasar ningun parametro o pasarlo con errores el `@media` aplicado será de 1200px. 

**Parte 2**
Aplica este `mixin` en una clase llamada `.container` para que:  
- Cambie el color de fondo a azul cuando se visualice en un dispositivo con un ancho máximo de 600px (teléfono).
- Cambie el color de fondo a verde cuando se visualice en un dispositivo con un ancho máximo de 900px (tableta).
- Cambie el color de fondo a rojo en cualquier otra caso.
El código deberá utilizar `@include` para aplicar el `mixin` dentro de la clase `.container`.

## 8.9 Mixins anidados
El anidamiento de @mixins implica la inclusión de un @mixin dentro de otro. Esto permite construir estilos más modulares y mantener la estructura organizada.
```
@mixin flex-container {
    display: flex;
    justify-content: center;
    align-items: center;  
    @content;
  }
  
  @mixin flex-item($grow: 1) {
    flex-grow: $grow;
  }
  
  .container {
    @include flex-container {
      height: 100vh;
      .item {
        @include flex-item(2);
      }
    }
  }
```

## 8.10 Mixins globales
El término "mixin global" se refiere a un mixin que está disponible para ser usado en cualquier parte de un proyecto debido a su ubicación en un archivo compartido o común que es importado globalmente.  
Esta manera de proceder permite definir tantos archivos (módulos) como elementos tengamos (variables, funciones, mixins...).
Como hemos visto en <a href="https://github.com/javieregeablasco/DAW/blob/main/DIW/UT.%205%20-%20SASS/UT.%205.1%20-%20SASS.md#7-directivas-import-use-y-forward"># 7 Directivas @import, @use y @forward</a> , los mixins globales se importan o reexportan con la directiva @use y @forward respectivamente. 
>**Ejemplo:**  
>Archivo **_mixins.scss**  
```
@mixin borde-redondeado($radio: 5px) {
  border-radius: $radio;
}
```
>Archivo **estilos.scss**
```
@use 'mixins'; // Importa el archivo que contiene el mixin global

.caja {
  @include mixins.borde-redondeado(10px);
}
```
## 9 Condicionales y bucles 
### 9.1 Condicionales
Podemos crear estilos más eficientes y flexibles utilizando condiciones. Por ejemplo, si dos elementos tienen el mismo estilo, pero existe una condición que solo uno de ellos cumple, podremos diferenciarlos usando mixins condicionales.

Con la directiva **@if** definiremos diferentes condiciones de uso. Además del `@if` también es habitual usar **@else if <condición> o @else**.
```
@mixin button-style($type) {
  @if $type == "primary" {
    background-color: blue;
    color: white;
  } @else if $type == "secondary" {
    background-color: gray;
    color: black;
  } @else {
    background-color: white;
    color: black;
  }
}

.btn-1 {
  @include button-style("primary");
}

.btn-2 {
  @include button-style("secondary");
}

.btn-3 {
  @include button-style("tertiary");
}
```
### 9.2 Bucles (iteradores)
#### 9.2.1 Directiva @each  
La directiva @each se utiliza para iterar sobre listas y mapas en Sass. Es ideal para recorrer elementos y aplicar estilos de forma dinámica.
>**Ejemplo con listas:**
```
$colores: red, blue, green;

@each $color in $colores {
  .text-#{$color} {
    color: $color;
  }
}
```  
>**Ejemplo con mapas:**
```
$espaciados: (
  small: 4px,
  medium: 8px,
  large: 16px
);

@each $nombre, $valor in $espaciados {
  .margen-#{$nombre} {
    margin: $valor;
  }
}
```  
#### 9.2.2 Directiva @for  
se utiliza para ejecutar un bloque de código **un número específico de veces**.
```
$inicio: 1;
$final: 5;

@for $i from $inicio through $final {
    .columna-#{$i} {
      width: 100% / $i;
    }
  }
```  
#### 9.2.3 Directiva while**
La directiva @while ejecuta un bloque de código mientras una condición sea verdadera.
```
$i: 1;

@while $i < 4 {
  .borde-#{$i} {
    border-width: $i * 2px;
  }
  $i: $i + 1;
}
```

# 10. Herencia de selectores y clase %
## 10.1 Herencias , @extend
La directiva **@extend**, permite compartir (heredar) reglas CSS entre múltiples selectores manteniendo el enfoque **DRY** (Don't Repeat Yourself).  
```
// Selector a heredar
.placeholder {
  color: #ccc;
  font-size: 14px;
  font-style: italic;
}

// Selectores que heredan los estilos CSS
.input-placeholder {
  @extend .placeholder;
}

.textarea-placeholder {
  @extend .placeholder;
}
```
## 10.2 Ejercicio
Sobre el ejemplo anterior definir una clase `output-placeholder` con los siguientes estilos `color: green` y `font-size: 10px`.  
Esa clase, aparte de tener sus estilos propios, también heredará de la clase `placeholder`.  
Montar un archivo HTML, con al menos un elemento al que se le aplique `output-placeholder`, y comprobar qué estilos se le aplica y la estructura del archivo *.css compilado.   

## 10.3 Herencia de selectores anidados.
`@extend` también puede usarse en selectores anidados.  
>Archivo *.scss 
```
.card {
  border: 1px solid #ccc;
  padding: 10px;

  .card-header {
    font-size: 18px;
    font-weight: bold;
  }

  .card-body {
    font-size: 14px;
  }
}

.featured-card {
  @extend .card;
  
  .card-header {
    color: red;
  }

  .card-body {
    font-size: 16px;
  }
}
```
>Archivo *.css compilado.  
```
.card, .featured-card {
  border: 1px solid #ccc;
  padding: 10px;
}
.card .card-header, .featured-card .card-header {
  font-size: 18px;
  font-weight: bold;
}
.card .card-body, .featured-card .card-body {
  font-size: 14px;
}

.featured-card .card-header {
  color: red;
}
.featured-card .card-body {
  font-size: 16px;
}

/*# sourceMappingURL=estilos.css.map */
```

## 10.4 Limitaciones de @extend
Como ya hemos visto en los ejemplos anteriores, `@extend` tiene algunas limitaciones a tener en cuenta:  
1 - Puede generar selectores inesperadamente específicos o generales, complicando la administración de estilos.
2 - Los cambios en los selectores extendidos pueden afectar a varios elementos, lo que puede ser difícil de mantener en proyectos grandes.  
3 - Puede generar un CSS final más grande debido a la combinación de selectores.  

## 10.5 Clase %
La clase `%` también conocida como **placeholder (selector)** (selector de marcador de posición), se utiliza para definir un conjunto de reglas de estilo **que no se aplican directamente a ningún elemento** pero que pueden ser **extendidas mediante `@extend`**.  
La `clase %` es especialmente útil para compartir estilos entre selectores sin agregar clases extra al HTML ni generar CSS redundante.
Al no aplicarse directamente a ningún elemento, **no se compila** y así pues, no aparecerá en el *.css. 

>Archivo scss
```
// placeholder 
%estilosComunes {
  color: #333;
  font-size: 16px;
  padding: 10px;
  border:2px solid black;
  border-radius: 5px;

}
  
// Selectores que extienden el placeholder
.btn {
  @extend %estilosComunes;
  background-color: #007BFF;

  &:hover {
    background-color: green;
  }
}
  
.alert {
  @extend %estilosComunes;
  background-color: #FFC107;

  &:hover {
    background-color: red;

  }
}
```

>archivo css compilado
```
.alert, .btn {
  color: #333;
  font-size: 16px;
  padding: 10px;
  border: 2px solid black;
  border-radius: 5px;
}

.btn {
  background-color: #007BFF;
}
.btn:hover {
  background-color: green;
}

.alert {
  background-color: #FFC107;
}
.alert:hover {
  background-color: red;
}

/*# sourceMappingURL=estilos.css.map */
```
>Archivo HTML
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="estilos.css">
    <title>Placeholder</title>
</head>
<body>
    <main>
        <p>Ejemplo de placeholder</p>
        <section>
            <p>
                <a href="#" class="btn">Confirmar</a>
                <a href="#" class="alert">Eliminar</a>
            </p>
        </section>
    </main>
</body>
```

## 10.6 Beneficios de usar placeholders.
- **Reutilización de código**: Ayuda a evitar la duplicación de código al permitir que varios selectores compartan los mismos estilos.
- **Optimización**: No generan CSS por sí solos, solo generan estilos cuando se utilizan, lo que permite mantener la hoja de estilos más limpia.
- **Fácil mantenimiento**: Actualizar los estilos del placeholder actualiza automáticamente todos los selectores que lo extienden. 

# 11. Estructuración de proyectos con Sass y buenas prácticas
## 11.1 Estructuración
La estructuración de proyectos en Sass es clave para mantener el código organizado, legible y fácil de mantener.  
Sass proporciona convenciones de organización que ayudan a estructurar los proyectos de una manera coherente y ordenada.  
**Principios Básicos de Estructuración**.  
 - **Modularidad:**
   Dividir el código en módulos pequeños, especificos y reutilizables.
 - **Consistencia:**
   Definir y mantener una convención de nombres y estructura de archivos coherente a lo largo del proyecto.
 - **Separación lógica de elemetos:**  
   Definir y mantener la separación lógica entre diferentes tipos de estilos, variables, mixins, componentes...

## 11.2 Buenas prácticas

