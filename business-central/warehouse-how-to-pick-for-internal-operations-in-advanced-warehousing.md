---
title: "Cómo realizar el picking en operaciones internas en configuraciones avanzadas de almacén | Documentos de Microsoft"
description: "En la configuración avanzada de almacén en donde se configura la ubicación para utilizar picking y envío, podrá escoger los componentes para las actividades de producción y de ensamblado con la página **Picking almacén**."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 01/22/2019
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 5d6d2d9527e81a92987f6b8fcdbe8e087c3c537a
ms.openlocfilehash: bb4941c948c2e4479ec36fdebee11f1d75e62c68
ms.contentlocale: es-es
ms.lasthandoff: 01/22/2019

---
# <a name="pick-for-production-or-assembly-in-advanced-warehouse-configurations"></a>Realizar picking para ensamblado o producción en una configuración avanzada de almacén
En la configuración avanzada de almacén en donde se configura la ubicación para utilizar picking y envío, podrá escoger los componentes para las actividades de producción y de ensamblado con la página **Picking almacén**.  

También podrá utilizar la página **Hoja trabajo movimiento** para mover los artículos entre las ubicaciones ad hoc (es decir, sin referencia a un documento de origen). Para obtener más información, consulte [Mover los artículos en las configuraciones avanzadas de almacén](warehouse-how-to-move-items-in-advanced-warehousing.md).  

Para obtener información acerca de los artículos de picking para las operaciones internas en las ubicaciones del almacén básico configuradas sólo para picking, consulte [Mover componentes a un área de operaciones en la configuración básica de almacén](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).  

No se puede crear un documento de picking de almacén desde cero porque una actividad de picking siempre forma parte de un flujo de trabajo, tanto en un escenario de extracción como de inserción.  

Puede crear el documento de picking de almacén mediante inserción seleccionando **Crear picking almacén** en el documento de origen, como un pedido de ensamblado enviado o un envío de almacén. Para obtener más información, vea [Realizar picking de productos con picking almacén](warehouse-how-to-pick-items-for-warehouse-shipment.md).  

Alternativamente, puede crear el documento de picking de almacén de forma de la extracción utilizando la página **Preparar hoj. trab. pedido** para detectar pedidos de picking, tanto para envío y como para operaciones internas y, a continuación crear los documentos de picking de almacén necesarios.  

El procedimiento siguiente explica un escenario de envío en donde se va a realizar el picking de los componentes para un orden de producción lanzada a través de la página **Hojas trabajo picking**. El procedimiento también se aplica a un pedido de ensamblado.  

Para crear pedidos de picking, para escenarios de extracción y de empuje, deben lanzarse los documentos de origen en cuestión. Lance los documentos de origen para las operaciones internas de las siguientes formas.  

|Documento origen|Método de lanzamiento|  
|---------------------|--------------------|  
|Orden producción|Cambie el tipo de pedido a orden de producción lanzada.|  
|Pedido de ensamblado|Cambie el estado a Lanzada.|  

## <a name="to-pick-components-using-the-pick-worksheet"></a>Para realizar el picking de componentes desde la hoja de trabajo de picking  
1.  Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Hoja trabajo picking** y luego elija el enlace relacionado.  
2.  Elija la acción **Documentos almacén** y seleccione las líneas de componente del pedido de producción lanzado.  
3.  Explore las líneas, ordénelas para asegurar un picking más eficaz y combínelas con otras líneas de hoja de trabajo si es necesario para ahorrar tiempo a los empleados.  
4.  Elija la acción **Crear picking**.  
5.  Defina cómo crear los documentos de picking de almacén y cómo ordenar las líneas de picking rellenando los campos de la página **Crear picking**.  
6.  Elija el botón **Aceptar**. Los documentos de picking de almacén se crean con las líneas de picking para cada componente necesario en la operación interna.  

Si el área de operaciones internas, como un suelo de departamento de producción, se ha configurado con una ubicación predeterminada para la colocación de los componentes utilizados en la operación,ese código de ubicación se insertará en las líneas del lugar en el documento de picking de almacén para indicar a los trabajadores del almacén dónde ubicar los artículos. Para obtener más información, consulte el campo **Código de ubicación para producción** o **Código de ubicación para ensamblado**.

## <a name="filling-the-consumption-bin"></a>Rellenando la ubicación del consumo
Este organigrama muestra cómo se rellena el campo de **Código de ubicación** en las líneas del componente de la orden de producción según la ubicación.

![Gráfico de flujo de ubicación](media/binflow.png "BinFlow")  

## <a name="see-also"></a>Consulte también
[Gestión almacén](warehouse-manage-warehouse.md)  
[Grupos contables inventario](inventory-manage-inventory.md)  
[Configuración de la gestión del almacén](warehouse-setup-warehouse.md)     
[Gestión de ensamblaje](assembly-assemble-items.md)    
[Detalles de diseño: Gestión de almacén](design-details-warehouse-management.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

