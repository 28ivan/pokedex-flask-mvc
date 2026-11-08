# ⚡ Pokédex Web MVC

![Python](https://img.shields.io/badge/Python-3.12%2B-blue?logo=python&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-Web%20Framework-black?logo=flask&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-Database-lightgrey?logo=sqlite&logoColor=white)
![Architecture](https://img.shields.io/badge/Architecture-MVC-orange)

Aplicación web interactiva basada en el patrón de arquitectura **Modelo-Vista-Controlador (MVC)**, desarrollada en **Python** con el microframework **Flask** y base de datos relacional **SQLite**. El sistema implementa autenticación basada en roles, gestión integral de Pokémon y creación de equipos personalizados.

Proyecto desarrollado para la asignatura *Análisis y Diseño de Sistemas de Información (ADSI)* en el Grado en Ingeniería Informática.

---

## 🚀 Características Principales

- **Arquitectura MVC desacoplada:** Separación clara entre modelos de datos, lógica de negocio/controladores y plantillas de presentación (Jinja2).
- **Control de Acceso Basado en Roles (RBAC):**
  - **Administrador:** Gestión de usuarios, administración del catálogo y notificaciones del sistema.
  - **Entrenador:** Exploración de la Pokédex, filtrado avanzado y personalización de equipos Pokémon.
- **Persistencia de Datos:** Esquema relacional en SQLite con datos precargados y scripts de migración/volcado automático (`volcar_pokedex.py`).
- **Interfaz Web Dinámica:** Vistas responsivas desarrolladas con plantillas HTML5, CSS3 y JavaScript interactivo.

---

## 🛠️ Tecnologías Utilizadas

- **Lenguaje:** Python 3.12+
- **Backend / Framework Web:** Flask
- **Base de Datos:** SQLite3
- **Testing:** Pytest
- **Frontend:** Jinja2 Templates, HTML5, CSS3, JavaScript

---

## 📁 Estructura del Proyecto

```text
ADSI_PokeGatas/
├── app/
│   ├── controller/      # Controladores y lógica de negocio
│   │   ├── model/       # Modelos y entidades de datos
│   │   ├── ui/          # Rutas y controladores de interfaz
│   │   └── tests/       # Pruebas unitarias y de integración
│   ├── database/        # Conexión y scripts de esquema SQL (schema.sql)
│   ├── static/          # Recursos estáticos (CSS, JS, imágenes)
│   └── templates/       # Vistas y plantillas Jinja2
├── config.py            # Configuración de la aplicación
├── run.py               # Punto de entrada del servidor Flask
├── requirements.txt     # Dependencias del proyecto
├── database.sqlite      # Base de datos relacional SQLite
└── volcar_pokedex.py    # Script de inicialización y carga de datos
```

---

## ⚙️ Instalación y Puesta en Marcha

### Prerrequisitos
- Python 3.12 o superior instalado.

### 1. Clonar el repositorio
```bash
git clone https://github.com/28ivan/pokedex-flask-mvc.git
cd pokedex-flask-mvc
```

### 2. Crear y activar un entorno virtual (recomendado)
- **Windows (PowerShell):**
  ```powershell
  python -m venv venv
  .\venv\Scripts\Activate.ps1
  ```
- **Linux / macOS:**
  ```bash
  python3 -m venv venv
  source venv/bin/activate
  ```

### 3. Instalar dependencias
```bash
pip install -r requirements.txt
```

### 4. Ejecutar la aplicación
```bash
python run.py
```
Abre tu navegador en `http://localhost:5000` para acceder a la aplicación.

> **Nota sobre la base de datos:** El repositorio incluye `database.sqlite` precargada para probar la aplicación de inmediato. Si deseas reiniciar la base de datos desde cero, elimina el archivo `database.sqlite` y ejecuta `python volcar_pokedex.py` antes de iniciar el servidor.

---

## 🔑 Usuarios de Prueba

Para evaluar los diferentes roles del sistema, se encuentran disponibles las siguientes credenciales:

| Rol | Usuario | Contraseña | Permisos |
| :--- | :--- | :--- | :--- |
| **Administrador** | `admin_jefe` | `admin123` | Acceso al panel de administración y gestión total |
| **Entrenador** | `ash_ketchum` | `pikachu` | Visualización de Pokédex y gestión de equipos |

---

## 👥 Equipo de Desarrollo (Grupo PokeGatas)

- **Ivan Herrera**
- Daniel Talmaci
- June Castro
- Lou Marine Gomez
- David Miguez
