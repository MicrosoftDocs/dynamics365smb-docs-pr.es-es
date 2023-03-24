---
title: Configuración del explorador
description: Describe cómo configurar los navegadores para que funcionen con Business Central y los productos que se integran con él.
author: jswymer
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'Teams, web client, troubleshooting, errors'
ms.date: 04/01/2021
ms.author: jswymer
---
# Configuración y solución de problemas de su navegador para que funcione con Business Central Web Client

Este artículo explica cómo configurar su navegador para que [!INCLUDE[web_client](includes/web_client.md)] y todas sus características funcionan correctamente. Lea este artículo si tiene problemas para abrir [!INCLUDE[web_client](includes/web_client.md)], porque algunos problemas pueden deberse a la configuración de su navegador.

El artículo proporciona detalles para configurar Microsoft Edge, pero los requisitos para JavaScript, cookies y ventanas emergentes son los mismos para todos los navegadores compatibles. Para otros navegadores, consulte las instrucciones proporcionadas por el fabricante.  

## Usar un explorador admitido

Asegúrese de utilizar uno de los navegadores compatibles. Consulte [Requisitos mínimos para usar Business Central](product-requirements.md#browsers).  

## Permitir JavaScript desde Business Central

*Problema:*

Si el navegador no permite JavaScript, verá **JavaScript no compatible/desactivado** en la barra de direcciones y un mensaje **Error HTTP 404.0: no encontrado** cuando intente abrir [!INCLUDE[prod_short](includes/prod_short.md)] y 

<!-- http://localhost:8080/NotSupported/DisabledJavaScript HTTP Error 404.0 - Not Found
The resource you are looking for has been removed, had its name changed, or is temporarily unavailable. -->

*Reparar:*

1. En Microsoft Edge, vaya a **Configuraciones** > **Cookies y permisos del sitio** > **JavaScript**.
2. Realice una de los siguientes pasos. Elija el paso recomendado por su organización:

    - Mueva el control de alternancia **Permitido** a la izquierda (Desactivado). Luego, seleccione **Añadir** y escriba la dirección (URL) para [!INCLUDE[prod_short](includes/prod_short.md)] en el cuadro **Sitio**. Seleccione **Añadir** cuando termine.
    - Mueva el control de alternancia **Permitido** a la derecha (Activado).

## Permitir cookies desde Business Central

*Problema:*

Si el navegador no permite cookies, obtendrá el siguiente error:

**Lo siento, no se pudo encontrar la página. Compruebe la dirección e inténtelo de nuevo.** 

*Reparar:*

1. En Microsoft Edge, vaya a **Configuraciones** > **Cookies y permisos del sitio** > **Cookies y datos del sitio**.
2. Mueva el control de alternancia **Permitir que los sitios guarden y lean datos de cookies** a la derecha (activado).  

## <a name="popup"></a>Permitir ventanas emergentes desde Business Central

[!INCLUDE[prod_short](includes/prod_short.md)] se integra con varios productos. En algunos casos, como con Microsoft Teams, [!INCLUDE[prod_short](includes/prod_short.md)] se abre, o emerge, dentro del producto. Esta capacidad requiere que su navegador permita ventanas emergentes de [!INCLUDE[prod_short](includes/prod_short.md)].

*Problema:*

Si las ventanas emergentes para [!INCLUDE[prod_short](includes/prod_short.md)] están bloqueadas, recibe un mensaje similar al siguiente:

**Algo salió mal. Es posible que su navegador esté bloqueando las ventanas emergentes que necesita Business Central.**

<!--
Something went wrong
Your browser may be blocking pop-ups needed by Business Central.

Change your browser settings to allow pop-ups or allow this for trusted domains, then try again.
If these settings are managed for your organization, you should contact your administrator for assistance.

Try again
-->
*Reparar:*

1. En Microsoft Edge, vaya a **Configuraciones** > **Cookies y permisos del sitio** > **Ventanas emergentes y redireccionamientos**.
2. Mueva el control de alternancia **Bloqueado** a la derecha (Activado).
3. Seleccione **Añadir**. En el cuadro **Sitio**, escriba `https://businesscentral.dynamics.com`, luego seleccione **Añadir**.

## Consulte también

[Consejos para la solución de problemas de Teams](admin-teams-troubleshooting.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]