---
title: "Personalizar las señales visuales acerca de la actividad de una pila | Documentos de Microsoft"
description: "Configure un indicador de color en un mosaico Pila para proporcionar una señal visual personalizada de la actividad de la pila."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: personalize, customize
ms.date: 10/01/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: e4ceaeae1a37a521d2d5bd22ab711757283e6321
ms.contentlocale: es-es
ms.lasthandoff: 09/28/2018

---
# <a name="set-up-a-colored-indicator-on-cues"></a>Configurar un indicador de color en pilas
Puede configurar pilas para que aparezcan en el Área de trabajo de los usuarios a fin de que incluyan un indicador que cambia de color según los valores de datos de las pilas.

El indicador se muestra como una barra de color a lo largo del borde superior del mosaico de la pila. Proporciona una guía visual del estado de la actividad de la pila, que puede indicar condiciones favorables o desfavorables para que el usuario actúe en consecuencia. Por ejemplo, si una pila muestra las facturas de venta en curso, puede configurar que el indicador aparezca de color verde (favorable) si el número total de facturas de venta en curso es inferior a 10 y que aparezca de color rojo (desfavorable) si el total es mayor que 20.

En la ventana **Configuración de pila** se configuran indicadores para todas las pilas que están disponibles en la base de datos de la empresa.

Para configurar el indicador, especifique hasta dos valores de umbral que definan tres rangos de valores de datos (bajo, medio y alto) a los que se pueda aplicar otro color (o estilo).

## <a name="to-set-up-colored-indicators-on-cues"></a>Para configurar indicadores de color en las pilas
1. En **Actividades** en el Área de trabajo, elija **Configurar pilas**.  
   Aparece la ventana **Configuración de pila**. La ventana muestra los indicadores que están actualmente configurados en pilas.
2. Para modificar un marcador, edite los campos y modifique, por ejemplo, los valores para los distintos umbrales.  

La tabla siguiente muestra los colores que corresponden a las opciones de los campos **Estilo de rango bajo**, **Estilo de rango medio** y **Estilo de rango alto**.

| Opción | Color |
| --- | --- |
| **Ninguno** |Sin color (mismo color que el mosaico de la pila)|
| **Favorable** |Verde |
| **Desfavorable** |Rojo |
| **Ambiguo** |Amarillo |
| **Subordinado** |Gris |

## <a name="see-also"></a>Consulte también
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

