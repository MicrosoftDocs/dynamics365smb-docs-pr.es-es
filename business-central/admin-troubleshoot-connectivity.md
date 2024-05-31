---
title: Solucionar problemas de conectividad
description: Describe cómo usar la página Solucionar problemas de conectividad para identificar y solucionar problemas de conexión a Business Central online.
author: jswymer
ms.topic: get-started
ms.devlang: al
ms.search.keywords: 'connectivity, troubleshooting, connection problems'
ms.date: 11/24/2023
ms.author: jswymer
ROBOTS: NOINDEX
ms.service: dynamics-365-business-central
---

# Solucionar problemas de conectividad con Business Central

> **SE APLICA A:** [!INCLUDE[prod_short](includes/prod_short.md)] Online
>
> Esta característica está actualmente en versión preliminar. La funcionalidad y la documentación pueden cambiar en versiones posteriores. Si desea contribuir a la documentación basándose en sus propios hallazgos, seleccione ![Editar artículo en GitHub.](media/github-edit-pencil.png) **Editar** y proponer cambios. ¡Entonces echaremos un vistazo!

[!INCLUDE[prod_short](includes/prod_short.md)] Online incluye la página **Solución de problemas de conectividad** que puede utilizar para identificar problemas con su conexión al servicio en línea. Hay varias cosas que afectan la conectividad a Business Central, como la configuración del firewall de su red o la configuración del servicio de nombres de dominio. La página le permite ejecutar una lista de comprobaciones que diagnostican problemas comunes de conectividad de Business Central. Puede utilizar la información para intentar solucionar los problemas usted mismo o transmitirla a su representante de soporte.

> [!NOTE]
> La página **Solución de problemas de conectividad** no prueba el rendimiento o la confiabilidad de la red, como la velocidad de su conexión. Solo verifica la conectividad con diferentes recursos.

## Iniciar la verificación de conectividad 

1. Abra un navegador de Internet.
2. En la dirección, ingrese la URL que usa para abrir Business Central y agregue `/connectivity` al final. 

    Por ejemplo, si usa `https://businesscentral.dynamics.com`, luego ingrese:

    ```http
    https://businesscentral.dynamics.com/connectivity
    ```

    O, si la URL incluye el ID de inquilino, como `https://businesscentral.dynamics.com/12345678-1234-1234-1234-1234567890AB`, luego ingresaría:

    ```http
    https://businesscentral.dynamics.com/12345678-1234-1234-1234-1234567890AB/connectivity
    ```
 
3. En la página **Solución de problemas de conectividad**, elija **Iniciar comprobación**.

    Se ejecutan una serie de comprobaciones y se muestra el resultado de cada comprobación:

    - ![La comprobación de conectividad se realizó correctamente.](media/connectivity-check.png) indica que la verificación se realizó correctamente.
    - ![Error en comprobación de conectividad.](media/connectivity-failed.png) indica que la verificación produjo error. Revise el mensaje debajo de la marca de verificación para obtener más detalles.
    - ![No se ejecutó la verificación de conectividad.](media/connectivity-blocked.png) indica que la verificación no se ejecutó, generalmente debido a una falla en una verificación anterior. Revise el mensaje debajo de la marca de verificación para obtener más detalles.

4. Para ejecutar la verificación nuevamente, elija **Reiniciar comprobación**.

Las siguientes secciones explican las comprobaciones que se ejecutan y proporcionan algunos consejos para solucionar cualquier problema.

## Conectividad básica a Internet

Comprueba que tiene conexión a Internet verificando que puede acceder a un dominio público conocido, como www.bing.com.

|Problema|Soluciones que puede probar|
|-------|-------------|
|Su navegador no admite esta verificación|Abra la página en un navegador compatible y vuelva a intentarlo. Para obtener una lista de navegadores compatibles, consulte [Requisitos mínimos para utilizar Business Central - Exploradores](product-requirements.md#browsers)|
|Error al hacer ping al servidor en la siguiente URL: {url}|Compruebe la configuración del firewall.|

## Carga de recursos de CDN (content delivery network)

[!INCLUDE[prod_short](includes/prod_short.md)] usa Azure Content Delivery Network (CDN) para proporcionar recursos necesarios para ejecutar el cliente web de Business Central. Esta comprobación verifica que los recursos necesarios estén disponibles y accesibles haciendo ping a la instancia de Business Central en CDN.

|Problema|Soluciones que puede probar|
|-------|-------------|
|Su navegador no admite esta verificación|Vea la comprobación de **Conectividad básica a Internet**.|
|Error al hacer ping al servidor en la siguiente URL: {url}|Compruebe la configuración del firewall.|

## Autenticación de usuario

Comprueba que el usuario actual inicia sesión con una cuenta de Business Central válida.

|Problema|Soluciones que puede probar|
|-------|-------------|
|Ningún usuario está autenticado actualmente|Inicie sesión en Business Central con un nombre de usuario y una contraseña válidos.|

## Descubrimiento de entornos de Business Central

Comprueba los entornos de Business Central que están disponibles para un usuario autenticado y luego verifica si el usuario puede autenticarse en el entorno.
<!-- example: Your user name or password is incorrect, or you do not have a valid account.. Request duration: 332 milliseconds)-->

|Problema|Soluciones que puede probar|
|-------|-------------|
|Ningún usuario autenticado para realizar esta verificación|Vea la comprobación de **Autenticacion de usuario**.|
|Error al recuperar entornos disponibles para su cuenta.|Consulte la lista de entornos disponibles en el centro de administración de Business Central.|
|Su nombre de usuario o contraseña no son correctos, o no dispone de una cuenta válida.| Verifique que inicia sesión con el nombre de usuario y la contraseña correctos.|

## Conectividad del servicio de la aplicación

Comprueba que el usuario autenticado pueda conectarse a un entorno descubierto, normalmente comenzando con el entorno de producción.

|Problema|Soluciones que puede probar|
|-------|-------------|
|Ningún usuario autenticado para realizar esta verificación|Vea la comprobación de **Autenticacion de usuario**.|
|Error al recuperar entornos disponibles para su cuenta.|Vea **Descubrimiento de entornos de Business Central**.|
|No hay dirección de agrupación para realizar esta verificación|Consulte la lista de entornos disponibles en el centro de administración de Business Central.|
|El punto final de la versión no existe|Consulte la lista de entornos disponibles en el centro de administración de Business Central.|

## Conectividad del servidor web

Comprueba que el usuario autenticado puede establecer correctamente conexiones con el servidor web.

|Problema|Soluciones que puede probar|
|-------|-------------|
|No hay ningún usuario autenticado para realizar esta comprobación|Vea la comprobación de **Autenticacion de usuario**.|
|Error al recuperar entornos disponibles para su cuenta.|Vea **Descubrimiento de entornos de Business Central**.|
|No hay dirección de agrupación para realizar esta verificación|Consulte la lista de entornos disponibles en el centro de administración de Business Central.|
|No se pudo establecer una conexión con el servidor web|Borre el caché y vuelva a cargar la página.|

## Estado de mantenimiento del servicio

Informa sobre el estado de salud del servicio de Business Central comprobando las interrupciones declaradas.

|Problema|Soluciones que puede probar|
|-------|-------------|
|No hay ningún usuario autenticado para realizar esta comprobación|Vea la comprobación de **Autenticacion de usuario**.|
|Lo sentimos, Business Central no está disponible temporalmente. Vuelva a intentarlo más tarde.|Vuelva a intentarlo más tarde.|

## Consulte también

[Recursos de ayuda y soporte técnico](product-help-and-support.md)  
[Resumen de tareas para configurar Business Central](setup.md)  
[Preguntas frecuentes sobre el uso de Business Central](across-faq.yml)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[El centro de administración de Business Central](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center)

[!INCLUDE[footer-include](includes/footer-banner.md)]
