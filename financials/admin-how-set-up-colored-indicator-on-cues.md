---
title: "Especificar los indicadores de color para personalizar las señales visuales acerca de la actividad de una pila para la empresa o los usuarios individuales| Documentos de Microsoft"
description: "Como administrador, puede configurar pilas para que aparezcan en las áreas de trabajo de los usuarios a fin de que incluyan un indicador que cambia de color según los valores de datos de las pilas."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 17daf9dfa367907d10dd5101f1001ac2aaf7ea03
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-a-colored-indicator-on-cues-for-the-company-or-individual-users"></a>Configurar un indicador de color en pilas para la empresa o usuarios individuales
Como administrador, puede configurar pilas para que aparezcan en las áreas de trabajo de los usuarios a fin de que incluyan un indicador que cambia de color según los valores de datos de las pilas.  
  
El indicador se muestra como una barra de color a lo largo del borde superior del mosaico de la pila. Proporciona una guía visual del estado de la actividad de la pila, que puede indicar condiciones favorables o desfavorables para que el usuario actúe en consecuencia. Por ejemplo, si una pila muestra las facturas de venta en curso, puede configurar que el indicador aparezca de color verde (favorable) si el número total de facturas de venta en curso es inferior a 10 y que aparezca de color rojo (desfavorable) si el total es mayor que 20.  
  
En la ventana **Configuración de pila** se configuran indicadores para todas las pilas que están disponibles en la base de datos de la empresa. Puede configurar los indicadores de aplicación general para todos los usuarios de la empresa o usuarios por individual. La configuración del indicador en la ventana **Configuración de pilas** actúa como configuración de indicador predeterminada. Si la ventana **Configuración de la pila de usuario final** está disponible para los usuarios, estos pueden personalizar la configuración de indicadores definida en la ventana **Configuración de la pila**.  
  
Para configurar el indicador, especifique hasta dos valores de umbral que definan tres rangos de valores de datos (bajo, medio y alto) a los que se pueda aplicar otro color (o estilo).  
  
### <a name="to-set-up-colored-indicators-on-cues"></a>Para configurar indicadores de color en las pilas  
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), especifique **Configuración de pila** y elija el vínculo relacionado.  
  
     Aparece la ventana **Configuración de pila**. La ventana muestra los indicadores que están actualmente configurados en las pilas. Los indicadores aplicables a todos los usuarios de la empresa tienen un campo **Nombre de usurario** en blanco. Los indicadores que se aplican a un usuario específico incluyen el nombre del usuario de en el campo **Nombre de usuario**.  
  
    > [!NOTE]  
    >  Si configura un indicador para toda la empresa y un usuario lo modifica posteriormente, aparece una entrada independiente para el indicador en la lista de dicho usuario.  
  
2. Seleccione la acción **Editar lista**.  
3. Para configurar un indicador para una pila que no aparece en la ventana, seleccione la acción **Nuevo** y rellene los campos tal y como se describe a continuación. Si desea modificar un indicador existente, vaya al paso siguiente.  
  
    |  Campo  |  Description  |    
    |---------|---------------|  
    |**Nombre usuario**|Si desea configurar el indicador para todos los usuarios, deje este campo en blanco.<br /><br /> Si desea configurar el indicador para un usuario específico, establezca este campo en el nombre del usuario.|  
    |**Nº tabla**|Especifica el identificador del objeto de tabla que contiene la pila. Utilice el menú desplegable para buscar la tabla. La lista desplegable incluye todas las tablas de pila en la base de datos de la empresa.<br /><br /> El campo **Nombre de la tabla** se rellenará automáticamente según su selección.|  
    |**Nº campo**|Especifica el identificador en la pila en la que desea configurar un indicador. Utilice la lista desplegable para buscar la pila que le interesa. **Nota:** El identificador de pila se corresponde con el número de campo asignado a la pila en la tabla. <br /><br /> El campo **Nombre del campo** se rellena automáticamente según su selección.|  
  
4. Para configurar el indicador para una pila, defina los campos tal y como se describen en la siguiente tabla.  
  
    |  Campo  |  Description  |    
    |---------|---------------|  
    |**Estilo inferior**|Especifica el color del indicador cuando el valor de pila es inferior al valor del campo **Umbral 1**.|  
    |**Umbral inferior**|Especifica el valor en el cual, o por encima del cual, el indicador cambia al color especificado en el campo **Estilo de rango medio**.|  
    |**Estilo medio**|Especifica el color del indicador cuando el valor de pila es igual o superior al valor del campo **Umbral 1**, pero igual o menor al valor del campo **Umbral 2**.|  
    |**Umbral superior**|Especifica el valor por encima del cual el indicador cambia al color especificado en el campo **Estilo de rango alto**.|  
    |**Estilo superior**|Especifica el color que usar cuando el valor de pila es superior al valor del campo **Umbral 2**.|  
  
     La tabla siguiente muestra los colores que corresponden a las opciones de los campos **Estilo inferior**, **Estilo medio** y **Estilo superior**.  
  
    |  Opción  |  Color  |  
    |----------|---------|  
    |**Ninguno**|Sin color (mismo color que el mosaico de la pila)|  
    |**Favorable**|Verde|  
    |**Desfavorable**|Rojo|  
    |**Ambiguo**|Amarillo|  
    |**Subordinado**|Gris|  
  
## <a name="see-also"></a>Consulte también  
[Configurar un indicador de color en pilas del área de trabajo](ui-how-setup-colored-indicator-cues.md)  
