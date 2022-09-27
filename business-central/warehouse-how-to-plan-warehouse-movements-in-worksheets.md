---
title: Cómo planificar los movimientos de almacén en la hoja de trabajo | Documentos de Microsoft
description: Planifique los movimientos en la hoja de trabajo con una función de reposición de ubicación o manualmente mediante la planificación de las líneas que desea crear como instrucciones de movimiento.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 1ec80435211b139868bf62ddf0ce269a802d2abc
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/19/2022
ms.locfileid: "9534054"
---
# <a name="plan-warehouse-movements-in-worksheets"></a>Planificar movimientos de almacén en hojas de trabajo

Planifique los movimientos en la hoja de trabajo con una función de reposición de ubicación o manualmente mediante la planificación de las líneas que desea crear como instrucciones de movimiento.  

## <a name="to-calculate-a-replenishment-movement"></a>Para calcular un movimiento de reposición

Cuando el almacén envía los productos a los clientes, las ubicaciones con los ranking de ubicación más altos contienen cada vez menos productos. Para rellenar estas ubicaciones de picking de ranking más alto con productos de otras ubicaciones, ejecute la función **Calcular reposición ubicación** de la página **Hoja trabajo movimiento**.

1.  Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Hoja trabajo mov.** y, a continuación, elija el vínculo relacionado.  
2.  Elija la acción **Calcular reposición ubicación**.  

    [!INCLUDE[prod_short](includes/prod_short.md)] crea líneas que indican exactamente cómo debe mover los productos de las ubicaciones de ranking inferior a las ubicaciones de ranking superior.  

    > [!NOTE]  
    >  Un movimiento se sugiere según el FEFO cuando se activa la función **Crear movimiento** si cumple las siguientes condiciones para un artículo:  
    >   
    >  -   El producto tiene fecha de caducidad.  
    > -   Se selecciona la casilla **Picking según FEFO (Primero en caducar, primero en salir)** de la ficha de almacén.  
    > -   La casilla **Ubicac. obligatoria** de la ficha de almacén está seleccionada.  
    > -   Los campos **Desde zona** y **Desde ubicación** están en blanco.  

    Para obtener más información, consulte [Realización de picking por el FEFO](warehouse-picking-by-fefo.md).  

3.  Observe las líneas y cámbielas si es necesario, o elimine algunas si no tiene tiempo suficiente para ejecutar todas.  
4.  Elija la acción **Crear movimiento** para crear una instrucción de almacén para que los empleados de almacén realicen una acción.  

## <a name="to-move-the-entire-contents-of-one-or-more-bins-by-using-the-get-bin-content-function"></a>Mover todo el contenido de una o varias ubicaciones con la función Traer contenido ubicación

También puede utilizar la hoja de trabajo de movimiento para planificar otros movimientos de inventario en el almacén. Por ejemplo, cuando desee colocar productos en una ubicación para controlar la calidad, puede utilizar la hoja de trabajo de movimiento para planificar esta acción y, a continuación, crear un movimiento para darle instrucciones a un empleado.  

1.  Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Hoja trabajo mov.** y, a continuación, elija el vínculo relacionado.  
2.  Seleccione la acción **Traer contenido ubicación**. Utilice la página de solicitud para filtrar las ubicaciones y productos que desea que aparezcan en las líneas de la hoja de trabajo de movimiento.  
3.  Rellene los campos correspondientes de la página de solicitud del proceso. Por ejemplo, si desea ver el contenido de todas las ubicaciones en una determinada zona del almacén, rellene el campo **Cód. zona**. Si desea recuperar líneas de cada ubicación que contenga un producto determinado, rellene el campo **Nº producto**.  

    > [!NOTE]  
    >  No puede mover manualmente productos dentro o fuera de una ubicación de tipo RECEPCIÓN, porque los productos que están en una ubicación de tipo RECEPCIÓN deben ubicarse antes de que formen parte del inventario disponible.  

4.  Si recupera muchas líneas, seleccione **Ordenar** para seleccionar un método de ordenación que determine el orden en el que aparecerán las líneas en la hoja de trabajo y, a continuación, haga clic en **Aceptar**.  

    > [!NOTE]  
    >  Las líneas de movimiento se recuperan según el FEFO cuando se activa la función **Traer conten. ubicac.** si cumple las siguientes condiciones para un producto:  
    >   
    >  -   El producto tiene fecha de caducidad.  
    > -   Se selecciona la casilla **Picking según FEFO (Primero en caducar, primero en salir)** de la ficha de almacén.  
    > -   La casilla **Ubicac. obligatoria** de la ficha de almacén está seleccionada.  
    > -   Los campos **Desde zona** y **Desde ubicación** están en blanco.  

5.  Complete algunas de las líneas recuperadas para reflejar los cambios que desea realizar. En cada producto que desee mover, debe rellenar los campos **Nº producto**, **Desde cód. ubicación**, **Hasta cód. ubicación** y **Cantidad**.  
6.  Elimine las líneas incompletas que ha utilizado para su información.  
7.  Cuando las líneas de la hoja de trabajo de movimiento reflejen exactamente cómo debe realizar el empleado del almacén la acción de movimiento, elija la acción **Crear movimiento** para crear las instrucciones para el empleado.  

## <a name="see-related-microsoft-training"></a>Consultar la [formación de Microsoft](/training/modules/move-items/) relacionada

## <a name="see-also"></a>Consulte también .

[Warehouse Management](warehouse-manage-warehouse.md)  
[Inventario](inventory-manage-inventory.md)  
[Configuración de Warehouse Management](warehouse-setup-warehouse.md)     
[Gestión de ensamblaje](assembly-assemble-items.md)    
[Detalles de diseño: Warehouse Management](design-details-warehouse-management.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
