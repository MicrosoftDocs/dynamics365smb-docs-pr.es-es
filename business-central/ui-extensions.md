---
title: Instalación de extensiones para personalizar Business Central
description: Obtenga toda información sobre cómo agregar funcionalidad y personalizar Business Central mediante la instalación de extensiones.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: app, add-in, manifest, customize
ms.date: 06/23/2021
ms.author: edupont
ms.openlocfilehash: 073b89f7c80035da12f329f752b64dc8142f309d
ms.sourcegitcommit: e562b45fda20ff88230e086caa6587913eddae26
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "6325589"
---
# <a name="customizing-business-central-online-using-extensions"></a>Personalizar Business Central Online con extensiones

Puede cambiar [!INCLUDE[prod_short](includes/prod_short.md)] en línea instalando extensiones que agregan funciones, cambian el comportamiento o proporcionan acceso a nuevos servicios en línea, por ejemplo.

> [!NOTE]
> Para instalar extensiones desde AppSource o añadir extensiones por suscriptor, debe tener los permisos adecuados. Debe ser miembro del grupo de usuarios D365 EXTENSION MGT o debe tener el conjunto de permisos de ADMIN EXTENSIÓN MGT. Si es administrador, puede asignar grupos de usuarios y permisos a otros usuarios de su empresa.

Para utilizar la funcionalidad que proporciona una extensión, como abrir páginas, ejecutar informes, seleccionar acciones, etc., se le deben asignar los conjuntos de permisos que se instalan como parte de la extensión.

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

Microsoft proporciona las extensiones siguientes:  

* [Extensión AMC Banking 365 Fundamentals](ui-extensions-amc-banking.md)
* [Nóminas de Ceridian](ui-extensions-ceridian-payroll.md)
* [Hub de empresas](ui-extensions-company-hub.md)  
* [Migración de datos de Dynamics GP](ui-extensions-dynamicsgp-data-migration.md)
* [Envestnet Yodlee Bank Feeds](ui-extensions-yodlee-bank-feeds.md)
* [Información de la empresa esencial](ui-extensions-essential-business-insights.md)
* [Analizador de imágenes](ui-extensions-image-analyzer.md)
* [Nube inteligente](ui-extensions-data-replication.md)
* [Base de nube inteligente](ui-extensions-intelligent-cloud.md)  
* [Predicciones de pago atrasado](ui-extensions-late-payment-prediction.md)
* [Microsoft Pay](ui-extensions-microsoft-pay-payments.md)
* [PayPal Payments Standard](ui-extensions-paypal-payments-standard.md)
* [Migración de datos de QuickBooks](ui-extensions-quickbooks-data-migration.md)
* [Migración de datos de QuickBooks Online](ui-extensions-quickbooks-online-data-migration.md)
* [Importación del archivo de nómina de QuickBooks](ui-extensions-quickbooks-payroll.md)
* [Previsión de ventas e inventario](ui-extensions-sales-forecast.md)
* [Grupo de IVA](ui-extensions-vat-group.md)
* [WorldPay Payments Standard](ui-extensions-worldpay-payments-standard.md)
* [DK: migración de datos de C5](ui-extensions-c5-data-migration.md)
* [DK: pagos y conciliaciones de pagos](ui-extensions-payments-reconciliation-formats-dk.md)
* [DK: formatos de archivo de impuestos](ui-extensions-tax-file-formats-dk.md)
* [La extensión Códigos postales de Reino Unido de GetAddress.io](LocalFunctionality/UnitedKingdom/ui-extensions-getaddressio.md)  
* [US/CA/UK/AU/NZ/ZA: enviar aviso de remesa](ui-extensions-send-remittance-advice.md)

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
