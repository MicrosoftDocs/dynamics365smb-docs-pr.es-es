---
title: Sincronizar contactos con clientes y proveedores | Documentos de Microsoft
description: "Puede acoplar o sincronizar la información de contacto de los contactos que también son clientes, proveedores o cuentas bancarias, de modo que actualice únicamente la información en un solo lugar."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, CRM, integration, couple
ms.date: 10/01/2018
ms.author: edupont
redirect_url: marketing-create-contact-companies
ms.translationtype: HT
ms.sourcegitcommit: 8a73de1aa2f4a0f633c401ea341bb7bde6579723
ms.openlocfilehash: 736d1329b3d3c2e9367972c2a2fb9e2af0080c85
ms.contentlocale: es-es
ms.lasthandoff: 12/11/2018

---
# <a name="synchronizing-contacts-with-customers-vendors-and-bank-accounts"></a><span data-ttu-id="aee8b-103">Sincronizar contactos con clientes, proveedores y cuentas bancarias</span><span class="sxs-lookup"><span data-stu-id="aee8b-103">Synchronizing Contacts With Customers, Vendors, and Bank Accounts</span></span>
<span data-ttu-id="aee8b-104">Si algunos contactos también son clientes, proveedores o bancos, podrá sincronizar la información de contacto con el cliente, proveedor o la cuenta bancaria relacionados.</span><span class="sxs-lookup"><span data-stu-id="aee8b-104">If some of your contacts are also customers, vendors, or bank accounts, you can synchronize the contact information with the related customer, vendor, or bank account.</span></span> <span data-ttu-id="aee8b-105">La sincronización unifica la información que es común entre los contactos y los clientes, los proveedores o la cuenta bancaria.</span><span class="sxs-lookup"><span data-stu-id="aee8b-105">Synchronization makes information that is common between contacts and customers, vendors, or bank account the same.</span></span>  

<span data-ttu-id="aee8b-106">Antes de sincronizar los contactos con los clientes, proveedores o bancos, debe especificar un código de relación de negocio para clientes, proveedores y bancos en la página **Configuración de marketing**.</span><span class="sxs-lookup"><span data-stu-id="aee8b-106">Before you can synchronize your contacts with customers, vendors, or bank accounts, you must specify a business relation code for customers, vendors, and bank accounts on the **Marketing Setup** page.</span></span> <span data-ttu-id="aee8b-107">Para obtener más información, consulte [Configurar la gestión de relaciones](marketing-setup-marketing.md).</span><span class="sxs-lookup"><span data-stu-id="aee8b-107">For more information, see [Setting Up Relationship Management](marketing-setup-marketing.md).</span></span>

## <a name="different-ways-to-synchronize-contacts-with-customers-vendors-and-bank-accounts"></a><span data-ttu-id="aee8b-108">Formas distintas de sincronizar contactos con clientes, proveedores y cuentas bancarias</span><span class="sxs-lookup"><span data-stu-id="aee8b-108">Different Ways to Synchronize Contacts with Customers, Vendors and Bank Accounts</span></span>
<span data-ttu-id="aee8b-109">Puede sincronizar sus contactos con clientes, proveedores o bancos mediante tres métodos:</span><span class="sxs-lookup"><span data-stu-id="aee8b-109">You can synchronize your contacts with customers, vendors, or bank accounts by three methods:</span></span>

* <span data-ttu-id="aee8b-110">relacionar los contactos relacionados con clientes existentes, proveedores o bancos de la ficha de contacto.</span><span class="sxs-lookup"><span data-stu-id="aee8b-110">Link contacts with existing customers, vendors, or bank accounts from the contact card.</span></span> <span data-ttu-id="aee8b-111">Para obtener más información, consulte [Vincular contactos con clientes, proveedores y cuentas bancarias](marketing-how-link-contact.md).</span><span class="sxs-lookup"><span data-stu-id="aee8b-111">For more information, see [Link Contacts With Customers, Vendors, and Bank Accounts](marketing-how-link-contact.md).</span></span>
* <span data-ttu-id="aee8b-112">Crear clientes, proveedores o cuentas bancarias a partir del contacto.</span><span class="sxs-lookup"><span data-stu-id="aee8b-112">Create customers, vendors, or bank accounts from the contact.</span></span> <span data-ttu-id="aee8b-113">Para obtener más información, consulte [Crear un cliente, proveedor o cuenta bancaria a partir de un contacto](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="aee8b-113">For more information, see [Create a Customer, Vendor, or Bank Account From a Contact](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).</span></span>
* <span data-ttu-id="aee8b-114">Crear contactos a partir de clientes, proveedores o bancos:</span><span class="sxs-lookup"><span data-stu-id="aee8b-114">Create contacts from customers, vendors or bank accounts.</span></span> <span data-ttu-id="aee8b-115">Para obtener más información, consulte [Crear un contacto de empresa a partir de un cliente, proveedor o una cuenta bancaria](marketing-how-create-contact-companies.md).</span><span class="sxs-lookup"><span data-stu-id="aee8b-115">For more information, see [Create a company contact from a customer, vendor, or bank account](marketing-how-create-contact-companies.md).</span></span>

## <a name="consequences-of-synchronization"></a><span data-ttu-id="aee8b-116">Consecuencias de la sincronización</span><span class="sxs-lookup"><span data-stu-id="aee8b-116">Consequences of Synchronization</span></span>
<span data-ttu-id="aee8b-117">Al sincronizar el contacto con el cliente, el proveedor o la cuenta bancaria:</span><span class="sxs-lookup"><span data-stu-id="aee8b-117">When the contact is synchronized with the customer, vendor, bank account:</span></span>

* <span data-ttu-id="aee8b-118">Solo es necesario actualizar la información en una de ellas.</span><span class="sxs-lookup"><span data-stu-id="aee8b-118">You only have to update information in one place.</span></span> <span data-ttu-id="aee8b-119">Por ejemplo, si modifica el número de teléfono del contacto, dicho número se actualizará automáticamente para reflejar la modificación en el cliente, el proveedor o la cuenta bancaria.</span><span class="sxs-lookup"><span data-stu-id="aee8b-119">For example, if you modify the phone number on the contact, the phone number is automatically updated with the same modification on the customer, the vendor, or the bank account.</span></span>
* <span data-ttu-id="aee8b-120">Si especificó un número de serie para los contactos y crea una ficha de cliente, proveedor o banco, se creará automáticamente una ficha de contacto para el cliente, proveedor o banco.</span><span class="sxs-lookup"><span data-stu-id="aee8b-120">If you have specified a number series for contacts, when you create a customer card, a vendor card, or a bank account card, a contact card is automatically created for the customer, vendor or bank account.</span></span>
* <span data-ttu-id="aee8b-121">Puede crear ofertas de venta y pedidos, y obtenerlos desde el contacto.</span><span class="sxs-lookup"><span data-stu-id="aee8b-121">You can create sales quotes and orders, and purchase quotes and orders from the contact.</span></span>
* <span data-ttu-id="aee8b-122">Puede hacer que se registren sus interacciones al llevar a cabo acciones como imprimir o abrir pedidos, crear pedidos de servicio, enviar correos electrónicos, etc.</span><span class="sxs-lookup"><span data-stu-id="aee8b-122">You can have your interactions recorded when you perform actions such as printing orders, blanket orders, creating sales service orders, sending e-mails, and so on.</span></span>
* <span data-ttu-id="aee8b-123">Si elimina un contacto relacionado con un cliente, proveedor o banco, solo se borra del sistema el contacto.</span><span class="sxs-lookup"><span data-stu-id="aee8b-123">If you delete a contact linked to a customer, vendor or bank account, only the contact is removed.</span></span> <span data-ttu-id="aee8b-124">El cliente, el proveedor o la cuenta bancaria permanece.</span><span class="sxs-lookup"><span data-stu-id="aee8b-124">The customer, vendor, or bank account remains.</span></span>
* <span data-ttu-id="aee8b-125">Si elimina un cliente, proveedor o banco relacionado con un contacto, el contacto permanecerá.</span><span class="sxs-lookup"><span data-stu-id="aee8b-125">If you delete a customer, vendor, bank account linked to a contact, the contact remains.</span></span>

> [!NOTE]  
>   <span data-ttu-id="aee8b-126">Algunos detalles, como los datos de facturación y registro, no aparecen en la ficha de contacto.</span><span class="sxs-lookup"><span data-stu-id="aee8b-126">Some details, such as invoicing and posting details, do not appear on the contact card.</span></span> <span data-ttu-id="aee8b-127">Por tanto, puede que desee agregarlos manualmente en la ficha de cliente, de proveedor o de banco al crear contactos como clientes, proveedores o bancos.</span><span class="sxs-lookup"><span data-stu-id="aee8b-127">Therefore, you may want to add them manually on the customer card, vendor card, or bank account card when you create contacts as customers, vendors or bank accounts.</span></span>

## <a name="see-also"></a><span data-ttu-id="aee8b-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="aee8b-128">See Also</span></span>
[<span data-ttu-id="aee8b-129">Gestionar contactos</span><span class="sxs-lookup"><span data-stu-id="aee8b-129">Managing Contacts</span></span>](marketing-contacts.md)  
<span data-ttu-id="aee8b-130">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="aee8b-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

