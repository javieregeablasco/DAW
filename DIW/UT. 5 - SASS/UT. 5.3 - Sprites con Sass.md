---
Título: UD. 5.3 - Sprites con Sass 
Autor: Javier Egea Blasco
Año: 24-25
Palabras clave: DAW, DIW
---

# 1 Introducción
## 1.1 ¿Qué es un sprite?
Un sprite es una imagen que contiene **múltiples gráficos pequeños combinados en una sola imagen**. Mediante CSS y Sass (para simplificar su uso), se pueden mostrar solo las partes específicas de la imagen que se necesitan.
**Ejemplo de sprite**  

## 2.2 ¿Por qué usar sprites?
Los origines de los sprites emergen de las conexiones a internet deficientes y de la necesidad de mejorar el rendimiento y la eficiencia de cargar de las páginas web. 

## 2.3 Ventajas de usar sprites
- **Reducción de solicitudes al servidor:** Al solo usar una imágen (multiple), se disminuye el número de peticiones HTTP.
- **Optimización del rendimiento:** Menos peticiones significa tiempos de carga más rápidos.
- **Consistencia visual:** Los sprites aseguran que todas las imágenes se carguen al mismo tiempo, evitando que algunos íconos se queden en blanco mientras se descargan.
- **Facilidad de mantenimiento:** Permiten centralizar la gestión de gráficos pequeños en un solo archivo, haciendo más fácil actualizarlos o reemplazarlos.

## 2.4 Formatos de imágenes admisibles  
Todos los formatos son admisibles pero los sprites se usan principalmentes con png y svg.
- **PNG:**
  - Es el formato más utilizado para sprites tradicionales debido a su soporte para transparencia y alta calidad de imagen.
  - Es ideal para gráficos pequeños como íconos y botones.

- **SVG:**  
  - Muy popular para sprites modernos, especialmente en gráficos escalables y dinámicos, ya que es un formato basado en vectores.
  - Ofrece flexibilidad en términos de edición, animación y calidad sin pérdida de resolución.

- **Otros formatos (JPG, GIF):**  
   - Técnicamente admisibles, pero menos comunes para sprites. El JPG no soporta transparencia, y el GIF es limitado en calidad y rendimiento.
