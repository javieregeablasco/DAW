---
Título: UD. 5.2 - SASS Práctica evaluable 
Autor: Javier Egea Blasco
Año: 24-25
Palabras clave: DAW, DIW
Resultado de aprendizaje y criterio de evaluación: RA3 CEh 
---


# 1 Introducción
En este práctica, nos seguiremos familiarizando con ecosistema Sass.

# 2 Clase boton btn
Escribe un código de Sass que defina la `.btn`, comúnmente utilizada para estilizar botones. A continuación, los requisitos de la clase.

## 2.1 Definición de los estilos de los botones
### 2.1.1 Elemento botón general
**Crear una clase btn que aplique los siguientes estilos**
- El boton debe comportarse como un bloque, pero debe permitir que se alinee con otros elementos en la misma línea.
- El contenido de los botones debe estar centrado.
- Se debe eliminar cualquier decoración del texto.
- Se debe usar la variable `$border-radius` para redondear las esquinas del botón.
- Se debe añadir un espacio interno de `0.75 unidades de rem` alrededor del contenido.
- Espesor de borde: 1px.

**Efecto al pasar el cursor sobre el botón**  
- Al pasar el cursor de ratón sobre el botón se aplicará un sobreado con las siguientes condiciones.
- **offset-x** = border-radius/2
- **offset-y** = border-radius/2
- **color** = color-shadow

### 2.1.2 Personalización de cada botón
**Crear las clases para asignar el color de fondo a los botones**
- Para crear las clases usar un bucle `@each` sobre la variable (lista) btn-colors.
- Asignar el nombre de las clases segun la clave de la lista de la siguiente manera .btn-`primary`, .btn-`secondary`, ..., .btn-`link`.
- Asignar el color de fondo según el valor del valor de la lista.  

**Efecto al hacer clic sobre el botón**   
- Oscurecer el fondo un 20%.
- Cambiar el color del texto a blanco.

## 2.2 

