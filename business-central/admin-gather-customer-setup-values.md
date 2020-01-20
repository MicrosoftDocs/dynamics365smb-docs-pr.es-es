---
title: Recopilación de valores de configuración de cliente | Documentos de Microsoft
description: Utilice el cuestionario de configuración para ayudar a reducir su carga de trabajo de implementación agilizando la tarea de configurar la empresa nueva. Puede generar el cuestionario de configuración en Business Central y después proporcionárselo al cliente como un archivo de Excel (.xlsx) o XML.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 4fc9ffe9205e8f075f1b133686c2b869495bf42a
ms.sourcegitcommit: 3d128a00358668b3fdd105ebf4604ca4e2b6743c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/20/2019
ms.locfileid: "2910861"
---
# <a name="gather-customer-setup-values"></a>Recopilación de valores de configuración de cliente
Utilice el cuestionario de configuración para ayudar a reducir su carga de trabajo de implementación agilizando la tarea de configurar la empresa nueva. Puede generar el cuestionario de configuración en [!INCLUDE[d365fin](includes/d365fin_md.md)] y después proporcionárselo al cliente como un archivo de Excel o XML.  

Puede cambiar todos los valores predeterminados en un cuestionario para ajustarse mejor a las necesidades del cliente.  

> [!TIP]  
>  Para obtener más información acerca de la configuración de los valores en los campos de planificación de suministros, consulte [Procedimientos recomendados de configuración: planificación de suministros](setup-best-practices-supply-planning.md).  

Cuando su cliente completa el cuestionario, importe el archivo en la nueva empresa de [!INCLUDE[d365fin](includes/d365fin_md.md)] del cliente. Usted y su cliente deben validar las respuestas del cuestionario antes de aplicarlas a la empresa.

## <a name="to-create-a-configuration-questionnaire"></a>Para crear un cuestionario de configuración
Puede usar un cuestionario para ayudarle a determinar el ámbito y necesidades de la configuración. Puede crear un nuevo cuestionario o modificar un cuestionario existente al agregar nuevas preguntas o áreas de preguntas.  

<!-- A configuration questionnaire has the following structure
* The name of the questionnaire itself
* Question Areas that group questions about a similar subject. For example, you might create a question area that focuses on entering company informtion. Typically, configuration questionnaires have many question groups
* Questions that are closed ended, meaning that the customer must choose an answer, and can choose only one. -->

 Puede crear cuestionarios para únicamente para tablas de tipo de configuración. Por ejemplo, puede utilizar la herramienta para proporcionar información a las páginas siguientes:  

-   Información de empresa  
-   Configuración activos fijos  
-   Configuración de contabilidad  
-   Configuración de inventario  
-   Conf. ensamblado
-   Configuración fabricación  
-   Configuración de compras y pagos  
-   Configuración de marketing  
-   Configuración del servicio  
-   Configuración de ventas y cobros  
-   Configuración almacén  

> [!NOTE]  
>  Para ver una lista completa de tablas de configuración, elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), introduzca **Configuración manual** y luego elija el enlace relacionado. Para determinar el ámbito de la migración de datos de registros, utilice la función de migración. Para obtener más información, consulte [Migrar datos del cliente](admin-migrate-customer-data.md).  

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), introduzca **cuestionarios de configuración** y luego elija el enlace relacionado.  
2. Seleccione la acción **Nuevo**.   
3. En la página **Cuestionario de configuración**, en el campo **Código**, introduzca ... 
<!--4. In the **Name** field, enter...
5. Choose the **Question Areas** action. .
6. On the **Config. Question Areas** page, in the **Code** field, enter...
  
    > [!Note]  
    > The code is alphanumeric, and must start with a letter of the alphabet.
7. In the Table ID field, choose the table to which to apply the answer to the question. Your selection will determine the fields that are available for the questions, and thereby the answer selections.
  
    > [!Tip]
    > The list of table objects is long. If you know the name of the table, use **Search** in the upper left to find it in the list.
8. In the **Description** field, enter text that indicates the subject of the question group.
9. In the **No.** field, enter a number to define where the question appears in the sequence of questions.
10. In the **Field ID** field, choose the field the the customer's answer will be applied to. You can choose from the fields on the table you chose in the **Table ID** field.
  
    When you choose a field, [!INCLUDE[d365fin](includes/d365fin_md.md)] provides a suggestion in the **Question** field. You can edit the question if needed.
11. To add more questions to the questionnaire, repeat steps seven through 10.

> [!Tip]
> If at some point you change a question, or add a new one, choose the **Update Questions** action to update the list.

-->

3. Seleccione la acción **Áreas preguntas**. Se abre la página **Áreas de pregunta**.  
4. Seleccione la acción **Nuevo**. Se abre la página **Configurar área de pregunta**.  
5. En el campo **Id. de tabla**, seleccione el Id. de la tabla para la que desea recopilar información. El campo **Nombre de tabla** se rellena automáticamente.  
6. Seleccione la acción **Actualizar preguntas**. Cada campo de la tabla se agrega al cuestionario con un signo de interrogación seguido de su etiqueta.

Puede reformular la etiqueta para clarificar cómo se debe responder la pregunta. Por ejemplo, si un campo se denomina “Nombre”, podría modificarlo para indicar “Cuál es el nombre de <data being collected>”. También puede proporcionar orientación en el campo **Referencia**, incluida una URL a una página que proporciona información adicional.  

También se pueden eliminar las preguntas que no desea incluir en el cuestionario.  

> [!NOTE]  
>  El campo **Opción respuesta** describe el tipo y el formato de la respuesta de los datos apropiados. El campo **Respuesta** contiene información proporcionada por el usuario.  
>   
>  Según sea necesario, puede definir respuestas predeterminadas en el campo **Respuesta**. Estos valores se utilizan de forma predeterminada para la configuración personalizada. Sin embargo, la persona que rellena el cuestionario puede modificar y actualizar la respuesta.  

## <a name="to-complete-the-configuration-questionnaire"></a>Completar el cuestionario de configuración
Utilice el cuestionario de configuración para estructurar y documentar una discusión detallada acerca de las necesidades específicas del cliente. También se utiliza para recopilar los datos de configuración del cliente para configurar las tablas de configuración de [!INCLUDE[d365fin](includes/d365fin_md.md)] pertinentes, como la contabilidad, el inventario y los clientes.  

> [!NOTE]  
>  También puede crear su propio cuestionario de configuración para ajustarse a sus necesidades.  

1. Abra la empresa para la que desea completar el cuestionario.
2. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), introduzca **Cuestionarios de configuración** y luego elija el enlace relacionado.  
3. Seleccione el cuestionario para la empresa y luego elija la acción **Exportar a Excel**, de forma opcional la acción **Exportar a XML**.
4. Haga que el cliente complete el cuestionario de configuración al especificar las respuestas en el libro de Excel. Existen hojas de cálculo para cada una de las áreas de preguntas que se han creado para el cuestionario.   
5. Guarde el libro de Excel como *Datos XML*. Seleccione la acción **Importar desde XML** y seleccione el archivo .xml con las respuestas de cliente.
6. Seleccione la acción **Áreas pregunta** para iniciar el proceso de validación y aplicación de las respuestas al cuestionario de configuración.  

## <a name="to-complete-a-questionnaire-from-the-configuration-worksheet"></a>Procedimiento para completar un cuestionario de desde la hoja de trabajo de configuración  
En el procedimiento siguiente se proporciona una forma alternativa de acceder a los cuestionarios de configuración. Se presupone que el paquete de configuración que ha recibido incluye cuestionarios.  

1. Después de importar un paquete de configuración, abra la hoja de trabajo de configuración.  
2. Para las tablas en las que hay un área de preguntas, elija la acción **Preguntas**. Se abre la página del cuestionario.  
3. Responda las preguntas y, a continuación, elija la acción **Aplicar respuestas**.  
4. Elija el botón **Aceptar** para cerrar el cuestionario.

## <a name="to-validate-the-configuration-questionnaire"></a>Validar el cuestionario de configuración
Es importante validar el cuestionario de configuración antes de aplicarlo al formato de [!INCLUDE[d365fin](includes/d365fin_md.md)]. También es una manera de asegurarse de que el formato de los datos se preserva durante la importación desde Excel.  

Una tarea de validación habitual consiste en comprobar que no hay cadenas de texto introducidas en los campos de fecha. Este proceso de revisión es necesario porque el formato de la respuesta en el cuestionario no se valida automáticamente cuando ejecuta la función **Aplicar respuestas**.  

> [!NOTE]  
>  En general, la validación del cuestionario de configuración es un proceso manual. Sin embargo, se comprueba si hay incoherencias regionales de formato. Además, se producirán errores si la estructura de la base de datos de [!INCLUDE[d365fin](includes/d365fin_md.md)] no coincide con la estructura de la base de datos de migración.  

1. En la página **Cuestionario configuración**, seleccione el cuestionario necesario y después seleccione la acción **Áreas de pregunta**.  
2. Abra el área de pregunta pertinente.  
3. Para cada pregunta, verifique que el valor del campo **Respuesta** se corresponde con el formato proporcionado en el campo **Opción respuesta**. Por ejemplo, verifique que la dirección de una empresa tiene formato de texto.  
4. Si encuentra errores, puede solucionarlos y hacer correcciones en Excel exportando el cuestionario y, a continuación, importándolo de nuevo. De forma alternativa, puede corregir los errores directamente en [!INCLUDE[d365fin](includes/d365fin_md.md)] a medida que revisa las respuestas de la página **Configurar área de pregunta**.  
5. Repita estos pasos para cada área de preguntas.  

Cuando termine la validación, los datos estarán preparados para aplicarse a la base de datos.  

## <a name="to-apply-answers-from-the-configuration-questionnaire"></a>Aplicar respuestas del cuestionario de configuración
Después de que haya importado y validado información de un cuestionario de configuración, puede transferir o aplicar los datos de configuración a las tablas correspondientes en la base de datos de [!INCLUDE[d365fin](includes/d365fin_md.md)].  

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), introduzca **cuestionarios de configuración** y luego elija el enlace relacionado. Se abre la página **Cuestionario configuración**.  
2. Seleccione un cuestionario de configuración de la lista y elija la acción **Editar lista**.  
3. Puede aplicar respuestas de dos maneras.  

- Para aplicar el cuestionario completo, seleccione la acción **Aplicar respuestas**.  
- Para aplicar las respuestas para un **Área de preguntas** específica únicamente, seleccione la acción **Áreas pregunta**, un **Área preguntas** de la lista y, a continuación, elija la acción **Aplicar respuestas**.  

### <a name="to-verify-that-answers-have-been-applied-successfully"></a>Para comprobar que las respuestas se hayan aplicado correctamente  
1. Compruebe las páginas de configuración de las diversas áreas funcionales de [!INCLUDE[d365fin](includes/d365fin_md.md)]. Para localizar la página, elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), introduzca el nombre de la página a mostrar y, a continuación, elija el vínculo relacionado.  
2. Compruebe que los campos se hayan rellenado con los datos correctos de las distintas áreas de pregunta en el cuestionario de configuración.  

Ahora ha definido la configuración con la información y las reglas de negocio del cliente.

## <a name="see-also"></a>Consulte también  
[Configurar una empresa con RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Administración](admin-setup-and-administration.md)
