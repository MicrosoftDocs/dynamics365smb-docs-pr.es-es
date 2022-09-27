---
title: Enviar productos
description: Este artículo describe cómo enviar productos desde su almacén según la configuración de su almacén para el procesamiento del envío.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 7335, 7337, 7339, 7340, 7341, 7362, 9008
ms.date: 09/02/2022
ms.author: edupont
ms.openlocfilehash: b66a0a0a4cad12c4f41c53569b0007c51e846de7
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/19/2022
ms.locfileid: "9531221"
---
# <a name="ship-items"></a>Enviar productos

Cuando envíe artículos de un almacén que no está configurado para el procesamiento de envío de almacén, simplemente registre el envío en el documento de negocio relacionado, como un pedido de cliente, una orden de servicio, una orden de devolución de compra o una orden de transferencia de salida.

Cuando envía productos de un almacén que está configurado para realizar el proceso de envío de almacén, puede enviar productos solo basándose en los documentos de origen que otras unidades de la empresa han enviado al almacén para realizar una acción.

> [!NOTE]
> Si el almacén utiliza tránsito directo y ubicaciones, para cada línea, puede ver la cantidad de productos colocados en las ubicaciones de tránsito directo. La aplicación calcula estas cantidades automáticamente cada vez que se actualicen los campos en el envío. Si son los productos que se incluyen en el envío que está preparando, puede crear un picking de todas las líneas y, a continuación, completar el envío. Obtenga más información en [Productos de tránsito directo](warehouse-how-to-cross-dock-items.md).

## <a name="ship-items-with-a-sales-order"></a>Enviar productos con un pedido de ventas

Las instrucciones siguientes describen cómo enviar productos de un pedido de venta. Los pasos son iguales para las órdenes de devolución de compra, las órdenes de servicio y las órdenes de transferencia de salida.  

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pedidos de venta** y, a continuación, elija el vínculo relacionado.
2. Abra un pedido de venta existente o cree uno nuevo. Obtenga más información en [Vender productos](sales-how-sell-products.md).
3. Escriba la cantidad enviada en el campo **Cantidad a enviar**.

    El valor del campo **Cdad. enviada** se actualiza según corresponde. Si se trata de un envío parcial, el valor es menor que el valor del campo **Cantidad**. Obtenga más información en [Procesar envíos parciales](sales-how-send-partial-shipments.md).
4. Seleccione la acción **Registrar**.

> [!NOTE]
> Si su organización no utiliza pedidos de ventas, cuando contabilice la factura de ventas, [!INCLUDE [prod_short](includes/prod_short.md)] asume que ha enviado la cantidad completa. Si esto entra en conflicto con el funcionamiento de su organización, le recomendamos que utilice pedidos de ventas y registre envíos como se explica en este artículo.

## <a name="ship-items-with-a-warehouse-shipment"></a>Enviar productos con envío de almacén

Primero cree un documento de envío de un documento de origen de negocio. A continuación, seleccione los productos especificados para el envío.

### <a name="create-a-warehouse-shipment"></a>Crear un envío de almacén

Normalmente, el empleado responsable de los envíos crea un envío de almacén. El siguiente procedimiento describe cómo crear el envío manualmente en la versión predeterminada de [!INCLUDE[prod_short](includes/prod_short.md)]. Sin embargo, es posible que su organización haya automatizado parte del proceso, por ejemplo, con el uso de escáneres portátiles o montados respaldados por proveedores externos.  

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Envíos de almacén** y luego elija el enlace relacionado.  
2. Elija **Nuevo**.  

    Rellene los campos en la ficha desplegable **General**. Al recuperar las líneas del documento de origen, se copia parte de la información en cada línea.  

    Para una almacén configurado con ubicación y picking directos, si el almacén tiene una zona y ubicación genéricas para los envíos, se rellenarán automáticamente los campos **Cód. zona** y **Cód. ubicación**, pero puede cambiarlos como considere.  

    > [!NOTE]  
    > Si desea enviar productos con códigos de clase de almacén de la ubicación en el campo **Cód. ubicación** de la cabecera de documento, debe eliminar el contenido del campo **Cód. ubicación** en la cabecera antes de recuperar líneas del documento de origen para los productos.  
3. Seleccione la acción **Traer doc. origen**. Se abre la página **Documentos origen**.

    Desde una recepción o un envío de almacén nuevos o abiertos, puede utilizar la página **Filtros para traer docs. orig.** para recuperar las líneas del documento de origen lanzado que definen la artículos para recibir o enviar.

    1. Elija la acción **Utiliz. filt. para traer docs.**.  
    2. Para configurar un nuevo filtro introduzca un código descriptivo en el campo **Código** y, a continuación, elija la acción **Modificar**.  
    3. Defina el tipo de líneas del documento de origen que desea que recupere el sistema rellenando los campos de filtro correspondientes.  
    4. Seleccione la acción **Ejecutar**.  

    Todas las líneas del documento de origen lanzado que cumplan los criterios del filtro se insertarán en la página **Envío almacén** desde las que se activó la función del filtro.  

    Las combinaciones de filtros que defina se guardan en la página **Filtros para traer docs. orig.** hasta que la próxima vez que las necesite. Puede crear un número ilimitado de combinaciones de filtros. Puede modificar los criterios en cualquier momento eligiendo la acción **Modificar**.

4. Seleccione los documentos de origen para los que desea enviar productos y, a continuación, elija **Aceptar**.  

Las líneas de los documentos de origen aparecerán en la página **Envío almacén**. El campo **Cantidad a enviar** se rellena con la cantidad pendiente de cada línea, pero puede cambiarla según necesite. Si ha eliminado el contenido del campo **Cód. ubicación** de la ficha desplegable **General** antes de traer las líneas, debe rellenar un código de ubicación apropiado en cada línea de envío.  

> [!NOTE]  
> No puede enviar más productos que el número que se muestra en el campo **Cdad. pendiente** de la línea del documento de origen. Para enviar más productos, utilice la función de filtro para recuperar otro documento de origen que contenga una línea del mismo producto.  

Cuando tenga las líneas que desea enviar, puede iniciar el proceso que envía las líneas a los empleados del almacén para ejecutar el picking.

### <a name="pick-and-ship"></a>Realizar el picking y enviar

Normalmente, un empleado de almacén responsable del picking crea un documento de picking, o bien abre un documento ya creado de picking.  

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Envíos de almacén** y luego elija el enlace relacionado.
2. Seleccione el envío de almacén para el que desea realizar el picking, y después seleccione la acción **Crear picking**.
3. Rellene los campos en la página de solicitud y, a continuación, elija **Aceptar**. Se crea el documento de picking de almacén especificado.

    Alternativamente, abra un documento de picking de almacén existente.
4. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Picking** y luego elija el enlace relacionado. Seleccione el picking de almacén con el que desea trabajar.

    Si el almacén está configurado para utilizar ubicaciones, las líneas de picking se han convertido a líneas de acción Traer y Colocar.

    Si utiliza picking y ubicaciones directos, puede ordenar las líneas, asignar un empleado al picking, definir un filtro de división de bultos e imprimir las instrucciones.

5. Realice el picking de los productos y colóquelos en la ubicación de envío especificada, o en el área de envío, si no tiene ubicaciones.
6. Elija la acción **Registrar picking**.

    Se actualizarán los campos **Cantidad a enviar** y **Estado documento** de la cabecera del documento de envío. Los productos de los que ha realizado el picking ya no estarán disponibles para que otros pedidos hagan picking o para operaciones internas.
7. Imprima sus documentos de envío, prepare el embalaje y, a continuación, registre el envío.

Para obtener más información acerca de la selección para envíos de almacén, [Realizar un picking de los artículos para el envío de almacén](warehouse-how-to-pick-items-for-warehouse-shipment.md).

También puede utilizar la hoja de trabajo de picking para crear varias instrucciones de picking en una sola instrucción (para varios envíos) y, por tanto, mejorar la eficacia del picking en el almacén. Obtenga más información en [Planificar pickings en hojas de trabajo](warehouse-how-to-plan-picks-in-worksheets.md).

> [!NOTE]
> Si espera la llegada de productos específicos en el almacén y utiliza la funcionalidad de tránsito directo, [!INCLUDE[prod_short](includes/prod_short.md)] calcula la cantidad de producto que está en la ubicación de tránsito directo en cada línea de la hoja de trabajo de picking o envío. Este campo se actualiza cada vez que abandona y abre el documento de envío o la hoja de trabajo. Obtenga más información en [Productos de tránsito directo](warehouse-how-to-cross-dock-items.md).

## <a name="see-related-microsoft-training"></a>Consultar la [formación de Microsoft](/training/modules/ship-invoice-items-dynamics-365-business-central/) relacionada.

## <a name="see-also"></a>Consulte también .

[Warehouse Management](warehouse-manage-warehouse.md)  
[Inventario](inventory-manage-inventory.md)  
[Configuración de Warehouse Management](warehouse-setup-warehouse.md)  
[Gestión de ensamblaje](assembly-assemble-items.md)  
[Detalles de diseño: Warehouse Management](design-details-warehouse-management.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
