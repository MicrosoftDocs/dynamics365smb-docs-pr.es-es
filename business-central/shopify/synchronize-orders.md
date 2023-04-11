---
title: Sincronizar y cumplir con los pedidos de ventas
description: Configure y ejecute la importación y el procesamiento de pedidos de ventas desde Shopify.
ms.date: 05/27/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: '30110, 30111, 30112, 30113, 30114, 30115, 30121, 30122, 30123, 30128, 30129,'
author: edupont04
ms.author: andreipa
ms.reviewer: solsen
---

# Sincronizar y cumplir con los pedidos de ventas

Este artículo describe la configuración necesaria y los pasos que debe seguir para sincronizar y cumplir con los pedidos de ventas con Shopify en [!INCLUDE[prod_short](../includes/prod_short.md)].

## Configurar la importación de pedidos en la ficha de tienda Shopify

Introduzca un **código de moneda** si su tienda en línea utiliza una moneda diferente a la moneda local (LCY). La divisa especificada debe tener tipos de cambio configurados. Si su tienda en línea usa la misma divisa que [!INCLUDE[prod_short](../includes/prod_short.md)], deje el campo vacío. 

Puede ver la moneda de la tienda en la configuración de [Detalles de la tienda](https://www.shopify.com/admin/settings/general) en su Administrador de Shopify. Shopify se puede configurar para aceptar diferentes monedas, sin embargo, los pedidos importados a [!INCLUDE[prod_short](../includes/prod_short.md)] utilizan la moneda de la tienda.

Un pedido regular de Shopify puede incluir costes adicionales al subtotal, como los gastos de envío o, si está activado, las propinas. Estos importes se contabilizan directamente en la cuenta de contabilidad que se desea utilizar para los tipos de transacción específicos:

* **Cta. cargos envío**
* **Cuenta de tarjeta de regalo vendida**; obtenga más información en [Tarjeta regalo](synchronize-orders.md#gift-cards)
* **Cuenta de propina**  

Habilite **Crear pedidos automáticamente** para crear automáticamente documentos de ventas en [!INCLUDE[prod_short](../includes/prod_short.md)], una vez que se importe el pedido de Shopify.

Si desea liberar automáticamente un documento de ventas, active la opción **Liberación automática de pedidos de venta**.

El documento de ventas en [!INCLUDE[prod_short](../includes/prod_short.md)] se vincula al pedido de Shopify y puede agregar un campo que aún no se muestra en la página. Para obtener más información sobre cómo agregar un campo, vaya a [Para comenzar a personalizar una página a través del banner **Personalizar**](../ui-personalization-user.md#to-start-personalizing-a-page-through-the-personalizing-banner) . Si selecciona el campo **N.º de pedido de Shopify en línea de documento**, entonces esta información se repite en las líneas de ventas de tipo **Comentario**.

En el campo **Origen del área fiscal**, defina la prioridad sobre cómo seleccionar el código de área fiscal o el grupo contable comercial de IVA en función de la dirección. El pedido importado de Shopify contiene información sobre los impuestos, pero estos se recalculan cuando se crea el documento de venta, por lo que es importante que la configuración del IVA/impuestos sea correcta en [!INCLUDE[prod_short](../includes/prod_short.md)]. Para obtener más información acerca de los impuestos, consulte [Configurar impuestos para la conexión Shopify](setup-taxes.md).

### Asignación de método de envío

El **Código de método de envío** para documentos de venta importados desde Shopify, se puede rellenar automáticamente. Necesita configurar la **Asignación de métodos de envío**.

1. Elija el icono ![Bombilla que abre la función Dígame 1.](../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Tiendas de Shopify** y luego elija el enlace relacionado.
2. Seleccione la tienda para la que desea definir una asignación para abrir la página **Ficha de tienda de Shopify**.
3. Elija la acción **Asignación de métodos de envío**. Esto crea automáticamente registros de los métodos de envío definidos en la configuración de [**Envío**](https://www.shopify.com/admin/settings/payments) del **administrador de Shopify**.
4. En el campo **Nombre**, puede ver el nombre del método de envío desde Shopify.
5. Introduzca el **Código de método de envío** con el método de envío correspondiente en [!INCLUDE[prod_short](../includes/prod_short.md)].

> [!NOTE]  
> Si varios cargos de envío están asociados con un pedido de ventas, solo se seleccionará uno como Método de envío y se asignará al documento de ventas.

### Asignación de ubicación

La asignación de ubicación es necesario para tres propósitos:

* Para sincronizar el inventario, para obtener más información, consulte [Sincronizar inventario para Shopify](synchronize-items.md#sync-inventory-to-shopify)
* Para llenar el **Código de almacén** para documentos de venta importados de Shopify. Esto es importante cuando el conmutador de alternancia **Ubicación obligatoria** está habilitado en la ficha **Configuración de inventario**, de lo contrario no podrá crear documentos de ventas.
* Para actualizar el pedido Shopify con la información de cumplimiento basada en la página **Histórico albaranes venta**.

1. Elija el icono ![Bombilla que abre la función Dígame 1.](../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Tiendas de Shopify** y luego elija el enlace relacionado.
2. Seleccione la tienda para la que desea configurar la asignación de ubicaciones para abrir la página **Ficha de tienda de Shopify**.
3. Elija la acción **Ubicaciones** para abrir las **Ubicaciones de tiendas de Shopify**.
4. Elija la acción **Obtener ubicaciones de Shopify** para importar todas las ubicaciones definidas en Shopify. Puedes encontrarlas en la configuración de [**Ubicaciones**](https://www.shopify.com/admin/settings/locations), en el panel **Administrador de Shopify**. Tenga en cuenta que la ubicación marcada como *Predeterminada* se usará al importar los pedidos no rellenados de Shopify.
5. Introduzca el **Código de ubicación predeterminado** con la ubicación correspondiente en [!INCLUDE[prod_short](../includes/prod_short.md)].

## Ejecutar la sincronización de pedidos

El siguiente procedimiento describe cómo importar y actualizar pedidos de venta.

> [!NOTE]  
> Los pedidos archivados en Shopify no se pueden importar Desactive la opción **Archivar automáticamente el pedido** en la sección **Procesamiento de pedidos** de los ajustes de **Finalizar compra** del panel **Administrador de Shopify** para asegurarse de que todos los pedidos se importen a [!INCLUDE[prod_short](../includes/prod_short.md)]. Si necesita importar pedidos archivados, utilice la acción **Desarchivar pedidos** en la página [Pedidos](https://www.shopify.com/admin/orders) del panel **Administrador de Shopify**.

1. Elija el icono ![Bombilla que abre la función Dígame 1.](../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Tiendas de Shopify** y luego elija el enlace relacionado.
2. Seleccione la tienda para la que desea importar pedidos para abrir la página **Tarjeta de tienda de Shopify**.
3. Seleccione la acción **Pedidos**.
4. Elija la acción **Sincronizar usuarios desde Shopify**.
5. Defina filtros en los pedidos según sea necesario. Por ejemplo, puede importar pedidos totalmente pagados o con bajo nivel de riesgo.

> [!NOTE]  
> Al filtrar por etiqueta, debe usar tokens de filtro `@` y `*`. Por ejemplo, si desea importar pedidos que contengan *tag1*, utilice `@*tag1*`. `@` se asegurará de que el resultado no tenga en cuenta mayúsculas y minúsculas, mientras que `*` busca pedidos con varias etiquetas.

6. Elija el botón **Aceptar**.

Alternativamente, puede buscar el trabajo por lotes **Sincronizar pedidos desde Shopify**.

Puede programar la tarea para que se realice automáticamente. Obtenga más información en [Programar tareas recurrentes](background.md#to-schedule-recurring-tasks).

## Revisar pedidos importados

Una vez completada la importación, puede explorar el pedido de Shopify y encontrar toda la información relacionada, como transacciones de pago, costes de envío, procesos de entrega, nivel de riesgo, atraibutos y etiquetas de pedidos o los cumplimientos, si el pedido ya se cumplió en Shopify. También puede ver la confirmación de cualquier pedido que se haya enviado al cliente seleccionando la acción **Página de estado de Shopify**.

> [!NOTE]  
> Puede navegar a la ventana **Pedidos de Shopify** directamente y podrá ver pedidos con estado *abierto* de todas las tiendas. Para revisar los pedidos completados, debe abrir la página **Pedidos de Shopify** desde la ventana **Tarjeta de tienda de Shopify** específica.

## Crear documentos de ventas en Business Central

Si el conmutador de alternancia **Crear pedidos automáticamente** está habilitado en **Tarjeta de tienda de Shopify**, [!INCLUDE[prod_short](../includes/prod_short.md)] intenta crear un documento de ventas después de que se importa el pedido. Si se producen problemas, como la falta de un cliente o de un producto, tendrá que solucionarlos y volver a crear el pedido de venta.

### Para crear documentos de venta

1. Elija el icono ![Bombilla que abre la función Dígame 1.](../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Tiendas de Shopify** y luego elija el enlace relacionado.
2. Seleccione la tienda para la que desea sincronizar pedidos para abrir la página **Tarjeta de tienda de Shopify**.
3. Seleccione la acción **Pedidos**.
4. Seleccione el pedido para el que desea crear un documento de ventas y elija la acción **Crear documento de ventas**.
5. Elija **Sí**.

Si el pedido de Shopify requiere proceso de entrega, se crea un **Pedido de ventas**. Para pedidos Shopify entregados, como aquellos pedidos que contienen solo una tarjeta de regalo o que ya se controlan en Shopify, se crea una **Factura de venta**.

Ahora se crea un documento de ventas y se puede administrar utilizando la funcionalidad [!INCLUDE[prod_short](../includes/prod_short.md)] estándar.

### Gestionar clientes perdidos

Si su configuración impide crear un cliente automáticamente y no se puede encontrar un cliente existente adecuado, deberá asignar un cliente al pedido de Shopify manualmente. Existen varias formas de hacer esto:

* Puede asignar el **N.º de venta al cliente** y **Nº de cliente de facturación** directamente en la página **Pedidos de Shopify**, eligiendo un cliente de la lista de clientes existentes.
* Puede seleccionar un código de plantilla de cliente, crear y asignar el cliente a través de la acción **Crear nuevo cliente** en la página **Pedidos de Shopify**. Tenga en cuenta que el cliente de Shopify debe tener al menos una dirección. A los pedidos creados a través del canal de ventas Shopify POS a menudo les faltan los detalles de la dirección.
* Puede asignar un cliente existente al **Cliente de Shopify** relacionado en la ventana **Clientes de Shopify** y luego elegir la acción **Buscar asignación** en la página **Pedidos de Shopify**.

### Cómo el conector elige qué cliente usar

La función *Importar pedido de Shopify* intenta seleccionar los clientes en el siguiente orden:

1. Si el campo **N.º de cliente genérico** se define en la **Plantilla de cliente de Shopify** para el país correspondiente, se usa el **N.º de cliente genérico** independientemente de los ajustes de los campos **Importar cliente desde Shopify** y **Tipo de asignación de cliente**. Más información en [Plantilla de cliente por país](synchronize-customers.md#customer-template-per-country).
2. Si **Importar clientes desde Shopify** está establecido en *Ninguno* y el **N.º de cliente genérico** se define en la página **Shopify Tarjeta de tienda**, luego el **N.º de cliente genérico** .

Los próximos pasos dependen del **Tipo de asignación de cliente**.

* Si es **Tomar siempre el cliente predeterminado**, el conector usa el cliente definido en el campo **N.º de cliente predeterminado** en la página **Ficha de tienda de Shopify**.
* Si es **Por correo electrónico/teléfono**, el conector intenta encontrar el cliente existente primero por id., luego por correo electrónico y luego por número de teléfono. Si no se encuentra el cliente, el conector crea un nuevo cliente.
* Si es **Por información de dirección de facturación**, el conector intenta encontrar el cliente existente primero por id. y luego por la información de dirección de facturación. Si no se encuentra el cliente, el conector crea un nuevo cliente.

> [!NOTE]  
> El conector utiliza la información de la dirección de facturación y crea el cliente de facturación en [!INCLUDE[prod_short](../includes/prod_short.md)]. El cliente de venta es el mismo que el cliente de facturación.

### Impacto de las modificaciones de pedidos

En Shopify:

|Editar|Impacto para pedido ya importado|Impacto para el pedido que se importa por primera vez|
|------|-----------|-----------|
|Cambiar la ubicación de proceso de entrega | La ubicación original está en las líneas | La ubicación de proceso de entrega está sincronizada con [!INCLUDE[prod_short](../includes/prod_short.md)].|
|Editar un pedido y aumentar la cantidad| El encabezado del pedido y las tablas complementarias se actualizarán en [!INCLUDE[prod_short](../includes/prod_short.md)], las líneas no lo harán.| El pedido importado usará una nueva cantidad|
|Editar un pedido y disminuir la cantidad| El encabezado del pedido y las tablas complementarias se actualizarán en [!INCLUDE[prod_short](../includes/prod_short.md)], las líneas no lo harán.| El pedido importado usará la cantidad original, el campo Cantidad a cumplir contendrá un nuevo valor.|
|Editar un pedido y eliminar un producto existente | El encabezado del pedido y las tablas complementarias se actualizarán en [!INCLUDE[prod_short](../includes/prod_short.md)], las líneas no lo harán.| El producto eliminado aún se importará, el campo Cantidad a cumplir contendrá cero. |
|Editar un pedido y agregar un nuevo artículo | El encabezado del pedido se actualizará, las líneas no. | Se importarán los elementos originales y añadidos. |
|Procesar pedido: cumplir, actualizar información de pago | El encabezado del pedido se actualizará, pero las líneas no. |El cambio no tiene impacto sobre cómo se importa el pedido.|
|Cancelar pedido | El encabezado del pedido se actualizará, pero las líneas no. |El pedido cancelado no se importa |

En [!INCLUDE[prod_short](../includes/prod_short.md)]:

|Editar|Impacto|
|------|-----------|
|Cambie la ubicación a otra ubicación, asignada a las ubicaciones de Shopify. Registre el envío. | El pedido se marcará como entregado. Se utilizará el almacén original. |
|Cambie la ubicación a otra ubicación, no asignada a las ubicaciones de Shopify. Registre el envío. | El proceso de entrega no se sincronizará con Shopify. |
|Disminuya la cantidad. Registre el envío. | El pedido de Shopify se marcará como parcialmente entregado. |
|Incremente la cantidad. Registre el envío. | El proceso de entrega no se sincronizará con Shopify. |
|Agregue un artículo nuevo. Registre el envío. | El pedido de Shopify se marcará como entregado. Las líneas no se actualizarán. |

## Sincronizar envíos a Shopify

Cuando un pedido de venta que se crea a partir de un pedido de Shopify se envía, puede sincronizar los envíos con Shopify.

1. Elija el icono ![Bombilla que abre la función Dígame 1.](../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Sincronizar envíos a Shopify** y, a continuación, elija el vínculo relacionado.
2. Defina los filtros en los envíos según sea necesario. Por ejemplo, puede actualizar un envío registrado en una fecha específica.
3. Elija el botón **Aceptar**.

El pedido de Shopify se marcará como cumplido. El cliente recibe automáticamente un aviso de envío por correo electrónico o mensaje de texto (SMS). Si se especifican un agente de envío y un código de seguimiento en el envío, la información de seguimiento se incluye en el correo electrónico.

Como alternativa, utilice la acción **Sincronizar envíos** en los pedidos de ventas de Shopify o páginas de la tienda Shopify.

Puede programar la tarea para que se realice de forma automatizada. Obtenga más información en [Programar tareas recurrentes](background.md#to-schedule-recurring-tasks).

>[!Important]
>La ubicación, incluida la ubicación en blanco, definida en la línea de envío contabilizado, debe tener un registro coincidente en el almacén de Shopify. De lo contrario, esta línea no se devolverá a Shopify. Obtenga más información en [Asignación de almacén](synchronize-orders.md#location-mapping).

Recuerde ejecutar **Sincronizar pedidos desde Shopify** para actualizar el estado de proceso de entrega de un pedido en [!INCLUDE[prod_short](../includes/prod_short.md)]. La funcionalidad del conector también archiva pedidos completamente pagados y procesados en Shopify y [!INCLUDE[prod_short](../includes/prod_short.md)], siempre que se cumplan las condiciones.

### Agentes de envío y URL de seguimiento

Si el documento **Histórico albaranes venta** contiene el **Código de agente de envío** y/o el **Número de seguimiento del paquete**, esta información se enviará a Shopify y al cliente final en el correo electrónico de confirmación de envío.

La empresa de seguimiento se rellena en el siguiente orden (de mayor a menor) según el registro de la agencia de transporte:

* **Empresa de seguimiento de Shopify**
* **Nombre**
* **Código**

Si el campo **URL de seguimiento del paquete** se rellena para el registro del agente de envío, luego la confirmación de envío también contendrá una URL de seguimiento.

## Tarjetas regalo

En la tienda Shopify puede vender tarjetas de regalo, que se pueden usar para pagar productos reales.

Cuando se trata de tarjetas de regalo, es importante introducir un valor en el campo **Cuenta de tarjeta de regalo vendida**, en la ventana **Tarjeta de tienda de Shopify**. La tarjeta de regalo vendida se sincronizará junto con los pedidos en línea. Una tarjeta de regalo aplicada también se importará con el pedido, pero ahora como una transacción. Tenga en cuenta que la tarjeta de regalo no reduce el importe a facturar.

Para revisar las tarjetas de regalo emitidas y aplicadas, elija el icono ![Bombilla que abre la función Dígame.](../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Tarjetas regalo** y luego elija el enlace relacionado.

## Consulte también .

[Comenzar con el conector para Shopify](get-started.md)  
