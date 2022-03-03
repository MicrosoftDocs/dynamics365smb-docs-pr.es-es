---
title: Establecer la configuración de una empresa
description: Como socio, configure Business Central correctamente para su cliente con configuraciones predeterminadas o específicas del cliente que pueda agrupar en paquetes de configuración.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 841d57ec0e5897ee0395e498ed24dc19b4fcbaea
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2022
ms.locfileid: "8143939"
---
# <a name="set-up-company-configuration"></a>Establecer la configuración de una empresa
El proceso de la implementación comienza con el socio de Microsoft. Como socio, usted es el responsable de analizar los detalles de configuración y crear un paquete que un cliente podrá aplicar fácilmente. Antes de crear una nueva empresa en [!INCLUDE [prod_short](includes/prod_short.md)] en línea o local, debe planificar su configuración. Debe tener en cuenta los datos de configuración básica y tipos de datos que necesitará la solución [!INCLUDE[prod_short](includes/prod_short.md)]. Toda esta información se agrupa en paquetes de configuración.

RapidStart Services también le proporciona las herramientas que usará para migrar los datos heredados, como clientes y proveedores.  

Es recomendable crear paquetes de configuración con la mayoría de las tablas de configuración rellenadas, de modo que los clientes solo tengan que cambiar algunas opciones después de aplicar el paquete. Por ejemplo, cuando crea una nueva empresa, las tablas **Nº serie** y **Lín. nº serie**, este campo se rellenan con un conjunto de series numéricas y números de inicio. Los campos de **Serie numérica** correspondientes de las tablas de configuración también se rellenan automáticamente. No tiene que hacer el trabajo de introducir la serie numérica y otros datos básicos de configuración. También puede modificar manualmente todos los datos predeterminados que se use con RapidStart Services mediante la hoja de trabajo de configuración.  

Los paquetes de configuración se basan en una empresa preconfigurada. Después de configurar una empresa que satisfaga todas sus necesidades, puede crear un paquete de configuración que contenga los datos pertinentes para esta empresa. Luego podrá usarla al crear una nueva empresa que se deba configurar del mismo modo.  

Para facilitar la importación de datos maestros, tal como información del cliente y del proveedor, puede usar plantillas de configuración. Las plantillas de configuración contienen un conjunto de opciones de configuración predeterminadas que se asignan automáticamente a los registros importados en [!INCLUDE[prod_short](includes/prod_short.md)].

En la tabla siguiente se muestra una secuencia de tareas con vínculos a los temas que las describen.

|**Para**|**Consulte**|  
|------------|-------------|  
|Planifique la configuración de una empresa completando la hoja de trabajo de configuración.|[Gestionar la configuración de la empresa en una hoja de trabajo](admin-how-to-manage-company-configuration-in-a-worksheet.md)|  
|Crear un paquete de configuración, personalice un paquete, asigne tablas a un paquete, revise o edite los datos existentes del cliente, cree la nueva empresa y luego mueva los datos de prueba al entorno de producción.|[Preparar un paquete de configuración](admin-how-to-prepare-a-configuration-package.md)|

También puede crear paquetes de configuración con configuraciones estándar que puede usar una y otra vez. Para obtener más información, consulte [Configurar paquetes de configuración estándar de la empresa](/dynamics365/business-central/dev-itpro/administration/set-up-standard-company-configuration-packages) en el contenido de desarrolladores y administración.  

## <a name="see-also"></a>Consulte también

[Configurar una empresa con RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Administración](admin-setup-and-administration.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]