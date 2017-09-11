---
title: "Migrar datos de Dynamics GP con la extensión de la migración de datos | Documentos de Microsoft"
description: "Utilice la extensión de migración de datos de Dynamics GP para migrar clientes, proveedores, productos de inventario y cuentas desde Dynamics GP a Dynamics 365 for Financials."
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
ms.openlocfilehash: 31b698aea884da162cc18f16a912ebd57e35aed9
ms.contentlocale: es-es
ms.lasthandoff: 09/11/2017

---
# <a name="the-dynamics-gp-data-migration-extension-for-dynamics-365-for-financials"></a><span data-ttu-id="6800b-103">Extensión de la migración de datos de Dynamics GP para Dynamics 365 for Financials</span><span class="sxs-lookup"><span data-stu-id="6800b-103">The Dynamics GP Data Migration Extension for Dynamics 365 for Financials</span></span>
<span data-ttu-id="6800b-104">Esta extensión facilita la migración de clientes, proveedores, productos de inventario y cuentas de Dynamics GP a [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="6800b-104">This extension makes it easy to migrate customers, vendors, inventory items, and accounts from Dynamics GP to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="6800b-105">Si la empresa usa Dynamics GP actualmente, puede exportar los registros maestros correspondientes y después abrir una guía de instalación asistida para agregar los datos a [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="6800b-105">If your business uses Dynamics GP today, you can export the relevant master records and then open an assisted setup guide to add the data to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="6800b-106">Para obtener más información, vea [Migrar datos empresariales desde otros sistemas financieros](upload-data.md).</span><span class="sxs-lookup"><span data-stu-id="6800b-106">For more information, see [Migrate Business Data from Other Finance Systems](upload-data.md).</span></span>

## <a name="exporting-data-from-dynamics-gp"></a><span data-ttu-id="6800b-107">Exportar datos desde Dynamics GP</span><span class="sxs-lookup"><span data-stu-id="6800b-107">Exporting Data from Dynamics GP</span></span>
<span data-ttu-id="6800b-108">Deberá haber exportado todos los clientes, proveedores, productos de inventario y cuentas existentes, o parte de ellos, mediante la funcionalidad de exportación de datos de Dynamics GP.</span><span class="sxs-lookup"><span data-stu-id="6800b-108">You must have exported some or all of your existing customers, vendors, inventory items, and accounts to a file, using the Dynamics GP functionality for data export.</span></span> <span data-ttu-id="6800b-109">Para las finalidades de [!INCLUDE[d365fin](includes/d365fin_md.md)], puede exportar los tipos de datos siguientes:</span><span class="sxs-lookup"><span data-stu-id="6800b-109">For the purposes of [!INCLUDE[d365fin](includes/d365fin_md.md)], you can export the following types of data:</span></span>

* <span data-ttu-id="6800b-110">Cuenta</span><span class="sxs-lookup"><span data-stu-id="6800b-110">Account</span></span>  
* <span data-ttu-id="6800b-111">Cliente</span><span class="sxs-lookup"><span data-stu-id="6800b-111">Customer</span></span>  
* <span data-ttu-id="6800b-112">Elemento</span><span class="sxs-lookup"><span data-stu-id="6800b-112">Item</span></span>  
* <span data-ttu-id="6800b-113">Proveedor</span><span class="sxs-lookup"><span data-stu-id="6800b-113">Vendor</span></span>  

<span data-ttu-id="6800b-114">La extensión de la migración de datos de Dynamics GP asigna automáticamente los datos exportados para que estén a su disposición rápidamente en la nueva empresa de [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="6800b-114">The Dynamics GP Data Migration extension automatically maps the exported data so that your data is quickly available to you in your new [!INCLUDE[d365fin](includes/d365fin_md.md)] company.</span></span> <span data-ttu-id="6800b-115">Durante el proceso, se crea información de configuración auxiliar, por ejemplo grupos contables.</span><span class="sxs-lookup"><span data-stu-id="6800b-115">During the process, supporting setup information is created, such as posting groups.</span></span> <span data-ttu-id="6800b-116">Los productos de inventario se incorporarán al sistema con el método de valoración de coste FIFO.</span><span class="sxs-lookup"><span data-stu-id="6800b-116">Inventory items will be brought into the system with FIFO as the cost valuation method.</span></span> <span data-ttu-id="6800b-117">Las cuentas se configurarán como el segmento de cuenta principal desde Dynamics GP con dimensiones, porque [!INCLUDE[d365fin](includes/d365fin_long_md.md)] no tiene segmentos de cuentas.</span><span class="sxs-lookup"><span data-stu-id="6800b-117">Accounts will be set up as the main account segment from Dynamics GP with dimensions, because [!INCLUDE[d365fin](includes/d365fin_long_md.md)] does not have account segments.</span></span>

## <a name="see-also"></a><span data-ttu-id="6800b-118">Consulte también</span><span class="sxs-lookup"><span data-stu-id="6800b-118">See Also</span></span>
[<span data-ttu-id="6800b-119">Importar datos de empresa de otros sistemas financieros</span><span class="sxs-lookup"><span data-stu-id="6800b-119">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="6800b-120">[Personalizar [!INCLUDE[d365fin](includes/d365fin_md.md)] con extensiones](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="6800b-120">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)</span></span>  

