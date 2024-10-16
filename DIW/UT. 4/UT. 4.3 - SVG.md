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
Existen numerosos sitios web que ofrecen gráficos SVG listos para usar en proyectos. 

Flaticon
**SVGRepo**
Undraw
Iconmonstr


<a href="cocomaterial.com">**Coco Material**</a> 

**Free Icons:** freeicons.io.
**Game Icons:** game-icons.net.
Icon Duck: Una web con más de 100.000 iconos e imágenes SVG gratuitas y libres que puedes usar en cualquiera de tus proyectos. Están repartidas en paquetes temáticos, aunque también tienes un buscador para encontrar algo que se ajuste a tus necesidades. Web: iconduck.com.
Icon Finder: Este es un buscador de iconos e imágenes vectoriales con más de 5 millones de elementos a encontrar. La pega es que no solo verás iconos gratuitos, sino también otros que son de pago. Web: iconfinder.com.
Icons and Photos For Everything: Un buscador doble de recursos gratuitos, en el que puedes encontrar tanto fotos PNG como iconos SVG. Para ello tienes una barra de búsqueda en la que puedes especificar si buscar imágenes e iconos, luego escribes el término que quieras (principalmente en inglés) y verás los resultados. Web: thenounproject.com.
Patternpad: Esta es una página con la que vas a poder crear iconos e imágenes vectoriales por tu cuenta. Funciona a través de patrones que puedes personalizar a tu gusto, y cuando termines, te descargas el resultado. patternpad.com.
Pixabay: La popular página de Pixabay sirve para encontrar todo tipo de recursos e imágenes, algunas de pago y otras gratuitas y abiertas. Entre sus opciones está la de buscar gráficos vectoriales, que son los SVG, y eligiendo su pestaña en el buscador podrás encontrarlos de varias temáticas: Web: Pixabay.com.
SVG Repo: Un repositorio en el que encontrar una ingente cantidad de imágenes e iconos en formato SVG. Tienes un buscador y varios packs temáticos. Web: svgrepo.com.
SVG Silh: Un buscador de imágenes SVG e iconos. Como especial tiene que además de recurrir a su barra de búsqueda, vas a poder elegir el color en el que vas a querer cada imagen. No es un buscador por colores, sino que pinta todas las imágenes en el color que elijas. Web: svgsilh.com.
Uxwing: Una página con una colección exclusiva de iconos y gráficos vectoriales gratuitos, que puedes usar en negocios o propósitos comerciales sin necesidad de poner una atribución. Tienes una gran cantidad de sets, y una herramienta para personalizarlos. Web: uxwing.com.


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
