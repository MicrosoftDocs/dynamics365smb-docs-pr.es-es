---
title: 'Procedimiento: Configurar un servicio de intercambio de documentos | Documentos de Microsoft'
description: "Para intercambiar documentos electrónicos con socios comerciales se usa un proveedor de servicios externo."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/18/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 1191313565e813a92c13fa07b6278e7263eeaf19
ms.contentlocale: es-es
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-a-document-exchange-service"></a>Procedimiento: Configurar un servicio de intercambio de documentos
Para intercambiar documentos electrónicos con socios comerciales se usa un proveedor de servicios externo. Para obtener más información, vea [Intercambio de datos como documentos electrónicos](across-data-exchange.md).  

## <a name="to-set-up-a-document-exchange-service"></a>Para configurar un servicio de intercambio de documentos  
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Configuración servicio intercambio documentos** y, a continuación, seleccione el vínculo relacionado.  
2. Rellene los campos tal como se describe en la tabla siguiente.  

    |Campo|Description|  
    |---------------------------------|---------------------------------------|  
    |**Agente de usuario**|Escriba cualquier texto que pueda usarse para identificar a la empresa en los procesos de intercambio de documentos.|  
    |**Id. suscriptor intercambio documentos**|Introduzca el inquilino en el servicio de intercambio de documentos que representa a la empresa. Esto lo proporciona el proveedor de servicios de intercambio de documentos.|  
    |**Habilitado**|Especifique si el servicio está habilitado. **Nota**: En cuanto se active el servicio, se crean al menos dos movimientos de cola de proyectos para procesar el tráfico de los documentos electrónicos dentro y fuera de [!INCLUDE[d365fin](includes/d365fin_md.md)]. Cuando se deshabilita el servicio, se eliminan los movimientos de la cola de proyectos.|  
    |**URL de registro**|Especifique la página web donde se inscribe para el servicio de intercambio de documentos.|  
    |**URL de servicio**|Especifique la dirección del servicio de intercambio de documentos, al que se llamará cuando se envíen y se reciban documentos electrónicos.|  
    |**Conexión URL**|Especifique la página de inicio de sesión del servicio de intercambio de documentos, que es donde se introduce el nombre de usuario de su empresa y la contraseña para iniciar sesión en el servicio.|  
    |**Clave de consumidor**|Introduzca la clave OAuth de tres segmentos para la clave de consumidor. Esto lo proporciona el proveedor de servicios de intercambio de documentos.|  
    |**Secreto de consumidor**|Introduzca el secreto que protege la clave de consumidor. Esto lo proporciona el proveedor de servicios de intercambio de documentos.|  
    |**Token**|Introduzca la clave OAuth de tres segmentos para el token. Esto lo proporciona el proveedor de servicios de intercambio de documentos.|  
    |**Secreto de token**|Introduzca el secreto que protege el token. Esto lo proporciona el proveedor de servicios de intercambio de documentos.|  

> [!NOTE]  
>  Se recomienda usar esta función para proteger la información de inicio de sesión que se introduce en la ventana **Configuración del servicio VAN**. Puede cifrar datos en el servidor generando claves de cifrado nuevas o importando claves existentes que se activarán en la instancia del servidor que conecta con la base de datos. Esto se describe en el procedimiento siguiente:  

## <a name="to-encrypt-your-logon-information"></a>Para cifrar la información de inicio de sesión  
1. En la ventana **Configuración del servicio VAN**, seleccione la acción **Administración del cifrado**.  
2. En la ventana **Administración del cifrado de datos**, habilite el cifrado de los datos. <!--For more information, see [Manage Data Encryption](../manage-data-encryption.md).-->  

## <a name="see-also"></a>Consulte también  
[Configuración del intercambio de datos](across-set-up-data-exchange.md)  
[Intercambio de datos como documentos electrónicos ](across-data-exchange.md)

