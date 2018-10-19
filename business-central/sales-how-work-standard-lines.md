---
title: "Configurar líneas estándar para ventas y compras periódicas | Documentos de Microsoft"
description: "Puede configurar líneas de ventas y líneas de compras que realice con frecuencia e insertarlas en documentos de venta y compra para rellenar rápidamente las líneas con información estándar."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, sell, replenishment
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: df4f093ded0a55d45c40be15c5888035d6e3b2df
ms.contentlocale: es-es
ms.lasthandoff: 09/28/2018

---
# <a name="create-recurring-sales-and-purchase-lines"></a>Crear líneas de ventas y de compras periódicas
Si suele necesitar crear líneas de ventas y de compras con información similar, puede configurar líneas estándar que puede insertar en documentos de ventas y compras periódicas, por ejemplo, para órdenes de reposición periódicas.  

El siguiente procedimiento muestra cómo trabajar con líneas de ventas estándar. Funciona de forma similar para las líneas de compras estándar.  

## <a name="to-set-up-standard-sales-lines"></a>Para configurar las líneas de ventas estándar  
1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Líneas ventas estándar** y luego elija el enlace relacionado.  
2. En la ventana **Líneas ventas estándar**, elija la acción **Nuevo**.  
3. En la ficha desplegable **General**, rellene los campos como sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. En la ficha desplegable **Líneas**, introduzca la información en los campos para preparar líneas de ventas que reflejen las líneas estándar que desea utilizar como líneas recurrentes en los documentos de ventas.  

## <a name="to-insert-standard-sales-lines-on-a-sales-invoice"></a>Para insertar líneas de ventas estándar en una factura de ventas
1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Facturas** y luego elija el enlace relacionado.
2. Abra la factura de ventas en la que desee insertar una o varias líneas de ventas estándar.
3. Elija la acción **Obtener líneas de venta periódicas**.
4. En la ventana **Líneas de ventas periódicas**, elija el botón de búsqueda en el campo **Código** y seleccione un conjunto de líneas de ventas estándar.

    > [!NOTE]
    > Para usar las líneas de ventas recurrentes establecidas junto con el trabajo por lotes **Crear facturas de ventas periódicas**, también debe completar los campos **Válido desde la fecha** y **Válido hasta la fecha** en la ventana **Líneas de ventas recurrentes**. Para obtener más información, consulte la sección "Para crear varias facturas de venta basadas en líneas de ventas estándar".

5. Elija el botón **Aceptar** para insertar las líneas de ventas estándar en la factura, donde puede reutilizar la información tal como está o editarla.

## <a name="to-create-multiple-sales-invoices-based-on-standard-sales-lines"></a>Para crear varias facturas de venta basadas en líneas de ventas estándar
Puede utilizar el trabajo por lotes **Crear facturas de venta periódicas** para crear facturas de venta según las líneas de venta estándar asignadas a los clientes y con fechas de registro dentro de las fechas de inicio y fin de validez que especifique en las líneas de ventas estándar.

> [!NOTE]
> En la ventana **Líneas de ventas periódicas**, también puede especificar una forma de pago por adeudo directo y una orden de domiciliación de adeudo directo. Las facturas de venta que se crean con el trabajo por lotes **Crear facturas de venta periódicas** incluirá la información necesaria para cobrar los pagos por adeudo directo SEPA para las facturas de venta. Para obtener más información, consulte [Cobro de pagos mediante adeudo directo SEPA](finance-collect-payments-with-sepa-direct-debit.md).

1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Crear facturas de venta periódicas** y luego elija el enlace relacionado.
2. En la ventana **Crear facturas de venta periódicas**, rellene los campos necesarios.
3. En el campo de filtro **Código**, introduzca el código de las líneas de ventas asignadas a un cliente para el que desee crear las facturas de ventas.
4. Elija el botón **Aceptar**.

Las facturas de venta se crean para los clientes con el código de ventas de cliente estándar especificado y la información de domiciliación especificada, para el registro en la fecha especificada.

## <a name="see-also"></a>Consulte también  
[Ventas](sales-manage-sales.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

