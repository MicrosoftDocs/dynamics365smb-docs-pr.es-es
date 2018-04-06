---
title: "Definir los códigos de relaciones de negocio en contactos | Documentos de Microsoft"
description: Utilice las relaciones de negocio en Finance and Operations, Business edition como ayuda con el marketing y para indicar las relaciones de ese tipo con los clientes potenciales y los clientes, por ejemplo, un banco o un proveedor de servicios.
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: marketing, prospect, contact, client, customer
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: a72563f5057a1f9136a2d2b3aced6f028dc24051
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="setting-up-business-relations-on-contact-companies"></a><span data-ttu-id="c9eee-103">Configurar relaciones de negocio en empresas de contacto</span><span class="sxs-lookup"><span data-stu-id="c9eee-103">Setting Up Business Relations on Contact Companies</span></span>
<span data-ttu-id="c9eee-104">Puede usar relaciones de negocio se usan para indicar las relaciones de ese tipo con los contactos, por ejemplo, referencia, banco, consultora, proveedor de servicios, etc.</span><span class="sxs-lookup"><span data-stu-id="c9eee-104">You can use business relations to indicate the business relationship you have with your contacts, for example, a prospect, bank, consultant, service supplier, and so on.</span></span>

<span data-ttu-id="c9eee-105">El uso relaciones de negocio en contactos es un proceso que consta de dos pasos.</span><span class="sxs-lookup"><span data-stu-id="c9eee-105">Using business relations on contacts is a two-step process.</span></span> <span data-ttu-id="c9eee-106">Primero, debe definir el código de relación de negocio.</span><span class="sxs-lookup"><span data-stu-id="c9eee-106">First, you define the business relation code.</span></span> <span data-ttu-id="c9eee-107">Solo debe realizar este paso una vez para cada relación de negocio.</span><span class="sxs-lookup"><span data-stu-id="c9eee-107">You only have to perform this step one time for each business relation.</span></span> <span data-ttu-id="c9eee-108">Una vez tenga un código de relación de negocio, puede comenzar a asignar el código a empresas de contacto.</span><span class="sxs-lookup"><span data-stu-id="c9eee-108">Once you have a business relation code, you can start to assign the code to contact companies.</span></span>

> [!NOTE]  
>   <span data-ttu-id="c9eee-109">Si desea sincronizar sus contactos con proveedores, clientes o bancos en otras partes de la aplicación, se recomienda configurar una relación de negocio para ellos.</span><span class="sxs-lookup"><span data-stu-id="c9eee-109">If you plan to synchronize your contacts with vendors, customers, or bank accounts in other parts of the application, you may want to set up a business relation for them.</span></span>

## <a name="to-define-a-business-relation-code"></a><span data-ttu-id="c9eee-110">Para definir un código de relación de negocio</span><span class="sxs-lookup"><span data-stu-id="c9eee-110">To define a business relation code</span></span>
<span data-ttu-id="c9eee-111">El código de relación de negocio define una categoría o un tipo de relación de negocio, como BANCO o ABO.</span><span class="sxs-lookup"><span data-stu-id="c9eee-111">The business relation code defines a category or type of the business relationship, such as BANK or Law.</span></span> <span data-ttu-id="c9eee-112">Puede tener varios códigos de relación de negocio.</span><span class="sxs-lookup"><span data-stu-id="c9eee-112">You can have several business relation codes.</span></span> <span data-ttu-id="c9eee-113">Para definir relaciones de negocio, use la ventana **Relaciones de negocio**.</span><span class="sxs-lookup"><span data-stu-id="c9eee-113">To define the business relation, you use the **Business Relations** window.</span></span>

1. <span data-ttu-id="c9eee-114">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Relaciones negocio** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="c9eee-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Business Relations**, and then choose the related link.</span></span>
2. <span data-ttu-id="c9eee-115">Seleccione la acción **Nuevo** e introduzca un código y una descripción.</span><span class="sxs-lookup"><span data-stu-id="c9eee-115">Choose the **New** action, and fill in a code and description.</span></span> <span data-ttu-id="c9eee-116">El código admite un máximo de 11 caracteres y puede ser cualquier combinación de números y letras.</span><span class="sxs-lookup"><span data-stu-id="c9eee-116">The code can be a maximum of 11 characters, and can be any combination of numbers and letters.</span></span>

## <a name="AssignBusRelContact"></a> <span data-ttu-id="c9eee-117">Para asignar relaciones de negocio a un contacto</span><span class="sxs-lookup"><span data-stu-id="c9eee-117">To assign business relations to a contact</span></span>
<span data-ttu-id="c9eee-118">No puede asignar relaciones de contacto a una persona de contacto, solo a empresas.</span><span class="sxs-lookup"><span data-stu-id="c9eee-118">You cannot assign business relations to a contact person - only companies.</span></span>

1. <span data-ttu-id="c9eee-119">Abra el contacto.</span><span class="sxs-lookup"><span data-stu-id="c9eee-119">Open the contact.</span></span>
2. <span data-ttu-id="c9eee-120">Seleccione la acción **Empresa** y, a continuación, seleccione la acción **Relaciones de negocio**.</span><span class="sxs-lookup"><span data-stu-id="c9eee-120">Choose the **Company** action, and then the **Business Relations** action.</span></span>

    <span data-ttu-id="c9eee-121">Se abre la ventana **Relaciones de negocio de contacto**.</span><span class="sxs-lookup"><span data-stu-id="c9eee-121">The **Contact Business Relations** window opens.</span></span>
3. <span data-ttu-id="c9eee-122">En el campo **Cód. relación negocio**, seleccione la relación de negocio que desea asignar.</span><span class="sxs-lookup"><span data-stu-id="c9eee-122">In the **Business Relation Code** field, select the business relation you want to assign.</span></span>

<span data-ttu-id="c9eee-123">Repita estos pasos para asignar todos las relaciones de negocio que desee.</span><span class="sxs-lookup"><span data-stu-id="c9eee-123">Repeat these steps to assign as many business relations as you want.</span></span> <span data-ttu-id="c9eee-124">También puede asignar relaciones de negocio desde la lista de contactos con el mismo procedimiento.</span><span class="sxs-lookup"><span data-stu-id="c9eee-124">You can also assign business relations from the contact list by following the same procedure.</span></span>

<span data-ttu-id="c9eee-125">Aparece automáticamente el número de relaciones de negocio asignadas al contacto del campo **N.º de relaciones de negocio** en la sección **Segmentación** de la ventana **Contacto**.</span><span class="sxs-lookup"><span data-stu-id="c9eee-125">The number of business relations you have assigned to the contact is displayed in the **No. of Business Relations** field in the **Segmentation** section in the **Contact** window.</span></span>

<span data-ttu-id="c9eee-126">Después de asignar relaciones de negocio a sus contactos, puede utilizar esa información para seleccionar contactos para sus segmentos.</span><span class="sxs-lookup"><span data-stu-id="c9eee-126">After you have assigned business relations to your contacts, you can use this information to select contacts for your segments.</span></span> <span data-ttu-id="c9eee-127">Para obtener más información, vea [Agregar contactos a segmentos](marketing-add-contact-segment.md).</span><span class="sxs-lookup"><span data-stu-id="c9eee-127">For more information, see [Add Contacts to Segments](marketing-add-contact-segment.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="c9eee-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c9eee-128">See Also</span></span>
[<span data-ttu-id="c9eee-129">Crear empresas de contacto</span><span class="sxs-lookup"><span data-stu-id="c9eee-129">Creating Contact Companies</span></span>](marketing-create-contact-companies.md)  
<span data-ttu-id="c9eee-130">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c9eee-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

