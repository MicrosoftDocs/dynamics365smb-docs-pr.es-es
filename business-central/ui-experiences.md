---
title: Cambiar las funciones que se muestran
description: 'Obtenga información sobre lo que significan las capas de experiencia de usuario Esencial y Premium para la interfaz de usuario, las áreas de aplicación y su empresa.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'essential, basic, user interface, application area, experience'
ms.search.form: 1
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="change-which-features-are-displayed" />Cambiar las funciones que se muestran
[!INCLUDE[prod_short](includes/prod_short.md)] está diseñado para ayudarlo a administrar su empresa, independientemente del tamaño y la complejidad. En el núcleo del producto, encontrará características esenciales, como informes financieros, ventas, compras y administración de inventario. A medida que aumenta la complejidad empresarial, puede activar la funcionalidad para la fabricación y la administración de servicios, por ejemplo.

Puede definir el nivel de complejidad del producto y, por lo tanto, a qué características tienen acceso los usuarios de la empresa, cambiando la configuración **Experiencia** en la página **Información de empresa**. Tenga en cuenta que la configuración de experiencia también se puede cambiar agregando ciertas extensiones desde AppSource. Para obtener más información, consulte [Personalizar [!INCLUDE[prod_short](includes/prod_short.md)] mediante extensiones](ui-extensions.md).

La siguiente tabla enumera la experiencias que están disponibles actualmente.

| Experiencia | Impacto en la interfaz de usuario |
| --- | --- |
| **Essential** |Muestra todas las acciones y campos para todas las funcionalidades de negocio comunes.|
| **Prima de emisión** |Muestra todas las acciones y campos para todas las funcionalidades empresariales, incluidas las de Fabricación y Gestión de servicios.|

Las experiencias que se pueden seleccionar en [!INCLUDE[prod_short](includes/prod_short.md)] reflejan las licencias de solución, llamadas planes, que se definen para el producto. Para obtener información acerca de los planes de Esencial y Premium, consulte [Business Central](https://go.microsoft.com/fwlink/?linkid=870242) en el sitio de marketing de Microsoft Dynamics 365. Consulte también [[!INCLUDE[prod_short](includes/prod_short.md)], guía de licencia](https://go.microsoft.com/fwlink/?linkid=2068931).

> [!IMPORTANT]  
> Todos los usuarios habituales de una solución deben tener asignado el mismo plan, Essential o Premium, antes de poder seleccionar esa experiencia para la empresa. En consecuencia, un usuario no puede acceder a las funciones Premium si uno o más usuarios solo pueden acceder a las funciones Essential. Este no es el caso para los usuarios no regulares del tipo Miembro del equipo, Administrador interno, Contable externo y Administrador delegado, a quienes se les puede asignar un plan diferente al de otros usuarios en la solución.<br /><br /> Solo los usuarios de tipo Evaluación o Premium pueden cambiar el valor del campo **Experiencia** de Essential a Premium.

Antes de definir la configuración de experiencia de una empresa, defina el acceso de los usuarios a funciones y páginas específicas mediante la asignación de conjuntos de permisos. Para obtener más información, vea [Asignar permisos a usuarios y grupos](ui-define-granular-permissions.md).

La configuración **Experiencia** se aplica a todos los usuarios de una empresa, pero cada usuario puede personalizar aún más su propia experiencia cambiando el diseño y el contenido de la página. Para obtener más información, consulte [Personalizar el área de trabajo](ui-personalization-user.md).

## <a name="enabling-premium-features-after-upgrading-a-plan" />Habilitar características premium después de actualizar un plan
Los usuarios se asignan a planes en el Centro de administración de Microsoft 365 en relación con el trabajo general para crear los usuarios de Business Central. Para más información, vea [Agregue usuarios y asigne licencias al mismo tiempo](/microsoft-365/admin/add-users/add-users?view=o365-worldwide&preserve-view=true).

### <a name="to-update-plan-changes-in-users-groups" />Para actualizar los cambios del plan en grupos de usuarios

[!INCLUDE [2023rw1-sec-group-short](includes/2023rw1-sec-group-short.md)]

Cuando haya realizado un cambio en los planes de los usuarios en el Centro de administración de Microsoft 365, como asignar más usuarios al plan Premium, debe actualizar [!INCLUDE[prod_short](includes/prod_short.md)] para reflejar el cambio.

1. Inicie sesión como administrador.
2. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Usuarios** y luego elija el enlace relacionado.
3. En la página **Usuarios**, elija la acción **Actualizar usuarios desde Microsoft 365**.

### <a name="to-select-the-premium-experience" />Para seleccionar la experiencia Premium
Ahora puede proceder a seleccionar la nueva experiencia.
1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Información empresa** y luego elija el enlace relacionado.
2. En la página **Información empresa**, en la ficha desplegable **Experiencia del usuario**, seleccione Premium en el campo **Experiencia**.

## <a name="help-assumes-premium-experience" />En la ayuda se asume la experiencia premium
Todas las descripciones de funciones que aparecen en la documentación de [!INCLUDE[prod_short](includes/prod_short.md)] asumen la experiencia **Premium**, lo que significa que las descripciones cubren todo el alcance de los elementos de la interfaz de usuario.

## <a name="see-also" />Consulte también .
[Personalizar el área de trabajo](ui-personalization-user.md)  
[Personalizar Business Central](ui-customizing-overview.md)  
[Asignar permisos a usuarios y grupos](ui-define-granular-permissions.md)  
[Crear nuevas en empresas](about-new-company.md)  
[Cambiar la configuración básica](ui-change-basic-settings.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)], guía de licencia](https://go.microsoft.com/fwlink/?LinkId=871590&clcid=0x409)

## <a name="includeprodshortincludesfreetrialmdmd" />[!INCLUDE[prod_short](includes/free_trial_md.md)]


[!INCLUDE[footer-include](includes/footer-banner.md)]
