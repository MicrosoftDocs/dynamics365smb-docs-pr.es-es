---
title: "Especificar el diseño de un cheque | Documentos de Microsoft"
description: "Puede diseñar e imprimir los cheques en diferentes formatos para cumplir los estándares."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, customize
ms.date: 06/15/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: a2db2860846cd9b8010222faf580f0c9889e39a4
ms.contentlocale: es-es
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-define-check-layouts"></a>Procedimiento: Definir diseños de cheque
Puede diseñar los cheques conforme a los estándares definidos por las autoridades locales. Las imágenes de los cheques se pueden imprimir en inglés, francés o español.

Los cheques se han diseñado para imprimir formatos de imágenes de cheque de Estados Unidos y Canadá en un formato cheque-matriz-cheque o en un formato matriz-matriz-cheque.

## <a name="to-define-check-layouts"></a>Para definir diseños de cheque
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Selección informes banco** y, a continuación, seleccione el vínculo relacionado.
2. En la ventana **Informe selección - Bancos**, en el campo **Uso**, seleccione **Cheque**.
3. Seleccione uno de los identificadores de informes siguientes:

| Id. informe | Nombre informe | Descripción |
| --- | --- | --- |
| 1401 |Activar |Es el informe predeterminado. |
| 10401 |Cheque (Matriz/Matriz/Cheque) |Este informe está diseñado para imprimir cheques en un formato matriz/matriz/cheque. |
| 10411 |Cheque (Matriz/Cheque/Matriz) |Este informe está diseñado para imprimir cheques en un formato cheque/matriz/cheque. |

Cuando haya configurado los diseños de cheques, puede imprimir cheques desde la ventana **Diario de pagos**. Para obtener más información, consulte [Trabajar con cheques](payables-how-work-checks.md).

## <a name="see-also"></a>Consulte también
[Administrar pagos](payables-manage-payables.md)  
[Administrar cuentas bancarias](bank-manage-bank-accounts.md)   
[Completar procesos de fin de periodo](year-how-complete-period-end-processes.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Funciones empresariales generales](ui-across-business-areas.md)

