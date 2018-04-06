---
title: "Impresión de informes Intrastat"
description: "Todas las empresas de la Unión Europea (UE) deben enviar un informe estadístico Intrastat al Instituto Nacional de Estadística (INE), en el que se detallen las relaciones comerciales con otros países y regiones de la UE."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 445a84b5bb63dcce93b47430e2f5476cf91cfb10
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="print-intrastat-reports"></a><span data-ttu-id="d12bf-103">Imprimir informes Intrastat</span><span class="sxs-lookup"><span data-stu-id="d12bf-103">Print Intrastat Reports</span></span>
<span data-ttu-id="d12bf-104">Todas las empresas de la Unión Europea (UE) deben enviar un informe estadístico Intrastat al Instituto Nacional de Estadística (INE), en el que se detallen las relaciones comerciales con otros países y regiones de la UE.</span><span class="sxs-lookup"><span data-stu-id="d12bf-104">All European Union (EU) companies must submit an Intrastat statistics report to the Instituto Nacional de Estatística (INE) detailing their trade with other EU countries/regions.</span></span> <span data-ttu-id="d12bf-105">La empresas no deben enviar las declaraciones estadísticas para el sistema Intrastat si sus totales de importación y exportación son inferiores al umbral que ha definido su país o región.</span><span class="sxs-lookup"><span data-stu-id="d12bf-105">Companies do not have to submit statistical declarations for the Intrastat system if their import and export totals are lower than the threshold set by their country/region.</span></span>  

<span data-ttu-id="d12bf-106">La información comercial requerida se puede imprimir y enviar en el formato de archivo que ha aprobado la administración fiscal.</span><span class="sxs-lookup"><span data-stu-id="d12bf-106">You can print and send required trade information in a file format approved by the tax authorities.</span></span>  

## <a name="to-print-an-intrastat-checklist"></a><span data-ttu-id="d12bf-107">Para imprimir un test de Intrastat</span><span class="sxs-lookup"><span data-stu-id="d12bf-107">To print an Intrastat checklist</span></span>  

1.  <span data-ttu-id="d12bf-108">Seleccione el icono ![Buscar página o informe](../../media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Diario Intrastat** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="d12bf-108">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Intrastat Journal**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="d12bf-109">Rellene los campos tal como se describe en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="d12bf-109">Fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="d12bf-110">Campo</span><span class="sxs-lookup"><span data-stu-id="d12bf-110">Field</span></span>|<span data-ttu-id="d12bf-111">Description</span><span class="sxs-lookup"><span data-stu-id="d12bf-111">Description</span></span>|  
    |------------------------------------|---------------------------------------|  
    |<span data-ttu-id="d12bf-112">**Nombre sección**</span><span class="sxs-lookup"><span data-stu-id="d12bf-112">**Batch Name**</span></span>|<span data-ttu-id="d12bf-113">El nombre de sección del diario requerido.</span><span class="sxs-lookup"><span data-stu-id="d12bf-113">The required journal batch name.</span></span>|  
    |<span data-ttu-id="d12bf-114">**Escriba**</span><span class="sxs-lookup"><span data-stu-id="d12bf-114">**Type**</span></span>|<span data-ttu-id="d12bf-115">Seleccione **Recepción** o **Envío**.</span><span class="sxs-lookup"><span data-stu-id="d12bf-115">Select **Receipt** or **Shipment**.</span></span>|  

3.  <span data-ttu-id="d12bf-116">Para obtener movimientos Intrastat, elija la acción **Traer movs**.</span><span class="sxs-lookup"><span data-stu-id="d12bf-116">To get Intrastat entries, choose the **Get Entries** action.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="d12bf-117">También se pueden realizar entradas manualmente en la ventana **Diario Intrastat**.</span><span class="sxs-lookup"><span data-stu-id="d12bf-117">You can also make entries manually in the **Intrastat Journal** window.</span></span>  

4.  <span data-ttu-id="d12bf-118">Seleccione la acción **Crear declaración**.</span><span class="sxs-lookup"><span data-stu-id="d12bf-118">Choose the **Make Declaration** action.</span></span>  
5.  <span data-ttu-id="d12bf-119">En el proceso**Intrastat - Decl. disquete**, amplíe la ficha desplegable **Sección diario Intrastat** y, a continuación, haga clic en los filtros apropiados.</span><span class="sxs-lookup"><span data-stu-id="d12bf-119">In the **Intrastat - Make Disk Tax Auth** batch job, expand the **Intrastat Jnl. Batch** FastTab, and then select the appropriate filters.</span></span>  
6.  <span data-ttu-id="d12bf-120">Amplíe la ficha desplegable **Lín. diario Intrastat**, seleccione los filtros apropiados y elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="d12bf-120">Expand the **Intrastat Jnl. Line** FastTab, select the appropriate filters, and then choose the **OK** button.</span></span>  

<span data-ttu-id="d12bf-121">La información Intrastat se exporta y puede guardar los datos en un archivo o abrir el archivo en el programa correspondiente.</span><span class="sxs-lookup"><span data-stu-id="d12bf-121">The Intrastat information is exported, and you can save the data to a file, or open the file in the appropriate program.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d12bf-122">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d12bf-122">See Also</span></span>  
[<span data-ttu-id="d12bf-123">Funcionalidad local para España</span><span class="sxs-lookup"><span data-stu-id="d12bf-123">Spain Local Functionality</span></span>](spain-local-functionality.md)

