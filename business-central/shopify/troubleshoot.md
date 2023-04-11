---
title: Solución de problemas de Shopify y sincronización de Business Central
description: Descubra qué hacer si algo falla durante la sincronización de datos entre Shopify y Business Central
ms.date: 03/27/2023
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: '30118, 30119, 30120, 30101, 30102'
author: edupont04
ms.author: andreipa
ms.reviewer: solsen
---

# Solución de problemas de Shopify y sincronización de Business Central

Puede encontrarse con situaciones en las que necesite solucionar problemas al sincronizar datos entre Shopify y [!INCLUDE[prod_short](../includes/prod_short.md)]. Esta página define los pasos para solucionar algunos escenarios habituales.

## Ejecutar tareas en segundo plano

1. Elija el icono ![Bombilla que abre la función Dígame 1.](../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Tienda de Shopify** y luego elija el vínculo relacionado.
2. Seleccione la tienda para la que desea solucionar problemas para abrir la página **Tarjeta de tienda de Shopify**.
3. Desactive la alternancia **Permitir sincronizaciones en segundo plano**.

Ahora, cuando se desencadene la acción de sincronización, la tarea se ejecutará en primer plano y, si se produce un error, aparecerá un cuadro de diálogo de error con el vínculo **Copiar detalles**. Use este vínculo para copiar información adicional a un editor de texto para un análisis posterior.

## Registros

Si falla una tarea de sincronización, puede activar el conmutador de alternancia **Habilitado registro** en la página **Tarjeta de tienda de Shopify** para activar el registro. Luego puede desencadenar manualmente la tarea de sincronización y revise los registros.

### Para habilitar el registro

1. Elija el icono ![Bombilla que abre la función Dígame 1.](../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Tienda de Shopify** y luego elija el vínculo relacionado.
2. Seleccione la tienda para la que desea solucionar problemas para abrir la página **Tarjeta de tienda de Shopify**.
3. Active el botón de alternancia **Registro habilitado**.

### Para revisar registros

1. Elija el icono ![Bombilla que abre la función Dígame 1.](../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Movimientos de registro de Shopify** y luego elija el vínculo relacionado.
2. Seleccione el movimiento de registro relacionado y abra la página **Movimiento de registro de Shopify**.
3. Revise la solicitud, el código y la descripción de estado, y los valores de respuesta. Puede descargar los valores de solicitud y respuesta como archivos en formato de texto.

Más tarde recuerde desactivar el registro más tarde para evitar un impacto negativo en el rendimiento y un aumento en el tamaño de la base de datos.

Desde la página **Movimientos de registro de Shopify**, puede desencadenar la eliminación de todas las entradas de registro o las que tengan más de siete días.

## Captura de datos

Sin importar los ajustes de **Registro activado**, algunas respuestas de Shopify siempre se registran para que pueda inspeccionarlas o descargarlas usando la página **Lista de captura de datos**.

Elija la acción **Datos de Shopify recuperados** en una de las siguientes páginas:

- **Pedido de Shopify**
- **Cumplimento de pedido de Shopify**
- **Gastos de envío de pedido de Shopify**
- **Transacciones de pedido de Shopify**
- **Pagos de Shopify**
- **Transacciones de pago de Shopify**
- **Transacciones de Shopify**

## Restablecer sincronización

Para un rendimiento óptimo, el conector importa solo clientes, productos y pedidos creados o modificados desde la última sincronización. En la **Ficha de tienda de Shopify**, hay funciones disponibles que cambian la fecha/hora de la última sincronización o restablecerla por completo. Esta función garantiza que cuando se ejecuta la sincronización, se sincronizan todos los datos en lugar de solo los cambios desde la última sincronización.

Esta función solo se aplica a las sincronizaciones de Shopify a [!INCLUDE[prod_short](../includes/prod_short.md)]. Puede ser útil si necesita restaurar datos eliminados, como productos, clientes o pedidos eliminados.

## Solicitar el token de acceso

Si [!INCLUDE[prod_short](../includes/prod_short.md)] no puede conectarse a su cuenta de Shopify, intente solicitar el token de acceso de Shopify. Esta solicitud puede ser necesaria si hay una rotación de claves de seguridad o cambios en los permisos requeridos (ámbitos).

1. Elija el icono ![Bombilla que abre la función Dígame 1.](../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Tiendas de Shopify** y luego elija el enlace relacionado.
2. Seleccione la tienda para la que desea conseguir el token de acceoso para abrir la página **Tarjeta de tienda de Shopify**.
3. Elegir la acción **Solicitar acceso**.
4. Si se le solicita, inicie sesión en su cuenta de Shopify.

Se activará el conmutador de alternancia **Tiene clave de acceso**.

### Verifique y habilite los permisos para realizar solicitudes HTTP cuando se ejecuta en un entorno que no sea de producción

Para funcionar correctamente, la extensión del conector de Shopify requiere permiso para realizar solicitudes HTTP. Al probar en espacios aislados, las solicitudes HTTP están prohibidas para todas las extensiones.

1. Elija el icono ![Bombilla que abre la función Dígame 1.](../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **administración de extensiones** y luego elija el enlace relacionado.
2. Seleccione la extensión **Conector de Shopify**.
3. Seleccione la acción **Configurar** para abrir la página **Configuración de extensiones**.
4. Asegúrese de que el conmutador de alternancia **Permitir solicitudes HTTPClient** esté habilitado.

## Rotar el token de acceso de Shopify

Los siguientes procedimientos describen cómo rotar el token de acceso utilizado por el conector de Shopify para acceder a su tienda de Shopify en línea.

### En Shopify

1. Desde su **Administrador de Shopify**, vaya a [Aplicaciones](https://www.shopify.com/admin/apps).
2. Seleccione **Eliminar** en la fila con la aplicación **Dynamics 365 Business Central**.
3. En el mensaje que aparece, seleccione **Eliminar**.

### En [!INCLUDE[prod_short](../includes/prod_short.md)]

1. Elija el icono ![Bombilla que abre la función Dígame 1.](../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Tiendas de Shopify** y luego elija el enlace relacionado.
2. Seleccione la tienda para la que desea girar el token de acceoso para abrir la página **Tarjeta de tienda de Shopify**.
3. Elija la acción **Solicitar acceso**.
4. Si se le solicita, inicie sesión en su cuenta de Shopify, revise la privacidad y los permisos, y luego elija el botón **Instalar aplicación**.

## Problemas conocidos

### Error: el encabezado de ventas no existe. Campos y valores de identificación: Tipo de documento='Oferta',N.º='TIENDA DE SHOPIFY'

Para calcular los precios, el conector de Shopify crea un documento de venta temporal (oferta) para el cliente temporal (código de tienda) y permite que la lógica de cálculo de precio estándar haga su trabajo. Es un escenario típico cuando una extensión de terceros se suscribe a eventos en la línea de ventas, pero no verifica que el registro sea temporal, por lo que es posible que no se pueda acceder al encabezado. Nuestra recomendación es contactar con el proveedor de la extensión y pedirle que modifique su código para comprobar si los registros son temporales. En algunos casos, basta con agregar el método `IsTemporary` en el lugar correcto. Para obtener más información sobre IsTemporary, vaya a [IsTemporary](/dynamics365/business-central/dev-itpro/developer/methods-auto/record/record-istemporary-method). 

Para verificar que el problema lo causa una extensión de terceros, utilice el vínculo **Copiar información al portapapeles** en el mensaje de error y copie el contenido en el editor de texto. La información contiene una **pila de llamadas AL**, donde la línea superior es la línea donde ocurrió el error. El siguiente es un ejemplo de una pila de llamadas AL.

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

### Error: Gen. Grupo de contabilización Bus. debe tener un valor en Cliente: 'TIENDA DE SHOPIFY'. No puede estar vacío ni ser cero

Rellene el campo **Código de plantilla de cliente** en la ventana **Tarjeta de tienda de Shopify** con la plantilla que tiene **Grupo contable negocio**. La plantilla de cliente se utiliza no solo para la creación de clientes, sino también para el cálculo del precio de venta y durante la creación de documentos de venta.

### Error: la importación de datos a su tienda de Shopify no está habilitada. Vaya a la tarjeta de la tienda para habilitarla.

En la **Tarjeta de tienda de Shopify**, active la opción **Permitir la sincronización de datos para Shopify**. Esta opción está destinada a proteger la tienda en línea de obtener datos de demostración de [!INCLUDE[prod_short](../includes/prod_short.md)].

### Error: Oauth error invalid_request: no se pudo encontrar la aplicación API de Shopify con api_key

Parece que usa [Insertar aplicación](/dynamics365/business-central/dev-itpro/deployment/embed-app-overview), donde la URL del cliente tiene el formato: `https://[application name].bc.dynamics.com`. El conector Shopify no funciona para las aplicaciones integradas. Para más información, consulte [¿Qué productos de Microsoft tienen disponible el conector Shopify?](shopify-faq.md#which-microsoft-products-are-the-shopify-connector-available-for).

## Consulte también .

[Comenzar con el conector para Shopify](get-started.md)
