---
title: "Configuración del análisis de flujo de efectivo | Documentos de Microsoft"
description: "Configure los planes en el área de trabajo Cuentas como ayuda para analizar el flujo de dinero de su empresa, incluyendo gastos e ingresos, liquidez y recibos de efectivo menos los pagos en efectivo."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: money flow, expense and income, liquidity, cash receipts minus cash payments, Cartera, funds
ms.date: 06/02/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: ffc0a1c8a513556de2a40fc37db7af9be779225c
ms.contentlocale: es-es
ms.lasthandoff: 09/22/2017

---
# <a name="setting-up-cash-flow-analysis"></a>Configuración del análisis de flujo de efectivo
Si desea ayuda para decidir qué debe hacer con el efectivo, eche un vistazo a los gráficos del Área de trabajo Contable:  

* **Ciclo de efectivo**  
* **Ingresos y gastos**  
* **Flujo de efectivo**  
* **Previsiones de flujo de efectivo**  

En este tema se describe de dónde proceden los datos de los gráficos y, si es necesario, qué hacer para empezar a usar los gráficos.  

## <a name="the-cash-cycle-and-income--expense-charts"></a>Gráficos Ciclo de efectivo e Ingresos y gastos
Los gráficos **Ciclo de efectivo** e **Ingresos y gastos** están preparados para usarse, en función del plan de cuentas y los esquemas de cuentas. Los efectos son de donde proceden los datos y los esquemas de cuentas calculan la relación entre ventas y cobros. Se proporcionan algunas cuentas y esquemas de cuentas. Puede usarlos tal como están, modificarlos y agregar nuevos. Si se agrega cuentas al plan de cuentas, por ejemplo, importándolas de QuickBooks, deberá asignarlas a las cuentas de la página **Esquemas de cuentas** de los siguientes nombres del esquema de cuentas:  

| Nombre esquema cuenta | Dónde se usa |
| --- | --- |
| **I_CACYCLE** |Ciclo de efectivo |
| **I_CASHFLOW** |Tesorería |
| **I_INCEXP** |Ingresos y gastos |
| **I_MINTRIAL** |Como regularización si no utiliza el plan de cuentas |

**Nota** Es recomendable conservar los cálculos que se proporcionan para el esquema de cuentas.  

Introduzca las cuentas en el campo **Sumatorio** de **Total ingresos**, **Total cuentas por cobrar**, **Total cuentas por pagar** y **Total inventario**. Para asignarlo a un intervalo de cuentas, o a varias cuentas específicas, escriba los números de cuenta separados por ".." o por una barra vertical, respectivamente. Por ejemplo, **1111..4444** o **2222|3333|5555**.  

**Sugerencia** Verifique la asignación eligiendo la acción **Panorama**.  

## <a name="set-up-the-cash-flow-chart"></a>Configurar el gráfico Flujo de efectivo
El gráfico Flujo de efectivo se basa en lo siguiente:  

* Un gráfico de cuentas de flujo de efectivo.
* Una o más configuraciones en flujo de efectivo. Especifican las cuentas que se usarán para contabilidad general, compras, venta, servicios y activos fijos.  

Para ayudarle a empezar, se proporcionan algunas cuentas y configuraciones de flujo de efectivo. Puede agregarlas, cambiarlas o quitarlas.  

Para configurarla, busque **cuentas de flujo de efectivo**, elija el vínculo y rellene los campos. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Repita estos pasos para la **configuración de flujo de efectivo**.  

## <a name="set-up-cash-flow-forecasts"></a>Configurar previsiones de flujo de efectivo
El gráfico **Previsión de flujo de efectivo** utiliza cuentas de flujo de efectivo, configuraciones de flujo de efectivo y previsiones de flujo de efectivo. Se proporcionan algunas, pero configurar las suyas propias usando una guía de configuración asistida. Esta guía le ayuda a especificar aspectos como la frecuencia con que se actualizará la previsión, las cuentas en las que se basará, la información acerca de cuándo se pagan impuestos y si activar [Cortana Intelligence.](https://www.microsoft.com/en-us/cloud-platform/what-is-cortana-intelligence-suite).  

Las previsiones de flujo de efectivo pueden usar Cortana Intelligence para incluir documentos cuya fecha de vencimiento sea en el futuro. El resultado es una predicción más completa. La conexión a Cortana Intelligence ya está configurada automáticamente. Solo necesita activarla. Al iniciar sesión en [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)], se muestra una notificación en una barra azul y proporciona un vínculo a la configuración de flujo de caja predeterminada. La notificación solo se muestra una vez. Si la cierra pero decide activar Cortana Intelligence, puede utilizar la guía de configuración asistida o un proceso manual.  

> [!NOTE]  
>   También puede usar su propio servicio web de predicción. Para obtener más información, vea [Crear y usar su propio servicio web predictivo para las previsiones de flujo de efectivo](#AnchorText).  

Para usar la guía de configuración asistida:  

1. En el área de trabajo Contable, en el gráfico **Previsión de flujo de efectivo**, elija la acción **Abrir configuración asistida**.  
2. Rellene los campos en cada paso de la guía.  
3. En la página principal, elija **Previsión de flujo de efectivo** encima del gráfico y, a continuación, en **Recalcular previsión**.  

Para usar un proceso manual:  

1. En el área de trabajo Contable, busque **Configuración de flujo de efectivo** y, a continuación, elija el vínculo relacionado.  
2. Expanda la ficha desplegable **Cortana Intelligence** y, a continuación, elija la casilla **Cortana Intelligence habilitado**.  
3. En la página principal, elija **Previsión de flujo de efectivo** encima del gráfico y, a continuación, en **Recalcular previsión**.  

> [!TIP]  
>   Considere la duración de los periodos que el servicio usará en los cálculos. Cuantos más datos proporcione, más precisas serán las predicciones. Asimismo, controle las variaciones grandes en los periodos. También afectarán a las predicciones. Si Cortana Intelligence no encuentra suficientes datos, o los datos varían mucho, el servicio no creará ninguna predicción.  

## <a name="AnchorText"> </a>Crear y usar su propio servicio web predictivo para las previsiones de flujo de efectivo
También puede crear su propio servicio web predictivo basado en un modelo público denominado **Modelo de previsión para Microsoft Dynamics 365 for Financials**. Este modelo predictivo está disponible en línea en la galería de Cortana Intelligence. Para usar el modelo, siga estos pasos:  

1. Abra un explorador y vaya a la [Galería de Cortana Intelligence](https://go.microsoft.com/fwlink/?linkid=828352).  
2. Busque **Modelo de previsión para Microsoft Dynamics 365 for Financials** y, a continuación, abra el modelo en Azure Machine Learning Studio.  
3. Use su cuenta de Microsoft para iniciar sesión en un espacio de trabajo y, a continuación, copie el modelo.  
4. Ejecute el modelo y como publíquelo como un servicio web.  
5. Anote la URL de API y la clave de API. Usará estas credenciales para una configuración de flujo de caja.  
6. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), especifique **Configuración de flujo de efectivo** y elija el vínculo relacionado.  
7. Expanda la ficha desplegable **Cortana Intelligence** y, a continuación, rellene los campos.  

## <a name="see-also"></a>Consulte también
[Analizar el flujo de efectivo de la empresa](finance-analyze-cash-flow.md)  
[Configurar las finanzas](finance-setup-finance.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

