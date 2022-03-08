---
title: Ubicación de productos con ubicación de almacén | Documentos de Microsoft
description: Si el almacén está configurado para requerir los procesos de ubicación y recepción de almacén, utilice la función de documentos de ubicación de almacén para controlar la ubicación de los productos.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: f9c1e144e5574e04d1d5baec039d3f358839631e
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/03/2019
ms.locfileid: "2881659"
---
# <a name="put-items-away-with-warehouse-put-aways"></a>Ubicar productos con ubic. exist. almacén
Si el almacén está configurado para requerir los procesos de ubicación y recepción de almacén, utilice la función de documentos de ubicación de almacén para controlar la ubicación de los productos.  

Al registrar una recepción de almacén, se actualizan los documentos de origen, como la compra, transferencia de entrada o los pedidos de devolución de ventas; se registra la cantidad recibida en el diario de productos y se envían las líneas con los productos recibidos a la función de ubicación del almacén. Si tiene ubicación y picking internos, la ubicación interna también puede crear líneas para ubicación.  

Dependiendo de la configuración de almacén, se ponen a disposición las líneas en la hoja de trabajo de ubicación o se usan para generar instrucciones de ubicación inmediatamente. Para obtener más información, consulte [Planificar ubicaciones en hojas de trabajo](warehouse-how-to-plan-put-aways-in-worksheets.md).  

Además de las formas estándar de crear las ubicaciones de almacén que se describen en este tema, puede crear la ubicación de recepción de almacén registrado relacionada. Esta acción es útil si utiliza ubicaciones y picking directos y ha decidido no utilizar la hoja de trabajo de ubicación, ya que puede crear o volver a crear las instrucciones de ubicación desde líneas de albarán recibidas.  

## <a name="to-put-items-away-without-directed-put-away-and-pick"></a>Para ubicar productos sin picking y ubicaciones directas  
1.  Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Ubicaciones** y luego elija el enlace relacionado.  
2.  Abra el almacén la ubicación que está preparado para manipular.  

    Puede ordenar las ubicaciones por varios criterios, por ejemplo, por producto, número de estante o fecha de vencimiento y, por tanto, optimizar el proceso de ubicación.  
3.  En cada línea, en el campo **Cdad. a manipular**, escriba la cantidad que desea ubicar.  
4.  Una vez haya completado la ubicación de los productos, elija la acción **Registrar ubicación** para registrar la finalización de la actividad y hacer que los productos estén disponibles para picking.  

## <a name="to-put-items-away-with-directed-put-away-and-pick"></a>Para ubicar productos con ubicaciones y picking directos  
1.  Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Ubicaciones** y luego elija el enlace relacionado.
    Si se han creado instrucciones de ubicación, una ubicación de almacén está visible.  
2.  Abra la ubicación de almacén con el que desee trabajar.  
3.  Si el almacén lo requiere, escriba su id. de usuario en la ficha desplegable **General** cuando empiece a trabajar en una ubicación determinada.  
4.  Ejecute las acciones traer y colocar indicadas en el campo **Tipo acción** de las líneas.  

    Tenga en cuenta que cada línea de la recepción se ha convertido en al menos dos líneas en la ubicación de almacén:  

    -   La primera línea, con **Traer** en el campo **Tipo acción**, indica dónde están colocados los productos en el área de recepción. En esta línea no puede cambiar el campo zona y ubicación.  
    -   La siguiente línea, con **Colocar** en el campo **Tipo acción**, muestra dónde debe colocar los productos en el almacén. Si el almacén ha recibido muchos productos en una línea de recepción, quizá deba colocarlos en varias ubicaciones a fin de tener una línea Colocar en cada ubicación.  

        Si las líneas Traer y Colocar de cada línea de recepción no están una a continuación de otra y desea hacerlo, puede ordenar las líneas seleccionando **Producto** en el campo **Método ordenación** de la ficha desplegable **General**.  

        Si el diseño físico del almacén refleja los rankings de las ubicaciones, puede utilizar el método de ordenación **Ranking ubicación** para preparar una ubicación que minimizará los pasos que tiene que dar en el almacén.  

5.  Cuando haya colocado todos los productos en ubicaciones como se le ha indicado, elija la acción **Registrar ubicación**.  

En las ubicaciones configuradas para utilizar ubicación y picking directos, la siguiente es un requisito previo para el procedimiento anterior:  

- Se configura una plantilla de ubicación. Para obtener más información, vea [Configurar plantillas de ubicación](warehouse-how-to-set-up-put-away-templates.md).  
- Define el peso, cubicaje y requisitos especiales de almacenamiento del producto o la unidad de almacenamiento. Para obtener más información, consulte Peso bruto.  
- La capacidad, el tipo de ubicación y ranking de las ubicaciones. Para obtener más información, consulte Ranking ubicación.  

El ranking de ubicación se tiene en cuenta cuando varias ubicaciones cumplen los criterios de la plantilla de ubicación.  Si los criterios de la plantilla de ubicación y el ranking de ubicación son los mismos para varias ubicaciones, se selecciona la ubicación con el número más alto.

## <a name="to-create-a-put-away-from-a-posted-receipt"></a>Para crear una ubicación desde una recepción registrada  
 Si el almacén procesa la ubicación y la recepción y ha eliminado las líneas de ubicación, o si utiliza ubicaciones y picking directos y ha decidido no utilizar la hoja de trabajo de ubicación, puede crear o volver a crear las instrucciones de ubicación para líneas de albarán recibidas.

1.  Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Recep. almacén regis.** y luego elija el enlace relacionado.  
2.  Seleccione una recepción registrada que sea necesario ubicar.  
3.  Seleccione la acción **Ficha**.  

    Si el campo **Estado documento** está en blanco, la recepción aún no se ha ubicado. En caso contrario, el campo indica la recepción se ha ubicado parcial o completamente.  

4.  Si el albarán se ha ubicado parcialmente o no se ha ubicado, elija la acción **Crear ubicación**.  
5.  Rellene la página del proceso para crear la ubicación como necesite y a continuación seleccione **Aceptar**.   

## <a name="see-also"></a>Consulte también  
[Gestión almacén](warehouse-manage-warehouse.md)  
[Grupos contables inventario](inventory-manage-inventory.md)  
[Configuración de la gestión del almacén](warehouse-setup-warehouse.md)     
[Gestión de ensamblaje](assembly-assemble-items.md)    
[Detalles de diseño: Gestión de almacén](design-details-warehouse-management.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
