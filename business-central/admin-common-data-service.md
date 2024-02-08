---
title: Integrar con Microsoft Dataverse mediante la sincronización de datos
description: Introducción a cómo integrar y utilizar Microsoft Dataverse y sus componentes para conectarse a otras aplicaciones de Dynamics 365.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: ivkoleti
ms.topic: conceptual
ms.date: 06/28/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# Integrar con Microsoft Dataverse mediante la sincronización de datos

Las aplicaciones empresariales a menudo usan datos de más de un origen. [!INCLUDE[prod_short](includes/cds_long_md.md)] combina datos en un solo conjunto de lógica que facilita la conexión de [!INCLUDE[prod_short](includes/prod_short.md)] a otras aplicaciones de Dynamics 365. Por ejemplo, [!INCLUDE[crm_md](includes/crm_md.md)] o su propia aplicación basada en [!INCLUDE[prod_short](includes/cds_long_md.md)]. Para obtener más información sobre [!INCLUDE[prod_short](includes/cds_long_md.md)], vaya a [¿Qué es Dataverse?](/powerapps/maker/common-data-service/data-platform-intro).

Los pasos siguientes proporcionan una visión general de los pasos de la integración de [!INCLUDE[prod_short](includes/cds_long_md.md)] con [!INCLUDE[prod_short](includes/prod_short.md)]

> [!Note]  
> Estas tareas requieren el rol de seguridad **Administrador del sistema** en [!INCLUDE[prod_short](includes/cds_long_md.md)] y [!INCLUDE[prod_short](includes/prod_short.md)].  

1. Asignar las licencias de [!INCLUDE[prod_short](includes/cds_long_md.md)] a los usuarios de [!INCLUDE[prod_short](includes/prod_short.md)] que utilizarán las aplicaciones integradas.

2. Configure una conexión a [!INCLUDE[prod_short](includes/cds_long_md.md)]. Para obtener más información, vea [Conectar a Dataverse](admin-how-to-set-up-a-dynamics-crm-connection.md).  

3. Sincronice los datos entre las aplicaciones. Para obtener más información, consulte [Sincronización de Business Central y Dataverse](admin-synchronizing-business-central-and-sales.md). 

## Introducción a [!INCLUDE[prod_short](includes/cds_long_md.md)]

Para comenzar con [!INCLUDE[prod_short](includes/cds_long_md.md)] necesitará una cuenta de Microsoft Power Apps. Si aún no tiene una cuenta de Power Apps, puede obtener una gratis visitando [powerapps.com](https://make.powerapps.com/?utm_source=padocs&utm_medium=linkinadoc&utm_campaign=referralsfromdoc) y eligiendo el vínculo **Comenzar gratis**. Para obtener más información sobre cómo comenzar con [!INCLUDE[prod_short](includes/cds_long_md.md)], vaya al módulo [Empezar con Dataverse](/training/modules/get-started-with-powerapps-common-data-service/) de la formación de Microsoft.

## Sincronización de datos bidireccional o unidireccional

Puede sincronizar datos, hasta o desde una aplicación comercial de Dynamics 365 hasta otra o en ambas direcciones casi en tiempo real a través de [!INCLUDE[prod_short](includes/cds_long_md.md)]. Por ejemplo, si integra [!INCLUDE[prod_short](includes/prod_short.md)] con [!INCLUDE[crm_md](includes/crm_md.md)], un vendedor puede crear un pedido de ventas en [!INCLUDE[crm_md](includes/crm_md.md)] y el pedido se sincronizará con [!INCLUDE[prod_short](includes/prod_short.md)]. Por el contrario, desde [!INCLUDE[crm_md](includes/crm_md.md)], el vendedor comprobar la disponibilidad del artículo en el pedido en [!INCLUDE[prod_short](includes/prod_short.md)]. 

## Entidades estándar y personalizadas

[!INCLUDE[prod_short](includes/cds_long_md.md)] almacena de forma segura los datos en un conjunto de tablas, que son conjuntos de registros similares a cómo una tabla almacena datos dentro de una base de datos. [!INCLUDE[prod_short](includes/cds_long_md.md)] incluye un conjunto básico de tablas estándar que cubren escenarios típicos, pero también puede crear tablas personalizadas específicas de su organización. En [!INCLUDE[prod_short](includes/prod_short.md)], puede ver las tablas estándar y personalizadas que se sincronizan en la página Asignaciones de tablas de integración.

## Acerca de la solución de integración base de Business Central

La solución de integración base es un componente clave de la integración. La solución agrega los roles y los niveles de acceso requeridos a las cuentas de usuario para la integración y crea las tablas necesarias para asignar la empresa de [!INCLUDE[prod_short](includes/prod_short.md)] a la unidad de negocio en [!INCLUDE[prod_short](includes/cds_long_md.md)]. 

De forma predeterminada, la guía de configuración asistida **Configurar la conexión de [!INCLUDE[prod_short](includes/cds_long_md.md)]** importará la solución. Para ello, la guía de configuración utiliza la cuenta de usuario de administrador que especifique. Esta cuenta debe ser un usuario válido de [!INCLUDE[prod_short](includes/cds_long_md.md)] con el rol de seguridad **Administrador del sistema**:  

Para obtener más información sobre las cuentas de usuario, consulte los siguientes artículos:

* [Configuración de cuentas de usuario para la integración con [!INCLUDE[prod_short](includes/cds_long_md.md)]](admin-setting-up-integration-with-dynamics-sales.md) 
* [Crear usuarios y asignar roles de seguridad de aplicaciones Microsoft Dynamics 365 (online)](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles). 

La cuenta de administrador se usa solo una vez durante la instalación de los cambios en la configuración que realiza la solución de integración base en [!INCLUDE[prod_short](includes/cds_long_md.md)]. Después que la solución se importa, la cuenta ya no se necesita. La integración continuará utilizando la cuenta de usuario creada automáticamente para la integración.

Además de la personalización de [!INCLUDE [cds_long_md](includes/cds_long_md.md)], la solución también crea un rol de seguridad en [!INCLUDE [cds_long_md](includes/cds_long_md.md)] para la integración:

* **Integración de Business Central y Dataverse**: permite a los usuarios administrar la conexión entre [!INCLUDE [prod_short](includes/prod_short.md)] y [!INCLUDE [cds_long_md](includes/cds_long_md.md)]. Normalmente, este rol se asigna a la cuenta de usuario creada automáticamente para la sincronización. Para obtener más información sobre esta función, vaya a [Configuración de cuentas de usuario para la integración con [!INCLUDE[prod_short](includes/cds_long_md.md)]](admin-setting-up-integration-with-dynamics-sales.md).

Cuando configura la conexión, crea asignaciones de tablas de integración que son necesarias para sincronizar datos. Las entidades de [!INCLUDE[prod_short](includes/cds_long_md.md)] se asignan a tablas y campos de tabla en [!INCLUDE [prod_short](includes/prod_short.md)] a través de tablas de integración. Para obtener más información sobre asignaciones, vaya a [Asignación de entidad estándar para sincronización](admin-synchronizing-business-central-and-sales.md#standard-table-mapping-for-synchronization).

## Gestionar las diferencias en las monedas de transacción locales y base

Puede conectarse a un entorno [!INCLUDE[prod_short](includes/cds_long_md.md)] que tenga una moneda base diferente a la moneda local en [!INCLUDE[prod_short](includes/prod_short.md)]. La conexión se realiza en [!INCLUDE[prod_short](includes/prod_short.md)] en la página **Configuración de la conexión de Dataverse** o mediante la guía de configuración asistida **Configurar la conexión a Dataverse**.

Para poder conectarse, asegúrese de que la moneda base de la transacción en [!INCLUDE[prod_short](includes/cds_long_md.md)] tenga la divisa que se configuró en la página **Divisas** en [!INCLUDE [prod_short](includes/prod_short.md)] y se especifica al menos un tipo de cambio para la divisa en la página **Tipos de cambio de divisas**.

A continuación, tiene un ejemplo. Está conectando [!INCLUDE[prod_short](includes/cds_long_md.md)] con el euro (EUR) establecido como moneda local en la página **Configuración del libro mayor general** al entorno [!INCLUDE[prod_short](includes/cds_long_md.md)] que tiene una moneda de transacción base establecida en dólares estadounidenses (USD). Necesitará USD en la página **Divisas** en [!INCLUDE [prod_short](includes/prod_short.md)] y el tipo de cambio apropiado. 

Cuando habilita la conexión a [!INCLUDE[prod_short](includes/cds_long_md.md)], [!INCLUDE [prod_short](includes/prod_short.md)] añade su moneda local a la entidad **Divisa** en [!INCLUDE[prod_short](includes/cds_long_md.md)] con el tipo de cambio del campo **Factor de moneda** en la página **Tipos de cambio de moneda**.

La sincronización de moneda es unidireccional, desde [!INCLUDE [prod_short](includes/prod_short.md)] a [!INCLUDE [!INCLUDE[prod_short](includes/cds_long_md.md)], las cantidades monetarias se convierten y sincronizan de la siguiente manera:

* Los importes en la moneda base [!INCLUDE[prod_short](includes/cds_long_md.md)] se convierten a la moneda local [!INCLUDE [prod_short](includes/prod_short.md)] según el último tipo de cambio sincronizado desde [!INCLUDE [prod_short](includes/prod_short.md)].
* Los importes en la moneda local [!INCLUDE [prod_short](includes/prod_short.md)] se sincronizan con la moneda local [!INCLUDE [prod_short](includes/prod_short.md)] en una de las otras monedas (no base) en [!INCLUDE[prod_short](includes/cds_long_md.md)].

## Consulte también .

[Modelos de propiedad de datos](admin-cds-company-concept.md)  
<!--needs to be removed as this is moved to dev-itpro docs[Walkthrough: Customizing an Integration with Dataverse](\dynamics365\business-central\dev-itpro\administration\administration-custom-cds-integration) -->


[!INCLUDE[footer-include](includes/footer-banner.md)]
