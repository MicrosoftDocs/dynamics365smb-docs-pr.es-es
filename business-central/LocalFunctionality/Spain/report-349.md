---
title: Informe 349
description: Debe presentar un informe periódico de comercio con otros países o regiones de la UE a las autoridades fiscales. En España, este informe 349 es parte del sistema intracomunitario de intercambio de información sobre el IVA (VIES).
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: d1310a6baf88db077a68f313e691f0c303aa49b8
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2019
ms.locfileid: "918189"
---
# <a name="report-349"></a>Informe 349
Debe presentar un informe periódico de comercio con otros países o regiones de la UE a las autoridades fiscales. En España, este informe 349 es parte del sistema intracomunitario de intercambio de información sobre el IVA (VIES).  

En [!INCLUDE[d365fin](../../includes/d365fin_md.md)], el modelo de Informe 349 se basa en los movimientos de IVA filtrados por los códigos de país o región. Debe crear un modelo 349 y enviar el archivo a la web de la [Agencia Tributaria](https://go.microsoft.com/fwlink/?LinkId=238181) o con un CD-ROM.  

Al crear un modelo del informe 349 que incluye los abonos, los movimientos se muestren en la página **Advertencias 349 Cliente/Proveedor** para que pueda incluirlos como correcciones a las facturas. Debe realizar los cambios necesarios a las líneas de la página **Advertencias 349 Cliente/Proveedor** antes de que pueda enviar la declaración. Para obtener más información, [Crear informes 349](how-to-create-report-349.md).  

## <a name="delivery-operation-codes"></a>Códigos operación entrega  
El modelo del **informe 349** debe especificar los códigos de operación independientes para la entrega de mercancías a otros países o regiones de la UE. Puede configurar grupos de publicación de productos de IVA por separado para cada tipo de entrega de exportación. A continuación, cuando aplique un grupo de registro de IVA a un artículo vendido, [!INCLUDE[d365fin](../../includes/d365fin_md.md)] almacena el código de operación de entrega y la transacción se incluye en la declaración trimestral 349.  

Antes de enviar el modelo 349, debe asegurarse de que todos los movimientos de IVA tienen los códigos de operación de entrega correspondientes. En la tabla siguiente se describen los códigos de operación de entrega que se admiten actualmente en [!INCLUDE[d365fin](../../includes/d365fin_md.md)].  

|Código operación entrega|Description|  
|-----------------------------|---------------------------------------|  
|**E**|Identifica transacciones de productos que se entregados a los clientes en otro país o región de la UE y no se incluyen en el código de operación de entrega M o H.|  
|**M**|Identifica transacciones de productos que se entregados a los clientes en otro país o región de la UE y que se importaron anteriormente en España como exentos de impuestos según la ley de IVA.|  
|**H**|Identifica transacciones de productos que se entregados a los clientes en otro país o región de la UE, que se importaron anteriormente en España como exentos de impuestos según la ley de IVA. y que los gestionó un representante fiscal oficial.|  

 Para ayudarle a gestionar exportaciones en otros países o regiones de la UE en [!INCLUDE[d365fin](../../includes/d365fin_md.md)], puede crear grupos de registro de productos con IVA para cada código de operación. A continuación, cuando aplique un grupo de registro de IVA a un artículo vendido, el campo Código operación entrega de la tabla **Movimientos IVA** identifica las transacciones del IVA según el código de operación.  

### <a name="delivery-operation-codes-and-item-setup"></a>Códigos de operación de entrega y configuración de producto  
Puede configurar un grupo de publicación de productos de IVA para cada tipo de operación de entrega y luego asignar el grupo correspondiente a los artículos en la página Ficha de producto.  

Si tiene un producto de inventario que se puede importar de distintas maneras, por ejemplo si se está exento de impuestos en algunos casos y no lo está en otros, puede crear fichas independientes con el grupo de publicación de productos de IVA correspondiente.  

En el siguiente ejemplo, importa sillas de otro país o región de la UE y las revende a clientes en otros países y regiones. Un tipo de silla está exento de IVA cuando éste se importa en algunas circunstancias, pero no lo está en otras. Como resultado, crea dos fichas de producto:  

- Una tarjeta de artículo con un grupo de registro de productos con IVA con el campo **Código de operación de entrega** establecido en **M**.  
- Una tarjeta de artículo con un grupo de registro de productos con IVA con el campo **Código de operación de entrega** establecido en **E**.  

A continuación, cuando crea un pedido de venta, debe asegurarse de que seleccione el producto correcto en las líneas de venta.  

Cuando registra una factura de venta, [!INCLUDE[d365fin](../../includes/d365fin_md.md)] guarda el código de operación de entrega en la tabla **Movimientos IVA** y, a continuación, cuando se crea el modelo de informe 349, el importe del IVA se incluye en la sección del código de operación de entrega correspondiente.  

## <a name="see-also"></a>Consulte también  
 [Crear el informe 349](how-to-create-report-349.md)
