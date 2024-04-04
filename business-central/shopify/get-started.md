---
title: Primeros pasos con el conector para Shopify
description: Primeros pasos al configurar la conexión entre Business Central y Shopify
ms.date: 03/27/2023
ms.topic: article
ms.service: dynamics-365-business-central
ms.reviewer: solsen
ms.search.form: '30100, 30101, 30102, 30103, 30104, 30135,'
author: brentholtorf
ms.author: bholtorf
---

# <a name="get-started-with-the-shopify-connector"></a>Introducción al conector de Shopify

Conecte sus tiendas de Shopify con [!INCLUDE [prod_short](../includes/prod_short.md)] y maximice la productividad de su negocio. Administre y vea información de su negocio y su tienda de Shopify como una unidad.

Para usar Shopify con [!INCLUDE [prod_short](../includes/prod_short.md)], debe a hacer algunas cosas primero. Este artículo sirve como guía para integrar su tienda de Shopify con [!INCLUDE [prod_short](../includes/prod_short.md)].

## <a name="prerequisites-for-shopify"></a>Requisitos previos para Shopify

Debe tener:

- Una cuenta de Shopify
- Tienda en línea con Shopify

Para obtener más información sobre cómo crear pruebas de Shopify y las configuraciones recomendadas, vaya a [Crear y configurar una cuenta de Shopify](shopify-account.md).

## <a name="prerequisites-for-business-central"></a>Requisitos previos para Business Central

- Asegúrese de que la aplicación **[Connector de Shopify](https://go.microsoft.com/fwlink/?linkid=2196238)** esté instalada.

  La aplicación está preinstalada para todos los nuevos registros y pruebas. Más información sobre como instalar aplicaciones desde AppSource, en [Instalar y desinstalar extensiones](../ui-extensions-install-uninstall.md#install). Siga los pasos enumerados a continuación si no tiene [!INCLUDE[prod_short](../includes/prod_short.md)].

- Asegúrese de que el usuario tenga los permisos adecuados. Shopify Connector está cubierto por el conjunto de permisos **Shopify – Admin (SHPFY – ADMIN)**. Obtenga más información en [Crear usuarios según las licencias](../ui-how-users-permissions.md) y [Asignar permisos a usuarios y grupos](../ui-define-granular-permissions.md).

## <a name="install-the-dynamics-365-business-central-app-to-your-shopify-online-store"></a>Instalar la aplicación Dynamics 365 Business Central para su tienda en línea de Shopify

Por instancias de [!INCLUDE[prod_short](../includes/prod_short.md)] existentes, este paso es opcional y se puede omitir.

1. Localizar la aplicación [Dynamics 365 Business Central](https://apps.shopify.com/dynamics-365-business-central) en la [AppStore de Shopify](https://apps.shopify.com/)
2. Seleccione el botón **Agrega aplicación**. Si se le solicita, inicie sesión en su cuenta de Shopify. Seleccione la tienda en línea si tiene más de una.
3. Después de revisar la privacidad y los permisos, seleccione el botón **Instalar aplicación**.

   Puede encontrar y abrir la aplicación instalada **Dynamics 365 Business Central** en la sección **Aplicaciones** de la barra lateral de la página **administración de Shopify**.
4. Elija **Registrarse ahora** para empezar la prueba de [!INCLUDE[prod_short](../includes/prod_short.md)] o **Iniciar sesión** si ya tiene [!INCLUDE[prod_short](../includes/prod_short.md)]. Se le redirigirá a su página en [Business Central](https://businesscentral.dynamics.com).
5. En [!INCLUDE[prod_short](../includes/prod_short.md)], realice los siguientes pasos.

## <a name="connect-business-central-to-the-shopify-online-store"></a>Conectar Business Central a la tienda en línea de Shopify

1. Elija el icono ![Bombilla que abre la característica Dígame](../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Tienda de Shopify** y luego elija el vínculo relacionado.
2. Seleccione la acción **Nuevo**.  
3. En el campo **Código**, introduzca un código que hará que sea fácil de encontrar en [!INCLUDE[prod_short](../includes/prod_short.md)]. Por ejemplo, el nombre podría reflejar lo que vende una tienda, como "Muebles" o "Café", o el país o la región a la que sirve.
4. En el campo **URL de Shopify**, introduzca la URL de la tienda en línea a la se está conectando. Utilice el siguiente formato: `https://{shop}.myshopify.com/`.
5. Active la alternancia en **Habilitado** y revise y acepte los términos y condiciones.
6. Si se le solicita, inicie sesión en su cuenta de Shopify. Después de revisar los términos de privacidad y los permisos, elija el botón **Instalar aplicación**.

Repita los pasos 2 a 6 para todas las tiendas en línea que desee conectar.

### <a name="known-issues"></a>Problemas conocidos

- El navegador bloquea la ventana emergente. Al activar el conmutador en **Activado**, [!INCLUDE [prod_short](../includes/prod_short.md)] abre la página **En espera de una respuesta: no cierre esta página** mientras espera un token de acceso de Shopify. Si esa página está cerrada o bloqueada, no puede conectarse a Shopify. Obtenga más información en [Solicitar el token de acceso](troubleshoot.md#request-the-access-token).
- Podría ser una buena idea tener el administrador de Shopify abierto en el mismo navegador que [!INCLUDE [prod_short](../includes/prod_short.md)].
- [Error: error invalid_request de Oauth: no se pudo encontrar Aplicación API de Shopify con api_key](troubleshoot.md#error-oauth-error-invalid_request-could-not-find-shopify-api-application-with-api_key)
- [Error: error Oauth invalid_request: Su cuenta no tiene permiso para otorgar el acceso solicitado para esta aplicación.](troubleshoot.md#error-oauth-error-invalid_request-your-account-does-not-have-permission-to-grant-the-requested-access-for-this-app)
- [No se puede conectar desde el espacio aislado](troubleshoot.md#verify-and-enable-permissions-to-make-http-requests-in-a-non-production-environment)
- Asegúrese de ingresar la URL correcta en el campo **URL de Shopify**. Puede crear la URL combinando el ID de la tienda de la URL del administrador. Por ejemplo, `admin.shopify.com/store/{shop}` y `.myshopify.com` para obtener `https://{shop}.myshopify.com/`.

## <a name="next-steps"></a>Pasos siguientes

Ahora su tienda en línea está conectada a [!INCLUDE[prod_short](../includes/prod_short.md)]. En los siguientes pasos, definirá cómo y qué sincronizar.

- [Sincronizar elementos](synchronize-items.md)
- [Sincronizar clientes](synchronize-customers.md)
- [Sincronizar pedidos](synchronize-orders.md)

## <a name="testing-strategies"></a>Estrategias de pruebas

Existen diferentes enfoques para probar una integración, y cada enfoque tiene sus pros y sus contras.

Puede conectar cuentas de [!INCLUDE[prod_short](../includes/prod_short.md)] y Shopify con la frecuencia que desee. El conector Shopify afecta únicamente al entorno o, más exactamente, a la empresa donde está habilitado. Puede conectarse a la misma tienda en línea de Shopify desde múltiples entornos o empresas. Puede deshabilitar y volver a habilitar el conector.

Es fácil volver a ejecutar las pruebas de sincronización. El conector le permite eliminar datos importados, como productos, clientes y pedidos, y luego volver a importarlos. Simplemente [restablezca la sincronización](troubleshoot.md#reset-sync).

### <a name="shopify-sandbox-and-business-central-sandbox"></a>Espacio aislado de Shopify y espacio aislado de Business Central

Esta es probablemente la forma más segura de probar la integración. En lugar de usar un espacio aislado de Shopify, también puede usar una suscripción de prueba o una Tienda de desarrollo. En [!INCLUDE[prod_short](../includes/prod_short.md)], también puede utilizar una empresa de prueba en un entorno de producción.

Para obtener más información sobre los espacios aislados de [!INCLUDE[prod_short](../includes/prod_short.md)], vaya a [Crear un nuevo entorno](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#create-a-new-environment).

### <a name="shopify-sandbox-and-business-central-production"></a>Espacio aislado de Shopify y de producción de de Business Central

Esta *no* es una configuración recomendada para realizar pruebas porque el conector Shopify puede crear o modificar productos y clientes. También puede crear documentos de ventas, como pedidos y facturas. Estos documentos pueden ser difíciles de deshacer.
 
Si debe usar esta configuración, le recomendamos que revise y probablemente deshabilite las siguientes configuraciones:

* **Crear elemento desconocido automáticamente** para no crear elementos.
* **Shopify puede actualizar productos** para no actualizar elementos asignados.
* **Crear automáticamente un cliente desconocido** para no crear clientes ni contactos.
* **Shopify puede actualizar clientes** para no actualizar clientes existentes.
* **Crear pedido de venta automáticamente** para no crear pedidos de venta ni facturas de venta.

Para obtener más información, consulte [Restaurar un entorno](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-backup-restore).

### <a name="shopify-production-and-business-central-sandbox"></a>Producción de Shopify y espacio aislado de Business Central

Puede ser una buena idea hacer una copia de seguridad de sus datos. Por ejemplo, exporte sus productos y clientes. Para obtener más información, consulte [Uso de archivos CSV para realizar copias de seguridad de la información de la tienda](https://help.shopify.com/en/manual/shopify-admin/duplicate-store#using-csv-files-to-back-up-store-information).

Desactive el conmutador **Permitir sincronización de datos para Shopify** para que [!INCLUDE[prod_short](../includes/prod_short.md)] no escriba en Shopify. En este caso, podrá importar productos, imágenes, clientes y pedidos de Shopify. Pero no podrá enviar productos, precios, niveles de inventario, clientes ni información de cumplimiento a Shopify.

Si mantiene activado el conmutador **Permitir la sincronización de datos para Shopify** , las medidas de protección adicionales son:

*   Seleccione **Borrador** en el campo **Estado para crear producto** para asegurarse de que los productos exportados no estén disponibles para los compradores. Puede verificar cómo se ven los productos en la tienda en línea, sincronizar precios, opciones y niveles de existencias. Solo asegúrese de usar filtros en la página **Agregar elemento a Shopify**  para limitar la cantidad de elementos exportados.
* Desactive la opción **Exportar cliente a Shopify** para no enviar clientes a Shopify.

## <a name="see-also"></a>Consulte también .

[Tutorial: Configurar y usar el Shopify Connector](walkthrough-setting-up-and-using-shopify.md)  

