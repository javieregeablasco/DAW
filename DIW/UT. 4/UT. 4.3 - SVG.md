---
Título: UD. 4.3 - SVG
Autor: Javier Egea Blasco
Año: 24-25
Palabras clave: DAW, DIW
---

# 1. - Introducción
**SVG (Scalable Vector Graphics)** es un formato de gráficos vectoriales basado en XML que se utiliza para renderizar imágenes bidimensionales.   

A diferencia de los gráficos rasterizados (como JPEG o PNG), que están formados por píxeles, SVG define imágenes mediante formas geométricas (líneas, círculos, polígonos, etc.), lo que le permite ser escalado a cualquier tamaño sin pérdida de calidad.

Además, al estar basado en texto, puede ser manipulado mediante CSS y JavaScript, lo que lo convierte en una opción flexible y ligera para el desarrollo de interfaces web interactivas. 

También es compatible con todos los navegadores modernos, lo que asegura su versatilidad en la creación de aplicaciones web.

# 2. - Características de SVG
-  **Escalabilidad**: Los gráficos SVG pueden ser escalados a cualquier tamaño sin pérdida de calidad.

-  **Interactividad**: Permite agregar interactividad mediante eventos.
 
-  **Compatibilidad con CSS**: Los gráficos SVG admiten estilos CSS, lo que permite, entre otros, realizar animaciones.

-  **Tamaño de archivo reducido**: Los archivos SVG se almacenan en ficheros de texto plano, lo que los hacen más ligeros que cualquier imagen rasterizada, lo que mejora el rendimiento de la página web.

-  **Texto legible**: Al ser texto en XML, los gráficos SVG pueden ser indexados por motores de búsqueda y son accesibles para lectores de pantalla, mejorando la accesibilidad web.

-  **Soporte para animaciones**: SVG soporta **animaciones nativas** tanto dentro de su código como a través de CSS y JavaScript. 

-  **Compatibilidad con navegadores modernos**: SVG es compatible con todos los navegadores actuales.
   
-  **Formato basado en XML**: Al estar escrito en XML, puede ser editado con cualquier editor de texto.

# 3. - Repositorios de imágenes SVG.
Existen numerosos sitios web que ofrecen gráficos SVG listos para usar en proyectos (la mayoría piden suscripción). 

-  <a href="https://cocomaterial.com">**Coco Material**</a>   
-  <a href="https://freeicons.io">**Free Icons:**</a>  
-  <a href="https://game-icons.net">**Game Icons**</a>  
-  <a href="https://iconduck.com">**Icon Duck**</a>  
-  <a href="https://thenounproject.com">**Icons and Photos For Everything**</a>  
-  <a href="https://patternpad.com">**Patternpad**</a>  
-  <a href="https://Pixabay.com">**Pixabay**</a>  
-  <a href="https://svgrepo.com">**SVG Repo**</a>  
-  <a href="https://svgsilh.com">**SVG Silh**</a>  
-  <a href="https://uxwing.com">**Uxwing**</a>  
-  <a href="https://www.flaticon.es/">**Flaticon**</a>  
-  <a href="https://undraw.co/illustrations">**unDraw**</a>  
-  <a href="https://iconmonstr.com/">**iconmonstr**</a>  

## 4. - Formas de insertar imágenes SVG.
## 4.1 - Etiqueta img para un SVG
Es la forma más sencilla de incluir un archivo SVG. El archivo SVG permanecerá externo, pero será cargado en el documento HTML.  

Para agregar una imagen SVG utilizando la etiqueta <img>, simplemente especificaremos la ruta del archivo SVG dentro de la etiqueta img.
```
<!doctype html>
<html>
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link href="./output.css" rel="stylesheet">
</head>
<body>
  <h1 class="text-green-600 font-bold underline">
    ¡Mi primera imagen SVG!
  </h1>
  <img src="./img/icono.svg" alt="Imagen SVG" width=4%>
  
</body>
</html>
```

## 4.2 - SVG en línea (inline)
Las imágenes SVG pueden escribirse directamente en el documento HTML mediante la etiqueta <svg> </svg>.  

Para ello tendremos que acceder al código de la imagen.
1. Abrir el archivo SVG en el IDE.
2. Copiar todo el código SVG dentro de las etiquetas <svg> </svg>.
3. Pegar el código SVG dentro del elemento <body> del documento HTML. 
```
<p class="m-4 text-xl text-blue-700">SVG usando SVG en linea <strong>SVG</strong></p>
  <svg width="50" height="50" clip-rule="evenodd" fill-rule="evenodd" stroke-linejoin="round" stroke-miterlimit="2" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path d="m2.699 20c-.411 0-.699-.312-.699-.662 0-.249.145-.516.497-.703 1.788-.947 3.858-4.226 3.858-6.248-3.016.092-4.326-2.582-4.326-4.258 0-2.006 1.738-4.129 4.308-4.129 3.241 0 4.83 2.547 4.83 5.307 0 5.981-6.834 10.693-8.468 10.693zm10.833 0c-.41 0-.699-.312-.699-.662 0-.249.145-.516.497-.703 1.788-.947 3.858-4.226 3.858-6.248-3.015.092-4.326-2.582-4.326-4.258 0-2.006 1.739-4.129 4.308-4.129 3.241 0 4.83 2.547 4.83 5.307 0 5.981-6.833 10.693-8.468 10.693z" fill-rule="nonzero"/>
  </svg>
```  
## 4.3 - Etiqueta object
La etiqueta <object> </object> permite incrustar un archivo SVG como un objeto independiente en la página.  

La etiqueta <object> ofrece flexibilidad al incrustar SVGs, permitiendo un control preciso sobre el tamaño y la presentación del gráfico vectorial.
```
<p class="m-4 text-xl text-green-700">SVG usando <strong>object</strong></p>
<object type="image/svg+xml" data="/SVG1/src/img/icono.svg" width="50" height="50">
  Tu navegador no soporta SVGs.
</object>
```

Donde:
-  El atributo type="image/svg+xml" especifica el tipo de archivo como SVG.
-  El atributo data="/SVG1/src/img/icono.svg" indica la ruta del archivo SVG.
-  Los atributos width="50" y height="50" definen las dimensiones del objeto SVG.
  
## 4.4 - Etiqueta iframe
También se puede usar la etiqueta **iframe** para insertar imágenes SVG. 

Sin embargo, es importante tener en cuenta ciertas consideraciones al utilizar <iframe> para mostrar SVGs:
-  **Dificultades de mantenimiento**: Los <iframe> pueden ser difíciles de mantener, especialmente cuando existen múltiples elementos <iframe> en la página.
-  **SEO**: El uso **excesivo** de <iframe> puede **afectar negativamente** la optimización de l sitio web para motores de búsqueda.
-  **Escalabilidad:** Las imágenes SVG añadidas mediante <iframe> **no son escalables**, lo que **anula el propósito** de utilizar gráficos vectoriales escalables.

```
<p class="m-4 text-xl text-cyan-600">SVG usando <strong>iframe</strong></p>
<iframe src="./img/icono.svg" width="50" height="50" title="SVG"></iframe>
```

## 4.4 - Usando la propiedad backgroung-image
Al igual que la etiqueta iframe, backgroung-image también tiene limitaciones a tener en cuenta.  
-  **No Accesible:** Las imágenes de fondo SVG no son accesibles a través del texto alternativo (alt) como las imágenes <img>.
-  **Escalabilidad:** La escalabilidad del SVG se ven limitadas por las propiedad CSS del contenedor.
```
<div class="w-96 h-96 bg-[url('/SVG1/src/img/icono.svg')] bg-cover bg-no-repeat flex justify-center items-center">
  <p class="m-4 text-xl text-cyan-600">5. SVG usando <strong>background</strong></p>
</div>  
```

# 5 - Crear un SVG
Existen al menos 2 maneras diferentes de crear nuestras imagenes SVG:  
-  **Programarlas mediante formas geométricas simples**:   
    Como hemos visto SVG es un formato basado en XML lo que permite crear imágenes directamente escribiendo código. 
-  **Crear un diseño con un programa de edición de imágenes y guardarlo en formato SVG**:
    Programas de edición de imágenes como **Adobe Illustrator**, **Inkscape** o **Sketch** permiten diseñar imágenes visualmente y luego exportarlas o guardarlas como archivos SVG.  


## 5.1 - Crear SVG programado
Para ello podremos usar las formas básicas disponibles como rectángulos, círculos, líneas y rutas pero antes deberemos ver la sintaxis empleada.
### 5.1.1 - Sintaxis de SVG
SVG es un lenguaje XML, por lo que su sintaxis sigue las reglas del XML.

El documento SVG se describe de la siguiente manera:  
-  **Elemento raíz** que contiene el resto de elementos.
-  **Todas las etiquetas están cerradas** (las etiquetas vacías incluyen una barra / al final de la etiqueta).
-  **Las etiquetas de cierre coinciden con las de apertura** (incluso en el uso de mayúsculas y minúsculas).
-  **Todos los atributos tienen algún valor**.
-  **Los valores de los atributos están entre comillas** (simples o dobles).
- Algunos de los **atributos se escriben con algunas letras en mayúsculas** y no se pueden escribir en minúsculas (viewBox).
```
<p>
  <svg version="1.1" xmlns="http://www.w3.org/2000/svg"
    width="170" height="165" viewBox="-100 -50 170 165">
    <polygon fill="yellow" stroke="red" stroke-width="7"
      points="129,150 85,119 41,150 57,104 15,66
        68,66 85,15 102,65 156,66 113,98" />
  </svg>
</p>
```
Donde: 
**1. Etiqueta `<svg>`**:
   - **`version="1.1"`**: Especifica la versión del estándar SVG utilizado.
   - **`xmlns="http://www.w3.org/2000/svg"`**: Define el espacio de nombres XML para SVG. resulta necesario para que el navegador sepa que se trata de un documento SVG.
   - **`width="170"` y `height="165"`**: Dimensiones del contenedor SVG.
   - **`viewBox="0 0 170 165"`**: Define el sistema de coordenadas del SVG. El `viewBox` permite que el contenido SVG se escale y se ajuste al tamaño del contenedor. Aquí se indica que el área visible comienza en (0, 0) y tiene un tamaño de 170 por 165 unidades.

**2. Etiqueta `<polygon>`**:
   - **`fill="yellow"`**: Define el color de relleno del polígono. 
   - **`stroke="red"`**: Establece el color del contorno (borde) del polígono.
   - **`stroke-width="7"`**: Especifica el grosor del contorno del polígono. 
   - **`points="129,150 85,119 41,150 57,104 15,66 68,66 85,15 102,65 156,66 113,98"`**: Define los vértices del polígono mediante un conjunto de coordenadas (x, y). Cada par de números representa un vértice en el espacio del SVG. 

### 5.1.2 - El plano de SVG, atributo viewBox
<img src="https://www.aulaclic.es/html/graficos/coordenadas_svg.png">  
El origen de coordenadas es el punto (0,0) los valores de la coordenada x van hacia la derecha y los valores de la coordenada y van hacia abajo.  

El atributo viewBox establece la porción del plano SVG que muestra la imagen. Este atributo se establece con cuatro valores:

**1. Primer valor:** abcisa (X) de la esquina superior izquierda de la porción del plano que muestra la imagen.
**2. Segundo valor:** ordenada (Y) de la esquina superior izquierda de la porción del plano que muestra la imagen.
**3. Tercer valor:** ancho de la porción del plano que muestra la imagen.
**4. Cuarto valor:** alto de la porción del plano que muestra la imagen.

```
<svg version="1.1" xmlns="http://www.w3.org/2000/svg" width="200" height="200" viewBox="-100 -100 200 200" style="background-color: lightgray">
  <circle cx="0" cy="0" r="100" fill="none" stroke="red" stroke-width="1" />
  <line x1="-100" y1="0" x2="200" y2="0" stroke="black" stroke-width="1" />
  <line x1="0" y1="-100" x2="0" y2="200" stroke="black" stroke-width="1" />
</svg>
```
>Actividad 1
>Cambiar los valores de width="105", height="105" y viewBox="-5 -5 105 105
>Entender los resultados obtenidos.

>Actividad 2
>Cambiar los valores de width="105" height="105" viewBox="-100 -100 105 105
>Entender los resultados obtenidos.

### 5.1.3 - Atributos width y height no proporcionales a viewBox



### 5.1.4Formas básicas de SVG





 como rectángulos, círculos, líneas y rutas. Algunos elementos básicos son:
- `<svg>`: El contenedor principal para gráficos SVG.
- `<rect>`: Para dibujar rectángulos.
- `<circle>`: Para dibujar círculos.
- `<path>`: Para crear formas más complejas usando rutas.

**Ejemplo de SVG básico:**
```xml
<svg width="100" height="100">
  <circle cx="50" cy="50" r="40" stroke="black" stroke-width="3" fill="red" />
</svg>
```

#### 5. **Recursos didácticos**
- Ordenador con entorno de desarrollo web (Visual Studio Code, Brackets).
- Navegador web actualizado (Google Chrome, Firefox).
- Tutoriales en línea sobre SVG, CSS y JavaScript.

#### 6. **Evaluación**
La evaluación se realizará mediante:
- **Prácticas**: Se valorará la correcta creación y manipulación de SVGs en proyectos web.
- **Proyectos**: Cada alumno integrará un gráfico SVG en una página web como parte de un proyecto final.
- **Cuestionario**: Preguntas teóricas sobre las ventajas y limitaciones de SVG en comparación con otros formatos.

#### 7. **Conclusión**
SVG es una herramienta fundamental para el desarrollo moderno de aplicaciones web debido a su flexibilidad, interactividad y capacidad de escalado sin pérdida de calidad. Comprender su uso y potencial permite crear aplicaciones más eficientes, estéticas y accesibles. 

--- 
Esta unidad ofrece una base sólida sobre SVG, preparando a los estudiantes para utilizar este formato en proyectos reales de desarrollo web.


https://www.eniun.com/como-insertar-imagen-svg-html-css/

https://kinsta.com/es/base-de-conocimiento/como-abrir-un-archivo-svg/

https://developer.mozilla.org/es/docs/Web/SVG/Tutorial

https://jenkov.com/tutorials/svg/index.html

https://www.w3.org/2002/Talks/www2002-svgtut-ih/hwtut.pdf

https://www.tutorialspoint.com/svg/index.htm

https://flaviocopes.com/svg/

https://kurtbruns.github.io/svg-tutorial/

https://www.svgbasics.com/index.html

https://www.aleksandrhovhannisyan.com/blog/svg-tutorial/
