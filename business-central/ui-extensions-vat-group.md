---
title: Extensión Gestión de grupo de IVA | Microsoft Docs
description: Puede interactuar con otras empresas para formar un grupo de IVA y actuar como miembro o representante del grupo al declarar el IVA.
author: bholtorf
manager: annbe
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: VAT, value added tax, report
ms.date: 10/06/2020
ms.author: bholtorf
ms.openlocfilehash: 5dfadee976ce39e7d7ead2c09d907050682b4a7f
ms.sourcegitcommit: 4bca699d2a5ce182eb5572d72fac4fb478c4f293
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/12/2020
ms.locfileid: "3989420"
---
# <a name="the-vat-group-management-extension"></a>Extensión Gestión de grupo de IVA

Puede unirse a una o más empresas de su país para consolidar la declaración de IVA bajo un único número de registro. Este tipo de disposición se conoce como *Grupo de IVA*. Puede interactuar con el grupo como miembro o representante del grupo.

## <a name="forming-a-vat-group"></a>Formación de un grupo de IVA
Los miembros del grupo de IVA y el representante del grupo pueden utilizar la guía de configuración asistida de **Configuración de gestión de grupos de IVA** para definir su compromiso con el grupo y crear una conexión entre sus suscriptores de [!INCLUDE[d365fin](includes/d365fin_md.md)]. Los miembros del grupo utilizarán la conexión para enviar sus declaraciones de IVA al representante del grupo. El representante presentará el IVA a las autoridades fiscales en nombre del grupo mediante una única declaración de IVA. 

## <a name="vat-group-constellations"></a>Constelaciones de grupos de IVA
La comunicación se produce entre los miembros del grupo y el representante. El representante del grupo expone una API que permite a los miembros enviar sus declaraciones de IVA al representante del grupo de IVA. 
[!INCLUDE[d365fin](includes/d365fin_md.md)] admite los envíos de declaraciones de IVA entre grupos para empresas que utilizan [!INCLUDE[d365fin](includes/d365fin_md.md)] localmente o en línea, y en cualquier combinación. La configuración de la comunicación depende de la constelación. Las siguientes secciones describen cómo configurar varias constelaciones de grupos.

La siguiente lista muestra el orden recomendado de los pasos para configurar un grupo de IVA:

1. Cree la configuración en Azure Active Directory. Para obtener más información, consulte [Requisitos de autenticación](ui-extensions-vat-group.md#requirements-for-authentication).
2. Comparta la información técnica que los miembros del grupo de IVA y el representante necesitan para conectar sus suscriptores de [!INCLUDE[d365fin](includes/d365fin_md.md)].

  Normalmente, el representante del grupo de IVA tiene esta información, como el nombre del entorno del representante del grupo de IVA al que los miembros del grupo de IVA enviarán el IVA.
3. Cree usuarios en [!INCLUDE[d365fin](includes/d365fin_md.md)] del representante del grupo de IVA que los miembros del grupo de IVA pueden utilizar para autenticarse y conectarse.
4. Ejecute la guía de configuración asistida de **Configuración de gestión de grupos de IVA** para conectar a los miembros del grupo de IVA.

  La guía requiere cierta información del representante del grupo de IVA. Para obtener más información, consulte la sección [Configuración de miembros del grupo de IVA](#vat-group-member-setup). Tome nota del **Id. de miembro del grupo** para cada miembro del grupo de IVA. El representante necesita estos Id. para agregar las empresas al grupo de IVA.
5. Configure la extensión Gestión de grupo de IVA en [!INCLUDE[d365fin](includes/d365fin_md.md)] del representante del grupo de IVA, usando la guía de configuración asistida de **Configurar la gestión del grupo de IVA**. 

> [!NOTE]
> Para conectarse con el representante del grupo de IVA, los miembros del grupo necesitan un usuario con acceso al [!INCLUDE[d365fin](includes/d365fin_md.md)] del representante del grupo de IVA. El representante del grupo de IVA debe crear al menos un usuario para esto, sin embargo, por razones de seguridad, se recomienda que cree un usuario para cada miembro del grupo de IVA. Asegúrese de distribuir las credenciales de estos usuarios a los miembros del grupo de IVA de forma segura.

## <a name="understanding-the-vat-group-management-setup"></a>Conocimiento de la configuración de administración del grupo de IVA

El representante del grupo de IVA expone una API que los miembros del grupo de IVA pueden utilizar para conectarse a sus suscriptores de [!INCLUDE[d365fin](includes/d365fin_md.md)] y enviar declaraciones de IVA. Los miembros del grupo de IVA suelen utilizar [!INCLUDE[d365fin](includes/d365fin_md.md)] en suscriptores de Azure Active Directory separados. Por lo tanto, se necesita más configuración para establecer una conexión entre el miembro del grupo de IVA y el [!INCLUDE[d365fin](includes/d365fin_md.md)] del representante. 
  
Los miembros del grupo de IVA se conectan con el representante llamando a un servicio web en el suscriptor representante del grupo de IVA. La persona que llama debe estar autenticada mediante OAuth. Cuando se configura la extensión Gestión del grupo de IVA, se le pedirá que se autentique ante el representante del grupo de IVA para obtener y guardar un token de acceso. Este token de acceso se utiliza al enviar declaraciones de IVA al representante del grupo de IVA. 

La autenticación la maneja Azure Active Directory, por lo que su configuración debe realizarse en Azure Active Directory del representante del grupo de IVA para permitir conexiones. Debe configurarse un registro de la aplicación Azure Active Directory con acceso al [!INCLUDE[d365fin](includes/d365fin_md.md)] del representante del grupo de IVA. Esto también es cierto si el representante del grupo de IVA utiliza [!INCLUDE[d365fin](includes/d365fin_md.md)] local. Además, debe configurar el inicio de sesión único si el representante del grupo de IVA utiliza [!INCLUDE[d365fin](includes/d365fin_md.md)] local.

> [!NOTE]
> Durante un tiempo limitado, también se admite la autenticación mediante una clave de acceso al servicio web. Para más información, consulte [Funciones obsoletas en el lanzamiento de versiones 1 de 2021](/dynamics365/business-central/dev-itpro/upgrade/deprecated-features-w1#deprecated-features-in-2021-release-wave-1).

## <a name="requirements-for-authentication"></a>Requisitos de autenticación 
Cuando el representante del grupo de IVA utiliza [!INCLUDE[d365fin](includes/d365fin_md.md)] en línea o local, los miembros del grupo de IVA utilizan Azure Active Directory para autenticarse cuando envíen declaraciones de IVA al representante del grupo de IVA. Si los miembros del grupo de IVA también utilizan [!INCLUDE[d365fin](includes/d365fin_md.md)] en línea, el miembro del grupo de IVA puede autenticarse utilizando las credenciales de usuario designadas y la información del punto final. Para obtener más información, consulte [Configuración de miembros del grupo de IVA](ui-extensions-vat-group.md#vat-group-member-setup).

Los miembros del grupo de IVA que tienen [!INCLUDE[d365fin](includes/d365fin_md.md)] local deben configurar un registro de aplicación en Azure Active Directory para el suscriptor de [!INCLUDE[d365fin](includes/d365fin_md.md)] del representante del grupo de IVA. El registro de la aplicación permitirá que el [!INCLUDE[d365fin](includes/d365fin_md.md)] en línea del representante del grupo de IVA autentique al miembro del grupo. Para obtener más información, consulte [Inicio rápido: registrar una aplicación con la plataforma de identidad de Microsoft](/azure/active-directory/develop/quickstart-register-app).

Cuando crea el registro de la aplicación en Azure Active Directory, debe especificar lo siguiente.

* En la sección **Autenticación**, agregue **Web** como plataforma y utilice la siguiente **URL de redirección**: https://businesscentral.dynamics.com/OAuthLanding.htm.
* En la sección **Autenticación**, en la opción de seleccionar **Tipos de cuenta admitidos**, seleccione **Cuentas en cualquier directorio organizacional (Cualquier directorio de Azure AD, de varios suscriptores)**.
* En la sección **Certificados y secretos**, cree un nuevo secreto de cliente y anote el valor. Los miembros del grupo de IVA necesitarán el secreto al establecer la conexión con el representante del grupo.
* En la sección **Permisos de API**, agregue permisos a [!INCLUDE[d365fin](includes/d365fin_md.md)]. Habilite el acceso delegado a **Financials.ReadWrite.All** y **user_impersonation**.
* En la sección **Información general**, observe el **Id. de la aplicación (cliente)**. Los miembros del grupo de IVA necesitarán el Id. al establecer la conexión con el representante del grupo. 

## <a name="vat-group-member-setup"></a>Configuración de miembros del grupo de IVA
Configure al miembro del grupo de IVA iniciando la guía de configuración asistida de **Configuración de gestión de grupos de IVA**. 

> [!NOTE]
> Antes de comenzar, comuníquese con el representante del grupo de IVA para obtener la siguiente información sobre su suscriptor de [!INCLUDE[d365fin](includes/d365fin_md.md)]:
>
> * La URL de la API
> * El nombre de su empresa 
> * Id. de cliente
> * Secreto del cliente
> * Credenciales de inicio de sesión para el usuario dedicado 

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Grupo de IVA** y luego elija el vínculo relacionado.
2. Para definir el rol del grupo de IVA de la empresa, seleccione **Miembro** y luego elija **Siguiente**.
3. Copie el valor del campo **Id. de miembro del grupo** y luego compártalo con el representante del grupo de IVA para que puedan agregar su empresa como miembro aprobado del grupo.
4. Añada la **URL de API** del representante del grupo de IVA. Normalmente, la URL tiene el siguiente formato: `https://api.businesscentral.dynamics.com/v2.0/[TENANT-ID]/[ENVIRONMENTNAME]`. Por ejemplo, `https://api.businesscentral.dynamics.com/v2.0/907869c3-b252-4aca-b9cb-17a15d25477b/UKRepresentative`. 
5. Agregue el [!INCLUDE[d365fin](includes/d365fin_md.md)] nombre de la empresa del representante del grupo de IVA, como *CRONUS UK Ltd*.
6. Escoja **Tipo de autenticación**, escoja **OAuth2** y luego elija **Siguiente**.
7. En el campo **Id. de cliente**, introduzca el Id. proporcionado por el representante del grupo de IVA.
8. En el campo **Secreto de cliente proporcionado por el representante del grupo de IVA**, introduzca el secreto proporcionado por el representante del grupo de IVA.
9. En el campo **Extremo de autoridad OAuth 2.0**, introduzca *https://login.microsoftonline.com/common/oauth2*.
10. En el campo **URL de recurso de OAuth 2.0**, introduzca *https://api.businesscentral.dynamics.com/*.
11. En el campo **URL de redirección de OAuth 2.0**, introduzca *https://businesscentral.dynamics.com/OAuthLanding.htm*. 
12. Cuando haya especificado los distintos campos, elija **Siguiente** y, a continuación, introduzca las credenciales de usuario que le proporcionó el representante del grupo de IVA.
13. Elija la configuración de declaración de IVA que utiliza para declarar el IVA a las autoridades de su país.

  Por ejemplo, en el Reino Unido, la configuración de la declaración de IVA se configuraría para declarar el IVA a HMRC. La extensión Gestión del grupo de IVA copia esta configuración, pero reemplaza la codeunit de envío por una que admita el envío al representante del grupo de IVA en lugar de a las autoridades fiscales. Microsoft proporciona la codeunit. Cuando haya concluido, elija **Siguiente**.

## <a name="using-the-vat-group-management-features"></a>Uso de las características de gestión de grupos de IVA

Los miembros del grupo de IVA utilizan los procesos estándar para preparar declaraciones de IVA. La única diferencia es elegir la versión de la declaración **VATGROUP** que envía la declaración de IVA al representante del grupo de IVA en lugar de a las autoridades. Para obtener más información, consulte [Acerca de la declaración de devolución de IVA](/business-central/finance-how-report-vat#about-the-vat-return-report).

Las siguientes secciones describen las tareas que deben realizar los representantes de grupos de IVA.

### <a name="vat-group-submissions"></a>Envíos de grupos de IVA

La página **Envíos de grupos de IVA** enumera las declaraciones de IVA que los miembros han presentado. La página sirve como una ubicación preliminar para los envíos hasta que el representante del grupo de IVA los incluya en una declaración de IVA para el grupo. Puede abrir las presentaciones para revisar el IVA de las casillas individuales declaradas por el miembro del grupo de IVA.

### <a name="creating-a-group-vat-return"></a>Creación de una declaración de IVA de grupo

Para declarar el IVA en nombre del grupo, en la página **Devoluciones de IVA**, cree una declaración de IVA solo para su empresa. Luego, incluya las presentaciones de IVA más recientes de los miembros del grupo de IVA, seleccionando la acción **Incluir IVA de grupo**.  

Cuando la declaración de IVA del representante del grupo de IVA se haya presentado a las autoridades en nombre de todo el grupo, normalmente se ejecutará la acción **Calcular y contabilizar la liquidación del IVA**. Esta acción cierra los movimientos de IVA pendientes y transfiere los importes a la cuenta de liquidación de IVA. Actualmente, esta acción no tiene en cuenta los envíos de grupo. Esto significa que solo se contabilizarán los movimientos de IVA de la empresa representante del grupo de IVA. Los importes presentados por los miembros del grupo de IVA deben contabilizarse manualmente en el importe de liquidación del IVA, de modo que la cuenta de liquidación del IVA del representante del grupo de IVA refleje la responsabilidad de lo que se informó a las autoridades. Este comportamiento cambiará en una próxima actualización de [!INCLUDE[d365fin](includes/d365fin_md.md)], por lo que se liquidará todo el IVA del grupo (el importe total en las líneas de informe de la declaración de IVA). 

> [!NOTE]
> Los miembros del grupo de IVA pueden corregir las declaraciones de IVA enviadas siempre que el representante del grupo no haya emitido la declaración de IVA del grupo. Para realizar una corrección, el miembro del grupo de IVA debe crear una nueva declaración de IVA para el período de devolución de IVA y enviarla al representante del grupo de IVA. En el lado del representante del grupo de IVA, la última declaración de IVA se incluirá en la página **Declaraciones de IVA**. 

## <a name="see-also"></a>Consulte también
[Trabajar con el IVA por ventas y compras](finance-work-with-vat.md)  
[Configurar el impuesto sobre el valor añadido](finance-setup-vat.md)
