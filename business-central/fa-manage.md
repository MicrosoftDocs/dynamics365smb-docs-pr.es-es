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

# Administrar activos fijos

La funcionalidad de activos fijos de [!INCLUDE[prod_short](includes/prod_short.md)] proporciona un resumen de sus activos y ayuda a garantizar que su depreciación sea correcta. También le ayuda a realizar un seguimiento de los costos de mantenimiento, administrar pólizas de seguro, publicar transacciones de activos fijos y generar diversos informes y estadísticas.

## ¿Qué es un activo fijo?

Los activos fijos se diferencian de otros artículos de su almacén. Un activo fijo, también conocido como activo de capital, es una propiedad, planta o equipo tangible (PP&E) que usted posee o administra con la expectativa de que continuará ayudando a generar ingresos. Un activo es fijo cuando es un artículo que su empresa no consumirá, venderá ni convertirá en efectivo durante el próximo año calendario. Los activos fijos son diferentes de los activos corrientes, que están en efectivo o están programados para convertirse en efectivo dentro de los próximos 12 meses. Los activos fijos también difieren de su inventario, porque el inventario generalmente se consume en poco tiempo.

## Tipos de activos fijos

Las empresas suelen invertir en algunos tipos de activos fijos. Algunos ejemplos son:

- Edificios e instalaciones
- Equipos y software informáticos.
- Muebles y accesorios
- Maquinaria
- Vehículos

## Comprender la contabilidad de activos fijos

La contabilidad de activos fijos significa mantener registros financieros precisos sobre sus activos de capital. Estos registros incluyen detalles sobre las cinco etapas del ciclo de vida de un activo. Después de su compra inicial, el ciclo de vida de cada activo fijo incluye al menos tres de las siguientes etapas:

- Adquisición: Agrega un nuevo activo fijo a sus libros.
- Depreciación: registra la disminución periódica del valor de un activo, que utiliza un método de depreciación para calcular. Para obtener más información, vaya a [Cálculo de depreciación de FA](LocalFunctionality/India/FA_Depreciation.md).
- Revaluación: registra una evaluación del valor justo de mercado actual de un activo. Para obtener más información, vaya a [Revaluar activos fijos](fa-how-revalue.md).
- Deterioro: Se registra una reducción en el valor debido a hechos o circunstancias.
- Enajenación: Usted vende, desecha o utiliza otra forma de disponer de un activo al final de su vida útil.

Las auditorías también se incluyen en los controles detallados de los registros contables de su empresa después del cierre de los libros del ejercicio financiero. Ya sean internas o externas, en las auditorías es posible que notes inconsistencias o diferencias entre tus notas y el estado real de tus activos. Las auditorías promueven la transparencia en sus activos y contabilidad si está perdiendo más dinero del previsto.

## Resumen en vídeo

El siguiente video cubre los conceptos básicos de los activos fijos:

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4AegS?rel=0]

## Configuración inicial de activos fijos

Antes de poder administrar activos fijos, debe completar las siguientes configuraciones:

- Valores predeterminados
- Contabilidad de activos fijos
- Grupos y tipos de publicaciones
- Claves de asignación
- Diarios de activos fijos

Obtenga más información, vaya a [Configurar activos fijos](fa-setup.md).

## Análisis de activos fijos

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

## Registrar activos fijos

Para cada activo fijo debe configurar una ficha que contiene información sobre el mismo. Por ejemplo, puede configurar los edificios o los bienes de producción como activos principales con una lista de componentes. Puede agrupar los activos de varias formas, como por clase, departamento o ubicación. Ahora puede adquirir, mantener y vender los activos fijos. También puede configurar activos presupuestados. El presupuesto le permite incluir adquisiciones y ventas anticipadas en los informes.

| Para  | Vea |
| --- | --- |
| Gestionar presupuestos de activos fijos, costes, ventas/bajas y amortización. |[Administrar presupuestos para activos fijos.](fa-how-manage-budgets.md) |
| Crear activos fijos, asignar métodos de amortización, registrar adquisiciones, valores residuales e imprimir listas de activos fijos. |[Adquirir activos fijos](fa-how-acquire.md) |

## Establecer amortizaciones para los activos fijos

Para realizar un seguimiento de las amortizaciones de activos y otras transacciones financieras relacionadas con los activos, configure uno o varios libros de amortización para cada uno. Hay unos cuantos pasos para depreciar los activos:

1. Ejecute un informe que calcule la depreciación periódica.
1. Rellene un diario con las entradas resultantes.
1. Registre el diario.

[!INCLUDE[prod_short](includes/prod_short.md)] admite varios métodos de amortización. Para obtener más información, vaya a [Métodos de depreciación](fa-depreciation-methods.md). Puede configurar varios libros de amortización de cada activo fijo para propósitos distintos, por ejemplo, uno para la notificación de impuestos y otro para la elaboración de informes internos.

| Para  | Vea |
| --- | --- |
| Conocer varios métodos de amortización de activos fijos. |[Métodos de depreciación](fa-depreciation-methods.md) |
| Registrar y calcular la amortización y analizarla en informes de activos fijos. |[Depreciar o amortizar activos fijos](fa-how-depreciate-amortize.md) |
| Ver valores contables de depreciación modificados. | [Ver valores modificados del libro de amortización](fa-how-trans-split-combine.md#to-view-changed-depreciation-book-values-due-to-fixed-asset-reclassification) |
| Registre manualmente transacciones de activos en las páginas **A/F Diario general** o **Diario activos fijos**, dependiendo de si las transacciones son para la información financiera o la gestión interna. | [Configurar amortización de activos fijos](fa-how-setup-depreciation.md) |

## Mantenimiento y seguros de activos fijos

Puede registrar los costes de mantenimiento y la fecha del siguiente servicio de cada activo para cada activo. Realizar un seguimiento de los gastos de mantenimiento puede ser importante de cara al presupuesto y para decidir el reemplazo de un activo. Puede vincular cada activo fijo a una o más pólizas de seguro y verificar que las primas de las pólizas se alineen con el valor de los activos.

| Para  | Vea |
| --- | --- |
| Registrar visitas de servicio y registrar y monitorizar costes de mantenimiento. |[Mantener activos fijos](fa-how-maintain.md) |
| Supervise costes de mantenimiento. | [Supervisar costes de mantenimiento](fa-how-maintain.md#to-monitor-maintenance-costs)|
| Actualizar información de seguros, registrar costes en pólizas de seguros, modificar la cobertura del seguro, ver estadísticas de seguros y listar pólizas de seguros. |[Asegurar activos fijos](fa-how-insure.md) |
| Controle la cobertura de seguros. | [Controlar la cobertura de seguros](fa-how-insure.md#to-monitor-insurance-coverage) |

## Reclasificar, transferir, dividir/combinar, ajustar valor, amortizar y enajenar activos fijos

| Para  | Vea |
| --- | --- |
| Reclasificar activos fijos, transferir activos fijos a distintas ubicaciones, dividir o combinar activos. |[Permite transferir, dividir o combinar activos fijos](fa-how-trans-split-combine.md) |
| Ajustar valores de activos fijos, registrar apreciación y transacciones de depreciación. |[Revalorizar activos fijos](fa-how-revalue.md) |
| Registrar transacciones de venta/baja, ver movimientos de venta/baja y registrar ventas/bajas parciales. |[Cancelar o retirar activos fijos](fa-how-dispose-retire.md) |
| Ver movimientos de venta/baja. | [Ver movimientos de venta/baja](fa-how-dispose-retire.md#to-view-disposal-ledger-entries) |
| Vea valores de disposición proyectados. | [Ver valores venta/baja previstos](fa-how-manage-budgets.md#to-view-projected-disposal-values) |

## Consejos para mejorar la contabilidad de sus activos fijos

Hay algunas cosas que puede implementar en su estrategia contable para activos fijos que pueden ayudarlo a maximizar sus ganancias.

- Establecer un umbral de capitalización. Cuando compra un artículo, determine una cantidad fija para la capitalización. El monto ayuda a garantizar que sus libros contables sean consistentes y facilita que usted y su equipo detecten errores contables.
- Reevaluar el ciclo de vida del equipo. Es importante estimar correctamente el período de tiempo que puede utilizar sus activos fijos para su propósito original. Debido a que la contabilidad y la depreciación dependen de estimaciones precisas del ciclo de vida, reevalúe cuando sea necesario porque podría cambiar con el tiempo.
- Etiqueta tus activos. Es esencial realizar un seguimiento y etiquetar sus activos durante todo su ciclo de vida porque muchos factores pueden afectar su valor. El etiquetado ayuda a rastrear sus artículos a lo largo de las etapas de su ciclo de vida y ayuda a prevenir robos, eliminar extravíos y respaldar las estadísticas financieras.
- Automatice la información con el software de contabilidad de activos fijos. La automatización de las actividades manuales para realizar un seguimiento de sus datos con un software de contabilidad de activos fijos facilita la finalización de los procesos. La protección con contraseña puede ayudar a proporcionar acceso sólo a las personas que lo necesitan y están capacitadas para ello.

## Consulte también

[Configuración de activos fijos](fa-setup.md)  
[Información general de los análisis de activos fijos](fa-analytics-overview.md)  
[Información general sobre finanzas](finance.md)  
[Preparación para hacer negocios](ui-get-ready-business.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Cambiar las funciones que se muestran](ui-experiences.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
