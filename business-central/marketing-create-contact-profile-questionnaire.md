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
ms.date: 04/01/2020
ms.openlocfilehash: 9cf4817cd85951f193ffadbcd3e7ebc971bcca36
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/01/2020
ms.locfileid: "3181585"
---
# <a name="use-profile-questionnaires-to-classify-business-contacts"></a>Use cuestionarios de perfil para clasificar contactos comerciales
Puede configurar los cuestionarios de perfil que desea utilizar en el momento de especificar información de los perfiles de sus contactos. En cada cuestionario, puede configurar distintas preguntas que desee realizar a sus contactos.  

Puede ejecutar el cuestionario para que responder de forma automática algunas de las preguntas, según los datos del contacto, cliente o proveedor.  

## <a name="to-add-a-profile-questionnaire"></a>Para añadir un cuestionario de perfil
1.  Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), introduzca **Configuración de cuestionario** y luego elija el enlace relacionado.  
2.  Seleccione la acción **Nuevo**.  
3.  Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-add-questions-to-a-profile-questionnaire"></a>Para añadir preguntas a un cuestionario de perfil
1.  Seleccione el cuestionario de perfil correspondiente y, a continuación, elija la acción **Editar config. cuestionario**.  
2.  En la primera línea vacía, en el campo **Tipo**, elija **Pregunta** y escriba su pregunta en el campo **Descripción**. Rellene los otros campos de la línea.  
3.  En la siguiente línea vacía, en el campo **Tipo**, elija **Respuesta** y escriba su respuesta en el campo **Descripción**.  
4.  En el campo **Prioridad**, seleccione la prioridad. En los campos **Desde valor** y **Hasta valor**, defina un intervalo de punto. Los contactos que reciban puntos en el rango definido obtendrán la respuesta.  

Repita estos pasos para especificar todas las preguntas y respuestas del cuestionario de perfil.

Tras crear un cuestionario, debe crear clasificaciones de contactos para clasificar sus contactos. También puede configurar preguntas que se clasifican automáticamente según la información en la ficha de contacto.  

> [!NOTE]
> Si especifica una pregunta que el sistema responde de forma automática, seleccione <STRONG>Línea</STRONG> y, a continuación, <STRONG>Detalles pregunta</STRONG> para especificar los criterios para responder a la pregunta automáticamente.

## <a name="the-automatic-classification-of-contacts"></a>la clasificación automática de los contactos
Puede clasificar automáticamente sus contactos según la información de cliente, proveedor y contacto, si configura las preguntas del perfil en la página **Config. cuestionario perfil**.  

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
<td><p>U</p></td>
<td><p>contactos que han comprado 99.999 DL o menos</p></td>
</tr>
</tbody>
</table>

Para ello, rellene los datos de la página **Config. cuestionario perfil** de esta manera:


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
<th><strong>Escriba</strong></th>
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
<td><p> </p></td>
<td><p> </p></td>
</tr>
<tr class="even">
<td><p>Respuesta</p></td>
<td><p>A</p></td>
<td><p> </p></td>
<td><p>500.000</p></td>
<td><p> </p></td>
</tr>
<tr class="odd">
<td><p>Respuesta</p></td>
<td><p>P</p></td>
<td><p> </p></td>
<td><p>100,000</p></td>
<td><p>499,999</p></td>
</tr>
<tr class="even">
<td><p>Respuesta</p></td>
<td><p>U</p></td>
<td><p> </p></td>
<td><p> </p></td>
<td><p>99,999</p></td>
</tr>
</tbody>
</table>

A continuación, rellene los datos de la página **Detalles pregunta perfil** de la siguiente manera:
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

Al asignar el cuestionario perfil que contiene esta pregunta a un contacto, la aplicación escribe automáticamente la respuesta adecuada para este contacto en las líneas de perfil de la ficha de contacto.

## <a name="see-also"></a>Consulte también
[Crear contactos](marketing-create-contact-companies.md)  
