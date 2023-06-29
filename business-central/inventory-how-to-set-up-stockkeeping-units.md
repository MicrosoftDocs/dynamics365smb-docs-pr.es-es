---
title: Configuración de unidades de almacenamiento
description: Utilice unidades de almacenamiento para registrar información sobre los productos de un determinado almacén o de una variante en particular.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 04/19/2023
ms.custom: bap-template
ms.search.forms: '5704, 5700, 5702, 5701'
---

# <a name="set-up-stockkeeping-units"></a><a name="set-up-stockkeeping-units"></a><a name="set-up-stockkeeping-units"></a>Configurar unidades de almacenamiento

Utilice unidades de almacenamiento para registrar información sobre los productos de un determinado almacén o variante. Le permiten agregar información diferente sobre un artículo para una ubicación específica, por ejemplo:

* Un almacén o centro de distribución
* Variantes, como diferentes números de estante y diferente información de reposición, para el mismo artículo  

## <a name="to-set-up-a-stockkeeping-unit"></a><a name="to-set-up-a-stockkeeping-unit"></a><a name="to-set-up-a-stockkeeping-unit"></a>Para configurar una unidad de almacenamiento

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Unidades de almacenamiento**, y luego elija el enlace relacionado.  
2. Seleccione la acción **Nuevo**.  
3. Rellene los campos según sea necesario. Se requieren los siguientes campos: **Nº producto**, **Cód. almacén** y/o **Cód. variante**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

Una vez configurada la primera unidad de almacenamiento para un producto, se selecciona la casilla **Existe ud. de almacenam.** de la pestaña **Producto**.  

Para crear varias unidades de almacenamiento para un producto, utilice el proceso **Crear ud. de almacenan.**. Para obtener más información sobre trabajos por lotes, vaya a [Utilice las colas de trabajos para programar tareas](admin-job-queues-schedule-tasks.md).  

> [!NOTE]  
> La información de la ficha **Unidad de almacenamiento** tiene prioridad sobre la ficha de **Producto**.

> [!Warning]
> Si UA se suministra a través de producción, el campo **Coste estándar** no se usa al facturar y ajustar el coste real del producto fabricado. En su lugar, [!INCLUDE [prod_short](includes/prod_short.md)] utiliza el valor del campo **Coste estándar** de la ficha subyacente de producto, y cualquier desviación se calcula con el reparto de costes de dicho producto.<br><br>
> Si bien puede asingar L.M. de producción y rutas a UA, la distribución del coste unitario y el cálculo relacionado de la parte de costes no están disponibles en UA. Para obtener más información sobre costes estándar, vaya a [Acerca del cálculo del coste estándar](finance-about-calculating-standard-cost.md)

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Consultar la [formación de Microsoft](/training/modules/control-inventory-multiple-locations/) relacionada

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Consulte también .

[Registro de productos nuevos](inventory-how-register-new-items.md)  
[Configuración de Warehouse Management](warehouse-setup-warehouse.md)  
[Información general de la gestión de almacenes](design-details-warehouse-management.md)
[Inventario](inventory-manage-inventory.md)  
[Gestión de ensamblaje](assembly-assemble-items.md)    
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
