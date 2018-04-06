---
title: "Cómo configurar un plan de tipos de coste | Documentos de Microsoft"
description: El plan de tipos de coste es similar al plan de cuentas de contabilidad general.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cost types, general ledger, accounts
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 945a60af52eec7fb4f00842acdac42472d735a12
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-cost-types"></a>Configurar tipos de costes
El plan de tipos de coste es similar al plan de cuentas de contabilidad general. Puede configurar el plan de tipos de coste de la siguiente forma:  

-   Estructure el plan de tipos de coste de manera similar a las cuentas de ingresos del plan de cuentas de contabilidad general. Luego puede transferir el plan de cuentas de contabilidad al plan de tipos de coste. Puede hacer los ajustes necesarios después de la transferencia.  
-   Cree el nuevo plan de tipos de coste o agregue nuevos tipos de coste al plan existente de tipos de coste. Debe crear cada tipo de coste nuevo por separado.  

## <a name="to-transfer-the-general-ledger-chart-of-accounts-to-the-chart-of-cost-types"></a>Para transferir el plan de cuentas de contabilidad al plan de tipos de coste  
1.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Plan tipos coste** y, a continuación, seleccione el vínculo relacionado.  
2.  Elija la acción **Traer tipos coste de plan cuentas**. En el cuadro de diálogo, seleccione el botón **Sí** para confirmar la transferencia. La función utiliza el plan de cuentas para crear un plan de tipos de coste.  

    El plan de tipos de coste contendrá todas las cuentas de ingresos en la contabilidad e incluye títulos y subtotales. Puede cambiar el plan de tipos de coste, según sea necesario. Por ejemplo, puede eliminar los tipos de coste existentes duplicados.  

    > [!IMPORTANT]  
    >  La función **Registrar tipos de coste en plan ctas.** actualiza la relación entre el plan de cuentas y el plan de tipos de coste. El campo **Nº** se rellena y comprueba para asegurarse de que cada cuenta contable está relacionada con un solo tipo de coste. La función se ejecuta automáticamente antes de transferir los movimientos de contabilidad a la contabilidad de costes.  

## <a name="to-set-up-new-cost-types-in-the-chart-of-cost-types-window"></a>Configurar nuevos tipos de coste en la ventana Tipos centros coste  
1.  Abra la ventana **Tipos centros coste** en el modo de edición.  
2.  Rellene los campos descritos como necesarios. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    >  Puede configurar y mantener tipos de coste en la ventana **Ficha tipo de coste** o bien en la ventana **Plan tipos coste**. En este procedimiento, va a configurar tipos de coste en la ventana **Plan de tipos de coste**.

3.  Una vez creados todos los tipos de coste, elija la acción **Aplicar sangría a tipos coste**. En el cuadro de diálogo, elija el botón **Sí**.  
4.  Vincule el nuevo tipo de coste a la cuenta de contabilidad correspondiente.  

    > [!IMPORTANT]  
    >  Si se han escrito definiciones en el campo **Totales** para las cuentas de tipo **Fin-Total** antes de ejecutar la función **Aplicar sangría a tipos coste**, deberá volver a escribir las definiciones más adelante porque la función sobrescribe los valores de todos los campos **Fin-Total**.  

## <a name="to-update-cost-types"></a>Para actualizar tipos de coste  
1.  En la ventana **Configuración contabilidad costes**, seleccione si desea que el plan de tipos de coste se actualice automáticamente cuando el plan de cuentas se cambia.  
2.  En el campo **Alinear cuenta C/G** puede seleccionar de entre las siguientes opciones.  

- **Sin alineación**: no hay cambio aplicable en el plan de tipos de coste cuando se modifica el plan de cuentas.  
- **Automático**: se realiza el cambio correspondiente en el plan de tipos de coste cuando se modifica el plan de cuentas.  
- **Solicitud**: se muestra un mensaje que pregunta si desea realizar a cambio correspondiente en el plan de tipos de coste cuando se realiza un cambio en el plan de cuentas.  

## <a name="see-also"></a>Consulte también  
[Contabilidad para costes](finance-manage-cost-accounting.md)  
[Definición de la relación entre los tipos de coste y las cuentas de contabilidad](finance-defining-the-relationship-between-cost-types-and-general-ledger-accounts.md)   
[Definición de centros de coste y de objetos de coste para el plan de cuentas](finance-defining-cost-centers-and-cost-objects-for-chart-of-accounts.md)   
[Saldos entre el tipo de coste, centro de coste y objeto de coste](finance-balances-between-cost-type-cost-center-and-cost-object.md)   
[Configuración de contabilidad de costes](finance-set-up-cost-accounting.md)   
[Terminología en contabilidad de costes](finance-terminology-in-cost-accounting.md)   
[Acerca de la contabilidad de costes](finance-about-cost-accounting.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

