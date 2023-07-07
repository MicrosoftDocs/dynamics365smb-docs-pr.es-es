---
title: Configurar los grupos de precio de clientes
description: Obtenga información sobre cómo configurar grupos de precios para clientes y crear precios de venta para esos grupos.
author: jill-kotel-andersson
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'customer price groups, discounts, sales prices'
ms.date: 09/30/2021
ms.author: edupont
---

# <a name="set-up-customer-price-groups"></a>Configurar los grupos de precio de clientes
  
Los precios de venta pueden depender de los grupos de clientes a los que vende. Estos se denominan grupos de precio de cliente.

Para configurar los grupos de precio de clientes, primero debe decidir cuántos grupos desea tener y qué clientes estarán acogidos a cada uno de ellos.  

## <a name="how-to-create-sales-prices-for-a-group-of-customers"></a>Cómo crear precios de venta para un grupo de clientes

Cuando tenga un acuerdo sobre los precios que pagará el grupo de clientes por determinados productos, registre el acuerdo para cada producto en las líneas de la página **Precios venta**.

### <a name="to-create-sales-prices-for-a-group-of-customers"></a>Para crear precios de venta para un grupo de clientes

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Grupos precio cliente** y, a continuación, elija el vínculo relacionado.  

2. Seleccione la línea para el grupo de precios de cliente. Si aún no existe una línea, puede crear una nueva línea. Seleccione **Nueva** para crear una nueva entidad y darle un nombre.  
    
    Para la línea seleccionada, verifique el contenido de los campos **Permitir descuento de línea**, **Precio con impuestos incluidos**, **El precio incluye impuestos** y **Gr.regis. IVA negocio (precio)**. 
  
3. Seleccione la acción **Navegar** y elija **Precios de venta**. Se abre la página **Precios de ventas**. El campo **Tipo de venta** se completará con **Grupo precio cliente**.  
  
4. Complete el **Código de venta** con el código de venta que seleccionó en la página anterior.  
  
5. Rellene los campos de las líneas con el **N.º producto**, el **Código de unidad medida** y el **Precio unitario** acordado. También puede mostrar la columna **Cód. variante** y especificar el **Cód. variante** si hay diversas variantes del producto.  
  
6. Si el grupo de clientes necesita comprar una cantidad mínima para obtener el precio acordado, rellene al campo **Cantidad mínima**.  

7. Si es necesario, escriba la **Fecha inicial** y la **Fecha final** del acuerdo sobre precios.  
  
8. Si es relevante, también puede especifiar el **Código de divisa**.

Repita los pasos 4 a 8 por cada producto para el que desea crear un precio de venta.

## <a name="how-to-enter-customer-price-group-codes-on-customer-cards"></a>Cómo introducir los códigos de grupos de precio de cliente en las fichas de clientes

Después de configurar los grupos de precio de cliente, introduzca códigos respectivos en las fichas de clientes.

### <a name="to-enter-customer-price-group-codes-on-a-customer-card"></a>Para introducir los códigos de grupos de precio de cliente en la ficha de clientes

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Clientes** y luego elija el enlace relacionado.  

2. Abra la **Ficha cliente** que corresponda al cliente que desea que forme parte de un grupo de precios de cliente.  

3. En la ficha desplegable **Facturación**, en el campo **Grupo precio cliente**, seleccione el código **Grupo precio cliente**.  


## <a name="see-also"></a>Consulte también

[Ccial](sales-manage-sales.md)  
[Configuración de ventas](sales-setup-sales.md)  
[Registrar precios y descuentos de ventas especiales](sales-how-record-sales-price-discount-payment-agreements.md)  
[Configuración de grupos de descuento de cliente](sales-how-to-set-up-customer-discount-groups.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
