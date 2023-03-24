---
title: Transferir productos entre almacenes
description: Aprenda a mover el inventario de un lugar o almacén a otro con el diario de reclasificación o con pedidos de transferencia.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 02/21/2023
ms.custom: bap-template
ms.search.keywords: 'move, warehouse'
ms.search.forms: '5746, 5745, 5759, 5753, 5743, 5758, 5752, 5744, 5749, 5740, 5741, 5742, 5757, 5748, 5747, 9285, 5756, 5755'
---
# Transferir el inventario entre almacenes

Puede transferir inventarios de productos entre almacenes creando pedidos de transferencia. También puede usar el diario de reclasificación de productos.

> [!NOTE]
> Para transferir productos, debe configurar los almacenes y las rutas de transferencia. Para obtener más información sobre cómo configurar almacenes, vaya a [Configurar almacenes](inventory-how-setup-locations.md). No puede usar pedidos de transferencia para almacenes *en blanco*.

## Pedidos de transferencia

Puede enviar una transferencia de salida desde un almacén y recibir una transferencia de entrada en el destino. Con él, puede:

* Seguimiento de una cantidad en tránsito
* Defina calendarios, rutas y tiempos de manejo de entrada y salida para el cálculo y la planificación de fechas. Para obtener más información sobre la planificación, vaya a [Sobre la funcionalidad de la planificación](production-about-planning-functionality.md).
* Use diferentes funciones de almacén para los almacenes de entrada y salida.
* Con algunas limitaciones, puede usar pedidos de transferencia para transferencias directas.

## Diarios de reclasificación de productos

* Transferencia sencilla y directa de productos entre almacenes.
* Mueva productos entre ubicaciones. Para obtener más información sobre la transferencia de productos entre ubicaciones, vaya a [Mover productos no planificados en configuraciones básicas de almacén](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md).
* Cambie un número de serie o lote por un nuevo número de serie o lote. Para obtener más información sobre cómo reclasificar los números de serie o lote, vaya a [Reclasificar números de serie o lote](inventory-how-work-item-tracking.md#to-reclassify-serial-or-lot-numbers).
* Cambie la fecha de caducidad a una nueva fecha.
* Reclasifique productos desde un almacén *en blanco* hasta un almacén real.
* Las actividades de almacén no se administran. Se crearán movimientos de almacén.

## Para transferir productos con un pedido de transferencia

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pedidos de transferencia** y luego elija el enlace relacionado.
2. En la página **Pedido de transferencia**, rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    >   Si ha rellenado los campos **Cód. en tránsito**, **Cód. transportista** y **Cód. servicio transportista** en la página **Ruta transf. espec.** al configurar la ruta de transferencia, los campos correspondientes del pedido de transferencia se rellenan automáticamente.

    Cuando se especifica un valor en el campo **Servicio transportista**, se calcula la fecha de recepción en el almacén de destino de la transferencia, sumando el tiempo de envío del transportista a la fecha de envío.

3. Para rellenar las líneas, introdúzcalas manualmente o elija una de las siguientes opciones en la acción **Funciones**:

    * Elija la acción **Traer conten. ubicac.** para seleccionar productos existentes de un contenedor específico en el almacén.
    * Elija la acción **Traer líns. albarán** para seleccionar productos que acaban de llegar al almacén de transferencia.

    Como trabajador de almacén en el almacén de procedencia de la transferencia, continúe con el envío de los productos.
4. Seleccione la acción **Registrar**, seleccione la opción **Envío** y seleccione el botón **Aceptar**.

    Los productos ahora se encuentran en tránsito entre las ubicaciones especificadas, según la ruta de transferencia especificada.

    Como trabajador de almacén en el almacén de procedencia de la transferencia, continúe con la recepción de los productos. Las líneas del pedido de transferencia son las mismas que en el envío y no se pueden editar.
5. Seleccione la acción **Registrar**, seleccione la opción **Recepción** y seleccione el botón **Aceptar**.

## Para transferir productos con el diario de reclasificación de productos

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diarios reclasif. producto**, y luego elija el enlace relacionado.
2. En la página **Diarios reclasif. producto**, rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. En el campo **Cód. almacén**, escriba la el almacén donde se almacenan los productos actualmente.

    > [!NOTE]  
    > Para transferir productos que no tienen código de almacén, deje en blanco el campo **Cód. almacén**.
4. En el campo **Cód. almacén destino**, especifique el almacén al que desee transferir los productos.
5. Seleccione la acción **Registrar**.

## Consultar la [formación de Microsoft](/training/modules/transfer-items/) relacionada

## Consulte también .

[Gestionar inventario](inventory-manage-inventory.md)  
[Configurar ubicaciones](inventory-how-setup-locations.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Cambiar las funciones que se muestran](ui-experiences.md)  
[Funciones empresariales generales](ui-across-business-areas.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
