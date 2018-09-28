---
title: Recargo de equivalencia (RE)
description: "Un recargo de equivalencia (RE) es un impuesto que se utiliza en ventas minoristas y en actividades que no siguen las reglas del IVA. Según las reglas RE, las empresas deben pagar un recargo a sus proveedores al adquirir bienes además del IVA normal."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 4edd2067b1b7e093b61d398ba5abf403b76a89e0
ms.contentlocale: es-es
ms.lasthandoff: 09/28/2018

---
# <a name="equivalence-charges-ec"></a><span data-ttu-id="08e1f-104">Recargo de equivalencia (RE)</span><span class="sxs-lookup"><span data-stu-id="08e1f-104">Equivalence Charges (EC)</span></span>
<span data-ttu-id="08e1f-105">Un recargo de equivalencia (RE) es un impuesto que se utiliza en ventas minoristas y en actividades que no siguen las reglas del IVA.</span><span class="sxs-lookup"><span data-stu-id="08e1f-105">An Equivalence Charge (EC) is a tax that is used in retail sales and in activities that do not follow VAT rules.</span></span> <span data-ttu-id="08e1f-106">Según las reglas RE, las empresas deben pagar un recargo a sus proveedores al adquirir bienes además del IVA normal.</span><span class="sxs-lookup"><span data-stu-id="08e1f-106">Under EC rules, companies must pay a surcharge to their vendors when purchasing goods, in addition to the usual VAT.</span></span> <span data-ttu-id="08e1f-107">Sin embargo, al vender bienes, solo puede cargarse el IVA.</span><span class="sxs-lookup"><span data-stu-id="08e1f-107">However, when selling goods, only VAT can be charged.</span></span> <span data-ttu-id="08e1f-108">Algunos grupos de registro general deben tener un porcentaje RE, además del porcentaje de IVA.</span><span class="sxs-lookup"><span data-stu-id="08e1f-108">Some general posting groups must have an EC percentage in addition to the VAT percentage.</span></span> <span data-ttu-id="08e1f-109">Esta información se efectúa por separado, pero para minimizar los cambios, ambos impuestos se combinan.</span><span class="sxs-lookup"><span data-stu-id="08e1f-109">This information is tracked separately, but in order to minimize changes, both taxes are usually combined.</span></span>  

<span data-ttu-id="08e1f-110">El campo **% RE** es un campo independiente en las tablas **Lín. compra**, **Lín. venta**, **Archivo lín. venta** y **Archivo lín. compra** .</span><span class="sxs-lookup"><span data-stu-id="08e1f-110">The **EC %** field is a separate field in the **Purchase Line**, **Sales Line**, **Sales Line Archive** and **Purchase Line Archive** tables.</span></span> <span data-ttu-id="08e1f-111">No obstante, en las líneas de ventas y compras, se combinan ambos impuestos y el valor se muestra en el campo **% IVA**.</span><span class="sxs-lookup"><span data-stu-id="08e1f-111">However, in sales and purchase lines, both taxes are combined and the value is displayed in the **VAT %** field.</span></span> <span data-ttu-id="08e1f-112">Se utiliza el campo **% IVA + RE** cuando se combinan las opciones de configuración.</span><span class="sxs-lookup"><span data-stu-id="08e1f-112">The **VAT + EC %** field is used when these values are combined.</span></span> <span data-ttu-id="08e1f-113">En el momento de la publicación, el porcentaje de IVA y el porcentaje de RE se insertan en la tabla de **Movs. IVA**.</span><span class="sxs-lookup"><span data-stu-id="08e1f-113">At the time of posting, the VAT percentage and the EC percentage are inserted in the **VAT Entry** table.</span></span> <span data-ttu-id="08e1f-114">Esto permite imprimir el informe **Libro facturas emitidas** y el informe **Libro facturas recibidas**.</span><span class="sxs-lookup"><span data-stu-id="08e1f-114">This makes it possible to print the **Sales Invoice Book** report and the **Purchases Invoice Book** report.</span></span>  

## <a name="see-also"></a><span data-ttu-id="08e1f-115">Consulte también</span><span class="sxs-lookup"><span data-stu-id="08e1f-115">See Also</span></span>  
[<span data-ttu-id="08e1f-116">Funcionalidad local para España</span><span class="sxs-lookup"><span data-stu-id="08e1f-116">Spain Local Functionality</span></span>](spain-local-functionality.md)

