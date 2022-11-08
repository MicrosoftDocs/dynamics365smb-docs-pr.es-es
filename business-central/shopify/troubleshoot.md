---
title: Solución de problemas de Shopify y sincronización de Business Central
description: Descubra qué hacer si algo falla durante la sincronización de datos entre Shopify y Business Central
ms.date: 08/19/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: 30118, 30119, 30120,
author: edupont04
ms.author: andreipa
ms.reviewer: solsen
ms.openlocfilehash: 37fb8069f6149cc89c1c53f671eafe3788f54ccf
ms.sourcegitcommit: 5bb13966e9ba8d7a3c2f00dd32f167acccf90b82
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/28/2022
ms.locfileid: "9728362"
---
# <a name="troubleshooting-the-shopify-and-business-central-synchronization"></a>Solución de problemas de Shopify y sincronización de Business Central

Es posible encontrarse con situaciones en las que necesite solucionar problemas al sincronizar datos entre Shopify y [!INCLUDE[prod_short](../includes/prod_short.md)]. Esta página define los pasos para solucionar algunos escenarios comunes que pueden ocurrir.

## <a name="logs"></a>Registros

Si falla una tarea de sincronización, puede activar el registro habilitando el conmutador de alternancia **Habilitar registro** en la página **Ficha de tienda de Shopify**. Luego puede desencadenar manualmente la tarea de sincronización y revise los registros.

1. Elija el icono ![Bombilla que abre la función Dígame 1.](../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Movimientos de registro de Shopify** y luego elija el vínculo relacionado.
2. Seleccione el movimiento de registro relacionado y abra la página **Movimiento de registro de Shopify**.
3. Revise la solicitud, el código y la descripción de estado, y los valores de respuesta.

Más tarde recuerde desactivar el registro más tarde para evitar un impacto negativo en el rendimiento y un aumento en el tamaño de la base de datos.

Desde la página **Movimientos de registro de Shopify**, puede desencadenar la eliminación de todas las entradas de registro o las que tengan más de siete días.

## <a name="data-capture"></a>Captura de datos

Sin importar los ajustes de **Registro activado**, algunas respuestas de Shopify siempre se registran para que pueda inspeccionarlas o descargarlas usando la página **Lista de captura de datos**.

Elija la acción **Datos de Shopify recuperados** en una de las siguientes páginas:

- **Pedido de Shopify**
- **Cumplimento de pedido de Shopify**
- **Gastos de envío de pedido de Shopify**
- **Transacciones de pedido de Shopify**
- **Pagos de Shopify**
- **Transacciones de pago de Shopify**
- **Transacciones de Shopify**

## <a name="reset-sync"></a>Restablecer sincronización

Para un rendimiento óptimo, el conector importa solo clientes, productos y pedidos creados o modificados desde la última sincronización. En la **Ficha de tienda de Shopify**, hay funciones disponibles que cambian la fecha/hora de la última sincronización o restablecerla por completo. Esta función garantiza que cuando se ejecuta la sincronización, se sincronizan todos los datos en lugar de solo los cambios desde la última sincronización.

Esta función solo se aplica a las sincronizaciones de Shopify a [!INCLUDE[prod_short](../includes/prod_short.md)]. Puede ser útil si necesita restaurar datos eliminados, como productos, clientes o pedidos eliminados.

## <a name="request-the-access-token"></a>Solicitar el token de acceso

Si [!INCLUDE[prod_short](../includes/prod_short.md)] no puede conectarse a su cuenta de Shopify, intente solicitar el token de acceso de Shopify. Esta solicitud puede ser necesaria si hay una rotación de claves de seguridad o cambios en los permisos requeridos (ámbitos).

1. Elija el icono ![Bombilla que abre la función Dígame 1.](../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Tiendas de Shopify** y luego elija el enlace relacionado.
2. Seleccione la tienda para la que desea conseguir el token de acceoso para abrir la página **Tarjeta de tienda de Shopify**.
3. Elegir la acción **Solicitar acceso**.
4. Si se le solicita, inicie sesión en su cuenta de Shopify.

Se activará el conmutador de alternancia **Tiene clave de acceso**.

### <a name="verify-and-enable-permissions-to-make-http-requests-when-running-in-a-non-production-environment"></a>Verifique y habilite los permisos para realizar solicitudes HTTP cuando se ejecuta en un entorno que no sea de producción

Para funcionar correctamente, la extensión del conector de Shopify requiere permiso para realizar solicitudes HTTP. Al probar en espacios aislados, las solicitudes HTTP están prohibidas para todas las extensiones.

1. Elija el icono ![Bombilla que abre la función Dígame 1.](../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **administración de extensiones** y luego elija el enlace relacionado.
2. Seleccione la extensión **Conector de Shopify**.
3. Seleccione la acción **Configurar** para abrir la página **Configuración de extensiones**.
4. Asegúrese de que el conmutador de alternancia **Permitir solicitudes HTTPClient** esté habilitado.

## <a name="rotate-the-shopify-access-token"></a>Rotar el token de acceso de Shopify

Los siguientes procedimientos describen cómo rotar el token de acceso utilizado por el conector de Shopify para acceder a su tienda de Shopify en línea.

### <a name="in-shopify"></a>En Shopify

1. Desde su **Administrador de Shopify**, vaya a [Aplicaciones](https://www.shopify.com/admin/apps).
2. Seleccione **Eliminar** en la fila con la aplicación **Dynamics 365 Business Central**.
3. En el mensaje que aparece, seleccione **Eliminar**.

### <a name="in-prod_short"></a>En [!INCLUDE[prod_short](../includes/prod_short.md)]

1. Elija el icono ![Bombilla que abre la función Dígame 1.](../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Tiendas de Shopify** y luego elija el enlace relacionado.
2. Seleccione la tienda para la que desea girar el token de acceoso para abrir la página **Tarjeta de tienda de Shopify**.
3. Elija la acción **Solicitar acceso**.
4. Si se le solicita, inicie sesión en su cuenta de Shopify, revise la privacidad y los permisos, y luego elija el botón **Instalar aplicación**.

## <a name="known-issues"></a>Problemas conocidos

### <a name="the-gen-bus-posting-group-cannot-be-zero-or-empty-there-must-be-a-value-in-the-customer-field"></a>*Grupo de contabilización de negocio* no puede ser cero o vacío; debe haber un valor en el campo del cliente

Rellene el campo **Código de plantilla de cliente** en la ventana **Tarjeta de tienda de Shopify** con la plantilla que tiene **Grupo contable negocio**. La plantilla de cliente se utiliza no solo para la creación de clientes, sino también para el cálculo del precio de venta y durante la creación de documentos de venta.

### <a name="importing-data-to-your-shopify-shop-isnt-enabled-go-to-the-shop-card-to-enable-it"></a>La importación de datos a su tienda Shopify no está habilitada. Vaya a la tarjeta de la tienda para habilitarla.

En la **Tarjeta de tienda de Shopify**, active la opción **Permitir la sincronización de datos para Shopify**. Esta opción está destinada a proteger la tienda en línea de obtener datos de demostración de [!INCLUDE[prod_short](../includes/prod_short.md)].

### <a name="oauth-error-invalid_request-could-not-find-shopify-api-application-with-api_key"></a>Oauth error invalid_request: No se pudo encontrar Aplicación API Shopify con api_key

Parece que usa [Insertar aplicación](/dynamics365/business-central/dev-itpro/deployment/embed-app-overview), donde la URL del cliente tiene el formato: `https://[application name].bc.dynamics.com`. El conector Shopify no funciona para las aplicaciones integradas. Para más información, ver [¿Qué productos de Microsoft tienen disponible el conector Shopify](shopify-faq.md#what-microsoft-products-is-the-shopify-connector-available-for).

## <a name="see-also"></a>Consulte también .

[Comenzar con el conector para Shopify](get-started.md)
