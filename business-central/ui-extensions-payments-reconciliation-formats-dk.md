---
title: Utilizar la extensión de pagos y conciliaciones (DK) | Documentos de Microsoft
description: Esta extensión facilita la exportación de archivos con formato predefinido para cumplir con los requisitos del banco para envíos electrónicos.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: extension, bank, formats
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: 13ef7eb6cdda472d68758e7e6ef5cb7d73d9fba4
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5384079"
---
# <a name="the-payments-and-reconciliations-dk-extension"></a><span data-ttu-id="d1b51-103">Extensión de pagos y conciliaciones (DK)</span><span class="sxs-lookup"><span data-stu-id="d1b51-103">The Payments and Reconciliations (DK) Extension</span></span>

<span data-ttu-id="d1b51-104">Realice pagos rápidos y sin errores exportando archivos formateados específicamente para intercambios con su proveedor o banco.</span><span class="sxs-lookup"><span data-stu-id="d1b51-104">Make fast, error-free payments by exporting files that are formatted specifically for exchanges with your vendor or bank.</span></span> <span data-ttu-id="d1b51-105">Estos archivos aceleran los procesos de pago y conciliación, y eliminan los errores que pueden ocurrir al ingresar manualmente la información en un sitio web de un banco.</span><span class="sxs-lookup"><span data-stu-id="d1b51-105">These files speed up the payment and reconciliation processes, and eliminate errors that can happen when you manually enter the information on a bank website.</span></span>  

<span data-ttu-id="d1b51-106">Esta extensión admite los formatos de archivo para varios bancos de Dinamarca.</span><span class="sxs-lookup"><span data-stu-id="d1b51-106">This extension supports file formats for several Danish banks.</span></span> <span data-ttu-id="d1b51-107">Cuando exporta información de pago a un archivo, la extensión empaqueta los datos en el formato que su banco requiere.</span><span class="sxs-lookup"><span data-stu-id="d1b51-107">When you export payment information to a file, the extension packages the data into the format that your bank requires.</span></span> <span data-ttu-id="d1b51-108">Por ejemplo, algunos de los formatos son Bankdata-V3, BEC, SDC y FIK, que utilizan muchos bancos diferentes, y algunos que son más especializados para ciertos bancos, por ejemplo, Danske Bank y Nordea.</span><span class="sxs-lookup"><span data-stu-id="d1b51-108">For example, the formats include Bankdata-V3, BEC, SDC, and FIK, which many different banks use, and some that are more specialized for certain banks, for example, Danske Bank and Nordea.</span></span> <span data-ttu-id="d1b51-109">La extensión también incluye algunos formatos para importar y conciliar extractos bancarios.</span><span class="sxs-lookup"><span data-stu-id="d1b51-109">The extension also includes some formats for importing and reconciling bank statements.</span></span>  

> [!Note]
> <span data-ttu-id="d1b51-110">Para utilizar la extensión, es necesario conocer el formato que el banco o proveedor requiere.</span><span class="sxs-lookup"><span data-stu-id="d1b51-110">To use the extension, you must know the format that your bank or vendor requires.</span></span> <span data-ttu-id="d1b51-111">Algunos bancos o proveedores ofrecen esta información en las páginas web; sin embargo, es posible que deba contactar con su servicio de atención al cliente para obtener la información.</span><span class="sxs-lookup"><span data-stu-id="d1b51-111">Some banks or vendors provide this information on their websites; however, you might need to contact their customer service to get the information.</span></span>  

## <a name="supported-bank-formats"></a><span data-ttu-id="d1b51-112">Formatos bancarios compatibles</span><span class="sxs-lookup"><span data-stu-id="d1b51-112">Supported Bank Formats</span></span>
<span data-ttu-id="d1b51-113">Esta extensión puede liquidar los formatos de archivo siguiente para archivos de pagos:</span><span class="sxs-lookup"><span data-stu-id="d1b51-113">This extension can apply the following file formats for payment files:</span></span>  

* <span data-ttu-id="d1b51-114">BANKDATA-V3</span><span class="sxs-lookup"><span data-stu-id="d1b51-114">BANKDATA-V3</span></span>  
* <span data-ttu-id="d1b51-115">BEC-INDLAND</span><span class="sxs-lookup"><span data-stu-id="d1b51-115">BEC-INDLAND</span></span>  
* <span data-ttu-id="d1b51-116">BEC-CSV</span><span class="sxs-lookup"><span data-stu-id="d1b51-116">BEC-CSV</span></span>  
* <span data-ttu-id="d1b51-117">DANSKEBANK-CMKV</span><span class="sxs-lookup"><span data-stu-id="d1b51-117">DANSKEBANK-CMKV</span></span>  
* <span data-ttu-id="d1b51-118">DANSKEBANK-CMKXKSX</span><span class="sxs-lookup"><span data-stu-id="d1b51-118">DANSKEBANK-CMKXKSX</span></span>  
* <span data-ttu-id="d1b51-119">DANSKEBANK</span><span class="sxs-lookup"><span data-stu-id="d1b51-119">DANSKEBANK</span></span>  
* <span data-ttu-id="d1b51-120">FIK71</span><span class="sxs-lookup"><span data-stu-id="d1b51-120">FIK71</span></span>  
* <span data-ttu-id="d1b51-121">NORDEA-ERHVERV-CSV</span><span class="sxs-lookup"><span data-stu-id="d1b51-121">NORDEA-ERHVERV-CSV</span></span>  
* <span data-ttu-id="d1b51-122">NORDEA</span><span class="sxs-lookup"><span data-stu-id="d1b51-122">NORDEA</span></span>  
* <span data-ttu-id="d1b51-123">NORDEA-UNITEL-V3</span><span class="sxs-lookup"><span data-stu-id="d1b51-123">NORDEA-UNITEL-V3</span></span>  
* <span data-ttu-id="d1b51-124">SDC</span><span class="sxs-lookup"><span data-stu-id="d1b51-124">SDC</span></span>  
* <span data-ttu-id="d1b51-125">SDC-CSV</span><span class="sxs-lookup"><span data-stu-id="d1b51-125">SDC-CSV</span></span>  

## <a name="to-set-up-the-extension"></a><span data-ttu-id="d1b51-126">Para configurar la extensión</span><span class="sxs-lookup"><span data-stu-id="d1b51-126">To set up the extension</span></span>

<span data-ttu-id="d1b51-127">Existen algunos pasos a seguir para empezar.</span><span class="sxs-lookup"><span data-stu-id="d1b51-127">There are a few steps to get started.</span></span>  

* <span data-ttu-id="d1b51-128">Permitir exportaciones de datos de pagos.</span><span class="sxs-lookup"><span data-stu-id="d1b51-128">Allow payment data exports.</span></span> <span data-ttu-id="d1b51-129">Para ayudar a proteger sus datos, no se mostrarán.</span><span class="sxs-lookup"><span data-stu-id="d1b51-129">To help protect your data, this is not readily available.</span></span>  
* <span data-ttu-id="d1b51-130">Configurar compra y pagos de manera que no requieran números de documentos externos en las facturas.</span><span class="sxs-lookup"><span data-stu-id="d1b51-130">Set up purchase and payables so that you do not require external document numbers on invoices.</span></span> <span data-ttu-id="d1b51-131">Si es necesario, puede utilizar el número de referencia para hacer referencia a una factura específica.</span><span class="sxs-lookup"><span data-stu-id="d1b51-131">If needed, you can use the reference number to refer to a specific invoice.</span></span>  
* <span data-ttu-id="d1b51-132">Especificar la forma de pago de cada proveedor.</span><span class="sxs-lookup"><span data-stu-id="d1b51-132">Specify the payment method for each vendor.</span></span> <span data-ttu-id="d1b51-133">Las formas de pago definen cómo se pagan las facturas de los proveedores.</span><span class="sxs-lookup"><span data-stu-id="d1b51-133">Payment methods define how you pay invoices from the vendor.</span></span> <span data-ttu-id="d1b51-134">Por ejemplo, depósito bancario, efectivo, cheque o cuenta.</span><span class="sxs-lookup"><span data-stu-id="d1b51-134">For example, Bank, Cash, Check, or Account.</span></span>  
* <span data-ttu-id="d1b51-135">Especifique el tipo de formato que utiliza para cada uno de sus bancos.</span><span class="sxs-lookup"><span data-stu-id="d1b51-135">Specify the type of format to use for each of your bank accounts.</span></span> <span data-ttu-id="d1b51-136">Por ejemplo, NORDEA, DANSKEBANK, SDC, etc.</span><span class="sxs-lookup"><span data-stu-id="d1b51-136">For example, NORDEA, DANSKEBANK, SDC, and so on.</span></span>  

<span data-ttu-id="d1b51-137">Además, debe asignar a los proveedores a un **Grupo contable negocio** y un **Grupo contable proveedor** nacional.</span><span class="sxs-lookup"><span data-stu-id="d1b51-137">Additionally, you must assign vendors to a domestic **Gen. Bus. Posting Group** and a **Vendor Posting Group**.</span></span> <span data-ttu-id="d1b51-138">La configuración de país/región para el proveedor debe ser Dinamarca (DK).</span><span class="sxs-lookup"><span data-stu-id="d1b51-138">The Country/Region setting for the vendor must be Denmark (DK).</span></span> <span data-ttu-id="d1b51-139">Para obtener más información, consulte [Configurar los grupos contables](finance-posting-groups.md).</span><span class="sxs-lookup"><span data-stu-id="d1b51-139">For more information, see [Setting Up Posting Groups](finance-posting-groups.md).</span></span>  

### <a name="to-allow-prod_short-to-export-payment-data"></a><span data-ttu-id="d1b51-140">Para permitir que [!INCLUDE[prod_short](includes/prod_short.md)] realice exportaciones de datos de pagos</span><span class="sxs-lookup"><span data-stu-id="d1b51-140">To allow [!INCLUDE[prod_short](includes/prod_short.md)] to export payment data</span></span>

1. <span data-ttu-id="d1b51-141">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Diarios de pagos** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="d1b51-141">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Payment Journal**, and then choose the related link.</span></span>  
2. <span data-ttu-id="d1b51-142">En la página **Editar diario de pagos**, seleccione el proceso **Banco**.</span><span class="sxs-lookup"><span data-stu-id="d1b51-142">On the **Edit Payment Journal** page, choose the **Bank** batch.</span></span>  
3. <span data-ttu-id="d1b51-143">Seleccione la casilla de verificación **Permitir exportación de pagos**.</span><span class="sxs-lookup"><span data-stu-id="d1b51-143">Choose the **Allow Payment Export** check box.</span></span>  

### <a name="to-specify-a-payment-method-for-a-vendor"></a><span data-ttu-id="d1b51-144">Para especificar una forma de pago de un proveedor</span><span class="sxs-lookup"><span data-stu-id="d1b51-144">To specify a payment method for a vendor</span></span>

<span data-ttu-id="d1b51-145">La siguiente tabla muestra las combinaciones de formas de pago FIK y GIRO que [!INCLUDE[prod_short](includes/prod_short.md)] admite.</span><span class="sxs-lookup"><span data-stu-id="d1b51-145">The following table shows the combinations of FIK and GIRO payment methods that [!INCLUDE[prod_short](includes/prod_short.md)] supports.</span></span>

|<span data-ttu-id="d1b51-146">Combinación</span><span class="sxs-lookup"><span data-stu-id="d1b51-146">Combination</span></span>|<span data-ttu-id="d1b51-147">Tipo 01</span><span class="sxs-lookup"><span data-stu-id="d1b51-147">Type 01</span></span> | <span data-ttu-id="d1b51-148">Tipo 04</span><span class="sxs-lookup"><span data-stu-id="d1b51-148">Type 04</span></span> | <span data-ttu-id="d1b51-149">Tipo 71</span><span class="sxs-lookup"><span data-stu-id="d1b51-149">Type 71</span></span> | <span data-ttu-id="d1b51-150">Tipo 73</span><span class="sxs-lookup"><span data-stu-id="d1b51-150">Type 73</span></span> |
|----|--------|---------|---------|---------|
|<span data-ttu-id="d1b51-151">¿Número de cuenta de Giro o Número acreedor de FIK?</span><span class="sxs-lookup"><span data-stu-id="d1b51-151">Giro Account No. or FIK Creditor No.?</span></span> | <span data-ttu-id="d1b51-152">Número de cuenta de Giro</span><span class="sxs-lookup"><span data-stu-id="d1b51-152">Giro Account No.</span></span> | <span data-ttu-id="d1b51-153">Número de cuenta de Giro</span><span class="sxs-lookup"><span data-stu-id="d1b51-153">Giro Account No.</span></span> | <span data-ttu-id="d1b51-154">N.º acreedor de FIK</span><span class="sxs-lookup"><span data-stu-id="d1b51-154">FIK Creditor No.</span></span> | <span data-ttu-id="d1b51-155">N.º acreedor de FIK</span><span class="sxs-lookup"><span data-stu-id="d1b51-155">FIK Creditor No.</span></span>|
|<span data-ttu-id="d1b51-156">¿Se permiten los mensajes al destinatario?</span><span class="sxs-lookup"><span data-stu-id="d1b51-156">Allows Message to Recipient?</span></span> | <span data-ttu-id="d1b51-157">Sí</span><span class="sxs-lookup"><span data-stu-id="d1b51-157">Yes</span></span> |<span data-ttu-id="d1b51-158">No</span><span class="sxs-lookup"><span data-stu-id="d1b51-158">No</span></span> |<span data-ttu-id="d1b51-159">No</span><span class="sxs-lookup"><span data-stu-id="d1b51-159">No</span></span> | <span data-ttu-id="d1b51-160">Sí</span><span class="sxs-lookup"><span data-stu-id="d1b51-160">Yes</span></span> |
|<span data-ttu-id="d1b51-161">¿Contiene el número de referencia de pago?</span><span class="sxs-lookup"><span data-stu-id="d1b51-161">Contains Payment Reference number?</span></span> | <span data-ttu-id="d1b51-162">N.º</span><span class="sxs-lookup"><span data-stu-id="d1b51-162">No</span></span> | <span data-ttu-id="d1b51-163">Sí, 16 dígitos.</span><span class="sxs-lookup"><span data-stu-id="d1b51-163">Yes, 16 digits.</span></span> | <span data-ttu-id="d1b51-164">Sí, 15 dígitos.</span><span class="sxs-lookup"><span data-stu-id="d1b51-164">Yes, 15 digits.</span></span> | <span data-ttu-id="d1b51-165">No</span><span class="sxs-lookup"><span data-stu-id="d1b51-165">No</span></span>|

1. <span data-ttu-id="d1b51-166">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Proveedores** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="d1b51-166">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Vendors**, and then choose the related link.</span></span>  
2. <span data-ttu-id="d1b51-167">Abra la ficha, amplíe la pestaña **Pagos**, en el campo **Forma pago** seleccione la forma de pago.</span><span class="sxs-lookup"><span data-stu-id="d1b51-167">Open the card, expand the **Payments** tab, in the **Payment Method** field choose the payment method.</span></span>  
3. <span data-ttu-id="d1b51-168">Según de la opción que seleccione, debe rellenar otros campos.</span><span class="sxs-lookup"><span data-stu-id="d1b51-168">Depending on your selection, you must complete other fields.</span></span> <span data-ttu-id="d1b51-169">Consulte la tabla anterior para obtener una descripción de las combinaciones.</span><span class="sxs-lookup"><span data-stu-id="d1b51-169">See the table above for a description of the combinations.</span></span>  

### <a name="to-specify-the-format-to-use-for-a-bank-account"></a><span data-ttu-id="d1b51-170">Para especificar el formato que debe utilizar en un banco</span><span class="sxs-lookup"><span data-stu-id="d1b51-170">To specify the format to use for a bank account</span></span>

1. <span data-ttu-id="d1b51-171">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Bancos** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="d1b51-171">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Bank Accounts**, and then choose the related link.</span></span>  
2. <span data-ttu-id="d1b51-172">Abra la ficha del banco.</span><span class="sxs-lookup"><span data-stu-id="d1b51-172">Open the card for the bank account.</span></span>  
3. <span data-ttu-id="d1b51-173">En el campo **Formato de exportación de pagos**, seleccione el formato del archivo de exportación.</span><span class="sxs-lookup"><span data-stu-id="d1b51-173">In the **Payment Export Format** field, choose the format for your export file.</span></span>  

## <a name="choosing-the-fik-or-giro-payment-information-for-vendor-invoices"></a><span data-ttu-id="d1b51-174">Elección de la información de pago de FIK o Giro para facturas de proveedores</span><span class="sxs-lookup"><span data-stu-id="d1b51-174">Choosing the FIK or Giro payment information for vendor invoices</span></span>

1. <span data-ttu-id="d1b51-175">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Facturas de compra** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="d1b51-175">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Invoices**, and then choose the related link.</span></span>
2. <span data-ttu-id="d1b51-176">Seleccione el proveedor.</span><span class="sxs-lookup"><span data-stu-id="d1b51-176">Choose the vendor.</span></span> <span data-ttu-id="d1b51-177">Recuerde, debe ser un proveedor danés con una dirección en Dinamarca.</span><span class="sxs-lookup"><span data-stu-id="d1b51-177">Remember, this must be a Danish vendor with an address in Denmark.</span></span>
3. <span data-ttu-id="d1b51-178">Cree una factura.</span><span class="sxs-lookup"><span data-stu-id="d1b51-178">Create an invoice.</span></span> <span data-ttu-id="d1b51-179">Los campos **Forma pago** y **Número de proveedor** se rellenan según los valores de la ficha de proveedor.</span><span class="sxs-lookup"><span data-stu-id="d1b51-179">The **Payment Method** and **Vendor Number** fields are filled in based on settings on the Vendor card.</span></span> <span data-ttu-id="d1b51-180">Puede cambiarlo si lo desea.</span><span class="sxs-lookup"><span data-stu-id="d1b51-180">You can change them if you want.</span></span>
4. <span data-ttu-id="d1b51-181">En el campo **Referencia de pago**, introduzca el número de 15 dígitos de la factura del proveedor.</span><span class="sxs-lookup"><span data-stu-id="d1b51-181">In the **Payment Reference** field, enter the 15-digit number from the vendor invoice.</span></span>  

    > [!Tip]
    > <span data-ttu-id="d1b51-182">Tiene que agregar solo los 11 últimos dígitos del número.</span><span class="sxs-lookup"><span data-stu-id="d1b51-182">You only have to add the last 11 digits of the number.</span></span> [!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="d1b51-183">añadirá cuatro ceros al comienzo del número.</span><span class="sxs-lookup"><span data-stu-id="d1b51-183">will add four zeros to the beginning of the number.</span></span>  

5. <span data-ttu-id="d1b51-184">Registrar la factura.</span><span class="sxs-lookup"><span data-stu-id="d1b51-184">Post the invoice.</span></span>

## <a name="to-use-the-extension-to-export-payment-data"></a><span data-ttu-id="d1b51-185">Para utilizar la extensión para exportar datos de pago</span><span class="sxs-lookup"><span data-stu-id="d1b51-185">To use the extension to export payment data</span></span>

1. <span data-ttu-id="d1b51-186">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Diarios de pagos** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="d1b51-186">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Payment Journals**, and then choose the related link.</span></span>  
2. <span data-ttu-id="d1b51-187">Seleccione la acción **Proponer diarios de pagos a proveedores**.</span><span class="sxs-lookup"><span data-stu-id="d1b51-187">Choose the **Suggest Vendor Payment Journals** action.</span></span>  

    > [!Tip]
    > <span data-ttu-id="d1b51-188">Si desea exportar únicamente pagos específicos, utilice las opciones para filtrar los datos.</span><span class="sxs-lookup"><span data-stu-id="d1b51-188">If you want to export only specific payments, use the options for filtering the data.</span></span>  

3. <span data-ttu-id="d1b51-189">Si es necesario, puede agregar filtros para exportar únicamente pagos específicos.</span><span class="sxs-lookup"><span data-stu-id="d1b51-189">If needed, you can add filters to export only specific payments.</span></span>  
4. <span data-ttu-id="d1b51-190">En el campo **Tipo pago por banco**, elija **Pago electrónico**.</span><span class="sxs-lookup"><span data-stu-id="d1b51-190">In the **Bank Payment Type** field, choose **Electronic Payment**.</span></span>  
5. <span data-ttu-id="d1b51-191">Seleccione la acción **Exportar**.</span><span class="sxs-lookup"><span data-stu-id="d1b51-191">Choose the **Export** action.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d1b51-192">Consulte también .</span><span class="sxs-lookup"><span data-stu-id="d1b51-192">See also</span></span>

<span data-ttu-id="d1b51-193">[Personalizar Business Central for [!INCLUDE[prod_short](includes/prod_short.md)] con extensiones](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="d1b51-193">[Customizing Business Central for [!INCLUDE[prod_short](includes/prod_short.md)] Using Extensions](ui-extensions.md)</span></span>  
[<span data-ttu-id="d1b51-194">Cobrar pagos mediante adeudo directo SEPA</span><span class="sxs-lookup"><span data-stu-id="d1b51-194">Collect Payments with SEPA Direct Debit</span></span>](finance-collect-payments-with-sepa-direct-debit.md)  
[<span data-ttu-id="d1b51-195">Trabajar con diarios generales</span><span class="sxs-lookup"><span data-stu-id="d1b51-195">Working with General Journals</span></span>](ui-work-general-journals.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]