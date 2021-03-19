---
title: Migrar datos de Dynamics GP antes de la actualización 15.3 | Microsoft Docs
description: Antes de la actualización 15.3, puede utilizar datos de Dynamics GP para migrar clientes, proveedores, productos de inventario, cuentas de contabilidad y transacciones de pagos y cobros pendientes desde Dynamics GP a Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.date: 10/01/2020
ms.author: edupont
ROBOTS: NOINDEX
ms.openlocfilehash: 986612a04ea75e89c2ef7cc983af4ae507738871
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5377303"
---
# <a name="the-dynamics-gp-data-migration-extension"></a><span data-ttu-id="c70d5-103">Extensión de la migración de datos de Dynamics GP</span><span class="sxs-lookup"><span data-stu-id="c70d5-103">The Dynamics GP Data Migration Extension</span></span>

> [!NOTE]
> <span data-ttu-id="c70d5-104">Esta extensión se deja de usar en la actualización 15.3.</span><span class="sxs-lookup"><span data-stu-id="c70d5-104">This extension is deprecated in the 15.3 update.</span></span> <span data-ttu-id="c70d5-105">Recomendamos que los usuarios que quieran migrar desde Dynamics GP comiencen a utilizar el asistente **Migración en la nube** en su lugar.</span><span class="sxs-lookup"><span data-stu-id="c70d5-105">We recommend that users who want to migrate from Dynamics GP start using the **Cloud Migration** wizard instead.</span></span> <span data-ttu-id="c70d5-106">La extensión **Migración en la nube** tiene una funcionalidad más robusta y proporciona más datos a Business Central desde Dynamics GP.</span><span class="sxs-lookup"><span data-stu-id="c70d5-106">The **Cloud Migration** extension has more robust functionality and brings more data into Business Central from Dynamics GP.</span></span> <span data-ttu-id="c70d5-107">Para más información, consulte [Migrar a Business Central Online desde Dynamics GP](/dynamics365/business-central/dev-itpro/administration/migrate-dynamics-gp) en el contenido de la administración para [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="c70d5-107">For more information, see [Migrate to Business Central Online from Dynamics GP](/dynamics365/business-central/dev-itpro/administration/migrate-dynamics-gp) in the administration content for [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

## <a name="see-also"></a><span data-ttu-id="c70d5-108">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c70d5-108">See Also</span></span>

[<span data-ttu-id="c70d5-109">Extensiones inteligentes en la nube para la migración a la nube</span><span class="sxs-lookup"><span data-stu-id="c70d5-109">Intelligent Cloud Extensions for Cloud Migration</span></span>](ui-extensions-data-replication.md)  
[<span data-ttu-id="c70d5-110">Importar datos de empresa de otros sistemas financieros</span><span class="sxs-lookup"><span data-stu-id="c70d5-110">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="c70d5-111">[Personalizar [!INCLUDE[prod_short](includes/prod_short.md)] con extensiones](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="c70d5-111">[Customizing [!INCLUDE[prod_short](includes/prod_short.md)] Using Extensions ](ui-extensions.md)</span></span>  
[<span data-ttu-id="c70d5-112">Migrar a Business Central Online desde Dynamics GP</span><span class="sxs-lookup"><span data-stu-id="c70d5-112">Migrate to Business Central Online from Dynamics GP</span></span>](/dynamics365/business-central/dev-itpro/administration/migrate-dynamics-gp)  


[!INCLUDE[footer-include](includes/footer-banner.md)]