---
title: Enviar documentos electrónicos | Documentos de Microsoft
description: Aprenda a enviar facturas electrónicamente.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 8cb28db63e977cf02b81daa7043b64838406161f
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/29/2019
ms.locfileid: "1251612"
---
# <a name="send-electronic-documents"></a><span data-ttu-id="dabf0-103">Enviar documentos electrónicos</span><span class="sxs-lookup"><span data-stu-id="dabf0-103">Send Electronic Documents</span></span>
<span data-ttu-id="dabf0-104">La versión genérica de [!INCLUDE[d365fin](includes/d365fin_md.md)] admite el envío de facturas electrónicas y abonos en formato PEPPOL, admitido por los proveedores de servicios de intercambio de documentos más importantes.</span><span class="sxs-lookup"><span data-stu-id="dabf0-104">The generic version of [!INCLUDE[d365fin](includes/d365fin_md.md)] supports sending electronic invoices and credit memos in the PEPPOL format, which is supported by the largest document exchange service providers.</span></span> <span data-ttu-id="dabf0-105">El proveedor de servicios de intercambio de documentos entrega documentos electrónicos de un socio comercial a otro.</span><span class="sxs-lookup"><span data-stu-id="dabf0-105">A document exchange service provider dispatches electronic documents between trading partners.</span></span> <span data-ttu-id="dabf0-106">Para proporcionar compatibilidad con otros formatos de documento electrónico, utilice el marco de intercambio de datos.</span><span class="sxs-lookup"><span data-stu-id="dabf0-106">To provide support for other electronic document formats, you use the data exchange framework.</span></span>  

 <span data-ttu-id="dabf0-107">En la versión genérica de [!INCLUDE[d365fin](includes/d365fin_md.md)], hay preconfigurado un servicio de intercambio de documentos listo para ser configurado según su empresa.</span><span class="sxs-lookup"><span data-stu-id="dabf0-107">In the generic version of [!INCLUDE[d365fin](includes/d365fin_md.md)], a document exchange service is preconfigured and ready to be set up for your company.</span></span> <span data-ttu-id="dabf0-108">Para obtener más información, vea [Configurar un servicio de intercambio de documentos](across-how-to-set-up-a-document-exchange-service.md).</span><span class="sxs-lookup"><span data-stu-id="dabf0-108">For more information, see [Set Up a Document Exchange Service](across-how-to-set-up-a-document-exchange-service.md).</span></span>  

 <span data-ttu-id="dabf0-109">Para enviar una factura de venta como un documento electrónico PEPPOL, seleccione la opción **Documento electrónico** en el cuadro de diálogo **Registrar y enviar** donde también puede configurarlo como el perfil de envío de documentos predeterminado del cliente.</span><span class="sxs-lookup"><span data-stu-id="dabf0-109">To send a sales invoice as an electronic PEPPOL document, you select the **Electronic Document** option in the **Post and Send** dialog box from where you can also set up the customer’s default document sending profile.</span></span> <span data-ttu-id="dabf0-110">En primer lugar, debe configurar los distintos datos maestros, como la información de la empresa, los clientes, los productos y las unidades de medida.</span><span class="sxs-lookup"><span data-stu-id="dabf0-110">First, you must set up various master data, such as company information, customers, items, and units of measure.</span></span> <span data-ttu-id="dabf0-111">Se utilizan para identificar a los socios comerciales y los productos al convertir los datos de los campos de [Configurar el envío y la recepción de documentos electrónicos](across-how-to-set-up-electronic-document-sending-and-receiving.md)</span><span class="sxs-lookup"><span data-stu-id="dabf0-111">These are used to identify the business partners and items when converting data in fields in [Set Up Electronic Document Sending and Receiving](across-how-to-set-up-electronic-document-sending-and-receiving.md).</span></span>  

### <a name="to-send-an-electronic-sales-invoice"></a><span data-ttu-id="dabf0-112">Para enviar una factura de venta electrónica</span><span class="sxs-lookup"><span data-stu-id="dabf0-112">To send an electronic sales invoice</span></span>  

1.  <span data-ttu-id="dabf0-113">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Facturas ventas** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="dabf0-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Invoices**, and then choose the related link.</span></span>  

2.  <span data-ttu-id="dabf0-114">Cree una nueva factura de venta.</span><span class="sxs-lookup"><span data-stu-id="dabf0-114">Create a new sales invoice.</span></span>  

3.  <span data-ttu-id="dabf0-115">Cuando la factura de venta esté lista para facturarse, en la pestaña **Acciones**, en el grupo **Registro**, seleccione **Registrar y enviar**.</span><span class="sxs-lookup"><span data-stu-id="dabf0-115">When the sales invoice is ready to be invoiced, on the **Actions** tab, in the **Posting** group, choose **Post and Send**.</span></span>  

     <span data-ttu-id="dabf0-116">Si el perfil de envío predeterminado del cliente es **Documento electrónico**, se mostrará en el cuadro de diálogo **Registrar y enviar la confirmación** y solo tiene que elegir el botón **Sí** para registrar y enviar la factura electrónicamente en el formato seleccionado.</span><span class="sxs-lookup"><span data-stu-id="dabf0-116">If the customer’s default sending profile is **Electronic Document**, then it will be shown in the **Post and Send Confirmation** dialog box and you just have to choose the **Yes** button to post and send the invoice electronically in the selected format.</span></span>  

4.  <span data-ttu-id="dabf0-117">En el cuadro de diálogo **Registrar y enviar la confirmación**, seleccione el botón AssistEdit situado a la derecha del campo **Enviar documento a**.</span><span class="sxs-lookup"><span data-stu-id="dabf0-117">In the **Post and Send Confirmation** dialog box, choose the AssistEdit button to the right of the **Send Document to** field.</span></span>  

5.  <span data-ttu-id="dabf0-118">En el cuadro de diálogo **Enviar documento a**, en el campo **Documento electrónico**, seleccione **A través del servicio de intercambio de documentos**.</span><span class="sxs-lookup"><span data-stu-id="dabf0-118">In the **Send Document to** dialog box, in the **Electronic Document** field, choose **Through Document Exchange Service**.</span></span>  

6.  <span data-ttu-id="dabf0-119">En el campo **Formato**, seleccione **PEPPOL**.</span><span class="sxs-lookup"><span data-stu-id="dabf0-119">In the **Format** field, choose **PEPPOL**.</span></span>  

7.  <span data-ttu-id="dabf0-120">Elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="dabf0-120">Choose the **OK** button.</span></span> <span data-ttu-id="dabf0-121">Aparece el cuadro de diálogo **Registrar y enviar la confirmación**.</span><span class="sxs-lookup"><span data-stu-id="dabf0-121">The **Post and Send Confirmation** dialog box appears.</span></span> <span data-ttu-id="dabf0-122">**Documento electrónico (PEPPOL)** se agrega al campo **Enviar documento a**.</span><span class="sxs-lookup"><span data-stu-id="dabf0-122">**Electronic Document (PEPPOL)** is added to the **Send Document to** field.</span></span>  

8.  <span data-ttu-id="dabf0-123">Elija el botón **Sí**.</span><span class="sxs-lookup"><span data-stu-id="dabf0-123">Choose the **Yes** button.</span></span>  

     <span data-ttu-id="dabf0-124">Se registra la factura de venta y se envía al cliente como un documento electrónico en el formato PEPPOL.</span><span class="sxs-lookup"><span data-stu-id="dabf0-124">The sales invoice is posted and sent to the customer as an electronic document in the PEPPOL format.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="dabf0-125">También puede enviar una factura de venta registrada como documento electrónico.</span><span class="sxs-lookup"><span data-stu-id="dabf0-125">You can also send a posted sales invoice as an electronic document.</span></span> <span data-ttu-id="dabf0-126">El procedimiento es el mismo que el descrito en este tema para documentos de venta no registrada.</span><span class="sxs-lookup"><span data-stu-id="dabf0-126">The procedure is the same as described in this topic for non-posted sales documents.</span></span> <span data-ttu-id="dabf0-127">En la página **Factura venta reg.**, en la pestaña **Acciones**, en el grupo **General**, seleccione **Registro de actividades** para ver el estado del documento electrónico.</span><span class="sxs-lookup"><span data-stu-id="dabf0-127">On the **Posted Sales Invoice** page, on the **Actions** tab, in the **General** group, choose **Activity Log** to view the status of the electronic document.</span></span> <span data-ttu-id="dabf0-128">Para obtener más información, vea **Registro de actividades**.</span><span class="sxs-lookup"><span data-stu-id="dabf0-128">For more information, see **Activity Log**.</span></span>  

## <a name="see-also"></a><span data-ttu-id="dabf0-129">Consulte también</span><span class="sxs-lookup"><span data-stu-id="dabf0-129">See Also</span></span>  
[<span data-ttu-id="dabf0-130">Facturar ventas</span><span class="sxs-lookup"><span data-stu-id="dabf0-130">Invoice Sales</span></span>](sales-how-invoice-sales.md)  
[<span data-ttu-id="dabf0-131">Configurar perfiles de envío de documentos</span><span class="sxs-lookup"><span data-stu-id="dabf0-131">Set Up Document Sending Profiles</span></span>](sales-how-setup-document-send-profiles.md)  
[<span data-ttu-id="dabf0-132">Configurar el envío y la recepción de documentos electrónicos</span><span class="sxs-lookup"><span data-stu-id="dabf0-132">Set Up Electronic Document Sending and Receiving</span></span>](across-how-to-set-up-electronic-document-sending-and-receiving.md)  
[<span data-ttu-id="dabf0-133">Configurar un servicio de intercambio de documentos</span><span class="sxs-lookup"><span data-stu-id="dabf0-133">Set Up a Document Exchange Service</span></span>](across-how-to-set-up-a-document-exchange-service.md)  
[<span data-ttu-id="dabf0-134">Configurar definiciones de intercambio de datos</span><span class="sxs-lookup"><span data-stu-id="dabf0-134">Set Up Data Exchange Definitions</span></span>](across-how-to-set-up-data-exchange-definitions.md)  
[<span data-ttu-id="dabf0-135">Intercambio de datos electrónicamente</span><span class="sxs-lookup"><span data-stu-id="dabf0-135">Exchanging Data Electronically</span></span>](across-data-exchange.md)  
[<span data-ttu-id="dabf0-136">Funciones empresariales generales</span><span class="sxs-lookup"><span data-stu-id="dabf0-136">General Business Functionality</span></span>](ui-across-business-areas.md)  
