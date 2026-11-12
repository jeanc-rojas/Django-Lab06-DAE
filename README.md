# Django - Laboratorio 06 (Tienda Virtual)

Aplicación web de comercio electrónico desarrollada en **Django** para el Laboratorio 06 del curso **Desarrollo de Aplicaciones Empresariales (DAE)**. Combina modelos relacionales de categorías y productos, manejo de archivos multimedia (`media/`), procesadores de contexto personalizados y una interfaz responsiva basada en **Bootstrap**.

## Características Principales

* **Catálogo por Categorías y Productos:** Navegación estructurada mediante plantilla base (`layout.html`), vista principal (`index.html`) y detalle de producto (`producto.html`).
* **Procesador de Contexto (`context_processors.py`):** Inyección global de categorías/datos en todas las vistas del sitio.
* **Gestión Multimedia (`media/`):** Carga y visualización de imágenes reales para categorías (gaseosas, snacks) y productos.
* **Diseño Frontend:** Integración de Bootstrap, jQuery y estilos propios (`shop.css`).

## Estructura del Proyecto

```text
Django-Lab06-DAE/
├── manage.py
├── db.sqlite3                  # Base de datos SQLite con registros de prueba
├── DAE_Laboratorio 6.pdf       # Informe y capturas del desarrollo del laboratorio
├── lab06/                      # Configuración principal, rutas y media settings
├── media/                      # Imágenes subidas para categorias/ y productos/
└── tienda/                     # Aplicación de la tienda virtual
    ├── models.py               # Modelos Categoria y Producto con ImageField
    ├── context_processors.py   # Context processor global
    ├── static/                 # Recursos Bootstrap, jQuery y shop.css
    └── templates/              # Plantillas layout.html, index.html y producto.html
```

## Requisitos Previos

* **Python** 3.10 o superior.
* **Django** y **Pillow** (requerido para gestionar campos `ImageField`).

## Instalación y Ejecución

1. Clona el repositorio:
   ```bash
   git clone https://github.com
   cd Django-Lab06-DAE
   ```
2. Crea y activa un entorno virtual:
   ```bash
   python -m venv venv
   venv\Scripts\activate
   ```
3. Instala las dependencias:
   ```bash
   pip install django pillow
   ```
4. Ejecuta el servidor de desarrollo desde la raíz:
   ```bash
   python manage.py runserver
   ```
   Accede a `http://127.0.0` para ver la tienda o a `http://127.0.0admin/` para administrar productos y categorías.
