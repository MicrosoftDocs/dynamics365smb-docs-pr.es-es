---
title: Trabajar con el IVA por ventas y compras
description: 'Este tema describe las diversas formas de trabajar con IVA tanto manualmente como con la configuración automática, para ayudarle a cumplir las regulaciones específicas del país o región.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'VAT, sales, purchases'
ms.search.form: '7, 118, 130, 142, 459, 460, 525'
ms.date: 06/16/2021
ms.author: bholtorf
---
# Trabajar con el IVA por ventas y compras

Si su país o región exige que calcule e informe del impuesto sobre el valor añadido (IVA) en las transacciones de compra y venta, puede configurar [!INCLUDE[prod_short](includes/prod_short.md)] para calcular el IVA. Para obtener más información, vea [Configurar los cálculos y los métodos de registro del impuesto sobre el valor añadido](finance-setup-vat.md).

Sin embargo, hay algunas tareas relacionadas con el IVA que puede realizar manualmente. Por ejemplo, puede que tenga que corregir un importe registrado si descubre que un proveedor utiliza un método de redondeo diferente.  

> [!TIP]
> Puede dejar que [!INCLUDE[prod_short](includes/prod_short.md)] valide los CIF/NIF y otra información de la empresa al crear o actualizar documentos. Para más información, consulte [Validar CIF/NIF](finance-how-validate-vat-registration-number.md).

## Calcular y mostrar los importes del IVA en documentos de ventas y compras  

Cuando elija un número de producto en el campo **Nº** en un documento de compra o venta, [!INCLUDE[prod_short](includes/prod_short.md)] completa los campos **Precio unitario** y **Importe línea**. El precio de venta proviene de la ficha **Producto** o de los precios del producto admitidos para el producto y el cliente. [!INCLUDE[prod_short](includes/prod_short.md)] calcula el importe de línea si introduce una cantidad en la línea.  

Si desea que los precios unitarios y los importes de línea incluyan el IVA, por ejemplo, si vende a consumidores minoristas, seleccione la casilla **Precios IVA Incluido** en el documento. Para obtener más información, consulte [Inclusión o exclusión de IVA en precios e importes de línea](#including-or-excluding-vat-in-prices-and-line-amounts). 

Los importes del IVA de los documentos de ventas y compras se pueden calcular y mostrar de distintas maneras, según el tipo de cliente o proveedor de que se trate. También se puede cambiar el importe del IVA calculado de forma manual, por ejemplo, para que coincida con el calculado por el proveedor en una transacción concreta.

### Inclusión o exclusión del IVA en precios e importes de línea

Si elige la casilla **Precios IVA incluido** en un documento de ventas, los campos **Precio de venta** e **Importe de línea** incluirán el IVA. De forma predeterminada, los valores de estos campos no incluyen el IVA. Los nombres de los campos reflejan si los precios incluyen IVA.  

Puede configurar el valor predeterminado de **Precios IVA incluido** de todos los documentos de venta de un cliente en el campo **Precios IVA incluido** de la ficha **Cliente**. También puede configurar los precios de los productos con el IVA incluido o no incluido. Por lo general, los precios en la Ficha de producto no incluirán el IVA. 

En la tabla siguiente se ofrece una descripción global de cómo calcula la aplicación los precios unitarios de los documentos de ventas cuando no se han configurado los precios en la página **Precios de venta**:  

|**Campo Precio IVA incluido de la ficha Producto**|**Campo Precios IVA incluido**|**Acción realizada**|  
|-----------------------------------------------|----------------------------------------------------|--------------------------|  
|No habilitado|No habilitado|El **Precio de venta** de la ficha Producto se copia en el campo **Precio de venta IVA excl.** de las líneas de ventas.|  
|No habilitado|Habilitada|La aplicación calcula el importe del IVA por unidad y lo agrega al **Precio de venta** de la ficha Producto. A continuación, este precio unitario total se introduce en el campo **Precio de venta IVA incl.** de las líneas de ventas.|  
|Habilitada|No habilitado|La aplicación calcula el importe del IVA incluido en el campo **Precio unitario** en la **Ficha de producto** utilizando el porcentaje de IVA relativo a la combinación de Gr. contable negocio (Precio) y Grupo registro IVA prod. El **Precio unitario** en la ficha de producto, reducido por el importe de IVA, se introduce en el campo **Precio de venta IVA excl.** en las líneas de venta. Para obtener más información, consulte [Usar Grupos contable IVA negocio y Grupos precio cliente](finance-work-with-vat.md#using-vat-business-posting-groups-and-customer-price-groups).|  
|Habilitada|Habilitada|El **Precio de venta** de la ficha Producto se copia en el campo **Precio venta IVA incl.** de las líneas de ventas.|

#### Usar Grupos contables de IVA de negocio y grupos de precio de cliente 

Si desea que los precios incluyan el IVA, puede usar los grupos de registro de IVA de negocio para calcular el importe basado en la configuración de registro de IVA para el grupo. Para obtener más información, consulte [Configuración de grupos de registro de IVA de negocio](finance-setup-vat.md#set-up-vat-business-posting-groups).

Dependiendo de lo que desee hacer, puede asignar un grupo de registro de IVA de negocio a clientes o documentos de ventas de las siguientes maneras:

* Para usar el mismo tipo de IVA para todos los clientes, puede elegir un grupo en el campo **Grupo de registro de IVA de negocio (precio)** en la página **Configuración de ventas y cobros**.
* Para usar un tipo de IVA para un cliente específico, puede elegir un grupo en el campo **Grupo de registro de IVA de negocio (precio)** en la página **Ficha cliente**. 
* Para usar un tipo de IVA para clientes específicos, puede elegir un grupo en el campo **Grupo de registro de IVA de negocio (precio)** en la página **Grupo precio cliente**. Por ejemplo, esto resulta útil cuando desea que se aplique un precio a todos los clientes en una determinada región geográfica o una industria concreta.
* En todos los documentos de venta en el campo **Grupo de registro de IVA de negocio**. El importe de IVA especificado para el grupo se utiliza solo para el documento en el que está trabajando actualmente.

> [!NOTE]
> Si no especifica un grupo en el campo **Grupo de registro de IVA de negocio (precio)**, el IVA no se incluirá en los precios.

#### Ejemplos

Factores como el país o la región en los que vende, o el tipo de sectores a los que vende, pueden afectar al importe de IVA que debe contabilizar. Por ejemplo, un restaurante puede cobrar un 6 % de IVA por las comidas que se consumen en el local y un 17 % por las comidas para llevar. Para lograrlo, cree un grupo de registro de IVA de negocio (precio) para uso interno y uno para llevar.

## Trabajar con la fecha del IVA

### Fecha de IVA en documentos

Cuando crea nuevos documentos de compra o venta, la **Fecha de IVA** se basará en la configuración del campo **Fecha de IVA predeterminada** de la página **Configuración de contabilidad**. Este valor predeterminado puede ser el mismo que **Fecha registro** o **Fecha de documento**. Si necesita otra fecha de IVA, puede cambiar manualmente el valor en el campo **Fecha de IVA**. Al contabilizar el documento, la **Fecha de IVA** se mostrará en el documento de contabilización y en los movimientos de IVA y contabilidad.

> [!NOTE]
> Si el campo **Fecha de IVA** no está disponible en los documentos o diarios, eso significa que **No usar la funcionalidad de fecha de IVA** se ha elegido en el campo **Uso fecha IVA** en la página **Configuración de contabilidad**.  

> [!IMPORTANT]
> Si configura **Controlar periodo de IVA** en **Configuración de contabilidad** como **Bloquear registro dentro de periodo cerrado** o **Bloquear registro en cerrado y advertir para periodo liberado**, puede registrar documentos o diarios solo si la fecha del campo **Fecha de IVA** no está en un período cerrado en **Períodos de devolución de IVA**. Incluso si el período de **Periodos de devolución de IVA** está abierto, es posible que reciba una advertencia basada en el **Estado de devolución de IVA** y la configuración de **Controlar periodo de IVA**.

> [!IMPORTANT]
> A partir de la versión 23.1, puede evitar o permitir el registro de la **Fecha de IVA** para un rango de datos específico, usando los campos **Permitir la fecha de IVA desde** y **Permitir la fecha de IVA hasta** en la **Configuración de IVA** y **Configuración usuarios**. Si usa versiones anteriores, puede evitar o permitir el registro de la **Fecha de IVA** para un rango de datos específico, usando los campos **Permitir registro desde** y **Permitir registro hasta** en la **Configuración de contabilidad** y **Configuración usuarios**.  

> [!NOTE]
> Si deja la **Fecha de IVA** en blanco, [!INCLUDE [prod_short](includes/prod_short.md)] usará como **Fecha de IVA** en la transacción registrada la configuración predeterminada de **Fecha de IVA predeterminada** que se encuentra en **Configuración de contabilidad**.  

### Modificar la fecha de IVA en los movimientos registrados

Si es necesario, puede cambiar la fecha de IVA registrada en los documentos. Para cambiar la fecha del campo **Fecha de IVA** de un documento registrado, debe seguir estos pasos:

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Movimientos de IVA** y luego elija el enlace relacionado. 
2. Busque el movimiento con la fecha errónea de IVA.  
3. Elija la acción **Editar lista** e introduzca la fecha correcta en el campo **Fecha de IVA**.  
4. Cuando cierre la página, la fecha de IVA cambiará en los **Movimientos de contabilidad** relacionados y en el documento contabilizado.  

> [!NOTE]
> Puede cambiar el campo **Fecha de IVA** de **Movimientos de IVA** solo si la fecha actual no está en un periodo de devolución de IVA cerrado. Incluso si el período de **Periodos de devolución de IVA** está abierto, es posible que reciba una advertencia basada en el **Estado de devolución de IVA**.  

> [!NOTE]
> Si su documento tiene más de un **Movimiento de IVA**, solo necesita cambiar el valor en el campo **Fecha de IVA** en un movimiento relacionado con el documento. Para mantener la coherencia de los movimientos, [!INCLUDE[prod_short](includes/prod_short.md)] cambia automáticamente la fecha del IVA en las entradas de IVA relacionadas con esta transacción. [!INCLUDE [prod_short](includes/prod_short.md)] actualizará la **Fecha de IVA** en otras tablas (entradas y documentos del libro mayor), pero solo en relación con esta transacción.  

## Corrección manual de los importes del IVA en los documentos de ventas y compras  

Puede corregir movimientos de IVA contabilizados para poder cambiar los importes totales de IVA repercutido o soportado sin cambiar la base de IVA. Por ejemplo, si recibe una factura de un proveedor con un importe de IVA incorrecto.  

Aunque puede haber configurado una o varias combinaciones para administrar el importe de IVA, debe configurar al menos un grupo de registro de IVA de producto. Por ejemplo, puede nombrarla **CORRECTO** para las correcciones, a menos que pueda utilizar la misma cuenta de contabilidad en el campo **Cta. IVA acreditable** en la línea de configuración de registro de IVA. Para obtener más información, consulte [Configurar los cálculos y los métodos de registro del impuesto sobre el valor añadido](finance-setup-vat.md).

Si el descuento por pronto pago se ha calculado sobre la base de un importe de factura que incluye IVA, revierta la parte de descuento del importe del IVA cuando se conceda el descuento. Observe que debe activar el campo **Ajuste para dto. P.P.**, tanto en la configuración de la contabilidad en general como en la configuración de los grupos de registro de IVA para las combinaciones específicas de grupo de registro de IVA por negocio y grupo de registro de IVA por producto.  

### Para configurar el sistema para el movimiento de IVA manual en documentos de ventas
A continuación se describe cómo habilitar las modificaciones de IVA manuales en los documentos de ventas. Los pasos son similares a los de la página **Configuración de compras y pagos**.

1. En la página **Configuración contabilidad**, especifique una **Máx. diferencia IVA permitida** el importe calculado por la aplicación y el importe manual.  
2. En la página **Config. ventas y cobros**, active el campo **Permitir diferen. IVA**.  

### Para ajustar el IVA de un documento de venta

1. Abra el pedido de venta correspondiente.  
2. Seleccione la acción **Estadísticas**.  
3. En la ficha desplegable **Facturación**, seleccione el valor en el campo **N.º de líneas de impuestos**.
4. Edite el campo **Importe de IVA**.   

> [!NOTE]  
> El importe total del IVA de la factura, agrupado por identificador de IVA, se muestra en las líneas. Puede ajustar manualmente el importe del campo **Importe IVA** de las líneas de cada identificador de IVA. Si modifica el campo **Importe IVA**, la aplicación comprueba que no lo modifica en un importe mayor que el especificado como diferencia máxima permitida. Si el importe es mayor que la **Máx. diferencia IVA permitida**, se muestra una advertencia en la que se indica cuál es la mayor diferencia permitida. No podrá continuar hasta que ajuste el importe con un valor admitido. Haga clic en **Aceptar** y escriba otro **Importe IVA** que sea admitido. Si la diferencia del IVA es igual a o menor que el máximo permitido, el IVA se dividirá proporcionalmente entre las líneas del documento que tengan el mismo identificador de IVA.  

## Cálculo manual del IVA mediante los diarios  
También puede ajustar los importes de IVA en general, ventas y diarios de compras. Por ejemplo, podría ser necesario si introduce una factura de proveedor en el diario y hay una diferencia entre el importe del IVA calculado por [!INCLUDE[prod_short](includes/prod_short.md)] y el de la factura del proveedor.  

### Para configurar el sistema para el movimiento de IVA manual en un diario general
Debe realizar los pasos siguientes antes de introducir manualmente el IVA en un diario general.  

1. En la página **Configuración contabilidad**, especifique una **Máx. diferencia IVA permitida** el importe calculado por la aplicación y el importe manual.  
2. En la página **Libros diario general**, elija la casilla **Permitir diferen. IVA** del diario correspondiente.  

### Para configurar el sistema para el movimiento de IVA manual en un diario de ventas y compras

Debe realizar los pasos siguientes antes de introducir manualmente el IVA en un diario de ventas y compras.

1. En la página **Conf. compras y pagos**, seleccione la casilla **Permitir diferen. IVA**.  
2. Repita el paso 1 para la página **Configuración de ventas y cobros**.
3. Cuando haya completado las acciones descritas, puede ajustar el campo **Importe IVA** de la línea del diario general, o el campo **Importe IVA contrap.** de la línea del diario de ventas o compras. [!INCLUDE[prod_short](includes/prod_short.md)] comprobará que la diferencia no sea mayor que el máximo especificado.  

> [!NOTE]  
> Si la diferencia es mayor, se muestra una advertencia en la que se indica cuál es la mayor diferencia permitida. Para continuar, debe ajustar el importe. Elija **Aceptar** e introduzca un importe admitido. Si la diferencia de IVA es igual o menor que el máximo permitido, [!INCLUDE[prod_short](includes/prod_short.md)] mostrará la diferencia en el campo **Diferencia IVA**.  

## Registro del IVA de importación con facturas de compra
En lugar de utilizar diarios para registrar las facturas de IVA de importación, puede utilizar facturas de compra.  

### Procedimiento para configurar la compra para registrar facturas de IVA de importación

1. Configure una ficha de proveedor para la autoridad de importación que envía la factura de IVA de importación. Los campos **Grupo contable negocio** y **Grupo registro IVA neg.** deben configurarse de la misma forma que la contabilidad para el IVA de importación.  
2. Cree un **Gr. contable producto** para el IVA de importación y configure un **Grupo registro IVA producto** predeterminado del IVA de importación para el **Gr. contable producto** relacionado.  
3. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Plan de cuentas** y luego elija el enlace relacionado.  
4. Seleccione la cuenta contable de IVA de importación y, a continuación, seleccione la acción **Editar**.  
5. En la ficha desplegable **Registro**, seleccione la configuración **Grupo contable producto** para el IVA de importación. [!INCLUDE[prod_short](includes/prod_short.md)] debería rellenar automáticamente el campo **Grupo registro IVA prod.**  
6. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración grupos contables** y luego elija el enlace relacionado.  
7. Cree una combinación **Grupo contable negocio** para la autoridad de IVA y **Grupo contable producto** para el IVA de importación. Para esta combinación nueva, en el campo **Cuenta de compras**, elija la cuenta contable de IVA de importación.  

### Para crear una factura nueva para la autoridad de importación una vez haya finalizado la configuración  

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Facturas compra** y luego elija el enlace relacionado.  
2. Cree una nueva factura de compra.  
3. En el campo **Compra a-Nº proveedor**, elija la autoridad de importación y elija el botón **Aceptar**.  
4. En la primera línea de compra, en el campo **Tipo**, elija **Cuenta** y en el campo **Nº** elija la cuenta contable de IVA de importación.  
5. En el campo **Cantidad**, escriba **1**.  
6. En el campo **Coste unitario directo excl. IVA**, especifique el importe de IVA.  
7. Registrar la factura.  

## Procesamiento de certificados de oferta

Cuando se venden productos a un cliente en otro país o región de la UE, debe enviar al cliente un certificado de suministro que el cliente debe firmar y devolverle. Los procedimientos siguientes son para procesar certificados de suministro para los albaranes de venta, pero se siguen los mismos pasos para envíos de servicio de productos y envíos de devolución a proveedores.  

### Para ver detalles de un certificado de suministro  
1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Histórico albaranes venta** y, a continuación, elija el vínculo relacionado.  
2. Elija el albarán de venta correspondiente a un cliente de otro país o región de la UE.  
3. Elija **Detalles del certificado de suministro**.  
4. De forma predeterminada, la casilla **Certificado de suministro obligatorio** está seleccionada por la configuración de grupo de registro de IVA correspondiente al cliente, el campo **Estado** se configura en **Obligatorio**. Puede actualizar el campo para indicar si el cliente ha devuelto el certificado.  

> [!Note]  
>  Si la configuración del grupo de registro de IVA no tiene seleccionada la casilla **Certificado de suministro obligatorio**, se crea un registro y el campo **Estado** se establece en **No aplica**. Puede actualizar el campo para reflejar la información correcta del estado. Puede cambiar manualmente el estado de **No aplicable** a **Requerido**, y de **Requerido** a **No aplicable**, según sea necesario.  

   Cuando se actualiza el campo **Estado** a **Requerido**, **Recibido** o **No recibido**, se crea un certificado.  

> [!TIP]  
>  Puede utilizar la página **Certificados de suministro** para obtener una vista el estado de todos los envíos registrados para los que se haya creado un certificado de suministro.  

5. Elija **Imprimir certificado de suministro**.  

> [!Note]  
>  Puede ver o imprimir el documento. Cuando elige **Imprimir certificado de suministro** e imprime el documento, la casilla **Impreso** se selecciona automáticamente. Además, si no se ha especificado, el estado del certificado se actualiza a **Obligatorio**. Si es necesario, el certificado impreso se incluye con el envío.  

### Para imprimir certificado de suministro

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Histórico albaranes venta** y, a continuación, elija el vínculo relacionado.  
2. Elija el albarán de venta correspondiente a un cliente de otro país o región de la UE.  
3. Elija la acción **Imprimir certificado de suministro**.  

> [!NOTE]  
>  También puede imprimir un certificado desde la página **Certificado de suministro**.  

4. Para incluir la información de las líneas en el documento de envío en el certificado, seleccione la casilla **Imprimir detalles de línea**.  
5. Elija la casilla **Crear certificados de suministro si no se han creado** para que [!INCLUDE[prod_short](includes/prod_short.md)] cree certificados para envíos registrados que no tengan ninguno en el momento de ejecutarse. Cuando elije la casilla, se crearán los nuevos certificados para todos los envíos registrados que no tengan certificados dentro del rango seleccionado.  
6. De forma predeterminada, la configuración de filtro corresponde al documento de envío seleccionado. Rellene la información de filtro para seleccionar un certificado de suministro específico que desee imprimir.  
7. En la página **Certificado de suministro**, elija la acción **Imprimir** para imprimir el informe o elija la acción **Vista preliminar** para verlo en la pantalla.  

> [!Note]  
> El campo **Estado certificado de suministro** y el campo **Impreso** se actualizan para el envío en la página **Certificados de suministro**.  

8. Envíe el certificado de suministro impreso al cliente para su firma.  

### Para actualizar el estado de un certificado de suministro para un envío  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Histórico albaranes venta** y, a continuación, elija el vínculo relacionado.  
2. Elija el albarán de venta correspondiente a un cliente de otro país o región de la UE.  
3. En el campo **Estado**, seleccione la opción correspondiente.  

   Si el cliente ha devuelto el certificado de suministro firmado, elija **Recibido**. El campo **Fecha recepción** se actualiza. De forma predeterminada, la fecha de recepción se establece en la fecha de trabajo actual.  

   Puede modificar la fecha para reflejar la fecha en la que se recibió el certificado de suministro firmado por el cliente. También puede agregar un vínculo al certificado firmado con el sistema estándar de vinculación de [!INCLUDE[prod_short](includes/prod_short.md)].  

   Si el cliente no devuelve el certificado de suministro firmado, elija **No recibido**. Deberá entonces enviar al cliente una nueva factura que lleve IVA incluido, porque la autoridad fiscal no aceptará la factura original.  

Para ver un grupo de certificados, desde la página **Certificados de suministro** actualice la información sobre el estado de los certificados pendientes a medida que los reciba de sus clientes. Esto puede ser útil para buscar todos los certificados con un determinado estado, por ejemplo, **Requerido**, cuyo estado desee actualizar a **No recibido**.  

### Para actualizar el estado de un grupo de certificados de suministro  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Certificados de suministro** y, a continuación, elija el vínculo relacionado.  
2. Filtre el campo **Estado** por el valor que desee para crear la lista de certificados que desee manipular.  
3. Para actualizar la información de estado, elija **Editar lista**.  
4. En el campo **Estado**, seleccione la opción correspondiente.  

   Si el cliente ha devuelto el certificado de suministro firmado, elija **Recibido**. El campo **Fecha recepción** se actualiza. De forma predeterminada, la fecha de recepción se establece en la fecha de trabajo actual.  

   Puede modificar la fecha para reflejar la fecha en la que se recibió el certificado de suministro firmado. También puede agregar un vínculo al certificado firmado con el sistema estándar de vinculación de documentos [!INCLUDE[prod_short](includes/prod_short.md)].  

> [!NOTE]
> No puede crear un certificado de suministro nuevo en la página **Certificado de suministro** mientras se navega a él con este procedimiento. Para crear certificados para envíos no configurados para requerirlos, abra el albarán de venta y siga cualquiera de los dos procedimientos descritos antes:  
>
> * Para crear manualmente un certificado de suministro  
> * Para imprimir certificado de suministro.

## Consulte también

[Configurar los cálculos y los métodos de registro del impuesto sobre el valor añadido](finance-setup-vat.md)  
[Crear informes de IVA para la autoridad fiscal](finance-how-report-vat.md)  
[Validar un CIF/NIF](finance-how-validate-vat-registration-number.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
