---
title: Establecer precios y descuentos
description: Describe cómo definir acuerdos de precios y descuentos estándar y especiales para ventas y compras.
author: brentholtorf
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'price, pricing, discount, discounting, rebate, sale, purchase, invoice'
ms.search.form: '459, 460, 7001, 7011, 7015, 7016, 7017, 7018'
ms.date: 04/01/2021
ms.author: bholtorf
---
# <a name="set-up-prices-and-discounts"></a>Establecer precios y descuentos

> [!NOTE]
> En el segundo lanzamiento de versiones de 2020, lanzamos procesos optimizados para configurar y administrar precios y descuentos. Si es un cliente nuevo que usa esa versión, está usando la nueva experiencia. Si es un cliente existente, si está utilizando la nueva experiencia depende de si su administrador ha habilitado la actualización de funciones **Nueva experiencia de precios de venta** en la página **Administración de funciones**. Para más información, consulte [Habilitación de las próximas funciones antes de tiempo](/dynamics365/business-central/dev-itpro/administration/feature-management).

Las estrategias de precios y descuentos para la compra y venta de artículos y servicios son herramientas fundamentales para negocios exitosos. Después de configurar los artículos y servicios que su empresa compra y vende, puede definir lo que paga o cobra por ellos, y esos importes se agregarán automáticamente a los documentos de ventas y compras. 

## <a name="setting-up-prices-and-discounts"></a>Establecimiento de precios y descuentos

Antes de crear listas de precios, debe definir sus estrategias de precios y descuentos en la páginas **Configuración de ventas y cuentas de clientes** y **Configuración de compras y cuentas de proveedores**.

Puede configurar dos tipos de descuentos:

| Tipo de descuento | Descripción |
| --- | --- |
| **Descuento en línea** |Un importe de descuento que se otorga a las líneas de los documentos de compra y venta. Por lo general, los descuentos de línea se basan en una combinación de cliente, artículo, cantidad mínima, unidad de medida o período de tiempo que se define para las ventas y compras en las páginas **Configuración de ventas y cuentas de clientes** y **Configuración de compras y cuentas de proveedores**.|
| **Descuento en factura** |Un porcentaje de descuento que se resta del total de ventas y compras si la suma de todas las líneas del documento supera cierto límite. |

Dado que los descuentos de línea de venta y los precios de venta se basan en una combinación de artículo y cliente, también puede realizar esta configuración desde la página del producto corrrespondiente al producto al que se aplican las reglas y valores.

> [!TIP]  
> Si nunca debe venderse un producto con descuento, simplemente deje vacíos los campos de descuento en la ficha del producto y no incluya el producto en ninguna configuración de descuento de línea.

## <a name="about-price-lists"></a>Acerca de las listas de precios

Las listas de precios son flexibles y le permiten especificar el socio comercial o la actividad a la que se aplican. Por ejemplo, puede configurar una lista de precios que se aplique a todos los proveedores y clientes, u ofrecer precios especiales o descuentos para cada socio comercial, tal vez en función de una cantidad mínima en pedidos de compra o de venta, o de una determinada combinación de cliente, artículo, cantidad mínima, unidad de medida o períodos de tiempo. Los precios y descuentos que defina se aplican automáticamente a los documentos de compra y venta. 

## <a name="set-up-prices"></a>Configurar precios

Estos pasos difieren, dependiendo de si su administrador ha activado la actualiación de la característica **Nueva experiencia de precios de venta**. 

#### [Experiencia actual](#tab/current-experience)  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Clientes** y luego elija el enlace relacionado.
2. Elija el cliente y, a continuación, elija la acción **Precios**.
3. Rellene los campos de la línea como sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Rellene una línea para cada combinación que aplicará un precio de venta especial al cliente.

#### [Nueva experiencia](#tab/new-experience)  

Puede agregar artículos y servicios manualmente para cada línea, o puede usar la acción **Sugerir líneas** para crear nuevos precios para artículos seleccionados, grupos de descuentos de artículos, recursos y otros tipos de productos. Si escoge **Sugerir líneas** en al página **Líneas de precio: crear nueva**, puede utilizar filtros para seleccionar los productos o servicios que se incluirán en la lista de precios. También puede especificar si se debe considerar una cantidad mínima al calcular los precios, el factor de ajuste para aplicar nuevas líneas de lista de precios y el método de redondeo a aplicar a los precios. 

De forma predeterminada, el estado de las nuevas listas de precios es **Borrador**. Cuando esté listo para comenzar a usar la lista, puede cambiar el estado a **Activo**.

Para revisar las listas de precios y los precios que se aplican a clientes o proveedores específicos, en las páginas **Cliente** o **Proveedor**, elija la acción **Listas de precios de venta** o **Listas de precios de compra**. Para productos y recursos, puede ver las líneas de la lista de precios seleccionando **Precios de venta** o **Precios de compra** en las páginas **Producto** y **Recurso**.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Clientes** y luego elija el enlace relacionado.
2. Elija el cliente y, a continuación, elija la acción **Listas de precios de venta**. 
3. Para crear una nueva lista de precios, elija **Nueva**.
4. En las fichas desplegables **General** e **Impuesto**, rellene los campos como sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
5. Para agregar elementos a la lista, realice una de las siguientes acciones:
   * Para agregar muchos elementos, elija **Sugerir líneas** y luego introduzca los criterios de filtro para especificar los tipos de productos que se agregarán. Opcionalmente, también puede introducir algunas configuraciones adicionales para los productos específicos de la lista de precios. Puede cambiarlos más tarde si lo necesita.
   * Para copiar productos de otra lista de precios, elija **Copiar líneas** y luego elija la lista de precios a copiar.
   * Para agregar elementos manualmente, en el campo **Tipo de producto**, elija el tipo de producto para el que es la lista de precios. Dependiendo de la selección, rellene los campos restantes según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. Para empezar a utilizar la lista de precios, en el campo **Estado**, elija **Activo**.  

---

## <a name="to-set-up-a-sales-line-discount-for-a-customer"></a>Para configurar un descuento de línea de venta para un cliente

Estos pasos difieren, dependiendo de si su administrador ha activado la actualiación de la característica **Nueva experiencia de precios de venta**. 

#### [Experiencia actual](#tab/current-experience/)  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Clientes** y luego elija el enlace relacionado.
2. Abra la ficha de cliente correspondiente y, a continuación, elija la acción **Descuentos de línea**.
3. Rellene los campos de la línea como sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Rellene una línea para cada combinación que aplicará un descuento de línea de venta al cliente.

> [!Note]
> Cuando abra las páginas **Precios de venta** y **Descuentos de línea de ventas** de un cliente específico, los campos **Filtro de tipo de ventas** y **Filtro de código de ventas** se establecen para el cliente y no se pueden cambiar ni eliminar.
>
> Para configurar precios o descuentos de línea para todos los clientes, un grupo de precios de clientes o una campaña, debe abrir las páginas desde una tarjeta de producto. Alternativamente, para precios de venta, use la página **Hoja de trabajo de precio de venta**. Para obtener más información, vea [Para actualizar de forma masiva los precios de los productos](sales-how-record-sales-price-discount-payment-agreements.md#to-bulk-update-item-prices).  

#### [Nueva experiencia](#tab/new-experience/)  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Clientes** y luego elija el enlace relacionado.
2. Elija el cliente y, a continuación, elija la acción **Listas de precios de venta**.
3. Abra la lista de precios para la que desea especificar el descuento de línea.
4. Active el conmutador **Permitir descuento de línea**.
5. Cree una nueva línea o elija una existente y luego complete los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. En el campo **Define**, elija ya sea **Precio y descuento**, o solo **Descuento**. 
7. En el campo **% de descuento de línea**, especifique el porcentaje de descuento.

   > [!TIP]
   > Si está editando una línea existente, puede filtrar las líneas eligiendo la opción adecuada en el campo **Ver columnas para**.

---

## <a name="work-with-invoice-discounts-and-service-charges"></a>Trabajar con descuentos en factura y cargos por servicios

Al utilizar descuentos en factura, el importe de la factura determina el descuento aplicado. En la página **Descuentos en factura**, también puede añadir un cargo por servicio a las facturas que superen un determinado importe.  <!--The Invoice Discounts page is hard to find.-->

Para poder aplicar descuentos en factura a las ventas, primero debe especificar determinados datos en la aplicación. Debe decidir qué clientes recibirán este tipo de descuento y los porcentajes de descuento que utilizará.  

Si factura descuentos para que se calculen automáticamente, puede especificarlo en la página **Configuración ventas y cobros**.  

Decida si va a conceder o no descuentos en factura a cada cliente que cumpla el requisito (es decir, que el importe de su factura supere una determinada cantidad). Defina los términos de los descuentos en factura en divisa local para los clientes nacionales y en otras divisas para los clientes de otros países.  

Se relacionan los porcentajes de descuento con los importes de factura específicos en la página **Descuentos en factura**. Puede introducir tantos porcentajes como desee. Cada cliente puede tener su propia página o se pueden vincular varios clientes a la misma página.  

Además de (o en lugar de) un porcentaje de descuento, puede vincular un importe de cargo por servicios a un importe facturado específico.  

> [!TIP]  
> Antes de comenzar a introducir esta información, es una buena idea preparar su estructura de descuentos de antemano, para que sea más fácil ver qué clientes vincular a la misma página de descuento en factura. Para obtener más información sobre descuentos en ventas, consulte [Establecer descuentos para sus clientes](/training/modules/customer-discounts-dynamics-365-business-central/index).

### <a name="to-set-up-an-invoice-discount-for-a-customer"></a>Para configurar un descuento en factura para un cliente

Después de decidir qué clientes pueden obtener descuentos en factura, introduzca el código de descuento en factura en las fichas de cliente y especifique los términos de cada código.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Clientes** y luego elija el enlace relacionado.
2. Abra la página de cliente para un cliente que pueda obtener descuentos en factura.
3. En el campo **Código descuento factura**, seleccione un código para los términos relevantes de la factura con descuentos que usará para calcular los descuentos en facturas para el cliente. <!--Looks like I can only choose customers in this list-->

> [!NOTE]  
> Los códigos de descuento en factura se representan por las fichas existentes del cliente. Lo que permite asignar rápidamente las condiciones de descuento en factura a clientes realizando el picking del nombre de otros clientes con los mismos términos.

Configure de nuevo los términos de descuento en factura de ventas.

1. En la página **Clientes**, seleccione la acción **Descuentos en factura**. Aparecerá la página **Descuentos en factura al cliente**.
2. En el campo **Código divisa**, introduzca el código de una divisa que se aplique a los términos de descuento en factura en la línea. Deje el campo en blanco para establecer condiciones de descuento de factura en la divisa local.
3. En el campo **Importe mínimo**, escriba el importe mínimo que deba tener una factura para optar al descuento.
4. En el campo **% descuento**, introduzca el descuento en la factura como un porcentaje del importe de la factura.
5. Repita los pasos del 5 al 7 para cada divisa que el cliente reciba un descuento diferente de factura.

El descuento en factura ahora está configurado y asignado al cliente en cuestión. Al seleccionar el código del cliente en el campo **Cód. dto. factura** en otras fichas de cliente, se asigna el mismo descuento en factura a estos clientes.

## <a name="to-copy-sales-prices"></a>Para copiar precios de venta

Estos pasos difieren, dependiendo de si su administrador ha activado la actualiación de la característica **Nueva experiencia de precios de venta**. 

#### [Experiencia actual](#tab/current-experience/)  

Si desea copiar precios de venta, por ejemplo, los precios de venta de un cliente determinado a un grupo de precios de clientes, debe ejecutar el proceso **Sugerir precio venta en hoja**. en la página **Hoja de precios de venta**.  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Hoja de precios de venta** y luego elija el enlace relacionado.  
2. Elija **Sugerir precio venta en hoja**. .  
3. En la ficha desplegable **Precios venta**, rellene los campos **Tipo venta** y **Código ventas** con los precios de venta originales que desea copiar.  
4. En la parte superior de la página de solicitud, rellene los campos **Tipo venta** y **Código ventas** con el tipo y el nombre al que desea copiar los precios de venta.  
5. Si desea que el trabajo por lotes cree precios nuevos, seleccione la casilla **Crear precios nuevos**.  
6. Elija el botón **Aceptar** para rellenar las líneas de la página **Hoja precios venta** con los nuevos precios propuestos, indicando que son válidos para el tipo de venta seleccionado.  

   > [!NOTE]  
   > El proceso sólo crea propuestas; no implementa los cambios propuestos. Si está satisfecho con las propuestas y desea implementarlas, es decir, insertarlas en la página **Precios de venta**, elija la acción **Implementar cambios de precios** en la página **Hoja de precios de venta**.

#### [Nueva experiencia](#tab/new-experience/)  

El estado de la lista de precios debe ser **Borrador**. 

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Listas de precios de venta** y luego elija el enlace relacionado. 
2. Elija la lista de precios a copiar y luego elija **Copiar líneas**.
3. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

   > [!NOTE]
   > No puede tener dos líneas que tengan la misma configuración pero diferentes precios. Si eso sucede, aparecerá un mensaje cuando active una lista de precios. Puede elegir el precio a utilizar abriendo la lista y eliminando el precio incorrecto.  
  
---

## <a name="to-bulk-update-item-prices"></a>Para actualizar de forma masiva los precios de los artículos

Estos pasos difieren, dependiendo de si su administrador ha activado la actualiación de la característica **Nueva experiencia de precios de venta**. 

#### [Experiencia actual](#tab/current-experience/)

Si desea actualizar de forma masiva los precios de los artículos, como aumentar todos los precios de los artículos en algún porcentaje, debe ejecutar el proceso **Sugerir precio producto en hoja**. Trabajo por lotes . Puede encontrar un enlace al proceso en la página **Hoja precios venta**.  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Hoja de precios de venta** y luego elija el enlace relacionado.  
2. Elija **Sugerir precio producto en hoja**. .  
3. En la ficha desplegable **Artículo**, rellene los campos **N.º** o **Grupo registro inventario** u otros con los precios del artículo original que desea actualizar.  
4. En la parte superior de la página de solicitud, rellene el **Tipo venta** y **Código ventas** con el tipo y el nombre al que desea copiar los precios de venta.
5. Si desea que el proceso ajuste automáticamente los precios de los artículos sugeridos, introduzca el ajuste en el campo **Factor de ajuste**. Por ejemplo, debe introducir 1,15 en **Factor de ajuste** para un aumento del 15% en el precio del artículo.  
6. Si desea que el trabajo por lotes cree precios nuevos, seleccione el campo **Crear precios nuevos**.  
7. Elija el botón **Aceptar** para rellenar las líneas de la página **Hoja precios venta** con los nuevos precios propuestos, indicando que son válidos para el **Artículo** seleccionado.  

> [!NOTE]
> El proceso sólo crea propuestas; no implementa los cambios propuestos. Si está satisfecho con las propuestas y desea implantarlas, es decir, insertarlas en la tabla **Precios de venta**, puede utilizar el trabajo por lotes **Realizar cambio precio**, que se encuentra en la pestaña **Acciones**, en el grupo **Funciones**, en la página **Hoja de precios de venta**.

#### [Nueva experiencia](#tab/new-experience/)

Para actualizar los precios de varios productos, debe crear una nueva lista de precios y luego copiar las líneas desde una lista de precios existente. Cuando copie las líneas, puede usar filtros para especificar qué copiar, y puede especificar un número entero o decimal en el campo **Factor de ajuste** para aumentar o disminuir los precios. El estado de la lista de precios debe estar en estado **Borrador**. Si es necesario, puede desactivar la lista de precios anterior.

> [!NOTE]
> No puede tener dos líneas que tengan la misma configuración pero diferentes precios. Si eso sucede, aparecerá un mensaje cuando active una lista de precios. Puede elegir el precio a utilizar abriendo la lista y eliminando el precio incorrecto.  

---

## <a name="calculating-the-best-price"></a>Cálculo del mejor precio

Cuando haya registrado precios especiales y descuentos de línea para ventas y compras, [!INCLUDE[d365fin](includes/d365fin_md.md)] garantiza que el beneficio en operaciones comerciales de producto siempre sea óptimo, calculando automáticamente el mejor precio en los documentos de ventas y compras, y en líneas del diario de proyectos y productos. Para obtener más información, consulte [Cálculo del mejor precio](sales-how-record-sales-price-discount-payment-agreements.md#best-price-calculation).

## <a name="see-related-microsoft-training"></a>Consultar la [formación de Microsoft](/training/modules/customer-discounts-dynamics-365-business-central/) relacionada

## <a name="see-also"></a>Consulte también .

[Configuración de ventas](sales-setup-sales.md)  
[Ccial](sales-manage-sales.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
