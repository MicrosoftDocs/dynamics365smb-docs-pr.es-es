---
title: Crear un entorno aislado
description: Crear un entorno de "prueba" de entorno aislado para explorar, aprender, demostrar, desarrollar. solucionar problemas y probar con seguridad desde Business Central.
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sandbox, demo, develop
ms.date: 06/08/2021
ms.author: solsen
ms.openlocfilehash: 2f4ca6a98aac49fa5fea7d8658ef51a9510c97d7
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 07/08/2021
ms.locfileid: "6437682"
---
# <a name="creating-a-sandbox-environment-in-prod_short"></a>Crear un entorno aislado en [!INCLUDE[prod_short](includes/prod_short.md)]

Con [!INCLUDE[prod_short](includes/prod_short.md)], puede crear fácilmente un entorno seguro donde puede probar, formar o solucionar problemas sin alterar los procesos de trabajo o los datos de negocio de su empresa. Tal entorno de no producción se llama *entorno aislado*. Aislado de la producción, un entorno aislado es el lugar para explorar, aprender, demostrar, desarrollar y probar el servicio de forma segura sin el riesgo de afectar los datos y la configuración de su entorno de producción.  

Su administrador administra entornos aislados en el [centro de administración](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments?toc=/dynamics365/business-central/toc.json), pero si desea probar algo rápidamente, puede crear un entorno aislado desde dentro de [!INCLUDE[prod_short](includes/prod_short.md)]. Una vez que haya terminado, puede eliminar el entorno aislado, utilizando el centro de administración.  

> [!NOTE]
> Técnicamente, los entornos aislados son muy diferentes de los entornos de producción, incluso si su administrador crea un entorno aislado que incluye datos de producción. No puede usar un entorno aislado para un banco de pruebas y no puede solicitar una exportación de base de datos, por ejemplo. Si desea crear un entorno aislado para banco de pruebas, su administrador puede crear un entorno dedicado en el centro de administración. Para obtener más información, consulte [Entornos de producción y aislados](/dynamics365/business-central/dev-itpro/administration/environment-types).

## <a name="to-create-a-sandbox-environment-in-your-prod_short"></a>Para crear un entorno aislado en su [!INCLUDE[prod_short](includes/prod_short.md)]

1. Inicie sesión en su instancia de producción de [!INCLUDE[prod_short](includes/prod_short.md)].

2. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Entorno aislado** y, a continuación, elija el vínculo relacionado.
    <!-- ![Sandbox Environment Setup.](./media/across-sandbox/sandbox-environment-setup.png) -->
3. Haga clic en el botón **Crear**.  

    Se abre otra pestaña con [!INCLUDE[prod_short](includes/prod_short.md)] en la que puede terminar la configuración de su entorno aislado.

    > [!NOTE]  
    >  Si tiene activado el bloqueador de ventanas emergentes en su navegador, cámbielo para permitir las direcciones URL de la dirección *.businesscentral.dynamics.com.

Cuando el entorno aislado esté listo, se le redirigirá al asistente de bienvenida del entorno aislado.
<!-- ![Sandbox Welcome Wizard.](./media/across-sandbox/sandbox-wizard.png) -->

Puede elegir el botón **Más información** para leer acerca de los escenarios de desarrollador que puede probar en un entorno aislado o seleccione el botón **Cerrar** para continuar con el área de trabajo de su instancia aislada de [!INCLUDE[prod_short](includes/prod_short.md)].

En la parte superior del Área de trabajo, aparece una notificación para informarle de que se trata de un entorno aislado. También puede ver el tipo del entorno en la barra de título del cliente.
    <!-- ![Sandbox RoleCenter Notification.](./media/across-sandbox/sandbox-rolecenter-notification.png) -->

> [!NOTE]
> Un entorno aislado creado de esta manera solo contiene los datos de demostración predeterminados para la empresa de CRONUS. No se copian ni se transfieren datos del entorno de producción.
>
> Opcionalmente, cree un entorno de espacio aislado basado en datos de producción. Debe hacerlo a través del centro de administración. Para obtener más información, consulte [Administración de entornos](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments) en el contenido para desarrolladores y administradores.  

<!--To switch between your production and sandbox environments, you can use the Business Central app launcher.
    ![Sandbox Dynamics365 Menu.](./media/across-sandbox/sandbox-dynamics365-menu.png) -->

Un administrador puede limitar o incluso bloquear el acceso de algunos usuarios al entorno aislado. Esto se puede hacer mediante las características de seguridad estándar del producto, como la tarjeta de usuario, los grupos de usuarios y los conjuntos de permisos. Para obtener más información, vea [Asignar permisos a usuarios y grupos](ui-define-granular-permissions.md).  

<!-- ![Sandbox Permission Sets.](./media/across-sandbox/sandbox-permission-sets.png) -->

## <a name="advanced-functionality-in-the-sandbox-environment"></a>Funcionalidad avanzada del entorno aislado

El entorno aislado no es menos útil porque incluye un par de características útiles:

* [Experiencia de usuario avanzada](#advanced-user-experience)  
* [Datos de muestra completos](#complete-sample-data)  
* [Diseñador](#designer)  

### <a name="advanced-user-experience"></a>Experiencia de usuario avanzada

Es posible activar y probar la función avanzada (completa) de la versión estándar de [!INCLUDE[prod_short](includes/prod_short.md)] de un suscriptor aislado configurando el campo **Experiencia** en la página **Información de la empresa** a *Premium*. Busque la página **Información de la empresa** en el menú con el :::image type="content" source="media/ui-experience/settings_icon_small.png" alt-text="icono de Configuración."::: .  

Después de habilitar la experiencia de usuario *Premium*, obtendrá acceso a todos los perfiles estándar (roles) y áreas de trabajo en la versión estándar. También puede crear una empresa de evaluación que esté completamente configurada, incluyendo datos de demostración y acceso a las áreas avanzadas del producto. Alternativamente, póngase en contacto con un distribuidor para una demostración de las capacidades. Para obtener más información, vea [¿Cómo encuentro un socio distribuidor?](across-faq.yml#how-do-i-find-a-reselling-partner).  

### <a name="complete-sample-data"></a>Datos de muestra completos

Para situaciones en las que necesite datos de muestra adicionales, póngase en contacto con su socio distribuidor.
<!-- In the sandbox environment, you can also create a new company with the **Advanced Evaluation - Complete Sample Data** option so that you can take training or step through walkthroughs that require additional sample data, such as [Walkthrough: Receiving and Putting Away in Basic Warehouse Configurations](walkthrough-receiving-and-putting-away-in-basic-warehousing.md).   -->

#### <a name="to-create-a-company-with-complete-sample-data-in-a-sandbox"></a>Para crear una empresa con datos de muestra completos en un entorno aislado

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Empresas** y luego elija el enlace relacionado.  
2. Elija la acción **Nuevo** y, a continuación, elija **Crear nueva empresa**.  
3. En la página **Configuración asistida para crear una empresa**, elija **Siguiente**.  
4. Especifique un nombre para la nueva compañía y luego, en **Seleccionar los datos y la configuración para comenzar**, elija **Evaluación avanzada: completar datos de muestra**.  
5. Complete el resto de los pasos de la guía de configuración asistida.  

Cuando se completa la guía de configuración asistida, puede comenzar a explorar la nueva empresa con los datos de muestra completos. Para obtener más información, consulte [Crear nuevas empresas en [!INCLUDE[prod_short](includes/prod_short.md)]](about-new-company.md).  

### <a name="designer"></a>Diseñadora

En un entorno aislado, encontrará el **Diseñador** habilitado Puede activar Diseñador seleccionando el icono de diseño ![Diseñador.](./media/across-sandbox/sandbox-inclient-design-icon.png) en una página, o eligiendo el elemento de menú **Diseño** en el menú Configuración ![Configuración](media/ui-experience/settings_icon_small.png).  

Para más información, vea [Uso de diseñador](/dynamics365/business-central/dev-itpro/developer/devenv-inclient-designer) en el contenido para desarrolladores y administradores (solo en inglés).  

<!-- ![In-client Designer.](./media/across-sandbox/sandbox-inclient-designer.png) -->

## <a name="see-also"></a>Consulte también

[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Versiones de prueba y suscripciones de [!INCLUDE[prod_long](includes/prod_long.md)]](across-preview.md)  
[Administración de entornos en el centro de administración de Business Central](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
