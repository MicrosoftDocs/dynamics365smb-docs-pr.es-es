---
title: "Usar la extensión de migración de QuickBooks | Documentos de Microsoft"
description: "Describe cómo utilizar la extensión para importar clientes, proveedores, productos y cuentas desde QuickBooks Desktop a Dynamics 365 for Financials."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 37d90316ea0be5489fb5abe33645de3fe0d3cf90
ms.contentlocale: es-es
ms.lasthandoff: 09/11/2017

---
# <a name="the-quickbooks-data-migration-extension-for-dynamics-365-for-financials"></a><span data-ttu-id="6efca-103">Extensión de la migración de datos de QuickBooks para Dynamics 365 for Financials</span><span class="sxs-lookup"><span data-stu-id="6efca-103">The QuickBooks Data Migration Extension for Dynamics 365 for Financials</span></span>
<span data-ttu-id="6efca-104">Esta extensión facilita la migración de clientes, proveedores, productos y cuentas de QuickBooks a [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="6efca-104">This extension makes it easy to migrate customers, vendors, items, and accounts from QuickBooks to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="6efca-105">Si la empresa usa QuickBooks actualmente, puede exportar la información correspondiente y después abrir una guía de instalación asistida para cargar los datos en [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="6efca-105">If your business uses QuickBooks today, you can export the relevant information and then open an assisted setup guide to upload the data to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  
<span data-ttu-id="6efca-106">Para obtener más información, vea [Importar datos empresariales desde otros sistemas financieros](upload-data.md).</span><span class="sxs-lookup"><span data-stu-id="6efca-106">For more information, see [Importing Business Data from Other Finance Systems](upload-data.md).</span></span>

## <a name="exporting-data-from-quickbooks"></a><span data-ttu-id="6efca-107">Exportar datos desde QuickBooks</span><span class="sxs-lookup"><span data-stu-id="6efca-107">Exporting Data from QuickBooks</span></span>
<span data-ttu-id="6efca-108">Debe haber exportado algunos o todos los clientes, proveedores, productos de inventario y cuentas existentes a un archivo IIF (Intuit Interchange Format).</span><span class="sxs-lookup"><span data-stu-id="6efca-108">You must have exported some or all of your existing customers, vendors, inventory items, and accounts to an Intuit Interchange Format (IIF) file.</span></span> <span data-ttu-id="6efca-109">La extensión de la migración de datos de QuickBooks incluye una asociación predeterminada de datos de QuickBooks para que pueda usar sus datos existentes para probar su nueva empresa [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="6efca-109">The QuickBooks Data Migration extension includes a default mapping of QuickBooks data so that you can use your existing data to test your new [!INCLUDE[d365fin](includes/d365fin_md.md)] company.</span></span> <span data-ttu-id="6efca-110">La asignación predeterminada será suficiente en la gran mayoría de casos, pero puede cambiar la asignación en la guía de configuración asistida.</span><span class="sxs-lookup"><span data-stu-id="6efca-110">The default mapping will be sufficient in the vast majority of cases, but you can change the mapping in the assisted setup guide.</span></span>  
<span data-ttu-id="6efca-111">En QuickBooks, el menú Archivo incluye una utilidad para exportar listas.</span><span class="sxs-lookup"><span data-stu-id="6efca-111">In QuickBooks, the File menu includes a utility to export lists.</span></span> <span data-ttu-id="6efca-112">Para las finalidades de [!INCLUDE[d365fin](includes/d365fin_md.md)], puede exportar las listas siguientes:</span><span class="sxs-lookup"><span data-stu-id="6efca-112">For the purposes of [!INCLUDE[d365fin](includes/d365fin_md.md)], you can export the following lists:</span></span>

* <span data-ttu-id="6efca-113">Lista de clientes</span><span class="sxs-lookup"><span data-stu-id="6efca-113">Customer List</span></span>  
* <span data-ttu-id="6efca-114">Lista de proveedores</span><span class="sxs-lookup"><span data-stu-id="6efca-114">Vendor List</span></span>  
* <span data-ttu-id="6efca-115">Lista de productos</span><span class="sxs-lookup"><span data-stu-id="6efca-115">Item List</span></span>  
* <span data-ttu-id="6efca-116">Lista de cuentas</span><span class="sxs-lookup"><span data-stu-id="6efca-116">Account List</span></span>  

<span data-ttu-id="6efca-117">Los datos exportados se guardan como un archivo IIF que, a continuación, puede cargar a [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="6efca-117">The exported data is saved as an IIF file that you can then upload to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

## <a name="see-also"></a><span data-ttu-id="6efca-118">Consulte también</span><span class="sxs-lookup"><span data-stu-id="6efca-118">See Also</span></span>
[<span data-ttu-id="6efca-119">Importar datos de empresa de otros sistemas financieros</span><span class="sxs-lookup"><span data-stu-id="6efca-119">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="6efca-120">[Personalizar [!INCLUDE[d365fin](includes/d365fin_md.md)] con extensiones](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="6efca-120">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)</span></span>  

