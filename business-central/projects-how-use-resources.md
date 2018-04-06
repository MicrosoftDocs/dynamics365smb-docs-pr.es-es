---
title: Registrar y ajustar el uso y los precios de los recursos | Documentos de Microsoft
description: "Describe cómo puede registrar el uso o consumo de recursos asociados a un proyecto, para realizar el seguimiento y administrar costes, precios y tipos de trabajo."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, capacity, staff
ms.date: 01/25/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: cd7561e97439b6ffcac28937a24b75a11bb31987
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="use-resources-for-jobs"></a>Uso de recursos para proyectos
El consumo de los recursos en el diario de proyectos se registra para hacer un seguimiento de costes, precios y tipos de trabajo que están vinculados a proyectos. Para obtener más información, consulte [Registro del uso para proyectos](projects-how-record-job-usage.md).

El consumo de un recurso también se puede registrar en un diario de recursos. Los movimientos registrados en un diario de recursos no afectan a la contabilidad.

## <a name="to-assign-resources-to-jobs"></a>Para asignar recursos a proyectos
Asigne recursos a proyectos creando líneas de planificación para el proyecto. Para obtener más información, vea [Crear proyectos](projects-how-create-jobs.md).

## <a name="to-record-resource-usage-for-a-job"></a>Para registrar el uso de recursos de un proyecto
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Diarios de proyectos** y, a continuación, seleccione el vínculo relacionado.
2. Abra una sección del diario de proyectos correspondiente y, a continuación, rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Cuando el diario esté completo, seleccione la acción **Registrar**.

## <a name="to-adjust-resource-prices"></a>Para ajustar los precios de los recursos
Si desea modificar los precios de coste y de venta de un gran número de recursos, puede utilizar un proceso.  

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Modificar precios recursos** y, a continuación, seleccione el vínculo relacionado.
2. Rellene los campos de una línea según sea necesario y, a continuación, haga clic en el botón **Aceptar**.

> [!NOTE]  
>   Este proceso no crea ni ajusta costes o precios alternativos de recursos. Solo cambia el contenido del campo de la ficha del recurso del **Campo ajuste** seleccionada en el trabajo por lotes. Dado que el ajuste surte efecto en los recursos al instante, compruebe los factores de ajuste antes de ejecutar el trabajo por lotes.

## <a name="to-get-resource-price-change-suggestions-based-on-existing-alternate-prices"></a>Para obtener propuestas de modificación de precios de venta de recursos basadas en precios de venta alternativos existentes
Si ya ha configurado precios de venta alternativos para algunos recursos, puede utilizar un proceso para configurar varios precios de venta de recurso alternativos.

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Cambios de precio en recursos** y, a continuación, seleccione el vínculo relacionado.
2. Elija la acción **Prop. mod. recursos (precio)** y, a continuación, rellene los campos según sea necesario.
3. Elija el botón **Aceptar**.  
4. Cuando termine el proceso, la ventana **Cambios de precio en recursos** muestra los resultados del proceso.

## <a name="to-get-resource-price-change-suggestions-based-on-standard-prices"></a>Para obtener propuestas de cambio de precio de venta de recursos basadas en precios de venta estándar
Si desea configurar varios precios alternativos basados en los precios estándar que figuran en las fichas de recurso, puede utilizar un proceso.  

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Cambios de precio en recursos** y, a continuación, seleccione el vínculo relacionado.
2. Elija la acción **Prop. mod. recurso (recurso)** y, a continuación, rellene los campos según sea necesario.  
3. Elija el botón **Aceptar**.  
4. Cuando termine el proceso, abra la ventana **Cambios de precio en recursos** para ver los resultados del proceso.

## <a name="to-get-resource-price-change-suggestions-based-on-alternate-prices"></a>Para obtener propuestas para la modificación de precios de venta de recursos basadas en los precios de venta estándar
Si ya ha configurado precios de venta alternativos para algunos recursos, puede utilizar un proceso para configurar varios precios de venta de recurso alternativos.

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Prop. &mod. recursos (precio)** y, a continuación, seleccione el vínculo relacionado.  
2. Rellene los campos según sea necesario.
3. Elija el botón **Aceptar**.  
4. Cuando termine el proceso, abra la ventana **Cambios de precio en recursos** para ver los resultados del proceso.

## <a name="see-also"></a>Consulte también
[Administración de proyectos](projects-manage-projects.md)  
[Finanzas](finance.md)  
[Compras](purchasing-manage-purchasing.md)         
[Ventas](sales-manage-sales.md)     
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

