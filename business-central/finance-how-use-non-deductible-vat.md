---
title: Usar IVA no deducible
description: Este artículo explica cómo utilizar y declarar el IVA no deducible.
author: altotovi
ms.author: altotovi
ms.reviewer: null
ms.service: dynamics365-business-central
ms.topic: how-to
ms.search.keywords: 'VAT, non-deductible, return, settlement'
ms.search.form: '50, 51, 52, 161, 187, 317, 403, 6640, 9401'
ms.date: 04/26/2023
ms.custom: bap-template
---

# <a name="use-non-deductible-vat" />Usar IVA no deducible

Este artículo explica cómo utilizar y declarar el IVA no deducible.

## <a name="create-a-purchase-invoice-with-non-deductible-vat" />Crear una factura de compra con IVA no deducible

1. Seleccione el icono ![Bombilla que abre la característica Dígame 3.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Facturas compra** y, a continuación, elija el vínculo relacionado.
2. Seleccione **Nuevo** para crear una factura de compra e ingrese la información adecuada en el encabezado de la factura.
3. En la sección **Líneas**, cree una nueva línea de cualquier tipo, según el grupo contable de negocio de IVA y el grupo contable de productos de IVA donde configure el IVA no deducible.
4. En los campos **Cantidad** y **Coste unit. directo**, ingrese los valores apropiados.

    Si seleccionó la casilla **Mostrar IVA no ded. en líneas** en la página **Configuración de IVA**, las cantidades de los campos **Base IVA no deducible** y **Importe IVA no deducible** se calculan en función del campo **% IVA no deducible** de la página **Config. grupos registro IVA**.

5. Registrar la factura.

## <a name="create-a-purchase-order-with-non-deductible-vat" />Crear un pedido de compra con IVA no deducible

1. Seleccione el icono ![Bombilla que abre la característica Dígame 3.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pedidos de compra** y, a continuación, elija el vínculo relacionado.
2. Seleccione **Nuevo** para crear un pedido de compra e ingrese la información adecuada en el encabezado del documento.
3. En la sección **Líneas**, cree una nueva línea de cualquier tipo, según el grupo contable de negocio de IVA y el grupo contable de productos de IVA donde configure el IVA no deducible.
4. En los campos **Cantidad** y **Coste unit. directo**, ingrese los valores apropiados.

    Si seleccionó la casilla **Mostrar IVA no ded. en líneas** en la página **Configuración de IVA**, las cantidades de los campos **Base IVA no deducible** y **Importe IVA no deducible** se calculan en función del campo **% IVA no deducible** de la página **Config. grupos registro IVA**.

5. Registre el pedido de compra.

## <a name="adjust-rounded-vat-amounts-before-document-posting" />Ajustar los importes de IVA redondeados antes de la contabilización del documento

Si los importes del IVA no se redondean de la misma manera en su entorno y en el sistema contable externo (el documento de factura original), puede ajustar el importe del IVA antes de contabilizar el documento. Para realizar este ajuste, siga estos pasos antes de contabilizar el documento.

1. En el Panel de acciones, seleccione **Estadísticas**.
2. Si está trabajando con una factura de compra, siga estos pasos:

    1. En la ficha desplegable **Líneas**, seleccione el importe del IVA o el importe del IVA no deducible.
    2. Establezca los valores que necesita del documento original y luego cierre la página **Estad. factura compras**.

3.  Si está trabajando con el pedido de compra, siga estos pasos:

    1. En la ficha desplegable **Facturación**, seleccione **N.º de líneas de impuestos** para abrir la página **Líneas de importes de IVA**.
    2. Seleccione el importe del IVA o el importe del IVA no deducible que desea corregir.
    3. Introduzca los valores que necesita del documento original, cierre la página **Líns. importe IVA** y luego cierre la página **Estad. pedido compras**.

Para usar ajustes de importes de IVA, debe habilitar los ajustes. En la página **Configuración de contabilidad**, en la página **Máx. diferencia IVA permitida**, ingrese el importe máximo de IVA permitido para la corrección. A continuación, en la página **Conf. compras y pagos**, seleccione **Permitir diferen. IVA**.

Puede ajustar los valores de los campos **Importe de IVA** e **Importe IVA no deducible**. El valor del campo **IVA deduc. compras** es el resultado de estos dos valores. El importe que ingresa en el campo **Importe IVA no deducible** no puede ser mayor que el importe que ingresa en el campo **Importe de IVA**. El campo **Máx. diferencia IVA permitida** en la página **Configuración de contabilidad** funciona de forma independiente para los importes de IVA deducibles y no deducibles en las páginas de estadísticas cuando desea ajustar importes de IVA.

> [!IMPORTANT]
> No se puede utilizar IVA no deducible en las facturas de prepago.

## <a name="see-also" />Consulte también .

[Gestión financiera](finance.md)  
[Configurar los cálculos y los métodos de registro del impuesto sobre el valor añadido](finance-setup-vat.md)  
[Configurar el IVA no deducible](finance-setup-nondeductible-vat.md)  
[Crear informes de IVA para las autoridades fiscales](finance-how-report-vat.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
