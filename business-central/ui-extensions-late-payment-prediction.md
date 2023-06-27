---
title: Predecir pago atrasado para documentos de venta
description: Este tema explica cómo utilizar nuestro modelo predictivo para predecir si una factura se pagará a tiempo.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'customer, payment, invoice, sales, invoice, quote'
ms.search.form: '1950, 1951,'
ms.date: 12/20/2021
ms.author: bholtorf
---
# <a name="the-late-payment-prediction-extension" />Extensión de Predicción de pagos atrasados

La gestión efectiva de los cobres es importante para el estado financiero general de una empresa. La extensión de Predicción de pagos atrasados puede ayudarle a reducir los cobros pendientes y afinar su estrategia de cobros puesto que predice si las facturas de ventas se pagarán a tiempo. Por ejemplo, si se predice que un pago se retrasará, puede decidir ajustar los términos de pago o el método de pago para el cliente.

## <a name="getting-started" />Introducción

Cuando abra un documento de ventas registrado, se mostrará una notificación a la parte superior de la página. Para utilizar la extensión Predicción de pagos atrasados, elija **Activar** en la notificación. De forma opcional, puede configurar la extensión manualmente. Por ejemplo, si se arrepiente de haber cerrado la notificación.  

Para activar la extensión manualmente, siga estos pasos:

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de predicción de pago atrasado** y luego elija el enlace relacionado.  
2. Rellene los campos según sea necesario.

> [!NOTE]
> Si decide habilitar la extensión manualmente, tenga en cuenta que [!INCLUDE[prod_short](includes/prod_short.md)] no le permitirá hacerlo si la calidad del modelo es baja. La calidad del modelo indica la precisión de las predicciones. Varios factores pueden afectar la calidad de un modelo. Por ejemplo, podría no haber suficientes datos o que los datos no contuviesen suficiente variación. Puede ver la calidad del modelo que utiliza actualmente en la página **Configuración de predicción de pago atrasado**. También puede especificar un umbral mínimo de calidad para el modelo.   

## <a name="viewing-all-payment-predictions" />Ver todas las predicciones de pago

Si habilita la extensión, estará disponible un mosaico de **Pagos previstos como atrasados** el Área de trabajo del **administrador de negocio**. El mosaico muestra la cantidad de pagos que se prevé que se atrasarán y le permite abrir la página **Movs. clientes** en la que puede profundizar en las facturas publicadas. Hay tres columnas a las que se les debe prestar atención:  

* **Pago atrasado**: indica que se prevé que el pago de la factura esté atrasado.
* **Confianza de predicción**: indica la fiabilidad de la predicción. **Alta** indica que la predicción es al menos un 90% segura, **Media** es entre el 80 y el 90% y **Baja** es por debajo del 80%.
* **% de confianza de la predicción**: muestra el porcentaje actual por detrás de la clasificación de la confianza. De forma predeterminada, esta columna no se muestra, pero puede agregarla si lo desea. Para obtener más información, consulte [Personalizar el área de trabajo](ui-personalization-user.md).

> [!TIP]
> La página Movs. cliente también muestra un cuadro informativo a la derecha. Cuando esté revisando predicciones, le puede resultar útil la información que aparece en la sección **Detalles de cliente**. Cuando elija la factura en la lista, la sección mostrará información acerca del cliente. Esto también permite tomar medidas inmediatas. Por ejemplo, si un cliente con frecuencia pierde su billetera, puede abrir la ficha del cliente desde el cuadro de datos y bloquear al cliente para futuras ventas.  

## <a name="viewing-a-payment-prediction-for-a-specific-sales-document" />Visualización de una predicción de pago para un documento de ventas específico

También puede predecir pagos atrasados por adelantado. En las páginas **Ofertas venta**, **Pedidos venta** y **Facturas venta**, puede usar la acción **Predecir pago** para generar una predicción para el documento de ventas que está viendo.

<!--## Scheduling Payment Predictions
On the **Late Payment Prediction Setup** page you can schedule updates to payment predictions for a time that is convenient for you. -->

## <a name="design-details" />Detalles de diseño

Microsoft implementa y opera varios servicios web predictivos en todas las regiones donde [!INCLUDE[prod_short](includes/prod_short.md)] está disponible. El acceso a estos servicios web está incluido en su suscripción a [!INCLUDE[prod_short](includes/prod_short.md)]. Para obtener más información, consulte la Guía de licencias de Microsoft Dynamics 365 Business Central. La guía está disponible para descargar en el sitio web de [Business Central](https://dynamics.microsoft.com/business-central/overview/).

Los servicios web funcionan en tres modos:

* Modelo de entreno. El servicio web entrena el modelo en función del conjunto de datos proporcionado.
* Modelo de evaluación. El servicio web verifica si el modelo devuelve datos fiables para el conjunto de datos proporcionado.
* Predicción. El servicio web aplica el modelo al conjunto de datos proporcionado para hacer una predicción.

Estos servicios web no tienen estado, lo que significa que usan datos solo para calcular predicciones bajo demanda. No almacenan datos. 

> [!NOTE]  
> Puede usar su propio servicio web de predicción en lugar del nuestro. Para obtener más información, vea [Crear y usar su propia predicción de pago atrasado de servicio web predictivo](#AnchorText).

### <a name="data-required-to-train-and-evaluate-the-model" />Datos requeridos para entrenar y evaluar el modelo

Para cada **movimiento de cliente** que tiene un **histórico de facturas de de venta** relacionado:

* Importe (LCY) con IVA
* Las condiciones de pago en días se calculan como **Fecha de vencimiento** menos **Fecha de registro**.
* Si hay un abono aplicado. 

Además, el registro se enriquece con datos agregados de otras facturas relacionadas con el mismo cliente. Esto incluye lo siguiente:

- Número total y cantidad de facturas pagadas
- Número total y cantidad de facturas pagadas tarde
- Número total y cantidad de facturas pendientes
- Número total y cantidad de facturas pendientes ya retrasadas
- Promedio de días atrasados
- Proporción: número de facturas pagadas con retraso/pagadas
- Proporción: importe de facturas pagadas con retraso/pagadas
- Ratio: Número de facturas pendientes atrasadas/pendientes
- Ratio: importe de facturas pendientes atrasadas/pendientes

> [!NOTE]
> La información sobre el cliente no se incluye en el conjunto de datos.

### <a name="standard-model-and-my-model" />Modelo estándar y mi modelo

La extensión de Predicción de pagos atrasados contiene un modelo predictivo que se entrena utilizando datos que son representativos de varias pequeñas y medianas empresas. Cuando comience a contabilizar facturas y recibir pagos, [!INCLUDE[prod_short](includes/prod_short.md)] evaluará si el modelo estándar se ajusta a su flujo comercial. 

Si parece que sus procesos no coinciden con el modelo estándar, aún puede usar la extensión, pero necesitará obtener más datos. Solo siga usando [!INCLUDE[prod_short](includes/prod_short.md)].
> [!NOTE]
> Usamos algo de su tiempo de cálculo cada semana cuando evaluamos y reentrenamos el modelo. 

[!INCLUDE[prod_short](includes/prod_short.md)] ejecuta el entrenamiento y la evaluación automáticamente cuando hay suficientes facturas pagadas y atrasadas disponibles, sin embargo, puede hacerlo manualmente cuando lo desee.

#### <a name="to-train-and-use-your-model" />Para entrenar y usar el modelo

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de predicción de pago atrasado** y luego elija el enlace relacionado.  
2. En el campo **Modelo seleccionado**, elija **Mi modelo**.
3. Elija la acción **Crear mi modelo** para entrenar el modelo con sus datos.  

## <a name="a-nameanchortext-acreate-and-use-your-own-predictive-web-service-for-late-payment-prediction" /><a name="AnchorText"> </a>Crear y usar su propio servicio web predictivo para la predicción de pagos atrasados

También puede crear su propio servicio web predictivo basado en un modelo público denominado **Experimento de predicción para Dynamics 365 Business Central**. Este modelo predictivo está disponible en línea en la galería de Azure AI. Para usar el modelo, siga estos pasos:  

1. Abra un explorador y vaya a la [Galería de Azure AI](https://go.microsoft.com/fwlink/?linkid=2086310).  
2. Busque **Experimento de predicción para Dynamics 365 Business Central** y, a continuación, abra el modelo en Azure Machine Learning Studio.  
3. Use su cuenta de Microsoft para iniciar sesión en un espacio de trabajo y, a continuación, copie el modelo.  
4. Ejecute el modelo y como publíquelo como un servicio web.  
5. Anote la URL de API y la clave de API. Usará estas credenciales para una configuración de flujo de caja.  
6. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de predicción de pago atrasado** y luego elija el enlace relacionado.  
7. Seleccione la casilla de verificación **Usar Mi suscripción a Azure**.
8. En la ficha desplegable **Credenciales de mi modelo**, introduzca la URL y la clave de API para su modelo.  .  

## <a name="see-related-microsoft-training" />Consultar la [formación de Microsoft](/training/modules/predict-late-payments-sales-documents/) relacionada

## <a name="see-also" />Consulte también .

[Documentación de Azure Machine Learning Studio](/azure/machine-learning/classic/)  
[Personalizar Business Central con extensiones](ui-extensions.md)  
[[!INCLUDE[prod_long](includes/prod_long.md)]](welcome.md)  
[Usar inteligencia artificial en Microsoft Dynamics 365 Business Central](/training/paths/use-artificial-intelligence/)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
