---
title: Instalar y desinstalar aplicaciones
description: Aprenda a instalar y desinstalar extensiones y aplicaciones en Business Central.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: solsen
ms.topic: conceptual
ms.date: 06/26/2024
ms.custom: bap-template
ms.search.keywords: 'app, add-in, manifest, customize, install, uninstall'
ms.search.form: '2500, 2514, 20350'
ms.service: dynamics-365-business-central
---

# Instalar y desinstalar extensiones (Aplicaciones) en Business Central

Puede cambiar [!INCLUDE[prod_short](includes/prod_short.md)] instalando aplicaciones que, por ejemplo, agregan funciones, cambian el comportamiento o proporcionan acceso a nuevos servicios en línea. Para obtener más información, consulte [Personalizar Business Central con extensiones](ui-extensions.md).

> [!NOTE]
> Para instalar o desinstalar aplicaciones desde AppSource o añadir aplicaciones por suscriptor, debe tener los permisos adecuados. Debe ser miembro del grupo de usuarios D365 Extensión MGT o debe tener el conjunto de permisos de ADMIN. EXTENS. - Conjunto de permisos ADMIN. Si usted es administrador, puede asignar grupos de usuarios y permisos a otros usuarios de su empresa. Para obtener más información sobre grupos de usuarios y permisos, vaya a [Asignar permisos a usuarios y grupos](ui-define-granular-permissions.md).
>
> Para utilizar la funcionalidad que proporciona una extensión, como abrir páginas, ejecutar informes, seleccionar acciones, etc., se le deben asignar los conjuntos de permisos que se instalan como parte de la extensión.

Para usar una extensión, debe tener asignados los conjuntos de permisos que vienen con ella.

## <a name="install"></a>Instalar una extensión

Puede administrar las aplicaciones y extensiones en la página **Administración de extensiones**. Puede acceder a esta página desde Inicio. Como alternativa, elija el icono **Buscar por página o informe** ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") en la esquina superior derecha, ingrese **Extensión** y luego elija el enlace relacionado.  

Puede obtener nuevas aplicaciones disponibles en el mercado en [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646). El mercado ofrece todas las aplicaciones disponibles para [!INCLUDE[prod_short](includes/prod_short.md)], además de aplicaciones y paquetes de contenido para otros productos de Microsoft. Configure los filtros relevantes, revise la información para cada extensión y consiga una para [!INCLUDE[prod_short](includes/prod_short.md)].  

> [!NOTE]  
> Inicie sesión en [AppSource.microsoft.com](https://appsource.microsoft.com/) con la cuenta de correo electrónico que usa para [!INCLUDE[prod_short](includes/prod_short.md)]. Use la misma cuenta de correo para otros servicios y productos para disfrutar de una experiencia agilizada.  

También puede obtener AppSource desde [!INCLUDE[prod_short](includes/prod_short.md)]. En la página **Administración de extensiones**, puede ver las aplicaciones que están instaladas actualmente y puede abrir la página **Aplicaciones de Microsoft AppSource** que muestra todas las aplicaciones de [!INCLUDE[prod_short](includes/prod_short.md)] que están disponibles actualmente en AppSource. Si elige la acción **Ver AppSource**, se le redireccionará a [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646). Para obtener más información, consulte [Administrar aplicaciones de AppSource](admin-manage-appsource-apps.md).  

Elija una aplicación para obtener información sobre lo que hace y puede acceder a la Ayuda de la aplicación para obtener más información. Cuando elige una aplicación debe aceptar sus condiciones de uso. Si obtiene la aplicación del sitio web de AppSource, se requerirá el inicio de sesión en [!INCLUDE[prod_short](includes/prod_short.md)] para completar la instalación.  

Después de instalar una aplicación, es posible que deba configurarla. Algunas aplicaciones requieren que proporcione cierta información antes de poder usarlas. Por ejemplo, después de instalar la aplicación **Paypal Payments Standard**, debe especificar el correo electrónico o el ID de la cuenta del comerciante para su cuenta de PayPal. Para configurar una aplicación o averiguar qué información necesitará, en la página **Extensiones instaladas**, elija la acción **Configurar**.  

Otras aplicaciones simplemente agregan campos a una página existente o agregan una página nueva, por ejemplo.

Si desinstala una aplicación y cambia de idea, puede volver a instalarla. Cuando desinstala una aplicación que ha estado usando, sus datos no se eliminan. Los datos están disponibles si vuelve a instalar la aplicación.

Algunas de las aplicaciones las proporciona Microsoft y otras las proporcionan [otras empresas](ui-extensions-other.md). Le recomendamos que obtenga más información sobre la aplicación antes de elegir instalarla.

Microsoft proporciona las aplicaciones siguientes:

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
* [La extensión de códigos postales de Reino Unido de GetAddress.io](LocalFunctionality/UnitedKingdom/ui-extensions-getaddressio.md)  
* [US/CA/UK/AU/NZ/ZA: Enviar aviso de remesa](ui-extensions-send-remittance-advice.md)

## Configurar una aplicación

Después de instalar una aplicación, es posible que deba configurarla. Por ejemplo, para la aplicación**PayPal Payments Standard para [!INCLUDE[prod_short](includes/prod_short.md)]** debe especificar la cuenta de PayPal a utilizar. Si ese es el caso, cuando se complete la instalación [!INCLUDE[prod_short](includes/prod_short.md)] le preguntará si desea configurar la aplicación de inmediato. Las configuraciones pueden ser necesarias para que la aplicación funcione u opcionales.

Si elige configurar su aplicación de inmediato y tiene una configuración requerida, [!INCLUDE[prod_short](includes/prod_short.md)] abrirá la configuración requerida. La configuración puede ser una página en la que ingresa información o una guía de configuración asistida que lo ayuda a través de los pasos. Si no completa la configuración de una sola vez, puede usar la página **Configuraciones para _nombre de la aplicación_**, que enumera todas las configuraciones para la aplicación. Configuraciones requeridas indicadas por **letras en negrita**.

## Cargar una extensión por inquilino (PTE)

Cargue una PTE mediante la página **Administración de extensiones**. En la página **Administración de extensiones**, vaya a **Administrar** y elija **Cargar extensión**. En la página **Carga e implementación de una extensión**, especifique el archivo .app para cargar. Para continuar, elija el botón **Aceptar** y luego el botón **Implementar**, lo que iniciará el proceso de implementación del PTE.

Si el PTE contiene cambios de esquema de ruptura, es posible *obligar* una carga del mismo. Para hacer eso, en **Modo de sincronización de esquema**, elija la opción **Forzar**. Recibirá un cuadro de diálogo de confirmación para aceptar antes de continuar.  

## Desinstalar una aplicación

Desinstale una aplicación usando la página **Administración de extensiones**. Para desinstalar una aplicación, selecciónela en la página, luego seleccione la acción **Desinstalar**. Si desinstala una aplicación y cambia de idea, puede volver a instalarla.

De forma predeterminada, cuando desinstala una aplicación que ha estado usando, sus datos no se eliminan. Si está seguro de que no volverá a instalar la aplicación, puede eliminar los datos cuando la desinstale. Para eliminar datos cuando desinstala una aplicación, active la opción **Eliminar datos de extensión**. Aparecerá un cuadro de diálogo de confirmación y debe elegir **Sí** para activarlo. Después de activar el interruptor **Eliminar datos de extensión**, puede desinstalar la aplicación y se le pedirá que vuelva a confirmar que desea desinstalar la aplicación y eliminar los datos.

> [!IMPORTANT]  
> * Puede haber aplicaciones que requieran o dependan de la aplicación que quiera desinstalar. Estas aplicaciones se conocen como *dependientes*. No puede desinstalar una aplicación a menos que también desinstale sus dependientes. Cuando desinstala una aplicación que tiene dependientes, un cuadro de diálogo enumera los dependientes. Para continuar, deberá seleccionar **Sí** para desinstalar la aplicación y sus dependientes.
> * Si activa el control de alternancia **Eliminar datos de extensión**, la desinstalación de la aplicación eliminará todos los datos de la aplicación *más* los datos para todas las aplicaciones dependientes. La acción no se puede deshacer.
> * Algunas aplicaciones son obligatorias y no puede eliminarlas en la página **Administración de extensiones**.  

Si desea conservar los datos de una aplicación desinstalada, puede eliminarlos más tarde. La página **Eliminar datos de extensión huérfana** enumera las aplicaciones para las que todavía tienes datos. Para eliminar los datos, elija la aplicación y, a continuación, seleccione **Eliminar datos**. 

## Consulte también

[Personalizar Business Central](ui-customizing-overview.md)  
[Extensiones de Business Central de otros proveedores](ui-extensions-other.md)  
[Administrar aplicaciones de AppSource](admin-manage-appsource-apps.md)  
[Configurar el servicio Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md)  
[Permitir el pago de clientes mediante PayPal](sales-how-enable-payment-service-extensions.md)  
[Migrar datos de empresa de otros sistemas financieros](across-import-data-configuration-packages.md)  
[Configurar la extensión Códigos postales de Reino Unido de GetAddress.io](LocalFunctionality/UnitedKingdom/uk-setup-postal-code-service.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] Extensiones de otros proveedores](ui-extensions-other.md)  
[Preparación para hacer negocios](ui-get-ready-business.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
