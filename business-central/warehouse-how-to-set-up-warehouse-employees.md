---
title: Configurar empleados almacén | Documentos de Microsoft
description: Cada usuario que desarrolla actividades en el almacén debe estar configurado como empleado de almacén asignado a una ubicación predeterminada y otras ubicaciones potenciales no predeterminadas.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: a64aad29b9b4214a737cbda81b040b8df66b67d3
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5382284"
---
# <a name="set-up-warehouse-employees"></a>Configurar los empleados de almacén
Cada usuario que desarrolla actividades en el almacén debe estar configurado como empleado de almacén asignado a una ubicación predeterminada y otras ubicaciones potenciales no predeterminadas. Esta configuración de usuario filtra todas las actividades del almacén de la base de datos hasta la ubicación del empleado, de modo que éste sólo puede realizar las actividades de almacén de la ubicación predeterminada. Se puede asignar un usuario a otras ubicaciones no predeterminadas para las que el empleado podrá ver las líneas de la actividad, pero no realizar las actividades.

## <a name="to-set-up-warehouse-employees"></a>Para configurar los empleados de almacén  
1.  Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Empleados de almacén** y luego elija el enlace relacionado.  
2. Seleccione la acción **Nuevo**.  
3. Seleccione el campo **Id. usuario**, y seleccione al usuario que se desea agregar como empleado de almacén. Elija el botón **Aceptar**.  
6.  En el campo **Cód. almacén**, especifique el código de la ubicación en la que trabajará el usuario.  
7.  Seleccione la casilla de verificación **Predeterminada** para definir la ubicación como la única en la que el empleado puede realizar actividades de almacén.  
8.  Repita estos pasos para asignar otros empleados a ubicaciones o para asignar ubicaciones no predeterminadas a empleados de almacén existentes.  

## <a name="see-also"></a>Consulte también  
[Gestión almacén](warehouse-manage-warehouse.md)  
[Grupos contables inventario](inventory-manage-inventory.md)  
[Configuración de la gestión del almacén](warehouse-setup-warehouse.md)     
[Gestión de ensamblaje](assembly-assemble-items.md)    
[Detalles de diseño: Gestión de almacén](design-details-warehouse-management.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]