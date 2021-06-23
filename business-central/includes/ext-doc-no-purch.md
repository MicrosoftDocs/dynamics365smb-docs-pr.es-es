---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 05/27/2021
ms.author: edupont
ms.openlocfilehash: 59376b96dcd6f755040b07784ceca53e157bcf14
ms.sourcegitcommit: f9a190933eadf4608f591e2f1b04c69f1e5c0dc7
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/28/2021
ms.locfileid: "6115998"
---
<span data-ttu-id="ada28-101">En los documentos de compra y los diarios, puede especificar un número de documento que haga referencia al sistema de numeración del proveedor.</span><span class="sxs-lookup"><span data-stu-id="ada28-101">On purchase documents and journals, you can specify a document number that refers to the vendor's numbering system.</span></span> <span data-ttu-id="ada28-102">Utilice este campo para registrar el número que el proveedor asignó al pedido, la factura o el abono.</span><span class="sxs-lookup"><span data-stu-id="ada28-102">Use this field to record the number that the vendor assigned to the order, invoice, or credit memo.</span></span> <span data-ttu-id="ada28-103">Posteriormente podrá utilizar este número si, por alguna razón, necesita buscar la entrada registrada del diario mediante este número.</span><span class="sxs-lookup"><span data-stu-id="ada28-103">You can then use the number later if, for some reason, you need to search for the posted entry using this number.</span></span>

<span data-ttu-id="ada28-104">El campo **N.º doc. externo obligatorio** en la página **Configuración de compras y pagos** especifica si es obligatorio especificar un número de documento externo en las siguientes situaciones:</span><span class="sxs-lookup"><span data-stu-id="ada28-104">The **Ext. Doc. No. Mandatory** field in the **Purchases & Payables Setup** page specifies whether it is mandatory to enter an external document number in the following situations:</span></span>

* <span data-ttu-id="ada28-105">En los campos **N.º factura proveedor**, **N.º pedido proveedor**</span><span class="sxs-lookup"><span data-stu-id="ada28-105">In the **Vendor Invoice No.** field, **Vendor Order No.**</span></span> <span data-ttu-id="ada28-106">o **Nº abono proveedor**</span><span class="sxs-lookup"><span data-stu-id="ada28-106">field, or the **Vendor Cr. Memo No.**</span></span> <span data-ttu-id="ada28-107">en una cabecera de compra.</span><span class="sxs-lookup"><span data-stu-id="ada28-107">field on a purchase header</span></span>

* <span data-ttu-id="ada28-108">En el campo **Nº documento externo** de una línea del diario general, en la que el campo **Tipo documento** está establecido en *Factura*, *Abono* o *Documento de interés* y el campo **Tipo de cuenta** está establecido en *Proveedor*.</span><span class="sxs-lookup"><span data-stu-id="ada28-108">In the **External Document No.** field on a general journal line, where the **Document Type** field is set to *Invoice*, *Credit Memo*, or *Finance Charge Memo*, and the **Account Type** field is set to *Vendor*.</span></span>

<span data-ttu-id="ada28-109">Si selecciona este campo, no se podrá registrar ninguna factura, abono o el tipo de línea del diario cuyo valor en el campo Tipo mov. sea "Cliente" sin haber insertado previamente un número de documento externo.</span><span class="sxs-lookup"><span data-stu-id="ada28-109">If you select this field, it will not be possible to post an invoice, a credit memo, or the type of general journal line described above without an external document number.</span></span>

<span data-ttu-id="ada28-110">El número de documento externo se incluye en los documentos registrados donde puede buscar por el número relevante.</span><span class="sxs-lookup"><span data-stu-id="ada28-110">The external document number is included in posted documents where you can search by the relevant number.</span></span> <span data-ttu-id="ada28-111">También puede buscar utilizando el número de documento externo al navegar por los asientos de los movimientos de proveedores.</span><span class="sxs-lookup"><span data-stu-id="ada28-111">You can also search using the external document number when navigating on vendor ledger entries.</span></span>

<span data-ttu-id="ada28-112">Una forma diferente de gestionar los números de documento externo es usar el campo **Su referencia**.</span><span class="sxs-lookup"><span data-stu-id="ada28-112">A different way to handle external document numbers is to use the **Your Reference** field.</span></span> <span data-ttu-id="ada28-113">Si usa el campo **Su referencia**, el número se incluirá en los documentos publicados y puede buscar según este campo de la misma manera que para los valores de los campos **N.º documento externo**.</span><span class="sxs-lookup"><span data-stu-id="ada28-113">If you use the **Your Reference** field, the number will be included in posted documents, and you can search by it in the same way as for values from **External Document No.** fields.</span></span> <span data-ttu-id="ada28-114">Pero el campo no está disponible en líneas del diario.</span><span class="sxs-lookup"><span data-stu-id="ada28-114">But the field is not available on journal lines.</span></span>
