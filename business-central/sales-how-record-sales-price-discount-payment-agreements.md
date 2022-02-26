---
title: Configurar precios y descuentos de venta para clientes | Microsoft Docs
description: Describe cómo configurar y aplicar acuerdos de precios y descuentos para documentos de ventas.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: special price, alternate price, pricing
ms.search.form: 1345, 7002, 7007, 7015, 7016, 7023
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 5d03e3c567ed6a2932691cee58685e522814a03f
ms.sourcegitcommit: a6000804ad9a176de5750372d3951547ddb71006
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/25/2021
ms.locfileid: "7865551"
---
# <a name="record-sales-prices-and-discounts"></a>Registrar precios y descuentos de ventas
> [!NOTE]
> En el segundo lanzamiento de versiones de 2020, lanzamos procesos optimizados para configurar y administrar precios y descuentos. Si es un cliente nuevo que usa esa versión, está usando la nueva experiencia. Si es un cliente existente, si está utilizando o no la nueva experiencia depende de si su administrador ha habilitado la actualización de funciones **Nueva experiencia de precios de venta** en **Administración de características**. Para más información, consulte [Habilitación de las próximas funciones antes de tiempo](/dynamics365/business-central/dev-itpro/administration/feature-management).

[!INCLUDE[prod_short](includes/prod_short.md)] admite varias estrategias de precios, que van desde modelos de precio único para todos en los que un artículo siempre se vende al mismo precio, hasta acuerdos de precios especiales con clientes específicos, grupos de clientes u ofertas especiales cuando está ejecutando una campaña de ventas. Por ejemplo, puede ofrecer un precio especial en un pedido de cliente en las siguientes condiciones:

* Cuando es por una cantidad mínima
* Es para cierto tipo de artículo  
* Si se crea durante un período de tiempo específico

Para utilizar un modelo de precios básico, solo necesita especificar un precio unitario para un artículo o recurso. Ese precio siempre se utilizará en los documentos de venta. Para modelos más avanzados, por ejemplo, cuando está ejecutando una campaña de ventas y desea ofrecer precios especiales, puede especificar criterios para eso en la página **Precios de venta**. Puede ofrecer precios especiales basados en combinaciones de lo siguiente: 

* Cliente
* Producto
* Unidad de medida
* Cantidad mínima
* Rangos de fechas que definen cuando los precios son válidos

Además, después de configurar precios especiales, [!INCLUDE[prod_short](includes/prod_short.md)] puede calcular automáticamente el mejor precio en documentos de compra y venta y en líneas de diario de trabajos y artículos. Para obtener más información, vea [Cálculo del mejor precio](sales-how-record-sales-price-discount-payment-agreements.md#best-price-calculation).  

Para los descuentos de ventas, puede configurar y usar los siguientes tipos:

| Tipo de descuento | Descripción |
| --- | --- |
| **Descuento línea venta** |Un importe que se usa en las líneas de venta si existe una cierta combinación de cliente, producto, cantidad mínima, unidad de medida o fecha de inicio o de fin. Estas combinaciones funcionan igual que para los precios de venta. |
| **Descuento en factura** |Un porcentaje de descuento que se resta del total del documento de venta si la suma de todas las líneas del documento supera cierto límite. |

> [!TIP]  
> Si nunca debe venderse un producto con descuento, simplemente deje vacíos los campos de descuento en la ficha del producto y no incluya el producto en ninguna configuración de descuento de línea.

## <a name="to-set-up-a-sales-price-for-a-customer"></a>Para configurar un precio de venta para un cliente

Estos pasos difieren, dependiendo de si su administrador ha activado la actualización de la característica **Nueva experiencia de precios de venta**. Si la actualización de funciones no está activada, siga los pasos de la pestaña Experiencia actual. 

## <a name="current-experience"></a>[Experiencia actual](#tab/current-experience)

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Clientes** y luego elija el enlace relacionado.
2. Elija el cliente y, a continuación, elija la acción **Precios**.
3. Rellene los campos de la línea como sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Rellene una línea para cada combinación que aplicará un precio de venta especial al cliente.

## <a name="new-experience"></a>[Nueva experiencia](#tab/new-experience)  
De forma predeterminada, el estado de las nuevas listas de precios es Borrador. Las listas de precios preliminares no se incluyen en los cálculos de precios. Cuando haya terminado de agregar líneas y desee estar usando los precios, puede cambiar el estado a Activo.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Clientes** y luego elija el enlace relacionado.
2. Elija el cliente y, a continuación, elija la acción **Listas de precios de venta**. 
3. Para crear una nueva lista de precios, elija **Nueva**.
4. En las fichas desplegables **General** e **Impuesto**, rellene los campos como sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
5. Los productos se pueden agregar a la lista de varias formas:
   * Para agregar muchos elementos, elija **Sugerir líneas** y luego introduzca los criterios de filtro para especificar los tipos de productos que se agregarán. Opcionalmente, puede ingresar otras configuraciones para los elementos. Estos ajustes son específicos de la lista de precios. Puede cambiarlos más tarde si lo necesita.
   * Para copiar productos de otra lista de precios, elija **Copiar líneas** y luego elija la lista de precios a copiar.
   * Para agregar elementos manualmente, en el campo **Tipo de producto** en una línea, elija el tipo de producto para el que es la lista de precios. Dependiendo de la selección, rellene los campos restantes según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. Para empezar a utilizar la lista de precios, en el campo **Estado**, elija **Activo**.  

---

## <a name="using-sales-and-purchase-price-lists"></a>Uso de listas de precios de compra y venta
> [!NOTE]
> El uso de listas de precios requiere que su administrador haya habilitado la actualización de función **Nueva experiencia de precios de venta** en **Gestión de funciones**. Para más información, consulte [Habilitación de las próximas funciones antes de tiempo](/dynamics365/business-central/dev-itpro/administration/feature-management).

Los campos **Se aplica al tipo** y **Se aplica al N.º** le permiten elegir a qué se aplicará una lista de precios, como el cliente o el grupo de precios del cliente. Use el campo **Ver columnas para**, para mostrar columnas relevantes solo para precios, descuentos o precios y descuentos.

### <a name="converting-existing-prices-when-you-turn-on-the-pricing-feature-update"></a>Conversión de precios existentes al activar la actualización de la función de precios
Cuando habilita la actualización de funciones **Nueva experiencia de precios de venta** en la página **Gestión de funciones**, se abre la guía **Actualización de datos de funciones**. Use la opción **Usar precios predeterminados** de la siguiente manera:

* Si desea trabajar con todos los precios en una sola página, actívela. Los precios existentes se convierten en una lista de precios predeterminada para cada uno de los siguientes:

    * Ccial
    * Compras
    * Venta de proyectos
    * Compras de proyecto 

    Posteriormente, puede editar todos los precios de estas áreas en la página **Hoja de trabajo de precios**. Las listas de precios predeterminadas se establecen en las páginas **Configuración de ventas y cuentas por cobrar**, **Configuración de compras y cuentas a pagar** y **Configuración de trabajos**. 

    > [!NOTE]
    > Si los precios se establecen solo en tarjetas de artículos o recursos, las listas de precios predeterminadas no se completarán con esos precios durante la actualización de datos. Sin embargo, puede abrir cualquiera de las listas de precios predeterminadas o la página Hoja de trabajo de precios y usar la acción **Sugerir líneas** para agregar los precios establecidos en las tarjetas de artículos o recursos. 

* Para usar listas de precios de venta, desactívelo. Los precios existentes se convertirán en una nueva lista de precios para cada combinación de cliente, grupo de clientes o campaña y las fechas y monedas de inicio y finalización. Si tiene muchas combinaciones, tendrá muchas listas de precios.

Si ya ha habilitado la Nueva experiencia de precios, puede crear listas de precios predeterminadas manualmente o especificar una lista de precios existente como predeterminada. Para establecer una lista de precios existente como predeterminada, active la opción **Permitir actualizar valores predeterminados** en la lista de precios. Entonces, en las páginas **Configuración de ventas y cuentas por cobrar**, **Compras y cuentas a pagar** y **Configuración de trabajos** establezca la lista de precios como predeterminada.

## <a name="editing-active-price-lists"></a>Editar listas de precio activo
Para permitir que las personas editen precios en listas de precios activas para artículos, recursos, clientes, proveedores u otras entidades que usan precios, active la opción **Permitir editar precio activo** en las páginas **Configuración de ventas y cuentas por cobrar** y **Configuración de compras y pagos**. 

Cuando la opción **Permitir editar precio activo** está desactivada, para actualizar los precios en una lista de precios debe cambiar el estado de la lista de precios a **Borrador**, realice su cambio y luego reactive la lista de precios.

La página **Resumen de precios** proporciona una descripción general de todos los precios en las listas de precios. Puede configurar filtros para reducir la lista. Después de cambiar los precios, debe utilizar la acción **Verificar líneas** acción para verificar los precios con otras líneas de lista de precios. Por ejemplo, verificar los precios ayuda a evitar precios duplicados o conflictivos. 

> [!NOTE]
> Cuando edita una línea en una lista de precios activa, el estado de la línea se convierte en Borrador y la línea no se incluirá en los cálculos de precios hasta que use la acción **Verificar líneas**. Después de verificar el precio, el estado de la línea pasa a ser Activo y se utilizará en los cálculos de precios.

Para agregar nuevos precios, en la página **Resumen de precios**, utilice la acción **Agregar nuevas líneas**. La página **Hoja de trabajo de precios** se abre, donde agrega líneas de precios de las siguientes maneras:

* Sugiriéndolos basado en criterios
* Copiarlos de otras listas de precios
* Introducirlos manualmente. 

Posteriormente, puede utilizar la acción **Implementar cambio de precio** para comparar los nuevos precios con otras listas de precios para evitar duplicados.

## <a name="to-copy-sales-prices"></a>Para copiar precios de venta
Estos pasos difieren, dependiendo de si su administrador ha activado la actualización de la característica **Nueva experiencia de precios de venta**. Si la actualización de funciones no está activada, siga los pasos de la pestaña Experiencia actual.

## <a name="current-experience"></a>[Experiencia actual](#tab/current-experience)  

Si desea copiar precios de venta, por ejemplo, los precios de venta de un cliente determinado a un grupo de precios de clientes, debe ejecutar el proceso **Sugerir precio venta en hoja**. en la página **Hoja de precios de venta**.  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Hoja de precios de venta** y luego elija el enlace relacionado.  
2. Elija **Sugerir precio venta en hoja**. .  
3. En la ficha desplegable **Precios venta**, rellene los campos **Tipo venta** y **Código ventas** con los precios de venta originales que desea copiar.  
4. En la parte superior de la página de solicitud, rellene los campos **Tipo venta** y **Código ventas** con el tipo y el nombre al que desea copiar los precios de venta.  
5. Si desea que el trabajo por lotes cree precios nuevos, seleccione la casilla **Crear precios nuevos**.  
6. Elija el botón **Aceptar** para rellenar las líneas de la página **Hoja precios venta** con los nuevos precios propuestos, indicando que son válidos para el tipo de venta seleccionado.  

   > [!NOTE]  
   > El proceso sólo crea propuestas; no implementa los cambios propuestos. Si está satisfecho con las propuestas y desea implementarlas, es decir, insertarlas en la página **Precios de venta**, elija la acción **Implementar cambios de precios** en la página **Hoja de precios de venta**.

## <a name="new-experience"></a>[Nueva experiencia](#tab/new-experience)  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Listas de precios de venta** y luego elija el enlace relacionado. 
2. Elija la lista de precios a copiar y luego elija **Copiar líneas**.
3. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

   > [!NOTE]
   > No puede tener dos líneas que tengan la misma configuración pero diferentes precios. Si eso sucede, aparecerá un mensaje cuando active una lista de precios. Puede elegir el precio a utilizar abriendo la lista y eliminando el precio incorrecto.  
  
---

## <a name="to-bulk-update-item-prices"></a>Para actualizar de forma masiva los precios de los artículos
Estos pasos difieren, dependiendo de si su administrador ha activado la actualización de la característica **Nueva experiencia de precios de venta**. Si la actualización de funciones no está activada, siga los pasos de la pestaña Experiencia actual.

### <a name="current-experience"></a>[Experiencia actual](#tab/current-experience)

Si desea actualizar de forma masiva los precios de los artículos, como aumentar todos los precios de los artículos en algún porcentaje, puede rellenar la **Hoja de trabajo precios de venta** usando los siguientes trabajos por lotes:

* **Sugerir precio producto en hoja.** sugiere cambios aplicando un factor de ajuste a los precios de venta existentes o copiando los acuerdos de precios de venta existentes a otros clientes, grupos de precios de clientes o campañas de ventas.
* **Sugerir precio producto en hoja.** sugiere cambios aplicando un factor de ajuste a los precios unitarios existentes en las tarjetas de artículos, o sugiriendo precios para nuevas combinaciones de moneda, unidades de medida, etc. Los precios unitarios de los artículos no se modifican.    

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Hoja de precios de venta** y luego elija el enlace relacionado.  
2. Elija **Sugerir precio producto en hoja**. .  
3. En la ficha desplegable **Artículo**, rellene los campos **N.º** o **Grupo registro inventario** u otros con los precios del artículo original que desea actualizar.  
4. En la parte superior de la página de solicitud, rellene el **Tipo venta** y **Código ventas** con el tipo y el nombre al que desea copiar los precios de venta.
5. Si desea que el proceso ajuste automáticamente los precios de los artículos sugeridos, introduzca el ajuste en el campo **Factor de ajuste**. Por ejemplo, debe introducir **1,15** en **Factor de ajuste** para un aumento del **15 %** en el precio del artículo.  
6. Si desea que el trabajo por lotes cree precios nuevos, active la opción **Crear precios nuevos**.  
7. Escoja **Aceptar** para completar las líneas en la página **Hoja de trabajo de precio de venta** con los nuevos precios sugeridos.
8. Para implementar las sugerencias, utilice la acción **Implementar cambios de precio**. El trabajo por lotes crea sugerencias pero no las implementa.

## <a name="new-experience"></a>[Nueva experiencia](#tab/new-experience)

Para actualizar los precios de varios productos, debe crear una nueva lista de precios y luego copiar las líneas desde una lista de precios existente. Cuando copie las líneas, puede usar filtros para especificar qué copiar, y puede especificar un número entero o decimal en el campo **Factor de ajuste** para aumentar o disminuir los precios. El estado de la lista de precios debe estar en estado **Borrador**. Si es necesario, puede desactivar la lista de precios anterior.

> [!NOTE]
> No puede tener dos líneas que tengan la misma configuración pero diferentes precios. Si eso sucede, aparecerá un mensaje cuando active una lista de precios. Puede elegir el precio a utilizar abriendo la lista y eliminando el precio incorrecto.  

---

## <a name="sales-invoice-discounts-and-service-charges"></a>Descuentos en factura de ventas y cargos por servicios
Al utilizar descuentos en factura, el importe total de la factura determina el tamaño del descuento aplicado. En la página **Dtos. factura clientes**, también puede añadir un cargo por servicio a las facturas que superen un determinado importe.  

Si desea descuentos en factura para que se calculen automáticamente, en la página **Configuración ventas y cobros** active el conmutador **Calcular descuento inventario**.  

Para cada cliente, puede especificar si ofrecerá descuentos en la factura si se cumplen los criterios. Por ejemplo, si el monto de la factura es lo suficientemente grande. Defina los términos de los descuentos en factura en divisa local para los clientes nacionales y en otras divisas para los clientes de otros países.  

Se relacionan los porcentajes de descuento a los importes de factura específicos en la página **Dtos. factura cliente** para cada cilente. Puede introducir un número ilimitado de porcentajes. Cada cliente puede tener su propia página o se pueden vincular varios clientes a la misma página.  

Además de, o en lugar de, un porcentaje de descuento, puede vincular un importe de cargo por servicios a un importe facturado específico.  

Para formación sobre descuentos en ventas, consulte [Establecer descuentos para sus clientes](/learn/modules/customer-discounts-dynamics-365-business-central/index) en Microsoft Learn.  

### <a name="calculating-invoice-discounts-on-sales"></a>Calcular descuentos en factura para ventas

[!INCLUDE [sales-invoice-discounts](includes/sales-invoice-discounts.md)]

## <a name="to-set-up-a-sales-line-discount-for-a-customer"></a>Para configurar un descuento de línea de venta para un cliente
Estos pasos difieren, dependiendo de si su administrador ha activado la actualización de la característica **Nueva experiencia de precios de venta**. Si la actualización de funciones no está activada, siga los pasos de la pestaña Experiencia actual.

## <a name="current-experience"></a>[Experiencia actual](#tab/current-experience)  

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Clientes** y luego elija el enlace relacionado.
2. Abra la ficha de cliente correspondiente y, a continuación, elija la acción **Descuentos de línea**.
3. Rellene los campos de la línea como sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Rellene una línea para cada combinación que aplicará un descuento de línea de venta al cliente.

> [!Note]
> Cuando abra las páginas **Precios de venta** y **Descuentos de línea de ventas** de un cliente específico, los campos **Filtro de tipo de ventas** y **Filtro de código de ventas** se establecen para el cliente y no se pueden cambiar ni eliminar.
>
> Para configurar precios o descuentos de línea para todos los clientes, un grupo de precios de clientes o una campaña, debe abrir las páginas desde una tarjeta de producto. Alternativamente, para precios de venta, use la página **Hoja de trabajo de precio de venta**. Para obtener más información, vea [Para actualizar de forma masiva los precios de los productos](sales-how-record-sales-price-discount-payment-agreements.md#to-bulk-update-item-prices).  

## <a name="new-experience"></a>[Nueva experiencia](#tab/new-experience)  

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Clientes** y luego elija el enlace relacionado.
2. Elija el cliente y, a continuación, elija la acción **Listas de precios de venta**.
3. Abra la lista de precios para la que desea especificar el descuento de línea.
4. Cree una nueva línea o elija una existente y luego complete los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
5. En el campo **Define**, elija ya sea **Precio y descuento**, o solo **Descuento**. 
6. En el campo **% de descuento de línea**, especifique el porcentaje de descuento.

   > [!TIP]
   > Puede filtrar las líneas eligiendo la opción adecuada en el campo **Ver columnas para**.   
  
   > [!NOTE]
   > Los códigos de descuento en factura se representan por las fichas existentes del cliente. Usar nombres de clientes como códigos le permite asignar rápidamente las condiciones de descuento en factura a clientes realizando el picking del nombre de otros clientes con los mismos términos. Para configurar términos de descuento de factura específicos del cliente, configure el campo **Código des. factura** con el código de cliente y luego continúe con el siguiente paso.

---

## <a name="to-set-up-an-invoice-discount-for-a-customer"></a>Para configurar un descuento en factura para un cliente
Una vez que haya determinado los clientes que pueden obtener descuentos en factura, introduzca el código de descuento en factura en las fichas de cliente y especifique los términos de cada código.

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Clientes** y luego elija el enlace relacionado.
2. Abra la página de cliente para un cliente que pueda obtener descuentos en factura.
3. En el campo **Código descuento factura**, seleccione un código para los términos relevantes de la factura con descuentos que usará para calcular los descuentos en facturas para el cliente. 

> [!NOTE]  
> Los códigos de descuento en factura se representan por las fichas existentes del cliente. Usar nombres de clientes como códigos le permite asignar rápidamente las condiciones de descuento en factura a clientes realizando el picking del nombre de otros clientes con los mismos términos.

Ahora configure de nuevo los términos de descuento en factura de ventas.

1. En la página **Clientes**, seleccione la acción **Descuentos en factura**. Aparecerá la página **Descuentos en factura al cliente**.
2. En el campo **Código divisa**, introduzca el código de una divisa que se aplique a los términos de descuento en factura en la línea. Deje el campo en blanco para establecer condiciones de descuento de factura en la divisa local.
3. En el campo **Importe mínimo**, escriba el importe mínimo que deba tener una factura para optar al descuento.
4. En el campo **% descuento**, introduzca el descuento en la factura como un porcentaje del importe de la factura.
5. Repita los pasos del 5 al 7 para cada divisa que el cliente reciba un descuento diferente de factura.

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