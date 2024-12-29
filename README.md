# **Task Manager**

Este repositorio es el contenedor principal para los submódulos de los proyectos **Task Manager API** (backend) y **Task Manager Frontend** (frontend). Contiene enlaces a los repositorios de cada parte y permite gestionar ambas aplicaciones como un único proyecto.

Las aplicaciones están desplegadas en : 

- App: [https://cdcm-task-manager.netlify.app/](https://cdcm-task-manager.netlify.app/)
- Api: [https://task-manager-api-6ubk.onrender.com/](https://task-manager-api-6ubk.onrender.com/)

---

## **Video de Demostración**
Haz clic en el siguiente enlace para ver el video de presentación:

[Video de Presentación](https://drive.google.com/drive/folders/1WRcwv0Qyel1bczmZ7d-0FGR5ST6Yb47k?usp=sharing)

--- 

## **Estructura del Proyecto**

Este proyecto está compuesto por los siguientes submódulos:

- **Task Manager API**: [Repositorio Backend](https://github.com/123CarlosDaniel/task-manager-api)
- **Task Manager Frontend**: [Repositorio Frontend](https://github.com/123CarlosDaniel/task-manager-frontend)

La estructura es la siguiente:

```plaintext
task-manager/
├── api/              # Submódulo del backend (API)
├── frontend/         # Submódulo del frontend
└── README.md         # Este archivo
```

--- 

## **Requisitos**

Antes de comenzar, asegúrate de tener instalado:

- **GIt**: Para manejar submódulos.
- **Node.js**: versión 22 o superior.
- **npm**: versión 10 o superior.

---

## **Configuración del Proyecto**

### 1. **Clonar el Repositorio**
Para clonar el repositorio con los submódulos, usa el siguiente comando:
```bash
git clone --recurse-submodules https://github.com/123CarlosDaniel/task-manager.git
cd task-manager
```

### 2. **Actualizar Submódulos**
Si ya tienes el repositorio clonado pero olvidaste incluir los submódulos, puedes inicializarlos con:

```bash
git submodule update --init --recursive
```


### 3. **Configurar Variables de Entorno**
- Backend (Task Manager API)
Configura el archivo .env en la raíz del submódulo task-manager-api con las variables:

```plaintext
SUPABASE_PROJECT_URL=<tu_supabase_project_url>
SUPABASE_ANON_KEY=<tu_supabase_anon_key>
PORT=3000
APP_URL=<url_de_tu_app_frontend>
```

- Frontend (Task Manager Frontend)
Configura el archivo .env.local en la raíz del submódulo task-manager-frontend con las variables:

```plaintext	
VITE_API_URL=<url_de_tu_api_backend>
VITE_APP_URL=<url_de_tu_app_frontend>
VITE_SUPABASE_PROJECT_URL=<tu_supabase_project_url>
VITE_SUPABASE_ANON_KEY=<tu_supabase_anon_key>
```
Consulta los README de los submódulos para más detalles sobre la configuración de estas variables.

## Iniciar ambos proyectos

### 1. Iniciar el Backend (Task Manager API)
Accede a la carpeta del backend (task-manager-api), instala las dependencias, y ejecuta la aplicación:
```bash
cd task-manager-api
npm install
npm run dev
```
El backend estará corriendo en http://localhost:3000 de manera predeterminada.

### 2. Iniciar el Frontend (Task Manager Frontend)
Accede a la carpeta del frontend (task-manager-frontend), instala las dependencias, y ejecuta la aplicación:
```bash
cd task-manager-frontend
npm install
npm run dev
```
El frontend estará corriendo en http://localhost:5173 de manera predeterminada.

