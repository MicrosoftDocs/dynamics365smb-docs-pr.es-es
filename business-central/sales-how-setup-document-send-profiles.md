---
title: Configurar métodos preferidos para enviar documentos de venta | Documentos de Microsoft
description: Describe cómo configurar el método preferido de cada cliente de enviar documentos de venta, por ejemplo, correo electrónico, PDF, documento electrónico, etc.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: email, PDF, electronic document
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 18f9fdf997608cc75fbf2736cc7a834787a8b414
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5387576"
---
# <a name="set-up-document-sending-profiles"></a><span data-ttu-id="9b794-103">Configurar perfiles de envío de documentos</span><span class="sxs-lookup"><span data-stu-id="9b794-103">Set Up Document Sending Profiles</span></span>
<span data-ttu-id="9b794-104">Puede configurar cada cliente con un método preferido para enviar documentos de venta, de modo que no tenga que seleccionar una opción de envío cada vez que elija la acción **Registrar y enviar**.</span><span class="sxs-lookup"><span data-stu-id="9b794-104">You can set each customer up with a preferred method of sending sales documents, so that you do not have to select a sending option every time you choose the **Post and Send** action.</span></span>

<span data-ttu-id="9b794-105">En la página **Perfiles de envío de documentos**, puede establecer diferentes perfiles de envío que puede seleccionar del campo **Perfil de envío de documentos** de una ficha de cliente.</span><span class="sxs-lookup"><span data-stu-id="9b794-105">On the **Document Sending Profiles** page, you set up different sending profiles that you can select from in the **Document Sending Profile** field on a customer card.</span></span> <span data-ttu-id="9b794-106">Puede seleccionar la casilla de verificación **Predeterminado** para especificar que el perfil de envíos de documentos sea el perfil predeterminado para todos los clientes, en que el campo **Perfil de envío de documentos** se rellena con otro perfil de envío.</span><span class="sxs-lookup"><span data-stu-id="9b794-106">You can select the **Default** check box to specify that the document sending profile is the default profile for all customers, except for customers where the **Document Sending Profile** field is filled with another sending profile.</span></span>

<span data-ttu-id="9b794-107">Cuando elige la acción **Registrar y enviar** en un documento de venta, el cuadro de diálogo **Registrar y enviar confirmación** muestra el perfil de envío usado, tanto el configurado para el cliente como el predeterminado para todos los clientes.</span><span class="sxs-lookup"><span data-stu-id="9b794-107">When you choose the **Post and Send** action on a sales document, the **Post and Send Confirmation** dialog box shows the sending profile used, either the one set up for the customer or the default for all customers.</span></span> <span data-ttu-id="9b794-108">En el cuadro de diálogo puede cambiar el perfil de envío para el documento de venta.</span><span class="sxs-lookup"><span data-stu-id="9b794-108">In the dialog box, you can change the sending profile for the sales document.</span></span> <span data-ttu-id="9b794-109">Para obtener más información, vea [Facturar ventas](sales-how-invoice-sales.md).</span><span class="sxs-lookup"><span data-stu-id="9b794-109">For more information, see [Invoice Sales](sales-how-invoice-sales.md).</span></span>
<br><br>  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4jzHH?rel=0]

## <a name="to-set-up-a-document-sending-profile"></a><span data-ttu-id="9b794-110">Para configurar un perfil de envío de documentos</span><span class="sxs-lookup"><span data-stu-id="9b794-110">To set up a document sending profile</span></span>
1. <span data-ttu-id="9b794-111">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), introduzca **Perfiles de envío de documentos** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="9b794-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Document Sending Profiles**, and then choose the related link.</span></span>
2. <span data-ttu-id="9b794-112">En la página **Perfiles de envío de documentos**, elija la acción **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="9b794-112">On the **Document Sending Profiles** page, choose the **New** action.</span></span>
3. <span data-ttu-id="9b794-113">Rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="9b794-113">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-specify-a-sending-profile-on-a-customer-card"></a><span data-ttu-id="9b794-114">Para especificar un perfil de envío en una ficha cliente</span><span class="sxs-lookup"><span data-stu-id="9b794-114">To specify a sending profile on a customer card</span></span>
1. <span data-ttu-id="9b794-115">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Clientes** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="9b794-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Customers**, and then choose the related link.</span></span>
2. <span data-ttu-id="9b794-116">Abra la ficha del cliente para el que desea configurar un perfil de envío.</span><span class="sxs-lookup"><span data-stu-id="9b794-116">Open the card of the customer who you want to set up a sending profile for.</span></span>
3. <span data-ttu-id="9b794-117">En el campo **Perfil de envío de documentos**, seleccione un perfil que haya configurado como se describe en el procedimiento anterior.</span><span class="sxs-lookup"><span data-stu-id="9b794-117">In the **Document Sending Profile** field, select a profile that you have set up as described in the previous procedure.</span></span>

## <a name="see-also"></a><span data-ttu-id="9b794-118">Consulte también</span><span class="sxs-lookup"><span data-stu-id="9b794-118">See Also</span></span>
[<span data-ttu-id="9b794-119">Configuración de ventas</span><span class="sxs-lookup"><span data-stu-id="9b794-119">Setting Up Sales</span></span>](sales-setup-sales.md)  
[<span data-ttu-id="9b794-120">Ccial</span><span class="sxs-lookup"><span data-stu-id="9b794-120">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="9b794-121">[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="9b794-121">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]