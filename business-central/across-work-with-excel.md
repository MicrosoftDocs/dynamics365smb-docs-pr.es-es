---
title: Ver y editar en Excel desde Business Central
description: Obtenga más información sobre cómo puede abrir las páginas en Microsoft Excel desde Business Central para un mejor análisis de datos.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: 7e3abf36444c4701229ffaac7ceade11bb1879cc
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2021
ms.locfileid: "5786937"
---
# <a name="viewing-and-editing-in-excel-from-business-central"></a><span data-ttu-id="57727-103">Ver y editar en Excel desde Business Central</span><span class="sxs-lookup"><span data-stu-id="57727-103">Viewing and Editing in Excel From Business Central</span></span>

<span data-ttu-id="57727-104">Con las páginas que muestran una lista de registros en filas y columnas, como una lista de clientes, órdenes de venta o facturas, también puede ver los registros mediante Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="57727-104">With pages that display a list of records in rows and columns, like a list of customers, sale orders, or invoices, you can also view the records using Microsoft Excel.</span></span> <span data-ttu-id="57727-105">Para ello, tiene dos opciones.</span><span class="sxs-lookup"><span data-stu-id="57727-105">To do this, you have two options.</span></span> <span data-ttu-id="57727-106">Puede seleccionar la acción **Abrir en Excel** o la acción **Editar en Excel** en la página.</span><span class="sxs-lookup"><span data-stu-id="57727-106">You can either select the **Open in Excel** action or the **Edit in Excel** action on the page.</span></span> <span data-ttu-id="57727-107">Las diferencias entre las dos acciones son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="57727-107">The differences between the two actions are as follows:</span></span>  

## <a name="open-in-excel"></a><span data-ttu-id="57727-108">Abrir en Excel</span><span class="sxs-lookup"><span data-stu-id="57727-108">Open in Excel</span></span>

- <span data-ttu-id="57727-109">Con esta acción, Excel respeta los filtros de la página que limita los registros que se muestran.</span><span class="sxs-lookup"><span data-stu-id="57727-109">With this action, Excel respects any filters on the page that limit the records shown.</span></span> <span data-ttu-id="57727-110">El libro de Excel contendrá las mismas filas y columnas que aparecen en la página de [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="57727-110">The Excel workbook will contain the same rows and columns that appear on the page in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

- <span data-ttu-id="57727-111">Puede realizar cambios en los registros en Excel, pero no puede volver a publicar los cambios en [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="57727-111">You can make changes to the records in Excel, but you cannot publish the changes back to [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="57727-112">Solo puede guardar los cambios en el archivo de Excel en su ordenador.</span><span class="sxs-lookup"><span data-stu-id="57727-112">You can only save the changes to Excel file on your computer.</span></span>

- <span data-ttu-id="57727-113">Esta acción funciona tanto en Windows como en macOS.</span><span class="sxs-lookup"><span data-stu-id="57727-113">This action works on both on Windows and macOS.</span></span>

> [!NOTE]
> <span data-ttu-id="57727-114">Por [!INCLUDE[prod_short](includes/prod_short.md)] local, la acción **Abrir en Excel** está disponible de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="57727-114">For [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, the **Open in Excel** action is available by default.</span></span> <span data-ttu-id="57727-115">Sin embargo, si configura [!INCLUDE[prod_short](includes/prod_short.md)] local para editar datos en Excel, la acción **Abrir en Excel** se reemplaza por la acción **Editar en Excel**.</span><span class="sxs-lookup"><span data-stu-id="57727-115">However, if you set up [!INCLUDE[prod_short](includes/prod_short.md)] on-premises for editing data in Excel, then the **Open in Excel** action is replaced by the **Edit in Excel** action.</span></span>

## <a name="edit-in-excel"></a><span data-ttu-id="57727-116">Editar en Excel</span><span class="sxs-lookup"><span data-stu-id="57727-116">Edit in Excel</span></span>

- <span data-ttu-id="57727-117">Con esta acción, Excel respeta la mayoría de los filtros en la página que limitan los registros mostrados, por lo que el libro de Excel contendrá casi los mismos registros y columnas.</span><span class="sxs-lookup"><span data-stu-id="57727-117">With this action, Excel respects most filters on the page that limit the records shown, so the Excel workbook will contain almost the same records and columns.</span></span>

- <span data-ttu-id="57727-118">La ventaja de la acción **Editar en Excel** es que le permite realizar cambios en los registros en Excel y luego publicarlos de nuevo en [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="57727-118">The advantage of the **Edit in Excel** action is that it lets you make changes to records in Excel and then publish the changes back to [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

- <span data-ttu-id="57727-119">Solo funciona en Windows; en macOS, no.</span><span class="sxs-lookup"><span data-stu-id="57727-119">It only works on Windows; not macOS.</span></span>

- <span data-ttu-id="57727-120">Puede cambiar la compañía con la que está trabajando.</span><span class="sxs-lookup"><span data-stu-id="57727-120">You can switch the company that you are working with.</span></span> <span data-ttu-id="57727-121">Para cambiar de empresa, seleccione el icono **Opciones** ![Opciones de complemento de Excel](media/cogwheel.png "Opciones del complemento de Excel") en el panel Complemento de Excel y luego seleccione la compañía en el campo **Empresa**.</span><span class="sxs-lookup"><span data-stu-id="57727-121">To switch company, select the **Options** icon ![Excel add-in options](media/cogwheel.png "Excel add-in options") in the Excel Add-in pane, then select the company from the **Company** field.</span></span>  

    > [!IMPORTANT]
    > <span data-ttu-id="57727-122">Al cambiar de compañía, asegúrese de que el campo **Entorno** no está vacío.</span><span class="sxs-lookup"><span data-stu-id="57727-122">When changing the company, make sure that the **Environment** field is not empty.</span></span> <span data-ttu-id="57727-123">Si es así, configúrelo en una de las opciones disponibles; de lo contrario, el complemento no funcionará correctamente.</span><span class="sxs-lookup"><span data-stu-id="57727-123">If it is, then set it to one of the available options; otherwise, the add-in will not work correctly.</span></span>  

<span data-ttu-id="57727-124">Si realiza cambios en el complemento, debe volver a cargarlo para actualizar la conexión.</span><span class="sxs-lookup"><span data-stu-id="57727-124">If you make changes to the add-in, you must reload it to update the connection.</span></span> <span data-ttu-id="57727-125">Para recargar, use el menú del ![complemento de Excel](media/excel-addin-menu.png "Menú del complemento de Excel") en la esquina superior derecha del complemento.</span><span class="sxs-lookup"><span data-stu-id="57727-125">To reload, use the ![Excel add-in menu](media/excel-addin-menu.png "Excel add-in menu") menu in the top-right corner of the add-in.</span></span> <span data-ttu-id="57727-126">Si no puede cargar el complemento, hable con su administrador.</span><span class="sxs-lookup"><span data-stu-id="57727-126">If you cannot load the add-in, talk to your administrator.</span></span> <span data-ttu-id="57727-127">Si es el administrador, consulte [Configurar el complemento de Excel para editar datos de Business Central](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span><span class="sxs-lookup"><span data-stu-id="57727-127">If you are the administrator, see [Setting up the Excel Add-In for Editing Business Central Data](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span></span>

> [!NOTE]
> <span data-ttu-id="57727-128">Para [!INCLUDE[prod_short](includes/prod_short.md)] local, la acción **Editar en Excel** solo está disponible si el administrador ha configurado el complemento de Excel y solo está disponible para el cliente web.</span><span class="sxs-lookup"><span data-stu-id="57727-128">For [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, the **Edit in Excel** action is only available if the Excel add-in has been configured by your administrator, and only available for the Web client.</span></span> <span data-ttu-id="57727-129">Para los administradores: si desea aprender cómo instalar el complemento de Excel, consulte [Configuración del complemento de Excel para editar datos de Business Central](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span><span class="sxs-lookup"><span data-stu-id="57727-129">For administrators, if you want to learn how to install the Excel add-in, see [Setting up the Excel Add-In for Editing Business Central Data](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span></span>

### <a name="see-the-differences-between-the-options"></a><span data-ttu-id="57727-130">Consulte las diferencias entre las opciones</span><span class="sxs-lookup"><span data-stu-id="57727-130">See the differences between the options</span></span>
<br><br>  

> [!Video https://go.microsoft.com/fwlink/?linkid=2086039]

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="57727-131">Consulte la Formación relacionada en [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="57727-131">See Related Training at [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="57727-132">Consulte también</span><span class="sxs-lookup"><span data-stu-id="57727-132">See Also</span></span>

[<span data-ttu-id="57727-133">Análisis de estados financieros en Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="57727-133">Analyzing Financial Statements in Microsoft Excel</span></span>](finance-analyze-excel.md)  
[<span data-ttu-id="57727-134">Trabajar con Business Central</span><span class="sxs-lookup"><span data-stu-id="57727-134">Working with Business Central</span></span>](ui-work-product.md)  
[<span data-ttu-id="57727-135">Mejoras en la integración de Excel en el segundo lanzamiento de versiones 2 de 2019</span><span class="sxs-lookup"><span data-stu-id="57727-135">Enhancements to Excel integration in 2019 release wave 2</span></span>](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration)  


[!INCLUDE[footer-include](includes/footer-banner.md)]