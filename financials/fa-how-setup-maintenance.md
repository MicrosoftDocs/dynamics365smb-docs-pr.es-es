---
title: Configurar el mantenimiento de los activos fijos | Documentos de Microsoft
description: "Describe cómo configurar el sistema para el mantenimiento de los activos fijos."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: repair, service
ms.date: 03/23/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: e97f3cec67fa8b0ef270d406a0efe804da82d99f
ms.contentlocale: es-es
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-set-up-fixed-asset-maintenance"></a>Procedimiento: Configurar el mantenimiento de los activos fijos
Para gestionar el mantenimiento de los activos fijos, primero debe configurar la información de mantenimiento en una cuenta de registro para los costes de mantenimiento y los códigos de mantenimiento para los tipos de trabajo, como por ejemplo Servicio rutinario o Reparación.

## <a name="to-set-up-general-maintenance-information"></a>Para configurar la información general de mantenimiento
Si configura los campos para el mantenimiento, puede registrar los gastos de mantenimiento en un diario de activos fijos.

1. En la esquina superior derecha, seleccione el icono **Buscar página o informe** ![Buscar página o informe](media/ui-search/search_small.png "Icono Buscar página o informe"), especifique **Activos fijos** y elija el vínculo relacionado.
2. Seleccione el activo fijo del que definirá la cobertura de seguro y, a continuación, elija la acción **Editar**.
3. En la ficha desplegable **Mantenimiento**, rellene los campos como sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-maintenance-codes"></a>Para configurar los códigos de mantenimiento
Al registrar costes de mantenimiento desde un diario general, puede rellenar el campo **Cód. mantenimiento** para registrar el tipo de mantenimiento efectuado, como un servicio rutinario o una reparación.

1. En la esquina superior derecha, seleccione el icono **Buscar página o informe** ![Buscar página o informe](media/ui-search/search_small.png "Icono Buscar página o informe"), especifique **Mantenimiento** y elija el vínculo relacionado.
2. En la ventana **Mantenimiento**, configure los códigos para cada tipo de trabajo de mantenimiento.

## <a name="to-set-up-maintenance-expense-accounts"></a>Para configurar las cuentas de gastos de mantenimiento
Para registrar los costes de mantenimiento, primero debe introducir un número de cuenta en la ventana **A/F Grupos contables**.

1. En la esquina superior derecha, seleccione el icono **Buscar página o informe** ![Buscar página o informe](media/ui-search/search_small.png "Icono Buscar página o informe"), especifique **A/F Grupos contables** y elija el vínculo relacionado.
2. Rellene el campo **Cta. gastos mantenimiento** de cada grupo contable.

**Nota:** Para indicar que los costes de mantenimiento están distribuidos entre departamentos o proyectos, debe configurar claves de distribución. Para obtener más información, consulte [Procedimiento: Configurar funciones generales a los activos fijos](fa-how-setup-general.md).

## <a name="see-also"></a>Consulte también
[Configurar activos fijos](fa-setup.md)  
[Activos fijos](fa-manage.md)  
[Finanzas](finance.md)  
[[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)](ui-work-product.md)

