---
Título: UD. 3.1 - Frameworks - Tailwind CSS
Autor: Javier Egea Blasco
Año: 24-25
Palabras clave: DAW, DIW
---


# 1. Introducción: "Desarrollo Frontend con Tailwind CSS"

En el desarrollo web moderno, la creación de interfaces de usuario atractivas y funcionales es una de las tareas más desafiantes. En este contexto, **Tailwind CSS** ha emergido como una herramienta fundamental para facilitar y acelerar el proceso de diseño de frontend, permitiendo a los desarrolladores crear de manera eficiente páginas web estéticas y altamente personalizables.

**Tailwind CSS** es un framework de diseño basado en **clases utilitarias** que, a diferencia de otros frameworks como Bootstrap, no impone un diseño predefinido. En cambio, proporciona una serie de pequeñas clases reutilizables que permiten a los desarrolladores construir sus propias interfaces de manera modular y flexible. Estas clases abarcan una amplia gama de propiedades CSS lo que permite diseñar interfaces personalizadas **directamente desde el código HTML**.

El enfoque modular de **Tailwind CSS** no solo mejora la productividad, sino que también fomenta buenas prácticas de desarrollo, como el uso de código limpio y mantenible.

## Objetivos:
- Instalar y configurar **Tailwind CSS** en un proyecto web.
- Conocer las características y ventajas de **Tailwind CSS** en el desarrollo frontend.
- Aplicar clases utilitarias de Tailwind para diseñar elementos y componentes de interfaz.
- Crear diseños responsivos y accesibles usando **Tailwind CSS**.
- Optimizar el CSS del proyecto eliminando clases no utilizadas.

## Contenidos:
- Tailwind frente a otros frameworks de CSS.
- Instalación y configuración de **Tailwind CSS**.
- Uso de clases utilitarias: estructura y nomenclatura.
- Diseño responsivo con **Tailwind**.
- Buenas prácticas en la organización del código CSS.
- Personalización y optimización de Tailwind CSS en proyectos reales.

# 2. Tailwind frente a otros frameworks de CSS.
Existen muchos frameworks de CSS pero los desarrolladores suelen elegir el más rápido y fácil para aprender. Tailwind viene con muchas características y estilos incorporados a elegir y también se utiliza por su tendencia a reducir escribir código CSS. Tailwind CSS también crea pequeñas utilidades con un conjunto definido de opciones que permiten una fácil integración de clases existentes directamente en el código HTML.
<img src="https://media.geeksforgeeks.org/wp-content/uploads/20230710125344/Tailwind-css.webp" width=60%>

# 3. Instalación y configuración de **Tailwind CSS**.
Toda la información para la instalación y configuración de TailwindCSS en la página oficial.
<a href="https://tailwindcss.com/docs/installation">Haga click aquí</link>
## 3.1 - Uso con link CDN. 
Es ideal para prototipos, proyectos pequeños o experimentación. No se necesita una configuración compleja. Solo es necesario incluir una etiqueta `<link>` o una etiqueta `<script>` en la sección `<head>` del documento `HTML`. 
```
<script src=”https://cdn.tailwindcss.com”></script>
```
El uso de una CDN garantiza siempre estar usando la última versión disponible pero no se recomienda para producción.  

Ejemplo de proyecto listo para usar TailwindCSS
```
<!doctype html>
<html>
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <!-- añadimos el script -->
  <script src="https://cdn.tailwindcss.com"></script>
  <!-- ... -->
</head>
<body>
  <h1 class="text-3xl font-bold underline">
    Hello world!
  </h1>
</body>
</html>
```
## 3.2 - Instalación con Tailwind CLI. 
- **Instalar node.**
  
  Para comprobar si teneis instalado el node abrir un consola y teclear:
```
node -v
```
Si teneis node instalado os aparecerá la versión. De lo contrario, ir a la <a 
href="https://nodejs.org/en/download/prebuilt-installer">página de descarga de node</a> descargar e instalarlo.
- **Instalar tailwind.**
  
  Dentro de la carpeta donde tendremos nuestros proyectos, abrir una consola y escribir:
```
npm install -D tailwindcss
npx tailwindcss init
```
- **Configurar tailwind: Definir la carpeta de proyectos.**
  
  Tenemos que especificar en qué lugar tendremos nuestros archivos editando la línea `content: [],` del archivo 
  `tailwind.config.js` y reemplazandola por `content: ["./src/**/*.{html,js}"]`, donde `src`es el nombre de la carpeta elegida para nuestros proyectos.
- **Configurar tailwind: Añadir las directivas.**
  
  Para añadir las directivas para cada una de la capas de estilos de tailwind haremos lo siguiente.
  Dentro de la carpeta `src/` crear un archivo input.css' y añadirle:
```
@tailwind base;
@tailwind components;
@tailwind utilities;
```
- **Iniciar tailwind.**
  
  Para iniciar el escaneado de nuestros proyectos con tailwind usaremos de nuevo nuestras terminal y escribiendo:
  ```
  npx tailwindcss -i ./src/input.css -o ./src/output.css --watch
  ```
  **Nota:** No cerrar nunca la terminal mientras estemos trabajando con nuestros proyectos.
  
- **Empezar a usar tailwind.**
  
  Para poder empezar a usar las clases de tailtwind, añadir la ruta al archivo CSS compilado `output.css` al `<head>`de nuestro proyecto.
  El archivo quedará de la siguiente manera:
```
<!doctype html>
<html>
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link href="./output.css" rel="stylesheet">
</head>
<body>
  <h1 class="text-3xl font-bold underline">
    Hello world!
  </h1>
</body>
</html>
```

  **Nota 1:** Para poder usar todas las clases de tailwind, instalar el plugin `Tailwind CSS IntelliSense`. De lo contrario el código no se autocompletará al purgarse el archivo `output.css` continuamente.   
  
  **Nota 2:** Comprobar periodicamente que el `build process`esté ejecutándose.
  
# 4 - Clases utilitarias de Tailwind CSS.
## 4.1 - Colores
  Tailwind incopora una paleta de colores que se puede consultar <a href="https://tailwindcss.com/docs/customizing-colors">aquí</a>.  
- **Cambiar el color de texto:**

Por ejemplo escribir: 
```
 <h1 class="text-... "</h1>
```
Con la función de autocompletado, saldrán todos los colores que vienen por defecto.  

**Nota** Para evitar visualizar una lista interminable de atributos, poner la primera letra de la gama de colores que deseamos usar.
```
 <h1 class="text-g... "</h1>
```
- **Cambiar el color de fondo del texto:**

  De la misma manera que para el color del texto escribir `bg` (de background)...
```
<h1 class="text-green-300 bg...">Hola mundo</h1>
```
... y seleccionar el color escribiendo primero las primeras letras del color básico.    

- **Bordes, tipos de bordes y color de bordes.**  
  Usar `border` y consultar <a href="https://tailwindcss.com/docs/border-radius">la documentación</a> para encontrar los estilos que más convienen al proyecto.
  
  Por ejemplo:
  ```
  <h1 class="border-green-500 rounded-lg border-4">Hola mundo</h1>
  ```
- **Customización de colores.**

  A diferencia de `bootstrap` dónde la customización puede resultar algo tiedosa, crear colores (estilos) propios en tailwind es relativamente simple.
  Podemos difinir un color personalizado escribiendo:
  ```
  <h1 class="text-[
  ```
  Luego introducir el color en hexadecimal (por ejemplo `#d2d289`).
  Al final el código quedará como sigue: 
  ```
  <h1 class="text-[#d2d255]">Hola mundo</h1>
  ```
  Otra manera de customizar los colores es editar el archivo de configuración `tailwind.config.js`.
  
  Para añadir los 3 colores personalizados siguientes...
  ```
    - verde-caqui #363112
    - azul-petroleo #1b4a50
    - azul-electrico #242c6b
  ```    
  ... añadiremos al archivo de configuración los nuevos colores segun el formato clave, valor.  
      
  El archivo de configuración quedará de la siguiente manera:
  
  ```
  /** @type {import('tailwindcss').Config} */
  module.exports = {
    content: ["./src/**/*.{html,js,json}"],
    theme: {
      extend: {
        colors: {
          'verde-caqui': '#363112',
          'azul-petroleo': '#1b4a50',
          'azul-electrico': '#242c6b',
        }
      },
    },
    plugins: [],
  }
  
>**Actividad**  
>1. Añadir varios colores personalizados.  
>2. Añadir varias etiquetas y aplicar los nuevos colores a esas etiquetas (color de letra, fondo, ...).  
>3. Comprobar si los nuevos estilos se han añadido al archivo `output.css`
>4. Pasar el ratón sobre el color personaliza con código hexadecimal y elegir otro color.
>5. Quitar las comillas a 'verde-caqui', 'azul-petroleo' y 'azul-electrico' y adaptar el código para que no se generen errores.

### 4.1.1 - Colores de botones.
Los botones tienen varios estados y habitualmente el color de esos estados se realiza con pseudo clases.
>**Principales estados de los botones**  
>**hover:** — cuando el ratón está sobre el botón.  
>**focus:** — cuando el botón recibe foco.  
>**active:** — cuando el botón es presionado.  
>**disabled:** — cuando el botón está deshabilitado.  
>**visited:** — cuando un enlace ha sido visitado.  
>**focus-visible:** — cuando el foco es visible, según el contexto de uso.

Ahora vamos a ver como se definen esos estados en tailwind, para ello empezaremos declarando un color con el siguiente código:
```
<button class="bg-blue-950 text-white p-4 rounded-full">Pinchar aquí</button>
```
Si queremos centrar el botón añadiremos un `margin-auto` y `block`.
Si queremos separar el boton de los otros elementos añadiremos un `margin` de 6.

El código del botón quedará de la siguiente manera:
```
<button class="bg-blue-950 text-white p-4 rounded-full mx-auto block w-40 my-6">Pinchar aquí</button>
```

Para definir el color de los diferentes estados, simplemente empezar a escribir el estado y dejar que el código se autocomplete.
>**Actividad**  
>Definir el color de varios estados de un botón. Por ejemplo hover: y active:.

### 4.1.2 - Trabajando con gradientes.
Toda la información sobre gradientes disponible en la <a href="https://tailwindcss.com/docs/gradient-color-stops#basic-usage)">página oficial de Tailwind</a>.

#### 4.1.2.1 - Gradiente de 2 colores:
Para definir el color inicial de un fondo usar `bg-gradient-to-r from-...`  
Para definir el color final de un fondo usar `bg-gradient-to-r from-cyan500 to-...`  
**Ejemplo:**
```
<h1 class="bg-gradient-to-r from-blue-200 to to-blue-900 w-60 mx-auto block my-6">Mi primer gradiente</h1>
```
>**Actividad**  
>Añadir un borde de cualquier color y de cualquier grosor al elemento.

#### 4.1.2.2 - Gradiente de 3 colores:
Lo mismo que para 2 colores pero esta vez tendremos que definir el color intermedio con `via-*`. 
>**Actividad**  
>Crear un un nuevo elemento crear un gradiente de 3 colores.

#### 4.1.2.3 - Gradiente sobre textos:
Para realizar gradientes de colores aplicados sobre texto poder usar el siguiente código:  
```
<!-- gradiente de texto -->   
  <div class="text-3xl font-extrabold text-center" >
    <div class="bg-gradient-to-r from-blue-200 to to-blue-900 bg-clip-text text-transparent">Mi primer gradiente sobre texto</div>
  </div>
```
En este caso usamos la función de recortar el fondo según el texto (clip background) `bg-clip-text`y para poder visualizarlo haremos que el texto sea transparente con `text-transparent`. 

## 4.2 - Particularidades del archivo tailwind.config.js
Hemos visto que podemos añadir estilos nuevos declarándolos en el archivo ´tailwind.config.js´  
De momento, nos hemos limitado a añadir los nuevos estilos **dentro** de la carpeta `extend.`  
Pero, ¿qué ocurre si en vez de añadir los estilos en `extend` los hacemos directamente dentro de `theme`?
>**Actividad**  
>Desplazar los nuevos estilos de colores creados anteriormente y analizar los resultados.
El resultado debería ser similar a este:
```
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: ["./src/**/*.{html,js,json}"],
  theme: {
    
    colors: {
      verdecaqui: '#363112',
      azulpetroleo: '#1b4a50',
      azulelectrico: '#242c6b',
    },
    
    extend: {
    },
  },
  plugins: [],
}
```
## 4.3 - Fuentes de caracteres.
Toda la información sobre este apartado <a href="https://tailwindcss.com/docs/font-family">aquí</a>
### 4.3.1 - Tamaño de fuentes.
Si escribimos el código siguiente y lo pintamos en pantalla veremos que Tailwind no respeta el tamaño nativo de la etiquetas HTML.
```
<body>
    <h1>Texto en tamaño h1</h1>
    <h3>Texto en tamaño h3</h3>
    <h5>Texto en tamaño h5</h5>
    <p>Esto es un párrafo</p>
</body>
```
Si consultamos la documentación de tailwind vemos que la forma de cambiar el tamaño de fuente se realiza con la propiedad `text-*`
>Actividad
>Cambiar el tamaño de fuente de las etiquetas h1, h2, h3 y p de forma coherente.
>Sobreescribir los estilos **text-xs**, **text-sm** y **text-base** para obtener unos tamaños de fuente 13, 15 y 17px respectivamente.
>Añadir al documento 3 párrafos junto a los anteriores para ver la diferencia.

### 4.3.2 - Fuentes de caracteres.
En el framework de CSS Tailwind, vienen definidas 5 fuentes de caracteres principales

1. **sans**: Utiliza una fuente sans-serif, que incluye las fuentes del sistema.
2. **serif**: Una fuente con serifas, generalmente Times New Roman o similares.
3. **mono**: Una fuente monoespaciada, comúnmente utilizada para código, como Menlo, Consolas o monospace.

para incorporarlas a nuestros elementos escribiremos `font-**`

>**Actividad**
>1. Definir 2 elementos h1, h2.
>2. Personalizarlos con 2 tipos de fuentes y tamaños de fuentes distintos.
>3. Realizar la modificaciones necesarios para que, **al pasar el ratón por encima del texto** cambie el tipo de fuente así como su tamaño.

### 4.3.3 - Fuentes de caracteres personalizadas.
Para usar fuentes de carácteres personalizadas (para el ejmplo usaremos **roboto**, podemos hacer lo siguiente:
1. Importar la fuente desde Google Fonts en el archivo input.css
2. Configurar la fuente en tailwind.config.js.
3. Usar la clase personalizada.

**input.css** quedará de la  siguiente manera:
```
/*
@tailwind base;
@tailwind components;
@tailwind utilities;
*/
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap');

@import 'tailwindcss/base';
@import 'tailwindcss/components';
@import 'tailwindcss/utilities';
```

**tailwind.config.js** 
```
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: ["./src/**/*.{html,js,json}"],
  theme: {
    extend: {
      fontFamily: {
        roboto: ['Roboto'],
      },
    },
  },
  plugins: [],
}
```

>**Actividad**
>1. Importar 2 fuentes de caracteres. Una de las cuales será **Rubik Dirt**. 
>2. Definir 2 párrafos con las fuentes importadas.

### 4.3.4 - Estilos de fuentes de caracteres.
Para definir los estilos de las fuentes, negrita subrayado, cursiva, ... consultar la documentación oficial.

>**Actividad**
>1. Generar un párrafo de texto con loremipsum
>2. Poner en negrita 1 palabra del texto.
>3. Poner en cursiva toda una frase del párrrafo.

### 4.3.5 - Ejercicio.
>**Crear un HTML que haga lo siguiente:**  
>1. Dibujar el texto ´Fuente Roboto´ con la fuente Roboto y como fondo un color personalizado.
>2. Dibujar el texto ´Fuente Rubik Dirt´ con la fuente Rubik-Dirt y como fondo otro color personalizado.
>3. Al pasar el ratón por encima del primer texto, la etiqueta copiará los estilos de la segunda etiqueta.
>4. Al pasar el ratón por encima del segundo texto, la etiqueta copiará los estilos de la primera etiqueta.
>
>**Nota:** Podéis usar `javascript` o crear un pseudo elemento com `::after`.   

**Solución:**  

* **Archivo input.css**
```
/*
@tailwind base;
@tailwind components;
@tailwind utilities;
*/
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Rubik+Dirt&display=swap');


@import 'tailwindcss/base';
@import 'tailwindcss/components';
@import 'tailwindcss/utilities';
```
* **Archivo tailwind.confij.js.css**
```
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: ["./src/**/*.{html,js,json}"],
  theme: {
    
    extend: {
      
      fontFamily: {
        roboto: ['Roboto'],
        'rubik-dirt': ['Rubik Dirt']
      },

      colors: {
        verdecaqui: '#363112',
        azulpetroleo: '#1b4a50',
        azulelectrico: '#242c6b',
      },
            
    },
  },
  plugins: [],
}
```
* **Archivo index.html**
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link href="./output.css" rel="stylesheet">
    <title>Document</title>
</head>

<style>
  h5::after {
    content:'Fuente Roboto';
  }
  h5:hover::after{
    content:'Fuente Rubik Dirt';
  } 

  p::after {
    content:'Fuente Rubik Dirt';
  }
  p:hover::after{
    content:'Fuente Roboto';
  } 
</style>

<body>
    <h5 class="m-4 font-roboto text-3xl hover:font-rubik-dirt hover:w-72 hover:bg-azulpetroleo bg-verdecaqui w-52 h-20 text-yellow-400"></h5>
    <p class=" m-4 font-rubik-dirt text-3xl hover:font-roboto hover:w-52 hover:bg-verdecaqui bg-azulpetroleo text-yellow-300 w-72 h-20"></p>
</body>
</html>
```

## 4.4 - Espacios: border, margin & padding
### 4.4.1 - Border.
Permite definir todas las propiedades del borde.  
Toda la información sobre bordes <a href="https://tailwindcss.com/docs/border-radius">aquí</a>.

Para definir el borde, su ancho, el radio etc... iremos añadiendo propiedades. 

>**Ejemplo** donde tenemos:
>1. Un border: border-width de 4px
>2. Un color de borde: border-yellow-500
>3. Un radio de 8px solo en esquinas inferiores: rounded-b-lg
```
<h3 class="bg-green-950 text-white border-yellow-500 rounded-b-lg border-4  text-center">Definiendo border</h3>
```
>**Actividad**
>Generar un párrafo de texto con loremipsum que tenga el borde siguiente:
>1. Borde de tamaño 8px.
>2. Redondeado de 6px solo en la esquinas superiores. 

### 4.4.2 - Margin.
Permite definir los margenes de un elemento.
Toda la información sobre margenes <a href="https://tailwindcss.com/docs/margin#add-margin-to-a-single-side">aquí</a>.

>**Ejemplo** donde tenemos un margin de 1px
```
<h3 class="bg-yellow-950 text-white border-blue-400 border-4 text-center m-1">Definiendo margin</h3>
```

### 4.4.3 - Padding.
Permite definir los margenes **dentro** de un elemento.
Toda la información sobre padding <a href="https://tailwindcss.com/docs/padding">aquí</a>.

>**Ejemplo** donde tenemos un padding **superior e inferior** de 8px.
```
<h3 class="bg-green-950 text-white border-yellow-500 border-4  text-center w-64 h-20">Definiendo dimensiones de elementos</h3>
```

### 4.4.4 - Space between
Se utiliza en sistemas de diseño con **Flexbox** o **Grid** para distribuir automáticamente el espacio entre **los elementos hijos** dentro de un contenedor.
Toda la información sobre padding <a href="https://tailwindcss.com/docs/space">aquí</a>.

**Space Between** proporciona utilidades como `space-x-{0,1, n}` o `space-y-{0,1, n}` para agregar espacio horizontal o vertical entre **los elementos secundarios** de un **contenedor flex o grid**.

>**Ejemplo**: `space-x-4` añade un margen entre los elementos hijos de 1rem  o 4px en el eje horizontal.
>En este caso, solo habrá espacio **entre los elementos**, y no alrededor de los elementos o entre elementos y el borde del contenedor.
```
html
<div class="flex space-x-4">
  <div>Item 1</div>
  <div>Item 2</div>
  <div>Item 3</div>
</div>
```

## 4.5 - Medidas de los elementos.
Permite definir las medidas (ancho y alto) de los diferentes elementos.  

Toda la información sobre medidas (sizing) <a href="https://tailwindcss.com/docs/witdh">aquí</a>.

>**Ejemplo** donde tenemos un ancho de elemanto de 64px.
```
 <h3 class="bg-green-950 text-white border-yellow-500 rounded-b-lg border-4  text-center w-64 flex justify-center">Definiendo dimensiones de elementos</h3>
```
<br></br>    
## 4.6 - Tarea.
>**Actividad**: Crear una tarjeta de presentación para familiarizarse con las clases de Tailwind CSS márgenes, padding, colores, etc.
> 
>1. **Estructura de la tarjeta**:
>    - La tarjeta es un contenedor `div` con fondo blanco, bordes redondeados y sombra (clases `bg-white`, `rounded-lg`, `shadow-lg`).
>    - La imagen de perfil tiene bordes redondeados (`rounded-full`) y un borde azul alrededor (`border-4 border-blue-500`).
>    - Enlace de la foto: https://secure.gravatar.com/avatar/34147b9eecf59779b777eb68a1805113.jpg?s=600&d=mm
>    - El ancho de la tarjeta será de 96px (`w-96`).
>    - El fondo es de color gris (`bg-gray-200`).
>   
>2. **Márgenes y Padding de la tarjeta**:
>    - La tarjeta tiene `m-4` para margen externo.
>    - Se usa `p-6` para el padding interno de la tarjeta y `px-4 py-2` para los botones.
>   
>3. **Colores y estilos de texto y botones**:
>    - Color de fondo para el botón principal `bg-blue-500`, y para el botón secundario `bg-gray-300`.
>    - Los textos tienen colores personalizados `text-gray-800` y `text-gray-600`.
>
>4. **Bordes redondeados**:
>    - La tarjeta tiene bordes redondeados con `rounded-lg` y los botones con `rounded-full`.
>  
>   **Nota:** Para que los botones queden alineados y centrados usar  <div class= ... flex justify-center space-x-4">
>
> Veremos `flex` más adelante y `space-x-4` es la separación entre elementos (botones).
<br></br>  
**El resultado de la actividad se puede ver a continuación:**  

<img src="https://drive.google.com/uc?export=view&id=1m1wSxtPtQeUBjaWEXlZfpClbbKP_9UXC" width=40%>

# 5 - Clases personalizadas
Para crear clases personalizadas y evitar de estar reescribiendo el mismo código para definir estilos que se repinen a lo largo del documento HTML, se puede utilizar **la capa de componentes**.
Por convención, esas clases tendrán como nombres `card, btn, badge`.
**Nota:**
Aunque crear clases personalizadas se puede interpretar como una simplifcación del código HTML para darle más claridad, esa práctica añade una capa de abstracción que contraviene el espíritu **utility first** de tailwind... 
## 5.1 - Creación de clases personalizadas: @layer components
**Ejemplo:**
Archivo `import.css`:
```
@import 'tailwindcss/base';
@import 'tailwindcss/components';
@import 'tailwindcss/utilities';

@layer components {
  .btn {
    background-color: theme('colors.white');
    border-radius: theme('borderRadius.lg');
    padding: theme('spacing.6');
    box-shadow: theme('boxShadow.xl');
  }
  /* ... */
}
```
 ## 5.2 - Reutilización de clases personalizadas: @apply
Si deseamos ampliar una clase personalizada sin modificarla, usaremos la directiva @apply.
**Ejemplo**
```
@layer components {
  .btn-1 {
    @apply btn;
      rounded-b-lg shadow-md;
  }
}
```
## 5.3 - Actividad #1 - Creación de un componente de personalizado.  
1. Crea una clase personalizada llamada `card`.
2. Utiliza las siguientes propiedades de tailwind:
  - background-color: gray.100
  - border-radius: md
  - padding: 6
  - box-shadow: lg  
3. Utiliza en el HTML a continuación la clase card.
```
<div>
  <h2">Tarjeta 1</h2>
  <p>Esta es la tarjeta personalizada.</p>
</div>
```
## 5.4 - Actividad #2 - Creación de un botón.
1. Define una clase personalizada `btn` que utilice `@layer components` para definir los estilos de un botón básico.
2. Utiliza las siguientes propiedades para definir la clase `btn`:
  - background-color: gray.200
  - border-radius: lg
  - padding: 4
  - box-shadow: md
3. Define una clase `btn-primary` que extienda la clase `btn`con la directiva `@apply`.
4. La clase `btn-primary` añade estilos adicionales:
  - Estado primary: background-color: blue 500 y color de texto white.
  - Estado hover: background-color: blue 900
6. Utiliza las clases `btn` y `btn-primary` en el archivo HTML dado a continuación.

```
<button>
  Botón Secundario
</button>

<button>
  Botón Primario
</button>
```

# 6 - Responsive design.
El **responsive design** (diseño responsivo) es un enfoque en el desarrollo web que busca crear páginas que se adapten de manera óptima a diferentes tamaños de pantalla y dispositivos.
Toda la información sobre las herramientas de responsive design de Tailwind <a href="https://tailwindcss.com/docs/responsive-design">aquí</a>. 

En Tailwind disponemos, por defecto, de los siguientes `break points`. 
| Breakpoint prefix | Minimum width | CSS                                      |
|-------------------|---------------|------------------------------------------|
| sm                | 640px        | `@media (min-width: 640px) { ... }`    |
| md                | 768px        | `@media (min-width: 768px) { ... }`    |
| lg                | 1024px       | `@media (min-width: 1024px) { ... }`   |
| xl                | 1280px       | `@media (min-width: 1280px) { ... }`   |
| 2xl               | 1536px       | `@media (min-width: 1536px) { ... }`   |

## 6.1 - Responsive design con los breakpoints de Tailwind.
Para incorporarlos a nuestras etiquetas bastará con escribir el nombre del breakpoint.  

**Ejemplo:**  
`Sin breakpoints:` 
```
<body class="bg-gray-300">
  <div class="border-2 border-rose-700 p-6 w-1/4 mx-auto rounded-md mt-10">
    <h1 class="text-xl font-mono font-bold text-center text-blue-800">Mi primer diseño responsivo.</h1>
    <p class="mt-4 text-center text-sm text-green-800">Contenido del párrafo con las explicaciones de la funcionalidad.</p>  
  </div>
</body>
```
`Con breakpoints:`

```
<body class="bg-gray-300">
  <div class="border-2 border-rose-700 p-6 w-1/4 mx-auto rounded-md mt-10 bg-indigo-300 xl:bg-cyan-200 md:bg-cyan-800">
    <h1 class="text-xl font-mono font-bold text-center text-blue-800 md:text-cyan-100 xl:text-gray-900">Mi primer diseño responsivo.</h1>
    <p class="mt-4 text-center text-sm text-green-800 md:text-yellow-400 xl:text-green-900">Contenido del párrafo con las explicaciones de la funcionalidad.</p>  
  </div>
</body>
```

## 6.2 - Responsive design con breakpoints customizados.
Para definir los nuevos breakpoint iremos al archivo `railwind.config.js`y lo editaremos.

Por ejemplo para **añadir** un punto personalizado en 850px lo definiremos por clave-valor dentro de `theme` y luego `extend`.  
El archivo de configuración quedará de la siguiente manera. 
```
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: ["./src/**/*.{html,js,json}"],
  theme: {
    extend: {
      screens:{
        puntonuevo: '1000px',
      }
    },
  },
  plugins: [],
}
```

Para el ejemplo, al superar el `viewport` la resolución de 1000px, el fondo cambiará a amarillo, el texto del texo de `h1` a gris oscuro y el texto de `p` no se pintará en pantalla. 
```
<body class="bg-gray-300">
  <div class="border-2 border-rose-700 p-6 w-1/4 mx-auto rounded-md mt-10 bg-indigo-300 xl:bg-cyan-200 md:bg-cyan-800 puntonuevo:bg-yellow-400">
    <h1 class="text-xl font-mono font-bold text-center text-blue-800 md:text-cyan-100 xl:text-gray-900 puntonuevo:text-blue-950">Mi primer diseño responsivo.</h1>
    <p class="mt-4 text-center text-sm text-green-800 md:text-yellow-400 xl:text-green-900 puntonuevo:text-transparent">Contenido del párrafo con las explicaciones de la funcionalidad.</p>  
  </div>
</body>
``` 
## 6.3 - Ejercicio.
1. Crear un componente que muestre un título y un párrafo que cambie de color y tamaño según el tamaño de la pantalla.
2. Utilizar al menos tres breakpoints diferentes para modificar los estilos del texto y el contenedor.
3. Crear un breakpoint personalizado x2l: '1200px'

Contenido del HTML  
Título: Título Responsive  
Párrafo 1: Este párrafo con breakpoints.  
Párrafo 2: Este párrafo con breakpoint personalizado.  

# 7 - Flexbox.
Para activar el comportamiento de Flexbox en un contenedor, se utiliza la clase `flex` de Tailwind. 
Esto convierte al elemento en un contenedor flex, permitiendo que sus hijos sean distribuidos de acuerdo con las reglas de Flexbox.

Toda la información está disponible <a href="https://tailwindcss.com/docs/flex">aquí</a>
 
## 7.1 Contenedor Flex: flex
```
<div class="flex">
  <div>Elemento 1</div>
  <div>Elemento 2</div>
  <div>Elemento 3</div>
</div>
```

## 7.2 Dirección de los elementos: flex-direction
Tailwind ofrece varias clases para definir la dirección de los elementos dentro de un contenedor flex.

- `flex-row`: Elementos alineados en fila.
- `flex-col`: Elementos alineados en columna.

```
<div class="flex flex-row">
  <div>Elemento 1</div>
  <div>Elemento 2</div>
  <div>Elemento 3</div>
</div>
```

## 7.3 Justificación de contenido: justify-content
Permite controlar cómo se distribuye el espacio entre los elementos a lo largo del eje principal.

- `justify-start`: Los elementos se alinean al inicio.
- `justify-center`: Los elementos se centran.
- `justify-end`: Los elementos se alinean al final.
- `justify-between`: Espacio distribuido equitativamente entre los elementos.
- `justify-around`: Espacio distribuido alrededor de los elementos.

```
<div class="flex justify-center">
  <div>Elemento 1</div>
  <div>Elemento 2</div>
  <div>Elemento 3</div>
</div>
```

## 7.4 Alineación de elementos: align-items
Controla cómo se alinean los elementos a lo largo del eje transversal.

- `items-start`: Alinea los elementos al inicio.
- `items-center`: Alinea los elementos en el centro.
- `items-end`: Alinea los elementos al final.
- `items-stretch`: Los elementos se estiran para llenar el contenedor.

```
<div class="flex items-center">
  <div>Elemento 1</div>
  <div>Elemento 2</div>
  <div>Elemento 3</div>
</div>
```

## 7.5 Tamaño de los elementos: flex-grow, flex-shrink y flex-basis
- `grow`: Hace que un elemento crezca para ocupar el espacio disponible.
- `shrink`: Permite que los elementos se reduzcan en tamaño si es necesario.
- `basis`: Define el tamaño inicial de un elemento.

```
<div class="flex">
  <div class="flex-grow">Elemento 1 (crece)</div>
  <div>Elemento 2</div>
  <div>Elemento 3</div>
</div>
```

## 7.6 Envolver elementos: flex-wrap
Controla si los elementos dentro de un contenedor flex deben ser forzados a permanecer en una sola línea o pueden envolver a la siguiente línea.

- `flex-wrap`: Permite que los elementos se envuelvan en múltiples líneas.
- `flex-nowrap`: Fuerza a los elementos a estar en una sola línea.

```
<div class="flex flex-wrap">
  <div>Elemento 1</div>
  <div>Elemento 2</div>
  <div>Elemento 3</div>
</div>
```

## 7.7 Alineación del contenido del contenedor: align-content
Alinea el contenido de un contenedor flex en el eje transversal cuando hay espacio adicional.

- `content-start`, `content-center`, `content-end`, `content-between`, `content-around`.

```
<div class="flex flex-wrap content-center">
  <div>Elemento 1</div>
  <div>Elemento 2</div>
  <div>Elemento 3</div>
</div>
```
  
# 8 - Grid.
Para convertir un contenedor en un grid, se utiliza la clase `grid`. Esto permite organizar los elementos dentro de una cuadrícula.
Toda la información sobre las utilidades de grid de Tailwind <a href="https://tailwindcss.com/docs/grid-template-columns">aquí</a>.  

Algunas de las propiedades más importantes para definir y gestionar la estructura de un Grid son:
- grid: Define un contenedor como Grid.
- grid-cols-: Establece el número de columnas.
- grid-rows-: Establece el número de filas.
- gap-: Controla el espaciado entre las celdas del Grid.

**Ejemplo** 
Para activar el Grid, se utiliza la clase `grid`.
```
html
<div class="grid">
  <div>Elemento 1</div>
  <div>Elemento 2</div>
  <div>Elemento 3</div>
</div>
```

## 8.1 - Definir columnas: grid-cols
El número de columnas de una cuadrícula se define con `grid-cols-n`, donde `n` es el número de columnas.
**Ejemplos**
- `grid-cols-1`: Una columna.
- `grid-cols-2`: Dos columnas.
- `grid-cols-3`: Tres columnas, y así sucesivamente.

El HTML quedará de la siguiente manera.
```
<div class="grid grid-cols-3">
  <div>Elemento 1</div>
  <div>Elemento 2</div>
  <div>Elemento 3</div>
</div>
```

## 8.2 - Definir Filas: grid-rows
Se define el número de filas de una cuadrícula con clases como `grid-rows-n`, donde `n` es el número de columnas.

**Ejemplos**
- `grid-rows-1`: Una fila.
- `grid-rows-2`: Dos filas.

```
<div class="grid grid-rows-2">
  <div>Elemento 1</div>
  <div>Elemento 2</div>
  <div>Elemento 3</div>
</div>
```
## 8.3 - Diseño responsive con la clase grid.
Para obtener un **diseño responsive** podemos utilizar `grid-cols-1` a `grid-cols-12` (define de 1 a 12 columnas de un grid) conjutamente con los `breakpoints` vistos en el aprtado #6.
**Ejemplos**
- sm:grid-cols-2,
- md:grid-cols-4,
- etc.:
Con estos breakpoints, definiremos definiremos el número de columnas en función del tamaño del `viewport`, obteniendo un diseño responsive.

## 8.4  - Espaciado entre elementos: gap.
Tailwind permite definir el espaciado entre filas y columnas con la propiedad `gap`.

- `gap-{size}`: Define el espacio entre filas y columnas.
- `gap-x-{size}`: Espacio horizontal entre columnas.
- `gap-y-{size}`: Espacio vertical entre filas.

**Ejemplo**  
`gap-4` define un espacio uniforme de 1rem (16px).

```
<div class="grid grid-cols-3 gap-4">
  <div>Elemento 1</div>
  <div>Elemento 2</div>
  <div>Elemento 3</div>
</div>
```

## 8.5 - Alineación y Justificación de Contenido.
Los elementos dentro de un grid se pueden alinear con:

- **Justificar contenido horizontalmente justify-items**:
  - `justify-items-start`: Alinea los elementos al inicio de la celda.
  - `justify-items-center`: Centra los elementos dentro de la celda.
  - `justify-items-end`: Alinea los elementos al final de la celda.

- **Alinear contenido verticalmente items-start, items-center, items-end**:
  - `items-start`: Alinea los elementos al inicio.
  - `items-center`: Centra los elementos verticalmente.
  - `items-end`: Alinea los elementos al final.

**Ejemplo**
```
<div class="grid grid-cols-3 justify-items-center items-center">
  <div>Elemento 1</div>
  <div>Elemento 2</div>
  <div>Elemento 3</div>
</div>
```

## 8.6 - Tamaño de las columnas y de las filas.
El tamaño de las columnas y filas se define con `grid-col-[...]
- `grid-cols-[auto]`: El tamaño de la columna se ajusta automáticamente al contenido.
- `grid-cols-[fr]`: Asigna un tamaño flexible basado en la fracción disponible.
- `grid-cols-[100px]`: Especifica un tamaño fijo.
- `grid-cols-[10vw]`: Especifica un tamaño en función del viewport weight.
- ...

**Ejemplo**
```
<div class="grid grid-cols-[150px,2vw,1fr] gap-4 m-4">
  <div class="bg-slate-400 h-28 flex items-center justify-center">Elemento 1</div>
  <div class="bg-blue-400 flex items-center justify-center">Elemento 2</div>
  <div class="bg-red-400 flex items-center justify-center">Elemento 3</div>
</div>
```

## 8.7 - Amplitud de las celdas del grid.
### 8.7.1 - Amplitud de las celdas por columnas.
Para definir el ancho de las celdas por columnas usaremos `col-span-*`.  

**Ejemplo**
```
<div class="bg-gray-300 m-2 p-2 border-2 border-black rounded-xl">
  <div class="grid grid-cols-3 gap-4 m-1">
    <div class="bg-red-500 rounded-md flex justify-center items-center h-10">01</div>
    <div class="bg-red-500 rounded-md flex justify-center items-center h-10">02</div>
    <div class="bg-red-500 rounded-md flex justify-center items-center h-10">03</div>
    <div class="bg-red-900 rounded-md flex justify-center items-center h-10 col-span-2">04</div>
    <div class="bg-red-500 rounded-md flex justify-center items-center h-10">05</div>
    <div class="bg-red-500 rounded-md flex justify-center items-center h-10">06</div>
    <div class="bg-red-900 rounded-md flex justify-center items-center h-10 col-span-2">07</div>
    <div class="bg-red-900 rounded-md flex justify-center items-center h-10 col-span-3">08</div>
    <div class="bg-red-500 rounded-md flex justify-center items-center h-10">09</div>
    <div class="bg-red-500 rounded-md flex justify-center items-center h-10">10</div>
    <div class="bg-red-500 rounded-md flex justify-center items-center h-10">11</div>
  </div>
</html>
```

### 8.7.2 - Amplitud de las celdas por filas.
Para definir el ancho de las celdas por columnas usaremos `raw-span-`.

**Ejemplo**
```
<div class="bg-gray-300 m-2 p-2 border-2 border-black rounded-xl">
   <div class="grid grid-cols-3 gap-4 m-1">
     <div class="bg-red-500 rounded-md flex justify-center items-center h-10">01</div>
     <div class="bg-red-500 rounded-md flex justify-center items-center h-10">02</div>
     <div class="bg-red-500 rounded-md flex justify-center items-center h-10">03</div>
     <div class="bg-red-900 rounded-md flex justify-center items-center h-auto row-span-3">04</div>
     <div class="bg-red-500 rounded-md flex justify-center items-center h-10">05</div>
     <div class="bg-red-900 rounded-md flex justify-center items-center h-auto row-span-2">06</div>
     <div class="bg-red-500 rounded-md flex justify-center items-center h-10">07</div>
     <div class="bg-red-900 rounded-md flex justify-center items-center h-auto row-span-2">08</div>
     <div class="bg-red-500 rounded-md flex justify-center items-center h-10">09</div>
     <div class="bg-red-500 rounded-md flex justify-center items-center h-10">10</div>
     <div class="bg-red-500 rounded-md flex justify-center items-center h-10">11</div>
  </div>
</div>
```
### Actividades:
**Ejercicio 1**: Crear una cuadrícula de 3 columnas con un espacio uniforme de 16px entre los elementos.
**Ejercicio 2**: Crear una cuadrícula de 2 filas y 2 columnas, centrando los elementos tanto vertical como horizontalmente.
**Ejercicio 3**: Crear un layout responsivo que cambie de 1 columna a 2 y luego a 3 columnas en diferentes puntos de quiebre (`breakpoints`).

---



