---
title: "Detalles de diseño: Flujos internos de almacén | Documentos de Microsoft"
description: "El flujo de productos entre las ubicaciones en una ubicación de empresa se centra en el picking de los componentes y en la ubicación de productos para los pedidos de ensamblado u órdenes de producción, y en los movimientos ad hoc, como reposiciones de ubicación, sin una relación con los documentos de origen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/23/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: e7638c602568c15b0496d4f73aa6ea59c20f82e8
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-internal-warehouse-flows"></a>Detalles de diseño: Flujos de almacén internos
El flujo de productos entre las ubicaciones en una ubicación de empresa se centra en el picking de los componentes y en la ubicación de productos para los pedidos de ensamblado u órdenes de producción, y en los movimientos ad hoc, como reposiciones de ubicación, sin una relación con los documentos de origen. El ámbito y la naturaleza de las actividades implicadas varía entre almacenamiento básico y avanzado.  

 Algunos flujos internos se solapan con los flujos de entrada o de salida. Parte de esta superposición se muestra como los pasos 4 y 5 de los diagramas gráficos para los flujos de entrada y de salida avanzados, respectivamente. Para obtener más información, consulte [Detalles de diseño: Flujo de entrada del almacén](design-details-outbound-warehouse-flow.md).  

## <a name="internal-flows-in-basic-warehousing"></a>Flujos internos en gestión básica de almacén  
 En la configuración básica del almacén, el flujo de productos entre ubicaciones dentro de la empresa se centra en la selección de componentes y la ubicación de productos finales para pedidos de ensamblado u órdenes de producción, y en movimientos ad hoc, como reposiciones de ubicación, sin relación con los documentos de origen.  

### <a name="flows-to-and-from-production"></a>Flujos a o desde producción  
 La integración principal entre las órdenes de producción y las actividades de almacén básicas se representa mediante la capacidad de realizar el picking de los componentes de producción con las ventanas **Picking inventario** o **Movimiento inventario**.  

> [!NOTE]  
>  En la ventana **Picking inventario**, el consumo de componentes se registra junto con el registro de selección. En la ventana **Movimiento inventario** solo se registran los ajustes de la ubicación, ningún movimiento de producto.  

 Además de la gestión de componentes, la integración se representa mediante la capacidad de colocar los productos fabricados con la ventana **Ubicación inventario**.  

 Los campos **Cód. ubic. para producción**, **Cód. ubic. desde producción** y **Abre ubic. aprovision. manual** de la ficha de ubicación o de las fichas de máquina/centro de trabajo definen los flujos predeterminados a las áreas de producción y desde ellas.  

 Para obtener más información acerca del procedimiento de bajada del consumo desde las ubicaciones para producción o de aprovisionamiento manual, consulte la sección Consumo de componentes de producción en el almacén en este tema.  

### <a name="flows-to-and-from-assembly"></a>Flujos a o desde el ensamblado  
 La integración principal entre los pedidos de ensamblado y las actividades de almacén básico se representa por la capacidad de mover a los componentes del ensamblado al área de ensamblado.  

 Aunque no existe una funcionalidad de almacén específica para la ubicación de elementos de ensamblado, el código de ubicación del encabezado de pedido de ensamblado se puede configurar en una ubicación predeterminada. El registro del pedido de ensamblado funciona como el registro de una ubicación. La actividad de almacén para mover los elementos de ensamblado al almacén se puede administrar en la ventana **Movimiento interno**, sin relación con el pedido de ensamblado.  

 Existen los siguientes flujos de ensamblado.  

|Flujo de trabajo|Descripción|  
|----------|---------------------------------------|  
|Ensamblar para stock|Los componentes se necesitan en un pedido de ensamblado donde la salida se guarda en el almacén.<br /><br /> Este flujo de almacén se administra en la ventana **Movimiento inventario**. Una línea de toma especifica de dónde tomar los componentes. Una línea de plaza especifica dónde colocar los componentes.|  
|Ensamblar para pedido|Los componentes se necesitan en un pedido de ensamblado vinculado a un pedido de venta que se envía cuando se ensambla el producto vendido.|  

> [!NOTE]  
>  Si se ensamblan productos para un pedido, la selección de inventario del pedido de venta vinculado acciona un movimiento de inventario para todos los componentes de ensamblado que participan, no solo para el producto vendido, como ocurre al enviar productos de inventario.  

 Los campos de **Cód. ubic. para ensamblado**, **Cód. ubic. desde ensamblado** y **Cód. ubic. ens.contra-pedido** de la ficha de ubicación definen los flujos predeterminados a áreas del ensamblado y desde ellas.  

> [!NOTE]  
>  El campo **Cód. ubic. ens.contra-pedido** funciona como la ubicación desde ensamblado en los escenarios ensamblar para pedido.  

### <a name="ad-hoc-movements"></a>Movimientos ad hoc  
 En la gestión básica del almacén, el movimiento de los productos de ubicación a ubicación sin relación con los documentos de origen se realiza en la ventana **Movimiento interno**, la cual funciona conjuntamente con la ventana **Movimiento inventario**.  

 Otra forma de mover productos ad hoc entre ubicaciones es registrar movimientos positivos en el campo **Código ubicación nuevo** de la ventana **Diario reclasif. producto**.  

## <a name="internal-flows-in-advanced-warehousing"></a>Flujos internos en gestión avanzada de almacén  
 En configuraciones avanzadas de almacén, el flujo de productos entre las ubicaciones dentro de la empresa se centra en el componente de selección y colocación de productos finales para órdenes de producción y componentes de selección para pedidos de ensamblado. Además, los flujos internos se producen como movimientos ad hoc, como reposiciones de ubicación, sin relación con los documentos de origen.  

### <a name="flows-to-and-from-production"></a>Flujos a o desde producción  
 La integración principal entre las órdenes de producción y las actividades de almacén avanzadas se representa mediante la capacidad de realizar el picking de los componentes de producción, en las ventanas **Picking almacén** y **Hoja trabajo picking**, y la capacidad de ubicar los productos fabricados con la ventana **Ubicación interna alm.**  

 La ventana **Movimiento almacén** proporciona otro punto de integración en la producción, que junto con la ventana Hoja trabajo movimiento, le permite colocar componentes y hacerse con productos fabricados para las órdenes de producción lanzadas.  

 Los campos **Cód. ubic. para producción**, **Cód. ubic. desde producción** y **Abre ubic. aprovision. manual** de la ficha de ubicación o de las fichas de máquina/centro de trabajo definen los flujos predeterminados a las áreas de producción y desde ellas.  

 Para obtener más información acerca del procedimiento de bajada del consumo desde las ubicaciones para producción o de aprovisionamiento manual, consulte la sección Consumo de componentes de producción en el almacén en este tema.  

### <a name="flows-to-and-from-assembly"></a>Flujos a o desde el ensamblado  
 La integración principal entre los pedidos de ensamblado y las actividades de almacén avanzadas se representa por la capacidad de realizar el picking de los componentes del ensamblado, tanto en la ventana **Picking almacén** como en la ventana **Hoja trabajo picking**. Esta funcionalidad opera igual que al realizar el picking de componentes para las órdenes de producción.  

 Aunque no existe una funcionalidad de almacén específica para la ubicación de elementos de ensamblado, el código de ubicación del encabezado de pedido de ensamblado se puede configurar en una ubicación predeterminada. El registro del pedido de ensamblado funciona como el registro de una ubicación. La actividad de almacén para mover los elementos de ensamblado al almacén se puede administrar en la ventana **Hoja trabajo movimiento** o **Ubicación interna alm.**, sin relación con el pedido de ensamblado.  

> [!NOTE]  
>  Si se ensamblan productos para un pedido, el envío de almacén del pedido de venta vinculado acciona una selección de almacén para todos los componentes de ensamblado que participan, no solo para el producto vendido, como ocurre al enviar productos de inventario.  

 Los campos de **Cód. ubic. para ensamblado** y **Cód. ubic. desde ensamblado** de la ficha de ubicación definen los flujos predeterminados a áreas del ensamblado y desde ellas.  

### <a name="ad-hoc-movements"></a>Movimientos ad hoc  
 En la gestión avanzada del almacén, el movimiento de los productos de ubicación a ubicación sin relación con los documentos de origen se gestiona en la ventana **Hoja trabajo almacén** y se registra en la ventana Movimiento almacén.  

## <a name="flushing-production-components-in-the-warehouse"></a>Consumo de componentes de producción en el almacén  
 Si se han configurado en la ficha del producto, los componentes seleccionados mediante de almacén se registran como consumidos por la orden de producción cuando se registra la selección de almacén. Con los métodos de baja **Seleccionar + Adelante** y **Seleccionar + Atrás**, el registro de selección activa el registro de consumo relacionado cuando la primera operación comienza o cuando la última operación acaba, respectivamente.  

 Tenga en cuenta el ejemplo siguiente basado en la base de datos de demostración de [!INCLUDE[d365fin](includes/d365fin_md.md)], almacén BLANCO.  

 Existe una orden de producción para 15 UDS del producto LS-100. Algunos de los productos de la lista de componentes deben darse de baja manualmente en un diario de consumo, y en los demás productos de la lista se puede llevar a cabo el picking y la baja automáticamente mediante el método de baja **Pick + Atrás**.  

> [!NOTE]  
>  **Pick + Adelante** solo funciona si la segunda operación de línea de ruta de producción usa un código de vínculo de rutas. Lanzar una orden de producción planificada inicia la baja hacia adelante de los componentes configurados como **Pick + Adelante**. No obstante, la baja no puede realizarse hasta que se registre la selección de los componentes, que de nuevo solo puede tener lugar cuando se lance el pedido.  

 En los pasos siguientes se describen las acciones correspondientes para distintos usuarios y la respuesta relacionada:  

1.  El supervisor de planta lanza la orden de producción. Los productos con el método de baja **Anticipada** y sin código de conexión de ruta se deducen de la ubicación de aprovisionamiento manual.  
2.  El supervisor de planta elige el botón **Crear selección de almacén** en la orden de producción. Un documento de selección de almacén se crea para seleccionar productos con métodos de baja **Manual**, **Seleccionar + Atrás** y **Seleccionar + Adelante**. Estos productos se colocan en la ubicación para producción.  
3.  El administrador de almacén asigna los picking a un empleado de almacén.  
4.  El trabajador de almacén picking directos los productos de las ubicaciones y de los apartados apropiados estos comandos en la ubicación para producción o en la ubicación especificados en picking de almacén, que puede ser una ubicación del centro de trabajo o del centro de máquina.  
5.  El empleado de almacén registra el picking. La cantidad se resta de las ubicaciones de picking y se agregan a la ubicación de consumo. Se actualiza el campo **Cdad. preparada pedido** de la lista de componentes para todos los productos preparados.  

    > [!NOTE]  
    >  Solo se puede consumir la cantidad preparada.  

6.  El operador de máquina notifica al director de producción que se han completado los productos finales.  
7.  El supervisor de planta usa el diario de consumo o de producción para registrar el consumo de los productos componentes que usan el método de baja **Manual**, o bien los métodos de baja **Adelante** o **Pick + Adelante** junto con los códigos de conexión de ruta.  
8.  El administrador de producción registra la salida de la orden de producción y modifica el estado a **Terminada**. La cantidad de productos componentes que usan el método de baja **Atrás** se deduce de la ubicación de aprovisionamiento manual y la cantidad de los productos componentes que usan el método de baja **Pick + Atrás** se deduce de la ubicación para producción.  

 En la ilustración siguiente se muestra cuando se rellena el campo **Cód. ubicación** de la lista de componentes según la configuración de la máquina o del centro de trabajo.  

 ![Gráfico de flujo de ubicación](media/binflow.png "BinFlow")  

## <a name="see-also"></a>Consulte también  
 [Detalles de diseño: Gestión de almacén](design-details-warehouse-management.md)

