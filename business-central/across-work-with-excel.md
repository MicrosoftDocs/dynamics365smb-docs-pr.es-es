---
title: Ver y editar en Excel desde Business Central | Documentos de Microsoft
description: Obtenga más información sobre cómo puede abrir las páginas en Microsoft Excel desde Business Central para un mejor análisis de datos.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 10/01/2019
ms.author: jswymer
ms.openlocfilehash: 2474f83fd9fa137b40756a3d07ac025208f3ac6c
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2019
ms.locfileid: "2308265"
---
# <a name="viewing-and-editing-in-excel-from-business-central"></a><span data-ttu-id="597a4-103">Ver y editar en Excel desde Business Central</span><span class="sxs-lookup"><span data-stu-id="597a4-103">Viewing and Editing in Excel From Business Central</span></span> 

<span data-ttu-id="597a4-104">Con las páginas que muestran una lista de registros en filas y columnas, como una lista de clientes, órdenes de venta o facturas, también puede ver los registros mediante Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="597a4-104">With pages that display a list of records in rows and columns, like a list of customers, sale orders, or invoices, you can also view the records using Microsoft Excel.</span></span> <span data-ttu-id="597a4-105">Para ello, tiene dos opciones.</span><span class="sxs-lookup"><span data-stu-id="597a4-105">To do this, you have two options.</span></span> <span data-ttu-id="597a4-106">Puede seleccionar la acción **Abrir en Excel** o la acción **Editar en Excel** en la página.</span><span class="sxs-lookup"><span data-stu-id="597a4-106">You can either select the **Open in Excel** action or the **Edit in Excel** action on the page.</span></span> <span data-ttu-id="597a4-107">Las diferencias entre las dos acciones son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="597a4-107">The differences between the two actions is as follows:</span></span>  

## <a name="open-in-excel"></a><span data-ttu-id="597a4-108">Abrir en Excel</span><span class="sxs-lookup"><span data-stu-id="597a4-108">Open in Excel</span></span>

-    <span data-ttu-id="597a4-109">Con esta acción, Excel respeta los filtros de la página y limita los registros que se muestran.</span><span class="sxs-lookup"><span data-stu-id="597a4-109">With this action, Excel respects any filters on the page the limit the records shown.</span></span> <span data-ttu-id="597a4-110">Esto significa que el libro de Excel contendrá las mismas filas y columnas que aparecen en la página de [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="597a4-110">This means that the Excel workbook will contain the same rows and columns that appear on the the page in [!INCLUDE[prodshort](includes/prodshort.md)].</span></span>

-    <span data-ttu-id="597a4-111">Puede realizar cambios en los registros en Excel, pero no puede volver a publicar los cambios en [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="597a4-111">You can make changes to the records in Excel, but you cannot publish the changes back to [!INCLUDE[prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="597a4-112">Solo puede guardar los cambios en el archivo de Excel en su ordenador.</span><span class="sxs-lookup"><span data-stu-id="597a4-112">You can only save the changes to Excel file on your computer.</span></span> 

-    <span data-ttu-id="597a4-113">Esta acción funciona tanto en Windows como en macOS.</span><span class="sxs-lookup"><span data-stu-id="597a4-113">This action works on both on Windows and macOS.</span></span> 

>[!NOTE]
><span data-ttu-id="597a4-114">Para [!INCLUDE[prodshort](includes/prodshort.md)] local, la acción **Abrir en Excel** no está disponible si se está usando la acción **Editar en Excel**.</span><span class="sxs-lookup"><span data-stu-id="597a4-114">For [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, the **Open in Excel** action is not available if the **Edit in Excel** action is.</span></span>

## <a name="edit-in-excel"></a><span data-ttu-id="597a4-115">Editar en Excel</span><span class="sxs-lookup"><span data-stu-id="597a4-115">Edit in Excel</span></span>

-    <span data-ttu-id="597a4-116">Con esta acción, el libro de Excel no respeta los filtros de la página y no limita los registros que se muestran.</span><span class="sxs-lookup"><span data-stu-id="597a4-116">With this action, the Excel workbook does not respect filters on the page the limit the records shown.</span></span> <span data-ttu-id="597a4-117">Esto significa que el libro de Excel contiene todos los registros y columnas disponibles, independientemente de lo que se muestra en la página.</span><span class="sxs-lookup"><span data-stu-id="597a4-117">This means that the Excel workbook will contain all the available records and columns, regardless of what is shown on the page.</span></span> 

-    <span data-ttu-id="597a4-118">La ventaja de la acción **Editar en Excel** es que le permite realizar cambios en los registros en Excel y luego publicarlos de nuevo en [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="597a4-118">The advantage of the **Edit in Excel** action is that it lets you make changes to records in Excel and then publish the changes back to [!INCLUDE[prodshort](includes/prodshort.md)].</span></span>

-    <span data-ttu-id="597a4-119">Solo funciona en Windows; en macOS, no.</span><span class="sxs-lookup"><span data-stu-id="597a4-119">It only works on Windows; not macOS.</span></span>

>[!NOTE]
><span data-ttu-id="597a4-120">Para [!INCLUDE[prodshort](includes/prodshort.md)] local, la acción **Editar en Excel** solo está disponible si el administrador ha instalado el complemento de Excel.</span><span class="sxs-lookup"><span data-stu-id="597a4-120">For [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, the **Edit in Excel** action is only available if the Excel add-in has been installed by your administrator.</span></span> <span data-ttu-id="597a4-121">Para los administradores: si desea aprender cómo instalar el complemento de Excel, consulte [Configuración del complemento de Excel](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span><span class="sxs-lookup"><span data-stu-id="597a4-121">For administrators, if you want to learn how to install the excel add-in, see [Setting up the Excel Add-In](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span></span>

### <a name="see-the-differences-between-the-options"></a><span data-ttu-id="597a4-122">Consulte las diferencias entre las opciones</span><span class="sxs-lookup"><span data-stu-id="597a4-122">See the differences between the options</span></span> 
> [!Video https://go.microsoft.com/fwlink/?linkid=2086039]

## <a name="see-also"></a><span data-ttu-id="597a4-123">Consulte también</span><span class="sxs-lookup"><span data-stu-id="597a4-123">See Also</span></span>
[<span data-ttu-id="597a4-124">Trabajar con Business Central</span><span class="sxs-lookup"><span data-stu-id="597a4-124">Working with Business Central</span></span>](ui-work-product.md)  
