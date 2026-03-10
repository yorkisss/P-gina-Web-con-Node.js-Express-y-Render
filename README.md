# P-gina-Web-con-Node.js-Express-y-Render

# Objetivo ✔️
Este proyecto consiste en la adaptación de una plantilla web  obtenida del sitio HTML Codex para que funcione dentro de un servidor web desarrollado con Node.js y Express.js.

La aplicación permite servir archivos estáticos como HTML, CSS, JavaScript e imágenes a través de un servidor backend. Posteriormente, el proyecto fue desplegado en la nube utilizando la plataforma de hosting Render.

El objetivo de esta actividad es comprender cómo integrar una página web estática con un entorno de servidor y realizar su despliegue en internet.

# Proceso (breve) ✔️
Lo primero es crear nuestro paquete JSON con npm init -y. Luego instalar el paquete express con npm install express y finalmente el archivo .js con las directrices del proyecto,  y con node servidor.js, para confirmar que nuentro proyecto esta corriendo en el puerto 3000 (en mi caso)

# Codigo del archivo servidor.js 💻
const express = require('express');
const path = require('path');

const app = express();
const PORT = process.env.PORT || 3000;


app.use(express.static(path.join(__dirname)));

app.get('/', (req, res) => {
    res.sendFile(path.join(__dirname, 'index.html'));
});

app.listen(PORT, () => {
    console.log(`Servidor corriendo en puerto ${PORT}`);
});
# Posteriormente creo mi repositorio en GitHub 💻
Aqui simplemente inicio con git init y confirmo el estado de mi proyecto con git status, despues con un git add . agrego los archivos y demas, asi mismo con git commit -m hago mi commit, para notificar que agregue a mi repositorio todo mi trabajo. Y finalmente con el git push -u origin main y  subo TODO EL PROYECTO.

# Subir proyecto a Render 📝
1. Subo el proyecto a un repositorio en GitHub.
2. Conecto el repositorio con la plataforma Render.
3. Creo un nuevo Web Service.
4. Configuro con  los siguientes comandos:
   npm install (Build Command)
   node servidor.js (Start Command)
5. Finalmente expero unos segundos para la subida completa, y asi subo el proyecto publico.
