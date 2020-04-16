---
title: Recepción y ubicación en el almacenamiento avanzado | Documentos de Microsoft
description: En Business Central, los procesos de entrada para la recepción y la ubicación se pueden realizar de cuatro maneras utilizando distintas funciones según el nivel de complejidad del almacén.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 4027fd2d7ce3e514aa451279c8800453ba62711b
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/01/2020
ms.locfileid: "3195656"
---
# <a name="walkthrough-receiving-and-putting-away-in-advanced-warehouse-configurations"></a>Tutorial: recepción y ubicación en la configuración del almacenamiento avanzado

**Nota**: Este tutorial debe realizarse en una empresa de demostración con la opción **Evaluación completa - Datos de muestra completos**, que está disponible en el entorno de espacio aislado. Para obtener más información, consulte [Creación de un entorno aislado](across-how-create-sandbox-environment.md).

En [!INCLUDE[d365fin](includes/d365fin_md.md)], los procesos de entrada para la recepción y la ubicación se pueden realizar de cuatro maneras utilizando distintas funciones según el nivel de complejidad del almacén.  

|Método|Proceso de salida|Ubicaciones|Recepciones|Ubicaciones|Nivel de complejidad (consulte [Detalles de diseño: Configuración de almacén](design-details-warehouse-setup.md))|  
|------------|---------------------|----------|--------------|----------------|--------------------------------------------------------------------------------------------------------------------|  
|A|Registro de la recepción y ubicación desde la línea de pedido|X|||2|  
|P|Registro de la recepción y ubicación desde un documento de ubicación del inventario|||X|3|  
|C|Registro de la recepción y ubicación desde un documento de recepción de almacén||X||5/4/6|  
|D|Registro de la recepción desde un documento de recepción de almacén y registro de ubicación desde un documento de ubicación de almacén||X|X|5/4/6|  

Para obtener más información, consulte [Detalles de diseño: Flujo de entrada del almacén](design-details-inbound-warehouse-flow.md).  

En el siguiente tutorial se demuestra el método D de la tabla anterior.  

## <a name="about-this-walkthrough"></a>Acerca de este tutorial  
En la configuración avanzada de almacén, donde el almacén está configurado para requerir el procesamiento de recepción además del procesamiento de ubicación, utiliza la página **Recep. almacén** para registrar la recepción de productos en varios pedidos entrantes. Cuando se registra la recepción de almacén, se crean uno o más documentos de ubicación de almacén para indicar a los empleados del almacén que tomen el producto y lo coloquen en lugares designados según la configuración de la ubicación o en otras ubicaciones. La colocación específica de los productos se registra cuando se registra la ubicación del almacén. El documento de origen de entrada puede ser un pedido de compra, una devolución de ventas, un pedido de transferencia de entrada o una orden de producción o ensamblaje con salida que está preparada para ubicarse. Si el albarán se crea a partir de un pedido de entrada, se puede recuperar más de un documento de origen entrante para el albarán. Con este método puede registrar muchos productos que llegada de distintos pedidos de entrada con un albarán.  

En este tutorial, se demuestran las siguientes tareas.  

-   Configuración de la ubicación BLANCA para recepción y ubicación.  
-   Cree o lance dos pedidos de compra para la manipulación completa en el almacén.  
-   Cree y registre un documento de recepción de almacén para varias líneas de pedido de compra de proveedores específicos.  
-   Registrar una ubicación de almacén para los productos recibidos.  

## <a name="roles"></a>Funciones  
En este tutorial, se demuestran las tareas realizadas por los siguientes roles de usuario:  

-   Responsable de almacén  
-   Agente de compras  
-   Personal de recepción  
-   Trabajador de almacén  

## <a name="prerequisites"></a>Requisitos previos  
Para completar este tutorial, necesitará:  

-   CRONUS España S.A. instalado.  
-   Para convertirse en un empleado de almacén en el almacén BLANCO, realice los pasos siguientes:  

1.  Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Empleados de almacén** y luego elija el enlace relacionado.  
2.  Elija el campo **Id. de usuario** y seleccione su propia cuenta de usuario en la página **Usuarios**.  
3.  En el campo **Cód. almacén**, especifique BLANCO.  
4.  Seleccione el campo de **Predeterminado**.  

## <a name="story"></a>Historia  
Alicia, el agente de compra en CRONUS España S.A., crea dos pedidos de compra de productos de accesorio de los proveedores 10000 y 20000 para su entrega al almacén BLANCO. Cuando las salidas llegan al almacén, Sammy, responsable de recibir los productos de los proveedores 10000 y 20000, utiliza un filtro para crear las líneas de recepción para los pedidos de compra que llegan de los dos proveedores. Sammy registra los productos como recibidos en el inventario en una recepción de almacén y pone los productos a disposición para venta u otra demanda. Juan, el empleado del almacén, toma los artículos de la ubicación de recepción y los aparta. Guarda todas las unidades en sus ubicaciones predeterminadas, excepto 40 de las 100 bisagras recibidas, las cuales guarda en el departamento de ensamblado dividiendo la línea de ubicación interna. Cuando Juan registra la ubicación, se actualiza el contenido de la ubicación se y los productos se ponen a disposición para picking del almacén.  

## <a name="reviewing-the-white-location-setup"></a>Revisar la configuración de la ubicación BLANCA  
La configuración de la página **Ficha almacén** define los flujos de almacén de la empresa.  

### <a name="to-review-the-location-setup"></a>Para revisar la configuración de almacén  

1.  Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Almacenes** y, a continuación, elija el enlace relacionado.  
2.  Abra la ficha de almacén BLANCO.  
3.  Observe que en la ficha desplegable **Almacén** el casilla **Ubicac. y pick. directo**.  

    Esto significa que la ubicación está configurada para el máximo nivel de complejidad, reflejado por el hecho de que todas las casillas de manipulación de almacén de la ficha desplegable están seleccionadas.  

4.  Observe en la ficha desplegable **Ubicaciones** que las ubicaciones están especificadas en los campos **Cód. ubicación recepción** y **Cód. ubicación envío**.  

Esto significa que cuando se crea una recepción de almacén, este código de ubicación se copia en la cabecera del documento de recepción de almacén de manera predeterminada y en las líneas de las ubicaciones de almacén resultantes.  

## <a name="creating-the-purchase-orders"></a>Creación de pedidos de compra  
Los pedidos de compra son el tipo más común de documento de origen de entrada.  

### <a name="to-create-the-purchase-orders"></a>Procedimiento para crear pedidos de compra  

1.  Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Pedidos de compra** y luego elija el enlace relacionado.  
2.  Seleccione la acción **Nuevo**.  
3.  Cree un pedido de compra para el proveedor 10000 en la fecha de trabajo (23 de enero) con las líneas de pedido de compra siguientes.  

    |Producto|Cód. almacén|Cantidad|  
    |----------|-------------------|--------------|  
    |70200|BLANCO|100 UDS|  
    |70201|BLANCO|50 UDS|  

    Empiece a notificar el almacén para el que el pedido de compra está preparado para la manipulación en almacén cuando llegue la entrega.  

4.  Seleccione la acción **Liberar**.  

    Continúe creando el segundo pedido de compra.  

5.  Seleccione la acción **Nuevo**.  
6.  Cree un pedido de compra para el proveedor 20000 en la fecha de trabajo con las líneas de pedido de compra siguientes.  

    |Producto|Cód. almacén|Cantidad|  
    |----------|-------------------|--------------|  
    |70100|BLANCO|10 CAN|  
    |70101|BLANCO|12 CAN|  

    Seleccione la acción **Liberar**.  

    Las entregas de los artículos de los proveedores 10000 y 20000 han llegado al almacén BLANCO y Sammy comienza a procesar los albaranes de compra.  

## <a name="receiving-the-items"></a>Recibir los productos  
En la página **Recep. almacén**, puede administrar varios pedidos entrantes para documentos de origen, como un pedido de compra.  

### <a name="to-receive-the-items"></a>Procedimiento para recibir productos  
1.  Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Recepciones almacén** y luego elija el enlace relacionado.  
2.  Seleccione la acción **Nuevo**.  
3.  En el campo **Cód. almacén**, especifique BLANCO.  
4.  Elija la acción **Utiliz. filt. para traer docs.**.  
5.  En el campo **Código**, especifique **ACCESORIO**.  
6.  En el campo **Descripción**, escriba **Proveedores 10000 y 20000**.  
7.  Seleccione la acción **Modificar**.  
8.  En la ficha desplegable **Compra**, en el campo **Filtro compra-a nº proveedor**, especifique **10000&#124;20000**.  
9. Seleccione la acción **Ejecutar**. La recepción de almacén se rellena con cuatro líneas que representan líneas de pedido de compra para los proveedores especificados. Se rellena el campo **Cantidad a recibir** porque no seleccionó la casilla **No rellene cdad. a manipular** de la página **Filtros para traer docs. orig.**.  
10. También, si desea utilizar un filtro como se ha descrito anteriormente en esta sección, elija la opción **Obtener documento de origen** y, a continuación, seleccione los pedidos de compra de los proveedores en cuestión.  
11. Elija la acción **Registrar recepción** y, a continuación, seleccione el botón **Si**.  

    Los movimientos de producto positivos se crean reflejando los albaranes de compra registrados de los accesorios de los proveedores 10000 y 20000, y los artículos están listos para ubicarlos en el almacén de la ubicación de recepción.  

## <a name="putting-the-items-away"></a>Establecer la ubicación de productos  
En la página **Ubicar almacén**, puede administrar ubicaciones para un documento de recepción de almacén específico que cubre varios documentos de origen. Como todos los documentos de actividad de almacén, cada producto de la ubicación de almacén se representa por una línea Traer y una línea Colocar. En el procedimiento siguiente, el código de ubicación en las líneas Traer es la ubicación de recepción predeterminada en la ubicación BLANCO, W-08-0001.  

### <a name="to-put-the-items-away"></a>Para ubicar los productos  
1.  Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Ubicaciones** y luego elija el enlace relacionado.  
2.  Seleccione el único documento de ubicación de almacén en la lista y, a continuación, elija acción **Editar**.  

    El documento de ubicación de almacén se abre con un total de ocho líneas Traer o colocar para las cuatro líneas del pedido de compra.

    Al empleado del almacén se le indica que necesitan 40 bisagras en el departamento de ensamblado y divide la única línea Colocar para especificar una segunda línea Colocar para la ubicación W-02-0001 en el departamento de ensamblado donde coloca esa parte de las bisagras recibidas.  

3.  Seleccione la segunda línea de la página **Ubicar almacén**, la línea Colocar del producto 70200.  
4.  En el campo **Cdad. a manipular**, cambie el valor de 100 a 60.  
5.  En la ficha desplegable **Líneas**, elija **Acciones** y, a continuación, elija **Dividir línea**. Una nueva línea se inserta para el producto 70200 con 40 en el campo **Cdad. a manipular**.  
6.  En el campo **Cód. ubicación**, especifique W-02-0001. El campo **Cód. zona** se rellena de forma automática.  

    Continúe registrando la ubicación.  

7.  Elija la acción **Registrar ubicación** y, a continuación, seleccione el botón **Si**.  

    Los accesorios recibidos se ubican ahora en las ubicaciones predeterminadas de los productos y se colocan 40 bisagras en el departamento de ensamblado. Los productos recibidos están disponibles ahora para picking para demanda interna, como pedidos de ensamblado, o para demanda externa, como albaranes de venta.  

## <a name="see-also"></a>Consulte también  
 [Ubicar productos con ubic. exist. almacén](warehouse-how-to-put-items-away-with-warehouse-put-aways.md)   
 [Mover productos en configuraciones avanzadas de almacén](warehouse-how-to-move-items-in-advanced-warehousing.md)   
 [Detalles de diseño: Flujo de entrada en almacén](design-details-inbound-warehouse-flow.md)   
 [Tutorial: recepción y ubicación en la configuración del almacenamiento básico](walkthrough-receiving-and-putting-away-in-basic-warehousing.md)   
 [Tutoriales de procesos empresariales](walkthrough-business-process-walkthroughs.md)
