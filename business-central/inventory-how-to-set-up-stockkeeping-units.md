---
title: Configuración de unidades de almacenamiento
description: Utilice unidades de almacenamiento para registrar información sobre los productos de un determinado almacén o de un código de variante en particular.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.forms: '5704, 5700, 5702, 5701'
ms.date: 04/01/2021
ms.author: edupont
---
# Configurar unidades de almacenamiento

Utilice unidades de almacenamiento para registrar información sobre los productos de un determinado almacén o código de variante.  

Las unidades de almacenamiento vienen a complementar las fichas del producto. No los reemplazan, aunque guardan cierta relación con ellos. Estas unidades le permiten distinguir información sobre un producto de un determinado almacén, como un almacén o un centro de distribución, o de una determinada variante, como distintos códigos de situación e información de reposición.  

## Para configurar una unidad de almacenamiento  

1.  Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Unidades de almacenamiento**, y luego elija el enlace relacionado.  
2.  Seleccione la acción **Nuevo**.  
3.  Complete los campos de la ficha. Se requieren los siguientes campos: **Nº producto**, **Cód. almacén** y/o **Cód. variante**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

Una vez configurada la primera unidad de almacenamiento para un producto, se selecciona la casilla **Existe ud. de almacenam.** de la ficha **Producto**.  

Para crear varias unidades de almacenamiento para un producto, utilice el proceso **Crear ud. de almacenan.**.  

> [!NOTE]  
>  La información de la ficha **Unidad de almacenamiento** tiene prioridad sobre la ficha de **Producto**.

> [!Warning]
> Si UA se suministra a través de producción, el campo **Coste estándar** no se usa al facturar y ajustar el coste real del producto fabricado. En su lugar, el campo **Coste estándar** de la ficha subyacente de producto se utiliza, y cualquier desviación se calcula con el reparto de costes de dicho producto.<br /><br />
> Porque las L.M. y ruta no se pueden asignar a UA, la distribución del coste unitario y el cálculo relacionado de la parte de costes tampoco están disponibles en UA. Para obtener más información, consulte [Acerca de Calcular el coste estándar](finance-about-calculating-standard-cost.md)

## Consultar la [formación de Microsoft](/training/modules/control-inventory-multiple-locations/) relacionada

## Consulte también .

[Registro de productos nuevos](inventory-how-register-new-items.md)  
[Configuración de Warehouse Management](warehouse-setup-warehouse.md)  
[Información general de la gestión de almacenes](design-details-warehouse-management.md)
[Inventario](inventory-manage-inventory.md)  
[Gestión de ensamblaje](assembly-assemble-items.md)    
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
