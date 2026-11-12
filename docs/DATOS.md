# Modelo de datos — RepartoRuta

Base SQLite local (`expo-sqlite`). Fechas en formato ISO `AAAA-MM-DD`; montos en bolivianos con dos decimales (guardados como enteros en centavos).

## `rutas`

Columnas: id, nombre, dia_semana

## `clientes`

Columnas: id, ruta_id, nombre, direccion, telefono, lat, lng, orden

## `productos`

Columnas: id, nombre, precio, activo

## `visitas`

Columnas: id, cliente_id, fecha, estado, motivo_no_venta

## `visita_items`

Columnas: id, visita_id, producto_id, cantidad, precio

## `cobros`

Columnas: id, cliente_id, fecha, monto

## Reglas generales

- Cada tabla tiene `id` entero autoincremental.
- Los borrados con historial son **lógicos** (campo `activo`) para no romper reportes.
- Cambios de esquema mediante migraciones numeradas en `src/db/migraciones/`.
