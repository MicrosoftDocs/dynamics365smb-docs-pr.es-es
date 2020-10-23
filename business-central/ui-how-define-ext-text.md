---
title: Agregar líneas adicionales para definir descripciones ampliadas
description: Puede agregar líneas adicionales para ampliar el texto estándar que describe un producto, una cuenta y otros datos.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 1dd6c3085c0cb8696b6e7011fbea3c3cd9a1c86e
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2020
ms.locfileid: "3920452"
---
# <a name="add-extended-text"></a><span data-ttu-id="edce3-103">Agregar textos adicionales</span><span class="sxs-lookup"><span data-stu-id="edce3-103">Add Extended Text</span></span>

<span data-ttu-id="edce3-104">Puede ampliar la descripción para productos, unidades de almacenamiento, cuentas de contabilidad y recursos agregando líneas adicionales como texto adicional.</span><span class="sxs-lookup"><span data-stu-id="edce3-104">You can extend the description for items, stock-keeping units, general ledger accounts, and resources by adding extra lines as extended text.</span></span> <span data-ttu-id="edce3-105">También puede configurar condiciones para el uso de líneas adicionales.</span><span class="sxs-lookup"><span data-stu-id="edce3-105">You can also set up conditions for use of the extra lines.</span></span>  

<span data-ttu-id="edce3-106">La siguiente sección describe cómo agregar texto adicional a una descripción de un producto.</span><span class="sxs-lookup"><span data-stu-id="edce3-106">The following section describes how to add extended text to a description of an item.</span></span> <span data-ttu-id="edce3-107">Pero los mismos pasos se aplican a las unidades de almacenamiento, las cuentas de contabilidad y los recursos.</span><span class="sxs-lookup"><span data-stu-id="edce3-107">But the same steps apply to stock-keeping units, general ledger accounts, and resources.</span></span>  

## <a name="to-define-extended-text-for-an-description"></a><span data-ttu-id="edce3-108">Para definir el texto adicional de una descripción</span><span class="sxs-lookup"><span data-stu-id="edce3-108">To define extended text for an description</span></span>

1. <span data-ttu-id="edce3-109">Abra la ficha de un producto al que desee agregar texto adicional y, a continuación, elija la acción **Textos adicionales**.</span><span class="sxs-lookup"><span data-stu-id="edce3-109">Open the card for an item that you want to add extended text to, and then choose the **Extended Text** action.</span></span>
2. <span data-ttu-id="edce3-110">Rellene los campos **Código** y **Descripción**.</span><span class="sxs-lookup"><span data-stu-id="edce3-110">Fill in the **Code** and **Description** fields.</span></span>
3. <span data-ttu-id="edce3-111">Seleccione **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="edce3-111">Choose the **New**.</span></span>
4. <span data-ttu-id="edce3-112">Rellene el campo **Cód. idioma** o seleccione la casilla **Común a todos los idiomas** si usa códigos de idioma.</span><span class="sxs-lookup"><span data-stu-id="edce3-112">Fill in the **Language Code** field or select the **All Language Codes** check box if you use language codes.</span></span>
5. <span data-ttu-id="edce3-113">Rellene los campos **Fecha inicial** y **Fecha final** si desea limitar las fechas en las que se utiliza el texto adicional.</span><span class="sxs-lookup"><span data-stu-id="edce3-113">Fill in the **Starting Date** and **Ending Date** fields if you want to limit the dates on which the extended text is used.</span></span>
6. <span data-ttu-id="edce3-114">En el campo **Texto**, escriba el texto adicional.</span><span class="sxs-lookup"><span data-stu-id="edce3-114">In the **Text** field, write the extended text.</span></span>
7. <span data-ttu-id="edce3-115">Seleccione las casillas de verificación correspondientes para los tipos de documento donde desee imprimir el texto adicional.</span><span class="sxs-lookup"><span data-stu-id="edce3-115">Select relevant check boxes for the document types where you want the extended text printed.</span></span>
8. <span data-ttu-id="edce3-116">Cierre la página.</span><span class="sxs-lookup"><span data-stu-id="edce3-116">Close the page.</span></span>

<span data-ttu-id="edce3-117">Ahora puede agregar este texto adicional a los documentos.</span><span class="sxs-lookup"><span data-stu-id="edce3-117">You can now add this extended text to documents.</span></span> <span data-ttu-id="edce3-118">El siguiente procedimiento explica cómo agregar texto adicional a un pedido de ventas, pero los mismos pasos se aplican a cualquier otro documento que haya especificado para el texto adicional.</span><span class="sxs-lookup"><span data-stu-id="edce3-118">The following procedure explains how to add extended text to a sales order, but the same steps apply to any other document that you specified for the extended text.</span></span>  

## <a name="to-add-an-extended-item-text-on-a-sales-order-line"></a><span data-ttu-id="edce3-119">Para agregar un texto de producto adicional en un pedido de venta línea</span><span class="sxs-lookup"><span data-stu-id="edce3-119">To add an extended item text on a sales order line</span></span>

1. <span data-ttu-id="edce3-120">Abra un pedido de venta con la línea de venta para un producto que tenga texto adicional definido.</span><span class="sxs-lookup"><span data-stu-id="edce3-120">Open a sales order with a sales line for an item that has extended text defined.</span></span> <span data-ttu-id="edce3-121">Para obtener más información, vea [Vender productos](sales-how-sell-products.md).</span><span class="sxs-lookup"><span data-stu-id="edce3-121">For more information, see [Sell Products](sales-how-sell-products.md).</span></span>
2. <span data-ttu-id="edce3-122">Seleccione la línea en cuestión y, a continuación, la acción **Insertar textos adicionales**.</span><span class="sxs-lookup"><span data-stu-id="edce3-122">Select the line in question, and then choose the **Insert Ext. Text** action.</span></span>

## <a name="see-also"></a><span data-ttu-id="edce3-123">Consulte también</span><span class="sxs-lookup"><span data-stu-id="edce3-123">See Also</span></span>

[<span data-ttu-id="edce3-124">Configurar inventario</span><span class="sxs-lookup"><span data-stu-id="edce3-124">Setting Up Inventory</span></span>](inventory-setup-inventory.md)  
<span data-ttu-id="edce3-125">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="edce3-125">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
