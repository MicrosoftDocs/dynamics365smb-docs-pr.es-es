---
title: Realizar el picking en operaciones internas en configuraciones avanzadas de almacén
description: 'Si sus ubicaciones utilizan el picking y el envío, seleccione componentes para las actividades de producción, montaje y trabajo en la página Picking en almacén.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: null
ms.date: 04/23/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# Realizar picking para producción, ensamblado o proyectos en una configuración avanzada de almacén

La forma de realizar el picking de componentes para producción, proyectos u órdenes de ensamblado depende de la configuración del almacén. Obtenga más información en [Configuración de Warehouse Management](warehouse-setup-warehouse.md).

En una configuración de almacén avanzada para el flujo de salida (picking), active los botones de alternancia **Picking requerido** y **Envío requerido** en la página **Ficha almacén** para el almacén.

Cuando el almacén está configurado para requerir los procesos de picking de almacén y envío de almacén, utilice documentos de picking de almacén para crear y procesar la información antes de registrar el uso o el consumo de componentes.  

A continuación, puede crear los documentos de almacén desde cero. Los picking son parte de un flujo de trabajo en el que una persona que está procesando un pedido los crea de forma automática, o el empleado del almacén los crea de forma automática:

- De manera forzada, cuando utiliza la acción **Crear picking** en la página **Pedido de producción**, **Pedido de ensamblado** y **Ficha de proyecto**. Seleccione las líneas para picking y prepare los picking mediante la especificación, por ejemplo, de las ubicaciones de las que se tomarán, las ubicaciones en las que se colocarán y la cantidad de unidades que se manipularán. Las ubicaciones se pueden predefinir para la ubicación del almacén o el recurso.
- De manera forzada, donde libera **Pedido de producción**, **Pedido de ensamblado** y **Ficha de proyecto** al almacén haciendo que los productos estén disponibles para picking. A continuación, en la página **Hoja trabajo picking**, los empleados del almacén pueden usar la acción **Traer documentos almacén** para obtener los pickings asignados.

Para seleccionar o mover componentes para documentos de origen en forma de extracción, debe liberar el documento de origen para que esté listo para picking. Lance los documentos de origen para las operaciones internas de las siguientes formas.  

|Documento origen|Método de lanzamiento|  
|---------------------|--------------------|  
|Orden producción|Cambie el estado del pedido a Lanzado o cree un pedido de producción lanzado de inmediato.|  
|Pedido de ensamblado|Cambie el estado a Lanzada.|
|Proyectos | Cambie el estado a Abierto o cree un trabajo con el estado Abierto de inmediato.|  

## Producción

Utilice documentos de **Picking almacén** para seleccionar componentes de producción en el flujo a producción.

Para un almacén que usa ubicaciones para mover productos a ubicaciones de aprovisionamiento manual, puede usar los siguientes métodos:

* Para un almacén que utiliza almacenaje y picking dirigidos, siga los pasos del artículo [Mover productos en configuraciones avanzadas de almacén](warehouse-how-to-move-items-in-advanced-warehousing.md).
* Para otros almacenes, siga las instrucciones del artículo [Mover productos internos en configuraciones básicas de almacén](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md).

## Ensamblado  

Utilice los documentos **Picking almacén** para mover componentes del ensamblado al área de ensamblado.

[!INCLUDE [prod_short](includes/prod_short.md)] es compatible con los tipos ensamblar para stock y ensamblar para pedido de los flujos de ensamblado. Para obtener más información sobre el ensamblado para pedido en el flujo de almacén saliente, vaya a [Tratamiento de productos ensamblar para pedido en los envíos de almacén](warehouse-how-ship-items.md#handling-assemble-to-order-items-in-warehouse-shipments).

## Administración de proyectos  

Utilice documentos de **Picking almacén** para seleccionar componentes de proyecto en el flujo a la administración de proyectos.

> [!NOTE]
> Se agregó la capacidad de seleccionar componentes para las líneas de planificación de proyectos a [!INCLUDE[d365fin](includes/d365fin_md.md)] en el lanzamiento de versiones 2 de 2022. Para empezar a usar la capacidad, un administrador debe activar **Actualización de característica: habilitar el picking de almacén e inventario de los proyectos** en la página **Administración de características**.
>
> Los trabajos no admiten configuraciones avanzadas en las que el botón de alternancia **Pick. directo de almacén** está activado.

## Verifique si los artículos están disponibles para ser recogidos

[!INCLUDE [inventory-availability-overview](includes/inventory-availability-overview.md)]

## Para crear documentos de picking de forma masiva con la hoja de trabajo de picking

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Hoja trabajo picking** y luego elija el enlace relacionado.  

2. Seleccione la acción **Traer documentos almacén**.  

    La lista muestra la producción liberada, los proyectos y los pedidos de ensamblado que se han enviado a la función de picking. Los pedidos incluyen aquellos para los que ya se han creado instrucciones de picking. Los documentos con líneas de picking que ya se han preparado y registrado no se muestran en esta lista.  
3. Seleccione los pedidos para los que desea preparar el picking.

    > [!NOTE]  
    > Si selecciona un documento que ya tiene instrucciones para todas sus líneas, [!INCLUDE [prod_short](includes/prod_short.md)] le informa de que no hay nada que gestionar. Para combinar las instrucciones de picking de almacén ya creadas en una instrucción de picking, elimine primero los picking de almacén individuales.

4. Rellene el campo **Método ordenación** para ordenar las líneas de la forma que prefiera.  

    > [!NOTE]  
    > La forma en que se ordenan las líneas en la hoja de trabajo no se traslada automáticamente a la instrucción de picking. Sin embargo, las mismas herramientas de clasificación están disponibles, junto con la clasificación por ubicación. Puede recrear fácilmente el pedido de las líneas que planifica en la hoja de trabajo cuando se crean las instrucciones de picking o al ordenar las instrucciones de picking.

5. Rellene el campo **Cdad. a manipular**. Seleccione la acción **Rellenar cdad. manip. autom.** o rellene los campos manualmente.  

    La página muestra las cantidades disponibles en contenedores de cross-dock, lo cual es útil para planificar asignaciones de trabajo en situaciones de cross-docking. [!INCLUDE[prod_short](includes/prod_short.md)] siempre propondrá una selección de un contenedor de cross-dock primero.

6. Si es necesario, edite las líneas manualmente. También puede eliminar algunas líneas para realizar un picking más eficaz. Por ejemplo, si hay varias líneas con productos en ubicaciones de tránsito directo, es posible que desee realizar un picking de todas las líneas. Se seleccionan los productos de tránsito directo junto con el resto de los productos del documento de origen, y las ubicaciones de tránsito directo tienen espacio para la entrada de más productos.

    > [!NOTE]  
    >  Las líneas solo se eliminarán de esta hoja de trabajo, no de la lista de selección de picking.  

7. Elija la acción **Crear picking**. Se abrirá la página **Crear picking** en la que puede agregar más información al picking.  

    Especifique cómo se combinan las líneas de picking en los documentos de picking creados seleccionando una de las siguientes opciones.  

    |Opción|Descripción|
    |-|-|
    |Por almacén Documento|Crea los documentos de picking independientes para las líneas de la hoja de cálculo con el mismo documento de origen de almacén.|
    |Por Cli./Prov./Alm.|Crea documentos de picking separados para cada cliente (trabajos)|
    |Por prod.|Crea los documentos de picking independientes para cada producto en la hoja de cálculo de picking.|
    |Por Desde zona|Crea los documentos de picking independientes para cada zona de la que trae los productos.|
    |Por ubicación|Crea los documentos de picking independientes para cada ubicación de la que trae los productos.|
    |Por fecha vto.|Crea los documentos de picking independientes para los documentos de origen con la misma fecha de vencimiento.|

    Especifique cómo se crean los documentos de picking seleccionando una de las siguientes opciones.  

    |Opción|Descripción|
    |-|-|
    |Máx. Nº de líneas de picking|Crea los documentos de picking que tienen emplear no más del número de líneas especificado en cada documento.|
    |Máx. Nº de doc. origen picking|Crea documentos de picking que abarcan hasta el número de documentos de origen especificado.|
    |Id. usuario asignado|Crea los documentos de picking sólo para las líneas de la hoja de cálculo que se asignan al empleado seleccionado de almacén.|
    |Mét. clasif. para líns. picking|Seleccione una de las opciones disponibles para ordenar las líneas en el documento de picking creado.|
    |Define filtro div. bulto|Oculta líneas de picking de división de bulto intermedias cuando una unidad de medida grande se convierte en una más pequeña y con el picking realizado.|
    |No rellene cdad. a manipular|Deja el campo **Cdad. a manipular** vacío en las líneas de picking creadas.|
    |Imprim. picking|Imprime los documentos de picking cuando se crean. También puede imprimir de los documentos de picking creados.|

8. Elija el botón **Aceptar**.  

## Para seleccionar pedidos para un pedido de producción, pedido de ensamblado y trabajo

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Picking** y luego elija el enlace relacionado.  

    Si tiene que trabajar con un picking determinado, seleccione el picking de la lista o filtre la lista para encontrar los pickings que se le han asignado. Abra la ficha de la tarjeta.  
2. Si el campo **Id. usuario asignado** está vacío, escriba el id. para identificarse si es necesario.  
3. Elija los productos.  

    Si el almacén está configurado para utilizar ubicaciones, las ubicaciones genéricas de los productos se utilizan para sugerir de dónde tomar los productos. Las instrucciones contienen como mínimo dos líneas independientes para las acciones Traer y Colocar.  

    Las áreas de operación, como los talleres de producción, pueden tener un contenedor predeterminado para los componentes que requieren. Si es así, el código de ubicación predeterminado se agrega al documento de selección de almacén para indicar dónde colocar los artículos. Para obtener más información, consulte la información sobre herramientas de los campos **Cód. ubic. para producción**, **Cód. ubic. para ensamblado** y **Hasta-cód. hueco**.

    Si el almacén está configurado para utilizar ubicación y picking directos, el ranking de ubicación se utiliza para calcular las mejores ubicaciones de las que hacer picking. Esas ubicaciones se sugieren en las líneas de picking. Las instrucciones contienen como mínimo dos líneas independientes para las acciones Traer y Colocar.  

    * La primera línea, con **Traer** en el campo **Tipo acción**, indica dónde están colocados los productos en el área de picking. Si va a enviar un gran número de productos en una misma línea de envío, es posible que tenga que realizar el picking de los productos en varias ubicaciones, de modo que haya una línea Traer para cada ubicación.
    * La siguiente línea, con **Colocar** en el campo **Tipo acción**, muestra dónde debe colocar los productos en el almacén. En esta línea no puede cambiar la zona y ubicación.

    > [!NOTE]
    > Si es necesario realizar el picking o colocar los productos para otra línea en varias ubicaciones porque la ubicación designada está completa, por ejemplo, utilice la acción **Dividir línea** en la ficha desplegable **Líneas**. La acción crea una línea la cantidad restante que se debe administrar.

      Puede ordenar las líneas de picking por varios criterios, por ejemplo, por producto, número de estante o fecha de vencimiento. La clasificación puede ayudar a optimizar el proceso de almacenamiento, por ejemplo:

    * Si las líneas Traer y Colocar de cada línea de envío no están una a continuación de otra y desea que lo estén, puede ordenar las líneas seleccionando **Producto** en el campo **Método ordenación**.  
    * Si las clasificaciones de almacenamientos reflejan el diseño físico del almacén, utilice el método de clasificación **Clasificación de ubicaciones** para organizar el trabajo en torno a los almacenes de las ubicaciones.

  > [!NOTE]  
  > Las líneas se ordenan en orden ascendente por los criterios seleccionados. Si ordena por documento, la ordenación se realiza primero por tipo de documento según el campo **Documento de origen de la actividad de almacén**. Si ordena por destino de envío, la clasificación se realiza primero por tipo de destino según el campo **Tipo de destino de almacén**.

4. Después de realizar el picking y colocar los productos en el área de producción, ensamblado o trabajo, elija la acción **Registrar picking**.  

    Ahora puede llevar los productos al área correspondiente y contabilizar la utilización o el consumo de los componentes del picking mediante la contabilización del diario de consumo, el pedido de ensamblado o el diario de proyecto. Los siguientes artículos ofrecen más información:

    * [Registrar el consumo y la salida de una línea de orden de producción lanzada](production-how-to-register-consumption-and-output.md)
    * [Ensamblar productos](assembly-how-to-assemble-items.md)
    * [Registrar el consumo o uso para proyectos](projects-how-record-job-usage.md)

## Baja de componentes de producción en una configuración de almacén avanzada

Los métodos de baja afectan al flujo de componentes en producción. Obtenga más información en [Bajar componentes según la salida de la operación](production-how-to-flush-components-according-to-operation-output.md). Según el método de baja seleccionado, puede realizar el picking de componentes para la producción de las siguientes maneras:

* Utilice un documento de **Picking almacén** para registrar la selección de productos que usan el método de vaciado **Manual**. Debe registrar el consumo por separado. Obtenga más información en [Registrar consumibles de producción por lotes](production-how-to-post-consumption.md).
* Utilice un documento de **Picking almacén** para registrar el picking para productos que usan el método de baja **Pick + Adelante** y **Pick + Atrás**. El consumo de los componentes se produce automáticamente cuando cambie el estado de la orden de fabricación o al iniciar o finalizar una operación. Todos los componentes necesarios deben estar disponibles. De lo contrario, el registro del consumo de baja se detiene para ese componente.
* Use un documento de **Movimiento de almacén** sin una referencia a un documento de origen u otras formas de registrar el movimiento de componentes que usan el método de baja **Adelante** o **Atrás** . Los componentes se consumen automáticamente al cambiar de estado la orden de fabricación o al iniciar o finalizar una operación. Todos los componentes necesarios deben estar disponibles. De lo contrario, el registro del consumo de baja se detiene para ese componente. Obtenga más información en [Desplazar productos](warehouse-move-items.md).

### Ejemplo:

Tiene un pedido de fabricación de 15 unidades del producto SP-SCM1004. Algunos de los elementos de la lista de componentes deben eliminarse manualmente en un diario de consumo. Se puede realizar el picking y la baja de otros productos automáticamente mediante el método de baja **Pick + Atrás**.  

En los pasos siguientes se describen las acciones correspondientes para distintas personas y la respuesta relacionada:  

1. El supervisor de planta lanza la orden de producción. Los productos con el método de baja **Anticipada** y sin conexión de ruta se deducen de la ubicación de aprovisionamiento manual.  
2. El supervisor de planta elige la acción **Crear selección de almacén** en el pedido de producción. Un documento de selección de almacén se crea para seleccionar productos con métodos de baja **Manual**, **Seleccionar + Atrás** y **Seleccionar + Adelante**. Estos productos se colocan en la ubicación para producción.  
3. El administrador de almacén asigna los picking a un empleado de almacén.  
4. El empleado del almacén realiza el picking de los productos de las ubicaciones apropiadas y los coloca en la ubicación Para producción o en la ubicación especificada en el picking del almacén. La ubicación podría ser una ubicación de centro de trabajo o de centro de máquina.
5. El empleado de almacén registra el picking. La cantidad se transfiera de la ubicación de picking a la ubicación de consumo. Se actualiza el campo **Cdad. preparada pedido** de la lista de componentes para todos los productos preparados.

    > [!NOTE]  
    >  Solo se puede consumir la cantidad preparada.  
6. El operador de máquina notifica al director de producción que se han completado los productos finales.
7. El supervisor de planta usa el diario de consumo o de producción para registrar el consumo de los productos componentes que usan el método de baja **Manual**.
8. El supervisor de planta utiliza el diario de salida o el diario de producción para contabilizar la salida. La cantidad de elementos de componentes que utilizan los métodos de baja **Pick + Adelante** o **Pick + Atrás** con vínculos de enrutamiento se deduce de la papelera A producción.
9. El administrador de producción cambia el estado del pedido de producción y modifica el estado a **Terminado**. La cantidad de productos componentes que usan el método de baja **Atrás** se deduce de la ubicación de aprovisionamiento manual y la cantidad de los productos componentes que usan el método de baja **Pick + Atrás** y no se deduce ningún vínculo de enrutamiento de la ubicación para producción.  

En la ilustración siguiente se muestra cuando se rellena el campo **Cód. ubicación** de la lista de componentes según la configuración de la máquina o del centro de trabajo.  

:::image type="content" source="media/binflow.png" alt-text="Descripción general de cuándo y cómo se rellena el campo Código de ubicación.":::

## Componentes de producción bajo pedido (MTO) en una configuración de almacén avanzada

En escenarios en los que un artículo producido consta de materias primas y artículos semiacabados con la política de fabricación establecida en **Fabricación contra pedido**, la selección de almacén para esos componentes semiacabados se agrega a la misma orden de producción con el campo **Código de nivel de planificación** completado. Se espera que los artículos semiacabados estén disponibles para el consumo de inmediato y no requieran selección, por lo que no se incluyen en el documento de selección del almacén. Las selecciones de almacén creadas solo incluyen materias primas para artículos producidos y para artículos semiacabados.

Sin embargo, si hay artículos semiacabados disponibles en stock, el sistema de planificación sugiere que los consuma en lugar de producir la cantidad total. Por ejemplo, un artículo producido requiere cinco componentes semiacabados, pero ya hay tres en stock. En este caso, cinco artículos semiacabados se enumeran en los componentes de la orden de producción, pero solo dos se producen en la misma orden de producción como una línea de orden de producción separada.
Esta configuración no es compatible con las selecciones de almacén y, según la frecuencia, debe cambiar la política de fabricación de dichos artículos semiacabados a **Fabricación contra stock** o divida manualmente la línea de componentes de la orden de producción cuando necesite seleccionar los artículos semiacabados producidos anteriormente.


## Consulte también

- [Gestionar inventario](inventory-manage-inventory.md)  
- [Configuración de Warehouse Management](warehouse-setup-warehouse.md)  
- [Administración de ensamblados](assembly-assemble-items.md)  
- [Información general de la administración de almacenes](design-details-warehouse-management.md)
- [Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
