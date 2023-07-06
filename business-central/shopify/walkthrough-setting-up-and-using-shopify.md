---
title: Configurar y usar el Shopify Connector
description: Varios escenarios de integración para demostrar el flujo de trabajo entre Shopify y Business Central
ms.date: 06/21/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: '30101, 30102, 30106, 30107, 30113, 30115, 30126'
ms.reviewer: solsen
author: AndreiPanko
ms.author: andreipa
---

# <a name="walkthrough-set-up-and-use-the-shopify-connector"></a><a name="walkthrough-set-up-and-use-the-shopify-connector"></a><a name="walkthrough-set-up-and-use-the-shopify-connector"></a><a name="walkthrough-set-up-and-use-the-shopify-connector"></a>Tutorial: Configurar y usar el Shopify Connector

Esta sección muestra algunos escenarios típicos y lo guía a través de los pasos para probar o capacitar a los usuarios en el flujo de trabajo de la tienda [!INCLUDE[prod_short](../includes/prod_short.md)] integrada y Shopify.

## <a name="prerequisites"></a><a name="prerequisites"></a><a name="prerequisites"></a><a name="prerequisites"></a>Requisitos previos

### <a name="shopify"></a><a name="shopify"></a><a name="shopify"></a><a name="shopify"></a>Shopify

Debe tener:

- Una cuenta de Shopify
- Tienda en línea con Shopify

Obtenga más información sobre cómo crear pruebas y configuraciones recomendadas de Shopify en [Creación y configuración de la cuenta de Shopify](shopify-account.md).

### <a name="business-central"></a><a name="business-central"></a><a name="business-central"></a><a name="business-central"></a>Business Central

Debe tener una cuenta de [!INCLUDE[prod_short](../includes/prod_short.md)]. 

Por ejemplo, puede crear una cuenta de demostración o iniciar una prueba. Obtenga más información en [Preparar entornos de demostración de Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/administration/demo-environment) y [Registrarse para la prueba](../trial-signup.md). 

## <a name="connect-business-central-to-the-shopify-shop"></a><a name="connect-business-central-to-the-shopify-shop"></a><a name="connect-business-central-to-the-shopify-shop"></a><a name="connect-business-central-to-the-shopify-shop"></a>Conectar Business Central a la tienda de Shopify

En [!INCLUDE[prod_short](../includes/prod_short.md)], realice uno de los siguientes pasos:

1. Elija la ![Bombilla que abre la función Dígame.](../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Tiendas de Shopify** y luego elija el enlace relacionado.
2. Seleccione la acción **Nuevo**.
3. En el campo **Código**, especifique `DEMO1`.
4. En el campo **Shopify URL**, ingrese la URL de la tienda en línea a la que desea conectarse.
5. Active la alternancia **Habilitada** y revise y acepte los términos y condiciones.

Configure la tienda de Shopify como se describe en los pasos siguientes.

1. Active el botón de alternancia **Registro habilitado**.
2. Desactive la alternancia **Permitir sincronizaciones en segundo plano**.
3. Seleccione **Para Shopify**, en el campo **Sincronizar elemento**.
4. Seleccione **Para Shopify**, en el campo **Sincronizar imágenes de elementos**.
5. Active el botón de alternancia **Sincronizar atributos de elementos**.
6. Active el conmutador **Inventario con seguimiento**.
7. Seleccione **Denegar** en el campo **Política de inventario predeterminada** .
8. Active el conmutador **Creación automática de clientes desconocidos**.
9. Rellene el campo **Código de plantilla de cliente** con la plantilla adecuada.
10. Complete la **cuenta de gastos de envío**, la **Cuenta de propinas** con la cuenta de ingresos. Por ejemplo, en EE. UU., utilice `40100`.
11. Active el conmutador **Creación automática de pedidos**.

Configurar asignación de ubicación:

1. Elija la acción **Ubicaciones** para abrir **Ubicaciones de tienda de Shopify**.
2. Elija la acción **Obtener ubicaciones de Shopify** para importar todas las ubicaciones definidas en Shopify.
3. En **Filtro de ubicación**, introduzca `''|EAST|MAIN`
4. Deseleccione la alternancia **Desactivado** para habilitar la sincronización de inventario para la ubicación de Shopify seleccionada.

## <a name="walkthrough-start-selling-products-online"></a><a name="walkthrough-start-selling-products-online"></a><a name="walkthrough-start-selling-products-online"></a><a name="walkthrough-start-selling-products-online"></a>Tutorial: Comienzar a vender productos en línea

### <a name="scenario"></a><a name="scenario"></a><a name="scenario"></a><a name="scenario"></a>Escenario

Supongamos que desea probar Shopify como una tienda en línea sin perder mucho tiempo configurando cosas, especialmente porque ya mantiene sus artículos en [!INCLUDE[prod_short](../includes/prod_short.md)] correctamente. Después de lanzar su tienda en línea Shopify, obtiene inmediatamente nuevos clientes que están satisfechos con su tienda y su experiencia de compra. Entonces, deciden dejar propinas al momento de pagar.

### <a name="steps"></a><a name="steps"></a><a name="steps"></a><a name="steps"></a>Pasos

En [!INCLUDE[prod_short](../includes/prod_short.md)], realice los siguientes pasos:

1. Elija el icono ![Bombilla que abre la función Dígame.](../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Productos de Shopify** y luego elija el enlace relacionado.
2. Elija la acción **Agregar artículos**.
3. En el campo **Código de tienda**, especifique *DEMO1*.
4. Establezca el filtro `CHAIR` en el campo **Código de categoría del artículo** (agregue un campo de filtro si es necesario).
5. Seleccione **Aceptar** y espere hasta que se complete la sincronización inicial de artículos y precios.
6. Seleccione la acción **Sincronizar imágenes de productos**.
7. Elija la acción **Sincronizar inventario**.

En la **Tienda en línea de Shopify**
> [!Tip]  
> Abra **Administrador de Shopify** navegando a la URL especificada en el campo **URL** de la página **Ficha de tienda de Shopify**. A continuación, elija el icono del ojo junto al canal de ventas de la **Tienda en línea** que se encuentra en la barra lateral de **Administrador de Shopify**. 

Abra el catálogo de productos. Aviso:

* Títulos de productos, imágenes y precios.
* Indicador de disponibilidad (agotado para productos agotados).

Elija cualquier producto que se pueda vender, por ejemplo, el `BERLIN Swivel Chair, yellow`. Observe que la descripción contiene atributos del artículo.

Elija el botón **Cómprelo ahora** y proceda a pagar.

1. En el campo **Correo electrónico o número de teléfono móvil** , ingrese `cl@contoso.com` (o el correo electrónico donde desea recibir las confirmaciones de pedido y envío).
2. En **Nombre** y **Apellido**, ingrese `Claudia Lawson`.
3. Introduzca la dirección local.
4. Selecciona la casilla de verificación **Guardar esta información para la próxima vez** .
5. Elija el botón **Seguir comprando** para continuar.
6. Mantenga `Standard` como método de envío y luego elegir el botón **Continuar con el pago** .
7. Seleccione la propina `10%`.
8. En el campo **Tarjeta de crédito**, introduzca `1` si usa *(para probar) Bogus Gateway*, o introduzca `5555 5555 5555 4444`; si usa *Shopify Payments* en modo de prueba.
9. Complete el campo **Nombre en la tarjeta**.
10. En el campo **Fecha de vencimiento**, ingrese el mes/año actual.
11. En el **Código de seguridad**, especifique `111`.
12. Haga clic en el botón **Pagar ahora**.

En [!INCLUDE[prod_short](../includes/prod_short.md)], realice los siguientes pasos:

1. Elija el icono ![Bombilla que abre la función Dígame.](../media/ui-search/search_small.png "Dígame qué desea hacer") escriba **Pedidos de Shopify** y, a continuación, elija el vínculo relacionado.
2. Elija la acción **Sincronizar usuarios desde Shopify**.
3. Elija **Aceptar**.

El pedido importado está listo para ser procesado.

1. Seleccione el pedido importado para abrir la ventana **Pedido de Shopify**.
2. Observe que se crean el nuevo cliente y el pedido de ventas.
3. Explore las acciones **Riesgo** y **Coste de envío** .
4. Elija la acción **Pedido de ventas**, en la ventana **Pedido de ventas**. El pedido de venta es una demanda que, si es necesario, se puede cubrir con ensamblaje, producción o compra con la ayuda del motor de planificación. También es compatible con varios procesos de manejo de almacén con separación completa de funciones.
5. Seleccione la acción **Volver a abrir**.
6. En el campo **Agente**, introduzca `DHL`.
7. En el campo **Nº seguimiento bulto**, escriba `123456789`.
8. Seleccione la acción **Registrar**, mantenga la opción **Enviar y facturar** y seleccione el botón **Aceptar**.

Ahora los datos físicos y financieros se registran en [!INCLUDE[prod_short](../includes/prod_short.md)]. Es hora de notificar a Shopify sobre los cambios.

1. Elija el icono ![Bombilla que abre la característica Dígame.](../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Sincronizar envíos a Shopify** y, a continuación, elija el vínculo relacionado.
2. Elija **Aceptar**.

En **Administrador de Shopify** observe que el pedido ahora está marcado como *Cumplido*. También puede revisar los detalles del envío y ver la URL de seguimiento allí. Si vuelve a ejecutar **Sincronizar pedidos desde Shopify**, el pedido se archivará en ambos sistemas.

## <a name="walkthrough-invite-your-customers-to-your-new-online-store"></a><a name="walkthrough-invite-your-customers-to-your-new-online-store"></a><a name="walkthrough-invite-your-customers-to-your-new-online-store"></a><a name="walkthrough-invite-your-customers-to-your-new-online-store"></a>Tutorial: invitar a los clientes a una nueva tienda en línea

### <a name="scenario-1"></a><a name="scenario-1"></a><a name="scenario-1"></a><a name="scenario-1"></a>Escenario

Después de un lanzamiento rápido y exitoso de su nueva tienda en línea, desea que sus clientes actuales la visiten y comiencen a realizar pedidos.

### <a name="steps-1"></a><a name="steps-1"></a><a name="steps-1"></a><a name="steps-1"></a>Pasos

En [!INCLUDE[prod_short](../includes/prod_short.md)], realice uno de los siguientes pasos:

1. Elija el icono ![Bombilla que abre la característica Dígame](../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Tiendas de Shopify** y luego elija el enlace relacionado.
2. Seleccione la tienda **DEMO1** para la que desea sincronizar los clientes para abrir la página **Tarjeta de tienda de Shopify**.
3. Seleccione la acción **Sincronizar clientes**.

En **Administrador de Shopify** observe que los clientes fueron importados. Abra uno de los clientes y observe que el nombre y el apellido del cliente provienen del campo **Nombre de contacto** de la **Tarjeta de cliente**. El nombre de la empresa se puede encontrar en la dirección predeterminada, vinculada al cliente. Elija **Enviar invitación a la cuenta** para invitar al cliente.

## <a name="walkthrough-fine-tuning-of-item-management"></a><a name="walkthrough-fine-tuning-of-item-management"></a><a name="walkthrough-fine-tuning-of-item-management"></a><a name="walkthrough-fine-tuning-of-item-management"></a>Tutorial: ajuste fino de la gestión de artículos

### <a name="scenario-2"></a><a name="scenario-2"></a><a name="scenario-2"></a><a name="scenario-2"></a>Escenario

Le gustaría agregar más flexibilidad y control a sus procesos en torno a la gestión de artículos. Desea mejorar la descripción del producto y desea agregar más pasos de revisión antes de que los productos estén disponibles para el cliente final.

### <a name="steps-2"></a><a name="steps-2"></a><a name="steps-2"></a><a name="steps-2"></a>Pasos

En [!INCLUDE[prod_short](../includes/prod_short.md)], realice uno de los siguientes pasos:

Preparar datos.

1. Elija el icono ![Bombilla que abre la característica Dígame](../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Grupo de precios del cliente** y, a continuación, elija el vínculo relacionado.
2. Agregue un grupo de precios nuevo. En el campo **Código**, especifique `SHOPIFY`.
3. Cierre la ventana **Grupo de precios del cliente**.
4. Elija el icono ![Bombilla que abre la característica Dígame](../media/ui-search/search_small.png "Dígame qué desea hacer") y escriba **Productos** y luego elija el enlace relacionado.

Seleccione el producto **1896-S, Athens Desk** y ejecute los siguientes pasos.

1. Elija la acción **Variantes** y luego agregue las dos variantes `PREMIUM, Athens Desk, Premium edition` y `ESSENTIAL, Athens Desk, Essential edition`.
2. Elija la acción **Texto extendido**, cree un nuevo texto extendido válido para todos los códigos de idioma. En el campo **Descripción** escriba `Shopify`. 
3. Agregue el siguiente texto con etiquetas HTML: `<b>Simple stylish design</b> blends with any ensemble. <i>Available in two editions.</i>`.
4. Elija la acción **Precios de venta** y agregue nuevos precios como se muestra en la siguiente tabla:

  |Línea|**Tipo venta**|**Código ventas**|Tipo|Código|Cód. variante<br>(añadir el campo a través de la personalización)|Precio unitario|
  |------|------------|------------|------------|------------|------------|------------|
  |1|Grupo de precio de cliente|SHOPIFY|Artículo|1896-S|ESSENTIAL|700|
  |2|Grupo de precio de cliente|SHOPIFY|Producto|1896-S|PREMIUM|1000|

5. Elija la acción **Descuentos de ventas** y agregue un nuevo descuento:

* **Tipo de venta** *Grupo de discos de cliente*
* **Código de ventas** *RETAIL*
* **Tipo** *Producto*
* **Código** *1896-S*
* **Código de unidad medida** *PCS*
* **% de descuento en línea** *10*

6. Elija la acción **Referencias de productos** y agregue las siguientes líneas:

  |Línea|**Tipo referencia**|**N.º referencia**|Cód. variante|
  |------|------------|------------|------------|
  |1|Código de barras|77777777|ESSENTIAL|
  |2|Código de barras|11111111|PREMIUM|


Seleccione el producto **1920-S, ANTWERP Conference Table** y ejecute los siguientes pasos.

1. Elija **Ajustar inventario** y en el campo **Nuevo inventario**, ingrese `100` para las ubicaciones *ESTE* y *OESTE*. 
2. Elija **Aceptar**.

Ajuste la configuración de sincronización.

1. Elija el icono ![Bombilla que abre la característica Dígame](../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Tiendas de Shopify** y luego elija el enlace relacionado.
2. Seleccione la tienda *DEMO1* para la que desea sincronizar artículos para abrir la página Tarjeta de tienda de Shopify.
3. Seleccione *SHOPIFY* en el campo **Grupo de precios del cliente**.
4. Seleccione *RETAIL* en el campo **Grupo de descuentos del cliente**.
5. Habilite el campo **Texto extendido del elemento de sincronización**.
6. Seleccione *Número de artículo + Código de variante* en el campo **Asignación de SKU**.
7. Seleccione *Borrador* en el campo **Estado de productos creados**.
8. Seleccione *Estado en archivado* en el campo **Acción para producto eliminado**.

Ejecute la sincronización.

1. Elija el icono ![Bombilla que abre la característica Dígame](../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Tiendas de Shopify** y luego elija el enlace relacionado.
2. Seleccione la tienda *DEMO1* para la que desea sincronizar artículos para abrir la página **Tarjeta de tienda de Shopify**.
3. Seleccione la acción **Productos** para abrir la ventana **Productos de Shopify**.
4. Elija la acción **Agregar artículos**.
5. Configure el filtro *TABLE* en el campo **Código de categoría de artículo**.
6. Seleccione la acción **Sincronizar imágenes de productos**.
7. Elija la acción **Sincronizar inventario**.

Se agregan productos. Tenga en cuenta que el estado se establece en *Borrador* y, por lo tanto, los artículos no están visibles en la tienda en línea Shopify.

1. Seleccione la línea con el artículo *1920-S, ANTWERP Conference Table*. En **Título SEO**, escriba `Rectangular meeting table Antwerp, 10 seats, black`.
2. Seleccione *Activo* en el campo **Estado**.
3. Seleccione la línea con el elemento *1906-S, ATHENS, Mobile Pedestal* y luego elija la acción **Eliminar**.

En **Administrador de Shopify** observe que todos los productos tienen estados diferentes.

* *ANTWERP Conference Table* está *Activa* porque cambiamos el estado en la ventana **Producto de Shopify**.
* *ATHENS Desk* is *Borrador* porque configuramos que el estado predterminado para todos los productos añadidos fuera *Borrador*.
* *ATHENS Mobile Pedestal* es *Archivado* porque configuramos la tienda para asignar automáticamente el estado *Archivado* para productos eliminados.

Tenga en cuenta que el inventario de ANTWERP Conference Table es 100, porque configuramos el sistema para usar el inventario solo desde dos ubicaciones PRINCIPAL y ESTE. Se ignora el inventario en otras ubicaciones (OESTE).

* Abra *ANTWERP Conference Table*, observe los campos **Tipo personalizado**, **Proveedor**, **Peso**, **Coste por artículo** y la sección **Vista previa de lista de motor de búsqueda**.
* Abra *Athens Desk*, desplácese hacia abajo hasta la sección **Variantes** y observe cómo **SKU** está poblado.
* Elija **Editar** para revisar el código de barras y los precios.
* Cambie el estado de  *Athens Desk* a *Activo* y seleccione la acción **Vista previa**.

En la **Tienda online Shopify** abra el catálogo de productos, busque el producto *ATHENS Desk*. Tenga en cuenta que hay diferentes opciones disponibles. Para diferentes opciones, los precios son diferentes. Preste atención a la información de descuento.

## <a name="walkthrough-import-items-from-shopify"></a><a name="walkthrough-import-items-from-shopify"></a><a name="walkthrough-import-items-from-shopify"></a><a name="walkthrough-import-items-from-shopify"></a>Tutorial: Importar artículos desde Shopify

### <a name="scenario-3"></a><a name="scenario-3"></a><a name="scenario-3"></a><a name="scenario-3"></a>Escenario

Ya tiene una tienda en línea exitosa y le gustaría comenzar a usar [!INCLUDE[prod_short](../includes/prod_short.md)] como software de administración comercial. Le gustaría importar la mayor cantidad posible de datos de Shopify. 

### <a name="steps-3"></a><a name="steps-3"></a><a name="steps-3"></a><a name="steps-3"></a>Pasos

Esta es una continuación del [Tutorial: Comenzar a vender productos en línea](walkthrough-setting-up-and-using-shopify.md#walkthrough-start-selling-products-online). También puede probar con sus propios datos, por ejemplo, su tienda Shopify o espacio aislado.

En [!INCLUDE[prod_short](../includes/prod_short.md)], realice uno de los siguientes pasos:

#### <a name="prepare-data"></a><a name="prepare-data"></a><a name="prepare-data"></a><a name="prepare-data"></a>Preparar los datos

1. Cambie a una prueba gratuita de 30 días sin datos de muestra. Para obtener más información, consulte [Agregar sus propios datos a una prueba vacía](/dynamics365/business-central/dev-itpro/administration/trials-subscriptions#add-your-own-data-to-an-empty-trial-company).
2. Elija el icono ![Bombilla que abre la característica Dígame](../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Tiendas de Shopify** y luego elija el enlace relacionado.
3. Seleccione la acción **Nuevo**.
4. En el campo **Código**, especifique `DEMO2`.
5. En el campo **Shopify URL**, ingrese la URL de la tienda en línea a la que desea conectarse.
6. Active la alternancia **Habilitada** y revise y acepte los términos y condiciones.

Configure la tienda de Shopify como se describe a continuación en los pasos siguientes.

7. Habilite el botón de alternancia **Registro habilitado**.
8. Desactive la alternancia **Permitir sincronizaciones en segundo plano**.
9. Seleccione **De Shopify**, en el campo **Sincronizar elemento**.
5. Habilite la opción de alternancia **Creación automática de artículos desconocidos**.
11. Rellene el campo **Código de plantilla de artículos** con la plantilla adecuada.
12. Seleccione **De Shopify**, en el campo **Sincronizar imágenes de elementos**.
13. Seleccione **Todos los clientes** en **Importación de clientes de Shopify**.
14. Habilite la opción de alternancia **Creación automática de clientes desconocidos**.
15. Rellene el campo **Código de plantilla de cliente** con la plantilla adecuada.
16. Complete la **cuenta de gastos de envío**, la **Cuenta de propinas** con la cuenta de ingresos. Por ejemplo, en EE. UU., utilice `40100`.
17. Habilite el conmutador **Creación automática de pedidos**.

#### <a name="run-the-synchronization"></a><a name="run-the-synchronization"></a><a name="run-the-synchronization"></a><a name="run-the-synchronization"></a>Ejecutar la sincronización

1. Elija el icono ![Bombilla que abre la característica Dígame](../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Tiendas de Shopify** y luego elija el enlace relacionado.
2. Seleccione la tienda *DEMO2* para la que desea sincronizar datos para abrir la página **Tarjeta de tienda de Shopify**.
3. Seleccione la acción **Sincronizar productos**.
4. Seleccione la acción **Sincronizar imágenes de productos**.
5. Seleccione la acción **Sincronizar clientes**.

### <a name="results"></a><a name="results"></a><a name="results"></a><a name="results"></a>Resultados

* Los productos de Shopify se importan. Para verificarlo, elija el icono ![Bombilla que abre la función Dígame.](../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Productos de Shopify** y luego elija el enlace relacionado.
* Se crean elementos con imágenes. Para verificarlo, elija el icono ![Bombilla que abre la función Dígame.](../media/ui-search/search_small.png "Dígame qué desea hacer") y escriba **Producto** y luego elija el enlace relacionado.
* Los clientes de Shopify son importados. Para verificarlo, elija el icono ![Bombilla que abre la función Dígame.](../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Clientes de Shopify** y luego elija el enlace relacionado.
* Se crean clientes. Para verificarlo, elija el icono ![Bombilla que abre la función Dígame.](../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Clientes** y luego elija el enlace relacionado.


## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Consulte también

[Comenzar con el conector Shopify](get-started.md)  
