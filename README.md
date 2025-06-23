# Classroom Management System

Este proyecto es un sistema de gestión de aulas, asignaturas, docentes y estudiantes. Está diseñado para facilitar la administración educativa en instituciones académicas, permitiendo una organización clara de los recursos y asignaciones.

## 📚 Funcionalidades Principales

- **Gestión de Aulas**: Crear, listar y asignar aulas a distintas asignaturas.
- **Gestión de Asignaturas**: Crear asignaturas asignando un docente y un conjunto limitado de estudiantes.
- **Gestión de Docentes**: Registrar docentes y asignarlos a las asignaturas correspondientes.
- **Gestión de Estudiantes**: Registrar estudiantes y asignarlos a asignaturas respetando la capacidad máxima.
- **Validaciones**: Evita la duplicación de asignaturas para el mismo estudiante y docente. Valida la capacidad máxima de estudiantes por asignatura.

## 📁 Estructura del Proyecto

```
backend/
├── config/
│   └── database.js         # Configuración de la conexión Sequelize
├── models/                 # Definición de modelos Sequelize
├── controllers/            # Lógica de negocio y validaciones
├── routes/                 # Rutas API REST
├── migrations/             # Migraciones para la base de datos
├── seeders/                # Datos iniciales (semillas)
└── server.js               # Archivo principal del servidor
```

## 🚀 Scripts Disponibles

Estos scripts te permiten gestionar la base de datos y levantar el servidor fácilmente.

```bash
# Ejecutar el servidor en modo desarrollo con nodemon
npm run dev

# Ejecutar el servidor en modo producción
npm start

# Crear la base de datos
npm run db:create

# Eliminar la base de datos
npm run db:drop

# Ejecutar migraciones
npm run db:migrate

# Revertir todas las migraciones
npm run db:migrate:undo:all

# Ejecutar todos los seeders
npm run db:seed:all

# Revertir todos los seeders
npm run db:seed:undo:all
```

## 🛠️ Tecnologías Utilizadas

- **Node.js** - Entorno de ejecución del servidor
- **Express** - Framework web
- **Sequelize** - ORM para interacción con base de datos
- **PostgreSQL** - Motor de base de datos
- **Nodemon** - Recarga automática del servidor en desarrollo

## 📦 Instalación

1. Clona este repositorio.
2. Instala las dependencias:

```bash
npm install
```

3. Crea la base de datos y ejecuta las migraciones y seeders:

```bash
npm run db:create
npm run db:migrate
npm run db:seed:all
```

4. Ejecuta el servidor:

```bash
npm run dev
```

## ✅ Notas Adicionales

- Se recomienda utilizar herramientas como Postman para probar las rutas.
- Las relaciones están bien definidas con Sequelize, evitando la necesidad de insertar relaciones manuales.
- La validación de la capacidad de estudiantes por asignatura se realiza en el servicio antes de guardar.

---

Desarrollado con ❤️ para facilitar la administración académica.