---
title: Procedimientos recomendados de configuración de planificación global | Documentos de Microsoft
description: La ficha desplegable Planificación de la página Configuración fabricación contiene varios campos que definen las reglas globales para la planificación de suministros.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 9dfc1c42d2ce74792209b25b1fb6e48126ed9d5a
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5391104"
---
# <a name="setup-best-practices-global-planning-setup"></a>Procedimientos recomendados de configuración: configuración de planificación global
La ficha desplegable **Planificación** de la página **Configuración fabricación** contiene varios campos que definen las reglas globales para la planificación de suministros.  

 La tabla siguiente proporciona las prácticas recomendadas sobre cómo configurar los campos de parámetros de planificación global seleccionados. Para obtener más información acerca de un campo, elija el vínculo en la columna **Configurar el campo**.  

|Configurar el campo|Procedimiento recomendado|Comentario|  
|-----------------|-------------------|-------------|  
|Previsiones en almacenes|Seleccione si tiene previsiones para ubicaciones específicas.||  
|Componentes en alm.|Si los productos no se definen como UA, seleccione el código de almacén del almacén principal.|Esto también es de aplicación si solo utiliza la hoja de demanda.|  
|Nivel desbordamiento en blanco|Seleccione **Permitir el cálculo predeterminado** si está migrando del Microsoft Dynamics NAV 5.0 o anterior.|Use esta opción solo si desea permitir que todos los artículos o alguno de ellos superen el punto de pedido.|  
|Periodo predet. amortiguador|Establecer entre 1D y 5D.<br /><br /> Si es la primera vez que realiza una planificación en [!INCLUDE[prod_short](includes/prod_short.md)], establezca un periodo más largo.|Cuando los usuarios estén más familiarizados con las diversas razones de los mensajes de acción, acorte el periodo amortiguador para permitir más propuestas de cambio.|  
|% cantidad predet. amortiguador|Establezca entre el 5 y el 20 por ciento del tamaño de lote del producto.||  

## <a name="see-also"></a>Consulte también  
 [Procedimientos recomendados de configuración: planificación de suministros](setup-best-practices-supply-planning.md)   
 [Detalles de diseño: planificación de aprovisionamiento](design-details-supply-planning.md)   
 [Configurar áreas de aplicación complejas mediante procedimientos recomendados](set-up-complex-application-areas-using-best-practices.md)  
 [Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]