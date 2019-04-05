---
title: Predecir pago atrasado para documentos de venta | Documentos de Microsoft
description: Utilice nuestro modelo predictivo para predecir si una factura se pagará a tiempo.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customer, payment, invoice, sales, invoice, quote
ms.date: 10/01/2018
ms.author: bholtorf
ms.openlocfilehash: 4e47858bf1f7253f8fb8951fe8ea3cb611138852
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/08/2019
ms.locfileid: "806496"
---
# <a name="the-late-payment-prediction-extension"></a>Extensión de Predicción de pagos atrasados  
La gestión efectiva de los cobres es importante para el estado financiero general de una empresa. La extensión de Predicción de pagos atrasados puede ayudarle a reducir los cobros pendientes y afinar su estrategia de cobros puesto que predice si las facturas de ventas se pagarán a tiempo. Por ejemplo, si se predice que un pago se retrasará, puede decidir ajustar los términos de pago o el método de pago para el cliente.

## <a name="what-are-predictions-based-on"></a>¿En qué se basan las predicciones?  
La extensión de Predicción de pagos atrasados usa un modelo predictivo que desarrollamos en Azure Machine Learning Studio y formamos con datos que son representativos de varias pequeñas y medianas empresas. Aunque ya lo hemos formado y evaluado, nuestro modelo predictivo continuará obteniendo información de sus datos. Cuanto más use el modelo y más datos introduzca, las predicciones serán más precisas. De forma predeterminada, la extensión evalúa el modelo y actualiza las predicciones cada semana. Sin embargo, puede actualizar las predicciones siempre que lo desee seleccionando la acción **Actualizar predicción** en la página **Movs. clientes**.  

> [!Note]
> Usamos algo de su tiempo de cálculo cada semana cuando evaluamos el modelo y actualizamos sus predicciones. Además de actualizar manualmente sus predicciones, existen otras acciones que consumen tiempo de cálculo cuando se forma (acción que podría llevar a cabo si se han añadido datos recientemente) y se evalúa el modelo (que analiza la calidad del modelo).

## <a name="getting-started"></a>Introducción
La extensión es gratuita en [!INCLUDE[d365fin](includes/d365fin_md.md)] y proporcionamos además la subscripción a Azure Machine Learning. La subscripción ofrece 30 minutos de tiempo de cálculo por mes. Si necesita más que eso, puede crear su propio modelo predictivo y usarlo en su lugar. Para obtener más información, vea la sección _Crear su propio modelo predictivo_ que se presenta más adelante en este tema.  

Cuando abra un documento de ventas registrado, se mostrará una notificación a la parte superior de la página. Para utilizar la extensión Predicción de pagos atrasados, elija **Activar** en la notificación. De forma opcional, puede configurar la extensión manualmente. Por ejemplo, si se arrepiente de haber cerrado la notificación.  

Para activar la extensión manualmente, siga estos pasos:

1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Conexiones de servicio** y luego elija el enlace relacionado.  
2. Elija la opción **Configuración de predicción de pago atrasado** y rellene los campos según corresponda.

## <a name="viewing-all-payment-predictions"></a>Ver todas las predicciones de pago
Si habilita la extensión, estará disponible un mosaico de **Pagos previstos como atrasados** el Área de trabajo del **administrador de negocio**. El mosaico muestra la cantidad de pagos que se prevé que se atrasarán y le permite abrir la página **Movs. clientes** en la que puede profundizar en las facturas publicadas. Hay tres columnas a las que se les debe prestar atención:  

* **Pago atrasado**: indica que se prevé que el pago de la factura esté atrasado.
* **Confianza de predicción**: indica la fiabilidad de la predicción. **Alta** indica que la predicción es al menos un 90% segura, **Media** es entre el 80 y el 90% y **Baja** es por debajo del 80%.
* **% de confianza de la predicción**: muestra el porcentaje actual por detrás de la clasificación de la confianza. De forma predeterminada, esta columna no se muestra, pero puede agregarla si lo desea. Para obtener más información, vea [Personalización del área de trabajo](ui-personalization-user.md).

> [!Tip]
> La página Movs. cliente también muestra un cuadro informativo a la derecha. Cuando esté revisando predicciones, le puede resultar útil la información que aparece en la sección **Detalles de cliente**. Cuando elija la factura en la lista, la sección mostrará información acerca del cliente. Esto también le permite tomar medidas inmediatas. Por ejemplo, si un cliente con frecuencia pierde su billetera, puede abrir la ficha del cliente desde el cuadro de datos y bloquear al cliente para futuras ventas.  

## <a name="viewing-a-payment-prediction-for-a-specific-sales-document"></a>Visualización de una predicción de pago para un documento de ventas específico
También puede predecir pagos atrasados por adelantado. En las páginas **Ofertas venta**, **Pedidos venta** y **Facturas venta**, puede usar la acción **Predecir pago** para generar una predicción para el documento de ventas que está viendo.

<!--## Scheduling Payment Predictions
On the **Late Payment Prediction Setup** page you can schedule updates to payment predictions for a time that is convenient for you. -->

## <a name="building-your-own-predictive-model"></a>Crear un modelo predictivo personalizado
¿Le interesa crear un modelo predictivo personalizado? Puede usar Azure Machine Learning Studio para crear su propio modelo predictivo y usarlo en [!INCLUDE[d365fin](includes/d365fin_md.md)]. Para utilizar su propio modelo, debe suscribirse a Azure Machine Learning. Para obtener más información, vea [Documentación de Azure Machine Learning Studio](https://go.microsoft.com/fwlink/?linkid=861765).  

Sin embargo, le ofrecemos una forma más fácil de crear y usar su propio modelo predictivo. Puede compartir los datos de sus facturas con nuestro experimento predictivo en Azure Machine Learning y dejar que cree y forme un modelo predictivo basado en sus datos. Para compartir sus datos, en la página **Configuración de predicción de pago atrasado**, seleccione la acción **Crear mi modelo**. Después, las predicciones se basarán en su modelo y sus datos, no en los nuestros.  

> [!Note]
>   La calidad de modelo es importante. Cuando nuestro experimento predictivo utiliza sus datos para formar un modelo, determina un valor de calidad para el modelo como un porcentaje. La calidad del modelo indica la precisión de las predicciones. Varios factores pueden afectar la calidad de un modelo. Por ejemplo, estos factores pueden ser que no hay suficientes datos o que los datos no contienen suficiente variación. Puede ver la calidad del modelo que utiliza actualmente en la página **Configuración de predicción de pago atrasado**. También puede especificar un umbral mínimo de calidad para el modelo. Los modelos con el valor de calidad inferiores al umbral no generará predicciones.  

### <a name="to-use-your-model-instead-of-ours"></a>Para utilizar su modelo en lugar del nuestro  
Si crea su propio modelo en Azure Machine Learning Studio, sin utilizar las herramientas de [!INCLUDE[d365fin](includes/d365fin_md.md)], debe proporcionar sus credenciales para que [!INCLUDE[d365fin](includes/d365fin_md.md)] pueda acceder a él. Existen un par de pasos para hacerlo:

1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Configuración de predicción de pago atrasado** y luego elija el enlace relacionado.  
2. Seleccione la casilla de verificación **Usar Mi suscripción a Azure**.  
3. En el campo **Modelo seleccionado**, elija **Mi modelo**.  
4. En la ficha desplegable **Credenciales de mi modelo**, introduzca la URL y la clave de API para su modelo.  

## <a name="see-also"></a>Consulte también  
[Documentación de Azure Machine Learning Studio](https://go.microsoft.com/fwlink/?linkid=861765)  
[Personalizar Business Central con extensiones](ui-extensions.md)  
[[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
