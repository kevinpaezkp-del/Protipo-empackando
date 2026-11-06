# PlastiControl — piloto Empackando

Prototipo web público para revisar flujos de producción, inventario, traslados, ventas, despachos, flota y gastos.

## Abrir la demostración
https://kevinpaezkp-del.github.io/Protipo-empackando/

## Novedades: ventas, facturación y cartera
- Precios unitarios configurables en el catálogo, editables por el administrador; cada pedido guarda su precio al registrarse.
- Ventas por referencia y cantidad, subtotal, IVA configurable (0%, 5% o 19%) y retenciones configurables (retefuente, reteIVA, reteICA). El total a cobrar se calcula como subtotal + IVA - retenciones.
- El requerimiento de factura **no cambia automáticamente los impuestos**; la aplicación permite marcar si el cliente la solicita, si ya está emitida y registrar su número.
- Registro de pagos iniciales y abonos adicionales, cálculo automático de estados pagado, parcial, no pagado, y vencimiento.
- Módulo **Cartera y cobros**, con montos pendientes y vencidos y lista de facturas por emitir.
- Operación logística anterior intacta: inventario, producción, transferencias, ventas, flota, remisiones y gastos.

## Cómo probar
En **Ventas y despachos**, abre **Venta para despacho**, agrega cantidades y precios unitarios, configura IVA/retenciones y registra abonos. Luego abre **Cartera y cobros** para revisar saldos y facturas pendientes. Selecciona **Cobro / factura** en un pedido para agregar pagos y registrar la factura.
Los datos de ejemplo son simulados. Para obtener los nuevos ejemplos de cartera en un navegador que ya utilizó la versión anterior, abre en ventana privada o usa el botón para reiniciar el prototipo (este último elimina los cambios guardados en ese navegador).

## Importante: demostración, no uso contable ni productivo
- Los registros se guardan solo en el navegador (**localStorage**); cada persona ve su propio conjunto de datos, sin sincronización ni base de datos central.
- Los archivos de remisión también son locales (**IndexedDB**). No hay autenticación, permisos reales, pagos bancarios, factura electrónica ni integración con DIAN.
- Las tarifas tributarias son ilustrativas y **deben ser validadas por el área contable** según producto, cliente y responsabilidades fiscales. Una venta sin factura solicitada **no está automáticamente exenta de IVA**, y no se puede omitir la factura cuando exista obligación legal de expedirla.
- No ingresar nombres de clientes reales, datos sensibles, cuentas bancarias ni documentos comerciales reales.
- Para pasar a producción se requieren backend, base de datos compartida, gestión de accesos, auditoría y respaldos.
