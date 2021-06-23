---
title: Gestión de transacciones entre empresas vinculadas
description: Con la funcionalidad de empresas vinculadas, puede simplificar los procesos y transacciones empresariales entre empresas de la misma organización.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: IC, group, consolidation, affiliate, subsidiary
ms.date: 06/02/2021
ms.author: edupont
ms.openlocfilehash: 0a69507b32f8782fe876458adb590529bfd64b20
ms.sourcegitcommit: 1aab52477956bf1aa7376fc7fb984644bc398c61
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "6184429"
---
# <a name="managing-intercompany-transactions"></a>Gestión de transacciones entre empresas vinculadas

Su organización puede estar formada por varias empresas, pero puede no tener un número equivalente de departamentos de contabilidad y administrativos. La funcionalidad de empresas vinculadas le permite hacer transacciones con las subsidiarias y con otras organizaciones asociadas de la misma forma que con sus clientes y proveedores. La información sobre las transacciones entre empresas vinculadas sólo se introduce una vez en los documentos correspondientes. Puede usar las funciones que ya conoce, por ejemplo la gestión de cobros y pagos. Las opciones de asignación del plan de cuentas y las dimensiones contribuyen a garantizar que la información se muestra en los lugares correctos.  

La funcionalidad entre empresas vinculadas tienen cuatro ventajas principales:  

- Aumenta la productividad, como consecuencia del tiempo que se gana y el hecho de que las transacciones sean más sencillas  
- Hay menos posibilidades de cometer errores con la introducción de la información una sola vez y las actualizaciones automáticas en todo el sistema  
- Se logran un seguimiento y una visibilidad totales de las actividades empresariales y los historiales de las transacciones  
- Las transacciones con las subsidiarias y las filiales son eficaces y rentables  

El control sobre todos los documentos de las transacciones es total. Por ejemplo, puede rechazar un documento que ha recibido y, de esta forma, revertir los registros de diario y deshacer los recibos/envíos incorrectos. Al realizar una compra a un asociado o una subsidiaria puede actualizar el pedido de compra, siempre que la empresa vendedora no haya enviado los productos todavía.  

Al introducir una transacción, no tiene que especificar las cuentas de cada uno de los grupos de libros, si no que sólo tiene que proporcionar la identificación de la empresa asociada. La funcionalidad entre empresas vinculadas crean líneas del diario general que hacen que los libros queden cuadrados en las dos empresas implicadas en la transacción. En cobros y pagos, puede asignar un código de socio de empresa vinculada a cualquier cliente o proveedor. A partir de ese momento, todos los pedidos y facturas generados en relación con las transacciones realizadas con este tipo de empresas crearán los documentos correspondientes en la empresa asociada, y se cuadran correctamente todas las cuentas.  

Una vez que configura socios empresariales como clientes y proveedores en el sistema y les asigna códigos de socios de empresas vinculadas, puede intercambiar documentos de empresas vinculadas de compra y de venta, incluidos los productos y los cargos de producto. [!INCLUDE [prod_short](includes/prod_short.md)] admite transacciones entre empresas vinculadas en varias bases de datos de, por ejemplo, distintos países o regiones, así como en varias divisas, distintos planes de cuentas y dimensiones, y distintas numeraciones de productos.  

> [!NOTE]
> No todos los tipos de datos pueden intercambiarse entre empresas de esta forma. Las facturas de compra no se envían a los socios comerciales a través de procesos de empresas vinculadas. Pero las facturas de venta que se envían a través de procesos de empresas vinculadas se crearán como facturas de compra en la empresa receptora.

La consolidación de los datos financieros puede ser especialmente relevante para procesos entre empresas vinculadas. Para obtener más información, vea [Consolidar los datos financieros de varias empresas](finance-consolidated-company-reporting.md).

En la tabla siguiente se indican una serie de tareas con vínculos a los artículos que las describen.

|Para |Vea|
|---|---|
|Cree sus proveedores y clientes de empresas vinculadas, como los llamados socios de empresas vinculadas, y configure un plan de cuentas de empresas vinculadas.|[Configurar empresa vinculada](intercompany-how-setup.md)|
|Utilice documentos o diarios de empresas vinculadas para registrar transacciones con empresas vinculadas asociadas.|[Usar documentos y diarios de empresas vinculadas](intercompany-how-work-documents-journals.md)|
|Organice y procese las transacciones entrantes y salientes que intercambia con sus socios de empresas vinculadas.|[Administrar la bandeja de entrada y la bandeja de salida de empresas vinculadas](intercompany-how-manage-intercompany-inbox.md)|
|Utilice las contabilizaciones de empresas vinculadas para distribuir costes entre empresas asociadas.|[Asignar costos a socios entre empresas](intercompany-allocate-costs.md)|

## <a name="see-also"></a>Consulte también

[Finanzas](finance.md)  
[Configurar las finanzas](finance-setup-finance.md)  
[Trabajar con diarios generales](ui-work-general-journals.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]