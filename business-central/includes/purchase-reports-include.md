---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: ae96e5a3fc1cc7f4b17e5ef208650248cbe0b3c2
ms.sourcegitcommit: 2c972dfc94d27245eaa99efcf638d030dedafb22
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/09/2022
ms.locfileid: "8104262"
---
La siguiente tabla describe algunos de los informes clave en los informes de compra.

|Informe |Id. de objeto|Descripción  |
|---------|---------|---------|
|**Estadísticas compras**|312|[!INCLUDE [reports-purchase-statistics](reports-purchase-statistics.md)]|
|**Proveedor - Lista de los 10 mejores**|311|Muestra información de compras de proveedores durante un periodo determinado. Puede elegir el número de proveedores que desea incluir en el informe.<br>Los proveedores aparecen ordenados por importes, y, opcionalmente, pueden estar ordenados por importe de compras o por saldo. El informe ofrece una rápida visión de los proveedores a los que más se compra o a los que más se debe.|
|**Catálogo de productos de proveedor** o **Catálogo de productos/proveedores**|320 o 720|Muestra una lista de proveedores para los productos seleccionados o productos para proveedores seleccionados. De cada combinación de producto y proveedor se indica el precio de compra, el plazo de entrega (días) y el código de producto del proveedor.<br>En EE. UU., Canadá y México, este informe no está disponible. En su lugar, utilice el informe **Catálogo de productos/proveedores** (10164).|
|**Compras prov./producto**|313|Muestra una lista de los movimientos de productos por cada proveedor durante un periodo determinado. El informe contiene información sobre cantidad facturada, importes y posibles descuentos. Utilícelo, por ejemplo, para analizar compras de productos por parte de la empresa y para saber si existe alguna relación entre descuentos y compras de productos.|
|**Lista de precios y variación de existencias**|716|Muestra una lista con información de precios de los productos seleccionados o las unidades de almacenamiento: precio de compra, último coste directo, precio de venta, porcentaje de beneficio bruto y beneficio bruto.|
|**Proyección existencias en inventario**|707|Si desea tener una descripción general sobre artículos específicos y unidades de almacenamiento y su disponibilidad. Este informe mostrará los valores acumulados como los requisitos brutos, los albaranes programados y planificados, el inventario, etc. |
|**Compras de proveedores de inventario**|714|Muestra una lista de los proveedores a los que su empresa ha adquirido productos en un determinado periodo. Indica la cantidad facturada, el importe y el descuento. Este informe se puede utilizar para analizar las compras de productos de una empresa.|
|**Pedidos compra de inventario**|709|Muestra una lista de los productos pedidos a los proveedores. También muestra la fecha de recepción esperada, así como la cantidad y el importe de los pedidos por servir. Por ejemplo, utilice el informe para ver cuándo se van a recibir los productos y si se debe emitir un aviso de pago para un pedido pendiente.|
|**Disponibilidad reserva compra**|409|Muestra la disponibilidad de los productos para su envío en documentos de compra, como las devoluciones. Determine si el informe reflejará el estado de cada documento o el de cada línea de compra. <br>Cuando imprima el informe, también puede actualizar la cantidad disponible para enviar en el campo **Cdad. a recibir** de las líneas de compra. En los abonos de compra o líneas de pedido de compra negativas, el capo **Cantidad a recibir** contiene la cantidad a enviar. Luego, utilice el informe para determinar qué documentos va a imprimir. **Nota**: Este informe no está disponible para la funcionalidad de almacén avanzada.|
<!--|**Proveedor - Deuda pendiente**|11006| Específico de DACH: un informe que podría utilizar un jefe de equipo de su departamento de compras al igual que el de contabilidad. Aquí tendrá una descripción general de las facturas de proveedores pendientes de pago, incluidas las fechas de vencimiento, las divisas y los importes. La base son los movimientos de proveedores.| -->

