---
title: Configurar impresoras por correo electrónico
description: Descripción de instrucciones
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 01/26/2023
ms.custom: bap-template
---
# <a name="set-up-email-printers"></a>Configurar impresoras por correo electrónico

Este artículo explica cómo configurar impresoras habilitadas para correo electrónico en [!INCLUDE[prod_short](includes/prod_short.md)]. Con estas impresoras, [!INCLUDE[prod_short](includes/prod_short.md)] envía los trabajos de impresión a una impresora usando la dirección de correo electrónico de la impresora.

> [!TIP]
> Para conocer otras posibilidades de impresoras, vaya a [Descripción general de la administración de impresoras](admin-printer-setup-overview.md). 

## <a name="prerequisites"></a>Requisitos previos

- Lanzamiento de versiones 1 de 2020 de [!INCLUDE[prod_short](includes/prod_short.md)] o posterior
- La extensión **Enviar a impresora de correo electrónico** está instalada

    Esta extensión se instala por omisión. Obtenga más información sobre como instalar extensiones en [Instalar y desinstalar extensiones en Business Central](ui-extensions-install-uninstall.md).
- La funcionalidad de correo electrónico está configurada.

   Obtenga más información en [Configurar correo electrónico](admin-how-setup-email.md).

## <a name="add-an-email-printer"></a>Agregar una impresora de correo electrónico

La página **Administración de impresoras** le muestra las impresoras que están configuradas actualmente. La página también le da acceso a la página **Configuración** de cada impresora para editar una configuración existente o configurar una nueva impresora.

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Administración de impresoras** y, a continuación, elija el vínculo relacionado.
2. Seleccione **Imprimir correo electrónico** y, a continuación, elija **Agregar una impresora de correo electrónico**.
3. En la página **Configuración de impresora de correo electrónico**, rellene los campos necesarios. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]
    > Debe seleccionar manualmente el tamaño de papel adecuado para una impresora, ya que no se puede almacenar la impresora local o la configuración del usuario.
    >
    > Tenga en cuenta que la extensión de la impresora de correo electrónico está configurada con el tamaño de papel **A4** por defecto, que no es adecuado en Norteamérica, por ejemplo.

## <a name="privacy-notice"></a>Aviso de privacidad

Si usa la extensión de impresora de correo electrónico, todos o algunos trabajos de impresión se enviarán a la dirección de correo electrónico configurada para la impresora. Recomendamos encarecidamente que se vincule una identificación de correo electrónico única a un dispositivo de impresora utilizando solo los servicios oficiales proporcionados por el fabricante del hardware, como HP ePrint, KonicaMinolta EveryonePrint o Epson Email Print.

Tome todas las precauciones de privacidad necesarias, incluida la garantía de que la solución de impresión de correo electrónico haya configurado correctamente los permisos, la configuración de privacidad y las políticas de retención. Es su responsabilidad proporcionar una dirección de correo electrónico correcta, verificada y operativa. Más información en [Declaración de privacidad de Microsoft](https://privacy.microsoft.com/privacystatement).

## <a name="next-steps"></a>Pasos siguientes

[Configurar impresoras predeterminadas](ui-specify-printer-selection-reports.md)

## <a name="see-also"></a>Consulte también .

[Información general de administración de impresoras](admin-printer-setup-overview.md)  
[Configurar impresoras de impresión universal](admin-printer-setup-universal-print.md)
[Imprimir un informe](ui-work-report.md#PrintReport)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Ejecutar procesos](ui-how-run-batch-jobs.md)  
