---
title: 'Procedimiento: configure almacenes básicos con áreas de operaciones | Documentos de Microsoft'
description: Si las áreas de operaciones internas, como producción o ensamblado, existen en configuraciones de almacén básico donde las ubicaciones utilizan el campo de instalación de **Ubicac. obligatoria** y los campos de configuración **Picking requerido** y **Ubicación requerida**, puede utilizar tres documentos de almacén básico siguientes para registrar sus actividades de almacén para las áreas de operaciones internas.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 8ce9a861812294de642939d3111e40dc9f7052f6
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "3789105"
---
# <a name="set-up-basic-warehouses-with-operations-areas"></a>Configurar almacenes básicos con áreas de operaciones
Si las áreas de operaciones internas, como producción o ensamblado, existen en configuraciones de almacén básico donde las ubicaciones utilizan el campo de instalación de **Ubicac. obligatoria** y los campos de configuración **Picking requerido** y **Ubicación requerida**, puede utilizar los documentos de almacén básico siguientes para registrar sus actividades de almacén para las áreas de operaciones internas:  

- Página **Lista movs. inventario**.  
- Página **Lista picking invent.**  
- Página **Lista ubic. inventario**.

> [!NOTE]
> A pesar de que las configuraciones se denominan **Picking requerido** y **Ubicación requerida**, todavía puede registrar recibos y envíos directamente desde los documentos empresariales de origen en las ubicaciones donde se selecciona estas casillas de verificación.  

Para utilizar estas páginas con las operaciones internas, por ejemplo para realizar el picking y para mover a los componentes a producción, debe hacer alguno o todos los pasos de instalación siguientes dependiendo del control que necesite:  

- Habilitar el picking de existencias, el movimiento, y los documentos de ubicación.  
- Defina las estructuras de ubicación predeterminada para los componentes y los productos finales que fluirán a o desde los recursos de la operación.  
- Cree ubicaciones "de y a" que se dediquen a recursos específicos de la operación para evitar que realizar picking de artículos para los documentos de salida.

Los códigos de ubicación que se configuran en las fichas de almacén sólo definen un flujo de almacén predeterminado para algunas actividades determinadas, como componentes de un departamento de ensamblado. Existe otra funcionalidad para asegurarse de que los productos no están disponibles para otras actividades cuando se colocan en una ubicación concreta. Para obtener más información, consulte [Crear ubicaciones de componentes dedicadas](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md#to-create-dedicated-component-bins).

Los procedimientos siguientes se basan en las actividades del almacén básico de creación alrededor de un área de producción. Los pasos son parecidos para otras áreas de operación, como ensamblado, gestión del servicio y proyectos.  

> [!NOTE]  
>  En el procedimiento siguiente, el campo de configuración **Ubicac. obligatoria** en las fichas de almacén está seleccionado como condición previa porque se considera como la base de cualquier nivel de gestión de almacén.  

## <a name="to-enable-inventory-documents-for-internal-operation-activities"></a>Para activar los documentos del inventario para las actividades de la operación interna  
1.  Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Almacenes** y, a continuación, elija el enlace relacionado.
2. Abra la ficha de almacén que desea configurar.  
3.  En la ficha desplegable **Almacén**, seleccione la casilla **Ubicación requerida** para indicar que, cuando un documento de entrada o de origen interno con un código de ubicación emitido, se puede crear una ubicación de inventario o un documento de movimiento de inventario.  
4.  Seleccione la casilla **Ubicación requerida** para indicar que, cuando se crea un documento de salida o de origen interno con un código de ubicación emitido, debe crearse un pick de inventario o un documento de movimiento de inventario.  

## <a name="to-define-a-default-bin-structure-in-the-production-area"></a>Para definir una estructura de ubicación predeterminada en el área de producción  
1.  Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Almacenes** y, a continuación, elija el enlace relacionado.
2. Abra el almacén que desea configurar.  
3.  En la ficha desplegable **Ubicaciones**, en el campo **Abre cód. ubic. control planta**, introduzca el código de la ubicación en la área de producción con todos los componentes de los que el operador de máquina pueda consumir sin solicitar una actividad de almacén que los lleve a la ubicación. Los productos que se colocan en esta ubicación se suelen configurar para su registro automático o baja. Esto significa que el campo **Método de baja** contiene **Adelante** o **Atrás**.  
4. En el campo **Cód. ubic. para producción**, introduzca el código de la ubicación en el área de producción en la que se colocan por defecto componentes que se extraen para producción en este almacén antes de que se puedan consumir. Los productos que se colocan en esta ubicación se suelen configurar para el registro manual del consumo. Esto significa que el campo de **Método de baja** contiene **Manual** o **Pick + Adelante** o **Pick + Atrás** para picking y movimientos de inventario de almacén.  

    > [!NOTE]  
    >  Cuando se utiliza el picking de inventario, el campo **Cód. ubicación** de la línea de componente de orden de producción define la ubicación *traer* desde donde los componentes disminuyen cuando se registra el consumo. Al utilizar movimientos de inventario, el campo **Código de ubicación** en las líneas de componente de orden de producción define la ubicación *apartado* en el área de la operación donde el empleado de almacén debe colocar los componentes.  

5. En la ficha desplegable **Ubicaciones**, en el campo de **Cód. ubic. desde producción**, introduzca el código de la ubicación en la área de producción de donde se toman los productos finales terminados de forma predeterminada cuando el proceso implica una actividad de almacén. En las configuraciones básicas de almacén se registra la actividad como una ubicación o un movimiento de inventario.  

Las líneas de componente del pedido de producción con ese código predeterminado de almacén requieren que se coloquen allí los componentes vaciados hacia adelante. Sin embargo, hasta que los componentes se consumen en esa ubicación, se puede hacer picking de otras demandas de componentes o se los puede consumir de esa ubicación porque aún se los considera contenidos de ubicación disponibles. Para garantizar que el contenido de la ubicación está disponible sólo para la demanda de componente que utiliza esa ubicación para producción, debe seleccionar el campo **Dedicado** de la línea para ese código de ubicación en la página **Ubicaciones** a la que se accede desde la ficha de almacén.

Este organigrama muestra cómo se rellena el campo de **Cód. ubicación** en las líneas del componente de la orden de producción según la configuración.  

![Diagrama de flujo de ubicación](media/binflow.png "BinFlow")    

## <a name="to-define-a-default-bin-structure-in-the-assembly-area"></a>Para definir una estructura de ubicación predeterminada en el área de ensamblado
Los componentes para los pedidos de ensamblado no se seleccionar o registrar con picking de inventario. En lugar de eso, use la página **Movimiento inventario**. Para obtener más información, consulte [Mover componentes a un área de operaciones en el almacenamiento básico](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).

Cuando las cantidades de la línea de picking y envío que se ensamblan para el pedido, debe seguir ciertas reglas al crear las líneas de picking de inventario. Para obtener más información, vea la sección "Tratamiento de productos ensamblar para pedido en los picking de inventario" en [Realizar picking de productos con picking inventario](warehouse-how-to-pick-items-with-inventory-picks.md).

Para obtener más información, consulte [Gestión de ensamblado](assembly-assemble-items.md).

### <a name="to-set-up-that-an-inventory-movement-is-automatically-created-when-the-inventory-pick-for-the-assembly-item-is-created"></a>Para configurar que un movimiento de inventario se cree automáticamente cuando el picking de inventario para el producto del ensamblado se crea
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Conf. ensamblado** y luego elija el enlace relacionado.
2. Seleccione la casilla **Crear movimientos automáticamente**.

### <a name="to-set-up-the-bin-in-the-assembly-area-where-components-are-placed-by-default-before-they-can-be-consumed-in-assembly"></a>Para configurar la ubicación en el área de ensamblado en la que se colocan, de forma predeterminada, los componentes antes de que se puedan consumir en el ensamblado
El valor de este campo se inserta automáticamente en el campo **Cod. ubicación** de las líneas de pedido de ensamblado cuando esta ubicación se introduce en el campo **Cod. almacén** el campo de la línea de pedido de ensamblado.

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Almacenes** y, a continuación, elija el enlace relacionado.
2. Abra el almacén que desea configurar.
3. Rellene el campo **Cód. ubic. para ensamblado**.

### <a name="to-set-up-the-bin-in-the-assembly-area-where-finished-assembly-items-are-posted-to-when-they-are-assembled-to-stock"></a>Para configurar la ubicación en el área de ensamblado donde los elementos del ensamblado terminados se registran cuando se ensamblan para stock
El valor de este campo se inserta automáticamente en el campo **Cod. ubicación** de los encabezados de pedido de ensamblado cuando este código de ubicación se rellena en el campo **Cod. almacén** el campo del encabezado de pedido de ensamblado.

Los códigos de ubicación que se configuran en las fichas de almacén definen un flujo de almacén predeterminado para actividades de almacén específicas, como el consumo de componentes de un área de ensamblado. Existe otra funcionalidad para asegurarse de que los productos no están disponibles para otras actividades cuando se colocan en una ubicación predeterminada.

> [!NOTE]
> Esta configuración sólo es posible para las ubicaciones donde el campo Ubicac. obligatoria está seleccionado.

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Almacenes** y, a continuación, elija el enlace relacionado.
2. Abra el almacén que desea configurar.
3. Rellene el campo **Cód. ubic. desde ensamblado**.

### <a name="to-set-up-the-bin-where-finished-assembly-items-are-posted-to-when-they-are-assembled-to-a-linked-sales-order"></a>Para configurar la ubicación en la que los elementos del ensamblado terminados se registran cuando se ensamblan para un pedido de venta asociado
Desde esta ubicación, los productos de ensamblado se envían inmediatamente, mediante un picking de inventario, para cumplir el pedido de venta.

> [!NOTE]
> Este campo no se puede utilizar si el almacén está configurado para utilizar ubicación y picking directos.

El código de ubicación se copia de la línea de pedido de venta en la cabecera del pedido de ensamblado para comunicar a los empleados de ensamblado dónde ubicar la salida para alistarla para el envío. También se copia en la línea de picking de inventario para comunicar a los empleados de almacén dónde tomarla para enviarla.

> [!NOTE]
> La ubicación de envío de ensamblar para pedido está siempre vacía. Cuando se registra una línea de venta ensamblar para pedido, el contenido de la ubicación se ajusta primero positivamente a la salida de ensamblado. Inmediatamente después, se ajusta negativamente con la cantidad enviada.

El valor de este campo se inserta automáticamente en el campo Código ubicación de las líneas de pedido de venta que contienen una cantidad en el campo **Cdad. en ensamblar para pedido** o si el producto que se va a vender tiene **Ensamblar para pedido** en el campo **Sistema reposición**.

Si **Cód. ubic. ens.contra-pedido** está en blanco, el campo **Cód. ubic. desde ensamblado** se utiliza en su lugar. Si ambos campos de configuración están en blanco, tanto la última ubicación con el contenido se utiliza en el campo **Cod. ubicación** de las líneas de pedido de venta.

El mismo código de ubicación a su vez se copia al campo **Cod. ubicación** de la línea de picking de inventario que controla el envío de la cantidad de ensamblar para pedido. Para obtener más información, vea la sección "Tratamiento de productos ensamblar para pedido en los picking de inventario" en [Realizar picking de productos con picking inventario](warehouse-how-to-pick-items-with-inventory-picks.md).

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Almacenes** y, a continuación, elija el enlace relacionado.
2. Abra el almacén que desea configurar.
3. Rellene el campo **Cód. ubic. ens.contra-pedido**.

## <a name="to-create-dedicated-component-bins"></a>Para crear las ubicaciones de componentes dedicados
Puede especificar que las cantidades en una ubicación estén protegidas de picking para otras demandas que la demanda de su propósito actual.

Las cantidades de las ubicaciones dedicadas todavía pueden reservarse. Por consiguiente, las cantidades de las ubicaciones dedicadas se incluyen en el campo **Cdad. disponible total** de la página **Reservas**.

Por ejemplo, en un centro de trabajo se establece un código de ubicación en el campo **Cód. ubic. para producción**. Las líneas de componente del pedido de producción con ese código de almacén requieren que se coloquen allí los componentes vaciados hacia adelante. Sin embargo, hasta que los componentes se consumen en esa ubicación, se puede hacer picking de otras demandas de componentes o se los puede consumir de esa ubicación porque aún se los considera contenidos de ubicación disponibles. Para garantizar que el contenido de la ubicación está disponible sólo para la demanda de componente que utiliza esa ubicación para producción, debe seleccionar el campo **Dedicado** de la línea para ese código de ubicación en la página **Ubicaciones** a la que se accede desde la ficha de almacén.

La fabricación de una ubicación dedicada proporciona una funcionalidad similar al uso de tipos de ubicaciones, que sólo está disponible en la gestión avanzada de almacén. Para obtener más información, consulte [Configurar tipos de ubicaciones](warehouse-how-to-set-up-bin-types.md).

> [!Caution]
> Los productos de las ubicaciones dedicadas no se protegen cuando se les ha realizado el picking y se los consume como componentes de producción con la página Picking de inventario.

1.  Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Almacenes** y, a continuación, elija el enlace relacionado. Seleccione el almacén que desea actualizar.  
2.  Seleccione la acción **Ubicaciones**.  
3.  Seleccione el campo **Dedicado** para cada ubicación que desee usar exclusivamente para determinadas operaciones internas y donde desee reservar cantidades para esa operación una vez colocadas allí.  

> [!NOTE]  
>  La ubicación debe estar vacía antes de poder seleccionar o borrar el campo **Dedicado**.

## <a name="see-also"></a>Consulte también  
[Gestión almacén](warehouse-manage-warehouse.md)  
[Grupos contables inventario](inventory-manage-inventory.md)  
[Configuración de la gestión del almacén](warehouse-setup-warehouse.md)     
[Gestión de ensamblaje](assembly-assemble-items.md)    
[Detalles de diseño: Gestión de almacén](design-details-warehouse-management.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
