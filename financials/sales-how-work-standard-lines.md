---
title: "Configurar y usar líneas estándar para ventas y compras periódicas | Documentos de Microsoft"
description: "Puede configurar líneas de ventas y líneas de compras que realice con frecuencia e insertarlas en documentos de venta y compra para rellenar rápidamente las líneas con información estándar."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, sell, replenishment
ms.date: 07/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 85d15de13739e944ff8817b402b37ae1c7e1b144
ms.openlocfilehash: 980a0646317c2b5c02c0eadcde9ba984c11580c4
ms.contentlocale: es-es
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-create-recurring-sales-and-purchase-lines"></a>Crear líneas de ventas y de compras periódicas
Si suele necesitar crear líneas de ventas y de compras con información similar, puede configurar líneas estándar que puede insertar en documentos de ventas y compras periódicas, por ejemplo, para órdenes de reposición periódicas.  

El siguiente procedimiento muestra cómo trabajar con líneas de ventas estándar. Funciona de forma similar para las líneas de compras estándar.  

## <a name="to-set-up-standard-sales-lines"></a>Para configurar las líneas de ventas estándar  
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Códigos de venta estándar** y, a continuación, seleccione el vínculo relacionado.  
2. En la ventana **Líneas ventas estándar**, elija la acción **Nuevo**.  
3. En la ficha desplegable **General**, rellene los campos como sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. En la ficha desplegable **Líneas**, introduzca la información en los campos para preparar líneas de ventas que reflejen las líneas estándar que desea utilizar como líneas recurrentes en los documentos de ventas.  

## <a name="to-insert-standard-sales-lines-on-a-sales-invoice"></a>Para insertar líneas de ventas estándar en una factura de ventas
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Facturas** y, a continuación, seleccione el vínculo relacionado.
2. Abra la factura de ventas en la que desee insertar una o varias líneas de ventas estándar.
3. Elija la acción **Obtener líneas de venta periódicas**.
4. En la ventana **Líneas de ventas periódicas**, elija el botón de búsqueda en el campo **Código** y seleccione un conjunto de líneas de ventas estándar.
5. Elija el botón **Acep.** para insertar las líneas de ventas estándar en la factura, donde puede reutilizar la información tal como está o editarla.

## <a name="to-create-multiple-sales-invoices-based-on-standard-sales-lines"></a>Para crear varias facturas de venta basadas en líneas de ventas estándar
Puede utilizar el trabajo por lotes **Crear facturas de venta periódicas** para crear facturas de venta según las líneas de venta estándar asignadas a los clientes y con fechas de registro dentro de las fechas de inicio y fin de validez que especifique en el código de ventas estándar.

En la ventana **Líneas de ventas periódicas**, también puede especificar una forma de pago por adeudo directo y una orden de domiciliación de adeudo directo. Las facturas de venta que se crean con el trabajo por lotes **Crear facturas de venta periódicas** incluirá la información necesaria para cobrar los pagos por adeudo directo SEPA para las facturas de venta. Para obtener más información, consulte Cobrar pagos mediante adeudo directo SEPA.

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Crear facturas de venta periódicas** y, a continuación, seleccione el vínculo relacionado.
2. En la ventana **Crear facturas de venta periódicas**, rellene los campos necesarios.
3. En el campo **Código**, introduzca el código de las líneas de ventas asignadas a un cliente para el que desee crear las facturas de ventas.
4. Elija el botón **Aceptar**.

Las facturas de venta se crean para los clientes con el código de ventas de cliente estándar especificado y la información de domiciliación especificada, para el registro en la fecha especificada.

## <a name="see-also"></a>Consulte también  
[Ventas](sales-manage-sales.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

