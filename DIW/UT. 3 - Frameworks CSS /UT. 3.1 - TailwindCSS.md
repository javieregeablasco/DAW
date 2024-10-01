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
  Tailwind incopora una paleta de colores que se puede consultar <a href="https://tailwindcss.com/docs/customizing-colors)">aquí</a>.  
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
>**:hover** — cuando el ratón está sobre el botón.  
>**:focus** — cuando el botón recibe foco.  
>**:active** — cuando el botón es presionado.  
>**:disabled** — cuando el botón está deshabilitado.  
>**:visited** — cuando un enlace ha sido visitado.  
>**:focus-visible** — cuando el foco es visible, según el contexto de uso.

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
>Definir el color de varios estados de un botón. Por ejemplo :hover y active.

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
>Añadir un borde de cualquier color y de cualquier grosor al elemento.>

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
