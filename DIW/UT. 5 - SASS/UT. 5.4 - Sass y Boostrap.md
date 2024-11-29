---
Título: UD. 5.4 - Sass y Bootstrap
Autor: Javier Egea Blasco
Año: 24-25
Palabras clave: DAW, DIW
---


# 1 Introducción: "Desarrollo Frontend con Bootstrap"
<img src="https://github.com/javieregeablasco/DAW/blob/main/DIW/UT.%205%20-%20SASS/img/bootstrap-logo-shadow.png" width=250px>
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
## 5.1 Contenidos
Bootstrap proporciona una variedad de clases para mejorar y estructurar el contenido. Incluye clases de tipografía para encabezados, párrafos y alineación de texto, así como clases de ayuda para el espaciado y los colores de texto.  
<a href="https://getbootstrap.com/docs/5.3/content/reboot/">Más información</a>  

## 5.2 Formularios
Bootstrap simplifica la creación de formularios con componentes y diseños predefinidos. Incluye clases para controles de formulario como campos de texto, menús desplegables y casillas de verificación. Los formularios se pueden personalizar fácilmente con diferentes tamaños de entrada, estados de validación y opciones de diseño.
<a href="https://getbootstrap.com/docs/5.3/forms/overview/">**Más información**</a>

## 5.3 Componentes
Bootstrap ofrece un amplio conjunto de componentes predefinidos para simplificar el desarrollo de interfaces de usuario. Estos incluyen botones, tarjetas, modales, barras de navegación y más. Cada componente es personalizable y responsivo, lo que garantiza que tu aplicación web mantenga una apariencia coherente en diferentes dispositivos y tamaños de pantalla.
<a href="https://getbootstrap.com/docs/5.3/forms/overview/">**Más información**</a>

## 5.4 Componentes de ayuda
Los helpers de Bootstrap son clases utilitarias que simplifican tareas comunes y mejoran la legibilidad. Incluyen clases para la alineación de texto, visibilidad, propiedades de visualización y más. Los helpers facilitan el ajuste de elementos sin necesidad de escribir CSS personalizado, acelerando el desarrollo y garantizando la coherencia.
<a href="https://getbootstrap.com/docs/5.3/helpers/clearfix/">**Más información**</a>

## 5.5 Utilidades
Las utilidades de Bootstrap son clases pequeñas y reutilizables que proporcionan funcionalidad y control adicionales. Incluyen clases para espaciado, alineación, bordes y colores de fondo. Las utilidades ayudan a ajustar rápidamente y de manera eficiente la apariencia de los elementos, permitiendo realizar ajustes de diseño flexibles y responsivos.
<a href="https://getbootstrap.com/docs/5.3/utilities/api/">**Más información**</a>

## 5.6 Layout (paginación)
El diseño de Bootstrap está basado en un sistema de cuadrícula flexible que se ajusta al tamaño de la pantalla.  
**Utiliza un sistema de cuadrícula de 12 columnas** para crear diseños responsivos. 
Más información <a href="https://getbootstrap.com/docs/5.3/layout/breakpoints/">**aquí**</a>
>**Ejemplo**
