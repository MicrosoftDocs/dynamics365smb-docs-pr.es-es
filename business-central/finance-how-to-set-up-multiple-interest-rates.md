---
title: "Configurar varios tipos de interés"
description: "Puede calcular cargos financieros con tasas de interés múltiples para un período específico. El cálculo de intereses es similar para todos los cargos financieros, con variación solo en la tasa de interés para un período específico."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 12/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 0af01fe46f6b7df1149825c35a9fc0cc19482403
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-multiple-interest-rates"></a>Configurar varios tipos de interés.
Las tasas de interés múltiples se utilizan para diferentes períodos de pagos retrasados en las transacciones comerciales. Por ejemplo, un gobierno especifica el interés máximo que debe percibirse por un consumidor. Esta tipo de interés se puede modificar dos veces al año el 1 de enero y el 1 de julio. Las partes acuerdan la tasa de interés entre las empresas (B2B) y no existe un límite para ese grupo de clientes. La tasa anunciada es usualmente cuatro por ciento más que el interés bancario normal.

Cuando cree los términos de interés y los términos de recordatorio, para la penalización por pago atrasado, puede especificar múltiples tasas de interés para que la penalización se calcule a partir de diferentes tasas de interés en diferentes períodos. Para obtener más información, vea [Cobrar saldos pendientes](receivables-collect-outstanding-balances.md).

## <a name="to-set-up-multiple-interest-rates"></a>Configurar varios tipos de interés  
1.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Términos interés** y, a continuación, seleccione el vínculo relacionado.  
2.  En la ventana **Términos interés**, seleccione el término requerido de interés y después seleccione la acción **Tipos de interés**.  
3.  Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4.  Elija el botón **Aceptar**.  
5.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Recordatorio** y, a continuación, seleccione el vínculo relacionado.  
6.  En la ventana **Términos recordatorio**, seleccione el término recordatorio requerido y después seleccione la acción **Niveles**.  
7.  En la ventana **Niveles recordatorio**, seleccione el campo **Cálculo interés**.  

Cuando emite una nota de cargo financiero, la nota muestra los cargos financieros con tasas de interés múltiples para un período de tiempo específico. La nota también contiene los detalles de contacto del cliente, la empresa que emite la nota, el importe adicional y el importe total. El movimiento inicial de la nota se muestra en negrita. Los cargos financieros se calculan con tasas de interés múltiples para un período de tiempo específico y se imprimen después del movimiento inicial de la nota.  

## <a name="see-also"></a>Consulte también  
[Cobrar saldos pendientes](receivables-collect-outstanding-balances.md)  
[Configurar las finanzas](finance-setup-finance.md)

