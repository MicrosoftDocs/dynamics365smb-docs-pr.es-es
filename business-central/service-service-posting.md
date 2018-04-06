---
title: Registro de servicio | Documentos de Microsoft
description: "La funcionalidad de registro de servicios le permite procesar los documentos de manera eficaz y mantener una política de servicio al cliente satisfactoria. Puede crear y actualizar documentos registrados, así como crear movimientos en el área de servicio y en otros módulos para garantizar una correcta actualización."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/18/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: b191b5e8fbe0a60a32d32bd2dc1ca0cca07c06e4
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="service-posting"></a>Registro de servicio
La funcionalidad de registro de servicios le permite procesar los documentos de manera eficaz y mantener una política de servicio al cliente satisfactoria. Puede crear y actualizar documentos registrados, así como crear movimientos en el área de servicio y en otros módulos para garantizar una correcta actualización.  

> [!NOTE]  
>  A continuación se describe el registro del servicio independientemente del modo en que los artículos se controlan en el almacén.  
>   
>  En una ubicación en la que no se haya establecido el control de almacén como elemento obligatorio, las acciones de registro se realizan directamente desde la ventana **Líneas servicio**. En ubicaciones que requieran control de almacén, las acciones de registro descritas, salvo Enviar y Consumir, se realizan indirectamente mediante distintas funciones de envío de almacén, dependiendo de la configuración. Para obtener más información, vea [Realizar picking de productos con picking inventario](warehouse-how-to-pick-items-with-inventory-picks.md).  

## <a name="ship"></a>Envío  
La opción enviar permite registrar el tiempo y los productos que se hayan especificado en las líneas de un pedido de servicio una vez haya finalizado el servicio. Se crea un envío registrado y se llevan a cabo actualizaciones en el módulo Inventario y otros módulos de [!INCLUDE[d365fin](includes/d365fin_md.md)] a fin de reflejar que los productos se han excluido del inventario y se han enviado al cliente. En concreto, se generan movimientos de producto, de valores, de servicio y de garantía.  

Si el almacén está configurado para requerir el control de almacén, el envío y el movimiento de los productos de línea de servicio funcionan de la misma forma que para otros documentos de origen. La única diferencia es que los productos de línea de servicio pueden consumirse externa o internamente, lo cual requiere dos funciones diferentes de lanzamiento.

## <a name="invoice"></a>Facturar  
Esta opción se utiliza a fin de emitir una factura para el cliente al que desea cobrar el servicio. Normalmente, la factura recoge la diferencia entre la cantidad enviada registrada por la función **Registrar envío** y la cantidad consumida registrada por la función **Registrar consumo**. No se puede facturar algo que no se ha enviado. Al ejecutar la función **Registrar factura**, crea una factura de servicio registrada y actualiza los documentos registrados antes de concordarlos con las cantidades que se incluyen en la factura emitida. Al igual que en otros procedimientos de registro, se generan los movimientos correspondientes, incluidos los de contabilidad.  

## <a name="ship-and-invoice"></a>Enviar y facturar  
La opción de envío y facturación permite realizar envíos de servicio y de factura al mismo tiempo.  

## <a name="ship-and-consume"></a>Enviar y consumir  
Con la opción consumo puede registrar los productos, los costes o las horas que se hayan empleado en un servicio pero que no se pueden incluir en la factura del cliente. No se emite una factura, pero puede emitir documentos de envío y de consumo de servicio de forma simultánea a fin de reflejar que algunos productos u horas se han proporcionado al cliente sin cargo alguno. Asimismo, se crean los movimientos correspondientes para registrar el consumo.  

> [!NOTE]  
>  El procedimiento de registro de servicios permite realizar un registro parcial. Puede crear un envío o factura parciales rellenando los campos **Cantidad a enviar** y**Cdad. a facturar** en las líneas de servicio individuales de los pedidos de servicio antes del registro. Tenga en cuenta que no se puede crear una factura de algo que no se ha enviado. Es decir, para poder facturar, debe haber registrado un envío, o bien debe elegir enviar y facturar al mismo tiempo.  

Una vez finalizado el registro, podrá ver los documentos de servicio registrados desde las ventanas correspondientes, es decir, **Envío servicio registrado** y **Fact. ventas (servicio) regis.** Los movimientos registrados que se han creado pueden verse en diversas ventanas que contienen movimientos registrados, como **Movs. contabilidad**, **Movs. producto**, **Movs. almacén**, **Movs. servicio**, **Movs. proyectos** y **Movs. garantía**.  

## <a name="to-view-information-about-a-posted-service-document"></a>Para ver información sobre un documento de servicio registrado  
Cuando se registra una factura, un envío o un abono de servicio, la información del documento se transfiere a las ventanas **Fact. ventas (servicio) regis.**, **Envío servicio registrado** o **Abono ventas (servicio) regis.** respectivamente. No puede escribir, modificar ni eliminar información en estas ventanas. En ellas puede imprimir un albarán, una factura o un abono.  

El procedimiento siguiente utiliza una factura de servicio registrada como ejemplo, pero es posible aplicar el mismo procedimiento a los envíos de servicio registrados y al histórico de abonos.  

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Histórico de facturas de servicio** y, a continuación, seleccione el vínculo relacionado.  
2. Abra la factura de servicio registrada que desee ver.  
3. Para obtener un resumen de la factura registrada, elija la acción **Estadísticas**.  

    Se abre la ventana **Estad. pedido servicio**. Dicha ventana muestra información tal como la cantidad, el importe, el IVA, el coste, los beneficios y el crédito máximo del cliente en el documento registrado.

## <a name="see-also"></a>Consulte también  
[Registrar pedidos de servicio](service-how-to-post-service-orders.md)   
[Crear pedidos de servicio](service-how-to-create-service-orders.md)

