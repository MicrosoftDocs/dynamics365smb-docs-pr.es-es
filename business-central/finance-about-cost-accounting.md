---
title: Acerca de la contabilidad de costes
description: La contabilidad de costes puede ayudarle a conocer los costes de la dirección de una empresa. La información de contabilidad de costes se ha diseñado para analizar distintos problemas.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.form: '1101, 1103, 1105, 1108, 1111, 1112, 1124, 1123'
ms.date: 05/24/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Acerca de la contabilidad de costes

La contabilidad de costes puede ayudarle a conocer los costes de la dirección de una empresa. La información de contabilidad de costes se ha diseñado para analizar:  

- En qué tipos de costes incurre su empresa.  
- Dónde se producen los costes.
- Quién asume los costes.

En contabilidad de costes, puede asignar costes reales y presupuestados de las operaciones, departamentos, productos y proyectos para analizar la rentabilidad de su empresa.  

## Flujo de trabajo en contabilidad de costes

Contabilidad de costes tiene los siguientes componentes principales:  

- Tipos de coste, centros de coste y objetos de costes  
- Movimientos de costes y diarios de costes  
- Asignaciones coste  
- Presupuestos coste
- Información de coste  

El diagrama siguiente muestra el flujo de trabajo en contabilidad de costes.  

![Resumen de la contabilidad de costes.](media/costaccountingoverview.png "CostAccountingOverview")  

## Tipos de coste, centros de coste y objetos de costes

Define los tipos de coste, los centros de coste y los objetos de coste para analizar cuáles son los costes, de dónde provienen y quién debe asumirlos.  

Primero, define un plan de tipos de coste con una estructura y funciones que se asemejan al plan de cuentas de contabilidad. Puede crear su propio plan de tipos de coste o transferir las cuentas de ingresos de la contabilidad.  

Los centros de coste son departamentos y los centros de beneficios que son responsables de los costes y de los ingresos. A menudo, hay más centros de coste configurados en la contabilidad de costes que en cualquier dimensión configurada en la contabilidad. En la contabilidad, normalmente solo se utilizan los centros de coste del primer nivel para costes directos y costes iniciales. En la contabilidad de costes, se crean más centros de costes para los niveles de imputación adicionales.  

Los objetos de coste son productos, grupos de productos o servicios que ofrece una empresa. Estos objetos son "productos terminados" que incluyen los costes.  

Puede relacionar los centros de coste a los departamentos y los objetos de coste a los proyectos en su empresa. A través de la contabilidad general, puede vincular los centros de coste y los objetos de coste a cualquier dimensión y complementar esa información con subtotales y títulos.  

## Movimientos de costes y diarios de costes

Los costes operativos se pueden transferir desde la contabilidad. Puede transferir automáticamente los movimientos de coste de la contabilidad a los movimientos de coste con cada registro. También puede utilizar un trabajo por lotes para transferir movimientos de contabilidad a movimientos de coste basados en los registros de resúmenes diarios o mensuales.  

En los diarios de costes, puede registrar costes y actividades que no provengan de la contabilidad general ni se generen por asignaciones. Por ejemplo, puede registrar costes puros operativos, gastos internos, distribuciones y movimientos de corrección entre tipos de coste, centros de coste y objetos de coste por separado o periódicamente.  

## Asignaciones coste

Las asignaciones mueven los costes e ingresos entre tipos de coste, centros de coste y objetos de coste. Los costes generales se registran primero a centros de coste y luego se cargan a objetos de coste. Un ejemplo sería realizar en un departamento de ventas que vende varios productos al mismo tiempo. Los gastos generales del departamento, como salarios, suministros y gastos de viaje, se asignan inicialmente al centro de costes de ventas. A continuación, los costes se asignan entre los distintos productos (objetos de coste) vendidos, junto con los materiales adquiridos (coste directo).

La base de asignaciones y la exactitud de la definición de asignación tienen una influencia en el resultado de las asignaciones de costes. La definición de la imputación asigna primero los costes de los llamados centros de costes previos a los centros de costes principales, y después de los centros de costes a los objetos de coste.  

Cada asignación está formada por un origen de asignación y uno o varios destinos de asignación. Puede asignar valores reales o valores presupuestados utilizando el método de asignación estática basado en un valor definido. Por ejemplo, metros cuadrados, o una proporción de asignación establecida de 5:2:4. También puede asignar valores reales o valores presupuestados utilizando el método de asignación dinámica con nueve bases predefinidas de asignación y 12 rangos de fechas dinámicas.  

## Presupuestos coste

De manera similar a la elaboración de presupuestos en el libro mayor, puede crear presupuestos para planificar costos durante un período determinado (por ejemplo, un año fiscal), que se pueden aplicar a un centro de costos (departamento de la empresa) o a un objeto de costo (producto o servicio). Puede crear tantos presupuestos de coste como sea necesario. Luego puede copiar el presupuesto de costes en el presupuesto de contabilidad y viceversa. Y puede transferir los costes presupuestados como costes reales.

## Información de coste

La mayoría de los informes y las estadística se basan en los movimientos de costes registrados. Puede definir el orden de los resultados y usar filtros para definir qué datos deben mostrarse. Puede crear informes para el análisis de distribución del coste. Además, puede utilizar los informes financieros estándar para definir cómo se muestran los informes para el plan de tipos de coste.  

## Consulte también .

[Contabilidad de costes](finance-manage-cost-accounting.md)  
[Finanzas](finance.md)  
[Terminología en contabilidad de costes](finance-terminology-in-cost-accounting.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
