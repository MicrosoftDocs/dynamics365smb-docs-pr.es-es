---
title: Elegir la experiencia de usuario para mostrar u ocultar características avanzadas | Documentos de Microsoft
description: Obtenga información sobre lo que significan las capas de experiencia de usuario Esencial y Premium para la interfaz de usuario, las áreas de aplicación y su empresa.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: essential, basic, user interface, application area, experience
ms.date: 11/13/2019
ms.author: sgroespe
ms.openlocfilehash: 32de53150f90f2400962f33601a0fa45c059bd4c
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/03/2019
ms.locfileid: "2882163"
---
# <a name="change-which-features-are-displayed"></a>Cambiar las funciones que se muestran
[!INCLUDE[d365fin](includes/d365fin_md.md)] está diseñado para ayudarlo a administrar su empresa, independientemente del tamaño y la complejidad. En el núcleo del producto, encontrará características esenciales, como informes financieros, ventas, compras y administración de inventario. A medida que aumenta la complejidad empresarial, puede activar la funcionalidad para la fabricación y la administración de servicios, por ejemplo.

Puede definir el nivel de complejidad del producto y, por lo tanto, a qué características tienen acceso los usuarios de la empresa, cambiando la configuración **Experiencia** en la página **Información de empresa**. Tenga en cuenta que la configuración de experiencia también se puede cambiar agregando ciertas extensiones desde AppSource. Para obtener más información, consulte [Personalizar [!INCLUDE[d365fin](includes/d365fin_md.md)] mediante extensiones](ui-extensions.md).

La siguiente tabla enumera la experiencias que están disponibles actualmente.

| Experiencia | Impacto en la interfaz de usuario |
| --- | --- |
| **Essential** |Muestra todas las acciones y campos para todas las funcionalidades de negocio comunes.|
| **Prima de emisión** |Muestra todas las acciones y campos para todas las funcionalidades empresariales, incluidas las de Fabricación y Gestión de servicios.|

Las experiencias que se pueden seleccionar en [!INCLUDE[d365fin](includes/d365fin_md.md)] reflejan las licencias de solución, llamadas planes, que se definen para el producto. Para obtener información acerca de los planes de Esencial y Premium, consulte [Business Central](https://go.microsoft.com/fwlink/?linkid=870242) en el sitio de marketing de Microsoft Dynamics 365. Consulte también [Guía de licencia de [!INCLUDE[d365fin](includes/d365fin_md.md)]](https://go.microsoft.com/fwlink/?linkid=2068931) (se necesita acceso a CustomerSource o PartnerSource).

> [!IMPORTANT]  
> Todos los usuarios habituales de una solución deben tener asignado el mismo plan, Essential o Premium, antes de poder seleccionar esa experiencia para la empresa. En consecuencia, un usuario no puede acceder a las funciones Premium si uno o más usuarios solo pueden acceder a las funciones Essential. Este no es el caso para los usuarios no regulares del tipo Miembro del equipo, Administrador interno, Contable externo y Administrador delegado, a quienes se les puede asignar un plan diferente al de otros usuarios en la solución.<br /><br /> Solo los usuarios de tipo Evaluación o Premium pueden cambiar el valor del campo **Experiencia** de Essential a Premium.

Antes de definir la configuración de experiencia de una empresa, defina el acceso de los usuarios a funciones y páginas específicas mediante la asignación de conjuntos de permisos. Para obtener más información, vea [Asignar permisos a usuarios y grupos](ui-define-granular-permissions.md).

La configuración **Experiencia** se aplica a todos los usuarios de una empresa, pero cada usuario puede personalizar aún más su propia experiencia cambiando el diseño y el contenido de la página. Para obtener más información, consulte [Personalizar el área de trabajo](ui-personalization-user.md).

## <a name="enabling-premium-features-after-upgrading-a-plan"></a>Habilitar características premium después de actualizar un plan
Los usuarios se asignan a planes en el Centro de administración de Microsoft 365 en relación con el trabajo general para crear los usuarios de Business Central. Para obtener más información, vea [Agregar usuarios individualmente o en masa a Office 365](https://support.office.com/article/Add-users-to-Office-365-for-business-435ccec3-09dd-4587-9ebd-2f3cad6bc2bc).

### <a name="to-update-plan-changes-in-users-groups"></a>Para actualizar los cambios del plan en grupos de usuarios
Cuando haya realizado un cambio en los planes de los usuarios en el Centro de administración de Microsoft 365, como asignar más usuarios al plan Premium, debe reflejar el cambio en [!INCLUDE[d365fin](includes/d365fin_md.md)].

1. Inicie sesión como administrador.
2. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Usuarios** y luego elija el enlace relacionado.
3. En la página **Usuarios**, seleccione la acción **Actualizar todos los grupos de usuarios**.

Toda la información nueva sobre los planes de los usuarios y sus grupos de usuarios asignados ahora se actualizan de acuerdo con los cambios del plan.

### <a name="to-select-the-premium-experience"></a>Para seleccionar la experiencia Premium
Ahora puede proceder a seleccionar la nueva experiencia.
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Información de empresa** y luego elija el enlace relacionado.
2. En la página **Información empresa**, en la ficha desplegable **Experiencia del usuario**, seleccione Premium en el campo **Experiencia**.

## <a name="help-assumes-premium-experience"></a>En la ayuda se asume la experiencia premium
Todas las descripciones de funciones que aparecen en la documentación de [!INCLUDE[d365fin](includes/d365fin_md.md)] asumen la experiencia **Premium**, lo que significa que las descripciones cubren todo el alcance de los elementos de la interfaz de usuario.

## <a name="see-also"></a>Consulte también .
[Personalizar el área de trabajo](ui-personalization-user.md)  
[Personalizar Business Central](ui-customizing-overview.md)  
[Asignar permisos a usuarios y grupos](ui-define-granular-permissions.md)  
[Crear nuevas en empresas](about-new-company.md)  
[Cambiar la configuración básica](ui-change-basic-settings.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)], guía de licencia](https://go.microsoft.com/fwlink/?LinkId=871590&clcid=0x409)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
