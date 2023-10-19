---
title: 'Cómo imprimir informes de libro diario [ES]'
description: Aprenda a imprimir el informe Libro diario oficial y el informe del Libro diario oficial resumido con la versión en español de Business Central.
services: project-madeira
documentationcenter: ''
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/21/2021
ms.author: bholtorf
---
# <a name="print-account-book-reports-in-the-spanish-version"></a>Imprimir informes de libro diario en la versión en español
Los informes de libro diario muestran todos los movimientos de contabilidad creados en un periodo específico. Los dos informes de libro diario son:  

- Informe **Libro diario oficial**: muestra información sobre todos los movimientos de contabilidad, agrupados por transacción.  
- Informe **Libro diario oficial resumido**: muestra un resumen de los movimientos generales, agrupados por cuentas de registro o mayores.  

Al enviar estos informes a la administración o a los auditores, se pueden incluir páginas adicionales que precederán el informe. Para ello, se debe definir manualmente el número de la primera página del informe. Por ejemplo, si tiene tres páginas de información que preceden el informe, puede definir la primera página del informe para indicar que es la página 4.  

## <a name="to-print-an-official-account-book-report"></a>Para imprimir un informe de libro diario oficial

1.  Elija el icono ![Bombilla que abre la función Dígame.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Cuenta - Libro diario oficial** y luego elija el enlace relacionado.  
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

1.  Elija el icono ![Bombilla que abre la función Dígame.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Libro diario oficial resumido** y luego elija el enlace relacionado.  
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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
