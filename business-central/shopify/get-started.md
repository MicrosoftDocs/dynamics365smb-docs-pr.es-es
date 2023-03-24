---
title: Primeros pasos con el conector para Shopify
description: Primeros pasos al configurar la conexión entre Business Central y Shopify
ms.date: 05/27/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.reviewer: solsen
ms.search.form: '30100, 30101, 30102, 30103, 30104, 30135,'
author: AndreiPanko
ms.author: andreipa
---

# Comenzar con el conector de Shopify

Conecte su tienda (o tiendas) de Shopify con [!INCLUDE [prod_short](../includes/prod_short.md)] y maximice la productividad de su negocio. Administre y vea información de su negocio y su tienda de Shopify como una unidad.

Para usar Shopify con [!INCLUDE [prod_short](../includes/prod_short.md)], debe a hacer algunas cosas primero. Este artículo sirve como guía para integrar su tienda de Shopify con [!INCLUDE [prod_short](../includes/prod_short.md)].

## Requisitos previos para Shopify

Debe tener:

- Una cuenta de Shopify
- Tienda en línea con Shopify

Para más información sobre cómo crear pruebas y configuraciones recomendadas de Shopify, vaya a [Creación y configuración de la cuenta de Shopify](shopify-account.md).

## Requisitos previos para Business Central

- Asegúrese de que la aplicación **[Connector de Shopify](https://go.microsoft.com/fwlink/?linkid=2196238)** esté instalada.

  La aplicación está preinstalada para todos los nuevos registros y pruebas. Más información sobre como instalar aplicaciones desde AppSource, en [Instalar y desinstalar extensiones](../ui-extensions-install-uninstall.md#install). Siga los pasos enumerados a continuación si no tiene [!INCLUDE[prod_short](../includes/prod_short.md)].

- Asegúrese de que el usuario tenga suficientes permisos. Shopify Connector está cubierto por el conjunto de permisos *Shopify – Admin (SHPFY – ADMIN)*. Obtenga más información en [Crear usuarios según las licencias](../ui-how-users-permissions.md) y [Asignar permisos a usuarios y grupos](../ui-define-granular-permissions.md)


## Instalar la aplicación Dynamics 365 Business Central para su tienda en línea de Shopify

Por [!INCLUDE[prod_short](../includes/prod_short.md)] existentes, este paso es opcional y se puede omitir.

1. Localizar la aplicación [Dynamics 365 Business Central](https://apps.shopify.com/dynamics-365-business-central) en la [AppStore de Shopify](https://apps.shopify.com/)
2. Seleccione el botón **Agrega aplicación**. Si se le solicita, inicie sesión en su cuenta de Shopify. Seleccione la tienda en línea si tiene más de una.
3. Después de revisar la privacidad y los permisos, seleccione el botón **Instalar aplicación**.

   Puede encontrar y abrir la aplicación instalada **Dynamics 365 Business Central** en la sección **Aplicaciones** de la barra lateral de la página **administración de Shopify**.
4. Elija **Registrarse ahora** para empezar la prueba de [!INCLUDE[prod_short](../includes/prod_short.md)] o **Iniciar sesión** si ya tiene [!INCLUDE[prod_short](../includes/prod_short.md)]. Se le redirigirá a su página en [Business Central](https://businesscentral.dynamics.com).
5. Los siguientes pasos deben hacerse en [!INCLUDE[prod_short](../includes/prod_short.md)].

## Conectar Business Central a la tienda en línea de Shopify

1. Elija la ![Bombilla que abre la función Dígame.](../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Tienda de Shopify** y luego elija el vínculo relacionado.
2. Seleccione la acción **Nuevo**.  
3. En el campo **Código**, introduzca el código que hará que sea fácil de encontrar en [!INCLUDE[prod_short](../includes/prod_short.md)]. Por ejemplo, un nombre podría reflejar lo que vende una tienda, como "Muebles" o "Café", o el país o la región a la que sirve.
4. En el campo **URL de Shopify**, introduzca la URL de su tienda en línea, que debe conectarse. Utilice el siguiente formato: `https://{shop}.myshopify.com/`.
5. Active la alternancia **Habilitada** y revise y acepte los términos y condiciones.
6. Si se le solicita, inicie sesión en su cuenta de Shopify, revise los términos de privacidad y los permisos, y luego elija el botón **Instalar aplicación**.

Repita los pasos 2 a 6 para todas las tiendas en línea que desee conectar.

### Problemas conocidos

- El navegador bloquea la ventana emergente. Cuando activa la opción **Activado** el sistema abre la página **En espera de una respuesta - no cierre esta página**, que está esperando un token de acceso de Shopify, si esa página está cerrada o bloqueada, no puede conectarse a Shopify. Obtenga más información en [Solicitar el token de acceso](troubleshoot.md#request-the-access-token)
- [Error invalid_request de Oauth: No se pudo encontrar Aplicación API de Shopify con api_key](troubleshoot.md#oauth-error-invalid_request-could-not-find-shopify-api-application-with-api_key)
- [No se puede conectar desde el espacio aislado](troubleshoot.md#verify-and-enable-permissions-to-make-http-requests-when-running-in-a-non-production-environment)


## Pasos siguientes

Ahora su tienda en línea está conectada a [!INCLUDE[prod_short](../includes/prod_short.md)]. En los siguientes pasos, definirá cómo y qué sincronizar.

- [Sincronizar elementos](synchronize-items.md)
- [Sincronizar clientes](synchronize-customers.md)
- [Sincronizar pedidos](synchronize-orders.md)

## Consulte también .

[Tutorial: Configurar y usar el Shopify Connector](walkthrough-setting-up-and-using-shopify.md)  

