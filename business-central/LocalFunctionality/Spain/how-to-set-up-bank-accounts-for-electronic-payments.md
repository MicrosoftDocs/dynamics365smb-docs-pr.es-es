---
title: Configurar cuentas bancarias para realizar pagos electrónicos
description: En Business Central, puede configurar cuentas bancarias para realizar pagos electrónicos.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 48b9417048dc5ed91c080dfef2fb8e14f9d7e5c9
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2021
ms.locfileid: "5787312"
---
# <a name="set-up-bank-accounts-for-electronic-payments"></a><span data-ttu-id="9d53f-103">Configurar cuentas bancarias para realizar pagos electrónicos</span><span class="sxs-lookup"><span data-stu-id="9d53f-103">Set Up Bank Accounts for Electronic Payments</span></span>
<span data-ttu-id="9d53f-104">En [!INCLUDE[prod_short](../../includes/prod_short.md)], puede configurar cuentas bancarias para realizar pagos electrónicos.</span><span class="sxs-lookup"><span data-stu-id="9d53f-104">In [!INCLUDE[prod_short](../../includes/prod_short.md)], you can set up bank accounts to make electronic payments.</span></span>  

## <a name="to-set-up-bank-accounts-for-electronic-payments"></a><span data-ttu-id="9d53f-105">Para configurar cuentas bancarias para realizar pagos electrónicos</span><span class="sxs-lookup"><span data-stu-id="9d53f-105">To set up bank accounts for electronic payments</span></span>  

1.  <span data-ttu-id="9d53f-106">Elija el icono ![Bombilla que abre la función Dígame](../../media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Ficha banco proveedor** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="9d53f-106">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Bank Account Card**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="9d53f-107">En la ficha desplegable **Transferencia**, asegúrese de que los campos **CCC Cód. banco**, **CCC Cód. oficina**, **CCC Dígito control** y **CCC Nº cuenta** se rellenan correctamente.</span><span class="sxs-lookup"><span data-stu-id="9d53f-107">On the **Transfer** FastTab, make sure that the **CCC Bank No.**, **CCC Bank Branch No.**, **CCC Control Digits**, and **CCC Bank Account No.** fields are filled in correctly.</span></span>  
3.  <span data-ttu-id="9d53f-108">En la ficha desplegable **Transferencia**, rellene los campos tal como se describe en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="9d53f-108">On the **Transfer** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="9d53f-109">Campo</span><span class="sxs-lookup"><span data-stu-id="9d53f-109">Field</span></span>|<span data-ttu-id="9d53f-110">Description</span><span class="sxs-lookup"><span data-stu-id="9d53f-110">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="9d53f-111">**Ruta archivo exp. pago elec.**</span><span class="sxs-lookup"><span data-stu-id="9d53f-111">**E-Pay Export File Path**</span></span>|<span data-ttu-id="9d53f-112">Introduzca la ruta de acceso completa del archivo de pago electrónico, empiece con la letra de la unidad y acabe con una barra diagonal inversa (\).</span><span class="sxs-lookup"><span data-stu-id="9d53f-112">Enter the full path of the electronic payment file, start with the drive letter and end with a backslash ().</span></span> <span data-ttu-id="9d53f-113">El nombre no se escribe aquí.</span><span class="sxs-lookup"><span data-stu-id="9d53f-113">The file name is not included here.</span></span> <span data-ttu-id="9d53f-114">Debe utilizar el directorio donde [!INCLUDE[prod_short](../../includes/prod_short.md)] se encuentra instalado.</span><span class="sxs-lookup"><span data-stu-id="9d53f-114">You should use the directory where [!INCLUDE[prod_short](../../includes/prod_short.md)] is installed.</span></span> <span data-ttu-id="9d53f-115">Por ejemplo, podría escribir **C:NAV** en este campo.</span><span class="sxs-lookup"><span data-stu-id="9d53f-115">For example: **C:NAV** would be a possible entry for this field.</span></span> <span data-ttu-id="9d53f-116">Puede escribir 100 caracteres como máximo.</span><span class="sxs-lookup"><span data-stu-id="9d53f-116">You can enter a maximum of 100 characters.</span></span>|  
    |<span data-ttu-id="9d53f-117">**Nom. arch. exp. últ. pago elec.**</span><span class="sxs-lookup"><span data-stu-id="9d53f-117">**Last E-Pay Export File Name**</span></span>|<span data-ttu-id="9d53f-118">Especifique el nombre del archivo con la extensión de nombre de archivo .txt, sin la ruta. Debido a que el nombre del archivo se incrementará cada vez que se exporte un archivo de pago electrónico, este nombre de archivo debe tener dígitos.</span><span class="sxs-lookup"><span data-stu-id="9d53f-118">Specify the name of the file with the .txt file name extension, without the path., Because the file name will be incremented every time that an electronic payment file is exported, this file name should have digits in it.</span></span> <span data-ttu-id="9d53f-119">De esta forma se creará un registro permanente de cada archivo que haya exportado al banco.</span><span class="sxs-lookup"><span data-stu-id="9d53f-119">This will create a permanent record of every file that you have exported to the bank.</span></span> <span data-ttu-id="9d53f-120">Por ejemplo, **DD000000.txt** podría ser la primera entrada de este campo.</span><span class="sxs-lookup"><span data-stu-id="9d53f-120">For example, **DD000000.txt** could be a possible first entry for this field.</span></span> <span data-ttu-id="9d53f-121">Puede escribir 50 caracteres como máximo.</span><span class="sxs-lookup"><span data-stu-id="9d53f-121">You can enter a maximum of 50 characters.</span></span>|  

4.  <span data-ttu-id="9d53f-122">En la ficha desplegable **Registrando**, rellene los campos tal como se describe en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="9d53f-122">On the **Posting** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="9d53f-123">Campo</span><span class="sxs-lookup"><span data-stu-id="9d53f-123">Field</span></span>|<span data-ttu-id="9d53f-124">Description</span><span class="sxs-lookup"><span data-stu-id="9d53f-124">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="9d53f-125">**Nº último aviso pago**</span><span class="sxs-lookup"><span data-stu-id="9d53f-125">**Last Remittance Advice No.**</span></span>|<span data-ttu-id="9d53f-126">Especifique una serie de números distinta a la serie de números de los cheques.</span><span class="sxs-lookup"><span data-stu-id="9d53f-126">Specify a number series that differs from the check number series.</span></span> <span data-ttu-id="9d53f-127">Esto es necesario para que los números no entren en conflicto entre sí.</span><span class="sxs-lookup"><span data-stu-id="9d53f-127">This is needed so that the numbers do not conflict with each other.</span></span> <span data-ttu-id="9d53f-128">El aviso de pago se imprime en papel en blanco de forma que resulte fácil enviarlo al proveedor.</span><span class="sxs-lookup"><span data-stu-id="9d53f-128">The remittance advice is printed on blank paper in a form that is easy to mail to the vendor.</span></span>|  

## <a name="to-set-up-vendor-bank-accounts-for-electronic-payments"></a><span data-ttu-id="9d53f-129">Para configurar cuentas bancarias para realizar pagos electrónicos</span><span class="sxs-lookup"><span data-stu-id="9d53f-129">To set up vendor bank accounts for electronic payments</span></span>  

1.  <span data-ttu-id="9d53f-130">Elija el icono ![Bombilla que abre la función Dígame](../../media/ui-search/search_small.png "Dígame qué desea hacer"), introduzca **Ficha banco proveedor** y luego elija el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="9d53f-130">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Vendor Bank Account Card**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="9d53f-131">En la ficha desplegable **General**, rellene los campos tal como se describe en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="9d53f-131">On the **General** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="9d53f-132">Campo</span><span class="sxs-lookup"><span data-stu-id="9d53f-132">Field</span></span>|<span data-ttu-id="9d53f-133">Description</span><span class="sxs-lookup"><span data-stu-id="9d53f-133">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="9d53f-134">**Usar para pagos electrónicos**</span><span class="sxs-lookup"><span data-stu-id="9d53f-134">**Use For Electronic Payments**</span></span>|<span data-ttu-id="9d53f-135">Especifica si debe usarse esta cuenta bancaria del proveedor para los pagos electrónicos.</span><span class="sxs-lookup"><span data-stu-id="9d53f-135">Specify if this vendor bank account will be used for electronic payments.</span></span> <span data-ttu-id="9d53f-136">Para realizar pagos electrónicos solo se puede seleccionar una cuenta de banco por proveedor.</span><span class="sxs-lookup"><span data-stu-id="9d53f-136">For electronic payments, only one bank account can be selected for each vendor.</span></span>|  

3.  <span data-ttu-id="9d53f-137">En la ficha desplegable **Transferencia**, asegúrese de que los campos **CCC Cód. banco**, **CCC Cód. oficina**, **CCC Dígito control** y **CCC Nº cuenta** se rellenan correctamente.</span><span class="sxs-lookup"><span data-stu-id="9d53f-137">On the **Transfer** FastTab, make sure that the **CCC Bank No.**, **CCC Bank Branch No.**, **CCC Control Digits**, and **CCC Bank Account No.** fields are filled in correctly.</span></span>  

## <a name="see-also"></a><span data-ttu-id="9d53f-138">Consulte también</span><span class="sxs-lookup"><span data-stu-id="9d53f-138">See Also</span></span>  
 [<span data-ttu-id="9d53f-139">Pagos electrónicos – AEB N34.1</span><span class="sxs-lookup"><span data-stu-id="9d53f-139">Electronic Payments – AEB N34.1</span></span>](electronic-payments-aeb-n341.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]