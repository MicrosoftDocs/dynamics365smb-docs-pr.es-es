---
title: Instalar extensiones para personalizar Finance and Operations, Business edition | Documentos de Microsoft
description: "Obtenga información sobre cómo agregar funcionalidades y personalizar Finance and Operations, Business edition mediante la instalación de extensiones."
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: app, add-in, manifest, customize
ms.date: 07/07/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: b34f276a764f0e828fbc1f015429df9852242a4c
ms.openlocfilehash: 1bcb4bd3cbc32397423430f07b3849be5047ec00
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="customizing-finance-and-operations-business-edition-using-extensions"></a>Personalización de Finance and Operations, Business edition con extensiones
Puede cambiar [!INCLUDE[d365fin](includes/d365fin_md.md)] instalando extensiones que agregan funciones, cambian el comportamiento o proporcionan acceso a nuevos servicios en línea, por ejemplo.
Cuando inicia [!INCLUDE[d365fin](includes/d365fin_md.md)] por primera vez, ya están instaladas algunas extensiones. Con el tiempo, tendrá disponibles más extensiones y puede elegir si desea usar la extensión o no.

Por ejemplo, Microsoft ofrece una extensión que proporciona integración con PayPal Payments Standard. Esta extensión se instala por omisión.
Pero si está disponible otra extensión que ofrece integración con otro servicio de pago, puede instalar la nueva extensión y seleccionar cuál de los dos servicios quiere usar.  

Puede administrar las extensiones en la ventana **Administración de extensiones**. Puede acceder a esta ventana desde la página Inicio. También puede elegir el icono **Buscar página o informe** ![Buscar página o informe](media/ui-search/search_small.png "Icono Buscar página o informe") en la esquina superior derecha, especificar **Tablas amortización** y elegir el vínculo relacionado.  

> [!NOTE]  
>   Si cree que debería tener acceso a una extensión pero no encuentra la funcionalidad, consulte la ventana **Administración de extensiones**; si la extensión no aparece, puede instalarla tal como se describe en la sección siguiente.  

## <a name="installing-an-extension"></a>Instalar una extensión
Puede obtener extensiones nuevas en mercado en [AppSource.microsoft.com](https://appsource.microsoft.com/en-us/marketplace/apps?product=dynamics-365%3Bdynamics-365-for-financials&page=1). Aquí, puede ver todos los extensiones disponibles para [!INCLUDE[d365fin](includes/d365fin_md.md)], y puede obtener aplicaciones, extensiones, y paquetes de contenido para otros productos de Microsoft. Configure los filtros relevantes, revise la información para cada extensión y consiga una para [!INCLUDE[d365fin](includes/d365fin_md.md)].  
> [!NOTE]  
>   Inicie sesión en [AppSource.microsoft.com](https://appsource.microsoft.com/) con la cuenta de correo electrónico que usa para [!INCLUDE[d365fin](includes/d365fin_md.md)]. Use la misma cuenta de correo para otros servicios y productos para disfrutar de una experiencia agilizada.  

También puede ir al mercado de aplicaciones desde [!INCLUDE[d365fin](includes/d365fin_md.md)]. En la ventana **Gestión de extensiones**, puede ver las extensiones que están instaladas actualmente y puede abrir la página del **Mercado de extensiones** que muestra todas las extensiones para [!INCLUDE[d365fin](includes/d365fin_md.md)] que están disponibles actualmente en AppSource. Si elige el vínculo *Más aplicaciones* se le redireccionará a [AppSource.microsoft.com](https://appsource.microsoft.com/en-us/marketplace/apps?product=dynamics-365%3Bdynamics-365-for-financials&page=1).  

Si selecciona una extensión, puede consultar las funciones de la extensión y acceder al sitio de ayuda de la extensión para obtener más información. Cuando elige una extensión debe aceptar las condiciones de uso. Si obtiene la extensión del sitio web de AppSource, se requerirá el inicio de sesión en [!INCLUDE[d365fin](includes/d365fin_md.md)] para completar la instalación.  

Al instalar una extensión, es posible que tenga que configurarla, por ejemplo, especificar una cuenta para usar con la extensión **Estándar de pagos de PayPal para [!INCLUDE[d365fin](includes/d365fin_md.md)]**.
Otras extensiones simplemente agregan campos a una página existente o agregan una página nueva, por ejemplo.   

Si desinstala una extensión y cambia de idea, puede volver a instalarla. Al desinstalar una extensión que ha estado usando, los datos se guardan para que se vuelve a instalar la extensión estén disponibles.  

Algunas de las extensiones las proporciona Microsoft y otras las proporcionan [otras empresas](ui-extensions-other.md). Se prueban todas las extensiones antes de que estén disponibles, pero le recomendamos que acceda a los vínculos que se proporcionan con cada extensión para obtener más información sobre la extensión antes de optar por instalarla.  

Microsoft proporciona las extensiones siguientes:  

* [Migración de datos de Dynamics GP](ui-extensions-dynamicsgp-data-migration.md)  
* [Fuentes de bancos de Envestnet Yodlee](ui-extensions-yodlee-bank-feeds.md)  
* [Microsoft Pay](ui-extensions-microsoft-pay-payments.md)
* [PayPal Payments Standard](ui-extensions-paypal-payments-standard.md)  
* [Migración de datos de QuickBooks](ui-extensions-quickbooks-data-migration.md)  
* [Previsión de ventas e inventario](ui-extensions-sales-forecast.md)  
* [Nóminas de Ceridian](ui-extensions-ceridian-payroll.md)  
* [Importación del archivo de nómina de QuickBooks](ui-extensions-quickbooks-payroll.md)  
* [Estándar de pagos de WorldPay](ui-extensions-worldpay-payments-standard.md)
* [Códigos postales de Reino Unido de GetAddress.io](ui-extensions-getaddressio.md)
* [Migración de datos de QuickBooks Online](ui-extensions-quickbooks-online-data-migration.md)
* [Portal para contadores](ui-extensions-accountant-portal.md)  
* [Analizador de imágenes](ui-extensions-image-analyzer.md)
* [Pagos y conciliaciones de pagos (DK)](ui-extensions-payments-reconciliation-formats-dk.md)
* [Migración de datos C5](ui-extensions-c5-data-migration.md)

> [!NOTE]  
>  Las nuevas extensiones no están disponibles en AppSource inmediatamente después anunciar una actualización. Puede estar atento a las extensiones en [AppSource.microsoft.com](https://appsource.microsoft.com/en-us/marketplace/apps?product=dynamics-365%3Bdynamics-365-for-financials&page=1).

## <a name="see-also"></a>Consulte también
[Configuración del servicio de fuentes de banco de Envestnet Yodlee](bank-how-setup-bank-statement-service.md)  
[Permitir el pago de clientes mediante PayPal](sales-how-enable-payment-service-extensions.md)  
[Migrar datos de empresa de otros sistemas financieros](upload-data.md)  
[Configurar la extensión Códigos postales de Reino Unido de GetAddress.io](LocalFunctionality/UnitedKingdom/uk-setup-postal-code-service.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] Extensiones de otros proveedores](ui-extensions-other.md)  
[[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]

