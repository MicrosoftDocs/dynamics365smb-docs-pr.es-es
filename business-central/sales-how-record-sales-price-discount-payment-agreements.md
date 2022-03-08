---
title: Configurar precios y descuentos de venta especiales para clientes | Documentos de Microsoft
description: Describe cómo definir los acuerdos de precios y descuentos alternativos que desea aplicar a los documentos de venta al vender a distintos clientes.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: special price, alternate price, pricing
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: bb93853d878ec1aa9b8b0095eb89589c35610f1a
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216158"
---
# <a name="record-special-sales-prices-and-discounts"></a>Registrar precios y descuentos de ventas especiales
> [!NOTE]
> En el segundo lanzamiento de versiones de 2020, lanzamos procesos optimizados para configurar y administrar precios y descuentos. Si es un cliente nuevo que usa esa versión, está usando la nueva experiencia. Si es un cliente existente, si está utilizando o no la nueva experiencia depende de si su administrador ha habilitado la actualización de funciones **Nueva experiencia de precios de venta** en **Administración de características**. Para más información, consulte [Habilitación de las próximas funciones antes de tiempo](/dynamics365/business-central/dev-itpro/administration/feature-management).

Es necesario definir los acuerdos de precios y descuentos que se aplican al vender a los clientes, de modo que se apliquen las reglas y valores acordados a los documentos de venta.

Cuando haya registrado precios especiales y los descuentos de línea para ventas y compras, [!INCLUDE[prod_short](includes/prod_short.md)] garantiza que el beneficio en operaciones comerciales de producto siempre son óptimos calculando automáticamente el mejor precio en los documentos de ventas y compras, y en líneas del diario de proyectos y recursos. Para obtener más información, vea [Cálculo del mejor precio](sales-how-record-sales-price-discount-payment-agreements.md#best-price-calculation).

Respecto a los precios, puede tener una precio especial de venta insertado en las líneas de venta si existe una cierta combinación de cliente, producto, cantidad mínima, unidad de medida o fecha de inicio o de fin. Para obtener más información, consulte las secciones [Para configurar un precio de venta para un cliente](#to-set-up-a-sales-price-for-a-customer) y [Cálculo del mejor precio](#best-price-calculation).  

Respecto a los descuentos, puede configurar y usar dos tipos de descuentos de ventas:

| Tipo de descuento | Descripción |
| --- | --- |
| **Descuento línea venta** |Un importe de descuento que está insertado en las líneas de venta si existe una cierta combinación de cliente, producto, cantidad mínima, unidad de medida o fecha de inicio o de fin. Funciona igual que para los precios de venta. |
| **Descuento en factura** |Un porcentaje de descuento que se resta del total del documento de venta si la suma de todas las líneas del documento supera cierto límite. |

Dado que los descuentos de línea de venta y los precios de venta se basan en una combinación de artículo y cliente, también puede realizar esta configuración desde la página del producto corrrespondiente al producto al que se aplican las reglas y valores.

> [!TIP]  
> Si nunca debe venderse un producto con descuento, simplemente deje vacíos los campos de descuento en la ficha del producto y no incluya el producto en ninguna configuración de descuento de línea.

Los campos **Se aplica al tipo** y **Se aplica al N.º** le permiten elegir a qué se aplicará esta lista de precios, como el cliente o el grupo de precios del cliente. Usando **Ver columnas para**, puede mostrar u ocultar columnas relevantes para establecer precios, descuentos o precios y descuentos.

Puede establecer manualmente líneas de lista de precios o puede usar, por ejemplo, la acción **Sugerir líneas** para crear nuevos precios para productos seleccionados, grupos de descuentos de productos, recursos y otros tipos de productos. Si elige Sugerir líneas, la página Líneas de precios: Crear nueva le permite configurar filtros para seleccionar productos para los que desea crear nuevas líneas de lista de precios. También puede especificar si se debe considerar una cantidad mínima al calcular los precios, el factor de ajuste para aplicar nuevas líneas de lista de precios y el método de redondeo a aplicar a los precios. La acción **Copiar líneas** le permite copiar líneas de lista de precios existentes entre listas de precios.

De forma predeterminada, el estado de las nuevas listas de precios es Borrador. Cuando haya terminado de agregar líneas y desee que el motor de cálculo de precios lo incluya, puede cambiar el estado a Activo.

Para revisar las listas de precios y los precios que se aplican a clientes o proveedores específicos, en la página **Cliente**, elija **Proveedor** o, en la página **Proveedor**, elija **Listas de precios de compra**. Puede ver las líneas de lista de precios en diversas listas de precios seleccionando **Precios de venta** o **Precios de compra** en las páginas **Producto** y **Recurso**.

## <a name="to-set-up-a-sales-price-for-a-customer"></a>Para configurar un precio de venta para un cliente

Estos pasos difieren, dependiendo de si su administrador ha activado la actualiación de la característica **Nueva experiencia de precios de venta**.  

#### <a name="current-experience"></a>[Experiencia actual](#tab/current-experience/)

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Clientes** y luego elija el enlace relacionado.
2. Elija el cliente y, a continuación, elija la acción **Precios**.
3. Rellene los campos de la línea como sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Rellene una línea para cada combinación que aplicará un precio de venta especial al cliente.

#### <a name="new-experience"></a>[Nueva experiencia](#tab/new-experience/)  

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Clientes** y luego elija el enlace relacionado.
2. Elija el cliente y, a continuación, elija la acción **Listas de precios de venta**. 
3. Para crear una nueva lista de precios, elija **Nueva**.
4. En las fichas desplegables **General** e **Impuesto**, rellene los campos como sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
5. Para agregar elementos a la lista, realice una de las siguientes acciones:
   * Para agregar muchos elementos, elija **Sugerir líneas** y luego introduzca los criterios de filtro para especificar los tipos de productos que se agregarán. Opcionalmente, también puede introducir algunas configuraciones adicionales para los productos específicos de la lista de precios. Puede cambiarlos más tarde si lo necesita.
   * Para copiar productos de otra lista de precios, elija **Copiar líneas** y luego elija la lista de precios a copiar.
   * Para agregar elementos manualmente, en la cuadrícula, en el campo **Tipo de producto**, elija el tipo de producto para el que es la lista de precios. Dependiendo de la selección, rellene los campos restantes según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. Para empezar a utilizar la lista de precios, en el campo **Estado**, elija **Activo**.  

---

## <a name="sales-invoice-discounts-and-service-charges"></a>Descuentos en factura de ventas y cargos por servicios
Al utilizar descuentos en factura, el importe total de la factura determina el tamaño del descuento aplicado. En la página **Dtos. factura clientes**, también puede añadir un cargo por servicio a las facturas que superen un determinado importe.  

Para poder aplicar descuentos en factura a las ventas, primero debe especificar determinados datos. Debe decidir lo siguiente:  

- A qué clientes se le concederá este tipo de descuento  
- Qué porcentajes de descuento se van a aplicar  

Si desea descuentos en factura para que se calculen automáticamente, puede especificarlo en la página **Configuración ventas y cobros**.  

Decida si va a conceder o no descuentos en factura a cada cliente que cumpla el requisito (es decir, que el importe de su factura supere una determinada cantidad). Defina los términos de los descuentos en factura en divisa local para los clientes nacionales y en otras divisas para los clientes de otros países.  

Se relacionan los porcentajes de descuento a los importes de factura específicos en la página **Dtos. factura cliente** para cada cilente. Puede introducir un número ilimitado de porcentajes. Cada cliente puede tener su propia página o se pueden vincular varios clientes a la misma página.  

Además de (o en lugar de) un porcentaje de descuento, puede vincular un importe de cargo por servicios a un importe facturado específico.  

> [!TIP]  
> Antes de introducir esta información, se recomienda preparar un esquema de la estructura de descuentos que desea utilizar. De este modo, podrá ver fácilmente los clientes que se pueden vincular a la misma página de descuentos en factura. Cuantas menos páginas tenga que configurar, más rápido introducirá la información básica.

Para formación sobre descuentos en ventas, consulte [Establecer descuentos para sus clientes](/learn/modules/customer-discounts-dynamics-365-business-central/index) en Microsoft Learn.  

### <a name="calculating-invoice-discounts-on-sales"></a>Calcular descuentos en factura para ventas

[!INCLUDE [sales-invoice-discounts](includes/sales-invoice-discounts.md)]

## <a name="to-set-up-a-sales-line-discount-for-a-customer"></a>Para configurar un descuento de línea de venta para un cliente
Estos pasos difieren, dependiendo de si su administrador ha activado la actualiación de la característica **Nueva experiencia de precios de venta**. 

#### <a name="current-experience"></a>[Experiencia actual](#tab/current-experience/)  

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Clientes** y luego elija el enlace relacionado.
2. Abra la ficha de cliente correspondiente y, a continuación, elija la acción **Descuentos de línea**.
3. Rellene los campos de la línea como sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Rellene una línea para cada combinación que aplicará un descuento de línea de venta al cliente.

> [!Note]
> Cuando abra las páginas **Precios de venta** y **Descuentos de línea de ventas** de un cliente específico, los campos **Filtro de tipo de ventas** y **Filtro de código de ventas** se establecen para el cliente y no se pueden cambiar ni eliminar.
>
> Para configurar precios o descuentos de línea para todos los clientes, un grupo de precios de clientes o una campaña, debe abrir las páginas desde una tarjeta de producto. Alternativamente, para precios de venta, use la página **Hoja de trabajo de precio de venta**. Para obtener más información, vea [Para actualizar de forma masiva los precios de los productos](sales-how-record-sales-price-discount-payment-agreements.md#to-bulk-update-item-prices).  

#### <a name="new-experience"></a>[Nueva experiencia](#tab/new-experience/)  

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Clientes** y luego elija el enlace relacionado.
2. Elija el cliente y, a continuación, elija la acción **Listas de precios de venta**.
3. Abra la lista de precios para la que desea especificar el descuento de línea.
4. Active el conmutador **Permitir descuento de línea**.
5. Cree una nueva línea o elija una existente y luego complete los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. En el campo **Define**, elija ya sea **Precio y descuento**, o solo **Descuento**. 
7. En el campo **% de descuento de línea**, especifique el porcentaje de descuento.

    > [!TIP]
    > Si está editando una línea existente, puede filtrar las líneas eligiendo la opción adecuada en el campo **Ver columnas para**.

    > [!NOTE]  
    > Los códigos de descuento en factura se representan por las fichas existentes del cliente. Lo que permite asignar rápidamente las condiciones de descuento en factura a clientes realizando el picking del nombre de otros clientes con los mismos términos. Para configurar términos de descuento de factura específicos del cliente, configure el campo **Código des. factura** con el código de cliente y luego continúe con el siguiente paso.

8. En la página **Ficha de cliente**, seleccione la acción **Descuento factura**. Aparecerá la página **Dtos. factura cliente**.
9. En el campo **Código divisa**, introduzca el código de una divisa que se aplique a los términos de descuento en factura en la línea. Deje el campo en blanco para establecer condiciones de descuento en su divisa local.
10. Opcionalmente, en el campo **Importe mínimo**, escriba el importe mínimo que deba tener una factura para optar al descuento.
11. En el campo **% descuento**, introduzca el descuento en la factura como un porcentaje del importe de la factura.
12. Repita los pasos del 5 al 7 para cada divisa que el cliente reciba un descuento diferente de factura.

El descuento en factura ahora está configurado y asignado al cliente. Al seleccionar el código del cliente en el campo **Código de descuento en factura** en otras fichas de cliente, se asigna el mismo descuento en factura a estos clientes.

---

## <a name="to-set-up-an-invoice-discount-for-a-customer"></a>Para configurar un descuento en factura para un cliente
Una vez que haya determinado los clientes que pueden obtener descuentos en factura, introduzca el código de descuento en factura en las fichas de cliente y especifique los términos de cada código.

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Clientes** y luego elija el enlace relacionado.
2. Abra la página de cliente para un cliente que pueda obtener descuentos en factura.
3. En el campo **Código descuento factura**, seleccione un código para los términos relevantes de la factura con descuentos que usará para calcular los descuentos en facturas para el cliente. <!--Looks like I can only choose customers in this list-->

> [!NOTE]  
> Los códigos de descuento en factura se representan por las fichas existentes del cliente. Lo que permite asignar rápidamente las condiciones de descuento en factura a clientes realizando el picking del nombre de otros clientes con los mismos términos.

Configure de nuevo los términos de descuento en factura de ventas.

1. En la página **Clientes**, seleccione la acción **Descuentos en factura**. Aparecerá la página **Descuentos en factura al cliente**.
2. En el campo **Código divisa**, introduzca el código de una divisa que se aplique a los términos de descuento en factura en la línea. Deje el campo en blanco para establecer condiciones de descuento en su divisa local.
3. En el campo **Importe mínimo**, escriba el importe mínimo que deba tener una factura para optar al descuento.
4. En el campo **% descuento**, introduzca el descuento en la factura como un porcentaje del importe de la factura.
5. Repita los pasos del 5 al 7 para cada divisa que el cliente reciba un descuento diferente de factura.

## <a name="to-copy-sales-prices"></a>Para copiar precios de venta
Estos pasos difieren, dependiendo de si su administrador ha activado la actualiación de la característica **Nueva experiencia de precios de venta**. 

#### <a name="current-experience"></a>[Experiencia actual](#tab/current-experience/)  

Si desea copiar precios de venta, por ejemplo, los precios de venta de un cliente determinado a un grupo de precios de clientes, debe ejecutar el proceso **Sugerir precio venta en hoja**. en la página **Hoja de precios de venta**.  

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Hoja de precios de venta** y luego elija el enlace relacionado.  
2. Elija **Sugerir precio venta en hoja**. .  
3. En la ficha desplegable **Precios venta**, rellene los campos **Tipo venta** y **Código ventas** con los precios de venta originales que desea copiar.  
4. En la parte superior de la página de solicitud, rellene los campos **Tipo venta** y **Código ventas** con el tipo y el nombre al que desea copiar los precios de venta.  
5. Si desea que el trabajo por lotes cree precios nuevos, seleccione la casilla **Crear precios nuevos**.  
6. Elija el botón **Aceptar** para rellenar las líneas de la página **Hoja precios venta** con los nuevos precios propuestos, indicando que son válidos para el tipo de venta seleccionado.  

   > [!NOTE]  
   > El proceso sólo crea propuestas; no implementa los cambios propuestos. Si está satisfecho con las propuestas y desea implementarlas, es decir, insertarlas en la página **Precios de venta**, elija la acción **Implementar cambios de precios** en la página **Hoja de precios de venta**.

#### <a name="new-experience"></a>[Nueva experiencia](#tab/new-experience/)  

El estado de la lista de precios debe ser **Borrador**. 

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Listas de precios de venta** y luego elija el enlace relacionado. 
2. Elija la lista de precios a copiar y luego elija **Copiar líneas**.
3. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

   > [!NOTE]
   > No puede tener dos líneas que tengan la misma configuración pero diferentes precios. Si eso sucede, aparecerá un mensaje cuando active una lista de precios. Puede elegir el precio a utilizar abriendo la lista y eliminando el precio incorrecto.  
  
---

## <a name="to-bulk-update-item-prices"></a>Para actualizar de forma masiva los precios de los artículos
Estos pasos difieren, dependiendo de si su administrador ha activado la actualiación de la característica **Nueva experiencia de precios de venta**. 

#### <a name="current-experience"></a>[Experiencia actual](#tab/current-experience/)

Si desea actualizar de forma masiva los precios de los artículos, como aumentar todos los precios de los artículos en algún porcentaje, debe ejecutar el proceso **Sugerir precio producto en hoja**. Trabajo por lotes . Puede encontrar un enlace al proceso en la página **Hoja precios venta**.  

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Hoja de precios de venta** y luego elija el enlace relacionado.  
2. Elija **Sugerir precio producto en hoja**. .  
3. En la ficha desplegable **Artículo**, rellene los campos **N.º** o **Grupo registro inventario** u otros con los precios del artículo original que desea actualizar.  
4. En la parte superior de la página de solicitud, rellene el **Tipo venta** y **Código ventas** con el tipo y el nombre al que desea copiar los precios de venta.
5. Si desea que el proceso ajuste automáticamente los precios de los artículos sugeridos, introduzca el ajuste en el campo **Factor de ajuste**. Por ejemplo, debe introducir 1,15 en **Factor de ajuste** para un aumento del 15% en el precio del artículo.  
6. Si desea que el trabajo por lotes cree precios nuevos, seleccione el campo **Crear precios nuevos**.  
7. Elija el botón **Aceptar** para rellenar las líneas de la página **Hoja precios venta** con los nuevos precios propuestos, indicando que son válidos para el **Artículo** seleccionado.  

> [!NOTE]
> El proceso sólo crea propuestas; no implementa los cambios propuestos. Si está satisfecho con las propuestas y desea implantarlas, es decir, insertarlas en la tabla **Precios de venta**, puede utilizar el trabajo por lotes **Realizar cambio precio**, que se encuentra en la pestaña **Acciones**, en el grupo **Funciones**, en la página **Hoja de precios de venta**.

#### <a name="new-experience"></a>[Nueva experiencia](#tab/new-experience/)

Para actualizar los precios de varios productos, debe crear una nueva lista de precios y luego copiar las líneas desde una lista de precios existente. Cuando copie las líneas, puede usar filtros para especificar qué copiar, y puede especificar un número entero o decimal en el campo **Factor de ajuste** para aumentar o disminuir los precios. El estado de la lista de precios debe estar en estado **Borrador**. Si es necesario, puede desactivar la lista de precios anterior.

> [!NOTE]
> No puede tener dos líneas que tengan la misma configuración pero diferentes precios. Si eso sucede, aparecerá un mensaje cuando active una lista de precios. Puede elegir el precio a utilizar abriendo la lista y eliminando el precio incorrecto.  

---

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

2. [!INCLUDE[d365fin](includes/d365fin_md.md)] comprueba si se aplican acuerdos de precios o descuentos a la información de la línea de documento o de diario y, a continuación, inserta el precio unitario y porcentaje de descuento de línea, utilizando el siguiente criterio:

    - ¿Hay un requisito de cantidad mínima en el acuerdo de precios o descuentos que se debe cumplir?
    - ¿Hay un requisito de divisa en el acuerdo de precios o descuentos que se debe cumplir? Si es así, se insertan el precio más bajo y el descuento de línea más alto para esa divisa, incluso si la divisa local proporciona un precio mejor. Si no existen acuerdos de precios o descuentos para el código de divisa especificado, [!INCLUDE[d365fin](includes/d365fin_md.md)] inserte el menor precio y el mayor descuento de línea en la su divisa local.

Si no se puede calcular ningún precio especial para el producto de la línea, se inserta el último coste directo o el precio unitario de la ficha de producto.

## <a name="see-related-training-at-microsoft-learn"></a>Consulte Formación relacionada en [Microsoft Learn](/learn/modules/manage-sales-prices-dynamics-365-business-central/index)

## <a name="see-also"></a>Consulte también

[Configuración de ventas](sales-setup-sales.md)  
[Ccial](sales-manage-sales.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]