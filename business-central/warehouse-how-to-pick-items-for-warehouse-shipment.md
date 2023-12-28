---
title: Realizar un picking de los artículos para el envío de almacén
description: Obtenga información sobre cómo a utilizar los documentos de picking de almacén para crear y procesar información de picking antes de registrar el envío del almacén.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 09/11/2023
ms.custom: bap-template
ms.search.forms: '7335, 7339, 7345,'
---
# Realizar un picking de los artículos para el envío de almacén

En [!INCLUDE[prod_short](includes/prod_short.md)], la selección y el envío de productos se realizan mediante uno de los cuatro métodos, como se describe en la siguiente tabla.

|Método|Proceso de salida|Picking requerido|Envío requerido|Nivel de complejidad (Obtenga más información en [Descripción general de la gestión de almacenes](design-details-warehouse-management.md))|  
|------|----------------|-----|---------|-------------------------------------------------------------------------------------|  
|A|Registro de picking y envío desde la línea de pedido|||No hay ninguna actividad de almacén dedicada.|  
|B|Registro de picking y envío desde un documento de picking de existencias|Activado||Básico: Pedido por pedido|  
|P|Registro de picking y envío desde un documento de envío de almacén||Activado|Básico: Publicación consolidada de recepción/envío para múltiples pedidos.|  
|D|Registro de picking desde un documento de picking de almacén y registro de envío de un documento de envío de almacén|Activado|Activado|Avanzado|  

Obtenga más información en [Flujo de salida del almacén](design-details-outbound-warehouse-flow.md).

Este artículo hace referencia al método D de la tabla. Para obtener más información sobre el envío de productos, vaya a [Envío de productos](warehouse-how-ship-items.md).

Cuando el almacén está configurado para requerir el procesamiento de picking de almacén y el envío de almacén, utilice documentos de picking de almacén para crear y procesar la información antes de que registre el envío de almacén.  

A continuación, puede crear los documentos de almacén desde cero. Los pickings son parte de un flujo de trabajo en el que una persona que está procesando un pedido los crea de forma automática, o el empleado del almacén los crea de forma automática:

- De manera forzada, donde utiliza la acción **Crear picking** en la página **Envío de almacén** . Seleccione las líneas que se van a seleccionar y prepare los picking mediante la especificación, por ejemplo, de las ubicaciones de las que se tomarán, las ubicaciones en las que se colocarán y la cantidad de unidades que se manipularán. Las ubicaciones se pueden predefinir para la ubicación del almacén o el recurso.
- De manera forzada, donde usa la acción **Liberar** en la página **Envío de almacén** para hacer que los artículos estén disponibles para el picking. A continuación, en la página **Hoja trabajo picking**, los empleados del almacén pueden usar la acción **Traer documentos almacén** para obtener los pickings asignados.

> [!NOTE]  
> El picking para un envío de almacén de los productos que se ensamblan para un pedido de venta sigue los mismos pasos que para el picking de almacén normales para envíos, tal como se describe en este artículo. Sin embargo, el número de líneas de picking para la cantidad a enviar puede ser de "varias a una" porque realiza el picking de los componentes, no el producto ensamblado.  
>
> Las líneas de picking de almacén se crean para el valor del campo **Cantidad pendiente** en las líneas de pedido de ensamblado vinculado a la línea de pedido de venta que se envía. Se realiza en picking en todos los componentes en una acción. Obtenga más información en [Tratamiento de productos de ensamblar para pedido en los envíos de almacén](warehouse-how-ship-items.md#handling-assemble-to-order-items-in-warehouse-shipments).  
>  
> Para obtener información acerca de la realización de picking de componentes para pedidos de ensamblado en general, incluidas las situaciones en las que los productos no están relacionados con un envío de ventas, consulte [Picking para producción, ensamblado o proyectos en configuraciones avanzadas de almacén](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md).  

## Verifique si los artículos están disponibles para ser recogidos

[!INCLUDE [inventory-availability-overview](includes/inventory-availability-overview.md)]

## Para crear documentos de picking de forma masiva con la hoja de trabajo de picking

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Hoja trabajo picking** y luego elija el enlace relacionado.  

2. Seleccione la acción **Traer documentos almacén**.  

    La lista incluirá todos los envíos que se hayan liberado para picking, incluidos aquellos para los que ya se han creado instrucciones de picking. Los documentos con líneas de picking que ya se han preparado completamente no se muestran en la lista.  
3. Escriba el envío para el que desea preparar el picking.

    > [!NOTE]  
    >  Si intenta seleccionar un documento de envío o picking interno para el que ya ha creado instrucciones para todas sus líneas obtendrá un mensaje que indica algo similar a "no tiene nada que manipular". Para combinar instrucciones de picking de almacén que ya haya creado en una instrucción de picking más eficiente, debe eliminar los picking de almacén individuales primero.

4. Rellene el campo **Método ordenación** para ordenar las líneas.  

    > [!NOTE]  
    >  La forma en que se ordenan las líneas en la hoja de trabajo no se traslada automáticamente a la instrucción de picking. Sin embargo, existen las mismas oportunidades de ordenación y clasificación de ubicaciones. Puede recrear fácilmente el orden de las líneas que planifica en la hoja de trabajo cuando se crean las instrucciones de picking o al ordenar las instrucciones de picking.

5. Rellene el campo **Cantidad a manipular** de forma manual o usando la acción **Autorrellenar el campo Cdad. para manipular**.  

    La página muestra las cantidades disponibles en contenedores de cross-dock. Esta información es útil para planificar asignaciones de trabajo en situaciones de cross-docking. [!INCLUDE[prod_short](includes/prod_short.md)] siempre propondrá una selección de un contenedor de cross-dock primero.
6. Si es necesario, edite las líneas. También puede eliminar líneas para realizar un picking más eficaz. Por ejemplo, si hay varias líneas con productos en ubicaciones de tránsito directo, es posible que desee realizar un picking de todas las líneas. Se enviarán los productos de tránsito directo con el resto de los productos de los envíos, y las ubicaciones de tránsito directo tendrán espacio para la entrada de más productos.  

    > [!NOTE]  
    >  Si elimina líneas, solo se eliminan de la hoja de trabajo. No se eliminan de la lista de selección de picking.  

7. Elija la acción **Crear picking**. Se abrirá la página **Crear picking** en la que puede agregar más información al picking que está creando. Especifique cómo se combinan las líneas de picking en los documentos de picking creados seleccionando una de las siguientes opciones.  

    |Opción|Descripción|
    |-|-|
    |Por almacén Documento|Crea los documentos de picking independientes para las líneas de la hoja de cálculo con el mismo documento de origen de almacén.|
    |Por Cli./Prov./Alm.|Cree los documentos de picking independientes para cada cliente (pedidos de venta), el proveedor (devoluciones de compra), y la ubicación (pedidos de transferencia).|
    |Por prod.|Cree los documentos de picking independientes para cada producto en la hoja de cálculo de picking.|
    |Por Desde zona|Cree los documentos de picking independientes para cada zona de la que traerá los productos.|
    |Por ubicación|Cree los documentos de picking independientes para cada ubicación de la que traerá los productos.|
    |Por fecha vto.|Cree los documentos de picking independientes para los documentos de origen con la misma fecha de vencimiento.|

    Especifique cómo se crean los documentos de picking seleccionando una de las siguientes opciones.

    |Opción|Descripción|
    |-|-|
    |Máx. Nº de líneas de picking|Crea los documentos de picking que tienen emplear no más del número de líneas especificado en cada documento.|
    |Máx. Nº de doc. origen picking|Crea documentos de picking que, cada uno, abarca no más del número de documentos de origen especificado.|
    |Id. usuario asignado|Crea los documentos de picking sólo para las líneas de la hoja de cálculo que se asignan al empleado seleccionado de almacén.|
    |Mét. clasif. para líns. picking|Seleccione una de las opciones disponibles para ordenar las líneas en el documento de picking creado.|
    |Define filtro div. bulto|Oculta líneas de picking de división de bulto intermedias cuando una unidad de medida grande se convierte en una más pequeña y con el picking realizado completamente.|
    |No rellene cdad. a manipular|Deja el campo Cdad. a manipular vacío en las líneas de picking creadas.|
    |Imprim. picking|Imprime los documentos de picking cuando se crean. También puede imprimir de los documentos de picking creados.|

8. Elija **Aceptar**. [!INCLUDE [prod_short](includes/prod_short.md)] creará el picking de acuerdo con sus selecciones.  

## Para realizar un picking de los envíos de almacén

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Picking almacén** y luego elija el enlace relacionado.  

    Si tiene que trabajar con un picking determinado, seleccione el picking de la lista o filtre la lista para encontrar los pickings que se le han asignado específicamente. Abra la ficha de la tarjeta.  
2. Si el campo **Id. usuario asignado** está vacío, escriba el id. para identificarse si es necesario.  
3. Elija los productos.  

    Si el almacén está configurado para utilizar ubicaciones, las ubicaciones genéricas de los productos se utilizan para sugerir de dónde tomar los productos. Las instrucciones contienen como mínimo dos líneas independientes para las acciones Traer y Colocar.  

    Si el almacén está configurado para utilizar ubicación y picking directos, el ranking de ubicación se utiliza para calcular las mejores ubicaciones de las que hacer picking. Esas ubicaciones se sugieren en las líneas de picking. Las instrucciones contienen como mínimo dos líneas independientes para las acciones Traer y Colocar.  

    * La primera línea, con **Traer** en el campo **Tipo acción**, indica dónde están colocados los productos en el área de picking. Si va a enviar un gran número de productos en una misma línea de envío, es posible que tenga que realizar el picking de los productos en varias ubicaciones, de modo que haya una línea Traer para cada ubicación.
    * La siguiente línea, con **Colocar** en el campo **Tipo acción**, muestra dónde debe colocar los productos en el almacén. En esta línea no puede cambiar la zona y ubicación.

    > [!NOTE]
    > Si es necesario realizar el picking o colocar los productos para otra línea en varias ubicaciones porque la ubicación designada está completa, por ejemplo, utilice la acción **Dividir línea** en la ficha desplegable **Líneas**. La acción crea una línea la cantidad restante que se debe administrar.

4. Después de terminar el picking y colocar los productos en el área de o ubicación de envío, elija la acción **Registrar picking**.  

Ahora puede llevar los artículos al muelle de envío y registrar el envío, incluido el documento de origen relacionado, en la página **Envío de almacén**. Obtenga más información en [Enviar productos](warehouse-how-ship-items.md).

## Consulte también

- [Información general de la administración de almacenes](design-details-warehouse-management.md)
- [Gestionar inventario](inventory-manage-inventory.md)  
- [Configuración de Warehouse Management](warehouse-setup-warehouse.md)     
- [Administración de ensamblados](assembly-assemble-items.md)    
- [Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
