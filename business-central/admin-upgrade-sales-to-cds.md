---
title: Actualización de una integración con Dynamics 365 Sales
description: Este tema explica cómo mover su integración de Dynamics 365 Business Central con Dynamics 365 Sales a la última versión.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'sales, crm, integration, integrating'
ms.date: 06/14/2021
ms.author: bholtorf
---
# <a name="upgrading-an-integration-with-dynamics-365-sales" />Actualización de una integración con Dynamics 365 Sales
[!INCLUDE[prod_short](includes/prod_short.md)] se integra con [!INCLUDE[prod_short](includes/cds_long_md.md)], lo que facilita la conexión y sincronización de datos con otras aplicaciones de Dynamics 365, como [!INCLUDE[crm_md](includes/crm_md.md)], o incluso aplicaciones que crea usted mismo. Si está integrando por primera vez, le recomendamos que lo haga a través de [!INCLUDE[prod_short](includes/cds_long_md.md)]. Para obtener más información, vea [Integración con Dataverse](admin-common-data-service.md).

Si ya ha integrado [!INCLUDE[crm_md](includes/crm_md.md)] con [!INCLUDE[prod_short](includes/prod_short.md)], puede continuar sincronizando datos utilizando su configuración. Sin embargo, si actualiza [!INCLUDE[prod_short](includes/prod_short.md)] o desactiva la integración de [!INCLUDE[crm_md](includes/crm_md.md)], para activarla de nuevo debe conectarse a través de [!INCLUDE[prod_short](includes/cds_long_md.md)]. 

> [!NOTE]
> La reconexión a través de [!INCLUDE[prod_short](includes/cds_long_md.md)] aplicará la configuración de sincronización predeterminada y sobrescribirá cualquier configuración que tenga. Por ejemplo, se aplicarán las asignaciones de tabla predeterminadas.

## <a name="to-upgrade-your-connection-to-use-dataverse" />Para actualizar su conexión para usar Dataverse
1. Abra la página **Configuración de conexión de Microsoft Dynamics 365** y desactive **Habilitado**. Luego cierre la página para desconectarse de [!INCLUDE[crm_md](includes/crm_md.md)].
2. Abre la página **Configuración de conexión de Dataverse** y en el campo **Modelo de propiedad**, elija **Persona**. Luego elija el botón de alternancia **Habilitado** para activar la conexión con [!INCLUDE[prod_short](includes/cds_long_md.md)].
  
   > [!NOTE]
   > Después de habilitar la conexión, la solución de integración base de Business Central se implementa en Dataverse.
4. En la página **Configuración de conexión de Microsoft Dynamics 365**, elija **Volver a implementar la solución de integración** para volver a instalar la solución de integración de Business Central.
5. Active el botón de alternancia **Habilitado** para volver a conectarse a [!INCLUDE[crm_md](includes/crm_md.md)].
  
   > [!NOTE]
   > Después de habilitar la conexión, la solución de integración base de Business Central se implementa en [!INCLUDE[prod_short](includes/prod_short.md)]. Esto permite la integración con tablas que son específicas de [!INCLUDE[crm_md](includes/crm_md.md)], como pedidos de ventas, presupuestos y facturas.
6. En la página **Configuración de conexión de Sales**, elija **Usar configuración de sincronización predeterminada** para inicializar las asignaciones de tablas de integración para [!INCLUDE[crm_md](includes/crm_md.md)].

   > [!IMPORTANT]
   > El uso de la acción **Usar la configuración de sincronización predeterminada** aplicará las asignaciones predeterminadas de la tabla de integración. Se sobrescribirán todas las asignaciones personalizadas. Si tiene asignaciones personalizadas que desea conservar, le recomendamos que las exporte a Excel o hable con su socio de Microsoft sobre otras formas de mantener sus asignaciones personalizadas.    

## <a name="see-also" />Consulte también
[Integración con Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Integración con Microsoft Dataverse](admin-common-data-service.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
