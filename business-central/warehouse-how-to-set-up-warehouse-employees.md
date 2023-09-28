---
title: Configurar los empleados de almacén
description: Cada usuario que desarrolla actividades en el almacén debe estar configurado como empleado de almacén asignado a una ubicación predeterminada y otras ubicaciones potenciales no predeterminadas.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 03/09/2023
ms.custom: bap-template
ms.search.form: '7328, 7348'
---
# <a name="set-up-warehouse-employees"></a>Configurar los empleados de almacén

Cada usuario que desarrolla actividades en el almacén debe estar configurado como empleado de almacén y estar asignado a una ubicación predeterminada. [!INCLUDE [prod_short](includes/prod_short.md)] filtra las actividades del almacén a la ubicación predeterminada del empleado. Solo pueden realizar las actividades de almacén en la ubicación. También puede asignar a un usuario a otros almacenes. Pueden acceder pero no realizar actividades en esos lugares.

## <a name="to-set-up-warehouse-employees"></a>Para configurar los empleados de almacén

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Empleados de almacén** y luego elija el enlace relacionado.  
2. Seleccione la acción **Nuevo**.  
3. Seleccione el campo **Id. usuario**, y seleccione al usuario que se desea agregar como empleado de almacén. Elija el botón **Aceptar**.  
4. En el campo **Cód. almacén**, especifique el código de la ubicación en la que trabajará el usuario.  
5. Active el conmutador **Predeterminado** para especificar que la ubicación es la única en la que el empleado puede realizar actividades de almacén.  
6. Repita estos pasos para asignar otros empleados a ubicaciones o para asignar otras ubicaciones a empleados de almacén existentes.  

## <a name="see-also"></a>Consulte también .

[Información general de la gestión de almacenes](design-details-warehouse-management.md)
[Inventario](inventory-manage-inventory.md)  
[Configuración de Warehouse Management](warehouse-setup-warehouse.md)  
[Gestión de ensamblaje](assembly-assemble-items.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Definir una directiva de registro de facturas para usuarios](admin-setup-invoice-posting-policy.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
