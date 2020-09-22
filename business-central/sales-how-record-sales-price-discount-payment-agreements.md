---
title: Configurar precios y descuentos de venta especiales para clientes | Documentos de Microsoft
description: Describe cómo definir los acuerdos de precios y descuentos alternativos que desea aplicar a los documentos de venta al vender a distintos clientes.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: special price, alternate price, pricing
ms.date: 07/07/2020
ms.author: edupont
ms.openlocfilehash: 46c94de4b1852549aea9fb7d2279fe045e33df1f
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "3789030"
---
# <a name="record-special-sales-prices-and-discounts"></a>Registrar precios y descuentos de ventas especiales

Es necesario definir los acuerdos de precios y descuentos que se aplican al vender a distintos clientes de modo que se apliquen las reglas y valores acordados a los documentos de venta que cree para los clientes.

Cuando haya registrado precios especiales y los descuentos de línea para ventas y compras, [!INCLUDE[d365fin](includes/d365fin_md.md)] garantiza que el beneficio en operaciones comerciales de producto siempre son óptimos calculando automáticamente el mejor precio en los documentos de ventas y compras, y en líneas del diario de proyectos y recursos. Para obtener más información, vea [Cálculo del mejor precio](sales-how-record-sales-price-discount-payment-agreements.md#best-price-calculation).

Respecto a los precios, puede tener una precio especial de venta insertado en las líneas de venta si existe una cierta combinación de cliente, producto, cantidad mínima, unidad de medida o fecha de inicio o de fin.

Respecto a los descuentos, puede configurar y usar dos tipos de descuentos de ventas:

| Tipo de descuento | Descripción |
| --- | --- |
| **Descuento línea venta** |Un importe de descuento que está insertado en las líneas de venta si existe una cierta combinación de cliente, producto, cantidad mínima, unidad de medida o fecha de inicio o de fin. Funciona igual que para los precios de venta. |
| **Descuento en factura** |Un porcentaje de descuento que se resta del total del documento si el importe de todas las líneas de un documento de venta supera cierto límite. |

Dado que los descuentos de línea de venta y los precios de venta se basan en una combinación de producto y cliente, también puede basar esta configuración en la ficha del producto al que se aplican las reglas y valores.

> [!NOTE]  
> Si no desea que un artículo se venda a un precio con descuento, simplemente deje los campos de descuento en la ficha del artículo en blanco y no los incluya en la configuración de descuento de línea.

## <a name="to-set-up-a-sales-price-for-a-customer"></a>Para configurar un precio de venta para un cliente

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Clientes** y luego elija el enlace relacionado.
2. Abra la ficha de cliente correspondiente y, a continuación, elija la acción **Precios**.

    En la página **Precios ventas**, el campo **Tipo venta** se rellena con **Cliente** y el campo **Código ventas** se rellena con el número de cliente.
3. Rellene los campos de la línea como sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Rellene una línea para cada combinación que aplicará un precio de venta especial al cliente.

## <a name="to-set-up-a-sales-line-discount-for-a-customer"></a>Para configurar un descuento de línea de venta para un cliente

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Clientes** y luego elija el enlace relacionado.
2. Abra la ficha de cliente correspondiente y, a continuación, elija la acción **Dto. línea**.

    En la página **Descuentos línea de ventas**, el campo **Tipo venta** se rellena con **Cliente** y el campo **Código ventas** se rellena con el número de cliente.
3. Rellene los campos de la línea como sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Rellene una línea para cada combinación que aplicará un descuento de línea de venta al cliente.

> [!Note]
> Cuando abra las ventanas **Precios de venta** y **Descuentos de línea de ventas** de un cliente específico, los campos **Filtro de tipo de ventas** y **Filtro de código de ventas** se establecen para el cliente y no se pueden cambiar ni eliminar, lo que se indica mediante el valor atenuado en el campo **Filtro de código de ventas**.
>
> Para configurar precios o descuentos de línea para todos los clientes, un grupo de precios de clientes o una campaña, debe abrir las ventanas desde una tarjeta de producto. Alternativamente, para precios de venta, use la página **Hoja de trabajo de precio de venta**. Para obtener más información, vea [Para actualizar de forma masiva los precios de los productos](sales-how-record-sales-price-discount-payment-agreements.md#to-bulk-update-item-prices).  

## <a name="to-set-up-an-invoice-discount-for-a-customer"></a>Para configurar un descuento en factura para un cliente

Una vez que haya determinado los clientes que pueden obtener descuentos en factura, introduzca el código de descuento en factura en las fichas de cliente y especifique los términos de cada código.

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Clientes** y luego elija el enlace relacionado.
2. Abra la ficha de un cliente que pueda obtener descuentos en factura.
3. En el campo **Código descuento factura**, seleccione un código para los términos relevantes de la factura con descuentos que usará para calcular los descuentos en facturas para el cliente.

> [!NOTE]  
> Los códigos de descuento en factura se representan por las fichas existentes del cliente. Lo que permite asignar rápidamente las condiciones de descuento en factura a clientes realizando el picking del nombre de otros clientes con los mismos términos.

Configure de nuevo los términos de descuento en factura para ventas.

1. En la página **Ficha de cliente**, seleccione la acción **Descuento factura**. Aparecerá la página **Dtos. factura cliente**.
2. En el campo **Código divisa**, introduzca el código de una divisa que se aplique a los términos de descuento en factura en la línea. Deje el campo en blanco para establecer condiciones de descuento de factura en la divisa local.
3. En el campo **Importe mínimo**, escriba el importe mínimo que deba tener una factura para optar al descuento.
4. En el campo **% descuento**, introduzca el descuento en la factura como un porcentaje del importe de la factura.
5. Repita los pasos del 5 al 7 para cada divisa que el cliente reciba un descuento diferente de factura.

El descuento en factura ahora está configurado y asignado al cliente en cuestión. Al seleccionar el código del cliente en el campo **Cód. dto. factura** en otras fichas de cliente, se asigna el mismo descuento en factura a estos clientes.

## <a name="to-work-with-sales-invoice-discounts-and-service-charges"></a>Trabajar con descuentos y cargos por servicios de la factura de venta

Al utilizar descuentos en factura, el importe de la factura determina el descuento aplicado.  

En la página **Dtos. factura clientes**, también puede añadir un cargo por servicio a las facturas que superen un determinado importe.  

Para poder aplicar descuentos en factura a las ventas, primero debe especificar determinados datos en la aplicación. Deberá determinar las siguientes cuestiones:  

- a qué clientes se le concederá este tipo de descuento.  
- qué porcentajes de descuento se va a aplicar.  

Si factura descuentos para que se calculen automáticamente, puede especificarlo en la página **Configuración ventas y cobros**.  

Decida si va a conceder o no descuentos en factura a cada cliente que cumpla el requisito (es decir, que el importe de su factura supere una determinada cantidad). Defina los términos de los descuentos en factura en divisa local para los clientes nacionales y en otras divisas para los clientes de otros países.  

Se relacionan los porcentajes de descuento a los importes de factura específicos en las páginas **Dtos. factura cliente**. Puede introducir un número ilimitado de porcentajes en cada página. Cada cliente puede tener su propia página o se pueden vincular varios clientes a la misma página.  

Además de (o en lugar de) un porcentaje de descuento, puede vincular un importe de cargo por servicios a un importe facturado específico.  

> [!TIP]  
> Antes de introducir esta información, se recomienda preparar un esquema de la estructura de descuentos que desea utilizar. De este modo, podrá ver fácilmente los clientes que se pueden vincular a la misma página de descuentos en factura. Cuantas menos páginas tenga que configurar, más rápido introducirá la información básica.

Para obtener más información sobre descuentos en ventas, consulte [Establecer descuentos para sus clientes](/learn/modules/customer-discounts-dynamics-365-business-central/index) en Microsoft Learn.  

## <a name="best-price-calculation"></a>Cálculo del mejor precio

Cuando haya registrado precios especiales y los descuentos de línea para ventas y compras, [!INCLUDE[d365fin](includes/d365fin_md.md)] garantiza que el beneficio en operaciones comerciales de producto siempre son óptimos calculando automáticamente el mejor precio en los documentos de ventas y compras, y en líneas del diario de proyectos y recursos.

El mejor precio es el precio más bajo permisible con el mayor descuento de línea permisible en una fecha indicada. [!INCLUDE[d365fin](includes/d365fin_md.md)] lo calcula automáticamente al insertar el precio por unidad y el porcentaje de descuento de línea de los productos en las nuevas líneas de documento y diario.

> [!NOTE]  
> A continuación se describe cómo se calcula el mejor precio para las ventas. El cálculo es igual para las compras.

1. [!INCLUDE[d365fin](includes/d365fin_md.md)] comprueba la combinación de la factura a cliente y el producto, y calcula el precio por unidad y el porcentaje de descuento de línea aplicables utilizando los siguientes criterios:

    - ¿El cliente tiene un acuerdo de precios o descuentos, o el cliente pertenece a un grupo que lo tiene?
    - ¿Está incluido el producto o el grupo de descuento del producto de la línea en alguno de estos acuerdos de precios o descuentos?
    - ¿La fecha de pedido (o la fecha de registro de la factura y abono) está comprendida entre la fecha inicial y la fecha final del acuerdo de precios o descuentos?
    - ¿Se ha especificado un código de unidad de medida? Si es así, [!INCLUDE[d365fin](includes/d365fin_md.md)] comprueba los precios o descuentos con el mismo código de unidad de medida y los precios o descuentos sin un código de unidad de medida.

2. [!INCLUDE[d365fin](includes/d365fin_md.md)] comprueba si se aplican acuerdos de precios o de descuentos a la información de la línea de documento o de diario y, a continuación, inserta el precio unitario y porcentaje de descuento de línea, utilizando el siguiente criterio:

    - ¿Hay un requisito de cantidad mínima en el acuerdo de precios o descuentos que se debe cumplir?
    - ¿Hay un requisito de divisa en el acuerdo de precios o descuentos que se debe cumplir? Si es así, se insertan el precio más bajo y el descuento de línea más alto para esa divisa, incluso si la divisa local proporciona un precio mejor. Si no existen acuerdos de precios o descuentos para el código de divisa especificado, [!INCLUDE[d365fin](includes/d365fin_md.md)] inserte el menor precio y el mayor descuento de línea en la su divisa local.

Si no se puede calcular ningún precio especial para el producto de la línea, se inserta el último coste directo o el precio unitario de la ficha de producto.

## <a name="to-copy-sales-prices"></a>Para copiar precios de venta

Si desea copiar precios de venta, por ejemplo, los precios de venta de un cliente determinado a un grupo de precio de cliente, debe ejecutar el proceso **Sugerir precio venta en hoja**. proceso, que se ejecuta desde la página **Hoja precios venta**.  

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Hoja de precios de venta** y luego elija el enlace relacionado.  
2. Elija **Sugerir precio venta en hoja**. .  
3. En la ficha desplegable **Precios venta**, rellene los campos **Tipo venta** y **Código ventas** con los precios de venta originales que desea copiar.  
4. En la parte superior de la página de solicitud, rellene los campos **Tipo venta** y **Código ventas** con el tipo y el nombre al que desea copiar los precios de venta.  
5. Si desea que el trabajo por lotes cree precios nuevos, seleccione la casilla **Crear precios nuevos**.  
6. Elija el botón **Aceptar** para rellenar las líneas de la página **Hoja precios venta** con los nuevos precios propuestos, indicando que son válidos para el tipo de venta seleccionado.  

> [!NOTE]  
> El proceso sólo crea propuestas; no implementa los cambios propuestos. Si está satisfecho con las propuestas y desea implementarlas, es decir, insertarlas en la página **Precios de venta**, elija la acción **Implementar cambios de precios** en la página **Hoja precios ventas**.

## <a name="to-bulk-update-item-prices"></a>Para actualizar de forma masiva los precios de los artículos

Si desea actualizar de forma masiva los precios de los artículos, como aumentar todos los precios de los artículos en algún porcentaje, debe ejecutar el proceso **Sugerir precio producto en hoja**. Trabajo por lotes . Puede encontrar un enlace al proceso en la página **Hoja precios venta**.  

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Hoja de precios de venta** y luego elija el enlace relacionado.  
2. Elija **Sugerir precio producto en hoja**. .  
3. En la ficha desplegable **Artículo**, rellene los campos **N.º** o **Grupo registro inventario** u otros con los precios del artículo original que desea actualizar.  
4. En la parte superior de la página de solicitud, rellene el **Tipo venta** y **Código ventas** con el tipo y el nombre al que desea copiar los precios de venta.
5. Si desea que el proceso ajuste automáticamente los precios de los artículos sugeridos, introduzca el ajuste en el campo **Factor de ajuste**. Por ejemplo, debe introducir 1,15 en **Factor de ajuste** para un aumento del 15% en el precio del artículo.  
6. Si desea que el trabajo por lotes cree precios nuevos, seleccione el campo **Crear precios nuevos**.  
7. Elija el botón **Aceptar** para rellenar las líneas de la página **Hoja precios venta** con los nuevos precios propuestos, indicando que son válidos para el **Artículo** seleccionado.  

> [!NOTE]
> El proceso sólo crea propuestas; no implementa los cambios propuestos. Si está satisfecho con las propuestas y desea implantarlas, es decir, insertarlas en la tabla **Precios de venta**, puede utilizar el trabajo por lotes **Realizar cambio precio**, que se encuentra en la pestaña **Acciones**, en el grupo **Funciones**, en la página **Hoja precios venta**.

## <a name="see-related-training-at-microsoft-learn"></a>Consulte Formación relacionada en [Microsoft Learn](/learn/modules/manage-sales-prices-dynamics-365-business-central/index)

## <a name="see-also"></a>Consulte también

[Configuración de ventas](sales-setup-sales.md)  
[Ccial](sales-manage-sales.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
