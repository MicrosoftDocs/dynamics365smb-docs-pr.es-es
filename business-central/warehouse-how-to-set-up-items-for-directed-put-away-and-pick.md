---
title: Configurar la ubicación y el picking directos | Documentos de Microsoft
description: Cuando un almacén está configurado para ubicación y picking directos, tiene disponible nueva funcionalidad que le ayuda a ejecutar los procesos de almacén de la forma más eficaz posible. 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 5e76ef000ffc9242cf98e11be353b604990bf5ea
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/03/2019
ms.locfileid: "2876412"
---
# <a name="set-up-items-and-locations-for-directed-put-away-and-pick"></a>Configurar productos y almacenes para ubicaciones y picking directos
Cuando un almacén está configurado para ubicación y picking directos, tiene disponible nueva funcionalidad que le ayuda a ejecutar los procesos de almacén de la forma más eficaz posible. Para utilizar toda esta funcionalidad, tiene que proporcionar información adicional sobre los productos, que, a su vez, ayuda a que se realicen los cálculos necesarios para sugerir las formas más efectivas y eficaces de dirigir las actividades de almacén. Para obtener más información, consulte [Detalles de diseño: Configuración almacén](design-details-warehouse-setup.md).

## <a name="to-set-up-an-item-for-directed-put-away-and-pick"></a>Para configurar productos para picking y ubicaciones directas  
1.  Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Productos** y luego elija el enlace relacionado.  
2.  Abra la ficha del producto que desee configurar para picking y ubicaciones directas.
3. En la ficha desplegable **Almacén** de la ficha de producto, rellene los campos para definir cómo debe gestionarse el producto en el almacén.  
4.  Elija la acción **Unidades medida**.
5. En la página **Unidades medida producto**, rellene los campos de este formulario para definir las diferentes unidades de medida en las que se puede trabajar con el producto, incluidos el alto, el ancho, la longitud, el cubicaje y el peso de la unidad de medida.
6. Seleccione la acción **Contenido ubicación**.
7. En la página **Contenidos ubicación** puede definir el almacén y la ubicación con la que debe asociarse el producto. El campo **Genérico** no se utiliza cuando el almacén está configurado para ubicación y picking directos.  

## <a name="to-activate-directed-put-away-and-pick-functionality"></a>Para activar la funcionalidad de ubicación y picking directos  
La ubicación y picking directos le ofrecen la posibilidad de tener acceso a características de configuración avanzada de almacén que pueden mejorar su eficacia y la fiabilidad de sus datos. Para utilizar esta funcionalidad, primero debe configurar varios parámetros en su almacén.  

Para utilizar la funcionalidad de ubicación y picking directos debe activar la funcionalidad en la ficha de almacén.    
1.  Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Almacenes** y, a continuación, elija el enlace relacionado.  
2.  Seleccione el almacén donde desea utilizar la ubicación y picking directos y, a continuación, elija la acción **Editar**.  
3.  En la ficha desplegable **Almacén**, seleccione la casilla **Ubicac. y pick. directo**.  

No tiene que rellenar ningún otro campo de la ficha de almacén hasta más tarde en el proceso de configuración.  

> [!NOTE]  
>  No puede configurar el almacén para utilizar ubicaciones cuando el almacén tiene movimientos de producto pendientes.  

El siguiente paso es definir el tipo de ubicaciones con las que desea trabajar. Para obtener más información, consulte [Configurar tipos de ubicaciones](warehouse-how-to-set-up-bin-types.md). El tipo de ubicación define cómo utilizar una ubicación determinada cuando procese el flujo de productos a través del almacén. Un tipo de ubicación se puede asignar a una zona y a una ubicación.  

También puede definir los códigos de clase de almacén, si el almacén trabaja con productos que necesitan diversas condiciones de almacenamiento. Los códigos de clase de almacén se utilizan cuando se sugiere la colocación del artículo en las ubicaciones. Asigne los códigos de clase de almacén a los grupos de artículos, que luego se asignarán a los artículos y UA, o a las zonas y a las ubicaciones que pueden adaptarse a las condiciones de almacenamiento requeridas por los códigos de clase de almacén.  

Ahora está preparado para configurar zonas, si desea trabajar con ellas en el almacén. El uso de zonas reduce el número de campos que tiene que rellenar al configurar sus ubicaciones, porque las ubicaciones creadas en zonas heredan varias propiedades de la zona. Las zonas también ayudan a los empleados nuevos o temporales a orientarse en el almacén. Observe que el flujo se controla a través de las ubicaciones, por tanto es posible funcionar con las ubicaciones y una sola zona.  

## <a name="to-set-up-a-zone-in-your-warehouse"></a>Para configurar una zona en el almacén  
1.  Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Almacenes** y, a continuación, elija el enlace relacionado.  
2.  Seleccione el almacén donde desee configurar la zona y abra la ficha de almacén y elija la acción **Zonas**.  
3.  En la página **Zonas**, rellene los campos necesarios. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

Al cambiar un parámetro de zona, todas las ubicaciones creadas a partir de entonces en dicha zona presentarán las nuevas características. Sin embargo, las ubicaciones originales no cambiarán.  

> [!NOTE]  
>  Si desea trabajar sin zonas, aún necesita crear un código de zona que no esté definido, excepto por el código.  

El siguiente paso en la configuración del almacén es definir ubicaciones. Para obtener más información, consulte [Configurar lugares para utilizar las ubicaciones](warehouse-how-to-set-up-locations-to-use-bins.md).  

Además, deberá crear plantillas de ubicación y periodos de cuenta. Para obtener más información, vea [Configurar plantillas de ubicación](warehouse-how-to-set-up-put-away-templates.md).  

## <a name="see-also"></a>Consulte también  
[Gestión de almacenes](warehouse-manage-warehouse.md)  
[Grupos contables inventario](inventory-manage-inventory.md)  
[Configuración de la gestión del almacén](warehouse-setup-warehouse.md)     
[Gestión de ensamblaje](assembly-assemble-items.md)    
[Detalles de diseño: Gestión de almacén](design-details-warehouse-management.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
