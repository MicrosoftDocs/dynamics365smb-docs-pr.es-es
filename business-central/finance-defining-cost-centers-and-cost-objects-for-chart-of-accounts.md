---
title: Definición de centros de coste y de objetos de coste para el plan de cuentas | Documentos de Microsoft
description: Puede transferir automáticamente los movimientos de gastos y de ingresos de la contabilidad a la contabilidad de costes para cada registro de contabilidad o con un trabajo por lotes. Cuando lleva a cabo la transferencia, el sistema transfiere sólo los movimientos ya vinculados a un centro o un objeto de coste. Para establecer una transferencia significativa, debe asegurarse de que los centros de coste y los objetos de coste están definidos correctamente.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
redirect_url: finance-set-up-cost-accounting
ms.openlocfilehash: 1a9178f80f6c16659509f1ae22b9225b1b6d2f70
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2019
ms.locfileid: "2302433"
---
# <a name="defining-cost-centers-and-cost-objects-for-chart-of-accounts"></a>Definición de centros de coste y de objetos de coste para el plan de cuentas
Puede transferir automáticamente los movimientos de gastos y de ingresos de la contabilidad a la contabilidad de costes para cada registro de contabilidad o con un trabajo por lotes. Cuando lleva a cabo la transferencia, [!INCLUDE[d365fin](includes/d365fin_md.md)] transfiere sólo los movimientos ya vinculados a un centro o un objeto de coste. Para establecer una transferencia significativa, debe asegurarse de que los centros de coste y los objetos de coste están definidos correctamente.  

## <a name="defining-default-dimension-values-for-general-ledger-accounts"></a>Definición de los valores de dimensión predeterminados para cuentas de contabilidad  
Para cada cuenta de contabilidad, puede definir valores de dimensión predeterminados de la tabla **Dimensión predeterminada**. El siguiente ejemplo muestra cómo definir que siempre debe haber un centro de coste de DEPARTAMENTO, pero nunca un objeto de coste de PROYECTO al registrar en una cuenta de contabilidad.  

|**Cód. dimensión**|**Registro valor**|  
|------------------------------------------|-----------------------------------------|  
|Departamento|Código obligatorio|  
|Programa|Sin código|  

## <a name="defining-dimension-values-for-overhead-costs-and-direct-costs"></a>Definición de valores de dimensión para costes generales y costes directos  
 Puede transferir costes generales a un centro de coste y costes directos a un objeto de coste. La siguiente tabla muestra la combinación óptima de valores de configuración de dimensión.  

|Transferir a|Registro del centro de coste|Registro del objeto de coste|  
|-----------------|-------------------------|-------------------------|  
|Centro coste|Código obligatorio|Sin código|  
|Objeto coste|Sin código|Código obligatorio|  

> [!NOTE]  
>  Para garantizar que el centro de coste y el objeto de coste predefinidos que configuró en la contabilidad sean transportados automáticamente a la contabilidad de costes, seleccione la casilla **Comprobar registros C/G** en la página Configuración contabilidad costes.  

## <a name="see-also"></a>Consulte también  
[Contabilidad para costes](finance-manage-cost-accounting.md)  
[Configuración de contabilidad de costes](finance-set-up-cost-accounting.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
