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
