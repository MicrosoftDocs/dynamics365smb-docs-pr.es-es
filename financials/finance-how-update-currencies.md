---
title: Actualizar los tipos de cambio de divisa desde un servicio | Documentos de Microsoft
description: Trabajar con varias divisas
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies, Yahoo
ms.date: 03/24/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: b261da0f233ce78a9f14c2979c876be401ffedef
ms.contentlocale: es-es
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-update-currency-exchange-rates"></a>Actualizar los tipos de cambio de divisa
Debe configurar un código por cada una de las divisas usadas en caso de que las operaciones de compra y venta se realicen en una divisa que no sea la divisa local (DL), tenga cobros y pagos en otras divisas o registre las transacciones de contabilidad en diferentes divisas.  

**Nota**: Esta funcionalidad que requiere que la experiencia esté definida en **Conjunto de aplicaciones**. Para obtener más información, consulte [Personalizar la experiencia de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md).

Puede utilizar un servicio externo para mantener actualizados los tipos de cambio de divisa. El servicio de tipos de cambio de divisa de Yahoo está preinstalado y listo para activarse.

## <a name="to-set-up-a-currency-exchange-rate-service"></a>Para configurar un servicio de tipo de cambio de divisa
1. En la esquina superior derecha, seleccione el icono **Buscar página o informe** ![Buscar página o informe](media/ui-search/search_small.png "Icono Buscar página o informe"), especifique **Servicios de tipo de cambio de divisas** y elija el vínculo relacionado.
2. Seleccione la acción **Nuevo**.
3. En la ventana **Servicio de tipo de cambio de divisas**, rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Seleccione la casilla de verificación **Activado** para activar el servicio.

## <a name="to-update-currency-exchange-rates-through-a-service"></a>Para actualizar los tipos de cambio de divisa mediante un servicio
1. En la esquina superior derecha, seleccione el icono **Buscar página o informe** ![Buscar página o informe](media/ui-search/search_small.png "Icono Buscar página o informe"), especifique **Divisas** y elija el vínculo relacionado.
2. Seleccione la acción **Actualizar tipos de cambio**.

El valor del campo **Tipo cambio** en la ventana **Divisas** se actualiza con el último tipo de cambio de divisa.

## <a name="see-also"></a>Consulte también
[Cerrar años y periodos](year-close-years-periods.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)](ui-work-product.md)

