---
title: Solución de problemas de Shopify y sincronización de Business Central
description: Descubra qué hacer si algo falla cuando sincroniza datos entre Shopify y Business Central.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 04/24/2023
ms.custom: bap-template
ms.search.form: '30118, 30119, 30120, 30101, 30102'
---

# <a name="troubleshooting-the-shopify-and-business-central-synchronization"></a>Solución de problemas de Shopify y sincronización de Business Central

Puede encontrarse con situaciones en las que necesite solucionar problemas al sincronizar datos entre Shopify y [!INCLUDE[prod_short](../includes/prod_short.md)]. Esta página define los pasos para solucionar algunos escenarios habituales.

## <a name="run-tasks-in-the-foreground"></a>Ejecutar tareas en segundo plano

1. Elija el icono ![Bombilla que abre la función Dígame 1.](../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Tienda de Shopify** y luego elija el vínculo relacionado.
2. Seleccione la tienda para la que desea solucionar problemas para abrir la página **Tarjeta de tienda de Shopify**.
3. Desactive la alternancia **Permitir sincronizaciones en segundo plano**.

Ahora, cuando se active la acción de sincronización, la tarea se ejecutará en primer plano. Si se produce un error, aparecerá un cuadro de diálogo de error con un vínculo **Copiar detalles**. Use el vínculo para copiar información a un editor de texto para un análisis posterior.

## <a name="logs"></a>Registros

Si falla una tarea de sincronización, puede activar el conmutador de alternancia **Habilitado registro** en la página **Tarjeta de tienda de Shopify** para activar el registro. Luego puede desencadenar manualmente la tarea de sincronización y revise los registros.

### <a name="to-enable-logging"></a>Para habilitar el registro

1. Elija el icono ![Bombilla que abre la función Dígame 1.](../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Tienda de Shopify** y luego elija el vínculo relacionado.
2. Seleccione la tienda para la que desea solucionar problemas para abrir la página **Tarjeta de tienda de Shopify**.
3. Active el botón de alternancia **Registro habilitado**.

### <a name="to-review-logs"></a>Para revisar registros

1. Elija el icono ![Bombilla que abre la función Dígame 1.](../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Movimientos de registro de Shopify** y luego elija el vínculo relacionado.
2. Seleccione el movimiento de registro relacionado y luego abra la página **Movimiento de registro de Shopify**.
3. Revise la solicitud, el código y la descripción de estado, y los valores de respuesta. Puede descargar los valores de solicitud y respuesta como archivos en formato de texto.

Más tarde recuerde desactivar el registro para evitar un impacto negativo en el rendimiento y un aumento en el tamaño de la base de datos.

Desde la página **Movimientos de registro de Shopify**, puede desencadenar la eliminación de todas las entradas de registro o las que tengan más de siete días.

## <a name="data-capture"></a>Captura de datos

Independientemente de si **Registro activado** está activado, algunas respuestas de Shopify siempre se registran. Puede inspeccionar o descargar los registros desde la página **Lista de captura de datos**.

Elija la acción **Datos de Shopify recuperados** en una de las siguientes páginas:

- **Pedido de Shopify**
- **Shopify línea de pedido**
- **Shopify procesos de entrega**
- **Gastos de envío de pedido de Shopify**
- **Transacciones de pedido de Shopify**
- **Shopify devolución**
- **Shopify lín. devol.**
- **Shopify reembolso**
- **Shopify línea de reembolso**
- **Pagos de Shopify**
- **Transacciones de pago de Shopify**
- **Transacciones de Shopify**

## <a name="reset-sync"></a>Restablecer sincronización

Para un rendimiento óptimo, el conector importa solo clientes, productos y pedidos creados o modificados desde la última sincronización. En la **Ficha de tienda de Shopify**, hay funciones disponibles que cambian la fecha/hora de la última sincronización o restablecerla por completo. Esta función garantiza que se sincronizan todos los datos, en lugar de solo los cambios desde la última sincronización.

Esta función solo se aplica a las sincronizaciones de Shopify a [!INCLUDE[prod_short](../includes/prod_short.md)]. Puede ser útil si necesita restaurar datos eliminados, como productos, clientes o pedidos eliminados.

## <a name="request-the-access-token"></a>Solicitar el token de acceso

Si [!INCLUDE[prod_short](../includes/prod_short.md)] no puede conectarse a su cuenta de Shopify, intente solicitar el token de acceso de Shopify. Es posible que necesite solicitar un nuevo token si hubo cambios en las claves de seguridad o permisos requeridos (ámbitos de aplicación).

1. Elija el icono ![Bombilla que abre la función Dígame 1.](../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Tiendas de Shopify** y luego elija el enlace relacionado.
2. Seleccione la tienda para la que desea conseguir el token de acceoso para abrir la página **Tarjeta de tienda de Shopify**.
3. Elegir la acción **Solicitar acceso**.
4. Si se le solicita, inicie sesión en su cuenta de Shopify.

Se activará el conmutador de alternancia **Tiene clave de acceso**.

## <a name="verify-and-enable-permissions-to-make-http-requests-in-a-non-production-environment"></a>Verifique y habilite los permisos para realizar solicitudes HTTP en un entorno que no sea de producción

Para funcionar correctamente, la extensión del conector de Shopify requiere permiso para realizar solicitudes HTTP. Al probar en espacios aislados, las solicitudes HTTP están prohibidas para todas las extensiones.

1. Elija el icono ![Bombilla que abre la función Dígame 1.](../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Administración de extensiones** y luego elija el enlace relacionado.
2. Seleccione la extensión **Conector de Shopify**.
3. Seleccione la acción **Configurar** para abrir la página **Configuración de extensiones**.
4. Asegúrese de que el conmutador de alternancia **Permitir solicitudes HTTPClient** esté habilitado.

## <a name="rotate-the-shopify-access-token"></a>Rotar el token de acceso de Shopify

Los siguientes procedimientos describen cómo rotar el token de acceso utilizado por el conector de Shopify para acceder a su tienda de Shopify en línea.

### <a name="in-shopify"></a>En Shopify

1. Desde su **Administrador de Shopify**, vaya a [Aplicaciones](https://www.shopify.com/admin/apps).
2. Seleccione **Eliminar** en la fila con la aplicación **Dynamics 365 Business Central**.
3. En el mensaje que aparece, seleccione **Eliminar**.

### <a name="in-"></a>En [!INCLUDE[prod_short](../includes/prod_short.md)]

1. Elija el icono ![Bombilla que abre la función Dígame 1.](../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Tiendas de Shopify** y luego elija el enlace relacionado.
2. Seleccione la tienda para la que desea girar el token de acceoso para abrir la página **Tarjeta de tienda de Shopify**.
3. Elija la acción **Solicitar acceso**.
4. Si se le solicita, inicie sesión en su cuenta de Shopify, revise la privacidad y los permisos, y luego elija el botón **Instalar aplicación**.

## <a name="known-issues"></a>Problemas conocidos

### <a name="error-the-sales-header-does-not-exist-identification-fields-and-values-document-typequotenoyour-shopify-store"></a>Error: el encabezado de ventas no existe. Campos y valores de identificación: Tipo de documento='Oferta',N.º='TIENDA DE SHOPIFY'

Para calcular los precios, el conector de Shopify crea un documento de venta temporal (oferta) para un cliente temporal (código de tienda) y utiliza la lógica de cálculo de precio estándar haga su trabajo. Si una extensión de terceros se suscribe a eventos en un documento de ventas temporal, es posible que el encabezado no esté disponible. Le recomendamos que se ponga en contacto con el proveedor de la extensión. Pídales que modifiquen su código para buscar registros temporales. En algunos casos, solo tienen que agregar el método `IsTemporary` en el lugar correcto. Para obtener más información sobre `IsTemporary`, vaya a [IsTemporary](/dynamics365/business-central/dev-itpro/developer/methods-auto/record/record-istemporary-method). 

Para verificar que el problema lo causa una extensión de terceros, utilice el vínculo **Copiar información al portapapeles** en el mensaje de error y copie el contenido en el editor de texto. La información contiene una **pila de llamadas AL**, donde la línea superior es la línea donde ocurrió el error. El siguiente ejemplo muestra una pila de llamadas AL.

Pila de llamadas AL:

```AL
[Object Name]([Object type] [Object Id]).[Function Name] line [XX] - [Extension Name] by [Publisher] 
...
"Sales Line"(Table 37)."No. - OnValidate"(Trigger) line 98 - Base Application by Microsoft
"Shpfy Product Price Calc."(CodeUnit 30182).CalcPrice line 20 - Shopify Connector by Microsoft
"Shpfy Create Product"(CodeUnit 30174).CreateTempProduct line 137 - Shopify Connector by Microsoft
"Shpfy Create Product"(CodeUnit 30174).CreateProduct line 5 - Shopify Connector by Microsoft
"Shpfy Create Product"(CodeUnit 30174).OnRun(Trigger) line 12 - Shopify Connector by Microsoft
"Shpfy Add Item to Shopify"(Report 30106)."Item - OnAfterGetRecord"(Trigger) line 2 - Shopify Connector by Microsoft
"Shpfy Products"(Page 30126)."AddItems - OnAction"(Trigger) line 5 - Shopify Connector by Microsoft
```

Recuerde compartir la información de la pila de llamadas AL con el proveedor de la extensión.

### <a name="error-gen-bus-posting-group-must-have-a-value-in-customer-your-shopify-store-it-cannot-be-zero-or-empty"></a>Error: Gen. Grupo de contabilización Bus. debe tener un valor en Cliente: 'TIENDA DE SHOPIFY'. No puede estar vacío ni ser cero

Rellene el campo **Código de plantilla de cliente** de la página **Tarjeta de tienda de Shopify**, elija la plantilla que tiene **Grupo contable negocio**. La plantilla de cliente se utiliza para crear clientes y calcular precios de venta en documentos de ventas.

### <a name="error-importing-data-to-your-shopify-shop-isnt-enabled-go-to-the-shop-card-to-enable-it"></a>Error: la importación de datos a su tienda de Shopify no está habilitada. Vaya a la tarjeta de la tienda para habilitarla.

En la página **Tarjeta de tienda de Shopify**, active la opción **Permitir la sincronización de datos para Shopify**. Este ajuste ayuda a proteger la tienda en línea de obtener datos de demostración de [!INCLUDE[prod_short](../includes/prod_short.md)].

### <a name="error-oauth-error-invalid_request-could-not-find-shopify-api-application-with-api_key"></a>Error: Oauth error invalid_request: no se pudo encontrar la aplicación API de Shopify con api_key

Parece que usa [Insertar aplicación](/dynamics365/business-central/dev-itpro/deployment/embed-app-overview), donde la URL del cliente tiene el formato: `https://[application name].bc.dynamics.com`. El conector Shopify no funciona para las aplicaciones integradas. Para obtener más información, vaya a [¿Qué productos de Microsoft tienen disponible el conector Shopify?](shopify-faq.md#which-microsoft-products-are-the-shopify-connector-available-for).

### <a name="error-internal-error-looks-like-something-went-wrong-on-our-end-request-id-xxxxxxxx-xxxx-xxxx-xxxx-xxxx"></a>Error: error interno. Parece que hemos tenido un problema. ID de solicitud: XXXXXXXX-XXXX-XXXX-XXXX-XXXX

Póngase en contacto con el soporte técnico de Shopify dentro de los 7 días de haber experimentado este error y proporcione la identificación de la solicitud. Para obtener más información, vaya a [Opciones de soporte técnico para Shopify](shopify-faq.md#shopify).

### <a name="error-oauth-error-invalid_request-your-account-does-not-have-permission-to-grant-the-requested-access-for-this-app"></a>Error: error Oauth invalid_request: Su cuenta no tiene permiso para otorgar el acceso solicitado para esta aplicación.

Parece que el usuario que solicita acceso no tiene derechos para administrar aplicaciones (capacidad para administrar e instalar aplicaciones y canales, así como también aprobar potencialmente cargos de aplicaciones). Es posible que puedas resolver este problema instalando la aplicación como propietario de la cuenta. Como alternativa, puede comprobar el **Permiso de apicación** del usuario en la configuración de [**usuario y permisos**](https://www.shopify.com/admin/settings/account) en el **Administrador de Shopify**.  

## <a name="see-also"></a>Consulte también .

[Comenzar con el conector para Shopify](get-started.md)
