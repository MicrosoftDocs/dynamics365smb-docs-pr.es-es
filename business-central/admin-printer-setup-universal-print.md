---
title: Configurar impresoras de Impresión universal
description: Aprenda cómo puede usar Universal Print para proporcionar impresión en la nube en Business Central.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.date: 01/26/2023
ms.custom: bap-template
---

# Configurar impresoras de Impresión universal

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Impresión universal es un servicio basado en suscripción de Microsoft 365 que se ejecuta completamente en Microsoft Azure. Le brinda una administración centralizada de la impresora a través del portal de Impresión universal. [!INCLUDE[prod_short](includes/prod_short.md)] hace que las impresoras configuradas en Impresión universal estén disponibles para los usuarios cliente a través de la extensión **Integración de Impresión universal**.

![Configuración de impresión universal.](media/Universal-Print-arch.png)

La configuración completa requiere que trabaje en Microsoft Azure, usando [Azure Portal](https://portal.azure.com) y en [!INCLUDE[prod_short](includes/prod_short.md)]. La configuración se divide en dos tareas principales, como se describe en este artículo:

1. En Microsoft Azure, configure Universal Print y agregue las impresoras que desea usar en Business Central a un recurso compartido de impresión. Vaya a [esta sección](#set-up-universal-print-and-printers-in-microsoft-azure)
2. En [!INCLUDE[prod_short](includes/prod_short.md)], agregue las impresoras de los recursos compartidos de impresión en Universal Print. Vaya a [esta sección](#add-printers-in-business-central-online) para obtener información en línea o [aquí](#add-printers-in-business-central-on-premises) para obtener información local.

## Requisitos previos

- Impresoras compatibles

  [!INCLUDE[prod_short](includes/prod_short.md)] admite las mismas impresoras que Impresión universal, que pueden ser impresoras compatibles con Impresión universal o no compatibles. Las impresoras no compatibles no pueden comunicarse directamente con Impresión universal, por lo que requieren un software de conector adicional, que es proporcionado por Impresión universal. Es posible que algunas impresoras más antiguas no sean compatibles. 

- Impresión universal:

  - Una suscripción/licencia de Impresión universal para su organización.

    Más información acerca de la [Licencia de Impresión universal](/universal-print/fundamentals/universal-print-license).

  - Tiene los roles **Administrador de impresoras** (o Gestor de impresoras) **Administrador global** en Azure.

    Para administrar Impresión universal, su cuenta debe tener los roles **Administrador de impresoras** y **Administrador global** en Microsoft Entra ID. Estos roles solo son necesarios para administrar Impresión universal. No son necearios para personas que configuren las impresoras desde [!INCLUDE[prod_short](includes/prod_short.md)].

- [!INCLUDE[prod_short](includes/prod_short.md)] online y local:

  - Lanzamiento de versiones 1 de 2021 de [!INCLUDE[prod_short](includes/prod_short.md)] o posterior.
  - La extensión **Integración de Impresión universal** está instalada.

    Esta extensión se publica e instala de forma predeterminada como parte de [!INCLUDE[prod_short](includes/prod_short.md)] Online y local. Puede verificar si se está instalado en la página **Administración de extensiones**. Más información sobre [Instalar y desinstalar extensiones en Business Central](ui-extensions-install-uninstall.md).
- [!INCLUDE[prod_short](includes/prod_short.md)] solo local:
  - La autenticación de Microsoft Entra ID o NavUserPassword está configurada.
    > [!NOTE]
    >  La extensión Universal Print no admite la autenticación de servicio a servicio (S2S). Requiere un usuario que haya iniciado sesión para enviar trabajos de impresión al servicio Universal Print a través de Graph API.
  - Una aplicación para Business Central está registrada en su suscriptor de Microsoft Entra y [!INCLUDE[prod_short](includes/prod_short.md)].

    Como otros servicios de Azure que funcionan con [!INCLUDE[prod_short](includes/prod_short.md)], Impresión universal requiere un registro de aplicación para [!INCLUDE[prod_short](includes/prod_short.md)] en Microsoft Entra ID. El registro de la aplicación proporciona servicios de autenticación y autorización entre [!INCLUDE[prod_short](includes/prod_short.md)] y Impresión universal.

    Es posible que su implementación ya esté usando un registro de aplicación para otros servicios de Azure, como Power BI. Si es así, use también el registro de la aplicación existente para Impresión universal, en lugar de agregar uno nuevo. En este caso, lo único que tendrá que hacer es modificar el registro de la aplicación para incluir los permisos de impresión pertinentes para Microsoft Graph API: **PrinterShare.ReadBasic.All**, **PrintJob.Create** y **PrintJob.ReadBasic.** 

    Para registrar una aplicación y establecer los permisos adecuados, siga los pasos descritos en [Registrar una aplicación en Microsoft Entra ID](/dynamics365/business-central/dev-itpro/administration/register-app-azure#register-an-application-in-azure-active-directory).

## Configurar Impresión universal e impresoras en Microsoft Azure

Antes de que pueda empezar a administrar las impresoras de Impresión universal en Business Central, hay varias tareas para que Impresión universal funcione en Azure con las impresoras que desea usar.

Para obtener instrucciones detalladas sobre cómo realizar la configuración, consulte [Introducción: configurar Impresión universal](/universal-print/fundamentals/universal-print-getting-started) en la documentación de Impresión universal. Aquí se muestra un resumen de los pasos que tendrá que completar. La mayoría de estos pasos se realizan en Azure Portal.

1. Asigne licencias de Impresión universal para usted y otros usuarios.

    La forma de asignar la licencia depende de si se está integrando con Business Central Online o local.

    - Con [!INCLUDE[prod_short](includes/prod_short.md)] en línea, las licencias se asignan mediante el Centro de administración de Microsoft 365.

      Para obtener más información, consulte [Ayuda del Centro de administración de Microsoft: asigne licencias a los usuarios](/microsoft-365/admin/manage/assign-licenses-to-users).

    - Con [!INCLUDE[prod_short](includes/prod_short.md)] local, asigna licencias en su suscriptor mediante Azure Portal.

      Para obtener más información, consulte [Asigne o elimine licencias en Azure Portal](/azure/active-directory/fundamentals/license-users-groups).

2. Instale el conector de Impresión universal para registrar impresoras que no puedan comunicarse directamente con Impresión universal.

    La mayoría de impresoras del mercado no pueden comunicarse directamente con Impresión universal, así que deberá instalar el conector de Impresión universal. Para obtener más información, consulte [Instalar el conector de Impresión universal](/universal-print/fundamentals/universal-print-connector-installation).

3. Registre sus impresoras en Impresión universal.

    El registro de una impresora hace que Impresión universal tenga en cuenta la impresora.

    - Para las impresoras que pueden comunicarse directamente con Impresión universal, siga los pasos proporcionados por el fabricante de la impresora.

    - Para otras impresoras, registre las impresoras usando el conector de Impresión universal. 

      Más información en [Registro de impresora](/universal-print/fundamentals/universal-print-connector-printer-registration).

4. Cambie las propiedades de la impresora (opcional).

    Una vez registrada una impresora, puede ver y modificar las propiedades de la impresora, como las preferencias predeterminadas.

    Para obtener más información, consulte [Administración de la configuración de la impresora mediante el portal de impresión universal](/universal-print/portal/configure-printer-settings).

5. Compartir las impresoras con los usuarios.

    Cualquier impresora que desee usar en [!INCLUDE[prod_short](includes/prod_short.md)] tendrá que añadirse a un *recurso compartido de impresora* en Impresión universal. Cualquier usuario que necesite acceso a la impresora debe agregarse como miembro del recurso compartido de la impresora. Más información en [Compartir una impresora](/universal-print/portal/share-printers).

    > [!TIP]
    > Siempre puede agregar o eliminar usuarios más tarde. Más información en [Permisos de impresora](/universal-print/portal/share-printers#configure-user-permissions-for-a-printer-share).

6. Habilite la conversión de documentos.

    Impresión universal procesa el contenido para imprimir en formato XPS. Algunas impresoras heredadas del mercado no admiten la representación de contenido XPS; en muchos casos, solo en formato PDF. La impresión en estas impresoras producirá un error a menos que Impresión universal esté configurado para convertir documentos al formato compatible con la impresora.

    Obtenga más información en [Resumen de conversión de documentos](/universal-print/portal/document-conversion).

Ahora, está listo para agregar las impresoras a [!INCLUDE[prod_short](includes/prod_short.md)], configurar impresoras predeterminadas para informes e imprimir.  

## Agregar impresoras en Business Central Online

Una vez configuradas y compartidas las impresoras en Impresión universal, estará listo para agregarlas a [!INCLUDE[prod_short](includes/prod_short.md)] para su uso. Hay dos formas de agregar impresoras de Impresión universal. Puede agregar las impresoras todas a la vez o individualmente, una a una.

Agregar impresoras individualmente le permite configurar la misma impresora de Impresión universal en [!INCLUDE[prod_short](includes/prod_short.md)] más de una vez. A continuación, para cada impresora agregada, puede cambiar la configuración de impresión, como la bandeja de papel, el tamaño y la orientación. De esta manera, puede configurar impresoras para diferentes informes y documentos con requisitos de salida especiales.

> [!NOTE]
> ¿Está utilizando [!INCLUDE[prod_short](includes/prod_short.md)] localmente? Si es así, vaya a la [siguiente sección](#add-printers-in-business-central-on-premises), la configuración inicial es ligeramente diferente.  
<!-- To Do Adding printers individually lets you duplicate printers with custom , like different paper trays and paper size and orientation.  To add printers individually, you'll need to know printer's share name in Universal Print. -->

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Administración de impresoras** y, a continuación, elija el vínculo relacionado.
2. Seleccione **Impresión universal** y, a continuación, elija una de las siguientes opciones:

   - **Agregar todas las impresoras de Impresión universal** para agregar todas las impresoras que aún no se agregaron. Puede usar esta opción incluso si ya se han agregado impresoras.
   - **Agregar una impresora de Impresión universal** para agregar una impresora específica.  
3. Siga las instrucciones en pantalla.

    - Si eligió **Agregar todas las impresoras de Impresión universal**, entonces se inicia la configuración **Agregar impresoras de Impresión universal**. 

    - Si eligió **Agregar una impresora de Impresión universal**, entonces aparece la página **Configuración de Impresión universal**. Rellene el campo **Nombre**, seleccione **...** al lado del campo **Imprimir recurso compartido en Impresión universal** para seleccionar el recurso compartido de impresora que contiene la impresora de Impresión universal. Rellene los campos restantes según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

Una vez que se ha agregado una impresora, puede ver y cambiar su configuración desde la página **Administración de impresoras**. Simplemente seleccione la impresora y, a continuación, elija **Editar configuración de impresora**.

## Agregar impresoras en Business Central local

<!--With [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, unlike online, users aren't automatically authenticated with the registered app in Azure used for the Universal Print service. So, before any Business Central user (including admins) can add or even use Universal Print printers, they'll have to authenticate with the Azure app and grant access to the Universal Print service. The following procedure describes how to initiate this authentication flow. Each user typically only has to do this task once.-->

Antes de que un usuario pueda agregar o usar las impresoras de Universal Print Business Central, debe autorizar el acceso a los servicios de Azure utilizados por Universal Print y otorgarle permiso para datos y operaciones como:

- Iniciar sesión y leer el perfil de usuario
- Lectura de información básica del trabajo de impresión
- Crear trabajos de impresión

Por lo general, esto se hace la primera vez que se conectan a la aplicación registrada de Azure que se usa para Universal Print. En Business Central Online, este flujo de autorización se realiza sin problemas, sin interacción del usuario. Pero Business Central local funciona de manera diferente. Requiere que usted, o cualquier otro usuario que quiera usar las impresoras Universal Print, inicie el flujo de autenticación; por lo general, una sola vez. La forma más directa se describe en los pasos siguientes. Una forma menos directa es conectarse a otro servicio integrado que use la misma aplicación registrada de Azure, como Power BI o OneDrive. Normalmente, cada usuario solo tiene que realizar esta tarea una vez.

> [!NOTE]
> Si es administrador, le recomendamos que complete esta tarea antes que otros usuarios. Luego, informe a los usuarios que necesitarán usar impresoras Universal Print cómo hacerlo. Si la aplicación registrada de Azure para Universal Print requiere el consentimiento del administrador para los permisos de API, es más fácil si otorga el consentimiento en nombre de la organización. Puede otorgar el consentimiento del administrador desde Azure Portal o cuando ejecuta los pasos que se indican a continuación. 

<!-- To Do Adding printers individually lets you duplicate printers with custom , like different paper trays and paper size and orientation.  To add printers individually, you'll need to know printer's share name in Universal Print. -->
### Conéctese a Universal Print por primera vez

Complete estos pasos para conectarse al servicio Universal Print por primera vez.

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Administración de impresoras** y, a continuación, elija el vínculo relacionado.
2. Seleccione **Impresión universal** > **Agregar todas las impresoras de impresión universal** para iniciar la guía de configuración asistida (asistente) **Agregar impresoras de impresión universal**.
3. Siga las instrucciones en pantalla hasta llegar a la página **PERMISOS DEL SERVICIO MICROSOFT ENTRA**.

    <!--The MICROSOFT ENTRA SERVICE PERMISSIONS page appears. You'll be prompted to give consent to Azure Services. You'll be lead through the process of verifying your Microsoft Entra ID setup, checking your Universal Print license, and then adding the printers.-->

   ![Muestra la página PERMISOS DEL SERVICIO MICROSOFT ENTRA](media/azure-ad-services-permissions.png "Muestra la página PERMISOS DEL SERVICIO MICROSOFT ENTRA")

4. Seleccione el enlace **Autorizar servicios de Azure**.

   1. Si aparece la página **Permiso solicitado**, léala detenidamente y seleccione **Aceptar** para aceptar y continuar. Si se postula como administrador, puede seleccionar **Consentimiento en nombre de la organización** si desea otorgar consentimiento para todos los usuarios.

      ![Muestra la página de permisos de solicitud de Azure](media/azure-ad-permissions-requested.png "Página de solicitud de permisos de Azure").

   2. Si se le solicita, inicie sesión con su nombre de usuario y contraseña.

5. Cuando la autorización se complete correctamente, volverá a la página **Agregar impresoras de impresión universal**. Para completar la configuración, seleccione **Siguiente** >  **Terminar**.

Una vez que se ha agregado una impresora, puede ver y cambiar su configuración desde la página **Administración de impresoras**. Simplemente seleccione la impresora y, a continuación, elija **Editar configuración de impresora**.

Una vez que complete el inicio de sesión inicial, puede usar las impresoras Universal Print para imprimir informes y otros trabajos de impresión. Para más información, vaya a [Imprimir un informe](ui-work-report.md#PrintReport). Si desea agregar, quitar o cambiar cualquier impresora, simplemente regrese a la página **Administración de impresión** y seleccione **Impresión universal**.

## Problemas comunes y sus soluciones

En esta sección, aprenderá acerca de los problemas comunes que los usuarios pueden experimentar cuando intentan configurar o usar impresoras Universal Print.

### No tiene acceso a la impresora \<your-printer\>.

Si un usuario recibe este mensaje cuando intenta imprimir un documento en una impresora Universal Print, puede deberse a una de las siguientes condiciones:

- El usuario no tiene una licencia de Universal Print asignada a su cuenta de Microsoft 365 o Azure Active AD. 
- El usuario no está asignado al recurso compartido de impresora en Universal Print.
- (Local) El registro de la aplicación de Azure que se usa para Universal Print no funciona o ha cambiado recientemente desde la última vez que el usuario inició sesión.
- (Local) El usuario aún no ha iniciado sesión en la aplicación registrada de Azure para la aplicación Universal Printer y ha dado su consentimiento por primera vez.

## Se produjo un error al capturar las impresoras compartidas con usted.

Si un usuario recibe este mensaje cuando intenta agregar una impresora Universal Print desde la página **Administración de impresoras**, generalmente se debe a que aún no ha iniciado sesión en la aplicación registrada de Azure para Universal. Aplicación de impresora y consentida por primera vez. 
<!--
### Troubleshooting

#### You don't see the a printer in the 

The printer is not shared in Universal Print.

### You get an error when tryong to add all or a single printer

You have'nt been assigned a Uincersla Print license.

There was an error fetching printers shared to you. You don't have access to the data. Make sure your account has been assigned a Universal Print license and you have the required permissions.
or 
You don't seem to have access to Universal Print. Make sure you have a Universal Print subscription, and that your account has been assigned a Universal Print license.

## Could not upload the document to print job 50.

There is a technical problem withe the printer. Unsupported document-format: application/pdf. Supported formats: Attribute document-format-supported: SimpleIppValue-Type:MimeMediaType-Value:application/oxps




-->

## Pasos siguientes
[Configurar impresoras predeterminadas](ui-specify-printer-selection-reports.md).

## Consulte también .

[Información general de las impresoras](admin-printer-setup-overview.md)  
[Configurar impresoras de correo electrónico](admin-printer-setup-email.md)
[Imprimir un informe](ui-work-report.md#PrintReport)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Ejecutar procesos](ui-how-run-batch-jobs.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
