---
title: "Aplicar y modificar la configuración guardada en los informes | Documentos de Microsoft"
description: Describe las opciones y los filtros predefinidos para personalizar un informe y para generar los datos correctos.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customization, personalization
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 6027ba17868aca0a6571e059c9d157c542d12823
ms.contentlocale: es-es
ms.lasthandoff: 09/28/2018

---
# <a name="managing-saved-settings-on-reports"></a>Administrar configuración guardada en los informes
Cuando se ejecuta un informe, a los usuarios normalmente se les presenta una página que les permite definir determinados opciones y filtros para cambiar los datos que se incluyen en el informe generado. Esta página se llama página de solicitud de informe. Un informe puede incluir una o varias *opciones de configuración guardadas* que los usuarios pueden aplicar al informe de la página de solicitud. La *configuración guardada* son básicamente opciones y filtros predeterminados. El uso de la configuración guardada es una forma rápida y confiable de generar de forma coherente informes que contienen los datos correctos. Para obtener más información acerca de cómo se utilizan los ajustes guardados, consulte [Uso de la configuración guardada](ui-work-report.md#SavedSettings).

Si tiene los permisos adecuados, puede ver, crear y modificar la configuración guardada de todos los informes para todos los usuarios de la empresa. Puede asignar la configuración guardada de un informe a usuarios individuales o a todos los usuarios de la empresa.

<!-- 
## Apply saved settings to a report
1. Open the report.

   The report request page appears.    
2. In the **Saved Settings** section of the page, set the **Name** field  to the saved settings that you want to use.

   The **Saved Settings** section only appears if the report has been run before or if there are existing saved settings entries. The saved settings entry called **Last used options and filters** is always available. These settings are the option and filter values that were used the last time you ran the report.

-->

## <a name="create-and-modify-saved-settings-for-all-users"></a>Crear y modificar la configuración guardada para todos los usuarios
La configuración guardada se administra en la página **Configuración del informe 1560**. Hay dos maneras de abrir esta página:
-   Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Config. de informe** y luego elija el enlace relacionado.
-   Abra un informe, seleccione la búsqueda junto al cuadro **Utilizar valores predeterminado desde:**, elija **Seleccionar de la lista completa**.

La página muestra todas las entradas de configuración de almacenamiento existentes para todos los usuarios. Si hay un nombre de usuario en la columna **Asignado a**, solo ese usuario puede utilizar los parámetros guardados para el informe asociado. Si hay una marca de verificación en la columna **Compartir con todos los usuarios**, todos los usuarios pueden utilizar las opciones guardadas para el informe.

Desde la ventana **Configuración del informe**, puede:
-   Seleccione **Nuevo** para crear una nueva entrada de configuración guardada desde cero.
-   Seleccione una entrada de configuración guardada de la lista y seleccione **Copiar** para crear una copia.
-   Seleccione una entrada de configuración guardada de la lista y elija **Editar** para modificar una entrada de configuración guardada.


> [!Important]
> Considere el nombre que le asigna a una entrada de configuración guardada. Si crea una entrada de configuración guardada para todos los usuarios y le asigna el mismo nombre que la entrada de configuración guardada existente que está asignada a un usuario determinado únicamente, ese usuario no podrá utilizar la entrada de configuración guardada que se asigne a todos.  En **Configuración guardada** de la página de solicitud de informe, el usuario verá dos entradas de configuración guardada con el mismo nombre. Sin embargo, independientemente de la opción que elija, se usará la entrada de configuración guardada específica del usuario.

> [!NOTE]
> La característica de configuración guardada solo está disponible en los informes en los que la [propiedad SaveValues](https://docs.microsoft.com/en-us/dynamics-nav/savevalues-property) de la página de solicitud del informe está establecida en `Yes`. La propiedad **SaveValues** se define en el entorno de desarrollo.  

## <a name="see-also"></a>Consulte también
[Trabajar con informes](ui-work-report.md)  

