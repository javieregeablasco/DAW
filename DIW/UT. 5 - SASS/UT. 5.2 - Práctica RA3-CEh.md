---
Título: UD. 5.2 - SASS Práctica evaluable 
Autor: Javier Egea Blasco
Año: 24-25
Palabras clave: DAW, DIW
Resultado de aprendizaje y criterio de evaluación: RA3 CEh 
---


# 1 Introducción
En este práctica, nos seguiremos familiarizando con ecosistema Sass.

# 2 Estilos de los botones 
## 2.1 Elemento botón general
Escribe un código de Sass que defina la clase `.btn`, comúnmente utilizada para estilizar botones.  
A continuación, los requisitos de la clase.

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

## 2.2 Elemento botón al hacer click
Crear las clases para asignar el color de fondo a los botones.
**Personalización de cada botón**
- Para crear las clases usar un bucle `@each` sobre la variable (lista) btn-colors.
- Asignar el nombre de las clases segun la clave de la lista de la siguiente manera .btn-`primary`, .btn-`secondary`, ..., .btn-`link`.
- Asignar el color de fondo según el valor del valor de la lista.  

**Efecto al hacer clic sobre el botón**   
- Oscurecer el fondo un 20%.
- Cambiar el color del texto a blanco.

## 2.3 Analizar el siguiente fragmento de programa
```
@each $k, $v in $btn-colors {
  .btn-#{$k} {
    background-color: $v;    
  &:active {
    background-color: color.adjust($v, $lightness: -20%);
    color:white;
    }
  }
}
```
>**Pregunta:** ¿Qué realiza ese bucle?

# 3 Estilos de tabla
## 3.1 Analizar el siguiente fragmento de programa
```
@for $num from $inicio through $fin {
  tbody tr td:nth-child(#{$num}) {
    background-color: colum-color($num);
  }
}
```
¿Qué realiza ese fragmento de programa?
## 3.2 Programar la función colum-color().
Programar la función column-color para que devuelva $color-col-pares o  $color-col-impares dependiendo de si el indice de la columna es par o impar.  
**Pista:** Para determinar si el indice de la columna es par o impar usar la función `%` que permite determinar si el módulo de la división es nulo o no.

# 4 Estilos de sistema de columnas 
## 4.1 Analizar el siguiente fragmento de programa
```
@function anchura_col($i) {
  @return calc((100/$num_elementos)*$i); 
}
```

## 4.2 Crear las clases para definir el ancho de las columnas
Realizar un bucle `@for` **sobre la variable $sum_elementos** que haga lo siguiente:
 - A cada iteración se creará una clase **.col-#{$i}** que será hija directa de la clase `.row`.
 - El contenido de la clase creada será el siguiente: `padding: 1rem` y **width: resultado de anchura_col()+"%"**.
   
>**Pregunta:** ¿Qué realiza este bucle?  


# 5 Tarea RA2CEj
Siguiendo las buenas prácticas de Sass redistribuir las diferentes declaraciones, funciones y mixins en sus correspondientes carpetas siguiendo la estructura dada a continuación. 
```
styles/  
├── main.scss
├── base/  
├── components/  
├── layout/  
├── pages/  
├── themes/  
└── utils/  
```
**Nota:** Optimizar el código de tal manera que en `main.scss`solo hayan **@directivas de tipo @use**.
