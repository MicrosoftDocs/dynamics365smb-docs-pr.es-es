---
title: "Configurar métodos preferidos para enviar documentos de venta | Documentos de Microsoft"
description: "Describe cómo configurar el método preferido de cada cliente de enviar documentos de venta, por ejemplo, correo electrónico, PDF, documento electrónico, etc."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: email, PDF, electronic document
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 974e0567b1207eb3dd2204f1d90e9b65061cbc54
ms.contentlocale: es-es
ms.lasthandoff: 01/30/2018

---
# <a name="set-up-document-sending-profiles"></a><span data-ttu-id="91b13-103">Configurar perfiles de envío de documentos</span><span class="sxs-lookup"><span data-stu-id="91b13-103">Set Up Document Sending Profiles</span></span>
<span data-ttu-id="91b13-104">Puede configurar cada cliente con un método preferido para enviar documentos de venta, de modo que no tenga que seleccionar una opción de envío cada vez que elija la acción **Registrar y enviar**.</span><span class="sxs-lookup"><span data-stu-id="91b13-104">You can set each customer up with a preferred method of sending sales documents, so that you do not have to select a sending option every time you choose the **Post and Send** action.</span></span>

<span data-ttu-id="91b13-105">En la ventana **Perfiles de envío de documentos**, puede establecer diferentes perfiles de envío que puede seleccionar del campo **Perfil de envío de documentos** de una ficha de cliente.</span><span class="sxs-lookup"><span data-stu-id="91b13-105">In the **Document Sending Profiles** window, you set up different sending profiles that you can select from in the **Document Sending Profile** field on a customer card.</span></span> <span data-ttu-id="91b13-106">Puede seleccionar la casilla de verificación **Predeterminado** para especificar que el perfil de envíos de documentos sea el perfil predeterminado para todos los clientes, en que el campo **Perfil de envío de documentos** se rellena con otro perfil de envío.</span><span class="sxs-lookup"><span data-stu-id="91b13-106">You can select the **Default** check box to specify that the document sending profile is the default profile for all customers, except for customers where the **Document Sending Profile** field is filled with another sending profile.</span></span>

<span data-ttu-id="91b13-107">Cuando elige la acción **Registrar y enviar** en un documento de venta, el cuadro de diálogo **Registrar y enviar confirmación** muestra el perfil de envío usado, tanto el configurado para el cliente como el predeterminado para todos los clientes.</span><span class="sxs-lookup"><span data-stu-id="91b13-107">When you choose the **Post and Send** action on a sales document, the **Post and Send Confirmation** dialog box shows the sending profile used, either the one set up for the customer or the default for all customers.</span></span> <span data-ttu-id="91b13-108">En el cuadro de diálogo puede cambiar el perfil de envío para el documento de venta.</span><span class="sxs-lookup"><span data-stu-id="91b13-108">In the dialog box, you can change the sending profile for the sales document.</span></span> <span data-ttu-id="91b13-109">Para obtener más información, vea [Facturar ventas](sales-how-invoice-sales.md).</span><span class="sxs-lookup"><span data-stu-id="91b13-109">For more information, see [Invoice Sales](sales-how-invoice-sales.md).</span></span>

## <a name="to-set-up-a-document-sending-profile"></a><span data-ttu-id="91b13-110">Para configurar un perfil de envío de documentos</span><span class="sxs-lookup"><span data-stu-id="91b13-110">To set up a document sending profile</span></span>
1. <span data-ttu-id="91b13-111">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Perfiles de envío de documentos** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="91b13-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Document Sending Profiles**, and then choose the related link.</span></span>
2. <span data-ttu-id="91b13-112">En la ventana **Perfiles de envío de documentos**, elija la acción **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="91b13-112">In the **Document Sending Profiles** window, choose the **New** action.</span></span>
3. <span data-ttu-id="91b13-113">Rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="91b13-113">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-specify-a-sending-profile-on-a-customer-card"></a><span data-ttu-id="91b13-114">Para especificar un perfil de envío en una ficha cliente</span><span class="sxs-lookup"><span data-stu-id="91b13-114">To specify a sending profile on a customer card</span></span>
1. <span data-ttu-id="91b13-115">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Clientes** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="91b13-115">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Customers**, and then choose the related link.</span></span>
2. <span data-ttu-id="91b13-116">Abra la ficha del cliente para el que desea configurar un perfil de envío.</span><span class="sxs-lookup"><span data-stu-id="91b13-116">Open the card of the customer who you want to set up a sending profile for.</span></span>
3. <span data-ttu-id="91b13-117">En el campo **Perfil de envío de documentos**, seleccione un perfil que haya configurado como se describe en el procedimiento anterior.</span><span class="sxs-lookup"><span data-stu-id="91b13-117">In the **Document Sending Profile** field, select a profile that you have set up as described in the previous procedure.</span></span>

## <a name="see-also"></a><span data-ttu-id="91b13-118">Consulte también</span><span class="sxs-lookup"><span data-stu-id="91b13-118">See Also</span></span>
[<span data-ttu-id="91b13-119">Configuración de ventas</span><span class="sxs-lookup"><span data-stu-id="91b13-119">Setting Up Sales</span></span>](sales-setup-sales.md)  
[<span data-ttu-id="91b13-120">Ventas</span><span class="sxs-lookup"><span data-stu-id="91b13-120">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="91b13-121">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="91b13-121">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

