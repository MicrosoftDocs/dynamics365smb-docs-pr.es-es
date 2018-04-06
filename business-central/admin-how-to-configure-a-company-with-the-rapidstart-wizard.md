---
title: Configurar una empresa con el asistente de RapidStart | Documentos de Microsoft
description: "Puede configurar rápidamente una nueva empresa que se haya creado mediante el asistente para la configuración de RapidStart Services."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/06/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 264788142ab4f2a84df3e1c9da6e39503a7e820f
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="configure-a-company-with-the-rapidstart-wizard"></a>Configurar una empresa con el asistente de RapidStart
Puede configurar rápidamente una nueva empresa que se haya creado mediante el asistente para la configuración de RapidStart Services.

En el procedimiento siguiente, proporcionó al cliente el paquete de configuración, que luego se instala en un equipo. El cliente abre la nueva empresa, que no contiene ningún elemento de datos de cliente. Usted o el cliente sigue los pasos del asistente de RapidStart Services y que se describen en este procedimiento, con el fin de proporcionar información básica sobre la empresa. El asistente importa el paquete de configuración y luego aplica este a la empresa.  

## <a name="to-configure-a-new-company"></a>Procedimiento para configurar una nueva empresa  
1. En el Área de trabajo del implementador de RapidStart Services, elija la acción **Asistente de RapidStart**.  
2. Expanda la ficha desplegable **Paso 1** que contiene información general sobre la nueva empresa. Especifique la información adecuada acerca de la nueva empresa en los campos correspondientes. Hay un campo que es obligatorio, **Nombre**. Los demás campos son opcionales.  
3. Expanda la ficha desplegable **Paso 2** que contiene información de comunicación y contacto para la nueva empresa. Especifique la información adecuada acerca de la nueva empresa en los campos correspondientes.
4. Expanda la ficha desplegable **Paso 3** que contiene la información del banco y de pagos para la nueva empresa. Especifique la información adecuada acerca de la nueva empresa en los campos correspondientes.  
5. Amplíe la ficha desplegable **Paso 4**. Seleccione el botón **AssistEdit** para seleccionar el paquete de configuración que desee aplicar. Se muestra el nombre del paquete de configuración. A continuación podrá realizar las acciones siguientes, en el orden indicado:  

    1. Aplique la configuración eligiendo la acción **Aplicar paquete**. Esto importa el paquete de configuración y al mismo tiempo aplica sus datos de base de datos.  

    2. Revisar la configuración después de su aplicación. Esta opción permite revisar los detalles y cuestionarios de la configuración que proporcione el socio, así como importar algunos datos maestros necesarios para la empresa. Elija la acción **Hoja de configuración**. Para obtener más información, consulte la sección "Completar el cuestionario de configuración" en [Recopilación de valores de configuración de cliente](admin-gather-customer-setup-values.md).  

6. Amplíe la ficha desplegable **Paso 5**. Especifique el Área de trabajo que desee establecer como valor predeterminado para la nueva empresa.  

    > [!IMPORTANT]  
    >  Solo cambie el Área de trabajo después de haber completado la configuración de la empresa. Si hay detalles de configuración adicionales que deben tenerse en cuenta o modificar, el primero use la hoja de trabajo de configuración para continuar con el trabajo. A continuación, vuelva al asistente para actualizar el perfil de Área de trabajo o elija la acción **Completar configuración**.

7. Elija el botón **Aceptar**.  
8. Para comprobar que la información de configuración se ha aplicado a la nueva empresa, elija el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Información empresa** y seleccione el vínculo relacionado.

La ventana **Información empresa** contiene la información especificada.   

Ya ha configurado la empresa y aplicado datos a ella.  

## <a name="see-also"></a>Consulte también  
[Aplicar la configuración a nuevas empresas](admin-apply-configuration-to-new-companies.md)  
[Configurar una empresa con RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Administración](admin-setup-and-administration.md)

