---
title: Informes y análisis de compra
description: Consulte qué informes y análisis de compra están disponibles en la versión estándar de Business Central para que pueda realizar un seguimiento de su negocio.
author: AndreiPanko
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: reporting
ms.date: 06/01/2021
ms.author: andreipa
ms.openlocfilehash: 5fc64db4120b80203f99742ed3ed834b23370c47
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216399"
---
# <a name="purchase-reports-and-analytics-in-business-central"></a>Informes y análisis de compra en Business Central

Los informes de compra en [!INCLUDE [prod_short](includes/prod_short.md)] permite a los profesionales de la adquisición y los negocios obtener información y estadísticas sobre las actividades de compra actuales y pasadas.  

## <a name="reports"></a>Informes

La siguiente tabla describe algunos de los informes clave en los informes de compra.

|Informe |Id. de objeto|Descripción  |
|---------|---------|---------|
|**Estadísticas compras**|312|Muestra las estadísticas de compra de cada proveedor. Esto incluye información para cinco períodos, comenzando en la fecha que especifique.<br>
El informe incluye el total de compras, pagos, intereses e información de descuento, incluidos los descuentos por pronto pago obtenidos y perdidos. Las estadísticas se calculan para las compras anteriores a la fecha especificada, en tres intervalos de un mes a partir de la fecha indicada y para un período que incluye todas las compras realizadas después del tercer intervalo de un mes.|
|**Proveedor - Lista de los 10 mejores**|311|Muestra información de compras de proveedores durante un periodo determinado. Puede elegir el número de proveedores que desea incluir en el informe.<br>Los proveedores aparecen ordenados por importes, y, opcionalmente, pueden estar ordenados por importe de compras o por saldo. El informe ofrece una rápida visión de los proveedores a los que más se compra o a los que más se debe.|
|**Catálogo de productos de proveedor** o **Catálogo de productos/proveedores**|320 o 720|Muestra una lista de proveedores para los productos seleccionados o productos para proveedores seleccionados. De cada combinación de producto y proveedor se indica el precio de compra, el plazo de entrega (días) y el código de producto del proveedor.<br>En EE. UU., Canadá y México, este informe no está disponible. En su lugar, utilice el informe **Catálogo de productos/proveedores** (10164).|
|**Compras prov./producto**|313|Muestra una lista de los movimientos de productos por cada proveedor durante un periodo determinado. El informe contiene información sobre cantidad facturada, importes y posibles descuentos. Utilícelo, por ejemplo, para analizar compras de productos por parte de la empresa y para saber si existe alguna relación entre descuentos y compras de productos.|
|**Lista de precios y variación de existencias**|716|Muestra una lista con información de precios de los productos seleccionados o las unidades de almacenamiento: precio de compra, último coste directo, precio de venta, porcentaje de beneficio bruto y beneficio bruto.|
|**Proyección existencias en inventario**|707|Si desea tener una descripción general sobre artículos específicos y unidades de almacenamiento y su disponibilidad. Este informe mostrará los valores acumulados como los requisitos brutos, los albaranes programados y planificados, el inventario, etc. |
|**Compras de proveedores de inventario**|714|Muestra una lista de los proveedores a los que su empresa ha adquirido productos en un determinado periodo. Indica la cantidad facturada, el importe y el descuento. Este informe se puede utilizar para analizar las compras de productos de una empresa.|
|**Pedidos compra de inventario**|709|Muestra una lista de los productos pedidos a los proveedores. También muestra la fecha de recepción esperada, así como la cantidad y el importe de los pedidos por servir. Por ejemplo, utilice el informe para ver cuándo se van a recibir los productos y si se debe emitir un aviso de pago para un pedido pendiente.|
|**Disponibilidad reserva compra**|409|Muestra la disponibilidad de los productos para su envío en documentos de compra, como las devoluciones. Determine si el informe reflejará el estado de cada documento o el de cada línea de compra. <br>Cuando imprima el informe, también puede actualizar la cantidad disponible para enviar en el campo **Cdad. a recibir** de las líneas de compra. En los abonos de compra o líneas de pedido de compra negativas, el capo **Cantidad a recibir** contiene la cantidad a enviar. Luego, utilice el informe para determinar qué documentos va a imprimir. **Nota**: Este informe no está disponible para la funcionalidad de almacén avanzada.|
<!--|**Proveedor - Deuda pendiente**|11006| Específico de DACH: un informe que podría utilizar un jefe de equipo de su departamento de compras al igual que el de contabilidad. Aquí tendrá una descripción general de las facturas de proveedores pendientes de pago, incluidas las fechas de vencimiento, las divisas y los importes. La base son los movimientos de proveedores.| -->




## <a name="tasks"></a>Tareas

Los siguientes artículos describen algunas de las tareas clave para analizar el estado de su empresa:

* [Crear informes de análisis](bi-how-create-analysis-views-reports.md)  
* [Consultar la disponibilidad de los productos](inventory-how-availability-overview.md)  


## <a name="see-also"></a>Consulte también .

[Configurar compras](purchasing-setup-purchasing.md)  
[Compras](purchasing-manage-purchasing.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
