---
title: Uso de Microsoft Dataverse
description: Introducción a cómo integrar y utilizar Microsoft Dataverse y sus componentes para conectarse a otras aplicaciones de Dynamics 365.
author: bholtorf
ms.author: bholtorf
ms.custom: na
ms.reviewer: na
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 06/14/2021
ms.openlocfilehash: 9555ce9f7a072376b38a0be460b74c46f2b3f3f9
ms.sourcegitcommit: 1508643075dafc25e9c52810a584b8df1d14b1dc
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/28/2022
ms.locfileid: "8049482"
---
# <a name="integrating-with-microsoft-dataverse"></a>Integración con Microsoft Dataverse


Las aplicaciones empresariales a menudo usan datos de más de un origen. [!INCLUDE[prod_short](includes/cds_long_md.md)] combina datos en un solo conjunto de lógica que facilita la conexión de otras aplicaciones de Dynamics 365, como [!INCLUDE[crm_md](includes/crm_md.md)] o su propia aplicación construida sobre [!INCLUDE[prod_short](includes/cds_long_md.md)], a [!INCLUDE[prod_short_md](includes/prod_short.md)]. Para obtener más información sobre [!INCLUDE[prod_short](includes/cds_long_md.md)], consulte [Qué es Dataverse](/powerapps/maker/common-data-service/data-platform-intro).

Los pasos siguientes proporcionan una visión general de los pasos de la integración de [!INCLUDE[prod_short](includes/cds_long_md.md)] con [!INCLUDE[prod_short](includes/prod_short.md)]

> [!Note]  
> Estas tareas requieren el rol de seguridad **Administrador del sistema** en [!INCLUDE[prod_short](includes/cds_long_md.md)] y [!INCLUDE[prod_short](includes/prod_short.md)].  

1. Asignar las licencias de [!INCLUDE[prod_short](includes/cds_long_md.md)] a los usuarios de [!INCLUDE[prod_short](includes/prod_short.md)] que utilizarán las aplicaciones integradas.

2. Configure una conexión a [!INCLUDE[prod_short](includes/cds_long_md.md)]. Para obtener más información, vea [Conectar a Dataverse](admin-how-to-set-up-a-dynamics-crm-connection.md).  

3. Sincronice los datos entre las aplicaciones. Para obtener más información, consulte [Sincronización de Business Central y Dataverse](admin-synchronizing-business-central-and-sales.md). 

## <a name="getting-started-with-prod_short"></a>Introducción a [!INCLUDE[prod_short](includes/cds_long_md.md)]
Para comenzar con [!INCLUDE[prod_short](includes/cds_long_md.md)] necesitará una cuenta de Microsoft Power Apps. Si aún no tiene una cuenta de Power Apps, puede obtener una gratis visitando [powerapps.com](https://make.powerapps.com/?utm_source=padocs&utm_medium=linkinadoc&utm_campaign=referralsfromdoc) y eligiendo el vínculo **Comenzar gratis**. Para obtener más información sobre cómo comenzar con [!INCLUDE[prod_short](includes/cds_long_md.md)], consulte el módulo [Empezar con Dataverse](/learn/modules/get-started-with-powerapps-common-data-service/) de Microsoft Learn.

## <a name="bi-directional-or-uni-directional-data-synchronization"></a>Sincronización de datos bidireccional o unidireccional
Dependiendo de las necesidades de su negocio, puede configurar la integración para sincronizar datos, hasta o desde una aplicación comercial de Dynamics 365 hasta otra o en ambas direcciones casi en tiempo real a través de [!INCLUDE[prod_short](includes/cds_long_md.md)]. Por ejemplo, si integra [!INCLUDE[prod_short](includes/prod_short.md)] con [!INCLUDE[crm_md](includes/crm_md.md)] mediante [!INCLUDE[prod_short](includes/cds_long_md.md)], un vendedor puede crear un pedido de ventas en [!INCLUDE[crm_md](includes/crm_md.md)] y el pedido se sincronizará con [!INCLUDE[prod_short](includes/prod_short.md)]. Por el contrario, desde [!INCLUDE[crm_md](includes/crm_md.md)], el vendedor puede ver información de [!INCLUDE[prod_short](includes/prod_short.md)] sobre la disponibilidad del artículo en el pedido. 

## <a name="standard-and-custom-entities"></a>Entidades estándar y personalizadas
[!INCLUDE[prod_short](includes/cds_long_md.md)] almacena de forma segura los datos en un conjunto de tablas, que son conjuntos de registros similares a cómo una tabla almacena datos dentro de una base de datos. [!INCLUDE[prod_short](includes/cds_long_md.md)] incluye un conjunto básico de tablas estándar que cubren escenarios típicos, pero también puede crear tablas personalizadas específicas de su organización. En [!INCLUDE[prod_short](includes/prod_short.md)], puede ver las tablas estándar y personalizadas que se sincronizan en la página Asignaciones de tablas de integración.

## <a name="about-the-business-central-base-integration-solution"></a>Acerca de la solución de integración base de Business Central

La solución de integración base es un componente clave de la integración. La solución agrega los roles y los niveles de acceso requeridos a las cuentas de usuario para la integración y crea las tablas necesarias para asignar la empresa de [!INCLUDE[prod_short](includes/prod_short.md)] a la unidad de negocio en [!INCLUDE[prod_short](includes/cds_long_md.md)]. 

De forma predeterminada, la guía de configuración asistida **Configurar la conexión de [!INCLUDE[prod_short](includes/cds_long_md.md)]** importará la solución. Para ello, la guía de configuración utiliza la cuenta de usuario de administrador que especifique. Esta cuenta debe ser un usuario válido de [!INCLUDE[prod_short](includes/cds_long_md.md)] con el rol de seguridad siguiente:

* Administrador del sistema  

Para obtener más información, consulte [Configuración de cuentas de usuario para la integración con [!INCLUDE[prod_short](includes/cds_long_md.md)]](admin-setting-up-integration-with-dynamics-sales.md) y [Crear usuarios en Microsoft Dynamics 365 (online) y asignar roles de seguridad](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles). 

La cuenta de administrador se usa solo una vez durante la instalación de los cambios en la configuración que realiza la solución de integración base en [!INCLUDE[prod_short](includes/cds_long_md.md)]. Después que la solución se importa, la cuenta ya no se necesita. La integración continuará utilizando la cuenta de usuario creada automáticamente para la integración.

Además de la personalización de [!INCLUDE[prod_short](includes/cds_long_md.md)], la solución de integración también crea los siguientes roles en [!INCLUDE[prod_short](includes/cds_long_md.md)] para la integración:

* **Administrador de integración**: permite a los usuarios administrar la conexión entre [!INCLUDE[prod_short](includes/prod_short.md)] y [!INCLUDE[prod_short](includes/cds_long_md.md)]. Normalmente, solo se asigna a la cuenta de usuario creada automáticamente para la sincronización.  
* **Usuario de integración**: permite a los usuarios acceder a los datos sincronizados. Normalmente, se asigna a la cuenta de usuario creada automáticamente para la sincronización y a otros usuarios que necesiten ver los datos sincronizados o acceder a ellos.

Para obtener más información sobre cada rol, como los permisos y los niveles de acceso, consulte [Configuración de cuentas de usuario para la integración con [!INCLUDE[prod_short](includes/cds_long_md.md)]](admin-setting-up-integration-with-dynamics-sales.md).

Durante la configuración de la conexión, se crean asignaciones de tablas de integración que son necesarias para sincronizar datos. Las entidades de [!INCLUDE[prod_short](includes/cds_long_md.md)] se asignan a tablas y campos de tabla en Business Central a través de tablas de integración. Para obtener más información, consulte [Asignación de entidad estándar para la sincronización](admin-synchronizing-business-central-and-sales.md#standard-table-mapping-for-synchronization).

## <a name="see-also"></a>Consulte también
[Modelos de propiedad de datos](admin-cds-company-concept.md)  
<!--needs to be removed as this is moved to dev-itpro docs[Walkthrough: Customizing an Integration with Dataverse](\dynamics365\business-central\dev-itpro\administration\administration-custom-cds-integration) -->





[!INCLUDE[footer-include](includes/footer-banner.md)]