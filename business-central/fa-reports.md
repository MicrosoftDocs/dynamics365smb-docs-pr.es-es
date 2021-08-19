---
title: Informes y análisis de activos fijos
description: Consulte qué informes y análisis están disponibles en la versión estándar de Business Central para que pueda realizar un seguimiento de sus activos fijos.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: reporting
ms.date: 07/13/2021
ms.author: edupont
ms.openlocfilehash: c28e62a2de51323e0a7dcd2f4b5ea26d5896d718
ms.sourcegitcommit: a486aa1760519c380b8cdc8fdf614bed306b65ea
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 07/13/2021
ms.locfileid: "6543369"
---
# <a name="fixed-assets-reports-and-analytics-in-business-central"></a>Informes y análisis de activos fijos en Business Central

Para ayudarlo a administrar sus activos fijos en [!INCLUDE [prod_short](includes/prod_short.md)], los informes y análisis estándar están integrados. Va más allá de las restricciones tradicionales de los informes, para ayudarle a diseñar diversos tipos de informes.  

## <a name="reports"></a>Informes

La siguiente tabla describe algunos de los informes clave en los informes de activos fijos.

| Informe | Id. de objeto | Descripción |
|--|--|--|
| **Lista de activos fijos** | 5601 | Muestra la lista de activos fijos y su información de configuración para un libro de amortización determinado. |
| **A/F - Lista adquisición** | 5608 | Enumere todos los activos adquiridos dentro de un rango de fechas determinado. También puede incluir activos fijos creados pero que aún no se han adquirido. |
| **Detalles de activos fijos** | 5604 | Muestra los movimientos contables de activos fijos. |
| **Análisis de activos fijos** | 5600 | Un informe de análisis donde puede especificar dos columnas de fecha y tres columnas de datos para ver en el informe. Por ejemplo, para generar un informe que se utilizará para conciliar con el libro mayor, agregue columnas para el coste de adquisición en la fecha de finalización, la amortización en la fecha de finalización y el valor contable en la fecha de finalización. Un informe de verificación podría tener adquisiciones/cambio neto, amortización/cambio neto y apreciación/cambio neto, por lo que cada cambio en el activo fijo se puede verificar si es necesario. Si selecciona el campo **Informe presupuesto** y especifica una fecha de finalización en el futuro, el informe calculará la amortización futura y puede proporcionar estimaciones para la amortización futura y los valores contables, si seleccionó esos campos como columnas del informe. |
| **Valor proyectado de activo fijo** | 5607 | Muestra los importes de amortización proyectados y el valor neto para un período futuro para los activos. El informe es útil cuando utiliza diferentes métodos de amortización para sus activos y desea estimar la amortización del próximo año, por ejemplo. Utilice el informe para crear los importes presupuestarios para amortización seleccionando un presupuesto y el campo **Copiar a nomb. ppto. cont.**. |
| **Valor contable de activo fijo 01** | 5605 | Muestra información detallada acerca del coste de adquisición, el valor de amortización y el valor neto tanto de activos individuales como de grupos de activos. Para cada uno de estos tres tipos de importe, los importes se calculan al inicio y al final de un periodo especificado y para el propio periodo. Si selecciona el campo **Informe presupuesto**, el informe calculará la amortización esperada para el período. Escriba un *tipo de grupo* si desea que el informe agrupe los activos e imprima los totales de grupo. Por ejemplo, si ha configurado seis clases de activos, seleccione la opción *A/F Clase* para imprimir los totales de grupo de los seis códigos de clase.|
| **Valor contable de activo fijo 02** | 5606 |Muestra el desglose del valor neto de los activos fijos por cambios en adquisiciones, amortización y apreciación dentro del período con un desglose adicional por adiciones y ventas/bajas dentro del período. Utilice este informe para describir los cambios en los activos fijos durante un período determinado cuando se producen muchos cambios diferentes en la agrupación de activos fijos. Si selecciona el campo **Informe presupuesto**, el informe calculará la amortización esperada para el período. Escriba un *tipo de grupo* si desea que el informe agrupe los activos e imprima los totales de grupo. Por ejemplo, si ha configurado seis clases de activos, seleccione la opción *A/F Clase* para imprimir los totales de grupo de los seis códigos de clase. |
| **Análisis de contabilidad de activo fijo**| 5610 |Muestra un análisis de los activos fijos (A/F) con diversos tipos de datos, tanto para activos individuales como para grupos de activos. En la ficha desplegable Activos fijos, puede definir filtros si desea que el informe sólo incluya determinados activos fijos. En la ficha desplegable Opciones, adapte el informe para satisfacer sus necesidades específicas. El informe es similar al informe **Análisis de activos fijos**, pero específicamente para conciliar con el libro mayor y específicamente para validar los movimientos de venta/baja. El informe asume que conoce las cuentas contables que se especifican en la configuración contable. |
| **A/F - Registro movs.** |5603  |Muestra los movimientos registrados de la contabilidad de activos fijos, ordenados y agrupados en función de su número de registro. Es posible determinar los movimientos de los registros que se muestran configurando un filtro. Es importante definir un filtro ya que, en caso contrario, el informe puede mostrar una gran cantidad de información. |

## <a name="see-also"></a>Consulte también .

[Análisis de estados financieros en Microsoft Excel](finance-analyze-excel.md)  
[Trabajar con dimensiones](finance-dimensions.md)  
[Administrar activos fijos](fa-manage.md)  
[Información general de funcionalidad local](about-localization.md)  
[Experiencias contables en [!INCLUDE[prod_long](includes/prod_long.md)]](finance-accounting.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]