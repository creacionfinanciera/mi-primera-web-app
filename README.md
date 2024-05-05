# mi-primera-web-app

## Introducción 

Este repositorio es para crear una aplicación web a través de `clasp google apps script`.

La documentación de `clasp` en google se encuentra en el siguiente link: `https://developers.google.com/apps-script/guides/clasp?hl=es-419`.
`clasp` te permite desarrollar tus proyectos de Apps Script de forma local. Puedes escribir código en tu propia computadora y subirlo a Apps Script cuando termines. También puedes descargar proyectos existentes de Apps Script para poder editarlos cuando estés sin conexión. Como el código es local, puedes usar tus herramientas de desarrollo favoritas, como git, cuando compiles proyectos de Apps Script.

## Instalación

`clasp` se escribe en Node.js y se distribuye a través de la herramienta npm. Antes de usar clasp, debes tener instalada Node.js 4.7.4 o versiones posteriores. La instalación de Node.js requiere privilegios de administrador.

1. `npm install @google/clasp -g` => para instalar clasp en la terminal
2. `npm install --save @types/google-apps-script` => para instalar el autocompletado de google apps script
3. `https://script.google.com/home` => vamos a este link
4. Vamos a `Configuración`
5. Damos clic en `API de Google Apps Script`
6. Activamos la API si se encuentra desactivada

## Inicio de sesión

1. `clasp login` => nos sirve para inciar sesión y autorizar la administración de los proyectos de google apps script
2. Nos lleva al navegador, seleccionamos la cuenta de google y autorizamos todos los permisos
3. `clasp create mi-primera-app-web` => ahora creamos desde la terminal nuestro proyecto
4. Y seleccionamos el tipo de proyecto, en esta ocasión será un proyecto de google sheets
5. Automaticamente nos crea en VSC dos archivos:
    - `{} .clasp.json` => que nos indica el ID del proyecto
    - `{} appsscript.json` => donde estan los metadatos del proyecto actual, este es el unico archivo que se carga de manera oculta
6. Si vamos a la pantalla de "Mis proyectos" en google apps script, observaremos que nos creo el proyecto

## Creación de archivo

1. Creamos un archivo de javascript `prueba.js`, para que funcione bien el autocompletado de apps script, y despues cuando subamos los cambios, pasara a la plataforma de apps script como `prueba.gs`
2. Escribimos una función con código en VSC y guardamos
3. `clasp push` => para subir desde Visual Studio Code los cambios a google apps script
4. Ahora escribimos código en la plataforma de Google Apps Script, y creamos un archivo más `web.html`
5. `clasp pull` => para bajar los cambios desde la plataforma de google apps script hacia Visual Studio Code

## Clonación de proyecto

1. Copiamos el ID del proyecto existente en la plataforma de google apps script
2. Vamos a "Mis proyectos"
3. Copiamos el ID: `1liUQrhBRQwVQfxBYmV4AY3ZtCv_1Fnt1aeUxn00ObCTe_BYoXjaS6EdG`
4. `mkdir` + `nombre del proyecto` => para crear la carpeta del proyecto en mi entorno local
5. `code .` => para abrir VSC desde la carpeta del nuevo proyecto
6. `clasp clone 1liUQrhBRQwVQfxBYmV4AY3ZtCv_1Fnt1aeUxn00ObCTe_BYoXjaS6EdG` => para clonar el proyecto y bajarlo a mi entorno de trabajo local
7. Visualizamos en Visual Studio Code como nos baja todos los archivos del proyecto
8. Si hacemos cambios a los archivos en VSC
9. Hacemos `clasp push`, y nos sube los cambios hechos a la plataforma de GAS





