---
title: Cómo crear productos de servicio
description: 'Lea acerca de las diferentes formas en que puede crear productos de servicio en Business Central, por ejemplo, en una orden de servicio o al enviar artículos.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.search.keywords: null
ms.date: 03/22/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Crear prods. servicio

En [!INCLUDE[prod_short](includes/prod_short.md)], el término “producto de servicio” se refiere el equipo o productos que requieren servicio. Al crear un pedido de servicio, se especifican los productos que necesitan servicio. En el pedido, puede vincular un producto de servicio a un producto en existencias o un grupo de productos de servicio.

Cuando reciba un producto que necesita servicio, puede registrarlo como un producto de servicio. Existen varias formas de hacerlo. Por ejemplo, puede crear un producto de servicio en la página **Productos de servicio**, o como parte de otro proceso, por ejemplo al trabajar con un pedido de servicio.

## Para crear un producto de servicio

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Productos de servicio** y luego elija el enlace relacionado.
2. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## Para crear productos de servicio en un pedido de servicio

Cuando se reciben productos para servicio que desea registrar como productos de servicio, puede crearlos como productos de servicio en las páginas **Pedido servicio** u **Oferta servicio**.  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pedidos de servicio** y luego elija el enlace relacionado.  
2. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Elija la acción **Crear producto de servicio**.  

    Se asignará un número al artículo de servicio y se creará una ficha de artículo de servicio. El campo **Nº producto servicio** se rellenará con el número del nuevo producto de servicio.

## Para crear un producto de servicio al enviar productos

Cuando se envían los productos al registrar los pedidos o las facturas de venta, los productos enviados se registran automáticamente como productos de servicio cuando se cumple la condición siguiente. Los artículos deben pertenecer a un grupo de artículo de servicio con la casilla **Crear prod. servicio** activada. Si los artículos tienen números de serie registrados en la página Líns. seguim. prod., esta información se copiará automáticamente al campo **Nº serie** en la ficha de artículo de servicio al crear artículos de servicio.  

El siguiente procedimiento muestra cómo crear productos de servicio al enviar productos de pedidos de venta.  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pedidos de venta** y, a continuación, elija el vínculo relacionado.  
2. Abra el pedido de venta correspondiente.  
3. Seleccione la acción **Registrar** o **Registrar e imprimir**.  
4. Seleccione la acción **Enviar** o **Enviar y facturar**.  
5. Se crearán automáticamente productos de servicio para los productos del pedido, siempre que pertenezcan a un grupo de productos de servicio que se ha configurado para crear productos de servicio. Si ha registrado números de serie específicos en la página **Líns. seguim. prod.**, éstos se asignarán a los productos de servicio.  

> [!NOTE]  
> Si un producto es una L.M. y la ha desplegado, los productos de la L.M. desplegada se procesarán de la misma forma que los productos comunes. Los productos de servicio se crean en base a la condición del grupo de productos de servicio y, de manera opcional, en la condición de los números de serie. Además, si se crea un producto de servicio para un producto de la L.M. desplegada compuesto por otros componentes de la L.M., estos productos se crearán como componentes de un producto de servicio para el producto de servicio de la L.M. desplegada.  
>
> Si un producto es una L.M. y no ha desplegado la L.M., se crea un producto de servicio para aquel basándose en la condición del grupo de productos de servicio y, de manera opcional, en la condición de los números de serie.  

## Para insertar un gasto de inicio para un producto de servicio

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Tareas de servicio** y luego elija el enlace relacionado.
2. Elija la acción **Hoja de producto**.
3. Seleccione la línea de servicio y, a continuación elija **Acciones**, seleccione **Funciones** y luego la acción **Insertar cuota inicial**.  

    Se insertará una línea de servicio del tipo **Coste** con el gasto de inicio. El gasto de inicio se aplica al producto de servicio seleccionado.

## Bloquear artículos, variantes de artículos o artículos de servicio específicos

Puede evitar que se utilicen artículos, variantes de artículo o artículos de servicio en transacciones de gestión de servicios, como contratos de servicio, órdenes de servicio y facturas de servicio. Esto puede resultar útil si desea restringir la disponibilidad de algunos artículos o artículos de servicio para fines de servicio, por ejemplo, debido a la interrupción del soporte, stock limitado o acuerdos contractuales.

Para bloquear el uso de un artículo o una variante de artículo en transacciones de gestión de servicios, active la opción **Servicio bloqueado** en la **Tarjeta de artículo**, **Variantes de artículo** y página **Tarjeta de variante de artículo**. También puede configurar este campo en la página **Plantilla de artículos**, y se copiará en los artículos creados a partir de esa plantilla.

Cuando el servicio bloquea un artículo o una variante de artículo, no está disponible para su selección en las siguientes páginas:

- Línea de servicio (excepto notas de crédito de servicio, donde verá una notificación de que el artículo o variante está bloqueado, pero permitido en este tipo de documento)
- Artículo servicio
- Línea contrato servicio
- Línea servicio estándar

Si ingresa manualmente un número de artículo o variante que está bloqueado, recibirá un mensaje de error que indica: "El campo contiene un valor que no se puede encontrar en la tabla relacionada".

Además, si tiene contratos de servicio, cotizaciones de contratos de servicio u órdenes de servicio que incluyen artículos de servicio bloqueados o variantes de artículos, no puede utilizar las siguientes acciones:

- **Bloquear** o **Hacer contrato** en la página **Oferta de contrato de servicio**.
- **Bloquear contrato**, **Firmar contrato**, **Crear órdenes de servicio de contrato** o **Crear facturas de contrato**  en la página **Contrato de servicio**.
- **Convertir en pedido** en la página **Oferta de servicio**.
- **Liberar para enviar** o **Registrar** en la página **Orden de servicio**.
- **Registrar** en la página **Factura de servicio**.

### Bloquear un artículo de servicio

Para bloquear el uso de un artículo de servicio en transacciones de gestión de servicios, en la página **Tarjeta de artículo de servicio**, en el campo **Bloqueado**, elija una de las siguientes opciones:

- **Contrato de servicio**: bloquea el uso del elemento de servicio en contratos de servicio y cotizaciones de contratos de servicio, pero no en órdenes de servicio u otros documentos de servicio.
- **Todo**: bloquea el uso del elemento de servicio en cualquier transacción de administración de servicio, incluyendo contratos de servicio, órdenes de servicio y otros documentos de servicio.

Cuando un elemento de servicio está bloqueado, no puede seleccionarlo en las siguientes páginas:

- Línea de contrato de servicio (si está bloqueada para el contrato de servicio o para todos)
- Línea de artículo de servicio (excepto notas de crédito de servicio, si están bloqueadas para todos)

Si ingresa manualmente un número de artículo de servicio para un articulo de servicio está bloqueado, recibirá el mensaje de error "El campo contiene un valor que no se puede encontrar en la tabla relacionada".

Además, si tiene contratos de servicio, cotizaciones de contratos de servicio u órdenes de servicio que incluyen artículos de servicio bloqueados, no puede utilizar las siguientes acciones:

- **Bloquear** y **Convertir en contrato** en la página **Oferta de contrato de servicio** (si está bloqueada para servicio contrato, o todos).
- **Bloquear contrato**, **Firmar contrato** o **Cambiar cliente** en la página **Contrato de servicio** (si está bloqueado para contrato de servicio o todos).
- **Convertir en pedido** en la **Oferta de servicio** (si está bloqueado para todos).
- **Liberar para enviar** o **Registrar** en la página **Orden de servicio** (si está bloqueado para todos. Si los documentos de orden de servicio contienen varios artículos de servicio y algunos están bloqueados y otros no, puede liberar y publicar líneas no bloqueadas. Considere si desea activar la opción **Línea/pedido de un artículo de servicio** en la página **Configuración de administración de servicios**).
- **Registrar** en la página **Factura de servicio** (si está bloqueado para todos).

También puede ver los elementos de servicio bloqueados aplicando un filtro a los siguientes informes:

- Artículos de servicio (informe 5935)
- Artículos de servicio fuera de garantía (informe 5937)
- Beneficio de servicio (artículos de servicio) (informe 5938)

### Actualización de datos

Esta característica no requiere configuración adicional. Sin embargo, si actualiza su [!INCLUDE [prod_short](includes/prod_short.md)], tenga en cuenta lo siguiente:

- Si tiene artículos, variantes de artículos o plantillas de artículos donde la opción **Ventas bloqueadas** está activada, el campo **Servicio bloqueado** también se activa para esos registros durante la actualización. Esto garantiza que la lógica de bloqueo de ventas existente también se aplique a las transacciones de gestión de servicios.
- Actualizaciones de datos solo si tiene al menos un elemento de servicio en su empresa, lo que significa que está utilizando la funcionalidad de administración de servicios y necesita la actualización de datos. Si no tiene artículos de servicio, la actualización de datos se omite y la opción **Servicio bloqueado** está desactivada de forma predeterminada para todos los artículos, variantes de artículos y plantillas de artículos.

## Consulte también

[Configurar productos de servicio y componentes de productos de servicio](service-how-setup-service-items.md)  
[Configurar la gestión de servicios](service-setup-service.md)  
[Gestión de servicios](service-service.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
