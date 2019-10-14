---
title: Trabajar con el IVA por ventas y compras | Documentos de Microsoft
description: En este tema se describe cómo realizar tareas como la corrección del IVA registrado. En países y regiones de la UE, cada transacción de compra y venta está sujeta a cálculos de IVA. En este tema se describe cómo.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, sales, purchases,
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: ab408bbef4e2fc9535eaa64e61a9e93d2d87378c
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2019
ms.locfileid: "2301569"
---
# <a name="work-with-vat-on-sales-and-purchases"></a>Trabajar con el IVA por ventas y compras
Si su país o región requiere que calcule el impuesto al valor añadido (IVA) en las transacciones de compra y venta para que pueda informar de los importes a una autoridad fiscal, puede configurar [!INCLUDE[d365fin](includes/d365fin_md.md)] para calcular el IVA automáticamente en documentos de ventas y compras. Para obtener más información, vea [Configurar los cálculos y los métodos de registro del impuesto sobre el valor añadido](finance-setup-vat.md).

Sin embargo, hay algunas tareas relacionadas con el IVA que puede realizar manualmente. Por ejemplo, puede que tenga que corregir un importe registrado si descubre que un proveedor utiliza un método de redondeo diferente.

## <a name="calculating-and-displaying-vat-amounts-in-sales-and-purchase-documents"></a>Calcular y mostrar los importes del IVA en documentos de ventas y compras  
Los importes del IVA de los documentos de ventas y compras se pueden calcular y mostrar de distintas maneras, según el tipo de cliente o proveedor de que se trate. También se puede anular el importe del IVA calculado de forma que coincida con el calculado por el proveedor en una transacción concreta.  

### <a name="unit-price-and-line-amount-includingexcluding-vat-on-sales-documents"></a>Precio de venta e importe de línea incluido/excluido el IVA en documentos de ventas  
Cuando elija un número de producto en el campo **Nº** de un documento de venta, [!INCLUDE[d365fin](includes/d365fin_md.md)] rellenará el campo **Precio de venta**. El precio de venta proviene de la ficha **Producto** o de los precios del producto admitidos para el producto y el cliente. [!INCLUDE[d365fin](includes/d365fin_md.md)] solo calcula el **Importe de línea** si introduce una cantidad en la línea.  

Si está vendiendo a consumidores minoristas, es posible que desee que los precios de los documentos de ventas incluyan el IVA. Para ello, seleccione la casilla de verificación **Precios IVA incluido** del documento.  

### <a name="including-or-excluding-vat-on-prices"></a>Inclusión o exclusión de IVA en los precios
Si la casilla de verificación **Precios IVA incluido** está seleccionada en un documento de ventas, los campos **Precio de venta** e **Importe de línea** incluirán el IVA, lo que también se indicará en el nombre de los campos. De forma predeterminada, no se incluye el IVA en estos campos.  

Si el campo no está activado, la aplicación rellenará los campos **Precio de venta** e **Importe de línea** sin incluir el IVA, lo que quedará indicado en el nombre de los campos.  

Puede configurar el valor predeterminado de **Precios IVA incluido** de todos los documentos de venta de un cliente en el campo **Precios IVA incluido** de la ficha **Cliente**. También puede configurar los precios de los productos con el IVA incluido o no incluido. Normalmente, los precios de los productos de la ficha Producto no incluirán el IVA. La aplicación usa la información del campo **Precio IVA incluido** de la ficha **Producto** para determinar el precio de venta de los documentos de ventas.  

En la tabla siguiente se ofrece una descripción global de cómo calcula la aplicación los precios unitarios de los documentos de ventas cuando no se han configurado los precios en la página **Precios de venta**:  

|**Campo Precio IVA incluido de la ficha Producto**|**Campo Precio IVA incluido de la Cabecera Venta**|**Acción realizada**|  
|-----------------------------------------------|----------------------------------------------------|--------------------------|  
|Sin marca de verificación|Sin marca de verificación|El **Precio de venta** de la ficha Producto se copia en el campo **Precio de venta IVA excl.** de las líneas de ventas.|  
|Sin marca de verificación|Marca de verificación|La aplicación calcula el importe del IVA por unidad y lo agrega al **Precio de venta** de la ficha Producto. A continuación, este precio de venta total se introduce en el campo **Precio de venta IVA incl.** de las líneas de ventas.|  
|Marca de verificación|Sin marca de verificación|La aplicación calcula el importe del IVA incluido en **Precio unitario** en la ficha de producto utilizando el % de IVA relativo a la combinación de Gr. contable negocio (Precio) y Grupo registro IVA prod. El **Precio unitario** en la ficha de producto, reducido por el importe de IVA, se introduce en el campo **Precio de venta IVA excl.** en las líneas de venta.|  
|Marca de verificación|Marca de verificación|El **Precio de venta** de la ficha Producto se copia en el campo **Precio venta IVA incl.** de las líneas de ventas.|

## <a name="correcting-vat-amounts-manually-in-sales-and-purchase-documents"></a>Corrección manual de los importes del IVA en los documentos de ventas y compras  
Puede corregir los movimientos del IVA registrados. Así, puede cambiar los importes totales del IVA de ventas o compras sin cambiar la base del IVA. Esto resulta necesario, por ejemplo, si recibe una factura de un proveedor que haya calculado el IVA de forma incorrecta.  

Aunque puede haber configurado una o varias combinaciones para administrar el importe de IVA, debe configurar al menos un grupo de registro de IVA de producto. Por ejemplo, puede nombrarla **CORRECTO** para las correcciones, a menos que pueda utilizar la misma cuenta de contabilidad en el campo **Cta. IVA acreditable** en la línea de configuración de registro de IVA. Para obtener más información, vea [Configurar los cálculos y los métodos de registro del impuesto sobre el valor añadido](finance-setup-vat.md).

Si el descuento por pronto pago se ha calculado sobre la base de un importe de factura que incluye IVA, revierta la parte de descuento del importe del IVA cuando se conceda el descuento. Observe que debe activar el campo **Ajuste para dto. P.P.**, tanto en la configuración de la contabilidad en general como en la configuración de los grupos de registro de IVA para las combinaciones específicas de grupo de registro de IVA por negocio y grupo de registro de IVA por producto.  

### <a name="to-set-the-system-up-for-manual-vat-entry-in-sales-documents"></a>Para configurar el sistema para el movimiento de IVA manual en documentos de ventas
A continuación se describe cómo habilitar las modificaciones de IVA manuales en los documentos de ventas. Los pasos son similares a los de la página **Configuración de compras y pagos**.

1. En la página **Configuración contabilidad**, especifique una **Máx. diferencia IVA permitida** el importe calculado por la aplicación y el importe manual.  
2. En la página **Config. ventas y cobros**, active el campo **Permitir diferen. IVA**.  

### <a name="to-adjust-vat-for-a-sales-document"></a>Para ajustar el IVA de un documento de venta  
1. Abra el pedido de venta correspondiente.  
2. Seleccione la acción **Estadísticas**.  
3. En la ficha desplegable **Facturación**, seleccione el valor en el campo **N.º de líneas de impuestos**.
4. Edite el campo **Importe de IVA**.   

> [!NOTE]  
> El importe total del IVA de la factura, agrupado por identificador de IVA, se muestra en las líneas. Puede ajustar manualmente el importe del campo **Importe IVA** de las líneas de cada identificador de IVA. Si modifica el campo **Importe IVA**, la aplicación comprueba que no lo modifica en un importe mayor que el especificado como diferencia máxima permitida. Si el importe es mayor que la **Máx. diferencia IVA permitida**, se muestra una advertencia en la que se indica cuál es la mayor diferencia permitida. No podrá continuar hasta que ajuste el importe con un valor admitido. Haga clic en **Aceptar** y escriba otro **Importe IVA** que sea admitido. Si la diferencia del IVA es igual a o menor que el máximo permitido, el IVA se dividirá proporcionalmente entre las líneas del documento que tengan el mismo identificador de IVA.  

## <a name="calculating-vat-manually-using-journals"></a>Cálculo manual del IVA mediante los diarios  
También puede ajustar los importes de IVA en general, ventas y diarios de compras. Por ejemplo, podría ser necesario si introduce una factura de proveedor en el diario y hay una diferencia entre el importe del IVA calculado por [!INCLUDE[d365fin](includes/d365fin_md.md)] y el de la factura del proveedor.  

### <a name="to-set-the-system-up-for-manual-vat-entry-in-a-general-journals"></a>Para configurar el sistema para el movimiento de IVA manual en un diario general
Debe realizar los pasos siguientes antes de introducir manualmente el IVA en un diario general.  

1. En la página **Configuración contabilidad**, especifique una **Máx. diferencia IVA permitida** el importe calculado por la aplicación y el importe manual.  
2. En la página **Libros diario general**, elija la casilla **Permitir diferen. IVA** del diario correspondiente.  

### <a name="to-set-the-system-up-for-manual-vat-entry-in-a-sales-and-purchase-journals"></a>Para configurar el sistema para el movimiento de IVA manual en un diario de ventas y compras
Debe realizar los pasos siguientes antes de introducir manualmente el IVA en un diario de ventas y compras.

1. En la página **Conf. compras y pagos**, seleccione la casilla **Permitir diferen. IVA**.  
2. Repita el paso 1 para la página **Configuración de ventas y cobros**.
3. Cuando haya completado las acciones descritas, puede ajustar el campo **Importe IVA** de la línea del diario general, o el campo **Importe IVA contrap.** de la línea del diario de ventas o compras. [!INCLUDE[d365fin](includes/d365fin_md.md)] comprobará que la diferencia no sea mayor que el máximo especificado.  

    > [!NOTE]  
    > Si la diferencia es mayor, se muestra una advertencia en la que se indica cuál es la mayor diferencia permitida. Para continuar, debe ajustar el importe. Elija **Aceptar** e introduzca un importe admitido. Si la diferencia de IVA es igual o menor que el máximo permitido, [!INCLUDE[d365fin](includes/d365fin_md.md)] mostrará la diferencia en el campo **Diferencia IVA**.  

## <a name="posting-import-vat-with-purchase-invoices"></a>Registro del IVA de importación con facturas de compra
En lugar de utilizar diarios para registrar las facturas de IVA de importación, puede utilizar facturas de compra.  

### <a name="to-set-up-purchasing-for-posting-import-vat-invoices"></a>Procedimiento para configurar la compra para registrar facturas de IVA de importación  
1. Configure una ficha de proveedor para la autoridad de importación que envía la factura de IVA de importación. Los campos **Grupo contable negocio** y **Grupo registro IVA neg.** deben configurarse de la misma forma que la contabilidad para el IVA de importación.  
2. Cree un **Gr. contable producto** para el IVA de importación y configure un **Grupo registro IVA producto** predeterminado del IVA de importación para el **Gr. contable producto** relacionado.  
3. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Plan de cuentas** y luego elija el enlace relacionado.  
4. Seleccione la cuenta del IVA de importación y, a continuación, en la pestaña **Inicio**, grupo **Administrar**, elija **Editar**.  
5. En la ficha desplegable **Registro**, seleccione la configuración **Grupo contable producto** para el IVA de importación. [!INCLUDE[d365fin](includes/d365fin_md.md)] debería rellenar automáticamente el campo **Grupo registro IVA prod.**  
6. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Configuración de registro general** y luego elija el enlace relacionado.  
7. Cree una combinación **Grupo contable negocio** para la autoridad de IVA y **Grupo contable producto** para el IVA de importación. Para esta combinación nueva, en el campo **Cuenta de compras**, elija la cuenta contable de IVA de importación.  

### <a name="to-create-a-new-invoice-for-the-import-authority-vendor-once-you-have-completed-the-setup"></a>Para crear una factura nueva para la autoridad de importación una vez haya finalizado la configuración  
1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Facturas compra** y luego elija el enlace relacionado.  
2. Cree una nueva factura de compra.  
3. En el campo **Compra a-Nº proveedor**, elija la autoridad de importación y elija el botón **Aceptar**.  
4. En la primera línea de compra, en el campo **Tipo**, elija **Cuenta** y en el campo **Nº** elija la cuenta contable de IVA de importación.  
5. En el campo **Cantidad**, escriba **1**.  
6. En el campo **Coste unitario directo excl. IVA**, especifique el importe de IVA.  
7. Registrar la factura.  

## <a name="processing-certificates-of-supply"></a>Procesamiento de certificados de suministro
Cuando se venden productos a un cliente en otro país o región de la UE, debe enviar al cliente un certificado de suministro que el cliente debe firmar y devolverle. Los procedimientos siguientes son para procesar certificados de suministro para los albaranes de venta, pero se siguen los mismos pasos para envíos de servicio de productos y envíos de devolución a proveedores.  

### <a name="to-view-certificate-of-supply-details"></a>Para ver detalles de un certificado de suministro  
1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Histórico albaranes venta** y luego elija el enlace relacionado.  
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

### <a name="to-print-a-certificate-of-supply"></a>Para imprimir certificado de suministro  
1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Histórico albaranes venta** y luego elija el enlace relacionado.  
2. Elija el albarán de venta correspondiente a un cliente de otro país o región de la UE.  
3. Elija la acción **Imprimir certificado de suministro**.  

    > [!NOTE]  
    >  También puede imprimir un certificado desde la página **Certificado de suministro**.  

4. Para incluir la información de las líneas en el documento de envío en el certificado, seleccione la casilla **Imprimir detalles de línea**.  
5. Elija la casilla **Crear certificados de suministro si no se han creado** para que [!INCLUDE[d365fin](includes/d365fin_md.md)] cree certificados para envíos registrados que no tengan ninguno en el momento de ejecutarse. Cuando elije la casilla, se crearán los nuevos certificados para todos los envíos registrados que no tengan certificados dentro del rango seleccionado.  
6. De forma predeterminada, la configuración de filtro corresponde al documento de envío seleccionado. Rellene la información de filtro para seleccionar un certificado de suministro específico que desee imprimir.  
7. En la página **Certificado de suministro**, elija la acción **Imprimir** para imprimir el informe o elija la acción **Vista preliminar** para verlo en la pantalla.  

    > [!Note]  
    > El campo **Estado certificado de suministro** y el campo **Impreso** se actualizan para el envío en la página **Certificados de suministro**.  

8. Envíe el certificado de suministro impreso al cliente para su firma.  

### <a name="to-update-the-status-of-a-certificate-of-supply-for-a-shipment"></a>Para actualizar el estado de un certificado de suministro para un envío  
1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Histórico albaranes venta** y luego elija el enlace relacionado.  
2. Elija el albarán de venta correspondiente a un cliente de otro país o región de la UE.  
3. En el campo **Estado**, seleccione la opción correspondiente.  

   Si el cliente ha devuelto el certificado de suministro firmado, elija **Recibido**. El campo **Fecha recepción** se actualiza. De forma predeterminada, la fecha de recepción se establece en la fecha de trabajo actual.  

   Puede modificar la fecha para reflejar la fecha en la que se recibió el certificado de suministro firmado por el cliente. También puede agregar un vínculo al certificado firmado con el sistema estándar de vinculación de [!INCLUDE[d365fin](includes/d365fin_md.md)].  

   Si el cliente no devuelve el certificado de suministro firmado, elija **No recibido**. Deberá entonces enviar al cliente una nueva factura que lleve IVA incluido, porque la autoridad fiscal no aceptará la factura original.  

Para ver un grupo de certificados, desde la página **Certificados de suministro** actualice la información sobre el estado de los certificados pendientes a medida que los reciba de sus clientes. Esto puede ser útil para buscar todos los certificados con un determinado estado, por ejemplo, **Requerido**, cuyo estado desee actualizar a **No recibido**.  

### <a name="to-update-the-status-of-a-group-of-certificates-of-supply"></a>Para actualizar el estado de un grupo de certificados de suministro  
1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Certificados de suministro** y elija el enlace relacionado.  
2. Filtre el campo **Estado** por el valor que desee para crear la lista de certificados que desee manipular.  
3. Para actualizar la información de estado, elija **Editar lista**.  
4. En el campo **Estado**, seleccione la opción correspondiente.  

   Si el cliente ha devuelto el certificado de suministro firmado, elija **Recibido**. El campo **Fecha recepción** se actualiza. De forma predeterminada, la fecha de recepción se establece en la fecha de trabajo actual.  

   Puede modificar la fecha para reflejar la fecha en la que se recibió el certificado de suministro firmado. También puede agregar un vínculo al certificado firmado con el sistema estándar de vinculación de documentos [!INCLUDE[d365fin](includes/d365fin_md.md)].  

    > [!NOTE]  
    >  No puede crear un certificado de suministro nuevo en la página **Certificado de suministro** mientras se navega a él con este procedimiento. Para crear certificados para envíos no configurados para requerirlos, abra el albarán de venta y siga cualquiera de los dos procedimientos descritos antes:  
    >   
    > * Para crear manualmente un certificado de suministro  
    > * Para imprimir certificado de suministro.

## <a name="see-also"></a>Consulte también  
[Configurar los cálculos y los métodos de registro del impuesto sobre el valor añadido](finance-setup-vat.md)   
[Crear informes de IVA para una autoridad fiscal](finance-how-report-vat.md)   
