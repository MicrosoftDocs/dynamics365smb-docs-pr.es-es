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
ms.date: 09/08/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 2286b728a464943841b192031cfea13644441013
ms.openlocfilehash: f5225d1f6d0d4ac0020fb073d5df6da83b5c0f5b
ms.contentlocale: es-es
ms.lasthandoff: 06/28/2018

---
# <a name="managing-saved-settings-on-reports"></a>Administrar configuración guardada en los informes
Según el informe que se ejecute, es posible que se le presente una página que permite definir determinadas opciones y filtros para cambiar los datos que se incluyen en el informe generado. Esta página se conoce como la página de solicitud de informe. Un informe puede incluir una o varias *opciones de configuración guardadas* que puede aplicar al informe de la página de solicitud. La *configuración guardada* son básicamente opciones y filtros predeterminados. El uso de la configuración guardada es una forma rápida y confiable de generar de forma coherente informes que contienen los datos correctos.

Puede ver la configuración guardada que están a su disposición para un informe en la sección **Configuración guardada** de la página de solicitud de informe.  

## <a name="apply-saved-settings-to-a-report"></a>Aplicar la configuración guardada a un informe
1. Abra el informe.

   Aparece la página de solicitud de informe.    
2. En la sección **Configuración guardada** de la página, configure el campo **Nombre** como la configuración guardada que desea usar.

   La sección **Valores guardados** solo aparece si el informe se ha ejecutado antes o si hay configuraciones existentes guardadas. La configuración guardada que se denomina **Filtros y opciones usados por última vez** está siempre disponible. Esta configuración son los valores de opción y filtro que se utilizaron la última vez que ejecutó el informe.

## <a name="create-and-modify-saved-settings-for-all-users"></a>Crear y modificar la configuración guardada para todos los usuarios
Si tiene los permisos adecuados, puede ver, crear y modificar la configuración guardada de todos los informes para todos los usuarios de la empresa. Puede asignar la configuración guardada de un informe a usuarios individuales o a todos los usuarios de la empresa.

La configuración guardada se administra en la página 1506 **Configuración del informe**. Para abrir esta página, elija el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Configuración del informe** y, a continuación, seleccione el vínculo relacionado.

En la página **Configuración del informe**, puede crear nuevos valores de cero o hacer una copia y modificar la configuración existente. Para modificar las opciones y los filtros de una configuración, elija la acción **Editar**.

> [!NOTE]
> La característica de configuración guardada en informes es relevante únicamente cuando la propiedad SaveValues de la página de solicitud se define en Sí. La propiedad SaveValues se define en el entorno de desarrollo.  

> [!Important]
> Si crea un elemento de configuración guardada para todos los usuarios y tiene el mismo nombre que la configuración guardada existente de un usuario determinado, ese usuario no podrá utilizar la configuración guardada que se asigne a todos.  En el campo Configuración guardada de la página de solicitud de informe, el usuario verá dos opciones de configuración guardada con el mismo nombre. Sin embargo, independientemente de la opción que elija, se usará la configuración guardada específica del usuario.

## <a name="see-also"></a>Consulte también
[Trabajar con informes](ui-work-report.md)  

