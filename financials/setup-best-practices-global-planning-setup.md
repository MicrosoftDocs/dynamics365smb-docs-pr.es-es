---
title: "Procedimientos recomendados de configuración de planificación global | Documentos de Microsoft"
description: "La ficha desplegable **Planificación** de la ventana **Configuración fabricación** contiene varios campos que definen las reglas globales para la planificación de suministros."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: f1a4e3a30d4d665a83ab599ad19dfd3760d744b2
ms.contentlocale: es-es
ms.lasthandoff: 09/22/2017

---
# <a name="setup-best-practices-global-planning-setup"></a>Procedimientos recomendados de configuración: configuración de planificación global
La ficha desplegable **Planificación** de la ventana **Configuración fabricación** contiene varios campos que definen las reglas globales para la planificación de suministros.  

 La tabla siguiente proporciona las prácticas recomendadas sobre cómo configurar los campos de parámetros de planificación global seleccionados. Para obtener más información acerca de un campo, elija el vínculo en la columna **Configurar el campo**.  

|Configurar el campo|Procedimiento recomendado|Comentario|  
|-----------------|-------------------|-------------|  
|Previsiones en almacenes|Seleccione si tiene previsiones para ubicaciones específicas.||  
|Componentes en alm.|Si los productos no se definen como UA, seleccione el código de almacén del almacén principal.|Esto también es de aplicación si solo utiliza la hoja de demanda.|  
|Nivel desbordamiento en blanco|Seleccione **Permitir el cálculo predeterminado** si está migrando del Microsoft Dynamics NAV 5.0 o anterior.|Use esta opción solo si desea permitir que todos los artículos o alguno de ellos superen el punto de pedido.|  
|Periodo predet. amortiguador|Establecer entre 1D y 5D.<br /><br /> Si es la primera vez que realiza una planificación en [!INCLUDE[d365fin](includes/d365fin_md.md)], establezca un periodo más largo.|Cuando los usuarios estén más familiarizados con las diversas razones de los mensajes de acción, acorte el periodo amortiguador para permitir más propuestas de cambio.|  
|Cantidad predet. amortiguador|Establezca entre el 5 y el 20 por ciento del tamaño de lote del producto.||  

## <a name="see-also"></a>Consulte también  
 [Procedimientos recomendados de configuración: planificación de suministros](setup-best-practices-supply-planning.md)   
 [Detalles de diseño: planificación de aprovisionamiento](design-details-supply-planning.md)   
 [Configurar áreas de aplicación complejas mediante procedimientos recomendados](set-up-complex-application-areas-using-best-practices.md)  
 [Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

