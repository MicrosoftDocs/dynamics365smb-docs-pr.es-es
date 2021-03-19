---
title: Configurar varios tipos de interés
description: Puede calcular cargos financieros con tasas de interés múltiples para un período específico. El cálculo de intereses es similar para todos los cargos financieros, con variación solo en la tasa de interés para un período específico.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 96098ca669dd5001f334cf464d8e3a37de5dbf03
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5387279"
---
# <a name="set-up-multiple-interest-rates"></a>Configurar varios tipos de interés.
Las tasas de interés múltiples se utilizan para diferentes períodos de pagos retrasados en las transacciones comerciales. Por ejemplo, un gobierno especifica el interés máximo que debe percibirse por un consumidor. Esta tipo de interés se puede modificar dos veces al año el 1 de enero y el 1 de julio. Las partes acuerdan la tasa de interés entre las empresas (B2B) y no existe un límite para ese grupo de clientes. La tasa anunciada es usualmente cuatro por ciento más que el interés bancario normal.

Cuando cree los términos de interés y los términos de recordatorio, para la penalización por pago atrasado, puede especificar múltiples tasas de interés para que la penalización se calcule a partir de diferentes tasas de interés en diferentes períodos. Para obtener más información, vea [Cobrar saldos pendientes](receivables-collect-outstanding-balances.md).

## <a name="to-set-up-multiple-interest-rates"></a>Configurar varios tipos de interés  
1.  Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Términos interés** y luego elija el enlace relacionado.  
2.  En la página **Términos interés**, seleccione el término requerido de interés y después seleccione la acción **Tipos de interés**.  
3.  Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4.  Elija el botón **Aceptar**.  
5.  Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Términos recordatorio** y luego elija el enlace relacionado.  
6.  En la página **Términos recordatorio**, seleccione el término recordatorio requerido y después seleccione la acción **Niveles**.  
7.  En la página **Niveles recordatorio**, seleccione el campo **Cálculo interés**.  

Cuando emite una nota de cargo financiero, la nota muestra los cargos financieros con tasas de interés múltiples para un período de tiempo específico. La nota también contiene los detalles de contacto del cliente, la empresa que emite la nota, el importe adicional y el importe total. El movimiento inicial de la nota se muestra en negrita. Los cargos financieros se calculan con tasas de interés múltiples para un período de tiempo específico y se imprimen después del movimiento inicial de la nota.  

## <a name="see-also"></a>Consulte también  
[Cobrar saldos pendientes](receivables-collect-outstanding-balances.md)  
[Configurar las finanzas](finance-setup-finance.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]