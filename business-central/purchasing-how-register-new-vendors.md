---
title: Crear una ficha de proveedor para registrar un proveedor nuevo | Documentos de Microsoft
description: Obtenga información sobre cómo crear una ficha de proveedor para registrar un nuevo proveedor.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supplier
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: f1028b91101f8faa38d4d4d5d2695ee498ff6d2e
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2021
ms.locfileid: "5772659"
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

Para registrar un nuevo proveedor, debe rellenar una ficha de proveedor. Puede establecer plantillas para diferentes perfiles de proveedores, o puede agregar proveedores sin plantillas. También puede crear un proveedor a partir de un contacto. Para obtener más información, consulte [Para crear un contacto como proveedor, empleado o banco de un contacto](marketing-create-contact-companies.md#to-create-a-customer-vendor-employee-or-bank-account-from-a-contact).  

> [!NOTE]  
> Si existen plantillas de proveedor para distintos tipos de proveedor, una página aparece cuando se crea una nueva ficha de proveedor en la que puede seleccionar una plantilla adecuada. Si solo existe una plantilla de proveedor, las nuevas fichas de proveedor utilizan siempre esa plantilla.  

### <a name="to-create-a-new-vendor-card"></a>Para crear una nueva ficha de proveedor

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Proveedores** y luego elija el enlace relacionado.  
2. En la página **Proveedores**, elija **Nuevo**.

    Si existe más de una plantilla de proveedor, se abre una página desde la que puede seleccionar una plantilla de proveedor. En ese caso, siga los dos pasos siguientes.
    1. En la página **Seleccionar una plantilla para un proveedor nuevo**, seleccione la plantilla que quiere usar para la nueva ficha de proveedor.
    2. Elija el botón **Aceptar**. Una nueva ficha de proveedor se abre con algunos campos completados con la información de la plantilla.
3. Empiece a rellenar o cambiar campos en la ficha de proveedor, según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!TIP]  
    > Si no conoce de antemano la dirección de facturación que se utilizará para todas las facturas de un proveedor, no rellene el campo **Nº proveedor** de la ficha de proveedor. En su lugar, elija el número del pago-a proveedor cuando haya configurado una oferta, pedido o encabezado de compra.

El proveedor estará registrado y la ficha de proveedor está lista para usarse en los documentos de compra.

Si desea usar esta ficha de proveedor como plantilla cuando cree nuevas fichas de proveedor, puede guardarla. Para obtener más información, consulte la sección [Para guardar la ficha de proveedor como una plantilla](#to-save-the-vendor-card-as-a-template).

### <a name="deleting-vendor-cards"></a>Eliminar fichas de proveedores

Si ha publicado una transacción para un proveedor, no puede eliminar la ficha porque los movimientos pueden ser necesarias para la auditoría. Para eliminar fichas de proveedores con movimientos, póngase en contacto con su socio de Microsoft para hacerlo a través del código.

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