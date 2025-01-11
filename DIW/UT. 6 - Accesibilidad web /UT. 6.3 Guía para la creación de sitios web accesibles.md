
# 3 Guía para crear sitios web accesibles
A continuación, se presentan las mejores prácticas para crear una página web accesible.  

## 3.1 Estructura semántica correcta
Utilizar etiquetas HTML semánticas para organizar el contenido de la página. Esto ayuda a los usuarios que utilizan lectores de pantalla a comprender la estructura del sitio.

>**Buenas prácticas de uso:**
- Usar etiquetas como `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, y `<footer>`.
- Utilizar encabezados (`<h1>` a `<h6>`) de manera jerárquica y lógica.

**Ejemplo:**
```html
<header>
  <h1>Bienvenido a mi sitio web</h1>
</header>
<main>
  <section>
    <h2>Sobre nosotros</h2>
    <p>Contenido descriptivo...</p>
  </section>
</main>
```
## 3.2 Textos alternativos para imágenes y animaciones
Proporcionar semántica adecuada y descripciones alternativas (atributo <a href="https://html.spec.whatwg.org/multipage/images.html#alt">alt</a>) para todas las imágenes.

El atributo alt especifica un texto alternativo para navegadores que no puedan mostrar imágenes, formularios o aplicaciones. El idioma de este texto alternativo está especificado por el atributo lang.

Varios elementos no textuales (IMG, AREA, APPLET e INPUT) permiten a los autores especificar texto alternativo que sirva como contenido cuando el elemento no pueda ser representado normalmente. El especificar texto alternativo ayuda a los usuarios que no tengan terminales gráficas, a los usuarios cuyos navegadores no soporten formularios, a los usuarios con discapacidades visuales, a aquellos que utilicen sintetizadores de voz, a aquellos que hayan configurado sus agentes de usuario para no mostrar imágenes, etc.

>**Buenas prácticas de uso:**
- Semántica adecuada.
- Describir brevemente la imagen y su función.
- Si la imagen es decorativa, dejar el atributo `alt` vacío (`alt=""`).

**Ejemplo:**
- **Así no:**
```html
<img src="imagen-producto.jpg" alt="">
```
- **Así sí:**
```
<figure aria-label="Ilustración de un pájaro estilizado">
  <img src="img1.png" alt="Pájaro estilizado" class="imagen-pajaro">
  <figcaption>Esta es una ilustración artística de un pájaro estilizado, utilizada como parte del diseño visual.</figcaption>
</figure>
```
## 3.3 Contraste de colores adecuado
Asegúrarse de que el texto tenga un contraste suficiente con el fondo para facilitar la lectura.

>**Buenas prácticas de uso:**
- Usar herramientas como [WebAIM Contrast Checker](https://webaim.org/resources/contrastchecker/) para verificar el contraste.
- Seguir las pautas <a href="https://www.w3.org/WAI/standards-guidelines/wcag/es">WCAG</a> que recomiendan un ratio mínimo de 4.5:1 para texto normal y 3:1 para texto grande.

**Ejemplo:**
```css
body {
  color: #333;
  background-color: #fff;
}
```
<img src="https://github.com/javieregeablasco/DAW/blob/main/DIW/UT.%206%20-%20Accesibilidad%20web%20/img/contraste.png">

## 3.4 Navegación accesible con el teclado
Asegura que los usuarios puedan navegar por el sitio utilizando solo el teclado.

>**Buenas prácticas de uso:**
- Evitar trampas de teclado (elementos que no permiten salir de ellos).
- Utilizar el atributo `tabindex` para controlar el orden de tabulación cuando sea necesario.

**Ejemplo:**
```html
<a href="#contenido-principal" tabindex="1">Ir al contenido principal</a>
```

## 3.5 Formularios accesibles
Etiquetar correctamente los campos de los formularios para que los usuarios con tecnologías de asistencia puedan interactuar con ellos.

>**Buenas prácticas de uso:**
- Usar la etiqueta `<label>` para cada campo de formulario.
- Asociar cada etiqueta con su campo mediante el atributo `for`.

**Ejemplo:**
```html
<form aria-labelledby="accessible-form" style="background-color: antiquewhite;">
  <h2 id="accessible-form">Formulario Accesible</h2>

  <label for="name">Nombre completo:</label>
  <input type="text" id="name" name="name" required aria-required="true">
  <br><br>

  <label for="email">Correo electrónico:</label>
  <input type="email" id="email" name="email" required aria-required="true">
  <br><br>

  <fieldset>
    <legend>Género:</legend>
    <input type="radio" id="male" name="gender" value="male">
    <label for="male">Masculino</label><br>

    <input type="radio" id="female" name="gender" value="female">
    <label for="female">Femenino</label><br>

    <input type="radio" id="other" name="gender" value="other">
    <label for="other">Otro</label>
  </fieldset>
  <br>
```
<img src="https://github.com/javieregeablasco/DAW/blob/main/DIW/UT.%206%20-%20Accesibilidad%20web%20/img/formulario.png">

## 3.6 Contenidos multimedia accesibles
Los elementos multimedia que tanto se utilizan en las páginas web hoy en día pueden ocasionar graves problemas de accesibilidad, ya no sólo a las personas con algún tipo de discapacidad, sino a todo el mundo en general. Al ser elementos que no son HTML requieren, en la mayoría de los casos, la instalación de un visor específico (plug-in, add-on o extensión) que sea capaz de interpretar el elemento multimedia.  

Por tanto, **como regla general**, no se debe abusar de los elementos multimedia y el diseñador de una página web se tiene que preguntar si es un elemento esencial que no se puede eliminar o sustituir por otro más accesible.

>**Buenas prácticas de uso:**
- Proporcionar subtítulos para los vídeos.
- Ofrecer transcripciones para los audios.

**Ejemplo:**
```html
<video controls>
  <source src="video.mp4" type="video/mp4">
  Tu navegador no soporta la reproducción de vídeos.
</video>
<p>Transcripción: [Descripción del contenido del vídeo]</p>
```

## 3.7 Enlaces de hipertexto
Usar texto para el hipertexto que tenga sentido leído fuera de contexto. Por ejemplo, evitar abusar del **"pinchar aquí"**.
Algunos navegadores y algunos programas de ayuda que emplean las personas con discapacidad (por ejemplo, los lectores de pantalla) ofrecen al usuario la posibilidad de mostrar, normalmente en una ventana aparte, la lista de enlaces que contiene una página web. Si el texto de un enlace no tiene sentido fuera de su contexto, el enlace no tendrá sentido en esta lista de enlaces.
Por otro lado, si los enlaces poseen un estilo especial para resaltarlos, los usuarios suelen fijar su atención en ellos, por lo que es importante que el texto de los enlaces sea lo más claro y significativo posible.
<img src="https://github.com/javieregeablasco/DAW/blob/main/DIW/UT.%206%20-%20Accesibilidad%20web%20/img/enlace.png">

## 3.8. Uso de ARIA (Accessible Rich Internet Applications)
Implementar atributos **ARIA** cuando no sea posible lograr la accesibilidad solo con HTML.

>**Buenas prácticas de uso:**
- Usar `aria-label` para proporcionar etiquetas adicionales.
- Utilizar roles ARIA para definir el propósito de los elementos.

**Ejemplo:**
```
<nav role="navigation" aria-label="Navegación principal">
  <ul>
    <li><a href="#">Inicio</a></li>
    <li><a href="#">Servicios</a></li>
    <li><a href="#">Contacto</a></li>
  </ul>
</nav>
```
