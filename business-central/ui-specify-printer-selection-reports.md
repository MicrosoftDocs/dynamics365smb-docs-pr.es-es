---
title: Configuración de impresoras
description: Obtenga información sobre cómo configurar impresoras para informes y documentos y las diferentes funciones de impresión disponibles en Business Central.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: online printing, email printing, cloud printing, Universal Print
ms.search.form: 2650, 2750, 2752, 2753, 2754, 8900,
ms.date: 09/22/2022
ms.author: jswymer
ms.openlocfilehash: 07cda9c796a08436dc48d623f64fcc1252305a14
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/30/2022
ms.locfileid: "9607748"
---
# <a name="set-up-printers"></a>Configuración de impresoras

La impresión de documentos e informes desde [!INCLUDE[prod_short](includes/prod_short.md)] es una tarea importante para los usuarios empresariales. Usted normalmente querrá enviar trabajos de impresión directamente a una de las impresoras de su organización&mdash;independientemente del cliente o la aplicación de [!INCLUDE[prod_short](includes/prod_short.md)] que use. Puesto que [!INCLUDE[prod_short](includes/prod_short.md)] Online es un servicio en la nube, no puede llegar directamente a las impresoras locales conectadas a los dispositivos de los usuarios, pero puede conectarlo a impresoras habilitadas para la nube.

Para satisfacer sus necesidades de impresión, [!INCLUDE[prod_short](includes/prod_short.md)] ofrece las siguientes características:

|Característica|Descripción|Cliente web| Aplicación móvil|Aplicación para Teams|
|-------|-----------|----------|-----------|--------------|
|Impresión universal|Impresión universal es una solución de gestión de impresoras disponible como servicio en la nube de Microsoft. Con esta característica, puede configurar sus impresoras en Impresión universal y, a continuación, registrarlas para su uso en [!INCLUDE[prod_short](includes/prod_short.md)]. Esta característica requiere una suscripción a Impresión universal y la extensión **Integración de Impresión universal** extensión|![trabaja en línea.](media/check.png)|![trabaja en línea.](media/check.png)|![trabaja en línea](media/check.png)|
|Impresión por correo electrónico|Esta característica le permite configurar impresoras habilitadas para correo electrónico. [!INCLUDE[prod_short](includes/prod_short.md)] envía los trabajos de impresión a una impresora usando la dirección de correo electrónico de la impresora. Esta característica requiere impresoras habilitadas para correo electrónico y la extensión **Enviar a impresora de correo electrónico**.|![trabaja en línea.](media/check.png)|![trabaja en línea](media/check.png)|![trabaja en línea](media/check.png)|
|Impresión en el navegador|Los trabajos de impresión son gestionados por la funcionalidad de impresión del navegador del usuario. Si no se instala y configura una impresora en la nube o si falla una impresora instalada, la impresión tendrá las opciones de impresión predeterminadas para el navegador. El campo **Impresora** en la página de solicitud de informe mostrará *(Manejado por el navegador)*.|![trabaja en línea](media/check.png)|||

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_short.md)] admite otras extensiones de impresora personalizadas que agregan aún más características de impresión. Por lo tanto, si instala extensiones de impresora personalizadas, su aplicación puede incluir características de impresión que no se describen en este artículo. 

## <a name="set-up-universal-print"></a>Configurar Impresión universal

Impresión universal es un servicio basado en suscripción de Microsoft 365 que se ejecuta completamente en Microsoft Azure. Le brinda una administración centralizada de la impresora a través del portal de Impresión universal. [!INCLUDE[prod_short](includes/prod_short.md)] hace que las impresoras configuradas en Impresión universal estén disponibles para los usuarios cliente a través de la extensión **Integración de Impresión universal**.

![Configuración de impresión universal.](media/Universal-Print-arch.png)

La configuración completa requiere que trabaje en Microsoft Azure, usando [Azure Portal](https://portal.azure.com) y en [!INCLUDE[prod_short](includes/prod_short.md)].

### <a name="supported-printers"></a>Impresoras compatibles

[!INCLUDE[prod_short](includes/prod_short.md)] admite las mismas impresoras que Impresión universal, que pueden ser impresoras compatibles con Impresión universal o no compatibles. Las impresoras no compatibles no pueden comunicarse directamente con Impresión universal, por lo que requieren un software de conector adicional, que es proporcionado por Impresión universal. Es posible que algunas impresoras más antiguas no sean compatibles. 

<!-- TODO If not installed, go to AppSource -->

### <a name="prerequisites"></a>Requisitos previos

**Para [!INCLUDE[prod_short](includes/prod_short.md)]**

- Lanzamiento de versiones 1 de 2021 de [!INCLUDE[prod_short](includes/prod_short.md)] o posterior.
- La extensión **Integración de Impresión universal** está instalada.

    Esta extensión se publica e instala de forma predeterminada como parte de [!INCLUDE[prod_short](includes/prod_short.md)] Online y local. Puede verificar si se está instalado en la página **Administración de extensiones**. Más información sobre [Instalar y desinstalar extensiones en Business Central](ui-extensions-install-uninstall.md).

- [!INCLUDE[prod_short](includes/prod_short.md)] local:
  - La autenticación de Azure Active Directory (AD) o NavUserPassword está configurada.
  - Una aplicación para Business Central está registrada en su suscriptor de Azure AD y [!INCLUDE[prod_short](includes/prod_short.md)].

      Como otros servicios de Azure que funcionan con [!INCLUDE[prod_short](includes/prod_short.md)], Impresión universal requiere un registro de aplicación para [!INCLUDE[prod_short](includes/prod_short.md)] en Azure AD. El registro de la aplicación proporciona servicios de autenticación y autorización entre [!INCLUDE[prod_short](includes/prod_short.md)] y Impresión universal.

      Es posible que su implementación ya esté usando un registro de aplicación para otros servicios de Azure, como Power BI. Si es así, use también el registro de la aplicación existente para Impresión universal, en lugar de agregar uno nuevo. En este caso, lo único que tendrá que hacer es modificar el registro de la aplicación para incluir los permisos de impresión pertinentes para la API de Microsoft Graph.

      Para registrar una aplicación y establecer los permisos adecuados, siga los pasos descritos en [Registrar una aplicación en Azure Active Directory](/dynamics365/business-central/dev-itpro/administration/register-app-azure#register-an-application-in-azure-active-directory).

**Para Impresión universal**

- Una suscripción/licencia de Impresión universal para su organización.

    Más información acerca de la [Licencia de Impresión universal](/universal-print/fundamentals/universal-print-license).

- Tiene los roles **Administración de impresoras** y **Administrador global** en Azure.

    Para administrar Impresión universal, su cuenta debe tener los roles **Administración de impresoras** y **Administrador global** en Azure AD. Estos roles solo son necesarios para administrar Impresión universal. Los usuarios no los necesitan para usar las impresoras de [!INCLUDE[prod_short](includes/prod_short.md)].

### <a name="set-up-universal-print-and-add-printers-in-microsoft-azure"></a>Configurar Impresión universal y agregar impresoras en Microsoft Azure

Antes de que pueda empezar a administrar las impresoras de Impresión universal en Business Central, hay varias tareas que deberá realizar para que Impresión universal funcione en Azure con las impresoras que desea usar.

Para obtener instrucciones detalladas sobre cómo realizar la configuración, consulte [Introducción: configurar Impresión universal](/universal-print/fundamentals/universal-print-getting-started) en la documentación de Impresión universal. Aquí se muestra un resumen de los pasos que tendrá que completar. La mayoría de estos pasos se realizan en Azure Portal.

1. Asigne licencias de Impresión universal para usted y otros usuarios.

    La forma de asignar la licencia depende de si se está integrando con Business Central Online o local.

    - Con [!INCLUDE[prod_short](includes/prod_short.md)] en línea, las licencias se asignan mediante el Centro de administración de Microsoft 365.

      Para obtener más información, consulte [Ayuda del Centro de administración de Microsoft: asigne licencias a los usuarios](/microsoft-365/admin/manage/assign-licenses-to-users).

    - Con [!INCLUDE[prod_short](includes/prod_short.md)] local, asigna licencias en su suscriptor de Azure mediante Azure Portal.

      Para obtener más información, consulte [Azure Directory: asigne o elimine licencias en el portal de Azure Active Directory](/azure/active-directory/fundamentals/license-users-groups).

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

5. Comparta las impresoras.

    Cualquier impresora que desee usar en [!INCLUDE[prod_short](includes/prod_short.md)] tendrá que compartirse en Impresión universal.

    <!--Learn more at [Share a Printer](/universal-print/fundamentals/universal-print-printer-permissions#share-a-printer). -->

    Más información en [Compartir una impresora](/universal-print/portal/share-printers).

6. Conceda permisos a los usuarios para las impresoras compartidas.

    <!--Learn more at [Printer Permissions](/universal-print/fundamentals/universal-print-printer-permissions#printer-permissions).-->

    Más información en [Permisos de impresora](/universal-print/portal/share-printers#configure-user-permissions-for-a-printer-share).


7. Habilite la conversión de documentos.

    Impresión universal procesa el contenido para imprimir en formato XPS. Algunas impresoras heredadas del mercado no admiten la representación de contenido XPS; en muchos casos, solo en formato PDF. La impresión en estas impresoras producirá un error a menos que Impresión universal esté configurado para convertir documentos al formato compatible con la impresora.

    Obtenga más información en [Resumen de conversión de documentos](/universal-print/portal/document-conversion).

Ahora, está listo para agregar las impresoras a [!INCLUDE[prod_short](includes/prod_short.md)], configurar impresoras predeterminadas para informes e imprimir.  

### <a name="add-universal-print-printers-to-business-central"></a>Agregar impresoras de impresión universal a Business Central

Una vez configuradas y compartidas las impresoras en Impresión universal, estará listo para agregarlas en Business Central. Hay dos formas de agregar impresoras de Impresión universal. Puede agregar las impresoras todas a la vez o individualmente, una a una.

Al agregar impresoras individualmente le permite configurar la misma impresora de Impresión universal en Business Central más de una vez. A continuación, para cada impresora agregada, puede cambiar la configuración de impresión, como la bandeja de papel, el tamaño y la orientación. De esta manera, puede configurar impresoras para diferentes informes y documentos con requisitos de salida especiales.
  
<!-- To Do Adding printers individually lets you duplicate printers with custom , like different paper trays and paper size and orientation.  To add printers individually, you'll need to know printer's share name in Universal Print. -->

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Administración de impresoras** y, a continuación, elija el vínculo relacionado.
2. Seleccione **Impresión universal** y, a continuación, elija una de las siguientes opciones:

    - **Agregar todas las impresoras de Impresión universal** para agregar todas las impresoras que aún no se agregaron. Puede usar esta opción incluso si ya se han agregado impresoras. 

    - **Agregar una impresora de Impresión universal** para agregar una impresora específica.  
3. Siga las instrucciones en pantalla.

    - Si eligió **Agregar todas las impresoras de Impresión universal**, entonces se inicia la configuración **Agregar impresoras de Impresión universal**. <!--This setup leads you through the process of verifying your Azure AD setup (for on-premises), checking your Universal Print license, and then finally adding the printers.-->

    - Si eligió **Agregar una impresora de Impresión universal**, entonces aparece la página **Configuración de Impresión universal**. Rellene el campo **Nombre**, seleccione **...** al lado del campo **Imprimir recurso compartido en Impresión universal** para seleccionar la impresora de Impresión universal. Rellene los campos restantes según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].
  
    Estas acciones verifican su configuración de Azure AD (para instalaciones locales), comprueban que tiene la licencia de Impresión universal y, finalmente, agregan las impresoras.

    > [!NOTE]
    > Para las instalaciones locales, si es la primera vez que se conecta a Impresión universal, aparece la página PERMISOS DE SERVICIOS DE AZURE ACTIVE DIRECTORY y se le pedirá que dé su consentimiento a Azure Services. Solo tiene que dar su consentimiento una vez.

Una vez que se ha agregado una impresora, puede ver y cambiar su configuración desde la página **Administración de impresoras**. Simplemente seleccione la impresora y, a continuación, elija **Editar configuración de impresora**. 

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

## You don't have access to the printer

- You have not been assigned an UP license
- You have not been given access to the printer in UP.
- (On-premises) The app registration has been broken.
-->
## <a name="set-up-email-print"></a>Configurar impresión por correo electrónico

### <a name="prerequisites"></a>Requisitos previos

- Lanzamiento de versiones 1 de 2020 de [!INCLUDE[prod_short](includes/prod_short.md)] o posterior
- La extensión **Enviar a impresora de correo electrónico** está instalada

    Esta extensión se instala por omisión. Para obtener información sobre la instalación de extensiones, consulte<!--see what?--> 
- La funcionalidad de correo electrónico está configurada.

   Obtenga más información en [Configurar correo electrónico](admin-how-setup-email.md).

### <a name="add-an-email-printer"></a>Agregar una impresora de correo electrónico

La página **Administración de impresoras** le muestra las impresoras que están configuradas actualmente. La página también le da acceso a la página **Configuración** de cada impresora para editar una configuración existente o configurar una nueva impresora.

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Administración de impresoras** y, a continuación, elija el vínculo relacionado.
2. Seleccione **Imprimir correo electrónico** y, a continuación, elija **Agregar una impresora de correo electrónico**.
3. En la página **Configuración de impresora de correo electrónico**, rellene los campos necesarios. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]
    > Debe seleccionar manualmente el tamaño de papel adecuado para una impresora, ya que no se puede almacenar la impresora local o la configuración del usuario.
    >
    > Tenga en cuenta que la extensión de la impresora de correo electrónico está configurada con el tamaño de papel **A4** por defecto, que no es adecuado en Norteamérica, por ejemplo.

### <a name="privacy-notice"></a>Aviso de privacidad

Si usa la extensión de impresora de correo electrónico, todos o algunos trabajos de impresión se enviarán a la dirección de correo electrónico configurada para la impresora. Recomendamos encarecidamente que se vincule una identificación de correo electrónico única a un dispositivo de impresora utilizando solo los servicios oficiales proporcionados por el fabricante del hardware, como HP ePrint, KonicaMinolta EveryonePrint o Epson Email Print.

Tome todas las precauciones de privacidad necesarias, incluida la garantía de que la solución de impresión de correo electrónico haya configurado correctamente los permisos, la configuración de privacidad y las políticas de retención. Es su responsabilidad proporcionar una dirección de correo electrónico correcta, verificada y operativa. Más información en [Declaración de privacidad de Microsoft](https://privacy.microsoft.com/privacystatement).

## <a name="set-up-default-printers"></a><a name="default"></a>Configurar impresoras predeterminadas

Existen un par de formas de configurar las impresoras que se usarán de forma predeterminada para los trabajos de impresión. Una impresora predeterminada es útil si trabaja con diferentes informes que requieren impresoras diferentes debido a su ubicación en la empresa o sus capacidades de salida.

### <a name="set-a-printer-as-a-default-printer-for-all-print-jobs"></a>Configurar una impresora como impresora predeterminada para todos los trabajos de impresión

Mediante la página **Administración de impresoras** puede configurar una impresora como impresora predeterminada para todos los trabajos de impresión. Puede especificar la impresora como predeterminada solo para usted o para todos los usuarios.

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Administración de impresoras** y, a continuación, elija el vínculo relacionado.

    > [!TIP]
    > También puede abrir la página **Administración de impresoras** desde la página **Selecciones de impresora** eligiendo **Administración de impresoras**.  
2. En la página **Administración de impresoras**, seleccione una impresora de la lista, elija **Administrar** y, a continuación, **Establecer como mi impresora predeterminada** o **Establecer como impresora predeterminada para todos los usuarios**.

> [!NOTE]
> La configuración de una impresora predeterminada desde el **Administración de impresoras** agregará una entrada en las **Selecciones de impresora**.

### <a name="set-a-default-printer-for-specific-reports"></a>Establecer una impresora predeterminada para informes específicos

La página **Selecciones de impresora** le permite especificar la impresora que usará un informe de forma predeterminada. Las impresoras predeterminadas se configuran por cuenta de usuario. Puede configurar una impresora predeterminada solo para usted, para otro usuario o para todos los usuarios.

> [!IMPORTANT]
> Para [!INCLUDE[prod_short](includes/prod_short.md)] local, la página **Selecciones de impresora** solo se puede usar para impresoras en la nube definidas por extensiones de impresora, como las impresoras Email Print y Impresión universal. No se puede utilizar para impresoras locales.

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Selecciones de impresora** y, a continuación, elija el vínculo relacionado. Alternativamente, desde la página **Administración de impresoras**, seleccione una impresora y luego elija la acción **Selecciones de impresoras**.
2. Elija la acción **Nuevo** para agregar una selección de impresora para un informe específico.
3. Rellene los campos según sea necesario.

El informe especificado estará ahora configurado para imprimirse en la impresora seleccionada de manera predeterminada.

> [!NOTE]
> Cuando imprime el informe en cuestión, puede seleccionar uno diferente usando el campo **Imprimir** en la página de solicitud de informe.

> [!NOTE]
> Si no configura un informe para una impresora específica en la página **Selecciones de impresora**, se imprimirá en la impresora predeterminada de la empresa, tal como se define en la página **Administración de impresoras**.

Usted o el administrador también pueden usar la página **Selecciones de impresora** para definir otras variaciones de impresión para usuarios e informes. La tabla siguiente describe la combinación de valores para especificar una configuración de impresión diferente para un informe.

|Para                                                 |Establecer los valores siguientes                                             |
|---------------------------------------------------|---------------------------------------------------------------------|
|Imprimir un informe en una impresora específica para todos los usuarios |Especifique los valores de los campos **Id. informe** y **Nombre impresora** y deje en blanco el campo **Id. usuario**.|
|Imprimir todos los informes en una impresora específica para un usuario específico|Especifique los valores de los campos **Id. usuario** y **Nombre impresora** y deje en blanco el campo **Id. informe**. Esta entrada hace lo mismo que la acción **Establecer como mi impresora predeterminada** en la página **Administración de impresión**.|
|Establecer la impresora predeterminada para todos los informes de todos los usuarios|Especifique un valor en el campo **Nombre impresora** y deje en blanco los campos **Id. usuario** e **Id. informe**. Esta entrada hace lo mismo que la acción **Establecer como impresora predeterminada para todos los usuarios** en la página **Administración de impresión**.|
|Imprimir un informe específico en la impresora predeterminada del usuario|Especifique un valor en el campo **Id. informe** y deje en blanco los campos **Id. usuario** y **Nombre impresora**.|
|Imprimir un informe específico en una impresora concreta para un usuario específico|Especifique los valores de los tres campos.|

> [!NOTE]
> Las selecciones de impresora más específicas tienen preferencia sobre las selecciones de impresora más generales. Por ejemplo, una selección de impresora que tenga valores en **ID de usuario**, **ID de informe** y **Nombre de impresora** tiene prioridad sobre una selección de impresora que tenga entradas en blanco en los campos **ID de usuario** o **ID de informe**.

### <a name="choosing-the-printer-when-running-a-report"></a>Elección de la impresora al generar un informe

En lugar de utilizar la impresora predeterminada al ejecutar un informe, puede anular esta configuración desde la página de solicitud. Simplemente elija la impresora que desea utilizar para esta generación del informe en el menú desplegable **Impresora**.

### <a name="sizing-print-jobs"></a>Cambio de tamaño de los trabajos de impresión

La impresión en la nube se ha diseñado para documentos de un tamaño razonable. La mayoría de los servicios en la nube, incluidos PrintNode y HP ePrint, tienen un límite de 10 MB por trabajo. Si necesita imprimir informes más grandes, es posible que deba dividirlos en varias copias impresas.

## <a name="see-related-microsoft-training"></a>Consulte la [formación de Microsoft](/training/modules/change-documents-dynamics-365-business-central/) relacionada.

## <a name="see-also"></a>Consulte también .

[Imprimir un informe](ui-work-report.md#PrintReport)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Ejecutar procesos](ui-how-run-batch-jobs.md)  
[Enviar documentos por correo electrónico](ui-how-send-documents-email.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
