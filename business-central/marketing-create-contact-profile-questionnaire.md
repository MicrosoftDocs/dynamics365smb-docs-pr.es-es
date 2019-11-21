---
title: Usa perfiles para clasificar contactos
description: Configure cuestionarios de perfil para ayudarlo a clasificar sus contactos comerciales
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: contacts, profiles
ms.author: edupont
ms.date: 10/01/2019
ms.openlocfilehash: 8d25dc4c27be6069782ff30e785f884ee406d2e4
ms.sourcegitcommit: 319023e53627dbe8e68643908aacc6fd594a4957
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2019
ms.locfileid: "2553947"
---
# <a name="use-profile-questionnaires-to-classify-business-contacts"></a><span data-ttu-id="a6a1b-103">Use cuestionarios de perfil para clasificar contactos comerciales</span><span class="sxs-lookup"><span data-stu-id="a6a1b-103">Use Profile Questionnaires to Classify Business Contacts</span></span>
<span data-ttu-id="a6a1b-104">Puede configurar los cuestionarios de perfil que desea utilizar en el momento de especificar información de los perfiles de sus contactos.</span><span class="sxs-lookup"><span data-stu-id="a6a1b-104">You can set up profile questionnaires that you want to use when entering information about your contacts' profiles.</span></span> <span data-ttu-id="a6a1b-105">En cada cuestionario, puede configurar distintas preguntas que desee realizar a sus contactos.</span><span class="sxs-lookup"><span data-stu-id="a6a1b-105">Within each questionnaire, you can set up the different questions you intend to ask your contacts.</span></span>  

<span data-ttu-id="a6a1b-106">Puede ejecutar el cuestionario para que responder de forma automática algunas de las preguntas, según los datos del contacto, cliente o proveedor.</span><span class="sxs-lookup"><span data-stu-id="a6a1b-106">You can also run the questionnaire to answer some of the questions based on contact, customer, or vendor data automatically.</span></span>  

## <a name="to-add-a-profile-questionnaire"></a><span data-ttu-id="a6a1b-107">Para añadir un cuestionario de perfil</span><span class="sxs-lookup"><span data-stu-id="a6a1b-107">To add a profile questionnaire</span></span>
1.  <span data-ttu-id="a6a1b-108">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Configuración de cuestionario** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="a6a1b-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Questionnaire Setup**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="a6a1b-109">Seleccione la acción **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="a6a1b-109">Choose the **New** Action.</span></span>  
3.  <span data-ttu-id="a6a1b-110">Rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="a6a1b-110">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-add-questions-to-a-profile-questionnaire"></a><span data-ttu-id="a6a1b-111">Para añadir preguntas a un cuestionario de perfil</span><span class="sxs-lookup"><span data-stu-id="a6a1b-111">To add questions to a profile questionnaire</span></span>
1.  <span data-ttu-id="a6a1b-112">Seleccione el cuestionario de perfil correspondiente y, a continuación, elija la acción **Editar config. cuestionario**.</span><span class="sxs-lookup"><span data-stu-id="a6a1b-112">Choose the relevant profile questionnaire, and then choose the **Edit Questionnaire Setup** action.</span></span>  
2.  <span data-ttu-id="a6a1b-113">En la primera línea vacía, en el campo **Tipo**, elija **Pregunta** y escriba su pregunta en el campo **Descripción**.</span><span class="sxs-lookup"><span data-stu-id="a6a1b-113">On the first empty line, in the **Type** field, choose **Question** and type your question in the **Description** field.</span></span> <span data-ttu-id="a6a1b-114">Rellene los otros campos de la línea.</span><span class="sxs-lookup"><span data-stu-id="a6a1b-114">Fill in the other fields on this line.</span></span>  
3.  <span data-ttu-id="a6a1b-115">En la siguiente línea vacía, en el campo **Tipo**, elija **Respuesta** y escriba su respuesta en el campo **Descripción**.</span><span class="sxs-lookup"><span data-stu-id="a6a1b-115">On the next empty line, in the **Type** field, choose **Answer** and type your answer in the **Description** field.</span></span>  
4.  <span data-ttu-id="a6a1b-116">En el campo **Prioridad**, seleccione la prioridad.</span><span class="sxs-lookup"><span data-stu-id="a6a1b-116">In the **Priority** field, select the priority.</span></span> <span data-ttu-id="a6a1b-117">En los campos **Desde valor** y **Hasta valor**, defina un intervalo de punto.</span><span class="sxs-lookup"><span data-stu-id="a6a1b-117">In the **From Value** and **To Value** fields, define a point range.</span></span> <span data-ttu-id="a6a1b-118">Los contactos que reciban puntos en el rango definido obtendrán la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a6a1b-118">Contacts that receive points within the defined range will get the answer.</span></span>  

<span data-ttu-id="a6a1b-119">Repita estos pasos para especificar todas las preguntas y respuestas del cuestionario de perfil.</span><span class="sxs-lookup"><span data-stu-id="a6a1b-119">Repeat these steps to enter all the questions and answers within the profile questionnaire.</span></span>

<span data-ttu-id="a6a1b-120">Tras crear un cuestionario, debe crear clasificaciones de contactos para clasificar sus contactos.</span><span class="sxs-lookup"><span data-stu-id="a6a1b-120">After you have created a questionnaire, you must create contact ratings to classify your contacts.</span></span> <span data-ttu-id="a6a1b-121">También puede configurar preguntas que se clasifican automáticamente según la información en la ficha de contacto.</span><span class="sxs-lookup"><span data-stu-id="a6a1b-121">You can also set up questions that are rated automatically based on information in the contact card.</span></span>  

> [!NOTE]
> <span data-ttu-id="a6a1b-122">Si especifica una pregunta que el sistema responde de forma automática, seleccione <STRONG>Línea</STRONG> y, a continuación, <STRONG>Detalles pregunta</STRONG> para especificar los criterios para responder a la pregunta automáticamente.</span><span class="sxs-lookup"><span data-stu-id="a6a1b-122">If you enter a question that is automatically answered, choose <STRONG>Line</STRONG>, and then choose <STRONG>Question Details</STRONG>, to enter the criteria to automatically answer the question.</span></span>

## <a name="the-automatic-classification-of-contacts"></a><span data-ttu-id="a6a1b-123">la clasificación automática de los contactos</span><span class="sxs-lookup"><span data-stu-id="a6a1b-123">The Automatic Classification of Contacts</span></span>
<span data-ttu-id="a6a1b-124">Puede clasificar automáticamente sus contactos según la información de cliente, proveedor y contacto, si configura las preguntas del perfil en la página **Config. cuestionario perfil**.</span><span class="sxs-lookup"><span data-stu-id="a6a1b-124">You can automatically classify your contacts according to customer, vendor, and contact information, by setting up automatically answered profile questions on the **Profile Questionnaire Setup** page.</span></span>  

> [!NOTE]
> <span data-ttu-id="a6a1b-125">Sólo a los contactos registrados como clientes se les puede asignar una clasificación según los datos de cliente y sólo a los contactos registrados como proveedores se les puede asignar una clasificación según datos de proveedor.</span><span class="sxs-lookup"><span data-stu-id="a6a1b-125">Only contacts that are recorded as customers can be assigned a classification based on customer data and only contacts that are recorded as vendors can be assigned a classification based on vendor data.</span></span> <span data-ttu-id="a6a1b-126">La clasificación automática no se actualiza automáticamente.</span><span class="sxs-lookup"><span data-stu-id="a6a1b-126">The automatic classification is not updated automatically.</span></span> <span data-ttu-id="a6a1b-127">Por lo tanto, quizás desee actualizar los cuestionarios de perfil, después de actualizar los datos del cliente, proveedor o contacto en los que se basa.</span><span class="sxs-lookup"><span data-stu-id="a6a1b-127">Consequently, you may want to update the profile questionnaires, after you have updated the customer, vendor or contact data they are based on.</span></span>  

<span data-ttu-id="a6a1b-128">Después de haber configurado las preguntas del perfil automático, si asigna el cuestionario de perfil que contiene esas preguntas a un contacto, [!INCLUDE[d365fin](includes/d365fin_md.md)] asignará automáticamente las respuestas correctas para ese contacto.</span><span class="sxs-lookup"><span data-stu-id="a6a1b-128">After you have set up automatically answered profile questions, if you assign the profile questionnaire containing these questions to a contact, [!INCLUDE[d365fin](includes/d365fin_md.md)] will automatically assign the right answers for the contact.</span></span>  

## <a name="example"></a><span data-ttu-id="a6a1b-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a6a1b-129">Example</span></span>
<span data-ttu-id="a6a1b-130">Puede clasificar sus contactos según el volumen de compras que le hagan:</span><span class="sxs-lookup"><span data-stu-id="a6a1b-130">You can classify your contacts according to how much they bought from you:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a6a1b-131"><strong>Respuesta</strong></span><span class="sxs-lookup"><span data-stu-id="a6a1b-131"><strong>Answer</strong></span></span></th>
<th><span data-ttu-id="a6a1b-132"><strong>Se aplica a</strong></span><span class="sxs-lookup"><span data-stu-id="a6a1b-132"><strong>Applies to</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a6a1b-133">A</span><span class="sxs-lookup"><span data-stu-id="a6a1b-133">A</span></span></p></td>
<td><p><span data-ttu-id="a6a1b-134">contactos que han comprado 500.000 DL o más</span><span class="sxs-lookup"><span data-stu-id="a6a1b-134">contacts who bought for 500,000 LCY or more</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6a1b-135">B</span><span class="sxs-lookup"><span data-stu-id="a6a1b-135">B</span></span></p></td>
<td><p><span data-ttu-id="a6a1b-136">contactos que han comprado de 100.000 DL hasta 499.999 DL</span><span class="sxs-lookup"><span data-stu-id="a6a1b-136">contacts who bought for 100,000 up to 499,999 LCY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6a1b-137">U</span><span class="sxs-lookup"><span data-stu-id="a6a1b-137">C</span></span></p></td>
<td><p><span data-ttu-id="a6a1b-138">contactos que han comprado 99.999 DL o menos</span><span class="sxs-lookup"><span data-stu-id="a6a1b-138">contacts who bought for 99,999 LCY or less</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a6a1b-139">Para ello, rellene los datos de la página **Config. cuestionario perfil** de esta manera:</span><span class="sxs-lookup"><span data-stu-id="a6a1b-139">To do this, fill on the **Profile Questionnaire Setup** page as follows:</span></span>


<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a6a1b-140"><strong>Escriba</strong></span><span class="sxs-lookup"><span data-stu-id="a6a1b-140"><strong>Type</strong></span></span></th>
<th><span data-ttu-id="a6a1b-141"><strong>Descripción</strong></span><span class="sxs-lookup"><span data-stu-id="a6a1b-141"><strong>Description</strong></span></span></th>
<th><span data-ttu-id="a6a1b-142"><strong>Clasificación automática</strong></span><span class="sxs-lookup"><span data-stu-id="a6a1b-142"><strong>Automatic Classification</strong></span></span></th>
<th><span data-ttu-id="a6a1b-143"><strong>Desde valor</strong></span><span class="sxs-lookup"><span data-stu-id="a6a1b-143"><strong>From Value</strong></span></span></th>
<th><span data-ttu-id="a6a1b-144"><strong>Hasta valor</strong></span><span class="sxs-lookup"><span data-stu-id="a6a1b-144"><strong>To Value</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a6a1b-145">Pregunta</span><span class="sxs-lookup"><span data-stu-id="a6a1b-145">Question</span></span></p></td>
<td><p><span data-ttu-id="a6a1b-146">Clasificación ABC</span><span class="sxs-lookup"><span data-stu-id="a6a1b-146">ABC Classification</span></span></p></td>
<td><p><span data-ttu-id="a6a1b-147">Haga clic para activar el campo</span><span class="sxs-lookup"><span data-stu-id="a6a1b-147">Click to insert a check mark</span></span></p></td>
<td><p> </p></td>
<td><p> </p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6a1b-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a6a1b-148">Answer</span></span></p></td>
<td><p><span data-ttu-id="a6a1b-149">A</span><span class="sxs-lookup"><span data-stu-id="a6a1b-149">A</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="a6a1b-150">500.000</span><span class="sxs-lookup"><span data-stu-id="a6a1b-150">500,000</span></span></p></td>
<td><p> </p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6a1b-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a6a1b-151">Answer</span></span></p></td>
<td><p><span data-ttu-id="a6a1b-152">P</span><span class="sxs-lookup"><span data-stu-id="a6a1b-152">B</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="a6a1b-153">100,000</span><span class="sxs-lookup"><span data-stu-id="a6a1b-153">100,000</span></span></p></td>
<td><p><span data-ttu-id="a6a1b-154">499,999</span><span class="sxs-lookup"><span data-stu-id="a6a1b-154">499,999</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6a1b-155">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a6a1b-155">Answer</span></span></p></td>
<td><p><span data-ttu-id="a6a1b-156">U</span><span class="sxs-lookup"><span data-stu-id="a6a1b-156">C</span></span></p></td>
<td><p> </p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="a6a1b-157">99,999</span><span class="sxs-lookup"><span data-stu-id="a6a1b-157">99,999</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a6a1b-158">A continuación, rellene los datos de la página **Detalles pregunta perfil** de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="a6a1b-158">Then fill on the **Profile Question Details** page as follows:</span></span>
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a6a1b-159"><strong>Campo</strong></span><span class="sxs-lookup"><span data-stu-id="a6a1b-159"><strong>Field</strong></span></span></th>
<th><span data-ttu-id="a6a1b-160"><strong>Valor</strong></span><span class="sxs-lookup"><span data-stu-id="a6a1b-160"><strong>Value</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a6a1b-161"><strong>Campo de clasificación de cliente</strong></span><span class="sxs-lookup"><span data-stu-id="a6a1b-161"><strong>Customer Classification Field</strong></span></span></td>
<td><span data-ttu-id="a6a1b-162"><emphasis>Ventas (DL)</emphasis></span><span class="sxs-lookup"><span data-stu-id="a6a1b-162"><emphasis>Sales (LCY)</emphasis></span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a6a1b-163"><strong>Método clasificación</strong></span><span class="sxs-lookup"><span data-stu-id="a6a1b-163"><strong>Classification Method</strong></span></span></td>
<td><span data-ttu-id="a6a1b-164"><emphasis>Valor definido</emphasis></span><span class="sxs-lookup"><span data-stu-id="a6a1b-164"><emphasis>Defined Value</emphasis></span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a6a1b-165">Al asignar el cuestionario perfil que contiene esta pregunta a un contacto, la aplicación escribe automáticamente la respuesta adecuada para este contacto en las líneas de perfil de la ficha de contacto.</span><span class="sxs-lookup"><span data-stu-id="a6a1b-165">When you assign the profile questionnaire containing this question to a contact, application automatically enters the relevant answer for this contact on the profile lines of the contact card.</span></span>

## <a name="see-also"></a><span data-ttu-id="a6a1b-166">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a6a1b-166">See Also</span></span>
[<span data-ttu-id="a6a1b-167">Crear contactos</span><span class="sxs-lookup"><span data-stu-id="a6a1b-167">Creating Contacts</span></span>](marketing-create-contact-companies.md)  
