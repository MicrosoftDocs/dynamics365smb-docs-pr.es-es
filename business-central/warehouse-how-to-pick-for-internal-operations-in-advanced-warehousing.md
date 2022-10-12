---
title: Realizar el picking en operaciones internas en configuraciones avanzadas de almacén
description: Si sus ubicaciones utilizan el picking y el envío, seleccione componentes para las actividades de producción, montaje y trabajo en la página Picking en almacén.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 09/02/2022
ms.author: bholtorf
ms.openlocfilehash: 2ef879e5dbabb9281114d62a956ad4b10113c199
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/30/2022
ms.locfileid: "9607559"
---
# <a name="pick-for-production-assembly-or-jobs-in-advanced-warehouse-configurations"></a>Realizar picking para producción, ensamblado o proyectos en una configuración avanzada de almacén

En la configuración avanzada de almacén en donde se configura la ubicación para utilizar picking y envío, podrá escoger los componentes para las actividades de producción y de ensamblado en la página **Picking almacén**.  

También puede utilizar la página **Hoja trabajo movimiento** para mover los artículos espontáneamente entre las ubicaciones sin referencia a un documento de origen. Para obtener más información, consulte [Mover los artículos en las configuraciones avanzadas de almacén](warehouse-how-to-move-items-in-advanced-warehousing.md).  

Para obtener información acerca de los artículos de picking en las ubicaciones del almacén básico configuradas sólo para picking, consulte [Mover componentes a un área de operaciones en la configuración básica de almacén](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).  

> [!NOTE]
> No se puede crear un documento de picking de almacén desde cero porque una actividad de picking siempre forma parte de un flujo de trabajo, tanto en un escenario de extracción como de inserción.  

Puede crear el documento de picking de almacén mediante inserción seleccionando **Crear picking almacén** en el documento de origen, como un pedido de ensamblado enviado o un envío de almacén. Para obtener más información, vea [Realizar picking de productos con picking almacén](warehouse-how-to-pick-items-for-warehouse-shipment.md).  

También puede crear un documento de selección de almacén de forma pull utilizando la página **Seleccionar hoja de trabajo** para detectar solicitudes de recolección. Este método es útil para envíos y operaciones internas. A continuación, puede crear los documentos de selección de almacén necesarios.  

El procedimiento siguiente explica un escenario de envío en donde se va a realizar el picking de los componentes para un orden de producción lanzada a través de la página **Hojas trabajo picking**. El procedimiento también se aplica a un pedido de ensamblado.  

Para crear pedidos de picking, para escenarios de extracción y de empuje, deben lanzarse los documentos de origen en cuestión. Lance los documentos de origen para las operaciones internas de las siguientes formas.  

|Documento origen|Método de lanzamiento|  
|---------------------|--------------------|  
|Orden producción|Cambie el tipo de pedido a orden de producción lanzada.|  
|Pedido de ensamblado|Cambie el estado a Lanzada.|
|Proyectos | Cambie el estado a Abierto.|  

## <a name="to-pick-components-using-the-pick-worksheet"></a>Para realizar el picking de componentes desde la hoja de trabajo de picking

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Hoja trabajo picking** y luego elija el enlace relacionado.  
2. Elija la acción **Documentos almacén** y seleccione las líneas de componente del pedido de producción lanzado.  
3. Clasifique las líneas para garantizar un picking eficiente. Es posible que desee combinar líneas para ahorrar tiempo a los empleados.  
4. Elija la acción **Crear picking**.  
5. Defina cómo crear los documentos de picking de almacén y cómo ordenar las líneas de picking rellenando los campos de la página **Crear picking**.  
6. Elija el botón **Aceptar**. Los documentos de picking de almacén se crean con las líneas de picking para cada componente necesario en la operación interna.  

Las áreas de operación, como los talleres de producción, pueden tener un contenedor predeterminado para los componentes que requieren. Si es así, el código de ubicación predeterminado se agrega al documento de selección de almacén para indicar dónde colocar los artículos. Para obtener más información, consulte la información sobre herramientas de los campos **Código de ubicación para producción** o **Código de ubicación para ensamblado**.

## <a name="filling-the-consumption-bin"></a>Rellenando la ubicación del consumo

Este organigrama muestra cómo se rellena el campo de **Código de ubicación** en las líneas del componente de la orden de producción según la ubicación.

![Diagrama de flujo de ubicación.](media/binflow.png "BinFlow")  

## <a name="see-related-microsoft-training"></a>Consultar la [formación de Microsoft](/training/paths/pick-ship-items-business-central/) relacionada

## <a name="see-also"></a>Consulte también .

[Warehouse Management](warehouse-manage-warehouse.md)  
[Inventario](inventory-manage-inventory.md)  
[Configuración de Warehouse Management](warehouse-setup-warehouse.md)  
[Gestión de ensamblaje](assembly-assemble-items.md)  
[Detalles de diseño: Warehouse Management](design-details-warehouse-management.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
