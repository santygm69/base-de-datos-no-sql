# 🛒 S&G TIENDAS - Sistema de Gestión

Sistema de escritorio desarrollado en **Python** utilizando **Tkinter** para la interfaz gráfica de usuario (GUI) y **MongoDB** como base de datos NoSQL para la gestión integral de una red de tiendas.

---

## 🚀 Características Principales

El sistema está estructurado mediante un menú principal intuitivo que permite realizar las siguientes operaciones:

1. **Gestión de Empleados:** Registro de colaboradores con datos de identificación, contacto y correo electrónico.
2. **Control de Productos:** Registro detallado de inventario (nombre, precio, stock, categoría y estado de disponibilidad).
3. **Administración de Sucursales:** Registro de ubicaciones físicas especificando dirección, departamento, municipio y teléfonos de contacto.
4. **Gestión de Clientes:** Base de datos de clientes con información personal y de contacto.
5. **Consultas Generales:** Visualización organizada mediante pestañas y tablas (`ttk.Treeview`) con barra de desplazamiento para cada una de las colecciones.
6. **Consultas Específicas y Resúmenes:** 
   - Conteo en tiempo real de los documentos en cada colección.
   - Buscador dinámico por nombre utilizando expresiones regulares (`$regex`) con soporte para coincidencias parciales e insensibles a mayúsculas.

---

## 🛠️ Tecnologías y Librerías Utilizadas

* **Python 3.x** - Lenguaje de programación principal.
* **Tkinter & ttk** - Biblioteca estándar de Python para la creación de interfaces gráficas de usuario.
* **PyMongo** - Conector oficial de Python para interactuar con MongoDB.
* **MongoDB** - Sistema de base de datos NoSQL orientado a documentos.

---

## ⚙️ Requisitos Previos

Antes de ejecutar la aplicación, asegúrate de tener instalado lo siguiente en tu equipo:

1. **Python** (versión 3.8 o superior recomendada).
2. **MongoDB Community Server** en ejecución localmente (puerto predeterminado `27017`).
3. La librería `pymongo`. Puedes instalarla ejecutando el siguiente comando en tu terminal:
   ```bash
   pip install pymongo