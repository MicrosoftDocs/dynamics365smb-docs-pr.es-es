---
title: Crear un entorno aislado | Documentos de Microsoft
description: Crear un entorno para explorar, aprender, demostrar, desarrollar y probar.
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sandbox, demo, develop
ms.date: 10/01/2020
ms.author: solsen
ms.openlocfilehash: 43442680578eca60fabdc620e1f8bd04036d214c
ms.sourcegitcommit: 32bfc2acaaf3693afc9aeb86feea505fd328caa1
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/19/2021
ms.locfileid: "5024442"
---
# <a name="creating-a-sandbox-environment-in-prod_short"></a>Crear un entorno aislado en [!INCLUDE[prod_short](includes/prod_short.md)]

Con [!INCLUDE[prod_short](includes/prod_short.md)], puede crear fácilmente un entorno seguro donde puede probar, formar o solucionar problemas sin alterar los procesos de trabajo o los datos de negocio de su empresa. Tal entorno de no producción se llama *entorno aislado*. Aislado de la producción, un entorno aislado es el lugar para explorar, aprender, demostrar, desarrollar y probar el servicio de forma segura sin el riesgo de afectar los datos y la configuración de su entorno de producción.  

Su administrador puede crear entornos aislados en el [centro de administración](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments?toc=/dynamics365/business-central/toc.json), pero si desea probar algo rápidamente, puede crear un entorno aislado desde dentro de [!INCLUDE[prod_short](includes/prod_short.md)].  

> [!NOTE]
> Técnicamente, los entornos aislados son muy diferentes de los entornos de producción, incluso si su administrador crea un entorno aislado que incluye datos de producción. No puede usar un entorno aislado para un banco de pruebas y no puede solicitar una exportación de base de datos, por ejemplo. Si desea crear un entorno aislado para banco de pruebas, su administrador puede crear un entorno de producción dedicado en el centro de administración. Para obtener más información, consulte [Tipos de entornos](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#types-of-environments).

## <a name="to-create-a-sandbox-environment-in-your-prod_short"></a>Para crear un entorno aislado en su [!INCLUDE[prod_short](includes/prod_short.md)]

1. Inicie sesión en su instancia de producción de [!INCLUDE[prod_short](includes/prod_short.md)].

2. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Entorno aislado** y luego elija el enlace relacionado.
    <!-- ![Sandbox Environment Setup](./media/across-sandbox/sandbox-environment-setup.png) -->
3. Haga clic en el botón **Crear**.  

    Se abre otra pestaña con [!INCLUDE[prod_short](includes/prod_short.md)] en la que puede terminar la configuración de su entorno aislado.

    > [!NOTE]  
    >  Si tiene activado el bloqueador de ventanas emergentes en su navegador, cámbielo para permitir las direcciones URL de la dirección *.businesscentral.dynamics.com.

Cuando el entorno aislado esté listo, se le redirigirá al asistente de bienvenida del entorno aislado.
<!-- ![Sandbox Welcome Wizard](./media/across-sandbox/sandbox-wizard.png) -->

Puede elegir el botón **Más información** para leer acerca de los escenarios de desarrollador que puede probar en un entorno aislado o seleccione el botón **Cerrar** para continuar con el área de trabajo de su instancia aislada de [!INCLUDE[prod_short](includes/prod_short.md)].

En la parte superior del Área de trabajo, aparece una notificación para informarle de que se trata de un entorno aislado. También puede ver el tipo del entorno en la barra de título del cliente.
    <!-- ![Sandbox RoleCenter Notification](./media/across-sandbox/sandbox-rolecenter-notification.png) -->

> [!NOTE]
> Un entorno aislado creado de esta manera solo contiene los datos de demostración predeterminados para la empresa de CRONUS. No se copian ni se transfieren datos del entorno de producción.<br /><br />
> También puede crear un entorno aislado que contenga los datos de producción. Debe hacerlo a través del centro de administración. Para obtener más información, consulte [Administración de entornos](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments) en la Ayuda para desarrolladores y profesionales de TI.  

<!--To switch between your production and sandbox environments, you can use the Business Central app launcher.
    ![Sandbox Dynamics365 Menu](./media/across-sandbox/sandbox-dynamics365-menu.png) -->

Un administrador puede limitar o incluso bloquear el acceso de algunos usuarios al entorno aislado. Esto se puede hacer mediante las características de seguridad estándar del producto, como la tarjeta de usuario, los grupos de usuarios y los conjuntos de permisos. Para obtener más información, vea [Asignar permisos a usuarios y grupos](ui-define-granular-permissions.md).  

<!-- ![Sandbox Permission Sets](./media/across-sandbox/sandbox-permission-sets.png) -->

## <a name="advanced-functionality-in-the-sandbox-environment"></a>Funcionalidad avanzada del entorno aislado

El entorno aislado no es menos útil porque incluye un par de características útiles.

### <a name="to-enable-the-advanced-user-experience"></a>Para activar la experiencia del usuario avanzado

Es posible activar y probar la función avanzada (completa) de la versión estándar de [!INCLUDE[prod_short](includes/prod_short.md)] de un suscriptor aislado configurando el campo **Experiencia** en la página **Información de la empresa** a *Premium*. Busque la página **Información de la empresa** en el menú con el :::image type="content" source="media/ui-experience/settings_icon_small.png" alt-text="icono de Configuración":::.  

Después de habilitar la experiencia de usuario *Premium*, obtendrá acceso a todos los perfiles estándar (roles) y áreas de trabajo en la versión estándar. También puede crear una empresa de evaluación que esté completamente configurada, incluyendo datos de demostración y acceso a las áreas avanzadas del producto. Alternativamente, póngase en contacto con un distribuidor para una demostración de las capacidades. Para obtener más información, vea [¿Cómo encuentro un socio distribuidor?](across-faq.md#findpartner)  

### <a name="to-enable-complete-sample-data"></a>Para habilitar datos de muestra completos

En el entorno de espacio aislado, también puede crear una nueva empresa con la opción **Evaluación avanzada: completar datos de muestra** para que pueda seguir la formación o realizar tutoriales que requieren datos de muestra adicionales, como [Tutorial: Recepción y ubicación en configuraciones básicas de almacén](walkthrough-receiving-and-putting-away-in-basic-warehousing.md).  

#### <a name="to-create-a-company-with-complete-sample-data-in-a-sandbox"></a>Para crear una empresa con datos de muestra completos en un entorno aislado

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Empresas** y luego elija el enlace relacionado.  
2. Elija la acción **Nuevo** y, a continuación, elija **Crear nueva empresa**.  
3. En la página **Configuración asistida para crear una empresa**, elija **Siguiente**.  
4. Especifique un nombre para la nueva compañía y luego, en **Seleccionar los datos y la configuración para comenzar**, elija **Evaluación avanzada: completar datos de muestra**.  
5. Complete el resto de los pasos de la guía de configuración asistida.  

Cuando se completa la guía de configuración asistida, puede comenzar a explorar la nueva empresa con los datos de muestra completos. Para obtener más información, consulte [Crear nuevas empresas en [!INCLUDE[prod_short](includes/prod_short.md)]](about-new-company.md).  

### <a name="designer"></a>Diseñadora

En un entorno aislado, encontrará el **Diseñador** habilitado Puede activar el Diseñador seleccionando el icono de diseño ![Diseñador](./media/across-sandbox/sandbox-inclient-design-icon.png) en una página o eligiendo el elemento de menú **Diseño** en el menú ![Configuración](media/ui-experience/settings_icon_small.png) Configuración.

<!-- ![In-client Designer](./media/across-sandbox/sandbox-inclient-designer.png) -->

## <a name="see-also"></a>Consulte también

[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Versiones de prueba y suscripciones de [!INCLUDE[prod_long](includes/prod_long.md)]](across-preview.md)  
[Administración de entornos en el centro de administración de Business Central](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments)  
