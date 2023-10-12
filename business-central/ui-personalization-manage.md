---
title: Personalización de páginas para roles
description: Aprenda a personalizar la interfaz de usuario para un perfil (rol) para que todos los usuarios asignados a ese rol vean un espacio de trabajo personalizado.
author: jswymer
ms.topic: conceptual
ms.search.keywords: 'customize, personalize, personalization, hide columns, remove fields, move fields'
ms.search.form: 9171
ms.date: 08/25/2023
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.custom: bap-template
---
# Personalizar páginas para perfiles

Business Central proporciona tanto [personalización](ui-personalization-user.md) para usuarios como personalización para administradores. La personalización permite a los usuarios adaptar su espacio de trabajo ajustando los diseños de página para adaptarlos a sus propias preferencias. Los administradores pueden personalizar diseños de páginas para un perfil específico, en función de los roles o departamentos empresariales, para que todos los usuarios asignados vean la misma página personalizada. Si bien la personalización permite a los usuarios mostrar, ocultar y mover campos y acciones en una página, la personalización ofrece capacidades adicionales. Por ejemplo, la personalización le permite mostrar campos que están en la tabla de origen o en las tablas de extensión de la página, pero que no están definidos en el objeto de la página, lo cual no es personalización posible.  <!--For more information, see [Personalize Your Workspace](ui-personalization-user.md).-->

<!--Similarly, administrators can customize pages for a profile, according to the related business role or department, so that all users assigned the profile see the customized page layout. As an administrator, you customize pages by using the same functionality as users do when they personalize pages, except with few extra capabilities. Like personalization, you can show, hide, and move fields, actions, or parts on a page. But while personalization only allows you to work with fields that are defined on the page object, customization allows you add fields that are in the source table or table extension, but not defined on the page object. -->

> [!NOTE]
> El uso de negocio típico de un perfil es un rol. Por lo tanto, un perfil se llama *Perfil (rol)* en la interfaz de usuario.

La personalización de la página comienza en la página **Perfiles (roles)**, el punto de partida del administrador para administrar los perfiles de los usuarios en fichas de perfil individuales. Además de personalizar el diseño de la página, puede controlar otras configuraciones para los perfiles en la página **Perfil (rol)** para cada perfil. Para obtener más información, consulte [Administrar perfiles](admin-users-profiles-roles.md).

## Requisitos previos

- Su cuenta de Business Central debe tener el conjunto de permisos **Gest. perf. D365** o permisos equivalentes. 

   El conjunto de permisos **Gest. perf. D365** incluye el permiso de ejecución en el objeto del sistema **9026 Agregar campo a tabla**. Si no tiene este permiso, no podrá agregar campos en la página a menos que estén definidos en el objeto de la página. 

## Personalizar páginas para un perfil

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Perfiles (roles)** y luego elija el enlace relacionado.
2. Seleccione la línea del perfil para el que desea personalizar páginas y, después, seleccione la acción **Editar**.
3. Elija la acción **Personalizar páginas**.

    [!INCLUDE[prod_short](includes/prod_short.md)] se abre en una nueva pestaña del explorador para el perfil seleccionado con el banner **Personalización** activado. El banner **Personalización** ofrece la misma funcionalidad que el banner **Personalización** que está disponible para los usuarios.

4. Personalice las páginas de acuerdo con las necesidades del rol o departamento en cuestión de la misma manera que lo haría un usuario al efectuar la personalización. Para obtener más información, consulte [Personalizar el área de trabajo](ui-personalization-user.md).

    > [!NOTE]
    > Para navegar durante la personalización, use <kbd>Ctrl</kbd>+<kbd>clic</kbd> en una acción si está resaltada por la punta de flecha.

5. Cuando haya terminado de cambiar el diseño de una o más páginas, elija el botón **Listo** en el banner **Personalización**.
6. Cierre la pestaña del explorador.

La personalización de las páginas se ha registrado ahora para el perfil.

## Ver todas las páginas personalizadas para un perfil

Puede obtener una visión general de qué páginas están personalizadas para un perfil, por ejemplo, para planificar cuáles personalizar o eliminar.

- En la página **Perfil (rol)**, elija la acción **Administrar páginas personalizadas**.

En la página **Páginas personalizadas**, puede eliminar personalizaciones y solucionar problemas mediante la búsqueda de posibles problemas.  

## Eliminar todas las personalizaciones de un perfil

Puede cancelar todas las personalizaciones que ha realizado en un perfil. Las personalizaciones introducidas con una extensión y las personalizaciones realizadas por un usuario no se eliminan. Puede eliminar todas las personalizaciones con otra acción. Para obtener más información, consulte [Para eliminar todas las personalizaciones efectuadas por un usuario](admin-users-profiles-roles.md#to-delete-all-personalizations-made-by-a-user).

- En la pestaña **Perfil (rol)** para un perfil personalizado, elija la acción **Borrar páginas personalizadas**.

El diseño en las páginas para el perfil se restablece al diseño predeterminado.  

## Eliminar la personalización de páginas específicas para un perfil

Puede eliminar personalizaciones de página individuales que ha efectuado para un perfil. Las personalizaciones introducidas con una extensión y las personalizaciones realizadas por un usuario no se eliminan. Puede eliminar las personalizaciones de página específicas con otra acción. Para obtener más información, consulte [Para eliminar las personalizaciones de páginas específicas](admin-users-profiles-roles.md#to-delete-personalizations-for-specific-pages).

1. En la página **Perfil (rol)**, elija la acción **Administrar páginas personalizadas**.
2. En la página **Páginas personalizadas**, seleccione una o más líneas de las personalizaciones de página que desea eliminar y, a continuación, elija la acción **Eliminar**.

El diseño en las páginas seleccionadas se ajusta a los cambios que ha hecho.

## Agregar un campo

Agrega campos a la página desde el panel **Agregar campo a la página**, que se abre seleccionando la acción **+ Campo** en el modo de personalización. Es importante comprender que el panel **Agregar campo a la página** se usa para mostrar campos que ya existen, en la página y sus tablas de origen, pero que actualmente están ocultos a la vista. No puede crear nuevos campos.

El panel **Agregar campo a la página** presenta todos los campos que se pueden mostrar en la página. Los campos se dividen en las siguientes categorías, según lo determinado por el diseño subyacente de la propia página, su tabla de origen y extensiones:

|Categoría|Descripción|
|-|-|
|Campos de tabla que no están en el objeto de página|Incluye campos que están definidos en la tabla base o en las tablas de extensión, pero que no están definidos en la página. La información sobre herramientas para estos campos incluye la etiqueta **Definido por la tabla**.<br><br>|
|Campos de página enlazados a una tabla|Incluye campos que se definen en la tabla base o en las extensiones de tabla y que también se definen en la página como mostrados u ocultos. La información sobre herramientas para estos campos incluye la etiqueta **Definido por la página**.|
|Campos de página que no están enlazados a una tabla| Campos que solo están definidos en la página, no en la tabla base o las tablas de extensión. Estos campos se utilizan normalmente para variables o cálculos. La información sobre herramientas para estos campos incluye la etiqueta **Definido por la página**.|

<!--
- Table fields not on the page object. Includes fields that are defined in the base table or extension tables, but aren't defined on the page, either as shown or hidden.   
- Page fields bound to a table. Includes fields that are defined in the base table or table extensions and are also defined on the page as either shown or hidden. 
 - Page fields that are not bound to a table. Fields that are Includes fields that are only defined on the page, not in base table or extension table. These fields typically used for variable or calculation. -->

Utilice el botón de filtro encima de la lista para cambiar qué categoría de campos se presentan en el panel **Agregar campo a página**.  

:::image type="content" source="media/customization-filter.svg" alt-text="Muestra el botón de filtro en el panel Agregar un campo en el modo de personalización.":::
 
### Agregar campo de tabla que no está en el objeto de página

Si desea que un campo de solo tabla esté disponible en una página para los usuarios , primero debe agregarlo a la página. Una vez que haya agregado el campo, los usuarios pueden elegir mostrar u ocultar el campo como quieran mediante personalización. Hay dos formas de agregar un campo.

- Una forma es arrastrarlo desde el panel **Agregar campo a página** hasta la posición deseada.
- Otra forma es seleccionar el campo en el panel para mostrar la ubicación recomendada en la página. A continuación, vaya a la ubicación del campo en las páginas, seleccione la punta de flecha, luego seleccione **Agregar**. 

Una vez que se haya agregado el campo, la información sobre herramientas para el campo en el panel **Agregar campo a página** cambia a **Definido por la página**. El campo agregado está bloqueado para edición y no se puede desbloquear.

## Eliminar un campo

Si ha agregado un campo de tabla que originalmente no estaba en el objeto de la página, puede volver a eliminarlo. Eliminar un campo es diferente a ocultarlo. Cuando oculta un campo, los usuarios aún pueden mostrarlo en su espacio de trabajo mediante la personalización. Sin embargo, si elimina un campo, el campo ya no estará disponible para que los usuarios lo muestren o lo oculten. Si el campo se muestra actualmente en el espacio de trabajo de un usuario, desaparece de su espacio de trabajo cuando lo elimina. 

Para eliminar un campo, seleccione la punta de flecha en el campo de la página y luego **Eliminar**. Si no encuentra el campo, selecciónelo en el panel **Agregar campo a página** para indicar su ubicación oculta. 

> [!IMPORTANT]
> Al eliminar un campo no se eliminan los datos almacenados en el campo ni sus tablas de origen. Simplemente elimina el campo de la vista. 

## Bloquear y desbloquear la edición

La personalización le permite bloquear (permitir la edición) o desbloquear la edición (impedir la edición) de la mayoría de los campos de una página. Para bloquear o desbloquear la edición, seleccione el campo en la página, seleccione la punta de flecha y luego seleccione **Bloquear edición** o **Desbloquear edición**. Es importante tener en cuenta algunas reglas sobre cómo bloquear y desbloquear campos:

- Los campos que originalmente no estaban en el objeto de la página, pero que se agregaron a la página mediante personalización, están siempre bloqueados y no se pueden desbloquear mediante adaptación o personalización.
- El diseño del campo también puede impedir que se edite. Si el desarrollador de AL estableció la [propiedad editable](/dynamics365/business-central/dev-itpro/developer/properties/devenv-editable-property) del campo en `false`, siempre estará bloqueado y no se podrá desbloquear.
- Es importante tener en cuenta que la característica de edición de bloqueo está destinada a ayudar en la precisión, coherencia y confiabilidad de los datos. No se ha pensado para garantizar la integridad de los datos.


<!--However, whatever option you choose for a field, users can always change the setting on their own workspace using personalization. For this reason, it's important to consider locking as a deterrence measure and not a preventative measure.--> 
## Información importante y sugerencias 

- No todos los campos de la tabla pueden estar disponibles para su personalización desde el panel **Agregar campo a la página**. El desarrollador de una tabla puede optar por evitar que un campo aparezca en la personalización estableciendo la propiedad [AllowInCustomization](/dynamics365/business-central/dev-itpro/developer/properties/devenv-allowincustomizations-property) del campo en `false`.
- No puede personalizar una página que está en [modo de análisis](analysis-mode.md). El modificador **Analizar** está desactivado. Si cambia al modo de personalización mientras la página está en modo de análisis, el modo de análisis se desactiva automáticamente. 
- Algunas páginas tienen varios campos de página que se asignan a la misma tabla de origen. El panel **Agregar campo a página** muestra todos estos campos de página de manera independiente. Puede mostrar, ocultar o mover estos campos de forma independiente sin afectar a los demás.
- Si una parte o grupo está oculto, aún puede identificar campos ocultos dentro de la parte o grupo, pero no puede agregar, mover ni mostrar campos en la parte o el grupo hasta que se hagan visibles. 
## Consulte también .

[Personalizar su área de trabajo](ui-personalization-user.md)  
[Administrar perfiles](admin-users-profiles-roles.md)  
[Cambiar la configuración básica](ui-change-basic-settings.md)  
[Cambiar las funciones que se muestran](ui-experiences.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
