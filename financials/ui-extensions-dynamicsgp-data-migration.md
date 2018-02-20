---
title: "Migrar datos de Dynamics GP con la extensión de la migración de datos | Documentos de Microsoft"
description: "Utilice la extensión de migración de datos de Dynamics GP para migrar clientes, proveedores, productos de inventario y cuentas desde Dynamics GP a Finance and Operations, Business edition."
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
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: bfd3ca3e28b6eb3efa2a16cc131b508db6bd1590
ms.contentlocale: es-es
ms.lasthandoff: 01/30/2018

---
# <a name="the-dynamics-gp-data-migration-extension-for-finance-and-operations-business-edition"></a><span data-ttu-id="c5531-103">Extensión de migración de datos de Dynamics GP para Finance and Operations, Business edition</span><span class="sxs-lookup"><span data-stu-id="c5531-103">The Dynamics GP Data Migration Extension for Finance and Operations, Business edition</span></span> 
<span data-ttu-id="c5531-104">Esta extensión facilita la migración de clientes, proveedores, productos de inventario y cuentas de Dynamics GP a [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="c5531-104">This extension makes it easy to migrate customers, vendors, inventory items, and accounts from Dynamics GP to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="c5531-105">Si la empresa usa Dynamics GP actualmente, puede exportar los registros maestros correspondientes y después abrir una guía de instalación asistida para agregar los datos a [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="c5531-105">If your business uses Dynamics GP today, you can export the relevant master records and then open an assisted setup guide to add the data to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="c5531-106">Para obtener más información, vea [Migrar datos empresariales desde otros sistemas financieros](upload-data.md).</span><span class="sxs-lookup"><span data-stu-id="c5531-106">For more information, see [Migrate Business Data from Other Finance Systems](upload-data.md).</span></span>

## <a name="exporting-data-from-dynamics-gp"></a><span data-ttu-id="c5531-107">Exportar datos desde Dynamics GP</span><span class="sxs-lookup"><span data-stu-id="c5531-107">Exporting Data from Dynamics GP</span></span>
<span data-ttu-id="c5531-108">Deberá haber exportado todos los clientes, proveedores, productos de inventario y cuentas existentes, o parte de ellos, mediante la funcionalidad de exportación de datos de Dynamics GP.</span><span class="sxs-lookup"><span data-stu-id="c5531-108">You must have exported some or all of your existing customers, vendors, inventory items, and accounts to a file, using the Dynamics GP functionality for data export.</span></span> <span data-ttu-id="c5531-109">Para las finalidades de [!INCLUDE[d365fin](includes/d365fin_md.md)], puede exportar los tipos de datos siguientes:</span><span class="sxs-lookup"><span data-stu-id="c5531-109">For the purposes of [!INCLUDE[d365fin](includes/d365fin_md.md)], you can export the following types of data:</span></span>

* <span data-ttu-id="c5531-110">Cuenta</span><span class="sxs-lookup"><span data-stu-id="c5531-110">Account</span></span>  
* <span data-ttu-id="c5531-111">Cliente</span><span class="sxs-lookup"><span data-stu-id="c5531-111">Customer</span></span>  
* <span data-ttu-id="c5531-112">Elemento</span><span class="sxs-lookup"><span data-stu-id="c5531-112">Item</span></span>  
* <span data-ttu-id="c5531-113">Proveedor</span><span class="sxs-lookup"><span data-stu-id="c5531-113">Vendor</span></span>  

<span data-ttu-id="c5531-114">La extensión de la migración de datos de Dynamics GP asigna automáticamente los datos exportados para que estén a su disposición rápidamente en la nueva empresa de [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="c5531-114">The Dynamics GP Data Migration extension automatically maps the exported data so that your data is quickly available to you in your new [!INCLUDE[d365fin](includes/d365fin_md.md)] company.</span></span> <span data-ttu-id="c5531-115">Durante el proceso, se crea información de configuración auxiliar, por ejemplo grupos contables.</span><span class="sxs-lookup"><span data-stu-id="c5531-115">During the process, supporting setup information is created, such as posting groups.</span></span> <span data-ttu-id="c5531-116">Los productos de inventario se incorporarán al sistema con el método de valoración de coste FIFO.</span><span class="sxs-lookup"><span data-stu-id="c5531-116">Inventory items will be brought into the system with FIFO as the cost valuation method.</span></span> <span data-ttu-id="c5531-117">Las cuentas se configurarán como el segmento de cuenta principal desde Dynamics GP con dimensiones, porque [!INCLUDE[d365fin](includes/d365fin_long_md.md)] no tiene segmentos de cuentas.</span><span class="sxs-lookup"><span data-stu-id="c5531-117">Accounts will be set up as the main account segment from Dynamics GP with dimensions, because [!INCLUDE[d365fin](includes/d365fin_long_md.md)] does not have account segments.</span></span>

## <a name="see-also"></a><span data-ttu-id="c5531-118">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c5531-118">See Also</span></span>
[<span data-ttu-id="c5531-119">Importar datos de empresa de otros sistemas financieros</span><span class="sxs-lookup"><span data-stu-id="c5531-119">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="c5531-120">[Personalizar [!INCLUDE[d365fin](includes/d365fin_md.md)] con extensiones](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="c5531-120">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)</span></span>  

