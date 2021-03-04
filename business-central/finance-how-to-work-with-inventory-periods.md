---
title: Trabajar con periodos inventario | Documentos de Microsoft
description: Usted puede controlar el periodo en el que la gente puede registrar cambios en el inventario mediante la definición de periodos de inventario.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: inventory, periods
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: ca5104a8d4268c9f4822e98150a3e969c6c66d48
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2020
ms.locfileid: "3924158"
---
# <a name="work-with-inventory-periods"></a>Trabajar con periodos de inventario
Los periodos del inventario definen un periodo de tiempo durante el cual es posible registrar cambios en el inventario. Un periodo del inventario se define por la fecha en la que finaliza. Cuando se cierra un periodo del inventario, no es posible registrar ningún cambio en él (ya sea previsto o facturado) antes de dicha fecha de finalización. Tampoco es posible registrar ningún valor nuevo en el inventario antes de dicha fecha. Si tiene movimientos de producto abiertos en ese periodo ya cerrado (lo que significa que existen cantidades positivas que todavía no ha aplicado a transacciones de salida), seguirá pudiendo aplicar cantidades de salida a dichos movimientos, incluso si el periodo está cerrado.  

En el siguiente apartado se explica cómo:

* Cree periodos de inventario.  
* Cierre periodos de inventario.  
* Vuelva a abrir periodos de inventario.  

## <a name="to-create-an-inventory-period"></a>Para crear un periodo de inventario  
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Periodos inventario** y luego elija el enlace relacionado.  
2. Cree una línea nueva.  
3. En el campo **Fecha final**, introduzca la última fecha del periodo que desee definir. Cuando se cierre el periodo del inventario, ya no podrá registrar cambios en el inventario antes de dicha fecha.  
4. Introduzca un nombre descriptivo en el campo **Nombre**. Elija el botón **Aceptar**.  

## <a name="closing-inventory-periods"></a>Cerrar periodos del inventario  
El campo **Cerrado** indica si el periodo del inventario se encuentra o no cerrado a efectos de poder realizar cambios en sus valores. Este campo no se puede modificar.  

Es posible cerrar un periodo del inventario siempre y cuando se cumplan las siguientes condiciones:  

* No existen movimientos de producto de salida abiertos (es decir, inventario negativo) en ese periodo.  
* Se ha ajustado el coste de todos los productos utilizando el proceso **Valorar stock - movs. producto**.  

Esto significa que todas las cantidades de transacciones de salida (como aquellas provenientes de los pedidos de ventas, transferencias de salida, facturas de ventas, devoluciones de compra o abonos de compra) deben aplicarse a una cantidad existente en el inventario.  

### <a name="to-close-an-inventory-period"></a>Para cerrar un periodo de inventario  
1. Antes de cerrar un periodo de inventario, elija la acción **Valorar stock - movs. producto** para asegurarse de que se hayan registrado todos los ajustes de costes.

     Ejecute el informe **Cerrar periodo inventario - Prueba** para determinar si existe algún movimiento de producto de salida dentro del periodo de inventario o cualquier producto cuyo coste no se haya ajustado todavía.  
2. Seleccione la acción **Cerrar periodo inventario - Prueba**.  

     Ejecute el trabajo por lotes **Reg. var. existencias en cont.** para asegurarse de que se hayan registrado todos los costes en el módulo de contabilidad.  
3. Elija la acción **Registrar inventario en C/G**.  
4. En la página **Periodos inventario**, seleccione el periodo de inventario que desea cerrar.  
5. Seleccione la acción **Cerrar periodo**. Una vez cerrado el periodo del inventario, ya no podrá registrar cambios en el antes de la fecha de finalización. Será necesario ajustar el coste de todos los productos mediante el proceso **Valorar stock - movs. producto** antes de que cierre el periodo del inventario.  
6. Seleccione le botón **Sí** para confirmar que desea cerrar el periodo, o bien elija **No** para cancelar el proceso.  
7. Se cierra el periodo de inventario y aparece un mensaje de confirmación cuando haya finalizado.  

## <a name="reopening-inventory-periods"></a>Volver a abrir periodos del inventario  
Después de haber cerrado el periodo de inventario, ya no podrá eliminarlo. No obstante, si lo desea podrá volver a abrirlo para permitir realizar cambios antes de la fecha de finalización del periodo del inventario. Al volver a abrir un periodo, también se volverán a abrir todos los periodos del inventario cuyas fechas de finalización sean posteriores a las del periodo que está volviendo a abrir.  

### <a name="to-reopen-an-inventory-period"></a>Para volver a abrir un periodo de inventario  
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Periodos inventario** y luego elija el enlace relacionado.  
2. Seleccione el periodo del inventario que desea volver a abrir.  
3. Seleccione la acción del periodo **Reabrir periodo**. Confirme que desea volver a abrir el periodo.  
4. Todos los periodos del inventario cuyas fechas de finalización sean posteriores a las del periodo que ha seleccionado se vuelven a abrir.  

## <a name="see-also"></a>Consulte también  
[Detalles de diseño: Periodos de inventario](design-details-inventory-periods.md)  
[Finanzas](finance.md)  
[Inventario](inventory-manage-inventory.md)  
[Trabajar con Financials](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]