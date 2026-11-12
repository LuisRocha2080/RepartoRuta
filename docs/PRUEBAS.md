# Plan de pruebas — RepartoRuta

## Automáticas (Jest)

La lógica de cálculo vive en `src/lib/` y se prueba sin interfaz.

- [ ] Selección de ruta según día de la semana.
- [ ] Visita con varios productos y cobro parcial.
- [ ] Cierre con diferencia de caja.
- [ ] Reordenamiento de clientes.
- [ ] Apertura del mapa con coordenadas vacías.

## Manuales en teléfono real

- [ ] Instalación del APK en Android 10 o superior.
- [ ] Uso completo en modo avión.
- [ ] Cierre abrupto de la app y reapertura sin pérdida de datos.
- [ ] Exportación y apertura del archivo en otra app.

## Comandos

```bash
npm test
npx tsc --noEmit
```
