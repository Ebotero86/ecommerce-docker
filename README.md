# 🛒 Ecommerce Full Stack Dockerizado

Proyecto académico que consiste en una aplicación **Full Stack** (Frontend + Backend + Base de Datos) totalmente contenerizada usando **Docker y Docker Compose**.

Este sistema permite ejecutar toda la aplicación con un solo comando, sin necesidad de instalar dependencias manualmente.

---

## 📌 Tecnologías Utilizadas

- **Frontend:** React.js
- **Backend:** Node.js + Express
- **Base de Datos:** MongoDB
- **Contenerización:** Docker y Docker Compose
- **Control de versiones:** Git y GitHub

---

## 📁 Estructura del Proyecto

ecommerce-docker/
│
├── docker-compose.yml
│
├── ecommerce-backend/
│ ├── Dockerfile
│ ├── package.json
│ ├── .env
│ └── src/
│
├── ecommerce-frontend/
│ ├── Dockerfile
│ ├── package.json
│ └── src/
│
└── README.md

yaml
Copiar código

---

## ✅ Requisitos Previos

Debe tener instalado en su equipo:

- Docker
- Docker Compose
- Git

Verificar instalación con:

```bash
docker --version
docker-compose --version
git --version
⚙️ Configuración del Proyecto
1️⃣ Clonar el Repositorio
bash
Copiar código
git clone https://github.com/Ebotero86/ecommerce-docker.git
cd ecommerce-docker
2️⃣ Variables de Entorno del Backend
Archivo ubicado en:

bash
Copiar código
ecommerce-backend/.env
Contenido:

env
Copiar código
MONGO_URI=mongodb://mongo:27017/ecommerce
PORT=4001
⚠️ Importante:
El backend se conecta a MongoDB usando el nombre del servicio (mongo), no localhost.

🐳 Construcción de las Imágenes Docker
Desde la raíz del proyecto, ejecutar:

bash
Copiar código
docker-compose build
Este comando crea las imágenes del:

Frontend

Backend

Base de datos

▶️ Ejecución de la Aplicación
Para levantar todos los servicios:

bash
Copiar código
docker-compose up -d
Verificar que los contenedores estén activos:

bash
Copiar código
docker ps
Debe mostrar:

ecommerce-frontend

ecommerce-backend

ecommerce-mongo

🌐 Accesos al Sistema
Una vez levantados los contenedores:

Frontend:
http://localhost:3000

Backend:
http://localhost:4001



⛔ Detener los Servicios
Para detener y eliminar los contenedores:

bash
Copiar código
docker-compose down
📦 Servicios Definidos en Docker Compose
Servicio	Descripción
mongo	Contenedor de la base de datos MongoDB
backend	API REST en Node.js y Express
frontend	Aplicación web en React

🧪 Pruebas de Funcionamiento
El frontend se muestra correctamente en el navegador.

El backend responde por el puerto 4001.

La base de datos MongoDB se conecta correctamente.

Los tres servicios corren simultáneamente mediante Docker Compose.

✅ Evidencias de Funcionamiento
Se recomienda adjuntar como evidencia:

Captura del comando docker ps

Captura del frontend en el navegador

Captura del backend respondiendo

👨‍💻 Autor Edwin Botero, Mariana Muñoz, Sara Angulo, Juliana Gutierrez
Proyecto realizado con fines académicos para la práctica de:

Contenerización de aplicaciones

Arquitectura Full Stack

Orquestación de servicios con Docker Compose

📄 Licencia
Este proyecto se distribuye con fines educativos.
