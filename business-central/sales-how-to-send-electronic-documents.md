---
title: Enviar documentos electrónicos
description: Aprenda a enviar facturas electrónicamente.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: d547f031d9d33c0d7cd5f8b20398fd7b6dbe0393
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5383005"
---
# <a name="send-electronic-documents"></a><span data-ttu-id="c815d-103">Enviar documentos electrónicos</span><span class="sxs-lookup"><span data-stu-id="c815d-103">Send Electronic Documents</span></span>

<span data-ttu-id="c815d-104">La versión genérica de [!INCLUDE[prod_short](includes/prod_short.md)] admite el envío de facturas electrónicas y abonos en formato PEPPOL, un formato admitido por los proveedores de servicios de intercambio de documentos más importantes.</span><span class="sxs-lookup"><span data-stu-id="c815d-104">The generic version of [!INCLUDE[prod_short](includes/prod_short.md)] supports sending electronic invoices and credit memos in the PEPPOL format, a format that the largest document exchange service providers support.</span></span> <span data-ttu-id="c815d-105">El proveedor de servicios de intercambio de documentos entrega documentos electrónicos de un socio comercial a otro.</span><span class="sxs-lookup"><span data-stu-id="c815d-105">A document exchange service provider dispatches electronic documents between trading partners.</span></span> <span data-ttu-id="c815d-106">Para proporcionar compatibilidad con otros formatos de documento electrónico, utilice el marco de intercambio de datos.</span><span class="sxs-lookup"><span data-stu-id="c815d-106">To provide support for other electronic document formats, you use the data exchange framework.</span></span>  

 <span data-ttu-id="c815d-107">En la versión genérica de [!INCLUDE[prod_short](includes/prod_short.md)], hay preconfigurado un servicio de intercambio de documentos listo para ser configurado según su empresa.</span><span class="sxs-lookup"><span data-stu-id="c815d-107">In the generic version of [!INCLUDE[prod_short](includes/prod_short.md)], a document exchange service is preconfigured and ready to be set up for your company.</span></span> <span data-ttu-id="c815d-108">Para obtener más información, vea [Configurar un servicio de intercambio de documentos](across-how-to-set-up-a-document-exchange-service.md).</span><span class="sxs-lookup"><span data-stu-id="c815d-108">For more information, see [Set Up a Document Exchange Service](across-how-to-set-up-a-document-exchange-service.md).</span></span> <span data-ttu-id="c815d-109">Sin embargo, en algunos casos, debe instalar una aplicación.</span><span class="sxs-lookup"><span data-stu-id="c815d-109">However, in some cases, you must install an app.</span></span> <span data-ttu-id="c815d-110">Para más información, vea [Preguntas frecuentes sobre facturación electrónica](faq-electronic-invoicing.yml).</span><span class="sxs-lookup"><span data-stu-id="c815d-110">For more information, see [Electronic Invoicing FAQ](faq-electronic-invoicing.yml).</span></span>  

 <span data-ttu-id="c815d-111">Para enviar una factura de venta como documento electrónico de PEPPOL, seleccione la opción **Documento electrónico** en el cuadro de diálogo **Registrar y enviar**.</span><span class="sxs-lookup"><span data-stu-id="c815d-111">To send a sales invoice as an electronic PEPPOL document, you select the **Electronic Document** option in the **Post and Send** dialog box.</span></span> <span data-ttu-id="c815d-112">Puede configurar también perfil de envío de documentos predeterminado del cliente desde ese cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="c815d-112">You can also set up the customer's default document sending profile from that dialog box.</span></span> <span data-ttu-id="c815d-113">En primer lugar, debe configurar los distintos datos maestros, como la información de la empresa, los clientes, los productos y las unidades de medida.</span><span class="sxs-lookup"><span data-stu-id="c815d-113">First, you must set up various master data, such as company information, customers, items, and units of measure.</span></span> <span data-ttu-id="c815d-114">Se utilizan para identificar a los socios comerciales y los productos al convertir los datos de los campos de [Configurar el envío y la recepción de documentos electrónicos](across-how-to-set-up-electronic-document-sending-and-receiving.md)</span><span class="sxs-lookup"><span data-stu-id="c815d-114">These are used to identify the business partners and items when converting data in fields in [Set Up Electronic Document Sending and Receiving](across-how-to-set-up-electronic-document-sending-and-receiving.md).</span></span>  

### <a name="to-send-an-electronic-sales-invoice"></a><span data-ttu-id="c815d-115">Para enviar una factura de venta electrónica</span><span class="sxs-lookup"><span data-stu-id="c815d-115">To send an electronic sales invoice</span></span>

1. <span data-ttu-id="c815d-116">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Facturas venta** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="c815d-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Invoices**, and then choose the related link.</span></span>  

2. <span data-ttu-id="c815d-117">Cree una nueva factura de venta.</span><span class="sxs-lookup"><span data-stu-id="c815d-117">Create a new sales invoice.</span></span>  

3. <span data-ttu-id="c815d-118">Cuando la factura de venta esté lista para facturarse, seleccione la acción **Registrar y enviar**.</span><span class="sxs-lookup"><span data-stu-id="c815d-118">When the sales invoice is ready to be invoiced, choose the **Post and Send** action.</span></span>  

     <span data-ttu-id="c815d-119">Si el perfil de envío predeterminado del cliente es **Documento electrónico**, entonces se mostrará en el cuadro de diálogo **Publicar y enviar confirmación**.</span><span class="sxs-lookup"><span data-stu-id="c815d-119">If the customer's default sending profile is **Electronic Document**, then it will be shown in the **Post and Send Confirmation** dialog box.</span></span> <span data-ttu-id="c815d-120">De esta forma, solo tiene que elegir el botón **Sí** para contabilizar y enviar la factura de forma electrónica en el formato seleccionado.</span><span class="sxs-lookup"><span data-stu-id="c815d-120">This way, you just have to choose the **Yes** button to post and send the invoice electronically in the selected format.</span></span>  

4. <span data-ttu-id="c815d-121">En el cuadro de diálogo **Registrar y enviar la confirmación**, seleccione el botón AssistEdit situado a la derecha del campo **Enviar documento a**.</span><span class="sxs-lookup"><span data-stu-id="c815d-121">In the **Post and Send Confirmation** dialog box, choose the AssistEdit button to the right of the **Send Document to** field.</span></span>  

5. <span data-ttu-id="c815d-122">En el cuadro de diálogo **Enviar documento a**, en el campo **Documento electrónico**, seleccione **A través del servicio de intercambio de documentos**.</span><span class="sxs-lookup"><span data-stu-id="c815d-122">In the **Send Document to** dialog box, in the **Electronic Document** field, choose **Through Document Exchange Service**.</span></span>  

6. <span data-ttu-id="c815d-123">En el campo **Formato**, seleccione **PEPPOL**.</span><span class="sxs-lookup"><span data-stu-id="c815d-123">In the **Format** field, choose **PEPPOL**.</span></span>  

7. <span data-ttu-id="c815d-124">Elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="c815d-124">Choose the **OK** button.</span></span> <span data-ttu-id="c815d-125">Aparece el cuadro de diálogo **Registrar y enviar la confirmación**.</span><span class="sxs-lookup"><span data-stu-id="c815d-125">The **Post and Send Confirmation** dialog box appears.</span></span> <span data-ttu-id="c815d-126">**Documento electrónico (PEPPOL)** se agrega al campo **Enviar documento a**.</span><span class="sxs-lookup"><span data-stu-id="c815d-126">**Electronic Document (PEPPOL)** is added to the **Send Document to** field.</span></span>  

8. <span data-ttu-id="c815d-127">Elija el botón **Sí**.</span><span class="sxs-lookup"><span data-stu-id="c815d-127">Choose the **Yes** button.</span></span>  

     <span data-ttu-id="c815d-128">Se registra la factura de venta y se envía al cliente en el formato PEPPOL.</span><span class="sxs-lookup"><span data-stu-id="c815d-128">The sales invoice is posted and sent to the customer in the PEPPOL format.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="c815d-129">También puede enviar una factura de venta registrada como documento electrónico.</span><span class="sxs-lookup"><span data-stu-id="c815d-129">You can also send a posted sales invoice as an electronic document.</span></span> <span data-ttu-id="c815d-130">El procedimiento es el mismo que el descrito en este tema para documentos de venta no registrada.</span><span class="sxs-lookup"><span data-stu-id="c815d-130">The procedure is the same as described in this topic for non-posted sales documents.</span></span> <span data-ttu-id="c815d-131">En la página **Factura venta reg.**, elija la acción **Registro de actividades** para ver el estado del documento electrónico.</span><span class="sxs-lookup"><span data-stu-id="c815d-131">On the **Posted Sales Invoice** page, choose the **Activity Log** action to view the status of the electronic document.</span></span>  

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="c815d-132">Consulte Formación relacionada en [Microsoft Learn](/learn/modules/electronic-documents-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="c815d-132">See Related Training at [Microsoft Learn](/learn/modules/electronic-documents-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="c815d-133">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c815d-133">See Also</span></span>

[<span data-ttu-id="c815d-134">Facturar ventas</span><span class="sxs-lookup"><span data-stu-id="c815d-134">Invoice Sales</span></span>](sales-how-invoice-sales.md)  
[<span data-ttu-id="c815d-135">Configurar perfiles de envío de documentos</span><span class="sxs-lookup"><span data-stu-id="c815d-135">Set Up Document Sending Profiles</span></span>](sales-how-setup-document-send-profiles.md)  
[<span data-ttu-id="c815d-136">Configurar el envío y la recepción de documentos electrónicos</span><span class="sxs-lookup"><span data-stu-id="c815d-136">Set Up Electronic Document Sending and Receiving</span></span>](across-how-to-set-up-electronic-document-sending-and-receiving.md)  
[<span data-ttu-id="c815d-137">Configurar un servicio de intercambio de documentos</span><span class="sxs-lookup"><span data-stu-id="c815d-137">Set Up a Document Exchange Service</span></span>](across-how-to-set-up-a-document-exchange-service.md)  
[<span data-ttu-id="c815d-138">Configurar definiciones de intercambio de datos</span><span class="sxs-lookup"><span data-stu-id="c815d-138">Set Up Data Exchange Definitions</span></span>](across-how-to-set-up-data-exchange-definitions.md)  
[<span data-ttu-id="c815d-139">Intercambio de datos electrónicamente</span><span class="sxs-lookup"><span data-stu-id="c815d-139">Exchanging Data Electronically</span></span>](across-data-exchange.md)  
[<span data-ttu-id="c815d-140">P+F sobre facturación electrónica</span><span class="sxs-lookup"><span data-stu-id="c815d-140">Electronic Invoicing FAQ</span></span>](faq-electronic-invoicing.yml)  
[<span data-ttu-id="c815d-141">Funciones empresariales generales</span><span class="sxs-lookup"><span data-stu-id="c815d-141">General Business Functionality</span></span>](ui-across-business-areas.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]