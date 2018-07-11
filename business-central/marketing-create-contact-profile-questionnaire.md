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
ms.date: 05/09/2018
ms.translationtype: HT
ms.sourcegitcommit: 75501b9402bb1c14fcfeb2fc6e61f055a2247493
ms.openlocfilehash: 00cfce8b467040a4de419c1b59a258c0eacf0b9a
ms.contentlocale: es-es
ms.lasthandoff: 05/15/2018

---

# <a name="use-profile-questionnaires-to-classify-business-contacts"></a>Use cuestionarios de perfil para clasificar contactos comerciales
Puede configurar los cuestionarios de perfil que desea utilizar en el momento de especificar información de los perfiles de sus contactos. En cada cuestionario, puede configurar distintas preguntas que desee realizar a sus contactos.  

Puede ejecutar el cuestionario para que responder de forma automática algunas de las preguntas, según los datos del contacto, cliente o proveedor.  

## <a name="to-add-a-profile-questionnaire"></a>Para añadir un cuestionario de perfil
1.  Elija el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Configuración cuestionario** y, a continuación, seleccione el vínculo relacionado.  
2.  En la pestaña **Inicio**, en el grupo **Nuevo**, seleccione **Nuevo**.  
3.  Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-add-questions-to-a-profile-questionnaire"></a>Para añadir preguntas a un cuestionario de perfil
1.  Seleccione el cuestionario de perfil correspondiente y, en la pestaña **Inicio**, grupo **Procesar**, elija **Editar config. cuestionario**.  
2.  En la primera línea vacía, en el campo **Tipo**, elija **Pregunta** y escriba su pregunta en el campo **Descripción**. Rellene los otros campos de la línea.  
3.  En la siguiente línea vacía, en el campo **Tipo**, elija **Respuesta** y escriba su respuesta en el campo **Descripción**.  
4.  En el campo **Prioridad**, seleccione la prioridad. En los campos **Desde valor** y **Hasta valor**, defina un intervalo de punto. Los contactos que reciban puntos en el rango definido obtendrán la respuesta.  

Repita estos pasos para especificar todas las preguntas y respuestas del cuestionario de perfil.

Tras crear un cuestionario, debe crear clasificaciones de contactos para clasificar sus contactos. También puede configurar preguntas que se clasifican automáticamente según la información en la ficha de contacto.  

> [!NOTE]
> Si especifica una pregunta que el sistema responde de forma automática, seleccione <STRONG>Línea</STRONG> y, a continuación, <STRONG>Detalles pregunta</STRONG> para especificar los criterios para responder a la pregunta automáticamente.

## <a name="the-automatic-classification-of-contacts"></a>la clasificación automática de los contactos
Puede clasificar automáticamente sus contactos según la información de cliente, proveedor y contacto, si configura las preguntas del perfil en la ventana **Config. cuestionario perfil**.  

> [!NOTE]
> Sólo a los contactos registrados como clientes se les puede asignar una clasificación según los datos de cliente y sólo a los contactos registrados como proveedores se les puede asignar una clasificación según datos de proveedor. La clasificación automática no se actualiza automáticamente. Por lo tanto, quizás desee actualizar los cuestionarios de perfil, después de actualizar los datos del cliente, proveedor o contacto en los que se basa.  

Después de haber configurado las preguntas del perfil automático, si asigna el cuestionario de perfil que contiene esas preguntas a un contacto, [!INCLUDE[d365fin](includes/d365fin_md.md)] asignará automáticamente las respuestas correctas para ese contacto.  

## <a name="example"></a>Ejemplo
Puede clasificar sus contactos según el volumen de compras que le hagan:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Respuesta</strong></th>
<th><strong>Se aplica a</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>A</p></td>
<td><p>contactos que han comprado 500.000 DL o más</p></td>
</tr>
<tr class="even">
<td><p>B</p></td>
<td><p>contactos que han comprado de 100.000 DL hasta 499.999 DL</p></td>
</tr>
<tr class="odd">
<td><p>C</p></td>
<td><p>contactos que han comprado 99.999 DL o menos</p></td>
</tr>
</tbody>
</table>

Para ello, rellene los datos de la ventana **Config. cuestionario perfil** de esta manera:


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
<th><strong>Tipo</strong></th>
<th><strong>Descripción</strong></th>
<th><strong>Clasificación automática</strong></th>
<th><strong>Desde valor</strong></th>
<th><strong>Hasta valor</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Pregunta</p></td>
<td><p>Clasificación ABC</p></td>
<td><p>Haga clic para activar el campo</p></td>
<td><p> </p></td>
<td><p> </p></td>
</tr>
<tr class="even">
<td><p>Respuesta</p></td>
<td><p>A</p></td>
<td><p> </p></td>
<td><p>500.000</p></td>
<td><p> </p></td>
</tr>
<tr class="odd">
<td><p>Respuesta</p></td>
<td><p>B</p></td>
<td><p> </p></td>
<td><p>100.000</p></td>
<td><p>499.999</p></td>
</tr>
<tr class="even">
<td><p>Respuesta</p></td>
<td><p>C</p></td>
<td><p> </p></td>
<td><p> </p></td>
<td><p>99.999</p></td>
</tr>
</tbody>
</table>

A continuación, rellene los datos de la ventana **Detalles pregunta perfil** de la siguiente manera:
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Campo</strong></th>
<th><strong>Valor</strong></th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>Campo de clasificación de cliente</strong></td>
<td><emphasis>Ventas (DL)</emphasis></td>
</tr>
<tr>
<td><strong>Método clasificación</strong></td>
<td><emphasis>Valor definido</emphasis></td>
</tr>
</tbody>
</table>

Al asignar el cuestionario perfil que contiene esta pregunta a un contacto, el programa escribe automáticamente la respuesta adecuada para este contacto en las líneas de perfil de la ficha de contacto.

## <a name="see-also"></a>Consulte también
[Crear personas de contacto](marketing-create-contact-persons.md)  
[Crear personas de contacto](marketing-how-create-contact-persons.md)  
[Crear empresas de contacto](marketing-create-contact-companies.md)  
