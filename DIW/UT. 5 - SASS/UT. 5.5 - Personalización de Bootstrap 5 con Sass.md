---
Título: UD. 5.5 - Personalización de Bootstrap 5 con Sass
Autor: Javier Egea Blasco
Año: 24-25
Palabras clave: DAW, DIW
---
  
<div align="center">
</br>
<img src="https://github.com/javieregeablasco/DAW/blob/main/DIW/UT.%205%20-%20SASS/img/love_sass.png">
</div>

# 1 Introducción
<a href="https://getbootstrap.com/">**Bootstrap**</a> es una de las librerías más utilizadas para el desarrollo de interfaces web, gracias a su facilidad de uso y diseño responsivo. Sin embargo, cada proyecto tiene requisitos únicos que a menudo exigen personalizar estilos para reflejar una identidad visual específica o mejorar la experiencia del usuario. 

Sass (Syntactically Awesome Stylesheets) permite modificar y extender Bootstrap ajustando colores, tipografías, espacios... y otros aspectos del diseño sin necesidad de sobrescribir clases directamente. Este enfoque no solo acelera el desarrollo y personalización del proyecto, sino que también asegura una mayor flexibilidad y consistencia en el diseño final.

# 2 Instalación de bootstrap: Vite
<img src="https://github.com/javieregeablasco/DAW/blob/main/DIW/UT.%205%20-%20SASS/img/bootstrap-vite.png" width=400px>
Para poder configurar Bootstrap necesitaremos descargar el framework completo de bootstrap, para ello usaremos Vite.  

Más información <a href="https://getbootstrap.com/docs/5.3/getting-started/vite/">aquí</a> 

## 2.1 Crear una carpeta proyecto e inicializar npm
Creamos la carpeta contenedora de nuestro proyecto y abrimos una terminal en nuestro IDE (o directamente desde una powershell para SO windows) y escribimos el siguiente comando.
```
npm init -y
```

## 2.2 Instalar Vite dentro de nuestro proyecto
Instalamos las dependencias de vite con el siguiente comando.
```
npm i --save-dev vite
```
El argumento `--save-dev` indica que la dependencia (en este caso, Vite) se utilizará únicamente en el entorno de desarrollo y no formará parte de las dependencias necesarias para el entorno de producción.

## 2.3 Instalar Bootstrap
La instalación **completa** de Bootstrap usando el siguiente comando.
```
npm i --save bootstrap @popperjs/core
```
## 2.4 Instalar otras dependencias 
Como es evidente, necesitaremos la dependencia de **Sass** para importar correctamente el paquete CSS de Bootstrap.
```
npm i --save-dev sass
```

# 3 Estructura de nuestro proyecto
Para definir la estructura básica de nuestro proyecto, crearemos una carpeta `src` así como los archivos `index.html', `main.js`, `styles.scss` y el archivo de configuración `vite.config.js`
```
New-Item -ItemType File src/index.html, src/js/main.js, src/scss/styles.scss, vite.config.js
```
