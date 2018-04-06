---
title: Configurar el seguro de activos fijos | Documentos de Microsoft
description: "Configure una ficha de seguridad y la información de póliza de seguro general para administrar la cobertura del seguro de los activos fijos."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: policy, coverage
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: fd59a1aea6cb42dbeac7c6978619a5648f877b52
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-fixed-asset-insurance"></a>Configure el seguro de los activos fijos
Para gestionar la cobertura del seguro de los activos fijos, debe configurar la información general de los seguros y una ficha de seguro por cada póliza.

## <a name="to-set-up-general-insurance-information"></a>Para configurar la información general de seguros
Para poder utilizar las características de seguro en [!INCLUDE[d365fin](includes/d365fin_md.md)], debe configurar antes alguna información general de seguro.  

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Configuración A/F** y, a continuación, seleccione el vínculo relacionado.  
2. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-set-up-insurance-types"></a>Para configurar tipos de seguros
Puede agrupar las pólizas de seguros en categorías, como seguro contra robo o contra incendios. Los tipos de seguros se utilizan en la ficha de seguro.

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Tipos seguros** y, a continuación, seleccione el vínculo relacionado.  
2. Rellene los campos según sea necesario.

## <a name="to-set-up-insurance-cards"></a>Para configurar fichas de seguros
Puede acumular información acerca de cada póliza de seguros en la ficha de seguro.  

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Seguro** y, a continuación, seleccione el vínculo relacionado.  
2. En la ventana **Seguro**, seleccione la acción **Nuevo** para crear una ficha de seguro nueva.  
3. Rellene los campos según sea necesario.

## <a name="to-set-up-insurance-journal-templates"></a>Para configurar libros diarios de seguros
[!INCLUDE[d365fin](includes/d365fin_md.md)] crea automáticamente un libro de diario de seguros la primera vez que abra la ventana **Diario seguros**, pero puede configurar libros de diario adicionales. Para obtener más información, consulte [Trabajar con diarios generales](ui-work-general-journals.md).  

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Libros diario seguros** y, a continuación, seleccione el vínculo relacionado.  
2. Rellene los campos según sea necesario.

## <a name="to-set-up-insurance-journal-batches"></a>Para configurar secciones del diario de seguros
En un libro del diario de seguros puede configurar secciones. Los valores de la sección del diario se utilizan como valores predeterminados si no se rellenan los campos de las líneas de diario. Para obtener más información, consulte [Trabajar con diarios generales](ui-work-general-journals.md)  

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Libros diario seguros** y, a continuación, seleccione el vínculo relacionado.  
2. Seleccione una plantilla de diario de seguros y, a continuación, selecciona la acción **Secciones**.
3. En la ventana **Secciones diario seguros**, rellene los campos según sea necesario.

> [!NOTE]  
>   Los números tienen una función especial en los nombres de diario. Si un nombre de libro diario o un nombre de sección del diario contiene un número, el número aumenta automáticamente en uno cada vez que se registra el diario. Por ejemplo, si se escribe HH1 en el campo **Nombre**, el nombre del diario cambiará a HH2 después de registrar el diario llamado HH1.

## <a name="see-also"></a>Consulte también
[Configurar activos fijos](fa-setup.md)  
[Activos fijos](fa-manage.md)  
[Finanzas](finance.md)  
[[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

