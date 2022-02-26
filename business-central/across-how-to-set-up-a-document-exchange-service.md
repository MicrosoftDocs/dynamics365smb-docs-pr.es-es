---
title: 'Procedimiento: Configurar un servicio de intercambio de documentos | Documentos de Microsoft'
description: Para intercambiar documentos electrónicos con socios comerciales se usa un proveedor de servicios externo.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/11/2021
ms.author: edupont
ms.openlocfilehash: eea1b946814803c1f05d5b4985d3c5330931fbc6
ms.sourcegitcommit: 6ad0a834fc225cc27dfdbee4a83cf06bbbcbc1c9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2021
ms.locfileid: "7588756"
---
# <a name="set-up-a-document-exchange-service"></a>Configurar un servicio de intercambio de documentos
Como parte del marco de intercambio de datos, puede intercambiar documentos de compra y venta con sus socios comerciales sin pasos adicionales, como adjuntar los documentos a mensajes de correo electrónico como archivos PDF. Por ejemplo, cuando esté listo para facturar a un cliente, puede registrar la factura y enviarla para su pago como un archivo que su cliente puede recibir en su aplicación de administración comercial. Para obtener más información, vea [Intercambio de datos electrónicamente](across-data-exchange.md).

> [!NOTE]
> La configuración de un servicio de intercambio de documentos para Business Central local requiere algunos pasos adicionales para la autorización. Para obtener más información, consulte [Configuración para Business Central local](#settings-for-business-central-on-premises).

## <a name="connecting-with-trading-partners"></a>Conexión con socios comerciales
El intercambio de documentos electrónicos requiere una conexión con sus socios comerciales. Para facilitar la creación de una conexión segura, [!INCLUDE[prod_short](includes/prod_short.md)] en línea se configura para utilizar la aplicación de integración de Business Central. La aplicación está disponible en la tienda de aplicaciones Tradeshift, y todo lo que usted y sus socios comerciales deben hacer es crear una cuenta de Tradeshift y luego habilitar la aplicación. La aplicación de integración de Business Central se encuentra en versiones de producción y de entorno aislado. Por ejemplo, usar la versión espacio aislado es bueno para probar el intercambio de documentos. Puede cambiar entre las versiones de producción y espacio aislado activando o desactivando el botón de alternancia **Espacio aislado** en la página **Configuración servicio intercambio documentos**. Cuando lo haga, la información de la ficha desplegable **Servicio** se actualiza automáticamente.

Alternativamente, si desea utilizar otro servicio, debe proporcionar información para realizar la conexión. Para obtener más información, vea [Para conectar con un servicio de intercambio de documentos](across-how-to-set-up-a-document-exchange-service.md#to-connect-to-a-document-exchange-service).

## <a name="to-connect-to-the-business-central-integration-app-on-tradeshift"></a>Para conectarse a la aplicación de integración de Business Central en Tradeshift
Puede crear rápidamente una cuenta de Tradeshift y comenzar con la aplicación de integración de Business Central desde la página **Configuración servicio intercambio documentos**. Elija el enlace **Activar aplicación** en la notificación o el campo **URL de la aplicación** para ir a la aplicación en la tienda de aplicaciones Tradeshift. En la página de inicio de sesión de Tradeshift, inicie sesión o regístrese.

> [!NOTE]
> Después de iniciar sesión en su cuenta de Tradeshift, es posible que el sitio no lo lleve a la página donde activa la aplicación. Para ello, puede hacer clic en el enlace en la página **Configuración servicio intercambio documentos** en Business Central nuevamente para ir directamente a la aplicación.

Si decide dejar de usar la aplicación de integración de Business Central, debe desactivarla en la tienda de aplicaciones Tradeshift. 

## <a name="to-connect-to-a-document-exchange-service"></a>Para conectar con un servicio de intercambio de documentos  
Si prefiere utilizar otro servicio de intercambio de documentos, debe proporcionar cierta información para conectarse al servicio.

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Configuración servicio intercambio documentos** y luego elija el enlace relacionado.  
2. Rellene los campos tal como se describe en la tabla siguiente.  

    |Campo|Descripción|  
    |---------------------------------|---------------------------------------|  
    |**Agente de usuario**|Escriba texto que pueda usarse para identificar a la empresa en los procesos de intercambio de documentos.|  
    |**Habilitado**|Especifique si está habilitada la conexión al servicio.<br><br> **Nota:** Cuando se activa el servicio, se crean al menos dos movimientos de cola de proyectos para enviar y recibir documentos electrónicos. Cuando se deshabilita el servicio, se eliminan los movimientos de la cola de proyectos.|  
    |**Espacio aislado**|Especifique si se está conectando a una versión de espacio aislado del servicio de intercambio de documentos.|
    |**URL de registro**|Especifique la página web donde se inscribe para el servicio de intercambio de documentos.|  
    |**URL de aplicación**|Elija el enlace para abrir la tienda de aplicaciones y activar o desactivar la aplicación de integración de Business Central.|
    |**URL de servicio**|Especifique la dirección del servicio de intercambio de documentos, al que se llamará cuando se envíen y se reciban documentos electrónicos.|  
    |**URL de inicio de sesión**|Especifique el URL de la página que utiliza para iniciar sesión en el servicio de intercambio de documentos. Esta es la página donde ingresa el nombre de usuario y la contraseña de su empresa.|  
    
    > [!NOTE]  
    > Sus credenciales de inicio de sesión se cifran automáticamente. No puede desactivar el cifrado.

    > [!NOTE]
    > Si no puede conectarse al servicio de intercambio de documentos debido a un problema de autorización, puede ser porque [!INCLUDE[prod_short](includes/prod_short.md)] no puede renovar automáticamente el token de acceso. Por ejemplo, esto podría ocurrir si no ha utilizado el servicio durante algún tiempo. Puede renovar el token manualmente utilizando la acción **Renovar token**.

## <a name="settings-for-business-central-on-premises"></a>Configuración de Business Central local
Para conectar Business Central local debe crear una aplicación en la tienda de aplicaciones Tradeshift. Cuando lo haga, utilice el URL de redireccionamiento del campo **URL de redireccionamiento** en la página **Configuración del servicio de intercambio de documentos**. Después de registrar su aplicación, Tradeshift le proporcionará un ID de cliente y un secreto de cliente. En [!INCLUDE[prod_short](includes/prod_short.md)], ingrese esos valores en la ficha desplegable **Autorización** en la página **Configuración del servicio de intercambio de documentos**.

Si prefiere almacenar el identificador y el secreto de la aplicación en una ubicación diferente, puede dejar en blanco los campos Id . del cliente y Secreto del cliente y escribir una extensión para obtener el identificador y el secreto de la ubicación. Puede proporcionar el secreto en tiempo de ejecución suscribiéndose a los eventos OnGetClientId y OnGetClientSecret en codeunit 1410 "Configuración servicio intercambio documentos".

## <a name="see-also"></a>Consulte también  
[Configuración del intercambio de datos](across-set-up-data-exchange.md)  
[Intercambio de datos electrónicamente](across-data-exchange.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]