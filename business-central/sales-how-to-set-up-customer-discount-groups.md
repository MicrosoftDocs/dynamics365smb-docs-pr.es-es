---
title: Configurar grupos de descuento para clientes
description: Obtenga información sobre cómo configurar grupos de descuento para clientes y crear descuentos de líneas de venta para esos grupos.
author: brentholtorf
ms.service: dynamics-365-business-central
ms.topic: article
ms.date: 07/05/2024
ms.author: bholtorf
ms.reviewer: bholtorf
---
# Configurar grupos de descuento para clientes

Puede definir descuentos de línea de venta para un grupo de clientes en lugar de aplicarlos individualmente.

**Los grupos de descuento de clientes** son similares a los [grupos de precios de clientes](sales-how-to-set-up-customer-price-groups.md), pero se pueden combinar con grupos de descuento de artículos para establecer rápidamente descuentos de línea para muchos artículos para clientes seleccionados.

## Crear descuentos en la línea de ventas para un grupo de clientes

1. Elija el icono ![Bombilla que abre la característica Dígame 1.](media/ui-search/search_small.png "Dígame qué desea hacer") icono, escriba **Grupos desc. clientes** y, a continuación, elija el vínculo relacionado.
2. En la página **Grupos desc. clientes**, seleccione **Nuevo** para crear un nuevo grupo de descuento y darle un nombre en la columna **Código** y agregue una descripción.
3. Seleccione la acción  **Descuentos en líneas de venta** .
4. Complete la columna **Código de venta** con el grupo de descuento creado en la página anterior.
5. Rellene los campos de las líneas con el **Tipo** (grupo de descuento de productos o producto), **Código**, **Código de unidad de medida** y el **% de descuento de la línea**.
6. Si el grupo de clientes necesita comprar una cantidad mínima para obtener el descuento acordado, rellene al campo **Cantidad mínima**.
7. Si es necesario, introduzca la **Fecha inicial** y la **Fecha final** del para el grupo de descuento.
8. Si es relevante, también puede especificar el **Código de divisa** o **Código de variante** después de [personalizar las columnas](ui-personalization-user.md).

Repita los pasos 4 a 8 para cada producto o grupo de descuento de productos para el que desee crear un descuento en la línea de ventas.

## Asignar un cliente a un grupo de descuento

Después de configurar los grupos de descuento de clientes, puede ingresar los códigos de grupo de descuento de clientes en el cliente Tarjetas.

1. Elija el icono ![Bombilla que abre la característica Dígame 1.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Clientes** y luego elija el enlace relacionado.
2. Abra la **Ficha cliente** para el cliente que desea que forme parte de un grupo de descuentos de cliente.
3. En la ficha desplegable **Facturación** en el campo **Grupo desc. de cliente**, seleccione el código de grupo.

## Consulte también .

[Ccial](sales-manage-sales.md)  
[Configuración de ventas](sales-setup-sales.md)  
[Registrar precios y descuentos de ventas especiales](sales-how-record-sales-price-discount-payment-agreements.md)  
[Configurar los grupos de precio de clientes](sales-how-to-set-up-customer-price-groups.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
