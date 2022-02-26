---
title: Configurar y publicar servicios web KPI para esquemas de cuentas
description: Este tema describe cómo mostrar los datos de KPI del esquema de cuentas según esquemas de cuentas específicos.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/15/2021
ms.author: bholtorf
ms.openlocfilehash: b224ea5e9bb2d0f53ce41c2dac66a1686dd5a90b
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 07/08/2021
ms.locfileid: "6437006"
---
# <a name="set-up-and-publish-kpi-web-services-based-on-account-schedules"></a>Configurar y publicar un servicio web KPI que se basa en esquemas de cuentas
En la página **Configuración de servicio Web KPI de esquema de cuentas**, se configura cómo mostrar los datos KPI del esquema de cuentas y en qué esquemas de cuentas específicos se deben basar los KPI. Cuando elige el botón **Publicar servicio Web**, los datos especificados KPI de esquema de cuentas se agregan a la lista de servicios Web publicados en la página **Servicios Web**.  

> [!NOTE]
> Cuando utiliza este servicio web, las fechas de cierre no se incluyen en su conjunto de datos. Esto le permite usar filtros en Power BI para analizar varios períodos de tiempo.

## <a name="to-set-up-and-publish-a-kpi-web-service-that-is-based-on-account-schedules"></a>Para configurar y publicar un servicio web KPI que se basa en esquemas de cuentas  
1.  Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de servicio web KPI de esquema de cuentas** y, a continuación, elija el vínculo relacionado.  
2.  En la ficha desplegable **General**, rellene los campos tal como se describe en la tabla siguiente.  

    |Campo|Descripción|  
    |---------------------------------|---------------------------------------|  
    |**Inicio de valores previstos**|Especifique en qué momento se muestran los valores previstos en el gráfico KPI del esquema de cuentas.<br /><br /> Los valores previstos se recuperan del presupuesto de contabilidad general que seleccione en el campo **Nombre presupuesto contable**. **Nota**: Para obtener KPI que muestren cifras previstas tras una fecha determinada y cifras reales antes de la fecha, puede cambiar el campo **Permitir registro desde** en la página **Configuración de contabilidad**. Para obtener más información, consulte Permitir registrar desde.|  
    |**Nombres pptos. contabilidad<**|Especifique el nombre del presupuesto de contabilidad que proporciona los valores previstos en el servicio web KPI de esquema de cuentas.|  
    |**Periodo**|Especifique el periodo en el que se basa el servicio web KPI de esquema de cuentas.|  
    |**Ver por**|Especifiqué en qué intervalo de tiempo se muestra el KPI de esquema de cuentas.|  
    |**Nombre del servicio web**|Especifique el nombre del servicio web KPI de esquema de cuentas.<br /><br /> Este nombre aparecerá en el campo **Nombre servicio** de la página **Servicios web**.|  

    Especifique uno o varios esquemas de cuentas que desee publicar como servicio web de KPI según la configuración que ha realizado en la tabla anterior.  

3.  En la ficha desplegable **Esquemas de cuentas**, rellene los campos tal como se describe en la tabla siguiente.  

    |Campo|Descripción|  
    |---------------------------------|---------------------------------------|  
    |**Nombre esq. cuentas**|Especifique el esquema de cuentas en el que se basa el servicio web KPI.|  
    |**Descripción esq. cuentas**|Especifique la descripción del esquema de cuentas en la que se basa el servicio web KPI.|  

4.  Repita el paso 3 para todos los esquemas de cuentas en los que desea basar el servicio web KPI de esquema de cuentas.  
5.  Para ver o editar el esquema de cuentas seleccionado, en la ficha desplegable **Esquema de cuentas**, elija **Editar esquema cuentas**.  
6.  Para ver los datos KPI del esquema de cuentas que ha configurado, elija la acción **Servicio Web KPI de esquema de cuentas**.  
7.  Para publicar el servicio Web KPI de esquema de cuentas, elija la acción **Publicar servicio Web**. El servicio web se agrega a la lista de servicios web publicados en la página **Servicios web**.  

> [!NOTE]  
>  También puede publicar el servicio web KPI seleccionando el objeto de la página **Configuración de servicio web KPI de esquema de cuentas** de la página **Servicios Web**. Para obtener más información, consulte [Publicar un servicio web](across-how-publish-web-service.md).  

## <a name="see-also"></a>Consulte también  
[Inteligencia empresarial](bi.md)  
[Finanzas](finance.md)  
[Configurar las finanzas](finance-setup-finance.md)  
[Libro mayor y plan de cuentas](finance-general-ledger.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]