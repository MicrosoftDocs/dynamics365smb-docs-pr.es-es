---
title: Emparejamiento y sincronización (contiene vídeo)
description: La sincronización de una asignación de tablas de integración permite la sincronización de datos de todos los registros de una tabla de Business Central y de la tabla de Dynamics 365 Sales que están emparejadas.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: crm, sales, couple, decouple, synchronize
ms.search.form: 6250
ms.date: 10/01/2021
ms.author: bholtorf
ms.openlocfilehash: c7d62f1122aee1930dd98ed008b7820e88fe9b14
ms.sourcegitcommit: c05806689d289d101bd558696199cefbd989473e
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/12/2022
ms.locfileid: "8115425"
---
# <a name="coupling-and-synchronizing-records-between-dataverse-and-business-central"></a>Emparejamiento y sincronización de registros entre Dataverse y Business Central

En este tema se describe cómo emparejar uno o más registros de [!INCLUDE[prod_short](includes/prod_short.md)] con registros de Dataverse o [!INCLUDE[crm_md](includes/crm_md.md)]. El emparejamiento de registros le permite ver información de Dataverse desde [!INCLUDE[prod_short](includes/prod_short.md)], y viceversa. El emparejamiento también le permite sincronizar datos entre los registros. Puede emparejar registros existentes o crear y emparejar nuevos registros.

> [!Note]
> El emparejamiento y la sincronización de datos solo están disponibles si el administrador del sistema ha creado una conexión entre [!INCLUDE[prod_short](includes/prod_short.md)] y Dataverse o [!INCLUDE[crm_md](includes/crm_md.md)]. Una forma rápida de comprobarlo es abrir la ficha **Cliente** y buscar la acción **Configurar emparejamiento**. Si la acción está disponible, las aplicaciones se conectan.   

## <a name="video-example"></a>Ejemplo de video
Este video muestra el acoplamiento y la sincronización de datos en el contexto de una integración con [!INCLUDE[crm_md](includes/crm_md.md)].

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098376]

## <a name="to-couple-a-record"></a>Para emparejar un registro  
1.  En [!INCLUDE[prod_short](includes/prod_short.md)], abra la tarjeta para el registro que desea emparejar. Por ejemplo, la tarjeta Cliente o Contacto.  

    También puede abrir simplemente la página de lista y seleccionar el registro que desee emparejar.  

2.  Seleccione la acción **Configurar emparejamiento**.  
3.  Rellene los campos y, a continuación, elija **Aceptar**.  

## <a name="to-synchronize-a-single-record"></a>Para sincronizar un solo registro  
1.  En [!INCLUDE[prod_short](includes/prod_short.md)], abra la tarjeta para el registro que desea emparejar. Por ejemplo, la tarjeta Cliente o Contacto.  
2.  Seleccione la acción **Sincronizar ahora**.  
3.  Si un registro se puede sincronizar en una dirección, seleccione la opción que especifica la dirección de actualización de datos y, a continuación, seleccione **Aceptar**.  

## <a name="to-synchronize-a-single-record-from-crm_md"></a>Para sincronizar un solo registro en [!INCLUDE[crm_md](includes/crm_md.md)]  
1.  En [!INCLUDE[crm_md](includes/crm_md.md)], abra el formulario para el registro que desea emparejar. Por ejemplo, el formulario Tarjeta de cuenta o Tarjeta de contacto.  
2.  Elija la acción **[!INCLUDE[prod_short](includes/prod_short.md)]** en la cinta para abrir y emparejar el registro automáticamente.

> [!Note]
> Puede sincronizar un solo registro desde [!INCLUDE[crm_md](includes/crm_md.md)] automáticamente solo cuando **Sincronizar solo reg. emparejados** está deshabilitado y la dirección de sincronización se establece en Bidireccional o Desde la tabla de integración en la página **Asignación de tabla de integración** para el registro. Para más información, vea [Asignación de tablas y campos para sincronizar](admin-how-to-modify-table-mappings-for-synchronization.md#creating-new-records).     

## <a name="to-couple-multiple-records-using-match-based-coupling"></a>Para emparejar varios registros mediante el emparejamiento basado en coincidencias

Puede especificar los datos que se sincronizarán para una entidad, como un cliente o un contacto, mediante el emparejamiento de registros basado en coincidencias. Puede acotar las coincidencias haciendo que la búsqueda distinga entre mayúsculas y minúsculas y asignando una prioridad para cada coincidencia. Si no se encuentra ninguna coincidencia, también puede especificar que desea crear la entidad en Dataverse. Para más información, vea [Personalizar emparejamiento basado en coincidencias](admin-how-to-set-up-a-dynamics-crm-connection.md#customize-the-match-based-coupling).  

1. En el cliente de [!INCLUDE[prod_short](includes/prod_short.md)], abra la página de lista para el registro, como las páginas de lista Clientes o Contactos.
2. Elija la acción **Emparejamiento basado en coincidencias**.
3. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-synchronize-multiple-records"></a>Para sincronizar varios registros  
1.  En el cliente de [!INCLUDE[prod_short](includes/prod_short.md)], abra la página de lista para el registro, como las páginas de lista Clientes o Contactos.  
2.  Seleccione los registros que desea sincronizar y, después, seleccione la acción **Sincronizar ahora**.  
3.  Si los registros se pueden sincronizar en una dirección, seleccione la opción que especifica la dirección y, a continuación, seleccione **Aceptar**.  

## <a name="uncoupling-records"></a>Desemparejamiento de registros
Puede desacoplar uno o más registros de las páginas de lista o la página **Errores de sincronización de datos acoplados** eligiendo una o más líneas y eligiendo **Eliminar acoplamiento**. También puede eliminar todos los acoplamientos para una o más asignaciones de tabla en la página **Asignaciones de tablas de integración**.

## <a name="see-also"></a>Consulte también  
[Uso de Dynamics 365 Sales desde Business Central](marketing-integrate-dynamicscrm.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]