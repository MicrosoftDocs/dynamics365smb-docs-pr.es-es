---
title: Informes y análisis de inventario y almacén
description: Consulte qué informes y análisis de inventario y almacén están disponibles en la versión estándar de Business Central para que pueda realizar un seguimiento de su negocio.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.search.keywords: reporting
ms.search.form: 'Report_707, Report_716, Report_813, Report_1001, Report_5807, Report_5808, Report_5809, Report_7313, Report_7319, Report_7320'
ms.date: 03/21/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="inventory-and-warehouse-reports-and-analytics"></a>Informes y análisis de inventario y almacén

Los informes de inventario y almacén en [!INCLUDE [prod_short](includes/prod_short.md)] proporcionan a los profesionales de la producción y los negocios información y estadísticas sobre las actividades de inventario y almacén actuales y pasadas.  

## <a name="reports"></a>Informes

[!INCLUDE [inventory_WMS_reports](includes/inventory-WMS-reports-include.md)]

## <a name="tasks"></a>Tareas

Los siguientes artículos describen algunas de las tareas clave para analizar el estado de su empresa:

* [Crear informes de análisis](bi-how-create-analysis-views-reports.md)  
* [Consultar la disponibilidad de los productos](inventory-how-availability-overview.md)

## <a name="print-and-scan-barcodes"></a>Imprimir y escanear códigos de barras

El uso de códigos de barras puede ayudarle a agilizar los procesos de entrada, salida e internos de su almacén. 

[!INCLUDE [barcode-mobile-app](includes/barcode-mobile-app.md)]

Después de instalar la aplicación, puede utilizar la acción **Imprimir etiqueta** para imprimir códigos de barras 1D y 2D desde las páginas enumeradas en la siguiente tabla.

|Página  |Los códigos de barras de valores de campo pueden incluir  |
|---------|---------|
|Productos, Ficha producto     |Nº producto, Descripción y GTIN         |
|Lista de referencia de productos, referencia de productos     |Nº producto, Descripción, Unidad de medida y N.º referencia         |
|Lista información nº lote, Etiqueta n.º lote     |N.º producto, Descripción y Número de lote       |
|SN de etiqueta     |N.º, Descripción y Número de serie         |

> [!NOTE]
> Algunas impresoras y formatos de código de barras/código QR requieren una implementación específica. Es posible que tenga que cargar una plantilla de Word diferente o clonar el informe para crear su propia versión personalizada.

## <a name="see-also"></a>Consulte también .

[Configurar inventario](inventory-setup-inventory.md)  
[Grupos contables inventario](inventory-manage-inventory.md)  
[Configuración de Warehouse Management](warehouse-setup-warehouse.md)  
[Información general de la gestión de almacenes](design-details-warehouse-management.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
