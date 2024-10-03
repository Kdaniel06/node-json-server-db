# Práctica JSON Server Node
Este es un mini servidor que simula datos sobre cursos, maestros y estudiantes. Utiliza json-server para crear rápidamente una API REST en Node.js con el objetivo de facilitar el desarrollo de pruebas y prototipos.

## Descripción
Este proyecto consiste en un pequeño servidor JSON que proporciona datos sobre:

* Profesores: Con su nombre, apellido y los cursos que imparten.
* Estudiantes: Con su nombre, apellido y promedio.
* Cursos: Con su nombre y nivel de dificultad.

El servidor está construido con json-server, lo cual permite ejecutar una API REST con solo usar un archivo JSON.

## Instalación
Sigue los pasos a continuación para clonar el repositorio y ejecutar el servidor localmente.

### Clonar el repositorio
```bash
git clone https://github.com/tu-usuario/practica-json-server-node.git
cd practica-json-server-node
```
### Instalación de dependencias
Asegúrate de tener Node.js instalado. Luego, instala las dependencias ejecutando:

```bash
npm install 
```

## Ejecución
Para iniciar el servidor, ejecuta el siguiente comando:

```bash
npm start
```

Este comando iniciará el servidor usando json-server para el archivo db.json.

Por defecto, el servidor estará disponible en la URL http://localhost:3000.

### Endpoints
Los datos del servidor se pueden acceder a través de los siguientes endpoints:

* Profesores: http://localhost:3000/teachers
* Estudiantes: http://localhost:3000/students
* Cursos: http://localhost:3000/courses

### Ejemplos de Peticiones
#### Obtener todos los profesores
```http
GET /teachers
```

#### Obtener un estudiante específico
```http
GET /students/:id
```

#### Agregar un nuevo curso
```http
POST /courses
```

* Cuerpo:
```json
{
  "name": "New Course",
  "difficulty": 3
}
```

### Estructura de Datos
#### Profesores (teachers):

```json
{
  "id": "string",
  "name": "string",
  "last_name": "string",
  "courses": [
    {
      "name": "string"
    }
  ]
}
```

#### Estudiantes (students):

```json
{
  "id": "string",
  "name": "string",
  "last_name": "string",
  "prom": "number"
}
```

#### Cursos (courses):
```json
{
  "id": "string",
  "name": "string",
  "difficulty": "number"
}
```

## Tecnologías Utilizadas
* Node.js: Entorno de ejecución para JavaScript en el servidor.
* JSON Server: Herramienta para crear APIs REST rápidas a partir de archivos JSON.

## Autor
Daniel Cascante

## Licencia
Este proyecto está bajo la Licencia ISC.

## Contribuciones
Las contribuciones son bienvenidas. Si deseas colaborar, siéntete libre de hacer un fork del proyecto y enviar un pull request.
