---
title: Registrar precios y descuentos de ventas especiales
description: Describe cómo definir acuerdos de precios y descuentos para documentos de ventas.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: ivkoleti
ms.topic: how-to
ms.date: 06/13/2023
ms.custom: bap-template
ms.search.keywords: 'special price, alternate price, pricing'
ms.search.form: '7022, 7024'
---

# <a name="record-special-sales-prices-and-discounts"></a>Registrar precios y descuentos de ventas especiales

> [!NOTE]
> El segundo lanzamiento de versiones de 2020 introdujo nuevos procesos optimizados para configurar y administrar precios y descuentos. Si es un cliente nuevo que usa la última versión, está usando la nueva experiencia. Si es un cliente existente, si está utilizando o no la nueva experiencia depende de si su administrador ha habilitado la actualización de funciones **Nueva experiencia de precios de venta** en **Administración de características**. Obtenga más información en [Habilitar las próximas funciones de antemano](/dynamics365/business-central/dev-itpro/administration/feature-management), en el contenido de la administración.

[!INCLUDE[prod_short](includes/prod_short.md)] admite varias estrategias de precios, tales como:

* Modelos de precio único para todos en los que un artículo siempre se vende al mismo precio.
* Acuerdos de precios especiales con clientes específicos, o grupos de clientes.
* Campañas cuando una venta cumple los criterios para una oferta especial. Por ejemplo, puede tener los siguientes criterios para un pedido:

  * Cumple una cantidad mínima
  * Es antes de cierta fecha
  * Incluye un determinado tipo de artículo  

Para utilizar un modelo de precios básico, solo necesita especificar un precio unitario cuando configura un artículo o recurso. Ese precio siempre se utilizará en los documentos de venta. Para modelos más avanzados, por ejemplo, cuando está ejecutando una campaña de ventas y desea ofrecer precios especiales, puede especificar criterios para eso en la página **Precios de venta**. Puede ofrecer precios especiales basados una combinación de la información siguiente:  

* Cliente
* Producto
* Unidad de medida
* Cantidad mínima
* Fechas que definen el período de validez de los precios.

Después de configurar precios especiales, [!INCLUDE[prod_short](includes/prod_short.md)] puede calcular los mejores precios en documentos de compra y venta y en líneas de diarios de trabajos y artículos. Obtenga más información en [Cálculo del mejor precio](sales-how-record-sales-price-discount-payment-agreements.md#best-price-calculation).

Puede configurar dos tipos de descuentos para ofertas:

| Tipo de descuento | Descripción |
| --- | --- |
| **Descuento línea venta** |Agregue un importe en las líneas de venta que tengan una cierta combinación de cliente, producto, cantidad mínima, unidad de medida o fecha de inicio o de fin. Este tipo funciona igual que para los precios de venta. |
| **Descuento en factura** |Un porcentaje de descuento que se resta del total del documento de venta si la suma de todas las líneas del documento supera cierto límite. |

> [!TIP]  
> Si nunca debe venderse un producto con descuento, simplemente deje vacíos los campos de descuento en la ficha del producto y no incluya el producto en ninguna configuración de descuento de línea.

## <a name="to-set-up-a-sales-price-for-a-customer"></a>Para configurar un precio de venta para un cliente

Estos pasos difieren, dependiendo de si su administrador ha activado la actualización de la característica **Nueva experiencia de precios de venta**. Si la actualización de funciones no está activada, siga los pasos de la pestaña Experiencia actual. 

#### [Experiencia actual](#tab/current-experience/)

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Clientes** y luego elija el enlace relacionado.
2. Elija el cliente y, a continuación, elija la acción **Precios**.
3. Rellene los campos de la línea como sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Rellene una línea para cada combinación que aplicará un precio de venta especial al cliente.

#### [Nueva experiencia](#tab/new-experience/)  

De forma predeterminada, el estado de las nuevas listas de precios es **Borrador**. Las listas de precios preliminares no se incluyen en los cálculos de precios. Cuando haya terminado de agregar líneas y desee empezar a usar los precios, puede cambiar el estado a **Activo**.

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Clientes** y luego elija el enlace relacionado.
2. Elija el cliente y, a continuación, elija la acción **Listas de precios de venta**. 
3. Para crear una nueva lista de precios, elija **Nueva**.
4. En las fichas desplegables **General** e **Impuesto**, rellene los campos como sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
5. Para agregar elementos a la lista, realice uno de los siguientes pasos:
   * Para agregar muchos elementos, elija **Sugerir líneas** y luego introduzca los criterios de filtro para especificar los tipos de productos que se agregarán. Opcionalmente, puede introducir otras configuraciones para los productos específicos de la lista de precios. Puede cambiarla las configuraciones más adelante, si lo necesita.
   * Para copiar productos de otra lista de precios, elija **Copiar líneas** y luego elija la lista de precios a copiar.
   * Para agregar elementos manualmente, en la cuadrícula, en el campo **Tipo de producto**, elija el tipo de producto para el que es la lista de precios. Dependiendo de la selección, rellene los campos restantes según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. Para empezar a utilizar la lista de precios, en el campo **Estado**, elija **Activo**.  

---

## <a name="using-sales-and-purchase-price-lists"></a>Uso de listas de precios de compra y venta

> [!NOTE]
> El uso de listas de precios requiere que su administrador haya habilitado la actualización de función **Nueva experiencia de precios de venta** en **Gestión de funciones**. Obtenga más información en [Habilitar las próximas funciones de antemano](/dynamics365/business-central/dev-itpro/administration/feature-management), en el contenido de la administración.

La mayor parte de la nueva experiencia de precios de venta es similar a la experiencia actual, pero hay algunas diferencias. Estas diferencias se describen en las siguientes secciones.

Los campos **Se aplica al tipo** y **Se aplica al N.º** le permiten elegir a qué se aplicará una lista de precios, como el cliente o el grupo de precios del cliente. Usando **Ver columnas para**, puede mostrar u ocultar columnas relevantes para establecer precios, descuentos o precios y descuentos.

### <a name="converting-existing-prices-when-you-turn-on-the-pricing-feature-update"></a>Conversión de precios ya existentes al activar la actualización de la función de precios

Cuando habilita la actualización de funciones **Nueva experiencia de precios de venta** en la página **Gestión de funciones**, se abre la guía **Actualización de datos de funciones**. Use la opción **Usar precios predeterminados** de la siguiente manera:

* Si desea trabajar con todos los precios en una sola página, actívela. Los precios existentes se convertirán en una lista de precios predeterminada para cada uno de los siguientes documentos:

  * Ccial
  * Compras
  * Venta de proyectos
  * Compras de proyecto

  Puede editar todos los precios de estas áreas en la página **Hoja de trabajo de precios**. Las listas de precios predeterminadas se establecen en las páginas **Configuración de ventas y cobros**, **Configuración de compras y pagos** y **Configuración de proyectos**.

> [!NOTE]
> Si los precios se establecen solo en fichas de productos o recursos, las listas de precios predeterminadas no se rellenarán con esos precios durante la actualización de datos. Sin embargo, puede abrir cualquiera de las listas de precios predeterminadas o la página **Hoja de precios de venta** y usar la acción **Sugerir líneas** para agregar los precios establecidos en las fichas de productos o recursos.

* Para usar listas de precios de venta, desactívelo. Los precios existentes se convertirán a una nueva lista de precios para cada combinación de las siguientes cosas:

  * Cliente
  * Grupo de clientes o campaña
  * Fechas de inicio y finalización
  * Divisas

Si tiene muchas combinaciones, tendrá muchas listas de precios.

Si ya ha habilitado la Nueva experiencia de precios, puede crear listas de precios predeterminadas manualmente o especificar una lista de precios existente como predeterminada. Para establecer una lista de precios existente como predeterminada, active la opción **Permitir actualizar valores predeterminados** en la lista de precios. A continuación, en las páginas **Configuración de ventas y cobros**, **Compras y pagos** y **Configuración de proyectos** establezca la lista de precios como predeterminada.

### <a name="editing-active-price-lists"></a>Editar listas de precios activas

Para permitir que las personas editen precios en listas de precios activas para artículos, recursos, clientes, proveedores u otras entidades que usan precios, active la opción **Permitir editar precio activo** en las páginas **Configuración de ventas y cuentas por cobrar** y **Configuración de compras y pagos**.

Cuando la opción **Permitir editar precio activo** está desactivada, para actualizar los precios en una lista de precios debe cambiar el estado de la lista de precios a **Borrador**, realice su cambio y luego reactive la lista de precios.

La página **Resumen de precios** proporciona una descripción general de todos los precios en las listas de precios. Puede establecer filtros para reducir la lista de precios que desee modificar o agregar. Después de modificar los precios, debe utilizar la acción **Verificar líneas** acción para verificar los precios con otras líneas de lista de precios. La verificación de precios ayuda a evitar duplicados y ambigüedades durante el cálculo de precios.

> [!NOTE]
> Cuando edita una línea en una lista de precios activa, el estado de la línea pasa a **Borrador** y la línea no se tendrá en cuenta durante los cálculos de precios hasta que use la acción **Comprobar líneas**. Después de verificar el precio, el estado de la línea pasa a ser **Activo** y se tendrá en cuenta al calcular los precios.

Para agregar nuevos precios, en la página **Resumen de precios**, utilice la acción **Agregar nuevas líneas**. La página **Hoja de cálculo de precios** se abre y puede agregar líneas de precios sugiriéndolas en función de los criterios, copiándolas de otras listas de precios o introduciéndolas manualmente. Posteriormente, puede utilizar la acción **Implementar cambio de precio** para comparar los nuevos precios con otras listas de precios para evitar duplicados y ambigüedades durante el cálculo de precios.

#### <a name="create-sales-price-lines-based-on-the-unit-price"></a>Crear líneas de precios de venta basadas en el precio unitario

1. En la página **Hoja de trabajo de precios**, elija la acción **Proponer líneas**.
2. En la página **Líneas de precio: crear nuevas**, rellene los campos según sus necesidades. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. En el campo **Filtro de productos**, defina filtros para el **Tipo de producto** seleccionado.
4. Elija el campo **Valores predeterminados** para especificar configuraciones como:
   * A qué entidades se asignará la lista de precios.
   * Fechas en las que el precio es válido.
   * El código de divisa.
   * El filtro de tipo de importe que define las columnas que se muestran en las líneas de lista de precios.
5. Elija **Aceptar**. Se agregarán más líneas a la página **Hoja de precios** con la configuración seleccionada y los precios unitarios de las fichas de productos.
6. Edite las líneas creadas con los nuevos precios unitarios o descuentos. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

#### <a name="create-sales-price-lines-based-on-existing-price-lists"></a>Crear líneas de precios de venta basadas en listas de precios ya existentes

1. En la página **Hoja de trabajo de precios**, elija la acción **Copiar líneas**.
2. En la página **Líneas de precio: copiar existente**, seleccione una lista de precios ya existente en el campo **De lista de precios**.
3. En el campo **Filtro de línea de precios**, defina filtros para los productos de la lista de precios seleccionada.
4. Elija el campo **Valores predeterminados** para especificar configuraciones como:
   * A qué entidades se asignará la lista de precios.
   * Fechas en las que el precio es válido.
   * El código de divisa.
   * El filtro de tipo de importe que define las columnas que se muestran en las líneas de lista de precios.
5. Rellene los demás campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. Elija **Aceptar**. Se agregarán líneas nuevas a la página **Hoja de precios** con la configuración seleccionada.
7. Edite las líneas creadas con los nuevos precios unitarios o descuentos. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-copy-sales-prices"></a>Para copiar precios de venta

Estos pasos difieren, dependiendo de si su administrador ha activado la actualización de la característica **Nueva experiencia de precios de venta**. Si la actualización de funciones no está activada, siga los pasos de la pestaña Experiencia actual.

#### [Experiencia actual](#tab/current-experience/)  

Si desea copiar precios de venta, por ejemplo, los precios de venta de un cliente determinado a un grupo de precios de clientes, debe ejecutar el proceso **Sugerir precio venta en hoja**. en la página **Hoja de precios de venta**.  

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Hoja de precios de venta** y luego elija el enlace relacionado.  
2. Elija **Sugerir precio venta en hoja**. .  
3. En la ficha desplegable **Precios venta**, rellene los campos **Tipo venta** y **Código ventas** con los precios de venta originales que desea copiar.  
4. En la parte superior de la página de solicitud, rellene los campos **Tipo venta** y **Código ventas** con el tipo y el nombre al que desea copiar los precios de venta.  
5. Si desea que el trabajo por lotes cree precios nuevos, seleccione la casilla **Crear precios nuevos**.  
6. Elija el botón **Aceptar** para rellenar las líneas de la página **Hoja precios venta** con los nuevos precios propuestos, indicando que son válidos para el tipo de venta seleccionado.  

   > [!NOTE]  
   > El proceso sólo crea propuestas; no implementa los cambios propuestos. Si está satisfecho con las propuestas y desea implementarlas, es decir, insertarlas en la página **Precios de venta**, elija la acción **Implementar cambios de precios** en la página **Hoja de precios de venta**.

#### [Nueva experiencia](#tab/new-experience/)  

Puede especificar la configuración que utilizará la lista de precios:

* Utilice la configuración del encabezado de la lista que está copiando.
* Utilice la configuración de la lista a la que está copiando. Para usar la configuración de la lista de precios a la que está copiando los precios, active la alternancia **Usar valores predeterminados desde destino**.

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Listas de precios de venta** y luego elija el enlace relacionado.
2. Elija la lista de precios a copiar y luego elija **Copiar líneas**.
3. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

   > [!NOTE]
   > No puedes tener dos artículos que tengan la misma configuración pero diferentes precios. Si eso sucede, aparecerá un mensaje cuando active la lista de precios. Puede elegir el precio a utilizar abriendo la lista y eliminando el precio incorrecto.  
  
---

## <a name="to-bulk-update-item-prices"></a>Para actualizar de forma masiva los precios de los artículos

Estos pasos difieren, dependiendo de si su administrador ha activado la actualización de la característica **Nueva experiencia de precios de venta**. Si la actualización de funciones no está activada, siga los pasos de la pestaña Experiencia actual.

#### [Experiencia actual](#tab/current-experience/)

Para actualizar de forma masiva los precios de los artículos, como aumentar todos los precios en un porcentaje, puede rellenar la página Hoja de trabajo precios de venta usando los siguientes trabajos por lotes:

* **Sugerir precio venta en hoja** sugiera cambios de una de estas dos formas:

  * Aplicando un factor de ajuste a los precios de venta existentes.
  * Copiando acuerdos de precios de venta existentes a otros clientes, grupos de precios de clientes o campañas de ventas.

* **Sugerir precio producto en hoja** sugiera cambios de una de estas dos formas:

  * Aplicando un factor de ajuste a precios unitarios existentes en fichas de productos.
  * Sugiriendo precios para nuevas combinaciones de moneda, unidades de medida, etc.

  Este trabajo por lotes no modifica los precios unitarios de los artículos.  

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Hoja de precios de venta** y luego elija el enlace relacionado.  
2. Elija **Sugerir precio producto en hoja**. .  
3. En la ficha desplegable **Artículo**, rellene los campos **N.º** o **Grupo registro inventario** u otros con los precios del artículo original que desea actualizar.  
4. En la parte superior de la página de solicitud, rellene el **Tipo venta** y **Código ventas** con el tipo y el nombre al que desea copiar los precios de venta.
5. Si desea que el proceso ajuste automáticamente los precios de los productos sugeridos, introduzca el ajuste en el campo **Factor de ajuste**. Por ejemplo, debe introducir 1,15 en **Factor de ajuste** para un aumento del 15 % en el precio del producto.  
6. Si desea que el trabajo por lotes cree precios nuevos, active la opción **Crear precios nuevos**.  
7. Elija el botón **Aceptar** para completar las líneas en la página **Hoja de trabajo de precio de venta** con los nuevos precios sugeridos.
8. Para implementar las sugerencias, utilice la acción **Implementar cambios de precio**. El trabajo por lotes crea sugerencias pero no las implementa. 

#### [Nueva experiencia](#tab/new-experience/)

Para actualizar los precios de varios productos, debe crear una nueva lista de precios y luego copiar las líneas desde una lista de precios existente. Cuando copie las líneas, puede usar filtros para especificar qué copiar, y puede especificar un número entero o decimal en el campo **Factor de ajuste** para aumentar o disminuir los precios. El estado de la lista de precios debe estar en estado **Borrador**. Si es necesario, puede desactivar la lista de precios anterior.

> [!NOTE]
> No puede tener dos líneas que tengan la misma configuración pero diferentes precios. Si eso sucede, aparecerá un mensaje cuando active una lista de precios. Puede elegir el precio a utilizar abriendo la lista y eliminando el precio incorrecto.  

---

## <a name="best-price-calculation"></a>Cálculo del mejor precio

Después de registrar precios especiales y alinear descuentos para ventas y compras, [!INCLUDE[prod_short](includes/prod_short.md)] calcula automáticamente el mejor precio en documentos de compra y venta y en líneas de diario de trabajos y artículos.

El mejor precio es el precio más bajo con el mayor descuento de línea permitido en una fecha indicada. [!INCLUDE[prod_short](includes/prod_short.md)] calcula los mejores precios al agregar precios unitarios y los porcentajes de descuento de línea de los productos en las nuevas líneas de documento y diario.

> [!NOTE]  
> A continuación se describe cómo se calcula el mejor precio para las ventas. Para las compras, el cálculo es similar pero se basa en los parámetros disponibles. Por ejemplo, los grupos de descuento de productos no se admiten para la compra.

1. [!INCLUDE[prod_short](includes/prod_short.md)] comprueba la combinación de la factura a cliente y el producto, y calcula el precio por unidad y el porcentaje de descuento de línea aplicables utilizando los siguientes criterios:

    * ¿El cliente tiene un acuerdo de precios o descuentos, o el cliente pertenece a un grupo que lo tiene?
    * ¿Está incluido el producto o el grupo de descuento del producto de la línea en alguno de estos acuerdos de precios o descuentos?
    * ¿Está la fecha dentro de la fecha inicial y final del acuerdo sobre precio/descuento? Para facturas y notas de abono, esta es la fecha en el campo **Fecha registro** en el encabezado del documento. Para todos los demás documentos, es la fecha en el campo **Fecha pedido** de sus encabezados.
    * ¿Se ha especificado un código de unidad de medida? Si es así, [!INCLUDE[prod_short](includes/prod_short.md)] comprueba los precios o descuentos con el mismo código de unidad de medida y los precios o descuentos sin un código de unidad de medida.

2. [!INCLUDE[prod_short](includes/prod_short.md)] comprueba si se aplican acuerdos de precio/descuento a la información del documento o línea de diario. Luego inserta el precio unitario aplicable y el porcentaje de descuento de línea utilizando los siguientes criterios:

    * ¿Hay un requisito de cantidad mínima en el acuerdo de precios o descuentos que se debe cumplir?
    * ¿Hay un requisito de divisa en el acuerdo de precios o descuentos que se debe cumplir? Si es así, se insertan el precio más bajo y el descuento de línea más alto para esa divisa, incluso si la divisa local proporciona un precio mejor. Si no existen acuerdos de precios o descuentos para el código de divisa especificado, [!INCLUDE[prod_short](includes/prod_short.md)] inserta el menor precio y el mayor descuento de línea en la su divisa local.

Si no se puede calcular ningún precio especial para el producto de la línea, se inserta el último coste directo o el precio unitario de la ficha de producto.

## <a name="sales-invoice-discounts-and-service-charges"></a>Descuentos y cargos por servicios de la factura de venta

Al utilizar descuentos en factura, el importe total de la factura determina el tamaño del descuento aplicado. En la página **Dtos. factura clientes**, también puede añadir un cargo por servicio a las facturas que superen un determinado importe.  

Para poder aplicar descuentos en factura a las ventas, primero debe especificar determinados datos. Debe tomar las decisiones siguientes:  

* ¿A qué clientes se le concederá este tipo de descuento?  
* ¿Qué porcentajes de descuento se van a aplicar?  

Si desea descuentos en factura para que se calculen automáticamente, en la página **Configuración ventas y cobros** active el conmutador **Calcular descuento inventario**.  

Puede especificar si ofrecerá descuentos en la factura si en la misma se cumplen ciertos criterios para cada cliente. Por ejemplo, si el monto de la factura es lo suficientemente grande. Los descuentos en factura pueden ser en divisa local para los clientes nacionales o en otras divisas para los clientes de otros países.  

Se relacionan los porcentajes de descuento a los importes de factura específicos en la página **Dtos. factura cliente** para cada cilente. Puede introducir un número ilimitado de porcentajes. Cada cliente puede tener su propia página o se pueden vincular varios clientes a la misma página.  

Además de, o en lugar de, un porcentaje de descuento, puede vincular un importe de cargo por servicios a un importe facturado específico.  

> [!TIP]  
> Antes de introducir esta información, se recomienda preparar un esquema de la estructura de descuentos que desea utilizar. La estructura hacer que resulte más fácil determinar los clientes que se pueden vincular a la misma página de descuentos en factura. Cuantas menos páginas tenga que configurar, más rápido introducirá la información básica.

Para formación sobre descuentos en ventas, consulte [Establecer descuentos para sus clientes](/training/modules/customer-discounts-dynamics-365-business-central/index).

### <a name="calculating-invoice-discounts-on-sales"></a>Calcular descuentos en factura para ventas

[!INCLUDE [sales-invoice-discounts](includes/sales-invoice-discounts.md)]

## <a name="to-set-up-a-sales-line-discount-for-a-customer"></a>Para configurar un descuento de línea de venta para un cliente

Estos pasos difieren, dependiendo de si su administrador ha activado la actualización de la característica **Nueva experiencia de precios de venta**. Si la actualización de funciones no está activada, siga los pasos de la pestaña Experiencia actual.

#### [Experiencia actual](#tab/current-experience/)  

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Clientes** y luego elija el enlace relacionado.
2. Abra la ficha de cliente correspondiente y, a continuación, elija la acción **Descuentos de línea**.
3. Rellene los campos de la línea como sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Rellene una línea para cada combinación que aplicará un descuento de línea de venta al cliente.

> [!NOTE]
> Cuando abra las páginas **Precios de venta** y **Descuentos de línea de ventas** de un cliente específico, los campos **Filtro de tipo de ventas** y **Filtro de código de ventas** se establecen para el cliente y no se pueden cambiar ni eliminar.
>
> Para configurar precios o descuentos de línea para todos los clientes, un grupo de precios de clientes o una campaña, debe abrir las páginas desde una tarjeta de producto. Alternativamente, para precios de venta, use la página **Hoja de trabajo de precio de venta**. Obtenga más información en [Para actualizar de forma masiva los precios de los productos](sales-how-record-sales-price-discount-payment-agreements.md#to-bulk-update-item-prices).  

#### [Nueva experiencia](#tab/new-experience/)  

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Clientes** y luego elija el enlace relacionado.
2. Elija el cliente y, a continuación, elija la acción **Listas de precios de venta**.
3. Abra la lista de precios para la que desea especificar el descuento de línea.
4. Cree una nueva línea o elija una existente y luego complete los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
5. En el campo **Define**, elija ya sea **Precio y descuento**, o solo **Descuento**. 
6. En el campo **% de descuento de línea**, especifique el porcentaje de descuento.

    > [!TIP]
    > Si está editando una línea existente, puede filtrar las líneas eligiendo la opción adecuada en el campo **Ver columnas para**.

    > [!NOTE]  
    > Los códigos de descuento en factura se representan por las fichas existentes del cliente. Lo que permite asignar rápidamente las condiciones de descuento en factura a clientes realizando el picking del nombre de otros clientes con los mismos términos. Para configurar términos de descuento de factura específicos del cliente, configure el campo **Código des. factura** con el código de cliente y luego continúe con el siguiente paso.

---

## <a name="to-set-up-an-invoice-discount-for-a-customer"></a>Para configurar un descuento en factura para un cliente

Después de decidir qué clientes pueden obtener descuentos en factura, introduzca el código de descuento en factura en las páginas de fichas cliente. Luego configure los términos para cada código.

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Clientes** y luego elija el enlace relacionado.
2. Abra la página de cliente para un cliente que pueda obtener descuentos en factura.
3. En el campo **Código descuento factura**, seleccione un código para los términos relevantes de la factura con descuentos que usará para calcular los descuentos en facturas para el cliente.

> [!NOTE]  
> Los códigos de descuento en factura se representan por las fichas existentes del cliente. Lo que permite asignar rápidamente las condiciones de descuento en factura a clientes realizando el picking del nombre de otros clientes con los mismos términos.

Configure los nuevos términos de descuento en factura de ventas.

1. En la página **Clientes**, seleccione la acción **Descuentos en factura**. Aparecerá la página **Descuentos en factura al cliente**.
2. En el campo **Código divisa**, introduzca el código de la divisa a la que se aplican los términos de descuento en factura en la línea. Deje el campo en blanco para establecer condiciones de descuento de factura en la divisa local.
3. En el campo **Importe mínimo**, escriba el importe mínimo que deba tener una factura para optar al descuento.
4. En el campo **% descuento**, introduzca el descuento en la factura como un porcentaje del importe de la factura.
5. Repita los pasos del 5 al 7 para cada divisa que el cliente reciba un descuento diferente de factura.

## <a name="see-related-microsoft-training"></a>Consultar la [formación de Microsoft](/training/modules/manage-sales-prices-dynamics-365-business-central/index) relacionada

## <a name="see-also"></a>Consulte también .

[Configuración de ventas](sales-setup-sales.md)  
[Ccial](sales-manage-sales.md)  
[Configurar los grupos de precio de clientes](sales-how-to-set-up-customer-price-groups.md)  
[Configuración de grupos de descuento de cliente](sales-how-to-set-up-customer-discount-groups.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
