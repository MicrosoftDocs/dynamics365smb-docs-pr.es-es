---
author: brentholtorf
ms.topic: include
ms.date: 09/21/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

Los empleados del almacén pueden enviar y recibir artículos que no están en el inventario junto con bienes físicos en órdenes de compra y venta. Los artículos que no están en el inventario son intangibles, como seguros o costes adicionales.

Las órdenes de compra y venta a menudo tienen varios tipos de cosas en sus líneas. Por ejemplo, las órdenes pueden incluir partidas del libro mayor, cuentas y activos fijos. Si utiliza documentos de almacén para manejar artículos físicos, también puede contabilizar algunos tipos de artículos que no son de inventario. Los siguientes son ejemplos de documentos de almacén:

* Almacenamientos de inventario
* Recepciones almacén
* Picking de inventario
* Envíos de almacén

Para permitir que los trabajadores del almacén envíen y reciban artículos que no están en el inventario, complete el campo **Auto Registrar no invt. mediante almac.** en las páginas **Configuración de ventas y cobros** y **Configuración de compras y proveedores**. Este campo proporciona las opciones siguientes:

|Opción  |Descripción  |
|---------|---------|
|Ninguna     |No envíe ni reciba artículos que no estén en el inventario.         |
|Asociado/asignado     | Registre los cargos de artículos y otras líneas de artículos que no están en el inventario y que están asignadas o adjuntas a artículos físicos. Para adjuntar líneas que no son de inventario a artículos físicos, use la acción **Adjuntar a línea de inventario**.        |
|Todo     | Registre todas las líneas que no sean de inventario en el documento de origen tan pronto como el documento de almacén registre al menos un artículo.        |

> [!NOTE]
> La opción **Completar** en el campo **Consejo de envío** de la orden de venta tiene prioridad sobre la selección en el campo **Auto registrar no invent. mediante almac.** en la página **Configuración de ventas y cobros**.