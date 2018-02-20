---
title: 'Procedimiento: configurar y publicar un servicios Web KPI que se basan en esquemas de cuentas | Documentos de Microsoft'
description: "En la ventana **Configuración de servicio Web KPI de esquema de cuentas**, se configura cómo mostrar los datos KPI del esquema de cuentas y en qué esquemas de cuentas específicos se deben basar los KPI."
services: project-madeira
documentationcenter: 
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
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 57f36592105faf0801864e034c3b930ae196ee62
ms.contentlocale: es-es
ms.lasthandoff: 01/30/2018

---
# <a name="set-up-and-publish-kpi-web-services-based-on-account-schedules"></a>Configurar y publicar un servicio web KPI que se basa en esquemas de cuentas
En la ventana **Configuración de servicio Web KPI de esquema de cuentas**, se configura cómo mostrar los datos KPI del esquema de cuentas y en qué esquemas de cuentas específicos se deben basar los KPI. Cuando elige el botón **Publicar servicio Web**, los datos especificados KPI de esquema de cuentas se agregan a la lista de servicios Web publicados en la ventana **Servicios Web**.  

## <a name="to-set-up-and-publish-a-kpi-web-service-that-is-based-on-account-schedules"></a>Para configurar y publicar un servicio web KPI que se basa en esquemas de cuentas  

1.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Configuración del servicio Web KPI de esquema de cuenta** y, a continuación, seleccione el vínculo relacionado.  
2.  En la ficha desplegable **General**, rellene los campos tal como se describe en la tabla siguiente.  

    |Campo|Descripción|  
    |---------------------------------|---------------------------------------|  
    |**Inicio de valores previstos**|Especifique en qué momento se muestran los valores previstos en el gráfico KPI del esquema de cuentas.<br /><br /> Los valores previstos se recuperan del presupuesto de contabilidad general que seleccione en el campo **Nombre presupuesto contable**. **Nota**: Para obtener KPI que muestren cifras previstas tras una fecha determinada y cifras reales antes de la fecha, puede cambiar el campo **Permitir registro desde** en la ventana **Configuración de contabilidad**. Para obtener más información, consulte Permitir registrar desde.|  
    |**Nombres pptos. contabilidad<**|Especifique el nombre del presupuesto de contabilidad que proporciona los valores previstos en el servicio web KPI de esquema de cuentas.|  
    |**Periodo**|Especifique el periodo en el que se basa el servicio web KPI de esquema de cuentas.|  
    |**Ver por**|Especifiqué en qué intervalo de tiempo se muestra el KPI de esquema de cuentas.|  
    |**Nombre del servicio web**|Especifique el nombre del servicio web KPI de esquema de cuentas.<br /><br /> Este nombre aparecerá en el campo **Nombre servicio** de la ventana **Servicios web**.|  

    Continúe especificando uno o varios esquemas de cuentas que desee publicar como servicio web de KPI según la configuración que ha realizado en la tabla anterior.  

3.  En la ficha desplegable **Esquemas de cuentas**, rellene los campos tal como se describe en la tabla siguiente.  

    |Campo|Descripción|  
    |---------------------------------|---------------------------------------|  
    |**Nombre esq. cuentas**|Especifique el esquema de cuentas en el que se basa el servicio web KPI.|  
    |**Descripción esq. cuentas**|Especifique la descripción del esquema de cuentas en la que se basa el servicio web KPI.|  

4.  Repita el paso 3 para todos los esquemas de cuentas en los que desea basar el servicio web KPI de esquema de cuentas.  
5.  Para ver o editar el esquema de cuentas seleccionado, en la ficha desplegable **Esquema de cuentas**, elija **Editar esquema cuentas**.  
6.  Para ver los datos KPI del esquema de cuentas que ha configurado, elija la acción **Servicio Web KPI de esquema de cuentas**.  
7.  Para publicar el servicio Web KPI de esquema de cuentas, elija la acción **Publicar servicio Web**. El servicio web se agrega a la lista de servicios web publicados en la ventana **Servicios web**.  

> [!NOTE]  
>  También puede publicar el servicio web KPI seleccionando el objeto de la página **Configuración de servicio web KPI de esquema de cuentas** de la ventana **Servicios Web**. Para obtener más información, consulte [Publicar un servicio web](across-how-publish-web-service.md).  

## <a name="see-also"></a>Consulte también  
[Inteligencia empresarial](bi.md)  
[Finanzas](finance.md)  
[Configurar las finanzas](finance-setup-finance.md)  
[Libro mayor y plan de cuentas](finance-general-ledger.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

