---
Título: UD. 5.2 - SASS Práctica evaluable
Autor: Javier Egea Blasco
Año: 24-25
Palabras clave: DAW, DIW
--- 

# 1 Introducción
En este práctica, nos seguiremos familiarizando con ecosistema Sass.

# 2 Clase boton btn
Escribe un código de Sass que defina la `.btn`, comúnmente utilizada para estilizar botones. A continuación, los requisitos de la clase.

## 2.1 Definición de los estilos de los botones
**Estructura principal del botón**
- El boton debe comportarse como un bloque, pero debe permitir que se alinee con otros elementos en la misma línea.
- El contenido de los botones debe estar centrado.
- Se debe eliminar cualquier decoración del texto.
- Se debe usar la variable `$border-radius` para redondear las esquinas del botón.
- Se debe añadir un espacio interno de `0.5 unidades de rem` alrededor del contenido.

**Efecto al pasar el cursor sobre el botón**  
- Al pasar el cursor de ratón sobre el botón se aplicará un sobreado con las siguientes condiciones.
- **offset-x** = border-radius/2
- **offset-y** = border-radius/2
- **color** = color-shadow

**Efecto al hacer clic sobre el botón**   
- Cambiar el color de fondo a naranja.
- Cambiar el color del texto a blanco.

## 2.2 Crear las clases para asignar el color de fondo a los botones
- Para crear las clases usar un bucle sobre la variable btn-colors.
- Asignar el nombre de las clases de la siguiente manera .btn-1, .btn-2, ..., .btn-4.
- Asignar el color de fondo según el valor del valor.
