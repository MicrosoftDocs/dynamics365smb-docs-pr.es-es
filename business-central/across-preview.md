---
title: Obtener la vista previa en nuevos mercados
description: "Obtenga información sobre cómo acceder a las vistas previas de Business Central."
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: preview, trial, sandbox
ms.date: 06/28/2018
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: 2286b728a464943841b192031cfea13644441013
ms.openlocfilehash: 0829c825ec0635a20c040fe17cd3e7cfc667ffd7
ms.contentlocale: es-es
ms.lasthandoff: 06/28/2018

---
# <a name="access-to-the-included365finlongincludesd365finlongmdmd-preview"></a>Acceder a la vista preliminar de [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]
[!INCLUDE[d365fin](includes/d365fin_md.md)] estará disponible en nuevos países a partir de la primavera de 2018. Para garantizar que [!INCLUDE[d365fin](includes/d365fin_md.md)] es la solución adecuada para esos clientes, ofrecemos una versión de vista previa del servicio antes del lanzamiento de primavera. La vista previa de Dinamarca estaba disponible en enero de 2018 y próximamente vendrán mercados adicionales.  

## <a name="getting-started-with-previews-and-sandboxes"></a>Introducción a vistas previas y entornos aislados
Las vistas preliminares y los entornos aislados son importantes formas de obtener ayuda con [!INCLUDE[d365fin](includes/d365fin_md.md)]. Una instancia de vista previa contiene funcionalidad que se suma a lo que está disponible en la versión actual. Las vistas previas ofrecen a los socios y clientes la oportunidad de probar y proporcionar comentarios sobre la funcionalidad que estamos pensando en lanzar. Aunque las vistas previas están pensadas principalmente para socios, los clientes también pueden usarlas durante un tiempo limitado. La vista previa actual de [!INCLUDE[d365fin](includes/d365fin_md.md)] contiene la mayoría de las capacidades disponibles en Dynamics NAV 2018, que normalmente requieren la ayuda de un socio para su configuración.

Para comenzar con una vista previa, vaya a [esta página](https://go.microsoft.com/fwlink/?linkid=866045) y proporcione la dirección de correo electrónico de su trabajo. Para obtener más información sobre [!INCLUDE[d365fin](includes/d365fin_md.md)] y las capacidades que ofrece, consulte la documentación en este sitio.

Puede pensar en un entorno aislado como un entorno que no es de producción y que puede usar en su instancia de producción o vista previa de [!INCLUDE[d365fin](includes/d365fin_md.md)]. Un entorno aislado le permite crear y probar extensiones de forma segura y desarrollar nuevas funcionalidades para personalizar el servicio sin afectar los datos y la configuración de su producción o las instancias de vista previa. En este momento, todos los clientes que tienen una versión de producción o vista previa pueden usar un entorno aislado.

Para aprender cómo comenzar con un entorno aislado, consulte las instrucciones siguientes.

## <a name="creating-a-sandbox-environment"></a>Crear un entorno aislado
Para trabajar en un entorno aislado, debe tener una suscripción a [!INCLUDE[d365fin](includes/d365fin_md.md)]. Puede haber solo un entorno aislado por suscripción.

### <a name="advanced-functionality-available-in-a-sandbox-environment"></a>Funcionalidad avanzada disponible en un entorno aislado
Los entornos aislados contienen una función de diseñador en el cliente que le permite diseñar páginas mediante una interfaz de arrastrar y soltar y crear extensiones en el cliente mediante la adición y reorganización de campos.

Para obtener más información, consulte [Uso de diseñador](https://docs.microsoft.com/en-us/dynamics-nav/developer/devenv-inclient-designer).

### <a name="to-create-a-sandbox-environment"></a>Para crear un entorno aislado
1.  Inicie sesión en su instancia de producción o vista previa del servicio [!INCLUDE[d365fin](includes/d365fin_md.md)].  
2.  Elija el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), introduzca **Entorno aislado** y elija el vínculo relacionado.
3.  Elija **Crear**. Se abrirá una pestaña en la que puede terminar de configurar su entorno aislado.

    > [!Note]
    > Si el bloqueador de ventanas emergentes está activado en su navegador, cámbielo para permitir las direcciones URL de la dirección *.businesscentral.dynamics.com*.  

4.  Cuando esté listo el entorno aislado, se mostrará una página de bienvenida.  
5.  Si desea leer sobre escenarios que puede probar en un entorno aislad, como por ejemplo cómo desarrollar extensiones, elija el enlace **Más información**. En caso contrario, elija **Cerrar** para continuar con el Área de trabajo de la instancia aislada de [!INCLUDE[d365fin](includes/d365fin_md.md)].  
6.  En la parte superior del Área de trabajo, aparece una notificación para informarle de que se trata de un entorno aislado. También puede ver el tipo del entorno en la barra de título del cliente.

    > [!Note]
    > El entorno aislado contiene datos de demostración de la empresa ficticia comprendida de CRONUS. No se copian ni se transfieren datos del entorno de producción.  

7.  Puede volver a la página Entorno aislado en cualquier momento para restablecerlo.

    > [!Note]
    > Restablecer un entorno aislado lo elimina por completo y luego lo recrea con los datos de demostración predeterminados.  

8.  Para cambiar entre el entorno de fabricación y el entorno aislado, utilice el menú de Dynamics 365 o la página web de Dynamics.

    > [!Note]
    > Un administrador u otro usuario puede limitar o incluso bloquear el acceso del usuario al entorno aislado utilizando las funciones de seguridad estándar en [!INCLUDE[d365fin](includes/d365fin_md.md)], como la tarjeta de usuario, los grupos de usuarios y los conjuntos de permisos.  

### <a name="building-new-solutions-and-intellectual-property"></a>Construir nuevas soluciones y propiedad intelectual
[!INCLUDE[d365fin](includes/d365fin_md.md)] ofrece un conjunto de herramientas de desarrollo y una plataforma moderna sobre la que construir para que pueda crear sus propias aplicaciones complementarias e integrar soluciones para conectar o ampliar [!INCLUDE[d365fin](includes/d365fin_md.md)].

[!INCLUDE[d365fin](includes/d365fin_md.md)] proporciona herramientas que puede usar para implementar su propia funcionalidad de inserción para agregar nuevas experiencias de extremo a extremo específicas de la industria o integrar soluciones de terceros. Por ejemplo, puede usar una API para construir una aplicación conectada para intercambiar datos entre [!INCLUDE[d365fin](includes/d365fin_md.md)] y su aplicación de nómina. Las liquidaciones de conexión también pueden hacer uso de extensiones para crear páginas que se utilizarán para la configuración, configuración o para admitir funciones específicas de la aplicación. Para obtener más información, vea [Desarrollo de aplicaciones para [!INCLUDE[d365fin](includes/d365fin_md.md)]](https://aka.ms/getstartedwithapps).

## <a name="see-also"></a>Consulte también
[Introducción](product-get-started.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

