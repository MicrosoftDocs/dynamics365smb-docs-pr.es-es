---
title: Personalizar Business Central Online con aplicaciones
description: Obtenga toda información sobre cómo agregar funcionalidad y personalizar Business Central mediante la instalación de las aplicaciones en este artículo.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: solsen
ms.topic: conceptual
ms.search.keywords: 'app, add-in, manifest, customize'
ms.search.form: '2500, 2502, 20350, 20353'
ms.date: 06/27/2024
ms.service: dynamics-365-business-central
---
# <a name="customizing-business-central-online-using-apps"></a>Personalizar Business Central Online con aplicaciones

Puede cambiar [!INCLUDE[prod_short](includes/prod_short.md)] en línea instalando aplicaciones que agregan funciones, cambian el comportamiento o proporcionan acceso a nuevos servicios en línea, por ejemplo. Estas aplicaciones también se llaman *extensiones* porque *extienden* [!INCLUDE [prod_short](includes/prod_short.md)].

## <a name="manage-apps"></a>Administrar aplicaciones

Cuando inicia [!INCLUDE[prod_short](includes/prod_short.md)] por primera vez, ya están instaladas algunas aplicaciones. Con el tiempo, tendrá disponibles más aplicaciones y puede elegir si desea usar la aplicación o no.

Por ejemplo, Microsoft ofrece una aplicación que permite la integración con PayPal Payments Standard. Esta extensión se instala por omisión. Sin embargo, podría aparecer una extensión que ofrezca integración con otro servicio de pago. En ese caso, puede instalar la nueva extensión y luego elegir cuál usar.  

Para usar una aplicación, debe tener asignados los conjuntos de permisos que vienen con ella.

Para instalar o desinstalar aplicaciones desde AppSource o añadir extensiones por suscriptor, debe tener los permisos adecuados. Debe ser miembro del grupo de usuarios **Admin extensión D365** o debe tener el conjunto de permisos de **ADMIN. EXTENS. - ADMIN** explícitamente. Si usted es administrador, puede asignar grupos de usuarios y permisos a otros usuarios de su empresa. Para obtener más información, vea [Crear usuarios de acuerdo con las licencias](ui-how-users-permissions.md).  

> [!IMPORTANT]  
> Para [!INCLUDE [prod_short](includes/prod_short.md)] local, no puede cargar extensiones por inquilino ni instalar aplicaciones AppSource a través de la página **Gestión de extensiones**. No puede instalar aplicación de AppSource locales, incluidas las implementaciones basadas en Docker.

Puede administrar las aplicaciones en la página **Administración de extensiones**. Puede acceder a esta página desde Inicio. De forma alternativa, seleccione el icono **Buscar página o informe** ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") en la esquina superior derecha, escriba **Extensión** y, a continuación, seleccione el enlace relacionado. Para más información, ver [Instalación y desinstalación de aplicaciones](ui-extensions-install-uninstall.md).

> [!NOTE]  
> Si cree que debería tener acceso a una aplicación pero no encuentra la funcionalidad, consulte la página **Administración de extensiones**; si la aplicación no aparece, puede instalarla tal como se describe en la sección siguiente.  

> [!NOTE]  
> Inicie sesión en [AppSource.microsoft.com](https://appsource.microsoft.com/) con la cuenta de correo electrónico que usa para [!INCLUDE[prod_short](includes/prod_short.md)] en línea. Use la misma cuenta de correo para otros servicios y productos para disfrutar de una experiencia agilizada.  

También puede obtener AppSource desde [!INCLUDE[prod_short](includes/prod_short.md)]. En la página **Administración de extensiones**, puede ver las aplicaciones que están instaladas actualmente y puede abrir la página **Aplicaciones de Microsoft AppSource** que muestra todas las aplicaciones de [!INCLUDE[prod_short](includes/prod_short.md)] que están disponibles actualmente en AppSource. Si elige la acción **Ver AppSource**, se le redireccionará a [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646). Para obtener más información, consulte [Administrar aplicaciones de AppSource](admin-manage-appsource-apps.md).

Si selecciona una aplicación, puede consultar las funciones de la aplicación y acceder al sitio de ayuda de la aplicación para obtener más información. Cuando elige una aplicación debe aceptar las condiciones de uso. Si obtiene la aplicación del sitio web de AppSource, inicie sesión en [!INCLUDE[prod_short](includes/prod_short.md)] para completar la instalación.  

Al instalar una aplicación, es posible que tenga que configurarla, por ejemplo, especificar una cuenta para usar con la extensión **Paypal Payments Standard para [!INCLUDE[prod_short](includes/prod_short.md)]**. Otras aplicaciones agregan campos a una página existente o agregan una página nueva, por ejemplo.

Si desinstala una aplicación y cambia de idea, puede volver a instalarla. Cuando desinstala una aplicación, sus datos se conservan. Si vuelve a instalar la aplicación, seguirá estando disponible. Hay algunas aplicaciones que son necesarias y no puede desinstalarlas desde la página **Administración de extensiones**.

Algunas de las aplicaciones las proporciona Microsoft y otras las proporcionan [otras empresas](ui-extensions-other.md). Se prueban todas las aplicaciones antes de que estén disponibles, pero se recomienda acceder a los vínculos que se proporcionan con cada extensión para obtener más información sobre la aplicación antes de optar por instalarla.  

> [!NOTE]  
> Puede estar atento a las nuevas aplicaciones de Microsoft y otros proveedores en [AppSource.microsoft.com](https://appsource.microsoft.com/marketplace/apps?product=dynamics-365%3Bdynamics-365-business-central&page=1).

## <a name="apps-and-data-transfer"></a>Aplicaciones y transferencia de datos

Puesto que las siguientes aplicaciones se comunican con otros servicios, pueden transferir datos fuera de la geografía del entorno de [!INCLUDE[prod_short](includes/prod_short.md)]:

* Extensión de AMC Banking 365 Fundamentals
* Analizador de imágenes
* Predicción de pago atrasado
* PayPal Payments Standard
* Previsión de ventas e inventario
* WorldPay Payments Standard

Lo mismo ocurre con la aplicación base, como las siguientes capacidades:

* Previsión de flujo de efectivo
* Servicio de intercambio de documentos
* Conexiones de Dataverse
* Servicio OCR
* Online Map
* CIF/NIF de la UE Servicio

## <a name="connect-your-business"></a>Conectar el negocio

A partir de 2022, lanzamiento de versiones 2, los entornos en línea de [!INCLUDE [prod_short](includes/prod_short.md)] pueden enumerar una o más aplicaciones en las páginas **Aplicaciones de conectividad** y **Aplicaciones bancarias**. Estas aplicaciones pueden conectar su negocio a servicios externos para aumentar la productividad mediante la automatización de procesos. Por ejemplo, puede conectarse a sus bancos e importar transacciones bancarias automáticamente. Las aplicaciones son fáciles de instalar y configurar directamente desde esta página. Elija una aplicación para obtener más información sobre las capacidades y los precios.  

Vea la lista de aplicaciones sugeridas eligiendo la acción **Aplicaciones de conectividad** en la página **Gestión de extensiones**.  

> [!NOTE]
> La primera persona en abrir la página **Aplicaciones de conectividad** debe permitir que la extensión se conecte a un servicio externo. Permitir la conexión una vez o siempre. Si elige bloquear la conexión, debe encontrar las aplicaciones relevantes en AppSource.

Este servicio externo genera una lista de aplicaciones relevantes según su país o región

## <a name="recommended-apps"></a>Aplicaciones recomendadas

Los socios y distribuidores de Microsoft pueden crear aplicaciones que pueden usar para compilar listas de aplicaciones que a menudo recomiendan a sus clientes. Si lo hacen y han implementado la aplicación para su inquilino, las aplicaciones estarán disponibles en la página **Aplicaciones recomendadas**. Allí puede leer sobre cada aplicación y decidir si desea instalarlas.

> [!NOTE]
> Si es un socio o distribuidor de Microsoft y está interesado en proporcionar una lista de aplicaciones recomendadas, consulte [Recomendar aplicaciones de AppSource](/dynamics365/business-central/dev-itpro/administration/recommend-apps) en la administración de contenidos.

## <a name="see-also"></a>Consulte también .

[Instalar y desinstalar aplicaciones](ui-extensions-install-uninstall.md)  
[Personalizar Business Central](ui-customizing-overview.md)  
[Aplicaciones de Business Central de otros proveedores](ui-extensions-other.md)  
[Configurar el servicio Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md)  
[Permitir los pagos de clientes mediante servicios de pago](sales-how-enable-payment-service-extensions.md)  
[Migrar datos de empresa de otros sistemas financieros](across-import-data-configuration-packages.md)  
[Configurar la extensión Códigos postales de Reino Unido de GetAddress.io](LocalFunctionality/UnitedKingdom/uk-setup-postal-code-service.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] aplicaciones de otros proveedores](ui-extensions-other.md)  
[Preparación para hacer negocios](ui-get-ready-business.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
