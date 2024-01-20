# Express JS
### Configuracion inicial
-  Crear una carpeta mi_proyecto.
-  Posicionarse dentro de la carpeta mi_proyecto con CMD.
-  Inicializar proyecto:
`$ npm init -y`
-  Modificar configuracion standard de package.json
```json
[{
  "name": "mis-tareas",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "keywords": [],
  "author": "mi_nombre",
  "license": "MIT"
  }]
```
-  Instalar Express JS:
`$npm install express`
-  Instalar Nodemon:
`$ npm i -D nodemon`
-  Configurar Nodemon en package.json agregando la linea:
`"server":"nodemon app.js"`
```json
{
  "name": "mis-tareas",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1",
    "server": "nodemon app.js" // linea agregada
  },
  "keywords": [],
  "author": "",
  "license": "ISC",
  "dependencies": {
    "express": "^4.18.2"
  },
  "devDependencies": {
    "nodemon": "^3.0.3"
  }
}
```
-  Crear archivo inicial de proyecto app.js

### Configuracion basica de un servidor
```javascript
// app.js
const express = require('express');
const app = express();

const PORT = process.env.PORT || 3000;
app.listen(PORT, console.log(`Servidor corriendo... en localhost:${PORT}`));
```
-  Correr servidor con:
`npm run server`
