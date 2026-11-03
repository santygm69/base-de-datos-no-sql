# Documentación de la Base de Datos

Este repositorio contiene los archivos JSON que representan las colecciones de la base de datos (NoSQL / MongoDB) para el sistema de gestión de tiendas y productos.

---

## 📐 Estructura General

La base de datos está compuesta por **4 colecciones principales**:

1. **`Cliente`**: Información de contacto e identificación de los clientes.
2. **`Empleado`**: Registros del personal contratado.
3. **`Productos`**: Catálogo de inventario, precios y disponibilidad.
4. **`Sucursales`**: Ubicación geográfica e información de las sedes comerciales.

---

## 🗂️ Detalle de Colecciones y Esquemas

### 1. Colección: `Cliente` (`Cliente.json`)
Almacena los datos personales de los clientes registrados.

| Campo | Tipo de Dato | Descripción | Ejemplo |
| :--- | :--- | :--- | :--- |
| `_id` | `ObjectId` | Identificador único en MongoDB | `6ae35aadef8d1709c0c22750` |
| `nombre` | `String` | Nombre completo del cliente | `"pablo arcila"` |
| `documento` | `String` | Número de identificación | `"1234"` |
| `telefono` | `String` | Número telefónico de contacto | `"3005583950"` |
| `correo` | `String` | Correo electrónico | `"pabloar@hotmail.com"` |

---

### 2. Colección: `Empleado` (`Empleado.json`)
Guarda los registros del personal de la empresa.

| Campo | Tipo de Dato | Descripción | Ejemplo |
| :--- | :--- | :--- | :--- |
| `_id` | `ObjectId` | Identificador único en MongoDB | `6ae36d03ef8d1709c0c22771` |
| `nombre` | `String` | Nombre completo del empleado | `"santiago garcia"` |
| `documento` | `String` | Número de identificación | `"12347"` |
| `telefono` | `String` | Teléfono de contacto | `"3005583958"` |
| `correo` | `String` | Correo electrónico de contacto | `"churrisgarcia@hotmail.com"` |

---

### 3. Colección: `Productos` (`Productos.json`)
Contiene el inventario de artículos disponibles para la venta.

| Campo | Tipo de Dato | Descripción | Opcional | Ejemplo |
| :--- | :--- | :--- | :---: | :--- |
| `_id` | `ObjectId` | Identificador único en MongoDB | No | `6ae369a2ef8d1709c0c22768` |
| `nombre` | `String` | Nombre del producto | No | `"Portatil Lenovo"` |
| `precio` | `Number` | Precio unitario del producto | No | `2500000` |
| `stock` | `Number` | Cantidad física disponible | No | `15` |
| `categoria` | `String` | Categoría a la que pertenece | **Sí** | `"Tecnologia"` |
| `disponible`| `Boolean` | Estado de disponibilidad en tienda | **Sí** | `true` |

*Nota: Algunos productos (como `"Pantalla Lenovo"`) pueden no incluir los campos opcionales `categoria` o `disponible`.*

---

### 4. Colección: `Sucursales` (`Sucursales.json`)
Contiene las sedes físicas o puntos de atención de la empresa.

| Campo | Tipo de Dato | Descripción | Ejemplo |
| :--- | :--- | :--- | :--- |
| `_id` | `ObjectId` | Identificador único en MongoDB | `6ae9ec859b9a3d5be1d087f0` |
| `nombre` | `String` | Nombre o código de la sucursal | `"S&G_monterrey"` |
| `direccion` | `String` | Dirección física del establecimiento | `"cr 45a # 66-50"` |
| `departamento` | `String` | Departamento de ubicación | `"antioquia"` |
| `municipio` | `String` | Ciudad o municipio | `"medellin"` |
| `telefono` | `String` | Teléfono de contacto de la sede | `"3005583939"` |
| `disponible` | `Boolean` | Estado operativo de la sucursal | `true` |

---

## 🛠️ Instrucciones de Importación (MongoDB CLI)

Para importar estos archivos JSON en una base de datos MongoDB local o remota, puedes ejecutar los siguientes comandos utilizando `mongoimport`:

```bash
mongoimport --db mi_tienda --collection Cliente --file Cliente.json --jsonArray
mongoimport --db mi_tienda --collection Empleado --file Empleado.json --jsonArray
mongoimport --db mi_tienda --collection Productos --file Productos.json --jsonArray
mongoimport --db mi_tienda --collection Sucursales --file Sucursales.json --jsonArray
```