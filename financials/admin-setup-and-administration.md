---
title: Tareas administrativas de Microsoft Dynamics 365 | Documentos de Microsoft
description: "Algunas tareas de Dynamics 365 requieren administración y configuración centrales. Consulte cuáles son aprenda y qué hacer."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/01/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: a49e50213f808fb72b43dfa22a34833b306ef12d
ms.openlocfilehash: c7e5efe85dddcc7db84b05879f0c71990167c775
ms.contentlocale: es-es
ms.lasthandoff: 12/14/2017

---
# <a name="setup-and-administration-in-dynamics-365-for-financials"></a>Configuración y Administración en Dynamics 365 for Financials
Normalmente, un rol de la empresa se encarga de las tareas de la administración central. El alcance de estas tareas puede depender del tamaño de la empresa, así como de las responsabilidades laborales del administrador. Estas tareas pueden incluir la administración de la sincronización de base de datos de las colas de proyectos y de correo electrónico, la configuración de usuarios, la personalización de la interfaz de usuario y la administración de las claves de cifrado.  

Es importante introducir los valores de configuración correctos desde el principio para el éxito de cualquier nuevo software de negocio. [!INCLUDE[d365fin](includes/d365fin_md.md)] incluye varias guías de configuración que le ayudan a configurar datos fundamentales. Para obtener más información, consulte [Configurar Dynamics 365 for Financials](setup.md).

<!--Whether you use [!INCLUDE[rim](../../includes/rim_md.md)] to implement setup values or you manually enter them in the new company, you can support your setup decisions with some general recommendations for selected setup fields that are known to potentially cause the solution to be inefficient if defined incorrectly.-->  

Un superusuario o un administrador puede configurar el marco de intercambio de datos para que los usuarios puedan exportar e importar los datos de los archivos de banco y de nómina, por ejemplo, para diferentes procesos de tesorería.  

En la tabla siguiente se indican una serie de tareas con vínculos a los temas que las describen.   

|**Para**|**Vea**|  
|------------|-------------|  
|Agregar usuarios, gestionar permisos y gestionar el acceso a los datos, asignar roles.|[Usuarios, perfiles, y áreas de trabajo de Microsoft Dynamics 365 for Financials](admin-users-profiles-roles.md)|  
|Realizar un seguimiento de todas las modificaciones directas que realicen los usuarios a los datos de la base de datos para identificar el origen de los errores y de las modificaciones en los datos.|[Registrar cambios en Dynamics 365 for Financials](across-log-changes.md)|  
|Apoye las decisiones de configuración con recomendaciones para los campos seleccionados que se saben que potencialmente la solución se haga ineficaz si no se configuran correctamente|[Configurar áreas de aplicación complejas mediante procedimientos recomendados](set-up-complex-application-areas-using-best-practices.md)|  
|Exponga las páginas, las unidades de código y las consultas como servicios web.|[Procedimiento: Publicar un servicio Web](across-how-publish-web-service.md)|  
|Configure un servidor SMTP para habilitar la comunicación de correo electrónico dentro y fuera de Dynamics 365 for Financials| [Configurar el correo electrónico manualmente o con la configuración asistida](madeira-how-setup-email.md)|  
|Introducir solicitudes únicas o periódicas para ejecutar informes o unidades de código.|[Uso de colas de proyectos para programar tareas](admin-job-queues-schedule-tasks.md)|  
|Administre, elimine, o comprima los documentos|[Administración de documentos](admin-manage-documents.md)|  
|Configure una nueva empresa usando plantillas|[Crear nuevas en empresas en [!INCLUDE[d365fin](includes/d365fin_md.md)]](about-new-company.md)|  

## <a name="see-also"></a>Consulte también
[Funciones empresariales](madeira-business-functionality.md)  
[Funciones empresariales generales](ui-across-business-areas.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]](index.md)  

