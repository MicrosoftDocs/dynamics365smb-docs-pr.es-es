---
title: Procedimientos recomendados de configuración de planificación global | Documentos de Microsoft
description: La ficha desplegable Planificación de la página Configuración fabricación contiene varios campos que definen las reglas globales para la planificación de suministros.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Procedimientos recomendados de configuración: configuración de planificación global
La ficha desplegable **Planificación** de la página **Configuración fabricación** contiene varios campos que definen las reglas globales para la planificación de suministros.  

 La tabla siguiente proporciona las prácticas recomendadas sobre cómo configurar los campos de parámetros de planificación global seleccionados. Para obtener más información acerca de un campo, elija el vínculo en la columna **Configurar el campo**.  

|Configurar el campo|Procedimiento recomendado|Comentario|  
|-----------------|-------------------|-------------|  
|Previsiones en almacenes|Seleccione si tiene previsiones para ubicaciones específicas.||  
|Componentes en alm.|Si los productos no se definen como UA, seleccione el código de almacén del almacén principal.|Esto también es de aplicación si solo utiliza la hoja de demanda.|  
|Nivel desbordamiento en blanco|Seleccione **Permitir el cálculo predeterminado** si está migrando del Microsoft Dynamics NAV 5.0 o anterior.|Use esta opción solo si desea permitir que todos los artículos o alguno de ellos superen el punto de pedido.|  
|Periodo predet. amortiguador|Establecer entre 1D y 5D.<br /><br /> Si es la primera vez que realiza una planificación en [!INCLUDE[prod_short](includes/prod_short.md)], establezca un periodo más largo.|Cuando los usuarios estén más familiarizados con las diversas razones de los mensajes de acción, acorte el periodo amortiguador para permitir más propuestas de cambio.|  
|% cantidad predet. amortiguador|Establezca entre el 5 y el 20 por ciento del tamaño de lote del producto.||  

## Consulte también  
 [Procedimientos recomendados de configuración: planificación de suministros](setup-best-practices-supply-planning.md)   
 [Detalles de diseño: planificación de aprovisionamiento](design-details-supply-planning.md)   
 [Configurar áreas de aplicación complejas mediante procedimientos recomendados](set-up-complex-application-areas-using-best-practices.md)  
 [Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]