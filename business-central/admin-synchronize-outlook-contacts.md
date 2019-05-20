---
title: Compartir contactos entre Business Central y Outlook | Microsoft Docs
description: Este servicio tiene una integración profunda con Office 365 para que pueda compartir contactos entre Outlook y Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: contacts, Office 365
ms.date: 04/01/2019
ms.author: edupont
ms.openlocfilehash: 93acc30c501b099b829a304650b09b356d2243e7
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/29/2019
ms.locfileid: "1244198"
---
# <a name="synchronize-contacts-in-business-central-with-contacts-in-microsoft-outlook"></a>Sincronizar los contactos de Business Central con los de Microsoft Outlook
Puede ver los mismos contactos en [!INCLUDE[d365fin](includes/d365fin_md.md)] que en Outlook si configura la sincronización de contactos. Por ejemplo, si es un vendedor, puede hacer parte de su trabajo en Outlook y parte de su trabajo en [!INCLUDE[d365fin](includes/d365fin_md.md)]. Si los contactos son los mismos en ambos lugares, su trabajo es más sencillo.  

Una carpeta dedicada en Outlook hace que los contactos sean fáciles de encontrar, y puede establecer un filtro para sincronizar solo los contactos de [!INCLUDE[d365fin](includes/d365fin_md.md)] que desea ver en Outlook. Una vez que se establece la sincronización de contactos, puede iniciarla manualmente o configurarla para que sea automática y mantenga los contactos sincronizados de forma programada.  

## <a name="set-up-synchronization"></a>Configurar sincronización
Configure cómo quiere sincronizar los contactos con Outlook en la página **Configuración de la sincronización de Exchange** en [!INCLUDE[d365fin](includes/d365fin_md.md)]. Como requisito previo, su perfil de usuario en [!INCLUDE[d365fin](includes/d365fin_md.md)] debe especificar su cuenta de correo electrónico de Office 365. Puede verificarlo en la sección **Autenticación de Office 365** de su perfil de usuario en la lista **Usuarios**.  

Luego, en la página **Configuración de la sincronización de Exchange**, puede validar que la conexión a Exchange está funcionando y luego configurar la sincronización de contactos. Abra la página **Configuración de sincronización de contactos** e inicie la sincronización. Opcionalmente, establezca un filtro para los contactos que desea sincronizar entre [!INCLUDE[d365fin](includes/d365fin_md.md)] y Outlook. Por ejemplo, puede establecer un filtro en nombre, tipo, compañía o similar. También puede cambiar el nombre predeterminado de la carpeta en la que se sincronizarán los contactos en Outlook. El nombre predeterminado es *Business Central*.  

Una vez configurada esta sincronización, cualquier cambio que realice en el contacto en Outlook o en [!INCLUDE[d365fin](includes/d365fin_md.md)] se sincronizará con el otro.  

Cada uno de sus compañeros de trabajo también puede configurar su propia sincronización de Exchange y establecer su propio filtro sobre qué contactos sincronizar.  

## <a name="synchronize-contacts"></a>Sincronizar contactos
Si está acostumbrado a trabajar con contactos en [!INCLUDE[d365fin](includes/d365fin_md.md)], le resultará fácil iniciar la sincronización manualmente siempre que le convenga desde la lista **Contactos**. Simplemente elija la acción **Sincronizar con Office 365** y luego decida si desea cambiar el filtro que ha configurado. Cuando elige el botón Aceptar, la sincronización se inicia de inmediato y los últimos cambios se aplican a sus contactos en Outlook.  

En la lista **Contactos**, puede sincronizar contactos de dos maneras:

* **Sincronizar con Office 365**

  Esta acción sincronizará todos los cambios de [!INCLUDE[d365fin](includes/d365fin_md.md)] a Office 365 desde la sincronización anterior, en función de la última fecha de modificación. Todos los contactos nuevos de Office 365 se sincronizarán nuevamente a [!INCLUDE[d365fin](includes/d365fin_md.md)]. Esto típicamente es más rápido que hacer una sincronización completa.  

* **Sincronización completa con Office 365**

  Esta acción sincroniza todos los contactos en ambas direcciones, independientemente de la fecha de la última sincronización y la fecha de última modificación.  

En ambos casos, los contactos solo se sincronizan desde Outlook si tienen rellenos los campos obligatorios. Los campos obligatorios para sincronizar a Office 365 son **Nombre**, **Dirección de correo electrónico** y deben ser de tipo Persona. [!INCLUDE[d365fin](includes/d365fin_md.md)] es el maestro de la información de contacto, por lo que la información de contacto de [!INCLUDE[d365fin](includes/d365fin_md.md)] se guardará en caso de duplicados.  

En Outlook, los contactos de [!INCLUDE[d365fin](includes/d365fin_md.md)] se muestran en una carpeta en **Otros contactos** en la vista **Personas**. Si no está familiarizado con la vista Personas en Outlook, puede acceder a ella desde las opciones de navegación en la esquina inferior izquierda de Outlook.  

## <a name="see-also"></a>Consulte también
[Introducción](product-get-started.md)  
[Finanzas](finance.md)  
[Ventas](sales-manage-sales.md)  
[Compras](purchasing-manage-purchasing.md)  
[Usar contactos (personas) en Outlook en la web](https://support.office.com/en-us/article/Using-contacts-People-in-Outlook-on-the-web-1e3438c7-26b2-420c-87de-3cea9d31b5cb?appver=OWB150)  
