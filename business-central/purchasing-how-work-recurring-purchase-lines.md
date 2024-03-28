---
title: Líneas de compra periódicas estándar
description: Configure líneas de compras que use con frecuencia para insertarlas en documentos de compra y rellenar rápidamente las líneas con información estándar.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'trade, purchase, replenishment'
ms.search.form: 177
ms.date: 07/06/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Crear líneas de compra periódicas

Si suele necesitar crear líneas de compras con información similar, puede configurar líneas estándar que puede insertar en documentos de compras periódicas, por ejemplo, para órdenes de reposición periódicas.

## Configurar las líneas de compras periódicas

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Líneas de compras periódicas** y, a continuación, elija el vínculo relacionado.
2. En la página **Líneas de compras periódicas**, elija la acción **Nuevo**.
3. En la ficha desplegable **General**, rellene los campos como sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. En la ficha desplegable **Líneas**, introduzca la información en los campos que reflejen las líneas estándar que desea utilizar como líneas recurrentes en los documentos de compras.

> [!NOTE]
> No puede definir precios en líneas de compras periódicas porque los precios, descuentos, etc., se calculan en los documentos de compras reales después de insertar las líneas de compras periódicas.

[!INCLUDE [line-no-info](includes/line-no-info.md)]

## Asignar líneas de compra recurrentes a un proveedor

Asigne una o varias líneas de compras periódicas a un proveedor para que estén disponibles para insertarlas en documentos de compras para ese proveedor.

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Proveedores** y luego elija el enlace relacionado.
2. Abra la ficha de un proveedor relevante.
3. Elija la acción **Líneas de compras periódicas**.
4. En la página **Líneas de compras periódicas**, seleccione los códigos de las líneas de compras periódicas que desea insertar en documentos de compras para el proveedor.
5. Rellene los otros campos para definir cuándo, cómo y dónde se deben utilizar las líneas de compras periódicas.
6. En los cuatro campos donde selecciona cómo se insertan las líneas en cada tipo de documento, seleccione una de las siguientes opciones:

|Opción|Descripción|
|------|-----------|
|**Manual**|Debe buscar manualmente e insertar una línea de compra recurrente que exista para el proveedor.|
|**Automática**|Si existen varias líneas de compra recurrentes para el proveedor, recibirá una notificación desde donde puede elegir cuál insertar. Si sólo existe una línea de compra recurrente, se insertará automáticamente.<br /><br />Esto solo funciona si el nuevo documento se creó a partir de una lista de documentos, por ejemplo, eligiendo la acción **Nuevo** en la página **Pedidos de compra**. No funciona si el documento se creó a partir de una ficha de proveedor, por ejemplo.|
|**Preguntar siempre**|Aparece una notificación y se muestran todas las líneas de compra recurrentes que existen para que pueda seleccionar una.

## Insertar líneas de compra recurrentes en una factura de compra

Si existen líneas de compras periódicas para el proveedor, puede insertarlas, o hacer que se agreguen automáticamente, en todos los tipos de documentos de compras, como una factura de compras. Si ha activado las opciones de **Preguntar siempre** al asignar líneas de compras periódicas a los proveedores, se le informará de si existen líneas de compras periódicas.

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Facturas compra** y luego elija el enlace relacionado.
2. Abra la factura de compras en la que desee insertar una o varias líneas de compras estándar.
3. Elija la acción **Obtener líneas de compra periódicas**.
4. En la página **Líneas de compras periódicas**, elija el botón de búsqueda en el campo **Código** y seleccione un conjunto de líneas de compras estándar.
5. Elija el botón **Aceptar** para insertar las líneas de compras estándar en la factura, donde puede reutilizar la información tal como está o editarla.

## Consulte también .

[Compras](purchasing-manage-purchasing.md)  
[Configurar compra](purchasing-setup-purchasing.md)  
[Crear ventas periódicas](sales-how-work-standard-lines.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]