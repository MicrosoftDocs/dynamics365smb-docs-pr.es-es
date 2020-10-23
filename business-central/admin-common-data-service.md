---
title: Uso de Common Data Service
description: Introducción a Common Data Service y sus componentes.
author: bholtorf
ms.author: bholtorf
ms.custom: na
ms.reviewer: na
ms.service: dynamics365-business-central
ms.topic: article
ms.date: 10/01/2020
ms.openlocfilehash: 85823e93b1d239bf4e59ec6a8872cdc4a2cef9c1
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2020
ms.locfileid: "3911585"
---
# <a name="integrating-with-common-data-service"></a>Integración con Common Data Service

Las aplicaciones empresariales a menudo usan datos de más de un origen. [!INCLUDE[d365fin](includes/cds_long_md.md)] combina datos en un solo conjunto de lógica que facilita la conexión de otras aplicaciones de Dynamics 365, como [!INCLUDE[crm_md](includes/crm_md.md)] o su propia aplicación construida sobre [!INCLUDE[d365fin](includes/cds_long_md.md)], a [!INCLUDE[d365fin_md](includes/d365fin_md.md)]. Para obtener más información sobre [!INCLUDE[d365fin](includes/cds_long_md.md)], consulte [Qué es Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro).

Los pasos siguientes proporcionan una visión general de los pasos de la integración de [!INCLUDE[d365fin](includes/cds_long_md.md)] con [!INCLUDE[d365fin](includes/d365fin_md.md)]

> [!Note]  
> Estas tareas requieren el rol de seguridad **Administrador del sistema** en [!INCLUDE[d365fin](includes/cds_long_md.md)] y [!INCLUDE[d365fin](includes/d365fin_md.md)].  

1. Asignar las licencias de [!INCLUDE[d365fin](includes/cds_long_md.md)] a los usuarios de [!INCLUDE[d365fin](includes/d365fin_md.md)] que utilizarán las aplicaciones integradas.

2. Configure una conexión a [!INCLUDE[d365fin](includes/cds_long_md.md)]. Para obtener más información, vea [Conectar a Common Data Service](admin-how-to-set-up-a-dynamics-crm-connection.md).  

3. Sincronice los datos entre las aplicaciones. Para obtener más información, consulte [Sincronización de Business Central y Common Data Service](admin-synchronizing-business-central-and-sales.md). 

## <a name="getting-started-with-d365fin"></a>Introducción a [!INCLUDE[d365fin](includes/cds_long_md.md)]
Para comenzar con [!INCLUDE[d365fin](includes/cds_long_md.md)] necesitará una cuenta de Microsoft Power Apps. Si aún no tiene una cuenta de Power Apps, puede obtener una gratis visitando [powerapps.com](https://web.powerapps.com/?utm_source=padocs&utm_medium=linkinadoc&utm_campaign=referralsfromdoc) y eligiendo el vínculo **Comenzar gratis**. Para obtener más información sobre cómo comenzar con [!INCLUDE[d365fin](includes/cds_long_md.md)], vea el módulo [Empezar con Common Data Service](https://docs.microsoft.com/learn/modules/get-started-with-powerapps-common-data-service/) de Microsft Learn.

## <a name="bi-directional-or-uni-directional-data-synchronization"></a>Sincronización de datos bidireccional o unidireccional
Dependiendo de las necesidades de su negocio, puede configurar la integración para sincronizar datos, hasta o desde una aplicación comercial de Dynamics 365 hasta otra o en ambas direcciones casi en tiempo real a través de [!INCLUDE[d365fin](includes/cds_long_md.md)]. Por ejemplo, si integra [!INCLUDE[d365fin](includes/d365fin_md.md)] con [!INCLUDE[crm_md](includes/crm_md.md)] mediante [!INCLUDE[d365fin](includes/cds_long_md.md)], un vendedor puede crear un pedido de ventas en [!INCLUDE[crm_md](includes/crm_md.md)] y el pedido se sincronizará con [!INCLUDE[d365fin](includes/d365fin_md.md)]. Por el contrario, desde [!INCLUDE[crm_md](includes/crm_md.md)], el vendedor puede ver información de [!INCLUDE[d365fin](includes/d365fin_md.md)] sobre la disponibilidad del artículo en el pedido. 

## <a name="standard-and-custom-entities"></a>Entidades estándar y personalizadas
[!INCLUDE[d365fin](includes/cds_long_md.md)] almacena de forma segura los datos en un conjunto de entidades, que son conjuntos de registros similares a cómo una tabla almacena datos dentro de una base de datos. [!INCLUDE[d365fin](includes/cds_long_md.md)] incluye un conjunto básico de entidades estándar que cubren escenarios típicos, pero también puede crear entidades personalizadas específicas de su organización. En [!INCLUDE[d365fin](includes/d365fin_md.md)], puede ver las entidades estándar y personalizadas que se sincronizan en la página Asignaciones de tablas de integración.

## <a name="about-the-base-cds-integration-solution"></a>Acerca de la solución de integración de CDS base

La solución de integración CDS base es un componente clave de la integración. La solución agrega los roles y los niveles de acceso requeridos a las cuentas de usuario para la integración y crea las entidades necesarias para asignar la empresa de [!INCLUDE[d365fin](includes/d365fin_md.md)] a la unidad de negocio en [!INCLUDE[d365fin](includes/cds_long_md.md)]. 

De forma predeterminada, la guía de configuración asistida **Configurar la conexión de [!INCLUDE[d365fin](includes/cds_long_md.md)]** importará la solución. Para ello, la guía de configuración utiliza la cuenta de usuario de administrador que especifique. Esta cuenta debe ser un usuario válido de [!INCLUDE[d365fin](includes/cds_long_md.md)] con el rol de seguridad siguiente:

* Administrador del sistema  

Para obtener más información, consulte [Configuración de cuentas de usuario para la integración con [!INCLUDE[d365fin](includes/cds_long_md.md)]](admin-setting-up-integration-with-dynamics-sales.md) y [Crear usuarios en Microsoft Dynamics 365 (online) y asignar roles de seguridad](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles). 

La cuenta de administrador se usa solo una vez durante la instalación debido a cambios en la configuración que está realizando la solución CDS base en [!INCLUDE[d365fin](includes/cds_long_md.md)]. Después que la solución se importa, la cuenta ya no se necesita. La integración continuará utilizando la cuenta de usuario creada automáticamente para la integración.

Además de la personalización de [!INCLUDE[d365fin](includes/cds_long_md.md)], la solución de integración también crea los siguientes roles en [!INCLUDE[d365fin](includes/cds_long_md.md)] para la integración:

* **Administrador de integración**: permite a los usuarios administrar la conexión entre [!INCLUDE[d365fin](includes/d365fin_md.md)] y [!INCLUDE[d365fin](includes/cds_long_md.md)]. Normalmente, solo se asigna a la cuenta de usuario creada automáticamente para la sincronización.  
* **Usuario de integración**: permite a los usuarios acceder a los datos sincronizados. Normalmente, se asigna a la cuenta de usuario creada automáticamente para la sincronización y a otros usuarios que necesiten ver los datos sincronizados o acceder a ellos.

Para obtener más información sobre cada rol, como los permisos y los niveles de acceso, consulte [Configuración de cuentas de usuario para la integración con [!INCLUDE[d365fin](includes/cds_long_md.md)]](admin-setting-up-integration-with-dynamics-sales.md).

Durante la configuración de la conexión, se crean asignaciones de tablas de integración que son necesarias para sincronizar datos. Las entidades de Common Data Service se asignan a tablas y campos de tabla en Business Central a través de tablas de integración. Para obtener más información, consulte [Asignación de entidad estándar para la sincronización](admin-synchronizing-business-central-and-sales.md#standard-entity-mapping-for-synchronization).

## <a name="see-also"></a>Consulte también
[Modelos de propiedad de datos](admin-cds-company-concept.md)  
<!--needs to be removed as this is moved to dev-itpro docs[Walkthrough: Customizing an Integration with Common Data Service](docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/administration-custom-cds-integration) -->



