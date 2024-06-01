---
title: Gestión de transacciones entre empresas vinculadas
description: 'Con la funcionalidad de empresas vinculadas, puede simplificar los procesos y transacciones empresariales entre empresas de la misma organización.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bhielse
ms.topic: conceptual
ms.date: 02/06/2023
ms.custom: bap-template
ms.search.keywords: 'IC, group, consolidation, affiliate, subsidiary'
ms.search.form: '605,'
ms.service: dynamics-365-business-central
---
# <a name="managing-intercompany-transactions"></a>Gestión de transacciones entre empresas vinculadas

Las empresas con más de una entidad legal con funciones contables separadas pueden beneficiarse de las transacciones entre empresas. Por ejemplo, es útil para empresas que tienen filiales en varios mercados o regiones internacionales. O bien, una organización puede estar formada por varias empresas, pero puede carecer del un número equivalente de departamentos de contabilidad y administrativos. Las transacciones entre empresas vinculadas le permiten simplificar los procesos y transacciones empresariales entre las empresas vinculadas.

Cuando haya especificado las relaciones de cliente y proveedor para las transacciones entre empresas, los socios introducen la información una vez en los documentos de compra y venta. Se crea un documento correspondiente en el otro socio involucrado en la transacción. La asignación del plan de cuentas y las dimensiones contribuyen a garantizar que la información se muestre en los lugares correctos.  

La funcionalidad entre empresas vinculadas tienen cuatro ventajas principales:  

* Aumenta la productividad, como consecuencia del tiempo que se gana y el hecho de que las transacciones sean más sencillas  
* Los errores se minimizan con la introducción de la información una sola vez y las actualizaciones automáticas en todo el sistema  
* Se logran un seguimiento y una visibilidad totales de las actividades empresariales y los historiales de las transacciones  
* Las transacciones con las subsidiarias y las filiales son eficaces y rentables  

## <a name="streamline-the-flow-of-business-activities"></a>Simplificar el flujo de actividades empresariales

Las transacciones entre empresas vinculadas le permiten distribuir los documentos de compras y ventas, así como los movimientos del diario general a todas las sucursales, oficinas de ventas o filiales. La distribución de transacciones ahorra tiempo y aumenta la eficiencia en toda la organización, al reducir la entrada de datos. Reduce la necesidad de enviar, recibir, imprimir y archivar documentos de compras y ventas.  

El control sobre todos los documentos de las transacciones es total. Por ejemplo, puede rechazar un documento que se le haya enviado y usar las acciones **Revertir los registros de diario** y **Deshacer recepciones/envíos** para hacer correcciones. Al realizar una compra a un asociado o una filial puede actualizar el pedido de compra, siempre que la empresa vendedora no haya enviado los productos todavía.  

Cuando introduce una transacción, no necesita especificar las cuentas a usar. Simplemente elija el socio de empresas vinculadas. La funcionalidad entre empresas vinculadas crea líneas del diario general que equilibran los libros de las dos empresas implicadas en la transacción. En cobros y pagos, puede asignar un código de socio de empresa vinculada a cualquier cliente o proveedor. A partir de ese momento, todos los pedidos y facturas de transacciones entre estas empresas producen los documentos correspondientes en la empresa asociada. El resultado son cuentas correctamente equilibradas.  

Las empresas vinculadas se enfocan en documentos de compras y ventas y líneas de diario generales, y permite transacciones entre múltiples bases de datos de [!INCLUDE [prod_short](includes/prod_short.md)]. Por ejemplo:

* En diferentes países/regiones
* Varias divisas
* Diferentes planes de cuentas
* Diferentes dimensiones
* Diferentes números de producto  

Las transacciones entre empresas utilizan varios tipos de entradas y documentos:  

* Movimientos del diario general
* Pedidos de compras y de ventas
* Facturas de compras y de ventas
* Abonos
* Devoluciones

Al configurar las transacciones entre empresas vinculadas, se crea una lista de socios de empresas vinculadas, un plan de cuentas de empresas vinculadas y dimensiones de empresas vinculadas. Posteriormente, puede crear transacciones en diarios generales de empresas vinculadas.

> [!NOTE]
> El diario general por sí mismo no incluye divisas. Convierte todas las cantidades a la moneda local con el tipo de cambio actual.

Una vez que configura socios empresariales como clientes y proveedores y les asigna códigos de socios de empresas vinculadas, puede intercambiar documentos de empresas vinculadas de compra y de venta, incluidos los productos y los cargos de producto. 

> [!NOTE]
> Las empresas no pueden utilizar empresas vinculadas para intercambiar todo tipo de datos. Las facturas de compra no se envían a los socios comerciales a través de procesos de empresas vinculadas. Sin embargo, las facturas de venta que se envían a través de procesos de empresas vinculadas se crearán como facturas de compra en la empresa receptora.

La consolidación de los datos financieros podría ser relevante para procesos entre empresas vinculadas. Para obtener más información, vea [Consolidar los datos financieros de varias empresas](finance-consolidated-company-reporting.md).

En la tabla siguiente se indican una serie de tareas con vínculos a los artículos que las describen.

|Para |Vea|
|---|---|
|Cree sus proveedores y clientes de empresas vinculadas, como socios, y configure un plan de cuentas de empresas vinculadas.|[Configurar empresa vinculada](intercompany-how-setup.md)|
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
