---
title: "Cómo verificar números CIF/NIF | Documentos de Microsoft"
description: "Puede usar un servicio web de la UE para verificar que los números de CIF/NIF que introduzca en las fichas de cliente, proveedor o contacto sean válidos."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/10/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 7180c7823055dba52a398584ed2f4c2952d08492
ms.contentlocale: es-es
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-verify-vat-registration-numbers"></a><span data-ttu-id="8f348-103">Verificación de números CIF/NIF</span><span class="sxs-lookup"><span data-stu-id="8f348-103">How to: Verify VAT Registration Numbers</span></span>
<span data-ttu-id="8f348-104">Puede usar un servicio web de la UE para verificar que los números de CIF/NIF que introduzca en las fichas de cliente, proveedor o contacto sean válidos.</span><span class="sxs-lookup"><span data-stu-id="8f348-104">You can use an EU web service to verify that VAT registration numbers that you enter on customer, vendor, or contact cards are valid.</span></span>  

 <span data-ttu-id="8f348-105">Cuando modifique el **CIF/NIF** en una tarjeta donde el valor del campo **Código país/región** es un país/región de la Unión Europea, el nuevo CIF/NIF y su Id. de usuario aparecen en la ventana **Registro de CIF/NIF**.</span><span class="sxs-lookup"><span data-stu-id="8f348-105">When you modify the **VAT Registration No.** field on a card where the value in the **Country/Region Code** field is an EU country/region, then the new VAT registration number and your user ID are logged in the **VAT Registration Log** window.</span></span> <span data-ttu-id="8f348-106">Para verificar un número de CIF/NIF se selecciona el botón **Verificar CIF/NIF** en la ventana **Registro de CIF/NIF**.</span><span class="sxs-lookup"><span data-stu-id="8f348-106">You verify a VAT registration number by choosing the **Verify Registration No.** button in the **VAT Registration Log** window.</span></span> <span data-ttu-id="8f348-107">Se crea una nueva línea cada vez que se usa la función de verificación.</span><span class="sxs-lookup"><span data-stu-id="8f348-107">A new line is created every time you use the verification function.</span></span> <span data-ttu-id="8f348-108">Si el número se pudo verificar, el campo **Estado** contiene **Válido**.</span><span class="sxs-lookup"><span data-stu-id="8f348-108">If the number could be verified, the **Status** field contains **Valid**.</span></span> <span data-ttu-id="8f348-109">Si no se puede verificar el número, el campo **Status** contiene **No válido** y se debe modificar el número del campo **CIF/NIF** en la ficha e iniciar la función de verificación de nuevo.</span><span class="sxs-lookup"><span data-stu-id="8f348-109">If the number could not be verified, the **Status** field contains **Invalid**, and you must then change the number in the **VAT Registration No.** field on the card and start the verification function again.</span></span>  

 <span data-ttu-id="8f348-110">La URL del servicio web predeterminado está configurada en el campo **URL de validación de CIF/NIF** en la ventana **Configuración de contabilidad**.</span><span class="sxs-lookup"><span data-stu-id="8f348-110">The URL of the default web service is set up in the **VAT Reg. No. Validation URL** field in the **General Ledger Setup** window.</span></span>  

 <span data-ttu-id="8f348-111">En la tabla **Formato CIF/NIF** puede modificar según cada país o región los distintos formatos de número de CIF/NIF que se permite a los usuarios especificar en el campo **CIF/NIF**.</span><span class="sxs-lookup"><span data-stu-id="8f348-111">In the **VAT Registration No. Format** table, you can change for each country/region the different formats of VAT registration number that users are allowed to enter in the **VAT Registration No.** field.</span></span>  

> [!WARNING]  
>  <span data-ttu-id="8f348-112">Este servicio web utiliza el protocolo HTTP, lo que significa que los datos transferidos a través del servicio no están cifrados.</span><span class="sxs-lookup"><span data-stu-id="8f348-112">This web service uses the http protocol, which means that data transferred through the service is not encrypted.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="8f348-113">Puede experimentar tiempos de inactividad para este servicio, de los cuales Microsoft no es responsable, ya que el servicio forma parte de una amplia red de registros nacionales de IVA de la UE.</span><span class="sxs-lookup"><span data-stu-id="8f348-113">You may experience downtime for this service for which Microsoft is not responsible, as the service is part of a broad EU network of national VAT registers.</span></span>  

## <a name="to-verify-a-vat-registration-number-from-a-customer-card"></a><span data-ttu-id="8f348-114">Para verificar un número de CIF/NIF desde una ficha de cliente</span><span class="sxs-lookup"><span data-stu-id="8f348-114">To verify a VAT registration number from a customer card</span></span>  
<span data-ttu-id="8f348-115">A continuación se describe cómo comprobar un CIF/NIF para un cliente.</span><span class="sxs-lookup"><span data-stu-id="8f348-115">The following describes how to verify a VAT registration number for a customer.</span></span> <span data-ttu-id="8f348-116">Los pasos son parecidos para un proveedor y un contacto.</span><span class="sxs-lookup"><span data-stu-id="8f348-116">The steps are similar for a vendor and a contact.</span></span>   
1.  <span data-ttu-id="8f348-117">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Clientes** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="8f348-117">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Customers**, and then choose the related link.</span></span>  

2.  <span data-ttu-id="8f348-118">Abra la ficha de un cliente para el cual desee comprobar el número de CIF/NIF.</span><span class="sxs-lookup"><span data-stu-id="8f348-118">Open the card of a customer where you want to verify the VAT registration number.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="8f348-119">El campo **Código país/región** en la ficha del cliente debe contener un país o región de la UE.</span><span class="sxs-lookup"><span data-stu-id="8f348-119">The **Country/Region Code** field on the customer card must contain an EU country/region.</span></span>  
3.  <span data-ttu-id="8f348-120">En la ficha desplegable **Facturación**, seleccione el botón Análisis junto al campo **CIF/NIF**.</span><span class="sxs-lookup"><span data-stu-id="8f348-120">On the **Invoicing** FastTab, choose the DrillDown button next to the **VAT Registration No.** field.</span></span>  

    <span data-ttu-id="8f348-121">La ventana **Registro de CIF/NIF** se abre con una línea en la que el campo **Estado** contiene **No verificado**.</span><span class="sxs-lookup"><span data-stu-id="8f348-121">The **VAT Registration Log** window opens showing one line where the **Status** field contains **Not Verified**.</span></span>  
4.  <span data-ttu-id="8f348-122">Seleccione la acción **Comprobar nº reg. mercantil**.</span><span class="sxs-lookup"><span data-stu-id="8f348-122">Choose the **Verify Registration No.** action.</span></span>  

     <span data-ttu-id="8f348-123">Se crea una nueva línea donde el campo **Estado** contiene **Válido** o **No válido**.</span><span class="sxs-lookup"><span data-stu-id="8f348-123">A new line is created where the **Status** field contains either **Valid** or **Invalid**.</span></span>  
5.  <span data-ttu-id="8f348-124">Si el campo **Status** contiene **No válido**, cambie el número en el campo **CIF/NIF** en la ficha y, a continuación, repita los pasos 3 y 4.</span><span class="sxs-lookup"><span data-stu-id="8f348-124">If the **Status** field contains **Invalid**, change the number in the **VAT Registration No.** field on the card, and then repeat steps 3 through 4.</span></span>  

## <a name="see-also"></a><span data-ttu-id="8f348-125">Consulte también</span><span class="sxs-lookup"><span data-stu-id="8f348-125">See Also</span></span>  
[<span data-ttu-id="8f348-126">Finanzas</span><span class="sxs-lookup"><span data-stu-id="8f348-126">Finance</span></span>](finance.md)  
[<span data-ttu-id="8f348-127">Registro de clientes nuevos</span><span class="sxs-lookup"><span data-stu-id="8f348-127">How to: Register New Customers</span></span>](sales-how-register-new-customers.md)  
[<span data-ttu-id="8f348-128">Registro de proveedores nuevos</span><span class="sxs-lookup"><span data-stu-id="8f348-128">How to: Register New Vendors</span></span>](purchasing-how-register-new-vendors.md)  
<span data-ttu-id="8f348-129">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="8f348-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

