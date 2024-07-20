---
title: Usar la extensión de previsión de ventas e inventario para administrar el inventario
description: 'Esta extensión le ayuda a predecir ventas, obtener un resumen claro de la falta de stock prevista e incluso le ayuda a crear solicitudes de reposición para proveedores.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'app, add-in, manifest, customize, budget'
ms.search.form: '1850, 1851, 1853,'
ms.date: 07/01/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="the-sales-and-inventory-forecast-extension"></a>Extensión de previsión de ventas e inventario

La gestión del inventario es un equilibrio entre el servicio al cliente y gestionar el coste. Por un lado, un inventario bajo requiere menos capital de trabajo, pero, por otro lado, la falta de stock puede llevar potencialmente la pérdida de ventas. La extensión de la previsión de inventario y ventas predice ventas potenciales con datos históricos y ofrece una visión general clara de la falta de stock prevista. Según la previsión, la extensión ayuda a crear solicitudes de reposición a los proveedores y le ahorra tiempo.  

## <a name="setting-up-forecasting"></a>Configurar la previsión

En [!INCLUDE[prod_short](includes/prod_short.md)], la conexión a [Azure AI](https://azure.microsoft.com/overview/ai-platform/) ya está configurada automáticamente. Pero puede configurar la previsión para que utilice diferentes tipos de periodo de información como, por ejemplo, cambiar la previsión mensual por la trimestral. También puede elegir el número de periodos para calcular la previsión según como desea que sea. Sugerimos que utilice la previsión mensual y con un horizonte de 12 meses.

> [!TIP]  
> Considere la duración de los periodos que el servicio usará en los cálculos. Cuantos más datos proporcione, más precisas serán las predicciones. Asimismo, controle las variaciones grandes en los periodos. También afectarán a las predicciones. Si Azure AI no encuentra suficientes datos, o los datos varían mucho, el servicio no creará ninguna predicción.

## <a name="use-the-forecasts"></a>Usar las previsiones

La extensión usa Azure AI para pronosticar las ventas futuras en función del historial de ventas para ayudarle a evitar la escasez de inventario. Por ejemplo, cuando elige un producto en la página **Productos**, la ficha del panel **Previsión del producto** muestra las ventas futuras estimadas de ese producto. De esta manera podrá ver si pronto agotará el stock del producto.  

También puede utilizar la extensión para sugerir cuándo desea almacenar el inventario. Por ejemplo, podría crear un pedido de compra para que Fabrikam compre su nueva silla de escritorio. La extensión Pronóstico de ventas e inventario podría sugerirle que también reabastezca la silla giratoria LONDON que normalmente compra a este proveedor. La ampliación puede pronosticar que pronto se agotarán las existencias de la silla giratoria LONDON, por lo que podría pedir ya más sillas.  

## <a name="design-details"></a>Detalles de diseño

Las suscripciones para [!INCLUDE[prod_short](includes/prod_short.md)] vienen con acceso a varios servicios web predictivos en todas las regiones donde [!INCLUDE[prod_short](includes/prod_short.md)] está disponible. Para obtener más información, consulte la Guía de licencias de Microsoft Dynamics 365 Business Central. La guía está disponible para descargar en el sitio web de [Business Central](https://dynamics.microsoft.com/en-us/business-central/overview/). 

Estos servicios web no tienen estado, lo que significa que usan datos solo para calcular predicciones bajo demanda. No almacenan datos.

> [!NOTE]  
>   También puede usar su propio servicio web de predicción en lugar del nuestro. Para obtener más información, vea [Crear y usar su propio servicio web predictivo para ventas y previsiones de inventario](#AnchorText). 

### <a name="data-required-for-forecast"></a>Datos requeridos para la previsión

Para hacer predicciones sobre ventas futuras, el servicio web requiere datos cuantitativos sobre ventas pasadas. Esa información proviene de los campos **Fecha de contabilización**, **Nº producto** y **Cantidad** de la página **Movs. productos**, donde:

- El tipo de movimiento es "Venta".
- La fecha de registro es entre la fecha que se calcula en función de los valores en los campos **Periodos históricos** y **Tipo de periodo** en la página **Configuración de previsión de ventas e inventario** y la fecha de trabajo.

Antes de usar el servicio web, [!INCLUDE[prod_short](includes/prod_short.md)] comprime las transacciones por **Nº producto** y **Fecha de registro** según el valor del campo **Tipo de periodo** en la página **Configuración de previsión de ventas e inventario**.

## <a name="a-nameanchortext-acreate-and-use-your-own-predictive-web-service-for-sales-and-inventory-forecasts"></a><a name="AnchorText"> </a>Crear y usar su propio servicio web predictivo para ventas y previsiones de inventario

Para [!INCLUDE[prod_short](includes/prod_short.md)] en línea, el modelo lo publica Microsoft y está conectado a la suscripción de Microsoft. Para otras opciones de implementación, debe crear recursos de Machine Learning en su propia suscripción de Azure. Puede encontrar pasos de muestra en el [repositorio de muestra](https://github.com/microsoft/BCTech/tree/master/samples/MachineLearning). El propósito de este tarea es obtener la URI de API y la clave de API.

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), , escriba **Configuración de previsión de ventas e inventario** y, a continuación, elija el vínculo relacionado.  
2. Expanda la ficha desplegable **General** y rellene los campos de URL de API y clave de API.  

## <a name="see-also"></a>Consulte también .

[Ventas](sales-manage-sales.md)  
[Grupos contables inventario](inventory-manage-inventory.md)  
[Personalizar [!INCLUDE[prod_short](includes/prod_short.md)] con extensiones](ui-extensions.md)  
[Usar inteligencia artificial en Microsoft Dynamics 365 Business Central](/training/paths/use-artificial-intelligence/)  
[Información general de la API de previsión](/dynamics365/business-central/dev-itpro/developer/ml-forecasting-api-overview)

[!INCLUDE[footer-include](includes/footer-banner.md)]
