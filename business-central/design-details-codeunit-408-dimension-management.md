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
# <a name="design-details-codeunit-408-dimension-management"></a><span data-ttu-id="ef042-103">Detalles de diseño: Gestión de dimensiones de codeunit 408</span><span class="sxs-lookup"><span data-stu-id="ef042-103">Design Details: Codeunit 408 Dimension Management</span></span>
<span data-ttu-id="ef042-104">La gestión de dimensiones de la codeunit 408 corresponde a una biblioteca de funciones que controla tareas comunes relacionadas con las dimensiones, como copiar desde una tabla a otra o desde un documento a otro.</span><span class="sxs-lookup"><span data-stu-id="ef042-104">Codeunit 408 Dimension Management is a function library that handles common tasks that are related to dimensions, such as copying from one table to another or from one document to another.</span></span> <span data-ttu-id="ef042-105">En este tema se enumeran las funciones que se han modificado en Microsoft Dynamics NAV 2013 R2 y se especifica qué se tiene que hacer en las funciones.</span><span class="sxs-lookup"><span data-stu-id="ef042-105">This topic lists the functions that are modified in Microsoft Dynamics NAV 2013 R2 and specifies what has to be done to the functions.</span></span> <span data-ttu-id="ef042-106">Muchas funciones se eliminan porque no es necesario realizar la copia entre tablas de dimensiones.</span><span class="sxs-lookup"><span data-stu-id="ef042-106">Many functions are deleted because there is no need for copying between dimension tables.</span></span>  

## <a name="modified-functions"></a><span data-ttu-id="ef042-107">Funciones modificadas</span><span class="sxs-lookup"><span data-stu-id="ef042-107">Modified Functions</span></span>  

|<span data-ttu-id="ef042-108">Nombre de función</span><span class="sxs-lookup"><span data-stu-id="ef042-108">Function Name</span></span>|<span data-ttu-id="ef042-109">Descripción de la modificación</span><span class="sxs-lookup"><span data-stu-id="ef042-109">Modification Description</span></span>|  
|-------------------|------------------------------|  
|<span data-ttu-id="ef042-110">CheckDimSetIDComb</span><span class="sxs-lookup"><span data-stu-id="ef042-110">CheckDimSetIDComb</span></span>|<span data-ttu-id="ef042-111">Nueva función que sustituye a otras funciones de comprobación y acepta un identificador de grupo de dimensiones como argumento en lugar de una tabla de dimensiones.</span><span class="sxs-lookup"><span data-stu-id="ef042-111">New function that substitutes the other check functions and takes a Dimension Set ID as an argument instead of a dimension table.</span></span>|  
|<span data-ttu-id="ef042-112">CheckDimSetIDComb</span><span class="sxs-lookup"><span data-stu-id="ef042-112">CheckDimSetIDComb</span></span><br /><br /> <span data-ttu-id="ef042-113">CheckDocDimComb</span><span class="sxs-lookup"><span data-stu-id="ef042-113">CheckDocDimComb</span></span><br /><br /> <span data-ttu-id="ef042-114">CheckServContractDimComb</span><span class="sxs-lookup"><span data-stu-id="ef042-114">CheckServContractDimComb</span></span><br /><br /> <span data-ttu-id="ef042-115">CheckDimBuffer</span><span class="sxs-lookup"><span data-stu-id="ef042-115">CheckDimBuffer</span></span><br /><br /> <span data-ttu-id="ef042-116">CheckDimComb</span><span class="sxs-lookup"><span data-stu-id="ef042-116">CheckDimComb</span></span><br /><br /> <span data-ttu-id="ef042-117">CheckDimValueComb</span><span class="sxs-lookup"><span data-stu-id="ef042-117">CheckDimValueComb</span></span>|<span data-ttu-id="ef042-118">Eliminar.</span><span class="sxs-lookup"><span data-stu-id="ef042-118">Delete.</span></span> <span data-ttu-id="ef042-119">Todo el uso debe cambiar a CheckDimSetIDComb.</span><span class="sxs-lookup"><span data-stu-id="ef042-119">All usage should be changed to CheckDimSetIDComb.</span></span>|  
|<span data-ttu-id="ef042-120">GetDefaultDim</span><span class="sxs-lookup"><span data-stu-id="ef042-120">GetDefaultDim</span></span>|<span data-ttu-id="ef042-121">Modificar para devolver un identificador entero de grupo de dimensiones en vez de un conjunto de registros.</span><span class="sxs-lookup"><span data-stu-id="ef042-121">Modify to return an integer Dimension Set ID instead of a set of records.</span></span>|  
|<span data-ttu-id="ef042-122">CopyJnlLineDimToICJnlDim</span><span class="sxs-lookup"><span data-stu-id="ef042-122">CopyJnlLineDimToICJnlDim</span></span><br /><br /> <span data-ttu-id="ef042-123">CopyICJnlDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="ef042-123">CopyICJnlDimToJnlLineDim</span></span><br /><br /> <span data-ttu-id="ef042-124">CopyDocDimtoICDocDim</span><span class="sxs-lookup"><span data-stu-id="ef042-124">CopyDocDimtoICDocDim</span></span><br /><br /> <span data-ttu-id="ef042-125">CopyICDocDimtoICDocDim</span><span class="sxs-lookup"><span data-stu-id="ef042-125">CopyICDocDimtoICDocDim</span></span>|<span data-ttu-id="ef042-126">Modificar para trabajar con DimSetID - > ICJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="ef042-126">Modify to work with DimSetID -> ICJnlLineDim</span></span>|  

## <a name="deleted-functions"></a><span data-ttu-id="ef042-127">Funciones eliminadas</span><span class="sxs-lookup"><span data-stu-id="ef042-127">Deleted Functions</span></span>  
 <span data-ttu-id="ef042-128">Las funciones que se han eliminado de la codeunit 408 en relación con los movimientos de grupo de dimensiones se presentan a continuación.</span><span class="sxs-lookup"><span data-stu-id="ef042-128">Functions that are deleted from codeunit 408 in connection with the Dimension Set Entries feature are listed below.</span></span>  

> [!CAUTION]  
>  <span data-ttu-id="ef042-129">Durante la actualización del código de aplicación desde Microsoft Dynamics NAV 2009 o versiones anteriores a Microsoft Dynamics NAV 2016, las funciones siguientes no están disponibles en Microsoft Dynamics NAV 2016.</span><span class="sxs-lookup"><span data-stu-id="ef042-129">During the upgrade of application code from Microsoft Dynamics NAV 2009 or earlier versions to Microsoft Dynamics NAV 2016, the following functions are not available in Microsoft Dynamics NAV 2016.</span></span> <span data-ttu-id="ef042-130">Si tiene personalizaciones que utilizan una o varias de las funciones, debe actualizar ese código según corresponda.</span><span class="sxs-lookup"><span data-stu-id="ef042-130">If you have customizations that use one or more of the functions, you must upgrade that code accordingly.</span></span>

 <span data-ttu-id="ef042-131">InsertJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="ef042-131">InsertJnlLineDim</span></span>  

 <span data-ttu-id="ef042-132">UpdateJnlLineDefaultDim</span><span class="sxs-lookup"><span data-stu-id="ef042-132">UpdateJnlLineDefaultDim</span></span>  

 <span data-ttu-id="ef042-133">GetJnlLineDefaultDim</span><span class="sxs-lookup"><span data-stu-id="ef042-133">GetJnlLineDefaultDim</span></span>  

 <span data-ttu-id="ef042-134">GetPreviousDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="ef042-134">GetPreviousDocDefaultDim</span></span>  

 <span data-ttu-id="ef042-135">GetPreviousProdDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="ef042-135">GetPreviousProdDocDefaultDim</span></span>  

 <span data-ttu-id="ef042-136">InsertDocDim</span><span class="sxs-lookup"><span data-stu-id="ef042-136">InsertDocDim</span></span>  

 <span data-ttu-id="ef042-137">UpdateDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="ef042-137">UpdateDocDefaultDim</span></span>  

 <span data-ttu-id="ef042-138">ExtractDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="ef042-138">ExtractDocDefaultDim</span></span>  

 <span data-ttu-id="ef042-139">InsertProdDocDim</span><span class="sxs-lookup"><span data-stu-id="ef042-139">InsertProdDocDim</span></span>  

 <span data-ttu-id="ef042-140">UpdateProdDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="ef042-140">UpdateProdDocDefaultDim</span></span>  

 <span data-ttu-id="ef042-141">InsertServContractDim</span><span class="sxs-lookup"><span data-stu-id="ef042-141">InsertServContractDim</span></span>  

 <span data-ttu-id="ef042-142">UpdateServcontractDim</span><span class="sxs-lookup"><span data-stu-id="ef042-142">UpdateServcontractDim</span></span>  

 <span data-ttu-id="ef042-143">UpdateDefaultDimNewDimValue</span><span class="sxs-lookup"><span data-stu-id="ef042-143">UpdateDefaultDimNewDimValue</span></span>  

 <span data-ttu-id="ef042-144">GetDocDim</span><span class="sxs-lookup"><span data-stu-id="ef042-144">GetDocDim</span></span>  

 <span data-ttu-id="ef042-145">GetProdDocDim</span><span class="sxs-lookup"><span data-stu-id="ef042-145">GetProdDocDim</span></span>  

 <span data-ttu-id="ef042-146">TypeToTableID1</span><span class="sxs-lookup"><span data-stu-id="ef042-146">TypeToTableID1</span></span>  

 <span data-ttu-id="ef042-147">TypeToTableID2</span><span class="sxs-lookup"><span data-stu-id="ef042-147">TypeToTableID2</span></span>  

 <span data-ttu-id="ef042-148">TypeToTableID3</span><span class="sxs-lookup"><span data-stu-id="ef042-148">TypeToTableID3</span></span>  

 <span data-ttu-id="ef042-149">TypeToTableID4</span><span class="sxs-lookup"><span data-stu-id="ef042-149">TypeToTableID4</span></span>  

 <span data-ttu-id="ef042-150">TypeToTableID5</span><span class="sxs-lookup"><span data-stu-id="ef042-150">TypeToTableID5</span></span>  

 <span data-ttu-id="ef042-151">DeleteJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="ef042-151">DeleteJnlLineDim</span></span>  

 <span data-ttu-id="ef042-152">DeleteDocDim</span><span class="sxs-lookup"><span data-stu-id="ef042-152">DeleteDocDim</span></span>  

 <span data-ttu-id="ef042-153">DeletePostedDocDim</span><span class="sxs-lookup"><span data-stu-id="ef042-153">DeletePostedDocDim</span></span>  

 <span data-ttu-id="ef042-154">DeleteProdDocDim</span><span class="sxs-lookup"><span data-stu-id="ef042-154">DeleteProdDocDim</span></span>  

 <span data-ttu-id="ef042-155">DeleteServContractDim</span><span class="sxs-lookup"><span data-stu-id="ef042-155">DeleteServContractDim</span></span>  

 <span data-ttu-id="ef042-156">ShowJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="ef042-156">ShowJnlLineDim</span></span>  

 <span data-ttu-id="ef042-157">SaveJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="ef042-157">SaveJnlLineDim</span></span>  

 <span data-ttu-id="ef042-158">ShowJnlLineNewDim</span><span class="sxs-lookup"><span data-stu-id="ef042-158">ShowJnlLineNewDim</span></span>  

 <span data-ttu-id="ef042-159">SaveJnlLineNewDim</span><span class="sxs-lookup"><span data-stu-id="ef042-159">SaveJnlLineNewDim</span></span>  

 <span data-ttu-id="ef042-160">ShowDocDim</span><span class="sxs-lookup"><span data-stu-id="ef042-160">ShowDocDim</span></span>  

 <span data-ttu-id="ef042-161">SaveDocDim</span><span class="sxs-lookup"><span data-stu-id="ef042-161">SaveDocDim</span></span>  

 <span data-ttu-id="ef042-162">ShowProdDocDim</span><span class="sxs-lookup"><span data-stu-id="ef042-162">ShowProdDocDim</span></span>  

 <span data-ttu-id="ef042-163">SaveProdDocDim</span><span class="sxs-lookup"><span data-stu-id="ef042-163">SaveProdDocDim</span></span>  

 <span data-ttu-id="ef042-164">ShowTempDim</span><span class="sxs-lookup"><span data-stu-id="ef042-164">ShowTempDim</span></span>  

 <span data-ttu-id="ef042-165">SaveTempDim</span><span class="sxs-lookup"><span data-stu-id="ef042-165">SaveTempDim</span></span>  

 <span data-ttu-id="ef042-166">ShowTempNewDim</span><span class="sxs-lookup"><span data-stu-id="ef042-166">ShowTempNewDim</span></span>  

 <span data-ttu-id="ef042-167">SaveTempNewDim</span><span class="sxs-lookup"><span data-stu-id="ef042-167">SaveTempNewDim</span></span>  

 <span data-ttu-id="ef042-168">SaveServContractDim</span><span class="sxs-lookup"><span data-stu-id="ef042-168">SaveServContractDim</span></span>  

 <span data-ttu-id="ef042-169">MoveJnlLineDimToLedgEntryDim</span><span class="sxs-lookup"><span data-stu-id="ef042-169">MoveJnlLineDimToLedgEntryDim</span></span>  

 <span data-ttu-id="ef042-170">MoveDocDimToPostedDocDim</span><span class="sxs-lookup"><span data-stu-id="ef042-170">MoveDocDimToPostedDocDim</span></span>  

 <span data-ttu-id="ef042-171">MoveOneDocDimToPostedDocDim</span><span class="sxs-lookup"><span data-stu-id="ef042-171">MoveOneDocDimToPostedDocDim</span></span>  

 <span data-ttu-id="ef042-172">MoveLedgEntryDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="ef042-172">MoveLedgEntryDimToJnlLineDim</span></span>  

 <span data-ttu-id="ef042-173">MoveDimBufToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="ef042-173">MoveDimBufToJnlLineDim</span></span>  

 <span data-ttu-id="ef042-174">MoveDimBufToLedgEntryDim</span><span class="sxs-lookup"><span data-stu-id="ef042-174">MoveDimBufToLedgEntryDim</span></span>  

 <span data-ttu-id="ef042-175">MoveDimBufToPostedDocDim</span><span class="sxs-lookup"><span data-stu-id="ef042-175">MoveDimBufToPostedDocDim</span></span>  

 <span data-ttu-id="ef042-176">MoveDimBufToGLBudgetDim</span><span class="sxs-lookup"><span data-stu-id="ef042-176">MoveDimBufToGLBudgetDim</span></span>  

 <span data-ttu-id="ef042-177">CopyJnlLineDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="ef042-177">CopyJnlLineDimToJnlLineDim</span></span>  

 <span data-ttu-id="ef042-178">CopyLedgEntryDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="ef042-178">CopyLedgEntryDimToJnlLineDim</span></span>  

 <span data-ttu-id="ef042-179">CopyDocDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="ef042-179">CopyDocDimToDocDim</span></span>  

 <span data-ttu-id="ef042-180">CopyPostedDocDimToPostedDocDim</span><span class="sxs-lookup"><span data-stu-id="ef042-180">CopyPostedDocDimToPostedDocDim</span></span>  

 <span data-ttu-id="ef042-181">CopyDocDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="ef042-181">CopyDocDimToJnlLineDim</span></span>  

 <span data-ttu-id="ef042-182">CopyDimBufToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="ef042-182">CopyDimBufToJnlLineDim</span></span>  

 <span data-ttu-id="ef042-183">CopyDimBufToDocDim</span><span class="sxs-lookup"><span data-stu-id="ef042-183">CopyDimBufToDocDim</span></span>  

 <span data-ttu-id="ef042-184">CopySCDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="ef042-184">CopySCDimToDocDim</span></span>  

 <span data-ttu-id="ef042-185">MoveDocDimToLedgEntryDim</span><span class="sxs-lookup"><span data-stu-id="ef042-185">MoveDocDimToLedgEntryDim</span></span>  

 <span data-ttu-id="ef042-186">MoveDocDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="ef042-186">MoveDocDimToDocDim</span></span>  

 <span data-ttu-id="ef042-187">MoveDocDimArchvToDocDim</span><span class="sxs-lookup"><span data-stu-id="ef042-187">MoveDocDimArchvToDocDim</span></span>  

 <span data-ttu-id="ef042-188">MoveLedgEntryDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="ef042-188">MoveLedgEntryDimToDocDim</span></span>  

 <span data-ttu-id="ef042-189">MoveProdDocDimToProdDocDim</span><span class="sxs-lookup"><span data-stu-id="ef042-189">MoveProdDocDimToProdDocDim</span></span>  

 <span data-ttu-id="ef042-190">MoveJnlLineDimToProdDocDim</span><span class="sxs-lookup"><span data-stu-id="ef042-190">MoveJnlLineDimToProdDocDim</span></span>  

 <span data-ttu-id="ef042-191">MoveJnlLineDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="ef042-191">MoveJnlLineDimToDocDim</span></span>  

 <span data-ttu-id="ef042-192">MoveJnlLineDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="ef042-192">MoveJnlLineDimToJnlLineDim</span></span>  

 <span data-ttu-id="ef042-193">CopyLedgEntryDimToLedgEntryDim</span><span class="sxs-lookup"><span data-stu-id="ef042-193">CopyLedgEntryDimToLedgEntryDim</span></span>  

 <span data-ttu-id="ef042-194">MoveTempFromDimToTempToDim</span><span class="sxs-lookup"><span data-stu-id="ef042-194">MoveTempFromDimToTempToDim</span></span>  

 <span data-ttu-id="ef042-195">TransferTempToDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="ef042-195">TransferTempToDimToDocDim</span></span>  

 <span data-ttu-id="ef042-196">MoveJnlLineDimToBuf</span><span class="sxs-lookup"><span data-stu-id="ef042-196">MoveJnlLineDimToBuf</span></span>  

 <span data-ttu-id="ef042-197">CopyICJnlDimToICJnlDim</span><span class="sxs-lookup"><span data-stu-id="ef042-197">CopyICJnlDimToICJnlDim</span></span>  

 <span data-ttu-id="ef042-198">TestDimValue</span><span class="sxs-lookup"><span data-stu-id="ef042-198">TestDimValue</span></span>  

 <span data-ttu-id="ef042-199">TestNewDimValue</span><span class="sxs-lookup"><span data-stu-id="ef042-199">TestNewDimValue</span></span>  

 <span data-ttu-id="ef042-200">MoveDimBufToItemBudgetDim.</span><span class="sxs-lookup"><span data-stu-id="ef042-200">MoveDimBufToItemBudgetDim.</span></span> <span data-ttu-id="ef042-201">(Eliminar porque se elimina la tabla ItemBudgetDim).</span><span class="sxs-lookup"><span data-stu-id="ef042-201">(Delete because the ItemBudgetDim Table is deleted.)</span></span>  

 <span data-ttu-id="ef042-202">GetServContractDim</span><span class="sxs-lookup"><span data-stu-id="ef042-202">GetServContractDim</span></span>  

 <span data-ttu-id="ef042-203">MoveTempDimToBuf</span><span class="sxs-lookup"><span data-stu-id="ef042-203">MoveTempDimToBuf</span></span>  

 <span data-ttu-id="ef042-204">UpdateSCInvLineDim</span><span class="sxs-lookup"><span data-stu-id="ef042-204">UpdateSCInvLineDim</span></span>  

 <span data-ttu-id="ef042-205">CopyJnlLineDimToBuffer</span><span class="sxs-lookup"><span data-stu-id="ef042-205">CopyJnlLineDimToBuffer</span></span>  

 <span data-ttu-id="ef042-206">UpdateDocDefaultDim2</span><span class="sxs-lookup"><span data-stu-id="ef042-206">UpdateDocDefaultDim2</span></span>  

## <a name="see-also"></a><span data-ttu-id="ef042-207">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ef042-207">See Also</span></span>
 <span data-ttu-id="ef042-208">[Detalles de diseño: Movimientos de grupo de dimensiones](design-details-dimension-set-entries.md) </span><span class="sxs-lookup"><span data-stu-id="ef042-208">[Design Details: Dimension Set Entries](design-details-dimension-set-entries.md) </span></span>  
 <span data-ttu-id="ef042-209">[Detalles de diseño: Resumen de Movimientos de grupo de dimensiones](design-details-dimension-set-entries-overview.md) </span><span class="sxs-lookup"><span data-stu-id="ef042-209">[Design Details: Dimension Set Entries Overview](design-details-dimension-set-entries-overview.md) </span></span>  
 <span data-ttu-id="ef042-210">[Detalles de diseño: Búsqueda de combinaciones de dimensiones](design-details-searching-for-dimension-combinations.md) </span><span class="sxs-lookup"><span data-stu-id="ef042-210">[Design Details: Searching for Dimension Combinations](design-details-searching-for-dimension-combinations.md) </span></span>  
 <span data-ttu-id="ef042-211">[Detalles de diseño: Estructura de tablas](design-details-table-structure.md) </span><span class="sxs-lookup"><span data-stu-id="ef042-211">[Design Details: Table Structure](design-details-table-structure.md) </span></span>  
 [<span data-ttu-id="ef042-212">Detalles de diseño: Ejemplos de código de patrones cambiados en las modificaciones</span><span class="sxs-lookup"><span data-stu-id="ef042-212">Design Details: Code Examples of Changed Patterns in Modifications</span></span>](design-details-code-examples-of-changed-patterns-in-modifications.md)
