---
author: brentholtorf
ms.topic: include
ms.date: 03/20/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

En los documentos de compra y los diarios, puede especificar un número de documento que haga referencia al sistema de numeración del proveedor. Utilice este campo para registrar el número que el proveedor asignó al pedido, la factura o el abono. Posteriormente podrá utilizar este número si, por alguna razón, necesita buscar la entrada registrada del diario mediante este número.

El campo **N.º doc. externo obligatorio** en la página **Configuración de compras y pagos** especifica si es obligatorio especificar un número de documento externo en las siguientes situaciones:

* En los campos **N.º factura proveedor**, **N.º pedido proveedor** o **Nº abono proveedor** en una cabecera de compra.

* En el campo **Nº documento externo** de una línea del diario general, en la que el campo **Tipo documento** está establecido en *Factura*, *Abono* o *Documento de interés* y el campo **Tipo de cuenta** está establecido en *Proveedor*.

Si selecciona este campo, no se podrá registrar ninguna factura, abono o el tipo de línea del diario cuyo valor en el campo Tipo mov. sea "Cliente" sin haber insertado previamente un número de documento externo.

El número de documento externo se incluye en los documentos registrados donde puede buscar por el número relevante. También puede buscar utilizando el número de documento externo al navegar por los asientos de los movimientos de proveedores.

Una forma diferente de gestionar los números de documento externo es usar el campo **Su referencia**. Si usa el campo **Su referencia**, el número se incluirá en los documentos publicados y puede buscar según este campo de la misma manera que para los valores de los campos **N.º documento externo**. Pero el campo no está disponible en líneas del diario.
