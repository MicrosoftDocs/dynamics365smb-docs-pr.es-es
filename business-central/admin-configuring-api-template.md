---
title: Configurar plantillas de API | Documentos de Microsoft
description: Describa los pasos que debe seguir para configurar las plantillas API para Dynamics 365 Business Central.
services: project-madeira
documentationcenter: ''
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: API templates, configuring templates
ms.date: 04/01/2021
ms.author: solsen
ms.openlocfilehash: 7d39262993a173fec1eae68bcb44a85332a9866a
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2021
ms.locfileid: "5773109"
---
# <a name="configuring-api-templates"></a>Configuración de plantillas API
La biblioteca API para [!INCLUDE[prod_short_md](includes/prod_short.md)] proporciona una representación simplificada de las entidades subyacentes. Todas las propiedades de la aplicación no están expuestas a través de la API asociada. La página **Configuración de API** le permite definir plantillas que se utilizan para llenar propiedades vacías en una entidad cuando crea una acción POST a través de la API. 

Por ejemplo, si se define una plantilla de configuración para la entidad del elemento, cuando se crea un nuevo registro del elemento a través de la API de elementos, las propiedades del nuevo elemento que no están definidas en la API se rellenarán a partir de la plantilla seleccionada. Si, por ejemplo, no se define ningún valor para el campo **Grupo contable producto** a través de la API, pero se define un valor en la plantilla seleccionada, el valor del grupo definido en la plantilla se aplicará al nuevo elemento. 

## <a name="setting-up-the-entity-template"></a>Configuración de la plantilla de entidad
Para usar plantillas con la biblioteca API, primero debe configurar y definir propiedades para las plantillas. Puede configurar estas plantillas en la página **Plantillas de configuración**. Para obtener más información, consulte [Prepararse para migrar datos del cliente](admin-use-templates-to-prepare-customer-data-for-migration.md). 

## <a name="assign-the-template-to-an-api"></a>Asigne la plantilla a una API

Para asignar una plantilla a una API, debe seguir los siguientes pasos.

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Configuración de API** y luego elija el enlace relacionado.
2. Seleccione **Nuevo** y el valor **Orden** para el registro.  
Si hay más de una plantilla seleccionada para una API (ID de página), las plantillas se aplican en el orden definido en la columna **Pedido**.   
Cuando se aplican las plantillas, los valores de campo definidos en la plantilla solo se aplican a los campos que aún no tienen un valor definido, ya sea explícitamente en la API o en una plantilla previamente aplicada en el pedido. 
3. Seleccionar un valor de **ID de página**.  
Esta es la página de la API a la que se aplicará la plantilla. La búsqueda de **ID de página** proporciona una lista de todas las API disponibles en la biblioteca.
4. Seleccione un valor en el campo **Código de plantilla**.  
El código de plantilla es el código para la plantilla que se definió en la página **Plantillas de configuración**. Los valores de plantilla definidos se aplican a la API. 
5. En el campo **Condiciones**, especifique qué plantilla se debe aplicar.  
La plantilla definida se aplica a un nuevo registro creado a través de la API si, y únicamente en el caso de que, las condiciones definidas en el campo **Condiciones** se cumplan con los valores ya definidos para la nueva instancia de la entidad.

## <a name="see-also"></a>Consulte también
[Documentación de la API](/dynamics-nav/fin-graph)  
[Desarrollo de aplicaciones de conexión para [!INCLUDE[prod_short_md](includes/prod_short.md)]](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  
[Activar las API](/dynamics-nav/enabling-apis-for-dynamics-nav)  
[Extremos para las API](/dynamics-nav/endpoints-apis-for-dynamics)  
[Configurar una empresa con RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Administración](admin-setup-and-administration.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]