---
title: Configurar y publicar un servicio web KPI que se basa en informes financieros
description: Este artículo describe cómo mostrar los datos de KPI de informes financieros según informes financieros específicos.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.date: 12/16/2022
ms.custom: bap-template
ms.search.form: '103, 104, 108, 195, 196, 197, 198, 489, 490, 764, 765, 766'
---
# <a name="set-up-and-publish-kpi-web-services-based-on-financial-reports"></a>Configurar y publicar un servicio web KPI que se basa en informes financieros

En la página **Configuración de servicio Web KPI de informes financieros**, se configura cómo mostrar los datos de indicadores clave de rendimiento (KPI) de informes financieros y en qué informes financieros específicos se deben basar los KPI. Cuando elige el botón **Publicar servicio Web**, los datos especificados de KPI de informes financieros se agregan a la lista de servicios Web publicados en la página **Servicios Web**.

> [!NOTE]
> Cuando utiliza este servicio web, las fechas de cierre no se incluyen en su conjunto de datos. Puede usar filtros en Power BI para analizar varios períodos de tiempo.

## <a name="set-up-and-publish-a-kpi-web-service-based-on-financial-reports"></a>Configurar y publicar un servicio web de KPI que se basa en informes financieros
  
1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de servicio web KPI de informes financieros** y, a continuación, elija el vínculo relacionado.
2. Rellene los campos en la ficha desplegable **General**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. En la ficha desplegable **Definiciones de fila**, rellene los campos.
4. Repita el paso 3 para todos los informes financieros en los que desea basar el servicio web KPI de informes financieros.  
5. Para ver o editar el informe financiero seleccionado, en la ficha desplegable **Definiciones de fila**, elija la acción **Editar definición de fila**.
6. Para ver los datos KPI de informes financieros que ha configurado, elija la acción **Servicio Web de KPI de informes financieros**.
7. Para publicar el servicio Web KPI de informes financieros, elija la acción **Publicar servicio Web**.

Ahora puede crear informes financieros en Power BI según el servicio o servicios web que haya creado.

> [!NOTE]  
> También puede publicar el servicio web KPI seleccionando el objeto de la página **Configuración de servicio web KPI de informes financieros** de la página **Servicios Web**. Obtenga más información en [Publicar un servicio web](across-how-publish-web-service.md).

## <a name="see-also"></a>Consulte también .

[Inteligencia empresarial financiera](bi.md)  
[Finanzas](finance.md)  
[Configurar las finanzas](finance-setup-finance.md)  
[Libro mayor y plan de cuentas](finance-general-ledger.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
