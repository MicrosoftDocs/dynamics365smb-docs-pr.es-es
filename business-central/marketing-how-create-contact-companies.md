---
title: Crear empresas de contacto | Documentos de Microsoft
description: "Describe cómo crear un contacto para cada nueva empresa o empresa potencial con la que interactúe o tenga una relación."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 64bef8820ec10bb293ccda88e7384d5d9e868e1f
ms.contentlocale: es-es
ms.lasthandoff: 09/28/2018

---
# <a name="create-contact-companies"></a><span data-ttu-id="fc72a-103">Crear empresas de contacto</span><span class="sxs-lookup"><span data-stu-id="fc72a-103">Create Contact Companies</span></span>
<span data-ttu-id="fc72a-104">Puede crear un contacto por cada nueva empresa con la que se relacione, como puede ser un cliente, un proveedor, un posible cliente, un banco, un despacho de abogados, una consultora, etc.</span><span class="sxs-lookup"><span data-stu-id="fc72a-104">You can create a contact for each new company you interact with, for example, a customer, vendor, prospective customer, bank, law firm, consultant, and so on.</span></span>

<span data-ttu-id="fc72a-105">Existen dos formas de crear un contacto: desde cero o a partir de un cliente, proveedor o cuenta bancaria existente.</span><span class="sxs-lookup"><span data-stu-id="fc72a-105">There are two ways to create a contact: from scratch or from an existing customer, vendor, or bank account.</span></span>

<span data-ttu-id="fc72a-106">Antes de crear un contacto, es posible que desee comprobar la configuración de la ventana **Configuración marketing**.</span><span class="sxs-lookup"><span data-stu-id="fc72a-106">Before creating a contact, you may want to check the settings in the **Marketing Setup** window.</span></span> <span data-ttu-id="fc72a-107">Para obtener más información, consulte [Configurar la gestión de relaciones](marketing-setup-marketing.md).</span><span class="sxs-lookup"><span data-stu-id="fc72a-107">For more information, see [Setting Up Relationship Management](marketing-setup-marketing.md).</span></span>

## <a name="create-a-company-contact-from-scratch"></a><span data-ttu-id="fc72a-108">Crear un contacto de compañía desde cero</span><span class="sxs-lookup"><span data-stu-id="fc72a-108">Create a company contact from scratch</span></span>
1. <span data-ttu-id="fc72a-109">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Contactos** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="fc72a-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Contacts**, and then choose the related link.</span></span>
2. <span data-ttu-id="fc72a-110">Seleccione la acción **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="fc72a-110">Choose the **New** action.</span></span>
3. <span data-ttu-id="fc72a-111">En el campo **N.º de campo** introduzca un número para el contacto.</span><span class="sxs-lookup"><span data-stu-id="fc72a-111">In the **No. field**, enter a number for the contact.</span></span>

    <span data-ttu-id="fc72a-112">Por otra parte, si configuró un número de serie para los contactos de la ventana **Configuración marketing**, puede pulsar Entrar para hacer que el sistema especifique el siguiente número de contacto disponible.</span><span class="sxs-lookup"><span data-stu-id="fc72a-112">Alternatively, if you have set up a number series for contacts in the **Marketing Setup** window, you can press the Enter key to select the next available contact number.</span></span>  
4. <span data-ttu-id="fc72a-113">Establezca **Tipo** en **Empresa**.</span><span class="sxs-lookup"><span data-stu-id="fc72a-113">Set **Type** to **Company**.</span></span>
5. <span data-ttu-id="fc72a-114">Rellene los demás campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="fc72a-114">Fill in the other fields as required.</span></span>

## <a name="to-create-a-company-contact-from-a-customer-vendor-or-bank-account"></a><span data-ttu-id="fc72a-115">Para crear un contacto desde un cliente, proveedor o banco</span><span class="sxs-lookup"><span data-stu-id="fc72a-115">To create a company contact from a customer, vendor, or bank account</span></span>
<span data-ttu-id="fc72a-116">Si ya configuró un cierto número de clientes, proveedores o bancos, podrá crear contactos según los datos existentes.</span><span class="sxs-lookup"><span data-stu-id="fc72a-116">If you have already set up a number of customers, vendors, and bank accounts, you can create contacts on the basis of the existing data.</span></span> <span data-ttu-id="fc72a-117">Al crear un contacto de esta manera, la información de contacto se sincroniza con la información del cliente, proveedor o de la cuenta bancaria.</span><span class="sxs-lookup"><span data-stu-id="fc72a-117">When you create a contact this way, the contact information is synchronized with the customer, vendor, or bank account information.</span></span>

> [!NOTE]  
>   <span data-ttu-id="fc72a-118">Para poder crear empresas de contacto, es necesario especificar un código de relación de negocio para los clientes, proveedores y las cuentas bancarias en la ventana **Configuración de marketing**.</span><span class="sxs-lookup"><span data-stu-id="fc72a-118">Before you can create contact companies this way, you must specify a business relation code for customers, vendors, and bank accounts in the **Marketing Setup** window.</span></span> <span data-ttu-id="fc72a-119">Si va a crear contactos a partir de cuentas bancarias, también debe especificar números de serie para las cuentas bancarias en la ventana **Configuración de contabilidad**.</span><span class="sxs-lookup"><span data-stu-id="fc72a-119">If you will be creating contacts from a bank accounts, you must also specify numbers series for bank accounts in the **General Ledger Setup** window.</span></span>

1. <span data-ttu-id="fc72a-120">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), especifique una de las siguientes opciones, según la ubicación desde la cual desee crear contactos y, a continuación, elija el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="fc72a-120">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter one of the following, depending on from where you want to create contacts, and then choose the related link.</span></span>
   * <span data-ttu-id="fc72a-121">**Crear Contactos desde Clientes**</span><span class="sxs-lookup"><span data-stu-id="fc72a-121">**Create Contacts from Customers**</span></span>
   * <span data-ttu-id="fc72a-122">**Crear Contactos desde Provs**</span><span class="sxs-lookup"><span data-stu-id="fc72a-122">**Create Contacts from Vendors**</span></span>
   * <span data-ttu-id="fc72a-123">**Crear Contactos desde Bancos**</span><span class="sxs-lookup"><span data-stu-id="fc72a-123">**Create Contacts from Bank Accounts**</span></span>
2. <span data-ttu-id="fc72a-124">En la ventana del proceso que se abre, establezca filtros en la sección **Cliente**, **Proveedor** o **Banco** si desea crear contactos solo desde determinados clientes, proveedores o bancos.</span><span class="sxs-lookup"><span data-stu-id="fc72a-124">In the batch job window that opens, in the **Customer**, **Vendor**, or **Bank Account** section, set filters if you want to create contacts from specific customers, vendors, or bank accounts.</span></span>
3. <span data-ttu-id="fc72a-125">Para crear contactos, seleccione **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="fc72a-125">Choose the **OK** button to start creating contacts.</span></span>

    <span data-ttu-id="fc72a-126">Los siguientes números de contacto de la serie se asignan a los nuevos contactos.</span><span class="sxs-lookup"><span data-stu-id="fc72a-126">The next contact numbers in the number series are assigned to the new contacts.</span></span> <span data-ttu-id="fc72a-127">El programa asigna la relación comercial para proveedores especificada en la ventana **Configuración marketing** a los contactos recién creados.</span><span class="sxs-lookup"><span data-stu-id="fc72a-127">The business relation for vendors that is specified in the **Marketing Setup** window is assigned to the newly created contacts.</span></span>

> [!TIP]  
>   <span data-ttu-id="fc72a-128">También puede crear un cliente, proveedor o una cuenta bancaria a partir de un contacto.</span><span class="sxs-lookup"><span data-stu-id="fc72a-128">You can also create a customer, vendor, or bank account from a contact.</span></span> <span data-ttu-id="fc72a-129">Para obtener más información, consulte [Crear un cliente, proveedor o cuenta bancaria a partir de un contacto](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="fc72a-129">For more information, see [Create a Customer, Vendor, or Bank Account From a Contact](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="fc72a-130">Consulte también</span><span class="sxs-lookup"><span data-stu-id="fc72a-130">See Also</span></span>
[<span data-ttu-id="fc72a-131">Sincronizar contactos con clientes, proveedores y cuentas bancarias</span><span class="sxs-lookup"><span data-stu-id="fc72a-131">Synchronizing Contacts With Customers, Vendors, and Bank Accounts</span></span>](marketing-synchronize-contacts-customers-vendors-bank-accounts.md)  
[<span data-ttu-id="fc72a-132">Asignar relaciones de negocio a un contacto</span><span class="sxs-lookup"><span data-stu-id="fc72a-132">Assign Business Relations to a Contact</span></span>](marketing-business-relations.md#AssignBusRelContact)  
[<span data-ttu-id="fc72a-133">Para asignar grupos de industria a un contacto</span><span class="sxs-lookup"><span data-stu-id="fc72a-133">Assign Industry Groups to a Contact</span></span>](marketing-industry-groups.md#AssignIndustryGroupContact)  
[<span data-ttu-id="fc72a-134">Asignar grupos de correo a un contacto</span><span class="sxs-lookup"><span data-stu-id="fc72a-134">Assign Mailing Groups to a Contact</span></span>](marketing-mailing-groups.md#AssignMailGroupContact)  
[<span data-ttu-id="fc72a-135">Crear personas de contacto</span><span class="sxs-lookup"><span data-stu-id="fc72a-135">Create Contact Persons</span></span>](marketing-create-contact-persons.md)  
[<span data-ttu-id="fc72a-136">Trabajar con Business Central</span><span class="sxs-lookup"><span data-stu-id="fc72a-136">Working with Business Central</span></span>](ui-work-product.md)

