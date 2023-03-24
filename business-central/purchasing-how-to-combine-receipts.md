---
title: Agrupar albaranes en una factura única
description: 'Si desea facturar varios albaranes de compra a la vez, puede utilizar la función Combinar albaranes.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: '136, 145, 146, 9308'
ms.date: 08/03/2022
ms.author: edupont
---
# Agrupar albaranes en una factura única

Si desea facturar varios albaranes de compra a la vez, puede seleccionar varias líneas de recibo en la factura de compra.  

Para poder crear un albarán de compra combinado, es necesario haber registrado primero más de un albarán del mismo proveedor y en la misma divisa. En otras palabras, debe haber rellenado dos o más pedidos de compra, así como haberlos registrado como recibidos, pero no facturado.  

Cuando se combinan varios albaranes de compra en una factura y se registran, se crea una factura de compra registrada para las líneas facturadas. El campo **Cantidad facturada** del pedido de compra de origen, o del pedido abierto de compra, se actualiza en función de la cantidad facturada. Sin embargo, este documento de compra original no se elimina, aunque se haya recibido y facturado por completo, por lo que debe eliminar el documento de compra.  

> [!NOTE]
> La factura de compra resultante no puede corregirse o cancelarse posteriormente. Si desea modificar una factura de compra que se crea de esta manera, debe usar notas de crédito de compra. Para obtener más información, vea [Corregir o cancelar las facturas de compra sin abonar](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)

## Para combinar albaranes

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Facturas compra** y luego elija el enlace relacionado.  
2. Seleccione la acción **Nuevo**. Para obtener más información, consulte [Registrar compras](purchasing-how-record-purchases.md).  
3. En la ficha desplegable Líneas, haga clic en **Acciones**, y elija la acción **Traer líns. recep**.  
4. Seleccione las distintas líneas de albarán que desee incluir en la factura.  

    Si se ha seleccionado una línea de albarán incorrecta o desea comenzar desde el principio, simplemente elimine las líneas de la factura de compra y vuelva a usar la función **Traer líns. recep**.  
5. Para registrar la factura, elija la acción **Registrar**.  

## Procedimiento para eliminar pedidos de compra abiertos después del registro de recepción combinada

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Eliminar peds. compra factdos** y seleccione el enlace relacionado.  
2. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].
3. Elija el botón **Aceptar**.  

También puede eliminar los pedidos individuales manualmente.

Repita las tareas 1 a 3 para cualquier otro documento asignado, como pedidos abiertos de compra.

## Consultar la [formación de Microsoft](/training/modules/processing-invoices-dynamics-365-business-central/) relacionada

## Consulte también .

[Compras](purchasing-manage-purchasing.md)  
[Corregir o cancelar facturas de compra sin abonar](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
