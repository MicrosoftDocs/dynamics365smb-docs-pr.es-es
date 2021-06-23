---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 05/27/2021
ms.author: edupont
ms.openlocfilehash: 50b4b331f00bdcdf030bac2332ffb5dafdfd2de6
ms.sourcegitcommit: f9a190933eadf4608f591e2f1b04c69f1e5c0dc7
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116001"
---
<span data-ttu-id="1fb13-101">En los documentos de venta y los diarios, puede especificar un número de documento que haga referencia al sistema de numeración del cliente.</span><span class="sxs-lookup"><span data-stu-id="1fb13-101">On sales documents and journals, you can specify a document number that refers to the customer's numbering system.</span></span> <!--You can enter a maximum of ten characters, both numbers and letters.--> <span data-ttu-id="1fb13-102">Utilice este campo para registrar el número que el cliente asignó al pedido, la factura o el abono.</span><span class="sxs-lookup"><span data-stu-id="1fb13-102">Use this field to record the number that the customer assigned to the order, invoice, or credit memo.</span></span> <span data-ttu-id="1fb13-103">Posteriormente podrá utilizar este número si, por alguna razón, necesita buscar la entrada registrada del diario mediante este número.</span><span class="sxs-lookup"><span data-stu-id="1fb13-103">You can then use the number later if, for some reason, you need to search for the posted entry using this number.</span></span>  

<span data-ttu-id="1fb13-104">El campo **N.º doc. externo obligatorio** en la página **Configuración de ventas y cobros** especifica si es obligatorio introducir un número de documento externo en el campo **N.º documento externo** en una cabecera de ventas y el campo **N.º documento externo** en una línea de diario general.</span><span class="sxs-lookup"><span data-stu-id="1fb13-104">The **Ext. Doc. No. Mandatory** field on the **Sales & Receivables Setup** page specifies whether it is mandatory to enter an external document number in the **External Document No.** field on a sales header and the **External Document No.** field on a general journal line.</span></span>

<span data-ttu-id="1fb13-105">Si selecciona este campo, no se podrá registrar ninguna factura ni ninguna línea de diario sin un número de documento externo.</span><span class="sxs-lookup"><span data-stu-id="1fb13-105">If you select this field, it will not be possible to post an invoice or a general journal line without an external document number.</span></span>

<span data-ttu-id="1fb13-106">El número de documento externo se incluye en los documentos registrados donde puede buscar por el número relevante.</span><span class="sxs-lookup"><span data-stu-id="1fb13-106">The external document number is included in posted documents where you can search by the relevant number.</span></span> <span data-ttu-id="1fb13-107">También puede buscar utilizando el número de documento externo al navegar por los asientos de los movimientos de clientes.</span><span class="sxs-lookup"><span data-stu-id="1fb13-107">You can also search using the external document number when navigating on customer ledger entries.</span></span>

<span data-ttu-id="1fb13-108">Una forma diferente de gestionar los números de documento externo es usar el campo **Su referencia**.</span><span class="sxs-lookup"><span data-stu-id="1fb13-108">A different way to handle external document numbers is to use the **Your Reference** field.</span></span> <span data-ttu-id="1fb13-109">Si usa el campo **Su referencia**, el número se incluirá en los documentos publicados y puede buscar según este campo de la misma manera que para los valores de los campos **N.º documento externo**.</span><span class="sxs-lookup"><span data-stu-id="1fb13-109">If you use the **Your Reference** field, the number will be included in posted documents, and you can search by it in the same way as for values from **External Document No.** fields.</span></span> <span data-ttu-id="1fb13-110">Pero el campo no está disponible en líneas del diario.</span><span class="sxs-lookup"><span data-stu-id="1fb13-110">But the field is not available on journal lines.</span></span>
