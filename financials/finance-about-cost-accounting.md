---
title: Acerca de la contabilidad de costes | Documentos de Microsoft
description: "La contabilidad de costes puede ayudarle a conocer los costes de la dirección de una empresa."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/16/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: b38e86fa63e179c1bd4ac78c29d7728716755e0c
ms.contentlocale: es-es
ms.lasthandoff: 09/22/2017

---
# <a name="about-cost-accounting"></a>Acerca de la contabilidad de costes
La contabilidad de costes puede ayudarle a conocer los costes de la dirección de una empresa. La información de contabilidad de costes se ha diseñado para analizar:  

-   ¿Cuáles son los tipos de costes que se tienen cuando se dirige una empresa?  
-   ¿Dónde se producen los costes?  
-   ¿Quién asume los costes?  

En contabilidad de costes, puede asignar costes reales y presupuestados de las operaciones, departamentos, productos y proyectos para analizar la rentabilidad de su empresa.  

## <a name="workflow-in-cost-accounting"></a>Flujo de trabajo en contabilidad de costes  
Contabilidad de costes tiene los siguientes componentes principales:  

-   Tipos de coste, centros de coste y objetos de costes  
-   Movimientos de costes y diarios de costes  
-   Asignaciones coste  
-   Presupuestos coste
-   Información de coste  

El diagrama siguiente muestra el flujo de trabajo en contabilidad de costes.  

![Resumen de la contabilidad de costes](media/costaccountingoverview.png "ResumenContabilidadCostes")  

## <a name="cost-types-cost-centers-and-cost-objects"></a>Tipos de coste, centros de coste y objetos de costes  
Define los tipos de coste, los centros de coste y los objetos de coste para analizar cuáles son los costes, de dónde provienen y quién debe asumirlos.  

Define un plan de tipos de coste con una estructura y funciones que se asemejan al plan de cuentas de contabilidad. Puede transferir las cuentas de ingresos de la contabilidad o crear su propio plan de tipos de coste.  

Los centros de coste son departamentos y los centros de beneficios que son responsables de los costes y de los ingresos. A menudo, hay más centros de coste configurados en la contabilidad de costes que en cualquier dimensión configurada en la contabilidad. En la contabilidad, normalmente sólo se utilizan los centros de coste del primer nivel para costes directos y costes iniciales. En contabilidad de costes, centros de coste adicionales se crean para niveles de asignación adicionales.  

Los objetos de coste son productos, grupos de productos o servicios de una empresa. Son productos terminados de una empresa que incluyen los costes.  

Puede relacionar los centros de coste a los departamentos y los objetos de coste a los proyectos en su empresa. Sin embargo, puede vincular los centros de coste y los objetos de coste a cualquier dimensión en la contabilidad y complementarlos con subtotales y títulos.  

## <a name="cost-entries-and-cost-journals"></a>Movimientos de costes y diarios de costes  
Los costes operativos se pueden transferir desde la contabilidad. Puede transferir automáticamente los movimientos de coste de la contabilidad a los movimientos de coste con cada registro. También puede utilizar un trabajo por lotes para transferir movimientos de contabilidad a movimientos de coste basados en los registros de resúmenes diarios o mensuales.  

En los diarios de costes, puede registrar costes y actividades que no provengan de la contabilidad general ni se generen por asignaciones. Por ejemplo, puede registrar costes puros operativos, gastos internos, distribuciones y movimientos de corrección entre tipos de coste, centros de coste y objetos de coste por separado o periódicamente.  

## <a name="cost-allocations"></a>Asignaciones de costes  
Las asignaciones mueven los costes e ingresos entre tipos de coste, centros de coste y objetos de coste. Los costes generales se registran primero a centros de coste y luego se cargan a objetos de coste. Por ejemplo, esto se puede realizar en un departamento de ventas que vende varios productos al mismo tiempo. Los costes directos pueden distribuirse directamente a un objeto de coste, por ejemplo, un material comprado para un producto específico.  

La base de asignaciones que se utiliza y la exactitud de la definición de asignación tienen una influencia en el resultado de las asignaciones de costes. La definición de la asignación se utiliza para asignar costes primero de los llamados centros de pre-coste a centros de coste principales y después de centros de coste a objetos de coste.  

Cada asignación está formada por un origen de asignación y uno o varios destinos de asignación. Puede distribuir valores reales o valores presupuestados utilizando el método de asignación estática que se basa en un valor definido, como metros cuadrados, o una proporción de asignación establecida de 5:2: 4. También puede asignar valores reales o valores presupuestados utilizando el método de asignación dinámica con nueve bases predefinidas de asignación y 12 rangos de fechas dinámicas.  

## <a name="cost-budgets"></a>Presupuestos de costes  
Puede crear tantos presupuestos de coste como sea necesario. Puede copiar el presupuesto de costes en el presupuesto de contabilidad y viceversa. Puede transferir los costes presupuestados como costes reales.  

## <a name="cost-reporting"></a>Información de coste  
La mayoría de los informes y las estadística se basan en los movimientos de costes registrados. Puede definir el orden de los resultados y usar filtros para definir qué datos deben mostrarse. Puede crear informes para el análisis de distribución del coste. Además, puede utilizar los esquemas de cuenta estándar para definir cómo se muestran los informes para el plan de tipos de coste.  

## <a name="see-also"></a>Consulte también  
 [Contabilidad para costes](finance-manage-cost-accounting.md)  
 [Finanzas](finance.md)   
 [Terminología en contabilidad de costes](finance-terminology-in-cost-accounting.md)  
 [Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

