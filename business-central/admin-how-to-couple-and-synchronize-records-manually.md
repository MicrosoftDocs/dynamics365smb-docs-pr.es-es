---
title: Emparejar y sincronizar registros manualmente| Documentos de Microsoft
description: La sincronización de una asignación de tablas de integración permite la sincronización de datos de todos los registros de una tabla de Business Central y de la entidad de Dynamics 365 Sales que están emparejadas.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: crm, sales, couple, decouple, synchronize
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 0c70b1ba34af32b7cf542149c8f15cb191761358
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2019
ms.locfileid: "2308121"
---
# <a name="couple-and-synchronize-records-manually"></a>Emparejar y sincronizar registros manualmente
En este tema se describe cómo emparejar uno o más registros de [!INCLUDE[d365fin](includes/d365fin_md.md)] con registros de [!INCLUDE[crm_md](includes/crm_md.md)]. El emparejamiento de registros le permite ver información de [!INCLUDE[crm_md](includes/crm_md.md)] desde [!INCLUDE[d365fin](includes/d365fin_md.md)], y viceversa. El emparejamiento también le permite sincronizar datos entre los registros. Puede emparejar registros existentes o crear y emparejar nuevos registros.

> [!Note]
> El emparejamiento y la sincronización de datos con [!INCLUDE[crm_md](includes/crm_md.md)] solo están disponibles si el administrador del sistema ha creado una conexión entre [!INCLUDE[d365fin](includes/d365fin_md.md)] y [!INCLUDE[crm_md](includes/crm_md.md)]. Una forma rápida de comprobarlo es abrir la ficha **Cliente** y buscar la acción **Configurar emparejamiento**. Si la acción está disponible, las aplicaciones se conectan.   

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098376]

## <a name="to-couple-a-record"></a>Para emparejar un registro  
1.  En [!INCLUDE[d365fin](includes/d365fin_md.md)], abra la tarjeta para el registro que desea emparejar. Por ejemplo, la tarjeta Cliente o Contacto.  

    También puede abrir simplemente la página de lista y seleccionar el registro que desee emparejar.  

2.  Seleccione la acción **Configurar emparejamiento**.  
3.  Rellene los campos y, a continuación, elija **Aceptar**.  

## <a name="to-synchronize-a-single-record"></a>Para sincronizar un solo registro  
1.  En [!INCLUDE[d365fin](includes/d365fin_md.md)], abra la tarjeta para el registro que desea emparejar. Por ejemplo, la tarjeta Cliente o Contacto.  
2.  Seleccione la acción **Sincronizar ahora**.  
3.  Si un registro se puede sincronizar desde [!INCLUDE[d365fin](includes/d365fin_md.md)] a [!INCLUDE[crm_md](includes/crm_md.md)] o desde [!INCLUDE[crm_md](includes/crm_md.md)] a [!INCLUDE[d365fin](includes/d365fin_md.md)], seleccione la opción que especifica la dirección de actualización de datos y, a continuación, seleccione **Aceptar**.  

## <a name="to-synchronize-multiple-records"></a>Para sincronizar varios registros  
1.  En el cliente de [!INCLUDE[d365fin](includes/d365fin_md.md)], abra la página de lista para el registro, como las páginas de lista Clientes o Contactos.  
2.  Seleccione los registros que desea sincronizar y, después, seleccione la acción **Sincronizar ahora**.  
3.  Si los registros se pueden sincronizar desde [!INCLUDE[d365fin](includes/d365fin_md.md)] a [!INCLUDE[crm_md](includes/crm_md.md)] o desde [!INCLUDE[crm_md](includes/crm_md.md)] a [!INCLUDE[d365fin](includes/d365fin_md.md)], seleccione la opción que especifica la dirección de actualización de datos y, a continuación, seleccione **Aceptar**.  

## <a name="see-also"></a>Consulte también  
[Uso de Dynamics 365 Sales desde Business Central](marketing-integrate-dynamicscrm.md)
