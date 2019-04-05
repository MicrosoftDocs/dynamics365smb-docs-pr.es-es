---
title: Configurar los orígenes web para empresas de contacto | Documentos de Microsoft
description: Puede definir sus orígenes web o de Internet y asignarlos a una empresa de contacto para identificar cómo desea buscar la información de sus contactos.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: internet
ms.date: 10/01/2018
ms.author: jswymer
redirect_url: marketing-setup-contacts
ms.openlocfilehash: 22b9f0be189fa24f366c1ffa20934d2d8e7e8fc5
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/08/2019
ms.locfileid: "806174"
---
# <a name="set-up-web-sources-for-contact-companies"></a>Configurar enlaces web para empresas de contacto
Puede usar enlaces web con sus empresas de contacto para identificar, por ejemplo, los motores de búsqueda y los sitios web de Internet que quiere usar para buscar información sobre los contactos. Al asignar enlaces web, especifica el motor de búsqueda y la palabra clave que la aplicación usará para buscar la información solicitada.

El uso de enlaces web en contactos es un proceso que consta de dos pasos. Primero, debe definir el código del enlace web. Solo debe realizar este paso una vez para cada enlace web. Una vez tenga código de enlace web, puede comenzar a asignar el código a personas de contacto.

## <a name="to-define-a-web-source-code"></a>Para definir un código de enlace Web
1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Enlaces web** y luego elija el enlace relacionado.
2. Elija la acción **Nuevo**.
3. Rellene los campos **Código**, **Descripción** y **URL**.

    Escriba %1 en el campo **Dirección URL** para insertar un marcador de posición para una palabra de búsqueda en la URL. Al ejecutar al enlace web desde una ficha de contacto, %1 se reemplaza con la palabra de búsqueda, por ejemplo, el nombre de la empresa, especificada en la página **Enlaces web de contactos**.

Repita estos pasos para configurar todos los orígenes web que desee.

## <a name="to-assign-web-sources-to-a-contact-company"></a>Para asignar enlaces Web a una empresa de contacto
Al asignar enlaces web, especifica el motor de búsqueda y la palabra clave que la aplicación usará para buscar la información solicitada.

1. Abra el contacto.
2. Elija la acción **Empresa** y, a continuación, elija la acción **Enlaces web**. Se abre la página **Enlaces web contacto**.
3. En el campo **Código de enlace web**, elija el enlace web que desea asignar.
4. Escriba en el campo **Busca palabra**, escriba la palabra de búsqueda que desea que use el sistema para buscar la información.

Repita estos pasos para asignar todos los orígenes web que desee.

También puede asignar orígenes web, con el mismo procedimiento, en la página **Lista contactos**.

## <a name="see-also"></a>Consulte también
[Crear contactos](marketing-create-contact-companies.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
