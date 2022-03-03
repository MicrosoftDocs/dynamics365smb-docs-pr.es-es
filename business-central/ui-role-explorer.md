---
title: Exploración y navegación de páginas por rol
description: Puede obtener una descripción general de todas las funciones empresariales que están disponibles para su rol y para otros roles con Explorador de roles.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: role explorer, find features, navigate
ms.search.form: 9020, 9022, 9027, 9018
ms.date: 08/01/2021
ms.author: jswymer
ms.openlocfilehash: 485018e4a15f3e8ecb7c19f365d6dd6d06650cdb
ms.sourcegitcommit: 75a388b1d8917e2bbd49398ef76cf86cf37e6767
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/17/2022
ms.locfileid: "8322908"
---
# <a name="finding-pages-with-the-role-explorer"></a>Búsqueda de páginas con el explorador de roles

Puede obtener una descripción general de todas las funciones empresariales que están disponibles para su rol y para otros roles si va un paso más allá. En la siguiente documentación, esta descripción general de funciones se denomina *explorador de roles*.

Cada elemento del explorador de roles es una acción que abre una página. En consecuencia, también puede usar el explorador de roles como un medio para navegar en [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="open-the-role-explorer"></a>Abrir el explorador de roles

Puede abrir el explorador de roles desde el área de trabajo y todas las páginas de la lista y desde la ventana **Dígame**.

- En su Área de trabajo o en cualquier página de lista, elija el ![botón Menú.](media/ui_menu_button.png "Botón Menú") a la derecha de la barra de navegación, o presione Mayús+F12.
- En la ventana **Dígame**, elija la acción **explorando** en la parte inferior.

Cuando abre por primera vez el área de trabajo, muestra enlaces a la mayoría de las funciones disponibles para su rol.

## <a name="navigate-features"></a>Navegar por las funciones

Las acciones que abren las páginas están organizadas en nodos con el nombre de las características o áreas de aplicación. Cada nodo se puede contraer o expandir individualmente y puede contraer/expandir todos los nodos a la vez.

- Para expandir/contraer un solo nodo, elija el nodo. Esto se aplica a los nodos de nivel superior y los subnodos.
- Para expandir/contraer todos los nodos de nivel superior en la página, pero dejar los nodos secundarios como están, elija **...** en la parte superior, luego elija **Expandir** o **Contraer**.
- Para expandir/contraer todos los nodos de nivel superior y todos los secundarios, elija **...** en la parte superior, luego elija la acción **Expandir todos** o **Contraer todos**.

## <a name="search-for-features"></a>Buscar características

Para ubicar funciones rápidamente, seleccione **Encontrar**, luego introduzca una palabra o frase para la función que está tratando de encontrar. El área de trabajo resaltará cualquier texto correspondiente. Si una función está oculta a la vista en un nodo contraído, el nodo contraído se marca con un punto. 

## <a name="explore-other-roles"></a>Explorar otros roles

Para explorar roles distintos al suyo, seleccione **Explorar más roles**. El área de trabajo muestra cada función bajo su propia cabecera, con vínculos a sus funciones. A continuación, puede navegar y buscar funciones tal como lo hace cuando explora su rol.

> [!NOTE]
> Solo verá los roles que están configurados para mostrarse en el explorador de roles. Si no ve un rol que esperaba ver, probablemente no esté configurado para él. Para obtener más información, consulte [Administrar perfiles](admin-users-profiles-roles.md). 

Al explorar otros roles, también puede reducir la exploración utilizando las acciones **Informes y análisis** y **Administración** en la parte superior del área de trabajo.

- **Informes y análisis** muestra solo las funciones que están categorizadas como funciones de informes y de análisis.
- **Administración** muestra solo aquellas funciones que están categorizadas como funciones de administración.

> [!TIP]
> Para los desarrolladores, puede categorizar las páginas y los informes estableciendo la [Propiedad UsageCategory](/dynamics365/business-central/dev-itpro/developer/properties/devenv-usagecategory-property) en el código AL del objeto.
<!--
 
## Role explorer actions

There a several actions along the top of the role explorer to help you locate features of your role and other roles.

|Action|Description|
|------|------|
|**All**|Shows all features that are related to the role.|
|**Find**|Lets you enter a word or phrase to quickly locate feature names that match.|
|**Explore more roles**|All business features that are available for all roles including your own. When exploring all roles, the other actions work the same way, except for all roles shown. **NOTE:** You will only see roles that are set up to show in role explorer. For more information, see [Manage Profiles](admin-users-profiles-roles.md).  |
|**Report & Analysis**|This action Shows only those features that are categorized as reports and analysis features.|
|**Administration**|Shows only those features that are categorized as administration features.|



<!--
Choose the **Find** action at the top of the role explorer to quickly locate feature names that contain a certain term.

Choose the **Explore more roles** action at the top of the role explorer to get an overview of all business features that are available for all roles including your own.

> [!NOTE]
> Only Role Center actions for profiles where the **Show in Role Explorer** check box is selected will appear on the extended version of the role explorer (shown with the **Explore more roles** action). For more information, see [Manage Profiles](admin-users-profiles-roles.md).
-->

## <a name="expand-and-collapse-nodes-on-the-role-explorer"></a>Expandir y contraer nodos en el explorador de roles

Las acciones que abren las páginas están organizadas en nodos con el nombre de las características o áreas de aplicación. Cada nodo se puede contraer o expandir individualmente y puede contraer/expandir todos los nodos a la vez.

- Para expandir/contraer un nodo, elija el nodo. Esto se aplica a los nodos de nivel superior y los subnodos.
- Para expandir/contraer todos los nodos de nivel superior de la página, elija la acción **Expandir** o **Contraer** en la esquina superior derecha.
- Para expandir o contraer todos los nodos de nivel superior y todos los subnodos dependientes, realice uno de los siguientes pasos:
  - Presione las teclas Ctrl+Mayús mientras elige la acción **Expandir** o **Contraer** en la esquina superior derecha.
  - Elija **...** en la esquina superior derecha y luego elija la acción **Expandir todo** o **Contraer todo**.

## <a name="see-also"></a>Consulte también
[Búsqueda de páginas e información con Dígame](ui-search.md)  
[Administración de perfiles](admin-users-profiles-roles.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]