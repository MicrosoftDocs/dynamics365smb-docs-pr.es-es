---
title: Cambiar el aspecto de un informe seleccionando otro diseño | Documentos de Microsoft
description: Puede utilizar diseños distintos para un informe y cambiar de un diseño a otro para cambiar el aspecto de un informe.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 07de4be7bc516cf9f4b802a48dc59293b1992f5f
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2019
ms.locfileid: "2315257"
---
# <a name="change-the-current-report-layout"></a>Cambiar el diseño de informe actual
Un informe se puede configurar con varios diseños de informe, entre los que puede cambiar según sea necesario.

Según los diseños disponibles para un informe, puede optar por usar un diseño de informe de RDLC integrado, un diseño de informe de Word integrado o un diseño personalizado. Para obtener más información acerca de los diseños de informe de RDLC y de Word, diseños personalizados e integrados y otros temas, consulte [Gestionar diseños de informe](ui-manage-report-layouts.md).

> [!TIP]  
> Los informes de documento (no listas) que utilizan un diseño de informe de Word suelen ser más rápidos que los que utilizan un diseño de informe RDLC. Por lo tanto, si tiene la opción de elegir entre un diseño de informe Word o RDLC para un informe de documento, utilice el diseño de informe Word para obtener el mejor rendimiento.  

## <a name="to-change-the-layout-that-is-used-on-a-report"></a>Para cambiar el diseño que se usa en un informe
1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Selección de diseño de informes** y luego elija el enlace relacionado.  
   La página **Selección de diseño de informes** muestra todos los informes disponibles en la empresa especificada en el campo Empresa en la parte superior de la página. El campo Diseño seleccionado especifica el diseño que actualmente se está usando en el informe.
2. Establezca el campo **Empresa** en la parte superior de la página en la empresa que incluye el informe.
3. Para cambiar el diseño que se usa en un informe, en la fila del informe en la lista, establezca el campo **Diseño seleccionado** en una de las opciones siguientes:
   * Usa el diseño de informe de RDLC integrado en el informe.
   * Usa el diseño de informe de Word integrado en el informe.
   * Custom, usa un diseño personalizado en el informe.  

Puede ver qué diseños personalizados estarán disponibles para el informe en el cuadro informativo **Parte de diseños de informe**. Si no hay diseños personalizados para el informe, deberá crear uno primero. Si elige esta opción, vaya al procedimiento siguiente para especificar el diseño personalizado que desea usar.

> [!NOTE]
> Si elige **RDLC (integrado)** o **Word (integrado)** y recibe un mensaje de error en el que se indica que el informe no tiene un diseño del tipo especificado, debe elegir otra opción de diseño o crear un diseño de informe personalizado del tipo que desea usar.

Si ha seleccionado un diseño de informe de RDLC o de Word, no se requiere ninguna otra acción y el diseño se utilizará la próxima vez que se ejecute el informe.

## <a name="to-specify-a-custom-layout-on-a-report"></a>Para especificar un diseño personalizado en un informe
1. El diseño personalizado que se usará en el informe se especifica en la página **Diseños de informe personalizados**. Si la página **Diseños de informes personalizados** no está abierta, seleccione el botón de búsqueda en el campo **Descripción de diseño de informe**.
2. En la página **Diseños de informe personalizados**, seleccione la fila del diseño personalizado que desee usar y, a continuación, cierre la página.

Puede volver a la página **Selección de diseño de informes**. El nombre del diseño personalizado seleccionado se muestra en el campo **Descripción de diseño personalizado**. El diseño personalizado se utilizará la siguiente vez que se ejecute el informe.

## <a name="see-also"></a>Consulte también
[Gestión de diseños de informe](ui-manage-report-layouts.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
