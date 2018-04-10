---
title: Configurar el mantenimiento de activos fijos | Documentos de Microsoft
description: "Para administrar las reparaciones y el servicio de los activos fijos, puede especificar información de mantenimiento general, códigos para el tipo de trabajo y una cuenta de mayor para costes."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: repair, service
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: b730e880a3cf9f2ba3a2abaa25a1b80848f52e97
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-fixed-asset-maintenance"></a>Configure el mantenimiento de los activos fijos
Para gestionar el mantenimiento de los activos fijos, primero debe configurar la información de mantenimiento en una cuenta de registro para los costes de mantenimiento y los códigos de mantenimiento para los tipos de trabajo, como por ejemplo Servicio rutinario o Reparación.

## <a name="to-set-up-general-maintenance-information"></a>Para configurar la información general de mantenimiento
Si configura los campos para el mantenimiento, puede registrar los gastos de mantenimiento en un diario de activos fijos.

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Activos fijos** y, a continuación, seleccione el vínculo relacionado.
2. Seleccione el activo fijo del que definirá la cobertura de seguro y, a continuación, elija la acción **Editar**.
3. En la ficha desplegable **Mantenimiento**, rellene los campos como sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-maintenance-codes"></a>Para configurar los códigos de mantenimiento
Al registrar costes de mantenimiento desde un diario general, puede rellenar el campo **Cód. mantenimiento** para registrar el tipo de mantenimiento efectuado, como un servicio rutinario o una reparación.

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Mantenimiento** y, a continuación, seleccione el vínculo relacionado.
2. En la ventana **Mantenimiento**, configure los códigos para cada tipo de trabajo de mantenimiento.

## <a name="to-set-up-maintenance-expense-accounts"></a>Para configurar las cuentas de gastos de mantenimiento
Para registrar los costes de mantenimiento, primero debe introducir un número de cuenta en la ventana **A/F Grupos contables**.

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **A/F Grupos contables** y, a continuación, seleccione el vínculo relacionado.
2. Rellene el campo **Cta. gastos mantenimiento** de cada grupo contable.

> [!NOTE]  
>   Para indicar que los costes de mantenimiento están distribuidos entre departamentos o proyectos, debe configurar claves de distribución. Para obtener más información, consulte [Configurar funciones generales a los activos fijos](fa-how-setup-general.md).

## <a name="see-also"></a>Consulte también
[Configurar activos fijos](fa-setup.md)  
[Activos fijos](fa-manage.md)  
[Finanzas](finance.md)  
[Introducción](product-get-started.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

