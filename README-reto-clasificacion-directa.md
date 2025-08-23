# 🟢 Reto Clasificación Directa – SENASoft 2025

Este proyecto implementa nuevas métricas en el backend de **Leonardo 🚥** usando **NodeJS + Express + MongoDB (Mongoose)**. Con estas métricas, Leonardo puede responder preguntas más detalladas sobre los aprendices inscritos.

## 🚀 Requisitos

- NodeJS v18 o superior
- MongoDB (local o Atlas)
- Git

## ⚙️ Instalación

1. Clonar tu fork del repositorio oficial:

```bash
git clone https://github.com/<tu-usuario>/senasoft.git
cd senasoft/backend/core/nodejs
npm install
```

2. Crear archivo `.env.development` en la raíz con tus variables:

```env
MONGO_URI=mongodb://localhost:27017/learning_metrics
DB_NAME=learning_metrics
ALLOWED_ORIGINS=*
PORT=8080
```

## 🗄️ Preparar la base de datos

Ejecuta el script de configuración (crea colecciones, índices y datos de ejemplo):

```bash
cd database/collection
node setupCollections.js
```

## 🌐 Levantar el servidor

Desde la carpeta `backend/core/nodejs`:

```bash
node server.js
```

Si todo va bien, verás en consola:

```
✅ Conectado a MongoDB Atlas
🚀 Servidor corriendo en el puerto 8080
```

## 📊 Endpoints disponibles

- **Aprendices por centro** → `GET /metrics/inscritos/centro`
- **Instructores recomendados por centro** → `GET /metrics/instructores/centro`
- **Aprendices por centro y programa** → `GET /metrics/inscritos/centro-programa`
- **Aprendices por departamento** → `GET /metrics/inscritos/departamento`
- **Aprendices con GitHub** → `GET /metrics/inscritos/github`
- **Aprendices con inglés B1/B2 por centro** → `GET /metrics/inscritos/ingles`
- **Métricas escalares (existente en repo oficial)** → `GET /metrics/scalar`

## 👥 Equipo

- Diego Alejandro Paloma Diaz
- Eimy Yuliana Yate Quesada
- Juan David Caicedo Robles
