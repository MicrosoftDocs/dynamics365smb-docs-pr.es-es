---
title: "Cómo ubicar la salida de producción | Documentos de Microsoft"
description: "La forma de ubicar la salida de su producción depende de cómo esté configurado el almacén."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/16/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 9555f2810e82711c9cac98cfe002cb99289ce474
ms.contentlocale: es-es
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-put-away-production-or-assembly-output"></a>Cómo ubicar la salida de producción o la salida de ensamblado
La forma de ubicar la salida de su producción depende de cómo esté configurado el almacén. Para obtener más información, consulte [Configuración de la administración de almacén](warehouse-setup-warehouse.md).  

En las configuraciones básicas de almacén, donde el almacén requiere el proceso de ubicación pero no el de recepción, utilice el documento **Ubicación inventario** para organizar y registrar la ubicación de la salida.  

En las configuraciones avanzadas de almacén, donde el almacén no requiere los procesos de ubicación y recepción, cree un documento de ubicación interno o un documento de movimiento para ubicar la salida.  

El primer paso para crear la ubicación de salida es crear la solicitud de almacén de entrada. Esta solicitud informa al almacén de que la salida del pedido de producción o ensamblado está preparada para ubicación.

## <a name="to-create-the-inbound-warehouse-request"></a>Para crear la solicitud de entrada al almacén  
1.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Orden producción lanzada** y, a continuación, seleccione el vínculo relacionado.  
2.  En la orden de producción que está preparada para ubicación, elija la acción **Crear petición entrada alm.**  

> [!NOTE]  
>  También puede crear la solicitud de almacén de entrada seleccionando la casilla de verificación **Crear solicitud de entrada** cuando actualice la orden de producción. Para obtener más información, vea [Procedimiento: Actualizar o replanificar o actualizar las órdenes de producción](production-how-to-replan-refresh-production-orders.md).  

## <a name="to-put-output-away-with-an-inventory-put-away"></a>Para ubicar la salida con una ubicación de inventario  
1.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Ubicac. inventario** y, a continuación, seleccione el vínculo relacionado.  
2.  Cree una ubicación de inventario nueva. Para obtener más información, vea [Procedimiento: ubique productos con ubicaciones de almacén](warehouse-how-to-put-items-away-with-inventory-put-aways.md).
3.  Para tener acceso a la salida de la orden de producción, elija la acción **Traer doc. origen** y, a continuación, seleccione la orden de producción lanzada.  
4.  Rellene las líneas de ubicación como crea conveniente.
5.  Cuando las líneas estén preparadas para registrar, elija la acción **Registrar**. El registro creará los movimientos de almacén necesarios y registrará la salida de los productos.  

También puede crear **Ubicación existencias** directamente de la orden de producción lanzada. Para obtener más información, vea [Procedimiento: ubique productos con ubicaciones de almacén](warehouse-how-to-put-items-away-with-inventory-put-aways.md).  

Al ubicar y registrar el inventario, se asume que todas las operaciones se registran según la ruta estándar, es decir, la cantidad de salida se registra de acuerdo con la última operación. Puede usar el diario de salida para registrar las desviaciones de la cantidad de salida y los tiempos de preparación y ejecución. Si es necesario realizar un registro parcial después de crear la ubicación de inventario, puede hacerlo con los tiempos de preparación y las cantidades de todas las operaciones, excepto la última. En tal caso, la ubicación de inventario controla la última operación.  

Si solo necesita registrar el tiempo de preparación y ejecución de la última operación, defina la cantidad de salida de la última operación en 0. También puede decidir no registrar la última línea eliminándola.  

## <a name="to-put-output-away-with-a-warehouse-internal-put-away"></a>Para ubicar la salida con una ubicación interna de almacén
1.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Ubicación interna almacén** y, a continuación, seleccione el vínculo relacionado.  
2. Seleccione la acción **Nuevo**.
3. Rellene la cabecera de una nueva ubicación interna con, al menos, el **Cód. almacén.**  
4. Rellene una línea por cada producto que desea mover al almacén. Sólo tiene que rellenar los campos **Nº producto** y **Cantidad**.  

    > [!NOTE]  
    >  Al seleccionar el campo **Nº producto**, se abrirá la **Lista contenidos** ubicación en vez de la **Lista de productos**. Esto es porque desea ubicar un producto que está en una ubicación determinada, un Contenido ubicación, que no es sólo un producto y ya conoce la ubicación de la que se debe traer el producto.  

4.  Para rellenar las líneas de la hoja de trabajo con todo el contenido de la ubicación o el contenido filtrado de las ubicaciones del almacén, elija la acción **Traer conten. ubicac.**.  
5.  Elija la acción **Crear ubicación** y los productos que desea mover a producción se colocarán en instrucciones de ubicación en espera de almacenamiento.  

> [!NOTE]  
>  Cuando el almacén está configurado para utilizar ubicaciones y picking directos, el al está vinculado al área de fabricación a través de las ubicaciones de producción genéricas: las ubicaciones de entrada y salida y la ubicación de control de planta, que define en la ficha desplegable **Ubicaciones** de la ficha de almacén. Cuando registra la salida de una orden de producción, la salida se coloca automáticamente en la **Ubicación de salida de producción**. Siga el mismo procedimiento descrito anteriormente para ubicar la salida de producción, excepto que en vez de utilizar la ubicación genérica del producto, moverá o ubicará los productos desde la **ubicación de salida de producción** en la ubicación predeterminado del producto.  

## <a name="to-manually-specify-a-bin-to-store-items-from-production-output"></a>Para especificar manualmente una ubicación para almacenar los artículos de la salida de producción  
1.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Hoja movimiento** y, a continuación, seleccione el vínculo relacionado.  
2.  Rellene la cabecera y cree una línea por cada producto que desea mover al almacén.  
3.  Rellene los campos **Desde cód. ubicación** y **Hasta cód. ubicación** e introduzca la cantidad en el campo **Cantidad**.  
4.  Para rellenar las líneas de la hoja de trabajo con todo el contenido de la ubicación o el contenido filtrado de las ubicaciones del almacén, elija la acción **Traer conten. ubicac.**.  
5. Seleccione la acción **Crear movimiento**. Se crean instrucciones de movimiento de almacén con líneas Traer y Colocar para que los empleados de almacén las ejecuten.  

> [!NOTE]  
>  En los documentos de almacén (documentos de ubicación interna, ubicación o movimiento) no puede introducir el número del documento de origen (número de orden de producción) de cada proceso.  

## <a name="see-also"></a>Consulte también  
[Gestión almacén](warehouse-manage-warehouse.md)  
[Grupos contables inventario](inventory-manage-inventory.md)  
[Configuración de la gestión del almacén](warehouse-setup-warehouse.md)     
[Gestión de ensamblaje](assembly-assemble-items.md)    
[Detalles de diseño: Gestión de almacén](design-details-warehouse-management.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

