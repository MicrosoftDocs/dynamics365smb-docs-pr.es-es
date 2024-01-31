---
author: brentholtorf
ms.topic: include
ms.date: 05/27/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

En los documentos de venta y los diarios, puede especificar un número de documento que haga referencia al sistema de numeración del cliente. <!--You can enter a maximum of ten characters, both numbers and letters.--> Utilice este campo para registrar el número que el cliente asignó al pedido, la factura o el abono. Posteriormente podrá utilizar este número si, por alguna razón, necesita buscar la entrada registrada del diario mediante este número.  

El campo **N.º doc. externo obligatorio** en la página **Configuración de ventas y cobros** especifica si es obligatorio introducir un número de documento externo en el campo **N.º documento externo** en una cabecera de ventas y el campo **N.º documento externo** en una línea de diario general.

Si selecciona este campo, no se podrá registrar ninguna factura ni ninguna línea de diario sin un número de documento externo.

El número de documento externo se incluye en los documentos registrados donde puede buscar por el número relevante. También puede buscar utilizando el número de documento externo al navegar por los asientos de los movimientos de clientes.

Una forma diferente de gestionar los números de documento externo es usar el campo **Su referencia**. Si usa el campo **Su referencia**, el número se incluirá en los documentos publicados y puede buscar según este campo de la misma manera que para los valores de los campos **N.º documento externo**. Pero el campo no está disponible en líneas del diario.
