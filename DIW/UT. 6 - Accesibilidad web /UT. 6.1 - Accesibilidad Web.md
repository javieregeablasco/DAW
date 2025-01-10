---
Título: UD. 6.1 - Accesibilidad web
Autor: Javier Egea Blasco
Año: 24-25
Palabras clave: DAW, DIW
---
  
<div align="center">
</br>
<img src="https://github.com/javieregeablasco/DAW/blob/main/DIW/UT.%205%20-%20SASS/img/love_sass.png">
</div>


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

# 3 Software específico para mejorar la accesibilidad web  
## 3.1 Ayudas técnicas
La Norma <a href="https://www.une.org/encuentra-tu-norma/busca-tu-norma/norma?c=N0029860">UNE 139802:2003 Aplicaciones informáticas para personas con discapacidad. Requisitos de accesibilidad al ordenador. Software</a> define el concepto ayuda técnica:

```
3.3 ayuda técnica: Cualquier producto, instrumento, equipo o sistema técnico utilizado por una persona minusválida,
fabricado especialmente o disponible en el mercado para prevenir, compensar, mitigar o neutralizar la deficiencia, 
incapacidad o discapacidad. (UNE-EN ISO 9999). Incluye tanto productos hardware como software.
```
La clasificación de las ayudas técnicas está definida en la <a href="https://www.une.org/encuentra-tu-norma/busca-tu-norma/norma?c=N0039568">Norma UNE-EN ISO 9999:2007: Productos de apoyo para personas con discapacidad. Clasificación y terminología (ISO 9999:2007)</a>. Esta norma establece que ya no se tienen que llamar ayudas técnicas, sino tecnologías de apoyo.

A continuación, algunas de las ayudas técnicas basadas en software que emplean las personas con discapacidad para utilizar un ordenador y navegar por la Web. También se incluye otro tipo de software, como simuladores de algunas de las alteraciones que presentan las personas con discapacidad:

- **Lectores de pantalla**. Los lectores de pantalla permiten la utilización del sistema operativo y las distintas aplicaciones mediante el empleo de un sintetizador de voz que "lee y explica" lo que se visualiza en la pantalla, lo que supone una ayuda para las personas con graves problemas de visión o completamente ciegas. Se muestran a continuación los softwares más conocidos.
  - JAWS (Windows). Jaws es el lector de pantalla más utilizado a nivel mundial. Es de pago y está disponible para todas las versiones de Windows.
  - NVDA (Windows). NVDA - Non Visual Desktop Access, es un lector de pantalla gratuito, de código abierto. Nace como alternativa a Jaws y su elevado precio. Está disponible para las versiones de Windows XP, 7, 8 y 10 de Microsoft.
  - Narrador (Windows). Narrador es un lector de pantalla gratuito que viene incluido por defecto en las versiones de Windows 7, 8 y 9. Nos permite utilizar el ordenador con la mayoría de sus funcionalidades. Si bien no es la opción más completa, ni la más extendida, puede utilizarse en ocasiones concretas donde no dispongamos de otras alternativas superiores, como las anteriormente comentadas Jaws o NVDA.
  - VoiceOver (macOS). VoiceOver es un lector de pantalla que cuenta con unas síntesis voz avanzadas y voces de gran calidad, leen de una forma realista, incluso se toman respiros si leen mucho.
  - Orca (Linux). El programa Orca permite a personas con deficiencias visuales o ceguera a manejarse en el entorno de su ordenador, así como personas con deficiencias motoras. Utiliza una combinación de voz, braille y magnificación.
  - VoiceOver (iOS). Los iPhone e iPad cuentan con el lector de pantalla VoiceOver. Para iniciarlo debemos ir a Ajustes -> Accesibilidad -> VoiceOver y activar el botón de VoiceOver.
  - TalkBack (Android). La mayoría de los dispositivos móviles con Sistema Operativo Android cuentan con el lector de pantalla TalkBack integrado en el sistema.
  
- **Magnificadores de pantalla**. Los magnificadores de pantalla o sistemas de ampliación de pantalla, son un software o dispositivos hardware que permiten visualizar la pantalla con un considerable aumento en su tamaño. Con estas ayudas técnicas, un usuario que posee algún residuo visual puede ver la pantalla del ordenador mediante el aumento del tamaño de la pantalla.
  - Ampliador de Windows. Disponible en los sistemas operativos Microsoft Windows XP y Microsoft Vista.
  - Dolphin Lunar. Magnificador de pantalla.
  - Dolphin LunarPlus. Magnificador de pantalla que incluye también lector de pantalla.
  - iZoom Standard Magnifier/Reader. Magnificador de pantalla completa, con varios modos de magnificación, puede magnificar hasta 16 veces, e incluye opción de voz sintetizada.
  - iZoom USB Magnifier/Reader. Similar a iZoom, pero disponible en una memoria USB para utilizar en cualquier ordenador sin instalación y sin derechos de administrador.
  - MAGic. De los creadores del lector de pantalla JAWS, incluye múltiples opciones.
  - MaGUI. Magnificador de pantalla gratuito para Microsoft Windows desarrollado en España.
  - The Magnifier. Magnificador de área o pantalla completa, desde 1.1 a 40 niveles de aumento.
  - WinZoom Magnifier/Reader. Magnificador y lector de pantalla, con 8 tipos de zoom y 36 niveles de aumento.
  - WinZoom USB. Similar a WinZoom, pero disponible en una memoria USB para utilizar en cualquier ordenador sin instalación.
  - ZoomText. Desde 1 a 36 niveles de aumento, posee la tecnología xFont para aumentar sin pérdida de calidad el texto, incluye controles de color, contraste y brillo.

## 3.2 Traductores de Braille
Los **traductores de Braille** son herramientas que convierten texto digital en texto legible mediante dispositivos Braille. Estos dispositivos permiten a las personas ciegas o con discapacidad visual **interactuar con contenido web** de manera efectiva. El uso de tecnologías que soporten el Braille en la web mejora la **inclusión digital** y garantiza que las personas con discapacidades visuales tengan acceso a la información de forma autónoma.

Los traductores de Braille se integran con tecnologías de asistencia, como:
- **Lectores de pantalla (Screen Readers)**: Como **NVDA**, **JAWS** o **VoiceOver**, que envían texto a dispositivos de línea Braille.
- **Dispositivos de línea Braille**: Estos dispositivos tienen una serie de celdas dinámicas que suben y bajan puntos en relieve según el contenido que se muestra en pantalla.

<img src="https://github.com/javieregeablasco/DAW/blob/main/DIW/UT.%206%20-%20Accesibilidad%20web%20/img/Braille.jpg">

📋 **Buenas prácticas para desarrolladores web**  
Para garantizar que los traductores de Braille funcionen correctamente en un sitio web, los desarrolladores deben:

1. **Usar etiquetas semánticas correctas**: Como `<header>`, `<main>`, `<nav>`, etc.
2. **Proporcionar texto alternativo (alt)** para imágenes.
3. **Evitar el uso de contenido solo visual**.
4. **Asegurar la navegabilidad por teclado**.
5. **Respetar las recomendaciones de ARIA (Accessible Rich Internet Applications)** para enriquecer la semántica del contenido.

# 4 Hardware específico para mejorar la accesibilidad web
La Norma <a href="https://www.une.org/encuentra-tu-norma/busca-tu-norma/norma?c=N0029860">UNE 139802:2003 Aplicaciones informáticas para personas con discapacidad. Requisitos de accesibilidad al ordenador. Software</a> define los conceptos de dispositivo apuntador, dispositivo de entrada salida, emulador de teclado y emulador de ratón:
```
3.5 dispositivo apuntador: Dispositivo de entrada conectado a un ordenador o a un terminal,
cuya función es mover el cursor por la pantalla para dar órdenes.
Ejemplos: ratón, trackball, joystick, touchpad, headmaster, etc.

3.6 dispositivo entrada/salida: Una combinación de elementos físicos o lógicos para emular el funcionamiento completo
de un único dispositivo de entrada/salida. Es considerado como un único dispositivo en esta norma.

3.7 emulador de teclado: Dispositivo o programa cuyo fin es sustituir al teclado convencional.

3.8 emulador de ratón: Dispositivo o programa cuyo fin es sustituir al ratón convencional.
```
## 4.1 Dispositivo apuntador
Un **dispositivo apuntador** es cualquier hardware o tecnología que permite a una persona **interactuar con una interfaz digital moviendo un puntero** y **seleccionando elementos** en la pantalla. 
Los dispositivos apuntadores van **más allá del mouse tradicional** y están diseñados para ser usados por personas con **movilidad reducida**, **dificultades motoras** o **discapacidades físicas**.

🖱️ **Ejemplos de Dispositivos Apuntadores Accesibles:**
1. **Trackballs:**  
2. **Joysticks:**  
3. **Pantallas Táctiles:**  
4. **Dispositivos de Cabeza (Head Mouse):**  
5. **Eye-Tracking (Seguimiento Ocular):**  
6. **Switches (Pulsadores):**  

📋 **Buenas Prácticas en Diseño Web para Dispositivos Apuntadores:**

| **Práctica**                  | **Descripción**                                              |
|--------------------------------|--------------------------------------------------------------|
| Proporcionar un área de clic grande | Asegura que los botones y enlaces tengan un área suficiente para facilitar el clic. |
| Habilitar navegación por teclado | Muchos dispositivos apuntadores emulan el uso del teclado. Asegúrate de que todo sea accesible con `Tab`. |
| Evitar acciones complejas       | No obligar al usuario a realizar arrastrar y soltar, gestos, o movimientos complicados. |
| Proporcionar retroalimentación visual | Cambiar el estado de los elementos interactivos al enfocarse o seleccionarse. |


## 4.2 Dispositivo de entrada/salida
Un **dispositivo de entrada/salida (E/S)** es un **hardware especializado** que permite a las personas con **discapacidades físicas, sensoriales o cognitivas** interactuar con un sistema digital, enviando información al dispositivo (entrada) y recibiendo retroalimentación (salida). 

### 4.2.1 Dispositivos de Entrada
Permiten a los usuarios **introducir información o realizar acciones** en un sistema digital.

| **Dispositivo**         | **Descripción**                                                            |
|-------------------------|----------------------------------------------------------------------------|
| **Teclado Adaptado**     | Teclados con teclas más grandes, teclas táctiles o teclas de funciones específicas para personas con movilidad reducida. |
| **Mouse Adaptado**       | Trackballs, joysticks y dispositivos que se controlan con la cabeza o los ojos. |
| **Switches (Pulsadores)**| Botones grandes que permiten a los usuarios realizar acciones con un solo clic. |
| **Sistemas de Seguimiento Ocular** | Permiten controlar un sistema digital mediante los movimientos oculares. |
| **Reconocimiento de Voz**| Permite a los usuarios controlar dispositivos y escribir mediante comandos de voz. |
| **Pantallas Táctiles**   | Útiles para personas con discapacidades motoras que no pueden usar un mouse o teclado tradicional. |

### 4.2.2 Dispositivos de Salida
Proporcionan **información de retorno al usuario** para que puedan interactuar de manera efectiva con el contenido digital.

| **Dispositivo**          | **Descripción**                                                            |
|--------------------------|----------------------------------------------------------------------------|
| **Lectores de Pantalla**  | Software que convierte el texto de la pantalla en voz o en braille. Ejemplo: JAWS, NVDA, VoiceOver. |
| **Líneas Braille**        | Dispositivos que convierten el texto de la pantalla en braille táctil para personas con discapacidad visual. |
| **Altavoces o Auriculares** | Utilizados por personas que necesitan retroalimentación auditiva, como aquellos que usan lectores de pantalla. |
| **Dispositivos Hápticos** | Proporcionan retroalimentación táctil (vibraciones) para personas con discapacidades auditivas o visuales. |
| **Pantallas Adaptativas** | Pantallas que pueden mostrar contenido con alto contraste, fuentes grandes o contenido simplificado. |

## 4.3 Emulador de teclado
Un **emulador de teclado** es un dispositivo o software que **simula las funciones de un teclado físico**, permitiendo a personas con **discapacidades físicas o motoras** interactuar con una computadora o sitio web de forma alternativa. 
Un emulador de teclado se utiliza principalmente para **facilitar el acceso digital** a personas con:
- Discapacidades motoras severas (como tetraplejia o parálisis).
- Dificultades para controlar movimientos finos.
- Falta de movilidad en manos o dedos.
- Necesidad de controlar un dispositivo con **movimientos de cabeza, voz, ojos** o mediante **pulsadores**.

Estos dispositivos convierten **diferentes tipos de entradas** (como comandos de voz, movimientos oculares o clics en pantalla) en **comandos de teclado**, permitiendo la interacción con sitios web, aplicaciones y software.

## 4.4 Emulador de ratón
Un **emulador de ratón** es un **dispositivo o software** que permite **simular las funciones de un ratón físico** a través de **entradas alternativas**, como comandos de voz, movimientos oculares, pulsadores o incluso gestos corporales. 
Un emulador de ratón permite:
- **Controlar el cursor del ratón** sin usar las manos.
- **Navegar por páginas web** y aplicaciones sin necesidad de un ratón físico.
- **Realizar clics, arrastres, desplazamientos y selecciones** mediante métodos alternativos.
