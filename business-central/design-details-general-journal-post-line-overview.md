---
title: Descripción de la línea de registro en diario general | Documentos de Microsoft
description: Este tema introduce cambios en la codeunit 12, **Diario general-línea de registro**, que es el objeto principal de aplicación para el registro en contabilidad y es el único lugar donde insertar movimientos de contabilidad, de IVA, de clientes y de proveedores.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, general ledger, post
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: 1f6060eb7672b332fb570eb13fe027a3b58e6594
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/09/2021
ms.locfileid: "6215258"
---
# <a name="general-journal-post-line-overview"></a><span data-ttu-id="73011-103">Descripción de la línea de registro en diario general</span><span class="sxs-lookup"><span data-stu-id="73011-103">General Journal Post Line Overview</span></span>

<span data-ttu-id="73011-104">La codeunit 12, **Diario general-lín. reg.**, es el objeto principal de aplicación para el registro en contabilidad y es el único lugar donde insertar movimientos de contabilidad, de IVA, de clientes y de proveedores.</span><span class="sxs-lookup"><span data-stu-id="73011-104">Codeunit 12, **Gen. Jnl.-Post Line**, is the major application object for general ledger posting and is the only place to insert general ledger, VAT, and customer and vendor ledger entries.</span></span> <span data-ttu-id="73011-105">Esta codeunit se usa también para todas las operaciones de Liquidar, Desliquidar y Revertir.</span><span class="sxs-lookup"><span data-stu-id="73011-105">This codeunit is also used for all Apply, Unapply and Reverse operations.</span></span>  
  
<span data-ttu-id="73011-106">En Microsoft Dynamics NAV 2013 R2, la codeunit se rediseñó porque se había vuelto muy grande, con aproximadamente 7600 líneas de código.</span><span class="sxs-lookup"><span data-stu-id="73011-106">In Microsoft Dynamics NAV 2013 R2, the codeunit was redesigned because it had become very large, with approximately 7,600 code lines.</span></span> <span data-ttu-id="73011-107">La arquitectura había cambiado y la codeunit hizo más sencilla y más fácil de mantener.</span><span class="sxs-lookup"><span data-stu-id="73011-107">The architecture was changed and the codeunit has been made simpler and more maintainable.</span></span> <span data-ttu-id="73011-108">Esta documentación describe los cambios y proporciona información que necesitará para actualizar.</span><span class="sxs-lookup"><span data-stu-id="73011-108">This documentation describes the changes and provides information that you will need for upgrade.</span></span>  
  
## <a name="old-architecture"></a><span data-ttu-id="73011-109">Arquitectura antigua</span><span class="sxs-lookup"><span data-stu-id="73011-109">Old Architecture</span></span>  
<span data-ttu-id="73011-110">La arquitectura antigua tenía las características siguientes:</span><span class="sxs-lookup"><span data-stu-id="73011-110">The old architecture had the following features:</span></span>  
  
* <span data-ttu-id="73011-111">Se hacía un uso extensivo de variables globales, lo que aumentaba la posibilidad de que se produjeran errores ocultos por el uso de variables con ámbito incorrecto.</span><span class="sxs-lookup"><span data-stu-id="73011-111">There was extensive use of global variables, which increased the possibility of hidden errors due to use of variables with the wrong scope.</span></span>  
* <span data-ttu-id="73011-112">Había muchos procedimientos largos (con más de 100 líneas de código) que también tenían una elevada complejidad ciclomática (es decir, muchas declaraciones anidadas CASE, REPEAT e IF ), que hacían el código muy complicado de leer y mantener.</span><span class="sxs-lookup"><span data-stu-id="73011-112">There were many long procedures (with more than 100 code lines) that also had high cyclomatic complexity (that is, a lot of CASE, REPEAT, IF nested statements), which made the code very difficult to read and maintain.</span></span>  
* <span data-ttu-id="73011-113">Varios procedimientos que solo se usaban localmente y solo debían usarse localmente no estaban marcados como locales.</span><span class="sxs-lookup"><span data-stu-id="73011-113">Several procedures that were only used locally and were only meant to be used locally were not marked as local.</span></span>  
* <span data-ttu-id="73011-114">La mayoría de los procedimientos no tenían parámetros y usaban variables globales.</span><span class="sxs-lookup"><span data-stu-id="73011-114">Most procedures had no parameters and used global variables.</span></span> <span data-ttu-id="73011-115">Algunos parámetros utilizados y variables globales reemplazadas con variables locales.</span><span class="sxs-lookup"><span data-stu-id="73011-115">Some used parameters and overrode global variables with locals.</span></span>  
* <span data-ttu-id="73011-116">Los patrones de código para buscar las cuentas de contabilidad y crear movimientos de contabilidad y de IVA no estaban estandardizados y variaban de un lugar a otro.</span><span class="sxs-lookup"><span data-stu-id="73011-116">Code patterns for searching the general ledger accounts and creating general ledger and VAT entries was not standardized and varied from place to place.</span></span> <span data-ttu-id="73011-117">Además, se producían muchas duplicaciones de código y corrupciones de simetría entre el código del cliente y el del proveedor.</span><span class="sxs-lookup"><span data-stu-id="73011-117">In addition, there was a lot of code duplication and broken symmetry between customer and vendor code.</span></span>  
* <span data-ttu-id="73011-118">Una gran parte del código en la codeunit 12, aproximadamente el 30 por ciento, relacionado con los cálculos de descuento de pago y tolerancia, aunque estas características no se necesitan en muchos países o regiones.</span><span class="sxs-lookup"><span data-stu-id="73011-118">A large part of the code in codeunit 12, approximately 30 percent, related to payment discount and tolerance calculations, although these features are not needed in many countries or regions.</span></span>  
* <span data-ttu-id="73011-119">Las funciones de Registro, Liquidar, Desliquidar, Revertir, Descuento de pago y Tolerancia y Ajuste tipo cambio se incluían todas en la codeunit 12 con una larga lista de variables globales.</span><span class="sxs-lookup"><span data-stu-id="73011-119">Posting, Apply, Unapply, Reverse, Payment Discount and Tolerance, and Exchange Rate Adjustment were married together in codeunit 12 using a long list of global variables.</span></span>  
  
### <a name="new-architecture"></a><span data-ttu-id="73011-120">Nueva arquitectura</span><span class="sxs-lookup"><span data-stu-id="73011-120">New Architecture</span></span>  
<span data-ttu-id="73011-121">En [!INCLUDE[prod_short](includes/prod_short.md)], la codeunit 12 incluye las mejoras siguientes:</span><span class="sxs-lookup"><span data-stu-id="73011-121">In [!INCLUDE[prod_short](includes/prod_short.md)], codeunit 12 has had the following improvements:</span></span>  
  
* <span data-ttu-id="73011-122">La codeunit 12 se ha refactorizado en procedimientos más pequeños (todos con menos de 100 líneas de código).</span><span class="sxs-lookup"><span data-stu-id="73011-122">Codeunit 12 has been refactored into smaller procedures (all less than 100 code lines).</span></span>  
* <span data-ttu-id="73011-123">Se han implementado patrones estandardizados para la búsqueda de cuentas de contabilidad mediante funciones de ayudante desde las tablas Grupo contable.</span><span class="sxs-lookup"><span data-stu-id="73011-123">Standardized patterns for the search of general ledger accounts have been implemented by using helper functions from Posting Group tables.</span></span>  
* <span data-ttu-id="73011-124">Se ha implementado un cuadro de motor de registro para gestionar el inicio y el fin de las transacciones y para aislar la creación en las entradas de IVA y de contabilidad, el cobro de ajustes de IVA y el cálculo de importes adicionales de divisa.</span><span class="sxs-lookup"><span data-stu-id="73011-124">A Posting Engine Framework has been implemented to manage the start and finish of transactions and to isolate the creation to general ledger and VAT entries, the collection of VAT adjustment, and the calculation of additional currency amounts.</span></span>  
* <span data-ttu-id="73011-125">Se ha eliminado la duplicación del código.</span><span class="sxs-lookup"><span data-stu-id="73011-125">Code duplication has been eliminated.</span></span>  
* <span data-ttu-id="73011-126">Muchas funciones de ayuda se han transferido a las tablas correspondientes de movimientos de cliente y de proveedor.</span><span class="sxs-lookup"><span data-stu-id="73011-126">Many helper functions have been transferred to corresponding customer and vendor ledger entry tables.</span></span>  
* <span data-ttu-id="73011-127">El uso de variables globales se ha minimizado, de modo que cada procedimiento utiliza parámetros y encapsula su propia lógica de aplicación.</span><span class="sxs-lookup"><span data-stu-id="73011-127">The use of global variables has been minimized, so that each procedure uses parameters and encapsulates its own application logic.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="73011-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="73011-128">See Also</span></span>

[<span data-ttu-id="73011-129">Detalles de diseño: estructura de interfaz de registro</span><span class="sxs-lookup"><span data-stu-id="73011-129">Design Details: Posting Interface Structure</span></span>](design-details-posting-interface-structure.md)  
[<span data-ttu-id="73011-130">Detalles de diseño: estructura de motor de registro</span><span class="sxs-lookup"><span data-stu-id="73011-130">Design Details: Posting Engine Structure</span></span>](design-details-posting-engine-structure.md)  
[<span data-ttu-id="73011-131">Detalles de diseño: línea de registro en diario general (Dynamics NAV)</span><span class="sxs-lookup"><span data-stu-id="73011-131">Design Details: General Journal Post Line (Dynamics NAV)</span></span>](/dynamics-nav-app/design-details-general-journal-post-line)  


[!INCLUDE[footer-include](includes/footer-banner.md)]