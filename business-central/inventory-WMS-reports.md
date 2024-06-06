---
title: Informes y análisis de inventario y almacén
description: Consulte qué informes y análisis de inventario y almacén están disponibles en la versión estándar de Business Central para que pueda realizar un seguimiento de su negocio.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: reporting
ms.search.form: 'Report_707, Report_716, Report_813, Report_1001, Report_5807, Report_5808, Report_5809, Report_7313, Report_7319, Report_7320'
ms.date: 03/21/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# Informes y análisis de inventario y almacén

Los informes de inventario y almacén en [!INCLUDE [prod_short](includes/prod_short.md)] proporcionan a los profesionales de la producción y los negocios información y estadísticas sobre las actividades de inventario y almacén actuales y pasadas.  

## Informes

[!INCLUDE [inventory_WMS_reports](includes/inventory-WMS-reports-include.md)]

## Tareas

Los siguientes artículos describen algunas de las tareas clave para analizar el estado de su empresa:

* [Crear informes de análisis](bi-how-create-analysis-views-reports.md)  
* [Consultar la disponibilidad de los productos](inventory-how-availability-overview.md)

## Imprimir y escanear códigos de barras

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


## Explorar los informes de inventario con el Explorador de informes

Para obtener una descripción general de los informes disponibles para su inventario, elija **Todos los informes** en la página de inicio. Esta acción abre el explorador de roles, que se filtra según las funciones en la opción **Informe y análisis**. En el encabezado **Ventas y marketing**, elija **Explorar**.

:::image type="content" source="media/report-explorer-sales.png" alt-text="Ejemplo de informes sobre el centro de roles financieros" lightbox="media/report-explorer-sales.png":::

Para obtener más información, vaya a [Búsqueda de informes con el explorador de roles](ui-role-explorer.md).


## Consulte también

[Análisis ad-hoc de datos de inventario](ad-hoc-analysis-inventory.md)  
[Información general de análisis de inventario](inventory-analytics-overview.md)   
[Configurar inventario](inventory-setup-inventory.md)  
[Grupos contables inventario](inventory-manage-inventory.md)  
[Configuración de Warehouse Management](warehouse-setup-warehouse.md)  
[Información general de la gestión de almacenes](design-details-warehouse-management.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
