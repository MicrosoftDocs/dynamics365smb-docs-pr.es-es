---
title: 'Procedimiento: Configurar un servicio de intercambio de documentos | Documentos de Microsoft'
description: Para intercambiar documentos electrónicos con socios comerciales se usa un proveedor de servicios externo.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: a89cf3988e7576070a58a798e0f88693e598ef92
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2021
ms.locfileid: "5787287"
---
# <a name="set-up-a-document-exchange-service"></a>Configurar un servicio de intercambio de documentos
Para intercambiar documentos electrónicos con socios comerciales se usa un proveedor de servicios externo. Para obtener más información, vea [Intercambio de datos electrónicamente](across-data-exchange.md).  

## <a name="to-set-up-a-document-exchange-service"></a>Para configurar un servicio de intercambio de documentos  
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Configuración servicio intercambio documentos** y luego elija el enlace relacionado.  
2. Rellene los campos tal como se describe en la tabla siguiente.  

    |Campo|Descripción|  
    |---------------------------------|---------------------------------------|  
    |**Agente de usuario**|Escriba cualquier texto que pueda usarse para identificar a la empresa en los procesos de intercambio de documentos.|  
    |**Id. suscriptor intercambio documentos**|Introduzca el inquilino en el servicio de intercambio de documentos que representa a la empresa. Esto lo proporciona el proveedor de servicios de intercambio de documentos.|  
    |**Habilitado**|Especifique si el servicio está habilitado. **Nota**: En cuanto se active el servicio, se crean al menos dos movimientos de cola de proyectos para procesar el tráfico de los documentos electrónicos dentro y fuera de [!INCLUDE[prod_short](includes/prod_short.md)]. Cuando se deshabilita el servicio, se eliminan los movimientos de la cola de proyectos.|  
    |**URL de registro**|Especifique la página web donde se inscribe para el servicio de intercambio de documentos.|  
    |**URL de servicio**|Especifique la dirección del servicio de intercambio de documentos, al que se llamará cuando se envíen y se reciban documentos electrónicos.|  
    |**Conexión URL**|Especifique la página de inicio de sesión del servicio de intercambio de documentos, que es donde se introduce el nombre de usuario de su empresa y la contraseña para iniciar sesión en el servicio.|  
    |**Clave de consumidor**|Introduzca la clave OAuth de tres segmentos para la clave de consumidor. Esto lo proporciona el proveedor de servicios de intercambio de documentos.|  
    |**Secreto de consumidor**|Introduzca el secreto que protege la clave de consumidor. Esto lo proporciona el proveedor de servicios de intercambio de documentos.|  
    |**Token**|Introduzca la clave OAuth de tres segmentos para el token. Esto lo proporciona el proveedor de servicios de intercambio de documentos.|  
    |**Secreto de token**|Introduzca el secreto que protege el token. Esto lo proporciona el proveedor de servicios de intercambio de documentos.|  

    > [!NOTE]  
    > Los datos de inicio de sesión se cifran automáticamente.

## <a name="see-also"></a>Consulte también  
[Configuración del intercambio de datos](across-set-up-data-exchange.md)  
[Intercambio de datos electrónicamente](across-data-exchange.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]