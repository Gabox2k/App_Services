# Changelog

Todas las mejoras y cambios importantes del proyecto **Servicios Asunción** se documentan en este archivo.

---

## [1.1.0] - 2025-03-26

### ✨ Nuevas funcionalidades

* Se implementó carga dinámica de proveedores usando **fetch** desde `proveedores.json`.
* Se agregaron **filtros por categoría**:

  * Todos
  * Plomería
  * Electricidad
  * Pintura

### ⭐ Mejoras

* Las **estrellas de rating ahora se generan dinámicamente** según el valor del proveedor.
* Se organizó el código JavaScript para que sea más mantenible.

### ⚙️ Estados de la aplicación

Se implementaron los 3 estados obligatorios:

* ⏳ **Cargando** → mientras se obtienen los datos del JSON.
* 🚫 **Sin resultados** → cuando no hay proveedores disponibles en una categoría.
* ❌ **Error** → cuando falla la carga del archivo JSON.

### 🧹 Cambios técnicos

* Se eliminó el contenido estático de proveedores en HTML.
* Los proveedores ahora se renderizan dinámicamente desde JavaScript.
* Se creó la función `mostrarProveedores()` para filtrar y renderizar datos.
* Se agregó la función `generarEstrellas()` para mostrar el rating visualmente.

---

## [1.0.0] - 2025-03-20

### 🚀 Versión inicial

* Creación de la página **Servicios Asunción**.
* Diseño de la interfaz con tarjetas de proveedores.
* Secciones incluidas:

  * Inicio
  * Proveedores
  * Cómo funciona
  * Registro de proveedor
* Estilos personalizados con CSS.
