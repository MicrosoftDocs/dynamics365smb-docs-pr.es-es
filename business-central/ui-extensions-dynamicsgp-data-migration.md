---
title: Migrar datos de Dynamics GP antes de la actualización 15.3 | Microsoft Docs
description: Antes de la actualización 15.3, puede utilizar datos de Dynamics GP para migrar clientes, proveedores, productos de inventario, cuentas de contabilidad y transacciones de pagos y cobros pendientes desde Dynamics GP a Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.date: 10/01/2020
ms.author: edupont
ROBOTS: NOINDEX
ms.openlocfilehash: 7c17c5f54553e7960f4386918bda640fa2e0380e
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2020
ms.locfileid: "3915190"
---
# <a name="the-dynamics-gp-data-migration-extension"></a><span data-ttu-id="4f72b-103">Extensión de la migración de datos de Dynamics GP</span><span class="sxs-lookup"><span data-stu-id="4f72b-103">The Dynamics GP Data Migration Extension</span></span>

> [!NOTE]
> <span data-ttu-id="4f72b-104">Esta extensión se deja de usar en la actualización 15.3.</span><span class="sxs-lookup"><span data-stu-id="4f72b-104">This extension is deprecated in the 15.3 update.</span></span> <span data-ttu-id="4f72b-105">Recomendamos que los usuarios que quieran migrar desde Dynamics GP comiencen a utilizar el asistente **Migración en la nube** en su lugar.</span><span class="sxs-lookup"><span data-stu-id="4f72b-105">We recommend that users who want to migrate from Dynamics GP start using the **Cloud Migration** wizard instead.</span></span> <span data-ttu-id="4f72b-106">La extensión **Migración en la nube** tiene una funcionalidad más robusta y proporciona más datos a Business Central desde Dynamics GP.</span><span class="sxs-lookup"><span data-stu-id="4f72b-106">The **Cloud Migration** extension has more robust functionality and brings more data into Business Central from Dynamics GP.</span></span> <span data-ttu-id="4f72b-107">Para más información, consulte [Migrar a Business Central Online desde Dynamics GP](/dynamics365/business-central/dev-itpro/administration/migrate-dynamics-gp) en el contenido de la administración para [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="4f72b-107">For more information, see [Migrate to Business Central Online from Dynamics GP](/dynamics365/business-central/dev-itpro/administration/migrate-dynamics-gp) in the administration content for [!INCLUDE[prodshort](includes/prodshort.md)].</span></span>

## <a name="see-also"></a><span data-ttu-id="4f72b-108">Consulte también</span><span class="sxs-lookup"><span data-stu-id="4f72b-108">See Also</span></span>

[<span data-ttu-id="4f72b-109">Extensiones inteligentes en la nube para la migración a la nube</span><span class="sxs-lookup"><span data-stu-id="4f72b-109">Intelligent Cloud Extensions for Cloud Migration</span></span>](ui-extensions-data-replication.md)  
[<span data-ttu-id="4f72b-110">Importar datos de empresa de otros sistemas financieros</span><span class="sxs-lookup"><span data-stu-id="4f72b-110">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="4f72b-111">[Personalizar [!INCLUDE[prodshort](includes/prodshort.md)] con extensiones](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="4f72b-111">[Customizing [!INCLUDE[prodshort](includes/prodshort.md)] Using Extensions ](ui-extensions.md)</span></span>  
[<span data-ttu-id="4f72b-112">Migrar a Business Central Online desde Dynamics GP</span><span class="sxs-lookup"><span data-stu-id="4f72b-112">Migrate to Business Central Online from Dynamics GP</span></span>](/dynamics365/business-central/dev-itpro/administration/migrate-dynamics-gp)  
