---
title: Crear una ficha de proveedor para registrar un proveedor nuevo (contiene vídeo)
description: En este tema, aprenda a crear una ficha de proveedor para registrar un nuevo proveedor y guardar fichas de proveedor como plantilla.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supplier
ms.search.form: 26, 27, 34, 461, 786, 1379, 1385, 1386, 1628
ms.date: 09/29/2021
ms.author: edupont
ms.openlocfilehash: 1cbdf85f08939aa05c013901239bbd390400f3e1
ms.sourcegitcommit: c05806689d289d101bd558696199cefbd989473e
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/12/2022
ms.locfileid: "8115507"
---
# <a name="register-new-vendors"></a>Permite registrar nuevos proveedores

Los proveedores proporcionan los productos que vende. Cada proveedor del que compra debe estar registrado como ficha de proveedor.

Antes de que pueda registrar nuevos proveedores, debe configurar varios códigos de compra que pueda seleccionar al rellenar fichas de proveedores. Una vez creados todos los datos maestros necesarios, se puede efectuar una configuración adicional del proveedor, como priorizar el proveedor para fines de pago y crear una lista de productos que este y otros proveedores pueden suministrar. Otro grupo de tareas de configuración para proveedores es registrar los acuerdos relativos a descuentos, precios y métodos de pago. Para obtener más información, consulte [Configurar compras](purchasing-setup-purchasing.md).

Las fichas de proveedor contienen la información necesaria para comprar productos del proveedor. Para obtener más información, vea [Registrar compras](purchasing-how-record-purchases.md) y [Registrar nuevos productos](inventory-how-register-new-items.md).

> [!NOTE]  
> Si existen plantillas de proveedor para distintos tipos de proveedor, una página aparece cuando se crea una nueva ficha de proveedor en la que puede seleccionar una plantilla adecuada. Si solo existe una plantilla de proveedor, las nuevas fichas de proveedor utilizan siempre esa plantilla.
<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE3PZtd?rel=0]

## <a name="adding-new-vendors"></a>Agregar nuevos proveedores
Puede agregar nuevos proveedores manualmente, completando los campos en la página **Ficha de proveedor**, o puede utilizar plantillas que contienen información predefinida. Por ejemplo, puede crear plantillas para diferentes tipos de perfiles de proveedores. El uso de plantillas ahorra tiempo al agregar nuevos proveedores y ayuda a garantizar que la información sea correcta en todo momento. Si crea plantillas para más de un tipo de proveedor, puede elegir la plantilla que utilizará cuando agregue un proveedor. Si crea solo una plantilla, se utilizará para todos los proveedores nuevos. Después de crear una plantilla, puede usar la acción **Aplicar plantilla** para aplicarla a uno o más proveedores seleccionados. Para crear una plantilla, complete la información que desea reutilizar en la página Ficha de proveedor y luego guárdela como una plantilla. Para obtener más información, consulte la sección [Para guardar la página de proveedor como una plantilla](purchasing-how-register-new-vendors.md#to-save-the-vendor-card-as-a-template).

> [!TIP]
> Puede resultar útil personalizar la página **Ficha de proveedor** cuando crea una plantilla. Por ejemplo, es posible que desee agregar un campo que aún no se muestra en la página. Para obtener más información, consulte [Personalizar el área de trabajo](/dynamics365/business-central/ui-personalization-user#to-start-personalizing-a-page-through-the-personalizing-banner).

También puede crear un proveedor a partir de un contacto. Para obtener más información, consulte [Para crear un contacto como proveedor, empleado o banco de un contacto](marketing-create-contact-companies.md#to-create-a-customer-vendor-employee-or-bank-account-from-a-contact). 

### <a name="to-create-a-new-vendor"></a>Para crear un nuevo proveedor

[!INCLUDE[create_new_vendor](includes/create_new_vendor.md)]

> [!TIP]  
> Si no conoce de antemano la dirección de facturación que se utilizará para todas las facturas de un proveedor, no rellene el campo **Nº proveedor** de la ficha de proveedor. En su lugar, elija el número del pago-a proveedor cuando haya configurado una oferta, pedido o encabezado de compra.

El proveedor estará registrado y la ficha de proveedor está lista para usarse en los documentos de compra.

Si desea usar esta ficha de proveedor como plantilla cuando cree nuevas fichas de proveedor, puede guardarla. Para obtener más información, consulte la sección [Para guardar la ficha de proveedor como una plantilla](#to-save-the-vendor-card-as-a-template).

### <a name="deleting-and-editing-vendor-information"></a>Eliminar y editar la información del proveedor

Puede editar la información de las fichas de proveedor en cualquier momento. Sin embargo, si ha publicado una transacción para un proveedor, no puede eliminar la ficha porque los movimientos pueden ser necesarias para la auditoría. Para eliminar fichas de proveedores con movimientos, póngase en contacto con su socio de Microsoft para hacerlo a través del código.

> [!TIP]
> Puede cambiar el IBAN en la cuenta bancaria de un proveedor sin que el cambio afecte los movimientos del registro de transferencia de crédito históricos. Los movimientos del registro de transferencia de crédito almacenan el IBAN del destinatario, el número de cuenta bancaria del destinatario que se especificaron en los campos Cuenta bancaria del proveedor y Nombre del destinatario de la página Ficha del proveedor cuando se crearon los movimientos.


## <a name="to-save-the-vendor-card-as-a-template"></a>Para guardar la ficha de proveedor como una plantilla

1. En la página **Ficha proveedor**, seleccione la acción **Guardar como plantilla**. La página **Plantilla proveedor** se abre mostrando la ficha de proveedor como plantilla.
2. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Para volver a usar dimensiones en las plantillas, seleccione la acción **Dimensiones**. La página **Plantilla de dimensiones** se abre mostrando los códigos de dimensión configurados para el proveedor.
4. Modifique o introduzca los códigos de dimensión que se aplicarán a nuevas fichas de proveedor creadas con la plantilla.
5. Cuando haya finalizado la nueva plantilla de proveedor, seleccione el botón de **Aceptar**.  
   La plantilla de proveedor se agrega a la lista de plantillas de proveedor, de modo que puede usarla para crear nuevas fichas de proveedor.

## <a name="see-also"></a>Consulte también

[Combinar registros duplicados](sales-how-merge-duplicate-records.md)  
[Crear numeración](ui-create-number-series.md)  
[Compras](purchasing-manage-purchasing.md)  
[Registrar compras](purchasing-how-record-purchases.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]