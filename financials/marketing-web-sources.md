---
title: "Configurar los orígenes web para empresas de contacto | Documentos de Microsoft"
description: "Puede definir sus orígenes web o de Internet y asignarlos a una empresa de contacto para identificar cómo desea buscar la información de sus contactos."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: internet
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: b81deefcdf79a93cc988d216f80b08794efb8ab6
ms.contentlocale: es-es
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-web-sources-for-contact-companies"></a>Configurar enlaces web para empresas de contacto
Puede usar enlaces web con sus empresas de contacto para identificar, por ejemplo, los motores de búsqueda y los sitios web de Internet que quiere usar para buscar información sobre los contactos. Al asignar enlaces web, especifica el motor de búsqueda y la palabra clave que la aplicación usará para buscar la información solicitada.

El uso de enlaces web en contactos es un proceso que consta de dos pasos. Primero, debe definir el código del enlace web. Solo debe realizar este paso una vez para cada enlace web. Una vez tenga código de enlace web, puede comenzar a asignar el código a personas de contacto.

## <a name="to-define-a-web-source-code"></a>Para definir un código de enlace Web
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Enlaces web** y, a continuación, seleccione el vínculo relacionado.
2. Elija la acción **Nuevo**.
3. Rellene los campos **Código**, **Descripción** y **URL**.

    Escriba %1 en el campo **Dirección URL** para insertar un marcador de posición para una palabra de búsqueda en la URL. Al ejecutar al enlace web desde una ficha de contacto, %1 se reemplaza con la palabra de búsqueda, por ejemplo, el nombre de la empresa, especificada en la ventana **Enlaces web de contactos**.

Repita estos pasos para configurar todos los orígenes web que desee.

## <a name="to-assign-web-sources-to-a-contact-company"></a>Para asignar enlaces Web a una empresa de contacto
Al asignar enlaces web, especifica el motor de búsqueda y la palabra clave que la aplicación usará para buscar la información solicitada.

1. Abra el contacto.
2. Elija la acción **Empresa** y, a continuación, elija la acción **Enlaces web**. Se abre la ventana **Enlaces web contacto**.
3. En el campo **Código de enlace web**, elija el enlace web que desea asignar.
4. Escriba en el campo **Busca palabra**, escriba la palabra de búsqueda que desea que use el sistema para buscar la información.

Repita estos pasos para asignar todos los orígenes web que desee.

También puede asignar enlaces web, con el mismo procedimiento, en la ventana **Lista contactos**.

## <a name="see-also"></a>Consulte también
[Crear empresas de contacto](marketing-create-contact-companies.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

