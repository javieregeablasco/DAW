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
<img src="https://github.com/javieregeablasco/DAW/blob/main/DIW/UT.%205%20-%20SASS/img/sprite.png" width=50%>

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

# 2 Sprites sobre imágenes raster
## 2.1 Creación de la imágen
### 2.1.1 Herramientas para crear sprites.
Existen todo tipo de herramientas para construir sprites, desde **preprocesadores CSS**, hasta **generadores de iconos**.   
**1. Preprocesadores CSS**  
   - Sass, Less.
      
**2. Automatizadores de Tareas**
   - Gulp, Grunt, Webpack, Parcel.

3. **Generadores de Sprites Online**
   - Sprite Cow, Spritesmith, Shoebox.

4. **Programas de Diseño Gráfico**
   - Photoshop, Illustrator, Figma, Sketch.

5. **Herramientas de Optimización de Imágenes**
   - ImageMagick, TinyPNG, ImageOptim.

6. **Frameworks y Librerías Front-End**
   - Tailwind CSS, Bootstrap Icons.

7. **Herramientas de Desarrollo Visual**
   - TexturePacker, Shoebox.

8. **Herramientas de Generación de Iconos**
   - IcoMoon, Fontello.

### 2.1.2 Definir el tamaño del sprite
 - Crear una imagen como un cuadrado (o rectángulo) donde cada lado sea un multiple exacto de un icono.  
 (Por ejemplo, para un icono de 48px x 48px, usar 528px x 528px).
>**Pregunta:** ¿Cuantos iconos caben en una fila de esa imagen?

### 2.1.3 Planificación de la imagen
 - Definir la cantidad de columnas y filas.
 - Como lo veremos más adelante, es habitual trabajar con porcentajes, así pues, aumentar en 1 la cantidad de columnas/filas para acomodar los porcentajes, ya que el conteo comienza en 0 y termina en 100.
 - Cantidades recomendadas de columnas/filas: **2, 3, 5, 6, 11**  
 **Ejemplo:**  
     - 2: 0%, 100%  
     - 3: 0%, 50%, 100%  
     - 5: 0%, 25%, 50%, 75%, 100%  
     - 6: 0%, 20%, 40%, 60%, 80%, 100%  
     - 11: 0%, 10%, 20%, [...], 90%, 100%.

### 2.1.3 Añadir guías
 - Agregar guías en cada intervalo de columnas y filas *(ej. 16px, 48px, 96px, 144px, ...)* para alinear los iconos correctamente.
<img src="https://github.com/javieregeablasco/DAW/blob/main/DIW/UT.%205%20-%20SASS/img/guias.webp">

### 2.1.4 Colocar las imágenes
 - Alinear las imágenes en la cuadrícula.
<img src="https://github.com/javieregeablasco/DAW/blob/main/DIW/UT.%205%20-%20SASS/img/colocarImagenes.webp"> 
 - Recortar o escalar la imagen si es necesario.

## 2.2 Gestión del sprite con SCSS, ejemplo práctico
Después de crear la imagen del sprite, utilizaremos SCSS para gestionar los iconos de las imágenes. 
### 2.2.1 Archivo sprite
Importar el archivo y visualizar su contenido.
<a href="https://github.com/javieregeablasco/DAW/blob/main/DIW/UT.%205%20-%20SASS/img/flags.png">link al archivo</a>

## 2.2.2 Usar directivas
```
@use "sass:list";
```

### 2.2.2 Crear las variables del proyecto
$spriteArchivoFuente: './media/flags.png';
$ancho: 44px;
$alto: 30px;
$spriteRango: 0.413223;

$listaPaises: "ad", "ae", "af", "ag", "al", "am", "an", "ao", "aq", "ar", "as", "at", "au", 
"aw", "az", "ba", "bb", "bd", "be", "bf", "bg", "bh", "bi", "bj", "bm", "bn", "bo", "br",
"bs", "bt", "bv", "bw", "by", "bz", "ca", "cc", "cd", "cf", "cg", "ch", "ci", "ck", "cl", 
"cm", "cn", "co", "cr", "cu", "cv", "cx", "cy", "cz", "de", "dj", "dk", "dm", "do", "dz", 
"ec", "ee", "eg", "eh", "er", "es", "et", "fi", "fj", "fk", "fm", "fo", "fr", "ga", "gd", 
"ge", "gf", "gh", "gi", "gl", "gm", "gn", "gp", "gq", "gr", "gs", "gt", "gu", "gw", "gy", 
"hk", "hm", "hn", "hr", "ht", "hu", "id", "ie", "il", "in", "io", "iq", "ir", "is", "it", 
"jm", "jo", "jp", "ke", "kg", "kh", "ki", "km", "kn", "kp", "kr", "kw", "ky", "kz", "la",
"lb", "lc", "li", "lk", "lr", "ls", "lt", "lu", "lv", "ly", "ma", "mc", "md", "me", "mg",
"mh", "mk", "ml", "mm", "mn", "mo", "mp", "mq", "mr", "ms", "mt", "mu", "mv", "mw", "mx",
"my", "mz", "na", "nc", "ne", "nf", "ng", "ni", "nl", "no", "np", "nr", "nu", "nz", "om",
"pa", "pe", "pf", "pg", "ph", "pk", "pl", "pm", "pn", "pr", "pt", "pw", "py", "qa", "re", 
"ro", "rs", "ru", "rw", "sa", "sb", "sc", "sd", "se", "sg", "sh", "si", "sj", "sk", "sl", 
"sm", "sn", "so", "sr", "ss", "st", "sv", "sy", "sz", "tc", "td", "tf", "tg", "th", "tj", 
"tk", "tl", "tm", "tn", "to", "tp", "tr", "tt", "tv", "tw", "ty", "tz", "ua", "ug", "gb", 
"um", "us", "uy", "uz", "va", "vc", "ve", "vg", "vi", "vn", "vu", "wf", "ws", "ye", "za", 
"zm", "zr", "zw";

$listaNombrePais: "Andorra", "United Arab Emirates", "Afghanistan", "Antigua and Barbuda", "Albania", "Armenia", 
"Netherlands Antilles", "Angola", "Antarctica", "Argentina", "American Samoa", "Austria", "Australia", 
"Aruba", "Azerbaijan", "Bosnia and Herzegovina", "Barbados", "Bangladesh", "Belgium", "Burkina Faso", "Bulgaria", 
"Bahrain", "Burundi", "Benin", "Bermuda", "Brunei Darussalam", "Bolivia", "Brazil", "Bahamas", "Bhutan", 
"Bouvet Island", "Botswana", "Belarus", "Belize", "Canada", "Cocos (Keeling) Islands", "Congo (Kinshasa)", 
"Central African Republic", "Congo (Brazzaville)", "Switzerland", "Côte d'Ivoire", "Cook Islands", "Chile", 
"Cameroon", "China", "Colombia", "Costa Rica", "Cuba", "Cape Verde", "Christmas Island", "Cyprus", 
"Czech Republic", "Germany", "Djibouti", "Denmark", "Dominica", "Dominican Republic", "Algeria", 
"Ecuador", "Estonia", "Egypt", "Western Sahara", "Eritrea", "Spain", "Ethiopia", "Finland", "Fiji", 
"Falkland Islands", "Micronesia", "Faroe Islands", "France", "Gabon", "Grenada", "Georgia", 
"French Guiana", "Ghana", "Gibraltar", "Greenland", "Gambia", "Guinea", "Guadeloupe", "Equatorial Guinea", 
"Greece", "South Georgia and the South Sandwich Islands", "Guatemala", "Guam", "Guinea-Bissau", 
"Guyana", "Hong Kong", "Heard Island and McDonald Islands", "Honduras", "Croatia", "Haiti", 
"Hungary", "Indonesia", "Ireland", "Israel", "India", "British Indian Ocean Territory", "Iraq", 
"Iran", "Iceland", "Italy", "Jamaica", "Jordan", "Japan", "Kenya", "Kyrgyzstan", "Cambodia", 
"Kiribati", "Comoros", "Saint Kitts and Nevis", "North Korea", "South Korea", "Kuwait", 
"Cayman Islands", "Kazakhstan", "Laos", "Lebanon", "Saint Lucia", "Liechtenstein", "Sri Lanka", 
"Liberia", "Lesotho", "Lithuania", "Luxembourg", "Latvia", "Libya", "Morocco", "Monaco", 
"Moldova", "Montenegro", "Madagascar", "Marshall Islands", "North Macedonia", "Mali", "Myanmar", 
"Mongolia", "Macau", "Northern Mariana Islands", "Martinique", "Mauritania", "Montserrat", 
"Malta", "Mauritius", "Maldives", "Malawi", "Mexico", "Malaysia", "Mozambique", "Namibia", 
"New Caledonia", "Niger", "Norfolk Island", "Nigeria", "Nicaragua", "Netherlands", "Norway", 
"Nepal", "Nauru", "Niue", "New Zealand", "Oman", "Panama", "Peru", "French Polynesia", "Papua New Guinea", 
"Philippines", "Pakistan", "Poland", "Saint Pierre and Miquelon", "Pitcairn Islands", "Puerto Rico", 
"Portugal", "Palau", "Paraguay", "Qatar", "Réunion", "Romania", "Serbia", "Russia", "Rwanda", 
"Saudi Arabia", "Solomon Islands", "Seychelles", "Sudan", "Sweden", "Singapore", "Saint Helena", 
"Slovenia", "Svalbard and Jan Mayen", "Slovakia", "Sierra Leone", "San Marino", "Senegal", 
"Somalia", "Suriname", "South Sudan", "Sao Tome and Principe", "El Salvador", "Syria", 
"Eswatini", "Turks and Caicos Islands", "Chad", "French Southern Territories", "Togo", 
"Thailand", "Tajikistan", "Tokelau", "Timor-Leste", "Turkmenistan", "Tunisia", "Tonga", 
"East Timor", "Turkey", "Trinidad and Tobago", "Tuvalu", "Taiwan", "Tuvalu", "Tanzania", 
"Ukraine", "Uganda", "United Kingdom", "United States Minor Outlying Islands", "United States", 
"Uruguay", "Uzbekistan", "Vatican City", "Saint Vincent and the Grenadines", "Venezuela", 
"British Virgin Islands", "U.S. Virgin Islands", "Vietnam", "Vanuatu", "Wallis and Futuna", 
"Samoa", "Yemen", "South Africa", "Zambia", "Zaire", "Zimbabwe";

>**Pregunta:** ¿De donde viene el valor de $spriteRango: 0.413223?

### 2.2.3 Definir los estilos básicos
```
.bandera {
  display: flex;
  flex-direction: row;
  width: $ancho;
  height: $alto;  
  background: url($spriteArchivoFuente) no-repeat;
  background-size: 100%;  
  margin-top: 10px;
  margin-bottom: 10px;
}
```
Este estilo establece un contenedor que tiene un tamaño definido por las variables $ancho y $alto y establece **una imagen de fondo** que se ajusta al tamaño del contenedor.  

### 2.2.4 Definir las funciones del proyecto
Como acabamos de ver en el archivo sprite, la primera imagen es una `dummy` para cuando se escriba mal <a href="https://www.sanidad.gob.es/ciudadanos/saludAmbLaboral/docs/codigoIsoPai.pdf">**el codigo del país**</a>.  
Así pues, será conveniente invertir la lista de paises para empezar por el final.
```
@function funcionInvertirLista($listado) {
  $listaInvertida: ();
  @for $i from list.length($listado) through 1 {
    $listaInvertida: list.append($listaInvertida, list.nth($listado, $i));
  }
  @return $listaInvertida;
}
```
La función `funcionInvertirLista` toma una lista como argumento y devuelve una nueva lista en la que los elementos están invertidos respecto al orden de la lista original.  
Utiliza un bucle @for para recorrer la lista original desde el final hasta el principio, añadiendo los elementos uno por uno a la nueva lista invertida.
`list.nth($listado, $i)` devuelve el elemento de la lista $list en la posición $i. 
`list.append($listaInvertida, list.nth($listado, $i))` agrega un nuevo elemento al final de la lista $listaInvertida.

### 2.2.5 Definir los estilos para cada país
```
@each $pais in $listaInvertida {
  $i: list.index($listaInvertida, $pais);   
  
  .bandera-#{$pais} {
    background-position: 0 (100% - ($spriteRango * ($i - 1)) * 1%);  
   
    &::after{ 
      position: relative;
      left: 50px;
      top: 5px;                
      white-space: nowrap;
      content: list.nth($listaInvertidaPais, $i);
    }      
  }   
}
```

---
Este código es un ejemplo de cómo usar un **bucle `@each`** en **Sass** (SCSS) para iterar sobre una lista, en este caso, `$listaInvertida`, y aplicar estilos CSS dinámicamente a cada elemento de la lista. Además, se incluye un pseudo-elemento `::after` para añadir contenido adicional a cada elemento.

Vamos a desglosar el código línea por línea para entender cómo funciona:

### 1. **Iteración con `@each`**
```scss
@each $pais in $listaInvertida {
```
- **`@each`**: Esta es una directiva de Sass que se utiliza para iterar sobre una lista o mapa. En este caso, estamos iterando sobre la lista `$listaInvertida`.
- En cada iteración, el valor actual de la lista se asigna a la variable `$pais`.

### 2. **Obtener el índice del elemento**
```scss
  $i: list.index($listaInvertida, $pais);
```
- **`list.index($listaInvertida, $pais)`**: Esta función devuelve el índice (la posición) de un valor dentro de la lista `$listaInvertida`.
  - Si `$pais` es el valor actual que se está iterando, esta línea obtiene el índice de ese valor en la lista.
  - El valor de `$i` será el índice en la lista, comenzando desde 1 (el primer elemento tiene el índice 1).

### 3. **Definir una clase con el nombre de cada país**
```scss
  .bandera-#{$pais} {
```
- Esto define una clase CSS cuyo nombre está basado en el valor actual de `$pais`. Por ejemplo, si el valor de `$pais` es "España", el selector será `.bandera-España`.
- **`#{$pais}`**: La sintaxis `#{}` en Sass se usa para interpolar el valor de una variable dentro de un nombre de clase o un selector.

### 4. **Establecer la posición de fondo**
```scss
    background-position: 0 (100% - ($spriteRango * ($i - 1)) * 1%);
```
- **`background-position`**: Esta propiedad controla la posición de la imagen de fondo.
- `0`: Esto significa que la posición horizontal de la imagen de fondo será 0 (es decir, alineada al borde izquierdo).
- **`(100% - ($spriteRango * ($i - 1)) * 1%)`**: Este cálculo se usa para determinar la posición vertical del fondo.
  - `$spriteRango` es probablemente una variable que representa el tamaño de una "célula" dentro de un **sprite gráfico**.
  - El valor de `($i - 1)` multiplica el rango por el índice del país menos 1, para que el fondo se desplace hacia abajo correctamente según el orden de los países.

### 5. **Agregar contenido con `::after`**
```scss
    &::after{ 
      position: relative;
      left: 50px;
      top: 5px;
      white-space: nowrap;
      content: list.nth($listaInvertidaPais, $i);
    }
```
- **`&::after`**: Esto hace referencia al pseudo-elemento `::after` del selector actual (en este caso, `.bandera-#{$pais}`). El pseudo-elemento `::after` se utiliza para insertar contenido adicional después del elemento principal.
- **`position: relative;`**: Esto establece que el pseudo-elemento se posicionará de manera relativa respecto a su posición original dentro del contenedor.
- **`left: 50px;`**: Mueve el pseudo-elemento 50 píxeles hacia la derecha desde su posición inicial (relativa al contenedor).
- **`top: 5px;`**: Mueve el pseudo-elemento 5 píxeles hacia abajo desde su posición inicial.
- **`white-space: nowrap;`**: Esto asegura que el texto dentro del pseudo-elemento no se divida en varias líneas, evitando saltos de línea automáticos.
- **`content: list.nth($listaInvertidaPais, $i);`**: Esto inserta el contenido en el pseudo-elemento. La función `list.nth($listaInvertidaPais, $i)` devuelve el valor del elemento en la posición `$i` de la lista `$listaInvertidaPais`. Así, el contenido que se insertará será el nombre del país en esa posición de la lista.

### Resumen:
El código crea una clase `.bandera-#{$pais}` para cada país en la lista `$listaInvertida`. En cada iteración:
1. Se calcula la posición de fondo para ajustar el sprite gráfico.
2. Se inserta contenido adicional mediante el pseudo-elemento `::after`, con el nombre del país correspondiente de la lista `$listaInvertidaPais`.
3. El texto del pseudo-elemento se coloca de manera relativa y no se ajusta a varias líneas.

### Ejemplo práctico:
Si `$listaInvertida` tiene los valores `('España', 'Francia', 'Italia')` y `$listaInvertidaPais` tiene los valores `('España', 'Francia', 'Italia')`, el código generará lo siguiente:
- Para `.bandera-España`, la imagen de fondo se desplazará correctamente y se mostrará "España" debajo del contenedor.
- Para `.bandera-Francia`, la imagen de fondo se desplazará a la posición correspondiente y se mostrará "Francia".
- Lo mismo ocurrirá para `.bandera-Italia`.

---
