---
title: 'Detalles de diseño: Flujo de entrada en almacén | Documentos de Microsoft'
description: El flujo de entrada de un almacén comienza cuando los productos llegan al almacén de la ubicación de empresa, recibidos de orígenes externos o de otra ubicación de empresa. Un empleado registra los productos normalmente mediante el escaneo de un código de barras. Desde la dársena de recepción, las actividades de almacén se llevan a cabo en distintos niveles de complejidad para introducir los productos en el área de almacén.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 3083b52a2345d2c5dbaa15c34c7a93afb3b9d063
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/29/2019
ms.locfileid: "1247334"
---
# <a name="design-details-inbound-warehouse-flow"></a>Detalles de diseño: Flujo de entrada en almacén
El flujo de entrada de un almacén comienza cuando los productos llegan al almacén de la ubicación de empresa, recibidos de orígenes externos o de otra ubicación de empresa. Un empleado registra los productos normalmente mediante el escaneo de un código de barras. Desde la dársena de recepción, las actividades de almacén se llevan a cabo en distintos niveles de complejidad para introducir los productos en el área de almacén.  

 Cada producto se identifica y empareja con su documento de origen de entrada correspondiente. Existen los siguientes documentos de origen de entrada:  

- Pedido de compra  
- Pedido de transferencia de entrada  
- Pedido dev. venta  

Además, existen los siguientes documentos de origen internos que funcionan como orígenes de entrada:  

- Orden de producción con registro de salida  
- Pedido de ensamblado con registro de salida  

Los dos últimos representan los flujos de entrada al almacén desde las áreas de operaciones internas. Para obtener más información acerca de la gestión de almacenes para los procesos de entrada y salida internos, consulte [Detalles de diseño: Flujos de almacén internos](design-details-internal-warehouse-flows.md).  

Los procesos y los documentos de interfaz de usuario en los flujos de almacén de entrada varían según el la configuración básica y avanzada de almacén. La diferencia principal es que las actividades se realizan pedido a pedido en la configuración básica de almacén y se consolidan para varios pedidos en la configuración avanzada. Para obtener más información acerca de los diferentes niveles de complejidad de almacenes, consulte [Detalles de diseño: Resumen de almacén](design-details-warehouse-setup.md).  

En [!INCLUDE[d365fin](includes/d365fin_md.md)], los procesos de entrada para recepción y ubicación se pueden realizar de cuatro maneras utilizando distintas funciones según el nivel de complejidad del almacén.  

|Método|Proceso de salida|Ubicaciones|Recepciones|Ubicaciones|Nivel de complejidad (consulte [Detalles de diseño: configuración de almacén](design-details-warehouse-setup.md))|  
|------------|---------------------|----------|--------------|----------------|--------------------------------------------------------------------------------------------------------------------|  
|A|Registro de la recepción y ubicación desde la línea de pedido|X|||2|  
|P|Registro de la recepción y ubicación desde un documento de ubicación del inventario|||X|3|  
|C|Registro de la recepción y ubicación desde un documento de recepción de almacén||X||5/4/6|  
|D|Registro de la recepción desde un documento de recepción de almacén y registro de ubicación desde un documento de ubicación de almacén||X|X|5/4/6|  

La selección de un planteamiento depende de las prácticas aceptadas de la empresa y del nivel de su complejidad organizativa. En un entorno de almacén de pedido por pedido, donde la mayoría del personal de almacén trabaja directamente con documentos de pedido, una empresa puede decidir utilizar el método A. Un almacén de pedido por pedido que tenga procesos de colocación más complejos, o donde haya personal de almacén dedicado para realizar funciones de almacenamiento, se puede decidir separar las funciones de ubicación del documento de pedido, el método B. Además, las empresas que necesitan planificar la gestión de varios pedidos pueden encontrar útil usar documentos de recepción de almacén, los métodos C y D.  

En los métodos A, B y C, las acciones de recepción y ubicación se agrupan en un paso al registrar los documentos correspondientes como recibidos. En el método D, se registra primero la recepción para reconocer la entrada de existencias y que hay productos disponibles para su venta. A continuación, el empleado de almacén registra la ubicación a fin de que los productos estén disponibles para picking.  

## <a name="basic-warehouse-configurations"></a>Configuración básica de almacén  
En el diagrama siguiente se ilustran los flujos de almacén de entrada por tipo de documento en la configuración básica de almacén. Los números del diagrama corresponden a los pasos de las secciones que siguen el diagrama.  

![Flujo de entrada en la configuración básica de almacén](media/design_details_warehouse_management_inbound_basic_flow.png "Flujo de entrada en la configuración básica de almacén")  

### <a name="1-release-source-document--create-inventory-put-away"></a>1: Lanzar documento de origen/Crear ubicación de inventario  
Cuando se reciben productos en el almacén, el usuario responsable de la recepción libera el documento de origen, como, por ejemplo, un pedido de compra o un pedido de transferencia interna, para señalizar a los empleados de almacén que los productos recibidos se pueden guardar en el inventario. El usuario también puede crear mediante envío documentos de ubicación de inventario para líneas de pedido particulares, en función de las ubicaciones especificadas y de las cantidades que gestionar.  

### <a name="2-create-inbound-request"></a>2: Crear solicitud de entrada  
Cuando se libera el documento de origen de entrada, se crea automáticamente una solicitud de almacén de entrada. Contiene referencias al tipo y el número de documento de origen y no puede verlo el usuario.  

### <a name="3-create-inventory-put-away"></a>3: Crear ubicación de inventario  
En la página **Ubicación inventario**, el trabajador del almacén recupera, mediante extracción, las líneas pendientes del documento de origen basándose en las solicitudes de entrada al almacén. Las líneas de ubicación de inventario las puede crear también mediante envío el usuario responsable del documento de origen.  

### <a name="4-post-inventory-put-away"></a>4: Publicar ubicación de inventario  
En cada línea de los productos que se han ubicado, parcial o totalmente, el empleado del almacén rellena el campo **Cantidad** y, a continuación, registra la ubicación de inventario. Los documentos de origen que están relacionados con la ubicación de inventario se registran como recibidos.  

Se crean movimientos de producto positivos, se crean movimientos de almacén y se elimina la solicitud de ubicación, si se ha manipulado por completo. Por ejemplo, se actualiza el campo **Cantidad recibida** en la línea de entrada del documento de origen. Se crea un documento de recepción registrada que refleja el pedido de compra, por ejemplo, y los productos recibidos.  

## <a name="advanced-warehouse-configurations"></a>Configuración avanzada de almacén  
En el diagrama siguiente se ilustran los flujos de almacén de entrada por tipo de documento en la configuración avanzada de almacén. Los números del diagrama corresponden a los pasos de las secciones que siguen el diagrama.  

![Flujo de entrada en la configuración avanzada de almacén](media/design_details_warehouse_management_inbound_advanced_flow.png "Flujo de entrada en la configuración avanzada de almacén")  

### <a name="1-release-source-document"></a>1: Lanzar documento de origen  
Cuando se reciben productos en el almacén, el usuario responsable de la recepción libera el documento de origen, como, por ejemplo, un pedido de compra o un pedido de transferencia interna, para señalizar a los empleados de almacén que los productos recibidos se pueden guardar en el inventario.  

### <a name="2-create-inbound-request"></a>2: Crear solicitud de entrada  
Cuando se libera el documento de origen de entrada, se crea automáticamente una solicitud de almacén de entrada. Contiene referencias al tipo y el número de documento de origen y no puede verlo el usuario.  

### <a name="3-create-warehouse-receipt"></a>3: Crear recepción de almacén  
En la página **Recep. almacén**, el usuario responsable de recibir los productos recupera las líneas pendientes del documento de origen basándose en la solicitud de entrada en el almacén. Se pueden combinar varias líneas del documento de origen en un documento de recepción de almacén.  

El usuario rellena el campo **Cdad. a manipular** y selecciona la zona y la ubicación de recepción, si procede.  

### <a name="4-post-warehouse-receipt"></a>4: Registrar recepción de almacén  
El usuario registra la recepción de almacén. Se crean movimientos de producto positivos. Por ejemplo, se actualiza el campo **Cantidad recibida** en la línea de entrada del documento de origen.  

### <a name="5-create-warehouse-internal-put-away"></a>5: Crear ubicación interna de almacén  
El usuario responsable de la ubicación a partir de las operaciones internas crea una ubicación interna de almacén para los productos que tienen que ubicarse en el almacén, como la salida de producción o de ensamblado. El usuario especifica la cantidad, la zona y la ubicación donde se deben colocar los productos, potencialmente con la función **Traer conten. ubicac.** El usuario lanza la ubicación interna de almacén, lo que crea una solicitud de almacén de entrada, de modo que la tarea se puede recuperar en documentos de ubicación de almacén o en la hoja de trabajo de ubicación.  

### <a name="6-create-put-away-request"></a>6: Crear petición de ubicación  
Cuando se registra el documento de origen de entrada, se crea automáticamente una solicitud de ubicación de almacén. Contiene referencias al tipo y el número de documento de origen y no puede verlo el usuario. Dependiendo de la configuración, la salida de una orden de producción también crea una solicitud de almacén para colocar los productos terminados en el inventario.  

### <a name="7-generate-put-away-worksheet-lines-optional"></a>7: Generar líneas de hoja de trabajo de ubicación (opcional)  
El usuario responsable de coordinar las ubicaciones recupera las líneas de ubicación de almacén en **Hoja trabajo ubicación** basándose en las recepciones de almacén registradas o las operaciones internas con salida. El usuario selecciona las líneas para ubicación y prepara las ubicaciones mediante la especificación de las ubicaciones de las que se tomarán, las ubicaciones en las que se colocarán y la cantidad de unidades que se manipularán. Las ubicaciones se pueden predefinir mediante la configuración del recurso de ubicación de almacén o de operación.  

Cuando todas las ubicaciones se planifican y asignan a empleados de almacén, el usuario genera los documentos de ubicación de almacén. Las líneas con ubicación totalmente asignada se eliminan de **Hoja trabajo ubicación**.  

> [!NOTE]  
>  Si el campo **Utilizar hoja trabajo ubicación** no se ha seleccionado en la ficha de almacén, los documentos de ubicación en almacén se crean directamente de acuerdo con las recepciones de almacén registradas. En ese caso, se omite el paso 7.  

### <a name="8-create-warehouse-put-away-document"></a>8: Cree documento de ubicación de almacén  
El empleado de almacén que realiza las ubicaciones crea un documento de ubicación de almacén, mediante extracción, basándose en la recepción de almacén registrada. El documento de ubicación de almacén se crea y se asigna también a un trabajador de almacén mediante envío.  

### <a name="9-register-warehouse-put-away"></a>9: Registrar ubicación de almacén  
En cada línea de los productos que se han ubicado, parcial o totalmente, el empleado del almacén rellena el campo **Cantidad** en la página **Ubicación almacén** y, a continuación, registra la ubicación de inventario.  

Se crean movimientos de almacén y se eliminan las líneas de ubicación de almacén, si se han manipulado por completo. El documento de ubicación de almacén permanecerá abierto hasta que se registre la cantidad total de la recepción de almacén registrada relacionada. El campo **Cantidad a ubicar** de las líneas de pedido de recepción de almacén se actualiza como corresponde.  

## <a name="see-also"></a>Consulte también  
[Detalles de diseño: Gestión de almacén](design-details-warehouse-management.md)
