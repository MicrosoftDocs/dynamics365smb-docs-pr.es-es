---
title: Crear un entorno aislado | Documentos de Microsoft
description: Crear un entorno para explorar, aprender, demostrar, desarrollar y probar.
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sandbox, demo, develop
ms.date: 08/18/2017
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: d7bcb866d5f69e77e5a175d0b73e8ac03cf09d98
ms.contentlocale: es-es
ms.lasthandoff: 09/22/2017

---
[!INCLUDE[d365fin_early_release](includes/d365fin_early_release.md.md)]

# <a name="how-to-create-a-sandbox-environment"></a>Crear un entorno aislado
Un entorno aislado (vista preliminar) es una instancia de no producción de [!INCLUDE[d365fin](includes/d365fin_md.md)]. Aislado de la producción, un entorno aislado es el lugar para explorar, aprender, demostrar, desarrollar y probar el servicio de forma segura sin el riesgo de afectar los datos y la configuración de su entorno de producción.

## <a name="to-create-a-sandbox-environment"></a>Para crear un entorno aislado
Debe tener una suscripción a [!INCLUDE[d365fin](includes/d365fin_md.md)] para poder crear un entorno aislado. Puede haber solo un entorno aislado por suscripción.

1. Inicie sesión en su instancia de producción del servicio [!INCLUDE[d365fin](includes/d365fin_md.md)].
2. Elija el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), introduzca **Entorno aislado** y elija el vínculo relacionado.
![Configuración de un entorno aislado](./media/across-sandbox/sandbox-environment-setup.png)
3. Seleccione **Crear**.  
  Se abrirá otra pestaña en el navegador para finalizar la configuración del entorno aislado.
> [!NOTE]  
>  Si tiene activado el bloqueador de ventanas emergentes en su navegador, cámbielo para permitir las direcciones URL de la dirección *.financials.dynamics.com.   

4. Cuando el entorno aislado esté listo, se le redirigirá al asistente de bienvenida del entorno aislado.
![Asistente de bienvenida del entorno aislado](./media/across-sandbox/sandbox-wizard.png)

5. Seleccione **Más información** para consultar información sobre los escenarios que puede probar en un entorno aislado. O bien, elija **Cerrar** para continuar con el Área de trabajo de la instancia aislada de [!INCLUDE[d365fin](includes/d365fin_md.md)].
6. En la parte superior del Área de trabajo, aparece una notificación para informarle de que se trata de un entorno aislado. También puede ver el tipo del entorno en la barra de título del cliente.
![Notificaciones del Área de trabajo del entorno aislado](./media/across-sandbox/sandbox-rolecenter-notification.png)  
En el entorno aislado, se ha creado un nuevo suscriptor. Este suscriptor se carga con datos de demostración predeterminados para la empresa CRONUS. No se copian ni se transfieren datos del entorno de producción durante la creación del entorno aislado.
7.  Cuando lo desee puede volver a la página **Entorno aislado** y restablecerlo.
> [!NOTE]  
>  Al restablecer el entorno aislado se eliminará completamente y, a continuación, se creará de nuevo con los datos de demostración predeterminados.  

8.  Para cambiar entre los entornos de producción y aislado, puede utilizar el lanzador de aplicaciones de Dynamics 365.
![Menú del espacio aislado de Dynamics365](./media/across-sandbox/sandbox-dynamics365-menu.png)

9.  Es posible que un administrador u otro usuario limite o incluso bloquee el acceso de algunos usuarios al entorno aislado. Esto se puede hacer mediante las características de seguridad estándar del producto, como la tarjeta de usuario, los grupos de usuarios y los conjuntos de permisos.

![Conjuntos de permisos del entorno aislado](./media/across-sandbox/sandbox-permission-sets.png)

## <a name="advanced-functionality-in-the-sandbox-environment"></a>Funcionalidad avanzada del entorno aislado
### <a name="the-in-client-designer"></a>El diseñador del cliente
En un entorno aislado, se encuentra habilitada la función de diseñador en el cliente, que puede activar seleccionando el icono de diseño ![Diseñadora](./media/across-sandbox/sandbox-inclient-design-icon.png) en una página.

![Diseñador del cliente](./media/across-sandbox/sandbox-inclient-designer.png)

### <a name="enable-the-advanced-user-experience"></a>Activar la experiencia del usuario avanzado
Es posible activar y probar la funcionalidad avanzada (completa) de [!INCLUDE[d365fin](includes/d365fin_md.md)] en un suscriptor aislado configurando el campo **Experiencia** en la página **Información de la empresa**.

![Entorno aislado avanzado](./media/across-sandbox/sandbox-advanced.png)

![Producción de entorno aislado](./media/across-sandbox/sandbox-production.png)

Después de habilitar la funcionalidad avanzada en un inquilino aislado, obtiene acceso a todos los perfiles y áreas de trabajo estándar. También puede crear una empresa de evaluación que esté completamente configurada, incluyendo datos de demostración y acceso a las áreas avanzadas del producto.

![Nueva empresa aislada](./media/across-sandbox/sandbox-newcompany.png)


## <a name="see-also"></a>Consulte también
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

