---
title: Actualización de una integración con Dynamics 365 Sales
description: Aprenda a mover su integración de Dynamics 365 Business Central con Dynamics 365 Sales a la última versión.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, integrating
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 4e3b79d6245a0f1b8277c94faa58c24edc66662e
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2021
ms.locfileid: "5777021"
---
# <a name="upgrading-an-integration-with-dynamics-365-sales"></a>Actualización de una integración con Dynamics 365 Sales
[!INCLUDE[prod_short](includes/prod_short.md)] se integra con [!INCLUDE[prod_short](includes/cds_long_md.md)], lo que facilita la conexión y sincronización de datos con otras aplicaciones de Dynamics 365, como [!INCLUDE[crm_md](includes/crm_md.md)], o incluso aplicaciones que crea usted mismo. Si está integrando por primera vez, le recomendamos que lo haga a través de [!INCLUDE[prod_short](includes/cds_long_md.md)]. Para obtener más información, vea [Integración con Dataverse](admin-common-data-service.md).

Si ya ha integrado [!INCLUDE[crm_md](includes/crm_md.md)] con [!INCLUDE[prod_short](includes/prod_short.md)], puede continuar sincronizando datos utilizando su configuración. Sin embargo, si actualiza [!INCLUDE[prod_short](includes/prod_short.md)] o desactiva la integración de [!INCLUDE[crm_md](includes/crm_md.md)], para activarla de nuevo debe conectarse a través de [!INCLUDE[prod_short](includes/cds_long_md.md)]. 

> [!NOTE]
> La reconexión a través de [!INCLUDE[prod_short](includes/cds_long_md.md)] aplicará la configuración de sincronización predeterminada y sobrescribirá cualquier configuración que tenga. Por ejemplo, se aplicarán las asignaciones de tabla predeterminadas.

## <a name="to-upgrade-your-connection-to-use-dataverse"></a>Para actualizar su conexión para usar Dataverse
1. Abra la página **Configuración de conexión de Microsoft Dynamics 365** y desactive el control de alternancia **Habilitar** para desconectarse de [!INCLUDE[crm_md](includes/crm_md.md)].
2. Abra la página **Configuración de conexión de Dataverse** y elija el control de alternancia **Habilitar** para activar la conexión a [!INCLUDE[prod_short](includes/cds_long_md.md)].
  
   > [!NOTE]
   > Después de habilitar la conexión, la solución de integración base de Business Central se implementa en Dataverse.
3. Elija **Volver a implementar la solución de integración** para reinstalar la Solución de integración de Business Central.
4. En la página **Configuración de conexión de Microsoft Dynamics 365**, elija el botón de alternancia **Habilitar** para reconectarse a [!INCLUDE[crm_md](includes/crm_md.md)].
  
   > [!NOTE]
   > Después de habilitar la conexión, la solución de integración base de Business Central se implementa en [!INCLUDE[prod_short](includes/prod_short.md)]. Esto permite la integración con tablas que son específicas de [!INCLUDE[crm_md](includes/crm_md.md)], como pedidos de ventas, presupuestos y facturas.
5. Elija **Volver a implementar la solución de integración** para reinstalar la Solución de integración de Business Central.
6. En la página **Configuración de conexión de Sales**, elija **Usar configuración de sincronización predeterminada** para inicializar las asignaciones de tablas de integración para [!INCLUDE[crm_md](includes/crm_md.md)].

## <a name="see-also"></a>Consulte también
[Integración con Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Integración con Microsoft Dataverse](admin-common-data-service.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]