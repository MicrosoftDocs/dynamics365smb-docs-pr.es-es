---
title: Definición de la relación entre los tipos de coste y las cuentas de contabilidad | Documentos de Microsoft
description: Obtenga información sobre cómo definir la relación entre el tipo de coste y la cuenta de contabilidad.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cost types, general ledger
ms.date: 10/01/2019
ms.author: sgroespe
redirect_url: finance-transfer-and-post-cost-entries
ms.openlocfilehash: c781eeb37adb383ab64786f9672d982afe184759
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2019
ms.locfileid: "2302409"
---
# <a name="defining-the-relationship-between-cost-types-and-general-ledger-accounts"></a>Definición de la relación entre los tipos de coste y las cuentas de contabilidad
La relación entre el tipo de coste y la cuenta de contabilidad se crea en el tipo de coste y en la cuenta de contabilidad.  

* El campo **Intervalo cuenta C/G** en la tabla **Tipo coste** establece qué cuentas de contabilidad pertenecen a un tipo de coste.  
* El campo **Nº tipo coste** en el plan de cuentas establece a qué tipo de coste pertenece una cuenta de contabilidad.  

Estos dos campos se rellenan automáticamente cuando utiliza la función **Obtener tipos coste de plan ctas.**  

## <a name="relationship-between-general-ledger-accounts-and-cost-types"></a>Relación entre las cuentas de contabilidad y los tipos de coste  
Existe una relación n:1 entre las cuentas de contabilidad y los tipos de coste Varias cuentas de contabilidad pueden pertenecer a un tipo de coste, pero cada cuenta de contabilidad pertenece a sólo un tipo de coste. La siguiente tabla describe los detalles de la relación.  

|Relaciones|**Intervalo cuenta CG**|**Nº tipo coste**|  
|------------------|------------------------------------------------|-------------------------------------------|  
|Una cuenta de contabilidad para cada tipo de coste|Cuentas contables|Un tipo de coste|  
|Varias cuentas de contabilidad para un tipo de coste|Intervalo de cuenta de contabilidad, por ejemplo, 7110..7193 para cada cuenta de contabilidad|Para cada cuenta de contabilidad del intervalo, existe únicamente un tipo de coste|  
|Tipos de coste sin las cuentas de contabilidad correspondientes|<Empty>||  
|Cuentas de contabilidad cuyos movimientos no se transferirán||<Empty>|  

## <a name="cost-types-without-a-relationship-to-the-general-ledger"></a>Tipos de coste sin una relación con la contabilidad  
Un tipo de coste puede no tener una relación con las cuentas contables si una de las siguientes condiciones es verdadera:  

* Las cuentas para la contabilidad operativa, como Calc. intereses y amortización, sólo toman costes de la contabilidad operativa.  
* Los tipos de coste de ayuda, como los tipos de coste 9901, 9902 y 9903, en la base de datos de [!INCLUDE[d365fin](includes/d365fin_md.md)], se utilizan como cuentas de crédito y débito para asignaciones.  
* La cuenta de ayuda, 9920 en la base de datos de [!INCLUDE[d365fin](includes/d365fin_md.md)], contiene las acumulaciones reales que muestran la diferencia entre los costes y el gasto de contabilidad.  

## <a name="see-also"></a>Consulte también  
[Contabilidad para costes](finance-manage-cost-accounting.md)  
[Configuración de contabilidad de costes](finance-set-up-cost-accounting.md)   
[Acerca de la contabilidad de costes](finance-about-cost-accounting.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
