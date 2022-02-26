---
title: Tareas administrativas en Business Central
description: Algunas tareas de Business Central requieren administración y configuración centrales. Consulte cuáles son aprenda y qué hacer.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 07/23/2021
ms.author: edupont
ms.openlocfilehash: 959a56e4bb7fcaac57b05d30dca4939ed2f8576d
ms.sourcegitcommit: e904da8dc45e41cdd1434111c15e2a9d9edd3fa2
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 07/23/2021
ms.locfileid: "6660136"
---
# <a name="administration"></a>Administración

Normalmente, un rol de la empresa se encarga de las tareas de la administración central. El alcance de estas tareas puede depender del tamaño de la empresa, así como de las responsabilidades laborales del administrador. Estas tareas pueden incluir la administración de la sincronización de base de datos de las colas de proyectos y de correo electrónico, la configuración de usuarios y la personalización de la interfaz de usuario.  

Es importante introducir los valores de configuración correctos desde el principio para el éxito de cualquier nuevo software de negocio. [!INCLUDE[prod_short](includes/prod_short.md)] incluye varias guías de configuración que le ayudan a configurar datos fundamentales. Para obtener más información, consulte [Configurar Business Central](setup.md).

> [!NOTE]
> Puede configurar una nueva empresa en [!INCLUDE[prod_short](includes/prod_short.md)] con RapidStart Services, que es una herramienta diseñada para acortar los tiempos de implementación, mejorar la calidad de la implementación, introducir un método de repetición para las implementaciones y mejorar la productividad mediante la automatización y simplificación de las tareas periódicas. Para obtener más información, consulte [Configuración de una empresa con RapidStart Services](admin-set-up-a-company-with-rapidstart.md).

Si utiliza RapidStart Services para implementar los valores de configuración o si los introduce manualmente en la nueva empresa, puede sustentar su decisiones de configuración con algunas recomendaciones generales para los campos de configuración seleccionados que son conocidos porque pueden provocar que la solución resulte ineficaz si están definidos forma incorrecta.  

Un superusuario o un administrador puede configurar el marco de intercambio de datos para que los usuarios puedan exportar e importar los datos de los archivos de banco y de nómina, por ejemplo, para diferentes procesos de tesorería. Para obtener más información, vea [Intercambio de datos electrónicamente](across-data-exchange.md).

En la tabla siguiente se indican una serie de tareas con vínculos a los artículos que las describen.  

|**Para**|**Vea**|  
|------------|-------------|
|Defina quién puede iniciar sesión en [!INCLUDE[prod_short](includes/prod_short.md)] creando usuarios en el centro de administración de Microsoft 365 según las licencias del producto.|[Crear usuarios de acuerdo con las licencias](ui-how-users-permissions.md)|
|Asignar permisos a los usuarios, modificar conjuntos de permisos y agrupar usuarios para facilitar la administración de permisos.|[Asignar permisos a usuarios y grupos](ui-how-users-permissions.md)|
|Agregar usuarios, gestionar permisos y gestionar el acceso a los datos, asignar roles.|[Administración de perfiles](admin-users-profiles-roles.md)|
|Administre la configuración del usuario, como empresa, función, idioma, región y zona horaria.|[Configuración de usuario](admin-manage-user-settings-preferences.md)|
|Configure impresoras y especifique qué informes imprimir en qué impresoras.|[Configuración de impresoras](ui-specify-printer-selection-reports.md)|
|Clasifique la confidencialidad de los datos para los campos, de modo que pueda responder a las solicitudes de los asuntos relacionadas con sus datos personales.|[Clasificar confidencialidad de datos](admin-classifying-data-sensitivity.md)|
|Responda a las solicitudes de los asuntos relacionadas con sus datos personales.|[Respuesta a las solicitudes de datos personales](admin-responding-to-requests-about-personal-data.md)|
|Configure una nueva empresa usando plantillas|[Crear nuevas en empresas](about-new-company.md)|
|Realizar un seguimiento de todas las modificaciones directas que realicen los usuarios a los datos de la base de datos para identificar el origen de los errores y de las modificaciones en los datos.|[Registrar cambios](across-log-changes.md)|  
|Introducir solicitudes únicas o periódicas para ejecutar informes o codeunits.|[Usar colas de proyectos para programar tareas](admin-job-queues-schedule-tasks.md)|  
|Administre, elimine, o comprima los documentos|[Eliminar documentos](admin-manage-documents.md)|  
|Exponga las páginas, los codeunits y las consultas como servicios web.|[Publicar un servicio web](across-how-publish-web-service.md)|
|Como parte de la creación de Connect Apps entre soluciones de [!INCLUDE[prod_short](includes/prod_short.md)] y de terceros a través de las API de REST, defina plantillas que se utilizan para completar propiedades vacías en una entidad cuando crea una acción POST a través de una API.|[Configuración de plantillas API](admin-configuring-api-template.md)|
|Cifre los datos en el servidor de [!INCLUDE[prod_short](includes/prod_short.md)] generando claves de cifrado nuevas o importando claves existentes que se activarán en el servidor.|[Administración del cifrado de datos](admin-manage-data-encryption.md)|
|Conecte Dynamics 365 Sales con [!INCLUDE[prod_short](includes/prod_short.md)] para obtener una integración perfecta entre las relaciones con los clientes y el procesamiento de pedidos en el proceso de obtención de efectivo.|[Integración con Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)|
|Cambie los campos y las acciones que se muestran en la interfaz de usuario para adaptarla a los procesos de la empresa y ampliar la solución con aplicaciones.|[Personalización de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-customizing-overview.md)|

## <a name="administration-in-the-admin-center"></a>Administración en el Centro de administración

Los administradores internos y delegados tienen acceso al [!INCLUDE [prod_short](includes/prod_short.md)] centro de administración donde pueden configurar, supervisar y solucionar problemas en [!INCLUDE [prod_short](includes/prod_short.md)] ambientes. En la tabla siguiente se indican algunas tareas clave con vínculos a los artículos que las describen.  

|**Para**|**Vea**|  
|------------|-------------|
|Conozca las herramientas que están disponibles para ayudarlo a solucionar problemas.|[Soporte técnico](/dynamics365/business-central/dev-itpro/technical-support)|
|Supervise el uso y solucione problemas de sesiones|[Telemetría del entorno en el centro de administración de Business Central](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-telemetry)|
|Administre sesiones de usuario, incluida la cancelación de una sesión si el usuario está bloqueado.|[Administración de sesiones](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#managing-sessions)|
|Configure el suscriptor para enviar datos de telemetría a Azure Application Insights para mejor análisis y resolución de problemas.|[Habilitar envío de telemetría a Application Insights](/dynamics365/business-central/dev-itpro/administration/telemetry-enable-application-insights)|

## <a name="see-related-training-at-microsoft-learn"></a>Consulte Formación relacionada en [Microsoft Learn](/learn/paths/deploy-configure-dynamics-365-business-central/)

## <a name="see-also"></a>Consulte también

[Funciones empresariales](across-business-functionality.md)  
[Funciones empresariales generales](ui-across-business-areas.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Preparación para hacer negocios](ui-get-ready-business.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]