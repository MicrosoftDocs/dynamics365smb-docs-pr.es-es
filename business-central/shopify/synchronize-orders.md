---
title: Sincronizar y cumplir con los pedidos de ventas
description: Configure y ejecute la importación y el procesamiento de pedidos de ventas desde Shopify.
ms.date: 05/16/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
ms.reviewer: solsen
ms.openlocfilehash: e7c54cc620011d238942c093a05918e2f4e57c7d
ms.sourcegitcommit: f071aef3660cc3202006e00f2f790faff849a240
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/18/2022
ms.locfileid: "8768138"
---
# <a name="synchronize-and-fulfill-sales-orders"></a>Sincronizar y cumplir con los pedidos de ventas

Este artículo describe la configuración necesaria y los pasos que debe realizar para sincronizar y cumplir con los pedidos de ventas.

## <a name="set-import-of-orders-on-the-shopify-shop-card"></a>Configurar la importación de pedidos en la tarjeta de tienda Shopify

Un pedido regular de Shopify puede tener montos adicionales en la parte superior, como gastos de envío o, si están habilitadas, propinas. Estos importes se contabilizarán directamente en las cuentas de mayor. Elija la cuenta de mayor que debe usarse para transacciones específicas:

- **Importe de gastos de envío**
- **Cuenta de tarjeta de regalo vendida**, para más información, vea [Tarjeta de regalo](synchronize-orders.md#gift-cards).
- **Cuenta de propina**  

Habilite **Crear pedidos automáticamente** para crear automáticamente documentos de ventas en [!INCLUDE[prod_short](../includes/prod_short.md)] una vez que se importe el pedido de Shopify.
El documento de ventas de [!INCLUDE[prod_short](../includes/prod_short.md)] contiene un enlace al pedido de Shopify. Si habilita **N.º de pedido de Shopify en línea de documento**, entonces esta información se repetirá en la línea de ventas de tipo *Comentario*.

En el campo **Origen del área fiscal**, puede definir la prioridad sobre cómo seleccionar el código de área fiscal o el grupo contable comercial de IVA en función de la dirección. Este paso es relevante para países con impuestos sobre las ventas, pero puede usarse para países con IVA. Para obtener más información, consulte [Observaciones sobre impuestos](synchronize-orders.md#tax-remarks).

### <a name="shipment-method-mapping"></a>Asignación de método de envío

**Código de método de envío** para documentos de venta importados de Shopify, se puede rellenar automáticamente. Necesita configurar **Asignación de métodos de envío**.

1. Vaya al icono de búsqueda ![Bombilla que abre la función Dígame](../media/ui-search/search_small.png "Dígame qué desea hacer"). , escriba **Tienda de Shopify** y luego elija el vínculo relacionado.
2. Seleccione la tienda para la que desea definir la asignación para abrir la página **Tarjeta de tienda de Shopify**.
3. Elija la acción **Asignación de métodos de envío**. Los registros de los métodos de envío definidos en la configuración de [**Envío**](https://www.shopify.com/admin/settings/payments) del **administrador de Shopify** se crean automáticamente.
4. En el campo **Nombre**, puede ver el nombre del método de envío desde Shopify.
5. Introduzca el **Código de método de envío** con el método de envío correspondiente en [!INCLUDE[prod_short](../includes/prod_short.md)].

> [!NOTE]  
> Si varios cargos de envío están asociados con un pedido de ventas, solo se seleccionará uno como Método de envío y se asignará al documento de ventas.

### <a name="payment-method-mapping"></a>Asignación de método de pago

Para llenar el **Código de método de pago** para documentos de venta importados de Shopify automáticamente, necesita configurar **Asignación de métodos de pago**.

1. Vaya al icono ![Bombilla que abre la función Dígame](../media/ui-search/search_small.png "Dígame qué desea hacer") de búsqueda. , escriba **Tienda de Shopify** y luego elija el vínculo relacionado.
2. Seleccione la tienda para la que desea definir la asignación para abrir la página **Tarjeta de tienda de Shopify**.
3. Elija la acción **Asignación de métodos de pago**.
4. En los campos **Puerta de enlace** y **Compañía de tarjeta de crédito**, introduzca el nombre del método de pago de Shopify. El registro se crea automáticamente cuando importa pedidos de Shopify.
5. Introduzca el **Código de método de pagoo** con el método de pago correspondiente en [!INCLUDE[prod_short](../includes/prod_short.md)].
6. Seleccione la **Prioridad** para los casos en que el cliente utilice múltiples medios de pago. El método de pago con la prioridad más alta se selecciona en el documento de ventas. Si ambos métodos de pago tienen la misma prioridad, se utiliza el método de pago con el importe más alto.

## <a name="run-order-synchronization"></a>Ejecutar sincronización de pedidos

El siguiente procedimiento describe cómo importar y actualizar pedidos de venta.

> [!NOTE]  
> Los pedidos archivados en Shopify no se pueden importar Desactive **Archivar automáticamente el pedido** en la sección **Procesamiento de pedidos** de los ajustes de **Finalizar compra** del **administrador de Shopify** para asegurarse de que todos los pedidos se importen a [!INCLUDE[prod_short](../includes/prod_short.md)]. Si necesita importar pedidos archivados, utilice la acción **Desarchivar pedidos** de la página [Pedidos](https://www.shopify.com/admin/orders) del administrador de Shopify.

1. Vaya al icono ![Bombilla que abre la función Dígame](../media/ui-search/search_small.png "Dígame qué desea hacer") de búsqueda. , escriba **Tienda de Shopify** y luego elija el vínculo relacionado.
2. Seleccione la tienda para la que desea importar pedidos para abrir la página **Tarjeta de tienda de Shopify**.
3. Seleccione la acción **Pedidos**.
4. Elija la acción **Sincronizar usuarios desde Shopify**.
5. Defina filtros en los pedidos según sea necesario. Por ejemplo, puede importar pedidos totalmente pagados o con bajo nivel de riesgo.
6. Elija el botón **Aceptar**.

Alternativamente, puede buscar el trabajo por lotes **Sincronizar pedidos desde Shopify**.

Una vez completada la importación, puede explorar el pedido de Shopify y encontrar toda la información relacionada, como transacciones de pago, costes de envío, procesos de entrega, nivel de riesgo. También puede ver la confirmación del pedido enviada al cliente seleccionando la acción **Página de estado de Shopify**.

> [!NOTE]  
> Puede navegar a la ventana **Pedidos de Shopify** directamente y podrá ver pedidos con estado *abierto* de todas las tiendas. Para revisar los pedidos completados, debe abrir la página **Pedidos de Shopify** desde la ventana de **Tarjeta de tienda de Shopify** específica.

## <a name="create-sales-document-in-business-central"></a>Crear documento de ventas en Business Central

Si la alternancias **Crear pedidos automáticamente** está habilitada en **Tarjeta de tienda de Shopify**, la [!INCLUDE[prod_short](../includes/prod_short.md)] intenta crear un documento de ventas una vez que se importa el pedido. En caso de que el proceso encuentre problemas, por ejemplo, si falta un cliente o un producto, deberá solucionar el problema e intentar crear un pedido de ventas nuevamente.

### <a name="to-create-sales-document"></a>Para crear un documento de venta

1. Vaya al icono ![Bombilla que abre la función Dígame](../media/ui-search/search_small.png "Dígame qué desea hacer") de búsqueda. , escriba **Tienda de Shopify** y luego elija el vínculo relacionado.
2. Seleccione la tienda para la que desea sincronizar pedidos para abrir la página **Tarjeta de tienda de Shopify**.
3. Seleccione la acción **Pedidos**.
4. Seleccione el pedido para el que desea crear un documento de ventas y elija la acción **Crear documento de ventas**.
5. Elija **Sí**.

Si el pedido de Shopify requiere proceso de entrega, se creará el **Pedido de ventas** para los pedidos entregados de Shopify. Por ejemplo, para los que contienen solo una tarjeta de regalo, se crea la **Factura de venta**.

Ahora se crea un documento de ventas y se puede administrar utilizando las funcionalidades [!INCLUDE[prod_short](../includes/prod_short.md)] estándar.

### <a name="manage-missing-customers"></a>Gestionar clientes perdidos

Si su configuración impide crear un cliente automáticamente y no se puede encontrar un cliente existente adecuado, asignará un cliente al pedido de Shopify manualmente. Existen algunas opciones:

- Puede asignar el **N.º de venta al cliente** directamente en el **Pedido de Shopify**, eligiendo un cliente de la lista de clientes existentes.
- Puede seleccionar un código de plantilla de cliente, crear y asignar el cliente a través de la acción **Crear nuevo cliente** del **Pedido de Shopify**.
- Puede asignar un cliente existente al **Cliente de Shopify** relacionado en la ventana **Clientes de Shopify** y luego elija la acción **Buscar mapeo** en el **Pedido Shopify**.

### <a name="tax-remarks"></a>Observaciones sobre impuestos

Mientras que el pedido de Shopify importado contiene información sobre impuestos, los impuestos se vuelven a calcular cuando se crea el documento de ventas. Por eso es importante que la configuración de IVA/Impuestos sea correcta en [!INCLUDE[prod_short](../includes/prod_short.md)].

- Múltiples tasas de impuestos/IVA sobre productos. Por ejemplo, algunas categorías de productos están sujetas a tipos impositivos reducidos. Esos elementos deben existir en [!INCLUDE[prod_short](../includes/prod_short.md)] y estar asignados a productos de Shopify. De lo contrario, con la creación automática de elementos faltantes, se utilizará el grupo de contabilización de productos con IVA.

- Tasas de impuestos dependientes de la dirección. Utilice el campo **Prioridad de zona fiscal** junto con la tabla **Plantillas de clientes** para sobrescribir la lógica estándar que completa el **Código de área fiscal** en el documento de venta. El campo **Prioridad de área fiscal** especifica la prioridad de dónde la función debe tomar información sobre el país/región y el estado/provincia. Luego, se encuentra el registro correspondiente en las plantillas de cliente de Shopify y se usan **Código de área fiscal**, **Sujeto a impuestos** y **Negocio con IVA. Grupo de contabilización** se utiliza cuando se crea un documento de ventas.

## <a name="synchronize-shipments-to-shopify"></a>Sincronizar envíos a Shopify

Cuando un pedido de venta que se crea a partir de un pedido de Shopify se envía, puede sincronizar los envíos a Shopify.

1. Vaya al icono ![Bombilla que abre la función Dígame](../media/ui-search/search_small.png "Dígame qué desea hacer") de búsqueda. , escriba **Sincronizar envíos a Shopify** y, a continuación, elija el vínculo relacionado.
2. Defina filtros en los envíos según sea necesario. Por ejemplo, puede actualizar el envío registrado en una fecha específica.
3. Elija el botón **Aceptar**.

El pedido de Shopify se marcará como cumplido. El cliente recibe automáticamente un aviso de envío por correo electrónico o mensaje de texto (SMS). Si se especifican un agente de envío y un código de seguimiento en el envío, la información de seguimiento se incluye en el correo electrónico.

> [!NOTE]  
> Recuerde ejecutar **Sincronizar pedidos desde Shopify** para actualizar el estado de proceso de entrega del pedido en [!INCLUDE[prod_short](../includes/prod_short.md)]. La funcionalidad del conector también archiva pedidos completamente pagados y procesados en Shopify y en [!INCLUDE[prod_short](../includes/prod_short.md)], siempre que se cumplan las condiciones.

### <a name="shipping-agents-and-tracking-url"></a>Agentes de envío y URL de seguimiento

Si el documento **Histórico albaranes venta** contiene **Código de agente de envío** y/o **Número de seguimiento del paquete**, esta información será enviada a Shopify y al cliente final en el correo electrónico de confirmación de envío.

La empresa de seguimiento se completa según el registro del agente de envío con las siguientes prioridades (de mayor a menor):

- **Empresa de seguimiento de Shopify**
- **Nombre**
- **Código**

Si el campo **URL de seguimiento del paquete** se completa para el registro del agente de envío, luego la confirmación de envío también contendrá una URL de seguimiento.

## <a name="gift-cards"></a>Tarjetas regalo

En la tienda Shopify puede vender tarjetas de regalo, que luego se pueden usar para pagar productos reales.

Cuando se trata de tarjetas de regalo, es importante introducir un valor en el campo **Cuenta de tarjeta de regalo vendida**, en la ventana **Tarjeta de tienda de Shopify**. La tarjeta de regalo vendida se sincronizará junto con los pedidos en línea. Una tarjeta de regalo aplicada también se importará con el pedido, pero ahora como una transacción. Tenga en cuenta que la tarjeta de regalo no reduce el importe a facturar.

Para revisar las tarjetas de regalo emitidas y aplicadas, elija el icono ![Bombilla que abre la función Dígame.](../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Tarjetas regalo** y luego elija el enlace relacionado.

## <a name="transactions"></a>Transacciones

Las transacciones de pago que tuvieron lugar en Shopify se sincronizan junto con los pedidos y se pueden ver desde el *Pedido de Shopify*.

Para revisar todas las transacciones, elija el icono ![Bombilla que abre la función Dígame.](../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Transacciones**, y luego seleccione el enlace relacionado.

## <a name="payouts"></a>Pagos

Si su tienda tiene habilitados Shopify Payments, recibirá pagos a través de *Pagos de Shopify* cuando un cliente paga usando Shopify Payments y finalizaciones de compra aceleradas.

1. Vaya al icono ![Bombilla que abre la función Dígame](../media/ui-search/search_small.png "Dígame qué desea hacer") de búsqueda. , escriba **Tienda de Shopify** y luego elija el vínculo relacionado.
2. Seleccione la tienda para la que desea sincronizar los pagos para abrir la página **Tarjeta de tienda de Shopify**.
3. Seleccione la acción **Sincronizar pagos**.

Para revisar todos los pagos, elija el icono ![Bombilla que abre la función Dígame.](../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pagos**, y luego seleccione el enlace relacionado.

## <a name="see-also"></a>Consulte también

[Comenzar con el conector para Shopify](get-started.md)  
