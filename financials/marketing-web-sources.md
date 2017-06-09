---
title: "Configurar los orígenes web para empresas de contacto | Documentos de Microsoft"
description: "Describe cómo usar enlaces web para contactos en Financials"
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: internet
ms.date: 03/28/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 8a452619aeeee907cf61fd5d1a8fce409ad2e42d
ms.contentlocale: es-es
ms.lasthandoff: 05/04/2017


---
# <a name="setting-up-web-sources-for-contact-companies"></a>Configurar enlaces web para empresas de contacto
Puede usar enlaces web con sus empresas de contacto para identificar, por ejemplo, los motores de búsqueda y los sitios web de Internet que quiere usar para buscar información sobre los contactos. Al asignar enlaces web, especifica el motor de búsqueda y la palabra clave que la aplicación usará para buscar la información solicitada.

El uso de enlaces web en contactos es un proceso que consta de dos pasos. Primero, debe definir el código del enlace web. Solo debe realizar este paso una vez para cada enlace web. Una vez tenga código de enlace web, puede comenzar a asignar el código a personas de contacto.

## <a name="to-define-a-web-source-code"></a>para definir un código de origen web
1. En la esquina superior derecha, seleccione el icono **Buscar página o informe** ![Buscar página o informe](media/ui-search/search_small.png "Icono Buscar página o informe"), especifique **Orígenes web** y elija el vínculo relacionado.
2. Elija la acción **Nuevo**.
3. Rellene los campos **Código**, **Descripción** y **URL**.

    Escriba %1 en el campo **Dirección URL** para insertar un marcador de posición para una palabra de búsqueda en la URL. Al ejecutar al enlace web desde una ficha de contacto, %1 se reemplaza con la palabra de búsqueda, por ejemplo, el nombre de la empresa, especificada en la ventana **Enlaces web de contactos**.

Repita estos pasos para configurar todos los orígenes web que desee.

## <a name="to-assign-web-sources-to-a-contact-company"></a>para asignar orígenes web a una empresa de contacto
Al asignar enlaces web, especifica el motor de búsqueda y la palabra clave que la aplicación usará para buscar la información solicitada.

1. Abra el contacto.
2. Elija la acción **Empresa** y, a continuación, elija la acción **Enlaces web**. Se abre la ventana **Enlaces web contacto**.
3. En el campo **Código de enlace web**, elija el enlace web que desea asignar.
4. Escriba en el campo **Busca palabra**, escriba la palabra de búsqueda que desea que use el sistema para buscar la información.

Repita estos pasos para asignar todos los orígenes web que desee.

También puede asignar enlaces web, con el mismo procedimiento, en la ventana **Lista contactos**.

## <a name="see-also"></a>Consulte también
[Crear empresas de contacto](marketing-create-contact-companies.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)](ui-work-product.md)

