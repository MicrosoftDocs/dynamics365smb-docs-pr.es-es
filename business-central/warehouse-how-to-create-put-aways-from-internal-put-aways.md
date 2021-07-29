---
title: Crear ubicaciones desde ubicaciones internas
description: Este tema trata sobre cómo realizar picking y ubicación sin un documento de origen, cómo crear un picking interno y cómo crear una ubicación interna.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/24/2021
ms.author: edupont
ms.openlocfilehash: 198c4fb8ead4179667e35957046b3446ce5d8065
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 07/08/2021
ms.locfileid: "6444185"
---
# <a name="pick-and-put-away-without-a-source-document"></a>Realizar el picking y la ubicación sin un documento de origen
Una vez ubicados los productos y antes de que se realice el picking de los mismos para cubrir las necesidades de una orden de producción o un envío, los productos se almacenan en el almacén como parte de las existencias disponibles.  

Puede darse el caso de que haya que sacar productos de las ubicaciones de picking de almacén temporalmente para utilizarlos como modelos de demostración en una presentación de ventas. Estos productos pertenecen a la empresa y forman parte de las existencias, pero no están disponibles para picking. Se registran en una ubicación especial que se crea con este fin; técnicamente, los productos están en el almacén, pero físicamente estarían en una sala de demostraciones.  

En otras situaciones, el departamento de producción es posible que necesite, de forma inesperada, determinados componentes para su proceso. Puede realizar el picking de productos para las ubicaciones de producción con un picking interno. Cuando finalice el proceso y se cree la salida, registre el consumo de los productos y vacíe la ubicación de producción, lo que reducirá la cantidad del producto en su almacén.  

De igual modo, los productos se pueden devolver al almacén para ubicarlos. Puede que los productos se hayan pasado del inventario disponible a una orden de producción y no se hayan utilizado. Deben ubicarse en el almacén para que formen parte de nuevo del inventario disponible.  

Los **Picking internos** le permiten realizar ubicaciones sin tener que hacer referencia a un documento de origen determinado. Puede configurar fácilmente toda la información que necesita para crear una instrucción de almacén de ubicación.  

> [!NOTE]  
>  Si no utiliza ubicación y picking directos, estos ajustes se pueden realizar con los métodos para mover productos entre ubicaciones o registrar ajustes de cantidades en una ubicación.  
>   
>  Cuando el almacén utiliza ubicación y picking directos y, por tanto, utiliza tipos de ubicaciones, no puede mover manualmente productos dentro o fuera de una ubicación de tipo RECEPCIÓN, porque los productos que están en una ubicación de tipo RECEPCIÓN deben ubicarse antes de que formen parte del inventario disponible.  

## <a name="to-create-an-internal-pick"></a>Para crear un picking interno  
1.  Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Picking interno alm.** y, a continuación, elija el vínculo relacionado.  
2. Seleccione la acción **Nuevo**.
3. Rellene el campo **No.**. **Código de almacén** y el campo **Hasta código de ubicación** de la ficha desplegable **General**. El campo **Hasta código de ubicación** especifica la ubicación donde deea colocar los productos recogidos. Para producción, esta ubicación sería la ubicación de producción de entrada o la ubicación de planta abierta. Para otros fines, seleccione un código de ubicación de tipo ubicación que no se utilice para recogida, probablemente una ubicación especial, de envío o intermedia.  
4.  Seleccione un producto en el campo **Nº producto** y rellene las cantidades que desea realizar el picking.  
5. Elija la acción **Crear picking**. Ahora está preparada una instrucción de picking de almacén para que un empelado la ejecute. Alternativamente, puede elegir la acción **Liberar** y crear recogidas de almacén utilizando la **Hoja de trabajo de recogidas**. Para obtener más información, consulte [Planificar recogidas en hojas de trabajo](warehouse-how-to-plan-picks-in-worksheets.md)

## <a name="to-create-an-internal-put-away"></a>Para crear un ubicación interna  
1.  Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Ubicación interna alm.** y, a continuación, elija el vínculo relacionado.  
2. Seleccione la acción **Nuevo**.
3. Rellene la cabecera de una nueva ubicación interna con, al menos, el **N.º** y el **Código de almacén**.
4. Rellene una línea por cada producto que desea mover al almacén. Sólo tiene que rellenar los campos **Nº producto** y **Cantidad**.

  > [!NOTE]  
  > Al seleccionar el campo **N.º producto**, se abrirá la **Lista de contenidos de ubicaciones** en vez de la **Lista de productos**. Esto es porque desea ubicar un producto que está en una ubicación determinada, el *contenido de ubicación*, no solo un producto y ya conoce la ubicación desde la que se debe traer el producto.  <!--If you filled in **From Bin Code** in the header, the bin content will be filtered by value defined in the **From Bin Code**.-->
5. Para rellenar las líneas con todo el contenido de la ubicación o el contenido filtrado de las ubicaciones del almacén, elija la acción **Obtener contenido de ubicación**.  
6. Seleccione la acción **Crear ubicación**. Ahora está preparada una instrucción de ubicación de almacén para que un empelado la ejecute. Alternativamente, puede elegir la acción **Liberar** y crear colocaciones de almacén utilizando la **Hoja de trabajo de colocaciones**. Para obtener más información, consulte [Planificar colocaciones en hojas de trabajo](warehouse-how-to-plan-put-aways-in-worksheets.md)

## <a name="see-also"></a>Consulte también  
[Gestión de almacenes](warehouse-manage-warehouse.md)  
[Inventario](inventory-manage-inventory.md)  
[Configuración de la gestión del almacén](warehouse-setup-warehouse.md)     
[Gestión de ensamblaje](assembly-assemble-items.md)    
[Detalles de diseño: Gestión de almacén](design-details-warehouse-management.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
