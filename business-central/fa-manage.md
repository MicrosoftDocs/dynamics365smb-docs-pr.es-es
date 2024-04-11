---
title: Administrar activos fijos (contiene vídeo)
description: Obtenga información sobre la funcionalidad de activos fijos y obtenga un resumen de cómo trabajar y administrar activos fijos.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: conceptual
ms.search.keywords: 'machinery, buildings'
ms.search.form: '5604, 5606, 5664, 5601, 5602, 5658, 5603, 5671, 5641, 5629, 5633, 5634, 5649, 5622, 5650'
ms.date: 03/25/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# Administrar activos fijos

La funcionalidad Activos fijos de [!INCLUDE[prod_short](includes/prod_short.md)] proporciona un resumen de sus activos y asegura una correcta amortización periódica. También le permite realizar un seguimiento de los costes de mantenimiento, gestionar las pólizas de seguros, registrar transacciones de activos y generar diversos informes y estadísticas.

## Resumen en vídeo

El siguiente video cubre los conceptos básicos de los activos fijos:

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4AegS?rel=0]

## Información general de los activos fijos

Deberá configurar una ficha con la información de cada activo. Puede configurar los edificios o los bienes de producción como activos principales con una lista de componentes y puede agruparlos de diferentes maneras como, por ejemplo, por clase, departamento o ubicación. Ahora puede empezar a adquirir, mantener y vender los activos fijos. También puede configurar activos presupuestados. El presupuesto le permite incluir adquisiciones y ventas anticipadas en los informes.

> [!IMPORTANT]
> Antes de poder administrar activos fijos, debe completar las siguientes configuraciones:
>
> * Valores predeterminados
> * Contabilidad de activos fijos
> * Grupos contables
> * Claves de asignación
> * Diarios de activos fijos
>
> Para obtener más información, vea [Configurar activos fijos](fa-setup.md).

Para realizar un seguimiento de las amortizaciones de activos y otras transacciones financieras relacionadas con los activos, configure uno o varios libros de amortización para cada uno. La amortización se calcula con la ejecución de un informe que calcula las amortizaciones periódicas y rellena un diario con los movimientos resultantes y después se registra el diario. [!INCLUDE[prod_short](includes/prod_short.md)] admite varios métodos de amortización. Para obtener más información, consulte [Métodos de amortización](fa-depreciation-methods.md). Puede configurar varios libros de amortización de activos para propósitos distintos, por ejemplo, uno para la notificación de impuestos y otro para la elaboración de informes internos.

Puede registrar los costes de mantenimiento y la fecha del siguiente servicio de cada activo. Realizar un seguimiento de los gastos de mantenimiento puede ser importante de cara al presupuesto y para decidir el reemplazo de un activo.

Puede vincular cada activo fijo a una o más pólizas de seguro y verificar que las primas de las pólizas se alineen con el valor de los activos.

> [!NOTE]  
> Puede registrar transacciones de activos en las páginas **A/F Diario general** o **Diario activos fijos**, dependiendo de si las transacciones son para la información financiera o la gestión interna. La ayuda para los activos fijos solo describe cómo utilizar la página **A/F Diario general**. Para obtener más información, consulte [Configurar amortización de activos fijos](fa-how-setup-depreciation.md).

## Cómo usar activos fijos

En la tabla siguiente se indican una serie de tareas con vínculos a los artículos que las describen.

| Para  | Vea |
| --- | --- |
| Establezca los requisitos previos para utilizar la función de activos fijos (definición de valores predeterminados, contabilidad de activos fijos, grupos de contabilización, claves de asignación, diarios y tipos de contabilización). | [Configuración de activos fijos](fa-setup.md)|
| Crear activos fijos, asignar métodos de amortización, registrar adquisiciones, valores residuales e imprimir listas de activos fijos. |[Activos fijos adquiridos](fa-how-acquire.md) |
| Registrar visitas de servicio y registrar y monitorizar costes de mantenimiento. |[Mantener activos fijos](fa-how-maintain.md) |
| Actualizar información de seguros, registrar costes en pólizas de seguros, modificar la cobertura del seguro, ver estadísticas de seguros y listar pólizas de seguros. |[Aseguramiento de activos fijos](fa-how-insure.md) |
| Reclasificar activos fijos, transferir activos fijos a distintas ubicaciones, dividir o combinar activos. |[Permite transferir, dividir o combinar activos fijos](fa-how-trans-split-combine.md) |
| Ajustar valores de activos fijos, registrar apreciación y transacciones de depreciación. |[Revalorizar activos fijos](fa-how-revalue.md) |
| Registrar y calcular la amortización y analizarla en informes de activos fijos. |[Depreciar o amortizar activos fijos](fa-how-depreciate-amortize.md) |
| Conocer varios métodos de amortización de activos fijos. |[Métodos de depreciación](fa-depreciation-methods.md) |
| Registrar transacciones de venta/baja, ver movimientos de venta/baja y registrar ventas/bajas parciales. |[Cancelar o retirar activos fijos](fa-how-dispose-retire.md) |
| Gestionar presupuestos de activos fijos, costes, ventas/bajas y amortización. |[Administrar presupuestos para activos fijos.](fa-how-manage-budgets.md) |
| Obtenga más información sobre las capacidades integradas de informes y análisis para activos fijos. | [Informes y análisis de activos fijos](fa-reports.md) |

## Consulte también

[Configuración de activos fijos](fa-setup.md)  
[Información general sobre finanzas](finance.md)  
[Preparación para hacer negocios](ui-get-ready-business.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Cambiar las funciones que se muestran](ui-experiences.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
