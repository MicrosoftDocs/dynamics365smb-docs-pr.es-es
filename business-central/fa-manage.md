---
title: Administrar activos fijos (contiene vídeo)
description: Obtenga información sobre la funcionalidad de activos fijos y obtenga un resumen de cómo trabajar y administrar activos fijos.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'machinery, buildings'
ms.search.form: '5604, 5606, 5664, 5601, 5602, 5658, 5603, 5671, 5641, 5629, 5633, 5634, 5649, 5622, 5650'
ms.date: 05/06/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# <a name="manage-fixed-assets"></a>Administrar activos fijos

La funcionalidad de activos fijos de [!INCLUDE[prod_short](includes/prod_short.md)] proporciona un resumen de sus activos y ayuda a garantizar que su depreciación sea correcta. También le permite realizar un seguimiento de los costes de mantenimiento, gestionar las pólizas de seguros, registrar transacciones de activos y generar diversos informes y estadísticas.

## <a name="video-overview"></a>Resumen en vídeo

El siguiente video cubre los conceptos básicos de los activos fijos:

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4AegS?rel=0]

## <a name="initial-setup-of-fixed-assets"></a>Configuración inicial de activos fijos

Antes de poder administrar activos fijos, debe completar las siguientes configuraciones:

- Valores predeterminados
- Contabilidad de activos fijos
- Grupos y tipos de publicaciones
- Claves de asignación
- Diarios de activos fijos

Obtenga más información, vaya a [Configurar activos fijos](fa-setup.md).

## <a name="fixed-assets-analytics"></a>Análisis de activos fijos

Esta sección describe las herramientas de análisis que puede usar para obtener información sobre sus activos fijos.

| Para... | Vea |
| --- | --- |
| Obtenga información sobre las capacidades para analizar datos sobre activos fijos. | [Información general de los análisis de activos fijos](fa-analytics-overview.md) |
| Realice análisis ad hoc de los datos sobre activos fijos directamente en las páginas de listas y consultas. | [Análisis ad-hoc de datos de activos fijos](ad-hoc-analysis-fa.md) |
| Explore informes de activos fijos integrados. | [Informes de activos fijos integrados](fa-reports.md) |
| Supervise costes de mantenimiento. | [Supervisar costes de mantenimiento](fa-how-maintain.md#to-monitor-maintenance-costs)|
| Controle la cobertura de seguros. | [Controlar la cobertura de seguros](fa-how-insure.md#to-monitor-insurance-coverage) |
| Ver movimientos de venta/baja. | [Ver movimientos de venta/baja](fa-how-dispose-retire.md#to-view-disposal-ledger-entries) |
| Vea valores de disposición proyectados. | [Ver valores venta/baja previstos](fa-how-manage-budgets.md#to-view-projected-disposal-values) |

## <a name="register-fixed-assets"></a>Registrar activos fijos

Para cada activo fijo debe configurar una ficha que contiene información sobre el mismo. Por ejemplo, puede configurar los edificios o los bienes de producción como activos principales con una lista de componentes. Puede agrupar los activos de varias formas, como por clase, departamento o ubicación. Ahora puede adquirir, mantener y vender los activos fijos. También puede configurar activos presupuestados. El presupuesto le permite incluir adquisiciones y ventas anticipadas en los informes.

| Para  | Vea |
| --- | --- |
| Gestionar presupuestos de activos fijos, costes, ventas/bajas y amortización. |[Administrar presupuestos para activos fijos.](fa-how-manage-budgets.md) |
| Crear activos fijos, asignar métodos de amortización, registrar adquisiciones, valores residuales e imprimir listas de activos fijos. |[Adquirir activos fijos](fa-how-acquire.md) |

## <a name="set-up-depreciations-for-your-fixed-assets"></a>Establecer amortizaciones para los activos fijos

Para realizar un seguimiento de las amortizaciones de activos y otras transacciones financieras relacionadas con los activos, configure uno o varios libros de amortización para cada uno. Hay unos cuantos pasos para depreciar los activos:

1. Ejecute un informe para calcular amortizaciones periódicas.
1. Rellene un diario con las entradas resultantes.
1. Registre el diario.

[!INCLUDE[prod_short](includes/prod_short.md)] admite varios métodos de amortización. Para obtener más información, vaya a [Métodos de depreciación](fa-depreciation-methods.md). Puede configurar varios libros de amortización de cada activo fijo para propósitos distintos, por ejemplo, uno para la notificación de impuestos y otro para la elaboración de informes internos.

| Para  | Vea |
| --- | --- |
| Conocer varios métodos de amortización de activos fijos. |[Métodos de depreciación](fa-depreciation-methods.md) |
| Registrar y calcular la amortización y analizarla en informes de activos fijos. |[Depreciar o amortizar activos fijos](fa-how-depreciate-amortize.md) |
| Ver valores contables de depreciación modificados. | [Ver valores modificados del libro de amortización](fa-how-trans-split-combine.md#to-view-changed-depreciation-book-values-due-to-fixed-asset-reclassification) |
| Registre manualmente transacciones de activos en las páginas **A/F Diario general** o **Diario activos fijos**, dependiendo de si las transacciones son para la información financiera o la gestión interna. | [Configurar amortización de activos fijos](fa-how-setup-depreciation.md) |

## <a name="fixed-assets-maintenance-and-insurance"></a>Mantenimiento y seguros de activos fijos

Puede registrar los costes de mantenimiento y la fecha del siguiente servicio de cada activo para cada activo. Realizar un seguimiento de los gastos de mantenimiento puede ser importante de cara al presupuesto y para decidir el reemplazo de un activo. Puede vincular cada activo fijo a una o más pólizas de seguro y verificar que las primas de las pólizas se alineen con el valor de los activos.

| Para  | Vea |
| --- | --- |
| Registrar visitas de servicio y registrar y monitorizar costes de mantenimiento. |[Mantener activos fijos](fa-how-maintain.md) |
| Supervise costes de mantenimiento. | [Supervisar costes de mantenimiento](fa-how-maintain.md#to-monitor-maintenance-costs)|
| Actualizar información de seguros, registrar costes en pólizas de seguros, modificar la cobertura del seguro, ver estadísticas de seguros y listar pólizas de seguros. |[Asegurar activos fijos](fa-how-insure.md) |
| Controle la cobertura de seguros. | [Controlar la cobertura de seguros](fa-how-insure.md#to-monitor-insurance-coverage) |

## <a name="reclassify-transfer-split-upcombine-adjust-value-write-down-and-dispose-fixed-assets"></a>Reclasificar, transferir, dividir/combinar, ajustar valor, amortizar y enajenar activos fijos

| Para  | Vea |
| --- | --- |
| Reclasificar activos fijos, transferir activos fijos a distintas ubicaciones, dividir o combinar activos. |[Permite transferir, dividir o combinar activos fijos](fa-how-trans-split-combine.md) |
| Ajustar valores de activos fijos, registrar apreciación y transacciones de depreciación. |[Revalorizar activos fijos](fa-how-revalue.md) |
| Registrar transacciones de venta/baja, ver movimientos de venta/baja y registrar ventas/bajas parciales. |[Cancelar o retirar activos fijos](fa-how-dispose-retire.md) |
| Ver movimientos de venta/baja. | [Ver movimientos de venta/baja](fa-how-dispose-retire.md#to-view-disposal-ledger-entries) |
| Vea valores de disposición proyectados. | [Ver valores venta/baja previstos](fa-how-manage-budgets.md#to-view-projected-disposal-values) |

## <a name="see-also"></a>Consulte también

[Configuración de activos fijos](fa-setup.md)  
[Visión general del análisis de activos fijos](fa-analytics-overview.md)  
[Información general sobre finanzas](finance.md)  
[Preparación para hacer negocios](ui-get-ready-business.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Cambiar las funciones que se muestran](ui-experiences.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
