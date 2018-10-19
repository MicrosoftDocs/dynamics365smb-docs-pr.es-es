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
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 62ed00ef7ca278245b9cdd1a28a4ee70cf9a8f11
ms.contentlocale: es-es
ms.lasthandoff: 09/28/2018

---
# <a name="transfer-general-ledger-entries-to-cost-entries"></a>Transferir movimientos de contabilidad a movimientos de coste
Puede transferir movimientos de contabilidad a movimientos de coste.  

Antes de ejecutar el proceso para transferir movimientos de contabilidad a movimientos de coste, debe preparar la transferencia para evitar el registro manual de corrección.  

## <a name="to-prepare-the-transfer"></a>Para preparar la transferencia  

1.  Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Configuración de contabilidad de costes** y luego elija el enlace relacionado.  
2.  En la ventana **Configuración contabilidad costes**, verifique que el campo **Fecha inicio para transferencia C/G** esté definido el valor correcto.  
3.  Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Plan tipos coste** y luego elija el enlace relacionado.  
4.  En la ventana **Ficha tipo coste**, verifique que el campo **Intervalo cuenta C/G** está vinculado correctamente para cada tipo de coste para tomar movimientos de la contabilidad.  
5.  Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Plan de cuentas** y luego elija el enlace relacionado.  
6.  Para cada cuenta contable correspondiente, en la ventana **Ficha cuenta**, compruebe que el campo **Nº tipo coste** está vinculado correctamente a un tipo de coste. Para obtener más información, consulte [Definición de la relación entre los tipos de coste y las cuentas de contabilidad](finance-defining-the-relationship-between-cost-types-and-general-ledger-accounts.md).  
7.  Verifique que todos los movimientos de contabilidad correspondientes tengan valores de dimensión que correspondan a un centro de coste y a un objeto de coste.  

## <a name="to-transfer-general-ledger-entries-to-cost-entries"></a>Para transferir movimientos de contabilidad a movimientos de coste  
1.  Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Transferir movimientos de contabilidad a costes** y luego elija el enlace relacionado.  
2.  Para iniciar la transferencia, elija el botón **Sí**. El proceso transfiere todos los movimientos de contabilidad que no se han transferido ya.  

    Durante la transferencia, el proceso crea conexiones en las entradas en la tabla **Movimiento de coste** y la tabla **Registro de costes**. Esto permite realizar un seguimiento del origen de los movimientos de coste.  

## <a name="see-also"></a>Consulte también  
 [Criterios para la transferencia de movimientos de contabilidad a movimientos de coste](finance-criteria-for-transferring-general-ledger-entries-to-cost-entries.md)   
 [Transferencia automática y movimientos combinados](finance-automatic-transfer-combined-entries.md)   
 [Resultados de la transferencia](finance-results-of-the-transfer.md)   
 [Transferencia y registro de movimientos de coste](finance-transfer-and-post-cost-entries.md)   
 [Definición de la relación entre los tipos de coste y las cuentas de contabilidad](finance-defining-the-relationship-between-cost-types-and-general-ledger-accounts.md)   

