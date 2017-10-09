---
title: Transferir productos entre almacenes | Documentos de Microsoft
description: "Describe cómo mover el inventario de un lugar o almacén a otro con el diario de reclasificación o con pedidos de transferencia."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: move, warehouse
ms.date: 06/02/2017
ms.author: SorenGP
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 41804dc183f9fa05ec1599db34c2b4f76a790a72
ms.contentlocale: es-es
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-transfer-inventory-between-locations"></a>Procedimiento: Transferir el inventario entre almacenes
Puede transferir inventarios de productos entre almacenes creando pedidos de transferencia. También puede usar el diario de reclasificación de productos.

Con los pedidos de transferencia, se envía la transferencia de salida desde un almacén y se recibe la transferencia de entrada en el otro almacén. Esto permite administrar las actividades de almacén correspondientes y proporciona más certidumbre de que las cantidades del inventario se actualizan correctamente.

Cono el diario de reclasificación, simplemente se rellenan los campos **Código de almacén** y **Nuevo código de almacén**. Al registrar el diario, los movimientos de productos se ajustan en los almacenes en cuestión. Con este método, las actividades de almacén no se administran.

> [!NOTE]  
>   Si tiene productos registrados en el inventario sin un código de almacén, por ejemplo cuando solo tenía un almacén, no podrá transferir estos productos con pedidos de transferencia. En su lugar, deberá utilizar el diario de reclasificación para reclasificar los productos desde un código de almacén en blanco a un código de almacén real.  Para obtener más información, vea el paso 3 en la sección "Para transferir productos con el diario de reclasificación".

Para transferir productos, se deben configurar las ubicaciones y las rutas de transferencia. Para obtener más información, vea [Procedimiento: Configurar almacenes](inventory-how-setup-locations.md).

> [!NOTE]  
>   Esta funcionalidad requiere que la experiencia esté definida en **Suite**. Para obtener más información, consulte [Personalizar la experiencia de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md).

## <a name="to-transfer-items-with-a-transfer-order"></a>Para transferir productos con un pedido de transferencia
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Pedidos de transferencia** y, a continuación, seleccione el vínculo relacionado.
2. En la ventana **Pedido de transferencia**, rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
>   Si ha rellenado los campos **Cód. en tránsito**, **Cód. transportista** y **Cód. servicio transportista** en la ventana **Ruta transf. espec.** cuando configuró la ruta de transferencia, los campos correspondientes del pedido de transferencia se rellenan automáticamente.

    Cuando se especifica un valor en el campo **Servicio transportista**, se calcula la fecha de recepción en el almacén de destino de la transferencia, sumando el tiempo de envío del transportista a la fecha de envío.

    Como trabajador de almacén en el almacén de procedencia de la transferencia, continúe con el envío de los productos.
3. Seleccione la acción **Registrar**, seleccione la opción **Envío** y seleccione el botón **Aceptar**.

    Los productos ahora se encuentran en tránsito entre las ubicaciones especificadas, según la ruta de transferencia especificada.

    Como trabajador de almacén en el almacén de procedencia de la transferencia, continúe con la recepción de los productos.
4. Seleccione la acción **Registrar**, seleccione la opción **Recepción** y seleccione el botón **Aceptar**.

## <a name="to-transfer-items-with-the-item-reclassification-journal"></a>Para transferir productos con el diario de reclasificación de productos
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Diarios reclas. producto** y, a continuación, seleccione el vínculo relacionado.
2. En la ventana **Diarios reclasif. producto**, rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. En el campo **Cód. almacén**, escriba la ubicación donde se almacenan los productos actualmente.

    > [!NOTE]  
>   Para transferir productos que no tienen código de almacén, deje en blanco el campo **Cód. almacén**.
4. En el campo **Cód. almacén destino**, especifique la ubicación a la que desee transferir los productos.
5. Seleccione la acción **Registrar**.

## <a name="see-also"></a>Consulte también
[Gestionar inventario](inventory-manage-inventory.md)  
[Configuración de almacenes](inventory-how-setup-locations.md)  
  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Personalizar la experiencia de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md)  
[Funciones empresariales generales](ui-across-business-areas.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
