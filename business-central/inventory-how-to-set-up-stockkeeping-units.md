---
title: Configurar unidades de almacenamiento | Documentos de Microsoft
description: "Utilice unidades de almacenamiento para registrar información sobre los productos de un determinado almacén o de un código de variante en particular."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 11/15/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 67400e424305cc705db5c1bd52a8e4de17ecc5a9
ms.openlocfilehash: d5582e1857481d32ad146d0732f4c60d1b678c74
ms.contentlocale: es-es
ms.lasthandoff: 11/20/2018

---
# <a name="set-up-stockkeeping-units"></a>Configurar unidades de almacenamiento
Utilice unidades de almacenamiento para registrar información sobre los productos de un determinado almacén o de un código de variante en particular.  

 Las unidades de almacenamiento vienen a complementar las fichas del producto. No los reemplazan, aunque guardan cierta relación con ellos. Estas unidades le permiten distinguir información sobre un producto de un determinado almacén, como un almacén o un centro de distribución, o de una determinada variante, como distintos códigos de situación e información de reposición.  

## <a name="to-set-up-a-stockkeeping-unit"></a>Para configurar una unidad de almacenamiento  

1.  Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Uds. de almacenam.** y luego elija el enlace relacionado.  
2.  Seleccione la acción **Nuevo**.  
3.  Complete los campos de la ficha. Se requieren los siguientes campos: **Nº producto**, **Cód. almacén** y/o **Cód. variante**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

Una vez configurada la primera unidad de almacenamiento para un producto, se selecciona la casilla **Existe ud. de almacenam.** de la ficha **Producto**.  

Para crear varias unidades de almacenamiento para un producto, utilice el proceso **Crear ud. de almacenan.**.  

> [!NOTE]  
>  La información de la ficha **Unidad de almacenamiento** tiene prioridad sobre la ficha de **Producto**.

> [!Warning]
> Si UA se suministra a través de producción, el campo **Coste estándar** no se usa al facturar y ajustar el coste real del producto fabricado. En su lugar, el campo **Coste estándar** de la ficha subyacente de producto se utiliza, y cualquier desviación se calcula con el reparto de costes de dicho producto.<br /><br />
> Porque las L.M. y ruta no se pueden asignar a UA, la distribución del coste unitario y el cálculo relacionado de la parte de costes tampoco están disponibles en UA. Para obtener más información, consulte [Acerca de Calcular el coste estándar](finance-about-calculating-standard-cost.md)

## <a name="see-also"></a>Consulte también  
[Registro de productos nuevos](inventory-how-register-new-items.md)  
[Configurar la gestión del almacén](warehouse-setup-warehouse.md)  
[Gestión de almacenes](warehouse-manage-warehouse.md)  
[Grupos contables inventario](inventory-manage-inventory.md)  
[Gestión de ensamblaje](assembly-assemble-items.md)    
[Detalles de diseño: Gestión de almacén](design-details-warehouse-management.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

