---
title: 'Mensaje de error: "La fecha de registro no está comprendida en su periodo de fechas de registro permitidas"'
description: 'Resuelva el error del mensaje "La fecha de registro no está comprendida en su periodo de fechas de registro permitidas" al ejecutar el trabajo por lotes Ajustar coste: movimientos de producto.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 09/17/2021
ms.author: bholtorf
---

# <a name="error-message-posting-date-is-not-within-your-range-of-allowed-posting-dates"></a>Mensaje de error: "La fecha de registro no está comprendida en su periodo de fechas de registro permitidas"

Al usar el trabajo por lotes **Ajustar coste: movimientos de producto** puede encontrarse con el siguiente mensaje de error:

**La fecha de registro no está comprendida en su periodo de fechas de registro permitidas**

Este mensaje de error indica que el usuario no puede publicar registros para la fecha en cuestión, y esto se puede solucionar cambiando la configuración del usuario.

## <a name="change-the-user-setup"></a>Cambiar la configuración del usuario

|Id. de usuario  |Permitir registro desde  | Permitir registro hasta  |
|---------|---------|--------|
|EUROPA  |  2020-09-11      |2020-09-30      |

El usuario en este caso tiene un rango de fechas de registro permitidas desde el 11 hasta el 30 de septiembre y, por lo tanto, no puede registrar el movimiento de valor de ajuste con fecha de publicación el 10 de septiembre.  

### <a name="overview-of-involved-posting-date-setup"></a>Descripción general de la configuración de la fecha de registro involucrada

#### <a name="inventory-periods"></a>Periodos de inventario

|Fecha final  |Name  |Cerrada  |
|---------|---------|---------|
|2020-01-31     |2020 de enero      |  Sí    |
|2020-02-28     |Febrero de 2020     |  Sí    |
|2020-03-31     |Marzo de 2020        |  Sí    |
|2020-04-30     |Abril de 2020        |  Sí    |
|2020-05-31     |Mayo de 2020        |  Sí    |
|2020-06-30     |Junio de 2020       |  Sí    |
|2020-07-31     |Julio de 2020        |   Sí   |
|2020-08-31     |Agosto de 2020     |   Sí   |
|2020-09-30     |Septiembre de 2020  |         |
|2020-10-31     |Octubre de 2020    |         |
|2020-11-30     |Noviembre de 2020   |         |
|2020-12-31     |Diciembre de 2020   |         |  

#### <a name="general-ledger-setup"></a>Configuración de contabilidad

|Campo|Valor|
|---------|---------|
|Permitir registro desde:  |  2020-09-10      |
|Permitir registro hasta:    |  2020-09-30      |
|Registrar tiempo:       |         |
|Formato dirección local:|   C.P.      |  

#### <a name="user-setup"></a>Configuración de usuarios

|Id. de usuario  |Permitir registro desde  | Permitir registro hasta  |
|---------|---------|--------|
|USERNAME |  2020-09-10      |2020-09-30      |

Al asignar un rango de fechas de registro permitido más amplio que en el periodo de inventario o la configuración de contabilidad, será posible evitar el conflicto que provoca el mensaje de error. El movimiento valor de ajuste con fecha de contabilización del 10 de septiembre se contabilizará correctamente con esta configuración.
  
## <a name="see-also"></a>Consulte también

[Detalles de diseño: Fecha registro en el movimiento de valor de ajuste](design-details-inventory-adjustment-value-entry-posting-date.md)  
[Detalles de diseño: Coste de inventario](design-details-inventory-costing.md)  
[Detalles de diseño: Liquidación de productos](design-details-item-application.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
