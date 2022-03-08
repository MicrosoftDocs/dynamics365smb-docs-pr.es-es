---
title: Informes y análisis de inventario y almacén
description: Consulte qué informes y análisis de inventario y almacén están disponibles en la versión estándar de Business Central para que pueda realizar un seguimiento de su negocio.
author: AndreiPanko
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: reporting
ms.date: 06/01/2021
ms.author: andreipa
ms.openlocfilehash: 8a4418699f28acd3ede80616ba69c56f50781e43
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216397"
---
# <a name="inventory-and-warehouse-reports-and-analytics-in-business-central"></a>Informes y análisis de inventario y almacén en Business Central

Los informes de inventario y almacén en [!INCLUDE [prod_short](includes/prod_short.md)] permite a los profesionales de la producción y los negocios obtener información y estadísticas sobre las actividades de inventario y almacén actuales y pasadas.  

## <a name="reports"></a>Informes

La siguiente tabla describe algunos de los informes clave en los informes de inventario y almacén.

|Informe |Id. de objeto|Descripción  |
|---------|---------|---------|
|**Proyección existencias en inventario**|707|Si desea tener una descripción general sobre artículos específicos y unidades de almacenamiento y su disponibilidad. Este informe muestra valores acumulados como los requisitos brutos, los albaranes programados y planificados, el inventario, etc. |
|**Valoración inventario**|1001|Muestra la valoración de inventario de los productos seleccionados en el inventario. El informe también proporciona información sobre el valor de las entradas y salidas del inventario con el tiempo.|
|**Caducidad producto - Cantidad**|5809|Muestra un panorama de las cantidades de los productos seleccionados en el inventario, cuyas fechas de caducidad se encuentran dentro de un periodo establecido. El listado muestra el número de unidades del producto seleccionado que caducarán en un cierto periodo de tiempo. Para cada uno de los productos que especificó al configurar el informe, el documento impreso muestra el número de unidades que caducarán durante los tres periodos de igual longitud, así como la cantidad total disponible en el inventario del producto seleccionado.<br>Especifique lo que se va a incluir en el informe mediante la aplicación de filtros. Si no define filtros, el informe incluirá todos los registros. Las cantidades expresadas en el informe solamente reflejan las cantidades de aquellos productos para los cuales se han definido unas fechas de caducidad.|
|**Composición antig. prod. - Cant.** o **Composición antig. prod.-valor**|5807 o 5808|Muestra un panorama de la composición de antigüedad de los productos seleccionados en las existencias. La lista contiene el número de unidades o valor del producto seleccionado que se agregaron o retiraron de las existencias y en qué momento. Los productos se pueden agregar a las existencias o retirar de éstas como resultado de las compras, ventas o entradas y salidas.|
|**Lista de precios y variación de existencias**|716|Muestra una lista con información de precios de los productos seleccionados o las unidades de almacenamiento: precio de compra, último coste directo, precio de venta, porcentaje de beneficio bruto y beneficio bruto. |
|**Lista ubicación almacén**|7319|Muestra una descripción general de las ubicaciones de almacén, su configuración y la cantidad de productos en las ubicaciones. Este informe se puede utilizar para todas las ubicaciones que tienen "ubicación" como campo obligatorio. |
|**Estado envío almacén**|7313|Muestra un resumen de documentos de origen abiertos que incluyen productos enviados o pendientes de envío por ubicación. Este informe se puede utilizar para todas las ubicaciones, donde **Envíos obligatorios** esté habilitado. **Estado envío almacén** muestra almacenes, códigos de ubicación, estado del documento, cantidades.|
|**Listado picking almacén**|813|Muestra una lista de los pedidos de ventas en los que se incluye un producto determinado. Se proporciona la siguiente información de cada producto: la línea de pedido de venta con el nombre del cliente, el código de variante, el código de almacén, el código de ubicación, la fecha de entrega, la cantidad a enviar y la unidad. Por cada producto se totaliza la cantidad a enviar. El informe se puede utilizar cuando los productos se recogen del stock.<br>NOTA: Esta funcionalidad no está disponible para la funcionalidad de almacén avanzada.|
|**Ubic. ajuste almacén**|7320|Este informe especial está destinado únicamente a almacenes avanzados y muestra las cantidades restantes que aún están almacenadas en la ubicación de ajuste. Normalmente, esta ubicación específica debería estar vacío. La única razón por la que se llenará esta ubicación es como resultado del proceso de recuento físico o si se eliminaron o agregaron cantidades de productos al almacén.|


## <a name="tasks"></a>Tareas

Los siguientes artículos describen algunas de las tareas clave para analizar el estado de su empresa:

* [Crear informes de análisis](bi-how-create-analysis-views-reports.md)  
* [Consultar la disponibilidad de los productos](inventory-how-availability-overview.md)


## <a name="see-also"></a>Consulte también .

[Configurar inventario](inventory-setup-inventory.md)  
[Inventario](inventory-manage-inventory.md)  
[Configuración de la gestión del almacén](warehouse-setup-warehouse.md)  
[Gestión de almacenes](warehouse-manage-warehouse.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
