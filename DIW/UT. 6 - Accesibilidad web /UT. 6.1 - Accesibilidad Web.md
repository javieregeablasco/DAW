---
Título: UD. 6.1 - Accesibilidad web
Autor: Javier Egea Blasco
Año: 24-25
Palabras clave: DAW, DIW
---

# 1. Introducción
## 1.1 ¿Qué es la Accesibilidad Web?  
La <a href="https://es.wikipedia.org/wiki/Accesibilidad_web">accesibilidad web</a> se refiere al diseño y desarrollo de sitios, aplicaciones y contenidos digitales que **puedan ser utilizados por todas las personas**, incluyendo aquellas con **discapacidades**. Esto implica garantizar que el contenido sea **perceptible**, **operable**, **comprensible** y **robusto**, de manera que cualquier persona pueda **acceder, navegar e interactuar** con él sin barreras.

## 1.2 Objetivo de la Accesibilidad Web
El objetivo de la **accesibilidad web** es **eliminar barreras digitales** para que cualquier usuario, independientemente de sus capacidades físicas, sensoriales, intelectuales o técnicas, pueda interactuar con la web de forma **autónoma** y **eficiente**.

Las personas que se benefician de la **accesibilidad web** incluyen:

- 🧑‍🦯 **Personas con discapacidades visuales** (ceguera, baja visión, daltonismo).
- 🧏 **Personas con discapacidades auditivas** (sordera, pérdida de audición).
- 🧑‍🦽 **Personas con discapacidades físicas** (movilidad reducida, temblores).
- 🧠 **Personas con discapacidades cognitivas o neurológicas** (dificultades de aprendizaje, trastornos del espectro autista).
- 👵 **Personas mayores**, que pueden experimentar pérdida de visión, audición o destrezas motoras.
- 📱 **Usuarios en condiciones temporales** (como personas con una mano ocupada o en entornos con mala iluminación).

## 1.3 Principios de la Accesibilidad Web (POUR)
La accesibilidad web se basa en **cuatro principios** fundamentales:

| Principio   | Descripción                                                                                                                                     |
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| **Perceptible** | El contenido debe ser presentado de forma que los usuarios puedan **percibirlo** a través de los sentidos (vista, oído, etc.).                 |
| **Operable**   | La interfaz y los componentes deben ser **fáciles de manejar** para todos los usuarios, incluidos aquellos que utilizan tecnologías de asistencia. |
| **Comprensible** | La información y la navegación deben ser **entendibles** para todos los usuarios.                                                           |
| **Robusto**     | El contenido debe ser **compatible** con diversas tecnologías presentes y futuras, incluidas las herramientas de asistencia.                    |

## 1.4 Pautas y Estándares de Accesibilidad
El estándar más utilizado a nivel internacional es el <a href="https://www.w3.org/WAI/">WAI (Web Accessibility Initiative)</a>, desarrollado por el <a href="https://www.w3.org/">W3C (World Wide Web consortium)</a>  

Las **WAI** están organizadas en tres niveles de conformidad:

- **A (mínimo)**: Requisitos básicos de accesibilidad.
- **AA (medio)**: Nivel recomendado para la mayoría de los sitios web.
- **AAA (alto)**: Máxima accesibilidad, generalmente aplicada a sitios específicos.

## 1.5 Tecnologías de Asistencia
Las tecnologías de asistencia permiten a las personas con discapacidades interactuar con contenido web. Algunos ejemplos incluyen:

- **Lectores de pantalla** (Jaws, NVDA, VoiceOver).
- **Teclados alternativos** o dispositivos de entrada especiales.
- **Software de reconocimiento de voz**.
- **Ampliadores de pantalla**.
- **Subtítulos y transcripciones** para contenido multimedia.

## 1.6 Buenas Prácticas para la Accesibilidad Web

1. ✅ **Etiquetar correctamente los elementos HTML** (`<alt>` en imágenes, `<label>` en formularios).
2. ✅ **Proporcionar texto alternativo** para imágenes.
3. ✅ **Crear contenido multimedia accesible** con subtítulos y transcripciones.
4. ✅ **Diseñar con colores contrastados** y evitar depender solo del color para transmitir información.
5. ✅ **Navegación accesible** mediante teclado.
6. ✅ **Proporcionar controles de interfaz accesibles**, como botones grandes y etiquetas claras.
7. ✅ **Evitar contenido que parpadee** o cause epilepsia fotosensible.

## 1.7 Beneficios de la Accesibilidad Web

- 🌍 **Mayor alcance**: Más personas pueden acceder al contenido, incluyendo personas con discapacidades.
- 💻 **Mejora del SEO**: Los sitios accesibles también son más fáciles de indexar por los motores de búsqueda.
- 📱 **Compatibilidad multiplataforma**: Contenido accesible suele ser más compatible con diferentes dispositivos y navegadores.
- 🔐 **Cumplimiento legal**: Evita problemas legales relacionados con la discriminación digital.

# 2 Legislación aplicable
## 2.1 Legislación dentro del sector público
Actualmente, (2025) la legislación aplicable en materia de accesibilidad web a la administración pública en España es el <a href="https://www.boe.es/boe/dias/2018/09/19/pdfs/BOE-A-2018-12699.pdf">Real Decreto 1112/2018</a>, de 7 de septiembre, sobre accesibilidad de los sitios web y aplicaciones para dispositivos móviles del sector público.    
Este Real Decreto es la trasposición a la legislación española de la <a href="https://www.boe.es/doue/2016/327/L00001-00015.pdf">Directiva UE 2016/2102</a>, del Parlamento Europeo y del Consejo, de 26 de octubre de 2016, sobre la accesibilidad de los sitios web y aplicaciones para dispositivos móviles de los organismos del sector público.

## 2.2 Legislación dentro del sector privado
La legislación aplicable en materia de accesibilidad web al sector privado en España es el <a href="https://www.boe.es/buscar/pdf/2023/BOE-A-2023-7417-consolidado.pdf">Real Decreto 193/2023</a>, de 21 de marzo, por el que se regulan las condiciones básicas de accesibilidad y no discriminación de las personas con discapacidad para el acceso y utilización de los bienes y servicios a disposición del público.

# 3 Guía básica para crear sitios web accesibles
A continuación, se presentan las mejores prácticas para crear una página web accesible.  

## 3.1 Estructura Semántica Correcta
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
## 3.2 Textos Alternativos para imágenes y animaciones
Proporcionar descripciones alternativas (<a href="https://html.spec.whatwg.org/multipage/images.html#alt">atributo `alt`</a>) para todas las imágenes.

El atributo alt especifica un texto alternativo para navegadores que no puedan mostrar imágenes, formularios o aplicaciones. El idioma de este texto alternativo está especificado por el atributo lang.

Varios elementos no textuales (IMG, AREA, APPLET e INPUT) permiten a los autores especificar texto alternativo que sirva como contenido cuando el elemento no pueda ser representado normalmente. El especificar texto alternativo ayuda a los usuarios que no tengan terminales gráficas, a los usuarios cuyos navegadores no soporten formularios, a los usuarios con discapacidades visuales, a aquellos que utilicen sintetizadores de voz, a aquellos que hayan configurado sus agentes de usuario para no mostrar imágenes, etc.

>**Buenas prácticas de uso:**
- Describir brevemente la imagen y su función.
- Si la imagen es decorativa, dejar el atributo `alt` vacío (`alt=""`).

**Ejemplo:**
```html
<img src="imagen-producto.jpg" alt="Foto del producto en venta">
```

## 3.3 Contenidos Multimedia Accesibles
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

## 3.3 Enlaces de hipertexto
Usar texto para el hipertexto que tenga sentido leído fuera de contexto. Por ejemplo, evitar abusar de "pincha aquí".
Algunos navegadores y algunos los programas de ayuda que emplean las personas con discapacidad (por ejemplo, los lectores de pantalla) ofrecen al usuario la posibilidad de mostrar, normalmente una ventana aparte, la lista de enlaces que contiene una página web. Esta lista de enlaces normalmente permite activar un enlace y navegar a la página de destino. Si el texto de un enlace no tiene sentido fuera de su contexto, el enlace no tendrá sentido en esta lista de enlaces.

Por otro lado, si los enlaces poseen un estilo especial para resaltarlos, los usuarios suelen fijar su atención en ellos, por lo que es importante que el texto de los enlaces sea lo más claro y significativo.

Por ejemplo, elPeriódico.com tiene una sección llamada Encuestas en la que se muestran todas las encuestas que existen. Cada encuesta tiene un enlace asociado con el texto Ver Resultados para visualizar los resultados de la encuesta seleccionada, como podemos ver en la siguiente imagen:





## 3. Contraste de Colores Adecuado
Asegúrate de que el texto tenga un contraste suficiente con el fondo para facilitar la lectura.

### Buenas prácticas:
- Usa herramientas como [WebAIM Contrast Checker](https://webaim.org/resources/contrastchecker/) para verificar el contraste.
- Sigue las pautas WCAG que recomiendan un ratio mínimo de 4.5:1 para texto normal y 3:1 para texto grande.

### Ejemplo CSS:
```css
body {
  color: #333;
  background-color: #fff;
}
```

---

## 4. Navegación Accesible con el Teclado
Asegura que los usuarios puedan navegar por el sitio utilizando solo el teclado.

### Buenas prácticas:
- Evita trampas de teclado (elementos que no permiten salir de ellos).
- Utiliza el atributo `tabindex` para controlar el orden de tabulación cuando sea necesario.

### Ejemplo:
```html
<a href="#contenido-principal" tabindex="1">Ir al contenido principal</a>
```

---

## 5. Formularios Accesibles
Etiqueta correctamente los campos de los formularios para que los usuarios con tecnologías de asistencia puedan interactuar con ellos.

### Buenas prácticas:
- Usa la etiqueta `<label>` para cada campo de formulario.
- Asocia cada etiqueta con su campo mediante el atributo `for`.

### Ejemplo:
```html
<label for="nombre">Nombre:</label>
<input type="text" id="nombre" name="nombre">
```

---



---

## 7. Uso de ARIA (Accessible Rich Internet Applications)
Implementa atributos ARIA cuando no sea posible lograr la accesibilidad solo con HTML.

### Buenas prácticas:
- Usa `aria-label` para proporcionar etiquetas adicionales.
- Utiliza roles ARIA para definir el propósito de los elementos.

### Ejemplo:
```html
<button aria-label="Cerrar menú">&times;</button>
```

---

## 8. Pruebas de Accesibilidad
Realiza pruebas para asegurarte de que tu página es accesible.

### Herramientas recomendadas:
- [Lighthouse](https://developers.google.com/web/tools/lighthouse)
- [Wave](https://wave.webaim.org/)
- [axe DevTools](https://www.deque.com/axe/devtools/)

---

### Resumen de Pautas
| Práctica             | Descripción                               |
|----------------------|-------------------------------------------|
| Estructura semántica | Usa etiquetas HTML semánticas             |
| Alt para imágenes    | Proporciona descripciones alternativas    |
| Contraste adecuado   | Asegura un contraste suficiente           |
| Navegación teclado   | Garantiza la navegación sin mouse         |
| Formularios          | Etiqueta los campos correctamente         |
| Multimedia           | Ofrece subtítulos y transcripciones       |
| ARIA                 | Usa atributos ARIA para mejorar la accesibilidad |

Aplicar estas prácticas ayuda a crear un entorno web más inclusivo para todos los usuarios.

