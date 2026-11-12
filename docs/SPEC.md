# Especificación — RepartoRuta

Requisitos escritos con el patrón EARS («Cuando…, el sistema deberá…»). Cada uno es verificable con una prueba (ver [PRUEBAS.md](PRUEBAS.md)).

## Alcance de la versión 1.0

Rutas de reparto y preventa: clientes por ruta y día, entregas, cobros y cierre de ruta sin conexión. Funciona en un solo dispositivo, sin cuentas de usuario y sin servidor.

## Requisitos funcionales

| ID | Requisito |
|---|---|
| R01 | Cuando comienza el día, el sistema deberá mostrar los clientes de la ruta asignada a ese día de la semana en su orden de visita. |
| R02 | Cuando el repartidor registra una visita, el sistema deberá marcar al cliente como visitado y sumar el total entregado a su cuenta corriente. |
| R03 | Cuando se registra un cobro, el sistema deberá restar el monto del saldo del cliente. |
| R04 | Si el repartidor no vende, el sistema deberá exigir un motivo de no venta. |
| R05 | Cuando el usuario toca la dirección de un cliente, el sistema deberá abrir la app de mapas del teléfono con la ubicación guardada. |
| R06 | Cuando se cierra la ruta, el sistema deberá calcular entregado, cobrado y saldo pendiente del día. |
| R07 | Si el dispositivo no tiene conexión, el sistema deberá permitir toda la operación de la ruta. |
| R08 | Cuando se reordenan los clientes de una ruta, el sistema deberá conservar el nuevo orden en las visitas siguientes. |

## Requisitos no funcionales

| ID | Requisito |
|---|---|
| N01 | La app deberá abrir en menos de 3 segundos en un teléfono Android de gama baja (2 GB de RAM). |
| N02 | Todos los datos deberán almacenarse en SQLite local y no enviarse a ningún servidor. |
| N03 | La interfaz deberá estar en español con montos en bolivianos (Bs) y fechas dd/mm/aaaa. |
| N04 | Los botones táctiles deberán medir al menos 48 dp. |
| N05 | La app deberá operar completa sin conexión a internet. |
| N06 | El costo de licencias de cualquier dependencia deberá ser cero. |

## Fuera de alcance (v1.0)

- No optimiza rutas automáticamente en la primera versión.
- Sin control de stock del camión de reparto.
- Un solo dispositivo por ruta.

## Criterios de aceptación globales

1. Un usuario nuevo registra su primer dato útil en menos de 5 minutos.
2. Ningún dato se pierde al cerrar la app de forma abrupta.
3. Los totales coinciden con un cálculo manual en los casos de prueba de [PRUEBAS.md](PRUEBAS.md).
