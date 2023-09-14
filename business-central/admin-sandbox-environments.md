---
title: Ambientes de espacio aislado
description: 'Obtenga información sobre cómo un ambiente dedicado puede ayudarle a explorar, aprender, hacer demostraciones, desarrollar, solucionar problemas y probar Business Central de forma segura.'
author: brentholtorf
ms.topic: conceptual
ms.reviewer: edupont
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'sandbox, demo, develop'
ms.date: 12/20/2021
ms.author: bholtorf
---
# Ambientes de espacio aislado en [!INCLUDE[prod_short](includes/prod_short.md)]

Con [!INCLUDE[prod_short](includes/prod_short.md)] en línea, puede obtener fácilmente un entorno seguro donde puede probar, formar o solucionar problemas sin alterar los procesos de trabajo o los datos de negocio de su empresa. Tal entorno de no producción se llama *entorno aislado*. Aislado de la producción, un entorno aislado es el lugar para explorar, aprender, demostrar, desarrollar y probar el servicio de forma segura sin el riesgo de afectar los datos y la configuración de su entorno de producción.  

> [!TIP]
> ¿Llegó a este artículo después de elegir el nombre de su entorno de [!INCLUDE [prod_short](includes/prod_short.md)] en la barra superior? Actualmente, no puede cambiar el nombre o el entorno de esa manera. En su lugar, debe pedirle a su administrador que cambie el nombre o pedirle que comparta el vínculo a otro entorno.

Su administrador gestiona los ambientes de espacio aislado en el [centro de administracion](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments?toc=/dynamics365/business-central/toc.json).  

Por ejemplo, si desea crear un ambiente aislado para banco de pruebas, su administrador puede crear un ambiente dedicado en el centro de administración. Para obtener más información, consulte [Ambientes de producción y espacios aislados](/dynamics365/business-central/dev-itpro/administration/environment-types) en el contenido para desarrolladores y administradores.  

También puede usar espacios aislados de forma segura para la formación, como por ejemplo, para seguir una ruta de aprendizaje de la [formación de Microsoft](/training/dynamics365/business-central?WT.mc_id=dyn365bc_landingpage-docs) porque es un ambiente seguro para experimentar. Si algo sale mal, simplemente elimine el espacio aislado y comience de nuevo.  

Una vez que haya terminado, puede eliminar el entorno aislado, utilizando el centro de administración.  

> [!NOTE]
> Técnicamente, los ambientes de espacios aislados son muy diferentes a los ambientes de producción. Su administrador puede crear una espacio aislado que incluya datos de producción, pero que siga siendo un espacio aislado, y no usted no podrá solicitar una exportación de base de datos, por ejemplo. Para obtener más información, consulte [Ambientes de espacios aislados](/dynamics365/business-central/dev-itpro/administration/environment-types#sandbox-environments) en el contenido para desarrolladores y administradores.

El entorno aislado no es menos útil porque incluye un par de características útiles:

* [Experiencia de usuario avanzada](#advanced-user-experience)  
<!--* [Complete sample data](#complete-sample-data)  -->
* [Diseñador](#designer)  

## Experiencia de usuario avanzada

Es posible activar y probar la función avanzada (completa) de la versión estándar de [!INCLUDE[prod_short](includes/prod_short.md)] de un suscriptor aislado configurando el campo **Experiencia** en la página **Información de la empresa** a *Premium*. Busque la página **Información de la empresa** en el menú con el :::image type="content" source="media/ui-experience/settings_icon_small.png" alt-text="icono de Configuración."::: .  

Después de habilitar la experiencia de usuario *Premium*, obtendrá acceso a todos los perfiles estándar (roles) y áreas de trabajo en la versión estándar. Alternativamente, póngase en contacto con un distribuidor para una demostración de las capacidades. Para obtener más información, vea [¿Cómo encuentro un socio distribuidor?](across-faq.yml#how-do-i-find-a-reselling-partner).  

### Datos de muestra completos

Para situaciones en las que necesite datos de muestra adicionales, póngase en contacto con su socio distribuidor.
<!-- In the sandbox environment, you can also create a new company with the **Advanced Evaluation - Complete Sample Data** option so that you can take training or step through walkthroughs that require additional sample data, such as [Walkthrough: Receiving and Putting Away in Basic Warehouse Configurations](walkthrough-receiving-and-putting-away-in-basic-warehousing.md).   -->

<!--#### To create a company with complete sample data in a sandbox

1. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Companies**, and then choose the related link.  
2. Choose the **New** action, and then choose **Create New Company**.  
3. In the **Assisted Setup for Creating a Company** page, choose **Next**.  
4. Specify a name for the new company, and then, in the **Select the data and setup to get started** field, choose **Advanced Evaluation - Complete Sample Data**.  
5. Complete the rest of the assisted setup guide.  

When the assisted setup guide completes, you can start exploring the new company with the complete sample data. For more information, see [Creating New Companies in [!INCLUDE[prod_short](includes/prod_short.md)]](about-new-company.md).  -->

## Diseñadora

En un entorno aislado, encontrará el **Diseñador** habilitado Puede activar Diseñador seleccionando el icono de diseño ![Diseñador.](./media/across-sandbox/sandbox-inclient-design-icon.png) en una página, o eligiendo el elemento de menú **Diseño** en el menú Configuración ![Configuración](media/ui-experience/settings_icon_small.png).  

Para obtener más información, consulte [Usar el diseñador](/dynamics365/business-central/dev-itpro/developer/devenv-inclient-designer) en el contenido para desarrolladores y administradores (solo en inglés).  

<!-- ![In-client Designer.](./media/across-sandbox/sandbox-inclient-designer.png) -->

## Consultar la [formación de Microsoft](/training/modules/admin-online-dynamics-365-business-central/) relacionada

## Consulte también .

[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Versiones de prueba y suscripciones de [!INCLUDE[prod_long](includes/prod_long.md)]](/dynamics365/business-central/dev-itpro/administration/trials-subscriptions)  
[Administración de entornos en el centro de administración de Business Central](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments)  
[Ambientes de producción y de espacios aislados](/dynamics365/business-central/dev-itpro/administration/environment-types)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
