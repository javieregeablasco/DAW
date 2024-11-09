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
Una de las características de Sass es la capacidad de anidar selectores CSS de una manera que refleja la estructura jerárquica del HTML. Eso hace que el código CSS sea más legible y fácil de organizar.

### 4.1 Sintaxis de Sass para los anidamientos de estilos.
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
  
### 4.2 Uso del selector padre `&`
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
  
### 4.3 Anidamiento con combinadores
El anidamiento puede incluir combinadores de selección como `>`, `+`, `~`, y un espacio (para descendientes). Esto permite especificar la relación entre los elementos de manera jerárquica.

**Ejemplo con combinadores.**
- `> p` selecciona los elementos `p` que son hijos directos de `div`.
- `p + ul` selecciona un `ul` que está inmediatamente después de un `p`.
- `p ~ div` selecciona todos los `div` que siguen a un `p` en el mismo nivel de jerarquía.
```
SCSS
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
```
CSS
div {
  background-color: lightblue;
}

div > p {
  font-weight: bold;
}

p + ul {
  margin-top: 10px;
}

p ~ div {
  border: 1px solid gray;
}
```

### 4.4. Buenas prácticas de Sass
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
  
### 4.5. Tarea RA3CEh
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


### 4.6 Uso de la propiedad `@import`
La directiva **@import** se utiliza para importar **otras hojas de estilo dentro de la hoja de estilo principal**.  
Esto es útil para modularizar los estilos, organizarlos en diferentes archivos y mantener el código más limpio y manejable.

Desde `Sass 1.23.0`, el uso de `@import` está desaconsejado, se recomienda usar `@use` y `@forward`.
---------------------------------------------------------------------------------------------------------------
Modificar y aligerar principio
---------------------------------------------------------------------------------------------------------------
Las directivas **`@use`** y **`@forward`** son características de **Sass** (la versión más reciente de Sass, conocida como Sass 1.23.0 y superior). Estas directivas se introdujeron para mejorar la modularización y organización de los estilos, y para reemplazar la antigua directiva **`@import`**, que tenía varios problemas de rendimiento y mantenimiento. 

### 1. **`@use`**: Importación de módulos en Sass

La directiva **`@use`** permite importar y cargar un archivo Sass de manera más controlada y eficiente que la antigua directiva `@import`. La principal ventaja es que permite evitar la duplicación de reglas y mantiene el código más modular y organizado.

#### Sintaxis:
```scss
@use "path/to/module";
```

#### Características clave de `@use`:

- **Cargar un archivo solo una vez**: Con `@use`, un archivo Sass solo se carga una vez, incluso si se importa en múltiples archivos. Esto evita que las mismas reglas se apliquen varias veces en el mismo proyecto.
  
- **Variables, mixins y funciones**: Las variables, mixins y funciones de un archivo importado con `@use` son "namespaced" (es decir, agrupadas bajo el nombre del archivo), lo que ayuda a evitar conflictos de nombres. No se importan directamente al espacio global.

- **Naming (espacios de nombres)**: Cuando usas `@use`, las variables, mixins y funciones del archivo importado se agrupan bajo un prefijo que se deriva del nombre del archivo. Por ejemplo, si importas un archivo llamado `_colors.scss`, las variables dentro de este archivo estarán accesibles como `colors.$primary`, `colors.$secondary`, etc.

#### Ejemplo:

```scss
// _colors.scss
$primary: #ff5733;
$secondary: #333333;
```

```scss
// styles.scss
@use "colors";

body {
  background-color: colors.$primary;
}
```

En este ejemplo:
- **`colors.$primary`** hace referencia a la variable `$primary` en el archivo `_colors.scss`.
- **`@use`** asegura que el archivo `_colors.scss` se cargue solo una vez, incluso si se importa en varios lugares.

#### Alias:
Puedes usar un alias para un archivo importado con `@use` para hacer más cortos los nombres de las variables o mixins que estás usando.

```scss
@use "colors" as c;

body {
  background-color: c.$primary;
}
```

### 2. **`@forward`**: Reexportación de módulos

La directiva **`@forward`** se utiliza para **reenviar** todo o parte de un módulo (archivo Sass) a otros archivos. Esto permite que un archivo Sass se convierta en un "paso intermedio" que reexporta el contenido de otros archivos, lo que facilita la creación de bibliotecas o colecciones de módulos reutilizables.

#### Sintaxis:
```scss
@forward "path/to/module";
```

#### Características clave de `@forward`:

- **Reexportar módulos**: Con `@forward`, puedes reexportar todas o algunas partes de un módulo a otros archivos que lo necesiten, sin necesidad de hacer un `@use` de cada archivo individualmente.
  
- **Control de lo que se reexporta**: Puedes usar `@forward` con opciones para excluir o incluir ciertas variables, mixins o funciones. Esto permite encapsular mejor lo que quieres hacer disponible para otros módulos sin exponer todo el contenido.

#### Ejemplo:
```scss
// _colors.scss
$primary: #ff5733;
$secondary: #333333;
```

```scss
// _index.scss
@forward "colors";
```

```scss
// styles.scss
@use "index" as *;

body {
  background-color: $primary;  // Usando la variable reexportada
}
```

En este ejemplo:
- El archivo `_index.scss` reexporta el contenido de `_colors.scss`.
- El archivo `styles.scss` usa `@use "index"`, lo que le da acceso a las variables de `_colors.scss` sin necesidad de importarlas directamente.

#### Uso de `@forward` con selección:
Puedes usar `@forward` para reexportar solo algunas partes del archivo original:

```scss
// _colors.scss
$primary: #ff5733;
$secondary: #333333;
$tertiary: #ffffff;
```

```scss
// _index.scss
@forward "colors" with $primary, $secondary;
```

En este caso, el archivo `_index.scss` solo reexportará las variables `$primary` y `$secondary`, excluyendo `$tertiary`.

### Comparación de `@use` y `@forward`

- **`@use`** se utiliza cuando **importas un módulo** y deseas usar sus variables, mixins y funciones en tu archivo actual, pero manteniendo un espacio de nombres (namespace).
  
- **`@forward`** se utiliza para **reenviar un módulo a otros archivos**, permitiendo que esos archivos accedan a lo que tú decides reexportar de un módulo.

### Ventajas sobre `@import`:

1. **Evitar duplicación de código**: Tanto `@use` como `@forward` ayudan a evitar la duplicación de código, ya que Sass solo carga los archivos una vez, independientemente de cuántos archivos los importen.
   
2. **Modularidad y mantenimiento**: Estas directivas permiten un código más organizado y modular, mejorando la gestión de proyectos grandes.

3. **Nombres más claros y sin conflictos**: Al usar `@use`, las variables, mixins y funciones son agrupadas bajo un espacio de nombres, lo que evita posibles conflictos de nombres que podrían ocurrir con `@import`.

### Resumen:

- **`@use`**: Para importar un archivo Sass de manera controlada, evitando la duplicación de código y proporcionando un espacio de nombres para las variables y mixins.
- **`@forward`**: Para reexportar un archivo Sass a otros archivos, permitiendo que esos archivos accedan a su contenido de forma organizada.

Ambas directivas son fundamentales para trabajar de manera eficiente con Sass en proyectos grandes y permiten una gestión más limpia de los estilos.


---------------------------------------------------------------------------------------------------------------
Modificar y aligerar fin
---------------------------------------------------------------------------------------------------------------
























### 7. **Anidamiento de media queries**:

Puedes anidar las reglas de media queries dentro de las reglas para hacer que los estilos sean responsivos.

#### Ejemplo con media queries anidados:

```scss
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

**Explicación:**
- Dentro de `.container`, se anidan las media queries para cambiar el ancho del contenedor según el tamaño de la pantalla.


---------------------------------------------------------------- 
Recursos utilizados
----------------------------------------------------------------

https://www.chucksacademy.com/es/topic/css-preprocessors/variables-in-sass


https://www.youtube.com/watch?v=MOstrhqpIsI&list=PLjwdMgw5TTLWVp8WUGheSrGnmEWIMk9H6&index=2

Partials
Modules
Mixins
Inheritance
Operators>
<https://www.youtube.com/watch?v=MOstrhqpIsI&list=PLjwdMgw5TTLWVp8WUGheSrGnmEWIMk9H6&index=2>
<https://www.youtube.com/watch?v=_kqN4hl9bGc&list=PL4cUxeGkcC9jxJX7vojNVK-o8ubDZEcNb>
<https://www.youtube.com/playlist?list=PLhSj3UTs2_yVyMlZyW-NAbgjtgAgLBzFP>
https://www.w3schools.com/sass/sass_variables.php
