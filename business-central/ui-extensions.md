---
title: Personalizar Business Central Online con aplicaciones
description: Obtenga toda información sobre cómo agregar funcionalidad y personalizar Business Central mediante la instalación de las aplicaciones en este artículo.
author: edupont04
ms.topic: conceptual
ms.search.keywords: 'app, add-in, manifest, customize'
ms.search.form: '2500, 2502, 20350, 20353'
ms.date: 09/27/2022
ms.author: edupont
---
# <a name="customizing-business-central-online-with-apps" />Personalizar Business Central Online con aplicaciones

Puede cambiar [!INCLUDE[prod_short](includes/prod_short.md)] en línea instalando aplicaciones que agregan funciones, cambian el comportamiento o proporcionan acceso a nuevos servicios en línea, por ejemplo. Estas aplicaciones también se llaman *extensiones* porque *extienden* [!INCLUDE [prod_short](includes/prod_short.md)].

## <a name="manage-apps" />Administrar aplicaciones

[!INCLUDE [2023rw1-sec-group-short](includes/2023rw1-sec-group-short.md)]

Cuando inicia [!INCLUDE[prod_short](includes/prod_short.md)] por primera vez, ya están instaladas algunas aplicaciones. Con el tiempo, tendrá disponibles más aplicaciones y puede elegir si desea usar la aplicación o no.

Por ejemplo, Microsoft ofrece una aplicación que proporciona integración con PayPal Payments Standard. Esta extensión se instala por omisión. Pero si está disponible otra extensión que ofrece integración con otro servicio de pago, puede instalar la nueva extensión y seleccionar cuál de los dos servicios quiere usar.  

Para utilizar la funcionalidad que proporciona una aplicación, como abrir páginas, ejecutar informes, seleccionar acciones, etc., se le deben asignar los conjuntos de permisos que se instalan como parte de la aplicación.

Para instalar o desinstalar aplicaciones desde AppSource o añadir extensiones por suscriptor, debe tener los permisos adecuados. Debe ser miembro del grupo de usuarios **Admin extensión D365** o debe tener el conjunto de permisos de **ADMIN. EXTENS. - ADMIN** explícitamente. Si es administrador, puede asignar grupos de usuarios y permisos a otros usuarios de su empresa. Para obtener más información, vea [Crear usuarios de acuerdo con las licencias](ui-how-users-permissions.md).  

> [!IMPORTANT]  
> Para [!INCLUDE [prod_short](includes/prod_short.md)] local, no puede cargar extensiones por inquilino ni instalar aplicaciones AppSource a través de la página **Gestión de extensiones**. No puede instalar aplicación de AppSource locales, incluidas las implementaciones basadas en Docker.

Puede administrar las aplicaciones en la página **Administración de extensiones**. Puede acceder a esta página desde Inicio. De forma alternativa, seleccione el icono **Buscar página o informe** ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") en la esquina superior derecha, escriba **Extensión** y, a continuación, seleccione el enlace relacionado. Para más información, ver [Instalación y desinstalación de aplicaciones](ui-extensions-install-uninstall.md).

> [!NOTE]  
> Si cree que debería tener acceso a una aplicación pero no encuentra la funcionalidad, consulte la página **Administración de extensiones**; si la aplicación no aparece, puede instalarla tal como se describe en la sección siguiente.  

> [!NOTE]  
> Inicie sesión en [AppSource.microsoft.com](https://appsource.microsoft.com/) con la cuenta de correo electrónico que usa para [!INCLUDE[prod_short](includes/prod_short.md)] en línea. Use la misma cuenta de correo para otros servicios y productos para disfrutar de una experiencia agilizada.  

También puede ir al mercado de aplicaciones desde [!INCLUDE[prod_short](includes/prod_short.md)]. En la página **Gestión de extensiones**, puede ver las aplicaciones que están instaladas actualmente y puede abrir la página del **Mercado de extensiones** que muestra todas las aplicaciones para [!INCLUDE[prod_short](includes/prod_short.md)] que están disponibles actualmente en AppSource. Si elige el vínculo *Más aplicaciones* se le redireccionará a [AppSource.microsoft.com](https://appsource.microsoft.com/marketplace/apps?product=dynamics-365%3Bdynamics-365-business-central&page=1).  

Si selecciona una aplicación, puede consultar las funciones de la aplicación y acceder al sitio de ayuda de la aplicación para obtener más información. Cuando elige una aplicación debe aceptar las condiciones de uso. Si obtiene la aplicación del sitio web de AppSource, se requerirá el inicio de sesión en [!INCLUDE[prod_short](includes/prod_short.md)] para completar la instalación.  

Al instalar una aplicación, es posible que tenga que configurarla, por ejemplo, especificar una cuenta para usar con la extensión **Paypal Payments Standard para [!INCLUDE[prod_short](includes/prod_short.md)]**.
Otras aplicaciones simplemente agregan campos a una página existente o agregan una página nueva, por ejemplo.   

Si desinstala una aplicación y cambia de idea, puede volver a instalarla. Al desinstalar una aplicación que ha estado usando, los datos se guardan para que se vuelve a instalar la aplicación estén disponibles. Hay algunas aplicaciones que son obligatorias. No puede desinstalarlas de la página **Administración de extensiones**. Si lo intenta, aparece un mensaje de error.  

Algunas de las aplicaciones las proporciona Microsoft y otras las proporcionan [otras empresas](ui-extensions-other.md). Se prueban todas las aplicaciones antes de que estén disponibles, pero se recomienda acceder a los vínculos que se proporcionan con cada extensión para obtener más información sobre la aplicación antes de optar por instalarla.  

> [!NOTE]  
> Puede estar atento a las nuevas aplicaciones de Microsoft y otros proveedores en [AppSource.microsoft.com](https://appsource.microsoft.com/marketplace/apps?product=dynamics-365%3Bdynamics-365-business-central&page=1).

## <a name="apps-and-data-transfer" />Aplicaciones y transferencia de datos

Puesto que las siguientes aplicaciones se comunican con otros servicios, pueden transferir datos fuera de la geografía del entorno de [!INCLUDE[prod_short](includes/prod_short.md)]:

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

## <a name="connect-your-business" />Conectar el negocio

A partir de 2022, lanzamiento de versiones 2, los entornos en línea de [!INCLUDE [prod_short](includes/prod_short.md)] pueden enumerar una o más aplicaciones en las páginas **Aplicaciones de conectividad** y **Aplicaciones bancarias**. Estas aplicaciones pueden conectar su negocio a servicios externos para aumentar la productividad mediante la automatización de procesos. Por ejemplo, puede conectarse a sus bancos e importar transacciones bancarias automáticamente. Las aplicaciones son fáciles de instalar y configurar directamente desde esta página. Elija una aplicación para obtener más información sobre las capacidades y los precios.  

Vea la lista de aplicaciones sugeridas eligiendo la acción **Aplicaciones de conectividad** en la página **Gestión de extensiones**.  

> [!NOTE]
> La primera persona en abrir la página **Aplicaciones de conectividad** debe permitir que la extensión se conecte a un servicio externo. Permitir la conexión una vez o siempre. Si elige bloquear la conexión, debe encontrar las aplicaciones relevantes en AppSource.

Este servicio externo generará una lista de aplicaciones relevantes según su país o región

## <a name="recommended-apps" />Aplicaciones recomendadas

Los socios y distribuidores de Microsoft pueden crear aplicaciones que pueden usar para compilar listas de aplicaciones que a menudo recomiendan a sus clientes. Si lo hacen y han implementado la aplicación para su inquilino, las aplicaciones estarán disponibles en la página **Aplicaciones recomendadas**. Allí puede leer sobre cada aplicación y decidir si desea instalarlas.

> [!NOTE]
> Si es un socio o distribuidor de Microsoft y está interesado en proporcionar una lista de aplicaciones recomendadas, consulte [Recomendar aplicaciones de AppSource](/dynamics365/business-central/dev-itpro/administration/recommend-apps) en la administración de contenidos.

## <a name="see-related-microsoft-trainingtrainingmodulescustomize-dynamics-365-business-central" />Consultar la [formación de Microsoft](/training/modules/customize-dynamics-365-business-central/) relacionada

## <a name="see-also" />Consulte también .

[Instalar y desinstalar aplicaciones](ui-extensions-install-uninstall.md)  
[Personalizar Business Central](ui-customizing-overview.md)  
[Aplicaciones de Business Central de otros proveedores](ui-extensions-other.md)  
[Configurar el servicio Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md)  
[Permitir los pagos de clientes mediante servicios de pago](sales-how-enable-payment-service-extensions.md)  
[Migrar datos de empresa de otros sistemas financieros](across-import-data-configuration-packages.md)  
[Configurar la extensión Códigos postales de Reino Unido de GetAddress.io](LocalFunctionality/UnitedKingdom/uk-setup-postal-code-service.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] aplicaciones de otros proveedores](ui-extensions-other.md)  
[Preparación para hacer negocios](ui-get-ready-business.md)  

## <a name="includeprodshortincludesfreetrialmdmd" />[!INCLUDE[prod_short](includes/free_trial_md.md)]


[!INCLUDE[footer-include](includes/footer-banner.md)]
