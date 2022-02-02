---
title: Informes y análisis de cuentas por pagar
description: Consulte qué informes y análisis están disponibles en la versión estándar de Business Central para que pueda realizar un seguimiento de sus cuentas por pagar.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: reporting
ms.search.form: 347
ms.date: 07/13/2021
ms.author: edupont
ms.openlocfilehash: edb3b32f88198d8e21aa2bfddafc1b7f319be9de
ms.sourcegitcommit: e008b3d7003c256475d6c606e5f7c9866a6bbb72
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/10/2022
ms.locfileid: "7953389"
---
# <a name="accounts-payable-reports-and-analytics-in-business-central"></a>Informes y análisis de cuentas por pagar en Business Central

Para ayudarlo a administrar sus cuentas por pagar en [!INCLUDE [prod_short](includes/prod_short.md)], los informes y análisis estándar están integrados. Va más allá de las restricciones tradicionales de los informes, para ayudarle a diseñar diversos tipos de informes.  

## <a name="reports"></a>Informes

La siguiente tabla describe algunos de los informes clave en los informes de cuentas por pagar.

| Informe | Id. de objeto | Descripción |
|--|--|--|
| **Antigüedad pagos** | 322|Muestra los saldos vencidos de los proveedores en intervalos de tiempo vencidos. Los importes vencidos se pueden mostrar por fecha de vencimiento, fecha de registro o por fecha de documento, según sea necesario. Puede optar por mostrar los importes en moneda local (DL) e imprimir los detalles de los documentos vencidos. Los intervalos de tiempo pueden tener encabezados con fechas o con el número de fechas vencidas, en relación con el vencimiento especificado por tipo.<br>Este informe es el informe principal para conciliar proveedores con contabilidad. Suponiendo que no ha permitido el registro directo en las cuentas utilizadas en la cuenta por pagar de los grupos de registro de proveedores, este informe es una especificación de los importes que encuentra en contabilidad.|
| **Proveedor - Saldo por fechas** | 321 | Muestra el saldo del proveedor en la fecha de finalización del rango de fechas especificado. Puede optar por mostrar el saldo del proveedor en su moneda local (DL). Seleccione el campo **Incluir movs. no liquidados** para mostrar las entradas que se han cerrado antes de la fecha de finalización, pero que no se han liquidado (abierto) en una fecha posterior. Seleccione **Mostrar movs. con saldo cero** para mostrar los proveedores con un saldo de cero en la fecha de finalización del filtro de fecha. El filtro de fecha se aplica a los movimientos detallados del libro mayor de proveedores para los movimientos del informe. Si tiene pagos posteriores a la fecha de finalización que se han aplicado a las facturas dentro del rango de fechas, las facturas aparecerán en el informe ya que no se han cerrado según la fecha de finalización. |
| **Proveedor - Balance sumas y saldos** | 329 | Muestra los cambios netos para los proveedores durante el período especificado en el filtro de fecha, así como el cambio neto acumulado anual para el ejercicio fiscal correspondiente al período seleccionado. El informe está agrupado por grupos de registro de proveedores y ofrecerá una vista del libro mayor de proveedores diferente al informe **Antigüedad pagos**. **Nota**: Si no ha configurado ningún período contable, el sistema no sabrá qué año fiscal utilizar y mostrará el acumulado anual del año fiscal más reciente definido o simplemente seleccionará el período, que puede ser o no desde el comienzo de un año.|
| **Proveedor - Balance de comprobación detallado** | 304 | Muestra todos los movimientos del libro mayor de proveedores en el filtro de fecha especificado. El informe muestra los saldos iniciales del proveedor en relación con el filtro de fecha. |
| **Estadísticas compras** |312 |[!INCLUDE [reports-purchase-statistics](includes/reports-purchase-statistics.md)]<br>Este informe también se puede utilizar en cuentas por pagar, ya que es más fácil realizar una búsqueda rápida de los pagos, descuentos y otras transacciones para un proveedor determinado.|
|**Proveedor - Pagos por periodos**|305| Informe heredado para cuentas por pagar vencidas. Le recomendamos que utilice el informe **Antigüedad pagos** en su lugar. Puede elegir una duración de período y una fecha para usar según la fecha de *vencimiento* establecida.|
|**Pagos retenidos**|319|Muestra los movimientos de proveedores donde el campo **Esperar** no está en blanco.|
|**Diario de prepago del proveedor**|317|Muestra el diario de pagos con información de tolerancia y descuento de pago. El informe se puede utilizar para verificar pagos antes de crear archivos de pago y registrar el diario. **Nota**: El informe mostrará los descuentos de pago de forma incorrecta cuando se hayan utilizado varias notas de crédito en una aplicación. En este caso, el descuento de pago de los abonos adicionales se mostrará como una cantidad no liquidada.|
|**Proveedor - Lista**|301|Muestra información básica de distinta índole sobre los proveedores, como grupo contable proveedor, información sobre pagos y descuentos, nivel de prioridad y divisa predeterminada, así como el saldo actual (en DL). Utilice el informe, por ejemplo, para mantener la información de la tabla Proveedor.|

## <a name="see-also"></a>Consulte también .

[Análisis de estados financieros en Microsoft Excel](finance-analyze-excel.md)  
[Trabajar con dimensiones](finance-dimensions.md)  
[Administrar activos fijos](fa-manage.md)  
[Información general de funcionalidad local](about-localization.md)  
[Experiencias contables en [!INCLUDE[prod_long](includes/prod_long.md)]](finance-accounting.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
