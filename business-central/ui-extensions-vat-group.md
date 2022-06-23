---
title: La extensión de gestión de grupo de IVA para el Reino Unido
description: Puede interactuar con otras empresas para formar un grupo de IVA donde todos los miembros declaran el IVA en una sola declaración.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, value added tax, report
ms.search.forms: ''
ms.date: 05/24/2022
ms.author: bholtorf
ms.openlocfilehash: c5757a78a44e3cdc2f6100c42b5105734928837b
ms.sourcegitcommit: 7a6efcbae293c024ca4f6622c82886decf86c176
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/02/2022
ms.locfileid: "8841925"
---
# <a name="the-vat-group-management-extension-for-the-united-kingdom"></a>La extensión de gestión de grupo de IVA para el Reino Unido

Puede conectar una o más empresas de su país para combinar la declaración de IVA bajo un único número de registro. Este tipo de disposición se conoce como *Grupo de IVA*. Puede interactuar con el grupo como miembro o representante del grupo.

## <a name="forming-a-vat-group"></a>Formación de un grupo de IVA
Los miembros del grupo de IVA y el representante del grupo pueden utilizar la guía de configuración asistida de **Configuración de gestión de grupos de IVA** para definir su compromiso con el grupo y crear una conexión entre sus suscriptores de [!INCLUDE[prod_short](includes/prod_short.md)]. Los miembros del grupo utilizarán la conexión para enviar sus declaraciones de IVA al representante del grupo. El representante utilizará una única declaración de IVA para presentar el IVA a las autoridades fiscales para el grupo. 

## <a name="license-requirements"></a>Requisitos de licencia
Los participantes en el grupo deben tener licencia para usar [!INCLUDE[prod_short](includes/prod_short.md)]. No puede usar cuentas de invitado en grupos de IVA. 

* Para calcular y enviar declaraciones de IVA, un usuario debe ser un usuario completo de Business Central.
* Para iniciar sesión y realizar tareas básicas, como crear cuentas, puede tener la Licencia de miembro del equipo de Dynamics 365 Business Central.

## <a name="vat-group-constellations"></a>Constelaciones de grupos de IVA
La comunicación se produce entre los miembros del grupo y el representante. El representante del grupo expone una URL API que permite a los miembros enviar sus declaraciones de IVA al representante del grupo de IVA. 
[!INCLUDE[prod_short](includes/prod_short.md)] admite los envíos de declaraciones de IVA entre grupos para empresas que utilizan [!INCLUDE[prod_short](includes/prod_short.md)] localmente o en línea, y en cualquier combinación. La configuración de la comunicación depende de la constelación. Este artículo describe varias constelaciones grupales.

La siguiente lista muestra el orden recomendado de los pasos para configurar un grupo de IVA:

1. Cree la configuración en Azure Active Directory. Para obtener más información, consulte [Requisitos de autenticación](ui-extensions-vat-group.md#requirements-for-authentication).
2. Comparta la información técnica que los miembros del grupo de IVA y el representante necesitan para conectar sus suscriptores de [!INCLUDE[prod_short](includes/prod_short.md)]. Normalmente, el representante del grupo de IVA tiene esta información, como el nombre del entorno del representante del grupo de IVA al que los miembros del grupo de IVA enviarán el IVA.
3. Crear usuarios que los miembros del grupo de IVA puedan utilizar para autenticarse cuando se conecten al representante del grupo de IVA de [!INCLUDE[prod_short](includes/prod_short.md)]. Los usuarios deben tener licencias de usuario completas para [!INCLUDE[prod_short](includes/prod_short.md)].
4. Ejecute la guía de configuración asistida de **Configuración de gestión de grupos de IVA** para conectar a los miembros del grupo de IVA.

  La guía requiere cierta información del representante del grupo de IVA. Para obtener más información, consulte [Configuración de miembros del grupo de IVA](#set-up-vat-group-members). Tome nota del **Id. de miembro del grupo** para cada miembro del grupo de IVA. El representante necesita estos Id. para agregar las empresas al grupo de IVA.
5. Configure la extensión Gestión de grupo de IVA en [!INCLUDE[prod_short](includes/prod_short.md)] del representante del grupo de IVA, usando la guía de configuración asistida de **Configurar la gestión del grupo de IVA**. 

> [!NOTE]
> Para conectarse con el representante del grupo de IVA, los miembros del grupo deben tener una cuenta de usuario con acceso al [!INCLUDE[prod_short](includes/prod_short.md)] del representante del grupo de IVA. El representante del grupo de IVA debe crear al menos un usuario para esto, sin embargo, por razones de seguridad, se recomienda que cree un usuario para cada miembro del grupo de IVA. Asegúrese de distribuir las credenciales de estos usuarios a los miembros del grupo de IVA de forma segura. Esta es una cuenta de usuario del sistema que no está relacionada con una persona real.

## <a name="about-the-vat-group-management-setup"></a>Sobre la configuración de administración del grupo de IVA

El representante del grupo de IVA expone una API a los miembros del grupo. Los miembros usan la API para conectarse al suscriptor de [!INCLUDE[prod_short](includes/prod_short.md)] del representante y presentar declaraciones de IVA. Los miembros del grupo de IVA suelen utilizar [!INCLUDE[prod_short](includes/prod_short.md)] en suscriptores de Azure Active Directory separados. Por lo tanto, es necesario conectarse para establecer una conexión entre el miembro del grupo de IVA y el [!INCLUDE[prod_short](includes/prod_short.md)] del representante. 
  
Los miembros del grupo de IVA se conectan con el representante llamando a un servicio web en el suscriptor representante del grupo de IVA. La persona que llama debe estar autenticada mediante OAuth2. Cuando se configura la extensión Gestión del grupo de IVA, se le pedirá que se autentique ante el representante del grupo de IVA para obtener y guardar un token de acceso. Este token de acceso se utiliza al enviar declaraciones de IVA al representante del grupo de IVA. 

## <a name="construct-the-api-url"></a>Construya la URL de la API
1. En el centro de administración de Business Central para el arrendatario del representante, elija la pestaña **Entornos**.
2. En la sección **Detalles**, copie el **URL**.
3. Abra el Bloc de notas y pegue la URL. Reemplace **https://businesscentral.dynamics.com** con **https://api.businesscentral.dynamics.com/v2.0**.

## <a name="requirements-for-authentication"></a>Requisitos de autenticación 
> [!NOTE]
> Esto requiere las credenciales de una cuenta de administrador que tenga una licencia de usuario completa para [!INCLUDE[prod_short](includes/prod_short.md)].

Cuando el representante del grupo de IVA utiliza [!INCLUDE[prod_short](includes/prod_short.md)] en línea o local, los miembros del grupo de IVA deben utilizar Azure Active Directory para autenticar usuarios cuando envíen declaraciones de IVA al representante del grupo de IVA. Para [!INCLUDE[prod_short](includes/prod_short.md)] local, los miembros deben configurar el inicio de sesión único. Para obtener más información, consulte [Configurar Autenticación con servicios web de Azure Active Directory](/dynamics365/business-central/dev-itpro/administration/authenticating-users-with-azure-active-directory?tabs=singletenant%2Cadmintool). Si los miembros del grupo de IVA también utilizan [!INCLUDE[prod_short](includes/prod_short.md)] en línea, el miembro del grupo de IVA puede autenticarse utilizando las credenciales de usuario designadas y la información del punto final. Para obtener más información, consulte [Configuración de miembros del grupo de IVA](ui-extensions-vat-group.md#set-up-vat-group-members).

Los miembros del grupo de IVA que tienen [!INCLUDE[prod_short](includes/prod_short.md)] local deben configurar un registro de aplicación en Azure Active Directory para el suscriptor de [!INCLUDE[prod_short](includes/prod_short.md)] del representante del grupo de IVA. El registro de la aplicación permite que el [!INCLUDE[prod_short](includes/prod_short.md)] en línea del representante del grupo de IVA autentique al miembro del grupo. Para obtener más información, consulte [Inicio rápido: registrar una aplicación con la plataforma de identidad de Microsoft](/azure/active-directory/develop/quickstart-register-app).

Cuando crea el registro de la aplicación en Azure Active Directory, debe especificar la siguiente información.

* En la sección **Autenticación**, agregue **Web** como plataforma y utilice la siguiente **URL de redirección**: https://businesscentral.dynamics.com/OAuthLanding.htm.
* En la sección **Autenticación**, en la opción de seleccionar **Tipos de cuenta admitidos**, seleccione **Cuentas en cualquier directorio organizacional (Cualquier directorio de Azure AD, de varios suscriptores)**.
* En la sección **Certificados y secretos**, cree un nuevo secreto de cliente y anote el valor. Los miembros del grupo de IVA necesitarán el secreto al establecer la conexión con el representante del grupo.
* En la sección **Permisos de API**, agregue permisos a [!INCLUDE[prod_short](includes/prod_short.md)]. Habilite el acceso delegado a **Financials.ReadWrite.All** y **user_impersonation**.
* En la sección **Información general**, observe el **Id. de la aplicación (cliente)**. Los miembros del grupo de IVA necesitarán el Id. al establecer la conexión con el representante del grupo. 

## <a name="set-up-vat-group-members"></a>Configurar los miembros de grupos de IVA
> [!IMPORTANT]
> Las empresas miembro del grupo de IVA no necesitan conectarse a HMRC porque informan a través del representante del grupo.

Antes de comenzar, comuníquese con el representante del grupo de IVA para obtener la siguiente información sobre su suscriptor de [!INCLUDE[prod_short](includes/prod_short.md)]:

* La URL de la API
* El nombre de su empresa 
* Id. de cliente
* Secreto del cliente
* Credenciales de inicio de sesión para el usuario dedicado 

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") icono, escriba **Configuración de administración de servicios** y luego elija el enlace relacionado.
2. En el campo **Función de grupo de IVA**, especifique si es miembro del grupo o representante del mismo. Elija **Mimebro** para actuar como miembro del grupo y presentar sus declaraciones de IVA al representante del grupo en lugar de a las autoridades fiscales, y luego elegir **Siguiente**.
3. Copie el valor del campo **Id. de miembro del grupo** y luego compártalo con el representante del grupo de IVA para que puedan agregar su empresa como miembro aprobado del grupo.
4. En el campo **Versión del producto del representante del grupo**, especifique la versión de [!INCLUDE[prod_short](includes/prod_short.md)] que el representante está utilizando.
5. En el campo **Empresa representante del grupo**, introduzca el nombre de la empresa del representante del grupo de IVA. Por ejemplo, **UK Ltd CRONUS**.
6. En el campo **Tipo de autenticación**, elija **OAuth2**. Si el representante del grupo de IVA está utilizando [!INCLUDE[prod_short](includes/prod_short.md)] en línea, especifique que el **Representante de grupo utiliza Business Central Online** y luego elija **Siguiente**. Dependiendo de si el representante está usando [!INCLUDE[prod_short](includes/prod_short.md)] en línea o localmente, siga los pasos en las secciones [El representante del grupo de IVA utiliza Business Central Online](ui-extensions-vat-group.md#vat-group-representative-uses-business-central-online) o [El representante del grupo de IVA utiliza Business Central local](ui-extensions-vat-group.md#vat-group-representative-uses-business-central-on-premesis).

### <a name="vat-group-representative-uses-business-central-online"></a>Representante de grupo de IVA que usa Business Central Online
1. Escriba las credenciales de usuario proporcionadas por el representante del grupo de IVA y agregue los permisos necesarios.
2. Elija la configuración del informe de IVA que se está utilizando actualmente para enviar declaraciones de IVA a las autoridades fiscales. Después de completar la configuración, [!INCLUDE[prod_short](includes/prod_short.md)] creará una nueva configuración basada en esta elección y usará la configuración para enviar declaraciones de IVA al representante del grupo de IVA.  
3. Añada la **URL de API** del representante del grupo de IVA. Normalmente, la URL tiene el siguiente formato: `https://api.businesscentral.dynamics.com/v2.0/[TENANT-ID]/[ENVIRONMENTNAME]`. Por ejemplo, `https://api.businesscentral.dynamics.com/v2.0/907869c3-b252-4aca-b9cb-17a15d25477b/UKRepresentative`.

### <a name="vat-group-representative-uses-business-central-on-premesis"></a>Representante de grupo de IVA que usa Business Central local
1. En el campo **Identificación del cliente**, especifique el ID de cliente del registro de su aplicación en Azure Active Directory.
2. En el campo **Cliente Secreto**, especifique el cliente secreto del registro de su aplicación en Azure Active Directory.
3. En el campo **Punto de conexión de autoridad de OAuth 2.0** introduzca `https://login.microsoftonline.com/common/oauth2`.
4. En el campo **URL de recurso de OAuth 2.0**, introduzca `https://api.businesscentral.dynamics.com/`.
5. En el campo **URL de redirección de OAuth 2.0**, introduzca `https://businesscentral.dynamics.com/OAuthLanding.htm`.
6. Cuando haya especificado los distintos campos, elija **Siguiente** y, a continuación, introduzca las credenciales de usuario que le proporcionó el representante del grupo de IVA.
7. Elija la configuración de declaración de IVA que utiliza para declarar el IVA a las autoridades de su país.

## <a name="set-up-the-vat-group-representative"></a>Configurar el representante del grupo de IVA
> [!NOTE]
> Para local, admitimos solo una única instancia de inquilino del representante del grupo.

> [!IMPORTANT]
> La empresa representante debe habilitar la conexión de servicio **Configuración de IVA de HMRC** en la página **Conexiones de servicio**. Los representantes también deben descargar los períodos de devolución del IVA de HMRC.

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") icono, escriba **Configuración de administración de servicios** y luego elija el enlace relacionado.
2. En el campo **Función de grupo de IVA**, especifique si es miembro del grupo o representante del mismo. Elija **Representante** para actuar como representante del grupo en materia de IVA y presentar las declaraciones de IVA a las autoridades fiscales para el grupo, y luego elija **Siguiente**.
3. En el campo **Cuenta de liquidación de IVA**, especifique la cuenta que utiliza para liquidaciones de IVA.
4. En la **Casilla de IVA pendiente n.º** campo, especifique la casilla que representa el importe total del IVA adeudado por la presentación de un grupo de IVA.
5. En el campo **Libro diario general de liquidación de grupo**, especifique el libro diario general utilizado para el documento para contabilizar el IVA del grupo en la cuenta de liquidación.
6. El campo **Miembros aprobados** muestra el número de miembros del grupo que están configurados para enviar declaraciones de IVA al representante. Para agregar nuevos miembros, elija el número para abrir la página **Miembros aprobados**.
7. Para agregar nuevos miembros, agregue la siguiente información en la página **Miembros aprobados del grupo de IVA**:
    1. En el campo **ID de miembro del grupo**, introduzca un identificador para el miembro del grupo.
    2. En el campo **Nombre del miembro del grupo**, especifique el nombre del miembro del grupo. 
    3. En el campo **Empresa**, especifique la empresa desde la que el miembro del grupo presentará las declaraciones de IVA en [!INCLUDE[prod_short](includes/prod_short.md)]. Por ejemplo, **UK Ltd CRONUS**.
    4. Especifique los detalles de contacto de la empresa.

## <a name="use-the-vat-group-management-features"></a>Usar las características de gestión de grupos de IVA
Los miembros del grupo de IVA utilizan los procesos estándar para preparar declaraciones de IVA. La única diferencia es elegir la versión de la declaración **VATGROUP** que envía la declaración de IVA al representante del grupo de IVA en lugar de a las autoridades. Para obtener más información, consulte [Acerca de la declaración de devolución de IVA](finance-how-report-vat.md#vatreturn).

Las siguientes secciones describen las tareas que deben realizar los representantes de grupos de IVA.

### <a name="vat-group-submissions"></a>Envíos grupos de IVA

La página **Envíos de grupos de IVA** enumera las declaraciones de IVA que los miembros han presentado. La página sirve como una ubicación preliminar para los envíos hasta que el representante del grupo de IVA los incluya en una declaración de IVA para el grupo. Puede abrir las presentaciones para revisar el IVA de las casillas individuales declaradas por el miembro del grupo de IVA. 

> [!TIP]
> En la página **Períodos de devolución de IVA**, el campo **Declaraciones de miembros del grupo** muestra cuántas devoluciones han enviado los miembros. Para asegurarse de que este número está actualizado, elija la acción **Obtener devoluciones de IVA**.

### <a name="creating-a-group-vat-return"></a>Creación de una declaración de IVA de grupo

Para declarar el IVA en nombre del grupo, en la página **Devoluciones de IVA**, cree una declaración de IVA solo para su empresa. Luego, incluya las presentaciones de IVA más recientes de los miembros del grupo de IVA, seleccionando la acción **Incluir IVA de grupo**.  

Cuando la declaración de IVA del representante del grupo de IVA se haya presentado a las autoridades en nombre de todo el grupo, normalmente se ejecutará la acción **Calcular y contabilizar la liquidación del IVA**. Esta acción cierra los movimientos de IVA pendientes y transfiere los importes a la cuenta de liquidación de IVA. Actualmente, esta acción no tiene en cuenta los envíos de grupo. <!--Has this changed?--> Solo se contabilizarán los movimientos de IVA de la empresa representante del grupo de IVA. Los importes presentados por los miembros del grupo de IVA deben contabilizarse manualmente en el importe de liquidación del IVA, de modo que la cuenta de liquidación del IVA del representante del grupo de IVA refleje la responsabilidad de lo que se informó a las autoridades. Este comportamiento cambiará en una próxima actualización de [!INCLUDE[prod_short](includes/prod_short.md)], por lo que se liquidará todo el IVA del grupo (el importe total en las líneas de informe de la declaración de IVA). <!--Has this behavior changed?-->

> [!NOTE]
> Los miembros del grupo de IVA pueden corregir las declaraciones de IVA enviadas siempre que el representante del grupo no haya emitido la declaración de IVA del grupo. Para realizar una corrección, el miembro del grupo de IVA debe crear una nueva declaración de IVA para el período de devolución de IVA y enviarla al representante del grupo de IVA. En el lado del representante del grupo de IVA, la última declaración de IVA se incluirá en la página **Declaraciones de IVA**. 

> [!IMPORTANT]
> La funcionalidad del grupo de IVA solo se admite en aquellos mercados en los que [!INCLUDE[prod_short](includes/prod_short.md)] utiliza un marco de IVA que consta de declaraciones de IVA y períodos de devolución de IVA. No puede utilizar grupos de IVA en otros mercados que tengan otras implementaciones de informes de IVA locales, como Austria, Alemania, Italia, España y Suiza. 

## <a name="see-also"></a>Consulte también
[Funcionalidad local del Reino Unido en la versión británica](LocalFunctionality/unitedkingdom/united-kingdom-local-functionality.md)  
[Crear impuestos digitales en el Reino Unido](LocalFunctionality/UnitedKingdom/making-tax-digital-submit-vat-return.md)  
[Trabajar con el IVA por ventas y compras](finance-work-with-vat.md)  
[Configurar el impuesto sobre el valor añadido](finance-setup-vat.md)  
[Trabajar con el IVA por ventas y compras](finance-work-with-vat.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
