---
title: Resumen de tareas para configurar las compras
description: Describe las tareas para definir las directivas de aprovisionamiento de su empresa y configurar sus procesos de compra.
author: SorenGP
ms.topic: overview
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'procurement, supply, vendor order'
ms.search.form: '175, 176, 177, 178, 456, 460, 5727, 5729'
ms.date: 08/30/2022
ms.author: edupont
---
# <a name="setting-up-purchasing"></a><a name="setting-up-purchasing"></a><a name="setting-up-purchasing"></a>Configurar compras

Para poder administrar procesos de compra, debe configurar las reglas y valores que definen las políticas de compra de la empresa.

Debe definir la configuración general en la página **Configuración de compras y pagos**, que normalmente se realiza una vez durante la implementación inicial. Obtenga más información en la siguiente sección, [Configuración de compras y pagos](#purchases-and-payables-setup).

Una serie de tareas independientes relacionadas con el registro de nuevos proveedores consiste en registrar acuerdos de precios especiales o descuentos que tenga con cada proveedor.

La configuración de compra relacionada con las finanzas, como las formas de pago o las divisas, se describe en la sección de configuración de finanzas. Obtenga más información en [Configurar las finanzas](finance-setup-finance.md). Del mismo modo, la configuración de compras relacionadas con el inventario, como las unidades de medida y los códigos de seguimiento de artículos, se puede encontrar en la [sección Configuración de inventario](inventory-setup-inventory.md).

## <a name="purchases-and-payables-setup"></a><a name="purchases-and-payables-setup"></a><a name="purchases-and-payables-setup"></a>Configuración de compras y pagos

Antes de trabajar con compras y pagos, especifique en la página **Configuración de compras y pagos** cómo se registran los valores de compra y las series numéricas utilizadas para proveedores y documentos de compra.

### <a name="general-settings"></a><a name="general-settings"></a><a name="general-settings"></a>Configuración general

En la ficha desplegable **General**, puede especificar opciones como el método de cálculo y registro de descuentos y si desea redondear las facturas. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

Algunos campos requieren una atención especial, como el campo **Calc. dto. fra. por ID IVA**, que especifica si el descuento en factura se calcula según el identificador de impuestos o el total de la factura. Obtenga más información en [Combinar grupos de registro de IVA en configuraciones de registro de IVA](finance-setup-vat.md#combine-vat-posting-groups-in-vat-posting-setups)

Del mismo modo, el campo **Liquidación entre divisas** puede producir pequeñas diferencias de redondeo al liquidar movimientos en distintas divisas. Obtenga más información en [Permitir la liquidación de movimientos de cliente en distintas divisas](finance-how-enable-application-ledger-entries-different-currencies.md).

Además, algunos campos cambian su comportamiento o dependen de cómo se configuran otros campos. Por ejemplo, la característica **Comprobar prepago al registrar** está influenciada por cómo el campo **Actualización automática prepago** está configurado para comprobar los pagos anticipados pendientes.

Leer detalles sobre los campos [**Nº doc. externo obligatorio**](#external-document-number) y [**Coste exacto devol. obligatorio**](#exact-cost-reversing) siguientes.

### <a name="number-series-settings"></a><a name="number-series-settings"></a><a name="number-series-settings"></a>Configuración de series numéricas

En la ficha desplegable **Serie numérica**, debe especificar los códigos de identificación únicos que se utilizarán para proveedores, facturas y otros documentos de compra. La numeración es importante no solo para los procesos internos, sino que también puede ser necesaria para cumplir las normas locales. Por lo tanto, podría valer la pena considerar configurar todas las series de la página **N.º serie** de antemano en lugar de crear otras nuevas a partir de **Configuración de compras y pagos**. Obtenga más información en [Crear numeración](ui-create-number-series.md).

## <a name="external-document-number"></a><a name="external-document-number"></a><a name="external-document-number"></a>Número de documento externo

[!INCLUDE [ext-doc-no-purch](includes/ext-doc-no-purch.md)]

## <a name="exact-cost-reversing"></a><a name="exact-cost-reversing"></a><a name="exact-cost-reversing"></a>Reversión de coste exacto

La función **Coste exacto devol. obligatorio** ayuda a garantizar que los bienes devueltos se valoren al mismo coste que cuando se extrajeron originalmente del inventario, utilizando una liquidación fija en lugar de seguir un método de coste promedio o primero en entrar, primero en salir (FIFO). Obtenga más información en la sección [Detalles de diseño: liquidación fija](design-details-item-application.md#fixed-application). Si se agrega un coste adicional posterior a la compra original, el programa actualiza el valor de la devolución de compra correspondiente.

Con la característica habilitada, solo se puede registrar una transacción de devolución especificando el número de movimiento de producto en el campo **Liq. por nº orden producto** en la línea de pedido de devolución de compra. De forma predeterminada no se muestra el campo en la ficha desplegable **Líneas**. Aprenda a agregar campos a las páginas en la sección [Personalizar el área de trabajo](ui-personalization-user.md#to-start-personalizing-a-page-through-the-personalizing-banner).

[!INCLUDE[local-functionality](includes/local-functionality.md)]

## <a name="more-purchasing-setups"></a><a name="more-purchasing-setups"></a><a name="more-purchasing-setups"></a>Más configuraciones de compra

| Para | Vea |
| --- | --- |
| Cree una ficha de proveedor por cada proveedor al que compre. |[Permite registrar nuevos proveedores](purchasing-how-register-new-vendors.md) |
| De prioridad a los proveedores. |[De prioridad a los proveedores](purchasing-how-prioritize-vendors.md) |
| Introduzca la información de la cuenta bancaria, incluidos los códigos de cuenta bancaria internacional (IBAN) y SWIFT, en la ficha de su proveedor. | [Configurar cuentas bancarias de proveedor](purchasing-how-set-up-vendors-bank-accounts.md) |
| Configure compradores, asígneles proveedores y códigos para realizar un seguimiento de las estadísticas. |[Configurar compradores](purchasing-how-setup-purchasers.md) |
| Introduzca los diferentes descuentos y precios especiales que los proveedores le ofrecen en función del producto, la cantidad y/o la fecha. |[Registrar acuerdos de pago, descuentos y precios de venta](purchasing-how-record-purchase-price-discount-payment-agreements.md) |
| Defina lo que paga por los artículos y servicios adquiridos por su empresa.  | [Establecer precios y descuentos](across-prices-and-discounts.md) |
| Cree líneas estándar para insertar en documentos de compra recurrentes. | [Configurar las líneas de compras periódicas](purchasing-how-work-recurring-purchase-lines.md) |
| Cree secuencias de tareas para conectar procesos realizados por diferentes usuarios, como solicitar y aprobar órdenes de compra. | [Configurar flujos de trabajo de aprobación de compra](across-set-up-workflows.md) |
| Administre las interacciones comerciales con sus proveedores, importe los documentos de factura recibidos y registre nuevos proveedores utilizando el cliente de correo electrónico de Outlook. | [Configurar el complemento Business Central para Outlook](admin-outlook.md) |
| Revise recibos de gastos, convierta documentos en papel y electrónicos en líneas de diario y digitalice facturas en papel de los proveedores. | [Configurar documentos entrantes](across-how-setup-income-documents.md) |
| Especifique informes predeterminados que se utilizarán para diferentes tipos de documentos. |[Selección de informes en Business Central](across-report-selections.md)|

## <a name="see-related-training-at-microsoft-learn"></a><a name="see-related-training-at-microsoft-learn"></a><a name="see-related-training-at-microsoft-learn"></a>Consulte la formación relacionada en [Microsoft Learn](/learn/paths/trade-get-started-dynamics-365-business-central/).

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Consulte también .

[Compras](purchasing-manage-purchasing.md)  
[Descripción general de la configuración](setup.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
