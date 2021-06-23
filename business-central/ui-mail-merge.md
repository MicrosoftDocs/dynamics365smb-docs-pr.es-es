---
title: Uso de plantillas de Word para comunicaciones masivas | Microsoft Docs
description: Las plantillas de Word pueden facilitar la creación masiva de documentos personalizados para entidades específicas.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: document, mail, merge, Word, template, email
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: d29e29eca7dfc24ded51aed994ac7003fb4d30ab
ms.sourcegitcommit: 6bce51954f17b80491e180f25d67ff18b1618a88
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/27/2021
ms.locfileid: "6110959"
---
# <a name="using-word-templates-for-bulk-communication"></a><span data-ttu-id="607e8-103">Uso de plantillas de Word para comunicaciones masivas</span><span class="sxs-lookup"><span data-stu-id="607e8-103">Using Word Templates for Bulk Communication</span></span>
<span data-ttu-id="607e8-104">Las plantillas de Microsoft Word pueden facilitar la comunicación masiva con entidades como clientes y proveedores.</span><span class="sxs-lookup"><span data-stu-id="607e8-104">Microsoft Word templates can make it easier to mass communicate with entities such as customers and vendors.</span></span> <span data-ttu-id="607e8-105">Por ejemplo, puede crear folletos para alertar a los clientes sobre una campaña de ventas, cartas para informar a los proveedores sobre una nueva directiva de compras o invitaciones para atraer contactos a un próximo evento.</span><span class="sxs-lookup"><span data-stu-id="607e8-105">For example, you can create brochures to alert customers about a sales campaign, letters to inform vendors about a new purchasing policy, or invitations to attract contacts to an upcoming event.</span></span>

> [!NOTE]
> <span data-ttu-id="607e8-106">Puede usar plantillas de Word solo en dispositivos con Microsoft Word 2019 y el sistema operativo Windows instalado.</span><span class="sxs-lookup"><span data-stu-id="607e8-106">You can use Word templates only on devices with Microsoft Word 2019 and the Windows operating system installed.</span></span>

<span data-ttu-id="607e8-107">Puede usar entidades en [!INCLUDE[prod_short](includes/prod_short.md)] como origen de datos para la plantilla y agregar campos de combinación para personalizar documentos para cada entidad.</span><span class="sxs-lookup"><span data-stu-id="607e8-107">You can use entities in [!INCLUDE[prod_short](includes/prod_short.md)] as the data source for the template, and add merge fields to personalize documents for each entity.</span></span> <span data-ttu-id="607e8-108">Los campos de combinación proceden de la entidad en [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="607e8-108">The merge fields come from the entity in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="607e8-109">Cuando aplica una plantilla de Word a una entidad, los datos de los campos de combinación se insertan en el documento.</span><span class="sxs-lookup"><span data-stu-id="607e8-109">When you apply a Word template to an entity, data from the merge fields is inserted in the document.</span></span>

<span data-ttu-id="607e8-110">En la página **Plantillas de Word**, puede usar una guía de configuración asistida para descargar un archivo ZIP que contiene un DataSource.txt y un archivo de plantilla de Word para una entidad.</span><span class="sxs-lookup"><span data-stu-id="607e8-110">On the **Word Templates** page, you can use an assisted setup guide to download a ZIP file that contains a DataSource.txt and a Word template file for an entity.</span></span> <span data-ttu-id="607e8-111">Después de configurar la plantilla y agregar campos de combinación, use la misma guía para cargar la plantilla.</span><span class="sxs-lookup"><span data-stu-id="607e8-111">After you set up the template and add merge fields, you use the same guide to upload the template.</span></span> <span data-ttu-id="607e8-112">Solo puede usar la plantilla de Word y los archivos de origen de datos que descargue desde [!INCLUDE[prod_short](includes/prod_short.md)] y debe almacenar los archivos en la misma ubicación.</span><span class="sxs-lookup"><span data-stu-id="607e8-112">You can only use the Word template and data source files that you download from [!INCLUDE[prod_short](includes/prod_short.md)], and you must store the files in the same location.</span></span>

> [!NOTE]
> <span data-ttu-id="607e8-113">Cuando elige una entidad para la que crear una plantilla, la lista muestra todas las entidades en [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="607e8-113">When you choose an entity for which to create a template, the list shows all entities in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="607e8-114">Sin embargo, no puede crear plantillas para todas las entidades.</span><span class="sxs-lookup"><span data-stu-id="607e8-114">However, you cannot create templates for all entities.</span></span> <span data-ttu-id="607e8-115">Si el nombre de una entidad contiene caracteres especiales, como **/**, **.**, **_**, o **-**, no puede crear una plantilla para este.</span><span class="sxs-lookup"><span data-stu-id="607e8-115">If the name of an entity contains special characters, such as **/**, **.**, **_**, or **-**, you cannot create a template for it.</span></span> <span data-ttu-id="607e8-116">El nombre de la entidad se muestra en la columna **Título de objeto**</span><span class="sxs-lookup"><span data-stu-id="607e8-116">The name of the entity is shown in the **Object Caption** column.</span></span>

<span data-ttu-id="607e8-117">Cuando está configurando la plantilla en Word, en la pestaña **Correspondencia** puede agregar campos de combinación seleccionando **Insertar campo combinación**.</span><span class="sxs-lookup"><span data-stu-id="607e8-117">When you are setting up the template in Word, on the **Mailings** tab you can add merge fields by choosing **Insert Merge Field**.</span></span>

> [!NOTE]
> <span data-ttu-id="607e8-118">No puede usar campos de combinación si el nombre del campo contiene 40 caracteres o más.</span><span class="sxs-lookup"><span data-stu-id="607e8-118">You cannot use merge fields if the name of the field contains 40 characters or more.</span></span> <span data-ttu-id="607e8-119">Por ejemplo, no puede usar el campo Company__Information_Customs_Permit_Date porque tiene 40 caracteres.</span><span class="sxs-lookup"><span data-stu-id="607e8-119">For example, you cannot use the Company__Information_Customs_Permit_Date field because it has 40 characters.</span></span> 

<span data-ttu-id="607e8-120">Cuando su plantilla de Word esté lista, en la página **Plantillas de Word** puede elegir **Aplicar** para generar los documentos.</span><span class="sxs-lookup"><span data-stu-id="607e8-120">When your Word template is ready, on the **Word Templates** page you can choose **Apply** to generate the documents.</span></span> <span data-ttu-id="607e8-121">Puede crear un documento que contenga secciones para cada entidad o dividir la operación para crear un nuevo documento para cada entidad.</span><span class="sxs-lookup"><span data-stu-id="607e8-121">You can either create one document that contains sections for each entity, or split the operation to create a new document for each entity.</span></span>

## <a name="to-create-a-word-template"></a><span data-ttu-id="607e8-122">Para crear una plantilla de Word</span><span class="sxs-lookup"><span data-stu-id="607e8-122">To create a Word template</span></span>
1. <span data-ttu-id="607e8-123">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Plantillas de Word** y luego elija el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="607e8-123">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Word Templates**, and then choose the related link.</span></span>
2. <span data-ttu-id="607e8-124">Siga los pasos de la guía de configuración asistida.</span><span class="sxs-lookup"><span data-stu-id="607e8-124">Follow the steps in the assisted setup guide.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-also"></a><span data-ttu-id="607e8-125">Consulte también</span><span class="sxs-lookup"><span data-stu-id="607e8-125">See Also</span></span>
[<span data-ttu-id="607e8-126">Administrar diseños de informes y documentos</span><span class="sxs-lookup"><span data-stu-id="607e8-126">Managing Report and Document Layouts</span></span>](ui-manage-report-layouts.md)  
