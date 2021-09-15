---
title: Informes y análisis de ventas
description: Consulte qué informes y análisis de ventas están disponibles en la versión estándar de Business Central para que pueda realizar un seguimiento de su negocio.
author: AndreiPanko
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: reporting
ms.date: 06/01/2021
ms.author: andreipa
ms.openlocfilehash: b738eeef9771185c6907d963f368c462ae02f2d2
ms.sourcegitcommit: e891484daad25f41c37b269f7ff0b97df9e6dbb0
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/27/2021
ms.locfileid: "7440396"
---
# <a name="sales-reports-and-analytics-in-business-central"></a>Informes y análisis de ventas en Business Central

Los informes de ventas en [!INCLUDE [prod_short](includes/prod_short.md)] permite a los profesionales de las ventas y los negocios obtener información y estadísticas sobre las actividades de ventas actuales y pasadas.  

## <a name="reports"></a>Informes

La siguiente tabla describe algunos de los informes clave en los informes de ventas.

|Informe |Id. de objeto|Descripción  |
|---------|---------|---------|
|**Cliente - Resumen de pedidos**|107| Muestra el desglose de los pedidos con la cantidad no entregada aún de cada cliente en tres periodos consecutivos de 30 días cada uno, a partir de una fecha especificada. Existen también columnas con pedidos a entregar antes y después de los tres periodos, y una columna con el total del desglose de los pedidos por cliente. Utilice el informe para analizar el volumen de ventas previsto por la empresa. |
|**Los 10 mejores clientes**|111| Muestra información de compras y saldos de clientes durante un periodo determinado. Puede elegir el número de clientes que desea incluir en el informe. Solo se incluirán clientes que hayan comprado durante el periodo seleccionado, o que tengan algún saldo al final del mismo.<br>Los clientes aparecen ordenados por importes, y podrá elegir si aparecen ordenados por importe de ventas o por saldo. El informe ofrece una rápida visión de los clientes que más compran o que más deben.|
|**Cliente - Ventas por productos**|113|Muestra una lista de las ventas de producto por cada cliente durante un periodo determinado. El informe contiene información sobre la cantidad, el importe de ventas, el beneficio bruto y los posibles descuentos. Puede servir, por ejemplo, para analizar los grupos de clientes de una empresa.|
|**Ventas de inventario a clientes**|713|Una descripción general desde la perspectiva de la vista del almacén. Esta es una vista diferente en comparación con el informe **Venta de cliente/producto**, y muestra el artículo primero y luego el cliente que compró este producto.|
|**Cliente - Lista ventas**|119|Muestra las ventas a clientes durante un periodo. Utilícelo para informar a las autoridades fiscales y aduaneras. Puede elegir incluir sólo clientes cuyas ventas totales superen una cantidad mínima. También puede especificar si desea que el informe muestre detalles de direcciones de cada cliente.<br>El informe se basa en ventas registradas en DL de los movimientos de clientes. En la parte inferior del informe, se muestra el total de ventas en DL. El total se basa en los clientes que ha incluido en el informe, es decir, los clientes que están incluidos en los filtros de la ficha desplegable Cliente y cuyas ventas totales son mayores que la cantidad especificada en el campo **Importes (DL) mayores de** de la ficha desplegable **Opciones**.|
|**Cliente - Saldo por fechas**|121|Muestra un saldo detallado para los clientes seleccionados. Use el informe al cierre de un periodo contable o ejercicio, por ejemplo.|
|**Cliente - Balance comprobación**|129|Muestra un saldo detallado para los clientes seleccionados. Puede utilizar el informe para comprobar que el saldo de un grupo contable de clientes es igual que el saldo de la cuenta contable correspondiente en una fecha determinada. Use el informe al cierre de un periodo contable o ejercicio, por ejemplo. Si necesita una versión más detallada de este tipo de informe, utilice el informe **Balance de comprobación de los detalles del cliente** (104).|
|**Estadísticas ventas**|112|[!INCLUDE [reports-sales-statistics](includes/reports-sales-statistics.md)] |
|**Disponib. reserva venta**|209|Muestra la disponibilidad de productos para su envío en documentos de venta. Determine el que el informe refleje el estado de cada documento o el de cada línea de venta. Cuando imprima el informe, también puede actualizar la cantidad disponible para enviar en el campo **Cdad. a enviar** de las líneas de venta. Luego, utilice el informe para determinar qué documentos va a imprimir.<br>También existe una función con la que puede establecer la cantidad de mercancías que se enviarán. **Nota**: Este informe no está disponible para la funcionalidad de almacén avanzada.|
|**Estado envío almacén**|7313|Este informe se puede utilizar para todas las ubicaciones, donde el campo **Envío requerido** esté seleccionado. El informe **Estado de envío de almacén** muestra todos los documentos de envío de almacén no contabilizados, incluidos los almacenes, los códigos de ubicación, el estado del documento, las cantidades, etc. Este informe es perfecto para obtener una descripción general.|
|**Listado picking almacén**|813|Muestra una lista de los pedidos de ventas en los que se incluye un producto determinado. Se proporciona la siguiente información de cada producto: la línea de pedido de venta con el nombre del cliente, el código de variante, el código de almacén, el código de ubicación, la fecha de entrega, la cantidad a enviar y la unidad. Por cada producto se totaliza la cantidad a enviar. El informe se puede utilizar cuando los productos se recogen del stock.<br>**Nota**: Este informe no está disponible para la funcionalidad de almacén avanzada.|
|**Productos - Pedidos por servir**|718|Muestra una lista con las líneas de pedido cuya fecha de entrega ya ha pasado. Se proporciona la siguiente información del pedido de cada producto: número, nombre del cliente, número de teléfono del cliente, fecha de entrega, cantidad del pedido y cantidad en pedidos pendientes. El informe también muestra si existen otros productos para el cliente en pedidos pendientes.|
|**Inventario - Desglose pedidos**|708|Muestra una lista de pedidos que aun no se han enviado y los productos en los pedidos. Indica el número de pedido, el nombre del cliente, la fecha de entrega, la cantidad del pedido, la cantidad pendiente y el precio unitario, así como el posible porcentaje e importe del descuento. La cantidad en pedidos pendientes, y la cantidad y el importe pendientes, se totalizan para cada producto. Utilice el informe para averiguar si existen, o se puede suponer que existan, problemas de entrega en la actualidad.|



## <a name="tasks"></a>Tareas

Los siguientes artículos describen algunas de las tareas clave para analizar el estado de su empresa:

* [Crear informes de análisis](bi-how-create-analysis-views-reports.md)  
* [Consultar la disponibilidad de los productos](inventory-how-availability-overview.md)


## <a name="see-also"></a>Consulte también .

[Configuración de ventas](sales-setup-sales.md)  
[Ccial](sales-manage-sales.md)  
[Reservar artículos](inventory-how-to-reserve-items.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
