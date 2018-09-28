---
title: "Impresión de informes de libro diario"
description: "Los informes de libro diario muestran todos los movimientos de contabilidad creados en un periodo específico."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: d3a88619122972ba8dda0eefdcdde71621913125
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="print-account-book-reports"></a>Imprimir informes de libro diario
Los informes de libro diario muestran todos los movimientos de contabilidad creados en un periodo específico. Los dos informes de libro diario son:  

- Informe **Libro diario oficial**: muestra información sobre todos los movimientos de contabilidad, agrupados por transacción.  
- Informe **Libro diario oficial resumido**: muestra un resumen de los movimientos generales, agrupados por cuentas de registro o mayores.  

Al enviar estos informes a la administración o a los auditores, se pueden incluir páginas adicionales que precederán el informe. Para ello, se debe definir manualmente el número de la primera página del informe. Por ejemplo, si tiene tres páginas de información que preceden el informe, puede definir la primera página del informe para indicar que es la página 4.  

## <a name="to-print-an-official-account-book-report"></a>Para imprimir un informe de libro diario oficial  

1.  Seleccione el icono ![Buscar página o informe](../../media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Libro diario oficial** y, a continuación, seleccione el vínculo relacionado.  
2.  En la ficha desplegable **Opciones**, rellene los campos tal como se describe en la tabla siguiente.  

    |Campo|Description|  
    |---------------------------------|---------------------------------------|  
    |**Texto asiento cierre**|Escriba la descripción de la transacción de cierre del periodo.|  
    |**Texto asiento apertura**|Escriba la descripción de la transacción de apertura del periodo.|  
    |**Primera página**|Introduzca el número que desea incluir en la primera página del informe.|  
    |**Muestra importes en divisa adicional**|Seleccione que se muestren los importes del informe en una divisa adicional de informe (DA).|  

3.  En la ficha desplegable **Registro contabilidad**, seleccione los filtros apropiados.  
4.  Seleccione el botón de **Imprimir** para imprimir el informe o elegir el botón de **Vista previa** para verlo en la pantalla.  

## <a name="to-print-an-official-account-summarized-book-report"></a>Para imprimir un libro diario oficial resumido  

1.  Seleccione el icono ![Buscar página o informe](../../media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Libro diario oficial resumido** y, a continuación, seleccione el vínculo relacionado.  
2.  En la ficha desplegable **Opciones**, rellene los campos tal como se describe en la tabla siguiente.  

    |Campo|Description|  
    |---------------------------------|---------------------------------------|  
    |**Desde fecha**|Indique la fecha de inicio del informe.|  
    |**Hasta fecha**|Indique la fecha de fin del informe.|  
    |**Incluir movs. Regularización**|Seleccione esta opción para incluir movimientos de regularización en el informe.|  
    |**Muestra importes en divisa adicional**|Seleccione que se muestren los importes del informe en una divisa adicional de informe (DA).|  
    |**Primera página**|Introduzca el número que desea incluir en la primera página del informe.|  
    |**Tipo mov.**|Seleccione **Registro** o **Mayor**. **Registro** implica que se pueden registrar movimientos en la cuenta y **Mayor** implica que no se pueden registrar movimientos en la cuenta.|  

3.  Seleccione el botón de **Imprimir** para imprimir el informe o elegir el botón de **Vista previa** para verlo en la pantalla.  

## <a name="see-also"></a>Consulte también  
 [Funcionalidad local para España](spain-local-functionality.md)

