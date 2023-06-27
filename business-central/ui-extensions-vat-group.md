---
title: La extensión de gestión de grupo de IVA para el Reino Unido
description: Puede interactuar con otras empresas para formar un grupo de IVA donde todos los miembros declaran el IVA en una sola declaración.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'VAT, value added tax, report'
ms.search.form: '4700, 4701, 4703, 4704, 4705, 4706, 4707, 4708, 4709,'
ms.date: 07/08/2022
ms.author: bholtorf
---

# <a name="the-vat-group-management-extension-for-the-united-kingdom"></a><a name="the-vat-group-management-extension-for-the-united-kingdom"></a>La extensión de gestión de grupo de IVA para el Reino Unido

Puede conectar una o más empresas en el Reino Unido para combinar la declaración del impuesto sobre el valor añadido (IVA) bajo un único número de registro. Este tipo de disposición se conoce como *Grupo de IVA*. Puede interactuar con el grupo como miembro o representante del grupo.

## <a name="forming-a-vat-group"></a><a name="forming-a-vat-group"></a>Formación de un grupo de IVA

Los miembros del grupo de IVA y el representante del grupo pueden utilizar la guía de configuración asistida de **Configuración de gestión de grupos de IVA** para definir su compromiso con el grupo y crear una conexión entre sus suscriptores de [!INCLUDE[prod_short](includes/prod_short.md)]. Los miembros del grupo utilizan esta conexión para enviar sus declaraciones de IVA al representante del grupo. El representante utilizará una única declaración de IVA para presentar el IVA a las autoridades fiscales para el grupo.

[!INCLUDE[prod_short](includes/prod_short.md)] admite la presentación de declaraciones de IVA intragrupo para las empresas que utilizan [!INCLUDE[prod_short](includes/prod_short.md)] en las instalaciones o en línea, en cualquier combinación, lo que influye en la configuración de la comunicación entre las empresas. Este artículo describe varias configuraciones grupales.

### <a name="license-requirements"></a><a name="license-requirements"></a>Requisitos de licencia

Los participantes en el grupo deben tener licencia para usar [!INCLUDE[prod_short](includes/prod_short.md)]. No puede usar cuentas de invitado en grupos de IVA.

* Para calcular y enviar declaraciones de IVA, un usuario debe ser un usuario completo de [!INCLUDE[prod_short](includes/prod_short.md)].
* Para iniciar sesión y realizar tareas básicas, como crear cuentas, necesita una Licencia de miembro del equipo de [!INCLUDE[prod_long](includes/prod_long.md)].

## <a name="set-up-a-vat-group"></a><a name="set-up-a-vat-group"></a>Configurar un grupo de IVA

El siguiente es el orden recomendado de los pasos que un administrador utiliza para configurar un grupo de IVA:

1. Cree la configuración en [Azure Active Directory para los miembros del grupo](#azure-active-directory-setup-for-group-members).
2. Comparta la información técnica que los miembros del grupo de IVA y el representante del grupo necesitan para conectar sus suscriptores de [!INCLUDE[prod_short](includes/prod_short.md)]. Normalmente, el representante del grupo dispone de esta información, como la [URL de API](#group-api-setup) y el nombre del entorno del representante del grupo de IVA al que los miembros del grupo de IVA envían sus datos de IVA.
3. Crear usuarios que los miembros del grupo de IVA utilizarán para autenticarse cuando se conecten al representante del grupo de IVA de [!INCLUDE[prod_short](includes/prod_short.md)]. Los usuarios deben tener licencias de usuario completas para [!INCLUDE[prod_short](includes/prod_short.md)].
4. Ejecute la guía de configuración asistida de **Configuración de gestión de grupos de IVA** para conectar a los miembros del grupo de IVA.

   El representante del grupo de IVA debe suministrar cierta información a los miembros del grupo para completar su configuración. (Obtenga más información en la sección [Configurar los miembros de grupos de IVA](#set-up-vat-group-members) a continuación.) Anote el **ID de miembro del grupo** para cada miembro del grupo de IVA. El representante del grupo necesita estos Id. para agregar las empresas al grupo de IVA.
5. Configure la extensión Gestión de grupo de IVA en [!INCLUDE[prod_short](includes/prod_short.md)] del representante del grupo de IVA, usando la guía de configuración asistida de **Configurar la gestión del grupo de IVA**.

> [!NOTE]
> Para conectarse con el representante del grupo de IVA, los miembros del grupo deben tener una cuenta de usuario con acceso al [!INCLUDE[prod_short](includes/prod_short.md)] del representante del grupo de IVA. El representante del grupo de IVA debe crear al menos un usuario para esto. Sin embargo, por razones de seguridad, les recomendamos que creen un usuario para cada miembro del grupo de IVA, que puede ser una cuenta de usuario del sistema que no esté relacionada con una persona real. Asegúrese de distribuir las credenciales de usuario a los miembros del grupo de IVA de forma segura.

### <a name="azure-active-directory-setup-for-group-members"></a><a name="azure-active-directory-setup-for-group-members"></a>Configuración de Azure Active Directory para miembros del grupo

Cuando el representante del grupo de IVA utiliza [!INCLUDE[prod_short](includes/prod_short.md)] en línea o local, los miembros del grupo de IVA deben utilizar Azure Active Directory para autenticar usuarios cuando envíen declaraciones de IVA al representante del grupo de IVA. Para [!INCLUDE[prod_short](includes/prod_short.md)] local, los miembros deben configurar el inicio de sesión único. Obtenga más información en [Configurar Autenticación con servicios web de Azure Active Directory](/dynamics365/business-central/dev-itpro/administration/authenticating-users-with-azure-active-directory?tabs=singletenant%2Cadmintool).

Si los miembros del grupo de IVA también utilizan [!INCLUDE[prod_short](includes/prod_short.md)] en línea, el miembro puede autenticarse con las credenciales de usuario designadas y la información de inicio de sesión proporcionada por el representante del grupo. Obtenga más información en la sección [Configurar los miembros de grupos de IVA](#set-up-vat-group-members) a continuación.

Los miembros del grupo de IVA que tienen [!INCLUDE[prod_short](includes/prod_short.md)] local deben configurar un registro de aplicación en Azure Active Directory para el suscriptor de [!INCLUDE[prod_short](includes/prod_short.md)] del representante del grupo de IVA. El registro de la aplicación permite que el [!INCLUDE[prod_short](includes/prod_short.md)] en línea del representante del grupo de IVA autentique al miembro del grupo. Obtenga más información en [Inicio rápido: registrar una aplicación con la plataforma de identidad de Microsoft](/azure/active-directory/develop/quickstart-register-app).

Cuando el administrador del miembro del grupo de IVA crea el registro de la aplicación en Azure Active Directory, debe especificar la siguiente información.

* En la sección **Autenticación**, agregue **Web** como plataforma y utilice la siguiente **URL de redirección**: `https://businesscentral.dynamics.com/OAuthLanding.htm`.
* En la sección **Autenticación**, en la opción de seleccionar **Tipos de cuenta admitidos**, seleccione **Cuentas en cualquier directorio organizacional (Cualquier directorio de Azure AD, de varios suscriptores)**.
* En la sección **Certificados y secretos**, cree un nuevo secreto de cliente y anote el valor. Los miembros del grupo de IVA necesitarán el secreto al establecer la conexión con el representante del grupo.
* En la sección **Permisos de API**, agregue permisos a [!INCLUDE[prod_short](includes/prod_short.md)]. Habilite el acceso delegado a **Financials.ReadWrite.All** y **user_impersonation**.
* En la sección **Información general**, observe el **Id. de la aplicación (cliente)**. Los miembros del grupo de IVA necesitarán el Id. al establecer la conexión con el representante del grupo.

### <a name="group-api-setup"></a><a name="group-api-setup"></a>Configuración del grupo de API

El representante del grupo de IVA crea y suministra una API a los miembros del grupo. Los miembros usan esta API para conectarse al suscriptor de [!INCLUDE[prod_short](includes/prod_short.md)] del representante y presentar declaraciones de IVA. Los miembros del grupo de IVA suelen utilizar [!INCLUDE[prod_short](includes/prod_short.md)] en suscriptores de Azure Active Directory separados. Por ese motivo, es necesario conectarse para establecer una conexión entre el miembro del grupo de IVA y el [!INCLUDE[prod_short](includes/prod_short.md)] del representante.

> [!NOTE]
> Esta configuración requiere las credenciales de una cuenta de administrador que tenga una licencia de usuario completa para [!INCLUDE[prod_short](includes/prod_short.md)].

1. En el centro de administración de Business Central para el arrendatario del representante, elija la pestaña **Entornos**.
1. Elija el entorno del representante.
1. En la sección **Detalles**, copie el **URL**.
1. Abra el Bloc de notas y pegue la URL. Reemplace `https://businesscentral.dynamics.com` con `https://api.businesscentral.dynamics.com/v2.0`.

## <a name="set-up-vat-group-members"></a><a name="set-up-vat-group-members"></a>Configurar los miembros de grupos de IVA

Los miembros del grupo de IVA se conectan con el representante llamando a un servicio web en el suscriptor representante del grupo de IVA. La persona que llama debe estar autenticada mediante OAuth2. Cuando se configura la extensión de gestión del grupo de IVA, se pide a los miembros que se autentiquen ante el representante del grupo de IVA, durante lo cual se genera y guarda un token de acceso. Este token de acceso se utiliza al enviar declaraciones de IVA al representante del grupo de IVA.

> [!IMPORTANT]
> Las empresas miembro del grupo de IVA no necesitan conectarse a HMRC porque informan a través del representante del grupo.

Antes de que los miembros del grupo de IVA comiencen su configuración (enumerada a continuación), deben ponerse en contacto con el representante del grupo de IVA para obtener la siguiente información sobre su suscriptor de [!INCLUDE[prod_short](includes/prod_short.md)]:

* La URL de la API
* El nombre de su empresa
* Credenciales de inicio de sesión para el usuario dedicado

1. En la esquina superior derecha, elija **Configuración** ![Configuración.](media/ui-experience/settings_icon_small.png "Icono de configuración para el área de trabajo") , y luego elija la acción **Configuración asistida**.
2. Elija la acción **Configuración de gestión de grupos de IVA**.
3. En el campo **Función de grupo de IVA**, elija **Miembro** y, a continuación, **Siguiente**.
4. Copie el valor del campo **Id. de miembro del grupo** y luego compártalo con el representante del grupo de IVA para que puedan agregar su empresa como miembro aprobado del grupo.
5. En el campo **Versión del producto del representante del grupo**, especifique la versión de [!INCLUDE[prod_short](includes/prod_short.md)] que el representante está utilizando.
6. En el campo **URL de la API**, introduzca la URL de la API proporcionado por el representante del grupo de IVA. Normalmente, la URL tiene el siguiente formato: `https://api.businesscentral.dynamics.com/v2.0/[TENANT-ID]/[ENVIRONMENTNAME]`. Por ejemplo, `https://api.businesscentral.dynamics.com/v2.0/907869c3-b252-4aca-b9cb-17a15d25477b/UKRepresentative`.
7. En el campo **Empresa representante del grupo**, introduzca el nombre de la empresa del representante del grupo de IVA, como **CRONUS UK Ltd**.
8. En el campo **Tipo de autenticación**, elija **OAuth2**. Si el representante del grupo de IVA está utilizando [!INCLUDE[prod_short](includes/prod_short.md)] en línea, habilite el botón de alternancia **Representante de grupo utiliza Business Central Online** y luego elija **Siguiente**.

   A continuación, siga los pasos de la sección [Representante de grupo de IVA que usa Business Central Online](ui-extensions-vat-group.md#vat-group-representative-uses-business-central-online) o [Representante de grupo de IVA que usa Business Central local](ui-extensions-vat-group.md#vat-group-representative-uses-business-central-on-premises) a continuación.

### <a name="vat-group-representative-uses-business-central-online"></a><a name="vat-group-representative-uses-business-central-online"></a>Representante de grupo de IVA que usa Business Central Online

1. Escriba las credenciales de usuario proporcionadas por el representante del grupo de IVA y agregue los permisos necesarios para generar el token de acceso.
2. Elija la configuración del informe de IVA que utiliza para enviar declaraciones de IVA a las autoridades fiscales del Reino Unido. 

Después de completar la configuración, [!INCLUDE[prod_short](includes/prod_short.md)] creará una nueva configuración basada en esta elección que le permite enviar declaraciones de IVA al representante del grupo de IVA.

### <a name="vat-group-representative-uses-business-central-on-premises"></a><a name="vat-group-representative-uses-business-central-on-premises"></a>Representante de grupo de IVA que usa Business Central local

1. Introduzca las credenciales de usuario proporcionadas por el representante del grupo de IVA y elija **Siguiente**.
2. En el campo **Identificación del cliente**, especifique el ID de cliente del registro de su aplicación en [Azure Active Directory](#azure-active-directory-setup-for-group-members).
3. En el campo **Cliente Secreto**, especifique el cliente secreto del registro de su aplicación en Azure Active Directory.
4. En el campo **Punto de conexión de autoridad de OAuth 2.0** introduzca `https://login.microsoftonline.com/common/oauth2`.
5. En el campo **URL de recurso de OAuth 2.0**, introduzca `https://api.businesscentral.dynamics.com/`.
6. En el campo **URL de redirección de OAuth 2.0**, introduzca `https://businesscentral.dynamics.com/OAuthLanding.htm`.
7. Cuando haya especificado los distintos campos, elija **Siguiente** y, a continuación, confirme la conexión de autenticación para generar el token de acceso.
8. Elija la configuración del informe de IVA que utiliza para enviar declaraciones de IVA a las autoridades fiscales del Reino Unido.

## <a name="set-up-the-vat-group-representative"></a><a name="set-up-the-vat-group-representative"></a>Configurar el representante del grupo de IVA

> [!NOTE]
> Para local, [!INCLUDE[prod_short](includes/prod_short.md)] admite solo una única instancia de inquilino del representante del grupo.

> [!IMPORTANT]
> La empresa representante debe habilitar la conexión de servicio **Configuración de IVA de HMRC** en la página **Conexiones de servicio**. Los representantes también deben descargar los períodos de devolución del IVA de HMRC.

1. En la esquina superior derecha, elija el icono **Configuración** ![Configuración.](media/ui-experience/settings_icon_small.png "Icono de configuración para el área de trabajo") y, a continuación, elija la acción **Configuración asistida**.
2. Elija la acción **Configuración de gestión de grupos de IVA**.
3. En el campo **Función de grupo de IVA**, elija **Representante** para actuar como representante del grupo de IVA y, a continuación, elija **Siguiente**.
4. En el campo **Cuenta liquidación grupo** especifique la cuenta de liquidación utilizada para los importes del impuesto del IVA de los miembros del grupo. Esta cuenta debe tener **Activos** como **Categoría de cuenta**.
5. En el campo **Cuenta de liquidación de IVA**, especifique la cuenta que utiliza para liquidaciones de IVA. Esta cuenta debe tener **Pasivos** como **Categoría de cuenta**.
6. En la **Casilla de IVA pendiente n.º** , especifique la casilla que representa el importe total del IVA adeudado por la presentación de un grupo de IVA.
7. En el campo **Libro diario general de liquidación de grupo**, especifique el libro general diario utilizado para crear el documento con el que el representante del grupo contabiliza el IVA del grupo en la cuenta de liquidación.
8. El campo **Miembros aprobados** muestra el número de miembros del grupo que están configurados para enviar declaraciones de IVA al representante del grupo. Para agregar nuevos miembros, elija el número para abrir la página de **Miembros aprobados del grupo de IVA** y agregue la siguiente información:
    1. En el campo **ID de miembro del grupo** introduzca un identificador para el miembro del grupo, tal y como se muestra durante la configuración de los miembros del grupo (obtenga más información en la sección [Configuración de miembros del grupo de IVA](#set-up-vat-group-members) de más arriba).
    2. En el campo **Nombre del miembro del grupo**, especifique el nombre del miembro del grupo.
    3. En el campo **Empresa**, especifique la empresa de la que el miembro del grupo presentará las declaraciones de IVA en [!INCLUDE[prod_short](includes/prod_short.md)], como **CRONUS UK Ltd**.
    4. Especifique los detalles de contacto de la empresa.

## <a name="use-the-vat-group-management-features"></a><a name="use-the-vat-group-management-features"></a>Usar las características de gestión de grupos de IVA

Los miembros del grupo de IVA utilizan los procesos estándar para preparar declaraciones de IVA. La única diferencia es que los miembros deben elegir la versión de informe **VATGROUP** en la página **Devolución de IVA** para presentar la declaración de IVA al representante del grupo de IVA en lugar de a las autoridades. Obtenga más información en [Acerca del informe de devolución de IVA](finance-how-report-vat.md#vatreturn).

> [!NOTE]
> Los miembros del grupo de IVA pueden corregir las declaraciones de IVA enviadas siempre que el representante del grupo no haya emitido la declaración de IVA del grupo. Para realizar una corrección, el miembro del grupo de IVA debe crear una nueva declaración de IVA para el período de devolución de IVA y enviarla al representante del grupo de IVA. En el lado del representante del grupo de IVA, la última declaración de IVA del miembro reemplazará la anterior y se incluirá en la página **Declaraciones de IVA**.

Las siguientes secciones describen las tareas que deben realizar los representantes de grupos de IVA para presentar la declaración de IVA del grupo.

### <a name="review-vat-member-submissions"></a><a name="review-vat-member-submissions"></a>Revisar envíos de miembros de IVA

La página **Envíos de grupos de IVA** enumera las declaraciones de IVA que los miembros han presentado. La página sirve como una ubicación preliminar para los envíos hasta que el representante del grupo de IVA los incluya en una declaración de IVA para el grupo. El representante puede abrir los envíos para revisar las casillas individuales que contienen el importe declarado por cada miembro del grupo del IVA.

> [!TIP]
> En la página **Períodos de devolución de IVA**, el campo **Declaraciones de miembros del grupo** muestra cuántas devoluciones han enviado los miembros. Para asegurarse de que este número está actualizado, elija la acción **Obtener devoluciones de IVA**.

### <a name="create-a-group-vat-return"></a><a name="create-a-group-vat-return"></a>Creación de una declaración de IVA de grupo

Para declarar el IVA en nombre del grupo, en la página **Devoluciones de IVA**, cree una declaración de IVA solo para su empresa. Luego, incluya las presentaciones de IVA más recientes de los miembros del grupo de IVA, seleccionando la acción **Incluir IVA de grupo**.  

Cuando el representante del grupo ha enviado la declaración de IVA del grupo a las autoridades, el representante ejecuta normalmente la acción **Calcular y registrar liquidación de IVA**. Esta acción cierra los movimientos de IVA pendientes y transfiere los importes a la cuenta de liquidación de IVA. Actualmente, esta acción no tiene en cuenta los envíos de grupo. Solo se contabilizan los movimientos de IVA de la empresa representante del grupo de IVA. Los importes presentados por los miembros del grupo de IVA deben contabilizarse manualmente en el importe de liquidación del IVA, de modo que la cuenta de liquidación del IVA del representante del grupo de IVA refleje la responsabilidad de lo que se informó a las autoridades. Este comportamiento cambiará en una próxima actualización de [!INCLUDE[prod_short](includes/prod_short.md)], por lo que se liquida todo el IVA del grupo (el importe total en las líneas de informe de la declaración de IVA).

> [!IMPORTANT]
> La funcionalidad del grupo de IVA solo se admite en aquellos mercados en los que [!INCLUDE[prod_short](includes/prod_short.md)] utiliza un marco de IVA que consta de declaraciones de IVA y períodos de devolución de IVA. No puede utilizar grupos de IVA en otros mercados con otras implementaciones de informes de IVA locales, como Austria, Alemania, Italia, España y Suiza.

## <a name="see-also"></a><a name="see-also"></a>Consulte también .

[Funcionalidad local del Reino Unido en la versión británica](LocalFunctionality/unitedkingdom/united-kingdom-local-functionality.md)  
[Crear impuestos digitales en el Reino Unido](LocalFunctionality/UnitedKingdom/making-tax-digital-submit-vat-return.md)  
[Trabajar con el IVA por ventas y compras](finance-work-with-vat.md)  
[Configurar el impuesto sobre el valor añadido](finance-setup-vat.md)  
[Trabajar con el IVA por ventas y compras](finance-work-with-vat.md)  
[Consolidar los datos financieros de varias empresas](finance-consolidated-company-reporting.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
