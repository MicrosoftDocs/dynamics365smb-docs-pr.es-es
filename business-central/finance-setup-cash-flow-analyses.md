---
title: Configuración del análisis de flujo de efectivo (contiene vídeo)
description: 'Utilice los gráficos del área de trabajo Contable para analizar el flujo de dinero de su empresa, incluidos gastos e ingresos, liquidez y recibos de efectivo menos los pagos en efectivo.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'money flow, expense and income, liquidity, cash receipts minus cash payments, Cartera, funds'
ms.search.form: '846, 847, 849, 851, 855, 862, 869, 1818'
ms.date: 08/23/2022
ms.author: bholtorf
---
# <a name="setting-up-cash-flow-analysis" />Configuración del análisis de flujo de efectivo

Si desea ayuda para decidir qué debe hacer con el efectivo, eche un vistazo a los gráficos del Área de trabajo Contable:

* **Ciclo de efectivo**  
* **Ingresos y gastos**  
* **Flujo de efectivo**  
* **Previsiones de flujo de efectivo**  

En este artículo se describe de dónde proceden los datos de los gráficos y, si es necesario, qué hacer para empezar a usar los gráficos.
<br><br>  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4mJhc?rel=0]

## <a name="the-cash-cycle-and-income--expense-charts" />Gráficos Ciclo de efectivo e Ingresos y gastos

Los gráficos **Ciclo de efectivo** e **Ingresos y gastos** están preparados para usarse, en función del plan de cuentas y los informes financieros. Las cuentas son de donde proceden los datos y los informes financieros calculan la relación entre ventas y cobros. Se proporcionan algunas cuentas e informes financieros. Puede usarlos tal como están, modificarlos y agregar nuevos. Si se agrega cuentas al plan de cuentas, por ejemplo, importándolas de QuickBooks, deberá asignarlas a las cuentas de la página **Informes financieros** de los siguientes informes:

| Nombre de informe financiero | Dónde se usa |
| --- | --- |
| **I_CACYCLE** |Ciclo de efectivo |
| **I_CASHFLOW** |Tesorería |
| **I_INCEXP** |Ingresos y gastos |
| **I_MINTRIAL** |Como regularización si no utiliza el plan de cuentas |

> [!NOTE]
> Es recomendable conservar los cálculos que se proporcionan para el informe financiero.

Introduzca las cuentas en el campo **Sumatorio** de **Total ingresos**, **Total cuentas por cobrar**, **Total cuentas por pagar** y **Total inventario**. Para realizar asignaciones a un rango de cuentas, introduzca los números de cuenta separados por "..", como en **1111..4444**. O bien, para realizar asignaciones a cuentas en concreto, introduzca los números de cuenta separados por una barra vertical, como en **2222|3333|5555**.  

> [!TIP] 
> Verifique la asignación eligiendo la acción **Información general**.  

## <a name="set-up-the-cash-flow-chart" />Configurar el gráfico Flujo de efectivo

El gráfico Flujo de efectivo se basa en:  

* Un gráfico de cuentas de flujo de efectivo.
* Una o más configuraciones en flujo de efectivo. Estas configuraciones especifican las cuentas que se usarán para contabilidad general, compras, venta, servicios y activos fijos.  

Para ayudarle a empezar, se proporcionan algunas cuentas y configuraciones de flujo de efectivo. Puede agregarlas, cambiarlas o quitarlas.  

Para configurar las cuentas, busque **Plan de cuentas de flujo de efectivo**, elija el vínculo y rellene los campos. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Repita estos pasos para la **configuración de flujo de efectivo**.

## <a name="set-up-cash-flow-forecasts" />Configurar previsiones de flujo de efectivo

El gráfico **Previsión de flujo de efectivo** utiliza cuentas de flujo de efectivo, configuraciones de flujo de efectivo y previsiones de flujo de efectivo. Se proporcionan algunas, pero configurar las suyas propias usando una guía de configuración asistida. Esta guía le ayuda a especificar aspectos como la frecuencia con que se actualizará la previsión, las cuentas en las que se basará, la información acerca de cuándo se pagan impuestos y si activar [Azure AI](https://azure.microsoft.com/overview/ai-platform/).  

Las previsiones de flujo de efectivo pueden usar Azure AI para crear una previsión más completa. La conexión a Azure AI ya está configurada automáticamente. Solo necesita activarla. Al iniciar sesión en [!INCLUDE[prod_short](includes/prod_short.md)], se muestra una notificación en una barra azul y proporciona un vínculo a la configuración de flujo de caja predeterminada. La notificación solo se muestra una vez. Si la cierra pero luego decide activar Azure AI, puede utilizar la guía de configuración asistida o un proceso manual.  

> [!NOTE]
>
> También puede usar su propio servicio web de predicción. Para obtener más información, vea [Crear y usar su propio servicio web predictivo para las previsiones de flujo de efectivo](#AnchorText).  

Para usar la guía de configuración asistida:  

1. En el área de trabajo Contable, en el gráfico **Previsión de flujo de efectivo**, elija la acción **Abrir configuración asistida**.
2. Rellene los campos en cada paso de la guía. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. En el área de trabajo Contable, elija la acción **Recalcular previsión** en el gráfico **Previsión de flujo de efectivo**.

Para usar un proceso manual:  

1. En el área de trabajo Contable, elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración flujos efectivo** y luego elija el enlace relacionado.
2. Expanda la ficha desplegable **Azure AI** y elija el campo **Azure AI habilitado**.
3. En el área de trabajo Contable, elija la acción **Recalcular previsión** en el gráfico **Previsión de flujo de efectivo**.

> [!TIP]  
> Considere la duración de los periodos que el servicio usará en los cálculos. Cuantos más datos proporcione, más precisas serán las predicciones. Asimismo, controle las variaciones grandes en los periodos. También afectarán a las predicciones. Si Azure AI no encuentra suficientes datos, o los datos varían mucho, el servicio no creará ninguna predicción.  

## <a name="design-details" />Detalles de diseño

Las suscripciones para [!INCLUDE[prod_short](includes/prod_short.md)] vienen con acceso a varios servicios web predictivos en todas las regiones donde [!INCLUDE[prod_short](includes/prod_short.md)] está disponible. Obtenga más información en la guía sobre licencias de Microsoft Dynamics 365 Business Central. La guía está disponible para descargar en el sitio web de [Business Central](https://dynamics.microsoft.com/business-central/overview/).

Estos servicios web no tienen estado, lo que significa que usan datos solo para calcular predicciones bajo demanda. No almacenan datos.

> [!NOTE]
>
> Puede usar su propio servicio web de predicción en lugar del nuestro. Para obtener más información, vea [Crear y usar su propio servicio web predictivo para las previsiones de flujo de efectivo](#AnchorText).

### <a name="data-required-for-forecast" />Datos requeridos para la previsión

Para hacer predicciones sobre futuros ingresos y gastos, los servicios web requieren datos históricos de cuentas por cobrar, cuentas por pagar e impuestos.

#### <a name="receivables" />Cobros

Campos **Fecha de vencimiento**, **Monto (LCY)** de la página **Entradas de libro mayor de clientes**, donde:

* El tipo de documento es *Factura* o *Abono*.
* La fecha de vencimiento es entre la fecha que se calcula en función de los valores en los campos **Periodos históricos** y **Tipo de periodo** en la página **Configuración de flujo de efectivo** y la fecha de trabajo.

Antes de usar el servicio web predictivo, [!INCLUDE[prod_short](includes/prod_short.md)] comprime las transacciones por **Fecha de vencimiento** según el valor del campo **Tipo de periodo** de la página **Configuración de flujo de efectivo**.

#### <a name="payables" />Pagos

Campos **Fecha de vencimiento**, **Monto (LCY)** de la página **Movs. proveedores**, donde:

* El tipo de documento es *Factura* o *Abono*.
* La fecha de vencimiento es entre la fecha que se calcula en función de los valores en los campos **Periodos históricos** y **Tipo de periodo** en la página **Configuración de flujo de efectivo** y la fecha de trabajo.

Antes de usar el servicio web predictivo, [!INCLUDE[prod_short](includes/prod_short.md)] comprime las transacciones por **Fecha de vencimiento** según el valor del campo **Tipo de periodo** de la página **Configuración de flujo de efectivo**.

#### <a name="tax" />Tributos

Campos **Fecha de documento**, **Monto** de la página **Movs. IVA**, donde:

* El tipo de documento es *ventas*.
* La fecha de documento es entre la fecha que se calcula en función de los valores en los campos **Periodos históricos** y **Tipo de periodo** en la página **Configuración de flujo de efectivo** y la fecha de trabajo.

Antes de usar el servicio web predictivo, [!INCLUDE[prod_short](includes/prod_short.md)] comprime las transacciones por **Fecha de documento** según el valor del campo **Tipo de periodo** de la página **Configuración de flujo de efectivo**.

## <a name="a-nameanchortextacreate-and-use-your-own-predictive-web-service-for-cash-flow-forecasts" /><a name="AnchorText"></a>Crear y usar su propio servicio web predictivo para las previsiones de flujo de efectivo

También puede crear su propio servicio web predictivo basado en un modelo público denominado **Modelo de previsión para Microsoft Business Central**. Este modelo predictivo está disponible en línea en la galería de Azure AI. Para usar el modelo, siga estos pasos:  

1. Abra un explorador y vaya a la [Galería de Azure AI](https://go.microsoft.com/fwlink/?linkid=828352).  
2. Busque **Modelo de previsión para Microsoft Business Central** y, a continuación, abra el modelo en el estudio de Microsoft Azure Machine Learning.  
3. Use su cuenta de Microsoft para iniciar sesión en un espacio de trabajo y, a continuación, copie el modelo.  
4. Ejecute el modelo y como publíquelo como un servicio web.  
5. Anote la URL de API y la clave de API. Usará estas credenciales para una configuración de flujo de caja.  
6. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración flujos efectivo** y luego elija el enlace relacionado.  
7. Amplíe la ficha desplegable **Azure AI** y, a continuación, rellene los campos, incluidas la URL de API y la clave de API proporcionadas desde el estudio de Azure Machine Learning. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
8. En el área de trabajo Contable, elija la acción **Recalcular previsión** en el gráfico **Previsión de flujo de efectivo**.

## <a name="see-related-microsoft-trainingtrainingmodulesforecast-cash-flow-dynamics--business-centralindex" />Consultar la [formación de Microsoft](/training/modules/forecast-cash-flow-dynamics-365-business-central/index) relacionada

## <a name="see-also" />Consulte también .

[Analizar el flujo de efectivo de la empresa](finance-analyze-cash-flow.md)  
[Configurar las finanzas](finance-setup-finance.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
