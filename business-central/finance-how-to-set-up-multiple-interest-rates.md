---
title: Configurar tasas de interés múltiples para pagos atrasados
description: Este tema explica cómo calcular cargos financieros con tasas de interés múltiples para un período específico.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '6, 431, 432, 572'
ms.date: 06/16/2021
ms.author: bholtorf
---
# Configurar tasas de interés múltiples para pagos atrasados

Puede usar tasas de interés diferentes se utilizan para diferentes períodos de pagos retrasados en las transacciones comerciales. [!INCLUDE [multiple-interest-rates-def](includes/multiple-interest-rates-def.md)]

Por ejemplo, un gobierno especifica el interés máximo que debe percibirse por un consumidor. Esta tipo de interés se puede modificar dos veces al año el 1 de enero y el 1 de julio. Las partes acuerdan la tasa de interés entre las empresas (B2B) y no existe un límite para ese grupo de clientes. La tasa anunciada es usualmente cuatro por ciento más que el interés bancario normal.

Cuando cree los términos de interés y los términos de recordatorio, para la penalización por pago atrasado, puede especificar múltiples tasas de interés para que la penalización se calcule a partir de diferentes tasas de interés en diferentes períodos.  

## Configurar varios tipos de interés

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Términos interés** y, a continuación, elija el vínculo relacionado.  
2. En la página **Términos interés**, seleccione el término requerido de interés y después seleccione la acción **Tipos de interés**.  
3. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Elija el botón **Aceptar**.  
5. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Términos de recordatorios** y luego elija el enlace relacionado.  
6. En la página **Términos recordatorio**, seleccione el término recordatorio requerido y después seleccione la acción **Niveles**.  
7. En la página **Niveles de recordatorio**, para los niveles de recordatorio relevantes, seleccione el campo **Calcular interés**.  

Cuando emite una nota de cargo financiero, la nota muestra los cargos financieros con tasas de interés múltiples para un período de tiempo específico. La nota también contiene los detalles de contacto del cliente, la empresa que emite la nota, el importe adicional y el importe total. El movimiento inicial de la nota se muestra en negrita. Los cargos financieros se calculan con tasas de interés múltiples para un período de tiempo específico y se imprimen después del movimiento inicial de la nota.  

## Consulte también

[Cobrar saldos pendientes](receivables-collect-outstanding-balances.md)  
[Configurar las finanzas](finance-setup-finance.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]