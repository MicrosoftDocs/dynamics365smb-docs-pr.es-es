---
title: Administrar acceso a Business Central
description: Los administradores utilizan un enfoque por niveles para controlar el acceso a Business Central y sus capacidades.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: overview
ms.date: 04/04/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# Administrar acceso a Business Central

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Este artículo ofrece a los administradores y desarrolladores de aplicaciones una descripción general de alto nivel sobre cómo controlar el acceso a [!INCLUDE [prod_short](includes/prod_short.md)] y sus características. Use los enlaces para ir a otros artículos que brindan más detalles sobre los temas.

## Acceso por niveles

[!INCLUDE [prod_short](includes/prod_short.md)] utiliza un enfoque por niveles para la seguridad de las aplicaciones, como se describe en el siguiente diagrama. Para obtener más información sobre cada nivel, vaya a [Seguridad de aplicaciones en Business Central](/dynamics365/business-central/dev-itpro/security/security-application).

:::image type="content" source="media/security-overview.png" alt-text="Seguridad de las aplicaciones por niveles en Business Central.":::

## Licencias

Asigne usuarios de [!INCLUDE [prod_short](includes/prod_short.md)] a una licencia de **Dynamics 365 Business Central** para que puedan ver, modificar y actuar sobre sus datos comerciales desde cualquier interfaz de usuario. Para obtener más información sobre las licencias, vaya a [Licencias en Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/deployment/licensing).

Sin embargo, las personas que ocasionalmente necesitan acceso de solo lectura a la información en [!INCLUDE [prod_short](includes/prod_short.md)] pueden usar una licencia de **Microsoft 365**. Para obtener más información sobre conceder acceso limitado, vaya a [Acceso a Business Central con licencias de Microsoft 365](admin-access-with-m365-license.md).

Para obtener información completa sobre los diferentes tipos de licencias y cómo funcionan las licencias en [!INCLUDE[prod_short](includes/prod_short.md)], [descargue la Guía de licencias de Dynamics 365](https://go.microsoft.com/fwlink/?LinkId=866544).

## Tareas del administrador de Business Central

La siguiente tabla enumera cómo los administradores pueden controlar el acceso a [!INCLUDE [prod_short](includes/prod_short.md)] y las funciones que usarán las personas. Algunas de las tareas también ayudan a mantener actualizada la configuración de acceso.

|Tarea| Más información |
|--|--|--|
|Cada persona debe tener una cuenta de usuario antes de poder iniciar sesión en [!INCLUDE [prod_short](includes/prod_short.md)]. La forma más sencilla de configurar usuarios es agregarlos de uno en uno en el [Centro de administración de Microsoft 365](https://go.microsoft.com/fwlink/p/?linkid=2024339). |[Agregar usuarios y asignar licencias al mismo tiempo](/microsoft-365/admin/add-users/add-users)|
|Administre el acceso para todos los usuarios en el nivel de entorno. Cree un grupo de seguridad de Microsoft Entra y asígnelo al entorno.<br><br> También puede usar grupos de seguridad para administrar el acceso de grupos específicos de usuarios. | [Administrar el acceso a entornos](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-manage-access)<br><br>[Controlar el acceso a Business Central mediante grupos de seguridad](ui-security-groups.md) |
|Cree usuarios en [!INCLUDE [prod_short](includes/prod_short.md)] y defina quién puede iniciar sesión. | [Crear usuarios de acuerdo con las licencias](ui-how-users-permissions.md) |
|En combinación con las licencias de usuario, los permisos definen los objetos a los que puede tener acceso un usuario dentro de cada base de datos o entorno. Especifique si cada usuario puede leer, modificar o introducir datos en los objetos de la base de datos. |[Asignar permisos a usuarios y grupos](ui-define-granular-permissions.md)|
|Si un contable externo administra sus libros e informes financieros, invítelo a su [!INCLUDE [prod_short](includes/prod_short.md)]. Podrá trabajar más de cerca con usted en sus datos fiscales.|[Experiencias contables en [!INCLUDE[prod_long](includes/prod_long.md)]](finance-accounting.md)|
|Si es un socio distribuidor [!INCLUDE [prod_short](includes/prod_short.md)], puede enviar un correo electrónico a un cliente para solicitar una relación de distribuidor. Puede incluir privilegios de administración delegada para Microsoft Entra ID y Microsoft 365 en el correo electrónico.| [Acceso de administrador delegado a Business Central Online](/dynamics365/business-central/dev-itpro/administration/delegated-admin)|
|Una etiqueta de servicio de Azure representa un grupo de direcciones IP de las que puede provenir o a las que puede dirigirse el tráfico de un servicio. Use etiquetas de servicio para configurar cortafuegos para permitir tráfico solo desde ciertos servicios. La etiqueta **Dynamics365BusinessCentral** le permite usar reglas de grupo de seguridad de red y firewall para restringir el tráfico hacia y desde [!INCLUDE [prod_short](includes/prod_short.md)].| [Etiquetas de servicio de seguridad de Azure](/dynamics365/business-central/dev-itpro/security/security-service-tags)|
|Cuando utilice la autenticación de Microsoft Entra con [!INCLUDE [prod_short](includes/prod_short.md)], le recomendamos que aproveche la [autenticación multifactor de Microsoft Entra ID (MFA)](/azure/active-directory/authentication/concept-mfa-howitworks). MFA protege aún más el acceso a la aplicación y los datos.|[Autenticación multifactor para Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/security/multifactor-authentication)|

## Tareas para desarrolladores de Business Central

También hay una historia de desarrolladores para administrar el acceso a [!INCLUDE [prod_short](includes/prod_short.md)]. Por ejemplo, los desarrolladores y administradores pueden crear y conectar aplicaciones a [!INCLUDE [prod_short](includes/prod_short.md)] que beneficien a la empresa:  

* Agilizar procesos empresariales
* Mejorar las interacciones con los clientes
* Tomar decisiones mejores más rápido

La siguiente tabla vincula a información sobre cómo otorgar a aplicaciones y extensiones acceso a datos de [!INCLUDE [prod_short](includes/prod_short.md)].

| Tarea | Más información |
|--|--|
|Los dos conceptos principales para definir el acceso a las funciones son derechos y permisos. Los derechos otorgan un amplio acceso a los objetos de acuerdo con las licencias o los roles de Microsoft Entra. Los permisos y los conjuntos de permisos le permiten ajustar el acceso a los objetos. |[Resumen de derechos y conjuntos de permisos](/dynamics365/business-central/dev-itpro/developer/devenv-entitlements-and-permissionsets-overview)|

## Consulte también

[Seguridad en Business Central](/dynamics365/business-central/dev-itpro/security/security-and-protection)
