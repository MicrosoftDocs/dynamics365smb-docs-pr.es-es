---
title: 'Procedimiento: transferencia de movimientos de contabilidad a los movimientos de coste | Documentos de Microsoft'
description: Puede transferir movimientos de contabilidad a movimientos de coste.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 11/13/2018
ms.author: sgroespe
redirect_url: finance-transfer-and-post-cost-entries
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 273a8c4341f621710819fd5fbc5cb8ce579c86f5
ms.contentlocale: es-es
ms.lasthandoff: 11/26/2018

---
# <a name="transfer-general-ledger-entries-to-cost-entries"></a>Transferir movimientos de contabilidad a movimientos de coste
Puede transferir movimientos de contabilidad a movimientos de coste.  

Antes de ejecutar el proceso para transferir movimientos de contabilidad a movimientos de coste, debe preparar la transferencia para evitar el registro manual de corrección.  

## <a name="to-prepare-the-transfer"></a>Para preparar la transferencia  

1.  Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Configuración de contabilidad de costes** y luego elija el enlace relacionado.  
2.  En la página **Configuración contabilidad costes**, verifique que el campo **Fecha inicio para transferencia C/G** esté definido el valor correcto.  
3.  Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Plan tipos coste** y luego elija el enlace relacionado.  
4.  En la página **Ficha tipo coste**, verifique que el campo **Intervalo cuenta C/G** está vinculado correctamente para cada tipo de coste para tomar movimientos de la contabilidad.  
5.  Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Plan de cuentas** y luego elija el enlace relacionado.  
6.  Para cada cuenta contable correspondiente, en la página **Ficha cuenta**, compruebe que el campo **Nº tipo coste**. está vinculado correctamente a un tipo de coste. Para obtener más información, consulte [Configuración de contabilidad de costes](finance-set-up-cost-accounting.md).  
7.  Verifique que todos los movimientos de contabilidad correspondientes tengan valores de dimensión que correspondan a un centro de coste y a un objeto de coste.  

## <a name="to-transfer-general-ledger-entries-to-cost-entries"></a>Para transferir movimientos de contabilidad a movimientos de coste  
1.  Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Transferir movimientos de contabilidad a costes** y luego elija el enlace relacionado.  
2.  Para iniciar la transferencia, elija el botón **Sí**. El proceso transfiere todos los movimientos de contabilidad que no se han transferido ya.  

    Durante la transferencia, el proceso crea conexiones en las entradas en la tabla **Movimiento de coste** y la tabla **Registro de costes**. Esto permite realizar un seguimiento del origen de los movimientos de coste.  

## <a name="see-also"></a>Consulte también  
[Transferencia y registro de movimientos de coste](finance-transfer-and-post-cost-entries.md)   
[Configuración de contabilidad de costes](finance-set-up-cost-accounting.md)   

