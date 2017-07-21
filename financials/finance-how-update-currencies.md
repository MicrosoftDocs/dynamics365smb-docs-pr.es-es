---
title: Actualizar los tipos de cambio de divisa | Documentos de Microsoft
description: "Para utilizar varias divisas en su empresa, puede configurar un código para cada divisa y usar un servicio externo para el tipo de cambio, como Yahoo."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies, Yahoo
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: cc60569091b3aa37d17e981f1fae8f46c4a004df
ms.contentlocale: es-es
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-update-currency-exchange-rates"></a>Actualizar los tipos de cambio de divisa
Debe configurar un código por cada una de las divisas usadas en caso de que las operaciones de compra y venta se realicen en una divisa que no sea la divisa local (DL), tenga cobros y pagos en otras divisas o registre las transacciones de contabilidad en diferentes divisas.  

> [!NOTE]  
>   Esta funcionalidad requiere que la experiencia esté definida en **Conjunto de aplicaciones**. Para obtener más información, consulte [Personalizar la experiencia de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md).

Puede utilizar un servicio externo para mantener actualizados los tipos de cambio de divisa. El servicio de tipos de cambio de divisa de Yahoo está preinstalado y listo para activarse.

## <a name="to-set-up-a-currency-exchange-rate-service"></a>Para configurar un servicio de tipo de cambio de divisa
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Servicios de tipo de cambio de divisas** y, a continuación, elija el vínculo relacionado.
2. Seleccione la acción **Nuevo**.
3. En la ventana **Servicio de tipo de cambio de divisas**, rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Seleccione la casilla de verificación **Activado** para activar el servicio.

## <a name="to-update-currency-exchange-rates-through-a-service"></a>Para actualizar los tipos de cambio de divisa mediante un servicio
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Servicios de tipo de cambio de divisas"), escriba **Divisas** y, a continuación, seleccione el vínculo relacionado.
2. Seleccione la acción **Actualizar tipos de cambio**.

El valor del campo **Tipo cambio** en la ventana **Divisas** se actualiza con el último tipo de cambio de divisa.

## <a name="see-also"></a>Consulte también
[Cerrar años y periodos](year-close-years-periods.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

