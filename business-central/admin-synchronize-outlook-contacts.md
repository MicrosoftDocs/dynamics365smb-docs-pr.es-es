---
title: Compartir contactos entre Business Central y Outlook
description: Este servicio tiene una integración profunda con Microsoft 365 para que pueda compartir contactos entre Outlook y Business Central.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'contacts, Microsoft 365'
ms.search.form: '6700, 5320, 5300, 5301, 5302, 5303, 5304, 5305, 5306, 5307, 5308, 5309, 5310, 5311'
ms.date: 03/17/2023
ms.author: bholtorf
---
# <a name="synchronize-contacts-in-business-central-with-contacts-in-microsoft-outlook"></a><a name="synchronize-contacts-in-business-central-with-contacts-in-microsoft-outlook"></a>Sincronizar los contactos de Business Central con los de Microsoft Outlook

Puede configurar la sincronización de contactos para que sus contactos en [!INCLUDE[prod_short](includes/prod_short.md)] tengan la misma información que sus contactos en Microsoft Outlook. Por ejemplo, si es comercial, puede trabajar al mismo tiempo en Outlook y [!INCLUDE[prod_short](includes/prod_short.md)]. Si los contactos son los mismos en ambos lugares, su trabajo es más sencillo.  

De forma predeterminada, los contactos que está sincronizando se guardan en una carpeta de **Business Central** en sus Favoritos en el Panel de carpetas en Outlook. La carpeta Business Central puede facilitar la identificación de los contactos que está sincronizando. Puede configurar filtros para sincronizar solo contactos específicos de [!INCLUDE[prod_short](includes/prod_short.md)] a Outlook. Una vez que haya configurado la sincronización, puede sincronizar manualmente o automatizar el proceso para sincronizar de forma programada.  

## <a name="prerequisites"></a><a name="prerequisites"></a>Requisitos previos

- Su perfil de usuario en [!INCLUDE[prod_short](includes/prod_short.md)] debe especificar su cuenta de correo electrónico de Microsoft 365.

  Puede comprobar esta configuración en la sección **Autenticación de Microsoft 365** de su perfil de usuario en la lista **Usuarios**.
- Con [!INCLUDE[prod_short](includes/prod_short.md)], configuró la sincronización de contactos como se describe en [Configurar la sincronización de contactos con Outlook para Business Central local](admin-contact-sync-setup-onprem.md)

## <a name="set-up-synchronization"></a><a name="set-up-synchronization"></a>Configurar sincronización

Configure cómo quiere sincronizar los contactos con Outlook en la página **Configuración de la sincronización de Exchange** en [!INCLUDE[prod_short](includes/prod_short.md)]. 

En la página **Configuración de la sincronización de Exchange**, puede validar que la conexión a Exchange está funcionando y luego configurar la sincronización de contactos. Desde la página **Configuración de sincronización de Exchange**, puede abrir la página **Configuración de sincronización de contactos** e iniciar la sincronización. Opcionalmente, establezca un filtro para especificar los contactos que desea sincronizar. Por ejemplo, puede filtrar por nombre, tipo, empresa, etc. También puede cambiar el nombre predeterminado de la carpeta en Outlook en la que se sincronizarán los contactos.  

Cada uno de sus compañeros de trabajo también puede configurar su propia sincronización de Exchange y establecer su propio filtro sobre qué contactos sincronizar.  

Después de configurar la sincronización, puede sincronizar los cambios en el contacto manualmente o puede automatizar el proceso configurando una entrada en la cola de trabajos. Para obtener más información acerca de la automatización, consulte la siguiente sección de este artículo.

### <a name="automate-synchronization"></a><a name="automate-synchronization"></a>Automatizar sincronización

Puede crear una entrada en la cola de trabajos que sincronizará los contactos de acuerdo a una programación que defina. Para obtener más información, consulte [Uso de colas de proyectos para programar tareas](admin-job-queues-schedule-tasks.md). 

La siguiente tabla enumera los ajustes en la página **Ficha mov. cola proyecto** para sincronizar contactos:

|Campo|Configuración para la sincronización de contactos|
|-----|-----|
|Tipo objeto para ejecutar|Codeunit|
|Id. objeto para ejecutar|6700|

## <a name="synchronize-contacts"></a><a name="synchronize-contacts"></a>Sincronizar contactos

Si está acostumbrado a trabajar con contactos en [!INCLUDE[prod_short](includes/prod_short.md)], le resultará fácil sincronizar manualmente desde la lista **Contactos** cuando le convenga. Puede sincronizar sus contactos de dos maneras:

* **Sincronizar con Microsoft 365**

  Sincronice todos los cambios de [!INCLUDE[prod_short](includes/prod_short.md)] a Microsoft 365 que se hicieron desde la última sincronización, en función de la última fecha de modificación. Además, los contactos nuevos de Microsoft 365 se sincronizarán con [!INCLUDE[prod_short](includes/prod_short.md)]. Normalmente, esta acción es más rápida que hacer una sincronización completa. 

* **Sincronización completa con Microsoft 365**

  Sincronice todos los contactos en ambas direcciones, independientemente de la fecha de la última sincronización y la fecha de última modificación.  

En ambos casos, los contactos solo se sincronizan desde Outlook si tienen rellenos los campos obligatorios. Los campos obligatorios para sincronizar a Microsoft 365 son **Nombre**, **Dirección de correo electrónico** y el contacto deben ser de tipo **Persona**. [!INCLUDE[prod_short](includes/prod_short.md)] es la fuente de la información de contacto, por lo que la información de contacto de [!INCLUDE[prod_short](includes/prod_short.md)] se guardará si hay duplicados.  

> [!NOTE]
> Si elimina un contacto en Outlook, pero lo mantiene en [!INCLUDE[prod_short](includes/prod_short.md)], el contacto se volverá a crear en Outlook la próxima vez que sincronice. 

## <a name="see-also"></a><a name="see-also"></a>Consulte también

[Preparación para hacer negocios](ui-get-ready-business.md)  
[Finanzas](finance.md)  
[Ccial](sales-manage-sales.md)  
[Compras](purchasing-manage-purchasing.md)  
[Usar contactos (personas) en Outlook en la web](https://support.office.com/article/Using-contacts-People-in-Outlook-on-the-web-1e3438c7-26b2-420c-87de-3cea9d31b5cb?appver=OWB150)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
