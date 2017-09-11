---
title: Vincular contactos con clientes y proveedores | Documentos de Microsoft
description: "Describe cómo vincular un contacto con un cliente, proveedor o banco de la misma empresa, para poder sincronizar datos comunes."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: f5bbadb37a40dbc7b06668d940d2be9569aaa8e8
ms.contentlocale: es-es
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-link-contacts-with-customers-vendors-and-bank-accounts"></a><span data-ttu-id="46d99-103">Procedimiento: Cómo vincular contactos con clientes, proveedores y cuentas bancarias</span><span class="sxs-lookup"><span data-stu-id="46d99-103">How to: Link Contacts With Customers, Vendors, and Bank Accounts</span></span>
<span data-ttu-id="46d99-104">Si tiene un contacto y un cliente, proveedor o cuenta bancaria de la misma empresa, puede vincular las dos entidades.</span><span class="sxs-lookup"><span data-stu-id="46d99-104">If you have contact and either a customer, vendor, or bank account for the same company, you can link the two entities.</span></span> <span data-ttu-id="46d99-105">Al vincular las dos entidades, se pueden sincronizar los datos que son comunes para que sean los mismos en ambos sitios.</span><span class="sxs-lookup"><span data-stu-id="46d99-105">Linking the two entities enables you to synchronize data that is common so that it is the same in both places.</span></span>

## <a name="link-a-contact-to-an-existing-customer-vendor-or-bank-account"></a><span data-ttu-id="46d99-106">Vincular un contacto con un cliente, proveedor o cuenta bancaria existente</span><span class="sxs-lookup"><span data-stu-id="46d99-106">Link a Contact to an Existing Customer, Vendor, or Bank Account</span></span>
1. <span data-ttu-id="46d99-107">Abra el contacto que quiere vincular.</span><span class="sxs-lookup"><span data-stu-id="46d99-107">Open the contact that you want to link.</span></span>
2. <span data-ttu-id="46d99-108">Elija la acción **Vincular con** y, a continuación, elija **Cliente**, **Proveedor** o **Banco**.</span><span class="sxs-lookup"><span data-stu-id="46d99-108">Choose the **Link with existing** action, and then choose **Customer**, **Vendor**, or **Bank**.</span></span>
3. <span data-ttu-id="46d99-109">Seleccione el cliente, el proveedor o la cuenta bancaria al que quiere vincular el contacto.</span><span class="sxs-lookup"><span data-stu-id="46d99-109">Select the customer, vendor, or bank account to link to.</span></span>

   <span data-ttu-id="46d99-110">En los **Campos principales actuales**, especifique los campos a los que el sistema debe dar prioridad en caso de información conflictiva de los campos comunes al contacto y cliente, vendedor o cuenta.</span><span class="sxs-lookup"><span data-stu-id="46d99-110">In the **Current Master Fields**, you specify which fields should prioritize in case of conflicting information in fields common to the contact and customer, vendor, or account.</span></span> <span data-ttu-id="46d99-111">Por ejemplo, si el código de vendedor es diferente entre el contacto y el cliente, seleccione **Contacto** para definir que la información válida es la de la ficha de contacto.</span><span class="sxs-lookup"><span data-stu-id="46d99-111">For example, if the salesperson code is different in the contact than the customer, you can decide, by selecting **Contact**, to use the information in the contact.</span></span>

## <a name="see-also"></a><span data-ttu-id="46d99-112">Consulte también</span><span class="sxs-lookup"><span data-stu-id="46d99-112">See Also</span></span>
[<span data-ttu-id="46d99-113">Sincronizar contactos con clientes, proveedores y cuentas bancarias</span><span class="sxs-lookup"><span data-stu-id="46d99-113">Synchronizing Contacts With Customers, Vendors, and Bank Accounts</span></span>](marketing-synchronize-contacts-customers-vendors-bank-accounts.md)  
[<span data-ttu-id="46d99-114">Creación y administración de contactos</span><span class="sxs-lookup"><span data-stu-id="46d99-114">Creating and Managing Contacts</span></span>](marketing-contacts.md)  
<span data-ttu-id="46d99-115">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="46d99-115">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

