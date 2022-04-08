---
title: Crear una nueva orden de producción planificada en firme y cambiarla
description: Tutorial para un planificador de producción de Contoso Coffee que desea crear una orden de producción planificada en firme y luego modificarla.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
ms.openlocfilehash: 7a057e144ed6825435c62f565eeaaa73974fedf9
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2022
ms.locfileid: "8525253"
---
# <a name="walkthrough-create-a-firm-planned-production-order-and-change-it"></a>Tutorial: Crear una nueva orden de producción planificada en firme y cambiarla

En este artículo, le guiaremos a través de los pasos para usar los datos de demostración de Contoso Coffee para trabajar con órdenes de producción.  

## <a name="scenario"></a>Caso

Eduardo, el planificador de producción de Contoso Coffee, debe crear una nueva orden de producción para 10 unidades del artículo **SP-SCM1009, Airpot** con vencimiento el 28 de abril. Lo programa hacia atrás y confirma que puede iniciar el pedido el 27 de abril.  

Poco después de terminar esta tarea, se le pide que aumente el pedido a 50 unidades. Cuando hace esto, la funcionalidad de programación regresiva adelanta demasiado la fecha de inicio del pedido. Por lo tanto, adelanta el pedido del 23 de abril para determinar una fecha de finalización más realista.  

## <a name="steps"></a>Pasos

1. Cree la orden de producción inicial para 10 unidades del artículo **SP-SCM1009, Airpot**.

    1. Elija la ![Bombilla que abre la función Dígame.](../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **O.P. Planificadas en firme** y, a continuación, elija el vínculo relacionado.  

    2. Elija la acción **Nuevo** y, a continuación, rellene los campos tal como se describe en la tabla siguiente.  

        |Campo  |Valor  |
        |---------|---------|
        |**Tipo procedencia mov.** |Producto|
        |**Cód. procedencia mov.** |SP-SCM1009|
        |**Cantidad** |10|
        |**Fecha vencimiento**|Abril de 28  |

    3. Elija la acción **Actualizar orden producción**.  

    4. En la página **Actualizar orden producción**, acepte todos los valores predeterminados y, a continuación, elija el botón **Aceptar** para iniciar el proceso.  

        En la configuración actual, este proceso utiliza la programación regresiva. En la nueva línea de la orden de producción, la fecha de inicio es el 26 de abril.  

2. Cambie la cantidad de la orden de producción a 50 unidades y programe la orden.  

    1. En la ficha desplegable **Líneas** de la **L.M. de producción**, seleccione la línea agregada recientemente y luego, en el campo **Cantidad**, introduzca *50*.  

3. Elija la acción **Actualizar orden producción**.  

    La fecha de inicio se ha postpuesto al 20 de abril. Esta no es una fecha aceptable para Eduardo.

4. Activa una programación hacia delante de la orden de producción.

    1. En la ficha desplegable **Programación**, establezca el campo **Fecha de inicio** en *23 de abril*.

    El inicio del pedido es ahora el 25 de abril y la fecha de finalización es el 2 de mayo. La fecha de vencimiento del pedido se fija un día después, el 3 de mayo. Eduardo sabe ahora que tardará hasta el 3 de mayo en entregar el pedido aumentado.

> [!NOTE]
> La programación de un pedido cambiando su fecha de inicio o finalización no requiere el trabajo por lotes **Actualizar orden producción** porque todas las fechas se vuelven a calcular automáticamente.

La nueva orden de producción ya está configurada y se cumplen los requisitos de Eduardo.  

## <a name="see-also"></a>Consulte también .

[Introducción a datos de demostración de Contoso Coffee](contoso-coffee-intro.md)  
