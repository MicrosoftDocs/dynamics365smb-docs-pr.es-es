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
ms.date: 04/01/2020
ms.author: jswymer
ms.openlocfilehash: 2c6600ac7fe9f6e0aa44554883209039faabbd99
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/01/2020
ms.locfileid: "3187513"
---
# <a name="viewing-and-editing-in-excel-from-business-central"></a><span data-ttu-id="045d6-103">Ver y editar en Excel desde Business Central</span><span class="sxs-lookup"><span data-stu-id="045d6-103">Viewing and Editing in Excel From Business Central</span></span>

<span data-ttu-id="045d6-104">Con las páginas que muestran una lista de registros en filas y columnas, como una lista de clientes, órdenes de venta o facturas, también puede ver los registros mediante Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="045d6-104">With pages that display a list of records in rows and columns, like a list of customers, sale orders, or invoices, you can also view the records using Microsoft Excel.</span></span> <span data-ttu-id="045d6-105">Para ello, tiene dos opciones.</span><span class="sxs-lookup"><span data-stu-id="045d6-105">To do this, you have two options.</span></span> <span data-ttu-id="045d6-106">Puede seleccionar la acción **Abrir en Excel** o la acción **Editar en Excel** en la página.</span><span class="sxs-lookup"><span data-stu-id="045d6-106">You can either select the **Open in Excel** action or the **Edit in Excel** action on the page.</span></span> <span data-ttu-id="045d6-107">Las diferencias entre las dos acciones son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="045d6-107">The differences between the two actions is as follows:</span></span>  

## <a name="open-in-excel"></a><span data-ttu-id="045d6-108">Abrir en Excel</span><span class="sxs-lookup"><span data-stu-id="045d6-108">Open in Excel</span></span>

- <span data-ttu-id="045d6-109">Con esta acción, Excel respeta los filtros de la página que limita los registros que se muestran.</span><span class="sxs-lookup"><span data-stu-id="045d6-109">With this action, Excel respects any filters on the page that limit the records shown.</span></span> <span data-ttu-id="045d6-110">Esto significa que el libro de Excel contendrá las mismas filas y columnas que aparecen en la página de [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="045d6-110">This means that the Excel workbook will contain the same rows and columns that appear on the page in [!INCLUDE[prodshort](includes/prodshort.md)].</span></span>

- <span data-ttu-id="045d6-111">Puede realizar cambios en los registros en Excel, pero no puede volver a publicar los cambios en [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="045d6-111">You can make changes to the records in Excel, but you cannot publish the changes back to [!INCLUDE[prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="045d6-112">Solo puede guardar los cambios en el archivo de Excel en su ordenador.</span><span class="sxs-lookup"><span data-stu-id="045d6-112">You can only save the changes to Excel file on your computer.</span></span>

- <span data-ttu-id="045d6-113">Esta acción funciona tanto en Windows como en macOS.</span><span class="sxs-lookup"><span data-stu-id="045d6-113">This action works on both on Windows and macOS.</span></span>

> [!NOTE]
> <span data-ttu-id="045d6-114">Por [!INCLUDE[prodshort](includes/prodshort.md)] local, la acción **Abrir en Excel** está disponible de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="045d6-114">For [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, the **Open in Excel** action is available by default.</span></span> <span data-ttu-id="045d6-115">Sin embargo, si configura [!INCLUDE [prodshort](includes/prodshort.md)] local para editar datos en Excel, la acción **Abrir en Excel** se reemplaza por la acción **Editar en Excel**.</span><span class="sxs-lookup"><span data-stu-id="045d6-115">However, if you set up [!INCLUDE [prodshort](includes/prodshort.md)] on-premises for editing data in Excel, then the **Open in Excel** action is replaced by the **Edit in Excel** action.</span></span>

## <a name="edit-in-excel"></a><span data-ttu-id="045d6-116">Editar en Excel</span><span class="sxs-lookup"><span data-stu-id="045d6-116">Edit in Excel</span></span>

- <span data-ttu-id="045d6-117">Con esta acción, Excel respeta la mayoría de los filtros de la página que limitan los registros que se muestran.</span><span class="sxs-lookup"><span data-stu-id="045d6-117">With this action, Excel respects most filters on the page that limit the records shown.</span></span> <span data-ttu-id="045d6-118">Esto significa que el libro de Excel contendrá casi los mismos registros y columnas.</span><span class="sxs-lookup"><span data-stu-id="045d6-118">This means that the Excel workbook will contain almost the same records and columns.</span></span>

- <span data-ttu-id="045d6-119">La ventaja de la acción **Editar en Excel** es que le permite realizar cambios en los registros en Excel y luego publicarlos de nuevo en [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="045d6-119">The advantage of the **Edit in Excel** action is that it lets you make changes to records in Excel and then publish the changes back to [!INCLUDE[prodshort](includes/prodshort.md)].</span></span>

- <span data-ttu-id="045d6-120">Solo funciona en Windows; en macOS, no.</span><span class="sxs-lookup"><span data-stu-id="045d6-120">It only works on Windows; not macOS.</span></span>

- <span data-ttu-id="045d6-121">Puede cambiar la compañía con la que está trabajando.</span><span class="sxs-lookup"><span data-stu-id="045d6-121">You can switch the company that your are working with.</span></span> <span data-ttu-id="045d6-122">Para hacerlo, seleccione el icono **Opciones** ![Opciones de complemento de Excel](media/cogwheel.png "Opciones del complemento de Excel") en el panel Complemento de Excel y luego seleccione la compañía en el campo **Empresa**.</span><span class="sxs-lookup"><span data-stu-id="045d6-122">To do this, select the **Options** icon ![Excel add-in options](media/cogwheel.png "Excel add-in options") in the Excel Add-in pane, then select the company from the **Company** field.</span></span> 

    > [!IMPORTANT]
    > <span data-ttu-id="045d6-123">Al cambiar de compañía, asegúrese de que el campo **Entorno** no está vacío.</span><span class="sxs-lookup"><span data-stu-id="045d6-123">When changing the company, make sure that the **Environment** field is not empty.</span></span> <span data-ttu-id="045d6-124">Si es así, configúrelo en una de las opciones disponibles; de lo contrario, el complemento no funcionará correctamente.</span><span class="sxs-lookup"><span data-stu-id="045d6-124">If it is, then set it to one of the available options; otherwise, the add-in will not work correctly.</span></span>  

<span data-ttu-id="045d6-125">El complemento de Excel se mejoró en la ola de lanzamiento 2 de 2019.</span><span class="sxs-lookup"><span data-stu-id="045d6-125">The Excel Add-in was enhanced in 2019 release wave 2.</span></span> <span data-ttu-id="045d6-126">Para obtener más información, vea [Mejoras en la integración de Excel](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration).</span><span class="sxs-lookup"><span data-stu-id="045d6-126">For more information, see [Enhancements to Excel integration](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration).</span></span>

> [!NOTE]
> <span data-ttu-id="045d6-127">Para [!INCLUDE[prodshort](includes/prodshort.md)] local, la acción **Editar en Excel** solo está disponible si el administrador ha configurado el complemento de Excel y solo está disponible para el cliente web.</span><span class="sxs-lookup"><span data-stu-id="045d6-127">For [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, the **Edit in Excel** action is only available if the Excel add-in has been configured by your administrator, and only available for the Web client.</span></span> <span data-ttu-id="045d6-128">Para los administradores: si desea aprender cómo instalar el complemento de Excel, consulte [Configuración del complemento de Excel para editar datos de Business Central](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span><span class="sxs-lookup"><span data-stu-id="045d6-128">For administrators, if you want to learn how to install the excel add-in, see [Setting up the Excel Add-In for Editing Business Central Data](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span></span> <span data-ttu-id="045d6-129">Para [!INCLUDE[prodshort](includes/prodshort.md)] local.</span><span class="sxs-lookup"><span data-stu-id="045d6-129">For [!INCLUDE[prodshort](includes/prodshort.md)] on-premises.</span></span>

### <a name="see-the-differences-between-the-options"></a><span data-ttu-id="045d6-130">Consulte las diferencias entre las opciones</span><span class="sxs-lookup"><span data-stu-id="045d6-130">See the differences between the options</span></span>
<br><br>  

> [!Video https://go.microsoft.com/fwlink/?linkid=2086039]

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="045d6-131">Consulte Formación relacionada en [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="045d6-131">See Related Training at [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="045d6-132">Consulte también</span><span class="sxs-lookup"><span data-stu-id="045d6-132">See Also</span></span>
[<span data-ttu-id="045d6-133">Trabajar con Business Central</span><span class="sxs-lookup"><span data-stu-id="045d6-133">Working with Business Central</span></span>](ui-work-product.md)  
