---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 01/20/2021
ms.author: edupont
ms.openlocfilehash: 718845561c1a18701d20b93ebdc8339308ce7ac8
ms.sourcegitcommit: adf1a87a677b8197c68bb28c44b7a58250d6fc51
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/21/2021
ms.locfileid: "5035795"
---
<span data-ttu-id="fb326-101">Una vez que se hayan especificado todos los productos en las líneas de pedido de venta, podrá calcular el descuento en factura para todo el documento de venta si hace clic en la acción **Calcular dto. en la factura**.</span><span class="sxs-lookup"><span data-stu-id="fb326-101">When all the items have been entered on the sales order lines, you can calculate the invoice discount for the entire sales document by choosing the **Calculate Invoice Discount** action.</span></span>

<span data-ttu-id="fb326-102">Si se selecciona el campo **Calc. dto. factura** en la ventana **Config. ventas y cobros**, se calcula el descuento de la factura automáticamente cuando realiza una de las siguientes operaciones en un documento de venta:</span><span class="sxs-lookup"><span data-stu-id="fb326-102">If the **Calc. Inv. Discount** field is selected in the **Sales and Receivables Setup** window, then the invoice discount is calculated automatically when you do either of the following on a sales document:</span></span>

* <span data-ttu-id="fb326-103">Ver estadísticas</span><span class="sxs-lookup"><span data-stu-id="fb326-103">View statistics</span></span>
* <span data-ttu-id="fb326-104">Ver un test</span><span class="sxs-lookup"><span data-stu-id="fb326-104">View a test report</span></span>
* <span data-ttu-id="fb326-105">Imprimir</span><span class="sxs-lookup"><span data-stu-id="fb326-105">Print</span></span>
* <span data-ttu-id="fb326-106">Envíos postales</span><span class="sxs-lookup"><span data-stu-id="fb326-106">Post</span></span>

<span data-ttu-id="fb326-107">El descuento se distribuirá proporcionalmente a todas las líneas del documento de venta para productos en los que el campo **Permitir dto. factura** de la línea de pedido de venta contiene **Sí**.</span><span class="sxs-lookup"><span data-stu-id="fb326-107">The discount is apportioned over all the lines in the sales document for items where the **Allow Invoice Disc.** field on the sales order line contains **Yes**.</span></span> <span data-ttu-id="fb326-108">Este es el valor predeterminado para los productos.</span><span class="sxs-lookup"><span data-stu-id="fb326-108">This is the default setting for items.</span></span>

<span data-ttu-id="fb326-109">Las condiciones de descuentao de factura se definen en la página **Descuentos de factura de cliente** para calcular el descuento en factura.</span><span class="sxs-lookup"><span data-stu-id="fb326-109">The invoice discount terms are defined in the **Cust. Invoice Discounts** page to calculate the invoice discount.</span></span> <span data-ttu-id="fb326-110">El código de divisa del documento de venta se usa para buscar las condiciones de descuento en factura en la divisa correspondiente.</span><span class="sxs-lookup"><span data-stu-id="fb326-110">The currency code on the sales document is used to find the invoice discount terms in the corresponding currency.</span></span>

<span data-ttu-id="fb326-111">Si no se han definido descuentos facturas para divisas extranjeras, el programa utiliza las condiciones de descuento factura en DL que aparecen en la página **Dto. factura cliente** con importes en la divisa local y el tipo de cambio en la fecha de registro del documento de venta para calcular el descuento en factura en divisa extranjera.</span><span class="sxs-lookup"><span data-stu-id="fb326-111">If invoice discounts have not been defined for foreign currencies, then the invoice discount terms defined in the **Cust. Invoice Discounts** page with amounts in your local currency and the exchange rate on the posting date on the sales document are used to calculate the invoice discount in the foreign currency.</span></span>
