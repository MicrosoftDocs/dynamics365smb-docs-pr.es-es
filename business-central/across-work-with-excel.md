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
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: b25413c8f0479aaccfc67ae96f2870690f993dfa
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2020
ms.locfileid: "3927277"
---
# <a name="viewing-and-editing-in-excel-from-business-central"></a><span data-ttu-id="f1cb7-103">Ver y editar en Excel desde Business Central</span><span class="sxs-lookup"><span data-stu-id="f1cb7-103">Viewing and Editing in Excel From Business Central</span></span>

<span data-ttu-id="f1cb7-104">Con las páginas que muestran una lista de registros en filas y columnas, como una lista de clientes, órdenes de venta o facturas, también puede ver los registros mediante Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="f1cb7-104">With pages that display a list of records in rows and columns, like a list of customers, sale orders, or invoices, you can also view the records using Microsoft Excel.</span></span> <span data-ttu-id="f1cb7-105">Para ello, tiene dos opciones.</span><span class="sxs-lookup"><span data-stu-id="f1cb7-105">To do this, you have two options.</span></span> <span data-ttu-id="f1cb7-106">Puede seleccionar la acción **Abrir en Excel** o la acción **Editar en Excel** en la página.</span><span class="sxs-lookup"><span data-stu-id="f1cb7-106">You can either select the **Open in Excel** action or the **Edit in Excel** action on the page.</span></span> <span data-ttu-id="f1cb7-107">Las diferencias entre las dos acciones son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="f1cb7-107">The differences between the two actions is as follows:</span></span>  

## <a name="open-in-excel"></a><span data-ttu-id="f1cb7-108">Abrir en Excel</span><span class="sxs-lookup"><span data-stu-id="f1cb7-108">Open in Excel</span></span>

- <span data-ttu-id="f1cb7-109">Con esta acción, Excel respeta los filtros de la página que limita los registros que se muestran.</span><span class="sxs-lookup"><span data-stu-id="f1cb7-109">With this action, Excel respects any filters on the page that limit the records shown.</span></span> <span data-ttu-id="f1cb7-110">Esto significa que el libro de Excel contendrá las mismas filas y columnas que aparecen en la página de [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="f1cb7-110">This means that the Excel workbook will contain the same rows and columns that appear on the page in [!INCLUDE[prodshort](includes/prodshort.md)].</span></span>

- <span data-ttu-id="f1cb7-111">Puede realizar cambios en los registros en Excel, pero no puede volver a publicar los cambios en [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="f1cb7-111">You can make changes to the records in Excel, but you cannot publish the changes back to [!INCLUDE[prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="f1cb7-112">Solo puede guardar los cambios en el archivo de Excel en su ordenador.</span><span class="sxs-lookup"><span data-stu-id="f1cb7-112">You can only save the changes to Excel file on your computer.</span></span>

- <span data-ttu-id="f1cb7-113">Esta acción funciona tanto en Windows como en macOS.</span><span class="sxs-lookup"><span data-stu-id="f1cb7-113">This action works on both on Windows and macOS.</span></span>

> [!NOTE]
> <span data-ttu-id="f1cb7-114">Por [!INCLUDE[prodshort](includes/prodshort.md)] local, la acción **Abrir en Excel** está disponible de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="f1cb7-114">For [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, the **Open in Excel** action is available by default.</span></span> <span data-ttu-id="f1cb7-115">Sin embargo, si configura [!INCLUDE[prodshort](includes/prodshort.md)] local para editar datos en Excel, la acción **Abrir en Excel** se reemplaza por la acción **Editar en Excel**.</span><span class="sxs-lookup"><span data-stu-id="f1cb7-115">However, if you set up [!INCLUDE[prodshort](includes/prodshort.md)] on-premises for editing data in Excel, then the **Open in Excel** action is replaced by the **Edit in Excel** action.</span></span>

## <a name="edit-in-excel"></a><span data-ttu-id="f1cb7-116">Editar en Excel</span><span class="sxs-lookup"><span data-stu-id="f1cb7-116">Edit in Excel</span></span>

- <span data-ttu-id="f1cb7-117">Con esta acción, Excel respeta la mayoría de los filtros de la página que limitan los registros que se muestran.</span><span class="sxs-lookup"><span data-stu-id="f1cb7-117">With this action, Excel respects most filters on the page that limit the records shown.</span></span> <span data-ttu-id="f1cb7-118">Esto significa que el libro de Excel contendrá casi los mismos registros y columnas.</span><span class="sxs-lookup"><span data-stu-id="f1cb7-118">This means that the Excel workbook will contain almost the same records and columns.</span></span>

- <span data-ttu-id="f1cb7-119">La ventaja de la acción **Editar en Excel** es que le permite realizar cambios en los registros en Excel y luego publicarlos de nuevo en [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="f1cb7-119">The advantage of the **Edit in Excel** action is that it lets you make changes to records in Excel and then publish the changes back to [!INCLUDE[prodshort](includes/prodshort.md)].</span></span>

- <span data-ttu-id="f1cb7-120">Solo funciona en Windows; en macOS, no.</span><span class="sxs-lookup"><span data-stu-id="f1cb7-120">It only works on Windows; not macOS.</span></span>

- <span data-ttu-id="f1cb7-121">Puede cambiar la compañía con la que está trabajando.</span><span class="sxs-lookup"><span data-stu-id="f1cb7-121">You can switch the company that your are working with.</span></span> <span data-ttu-id="f1cb7-122">Para hacerlo, seleccione el icono **Opciones** ![Opciones de complemento de Excel](media/cogwheel.png "Opciones del complemento de Excel") en el panel Complemento de Excel y luego seleccione la compañía en el campo **Empresa**.</span><span class="sxs-lookup"><span data-stu-id="f1cb7-122">To do this, select the **Options** icon ![Excel add-in options](media/cogwheel.png "Excel add-in options") in the Excel Add-in pane, then select the company from the **Company** field.</span></span>  

    > [!IMPORTANT]
    > <span data-ttu-id="f1cb7-123">Al cambiar de compañía, asegúrese de que el campo **Entorno** no está vacío.</span><span class="sxs-lookup"><span data-stu-id="f1cb7-123">When changing the company, make sure that the **Environment** field is not empty.</span></span> <span data-ttu-id="f1cb7-124">Si es así, configúrelo en una de las opciones disponibles; de lo contrario, el complemento no funcionará correctamente.</span><span class="sxs-lookup"><span data-stu-id="f1cb7-124">If it is, then set it to one of the available options; otherwise, the add-in will not work correctly.</span></span>  

<span data-ttu-id="f1cb7-125">Si realiza cambios en el complemento, debe volver a cargarlo para actualizar la conexión.</span><span class="sxs-lookup"><span data-stu-id="f1cb7-125">If you make changes to the add-in, you must reload it in order to update the connection.</span></span> <span data-ttu-id="f1cb7-126">Para recargar, use el menú del ![complemento de Excel](media/excel-addin-menu.png "Menú del complemento de Excel") en la esquina superior derecha del complemento.</span><span class="sxs-lookup"><span data-stu-id="f1cb7-126">To reload, use the ![Excel add-in menu](media/excel-addin-menu.png "Excel add-in menu") menu in the top-right corner of the add-in.</span></span>

> [!NOTE]
> <span data-ttu-id="f1cb7-127">Para [!INCLUDE[prodshort](includes/prodshort.md)] local, la acción **Editar en Excel** solo está disponible si el administrador ha configurado el complemento de Excel y solo está disponible para el cliente web.</span><span class="sxs-lookup"><span data-stu-id="f1cb7-127">For [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, the **Edit in Excel** action is only available if the Excel add-in has been configured by your administrator, and only available for the Web client.</span></span> <span data-ttu-id="f1cb7-128">Para los administradores: si desea aprender cómo instalar el complemento de Excel, consulte [Configuración del complemento de Excel para editar datos de Business Central](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span><span class="sxs-lookup"><span data-stu-id="f1cb7-128">For administrators, if you want to learn how to install the excel add-in, see [Setting up the Excel Add-In for Editing Business Central Data](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span></span>

### <a name="see-the-differences-between-the-options"></a><span data-ttu-id="f1cb7-129">Consulte las diferencias entre las opciones</span><span class="sxs-lookup"><span data-stu-id="f1cb7-129">See the differences between the options</span></span>
<br><br>  

> [!Video https://go.microsoft.com/fwlink/?linkid=2086039]

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="f1cb7-130">Consulte la Formación relacionada en [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="f1cb7-130">See Related Training at [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="f1cb7-131">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f1cb7-131">See Also</span></span>

[<span data-ttu-id="f1cb7-132">Análisis de estados financieros en Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="f1cb7-132">Analyzing Financial Statements in Microsoft Excel</span></span>](finance-analyze-excel.md)  
[<span data-ttu-id="f1cb7-133">Trabajar con Business Central</span><span class="sxs-lookup"><span data-stu-id="f1cb7-133">Working with Business Central</span></span>](ui-work-product.md)  
[<span data-ttu-id="f1cb7-134">Mejoras en la integración de Excel en el segundo lanzamiento de versiones 2 de 2019</span><span class="sxs-lookup"><span data-stu-id="f1cb7-134">Enhancements to Excel integration in 2019 release wave 2</span></span>](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration)  
