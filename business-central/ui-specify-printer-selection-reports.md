---
title: Configuración informes para imprimir en impresoras específicas | Documentos de Microsoft
description: Obtenga información sobre cómo especificar una impresora para un informe y usar la página Selección impresoras.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: online printing
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 5bc01e711be7d05205362536f4b44a5dbfc4aa2c
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2020
ms.locfileid: "3915998"
---
# <a name="set-up-printers"></a>Configuración de impresoras
Como [!INCLUDE[prodshort](includes/prodshort.md)] es un servicio en la nube, no puede llegar a las impresoras locales conectadas a las máquinas de los usuarios. Sin embargo, puede conectarse a impresoras habilitadas para la nube. En la versión genérica de [!INCLUDE[prodshort](includes/prodshort.md)], una impresora en la nube llamada **Impresora de correo electrónico** se instala como extensión y está lista para usar después de la configuración inicial.

Si no se instala y configura una impresora en la nube o si falla una impresora instalada, la impresión tendrá las opciones de impresión predeterminadas para el navegador. Esto se indica mediante este valor en el campo **Impresora** en la página de solicitud de informe: *(ninguna, controlada por el navegador)*.

En la página **Administración de impresoras**, puede ver las impresoras que están configuradas. Cuando haya configurado una o más impresoras, puede abrir la página **Selecciones de impresoras** para configurar para su cuenta de usuario qué informes específicos imprimir con qué impresora.

Cuando se configura una impresora y se asigna a informes específicos, para imprimir un informe se selecciona el botón **Imprimir** en la página de solicitud de informe. Para más información, vea [Imprimir un informe](ui-work-report.md#PrintReport).

### <a name="sizing-print-jobs"></a>Cambio de tamaño de los trabajos de impresión
La impresión en la nube se ha diseñado para documentos de un tamaño razonable. La mayoría de los servicios en la nube, incluidos PrintNode y HP ePrint, tienen un límite de 10 MB por trabajo. Si necesita imprimir informes más grandes, es posible que deba dividirlos en varias copias impresas.

## <a name="to-set-up-a-printer"></a>Para configurar una impresora
En la página **Administración de impresoras**, puede ver las impresoras que están configuradas y puede acceder a la página **Configuraciones** para cada impresora para editar una configuración existente o configurar una nueva impresora.

El siguiente procedimiento describe cómo configurar la **Impresora de correo electrónico** existente, que es una extensión preinstalada.

> [!NOTE]
> Para utilizar la impresión por correo electrónico, se debe configurar la funcionalidad de correo electrónico. Para obtener más información, consulte [Configurar correo electrónico](admin-how-setup-email.md).

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Administración de impresoras** y luego seleccione el enlace relacionado.
2. Seleccione la línea para la **Impresora de correo electrónico** y luego elija la acción **Editar configuración de impresora**.
3. En la página **Configuración**, rellene los campos necesarios. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]
    > Debe seleccionar manualmente el tamaño de papel adecuado para una impresora, ya que no se puede almacenar la impresora local o la configuración del usuario.
    >
    > Tenga en cuenta que la extensión de la impresora de correo electrónico está configurada con el tamaño de papel **A4** por defecto, que no es adecuado en Norteamérica, por ejemplo.
4. Para hacer que una impresora sea la predeterminada, en la página **Administración de impresoras**, elija **Establecer como mi impresora predeterminada**.

### <a name="privacy-notice"></a>Aviso de privacidad
Si utiliza la extensión de impresora de correo electrónico, todos o algunos trabajos de impresión se enviarán a la dirección de correo electrónico que proporcionó al configurar la impresora. Recomendamos encarecidamente que se vincule una identificación de correo electrónico única a un dispositivo de impresora utilizando solo los servicios oficiales proporcionados por el fabricante del hardware, como HP ePrint, KonicaMinolta EveryonePrint o Epson Email Print.

Debe tomar todas las precauciones de privacidad necesarias, incluida la garantía de que la solución de impresión de correo electrónico haya configurado correctamente los permisos, la configuración de privacidad y las políticas de retención. Es su responsabilidad proporcionar una dirección de correo electrónico correcta, verificada y operativa. Para obtener más información, consulte la [Declaración de privacidad de Microsoft](https://privacy.microsoft.com/en-us/privacystatement).

## <a name="to-select-which-printers-print-which-reports"></a>Para seleccionar qué impresoras imprimen qué informes

En la página **Selecciones de impresoras**, puede configurar para su cuenta de usuario qué informes se imprimen en qué impresora. Esto es útil si trabaja con diferentes informes que requieren impresoras diferentes debido a su ubicación en la empresa o sus capacidades de salida.

> [!IMPORTANT]
> Para [!INCLUDE[prodshort](includes/prodshort.md)] local, la página **Selecciones de impresora** solo se puede utilizar para impresoras definidas por extensiones de impresora. No se puede utilizar para impresoras locales.

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Selecciones de impresora** y luego seleccione el enlace relacionado. Alternativamente, desde la página **Administración de impresoras**, seleccione una impresora y luego elija la acción **Selecciones de impresoras**.
2. Elija la acción **Nuevo** para agregar una selección de impresora para un informe específico.
3. Rellene los campos según sea necesario.

El informe especificado estará ahora configurado para imprimirse en la impresora seleccionada de manera predeterminada.

> [!NOTE]
> Cuando imprime el informe en cuestión, puede anular esta configuración seleccionando otra impresora en la página de solicitud **Configuraciones de impresión**.

> [!NOTE]
> Si no configura un informe para una impresora específica en la página **Selecciones de impresora**, se imprimirá en la impresora predeterminada de la empresa, tal como se define en la página **Administración de impresoras**.

Usted o el administrador también pueden usar la página **Selecciones de impresora** para definir otras variaciones de impresión para usuarios e informes. La tabla siguiente describe la combinación de valores para especificar una configuración de impresión diferente para un informe.

|Para                                                 |Establecer los valores siguientes                                             |
|---------------------------------------------------|---------------------------------------------------------------------|
|Imprimir un informe en una impresora específica para todos los usuarios |Especifique los valores de los campos **Id. informe** y **Nombre impresora** y deje en blanco el campo **Id. usuario**.|
|Imprimir todos los informes en una impresora específica para un usuario específico|Especifique los valores de los campos **Id. usuario** y **Nombre impresora** y deje en blanco el campo **Id. informe**.|
|Establecer la impresora predeterminada para todos los informes|Especifique un valor en el campo **Nombre impresora** y deje en blanco los campos **Id. usuario** e **Id. informe**.|
|Imprimir un informe específico en la impresora predeterminada del usuario|Especifique un valor en el campo **Id. informe** y deje en blanco los campos **Id. usuario** y **Nombre impresora**.|
|Imprimir un informe específico en una impresora concreta para un usuario específico|Especifique los valores de los tres campos.|

> [!NOTE]
> Las selecciones de impresora más específicas tienen preferencia sobre las selecciones de impresora más generales. Por ejemplo, una selección de impresora que tenga valores en **ID de usuario**, **ID de informe** y **Nombre de impresora** tiene prioridad sobre una selección de impresora que tenga entradas en blanco en los campos **ID de usuario** o **ID de informe**.

## <a name="see-also"></a>Consulte también
[Imprimir un informe](ui-work-report.md#PrintReport)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Ejecutar procesos](ui-how-run-batch-jobs.md)  
[Enviar documentos por correo electrónico](ui-how-send-documents-email.md)  
