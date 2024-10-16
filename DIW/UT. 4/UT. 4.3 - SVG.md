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


























 
##### 3.3. **Sintaxis de SVG**
SVG utiliza una estructura XML para describir formas geométricas como rectángulos, círculos, líneas y rutas. Algunos elementos básicos son:
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

##### 3.4. **Integración de SVG en HTML**
Existen varias maneras de integrar SVG en un documento HTML:
- **Incrustado directamente en el HTML**: El código SVG se coloca dentro del archivo HTML, lo que permite manipular el SVG mediante CSS y JavaScript.
- **Mediante archivo externo**: Se puede incluir un archivo SVG como si fuera una imagen con la etiqueta `<img>`, o como un fondo mediante CSS.

##### 3.5. **Ventajas del uso de SVG en aplicaciones web**
- **Calidad de imagen superior**: Ideal para gráficos como logotipos, íconos o gráficos que requieren alta definición.
- **Reducción del tamaño de archivo**: Aumenta el rendimiento de la web al reducir el peso total de la página.
- **Compatibilidad con CSS y JavaScript**: Permite cambiar estilos y añadir animaciones sin necesidad de librerías externas.

##### 3.6. **Manipulación de SVG con CSS y JavaScript**
SVG permite aplicar estilos directamente desde CSS y modificar atributos dinámicamente usando JavaScript. Ejemplos de efectos comunes son:
- Cambios de color al pasar el cursor (hover).
- Animación de transformaciones (rotar, escalar).
- Cambios dinámicos en la posición o dimensiones de los elementos gráficos.

#### 4. **Actividades**
1. **Crear un logo en SVG**: Los alumnos diseñarán un logotipo sencillo en SVG usando formas básicas y lo integrarán en una página web.
2. **Manipulación de SVG con CSS**: Aplicar estilos y animaciones a un SVG embebido en HTML utilizando propiedades como `fill`, `stroke`, y `transform`.
3. **Interactividad con JavaScript**: Crear un gráfico SVG interactivo donde al hacer clic sobre ciertas áreas se generen diferentes acciones (por ejemplo, mostrar alertas o modificar colores).

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



https://kinsta.com/es/base-de-conocimiento/como-abrir-un-archivo-svg/

https://developer.mozilla.org/es/docs/Web/SVG/Tutorial

https://jenkov.com/tutorials/svg/index.html

https://www.w3.org/2002/Talks/www2002-svgtut-ih/hwtut.pdf

https://www.tutorialspoint.com/svg/index.htm

https://flaviocopes.com/svg/

https://kurtbruns.github.io/svg-tutorial/

https://www.svgbasics.com/index.html

https://www.aleksandrhovhannisyan.com/blog/svg-tutorial/
