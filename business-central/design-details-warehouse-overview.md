---
title: 'Detalles de diseño: Resumen de almacén | Documentos de Microsoft'
description: Para respaldar la manipulación física de los productos en el nivel de zona y de ubicación, se debe realizar el seguimiento de toda la información por cada transacción o movimiento que se produzca en el almacén. Se administra en la tabla **Movimiento almacén**. Cada transacción se almacena en un registro de almacén.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 8a972cebc919e0e308f22b417a62f33cb8b06f62
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2021
ms.locfileid: "5785140"
---
# <a name="design-details-warehouse-overview"></a>Detalles de diseño: Resumen de almacén
Para respaldar la manipulación física de los productos en el nivel de zona y de ubicación, se debe realizar el seguimiento de toda la información por cada transacción o movimiento que se produzca en el almacén. Se administra en la tabla **Movimiento almacén**. Cada transacción se almacena en un registro de almacén.  

Los documentos de almacén y el diario de almacén se usan para registrar los movimientos de producto en el almacén. Cada vez que se mueve, recibe, ubica, selecciona, envía o ajusta un producto en el almacén, los movimientos de almacén se registran para almacenar la información física sobre zona, ubicación y cantidad.

La tabla **Contenido ubicación** se usa para controlar todas las dimensiones del contenido de una ubicación por producto, como la unidad de medida, la cantidad máxima y la cantidad mínima. La tabla **Contenido ubicación** también contiene los campos de flujo para los movimientos de almacén, las instrucciones de almacén y las líneas de diario de almacén, lo que garantiza que se puede calcular rápidamente la disponibilidad de un producto por ubicación y una ubicación para un producto. Para obtener más información, consulte [Detalles de diseño: Disponibilidad en el almacén](design-details-availability-in-the-warehouse.md).  

Cuando los registros de producto se producen fuera del módulo de almacén, se usa una ubicación de ajuste predeterminado por ubicación para sincronizar los movimientos de almacén con los movimientos de inventario. Durante el inventario físico del almacén, cualquier diferencia entre las cantidades calculadas y contadas se registra en la ubicación de ajuste y después se registra como corrección de los movimientos de producto. Para obtener más información, consulte [Detalles de diseño: Integración con inventario](design-details-integration-with-inventory.md).  

En la ilustración siguiente se describen los flujos de almacén típicos.  

![Resumen de procesos de almacén](media/design_details_warehouse_management_overview.png "Resumen de procesos de almacén")  

## <a name="basic-or-advanced-warehousing"></a>Gestión avanzada o básica de almacén  
La funcionalidad de almacén en [!INCLUDE[prod_short](includes/prod_short.md)] se puede implementar en distintos niveles de complejidad, en función de los procesos de una empresa y del volumen de pedidos. La diferencia principal es que las actividades se realizan pedido a pedido en el almacenamiento básico, mientras que se consolidan para varios pedidos en el almacenamiento avanzado.  

 Para diferenciar los distintos niveles de complejidad, en esta documentación se hace referencia a dos denominaciones generales: almacenamiento básico y avanzado. Esta diferenciación sencilla abarca diferentes niveles de complejidad, tal como se define mediante los módulos de producto y de ubicación, cada uno respaldado por distintos documentos de IU. Para obtener más información, consulte [Detalles de diseño: Configuración almacén](design-details-warehouse-setup.md).  

> [!NOTE]  
>  El nivel más avanzado del almacenamiento se denomina “instalaciones SGA” en esta documentación, ya que este nivel requiere el módulo más avanzado: Sistemas de gestión de almacén.  

 Los documentos de IU siguientes se usan en el almacenamiento básico y avanzado.  

## <a name="basic-ui-documents"></a>Documentos básicos de la IU  

-   **Ubicación existencias**  
-   **Picking inventario**  
-   **Movimiento inventario**  
-   **Diario productos**  
-   **Diario reclasificación producto**  
-   (Varios informes)  

## <a name="advanced-ui-documents"></a>Documentos avanzados de la IU  

-   **Recep. almacén**  
-   **Hoja trabajo ubic.**  
-   **Ubicar almacén**  
-   **Hoja trabajo picking**  
-   **Picking almacén**  
-   **Hoja trabajo mov.**  
-   **Movimiento almacén**  
-   **Picking almacén interno**  
-   **Ubicación almacén interno**  
-   **Hoja trab. creación ubicación**  
-   **Hoja trab. creac. cont. ubic.**  
-   **Diario producto almacén**  
-   **Diario recl. prod. almacén**  
-   (Varios informes)  

Para obtener más información acerca de cada documento, consulte los temas correspondientes en la página.  

### <a name="terminology"></a>Terminología  
Para establecer la correspondencia con los conceptos financieros de compras y ventas, en la documentación de almacén de [!INCLUDE[prod_short](includes/prod_short.md)] se hace referencia a los siguientes términos para el flujo de productos en el almacén.  

|Periodo|Description|  
|----------|---------------------------------------|  
|Flujo de entrada|Productos que se trasladan a la ubicación del almacén, como compras y transferencias de entrada.|  
|Flujo interno|Productos que se mueven dentro de la ubicación del almacén, como componentes de producción y salida.|  
|Flujo de salida|Productos que salen de la ubicación del almacén, como ventas y transferencias de salida.|  

## <a name="see-also"></a>Consulte también  
 [Detalles de diseño: Gestión de almacén](design-details-warehouse-management.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]