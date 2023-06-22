---
title: Configurar ubicación y picking directos
description: 'Si utiliza almacenamiento y picking dirigidos, tendrá la funcionalidad de ejecutar el almacén eficientemente.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: null
ms.date: 11/07/2022
ms.author: bholtorf
---
# <a name="set-up-items-and-locations-for-directed-put-away-and-pick" />Configurar productos y almacenes para ubicaciones y picking directos

Cuando un almacén está configurado para ubicación y picking directos, tiene disponible nueva funcionalidad que le ayuda a ejecutar los procesos de almacén de la forma más eficaz posible.  Para utilizar toda esta funcionalidad, tiene que proporcionar información adicional sobre los productos, que, a su vez, ayuda a que se realicen los cálculos necesarios para sugerir las formas más efectivas y eficaces de dirigir las actividades de almacén. 

## <a name="to-set-up-an-item-for-directed-put-away-and-pick" />Para configurar productos para picking y ubicaciones directas

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Productos**, y luego elija el enlace relacionado.  
2. Abra la ficha del producto que desee configurar para picking y ubicaciones directas.
3. En la ficha desplegable **Almacén** de la ficha de producto, rellene los campos para definir cómo debe gestionarse el producto en el almacén.  
4. Elija la acción **Unidades medida**.
5. En la página **Unidades de medida de productos**, defina las diferentes unidades de medida en las que se puede trabajar con cada producto, especificando el alto, el ancho, la longitud, el cubicaje y el peso del producto.
6. Seleccione la acción **Contenido ubicación**.
7. En la página **Contenidos ubicación** puede definir el almacén y la ubicación con la que debe asociarse el producto. El campo **Genérico** no se utiliza cuando el almacén está configurado para ubicación y picking directos.  

## <a name="to-start-using-directed-put-away-and-pick" />Para empezar a utilizar el almacenamiento y el picking dirigidos

La ubicación y picking directos le ofrecen la posibilidad de tener acceso a características de configuración avanzada de almacén que pueden mejorar su eficacia y la fiabilidad de sus datos. Para utilizar esta funcionalidad, primero debe configurar varios parámetros en su almacén.  

Para utilizar la funcionalidad de ubicación y picking directos debe activar la funcionalidad en la ficha de almacén.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Ubicaciones** y luego elija el enlace relacionado.  
2. Seleccione el almacén donde desea utilizar la ubicación y picking directos y, a continuación, elija la acción **Editar**.  
3. En la ficha desplegable **Almacén**, seleccione la casilla **Almacenamiento y picking dirigidos**.  

No tiene que rellenar ningún otro campo de la ficha de almacén hasta más tarde en el proceso de configuración.  

> [!NOTE]  
> No puede configurar el almacén para utilizar ubicaciones cuando el almacén tiene movimientos de producto pendientes.  

El siguiente paso es definir el tipo de ubicaciones con las que desea trabajar. Para obtener más información, consulte [Configurar tipos de ubicaciones](warehouse-how-to-set-up-bin-types.md). El tipo de ubicación define cómo utilizar una ubicación determinada cuando procese el flujo de productos a través del almacén. Un tipo de ubicación se puede asignar a una zona y a una ubicación.  

También puede definir los códigos de clase de almacén, si el almacén trabaja con productos que necesitan condiciones específicas de almacenamiento. Los códigos de clase de almacén se utilizan cuando se sugiere la colocación del artículo en las ubicaciones. Asigne los códigos de clase de almacén a los grupos de artículos, que luego se asignarán a los artículos y UA, o a las zonas y a las ubicaciones que pueden adaptarse a las condiciones de almacenamiento requeridas por los códigos de clase de almacén.  

Ahora está listo para configurar zonas, si lo desea. El uso de zonas reduce el número de campos que tiene que rellenar al configurar sus ubicaciones, porque las ubicaciones creadas en zonas heredan varias propiedades de la zona. Las zonas también ayudan a los empleados nuevos o temporales a orientarse en el almacén. Observe que el flujo se controla a través de las ubicaciones, por tanto es posible funcionar con las ubicaciones y una sola zona.  

## <a name="to-set-up-a-zone-in-your-warehouse" />Para configurar una zona en el almacén

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Ubicaciones** y luego elija el enlace relacionado.  
2. Seleccione el almacén donde desee configurar la zona y abra la ficha de almacén y elija la acción **Zonas**.  
3. En la página **Zonas**, rellene los campos necesarios. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

Al cambiar un parámetro de zona, todas las ubicaciones creadas a partir de entonces en dicha zona presentarán las nuevas características. Sin embargo, las ubicaciones originales no cambiarán.  

> [!NOTE]  
> Si desea trabajar sin zonas, aún necesita crear un código de zona que no esté definido, excepto por el código.  

El siguiente paso es definir ubicaciones. Para obtener más información, consulte [Configurar almacenes para utilizar ubicaciones](warehouse-how-to-set-up-locations-to-use-bins.md).  

Además, deberá crear plantillas de ubicación y periodos de cuenta. Para obtener más información, vea [Configurar plantillas de almacenamiento](warehouse-how-to-set-up-put-away-templates.md).  

## <a name="see-also" />Consulte también

[Información general de la gestión de almacenes](design-details-warehouse-management.md)
[Inventario](inventory-manage-inventory.md)  
[Configuración de Warehouse Management](warehouse-setup-warehouse.md)     
[Gestión de ensamblaje](assembly-assemble-items.md)    
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
