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
ms.date: 10/24/2019
ms.author: jswymer
ms.openlocfilehash: 71b4e5b7124f929255f1374b38cfbe28c9f12d2b
ms.sourcegitcommit: c6e28db8f78fa21db064c9b8a8d742f49d7db3ae
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2019
ms.locfileid: "2692805"
---
# <a name="viewing-and-editing-in-excel-from-business-central"></a><span data-ttu-id="2f185-103">Ver y editar en Excel desde Business Central</span><span class="sxs-lookup"><span data-stu-id="2f185-103">Viewing and Editing in Excel From Business Central</span></span>

<span data-ttu-id="2f185-104">Con las páginas que muestran una lista de registros en filas y columnas, como una lista de clientes, órdenes de venta o facturas, también puede ver los registros mediante Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="2f185-104">With pages that display a list of records in rows and columns, like a list of customers, sale orders, or invoices, you can also view the records using Microsoft Excel.</span></span> <span data-ttu-id="2f185-105">Para ello, tiene dos opciones.</span><span class="sxs-lookup"><span data-stu-id="2f185-105">To do this, you have two options.</span></span> <span data-ttu-id="2f185-106">Puede seleccionar la acción **Abrir en Excel** o la acción **Editar en Excel** en la página.</span><span class="sxs-lookup"><span data-stu-id="2f185-106">You can either select the **Open in Excel** action or the **Edit in Excel** action on the page.</span></span> <span data-ttu-id="2f185-107">Las diferencias entre las dos acciones son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="2f185-107">The differences between the two actions is as follows:</span></span>  

## <a name="open-in-excel"></a><span data-ttu-id="2f185-108">Abrir en Excel</span><span class="sxs-lookup"><span data-stu-id="2f185-108">Open in Excel</span></span>

- <span data-ttu-id="2f185-109">Con esta acción, Excel respeta los filtros de la página que limita los registros que se muestran.</span><span class="sxs-lookup"><span data-stu-id="2f185-109">With this action, Excel respects any filters on the page that limit the records shown.</span></span> <span data-ttu-id="2f185-110">Esto significa que el libro de Excel contendrá las mismas filas y columnas que aparecen en la página de [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="2f185-110">This means that the Excel workbook will contain the same rows and columns that appear on the page in [!INCLUDE[prodshort](includes/prodshort.md)].</span></span>

- <span data-ttu-id="2f185-111">Puede realizar cambios en los registros en Excel, pero no puede volver a publicar los cambios en [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="2f185-111">You can make changes to the records in Excel, but you cannot publish the changes back to [!INCLUDE[prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="2f185-112">Solo puede guardar los cambios en el archivo de Excel en su ordenador.</span><span class="sxs-lookup"><span data-stu-id="2f185-112">You can only save the changes to Excel file on your computer.</span></span> 

- <span data-ttu-id="2f185-113">Esta acción funciona tanto en Windows como en macOS.</span><span class="sxs-lookup"><span data-stu-id="2f185-113">This action works on both on Windows and macOS.</span></span> 

> [!NOTE]
> <span data-ttu-id="2f185-114">Por [!INCLUDE[prodshort](includes/prodshort.md)] local, la acción **Abrir en Excel** está disponible de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="2f185-114">For [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, the **Open in Excel** action is available by default.</span></span> <span data-ttu-id="2f185-115">Sin embargo, si configura [!INCLUDE [prodshort](includes/prodshort.md)] local para editar datos en Excel, la acción **Abrir en Excel** se reemplaza por la acción **Editar en Excel**.</span><span class="sxs-lookup"><span data-stu-id="2f185-115">However, if you set up [!INCLUDE [prodshort](includes/prodshort.md)] on-premises for editing data in Excel, then the **Open in Excel** action is replaced by the **Edit in Excel** action.</span></span>

## <a name="edit-in-excel"></a><span data-ttu-id="2f185-116">Editar en Excel</span><span class="sxs-lookup"><span data-stu-id="2f185-116">Edit in Excel</span></span>

- <span data-ttu-id="2f185-117">Con esta acción, Excel respeta la mayoría de los filtros de la página que limitan los registros que se muestran.</span><span class="sxs-lookup"><span data-stu-id="2f185-117">With this action, Excel respects most filters on the page that limit the records shown.</span></span> <span data-ttu-id="2f185-118">Esto significa que el libro de Excel contendrá casi los mismos registros y columnas.</span><span class="sxs-lookup"><span data-stu-id="2f185-118">This means that the Excel workbook will contain almost the same records and columns.</span></span>

- <span data-ttu-id="2f185-119">La ventaja de la acción **Editar en Excel** es que le permite realizar cambios en los registros en Excel y luego publicarlos de nuevo en [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="2f185-119">The advantage of the **Edit in Excel** action is that it lets you make changes to records in Excel and then publish the changes back to [!INCLUDE[prodshort](includes/prodshort.md)].</span></span>

- <span data-ttu-id="2f185-120">Solo funciona en Windows; en macOS, no.</span><span class="sxs-lookup"><span data-stu-id="2f185-120">It only works on Windows; not macOS.</span></span>

<span data-ttu-id="2f185-121">Esto se mejoró en la fase de lanzamiento 2 de 2019.</span><span class="sxs-lookup"><span data-stu-id="2f185-121">This was enhanced in 2019 release wave 2.</span></span> <span data-ttu-id="2f185-122">Para obtener más información, vea [Mejoras en la integración de Excel](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration).</span><span class="sxs-lookup"><span data-stu-id="2f185-122">For more information, see [Enhancements to Excel integration](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration).</span></span>

> [!NOTE]
> <span data-ttu-id="2f185-123">Para [!INCLUDE[prodshort](includes/prodshort.md)] local, la acción **Editar en Excel** solo está disponible si el administrador ha configurado el complemento de Excel.</span><span class="sxs-lookup"><span data-stu-id="2f185-123">For [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, the **Edit in Excel** action is only available if the Excel add-in has been configured by your administrator.</span></span> <span data-ttu-id="2f185-124">Para los administradores: si desea aprender cómo instalar el complemento de Excel, consulte [Configuración del complemento de Excel para editar datos de Business Central](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span><span class="sxs-lookup"><span data-stu-id="2f185-124">For administrators, if you want to learn how to install the excel add-in, see [Setting up the Excel Add-In for Editing Business Central Data](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span></span>

> [!NOTE]
> <span data-ttu-id="2f185-125">Por [!INCLUDE[prodshort](includes/prodshort.md)] local, esta función solo está disponible para el cliente web.</span><span class="sxs-lookup"><span data-stu-id="2f185-125">For [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, this feature is only available for the Web client.</span></span>

### <a name="see-the-differences-between-the-options"></a><span data-ttu-id="2f185-126">Consulte las diferencias entre las opciones</span><span class="sxs-lookup"><span data-stu-id="2f185-126">See the differences between the options</span></span> 
> [!Video https://go.microsoft.com/fwlink/?linkid=2086039]

## <a name="see-also"></a><span data-ttu-id="2f185-127">Consulte también</span><span class="sxs-lookup"><span data-stu-id="2f185-127">See Also</span></span>
[<span data-ttu-id="2f185-128">Trabajar con Business Central</span><span class="sxs-lookup"><span data-stu-id="2f185-128">Working with Business Central</span></span>](ui-work-product.md)  
