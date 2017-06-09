---
title: Configurar ciclos de ventas de oportunidad y etapas de ciclo | Documentos de Microsoft
description: "Describe cómo configurar etapas y ciclos de ventas de oportunidad en Financials"
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 03/28/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 63d3e4689a751e8e56363efcfde1d609762a419e
ms.contentlocale: es-es
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-set-up-opportunity-sales-cycles-and-cycle-stages"></a>Procedimiento: Configurar ciclos de ventas de oportunidad y etapas de ciclo
Para poder usar oportunidades de ventas, debe configurar ciclos de ventas y etapas del ciclo de ventas. Un ciclo de ventas se compone de una serie de etapas que van desde el contacto inicial hasta el cierre de una venta. Cada etapa puede tener determinados requisitos que se deben cumplir, por ejemplo, requerir una oferta de venta, antes de que la oportunidad pueda pasar a la siguiente etapa. También puede especificar si se puede omitir una etapa. Puede configurar tantos ciclos de ventas como necesite y tantas etapas del ciclo de ventas como sean necesarias para el ciclo de ventas.

La implementación de ciclos de ventas de oportunidad implica la configuración del código de ciclo de ventas, que define las diferentes etapas del ciclo, y la asignación del ciclo a oportunidades.

## <a name="to-set-up-an-opportunity-sales-cycle-code"></a>Para configurar un código de ciclo de ventas de oportunidad
1. En la esquina superior derecha, seleccione el icono **Buscar página o informe** ![Buscar página o informe](media/ui-search/search_small.png "Icono Buscar página o informe"), especifique **Ciclos venta** y elija el vínculo relacionado. Se abre la ventana **Ciclos de ventas** y se muestran todos los ciclos de ventas existentes.
2. Seleccione la acción **Nuevo** y rellene los campos.

Repita estos pasos para configurar todos los ciclos de venta que desee. Después de configurar los ciclos de ventas de oportunidad, puede que quiera configurar las distintas etapas de cada ciclo.

## <a name="to-define-opportunity-sales-cycle-stages"></a>Para definir las etapas del ciclo de ventas de oportunidad
1. En la ventana **Ciclos de ventas**, seleccione el ciclo de ventas de oportunidad para el que quiere configurar etapas y, a continuación, seleccione la acción **Etapas**. Se abre la ventana **Etapas de ciclo de ventas**.
2. Seleccione la acción **Nuevo** para introducir una nueva etapa en el ciclo de ventas.

Repita estos pasos para configurar tantas etapas como desee del ciclo de ventas.

## <a name="to-assign-stage-cycle-to-an-opportunity"></a>Para asignar el ciclo de la etapa a una oportunidad
Cuando haya agregado el ciclo de la etapa de oportunidades, puede empezar a agregar oportunidades de ventas y, a continuación, asignar el ciclo de la etapa a oportunidades configurando el campo **Código de ciclo de ventas**. Para obtener más información, consulte [Procedimiento: Crear oportunidades de ventas](marketing-how-create-opportunities.md).

## <a name="see-also"></a>Consulte también
[Procesar oportunidades de ventas](marketing-processing-sales-opportunities.md)  
[Ventas](sales-manage-sales.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)](ui-work-product.md)

