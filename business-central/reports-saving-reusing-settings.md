---
title: Administrar configuraciones guardadas para informes y trabajos por lotes
description: Describe cómo el administrador puede configurar opciones y filtros predefinidos para un informe y compartir esa configuración con uno o todos los usuarios.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'customization, personalization'
ms.date: 12/21/2021
ms.author: edupont
---
# Administrar configuraciones guardadas para informes y trabajos por lotes

Cuando se ejecutan informes, a los usuarios normalmente se les presenta una página que les permite seleccionar opciones y establecer filtros para cambiar los datos que se incluyen en el informe generado. Esta página se llama *página de solicitud*. Un informe puede incluir una o varias *opciones de configuración guardadas* que los usuarios pueden aplicar al informe de la página de solicitud. La *configuración guardada* son básicamente opciones y filtros predeterminados. El uso de la configuración guardada es una forma rápida y confiable de generar de forma coherente informes que contienen los datos correctos. Para obtener más información, consulte [Uso de la configuración guardada](ui-work-report.md#SavedSettings).

> [!NOTE]
> Este tema hace referencia principalmente a los *informes*, pero se aplica información similar a los *trabajos por lotes*.

Si tiene los permisos adecuados, puede ver, crear y modificar la configuración guardada de todos los informes para todos los usuarios de una empresa. Puede asignar la configuración guardada de un informe a usuarios individuales o a todos los usuarios de la empresa.

## Administrar la configuración guardada

La configuración guardada se administra en la página **Configuración de informes**. Hay dos maneras de abrir esta página:

- Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración del informe** y luego elija el enlace relacionado.
- En la página de solicitud de un informe, seleccione la búsqueda en el campo **Utilizar valores predeterminado desde** y, a continuación, elija la acción **Seleccionar de la lista completa**.

    Este campo solo es visible si ha ejecutado el informe al menos una vez antes. La lista solo mostrará la configuración que está disponible para usted, ya sea porque es su propia configuración o porque la configuración se comparte con usted.

La página **Configuración del informe** muestra todas las entradas de configuración guardada de almacenamiento existentes para todos los usuarios. Si hay un nombre de usuario en el campo **Asignado a**, solo ese usuario puede utilizar los parámetros guardados para el informe asociado. Si hay una marca de verificación en el campo **Compartir con todos los usuarios**, todos los usuarios pueden utilizar las opciones guardadas para el informe.  

> [!TIP]
> Cuando un usuario ha ejecutado un informe que admite configuraciones compartidas, sus configuraciones se guardan y se agregan a esta lista. En la mayoría de los casos, el administrador puede editar esa configuración y elegir compartirla con todos los usuarios.
>
> Sin embargo, en algunos casos, la configuración no se puede compartir y el administrador tampoco puede cambiarla. La mayoría de los trabajos por lotes no admiten la configuración compartida.  

## Crear o modificar la configuración guardada para todos los usuarios

Desde la página **Configuración del informe**, puede:

- Seleccione la acción **Nuevo** para crear una nueva entrada de configuración guardada desde cero.
- Seleccione una entrada de configuración guardada de la lista y seleccione la acción **Copiar** para crear una copia.
- Seleccione una entrada de configuración guardada de la lista y elija la acción **Editar** para modificar una entrada de configuración guardada.

> [!Important]
> Considere el nombre que le asigna a una entrada de configuración guardada. Si crea una entrada de configuración guardada para todos los usuarios y le asigna el mismo nombre que la entrada de configuración guardada existente que está asignada a un usuario determinado únicamente, ese usuario no podrá utilizar la entrada de configuración guardada que se asigne a todos.  En la sección **Configuración guardada** de la página de solicitud, el usuario verá dos entradas de configuración guardada con el mismo nombre. Sin embargo, independientemente de la opción que elija, se usará la entrada de configuración guardada específica del usuario.

> [!NOTE]
> La posibilidad de guardar la configuración solo está disponible en los informes en los que la [propiedad SaveValues](/dynamics365/business-central/dev-itpro/developer/properties/devenv-savevalues-property) de la página de solicitud del informe está establecida en **Sí**. El desarrollador define la propiedad **SaveValues**.  

## Consulte también

[Trabajar con informes, trabajos por lotes y XMLports](ui-work-report.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]