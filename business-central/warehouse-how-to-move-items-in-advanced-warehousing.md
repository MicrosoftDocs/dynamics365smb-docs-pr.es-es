---
title: Cómo mover productos en configuraciones avanzadas de almacén | Microsoft Docs
description: En configuraciones de almacén avanzadas, es decir, en ubicaciones con ubicación y picking directos, los movimientos de almacén entre ubicaciones los realiza un empleado con experiencia que los prepara en la hoja de trabajo de movimientos y, a continuación, crea dichos movimientos para que los realicen los empleados de almacén.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 442f25cdeefba42815e3e97dedad8713c3ecf1e4
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2019
ms.locfileid: "912515"
---
# <a name="move-items-in-advanced-warehouse-configurations"></a>Mover productos en configuraciones avanzadas de almacén
En configuraciones de almacén avanzadas, es decir, en ubicaciones con ubicación y picking directos, los movimientos de almacén entre ubicaciones los realiza un empleado con experiencia que los prepara en la hoja de trabajo de movimientos y, a continuación, crea dichos movimientos para que los realicen los empleados de almacén.  

## <a name="to-move-items-with-the-warehouse-movement-worksheet"></a>Para mover los artículos con la hoja de cálculo del movimiento de almacén
En la página **Hoja trabajo movimiento** existen dos funciones que pueden ayudarle a rellenar las líneas automáticamente. La primera es la función **Calcular reposición ubicación**. Esta función utiliza los rankings de ubicación para sugerir el reabastecimiento para ubicaciones de alto ranking desde ubicaciones de bajo ranking. El segundo es la función **Traer conten. ubicac.**, que rellena las líneas de la hoja de cálculo con los contenidos enteros de las ubicaciones que especifique.

1.  Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Hoja trabajo mov.** y luego elija el enlace relacionado.  
2.  Especifique la información de movimientos de almacén en las líneas de la hoja de trabajo como crea conveniente.  
3. Elija la acción **Crear movimiento** para crear un documento de movimiento de almacén que, más tarde, se puede registrar cuando se complete el movimiento.  

### <a name="to-register-the-warehouse-movement"></a>Para registrar el movimiento de almacén  
1.  Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Movimientos** y luego elija el enlace relacionado.  
2.  Abra el movimiento de almacén que desee procesar.  
3.  En las líneas de acción tipo **Plaza**, especifique dónde, qué y cuándo mover el artículo en cuestión modificando los campos **Cód. zona**, **Cód. ubicación**, **Cdad. a manipular** o **Fecha vencimiento**.  

    Si su almacén se ha configurado para que los códigos de ubicación sigan la estructura física del almacén, puede traer varias cantidades de diferentes productos de ubicaciones correlativas y, a continuación, colocarlas en ubicaciones de picking sucesivas, que estarán próximas entre sí.  
4.  En las líneas de acción tipo **Toma**, especifique en el campo **Cdad. a manipular** una cantidad de la parte del contenido de la ubicación que desea mover. El resto de los campos de las líneas de tipo de acción **Tomar** son de solo lectura.  
5.  Para mover todas las cantidades sugeridas según lo especificado en el campo **Cantidad**, elija la acción **Cdad autorell. a manipular**.  
6. Elija la acción **Registrar**.  

> [!NOTE]  
>  Si el almacén utiliza ubicación y picking directos, no puede mover manualmente productos dentro o fuera de ubicaciones de tipo Recepción, porque los productos en dichas ubicaciones deben ubicarse antes de que formen parte del inventario disponible.

## <a name="to-register-the-movement-of-an-item-that-has-already-occurred"></a>Para registrar el movimiento de producto que ya se ha producido  
Si utiliza ubicación y picking directos y necesita mover productos a otros ubicaciones sin un movimiento, picking o ubicación de almacén existente, puede registrar la colocación correcta de los productos en el almacén con el **Diario reclasificación almacén**.

1.  Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Diario reclasif. almacén** y luego elija el enlace relacionado.  
2.  Rellene los campos **Nº producto**, **Desde cód. zona**, **Desde cód. ubicación**, **Hasta cód. zona**, **Hasta cód. ubicación**.  
3.  Elija la acción **Registrar**.  

## <a name="see-also"></a>Consulte también  
[Gestión almacén](warehouse-manage-warehouse.md)  
[Grupos contables inventario](inventory-manage-inventory.md)  
[Configuración de la gestión del almacén](warehouse-setup-warehouse.md)     
[Gestión de ensamblaje](assembly-assemble-items.md)    
[Detalles de diseño: Gestión de almacén](design-details-warehouse-management.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
