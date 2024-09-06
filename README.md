# git_practice

Instrucciones
Objetivo:
Practicar el proceso de creación, revisión y fusión de Pull Requests (PRs) en GitHub, trabajando en equipos de 2 o 3 personas. Cada equipo creará dos ramas, cada una con una nueva funcionalidad, y realizará PRs para ambas.

Duración 30 minutos
1. Repositorio Base
Repositorio

En el repositorio de GitHub encontrarás lo siguiente un archivo index.js con la siguiente estructura inicial:
// index.js
function greet(name) {
    return `Hello, ${name}!`;
}

console.log(greet("World"));
Objetivos
**Paso 1: Crear dos ramas **
En tu equipo, selecciona dos tareas o mejoras para el proyecto. Cada tarea se implementará en una rama diferente.

Ejemplo de tarea 1: Modificar la función greet para soportar múltiples idiomas.
Ejemplo de tarea 2: Agregar una nueva función farewell(name) para despedidas.
Crea una nueva rama para cada tarea:

Crear la primera rama (para la tarea 1):

git checkout -b nombre-de-la-rama1
Crear la segunda rama (para la tarea 2):

git checkout -b nombre-de-la-rama2
Paso 2: Realizar los cambios en cada rama
En la rama 1:

Modifica la función greet para que soporte múltiples idiomas.
Ejemplo de cambio:

function greet(name, language = "en") {
    if (language === "es") {
        return `¡Hola, ${name}!`;
    } else if (language === "fr") {
        return `Bonjour, ${name}!`;
    }
    return `Hello, ${name}!`;
}

console.log(greet("World", "es"));
En la rama 2:

Agrega una nueva función llamada farewell para despedir al usuario.
Ejemplo de cambio:

function farewell(name) {
    return `Goodbye, ${name}!`;
}

console.log(farewell("World"));
Paso 3: Hacer commit de los cambios en cada rama
En la rama 1 (función greet):

Añade el archivo modificado a Git:
git add index.js
Realiza el commit con un mensaje claro:
git commit -m "Modificado greet para soportar múltiples idiomas"
En la rama 2 (función farewell):

Añade el archivo modificado a Git:
git add index.js
Realiza el commit con un mensaje claro:
git commit -m "Agregada función farewell para despedidas"
Paso 4: Subir las ramas a GitHub
Sube la primera rama al repositorio remoto:

git push origin nombre-de-la-rama1
Sube la segunda rama al repositorio remoto:

git push origin nombre-de-la-rama2
Paso 5: Crear Pull Requests para ambas ramas
Dirígete al repositorio en GitHub.
Crea un PR para la primera rama (nombre-de-la-rama1) con una descripción clara. Ejemplo:
Este PR modifica la función greet para soportar múltiples idiomas. Ahora se puede saludar en español y francés.
Crea otro PR para la segunda rama (nombre-de-la-rama2). Ejemplo:
Este PR agrega la función farewell para despedir al usuario.
Paso 6: Fusión de los PRs
Una vez que ambos PRs han sido aprobados, fusiona las ramas a main:

git checkout main
git pull origin main
git merge nombre-de-la-rama1
git merge nombre-de-la-rama2
Actualiza tu repositorio local para reflejar los cambios:

git pull origin main
