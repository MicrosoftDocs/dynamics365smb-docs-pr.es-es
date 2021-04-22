---
title: Cómo recibir productos | Documentos de Microsoft
description: Cuando los productos llegan al almacén, se recuperan las líneas del documento de origen que ha activado su recepción. 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 5bf683be6e6d0976464240d08e0546639a46362a
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2021
ms.locfileid: "5771909"
---
# <a name="receive-items"></a>Recibir productos

Cuando los artículos llegan a un almacén que no está configurado para el procesamiento de recibo de almacén, simplemente registre el recibo en el documento comercial relacionado, como una orden de compra, una orden de devolución de ventas o una orden de transferencia de entrada.

Cuando los productos llegan al almacén, se recuperan las líneas del documento de origen que ha activado su recepción. Si tiene ubicaciones, puede aceptar que se rellene la ubicación genérica o, si el producto no se ha utiliza nunca antes en el almacén, rellenar la ubicación donde debe ubicarse el producto.  A continuación, debe rellenar las cantidades de los productos que ha recibido y registrar la recepción.  

## <a name="to-receive-items-with-a-purchase-order"></a>Para recibir productos con un pedido de compra

A continuación se describe cómo recibir productos con un pedido de compra. Los pasos son iguales para las órdenes de devolución de venta y las órdenes de transferencia.  

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Pedidos de compra** y luego elija el enlace relacionado.
2. Abra un pedido de compra existente o cree uno nuevo. Para obtener más información, consulte [Registrar compras](purchasing-how-record-purchases.md).
3. Escriba la cantidad recibida en el campo **Cantidad a recibir**.

  > [!NOTE]
  > Si la cantidad recibida es mayor que la ordenada en el pedido de compra, según el campo **Cantidad**, y el proveedor se ha configurado para permitir recepciones en exceso, entonces usa el campo **En exceso** para administrar la cantidad en exceso. Para más información, vea [Para recibir más artículos de los solicitados](warehouse-how-receive-items.md#to-receive-more-items-than-ordered).

4. Seleccione la acción **Registrar**.

  El valor del campo **Cdad. recibida** se actualiza según corresponde. Si se trata de un recibo parcial, el valor es menor que el valor del campo **Cantidad**.

> [!NOTE]
> Si usa un documento de almacén para contabilizar la recepción, no puede usar la acción **Registrar** en el pedido de compra. En su lugar, un trabajador del almacén ya ha publicado la cantidad del pedido de compra tal como se recibió. Para obtener más información, vea [Para recibir productos con recibo de almacén](warehouse-how-receive-items.md#to-receive-items-with-a-warehouse-receipt).

## <a name="to-receive-items-with-a-warehouse-receipt"></a>Para recibir productos con recibo de almacén

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Recepciones almacén** y luego elija el enlace relacionado.  
2. Seleccione la acción **Nuevo**.  

    Rellene los campos en la ficha desplegable **General**. Al recuperar las líneas del documento de origen, se copia parte de la información en cada línea.  

    Para la configuración de almacén con ubicación y picking directos, si el almacén tiene una zona y ubicación genéricas para los recibos, se rellenarán automáticamente los campos **Cód. zona** y **Cód. ubicación**, pero puede cambiarlos como considere.  

    > [!NOTE]  
    > Si desea recibir productos con códigos de clase de almacén de la ubicación en el campo **Cód. ubicación** de la cabecera de documento, debe eliminar el contenido del campo **Cód. ubicación** en la cabecera antes de recuperar líneas del documento de origen para los productos.  
3. Seleccione la acción **Traer doc. origen**. Se abre la página **Documentos origen**.

    Desde una recepción o un recibo de almacén nuevos o abiertos, puede utilizar la página **Filtros para traer docs. orig.** para recuperar las líneas del documento de origen lanzado que definen la artículos para recibir o enviar.

    1. Elija la acción **Utiliz. filt. para traer docs.**.  
    2. Para configurar un nuevo filtro introduzca un código descriptivo en el campo **Código** y, a continuación, elija la acción **Modificar**.  
    3. Defina el tipo de líneas del documento de origen que desea que recupere el sistema rellenando los campos de filtro correspondientes.  
    4. Seleccione la acción **Ejecutar**.  

    Todas las líneas del documento de origen lanzado que cumplan los criterios del filtro se insertarán en la página **Recibo almacén** desde las que se activó la función del filtro.  

    Las combinaciones de filtros que defina se guardan en la página **Filtros para traer docs. orig.** hasta que la próxima vez que las necesite. Puede crear un número ilimitado de combinaciones de filtros. Puede modificar los criterios en cualquier momento eligiendo la acción **Modificar**.

4. Seleccione los documentos de origen de los que desea recibir productos y, a continuación, haga clic en **Aceptar**.  

    Las líneas de los documentos de origen aparecerán en la página **Recep. almacén**. El campo **Cantidad a recibir** se rellena con la cantidad pendiente de cada línea, pero puede cambiarla según necesite. Si ha eliminado el contenido del campo **Cód. ubicación** de la ficha desplegable **General** antes de traer las líneas, debe rellenar un código de ubicación apropiado en cada línea de recepción.  

    > [!NOTE]  
    >  Para rellenar el campo de **Cdad. para recibir** en todas las líneas con cero, elija la acción **Eliminar cdad. a recibir**. Para rellenarlo de nuevo con la cantidad pendiente, elija la acción **Rellenar cdad. a recibir aut.**  

    > [!NOTE]  
    >  No puede recibir más productos que el número que se muestra en el campo **Cdad. pendiente** de la línea del documento de origen. Para recibir más productos, recupere otro documento de origen que contenga una línea para el producto mediante la función de filtro para traer documentos de origen con el producto.  

5. Registre la recepción de almacén. Los campos de cantidad se actualizan en el documento de origen y se registran los productos como parte de las existencias de la empresa.  

Si utiliza ubicación y picking directos, las líneas de recepción se envían a la función de ubicación de almacén. No es posible hacer picking de los productos, aunque se hayan recibido, hasta que se ubiquen. Los productos recibidos se identifican como existencias disponibles sólo cuando se haya registrado la ubicación.  

Si no utiliza ubicación de almacén, pero sí utiliza ubicaciones, se registra la ubicación de los productos en la ubicación especificada en la línea del documento de origen.  

> [!NOTE]  
> Si utiliza la función **Registrar e imprimir**, se registra la recepción y se imprime la instrucción de ubicación que muestra dónde se colocan los productos en el almacén.  
>
> Si su almacén utiliza ubicación y picking directos, las plantillas de ubicación se usarán para calcular el mejor lugar donde ubicar los productos. A continuación, esto se imprime en la instrucción de ubicación.

## <a name="to-receive-more-items-than-ordered"></a>Para recibir más artículos de los solicitados

Cuando reciba más productos de los que ha pedido, es posible que desee recibirlos en lugar de cancelar el albarán. Por ejemplo, puede ser más barato mantener el exceso en su inventario que devolverlos o su proveedor puede ofrecerle un descuento por conservarlos.

### <a name="to-set-up-over-receipts"></a>Para configurar recibos en exceso

Debe definir un porcentaje según el cual permite que se exceda la cantidad pedida en la recepción. Esto se define en un código de recepción en exceso, que contiene el porcentaje en el campo **Porcentaje de tolerancia de recepción en exceso**. Luego, asigna el código a las tarjetas de los artículos o proveedores pertinentes.  

A continuación, se describe cómo configurar y asignar un código de recepción en exceso a un artículo. Los pasos son parecidos para un proveedor.

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Productos** y luego elija el enlace relacionado.
2. Abra la tarjeta para un artículo que sospecha que a veces se puede entregar con una cantidad mayor que la solicitada.
3. Elija el botón de búsqueda en el campo **Código de recepción en exceso**.
4. Seleccione la acción **Nuevo**.
5. En la página **Códigos de recepción en exceso**, cree una o más líneas nuevas que definan diferentes políticas de recepción en exceso. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].
6. Seleccione una línea y luego seleccione el botón **Aceptar**.

El código de recepción en exceso se asigna al artículo. Cualquier pedido de compra o recibo de almacén para el artículo ahora permite recibir más que la cantidad solicitada de acuerdo con el porcentaje de tolerancia de recepción en exceso especificado.

> [!NOTE]
> Puede configurar un flujo de trabajo de aprobación para requerir que se aprueben las recepciones en exceso antes de que se puedan administrar. En ese caso, debe seleccionar la casilla **Aprobación requerida** en la página **Códigos de recepción en exceso**. Para obtener más información, consulte [Crear flujos de trabajo](across-how-to-create-workflows.md).

### <a name="to-perform-an-over-receipt"></a>Para realizar una recepción en exceso

En las líneas de compra y las líneas de recepción de almacén, el campo **Cantidad de recepción en exceso** se utiliza para registrar las cantidades recibidas en exceso, esto es, cantidades que exceden el valor del campo **Cantidad**, la cantidad pedida.

Cuando administra una recepción en exceso, puede aumentar el valor del campo **Cant. para recibir** con la cantidad realmente recibida. El campo **Cantidad de recepción en exceso** se actualiza para mostrar la cantidad en exceso. Alternativamente, puede introducir la cantidad en exceso en el campo **Cantidad de recepción en exceso**. El campo **Cantidad para recibir** se actualiza para mostrar la cantidad solicitada más la cantidad en exceso. El siguiente procedimiento describe cómo completar el campo **Cantidad para recibir**.  

1. En un pedido de compra o un documento de recibo de almacén donde la cantidad recibida sea mayor que la ordenada, introduzca la cantidad realmente recibida en el campo **Cantidad para recibir**.

    Si el aumento está dentro de la tolerancia especificada por el código de recepción en exceso asignado, el campo **Cantidad de recepción en exceso** se actualiza para mostrar la cantidad en la que se excede el valor del campo **Cantidad**.

    Si el aumento está por encima de la tolerancia especificada, no se permite la recepción en exceso. En ese caso, puede investigar si existe otro código de recepción en exceso que lo permita. De lo contrario, solo se puede recibir la cantidad pedida y la cantidad excedente se debe administrar de otra manera, por ejemplo, devolviéndola al proveedor.

2. Publique la recepción como lo haría con cualquier otra.

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_short.md)] no incluye funcionalidad para iniciar automáticamente la administración financiera de las recepciones en exceso. Debe administrar manualmente esto de acuerdo con el proveedor, por ejemplo, enviando una factura nueva o actualizada.

## <a name="see-related-training-at-microsoft-learn"></a>Consulte Formación relacionada en [Microsoft Learn](/learn/modules/receive-invoice-dynamics-d365-business-central/index)

## <a name="see-also"></a>Consulte también

[Gestión de almacenes](warehouse-manage-warehouse.md)  
[Inventario](inventory-manage-inventory.md)  
[Configuración de la gestión del almacén](warehouse-setup-warehouse.md)  
[Gestión de ensamblaje](assembly-assemble-items.md)  
[Detalles de diseño: Gestión de almacén](design-details-warehouse-management.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]