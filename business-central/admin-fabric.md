---
title: Introducción a Microsoft Fabric y Business Central
description: 'Obtener uan introducción al uso de Microsoft Fabric para conseguir información, inteligencia empresarial y KPI desde los datos de Business Central.'
author: kennienp
ms.topic: overview
ms.search.keywords: 'account schedule, analysis, reporting, financial report, business intelligence, KPI'
ms.search.form: '6316, 6317'
ms.reviewer: bholtorf
ms.date: 04/24/2024
ms.author: kepontop
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="introduction-to-microsoft-fabric-and-business-central"></a>Introducción a Microsoft Fabric y Business Central

[!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] es una solución de análisis de extremo a extremo con capacidades de servicio completo que incluyen movimiento de datos, lagos de datos, ingeniería de datos, integración de datos, ciencia de datos, análisis en tiempo real e inteligencia empresarial, todo respaldado por una plataforma compartida que proporciona seguridad, gobernanza y cumplimiento de datos. Su organización ya no necesita unir servicios de análisis individuales de múltiples proveedores. En su lugar, use una solución optimizada que sea fácil de conectar, incorporar y operar.

> [!NOTE]
> Para obtener información acerca del plan de lanzamiento de Microsoft Fabric, consulte [aka.ms/FabricRoadmap](https://aka.ms/FabricRoadmap)
> 
> La publicación periódica de esta hoja de ruta le ayudará a mantenerse informado sobre cómo [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] atenderá a sus necesidades.

## <a name="where-does--fit-into-includeprod_short-analytics"></a>Dónde encaja [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] en los análisis de [!INCLUDE[prod_short](includes/prod_short.md)]

[!INCLUDE[prod_short](includes/prod_short.md)] incluye muchos informes listos para usar y capacidades de análisis de datos, como informes financieros, apertura en Excel y modo de análisis en listas y consultas. Además de esto, es fácil definir informes Power BI que leen datos de API estándar y personalizadas, definir cuadros de mando de métricas de Power BI e incrustarlos todos directamente en el cliente de [!INCLUDE[prod_short](includes/prod_short.md)]. Pero para los clientes con escenarios de ciencia de datos o inteligencia empresarial más avanzados que requieren ingeniería o integración de datos más completa, [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] podría ser una buena opción. 

## <a name="onelake"></a>OneLake

Una parte clave de la oferta de [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] es OneLake. OneLake es un lago de datos lógico, único y unificado para toda la organización. Puede pensar en OneLake como el OneDrive para datos. Le proporciona un lago de datos como servicio sin tener que crearlo usted mismo. OneLake viene automáticamente con cada inquilino de [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] sin infraestructura que gestionar. Todos los datos que llegan a OneLake participan automáticamente en una gobernanza de datos lista para usar, como linaje de datos, protección de datos, certificación e integración de catálogos. Rompe los silos de datos al permitir que diferentes partes de la organización trabajen de forma independiente y al mismo tiempo contribuyan al mismo lago de datos.

Los elementos de [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] almacenan sus datos en OneLake en un formato de archivo abierto. Para datos tabulares estructurados, este formato es *delta parquet*. El formato delta parquet permite que todos los motores de análisis en [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] accedan a los datos de otros motores de análisis. De esta manera, los profesionales de datos tienen flexibilidad para utilizar las herramientas que elijan.

> [!NOTE]
> Esperamos que con uno de nuestros futuros lanzamientos, los datos de [!INCLUDE[prod_short](includes/prod_short.md)] también estén disponibles en OneLake para los clientes que utilicen [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] y [!INCLUDE[prod_short](includes/prod_short.md)] y tengan requisitos únicos en las áreas que respalda [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)]. La escala de tiempo dependerá del cronograma de disponibilidad general de [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] y sus componentes necesarios para permitir esta experiencia. Actualizaremos este artículo con una escala de tiempo más precisa, una vez que sepamos más.

## <a name="see-also"></a>Consulte también .
[Usar Power BI con Business Central](admin-powerbi.md)   

[!INCLUDE[footer-include](includes/footer-banner.md)]
