---
title: La solución de problemas de la extensión de Movs. Activos
description: Es más fácil trabajar con números enteros. Utilice esta extensión para redondear importes de activos fijos en el libro mayor de FA.
documentationcenter: ''
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'machinery, buildings'
ms.date: 10/01/2021
ms.author: bholtorf
---
# La solución de problemas de la extensión de Movs. Activos
Utilice la extensión Solución de problemas de Movs. Activos para redondear los montos de depreciación y adquisición en los asientos contables de activos fijos a números enteros. Por ejemplo, para redondear una cantidad de 30 000,44 a 30 000. Las causas típicas de los problemas de redondeo son la migración de datos, el comienzo repentino de registrar cantidades en el libro mayor o las personalizaciones que ha realizado en su [!INCLUDE[prod_short](includes/prod_short.md)].

La extensión Solución de problemas de Movs. Activos está preinstalada y lista para funcionar. Si elimina la extensión, pero desea instalarla nuevamente, puede encontrarla en AppSource.

## Solución de problemas de entradas del libro mayor de activos fijos
Cuando abre la página **Ficha activo** por primera vez, la entrada de cola de trabajo **Escaneo de Movs. Activos** está programada para supervisar los montos todos los domingos. Si encuentra cantidades que quizás desee redondear, aparecerá una notificación la próxima vez que abra la página Tarjeta de activo fijo. La notificación proporciona una opción **Ver más** que abre la página **Movs. Activos con problemas de redondeo**, que enumera las entradas con importes que es posible que desee redondear. Para redondear los importes, elija las entradas y luego elija la acción **Aceptar selección**. Puede usar la acción **Buscar entradas con problemas** para actualizar la lista con nuevos problemas que ocurrieron después de que se ejecutó la entrada de la cola de trabajos el domingo anterior.

## Consulte también
[Activos fijos](fa-manage.md)  
[Administrar activos fijos](fa-manage.md)  
[Mantener activos fijos](fa-how-maintain.md)  
[Personalizar Business Central Online con extensiones](ui-extensions.md)  
[Finanzas](finance.md)  
[Preparación para hacer negocios](ui-get-ready-business.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]



