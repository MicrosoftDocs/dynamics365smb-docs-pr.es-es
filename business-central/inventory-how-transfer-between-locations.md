---
title: Transferir productos entre almacenes | Documentos de Microsoft
description: Describe cómo mover el inventario de un lugar o almacén a otro con el diario de reclasificación o con pedidos de transferencia.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: move, warehouse
ms.date: 04/01/2020
ms.author: SorenGP
ms.openlocfilehash: c7d383fdaf75857013651944207616bdc7208e6d
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/01/2020
ms.locfileid: "3181969"
---
# <a name="transfer-inventory-between-locations"></a>Transferir el inventario entre almacenes
Puede transferir inventarios de productos entre almacenes creando pedidos de transferencia. También puede usar el diario de reclasificación de productos.

Con los pedidos de transferencia, se envía la transferencia de salida desde un almacén y se recibe la transferencia de entrada en el otro almacén. Esto permite administrar las actividades de almacén correspondientes y proporciona más certidumbre de que las cantidades del inventario se actualizan correctamente.

Cono el diario de reclasificación, simplemente se rellenan los campos **Código de almacén** y **Nuevo código de almacén**. Al registrar el diario, los movimientos de productos se ajustan en los almacenes en cuestión. Con este método, las actividades de almacén no se administran.

> [!NOTE]  
>   Si tiene productos registrados en el inventario sin un código de almacén, por ejemplo cuando solo tenía un almacén, no podrá transferir estos productos con pedidos de transferencia. En su lugar, deberá utilizar el diario de reclasificación para reclasificar los productos desde un código de almacén en blanco a un código de almacén real.  Para obtener más información, vea el paso 3 en [Para transferir productos con el diario de reclasificación](inventory-how-transfer-between-locations.md#to-transfer-items-with-the-item-reclassification-journal).

Para transferir productos, se deben configurar las ubicaciones y las rutas de transferencia. Para obtener más información, consulte [Configurar ubicaciones](inventory-how-setup-locations.md).

## <a name="to-transfer-items-with-a-transfer-order"></a>Para transferir productos con un pedido de transferencia
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Pedidos de transferencia** y luego elija el enlace relacionado.
2. En la cabecera de la página **Pedido de transferencia**, rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    >   Si ha rellenado los campos **Cód. en tránsito**, **Cód. transportista** y **Cód. servicio transportista** en la página **Ruta transf. espec.** cuando configuró la ruta de transferencia, los campos correspondientes del pedido de transferencia se rellenan automáticamente.

    Cuando se especifica un valor en el campo **Servicio transportista**, se calcula la fecha de recepción en el almacén de destino de la transferencia, sumando el tiempo de envío del transportista a la fecha de envío.

3. Para rellenar las líneas, introdúzcalas manualmente o elija una de las siguientes opciones en la acción **Funciones**:
    - Elija la acción **Traer conten. ubicac.** para seleccionar productos existentes de un contenedor específico en el almacén.
    - Elija la acción **Traer líns. albarán** para seleccionar productos que acaban de llegar al almacén de transferencia.   

    Como trabajador de almacén en el almacén de procedencia de la transferencia, continúe con el envío de los productos.
4. Seleccione la acción **Registrar**, seleccione la opción **Envío** y seleccione el botón **Aceptar**.

    Los productos ahora se encuentran en tránsito entre las ubicaciones especificadas, según la ruta de transferencia especificada.

    Como trabajador de almacén en el almacén de procedencia de la transferencia, continúe con la recepción de los productos. Las líneas del pedido de transferencia son las mismas que en el envío y no se pueden editar.
5. Seleccione la acción **Registrar**, seleccione la opción **Recepción** y seleccione el botón **Aceptar**.

## <a name="to-transfer-items-with-the-item-reclassification-journal"></a>Para transferir productos con el diario de reclasificación de productos
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Diarios reclasif. producto** y luego elija el enlace relacionado.
2. En la página **Diarios reclasif. producto**, rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. En el campo **Cód. almacén**, escriba la ubicación donde se almacenan los productos actualmente.

    > [!NOTE]  
    >   Para transferir productos que no tienen código de almacén, deje en blanco el campo **Cód. almacén**.
4. En el campo **Cód. almacén destino**, especifique la ubicación a la que desee transferir los productos.
5. Seleccione la acción **Registrar**.

## <a name="see-also"></a>Consulte también
[Gestionar inventario](inventory-manage-inventory.md)  
[Configurar ubicaciones](inventory-how-setup-locations.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Cambiar las funciones que se muestran](ui-experiences.md)  
[Funciones empresariales generales](ui-across-business-areas.md)
