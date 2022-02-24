---
title: Configuración de cuentas de usuario para la integración con Dynamics 365 Sales | Documentos de Microsoft
description: Obtenga información sobre cómo configurar las cuentas de usuario que las aplicaciones usan para intercambiar datos y que los usuarios usan para acceder y sincronizar datos en las aplicaciones.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 64dd9d1e4645b845c02872a8bc09f0925f4fa33c
ms.sourcegitcommit: 3d128a00358668b3fdd105ebf4604ca4e2b6743c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/20/2019
ms.locfileid: "2910567"
---
# <a name="setting-up-user-accounts-for-integrating-with-dynamics-365-sales"></a>Configuración de cuentas de usuario para la integración con Dynamics 365 Sales
Este artículo proporciona una visión general de cómo configurar las cuentas de usuario que se necesitan para integrar [!INCLUDE[crm_md](includes/crm_md.md)] con [!INCLUDE[d365fin](includes/d365fin_md.md)].  

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2085500]

## <a name="setting-up-the-administrator-user-account-in-sales"></a>Configuración de la cuenta de usuario administrador en Sales
Debe agregar su cuenta de usuario administrador para [!INCLUDE[d365fin](includes/d365fin_md.md)] como usuario en [!INCLUDE[crm_md](includes/crm_md.md)] y luego promocionar al usuario a administrador en [!INCLUDE[crm_md](includes/crm_md.md)]. La cuenta de usuario administrador también debe tener el rol Personalizador del sistema y al menos otro rol de usuario no administrativo, como Director de ventas, en [!INCLUDE[crm_md](includes/crm_md.md)].

## <a name="setting-up-the-user-account-for-the-integration"></a>Configuración de la cuenta de usuario para la integración
Debe crear una cuenta de usuario dedicada en su suscripción de Office 365 que [!INCLUDE[d365fin](includes/d365fin_md.md)] y [!INCLUDE[crm_md](includes/crm_md.md)] puedan utilizar para sincronizar datos. Esta cuenta de usuario debe poder iniciar sesión en [!INCLUDE[crm_md](includes/crm_md.md)], lo que significa que este usuario debe tener una licencia para [!INCLUDE[crm_md](includes/crm_md.md)] y al menos un rol de seguridad asignado en [!INCLUDE[crm_md](includes/crm_md.md)], tal y como se describe [aquí](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles#create-a-user-account). Para obtener más información sobre cómo crear usuarios en [!INCLUDE[crm_md](includes/crm_md.md)], consulte [Administrar la seguridad, los usuarios y los equipos](https://go.microsoft.com/fwlink/?LinkID=616518). Una vez establecida la conexión, [!INCLUDE[d365fin](includes/d365fin_md.md)] asignará a la cuenta de usuario los roles de seguridad que necesita en [!INCLUDE[d365fin](includes/d365fin_md.md)] y esta cuenta puede configurarse en [modo de acceso no interactivo](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles#create-a-non-interactive-user-account) en [!INCLUDE[crm_md](includes/crm_md.md)]

![Guía de configuración asistida que muestra el lugar para introducir las credenciales de usuario de sincronización](media/sync-user-setup.png "Página del asistente de configuración asistida de visualización que muestra el lugar para introducir las credenciales de usuario de sincronización")

> [!IMPORTANT]  
> No utilice la cuenta de administrador de [!INCLUDE[crm_md](includes/crm_md.md)] para la sincronización. Si lo hace, la sincronización se interrumpirá.
> Además, para evitar una sincronización constante, los cambios en los datos realizados por la cuenta de usuario de integración no están sincronizados. <!--What changes would this account make?--> Una vez establecida la conexión, se recomienda configurar el modo de acceso de la cuenta de usuario para la integración en modo no interactivo en [!INCLUDE[crm_md](includes/crm_md.md)]. Para obtener más información, consulte [Crear una cuenta de usuario no interactiva](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles#create-a-non-interactive-user-account).

## <a name="setting-up-accounts-for-salespeople"></a>Configuración de cuentas para vendedores
Debe crear cuentas de usuario en [!INCLUDE[crm_md](includes/crm_md.md)] para los vendedores desde [!INCLUDE[d365fin](includes/d365fin_md.md)]. Para hacerlo más fácil, el centro de administración de Microsoft 365 ofrece una plantilla de Excel que puede utilizar. En la página **Usuarios activos**, seleccione **Más** y, a continuación, **Importar varios usuarios**. Seleccione **Descargar un archivo CSV solo con cabeceras** y, a continuación, introduzca la información para los vendedores. Para ver un ejemplo, seleccione **Descargar un archivo CSV con cabeceras e información de usuario de ejemplo**. Después de introducir la información sobre los usuarios, el siguiente paso del proceso de importación es asignar las licencias de usuario al plan de Dynamics 365 Customer Engagement.  

Después de importar los usuarios y asignarles licencias para Dynamics 365 Customer Engagement, debe asignar los usuarios al rol **Vendedor** en [!INCLUDE[crm_md](includes/crm_md.md)].

![Emparejar vendedores con usuarios en Dynamics 365 Sales](media/couple-salespeople.png "Visualización de emparejamiento de vendedores con usuarios en Dynamics 365 Sales")

## <a name="minimum-permissions-for-user-accounts-in-crm_md"></a>Permisos mínimos para cuentas de usuario en [!INCLUDE[crm_md](includes/crm_md.md)]
Cuando instala la solución de integración, los permisos para la cuenta de usuario de integración se configuran en [!INCLUDE[crm_md](includes/crm_md.md)]. Si se cambian esos permisos, es posible que deba restablecerlos. Puede hacerlo reinstalando la solución de integración o restableciéndolos manualmente. Las siguientes tablas enumeran los permisos mínimos para las cuentas de usuario en [!INCLUDE[crm_md](includes/crm_md.md)].

### <a name="integration-administrator"></a>Administrador de integración
La siguiente tabla muestra los permisos mínimos en cada pestaña para cada rol de seguridad que se requiere para el usuario administrador.

##### <a name="customization"></a>Personalización
|Rol de seguridad|Nivel de acceso|Dynamics NAV 2018 y anteriores|Business Central <br> Octubre de 2018|Business Central <br> Abril de 2019|
|----|----|-----|----|----|
|Aplicación basada en modelos|Global|||Leer|
|Ensamblado de complemento|Global|Leer|Leer|Leer|
|Tipo de complemento|Global|Leer|Leer|Leer|
|Relaciones|Global|||Leer|
|Mensaje del SDK|Global|Leer|Leer|Leer|
|Paso de procesamiento de mensajes del SDK|Global|Leer|Leer|Leer|
|Imagen del paso de procesamiento de mensajes del SDK|Global|Leer|Leer|Leer|
|Sistema de origen|Global|||Escribir|

##### <a name="custom-entities"></a>Entidades personalizadas
|Rol de seguridad|Nivel de acceso|Dynamics NAV 2018 y anteriores|Business Central <br> Octubre de 2018|Business Central <br> Abril de 2019|
|----|----|-----|----|----|
|Estadísticas de cuenta de Business Central|Global|Leer|Leer|Leer|
|Conexión de Business Central|Global|Crear, leer, escribir, eliminar|Crear, leer, escribir, eliminar|Crear, leer, escribir, eliminar|
|Configuración de registro|Global|||Escribir|

#### <a name="integration-user"></a>Usuario de integración
La siguiente tabla muestra los permisos mínimos en cada pestaña para cada rol de seguridad que se requiere para el usuario de integración.

##### <a name="core-records"></a>Registros básicos
|Rol de seguridad|Nivel de acceso|Dynamics NAV 2018 y anteriores|Business Central <br> Octubre de 2018|Business Central <br> Abril de 2019|
|----|----|-----|----|----|
|Cuenta|Global|Crear, leer, escribir, anexar, anexar a, asignar|Crear, leer, escribir, anexar, anexar a, asignar|Crear, leer, escribir, anexar, anexar a, asignar|
|Ficha de acción|Global||Leer|Leer|
|Conexión|Global|Leer|Leer|Leer|
|Contacto|Global|Crear, leer, escribir, anexar, anexar a|Crear, leer, escribir, anexar, anexar a|Crear, leer, escribir, anexar, anexar a|
|Nota|Global|||Crear, leer, escribir, eliminar, anexar, asignar|
|Oportunidad|Global||Crear, leer, escribir, anexar, anexar a|Crear, leer, escribir, anexar, anexar a|
|Envíos postales|Global|||Crear, leer, anexar A|
|Interfaz de usuario de entidad de usuario|Usuario|Crear, leer, escribir|Crear, leer, escribir|Crear, leer, escribir|

##### <a name="sales"></a>Ccial
|Rol de seguridad|Nivel de acceso|Dynamics NAV 2018 y anteriores|Business Central <br> Octubre de 2018|Business Central <br> Abril de 2019|
|----|----|-----|----|----|
|Facturar|Global|Crear, leer, escribir, anexar, anexar a|Crear, leer, escribir, anexar, anexar a|Crear, leer, escribir, anexar, anexar a|
|Sentido|Global|Leer, escribir, anexar a|Leer, escribir, anexar a|Leer, escribir, anexar, anexar a, asignar|
|Producto|Global|Crear, leer, escribir, anexar, anexar a|Crear, leer, escribir, anexar, anexar a|Crear, leer, escribir, anexar, anexar a|
|Propiedad|Global|Leer|Leer|Leer|
|Asociación de propiedad|Global|Leer|Leer|Leer|
|Opción de propiedad Establecer producto|Global|Leer|Leer|Leer|
|Oferta|Global|Leer|Leer|Leer|

##### <a name="service"></a>Servicio
|Rol de seguridad|Nivel de acceso|Dynamics NAV 2018 y anteriores|Business Central <br> Octubre de 2018|Business Central <br> Abril de 2019|
|----|----|-----|----|----|
|Caso|Global|Leer|Leer|Leer|

##### <a name="business-management"></a>Administración empresarial
|Rol de seguridad|Nivel de acceso|Dynamics NAV 2018 y anteriores|Business Central <br> Octubre de 2018|Business Central <br> Abril de 2019|
|----|----|-----|----|----|
|Divisa|Global|Crear, leer, escribir|Crear, leer, escribir|Crear, leer, escribir|
|Organización|Global|Leer, escribir|Leer, escribir|Leer, escribir|
|Rol de seguridad|Global|||Leer|
|Usuario|Global|Crear, leer, escribir, anexar, anexar a|Crear, leer, escribir, anexar, anexar a|Crear, leer, escribir, anexar, anexar a|
|Configuración de usuario|Global|Crear, leer, escribir, eliminar, anexar a|Crear, leer, escribir, eliminar, anexar a|Crear, leer, escribir, eliminar, anexar a|
|Actuar en nombre de otro usuario|Global|Sí|Sí|Sí|

##### <a name="customization"></a>Personalización
|Rol de seguridad|Nivel de acceso|Dynamics NAV 2018 y anteriores|Business Central <br> Octubre de 2018|Business Central <br> Abril de 2019|
|----|----|-----|----|----|
|Campo|Global||Leer|Leer|
|Ensamblado de complemento|Global|Leer|Leer|Leer|
|Tipo de complemento|Global|Leer|Leer|Leer|
|Mensaje del SDK|Global|Leer|Leer|Leer|
|Paso de procesamiento de mensajes del SDK|Global|Leer|Leer|Leer|
|Recurso web|Global|Leer|Leer|Leer|

##### <a name="custom-entities"></a>Entidades personalizadas
|Rol de seguridad|Nivel de acceso|Dynamics NAV 2018 y anteriores|Business Central <br> Octubre de 2018|Business Central <br> Abril de 2019|
|----|----|-----|----|----|
|Estadísticas de cuenta de Dynamics 365 Business Central|Global|Crear, leer, escribir, anexar a|Crear, leer, escribir, anexar a|Crear, leer, escribir, anexar a|
|Conexión de Dynamics 365 Business Central|Global|Leer|Leer|Leer|

### <a name="product-availability-user"></a>Usuario de disponibilidad de producto
Puede permitir que los vendedores vean los niveles de inventario de los productos que venden otorgándoles los permisos descritos en la siguiente tabla.

##### <a name="custom-entities"></a>Entidades personalizadas
|Rol de seguridad|Nivel de acceso|Dynamics NAV 2018 y anteriores|Business Central <br> Octubre de 2018|Business Central <br> Abril de 2019|
|----|----|-----|----|----|
|Estadísticas de cuenta de Dynamics 365 Business Central|Global|Crear, leer, escribir, anexar a|Crear, leer, escribir, anexar a|Crear, leer, escribir, anexar a|
|Conexión de Dynamics 365 Business Central|Global|Leer|Leer|Leer|

## <a name="see-also"></a>Consulte también  
[Integración con Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  
