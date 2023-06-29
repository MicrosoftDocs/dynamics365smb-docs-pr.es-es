---
title: Configurar impuestos para la conexión Shopify
description: Cómo configurar impuestos en Shopify y Business Central.
ms.date: 08/19/2022
ms.topic: article
ms.service: dynamics365-business-central
author: AndreiPanko
ms.author: andreipa
---

# <a name="set-up-taxes-for-the-shopify-connection"></a><a name="set-up-taxes-for-the-shopify-connection"></a><a name="set-up-taxes-for-the-shopify-connection"></a>Configurar impuestos para la conexión Shopify

En este artículo, investigaremos cómo las diversas configuraciones de Shopify afectan a los precios de escaparate y los impuestos que se muestran a los clientes. También trataremos cómo configurar [!INCLUDE[prod_short](../includes/prod_short.md)] para apoyar la configuración en Shopify. Este artículo no pretende ser una guía fiscal completa. Para obtener más información, contacte con la autoridad fiscal local o con un profesional de impuestos.  

El producto asume que usted está obligado a pagar impuestos cuando vende productos a nivel local o internacional.

## <a name="if-you-sell-domestically"></a><a name="if-you-sell-domestically"></a><a name="if-you-sell-domestically"></a>Si vende a nivel nacional

Después de configurar su Shopify para recaudar impuestos en su país o región nacional, puede decidir cómo desea mostrar los precios en su escaparate.

Puede especificar si desea incluir impuestos en los precios activando o desactivando la opción **Todos los precios incluyen impuestos** en las configuraciones de [**Impuestos y aranceles**](https://www.shopify.com/admin/settings/taxes) del **Administrador de Shopify**.

La alternancia suele estar habilitada para los siguientes países:

* Australia
* Austria
* Bélgica
* República Checa
* Dinamarca
* Finlandia
* Francia
* Alemania
* Islandia
* Italia
* Países Bajos
* Nueva Zelanda
* Noruega
* España
* Suecia
* Suiza
* Reino Unido. 

En mercados como estos, un precio de 100 EUR definido en la ficha del producto ya contiene el impuesto al valor añadido (IVA). El precio, incluido el IVA, se muestra al cliente en el escaparate y al finalizar la compra.  

En EE. UU. y Canadá, los clientes no esperan que los precios incluyan impuestos. El impuesto se agrega al finalizar la compra, por lo que el conmutador **Todos los precios incluyen impuestos** generalmente está desactivado. En este caso, un precio de 100 $ definido en la tarjeta del producto es el precio sin impuestos. Al finalizar la compra, los impuestos se agregan al precio.

Para respaldar el escenario donde se selecciona **Todos los precios incluyen impuestos**, en [!INCLUDE[prod_short](../includes/prod_short.md)], complete los siguientes campos en la página de la **Tarjeta de tienda de Shopify**:  

1. Active el interruptor **Precio IVA incluido**.  
2. En el campo **Grupo contable comercial de IVA**, especifique el grupo contable que utiliza para los clientes nacionales.  

Ahora defina los precios de los productos en el campo **Tarjeta de producto** o **Lista de precios de venta**, con o sin impuestos. Al exportar precios a Shopify, [!INCLUDE [prod_short](../includes/prod_short.md)] incluye los impuestos nacionales en el precio calculado y muestra ese precio para el producto en Shopify.

[!Note]
> Estos ajustes afectan a la exportación de precios. Cuando importa pedidos desde Shopify, la configuración del campo **Precios IVA incluido** proviene de la **Plantilla de cliente** en la tarjeta de la tienda de Shopify, o la plantilla de cliente por país. Incluso si utiliza el cliente predeterminado para pedidos importados, debe completar el **Código de plantilla de cliente**.

## <a name="if-you-sell-internationally"></a><a name="if-you-sell-internationally"></a><a name="if-you-sell-internationally"></a>Si vende a nivel internacional

Esta sección explora la configuración para escenarios en los que debe recaudar impuestos cuando vende a otro país o región, como otros países de la UE.

Actualmente, el conector Shopify solo admite la exportación de un solo precio. Shopify aplica automáticamente los impuestos locales, las monedas y el redondeo. La opción **Todos los precios incluyen impuestos** da como resultado las acciones descritas en las siguientes subsecciones.

### <a name="all-prices-include-tax-is-selected"></a><a name="all-prices-include-tax-is-selected"></a><a name="all-prices-include-tax-is-selected"></a>Todos los precios incluyen impuestos es seleccionado

|-|Ventas domesticas|País extranjero donde estás recaudando impuestos|País extranjero donde no está recaudando impuestos|
|------------------------|--------|--------|--------|
|Precio mostrado en el escaparate|1200|1200|1200|
|Porcentaje de tasa fiscal|nº 20|25|0|
|Precio en la caja|1200|1200|1200|

El precio para el cliente permanece intacto, independientemente de su ubicación, pero su margen se ve afectado debido a las diferentes tipos impositivos que difieren según la región.

### <a name="all-prices-include-tax-is-not-selected"></a><a name="all-prices-include-tax-is-not-selected"></a><a name="all-prices-include-tax-is-not-selected"></a>Todos los precios incluyen impuestos no es seleccionado

|-|Ventas domesticas|País extranjero donde estás recaudando impuestos|País extranjero donde no está recaudando impuestos|
|------------------------|--------|--------|--------|
|Precio mostrado en el escaparate|1000|1000|1000|
|Porcentaje de tasa fiscal|nº 20|25|0|
|Precio en la caja|1200|1250|1000|

Shopify agrega impuestos locales al precio definido en la tarjeta del producto según el lugar al que se envíen los productos.

## <a name="dynamic-tax-inclusive-pricing"></a><a name="dynamic-tax-inclusive-pricing"></a><a name="dynamic-tax-inclusive-pricing"></a>Precios dinámicos con impuestos incluidos

Los países tienen diferentes requisitos para incluir impuestos en los precios. Si desea que los precios incluyan impuestos automáticamente, puede activar [Precio dinámico con impuestos incluidos](https://help.shopify.com/en/manual/markets/pricing/dynamic-tax-inclusive-pricing) en Shopify.

En su **Administrador de Shopify**, seleccione **Incluir o excluir impuestos según el país de su cliente** en la sección **Otros Mercados - Preferencias** de la configuración de [**Mercados**](https://www.shopify.com/admin/settings/markets).  

> [!NOTE]
> Esta configuración no afecta a los precios en los mercados nacionales, lo que controla la opción **Todos los precios incluyen impuestos**.

### <a name="all-prices-include-tax-is-selected-1"></a><a name="all-prices-include-tax-is-selected-1"></a><a name="all-prices-include-tax-is-selected-1"></a>Todos los precios incluyen impuestos es seleccionado

|-|Ventas domesticas|País extranjero donde el impuesto está incluido en el precio|País extranjero donde el impuesto está excluido|
|------------------------|--------|--------|--------|
|Precio mostrado en el escaparate|1200|1250|1000|
|Porcentaje de tasa fiscal|20|25|10|
|Precio en la caja|1200|1250|1100|

El precio para cada cliente cambia dependiendo de su ubicación.

### <a name="all-prices-include-tax-is-not-selected-1"></a><a name="all-prices-include-tax-is-not-selected-1"></a><a name="all-prices-include-tax-is-not-selected-1"></a>Todos los precios incluyen impuestos no es seleccionado

|-|Ventas domesticas|País extranjero donde el impuesto está incluido en el precio|País extranjero, donde el impuesto está excluido|
|------------------------|--------|--------|--------|
|Precio mostrado en el escaparate|1000|1250|1000|
|Porcentaje de tasa fiscal|20|25|10|
|Precio en la caja|1200|1250|1100|

> [!NOTE]
> La opción **Todos los precios incluyen impuestos** no cambia la forma en que se muestran los precios a los clientes internacionales.

## <a name="if-you-sell-to-eu-customers"></a><a name="if-you-sell-to-eu-customers"></a><a name="if-you-sell-to-eu-customers"></a>Si vende a clientes de la UE

Los diferentes países de la UE tienen diferentes tasas de impuestos locales. Sin embargo, si se encuentra en la UE y vende a otros países de la UE, puede utilizar su tasa impositiva local en algunos casos.  

En su **Administrador de Shopify**, marque la casilla **Recaudar IVA** en la sección **Unión Europea** de la configuración de [**Impuestos y aranceles**](https://www.shopify.com/admin/settings/taxes).

|Recaudar IVA|Tasa de IVA|
|-|-|
|Exención de microempresas|Use su tasa impositiva nacional para todas las ventas dentro de la UE|
|Ventanilla única o registro específico del país|Utilice la tasa de IVA del país o región de su cliente|

### <a name="collect-vat-set-to-one-stop-shop-registration"></a><a name="collect-vat-set-to-one-stop-shop-registration"></a><a name="collect-vat-set-to-one-stop-shop-registration"></a>Recaudar IVA configurado para el registro de ventanilla única

En el siguiente ejemplo, la opción **Todos los precios incluyen impuestos** está activada. El precio en la ficha del producto se establece en *1200*.

|-|Ventas domesticas|País extranjero|
|------------------------|--------|--------|
|Precio mostrado en el escaparate|1200|1250|
|Porcentaje de tasa fiscal|20|25|
|Precio en la caja|1200|1250|

### <a name="collect-vat-set-to-micro-business-exemption"></a><a name="collect-vat-set-to-micro-business-exemption"></a><a name="collect-vat-set-to-micro-business-exemption"></a>Recaudar IVA fijado en exención de microempresas

En el siguiente ejemplo, la opción **Todos los precios incluyen impuestos** está activada. El precio en la ficha del producto se establece en *1200*.

|-|Ventas domesticas|País extranjero con tasa impositiva local del 25 por ciento.|
|------------------------|--------|--------|
|Precio mostrado en el escaparate|1200|1200|
|Porcentaje de tasa fiscal|nº 20|nº 20|
|Precio en la caja|1200|1200|

Shopify usa la tasa impositiva nacional e ignora la tasa impositiva del país extranjero al calcular los precios finales.

## <a name="importing-shopify-orders-sold-to-international-customers"></a><a name="importing-shopify-orders-sold-to-international-customers"></a><a name="importing-shopify-orders-sold-to-international-customers"></a>Importando pedidos de Shopify vendidos a clientes internacionales

Si está recaudando impuestos de varios países, debe definir una configuración específica de país en [!INCLUDE[prod_short](../includes/prod_short.md)]. Hay una razón por la que se requiere esta configuración. Cuando se crea un documento de ventas en [!INCLUDE[prod_short](../includes/prod_short.md)], [!INCLUDE [prod_short](../includes/prod_short.md)] calcula los impuestos en lugar de reutilizar los impuestos importados desde Shopify.

Puede especificar los ajustes específicos de país/región en la página **Plantilla de cliente de Shopify**. Puede definir el **N.º de cliente genérico** o **N.º de plantilla de cliente**. En cualquier caso, asegúrese de que el cliente o la plantilla tengan rellenados los siguientes campos:

1. **Grupo contable de negocio general** (usado para clientes extranjeros).
2. **Grupo contable de negocio IVA** (usado para clientes extranjeros).
3. **Precios con IVA incluido** (alineado con la configuración en el lado de Shopify):

* Elija **Sí** si **Todos los precios incluyen impuestos** está habilitado e **Incluya o excluya impuestos según el país de su cliente** está desactivado.
* Elija **No** si **Todos los precios incluyen impuestos** está desactivado e **Incluya o excluya impuestos según el país de su cliente** está desactivado.
* Elija **Sí** si **Incluya o excluya impuestos según el país de su cliente** está activado y el país o región aparece en la lista [Países y regiones con impuestos incluidos](https://help.shopify.com/en/manual/markets/pricing/dynamic-tax-inclusive-pricing#tax-inclusive-versus-tax-exclusive-countries-and-regions).
* Elija **No** si **Incluir o excluir impuestos según el país de su cliente** está activado y el país o región no aparece en la lista [Países con impuestos incluidos](https://help.shopify.com/en/manual/markets/pricing/dynamic-tax-inclusive-pricing#tax-inclusive-versus-tax-exclusive-countries-and-regions).

> [!NOTE]
> La configuración del campo **Precios con IVA incluido** proviene de la plantilla, no del cliente específico. Es importante definir la plantilla de cliente.

## <a name="other-tax-remarks"></a><a name="other-tax-remarks"></a><a name="other-tax-remarks"></a>Otras observaciones sobre impuestos

Mientras que el pedido de Shopify importado contiene información sobre impuestos, los impuestos se vuelven a calcular cuando se crea el documento de ventas. Ese nuevo cálculo significa que es importante que la configuración de IVA/impuestos sea correcta en [!INCLUDE[prod_short](../includes/prod_short.md)].

* Múltiples tasas de impuestos o IVA sobre productos. Por ejemplo, algunas categorías de productos están sujetas a tipos impositivos reducidos. Puede usar la característica [anulación de impuestos](https://help.shopify.com/en/manual/taxes/tax-overrides#create-a-manual-collection-for-products-that-need-a-tax-override) en Shopify. Al importar y crear productos en [!INCLUDE[prod_short](../includes/prod_short.md)], usan la configuración de impuestos especificada en el código de plantilla de producto en la tienda Shopify. Antes de importar pedidos con dichos productos, actualice el grupo contable de productos con IVA.  
* Tasas de impuestos dependientes de la dirección. Utilice el campo **Prioridad de área fiscal** junto con la tabla **Plantillas de clientes** para sobrescribir la lógica estándar que rellena el **Código de área fiscal** en el documento de venta. El campo **Prioridad de área fiscal** especifica la prioridad de la que la función debe tomar la información sobre el país o región y el estado o provincia. Luego, se identifica el registro correspondiente en las plantillas de cliente de Shopify y se usan el **Código de área fiscal**, **Sujeto a impuestos** y **Grupo de registro de negocio con IVA** al crear un documento de ventas.  

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Consulte también

[Comenzar con el conector para Shopify](get-started.md)  
