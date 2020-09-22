---
title: Aplicar y modificar la configuración guardada en los informes | Documentos de Microsoft
description: Describe las opciones y los filtros predefinidos para personalizar un informe y para generar los datos correctos.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customization, personalization
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: d61e599b9e86f28de6edcf4ccff5b245503880fe
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "3784614"
---
# <a name="manage-saved-settings-for-reports-and-batch-jobs"></a>Administrar configuraciones guardadas para informes y trabajos por lotes
Cuando se ejecutan informes, a los usuarios normalmente se les presenta una página que les permite seleccionar opciones y establecer filtros para cambiar los datos que se incluyen en el informe generado. Esta página se llama página de solicitud. Un informe puede incluir una o varias *opciones de configuración guardadas* que los usuarios pueden aplicar al informe de la página de solicitud. La *configuración guardada* son básicamente opciones y filtros predeterminados. El uso de la configuración guardada es una forma rápida y confiable de generar de forma coherente informes que contienen los datos correctos. Para obtener más información, consulte [Uso de la configuración guardada](ui-work-report.md#SavedSettings).

> [!NOTE]
> Este tema hace referencia principalmente al "informe", pero se aplica información similar a los trabajos por lotes.

Si tiene los permisos adecuados, puede ver, crear y modificar la configuración guardada de todos los informes para todos los usuarios de una empresa. Puede asignar la configuración guardada de un informe a usuarios individuales o a todos los usuarios de la empresa.

<!--
## Apply saved settings to a report
1. Open the report.

   The request page appears.    
2. In the **Saved Settings** section of the page, set the **Name** field  to the saved settings that you want to use.

   The **Saved Settings** section only appears if the report has been run before or if there are existing saved settings entries. The saved settings entry called **Last used options and filters** is always available. These settings are the option and filter values that were used the last time you ran the report.

-->

## <a name="to-create-and-modify-saved-settings-for-all-users"></a>Para crear y modificar la configuración guardada para todos los usuarios
La configuración guardada se administra en la página **Configuración de informes**. Hay dos maneras de abrir esta página:
-   Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Configuración del informe** y luego elija el enlace relacionado.
-   Abra un informe, seleccione la búsqueda en el campo **Utilizar valores predeterminado desde** y, a continuación, elija la acción **Seleccionar de la lista completa**.

La página muestra todas las entradas de configuración guardada de almacenamiento existentes para todos los usuarios. Si hay un nombre de usuario en el campo **Asignado a**, solo ese usuario puede utilizar los parámetros guardados para el informe asociado. Si hay una marca de verificación en el campo **Compartir con todos los usuarios**, todos los usuarios pueden utilizar las opciones guardadas para el informe.

Desde la página **Configuración del informe**, puede:
-   Seleccione la acción **Nuevo** para crear una nueva entrada de configuración guardada desde cero.
-   Seleccione una entrada de configuración guardada de la lista y seleccione la acción **Copiar** para crear una copia.
-   Seleccione una entrada de configuración guardada de la lista y elija la acción **Editar** para modificar una entrada de configuración guardada.

> [!Important]
> Considere el nombre que le asigna a una entrada de configuración guardada. Si crea una entrada de configuración guardada para todos los usuarios y le asigna el mismo nombre que la entrada de configuración guardada existente que está asignada a un usuario determinado únicamente, ese usuario no podrá utilizar la entrada de configuración guardada que se asigne a todos.  En la sección **Configuración guardada** de la página de solicitud, el usuario verá dos entradas de configuración guardada con el mismo nombre. Sin embargo, independientemente de la opción que elija, se usará la entrada de configuración guardada específica del usuario.

> [!NOTE]
> La característica Configuración guardada solo está disponible en los informes en los que la [propiedad SaveValues](/dynamics365/business-central/dev-itpro/developer/properties/devenv-savevalues-property) de la página de solicitud del informe está establecida en **Sí**. La propiedad **SaveValues** se define en el entorno de desarrollo.  

## <a name="see-also"></a>Consulte también
[Trabajar con informes, trabajos por lotes y XMLports](ui-work-report.md)  
