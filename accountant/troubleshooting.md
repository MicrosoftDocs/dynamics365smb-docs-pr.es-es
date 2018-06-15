---
title: Maneras de solucionar problemas | Documentos de Microsoft
description: "Obtener información sobre cómo solucionar problemas en el Accountant Hub de Dynamics 365."
author: edupont04
ms.service: dynamics365-accountant
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, troubleshoot
ms.date: 10/23/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: acef03f32124c5983846bc6ed0c4d332c9c8b347
ms.openlocfilehash: e4f739e13123054527bf3116aec2c8c4133537e6
ms.contentlocale: es-es
ms.lasthandoff: 04/16/2018

---
# <a name="troubleshooting-include-d365acclongincludesd365acclongmdmd"></a>Solución de problemas de [!INCLUDE [d365acc_long](includes/d365acc_long_md.md)]
[!INCLUDE [d365fin_early_release](includes/d365fin_early_release.md.md)]

Registrarse en [!INCLUDE [d365acc](includes/d365acc_md.md)] es muy fácil y se puede realizar muy rápidamente. Agregar clientes al escritorio también es sencillo, si no este artículo le ayudará a solucionar los problemas que puedan surgirle.

## <a name="what-email-address-can-i-use-with-include-d365accincludesd365accmdmd"></a>¿Qué dirección de correo electrónico puedo usar en [!INCLUDE [d365acc](includes/d365acc_md.md)]?
Para iniciar sesión, [!INCLUDE [d365acc](includes/d365acc_md.md)] requiere una dirección de correo electrónico del trabajo o la escuela. [!INCLUDE [d365acc](includes/d365acc_md.md)] no admite direcciones de correo electrónico proporcionadas por servicios de correo electrónico del consumidor ni por proveedores de la telecomunicación. Esto incluye outlook.com, hotmail.com, gmail.com y otros.  

Si intenta iniciar sesión con una dirección de correo personal, recibirá un mensaje indicando que use una dirección del trabajo o la escuela.  

## <a name="why-cant-i-connect-to-my-clients-data"></a>¿Por qué no puedo conectarme a los datos de mi cliente?
Puede haber un par de razones, incluidas las siguientes:

- La dirección URL del campo **Dirección URL de cliente** no es válida  

  Vaya a **Administrar clientes**, abra el cliente al que no puede conectarse y seleccione **Probar dirección URL de cliente**.  
- La empresa del cliente está actualmente fuera de línea, por ejemplo, si se está actualizando

  En el escritorio, seleccione el elemento de menú **Herramientas** y, a continuación, elija **Comprobar errores**. De esta manera se abrirá una lista con detalles técnicos, por lo que es posible que desee ponerse en contacto con su administrador si encuentra errores. Por ejemplo, el mensaje de error "El servidor ha rechazado las credenciales del cliente" sugiere que no tiene acceso.  
- No ha recibido un correo electrónico de su cliente que lo invite a su [!INCLUDE [d365fin](includes/d365fin_md.md)], no ha abierto el enlace en el correo electrónico, o no ha aceptado la invitación.

  Debe abrir el enlace en la invitación y aceptar los pasos que lo agregan al [!INCLUDE [d365fin](includes/d365fin_md.md)] de su cliente. Hasta ese momento, no tendrá acceso a sus datos.  
- No tiene acceso a todas las empresas en el [!INCLUDE [d365fin](includes/d365fin_md.md)] de su cliente

  El cliente puede tener varias empresas o unidades de negocio en [!INCLUDE [d365fin](includes/d365fin_md.md)] y la invitación no siempre incluye todas las empresas. Ejecute su cliente para asegurarse de que tiene acceso a las empresas en las que el cliente quiere que trabaje.  

## <a name="why-doesnt-the-data-refresh-in-my-dashboard"></a>¿Por qué no se actualizan los datos de mi escritorio?
Cuando se agrega a un cliente o solicita una actualización de los datos, [!INCLUDE [d365acc](includes/d365acc_md.md)] busca los datos. Pero debe actualizar la ventana, mediante la acción "Volver a mostrar todas las compañías", actualizar la ventana del navegador, navegar desde el panel de control y luego volver de nuevo, o alguna acción similar. Es un problema en el que estamos trabajando para mejorarlo en una actualización posterior.  

## <a name="see-also"></a>Consulte también
[Introducción a [!INCLUDE[d365acc](includes/d365acc_md.md)]](get-started.md)  
[Agregar clientes al escritorio de [!INCLUDE[d365acc](includes/d365acc_md.md)]](add-client.md)  

