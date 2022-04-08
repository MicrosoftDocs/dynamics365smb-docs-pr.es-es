---
title: Gestión de transacciones entre empresas vinculadas
description: Con la funcionalidad de empresas vinculadas, puede simplificar los procesos y transacciones empresariales entre empresas de la misma organización.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: IC, group, consolidation, affiliate, subsidiary
ms.search.form: 605
ms.date: 08/11/2021
ms.author: edupont
ms.openlocfilehash: 356a484df2445dac39c02b9341cb9a0660a07467
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2022
ms.locfileid: "8511654"
---
# <a name="managing-intercompany-transactions"></a>Gestión de transacciones entre empresas vinculadas

Las funciones de las transacciones entre empresas vinculas están diseñadas para los usuarios que controlan más de una entidad empresarial legal y han configurado varias empresas para separar las funciones contables de cada una de dichas entidades. Esta descripción general sirve para muchos tipos de usuarios, sobre todos los que trabajan en mercados internaciones o lugares en los que existen distintas culturas empresariales y entornos normativos.

Su organización puede estar formada por varias empresas, pero puede no tener un número equivalente de departamentos de contabilidad y administrativos. Las transacciones entre empresas vinculadas le permiten simplificar los procesos y transacciones empresariales entre todas estas entidades.

Una vez que empiece a utilizar las transacciones entre empresas vinculadas, los negocios con las subsidiarias y con otras organizaciones asociadas son tan sencillas como las que realiza con sus clientes y proveedores. La información sobre las transacciones entre empresas vinculadas sólo se introduce una vez en los documentos correspondientes. Puede usar las funciones que ya conoce, por ejemplo la gestión de cobros y pagos. Las opciones de asignación del plan de cuentas y las dimensiones contribuyen a garantizar que la información se muestra en los lugares correctos.  

La funcionalidad entre empresas vinculadas tienen cuatro ventajas principales:  

- Aumenta la productividad, como consecuencia del tiempo que se gana y el hecho de que las transacciones sean más sencillas  
- Hay menos posibilidades de cometer errores con la introducción de la información una sola vez y las actualizaciones automáticas en todo el sistema  
- Se logran un seguimiento y una visibilidad totales de las actividades empresariales y los historiales de las transacciones  
- Las transacciones con las subsidiarias y las filiales son eficaces y rentables  

## <a name="streamlining-the-flow-of-business-activities"></a>Simplificar el flujo de actividades empresariales  

Las transacciones entre empresas vinculadas le permiten distribuir los documentos de compras y ventas, así como los movimientos del diario general a todas las sucursales, oficinas de ventas o subsidiarias, todo desde el interior del sistema. En consecuencia, se gana tiempo y se aumenta la eficacia en toda la organización, ya que se elimina la duplicación en la introducción de información y se evita el envío, recepción, impresión y archivado de los documentos en papel.  

El control sobre todos los documentos de las transacciones es total. Por ejemplo, puede rechazar un documento que ha recibido y, de esta forma, revertir los registros de diario y deshacer los recibos/envíos incorrectos. Al realizar una compra a un asociado o una subsidiaria puede actualizar el pedido de compra, siempre que la empresa vendedora no haya enviado los productos todavía.  

Al introducir una transacción, no tiene que especificar las cuentas de cada uno de los grupos de libros, si no que sólo tiene que proporcionar la identificación de la empresa asociada. La funcionalidad entre empresas vinculadas crean líneas del diario general que hacen que los libros queden cuadrados en las dos empresas implicadas en la transacción. En cobros y pagos, puede asignar un código de socio de empresa vinculada a cualquier cliente o proveedor. A partir de ese momento, todos los pedidos y facturas generados en relación con las transacciones realizadas con este tipo de empresas crearán los documentos correspondientes en la empresa asociada, y se cuadran correctamente todas las cuentas.  

La funcionalidad de las transacciones entre empresas vinculadas se centra en dar apoyo a las transacciones entre empresas vinculadas con documentos de ventas y compras y con líneas del diario general. En esta área, las transacciones entre empresas vinculadas admiten transacciones entre empresas vinculadas en varias bases de datos de [!INCLUDE [prod_short](includes/prod_short.md)], por ejemplo de distintos países o regiones, así como en varias divisas, distintos planes de cuentas y dimensiones, y distintas numeraciones de productos.  

Las transacciones entre empresas vinculadas usan varios movimientos y documentos de las transacciones entre empresas vinculadas:  

- Movimientos del diario general
- Pedidos de compras y de ventas
- Facturas de compras y de ventas
- Abonos
- Devoluciones

Al configurar las transacciones entre empresas vinculadas, crea una lista de socios de empresas vinculadas, denominados socios IC, y un plan de cuentas de empresas vinculadas. A continuación, lleva a cabo las transacciones de libro general entre empresas vinculadas. Si es necesario, debe configurar dimensiones por separado.  

> [!NOTE]
> El diario general en sí mismo no tiene la funcionalidad de divisas, si no que convierte todos los importes a la divisa local mediante el tipo de cambio que corresponda.

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
|Utilice las transacciones de empresas vinculadas para distribuir costes entre empresas asociadas.|[Asignar costes a socios entre empresas](intercompany-allocate-costs.md)|

## <a name="see-also"></a>Consulte también

[Finanzas](finance.md)  
[Configurar las finanzas](finance-setup-finance.md)  
[Trabajar con diarios generales](ui-work-general-journals.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
