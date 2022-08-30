---
title: Configurar impuestos para la conexión Shopify
description: Cómo configurar impuestos en Shopify y Business Central.
ms.date: 05/27/2022
ms.topic: article
ms.service: dynamics365-business-central
author: AndreiPanko
ms.author: andreipa
ms.openlocfilehash: 0070d583752002cc34ebff74dee2906c289b7136
ms.sourcegitcommit: b353f06e0c91aa6e725d59600f90329774847ece
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2022
ms.locfileid: "9317495"
---
# <a name="set-up-taxes-for-the-shopify-connection"></a>Configurar impuestos para la conexión Shopify

En este artículo, investigaremos cómo varias configuraciones en Shopify afectan a los precios de escaparate y los impuestos que se muestran al cliente. También veremos cómo configurar [!INCLUDE[prod_short](../includes/prod_short.md)] para apoyar la configuración en Shopify. Este artículo no pretende ser una guía fiscal completa. Para obtener más información, contacte con la autoridad fiscal local o con un profesional de impuestos.  

El artículo asume que usted está obligado a pagar impuestos cuando vende productos a nivel local o internacional.

## <a name="if-you-sell-domestically"></a>Si vende a nivel nacional 

Una vez que configure su Shopify para recaudar impuestos en su país o región nacional, puede decidir cómo desea mostrar los precios en su escaparate. Usted controla esto habilitando o deshabilitando la opción **Todos los precios incluyen impuestos** en la configuración de [**Impuestos y deberes**](https://www.shopify.com/admin/settings/taxes) en su **Administración de Shopify**.

Es común tener esta opción habilitada para países como Australia, Austria, Bélgica, República Checa, Dinamarca, Finlandia, Francia, Alemania, Islandia, Italia, Países Bajos, Nueva Zelanda, Noruega, España, Suecia, Suiza y el Reino Unido. En mercados como estos, el precio *100 euros* definido en la ficha del producto ya contiene el impuesto sobre el valor añadido (IVA) y ese mismo precio se muestra al cliente en el escaparate y en la caja.  

En EE. UU. y Canadá, los clientes esperan ver los precios de los productos sin impuestos, que se agregan al finalizar la compra. Así que el campo **Todos los precios incluyen impuestos** normalmente no está seleccionado. En este caso, el precio *100 $* definido en la ficha del producto representa el precio sin impuestos. En la etapa de pago, los impuestos se agregarán al precio para contar el total del pago.

Para apoyar el escenario donde **Todos los precios incluyen impuestos** se selecciona en el lado [!INCLUDE[prod_short](../includes/prod_short.md)], complete el campo **Código de plantilla de cliente** campo en la página **Tarjeta de tienda de Shopify** para acceder a la plantilla con los siguientes campos definidos:  
<!--I changed that last part of the sentence above because it didn't track logically. Just wanted to let you know in case I introduced an inaccuracy.-->

1. **Grupo contable de negocio general**, usado para clientes nacionales.  
2. **Grupo contable de negocio IVA**, usado para clientes nacionales.  
3. **Precios con IVA incluido** ajustado a *sí*.  

Ahora defina los precios de los artículos en el campo **Tarjeta de artículo** o **Lista de precios de venta**, con o sin impuestos. Al exportar precios a Shopify, el sistema calcula el precio para incluir los impuestos nacionales y luego muestra ese precio en la ficha del producto en Shopify.

> [!NOTE]
> Si configuró el conector Shopify para crear clientes automáticamente, es posible que necesite más campos en su plantilla, como **Grupo de contabilización de clientes**. Si usa el cliente predeterminado para los pedidos importados, asegúrese de que el cliente tenga los mismos campos completados. Seguirá necesitando rellenar el **Código de plantilla de cliente** como se especifica más arriba, porque el campo **Precios con impuestos incluidos**/**Precios IVA incluido** del documento de ventas creado no depende del cliente, sino de la **Plantilla de cliente** de la tarjeta de tienda de Shopify o la plantilla de cliente por país o región.

## <a name="if-you-sell-internationally"></a>Si vende a nivel internacional

En esta sección, exploraremos la configuración para escenarios en los que debe recaudar impuestos cuando vende a otro país o región, como otros países de la UE. 

Actualmente, la extensión **Conector Shopify** admite la exportación de un solo precio. Shopify aplica automáticamente los impuestos locales, las monedas y el redondeo. La opción **Todos los precios incluyen impuestos** da como resultado las acciones descritas en las siguientes subsecciones.

### <a name="all-prices-include-tax-is-selected"></a>*Todos los precios incluyen impuestos* es seleccionado

||Ventas domesticas|País extranjero donde estás recaudando impuestos|País extranjero donde no está recaudando impuestos|
|------------------------|--------|--------|--------|
|Precio mostrado en el escaparate|1200|1200|1200|
|Porcentaje de tasa fiscal|20|25|0|
|Precio en la caja|1200|1200|1200|

El precio para el cliente permanece intacto, independientemente de su ubicación, pero su margen se ve afectado debido a las tasas impositivas que difieren según el país o región.

### <a name="all-prices-include-tax-is-not-selected"></a>*Todos los precios incluyen impuestos* no es seleccionado

||Ventas domesticas|País extranjero donde estás recaudando impuestos|País extranjero donde no está recaudando impuestos|
|------------------------|--------|--------|--------|
|Precio mostrado en el escaparate|1000|1000|1000|
|Porcentaje de tasa fiscal|20|25|0|
|Precio en la caja|1200|1250|1000|

Shopify agrega impuestos locales además del precio definido en la tarjeta del producto según el lugar al que se envíen los productos.

## <a name="dynamic-tax-inclusive-pricing"></a>Precios dinámicos con impuestos incluidos

Debido a que los diferentes países o regiones tienen diferentes requisitos dependiendo de si incluye impuestos en el precio que se muestra o no, puede activar [precios dinámicos con impuestos incluidos](https://help.shopify.com/en/manual/markets/pricing/dynamic-tax-inclusive-pricing) en Shopify. Esto automatiza la función de inclusión de impuestos. 
<!--I added the last sentence to complete the thought. I hope that's okay.-->

Seleccione **Incluya o excluya impuestos según el país o región de su cliente** en la sección **Otros Mercados - Preferencias** de la configuración de [**Mercados**](https://www.shopify.com/admin/settings/markets) en su **Administración de Shopify**.  

> [!NOTE]
> Esta configuración no afecta la representación de los precios en los mercados domésticos, que es controlado por la opción **Todos los precios incluyen impuestos**.

### <a name="all-prices-include-tax-is-selected"></a>*Todos los precios incluyen impuestos* es seleccionado

||Ventas domesticas|País extranjero donde el impuesto está incluido en el precio|País extranjero donde el impuesto está excluido|
|------------------------|--------|--------|--------|
|Precio mostrado en el escaparate|1200|1250|1000|
|Porcentaje de tasa fiscal|20|25|10|
|Precio en la caja|1200|1250|1100|

El precio para cada cliente cambia dependiendo de su ubicación.

### <a name="all-prices-include-tax-is-not-selected"></a>*Todos los precios incluyen impuestos* no es seleccionado

||Ventas domesticas|País extranjero donde el impuesto está incluido en el precio|País extranjero, donde el impuesto está excluido|
|------------------------|--------|--------|--------|
|Precio mostrado en el escaparate|1000|1250|1000|
|Porcentaje de tasa fiscal|20|25|10|
|Precio en la caja|1200|1250|1100|

> [!NOTE]
> La opción **Todos los precios incluyen impuestos** no cambia la forma en que se muestran los precios a los clientes internacionales.

## <a name="if-you-sell-to-eu-customers"></a>Si vende a clientes de la UE

Los diferentes países de la UE tienen diferentes tasas de impuestos locales. Sin embargo, si se encuentra en la UE y vende a otros países de la UE, puede utilizar su tasa impositiva local en algunos casos.  

Marque la casilla **Recaudar IVA** en la sección **Unión Europea** de la configuración de [**Impuestos y deberes**](https://www.shopify.com/admin/settings/taxes) en su **Administración de Shopify**.

|Recaudar IVA|Tasa de IVA|
|-|-|
|Exención de microempresas|Use su tasa impositiva nacional para todas las ventas dentro de la UE|
|Ventanilla única o registro específico del país|Utilice la tasa de IVA del país o región de su cliente|


### <a name="collect-vat-set-to-one-stop-shop-registration"></a>Recaudar IVA configurado para el registro de ventanilla única

En el siguiente ejemplo, la opción **Todos los precios incluyen impuestos** está habilitada. El precio en la ficha del producto se establece en *1200*. 
        
|-|Ventas domesticas|País extranjero|
|------------------------|--------|--------|
|Precio mostrado en el escaparate|1200|1250|
|Porcentaje de tasa fiscal|20|25|
|Precio en la caja|1200|1250|       
        
### <a name="collect-vat-set-to-micro-business-exemption"></a>Recaudar IVA fijado en exención de microempresas

En el siguiente ejemplo, la opción **Todos los precios incluyen impuestos** está habilitada. El precio en la ficha del producto se establece en *1200*. 
        
|-|Ventas domesticas|País extranjero con tasa impositiva local del 25 por ciento.|
|------------------------|--------|--------|
|Precio mostrado en el escaparate|1200|1200|
|Porcentaje de tasa fiscal|20|20|
|Precio en la caja|1200|1200|           
    
Shopify ignora la tasa impositiva en el país extranjero al calcular los precios finales y utiliza la tasa impositiva nacional.

## <a name="importing-shopify-orders-sold-to-international-customers"></a>Importando pedidos de Shopify vendidos a clientes internacionales

Si está recaudando impuestos de varios países o regiones, lo más probable es que necesite definir una configuración específica de país o región en [!INCLUDE[prod_short](../includes/prod_short.md)]. Esto es necesario porque cuando se crea un documento de ventas en [!INCLUDE[prod_short](../includes/prod_short.md)], el sistema calcula los impuestos en lugar de reutilizar los importados de Shopify.

Los ajustes específicos de país/región se eligen en la ventana **Plantilla de cliente de Shopify**.
<!--Should this be "window" or "page"? I haven't been seeing "window" is use elsewhere, but I don't know what the interface looks like for this action.--> Allí puede definir el **N.º de cliente genérico** o **N.º de plantilla de cliente**. En cualquier caso, asegúrese de que el cliente o la plantilla seleccionados tengan definidos los siguientes campos:

1. **Grupo contable de negocio general** (usado para clientes extranjeros).
2. **Grupo contable de negocio IVA** (usado para clientes extranjeros).
3. **Precios con IVA incluido** (alineado con la configuración en el lado de Shopify):
* Elija *Sí* si **Todos los precios incluyen impuestos** está habilitado e **Incluya o excluya impuestos según el país de su cliente** está desactivado.
* Elija *No* si **Todos los precios incluyen impuestos** está desactivado e **Incluya o excluya impuestos según el país de su cliente** está desactivado.
* Elija *Sí* si **Incluya o excluya impuestos según el país de su cliente** está activado y el país o región aparece en la lista [Países y regiones con impuestos incluidos](https://help.shopify.com/en/manual/markets/pricing/dynamic-tax-inclusive-pricing#tax-inclusive-versus-tax-exclusive-countries-and-regions).
* Elija *No* si **Incluya o excluya impuestos según el país de su cliente** está activado y el país o región no aparece en la lista [Países y regiones con impuestos incluidos](https://help.shopify.com/en/manual/markets/pricing/dynamic-tax-inclusive-pricing#tax-inclusive-versus-tax-exclusive-countries-and-regions).
<!--I changed "Set" to "Choose" since "Set" really isn't an instruction we use. if they're toggling, we then would say "Toggle" as in "Toggle *No* if...."-->
> 
[!Note]
> La configuración del campo **Precios con IVA incluido** proviene de la plantilla, no del cliente específico. Por eso es importante tener definida la plantilla de cliente.

## <a name="other-tax-remarks"></a>Otras observaciones sobre impuestos

Mientras que el pedido de Shopify importado contiene información sobre impuestos, los impuestos se vuelven a calcular cuando se crea el documento de ventas. Ese nuevo cálculo significa que es importante que la configuración de IVA/impuestos sea correcta en [!INCLUDE[prod_short](../includes/prod_short.md)].

- Múltiples tasas de impuestos o IVA sobre productos. Por ejemplo, algunas categorías de productos están sujetas a tipos impositivos reducidos. Puede usar la característica [anulación de impuestos](https://help.shopify.com/en/manual/taxes/tax-overrides#create-a-manual-collection-for-products-that-need-a-tax-override) en Shopify. Cuando los elementos se importan y se crean en [!INCLUDE[prod_short](../includes/prod_short.md)], usan la configuración de impuestos tal como se completó en el código de plantilla de artículo en la tienda Shopify. Antes de importar pedidos con dichos artículos, debe actualizar el grupo de contabilización de productos con IVA.  

- Tasas de impuestos dependientes de la dirección. Utilice el campo **Prioridad de área fiscal** junto con la tabla **Plantillas de clientes** para sobrescribir la lógica estándar que rellena el **Código de área fiscal** en el documento de venta. El campo **Prioridad de área fiscal** especifica la prioridad de la que la función debe tomar la información sobre el país o región y el estado o provincia. Luego, se identifica el registro correspondiente en las plantillas de cliente de Shopify y se usan el **Código de área fiscal**, **Sujeto a impuestos** y **Grupo de registro de negocio con IVA** al crear un documento de ventas.  

## <a name="see-also"></a>Consulte también

[Comenzar con el conector para Shopify](get-started.md)  
