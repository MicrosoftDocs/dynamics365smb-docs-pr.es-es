---
title: Configurar una empresa con RapidStart Services
description: Puede configurar una nueva empresa en Business Central con RapidStart Services para mejorar la productividad al automatizar y simplificar las tareas recurrentes.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.search.form: 8610, 8614, 8615, 8620, 8632
ms.date: 03/28/2022
ms.author: edupont
ms.openlocfilehash: b2d3378e9c06221bc91977883a53bba8514c6afc
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2022
ms.locfileid: "8518316"
---
# <a name="set-up-a-company-with-rapidstart-services"></a>Configurar una empresa con RapidStart Services

Puede configurar una nueva empresa en [!INCLUDE[prod_short](includes/prod_short.md)] con RapidStart Services, que es una herramienta diseñada para acortar los tiempos de implementación, mejorar la calidad de la implementación, introducir un método de repetición para las implementaciones y mejorar la productividad mediante la automatización y simplificación de las tareas periódicas.  

Utilice estas capacidades para escalar su negocio como distribuidor. La mayoría de las páginas relevantes se aplican a tanto a [!INCLUDE [prod_short](includes/prod_short.md)] en línea como local. Sin embargo, algunos procesos se basan en el acceso a archivos en el disco y son demasiado complejos para usarlos para [!INCLUDE [prod_short](includes/prod_short.md)] en línea. Para [!INCLUDE [prod_short](includes/prod_short.md)] local, es probable que desee usar Windows PowerShell para ayudarle a implementar. Para obtener más información, consulte [Administración de Business Central local](/dynamics365/business-central/dev-itpro/administration/administration) y [ Administración de Business Central Online](/dynamics365/business-central/dev-itpro/administration/tenant-administration), respectivamente.  

RapidStart Services ayuda a obtener una visión general del proceso de configuración de la nueva empresa al proporcionar a una hoja de trabajo en la que puede configurar las tablas que suelen usarse en el proceso de configuración de nuevas empresas. A medida que avanza por el proceso, puede crear un cuestionario para guiar a los clientes a través de la colección de información de configuración. Los clientes tienen la opción de usar el cuestionario para configurar las áreas de aplicación, o pueden abrir la página de configuración directamente y establecer las opciones en ella. Lo que es más importante, RapidStart Services le ayuda, como cliente, a preparar la empresa con los datos de configuración predeterminados que puede ajustar y personalizar. Por último, cuando use RapidStart Services, puede configurar y emigrar los datos de cliente existentes, tal como la lista de clientes o productos, en la nueva empresa.

Puede utilizar los componentes siguientes para agilizar la configuración de su empresa:  

- Asistente para la configuración  
- Hoja de trabajo de configuración  
- Paquetes de configuración  
- Plantillas de configuración  
- Cuestionario de configuración  

> [!Note]  
> Existen áreas de [!INCLUDE[prod_short](includes/prod_short.md)] que tendrá que configurar manualmente. Entre ellas se incluye la adición de usuarios, la configuración de periodos contables y la configuración de las dimensiones para la inteligencia empresarial. Para obtener más información, consulte [Configurar [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md).

 En la tabla siguiente se muestra una secuencia de tareas con vínculos a los temas que las describen.

|**Para**|**Vea**|  
|------------|-------------|  
|Cree una nueva empresa e importe plantillas y datos de configuración básicos.|[Establecer la configuración de una empresa](admin-set-up-company-configuration.md)|  
|Implementar el paquete configurado a su cliente por la implementación.|[Aplicar la configuración a nuevas empresas](admin-apply-configuration-to-new-companies.md)|
|Definir y validar los valores de configuración de su cliente para todas las áreas centrales, como la información de la empresa, la contabilidad, el inventario, las ventas o la fabricación.|[Recopilación de valores de configuración de cliente](admin-gather-customer-setup-values.md)|  
|Configure registros de datos maestros básicos mediante plantillas para prepararse para migrar los datos existentes de clientes.|[Preparar migración de datos de cliente](admin-use-templates-to-prepare-customer-data-for-migration.md)|  
|Defina las tablas y campos, valide los datos existentes de clientes y migre los datos en la base de datos de [!INCLUDE[prod_short](includes/prod_short.md)].|[Migrar datos del cliente](admin-migrate-customer-data.md)|
|Prepárese para reutilizar las configuraciones de la empresa en otras empresas (en el contenido de desarrollador y administración).|[Crear paquetes de configuración de empresa personalizados](/dynamics365/business-central/dev-itpro/administration/set-up-standard-company-configuration-packages)|
|Busque soluciones para problemas conocidos en el kit de herramientas de RapidStart Services.|[Sugerencias y trucos: RapidStart Services](admin-tips-and-tricks-rapidstart-services.md)|  

## <a name="see-also"></a>Consulte también

[Administración](admin-setup-and-administration.md)  
[Configurar [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Configurar áreas de aplicación complejas mediante procedimientos recomendados](set-up-complex-application-areas-using-best-practices.md)   


[!INCLUDE[footer-include](includes/footer-banner.md)]