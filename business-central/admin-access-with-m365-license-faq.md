---
title: P+F del acceso con licencias de Microsoft 365
description: Obtenga respuestas a preguntas comunes sobre el acceso a Business Central con licencias de Microsoft 365.
author: mikebc
ms.author: mikebc
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: faq
ms.date: 11/22/2022
ms.custom: bap-template
---
# <a name="access-with-microsoft-365-licenses-faq"></a><a name="access-with-microsoft-365-licenses-faq"></a>P+F del acceso con licencias de Microsoft 365

[!INCLUDE [2023rw1-sec-group-short](includes/2023rw1-sec-group-short.md)]

Los usuarios pueden acceder a los datos de Business Central en Microsoft Teams usando su licencia de Microsoft 365. Este artículo responde a las preguntas más frecuentes de administradores, consultores y otros. Los desarrolladores deben consultar las Preguntas frecuentes para desarrolladores. Si tiene preguntas sobre la integración de Business Central con Microsoft Teams, vaya a [Preguntas frecuentes de Teams](teams-faq.md).

## [Permisos](#tab/permissions) 

### <a name="can-i-proactively-configure-different-starting-permissions-for-different-groups-of-users"></a><a name="can-i-proactively-configure-different-starting-permissions-for-different-groups-of-users"></a>¿Puedo configurar proactivamente diferentes permisos de inicio para diferentes grupos de usuarios?

No en este momento. Business Central solo permite configurar un grupo de permisos que se asignan a todos los usuarios de Microsoft 365 cuando inician sesión en Business Central por primera vez.

### <a name="can-i-proactively-configure-permissions-profiles-and-settings-for-individual-users-before-they-sign-in"></a><a name="can-i-proactively-configure-permissions-profiles-and-settings-for-individual-users-before-they-sign-in"></a>¿Puedo configurar proactivamente permisos, perfiles y configuraciones para usuarios individuales antes de que inicien sesión?

Sí. Se puede lograr a través de grupos de seguridad. Al aplicar un grupo de seguridad a un entorno, define el conjunto total de usuarios que tienen acceso a ese entorno. Este grupo de seguridad puede incluir usuarios con una licencia de Business Central y usuarios con una licencia Microsoft 365 . La próxima vez que actualice usuarios de Microsoft 365 en la lista **Usuarios**, se crearán los registros de usuario de Microsoft 365. Luego puede asignar grupos de usuarios, permisos, perfiles y otras configuraciones antes de que inicien sesión.

### <a name="after-a-user-signs-in-can-i-change-which-objects-they-have-access-to"></a><a name="after-a-user-signs-in-can-i-change-which-objects-they-have-access-to"></a>Después de que un usuario inicie sesión, ¿puedo cambiar a qué objetos tiene acceso?

Sí. Después de que un usuario haya iniciado sesión por primera vez y se haya aprovisionado su registro de usuario, los administradores administran esos usuarios como cualquier otro usuario de Business Central. Por ejemplo, pueden agregar o quitar permisos a diferentes objetos. Si cambia los conjuntos de permisos asignados a la licencia de Microsoft 365 en la página Configuración de licencia, el cambio solo afectará a los próximos usuarios que inicien sesión por primera vez.

### <a name="how-do-i-prevent-access-to-sensitive-tables"></a><a name="how-do-i-prevent-access-to-sensitive-tables"></a>¿Cómo evito el acceso a tablas confidenciales?

Business Central ofrece un modelo de permisos potente y flexible donde los administradores pueden definir conjuntos de permisos que otorgan acceso a objetos específicos, procesos comerciales o roles completos. Para evitar el acceso a tablas confidenciales, puede crear conjuntos de permisos personalizados que excluyan el permiso para objetos confidenciales. Para obtener más información acerca de cómo excluir permisos, vea [Crear un conjunto de permisos](ui-define-granular-permissions.md).  

### <a name="instead-of-customizing-the-license-configuration-can-i-customize-a-user-group"></a><a name="instead-of-customizing-the-license-configuration-can-i-customize-a-user-group"></a>En lugar de personalizar la configuración de la licencia, ¿puedo personalizar un grupo de usuarios?

Sí. Agregar conjuntos de permisos al grupo de usuarios Usuarios internos de Microsoft Teams en Business Central tiene el mismo efecto neto que agregar conjuntos de permisos a la licencia de Microsoft 365, siempre que la licencia de Microsoft 365 continúe asignándose a este grupo de usuarios. Este enfoque tiene el beneficio adicional de que los conjuntos de permisos siempre se sincronizan con los miembros del grupo cada vez que modifica el grupo de usuarios.

### <a name="when-a-business-central-user-shares-a-record-in-teams-do-they-grant-new-permissions"></a><a name="when-a-business-central-user-shares-a-record-in-teams-do-they-grant-new-permissions"></a>Cuando un usuario de Business Central comparte un registro en Teams, ¿concede nuevos permisos?

N.º Esta acción no es lo mismo que compartir un enlace a un documento de SharePoint donde la persona que comparte el documento puede elegir otorgar permiso a otros. En Business Central, solo los administradores pueden configurar y asignar permisos. En comparación con compartir documentos de SharePoint, es el equivalente a elegir la opción "Compartir con personas con acceso existente".

### <a name="does-this-feature-support-row-level-security"></a><a name="does-this-feature-support-row-level-security"></a>¿Esta función es compatible con la seguridad a nivel de fila?

Sí. Aunque una persona que acceda a un registro en Teams con su licencia de Microsoft 365 pueda tener los permisos de objeto de tabla y página correctos, los permisos de nivel de fila se aplicarán si se implementaron para esa tabla.  

### <a name="if-i-configure-permissions-that-include-write-access-will-users-be-able-to-write-in-teams"></a><a name="if-i-configure-permissions-that-include-write-access-will-users-be-able-to-write-in-teams"></a>Si configuro permisos que incluyen acceso de escritura, ¿los usuarios podrán escribir en Teams?

Si configura Business Central para asignar un conjunto de permisos que incluye insertar, modificar o eliminar el acceso a uno o más objetos, los usuarios con ese conjunto de permisos aún no podrán escribir en Teams cuando solo tengan una licencia de Microsoft 365. El servicio Business Central impone el acceso de solo lectura sin importar el permiso de inserción, modificación o eliminación que asigne.  

Aunque Business Central proporciona este nivel de protección, le recomendamos que evite los conjuntos de permisos con acceso de escritura. Hacerlo evita problemas posteriores cuando los usuarios cambian de rol o adquieren nuevas licencias.  

## [Instalación y configuración](#tab/setup)

### <a name="why-is-the-setting-to-enable-access-not-available-for-my-environment"></a><a name="why-is-the-setting-to-enable-access-not-available-for-my-environment"></a>¿Por qué la configuración para habilitar el acceso no está disponible para mi entorno?

Habilitar el acceso con licencias de Microsoft 365 licencias solo está disponible para entornos de Business Central de la plataforma versión 21.1 o posterior. Cuando su entorno se actualiza a esta versión mínima, la configuración pasa a estar disponible automáticamente. Para verificar la versión de su entorno, vaya a la página de detalles del entorno para el entorno en el centro de administración de Business Central. O bien, inicie sesión en el entorno y vaya a la página **Ayuda y soporte** del menú **Ayuda** .

### <a name="can-i-access-business-central-on-premises-with-microsoft-365-licenses"></a><a name="can-i-access-business-central-on-premises-with-microsoft-365-licenses"></a>¿Puedo acceder a Business Central en las instalaciones con licencias de Microsoft 365?

No, no se admite. Business Central muestra un error cuando los usuarios intentan acceder a los registros locales de Business Central en Teams.

### <a name="what-is-the-employee-profile"></a><a name="what-is-the-employee-profile"></a>¿Qué es el perfil del empleado?

El perfil de **Empleado** que se muestra en la página de lista **Perfiles (Roles)** se introdujo con la Actualización 21.1. Es el perfil predeterminado asignado a los usuarios que acceden a Business Central con su licencia Microsoft 365 . Este perfil está destinado a personas de una organización que no tienen un rol específico en Business Central y solo necesitan ver los datos que se compartieron con ellos.

### <a name="what-is-the-teams-users-user-group"></a><a name="what-is-the-teams-users-user-group"></a>¿Qué es el grupo de usuarios de usuarios de Teams?

El grupo **Usuarios internos de Microsoft Teams** que se muestra en la página **Grupos de usuarios** se presentó con la Actualización 21.1. Este grupo es el grupo de usuarios predeterminado asignado a los usuarios que acceden a Business Central con su licencia Microsoft 365 . El grupo de usuarios está destinado a personas dentro de la misma organización donde se aloja Business Central que colaboran en Microsoft Teams.  

### <a name="do-users-that-only-have-a-microsoft-365-license-show-up-in-the-users-list-in-business-central"></a><a name="do-users-that-only-have-a-microsoft-365-license-show-up-in-the-users-list-in-business-central"></a>¿Aparecen los usuarios que solo tienen una licencia de Microsoft 365 en la lista de usuarios de Business Central?

Sí. Si aplica grupos de seguridad a entornos, esos usuarios aparecerán en la lista de usuarios después de usar la acción Actualizar usuarios desde Microsoft 365 en la lista **Usuarios** . Si no aplica grupos de seguridad, los registros de usuario aparecen en la lista de usuarios después de la primera vez que acceden a un registro de Business Central.

### <a name="does-this-feature-work-for-embed-isv-solutions"></a><a name="does-this-feature-work-for-embed-isv-solutions"></a>¿Funciona esta característica para soluciones integradas de ISV?

Sí. Los usuarios con solo una licencia de Microsoft 365 también pueden acceder a registros en entornos que se ejecutan bajo el dominio *.bc.dynamics.com.

## [Licencias](#tab/license)

### <a name="can-a-customer-use-this-feature-if-they-dont-have-business-central"></a><a name="can-a-customer-use-this-feature-if-they-dont-have-business-central"></a>¿Puede un cliente usar esta función si no tiene Business Central?

El acceso a Business Central con una licencia de Microsoft 365 está destinado a organizaciones que ya están suscritas a Business Central y operan uno o más entornos de Business Central con usuarios de Business Central con licencia. No proporciona nuevas funciones ni derechos de uso a los clientes de Microsoft 365 que no tienen un plan Business Central.

### <a name="how-does-this-help-me-manage-subscription-costs-in-my-organization"></a><a name="how-does-this-help-me-manage-subscription-costs-in-my-organization"></a>¿Cómo me ayuda esto a administrar los costos de suscripción en mi organización?

Para maximizar la productividad y optimizar sus operaciones, las pymes suelen comprar Dynamics 365 Business Central junto con Microsoft 365. En cuyo caso, la mayoría de las personas reciben una licencia de Microsoft 365, pero solo determinados roles o personas reciben una licencia de Business Central. Business Central ofrece flexibilidad de licencias para que los clientes paguen solo por lo que necesitan:

- A los usuarios que requieren acceso completo a Business Central normalmente se les asigna una licencia Business Central Essentials o Business Central Premium. 
- A los usuarios que requieren acceso de escritura limitado normalmente se les asigna una licencia de miembro del equipo de Business Central.
- Todos los demás empleados de la organización que solo necesitan leer ocasionalmente los datos comerciales que se comparten con ellos, pueden hacerlo si tienen una licencia de Microsoft 365. No es necesario que se les asigne una licencia de miembro del equipo. Están disponibles otras opciones de licencias. Para obtener más información, descargue y lea la [guía de licencias de Dynamics 365](https://go.microsoft.com/fwlink/?LinkId=866544).

### <a name="is-this-100-free-of-charge"></a><a name="is-this-100-free-of-charge"></a>¿Esto es 100% gratuito?
 
N.º El acceso a los datos de Business Central en Microsoft Teams requiere que cada usuario tenga una licencia de Business Central o una licencia de Microsoft 365 de la lista de planes admitidos.

### <a name="does-this-work-with-microsoft-365-trials-and-business-central-trials"></a><a name="does-this-work-with-microsoft-365-trials-and-business-central-trials"></a>¿Funciona esto con pruebas de Microsoft 365 y pruebas de Business Central?

Sí. Si a un usuario se le asigna una licencia de Microsoft 365 de una versión de prueba de un plan compatible, también puede acceder a los registros de Business Central en Teams. Entonces es posible que los clientes prueben las aplicaciones empresariales y de productividad de Microsoft trabajando juntas, y permite que los vendedores y consultores asociados demuestren fácilmente esta función. Por ejemplo, los socios pueden aprovisionar sus propios inquilinos de Azure AD desde [https://aka.ms/CDX](https://aka.ms/CDX) que incluyen pruebas de Microsoft 365 y pruebas de Business Central para demostrar Business Central.

### <a name="the-list-of-licenses-in-business-central-shows-a-microsoft-365-license-whats-that"></a><a name="the-list-of-licenses-in-business-central-shows-a-microsoft-365-license-whats-that"></a>La lista de licencias en Business Central muestra una licencia de Microsoft 365. ¿Qué es eso?

La página **Configuración de licencias** en Business Central muestra los diferentes tipos de licencias que pueden proporcionar acceso al servicio de Business Central. En la versión 21, Microsoft agregó Microsoft 365 a esta lista como una nueva forma de acceder a Business Central. Esta lista de licencias no implica que su organización haya comprado suscripciones a ninguna de estas licencias o que su organización haya habilitado el acceso a través de esas licencias.

### <a name="do-i-need-to-acquire-a-new-type-of-microsoft-365-license-for-this-feature-to-work"></a><a name="do-i-need-to-acquire-a-new-type-of-microsoft-365-license-for-this-feature-to-work"></a>¿Necesito adquirir un nuevo tipo de licencia Microsoft 365 para que funcione esta función?

Microsoft no ha creado nuevas licencias ni nuevos planes para potenciar esta función. Esta función se basa por completo en los planes y licencias de Microsoft 365 existentes. Si ya está suscrito a uno de los planes admitidos Microsoft 365, entonces ya tiene este nuevo derecho de uso. De lo contrario, si no se suscribe a Microsoft 365 hoy, puede suscribirse a Microsoft 365 Business Premium o planes similares aquí. 

### <a name="how-do-i-find-out-which-users-have-only-a-microsoft-365-license"></a><a name="how-do-i-find-out-which-users-have-only-a-microsoft-365-license"></a>¿Cómo puedo saber qué usuarios solo tienen una licencia de Microsoft 365?

Hay múltiples formas. En el centro de administración de Microsoft 365, vaya a la lista de **Usuarios activos** y consulte la columna **Licencias**. En Business Central, vaya a la lista **Usuarios**, elija cualquiera de los usuarios y vea el cuadro informativo **Licencias**.  

### <a name="how-do-i-filter-the-users-list-in-business-central-to-see-users-that-only-have-a-microsoft-365-license"></a><a name="how-do-i-filter-the-users-list-in-business-central-to-see-users-that-only-have-a-microsoft-365-license"></a>¿Cómo filtro la lista Usuarios en Business Central para ver los usuarios que solo tienen una licencia de Microsoft 365?

Esta tarea actualmente no es posible usando un filtro o una vista de lista. Sin embargo, puede seleccionar un usuario en la lista y ver el Cuadro informativo de licencias que incluirá solo Microsoft 365, si el usuario solo tiene una licencia Microsoft 365.

### <a name="what-about-users-that-have-both-a-microsoft-365-license-and-a-business-central-license"></a><a name="what-about-users-that-have-both-a-microsoft-365-license-and-a-business-central-license"></a>¿Qué pasa con los usuarios que tienen tanto una licencia de Microsoft 365 como una licencia de Business Central?

Cuando se asignan varias licencias a un usuario, los derechos de uso de licencias mayores ganan sobre los derechos de uso de licencias menores al acceder a Business Central. En este caso, la licencia de Business Central otorga al usuario más derechos de usuario. Por lo tanto, los usuarios pueden leer y escribir registros de Business Central en Teams y acceder al cliente web de Business Central en el navegador, como cualquier otro titular de licencia de Business Central. Si se han configurado conjuntos de permisos específicos para la licencia de Microsoft 365, el usuario obtiene los conjuntos de permisos configurados combinados con los conjuntos de permisos de la licencia de Business Central o que ya se han asignado al usuario.

### <a name="is-this-licensing-related-to-the-business-central-team-member-license"></a><a name="is-this-licensing-related-to-the-business-central-team-member-license"></a>¿Esta licencia está relacionada con la licencia de Business Central Team Member?

No existe ninguna relación entre las licencias de miembro del equipo de Business Central y el acceso a Business Central en Microsoft Teams usando licencias de Microsoft 365. Aunque Microsoft Teams y su documentación se refieren a las personas de un equipo como *miembros del equipo*, es un término colectivo para un grupo de usuarios de Microsoft Teams. No hace referencia a las licencias de Business Central.

### <a name="does-business-central-enforce-any-of-the-constraints"></a><a name="does-business-central-enforce-any-of-the-constraints"></a>¿Business Central aplica alguna de las restricciones?

Sí, la plataforma Business Central aplica todas las restricciones y requisitos mínimos de la plataforma, incluidos los requisitos de licencia. Esto guía a los usuarios con mensajes de error específicos para ayudarlos a solucionar problemas de configuración y evitar abusos. Por ejemplo, si un usuario que solo tiene una licencia de Microsoft 365 intenta acceder al cliente web de Business Central en el navegador, se denegará el acceso y se mostrará un mensaje de error de orientación. 

## [Uso](#tab/usage)
 
### <a name="can-i-access-records-on-teams-for-ios-and-teams-for-android"></a><a name="can-i-access-records-on-teams-for-ios-and-teams-for-android"></a>¿Puedo acceder a registros en Teams para iOS y Teams para Android?

Actualmente, no es posible acceder a los datos de Business Central en el móvil de Teams usando solo una licencia de Microsoft 365. Microsoft está trabajando para habilitar esta capacidad en breve. 

### <a name="how-do-users-change-their-personal-settings-in-my-settings"></a><a name="how-do-users-change-their-personal-settings-in-my-settings"></a>¿Cómo cambian los usuarios su configuración personal en Mi configuración?

Cuando un usuario accede a Business Central por primera vez utilizando solo su licencia de Microsoft 365, su configuración de usuario, como el idioma, la zona horaria y la configuración regional, se establece automáticamente en función de su sistema operativo o la configuración del navegador. Los administradores pueden modificar esta configuración desde Business Central para cada usuario. 

### <a name="what-determines-the-choice-of-language-when-you-sign-in-for-the-first-time"></a><a name="what-determines-the-choice-of-language-when-you-sign-in-for-the-first-time"></a>¿Qué determina la elección del idioma cuando inicia sesión por primera vez?

El idioma con el que experimenta Business Central se establece en función de varios factores, incluido el cliente de Teams a través del cual accedió a Business Central la primera vez. Para la aplicación de escritorio de Teams, Teams para iOS y Teams para Android, se aplica el idioma del sistema operativo. Para Teams para la web, se aplica el idioma del navegador. En todos los casos, no se considera el idioma de Teams. 

### <a name="why-cant-i-activate-some-of-the-colored-links-in-tabs-and-card-details"></a><a name="why-cant-i-activate-some-of-the-colored-links-in-tabs-and-card-details"></a>¿Por qué no puedo activar algunos de los enlaces de colores en las pestañas y los detalles de la tarjeta?

Los enlaces procesables en las páginas de Business Central a menudo se muestran como hipervínculos en negrita que se pueden activar para ir a otro lugar o ejecutar alguna operación. En un nivel técnico, estos enlaces se implementan normalmente como valores de campo sin título que activan algún código y donde la elección del estilo a menudo refleja el estado. Cuando los usuarios acceden a las páginas de Business Central con su licencia de Microsoft 365, los enlaces se diseñan como si fueran accionables. Pero no se pueden activar porque esta licencia no ofrece derechos de uso para ejecutar acciones.  

### <a name="why-cant-i-activate-page-notification-actions"></a><a name="why-cant-i-activate-page-notification-actions"></a>¿Por qué no puedo activar las acciones de notificación de la página?

Las notificaciones contextuales que se muestran en las páginas suelen ir acompañadas de enlaces accionables. Cuando los usuarios acceden a las páginas de Business Central con su licencia de Microsoft 365, estos enlaces se muestran, pero no se pueden activar porque esta licencia no ofrece derechos de uso para ejecutar acciones. A nivel técnico, estos enlaces se implementan como acciones.

### <a name="can-microsoft-365-users-remove-tabs"></a><a name="can-microsoft-365-users-remove-tabs"></a>¿Pueden los usuarios de Microsoft 365 eliminar pestañas?

Sí. Cualquiera en el chat o canal puede eliminar las pestañas creadas por otros. Eliminar una pestaña no elimina ni afecta los datos en Business Central, pero la pestaña se eliminará para todos los usuarios en el chat o canal.

### <a name="if-i-cant-filter-will-i-still-see-a-filtered-list-that-was-created-by-others"></a><a name="if-i-cant-filter-will-i-still-see-a-filtered-list-that-was-created-by-others"></a>Si no puedo filtrar, ¿seguiré viendo una lista filtrada creada por otros?

Los usuarios que acceden a Business Central con su licencia de Microsoft 365 no tienen los derechos de uso para filtrar usando el panel de filtro o aplicar vistas de lista. Pero, si otro usuario ha creado una pestaña que contiene una página de lista filtrada, los usuarios de Microsoft 365 también verán los filtros aplicados a la pestaña.

---

## <a name="see-also"></a><a name="see-also"></a>Consulte también .

[Descripción general del acceso a Business Central con licencias de Microsoft 365](admin-access-with-m365-license.md#minimum-requirements)  
[Configurar acceso con licencias de Microsoft 365](admin-access-with-m365-license-setup.md)  
