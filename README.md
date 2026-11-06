# PlastiControl — piloto Empackando

Prototipo público de gestión de producción, inventarios, transferencias, despachos, flota y gastos.

## Abrir la demostración
Una vez habilitado GitHub Pages (Settings > Pages > Deploy from a branch > main > /(root)), abrir:

https://kevinpaezkp-del.github.io/Protipo-empackando/

El punto de entrada es `index.html`.

## Importante
- Los datos son sintéticos, almacenados solo en el navegador del visitante.
- No hay autenticación real ni sincronización con Google Sheets, Drive o Apps Script.
- Las remisiones se conservan localmente según las restricciones del navegador.
- No introducir información personal real o documentos sensibles.
- La versión V4 elimina el kilometraje, permite traslados con camión propio o tercero, cierre masivo de rutas y remisión independiente por entrega.


## Propuesta en revisión: cobros y facturación por pedido

En la rama `feature/pedidos-cobros-facturas-20261106` se agregó al prototipo:
- Valor total del pedido y abono recibido.
- Estado calculado: **valor pendiente**, **no pagado**, **pago parcial** o **pagado**.
- Indicador de solicitud de factura: **por confirmar**, **no requiere**, **por facturar** o **emitida**, con número de factura cuando corresponda.
- Acción **Cobro / factura** en la tabla de ventas y despachos.
- Validaciones para impedir abonos superiores al valor de la venta.

**Aviso:** esta funcionalidad sigue siendo demostrativa; los registros permanecen solo en el navegador. Los roles no equivalen a autenticación real. No usar este prototipo para cobrar clientes ni guardar facturas reales. Antes de producción se necesita backend, base de datos central, autenticación, auditoría y respaldos.
