---
Título: UD. 4.3 - SVG
Autor: Javier Egea Blasco
Año: 24-25
Palabras clave: DAW, DIW
---
<div align="center">
<img src="https://github.com/javieregeablasco/DAW/blob/main/DIW/UT.%204/img/SVG_logo.svg" width=25%>
</div>
 
# 1. - Introducción
**SVG (Scalable Vector Graphics)** es un formato de gráficos vectoriales basado en XML que se utiliza para renderizar imágenes bidimensionales.   

A diferencia de los gráficos rasterizados (como JPEG o PNG), que están formados por píxeles, SVG define imágenes mediante formas geométricas (líneas, círculos, polígonos, etc.), lo que le permite ser escalado a cualquier tamaño sin pérdida de calidad.

Además, al estar basado en texto, puede ser manipulado mediante CSS y JavaScript, lo que lo convierte en una opción flexible y ligera para el desarrollo de interfaces web interactivas. 

También es compatible con todos los navegadores modernos, lo que asegura su versatilidad en la creación de aplicaciones web.

- [Documentación oficial de SVG](https://developer.mozilla.org/es/docs/Web/SVG)

- <a href="https://marketplace.visualstudio.com/items?itemName=sidthesloth.svg-snippets">Extensión de SVG para VSC</a>

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

-  <a href="https://cocomaterial.com">Coco Material</a>   
-  <a href="https://freeicons.io">Free Icons:</a>  
-  <a href="https://game-icons.net">Game Icons</a>  
-  <a href="https://iconduck.com">Icon Duck</a>  
-  <a href="https://thenounproject.com">Icons and Photos For Everything</a>  
-  <a href="https://patternpad.com">Patternpad</a>  
-  <a href="https://Pixabay.com">Pixabay</a>  
-  <a href="https://svgrepo.com">SVG Repo</a>  
-  <a href="https://svgsilh.com">SVG Silh</a>  
-  <a href="https://uxwing.com">Uxwing</a>  
-  <a href="https://www.flaticon.es/">Flaticon</a>  
-  <a href="https://undraw.co/illustrations">unDraw</a>  
-  <a href="https://iconmonstr.com/">iconmonstr</a>  

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

## 4.4 - Usando la propiedad background-image
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


## 5.1 - Programar una imagen
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
Este concepto es similar al manejo de imágenes con la etiqueta **img**, donde los atributos **width** y **height** deben mantener la misma proporción que la imagen si no queremos que se produzcan distorsiones.  

A diferencia de la etiqueta **img**, la etiqueta **svg**, no produce deformación sino que se ajusta la porción visible.

Los navegadores se encargan de representar una sección del plano SVG con las proporciones de los atributos **width** y **height**, asegurándose de que incluya el área definida por el atributo **viewBox**.

**Ejemplo 1**
En este ejemplo solo vemos el círculo central.
```
<svg version="1.1" xmlns="http://www.w3.org/2000/svg" width="400" height="400" viewBox="-25 -25 50 50">
  <circle cx="-50" cy="0" r="25" fill="none" stroke="blue" stroke-width="2" />
  <circle cx="50" cy="0" r="25" fill="none" stroke="blue" stroke-width="2" />
  <circle cx="0" cy="-50" r="25" fill="none" stroke="green" stroke-width="2" />
  <circle cx="0" cy="50" r="25" fill="none" stroke="green" stroke-width="2" />
  <circle cx="0" cy="0" r="25" fill="none" stroke="red" stroke-width="2" />
</svg>
```

**Ejemplo 2**
En este ejemplo vemos los 4 círculos.
```
<svg version="1.1" xmlns="http://www.w3.org/2000/svg" width="150" height="150" viewBox="-75 -75 150 150">
  <circle cx="-50" cy="0" r="25" fill="none" stroke="blue" stroke-width="2" />
  <circle cx="50" cy="0" r="25" fill="none" stroke="blue" stroke-width="2" />
  <circle cx="0" cy="-50" r="25" fill="none" stroke="green" stroke-width="2" />
  <circle cx="0" cy="50" r="25" fill="none" stroke="green" stroke-width="2" />
  <circle cx="0" cy="0" r="25" fill="none" stroke="red" stroke-width="2" />
</svg>
```

>Actividad:
>Modificar el programa anterior para que solo se vean los circulos horizontales.
>Repetir la edición del programa para que solo se vean los circulos verticales.
>Analizar los resultados obtenidos.

### 5.1.4 - Margenes del viewBox
Para asegurarse de que todo el dibujo sea visible, es conveniente elegir un viewbox un poco más grande que la zona ocupada por los elementos del dibujo.  

En los siguientes ejemplos vemos como variando los argumentos pasados a viewBox ya no tenemos recortes del espesor del círculo.  

```
<svg version="1.1" xmlns="http://www.w3.org/2000/svg" width="400" height="400" viewBox="-25 -25 50 50">
  <circle cx="0" cy="0" r="25" fill="none" stroke="red" stroke-width="2" />
</svg>

<svg version="1.1" xmlns="http://www.w3.org/2000/svg" width="400" height="400" viewBox="-26 -26 52 52">
  <circle cx="0" cy="0" r="25" fill="none" stroke="red" stroke-width="2" />
</svg>
```

### 5.1.5 Formas básicas de SVG
Las formas básicas SVG son:
-  La línea <line ... />  
-  La polilínea <polyline ... />  
-  El círculo <circle ... />
-  La elipse <ellipse ... />,
-  El rectángulo <rect ... />
-  El polígono <polygon ... />  

**1. Línea** `<line ... />`
   -  La etiqueta <line /> dibuja una línea recta.  
   -  Los atributos principales propios de <line /> son:  
     -  (x1, y1): coordenadas del punto de inicio.   
     -  (x2, y2): coordenadas del punto final.
   - Sintaxis:
```
<svg>
  <line x1="" y1=""
      x2="" y2=""
      stroke=""
      stroke-width=""/>
</svg>
```    

**2. Polilínea** `<polyline ... />`
   -  La etiqueta <polyline /> dibuja un polígono abierto.  
   -  Los atributos principales propios de <polyline /> son:  
     -  (x1, y1) (x2, y2) (x3, y3) ... (xn, yn): Coordenadas de los puntos sucesivos de la polilínea.
  - Sintaxis:    
```
<svg>
  <polyline points="" style=""/>
</svg>
```

**3. Círculo** `<circle ... />`
   -  La etiqueta <circle /> dibuja un circulo.
   -  Los atributos principales propios de <cicle /> son:
     - (cx, cy): Coordenada y del centro y `r` (radio).
   - Sintaxis:
```
<svg>
  <circle cx="" cy="" r="" style=""/>
</svg>
```  
  
**4. Elipse** `<ellipse ... />`
   -  La etiqueta <ellipse /> dibuja una elipse.
   -  Los atributos principales propios de <cicle /> son:
     - (cx, cy): Coordenada y del centro.
     - `rx` (radio en dirección x)
     - `ry` (radio en dirección y)      
   - Sintaxis:
```
<svg>
  <ellipse cx="" cy="" rx="" ry="" style=""/>
</svg>
```
     
**5. Rectángulo** `<rect ... />`
   -  La etiqueta <rect /> dibuja un rectángulo.
   -  Los atributos principales propios de <rec /> son:
     - (x, y): Coordenadas la **esquina superior izquierda** del rectángulo
     - width: anchura del rectángulo
     - height: altura del rectángulo
     - rx: radio horizontal de las esquinas redondeadas
     - ry: radio vertical de las esquinas redondeadas
  - Sintaxis:
```
<svg>
  <rect x="" y="" width="" height="" style=""/>
</svg>
```
    
**6. Polígono** `<polygon .../>`
   - La etiqueta <polygon /> dibuja un poligono cerrado.
   - Los atributos principales de <polygon /> son:
      -  (x1, y1) (x2, y2) (x3, y3) ... (xn, yn): Coordenadas de los puntos sucesivos del polígono.
      -  El último punto (xn, yn) se une automáticamente con el primero (x1, y1).
   - Sintaxis:
```
<svg>
  <polygon points="" style=""/>
</svg>
```  

### 5.1.6 Ejercicios

-  #### 1. Dibuja una línea horizontal que conecte dos puntos en una vista de 300x100.

-  #### 2. Dibuja una polilínea que forma un zigzag entre varios puntos.

-  #### 3. Dibuja un círculo de radio 50 en el centro de un área de 200x200.

-  #### 4. Crea una elipse centrada con un radio horizontal de 70 y un radio vertical de 40.

-  #### 5. Dibuja un rectángulo de 150x100 con esquinas redondeadas en un área de 300x200.

-  #### 6. Crea un triángulo equilátero utilizando la etiqueta `<polygon />`.

-  #### 7. Dibuja una cruz usando dos líneas que se cruzan en el centro del área de 100x100.

-  #### 8. Crea una polilínea con curvas suaves.
>Nota: Para redondear las esquinas, usar `stroke-width`.

-  #### 9. Dibuja un rectángulo.

-  #### 10. Utiliza el elemento `<polygon />` para dibujar una estrella de 5 puntas.
        
### 5.1.7 Formas avanzadas de SVG: Etiqueta <path ... />
La etiqueta `<path />` define una forma mediante una serie de comandos que describen movimientos y dibujos en el espacio. A diferencia de otras etiquetas de SVG más simples <path /> **permite dibujar cualquier forma imaginable**.

[Editor de path](https://yqnn.github.io/svg-path-editor/)

**1. Etiqueta** `<path />`  
-  La etiqueta `<path />` utiliza un atributo principal llamado `d`, el cual contiene una lista de comandos y parámetros. Estos comandos indican cómo moverse y dibujar en el área gráfica.

**2. Comandos Básicos de** `<path />`
Los comandos se dividen en dos grupos: 
-  **Comandos en mayúsculas:** Utilizan coordenadas absolutas. Es decir, siempre se refieren al origen del gráfico. 
-  **Comandos en minúsculas:** Utilizan coordenadas relativas. Es decir, siempre se refieren desde donde se encuentra el puntero. 

| Comando | Parámetros                                   | Nombre                            | Descripción                                                                                                           |
|------|----------------------------------------------|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| M    | x,y                                          | moveto                            | Mueve el puntero al punto especificado x,y **sin dibujar**.                                                                 |
| m    | x,y                                          | moveto                            | Mueve el puntero al punto especificado x,y relativo a la ubicación actual del puntero, **sin dibujar**.                        |
| L    | x,y                                          | lineto                            | Dibuja una línea desde la ubicación actual del puntero hasta el punto especificado x,y.                                  |
| l    | x,y                                          | lineto                            | Dibuja una línea desde la ubicación actual del puntero hasta el punto especificado x,y relativo a la ubicación actual.   |
| H    | x                                            | horizontal lineto                 | Dibuja una línea horizontal hasta el punto definido por (x especificado, y actual del puntero).                         |
| h    | x                                            | horizontal lineto                 | Dibuja una línea horizontal hasta el punto definido por (x actual del puntero + x especificado, y actual del puntero).    |
| V    | y                                            | vertical lineto                   | Dibuja una línea vertical hasta el punto definido por (x actual del puntero, y especificado).                           |
| v    | y                                            | vertical lineto                   | Dibuja una línea vertical hasta el punto definido por (x actual del puntero, y actual del puntero + y especificado).      |
| C    | x1,y1 x2,y2 x,y                              | curveto                           | Dibuja una curva de Bézier cúbica desde el punto actual hasta x,y. x1,y1 y x2,y2 son los puntos de control de la curva.|
| c    | x1,y1 x2,y2 x,y                              | curveto                           | Igual que C, pero interpreta las coordenadas relativas al punto actual del puntero.                                     |
| S    | x2,y2 x,y                                    | shorthand / smooth curveto        | Dibuja una curva de Bézier cúbica hasta x,y. x2,y2 es el punto de control final, el inicial es el final de la curva anterior.|
| s    | x2,y2 x,y                                    | shorthand / smooth curveto        | Igual que S, pero interpreta las coordenadas relativas al punto actual del puntero.                                     |
| Q    | x1,y1 x,y                                    | quadratic Bezier curveto          | Dibuja una curva de Bézier cuadrática desde el punto actual hasta x,y. x1,y1 es el punto de control de la curva.      |
| q    | x1,y1 x,y                                    | quadratic Bezier curveto          | Igual que Q, pero interpreta las coordenadas relativas al punto actual del puntero.                                     |
| T    | x,y                                          | shorthand / smooth quadratic curveto | Dibuja una curva de Bézier cuadrática hasta x,y. El punto de control es el mismo que el último usado.                |
| t    | x,y                                          | shorthand / smooth quadratic curveto | Igual que T, pero interpreta las coordenadas relativas al punto actual del puntero.                                     |
| A    | rx,ry x-axis-rotation large-arc-flag, sweepflag x,y | elliptical arc                  | Dibuja un arco elíptico desde el punto actual hasta x,y. rx y ry son los radios de la elipse.                         |
| a    | rx,ry x-axis-rotation large-arc-flag, sweepflag x,y | elliptical arc                  | Igual que A, pero interpreta las coordenadas relativas al punto actual del puntero.                                     |
| Z    |                                              | closepath                         | Cierra el camino dibujando una línea desde el punto actual al primer punto.                                           |
| z    |                                              | closepath                         | Cierra el camino dibujando una línea desde el punto actual al primer punto.                                           |

**3. Sintaxis de** `<path />`  
La sintaxis del elemento path es como sigue:  
```
<path d="conjunto de comandos" />
```
Donde el conjunto de comandos está formado por los comandos moveto, lineto, curveto, arc y closepath.

-  **Ejemplo**
>Nota: Archivo disponible en /html/index_path.html 
```
<path d="M10,40 L40,40 L40,80 L80,80 L80,120 L120,120 L120,160 L40,160" />
```
**Significado del código:**
-  **moveto M (10,40):** Desplaza el cursor al punto (10,40). Sin **dibujar nada**.
-  **Lineto L (40,40):** Dibuja una línea entre el punto actual (10,40) y el punto especificado (40,40).
-  **Lineto L (40,80):** Dibuja una línea entre el punto actual (40,40) y el punto especificado (40,80).
-  **Lineto L (80,80):** Dibuja una línea entre el punto actual (40,80) y el punto especificado (80,80).
-  **Lineto L (80,120):** Dibuja una línea entre el punto actual (80,80) y el punto especificado (80,120).
-  **Lineto L (120,120):** Dibuja una línea entre el punto actual (80,120) y el punto especificado (120,120).
-  **Lineto L (120,160):** Dibuja una línea entre el punto actual (120,120) y el punto especificado (120,160).
-  **Lineto L (40,160):** Dibuja una línea entre el punto actual (120,160) y el punto especificado (40,160).

 lineto. L x y Dibuja una línea entre el punto actual y el punto especificado (x,y).

**Resultado:**  

<img src="https://github.com/javieregeablasco/DAW/blob/main/DIW/UT.%204/img/path.png" width=50%>

#### 5.1.7.1 Buenas prácticas y simplificación del código

-  **Etiqueta `<g>` en SVG**  
    -  La etiqueta `<g>` en SVG se utiliza para agrupar elementos gráficos. Como lo veremos más adelante (aunque ya lo estemos usando), esto permite aplicar transformaciones, estilos y atributos de manera conjunta a todos los elementos de un grupo.  
    -  Al usar `<g>`, se organiza mejor el contenido SVG, facilitando la manipulación y el mantenimiento del código. 

    -  **Ejemplo de uso de <g>:**

```
<svg width="200" height="200" xmlns="http://www.w3.org/2000/svg">
    <g fill="blue" stroke="black" stroke-width="2">
        <circle cx="50" cy="50" r="30"/>
        <rect x="100" y="20" width="60" height="60"/>
    </g>
</svg>
```

- **Evitar repeticiones dentro del comando <path>**  
    -  Al definir un `<path>` en SVG se dan muchas veces la circunstancia que se aplica el mismo comando varias veces **seguidas**.
    -  En este caso se puede optar por repetir el comando tantas veces como sea necesario. Eso puede dar **claridad en la Sintaxis** pero también sobrecargar el código.
    -  También se puede optar por omitir el comando. Entonces se considera, de manera implicita que los siguientes puntos introducidos tendrán el mismo comando.

    -  **Ejemplo de omisión del comando:**
>Repitiendo comandos.
```
<path d="M 10 10 C 20 20, 40 20, 50 10 C 60 0, 80 0, 90 10 C 40 60, 80 120, 30 90 Z" fill="none" stroke-width="1" stroke="black" />
```
>Sin repetir comandos.
```
<path d="M 10 10 C 20 20, 40 20, 50 10 60 0, 80 0, 90 10 40 60, 80 120, 30 90 Z" fill="none" stroke-width="1" stroke="black" />
```

#### 5.1.7.2 Diferencias entre coordenadas absolutas y relativas, ejemplo con lineto L y l
-  **Ejemplo usando lineto L**
```
<!-- Usando L (línea absoluta) -->
<path d="M10,50 L100,50 L100,150 L10,150 Z" fill="none" stroke="blue" stroke-width="2" />
<text x="10" y="40" font-size="12" fill="blue">Absoluto (L)</text>
```
**Explicación:**  
El cuadrado azul usa el comando `L` (absoluto), lo que significa que cada **coordenada especificada** es en relación al **sistema de coordenadas general** del SVG.  

-  **Ejemplo usando lineto l**
```  
<!-- Usando l (línea relativa) -->
<path d="M150,50 l90,0 l0,100 l-90,0 Z" fill="none" stroke="red" stroke-width="2" />
<text x="150" y="40" font-size="12" fill="red">Relativo (l)</text>
```
**Explicación:** 
El cuadrado rojo usa el comando `l` (relativo), lo que significa que las coordenadas son relativas al último punto en el que se trazó una línea. En este caso, las líneas se dibujan comenzando desde el punto inicial `M150,50`, y luego se desplazan de forma relativa a ese punto.

-  **Resultado**  
<img src="https://github.com/javieregeablasco/DAW/blob/main/DIW/UT.%204/img/html%20lineto.png" width=50%>

#### 5.1.7.3 Comando curveto C - curva cúbica de Bézier.
-  **Teoría.**  
Cuatro puntos del plano: P0, P1, P2 y P3 definen una curva cúbica de Bézier. La curva empieza en el punto P0, se dirige hacia P1 y llega a P3 viniendo de la dirección del punto P2. Usualmente, no pasará ni por P1 ni por P2. Estos puntos sólo están ahí para proporcionar información direccional.
<div align="center">
<img src="https://upload.wikimedia.org/wikipedia/commons/d/d0/Bezier_curve.svg" width=35%>
</div>

-  Las curvas de bezier cuadráticas se dibujan de la siguiente manera.  
<div align="center">
<img src="https://upload.wikimedia.org/wikipedia/commons/d/db/B%C3%A9zier_3_big.gif">
</div>
 
-  **Ejemplo**
```
<svg width="200" height="200" xmlns="http://www.w3.org/2000/svg">
    <g>
      <path d="M 30 270
               C 40 10, 65 10, 270 270 
               " 
      stroke="blue" 
      fill="transparent"
      stroke-width="2"/>
    </g>

    <g stroke-width="1" stroke="rgba(255, 0, 0, 0.25)">
      <line x1="30" y1="270" x2="40" y2="10"/>
      <line x1="270" y1="270" x2="40" y2="10"/>
    </g>
     
    <g stroke-width="1" stroke="lightblue">
      <line x1="30" y1="270" x2="65" y2="10"/>
      <line x1="270" y1="270" x2="65" y2="10"/>
    </g>
</svg>
```
-  **Explicación del código**
> `M 30 270`: Mueve el punto de inicio del camino a las coordenadas (30, 270).
> `C 40 10, 65 10, 95 80`: Dibuja una curva cúbica desde **el punto actual hasta el punto (270, 270),** utilizando los puntos de control (40, 10) y (65, 10) para definir la forma de la curva.

-  **Resultado**

<img src="https://github.com/javieregeablasco/DAW/blob/main/DIW/UT.%204/img/curvaC.png" width=50%>


#### 5.1.7.4 Comando smooth curveto S.  
- **Teoría**
  -  Dibuja una curva cúbica de Bézier desde el punto actual (x,y) hasta un punto (x2,y2).
  -  **El primer punto de anclaje es el reflejo del segundo punto de anclaje de la curva anterior.**
  -  Si no hay segundo punto de la curva anterior se toma el mismo punto de anclaje para `P-1` y `P1`.   
  -  x1,y1 son las coordenadas del segundo punto de anclaje (control point) P1.
  
-  Dibujado con solo un punto de control.  
<div align="center">
<img src="https://upload.wikimedia.org/wikipedia/commons/3/3d/B%C3%A9zier_2_big.gif">
</div>

- **Ejemplo con curva C anterior disponible.** 
```
<svg width="305" height="200" xmlns="http://www.w3.org/2000/svg">
  <!-- Ejes de referencia -->
  <line x1="0" y1="100" x2="300" y2="100" stroke="gray" stroke-width="1" />
  <line x1="150" y1="0" x2="150" y2="200" stroke="gray" stroke-width="1" />
    
  <!-- Curva cúbica suavizada -->
  <path d="M 50 150 C 100 50, 150 50, 150 100 S 250 150, 300 100" fill="transparent" stroke="blue" stroke-width="2" />
       
  <!-- Puntos de control -->
  <circle cx="50" cy="150" r="3" fill="red" />
  <circle cx="100" cy="50" r="3" fill="green" />
  <circle cx="150" cy="50" r="3" fill="green" />
  <circle cx="250" cy="150" r="3" fill="green" />
  <circle cx="300" cy="100" r="3" fill="red" />

  <!-- Linea punto de control P1 -->
  <line x1="250" y1="150"
    x2="300" y2="100"
    stroke="gray"
    stroke-width="1"/>
</svg>
```
-  **Resultado**  
<img src="https://github.com/javieregeablasco/DAW/blob/main/DIW/UT.%204/img/smoothCurvetoSgrid.png" width=50%>

- **Ejemplo sin curva C anterior disponible.** 
```
<svg>
  <!-- Ejes de referencia -->
  <line x1="0" y1="100" x2="300" y2="100" stroke="gray" stroke-width="1" />
  <line x1="150" y1="0" x2="150" y2="200" stroke="gray" stroke-width="1" />
  
  <!-- Curva cúbica suavizada -->
  <path d="M 40 180 S 150 50, 330 150" fill="transparent" stroke="blue" stroke-width="2" />
    
  <!-- Puntos de referencia -->
  <circle cx="40" cy="180" r="3" fill="red" />
  <circle cx="150" cy="50" r="3" fill="green" />
  <circle cx="330" cy="150" r="3" fill="red" />

  <!-- Lineas a puntos de control -->
  <line x1="40" y1="180"
        x2="150" y2="50"
        stroke="gray"
        stroke-width="1"/>
  <line x1="150" y1="50"
        x2="330" y2="150"
        stroke="gray"
        stroke-width="1"/>
</svg>
```
-  **Resultado**
<img src="https://github.com/javieregeablasco/DAW/blob/main/DIW/UT.%204/img/smoothCurvetoSgrid2.png" width=50%>

#### 5.1.7.5 Comando quadratic Bezier curveto Q.
-  **Teoría**  
Tres puntos del plano: a, pc y z definen una curva cuadrática de Bézier. La curva empieza en el punto a, se dirige hacia pc ( punto de control ) y llega a z viniendo de la dirección del punto de control. Usualmente, no pasará por pc. Este punto sólo proporciona información direccional.  
La línea recta que une cada uno de los puntos finales de la curva ( a y z ) con su correspondiente punto de control ( pc ) es tangente a la curva.

- **Ejemplo** 
```
<svg width="200" height="200" xmlns="http://www.w3.org/2000/svg">
  <!-- Ejes de referencia -->
  <line x1="0" y1="100" x2="300" y2="100" stroke="gray" stroke-width="1" />
  <line x1="150" y1="0" x2="150" y2="200" stroke="gray" stroke-width="1" />
          
  <!-- Curva cuadrática Bézier -->
  <path d="M 40 180 Q 150 50, 330 150" fill="transparent" stroke="blue" stroke-width="2" />
            
  <!-- Puntos de control -->
  <circle cx="40" cy="180" r="3" fill="red" />
  <circle cx="150" cy="50" r="3" fill="green" />
  <circle cx="330" cy="150" r="3" fill="red" />
          
 <!-- Lineas a puntos de control -->
 <line x1="40" y1="180"
       x2="150" y2="50"
       stroke="gray"
       stroke-width="1"/>
 <line x1="150" y1="50"
       x2="330" y2="150"
       stroke="gray"
       stroke-width="1"/>
</svg>
```
-  **Resultado**  
<img src="https://github.com/javieregeablasco/DAW/blob/main/DIW/UT.%204/img/CurvetoQgrid.png" width=50%>

#### 5.1.7.6 Comando quadratic Bezier curveto T.
-  Teoria
T (smooth quadratic curveto), toma automáticamente el punto de control de la curva cuadrática anterior, permitiendo que la curva **continúe suavemente**.


```
<svg>
  <!-- Ejes de referencia -->
  <line x1="0" y1="100" x2="400" y2="100" stroke="gray" stroke-width="1" />
  <line x1="150" y1="0" x2="150" y2="200" stroke="gray" stroke-width="1" />
            
  <!-- Curva cuadrática Bézier (Q) -->
  <path d="M 40 180 Q 150 50, 330 150 T 400 50" fill="transparent" stroke="blue" stroke-width="2" />
             
  <!-- Puntos de control -->
  <circle cx="40" cy="180" r="3" fill="red" />
  <circle cx="150" cy="50" r="3" fill="green" />
  <circle cx="330" cy="150" r="3" fill="red" />
  <circle cx="400" cy="50" r="3" fill="green" />
            
   <!-- Líneas a puntos de control -->
   <line x1="40" y1="180"
         x2="150" y2="50"
         stroke="gray"
         stroke-width="1"/>
   <line x1="150" y1="50"
         x2="330" y2="150"
         stroke="gray"
         stroke-width="1"/>
</svg>
```

- **Resultado**
<img src="https://github.com/javieregeablasco/DAW/blob/main/DIW/UT.%204/img/CurvetoTgridSmooth.png" width=50%>

## 5.1.8 Ejercicio
Realiza un SVG **usando path** replicando el logo de la banda musical Dûrga de Valencia.  
El logo en cuestión es el siguiente:  

<img src="https://github.com/javieregeablasco/DAW/blob/main/DIW/UT.%204/img/logoDurga.png" width=50%>

**Nota**  
Aun no hemos visto como aplicar estilos a svg.  
Para aplicar el color y el grosor de linea usar: stroke-width="4" stroke="#D9C472"  

**Ejemplo**
```
<svg width="200" height="200" xmlns="http://www.w3.org/2000/svg">
  <path d="M 10 10 L 190 10 L 190 190 L 10 190 Z" 
    stroke="#D9C472" 
    fill="transparent" 
    stroke-width="4"/>
</svg>
```

## 5.2 Atributos / estilos para SVG
### 5.2.1 Atributos SVG  
-  **Atributo stroke**   
El atributo **stroke** permite definir el color del trazo del elemento.

```
<svg viewBox="0 0 45 45" height="300" style="background:#aaa">
  <rect x="5" y="5" width="15" height="15" stroke="purple" />
  <rect x="25" y="5" width="15" height="15" stroke="red" />
  <rect x="5" y="25" width="15" height="15" stroke="deeppink" />
  <rect x="25" y="25" width="15" height="15" stroke="gold" />
</svg>
```  

-  **Atributo stroke-width**   
El atributo **stroke-width** permite modificar el grosor del trazo del elemento.

```
<svg viewBox="0 0 45 45" height="300" style="background:#aaa">
  <rect x="5" y="5" width="15" height="15" stroke="purple" stroke-width="0" />
  <rect x="25" y="5" width="15" height="15" stroke="red" stroke-width="1" />
  <rect x="5" y="25" width="15" height="15" stroke="deeppink" stroke-width="2" />
  <rect x="25" y="25" width="15" height="15" stroke="gold" stroke-width="6" />
</svg>
```  

-  **Atributo stroke-opacity**  
El atributo **stroke-opacity** permite establecer la opacidad del elemento (grado de transparencia). El valor a indicar es un número entre 0 y 1, con decimales (0 totalmente transparente y 1 es totalmente opaco).

```
<svg viewBox="0 0 45 45" height="300" style="background:#aaa">
  <rect x="5" y="5" width="15" height="15" stroke="red" stroke-opacity="0" />
  <rect x="25" y="5" width="15" height="15" stroke="red" stroke-opacity="0.25" />
  <rect x="5" y="25" width="15" height="15" stroke="red" stroke-opacity="0.5" />
  <rect x="25" y="25" width="15" height="15" stroke="red" stroke-opacity="1" />
</svg>
```

-  **Atributo stroke-linecap**  
Con **stroke-linecap** se indica la forma de los extremos de los trazos.  
Posibles valores de stroke-linecap:
    - `butt`, prederminado.
    - `round`, el extremo de la línea es redondeado.
    - `square`, el extremo de la línea es cuadrado.

```
<svg viewBox="0 0 30 30" height="300" style="background:#aaa">
  <path d="M5 5 L25 5" stroke="black" stroke-width="3" stroke-linecap="butt" />
  <path d="M5 15 L25 15" stroke="darkred" stroke-width="3" stroke-linecap="round" />
  <path d="M5 25 L25 25" stroke="purple" stroke-width="3" stroke-linecap="square" />
</svg>

<svg viewBox="0 0 30 30" height="300" style="background:#aaa">
  <path d="M15 5 L15 5" stroke="black" stroke-width="3" stroke-linecap="butt" />
  <path d="M15 15 L15 15" stroke="darkred" stroke-width="3" stroke-linecap="round" />
  <path d="M15 25 L15 25" stroke="purple" stroke-width="3" stroke-linecap="square" />
</svg>
```

-  **Atributo stroke-linejoin**  
Con **stroke-linejoin** se puede definir como serán las uniones de dos trayectos o dos lineas, y como se mostrarán.
Posibles valores de stroke-linejoin:


La propiedad `stroke-linejoin` en SVG define cómo se renderizan las uniones entre dos segmentos de una línea o trazo. Es útil cuando el contorno de una figura tiene esquinas o ángulos, y esta propiedad controla cómo se dibujan esos puntos de unión.

Los posibles valores de `stroke-linejoin` son:  
    - `miter`, predeterminado. Los segmentos de línea se unen en un punto afilado o en ángulo extendido, creando una esquina que puede sobresalir. Si el ángulo entre las líneas es muy agudo, la longitud de la unión puede limitarse utilizando la propiedad `stroke-miterlimit`.    
    - `bevel`. Los segmentos de línea se unen mediante un corte recto, creando una esquina "plana" o biselada. El punto de unión no es afilado como en `miter`, sino truncado.    
    - `miter-clip`. La unión se recorta si el ángulo es demasiado pequeño, evitando una esquina demasiado larga y afilada.
    - `round`. Los segmentos de línea se unen con un borde redondeado en las esquinas.  
   
```
<svg viewBox="0 0 300 100" width="1200" height="400">
 
  <path d="M5 60 l20 -5 l-3 20" stroke="blue" stroke-width="2" stroke-linejoin="miter" />
  <text x="5" y="90">miter</text>
    
  <path d="M55 60 l20 -5 l-3 20" stroke="blue" stroke-width="2" stroke-linejoin="round" />
  <text x="55" y="90">round</text>
    
  <path d="M105 60 l20 -5 l-3 20" stroke="blue" stroke-width="2" stroke-linejoin="bevel" />
  <text x="105" y="90">bevel</text>
   
  <path d="M155 60 l20 -5 l-3 20" stroke="blue" stroke-width="2" stroke-linejoin="miter-clip" />
  <text x="155" y="90">miter-clip</text>

</svg>
```

-  **Atributo stroke-misterlimit**













Aplicar estilos CSS a un SVG es similar a aplicar estilos a cualquier otro elemento HTML. 

### 1. **Estilos inline (en línea)**
Se aplican directamente a los elementos SVG usando el atributo `style`. Es la forma más directa, pero no la más reutilizable:

```html
<svg width="200" height="200">
  <circle cx="100" cy="100" r="50" style="fill: blue; stroke: black; stroke-width: 2;" />
</svg>
```

### 2. **Estilos usando atributos de presentación**
Los atributos de presentación son atributos SVG que pueden aplicarse a los elementos para definir sus estilos directamente (funciona similar al estilo inline pero sin usar el atributo `style`):

```html
<svg width="200" height="200">
  <circle cx="100" cy="100" r="50" fill="blue" stroke="black" stroke-width="2" />
</svg>
```

### 3. **Estilos en el archivo CSS externo o interno**
Puedes definir un archivo CSS externo o incluir reglas CSS en un bloque `<style>` dentro del documento para aplicar estilos a los elementos SVG utilizando selectores, clases, e identificadores (`id`), lo que permite reutilizar estilos.

**Archivo CSS externo o interno:**
```html
<svg width="200" height="200" xmlns="http://www.w3.org/2000/svg">
  <circle class="blue-circle" cx="100" cy="100" r="50" />
</svg>

<style>
  .blue-circle {
    fill: blue;
    stroke: black;
    stroke-width: 2;
  }
</style>
```

En este caso, se utiliza una clase `.blue-circle` en el CSS, que luego es asignada al elemento `<circle>` en el SVG.

### 4. **Estilos CSS en un archivo SVG independiente**
Cuando el SVG es un archivo independiente, puedes incluir el bloque `<style>` directamente en el archivo SVG, similar a un documento HTML:

```xml
<svg width="200" height="200" xmlns="http://www.w3.org/2000/svg">
  <style>
    .blue-circle {
      fill: blue;
      stroke: black;
      stroke-width: 2;
    }
  </style>
  <circle class="blue-circle" cx="100" cy="100" r="50" />
</svg>
```

### 5. **Estilos con pseudo-clases**
Puedes usar pseudo-clases como `:hover`, `:active`, o `:focus` para los elementos dentro de un SVG de la misma manera que lo harías con elementos HTML.

```html
<svg width="200" height="200" xmlns="http://www.w3.org/2000/svg">
  <circle class="interactive-circle" cx="100" cy="100" r="50" />
</svg>

<style>
  .interactive-circle {
    fill: blue;
    stroke: black;
    stroke-width: 2;
    transition: fill 0.3s;
  }

  .interactive-circle:hover {
    fill: red;
  }
</style>
```

En este ejemplo, el color de relleno del círculo cambia a rojo cuando se pasa el ratón por encima del elemento.

### 6. **Estilos aplicados a grupos (elemento `<g>`)**
Puedes agrupar elementos SVG dentro de un contenedor `<g>` y aplicar estilos a todo el grupo, de manera similar a como se hace en HTML con divs o contenedores:

```html
<svg width="200" height="200" xmlns="http://www.w3.org/2000/svg">
  <g class="group-style">
    <circle cx="50" cy="50" r="40" />
    <rect x="100" y="100" width="50" height="50" />
  </g>
</svg>

<style>
  .group-style {
    fill: blue;
    stroke: black;
    stroke-width: 2;
  }
</style>
```

Todos los elementos dentro del grupo `<g>` reciben los mismos estilos, lo que permite organizar y aplicar estilos de manera eficiente.

### Propiedades CSS comunes en SVG:
- **`fill`**: Define el color de relleno del interior de una figura.
- **`stroke`**: Define el color del borde de una figura.
- **`stroke-width`**: Define el grosor del borde.
- **`opacity`**: Define la opacidad de un elemento.
- **`fill-opacity` y `stroke-opacity`**: Controlan la opacidad del relleno o del borde por separado.
- **`transform`**: Permite aplicar transformaciones como rotaciones, escalados o traslaciones a los elementos SVG.

### Consideraciones
- No todos los estilos CSS de HTML son compatibles con SVG (por ejemplo, `box-shadow` no funcionará en la mayoría de los elementos SVG).
- Es importante usar correctamente el espacio de nombres `xmlns="http://www.w3.org/2000/svg"` cuando uses SVG embebido en HTML para garantizar la compatibilidad.

Así puedes aplicar estilos flexibles y reutilizables a tus gráficos SVG.

