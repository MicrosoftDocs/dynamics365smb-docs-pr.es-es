---
title: 'Detalles de diseño: Gestión de dimensiones de codeunit 408 | Documentos de Microsoft'
description: La gestión de dimensiones de la codeunit 408 corresponde a una biblioteca de funciones que controla tareas comunes relacionadas con las dimensiones, como copiar desde una tabla a otra o desde un documento a otro.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 95d4afc18b0be620df2f4b2067a093237c7c4df2
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/08/2019
ms.locfileid: "805347"
---
# <a name="design-details-codeunit-408-dimension-management"></a>Detalles de diseño: Gestión de dimensiones de codeunit 408
La gestión de dimensiones de la codeunit 408 corresponde a una biblioteca de funciones que controla tareas comunes relacionadas con las dimensiones, como copiar desde una tabla a otra o desde un documento a otro. En este tema se enumeran las funciones que se han modificado en Microsoft Dynamics NAV 2013 R2 y se especifica qué se tiene que hacer en las funciones. Muchas funciones se eliminan porque no es necesario realizar la copia entre tablas de dimensiones.  

## <a name="modified-functions"></a>Funciones modificadas  

|Nombre de función|Descripción de la modificación|  
|-------------------|------------------------------|  
|CheckDimSetIDComb|Nueva función que sustituye a otras funciones de comprobación y acepta un identificador de grupo de dimensiones como argumento en lugar de una tabla de dimensiones.|  
|CheckDimSetIDComb<br /><br /> CheckDocDimComb<br /><br /> CheckServContractDimComb<br /><br /> CheckDimBuffer<br /><br /> CheckDimComb<br /><br /> CheckDimValueComb|Eliminar. Todo el uso debe cambiar a CheckDimSetIDComb.|  
|GetDefaultDim|Modificar para devolver un identificador entero de grupo de dimensiones en vez de un conjunto de registros.|  
|CopyJnlLineDimToICJnlDim<br /><br /> CopyICJnlDimToJnlLineDim<br /><br /> CopyDocDimtoICDocDim<br /><br /> CopyICDocDimtoICDocDim|Modificar para trabajar con DimSetID - > ICJnlLineDim|  

## <a name="deleted-functions"></a>Funciones eliminadas  
 Las funciones que se han eliminado de la codeunit 408 en relación con los movimientos de grupo de dimensiones se presentan a continuación.  

> [!CAUTION]  
>  Durante la actualización del código de aplicación desde Microsoft Dynamics NAV 2009 o versiones anteriores a Microsoft Dynamics NAV 2016, las funciones siguientes no están disponibles en Microsoft Dynamics NAV 2016. Si tiene personalizaciones que utilizan una o varias de las funciones, debe actualizar ese código según corresponda.

 InsertJnlLineDim  

 UpdateJnlLineDefaultDim  

 GetJnlLineDefaultDim  

 GetPreviousDocDefaultDim  

 GetPreviousProdDocDefaultDim  

 InsertDocDim  

 UpdateDocDefaultDim  

 ExtractDocDefaultDim  

 InsertProdDocDim  

 UpdateProdDocDefaultDim  

 InsertServContractDim  

 UpdateServcontractDim  

 UpdateDefaultDimNewDimValue  

 GetDocDim  

 GetProdDocDim  

 TypeToTableID1  

 TypeToTableID2  

 TypeToTableID3  

 TypeToTableID4  

 TypeToTableID5  

 DeleteJnlLineDim  

 DeleteDocDim  

 DeletePostedDocDim  

 DeleteProdDocDim  

 DeleteServContractDim  

 ShowJnlLineDim  

 SaveJnlLineDim  

 ShowJnlLineNewDim  

 SaveJnlLineNewDim  

 ShowDocDim  

 SaveDocDim  

 ShowProdDocDim  

 SaveProdDocDim  

 ShowTempDim  

 SaveTempDim  

 ShowTempNewDim  

 SaveTempNewDim  

 SaveServContractDim  

 MoveJnlLineDimToLedgEntryDim  

 MoveDocDimToPostedDocDim  

 MoveOneDocDimToPostedDocDim  

 MoveLedgEntryDimToJnlLineDim  

 MoveDimBufToJnlLineDim  

 MoveDimBufToLedgEntryDim  

 MoveDimBufToPostedDocDim  

 MoveDimBufToGLBudgetDim  

 CopyJnlLineDimToJnlLineDim  

 CopyLedgEntryDimToJnlLineDim  

 CopyDocDimToDocDim  

 CopyPostedDocDimToPostedDocDim  

 CopyDocDimToJnlLineDim  

 CopyDimBufToJnlLineDim  

 CopyDimBufToDocDim  

 CopySCDimToDocDim  

 MoveDocDimToLedgEntryDim  

 MoveDocDimToDocDim  

 MoveDocDimArchvToDocDim  

 MoveLedgEntryDimToDocDim  

 MoveProdDocDimToProdDocDim  

 MoveJnlLineDimToProdDocDim  

 MoveJnlLineDimToDocDim  

 MoveJnlLineDimToJnlLineDim  

 CopyLedgEntryDimToLedgEntryDim  

 MoveTempFromDimToTempToDim  

 TransferTempToDimToDocDim  

 MoveJnlLineDimToBuf  

 CopyICJnlDimToICJnlDim  

 TestDimValue  

 TestNewDimValue  

 MoveDimBufToItemBudgetDim. (Eliminar porque se elimina la tabla ItemBudgetDim).  

 GetServContractDim  

 MoveTempDimToBuf  

 UpdateSCInvLineDim  

 CopyJnlLineDimToBuffer  

 UpdateDocDefaultDim2  

## <a name="see-also"></a>Consulte también
 [Detalles de diseño: Movimientos de grupo de dimensiones](design-details-dimension-set-entries.md)   
 [Detalles de diseño: Resumen de Movimientos de grupo de dimensiones](design-details-dimension-set-entries-overview.md)   
 [Detalles de diseño: Búsqueda de combinaciones de dimensiones](design-details-searching-for-dimension-combinations.md)   
 [Detalles de diseño: Estructura de tablas](design-details-table-structure.md)   
 [Detalles de diseño: Ejemplos de código de patrones cambiados en las modificaciones](design-details-code-examples-of-changed-patterns-in-modifications.md)
