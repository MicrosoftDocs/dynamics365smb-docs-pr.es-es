---
title: Establecer la configuración de una empresa | Documentos de Microsoft
description: El proceso de implementación comienza con la solución Business Central requerida. Toda esta información se agrupa en paquetes de configuración.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: e003f429122bd31ee35ef9b843682bfe8866407a
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2019
ms.locfileid: "926468"
---
# <a name="set-up-company-configuration"></a>Establecer la configuración de una empresa
El proceso de la implementación comienza con el socio de Microsoft. El socio es responsable de analizar los detalles de configuración y crear un paquete que un cliente podrá aplicar fácilmente. Antes de crear una nueva empresa, debe planificar su configuración. Debe tener en cuenta los datos de configuración básica y tipos de datos que necesitará la solución [!INCLUDE[d365fin](includes/d365fin_md.md)]. Toda esta información se agrupa en paquetes de configuración.

RapidStart Services también le proporciona las herramientas que usará para migrar sus datos heredados, como clientes y proveedores.  

Es recomendable crear paquetes de configuración con la mayoría de las tablas de configuración rellenadas, de modo que los clientes solo tengan que cambiar algunas opciones después de aplicar el paquete. Por ejemplo, cuando crea una nueva empresa, las tablas **Nº serie** y **Lín. nº serie**, este campo se rellenan con un conjunto de series numéricas y números de inicio. Los campos de **Serie numérica** correspondientes de las tablas de configuración también se rellenan automáticamente. No tiene que hacer el trabajo de introducir la serie numérica y otros datos básicos de configuración. También puede modificar manualmente todos los datos predeterminados que se use con RapidStart Services mediante la hoja de trabajo de configuración.  

Los paquetes de configuración se basan en una empresa preconfigurada. Después de configurar una empresa que satisfaga todas sus necesidades, puede crear un paquete de configuración que contenga los datos pertinentes para esta empresa. Luego podrá usarla al crear una nueva empresa que se deba configurar del mismo modo.  

Para facilitar la importación de datos maestros, tal como información del cliente y del proveedor, puede usar plantillas de configuración. Las plantillas de configuración contienen un conjunto de opciones de configuración predeterminadas que se asignan automáticamente a los registros importados en [!INCLUDE[d365fin](includes/d365fin_md.md)].

En la tabla siguiente se muestra una secuencia de tareas con vínculos a los temas que las describen.

|**Para**|**Consulte**|  
|------------|-------------|  
|Planifique la configuración de una empresa completando la hoja de trabajo de configuración.|[Gestionar la configuración de la empresa en una hoja de trabajo](admin-how-to-manage-company-configuration-in-a-worksheet.md)|  
|Crear un paquete de configuración, personalice un paquete, asigne tablas a un paquete, revise o edite los datos existentes del cliente, cree la nueva empresa y luego mueva los datos de prueba al entorno de producción.|[Preparar un paquete de configuración](admin-how-to-prepare-a-configuration-package.md)| 

## <a name="see-also"></a>Consulte también  
[Configurar una empresa con RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Administración](admin-setup-and-administration.md)
