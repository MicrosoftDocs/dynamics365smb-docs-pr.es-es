---
title: Cómo planificar pedido por pedido | Documentos de Microsoft
description: Esta tarea de planificación se puede realizar en la página **Programación de pedidos**, en la que se muestra toda la demanda nueva junto con información sobre disponibilidad y sugerencias de aprovisionamiento. Esta ventana proporciona la información y las herramientas necesarias para planificar de forma eficaz la demanda de las líneas de venta y las líneas de componentes y crear después directamente diferentes tipos de pedidos de suministros.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 43e93d44a1fb4e3fe840313ebff9171cebddf4f9
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2020
ms.locfileid: "3919168"
---
# <a name="plan-for-new-demand-order-by-order"></a>Planear la nueva demanda de pedido por pedido
Esta tarea de planificación se puede realizar en la página **Programación de pedidos**, en la que se muestra toda la demanda nueva junto con información sobre disponibilidad y sugerencias de aprovisionamiento. Esta ventana proporciona la información y las herramientas necesarias para planificar de forma eficaz la demanda de las líneas de venta y las líneas de componentes y crear después directamente diferentes tipos de pedidos de suministros.  

Puede entrar en la página **Planificación de pedidos** de dos formas distintas según para lo que la utilice: Desde una orden que desea planificar específicamente o en por lotes porque desea planificar todas y cualquier demanda nueva.  


## <a name="to-plan-for-new-production-order-demand"></a>Para planificar una nueva demanda de orden de producción  
1.  Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Órdenes producción planificadas** y luego elija el enlace relacionado. (Puede realizar estos pasos para una orden de producción planificada, planificada en firme o una orden de producción lanzada).
2.  Abra la orden de producción que se desea planificar y selección la acción **Planificación**.  
3.  En la página **Planificación de pedidos**, seleccione la acción **Calcular plan**.  

En la página se muestran las líneas de planificación en función del filtro de vista **Demanda de producción**, es decir, las líneas de componentes no satisfechos de todas las órdenes de producción existentes. No se muestra la demanda de una sola orden de producción, porque para planificar una orden de producción se necesita tener un panorama de la demanda de líneas de componentes posiblemente anteriores. Las líneas de planificación de la orden de producción en cuestión se expanden.  

## <a name="to-plan-for-any-new-demand"></a>Para planificar nueva demanda  
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Planificación de pedidos** y luego elija el enlace relacionado.  
2.  En la página **Planificación de pedidos**, seleccione la acción **Calcular plan**.
3.  Elija el botón **Expandir (+)** que aparece delante de la fecha en el campo **Fecha demanda** para ver las líneas de planificación subyacentes que representan las líneas de demanda con disponibilidad insuficiente.  
4.  Para cada línea de planificación expandida, es decir, línea de demanda, se muestran valores en los campos de información situados en la parte inferior de la página.  

    |Opción|Description|  
    |----------------------------------|---------------------------------------|  
    |**Cdad. otros almacenes**|Muestra si el producto existe en otro almacén. Puede realizar una búsqueda y seleccionarlo.|  
    |**Existe sustitutivo**|Muestra si se ha creado un producto sustitutivo para el producto. Puede realizar una búsqueda y seleccionarlo. Tenga en cuenta que esta función sólo se aplica a componentes, es decir, a las líneas de demanda del tipo **Producción**.|  
    |**Cdad. disponible**|Muestra la disponibilidad total del producto, es decir, el Saldo disponible estimado.|  
    |**Primera fecha posible**|Muestra la fecha de llegada del pedido de suministros entrante que puede cubrir la cantidad necesaria en una fecha posterior a la fecha de demanda.|  

5.  En el campo **Sistema reposición**, seleccione el tipo de pedido de suministros que se va a crear.  

    El valor predeterminado es el de la ficha producto, o ficha UA, pero puede cambiarlo por alguna de las tres opciones siguientes:  

    |Opción|Description|  
    |----------------------------------|---------------------------------------|  
    |**Compra**|Crea un pedido compra.|  
    |**Transferencia**|Crea un pedido de transferencia.|  
    |**Ord. prod.**|Crea una orden de producción.|  

    En el campo **Suministrado desde**, debe seleccionar un valor de acuerdo con el sistema de reposición elegido.  

    > [!NOTE]  
    >  Si no rellena este campo, el sistema mostrará un mensaje de error cuando utilice la función **Crear pedidos suministros**, y no se creará ningún pedido de suministros para la línea de planificación correspondiente. Esto, sin embargo, no sucede si el sistema de reposición es **Orden producción**.  

6.  En el campo **Suministrado desde**, puede consultar en la lista correspondiente y seleccionar de dónde debería proceder un suministro:  

    - Si el sistema de reposición es **Compra**, el botón de búsqueda de este campo busca en la página **Tarifas de compra productos**.  
    - Si el sistema de reposición es **Transferencia**, el botón de búsqueda de este campo busca en la página **Lista de almacenes**.  

    En caso de que el producto exista en otro almacén, el campo **Cdad. otros almacenes** situado en la parte inferior muestra un valor, y puede buscar y seleccionar el almacén del que debe suministrarse el producto cuando realice el pedido de transferencia.  

    Si existe un sustitutivo para el producto pedido, el campo **Existe sustitutivo** se establece en **Sí**, y puede realizar una búsqueda en la página **Movs. sustitución productos** para elegir un producto sustitutivo.  

7.  Seleccione la casilla de verificación **Reserva** si desea hacer una reserva entre el pedido de suministro que ha creado y la línea de demanda para la que se ha creado. De forma predeterminada, este campo está vacío.  

    > [!NOTE]  
    >  Sólo puede seleccionar esta casilla de verificación si el producto tiene el valor **Opcional** o **Siempre** en el campo **Reserva** de la ficha del producto.  

8.  En el campo **Cantidad que se pedirá**, puede especificar la cantidad que figurará en el pedido de suministros que va a crear.   
    El valor predeterminado es la misma cantidad que en el campo **Cantidad necesaria**. Sin embargo, podría decidir solicitar más o menos de esta cantidad según el conocimiento que disponga de la situación de demanda. Si, por ejemplo, ve en la página **Planificación de pedidos** que varias líneas de demanda no relacionadas corresponden al mismo producto comprado, y que su fecha de vencimiento es en torno a la misma fecha, podrá consolidarlas especificando la cantidad total necesaria en el campo **Cantidad que se pedirá** de una línea y, a continuación, eliminando el resto de líneas de planificación obsoletas de dicho producto.  

9.  En los campos **Fecha vencimiento** y **Fecha pedido**, puede especificar las fechas que deben aplicarse a los pedidos de suministros creados.  

    Estos dos campos están interrelacionados según el campo **Plazo seguridad genérico**, que se puede encontrar en la página **Configuración fabricación**. De forma predeterminada, la fecha de vencimiento es igual a la fecha de demanda, pero puede cambiarla si lo desea.  

> [!NOTE]  
>   Si especifica una fecha posterior a la fecha de demanda, se recibirá un mensaje de advertencia.  

## <a name="to-make-supply-orders"></a>Para crear pedidos de suministro  
1.  Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Órdenes producción planificadas** y luego elija el enlace relacionado. Puede realizar estos pasos para una orden de producción planificada, planificada en firme o lanzada.  
2.  Abra la orden de producción que se desea planificar y selección la acción **Planificación**.  
3.  Coloque el cursor en una línea de planificación relevante y seleccione la acción **Crear pedidos**.  
4.  En la página **Crear pedidos suministros**, en la ficha desplegable **Planificación de pedidos**, en el campo **Crear pedidos para**, seleccione una de las siguientes opciones.  

    |Opción|Description|  
    |----------------------------------|---------------------------------------|  
    |**La Línea activa**|Crea un pedido de suministro sólo para la línea donde está situado el cursor.|  
    |**El Pedido activo**|Crea pedidos de suministros para todas las líneas donde está situado el cursor.|  
    |**Todas líneas**|Crea pedidos de suministro para todas las líneas de la página **Programación de pedidos**.|  

5.  En la ficha desplegable **Opciones** defina el tipo de pedidos de suministros o líneas de hojas de demanda que se debe crear.  

    > [!NOTE]  
    >  la última configuración que realice en la página **Crear pedidos suministros** se guardará en su Id. de usuario para que se conserve la próxima vez que utilice la página.  

6.  Elija el botón **Aceptar** para crear los pedidos de suministro sugeridos o las líneas de la hoja de demanda.  

Ahora ha terminado de planificar la demanda insatisfecha mediante la creación de los pedidos de suministros correspondientes. La información detallada sobre los flujos de trabajo específicos cuando se utiliza la página **Planificación de pedidos** dependerá de las políticas internas de la empresa.  

Cuando termine el trabajo de planificación en la página **Programación de pedidos** (por ejemplo, cuando haya definido otro modo de suministrar la cantidad), puede empezar a crear pedidos de suministros para las distintas líneas de planificación.  

> [!NOTE]  
>  Los pedidos de suministro que cree pueden producir nueva demanda dependiente, por ejemplo, para órdenes de producción subyacentes y, por tanto, deberá seleccionar **Calcular plan** de nuevo para localizarlo y resolverlo antes de continuar.  

## <a name="see-also"></a>Consulte también  
[Planificación](production-planning.md)  
[Configuración de fabricación](production-configure-production-processes.md)  
[Fabricación](production-manage-manufacturing.md)    
[Grupos contables inventario](inventory-manage-inventory.md)  
[Compras](purchasing-manage-purchasing.md)  
[Detalles de diseño: planificación de aprovisionamiento](design-details-supply-planning.md)   
[Procedimientos recomendados de configuración: planificación de suministros](setup-best-practices-supply-planning.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
