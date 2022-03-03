---
title: Instalación de extensiones para personalizar Business Central
description: Obtenga toda información sobre cómo agregar funcionalidad y personalizar Business Central mediante la instalación de extensiones.
author: edupont04
ms.topic: conceptual
ms.search.keywords: app, add-in, manifest, customize
ms.date: 08/25/2021
ms.author: edupont
ms.openlocfilehash: 7839c4364f299619707b0a346b9b5d0db07e627b
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2022
ms.locfileid: "8132425"
---
# <a name="customizing-business-central-online-using-extensions"></a>Personalizar Business Central Online con extensiones

Puede cambiar [!INCLUDE[prod_short](includes/prod_short.md)] en línea instalando extensiones que agregan funciones, cambian el comportamiento o proporcionan acceso a nuevos servicios en línea, por ejemplo.

> [!NOTE]
> Para instalar o desinstalar extensiones desde AppSource o añadir extensiones por suscriptor, debe tener los permisos adecuados. Debe ser miembro de ADMIN. EXTENS. - Grupo de usuarios ADMIN o debe tener ADMIN. EXTENS. - Conjunto de permisos ADMIN. Si es administrador, puede asignar grupos de usuarios y permisos a otros usuarios de su empresa.
>
> Para utilizar la funcionalidad que proporciona una extensión, como abrir páginas, ejecutar informes, seleccionar acciones, etc., se le deben asignar los conjuntos de permisos que se instalan como parte de la extensión.

> [!NOTE]  
> El conjunto de permisos **ADMIN. EXTENS. - ADMIN** se introdujo en el primer lanzamiento de versiones de Business Central 2021 para sustituir al conjunto de permisos **ADMIN. EXTENS. D365** de versiones anteriores.

> [!IMPORTANT]  
> No se admite la carga de extensiones por inquilino y la instalación de extensiones de AppSource a través de la página **Administración de extensiones** para instalaciones locales. No puede instalar extensiones de AppSource locales, incluidas las implementaciones basadas en Docker.

Cuando inicia [!INCLUDE[prod_short](includes/prod_short.md)] por primera vez, ya están instaladas algunas extensiones. Con el tiempo, tendrá disponibles más extensiones y puede elegir si desea usar la extensión o no.

Por ejemplo, Microsoft ofrece una extensión que proporciona integración con PayPal Payments Standard. Esta extensión se instala por omisión.
Pero si está disponible otra extensión que ofrece integración con otro servicio de pago, puede instalar la nueva extensión y seleccionar cuál de los dos servicios quiere usar.  

Puede administrar las extensiones en la página **Administración de extensiones**. Puede acceder a esta página desde Inicio. De forma alternativa, seleccione el icono **Buscar página o informe** ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") en la esquina superior derecha, escriba **Extensión** y, a continuación, seleccione el enlace relacionado. Para más información, ver [Instalación y desinstalación de extensiones](ui-extensions-install-uninstall.md).

> [!NOTE]  
> Si cree que debería tener acceso a una extensión pero no encuentra la funcionalidad, consulte la página **Administración de extensiones**; si la extensión no aparece, puede instalarla tal como se describe en la sección siguiente.  

> [!NOTE]  
> Inicie sesión en [AppSource.microsoft.com](https://appsource.microsoft.com/) con la cuenta de correo electrónico que usa para [!INCLUDE[prod_short](includes/prod_short.md)] en línea. Use la misma cuenta de correo para otros servicios y productos para disfrutar de una experiencia agilizada.  

También puede ir al mercado de aplicaciones desde [!INCLUDE[prod_short](includes/prod_short.md)]. En la página **Gestión de extensiones**, puede ver las extensiones que están instaladas actualmente y puede abrir la página del **Mercado de extensiones** que muestra todas las extensiones para [!INCLUDE[prod_short](includes/prod_short.md)] que están disponibles actualmente en AppSource. Si elige el vínculo *Más aplicaciones* se le redireccionará a [AppSource.microsoft.com](https://appsource.microsoft.com/marketplace/apps?product=dynamics-365%3Bdynamics-365-business-central&page=1).  

Si selecciona una extensión, puede consultar las funciones de la extensión y acceder al sitio de ayuda de la extensión para obtener más información. Cuando elige una extensión debe aceptar las condiciones de uso. Si obtiene la extensión del sitio web de AppSource, se requerirá el inicio de sesión en [!INCLUDE[prod_short](includes/prod_short.md)] para completar la instalación.  

Al instalar una extensión, es posible que tenga que configurarla, por ejemplo, especificar una cuenta para usar con la extensión **Paypal Payments Standard para [!INCLUDE[prod_short](includes/prod_short.md)]**.
Otras extensiones simplemente agregan campos a una página existente o agregan una página nueva, por ejemplo.   

Si desinstala una extensión y cambia de idea, puede volver a instalarla. Al desinstalar una extensión que ha estado usando, los datos se guardan para que se vuelve a instalar la extensión estén disponibles. Hay algunas extensiones que son obligatorias. No puede desinstalarlas de la página **Administración de extensiones**. Si lo intenta, aparece un mensaje de error.  

Algunas de las extensiones las proporciona Microsoft y otras las proporcionan [otras empresas](ui-extensions-other.md). Se prueban todas las extensiones antes de que estén disponibles, pero se recomienda acceder a los vínculos que se proporcionan con cada extensión para obtener más información sobre la extensión antes de optar por instalarla.  

> [!NOTE]  
> Puede estar atento a las nuevas extensiones de Microsoft y otros proveedores en [AppSource.microsoft.com](https://appsource.microsoft.com/marketplace/apps?product=dynamics-365%3Bdynamics-365-business-central&page=1).


## <a name="extensions-and-data-transfer"></a>Extensiones y transferencia de datos

Puesto que las siguientes extensiones se comunican con otros servicios, pueden transferir datos fuera de la geografía del entorno de [!INCLUDE[prod_short](includes/prod_short.md)]:

* Extensión de AMC Banking 365 Fundamentals
* Analizador de imágenes
* Predicción de pago atrasado
* PayPal Payments Standard
* Previsión de ventas e inventario
* WorldPay Payments Standard

Esto también se aplica a algunas funcionalidades de la aplicación base, como las siguientes funciones:

* Previsión de flujo de efectivo
* Servicio de intercambio de documentos
* Conexiones de Dataverse
* Servicio OCR
* Online Map
* CIF/NIF de la UE Servicio

## <a name="recommended-apps"></a>Aplicaciones recomendadas
Los socios y distribuidores de Microsoft pueden crear extensiones que pueden usar para compilar listas de aplicaciones que a menudo recomiendan a sus clientes. Si lo hacen y han implementado la extensión para su inquilino, las aplicaciones estarán disponibles en la página **Aplicaciones recomendadas**. Allí puede leer sobre cada aplicación y decidir si desea instalarlas.

> [!NOTE]
> Si es un socio o distribuidor de Microsoft y está interesado en proporcionar una lista de aplicaciones recomendadas, consulte [Recomendar aplicaciones de AppSource](/dynamics365/business-central/dev-itpro/administration/recommend-apps).

## <a name="see-also"></a>Consulte también

[Personalizar Business Central](ui-customizing-overview.md)  
[Extensiones de Business Central de otros proveedores](ui-extensions-other.md)  
[Configurar el servicio Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md)  
[Permitir el pago de clientes mediante PayPal](sales-how-enable-payment-service-extensions.md)  
[Migrar datos de empresa de otros sistemas financieros](across-import-data-configuration-packages.md)  
[Configurar la extensión Códigos postales de Reino Unido de GetAddress.io](LocalFunctionality/UnitedKingdom/uk-setup-postal-code-service.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] Extensiones de otros proveedores](ui-extensions-other.md)  
[Preparación para hacer negocios](ui-get-ready-business.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
