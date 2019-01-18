---
title: Configurar nuevas empresas | Documentos de Microsoft
description: "Puede configurar y personalizar una nueva empresa que se haya creado. Para ajustar la implementación, procederá en tres fases para completar la configuración."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: a52a95bf3fc96b89e664041e3d2b289b6042c046
ms.contentlocale: es-es
ms.lasthandoff: 11/26/2018

---
# <a name="configure-new-companies"></a>Configurar nuevas empresas
Para configurar una nueva empresa en la implementación de su solución, generalmente sigue tres fases. En la primera fase, importará el paquete de configuración, un archivo .rapidstart con la información de configuración. En la segunda fase, modificará la información de configuración y luego la aplicará a la nueva empresa. En la fase final, revisará y corregirá todos los errores.  

Para los procedimientos siguientes se supone que se ha creado y guardado un paquete de configuración. Para obtener más información sobre cómo crear un proyecto, consulte [Preparar un paquete de configuración](admin-how-to-prepare-a-configuration-package.md).  

Los siguientes procedimientos presuponen que ha inicializado y abierto su nueva empresa y que está utilizando el Área de trabajo del implementador de RapidStart Services.

## <a name="to-import-a-configuration-package"></a>Procedimiento para importar un paquete de configuración  
1. Abra la nueva empresa en la base de datos de [!INCLUDE[d365fin](includes/d365fin_md.md)].  
2. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Paquetes de configuración** y luego seleccione el enlace relacionado.  
3. Elija la acción **Importar paquete**.  
4. Vaya a la ubicación donde guardó el archivo del paquete de configuración .rapidstart y luego elija el botón **Abrir**.  
5. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Información de empresa** y luego elija el enlace relacionado. Especifique la información sobre la empresa en la ficha de información de la empresa. Incluya información como, por ejemplo, el banco. También puede proporcionar un logotipo para la empresa.  

Se importan todas las tablas diseñadas para incluirse en la nueva empresa. Llegado a este punto, puede aplicar los datos del paquete a la base de datos, o bien ajustar y modificar los datos de la tabla para satisfacer las especificaciones del cliente.  

## <a name="to-apply-package-data"></a>Procedimiento para aplicar datos de paquete  
1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Hoja de configuración** y luego seleccione el enlace relacionado.  
2. Seleccione una tabla para la que desea modificar los datos y elija la acción **Aplicar datos**. Elija el botón **Sí** para confirmar la aplicación.
3. Para confirmar que los datos ahora están en la base de datos y que la aplicación se ha realizado correctamente, vuelva a la página **Configurar hoja trabajo** y elija la acción **Datos de base de datos**.  

> [!NOTE]  
>  Después de aplicar los datos, solo se pueden ver en la base de datos. Ya no se incluyen en el paquete.  

## <a name="to-modify-and-apply-package-data"></a>Procedimiento para modificar y aplicar los datos del paquete  
1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Hoja de configuración** y luego seleccione el enlace relacionado.  
2. Seleccione una tabla para la que desea modificar los datos y elija la acción **Datos de paquete**.  
3. En la página **Configurar registros de paquete**, cree las modificaciones. Por ejemplo, puede eliminar opciones que no se aplican.  
4. Elija la acción **Aplicar datos** y, a continuación, seleccione el botón **Aceptar**.  
5. Para confirmar que los datos ahora están en la base de datos y que la aplicación se ha realizado correctamente, vuelva a la página **Configurar hoja trabajo** y elija la acción **Datos de base de datos**.  

## <a name="to-locate-and-identify-a-configuration-error"></a>Procedimiento para localizar e identificar un error de configuración  
Existen ciertos tipos de errores que pueden producirse cuando se aplican datos a una base de datos. El error más común es que no se hayan incluido las tablas relacionadas requeridas. Corrige esos errores en la hoja de trabajo de configuración.

1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Paquetes de configuración** y luego seleccione el enlace relacionado.  
2. Seleccione el paquete que desea revisar y, a continuación, seleccione la acción **Editar**.  

    Se resaltarán las tablas que contienen errores. El número de errores del paquete se muestra en el campo **Nº errores paquete**.  

3. Elija el campo **Nº errores paquete** para abrir la página **Registros paquete config.**, que enumera los registros con errores.  

### <a name="to-fix-an-error"></a>Procedimiento para corregir un error  
1. Abra la empresa en la que basó el paquete de configuración.  
2. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Hoja de configuración** y luego seleccione el enlace relacionado.  
3. Corrija los errores como agregar a la hoja de trabajo las tablas relacionadas que faltan.  
4. Agregue las tablas al paquete de configuración existente o cree un nuevo paquete que contenga solo las tablas nuevas. Para obtener más información sobre cómo crear un proyecto, consulte [Preparar un paquete de configuración](admin-how-to-prepare-a-configuration-package.md).  
5. Vuelva a abrir la nueva empresa para la que está implementando la configuración.  
6. Importe el paquete de configuración.  

    > [!NOTE]  
    >  Si vuelve a importar el mismo paquete, puede sobrescribir las modificaciones de datos que ya haya realizado. Por ese motivo, es posible que desee agregar las tablas nuevas en un paquete nuevo e importar este que en su lugar.  

7. Aplique los datos a la base de datos, como se describe en la sección "Procedimiento para modificar y aplicar los datos del paquete".

## <a name="see-also"></a>Consulte también  
[Aplicar la configuración a nuevas empresas](admin-apply-configuration-to-new-companies.md)  
[Configurar una empresa con RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Administración](admin-setup-and-administration.md)

