---
title: Actualización de una integración con Dynamics 365 Sales | Microsoft Docs
description: Obtenga información sobre cómo preparar Dynamics 365 Business Central para integrarse con Dynamics 365 Sales.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, integrating
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 57bb8d6ee48b608074a669109bdd99abf8c452c2
ms.sourcegitcommit: 351eb465e6dfb3d01c0f3ea406db340f393f47fc
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/01/2020
ms.locfileid: "3742840"
---
# <a name="upgrading-an-integration-with-dynamics-365-sales"></a>Actualización de una integración con Dynamics 365 Sales
[!INCLUDE[d365fin](includes/d365fin_md.md)] se integra con [!INCLUDE[d365fin](includes/cds_long_md.md)], lo que facilita la conexión y sincronización de datos con otras aplicaciones de Dynamics 365, como [!INCLUDE[crm_md](includes/crm_md.md)], o incluso aplicaciones que crea usted mismo. Si está integrando por primera vez, le recomendamos que lo haga a través de [!INCLUDE[d365fin](includes/cds_long_md.md)]. Para obtener más información, vea [Integración con Common Data Service](admin-common-data-service.md).

Si ya ha integrado [!INCLUDE[crm_md](includes/crm_md.md)] con [!INCLUDE[d365fin](includes/d365fin_md.md)], puede continuar sincronizando datos utilizando su configuración. Sin embargo, si actualiza [!INCLUDE[d365fin](includes/d365fin_md.md)] o desactiva la integración de [!INCLUDE[crm_md](includes/crm_md.md)], para activarla de nuevo debe conectarse a través de [!INCLUDE[d365fin](includes/cds_long_md.md)]. 

> [!NOTE]
> La reconexión a través de [!INCLUDE[d365fin](includes/cds_long_md.md)] aplicará la configuración de sincronización predeterminada y sobrescribirá cualquier configuración que tenga. Por ejemplo, se aplicarán las asignaciones de tabla predeterminadas.

## <a name="to-upgrade-your-connection-to-use-common-data-service"></a>Para actualizar su conexión para usar Common Data Service
1. Abra la página **Configuración de conexión de Microsoft Dynamics 365** y elija **Habilitar** para desactivar la conexión existente con [!INCLUDE[crm_md](includes/crm_md.md)].
2. Abra la página **Configuración de conexión de Common Data Service** y elija **Habilitar** para activar la conexión.
  
   Después de habilitar la conexión CDS, la solución de integración base de CDS de Business Central se implementa en Common Data Service.
3. Desinstalar la solución de integración de Microsoft Dynamics 365 Business Central desde Dynamics 365 Sales. Para más información, ver [Desinstale o elimine un tema de solución](/powerapps/developer/common-data-service/uninstall-delete-solution). 

4. En la página **Configuración de conexión de Microsoft Dynamics 365**, elija **Habilitar** para conectarse a [!INCLUDE[crm_md](includes/crm_md.md)].
  
   Después de habilitar la conexión a Sales, la solución de integración de Business Central se implementa en Sales. Esto permite la integración con entidades que son específicas de [!INCLUDE[crm_md](includes/crm_md.md)], como pedidos de ventas, presupuestos y facturas.
5. En la página **Configuración de conexión de Sales**, elija **Usar configuración de sincronización predeterminada** para inicializar las asignaciones de tablas de integración para [!INCLUDE[crm_md](includes/crm_md.md)].

## <a name="see-also"></a>Consulte también
[Integración con Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Integración con Common Data Service](admin-common-data-service.md)
