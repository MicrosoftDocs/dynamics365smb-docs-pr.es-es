---
title: 'Detalles de diseño: Flujo de salida del almacén | Documentos de Microsoft'
description: El flujo de salida en el almacén comienza con una solicitud de los documentos de origen lanzados para sacar los productos del almacén, para enviarlos a una parte externa o a otra ubicación de la empresa. Desde el área de almacenamiento, las actividades de almacén se llevan a cabo en distintos niveles de complejidad para extraer productos de las dársenas de envío.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: d2ea80352352cfac83ebce97fee9d4f312e00348
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/08/2019
ms.locfileid: "805741"
---
# <a name="design-details-outbound-warehouse-flow"></a>Detalles de diseño: Flujo de salida del almacén
El flujo de salida en el almacén comienza con una solicitud de los documentos de origen lanzados para sacar los productos del almacén, para enviarlos a una parte externa o a otra ubicación de la empresa. Desde el área de almacenamiento, las actividades de almacén se llevan a cabo en distintos niveles de complejidad para extraer productos de las dársenas de envío.  

 Cada producto se identifica y empareja con su documento de origen de entrada correspondiente. Existen los siguientes documentos de origen de salida:  

- Pedido de venta  
- Pedido de transferencia de salida  
- Pedido dev. compra  
- Pedido servicio  

Además, existen los siguientes documentos de origen internos que funcionan como orígenes de salida:  

- Orden de producción con necesidad de componentes  
- Pedido de ensamblado con necesidad de componentes  

 Los dos últimos documentos representan los flujos de salida del almacén a las áreas de operaciones internas. Para obtener más información acerca de la gestión de almacenes para los procesos de entrada y salida internos, consulte [Detalles de diseño: Flujos de almacén internos](design-details-internal-warehouse-flows.md).  

 Los procesos y los documentos de interfaz de usuario en los flujos de almacén de salida varían según el la configuración básica y avanzada de almacén. La diferencia principal es que las actividades se realizan pedido a pedido en la configuración básica de almacén y se consolidan para varios pedidos en la configuración avanzada. Para obtener más información acerca de los diferentes niveles de complejidad de almacenes, consulte [Detalles de diseño: Resumen de almacén](design-details-warehouse-setup.md).  

 En [!INCLUDE[d365fin](includes/d365fin_md.md)], los procesos de salida para la selección y el envío se pueden realizar de cuatro maneras utilizando distintas funciones según el nivel de complejidad del almacén.  

|Método|Proceso de salida|Ubicaciones|Picking|Envíos|Nivel de complejidad (consulte [Detalles de diseño: configuración de almacén](design-details-warehouse-setup.md))|  
|------------|---------------------|----------|-----------|---------------|--------------------------------------------------------------------------------------------------------------------|  
|A|Registro de picking y envío desde la línea de pedido|X|||2|  
|P|Registro de picking y envío desde un documento de picking de existencias||X||3|  
|C|Registro de picking y envío desde un documento de envío de almacén|||X|5/4/6|  
|D|Registro de picking desde un documento de picking de almacén y registro de envío de un documento de envío de almacén||X|X|5/4/6|  

 La selección de un planteamiento depende de las prácticas aceptadas de la empresa y del nivel de su complejidad organizativa. En un entorno de pedido por pedido con procesos directos y estructura simple de ubicación, resulta apropiado el método A, selección y envío desde la línea de pedido. En otras empresas de pedido por pedido donde los productos para una línea de pedido pueden proceder de más de una ubicación o donde los trabajadores del almacén no pueden trabajar con documentos de pedido, es adecuado usar documentos de selección aparte, método B. En los casos de empresas donde los procesos de selección y envío implican una gestión de pedidos múltiples y por tanto requieren un mayor control y supervisión, la empresa puede optar por utilizar un documento de envío de almacén y un documento de selección de almacén para separar las tareas de selección y envío, métodos C y D.  

 En los métodos A, B y C, las acciones de selección y envío se agrupan en un paso al registrar el documento correspondiente como enviado. En el método D, primero se registra la selección y después se registra el envío más adelante desde otro documento.  

## <a name="basic-warehouse-configurations"></a>Configuración básica de almacén  
 En el diagrama siguiente se ilustran los flujos de almacén de salida por tipo de documento en la configuración básica de almacén. Los números del diagrama corresponden a los pasos de las secciones que siguen el diagrama.  

 ![Flujo de salida en la configuración básica de almacén](media/design_details_warehouse_management_outbound_basic_flow.png "Flujo de salida en la configuración básica de almacén")  

### <a name="1-release-source-document--create-inventory-pick-or-movement"></a>1: Lanzar documento de origen/Crear selección o movimiento de inventario  
 Cuando un usuario responsable de los documentos de origen, como un procesador de pedidos de venta o un planificador de producción, está preparado para la actividad de almacén salida, lanza el documento de origen para señalizar a los empleados de almacén que los productos o componentes vendidos se pueden preparar y colocar en las ubicaciones especificadas. Además, el usuario crea documentos de picking o de movimiento de inventario para las líneas de pedido individuales, mediante envío, basándose en las ubicaciones y cantidades especificadas para manipular.  

> [!NOTE]  
>  Los movimientos de inventario se utilizan para mover productos a áreas de operaciones internas en las configuraciones de almacén básico, según documentos de origen o ad hoc.  

### <a name="2-create-outbound-request"></a>2: Crear solicitud de salida  
 Cuando se libera el documento de origen de salida, se crea automáticamente una solicitud de almacén de salida. Contiene referencias al tipo y el número de documento de origen y no puede verlo el usuario.  

### <a name="3-create-inventory-pick-or-movement"></a>3: Crear selección de inventario o movimiento  
 En la página **Picking inventario** o **Movimiento de inventario**, el trabajador del almacén recupera, mediante extracción, las líneas pendientes del documento de origen basándose en las solicitudes de salida del almacén. Las líneas de selección de inventario las puede crear también mediante envío el usuario responsable del documento de origen.  

### <a name="4-post-inventory-pick-or-register-inventory-movement"></a>4: Registrar selección de inventario o Registrar movimiento de inventario  
 En cada línea de los productos en los que se ha realizado el picking o se han trasladado, parcial o totalmente, el empleado del almacén rellena el campo **Cantidad** y, a continuación, registra el picking de existencias o el movimiento de inventario. Los documentos de origen relacionados con el picking de existencias se registran como enviados o consumidos. No se registran los documentos de origen relacionados con los movimientos de inventario.  

 En el caso de selecciones de inventario, se crean movimientos de producto negativos y movimientos de almacén, así como se elimina la solicitud de selección si se ha gestionado íntegramente. Por ejemplo, se actualiza el campo **Cantidad enviada** en la línea de salida del documento de origen. Se crea un documento de envío registrado que refleja el pedido de venta, por ejemplo, y los productos enviados.  

## <a name="advanced-warehouse-configurations"></a>Configuración avanzada de almacén  
 En el diagrama siguiente se ilustran los flujos de almacén de salida por tipo de documento en la configuración avanzada de almacén. Los números del diagrama corresponden a los pasos de las secciones que siguen el diagrama.  

 ![Flujo de salida en la configuración avanzada de almacén](media/design_details_warehouse_management_outbound_advanced_flow.png "Flujo de salida en la configuración avanzada de almacén")  

### <a name="1-release-source-document"></a>1: Lanzar documento de origen  
 Cuando un usuario responsable de los documentos de origen, como un procesador de pedidos de venta o un planificador de producción, está preparado para la actividad de almacén de salida, lanza el documento de origen para señalizar a los empleados de almacén que los productos o componentes vendidos se pueden preparar y colocar en las ubicaciones especificadas.  

### <a name="2-create-outbound-request"></a>2: Crear solicitud de salida  
 Cuando se libera el documento de origen de entrada, se crea automáticamente una solicitud de almacén de salida. Contiene referencias al tipo y el número de documento de origen y no puede verlo el usuario.  

### <a name="3-create-warehouse-shipment"></a>3: Crear envío de almacén  
 En la página **Envío almacén**, el trabajador responsable de envíos recupera las líneas pendientes del documento de origen basándose en la solicitud de salida del almacén. Se pueden combinar varias líneas del documento de origen en un documento de envío de almacén.  

### <a name="4-release-shipment--create-warehouse-pick"></a>4: Lanzar envío/Crear selección de almacén  
 El empleado de envíos responsable libera el envío de almacén, para que los empleados de almacén puedan crear o coordinar el picking de almacén para el envío en cuestión.  

 El usuario también puede crear mediante envío documentos de selección de almacén para líneas de envío particulares, en función de las ubicaciones especificadas y de las cantidades que gestionar.  

### <a name="5-release-internal-operation--create-warehouse-pick"></a>5: Lanzar operación interna/Crear selección de inventario  
 El usuario responsable de las operaciones internas lanza un documento de origen interno, como, por ejemplo, una orden de producción y un pedido de ensamblado, de modo que los empleados de almacén pueden crear o coordinar los picking de almacén para la operación interna en cuestión.  

 El usuario también puede crear mediante envío documentos de selección de almacén para la orden de producción o el pedido de ensamblado particular, en función de las ubicaciones especificadas y de las cantidades que gestionar.  

### <a name="6-create-pick-request"></a>6: Crear petición de selección  
 Cuando se libera el documento de origen de salida, se crea automáticamente una solicitud de picking de almacén. Contiene referencias al tipo y el número de documento de origen y no puede verlo el usuario. Dependiendo de la configuración, el consumo de una orden de producción y un pedido de ensamblado también crea una solicitud de selección de los componentes necesarios del inventario.  

### <a name="7-generate-pick-worksheet-lines"></a>7: Generar líneas de hoja de trabajo de selección  
 El usuario responsable de coordinar el picking recupera las líneas de picking del almacén en la **Hoja trabajo picking**, basándose en las solicitudes de picking de los envíos de almacén o las operaciones internas con el consumo de componentes. El usuario selecciona las líneas para picking y prepara los picking mediante la especificación de las ubicaciones de las que se tomarán, las ubicaciones en las que se colocarán y la cantidad de unidades que se manipularán. Las ubicaciones se pueden predefinir mediante la configuración del recurso de ubicación de almacén o de operación.  

 El usuario especifica los métodos de picking para la manipulación optimizada en el almacén y, a continuación, usa una función para crear los documentos de picking de almacén correspondientes, que se asignan a distintos empleados de almacén que realizan los picking de almacén. Cuando los picking de almacén están totalmente asignados, se eliminan las líneas en **Hoja trabajo picking**.  

### <a name="8-create-warehouse-pick-documents"></a>8: Cree documentos de selección de almacén  
 El empleado de almacén que realiza las tareas de picking crea un documento de picking de almacén, mediante extracción, basándose en el documento de origen lanzado. El documento de selección de almacén se crea y se asigna también al trabajador de almacén mediante envío.  

### <a name="9-register-warehouse-pick"></a>9: Registrar selección de almacén  
 En cada línea de los productos en los que se ha realizado el picking, parcial o totalmente, el empleado del almacén rellena el campo **Cantidad** de la página **Picking almacén** y, a continuación, registra el picking del almacén.  

 Se crean movimientos de almacén y se eliminan las líneas de picking de almacén, si se han manipulado por completo. El documento de picking de almacén permanecerá abierto hasta que se registre la cantidad total del envío de almacén relacionado. El campo **Cdad. preparada pedido** de las líneas de albarán de almacén se actualiza como corresponde.  

### <a name="10-post-warehouse-shipment"></a>10: Registro de envío de almacén  
 Cuando todos los productos del documento de envío de almacén están registrados como preparados para las ubicaciones de envío especificadas, el empleado responsable de los envíos registra el envío de almacén. Se crean movimientos de producto negativos. Por ejemplo, se actualiza el campo **Cantidad enviada** en la línea de salida del documento de origen.  

## <a name="see-also"></a>Consulte también  
 [Detalles de diseño: Gestión de almacén](design-details-warehouse-management.md)
