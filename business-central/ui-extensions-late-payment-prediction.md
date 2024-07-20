---
title: Predecir pago atrasado para documentos de venta
description: Este artículo explica cómo utilizar nuestro modelo predictivo para predecir si un cliente pagará una factura a tiempo.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'customer, payment, invoice, sales, invoice, quote'
ms.search.form: '1950, 1951,'
ms.date: 07/01/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="the-late-payment-prediction-extension"></a>Extensión de predicción de pagos atrasados

La gestión efectiva de los cobres es importante para el estado financiero general de una empresa. Para reducir las cuentas pendientes de cobro y ayudarle a afinar su estrategia de cobros, la extensión predice si cabe esperar retrasos en los pagos. Por ejemplo, si se predice que un pago se retrasará, puede decidir ajustar los términos de pago o el método de pago para el cliente.

## <a name="get-started"></a>Introducción

Cuando abra un documento de ventas registrado, se muestra una notificación en la parte superior de la página. Para utilizar la extensión Predicción de pagos atrasados, elija **Activar** en la notificación. De forma opcional, puede configurar la extensión manualmente. Por ejemplo, si se arrepiente de haber cerrado la notificación.

Para activar la extensión manualmente, siga estos pasos:

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de predicción de pago atrasado** y luego elija el enlace relacionado.  
2. Rellene los campos según sea necesario.

> [!NOTE]
> Si decide habilitar la extensión manualmente, tenga en cuenta que [!INCLUDE[prod_short](includes/prod_short.md)] no le permitirá hacerlo si la calidad del modelo es baja. La calidad del modelo indica la precisión de las predicciones. Varios factores pueden afectar la calidad de un modelo. Por ejemplo, puede que no hubiera suficientes datos, o que no hubiera suficiente variación en los datos. Puede ver la calidad del modelo que utiliza actualmente en la página **Configuración de predicción de pago atrasado**. También puede especificar un umbral mínimo de calidad para el modelo.

## <a name="view-all-payment-predictions"></a>Ver todas las predicciones de pago

Si habilita la extensión, estará disponible un mosaico de **Pagos previstos como atrasados** en el Área de trabajo del **administrador de negocio**. El mosaico muestra la cantidad de pagos que se prevé que se atrasarán y le permite abrir la página **Movs. clientes** en la que puede profundizar en las facturas publicadas. Hay tres columnas a las que se les debe prestar atención:  

* **Pago atrasado**: indica que se prevé que el pago de la factura esté atrasado.
* **Confianza de predicción**: indica la fiabilidad de la predicción. **Alta** indica que la predicción es al menos un 90% segura, **Media** es entre el 80 % y el 90 % y **Baja** es por debajo del 80 %.
* **% de confianza de la predicción**: muestra el porcentaje actual por detrás de la clasificación de la confianza. De forma predeterminada, esta columna está oculta, pero puede agregarla si lo desea. Para obtener más información, consulte [Personalizar el área de trabajo](ui-personalization-user.md).

> [!TIP]
> La página Movimientos de cliente muestra un Cuadro informativo. Cuando esté revisando predicciones, le puede resultar útil la información que aparece en la sección **Detalles de cliente**. Cuando elija la factura en la lista, la sección mostrará información acerca del cliente. Esto también permite tomar medidas inmediatas. Por ejemplo, si un cliente con frecuencia pierde su billetera, puede abrir la ficha del cliente desde el cuadro de datos y bloquear al cliente para futuras ventas.  

## <a name="design-details"></a>Detalles de diseño

Microsoft implementa y opera servicios web predictivos en todas las regiones donde [!INCLUDE[prod_short](includes/prod_short.md)] está disponible. El acceso a estos servicios web está incluido en su suscripción a [!INCLUDE[prod_short](includes/prod_short.md)]. Para obtener más información, consulte la Guía de licencias de Microsoft Dynamics 365 Business Central. La guía está disponible para descargar en el sitio web de [Business Central](https://dynamics.microsoft.com/business-central/overview/).

Los servicios web funcionan en tres modos:

* Modelo de entreno. El servicio web entrena el modelo en función del conjunto de datos proporcionado.
* Modelo de evaluación. El servicio web verifica si el modelo devuelve datos fiables para el conjunto de datos proporcionado.
* Predicción. El servicio web aplica el modelo al conjunto de datos proporcionado para hacer una predicción.

Estos servicios web no tienen estado, lo que significa que usan datos solo para calcular predicciones bajo demanda. No almacenan datos.

> [!NOTE]  
> Puede usar su propio servicio web de predicción en lugar del nuestro. Para obtener más información, vea [Crear y usar su propia predicción de pago atrasado de servicio web predictivo](#AnchorText).

### <a name="data-required-to-train-and-evaluate-the-model"></a>Datos requeridos para entrenar y evaluar el modelo

Para cada **movimiento de cliente** que tiene un **histórico de facturas de de venta** relacionado:

* Importe en moneda local, impuestos incluidos
* Las condiciones de pago en días se calculan como **Fecha de vencimiento** menos **Fecha de registro**
* Si hay una nota de abono aplicada

Además, el registro tiene datos agregados de otras facturas relacionadas con el mismo cliente.

- Número total e importes de las facturas pagadas
- Número total e importes de las facturas que se han pagado con retraso
- Número total e importes de las facturas pendientes
- Número total e importes de facturas pendientes ya retrasadas
- Promedio de días atrasados
- Ratio: número de facturas pagadas con retraso/pagadas
- Ratio: importe de facturas pagadas con retraso/pagadas
- Ratio: número de facturas pendientes atrasadas/pendientes
- Ratio: importes de facturas pendientes atrasadas/pendientes

> [!NOTE]
> La información sobre el cliente no se incluye en el conjunto de datos.

### <a name="standard-model-and-my-model"></a>Modelo estándar y mi modelo

El modelo predictivo de la extensión de predicción de pagos atrasados se entrena con datos que representan a una serie de pequeñas y medianas empresas. Cuando comience a contabilizar facturas y recibir pagos, [!INCLUDE[prod_short](includes/prod_short.md)] evalúa si el modelo estándar se ajusta a su flujo comercial.

Si sus procesos no se ajustan al modelo estándar, puede usar la ampliación, pero tendrá que obtener más datos. Solo siga usando [!INCLUDE[prod_short](includes/prod_short.md)].

> [!NOTE]
> Usamos algo de su tiempo de cálculo cada semana cuando evaluamos y reentrenamos el modelo.

[!INCLUDE[prod_short](includes/prod_short.md)] ejecuta el entrenamiento y la evaluación automáticamente cuando se dispone de suficientes facturas pagadas y atrasadas. No obstante, puede ejecutarlo manualmente siempre que lo desee.

#### <a name="to-train-and-use-your-model"></a>Para entrenar y usar el modelo

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de predicción de pago atrasado** y luego elija el enlace relacionado.  
2. En el campo **Modelo seleccionado**, elija **Mi modelo**.
3. Elija la acción **Crear mi modelo** para entrenar el modelo con sus datos.  

## <a name="a-nameanchortext-acreate-and-use-your-own-predictive-web-service-for-late-payment-prediction"></a><a name="AnchorText"> </a>Crear y usar su propio servicio web predictivo para la predicción de pagos atrasados

Para [!INCLUDE[prod_short](includes/prod_short.md)] en línea, el modelo lo publica Microsoft y está conectado a la suscripción de Microsoft. Para otras opciones de implementación, debe crear recursos de Machine Learning en su propia suscripción de Azure. Puede encontrar pasos de muestra en el [repositorio de muestra](https://github.com/microsoft/BCTech/tree/master/samples/MachineLearning). El propósito de este tarea es obtener la URI de API y la clave de API.

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de predicción de pago atrasado** y luego elija el enlace relacionado.  
2. Seleccione la casilla de verificación **Usar Mi suscripción a Azure**.
3. En la ficha desplegable **Credenciales de mi modelo**, introduzca la URL y la clave de API para su modelo.  

## <a name="see-also"></a>Consulte también

[Personalizar Business Central con extensiones](ui-extensions.md)  
[[!INCLUDE[prod_long](includes/prod_long.md)]](welcome.md)  
[Usar inteligencia artificial en Microsoft Dynamics 365 Business Central](/training/paths/use-artificial-intelligence/)  
[Descripción general de la API de predicción](/dynamics365/business-central/dev-itpro/developer/ml-prediction-api-overview)

[!INCLUDE[footer-include](includes/footer-banner.md)]
