---
Título: UD. 5.4 - Bootstrap 5
Autor: Javier Egea Blasco
Año: 24-25
Palabras clave: DAW, DIW
---


# 1 Introducción: "Desarrollo Frontend con Bootstrap"
<div align="center">
</br>
<img src="https://github.com/javieregeablasco/DAW/blob/main/DIW/UT.%205%20-%20SASS/img/bootstrap-logo-shadow.png" width=250px>
</div>

El desarrollo frontend es una área esencial en la creación de aplicaciones y sitios web modernos. En este contexto, **Bootstrap CSS** se ha consolidado como una de las herramientas más populares para diseñar interfaces.  

**Bootstrap**, un framework CSS desarrollado originalmente por Twitter, ofrece un conjunto de herramientas predefinidas que incluyen sistemas de diseño responsivo basados en grid, componentes reutilizables como botones, menús y formularios, además de **utilidades para personalizar estilos**.  
Su objetivo principal es simplificar y acelerar el proceso de desarrollo, permitiendo que los desarrolladores se enfoquen más en la funcionalidad y la experiencia del usuario, sin tener que diseñar estilos propios.

El enfoque **mobile-first** y su compatibilidad con la navegadores modernos hacen de Bootstrap una elección ideal para desarrolladores y su estructura modular y personalizable facilita la adaptación de los estilos a las necesidades específicas de cada proyecto.

# 2 Boostrap frente a otros frameworks de CSS
<img src="https://github.com/javieregeablasco/DAW/blob/main/DIW/UT.%205%20-%20SASS/img/CSS-Framework---Bootstrap.webp" width=60%>  

Comparación del número de instalaciones de **Bootstrap** y **Tailwind**, durante el periodo 2023-2024, usando el comando `npm`.  
<img src="https://d2b57pa8jvjkcd.cloudfront.net/shEYQpSsZGZcwRfsh/XHyYpkAKLY-bootstrap-tailwind-css-popularity-chart-npm-trends.png" width=90%> 

# 3 Configuración básica de **Boostrap**
## 3.1 Enlazar con Boostrap desde un CDN
Toda la información de Boostrap <a href="https://getbootstrap.com/">**en la página oficial**</a>.  
Si solo deseamos usar `Bootstrap` sin alterar su contenido, simplemente añadiremos los `CDN links` via `jsDelivr` en los metadatos del `<head>` de nuestro proyecto.  
```
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet"
        integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH" crossorigin="anonymous">
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"
        integrity="sha384-YvpcrYf0tY3lHB60NNkmXc5s9fDVZLESaAA55NDzOxhy9GkcIdslK1eN7N6jIeHz"
        crossorigin="anonymous"></script>
    <title>Usar Bootsrap</title>
</head>
```
## 3.2 Usar extensiones de VSC para Bootstrap
Para evitar de siempre estar consultando la documentación oficial, se recomienda instalar utilidades `snippets` que permitiran autocompletar el código CSS con los estilos propios de Bootstrap.
>Ejemplo: Bootstrap 5 Quick Snippets

## 3.3 Usar Bootstrap conjuntamente con estilos propios
Puede que nos interese modificar el estilo predefinido de Bootstrap y aportar estilos propios.  
En este caso, podemos incluir una hoja de estilos CSS propia al proyecto, **siempre después de la declaración de Bootstrap** para evitar conflictos.
```
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet"
        integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH" crossorigin="anonymous">
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"
        integrity="sha384-YvpcrYf0tY3lHB60NNkmXc5s9fDVZLESaAA55NDzOxhy9GkcIdslK1eN7N6jIeHz"
        crossorigin="anonymous"></script>
    <link rel="stylesheet" href="css/estilos.css">

    <title>Usar Bootsrap</title>
</head>
```
# 4 Usar Boostrap en nuestro proyecto
para añadir clases de estilos propias de Bootstrap, simplemente añadiremos su nombre a la declaracion de estilos de la etiquetas que queremos modificar.
>Ejemplo de cambio de <a href="https://getbootstrap.com/docs/5.3/content/typography/">**tipografía**</a>
```
<body>
  <header>
    <h1 class="display-1">Cabecera del documento</h1>
  </header>
  <main>             
    <p class="display-6">Cuerpo del texto</p>     
  </main>
  <footer>
    <p>Pie del documento</p>
  </footer>
</body>
```
## 4.1 Tarea RA4 CEab
1. Buscar en la documentación de **Bootstrap** el listado de navegadores compatibles.
2. Mirar la versión del navegador web que usáis habitualemente y comprobar si es compatible con la última versión establa de Bootstrap.
3. Encontrar la información que permite saber si Bootstrap se puede utilizar en dispositivos mobiles.
4. Entregar las capturas de pantalla en un documento de texto y subirlo a AULES en el apartado correspondiente.

# 5 Componentes de Bootstrap.
## 5.1 Layout (paginación)
El diseño de Bootstrap está basado en un sistema de cuadrícula flexible que se ajusta al tamaño de la pantalla.  
**Utiliza un sistema de cuadrícula de 12 columnas** para crear diseños responsivos. 
Más información <a href="https://getbootstrap.com/docs/5.3/layout/breakpoints/">**aquí**</a>

## 5.2 Contenidos
Bootstrap proporciona una variedad de clases para mejorar y estructurar el contenido. Incluye clases de tipografía para encabezados, párrafos y alineación de texto, así como clases de ayuda para el espaciado y los colores de texto.  
<a href="https://getbootstrap.com/docs/5.3/content/reboot/">Más información</a>  

## 5.3 Formularios
Bootstrap simplifica la creación de formularios con componentes y diseños predefinidos. Incluye clases para controles de formulario como campos de texto, menús desplegables y casillas de verificación. Los formularios se pueden personalizar fácilmente con diferentes tamaños de entrada, estados de validación y opciones de diseño.
<a href="https://getbootstrap.com/docs/5.3/forms/overview/">**Más información**</a>

## 5.4 Componentes
Bootstrap ofrece un amplio conjunto de componentes predefinidos para simplificar el desarrollo de interfaces de usuario. Estos incluyen botones, tarjetas, modales, barras de navegación y más. Cada componente es personalizable y responsivo, lo que garantiza que tu aplicación web mantenga una apariencia coherente en diferentes dispositivos y tamaños de pantalla.
<a href="https://getbootstrap.com/docs/5.3/forms/overview/">**Más información**</a>

## 5.5 Componentes de ayuda
Los helpers de Bootstrap son clases utilitarias que simplifican tareas comunes y mejoran la legibilidad. Incluyen clases para la alineación de texto, visibilidad, propiedades de visualización y más. Los helpers facilitan el ajuste de elementos sin necesidad de escribir CSS personalizado, acelerando el desarrollo y garantizando la coherencia.
<a href="https://getbootstrap.com/docs/5.3/helpers/clearfix/">**Más información**</a>

## 5.6 Utilidades
Las utilidades de Bootstrap son clases pequeñas y reutilizables que proporcionan funcionalidad y control adicionales. Incluyen clases para espaciado, alineación, bordes y colores de fondo. Las utilidades ayudan a ajustar rápidamente y de manera eficiente la apariencia de los elementos, permitiendo realizar ajustes de diseño flexibles y responsivos.
<a href="https://getbootstrap.com/docs/5.3/utilities/api/">**Más información**</a>

# 6 Paginación (layout con Bootstrap)
En **Bootstrap 5**, los **layouts** son las estructuras basicas que se pueden usar para organizar el contenido en una página web.  

## 6.1 Breakpoints
Bootstrap 5 utiliza el **responsive design de forma nativa** lo que permite crear layouts adaptables al tamaño de la  pantalla.
Los breakpoints de Bootstrap vienen definidos en la siguiente tabla.

| Breakpoint | Prefijo de clase | Tamaño mínimo de pantalla |
|------------|------------------|---------------------------|
| Extra small |	None |	<576px |
| Small	 |sm	 | ≥576px |
| Medium |	md | ≥768px |
| Large |	lg	| ≥992px |
| Extra | large	xl |	≥1200px |
| Extra extra large |	xxl | ≥1400px |


## 6.2 Containers / contenedores
Son el elemento básico de Bootstrap y son necesarios si queremos usar el sistema de rejilla nativo (de Bootstrap).  
El selector `container` permite definir una caja con unas dimensiones `responsive` como podemos ver en la siguiente tabla. 

**Formas de definir el ancho de una caja con container :**
 - .container
 - .container-{breakpoint}
 - .container-fluid

|| Extra small <576px | Small ≥576px | Medium ≥768px | Large ≥992px | X-Large ≥1200px | XX-Larg ≥1400px |
|------------------|--------------------|--------------|---------------|--------------|-----------------|-----------------|
| .container |	100% | 540px | 720px | 960px |	1140px |	1320px |	
| .container-sm |	100% |	540px |	720px |	960px |	1140px |	1320px |
| .container-md	| 100% |	100% |	720px |	960px |	1140px |	1320px |
| .container-lg	| 100% |	100% |	100% |	960px |	1140px |	1320px |
| .container-xl |	100% |	100% |	100% |	100% |	1140px |	1320px |
| .container-xxl |	100% |	100% |	100% |	100% |	100% |	1320px |
| .container-fluid |	100% |	100% |	100% |	100% |	100% |	100% |

>**Ejemplo**
```
<body>
  <div class="container" style="background-color: antiquewhite;">Contenedor con container</div>
  <div class="container-lg" style="background-color: rgb(223, 250, 215);">Contenedor con container-lg</div>
  <div class="container-fluid" style="background-color: rgb(215, 236, 250);">Contenedor con container-fluid</div>
</body>
```

## 6.3 Grid / rejilla
El sistema de rejilla es el núcleo del diseño de Bootstrap. Está basado en **flexbox** y divide la página en un **sistema de 12 columnas**. Estas columnas se pueden combinar para crear diferentes diseños.  
El selector `row` sirve para estructurar el contenido de la página en filas. Cada fila estará compuesta de **una serie de columnas** y esas columnas, se ajustarán al tamaño de la pantalla. 

### 6.3.1 Columnas de ancho idéntico
Para renderizar columnas de ancho identico, usaremos el selector de clase `col`.
>**Ejemplo**
```
<body>
  <div class="container text-center">
    <div class="row" style="background-color: antiquewhite;">
      <div class="col">
        Columna 1
      </div>
      <div class="col" style="background-color: aqua;">
        Columna 2
      </div>
      <div class="col" style="background-color: aquamarine;">
        Column 3
      </div>
    </div>
  </div>
</body>
```

### 6.3.2 Columnas de ancho desigual
Para definir un tamaño de columnas personalizado, usaremos el sufijo `-XX`, donde XX puede adoptar los valores del 1 al 12 (recordar que el sistema de columnas en Bootstrap se basa sobre **una distribución máxima de 12 columnas**).
>**Ejemplo de 3 columnas que ocupan 2, 8 y 2 columnas (del grid) respectivamente.**  
```
<body> 
  <div class="container text-center">
    <div class="row" style="background-color: antiquewhite;">
      <div class="col-2">
        Columna 1
      </div>
      <div class="col-8" style="background-color: aqua;">
        Columna 2
      </div>
      <div class="col-2" style="background-color: aquamarine;">
        Column 3
      </div>
    </div>
  </div>
</body>
```
**Nota importante:** Para evitar resultados inesperados siempre respetar que la suma del ancho de las columnas sea igual a 12.

### 6.3.3 Columnas ajustables a su contenido
Es bastante habitual tener que reajustar el ancho de las columnas en función del tamaño del `viewport` y del contenido de las columnas. Para ello usaremos las clases `col-{breakpoint}-auto`. 

>**Ejemplo con y sin reajute del ancho de las columnas**  
>Al llegar al breakpoint (lg: 992px) **col-lg-auto** "pasa a ser col-lg" y sigue la misma estrategia que container.
<img src="https://github.com/javieregeablasco/DAW/blob/main/DIW/UT.%205%20-%20SASS/img/col-lg.png" width:200px>

```
<body> 
  <div class="container text-center" >
    <div class="row justify-content-md-center col-lg-auto" style="background-color: black; color: white;">
      Las columnas 1 y 3 tienen un ancho de 2. La columna 3 tiene un ancho automático a su contenido
    </div>
    <div class="row justify-content-md-center">
      <div class="col-2" style="background-color: antiquewhite;">
        1 of 3
      </div>
      <div class="col-lg-auto" style="background-color: aqua;">
        El ancho del contenedor se ajusta hasta llegar al breakpoint. 
      </div>
      <div class="col-2" style="background-color: aquamarine;">
        3 of 3
      </div>
    </div>
    <div class="row justify-content-md-center col-lg-auto" style="background-color: black; color: white;">
      Las columnas 1, 2 y 3 tienen un ancho de 2, 8 y 2 respectivamente
    </div>
    <div class="row justify-content-md-center">
      <div class="col-2" style="background-color: antiquewhite;">
        1 of 3
      </div>
      <div class="col-8" style="background-color: aqua;">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolor sit amet. 
      </div>
      <div class="col-2" style="background-color: aquamarine;">
        3 of 3
      </div>
    </div>
  </div>
</body>
```

### 6.3.3 Columnas ajustables al breakpoint
Del mismo modo que podemos ajustar el ancho del contenedor a su contenido, también podemos ajustarlo al ancho del contendor padre y en función del breakpoint.  
 
```
<body> 
  <div class="container text-center" >
    <div class="row justify-content-md-center">
      <div class="col-1" style="background-color: antiquewhite;">
        1 de 12
      </div>
      <div class="col-1" style="background-color:aqua;">
        2 de 12
      </div>
      <div class="col-1" style="background-color:bisque";>
        3 de 12
      </div>
      <div class="col-1" style="background-color:azure">
        4 de 12
      </div>
      <div class="col-1" style="background-color:beige">
        5 de 12
      </div>
      <div class="col-1" style="background-color:bisque">
        6 de 12
      </div>
      <div class="col-1" style="background-color:black; color:white">
        7 de 12
      </div>
      <div class="col-1" style="background-color:blanchedalmond">
        8 de 12
      </div>
      <div class="col-1" style="background-color:blue; color: aliceblue;">
        9 de 12
      </div>
      <div class="col-1" style="background-color:blueviolet; color:aliceblue">
        10 de 12
      </div>
      <div class="col-1" style="background-color:brown; color:aliceblue">
        11 de 12
      </div>
      <div class="col-1" style="background-color:burlywood">
        12 de 12
      </div>   
    </div>
    <div class="row justify-content-md-center col-lg-auto" style="background-color: black; color: white;">
      Las columnas 1, 2 y 3 tienen un ancho de 1, 10 y 1 respectivamente hasta el breakpoint "sm"
    </div>
    <div class="row justify-content-md-center">
      <div class="col-lg-1 " style="background-color: antiquewhite;">
        1
      </div>
      <div class="col-lg-10" style="background-color: aqua;">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolor sit amet. 
      </div>
      <div class="col-lg-1" style="background-color: aquamarine;">
        1
      </div>
    </div>
  </div>
</body>
```

También podemos definir más de un breakpoint para definir el ancho `responsive` de las columnas que ocupará más o menos columnas en función del ancho del `viewport`.  
En este ejemplo vemos como la distribución del ancho de las columnas pasa de ser 2,8,2 a ser 1,10,1 cuando el ancho de la ventana es inferior al `breakpoint Large` o sea `992px`.  

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet"
        integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH" crossorigin="anonymous">
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"
        integrity="sha384-YvpcrYf0tY3lHB60NNkmXc5s9fDVZLESaAA55NDzOxhy9GkcIdslK1eN7N6jIeHz"
        crossorigin="anonymous"></script>
    <title>col 2 brekpoints</title>
    <style>      
      @media screen and (max-width: 960px) {
        #comentario::after {
          background-color:red;
          color: black;
          width: 100%;
          content: "Luego pasa a 1, 10, 1";       
        }
      }

      @media screen and (max-width: 540px) {
        #comentario::after {
          background-color:blueviolet;
          color: wheat;
          width: 100%;
          content: "Luego pasa a 100%, 100%, 100%";       
        }
      }
    </style>
</head>
<body> 
  <div class="container text-center" >
    <div class="row justify-content-md-center">
      <div class="col-1" style="background-color: antiquewhite">
        1
      </div>
      <div class="col-1" style="background-color:aqua">
        2
      </div>
      <div class="col-1" style="background-color:bisque">
        3
      </div>
      <div class="col-1" style="background-color:azure">
        4
      </div>
      <div class="col-1" style="background-color:beige">
        5
      </div>
      <div class="col-1" style="background-color:bisque">
        6
      </div>
      <div class="col-1" style="background-color:black; color:white">
        7
      </div>
      <div class="col-1" style="background-color:blanchedalmond">
        8
      </div>
      <div class="col-1" style="background-color:blue; color: aliceblue">
        9
      </div>
      <div class="col-1" style="background-color:blueviolet; color:aliceblue">
        10
      </div>
      <div class="col-1" style="background-color:brown; color:aliceblue">
        11
      </div>
      <div class="col-1" style="background-color:burlywood">
        12
      </div>   
    </div>
    <div id="comentario" class="row justify-content-md-center col-lg-auto" style="background-color: black; color: white;">
      Las columnas 1, 2 y 3 tienen un ancho de 2, 8 y 2 respectivamente hasta el breakpoint "md" de **540px**.
    </div>
    <div class="row justify-content-md-center">
      <div class="col-lg-2 col-sm-1" style="background-color: antiquewhite;">
        1
      </div>
      <div class="col-lg-8 col-sm-10" style="background-color: aqua;">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolor sit amet. 
      </div>
      <div class="col-lg-2 col-sm-1" style="background-color: aquamarine;">
        1
      </div>
    </div>
  </div>
</body>
```

### 6.3.4 Predefinir la cantidad de columnas, clases row-cols
Las clases relacionadas con `row-cols` permiten configurar rápidamente el número de columnas en un diseño grid utilizando el sistema de filas y columnas (row y col).  
Estas clases son especialmente útiles cuando se quiere lograr un diseño con un número uniforme de columnas, independientemente de cuántas filas haya en total.
```
<body>
  <div class="container text-center">
    <div class="row">
      <div class="col-12" style="background-color: black;color: aliceblue;">
        Con row-cols-2, se predefine el contenedor a solo 2 columnas por fila
      </div>    
    </div>
    <div class="row row-cols-2">
      <div class="col" style="background-color: aliceblue;">Columna 1</div>
      <div class="col" style="background-color: antiquewhite;">Columna 2</div>
      <div class="col" style="background-color: aqua;">Columna 3</div>
      <div class="col" style="background-color: aquamarine;">Columna 4</div>
    </div>
    <div class="row">
      <div class="col-12" style="background-color: black;color: aliceblue;">
        También se puede definir la cantidad de columnas que ocupará cada columna
      </div>    
    </div>
    <div class="row row-cols-2">
      <div class="col-8" style="background-color: aliceblue;">Columna 1</div>
      <div class="col-4" style="background-color: antiquewhite;">Columna 2</div>
      <div class="col-3" style="background-color: aqua;">Columna 3</div>
      <div class="col-9" style="background-color: aquamarine;">Columna 4</div>
    </div>
    <div class="row">
      <div class="col-12" style="background-color: black;color: aliceblue;">
        Ejemplo con solo 3 columnas (a priori no sabemos cuantas columnas necesitabamos al iniciar el proyecto)
      </div>    
    </div>
    <div class="row row-cols-2">
      <div class="col-8" style="background-color: aliceblue;">Columna 1</div>
      <div class="col-4" style="background-color: antiquewhite;">Columna 2</div>
      <div class="col" style="background-color: aqua;">Columna 3</div>     
    </div>
  </div>
</body>
```  

Como es de esperar, también podemos ajustar la cantidad de columnas a la resolución de la pantalla.
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet"
        integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH" crossorigin="anonymous">
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"
        integrity="sha384-YvpcrYf0tY3lHB60NNkmXc5s9fDVZLESaAA55NDzOxhy9GkcIdslK1eN7N6jIeHz"
        crossorigin="anonymous"></script>
    <title>col 2 brekpoints</title>
    <style>      
      @media screen and (max-width: 992px) {
        #comentario::after {
          background-color:red;
          color: black;
          width: 100%;
          content: "Luego pasa a 2 columnas por fila hasta llegar sm";       
        }
      }

      @media screen and (max-width: 576px) {
        #comentario::after {
          background-color:blueviolet;
          color: wheat;
          width: 100%;
          content: "Luego pasa a 1 columna del 100%";       
        }
      }
    </style>
</head>
<body> 
  <div class="container text-center" >
    <div class="row justify-content-md-center">
      <div class="col-1" style="background-color: antiquewhite">
        1
      </div>
      <div class="col-1" style="background-color:aqua">
        2
      </div>
      <div class="col-1" style="background-color:bisque">
        3
      </div>
      <div class="col-1" style="background-color:azure">
        4
      </div>
      <div class="col-1" style="background-color:beige">
        5
      </div>
      <div class="col-1" style="background-color:bisque">
        6
      </div>
      <div class="col-1" style="background-color:black; color:white">
        7
      </div>
      <div class="col-1" style="background-color:blanchedalmond">
        8
      </div>
      <div class="col-1" style="background-color:blue; color: aliceblue">
        9
      </div>
      <div class="col-1" style="background-color:blueviolet; color:aliceblue">
        10
      </div>
      <div class="col-1" style="background-color:brown; color:aliceblue">
        11
      </div>
      <div class="col-1" style="background-color:burlywood">
        12
      </div>   
    </div>
    <div id="comentario" class="row justify-content-md-center col-lg-auto" style="background-color: black; color: white;">
      Las columnas 1, 2, 3 y 4 ocupan solamente una fila hasta llegar al breakpoint "lg"
    </div>
    <div class="row row-cols-lg-4 row-cols-sm-2 justify-content-md-center">
      <div style="background-color: antiquewhite;">
        columna 1 
      </div>
      <div style="background-color: aqua;">
        columna 2 
      </div>
      <div style="background-color:bisque ">
        columna 3
      </div>
      <div style="background-color: aquamarine;">
        columna 4
      </div>
    </div>
  </div>
</body>
```
### 6.3.5 Anidación de columnas
La anidación de columnas permite crear estructuras más complejas dentro del sistema grid.  
Consiste en anidar una fila (row) dentro de una columna (col) existente, permitiendo dividir esa columna en subcolumnas adicionales. Es particularmente útil para organizar contenido de nuestro proyecto en niveles jerárquicos. 

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet"
        integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH" crossorigin="anonymous">
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"
        integrity="sha384-YvpcrYf0tY3lHB60NNkmXc5s9fDVZLESaAA55NDzOxhy9GkcIdslK1eN7N6jIeHz"
        crossorigin="anonymous"></script>
    <title>col 2 brekpoints</title>
</head>

<body> 
  <div class="container text-center" >
    <div class="row justify-content-md-center col-lg-auto" style="background-color: black; color: white; border: 2px solid blue;">
        Ejemplo de anidación de columnas
    </div>
      <div class="row row-cols-2 justify-content-md-center">
        <div class="col-3" style="background-color:blueviolet; color:white;">
          columna no anidada 
        </div>    
        <div class="col-9" style="border: 1px solid mediumseagreen;">
          <div class="row" style="background-color: brown; padding: 5px 5px 5px 5px; margin: 5px;">
          <div class="col-3" style="background-color: aqua;">columna anidada 1</div>
          <div class="col-6" style="background-color: aquamarine;">columna anidada 2</div>
          <div class="col-3" style="background-color: bisque;">columna anidada 3</div>
        </div>                
      </div>
    </div>      
  </div>
</body>
```  

### 6.3.6 Tarea RA4 CEc

## 6.4 Estilos de columnas de Bootstrap
Los estilos de columnas permiten aplicar estilos para el renderizado de las columnas dentro de su contenedor.  

### 6.4.1 Alineación vertical de columnas
Para la alineación vertical de la columnas dentro de su contenedor, disponemos, entre otras, de las clases `align-items-start`, `align-items-center` y `align-items-end` que nos permiten posicionar los contenedores `col` dentro de su `row`.

´´´
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet"
        integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH" crossorigin="anonymous">
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"
        integrity="sha384-YvpcrYf0tY3lHB60NNkmXc5s9fDVZLESaAA55NDzOxhy9GkcIdslK1eN7N6jIeHz"
        crossorigin="anonymous"></script>
    <title>Alinación vertical</title>    
</head>

<body>  
  <div class="container text-center"> 
  
    <div class="row align-items-start" style="height: 33vh; background-color: bisque; padding: 5px;">         
      <div class="col" style="background-color: aliceblue;">
        Columnas arriba
      </div>
      <div class="col" style="background-color: antiquewhite;">
        Columnas arriba
      </div>
      <div class="col" style="background-color: aqua;">
        Columnas arriba
      </div>      
    </div>  

    <div class="row align-items-center" style="height: 33vh; background-color: blueviolet; padding: 5px;">         
      <div class="col" style="background-color: antiquewhite;">
        Columnas medio
      </div>
      <div class="col" style="background-color: aqua;">
        Columnas medio
      </div>
      <div class="col" style="background-color: aliceblue;">
        Columnas medio
      </div>
    </div>  
      
    <div class="row align-items-end" style="height: 33vh; background-color: brown; padding: 5px;">         
      <div class="col" style="background-color: aqua;">
        Columnas abajo
      </div>
      <div class="col" style="background-color: aliceblue;">
        Columnas abajo
      </div>
      <div class="col" style="background-color: antiquewhite;">
        Columnas abajo
      </div>
    </div>
  </div>    
</body>
´´´

### 6.4.2 Alineación horizontal de columnas
Para la alineación horizontal de los contenedores `col`, disponemos, entre otras, de las clases:
- **`justify-content-start`**: Alinea los elementos al inicio del contenedor.
- **`justify-content-center`**: Centra horizontalmente los elementos dentro del contenedor.
- **`justify-content-end`**: Alinea los elementos al final del contenedor.
- **`justify-content-around`**: Distribuye los elementos con espacio igual alrededor de ellos, dejando espacio extra al inicio y al final del contenedor.
- **`justify-content-between`**: Distribuye los elementos con el máximo espacio posible entre ellos, sin dejar espacio al inicio ni al final del contenedor.
- **`justify-content-evenly`**: Distribuye los elementos con espacio igual entre ellos y también entre los bordes del contenedor.

  ```
  <!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet"
        integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH" crossorigin="anonymous">
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"
        integrity="sha384-YvpcrYf0tY3lHB60NNkmXc5s9fDVZLESaAA55NDzOxhy9GkcIdslK1eN7N6jIeHz"
        crossorigin="anonymous"></script>
    <title>Alinación vertical</title>
    
</head>

<body>  
  <div class="container text-center"> 
  
    <div class="row justify-content-start" style="background-color:green;  padding: 5px;">         
      <div class="col-3" style="background-color: aliceblue;">
        Contenido start
      </div>
      <div class="col-4" style="background-color: antiquewhite;">
        Contenido start
      </div>
    </div>  

    <div class="row justify-content-center" style="background-color: blueviolet; padding: 5px;">         
      <div class="col-3" style="background-color: antiquewhite;">
        Contenido center
      </div>
      <div class="col-4" style="background-color: aqua;">
        Contenido center
      </div>
    </div>  
      
    <div class="row justify-content-end" style="background-color: brown; padding: 5px;">         
      <div class="col-3" style="background-color: aqua;">
        Contenido end
      </div>
      <div class="col-3" style="background-color: aliceblue;">
        Contenido end
      </div>
    </div>  

    <div class="row justify-content-around" style="background-color:green;  padding: 5px;">         
      <div class="col-3" style="background-color: aliceblue;">
        Contenido around
      </div>
      <div class="col-4" style="background-color: antiquewhite;">
        Contenido around
      </div>
    </div>  
  
    <div class="row justify-content-between" style="background-color: blueviolet; padding: 5px;">         
      <div class="col-3" style="background-color: antiquewhite;">
        Contenido between
      </div>
      <div class="col-4" style="background-color: aqua;">
        Contenido between
      </div>
    </div>  
      
    <div class="row justify-content-evenly" style="background-color: brown; padding: 5px;">         
      <div class="col-3" style="background-color: aqua;">
        Contenido evenly
      </div>
      <div class="col-3" style="background-color: aliceblue;">
        Contenido evenly
      </div>
    </div>
  </div>    
</body>
```
  
### 6.4.3 Organización de las columnas
La propiedad flex-wrap de CSS especifica si los elementos "hijos" son obligados a permanecer en una misma línea o pueden fluir en varias líneas. Si la cobertura (wrap) está permitida, esta propiedad también te permite controlar la dirección en la cual serán apilados los elementos.

### 6.4.4 Saltos de columnas a una linea nueva
### 6.4.5 Ordenar columnas
### 6.4.6 Clase offset para posicionar columnas
### 6.4.7 Márgenes
### 6.4.8 Columnas únicas




#### 3. **Alineación y distribución**
Bootstrap proporciona herramientas para alinear elementos dentro de filas y columnas:
- **Alineación vertical**:
  - `align-items-start`, `align-items-center`, `align-items-end`.
- **Distribución horizontal**:
  - `justify-content-start`, `justify-content-center`, `justify-content-between`, etc.

---

#### 4. **Espaciado (Spacing)**
El espaciado entre los elementos se controla mediante utilidades como:
- Márgenes: `m-`, `mt-`, `mb-`, etc.
- Padding: `p-`, `pt-`, `pb-`, etc.




#### 6. **Utilities para diseño avanzado**
Bootstrap 5 introduce utilidades adicionales para lograr diseños más personalizados sin necesidad de escribir CSS adicional:
- **Grid modificable**:
  Clases como `g-3` para definir el tamaño del espacio entre filas/columnas.
- **Clases de orden**:
  Clases como `order-md-1` para cambiar el orden de las columnas responsivamente.

