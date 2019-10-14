---
title: Especificar el diseño de un cheque | Documentos de Microsoft
description: Puede diseñar e imprimir los cheques en diferentes formatos para cumplir los estándares.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, customize
ms.date: 10/01/2019
ms.author: edupont
ms.openlocfilehash: fea52bfa75d953b96aecc0f3e354806324f77d83
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2019
ms.locfileid: "2306321"
---
# <a name="select-a-check-layout"></a>Seleccionar una plantilla de cheques
Puede diseñar los cheques conforme a los estándares definidos por las autoridades locales. Las imágenes de los cheques se pueden imprimir en inglés, francés o español.

Los cheques se han diseñado para imprimir formatos de imágenes de cheque de Estados Unidos y Canadá en un formato cheque-matriz-cheque o en un formato matriz-matriz-cheque.

## <a name="to-select-a-check-layout"></a>Para seleccionar una plantilla de cheques
1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Selección informes banco** y luego elija el enlace relacionado.
2. En la página **Informe selección - Bancos**, en el campo **Uso**, seleccione **Cheque**.
3. Seleccione uno de los identificadores de informes siguientes:

| Id. informe | Nombre informe | Descripción |
| --- | --- | --- |
| 1401 |Activar |Es el informe predeterminado. |
| 10411 |Cheque (Matriz/Matriz/Cheque) |Este informe está diseñado para imprimir cheques en un formato matriz/matriz/cheque. |
| 10412 |Cheque (Matriz/Cheque/Matriz) |Este informe está diseñado para imprimir cheques en un formato matriz/cheque/matriz. |
| 10413 |Tres cheques por página |Este informe está diseñado para imprimir tres cheques por página. |

Cuando haya configurado los diseños de cheques, puede imprimir cheques desde la página **Diario de pagos**. Para obtener más información, consulte [Trabajar con cheques](payables-how-work-checks.md).

Para cambiar una de estas plantillas de cheques predeterminadas, utilice la integración de Word o RDLC. Para obtener más información, vea [Crear y modificar un diseño de informe o documento personalizado](ui-how-create-custom-report-layout.md).

## <a name="see-also"></a>Consulte también
[Crear y modificar un diseño de informe o documento personalizado](ui-how-create-custom-report-layout.md)  
[Administrar pagos](payables-manage-payables.md)  
[Administrar cuentas bancarias](bank-manage-bank-accounts.md)   
[Completar procesos de fin de periodo](year-how-complete-period-end-processes.md)  
[Trabajar con [!INCLUDE[prodshort](includes/prodshort.md)]](ui-work-product.md)  
[Funciones empresariales generales](ui-across-business-areas.md)
