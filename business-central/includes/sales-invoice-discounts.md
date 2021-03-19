---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 01/25/2021
ms.author: edupont
ms.openlocfilehash: 539ee2eb2c9e4a71eacfb78d95320870128fb1d9
ms.sourcegitcommit: cb06aa973f5c767df774b0e1e199c6fbe0e85b88
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/17/2021
ms.locfileid: "5470292"
---
<span data-ttu-id="487d3-101">Una vez que se hayan especificado todos los productos en las líneas de venta, podrá calcular el descuento en factura para todo el documento eligiendo la acción **Calcular descuento en factura**.</span><span class="sxs-lookup"><span data-stu-id="487d3-101">When all the items have been entered on the sales lines, you can calculate the invoice discount for the entire document by choosing the **Calculate Invoice Discount** action.</span></span>

<span data-ttu-id="487d3-102">El descuento se calcula basándose en todas las líneas del documento de venta para productos en los que el campo **Permitir descuento en factura** de la línea de pedido de venta contiene **Sí**.</span><span class="sxs-lookup"><span data-stu-id="487d3-102">The discount is calculated based on all the lines in the sales document for items where the **Allow Invoice Disc.** field on the sales order line contains **Yes**.</span></span> <span data-ttu-id="487d3-103">Este es el valor predeterminado para los productos.</span><span class="sxs-lookup"><span data-stu-id="487d3-103">This is the default setting for items.</span></span> <span data-ttu-id="487d3-104">Las líneas con cargos de producto, por ejemplo, no se incluyen en el cálculo del descuento de factura.</span><span class="sxs-lookup"><span data-stu-id="487d3-104">Lines with item charges, for example, are not included in the calculation of the invoice discount.</span></span> <span data-ttu-id="487d3-105">Si desea aplicar un descuento a dichas líneas, debe establecer el campo **% de descuento de línea** en las líneas relevantes.</span><span class="sxs-lookup"><span data-stu-id="487d3-105">If you want to apply a discount to such lines, you must set the **Line Discount %** field on the relevant lines.</span></span>  

> [!TIP]
> <span data-ttu-id="487d3-106">Si se selecciona el campo **Calcular descuento de factura** en la página **Configuración ventas y cobros**, se calcula el descuento de la factura automáticamente cuando realiza una de las siguientes operaciones en un documento de venta:</span><span class="sxs-lookup"><span data-stu-id="487d3-106">If the **Calc. Inv. Discount** field is selected in the **Sales and Receivables Setup** page, then the invoice discount is calculated automatically when you do either of the following on a sales document:</span></span>
>
> * <span data-ttu-id="487d3-107">Ver estadísticas</span><span class="sxs-lookup"><span data-stu-id="487d3-107">View statistics</span></span>
> * <span data-ttu-id="487d3-108">Ver un test</span><span class="sxs-lookup"><span data-stu-id="487d3-108">View a test report</span></span>
> * <span data-ttu-id="487d3-109">Imprimir</span><span class="sxs-lookup"><span data-stu-id="487d3-109">Print</span></span>
> * <span data-ttu-id="487d3-110">Envíos postales</span><span class="sxs-lookup"><span data-stu-id="487d3-110">Post</span></span>

<span data-ttu-id="487d3-111">Las condiciones de descuento en factura para un cliente se definen en la página **Descuentos en factura de cliente** para el cliente.</span><span class="sxs-lookup"><span data-stu-id="487d3-111">The invoice discount terms for a customer are defined in the **Cust. Invoice Discounts** page for the customer.</span></span> <span data-ttu-id="487d3-112">El código de divisa del documento de venta se usa para buscar las condiciones de descuento en factura en la divisa correspondiente.</span><span class="sxs-lookup"><span data-stu-id="487d3-112">The currency code on the sales document is used to find the invoice discount terms in the corresponding currency.</span></span>

<span data-ttu-id="487d3-113">Si no se han definido descuentos facturas para divisas extranjeras, el programa utiliza las condiciones de descuento factura en DL que aparecen en la página **Dto. factura cliente** con importes en la divisa local y el tipo de cambio en la fecha de registro del documento de venta para calcular el descuento en factura en divisa extranjera.</span><span class="sxs-lookup"><span data-stu-id="487d3-113">If invoice discounts have not been defined for foreign currencies, then the invoice discount terms defined in the **Cust. Invoice Discounts** page with amounts in your local currency and the exchange rate on the posting date on the sales document are used to calculate the invoice discount in the foreign currency.</span></span>
