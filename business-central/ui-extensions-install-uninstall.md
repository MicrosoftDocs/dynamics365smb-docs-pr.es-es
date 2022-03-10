---
title: Instalar y desinstalar extensiones en Business Central | Documentos de Microsoft
description: Aprenda a instalar y desinstalar extensiones en Business Central.
documentationcenter: ''
author: SusanneWindfeldPedersen
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: app, add-in, manifest, customize, install, uninstall
ms.date: 06/03/2021
ms.author: solsen
ms.openlocfilehash: 7868e0dc10c3ec0f81f39b714b8d517fcf3c5f06
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2022
ms.locfileid: "8140402"
---
# <a name="installing-and-uninstalling-extensions-in-business-central"></a>Instalar y desinstalar extensiones en Business Central

Puede cambiar [!INCLUDE[prod_short](includes/prod_short.md)] instalando extensiones que, por ejemplo, agregan funciones, cambian el comportamiento o proporcionan acceso a nuevos servicios en línea. Para obtener más información, consulte [Personalizar Business Central con extensiones](ui-extensions.md).

> [!NOTE]
> Para instalar o desinstalar extensiones desde AppSource o añadir extensiones por suscriptor, debe tener los permisos adecuados. Debe ser miembro de ADMIN. EXTENS. - Grupo de usuarios ADMIN o debe tener ADMIN. EXTENS. - Conjunto de permisos ADMIN. Si es administrador, puede asignar grupos de usuarios y permisos a otros usuarios de su empresa.
>
> Para utilizar la funcionalidad que proporciona una extensión, como abrir páginas, ejecutar informes, seleccionar acciones, etc., se le deben asignar los conjuntos de permisos que se instalan como parte de la extensión.

> [!NOTE]  
> El conjunto de permisos **ADMIN. EXTENS. - ADMIN** se introdujo en el primer lanzamiento de versiones de Business Central 2021 para sustituir al conjunto de permisos **ADMIN. EXTENS. D365** de versiones anteriores.

## <a name="installing-an-extension"></a>Instalar una extensión

Puede administrar las extensiones en la página **Administración de extensiones**. Puede acceder a esta página desde Inicio. Como alternativa, elija el icono **Buscar por página o informe** ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") en la esquina superior derecha, ingrese **Extensión** y luego elija el enlace relacionado.  

Puede obtener nuevas extensiones disponibles en el mercado en [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646). Aquí puede ver todas las extensiones disponibles para [!INCLUDE[prod_short](includes/prod_short.md)] y puede obtener aplicaciones, extensiones y packs de contenido para otros productos de Microsoft. Configure los filtros relevantes, revise la información para cada extensión y consiga una para [!INCLUDE[prod_short](includes/prod_short.md)].  

> [!NOTE]  
> Inicie sesión en [AppSource.microsoft.com](https://appsource.microsoft.com/) con la cuenta de correo electrónico que usa para [!INCLUDE[prod_short](includes/prod_short.md)]. Use la misma cuenta de correo para otros servicios y productos para disfrutar de una experiencia agilizada.  

También puede ir al mercado de aplicaciones desde [!INCLUDE[prod_short](includes/prod_short.md)]. En la página **Gestión de extensiones**, puede ver las extensiones que están instaladas actualmente y puede abrir la página del **Mercado de extensiones** que muestra todas las extensiones para [!INCLUDE[prod_short](includes/prod_short.md)] que están disponibles actualmente en AppSource. Si elige el vínculo *Más aplicaciones* se le redireccionará a [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646).  

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


## <a name="uploading-a-per-tenant-extension-pte"></a>Cargar una extensión por inquilino (PTE)

Cargue una PTE mediante la página **Administración de extensiones**. En la página **Administración de extensiones**, vaya a **Administrar** y elija **Cargar extensión**. En la página **Carga e implementación de una extensión**, especifique el archivo .app para cargar. Para continuar, elija el botón **Aceptar** y luego el botón **Implementar**, lo que iniciará el proceso de implementación del PTE.

Si el PTE contiene cambios de esquema de ruptura, es posible *obligar* una carga del mismo. Para hacer eso, en el **Modo de sincronización de esquema**, elija la opción **Forzar**. Recibirá un cuadro de diálogo de confirmación para aceptar antes de continuar. 

## <a name="uninstalling-an-extension"></a>Desinstalar una extensión

Desinstale una extensión usando la página **Administración de extensiones**. Si desinstala una extensión y cambia de idea, puede volver a instalarla. Al desinstalar una extensión que ha estado usando, los datos se guardan por defecto para que se vuelve a instalar la extensión estén disponibles. En su lugar, puede optar por eliminar los datos con la extensión. Esto está controlado por la casilla **Eliminar datos de extensión**. Por defecto, esta casilla de verificación está *deshabilitada*.

> [!IMPORTANT]  
> Si habilita la casilla **Eliminar datos de extensión**, obtendrá un cuadro de diálogo de confirmación y debe elegir **Aceptar**. Con la casilla **Eliminar datos de extensión** habilitada, ahora puede desinstalar la extensión y se le pedirá que vuelva a confirmar que desea desinstalar la extensión y eliminar los datos. La acción no se puede deshacer.
Se requieren algunas extensiones. No puede desinstalarlas de la página **Administración de extensiones**. Si lo intenta, aparece un mensaje de error.  

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