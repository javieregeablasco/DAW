---
Título: UD. 5.1 - SASS
Autor: Javier Egea Blasco
Año: 24-25
Palabras clave: DAW, DIW
---  

<div align="center">
</br>
<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/9/96/Sass_Logo_Color.svg/480px-Sass_Logo_Color.svg.png" width=25%>
</div>
 
# 1. Introducción
SASS es un preprocesador de CSS utilizado para traducir un código de hojas de estilo no estándar a un código CSS estándar, legible por la mayoría de los navegadores.  
La principal utilidad de SASS es la de hacer más simple la escritura del código CSS, además de brindar diversas utilidades que a día de hoy el CSS no puede ofrecer.

**Ventajas de utilizar SASS**
Las hojas de estilo de un sitio web cada vez son más complejas y difíciles de mantener. En este punto, un preprocesador de CSS puede ser de gran utilidad y SASS permite emplear funcionalidades que no existen en CSS. Algunas de las principales ventajas del uso de SASS serían:  
- **Establecer variables.**
  De manera similar a cualquier lenguaje de programación, las variables permiten guardar información y emplearlas cuándo sea necesario.
  
- **Anidación más simple.**
Usar anidamiento en SASS permite escribir el código CSS con la misma estructura visual que el HTML. De este modo, se simplifica el uso de los selectores y se ofrece a los programadores un formato más visual y jerarquizado para seleccionar elementos anidados.

Utilizar mixins.
Se trata de grupos de código que se definen con la norma @mixin seguida del nombre que quiera darse y que, posteriormente, se pueden emplear con la regla @include más el nombre que se haya establecido. El mixin es algo comparable a lo que sería una función en otro lenguaje de programación y permiten reutilizar secciones íntegras de código escribiendo funciones con los parámetros que se definan.

que-es-sass

Herencias.
A través de SASS será posible unificar declaraciones, otorgándoles un nombre que irá siempre precedido del signo del tanto por ciento (%). Después, a través de la regla @extend seguida del nombre de la declaración, será posible emplear esas órdenes. Su peculiaridad es que no se procesan si no se utilizan, por ello, el código procesado estará totalmente libre de declaraciones no empleadas.

Importar.
A través de la norma @import es posible dividir el código CSS en diferentes ficheros y esto constituye una ventaja, puesto que hace posible tener el código distribuido en varios ficheros y luego generar un solo CSS.

Rapidez.
Empleando SASS los desarrolladores ahorran mucho tiempo porque es posible acortar el código que deben escribir, así como el número de ficheros a implementar. Aumenta, por lo tanto, la productividad.
