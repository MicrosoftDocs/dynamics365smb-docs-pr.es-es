---
title: Configuración de la integración de OneDrive con Business Central local
description: Obtenga información sobre cómo configurar Business Central en las instalaciones para integrarse con OneDrive para la Empresa.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'OneDrive, share, browser'
ms.date: 09/06/2022
ms.author: jswymer
---
# <a name="configuring-onedrive-integration-with-business-central-on-premises"></a>Configuración de la integración de OneDrive con Business Central local

Este artículo explica cómo configurar la integración de OneDrive con Business Central local. A diferencia de [!INCLUDE[prod_short](includes/prod_short.md)] en línea, la conexión entre Business Central y OneDrive para la Empresa no se configura automáticamente. Si la conexión no se configura, los usuarios no pueden usar las funciones para OneDrive.

Hay dos tareas que deben realizarse para configurar la integración de OneDrive.

- La primera tarea consiste en registrar una aplicación (app) en su inquilino de Azure Active Directory de su plan de Microsoft 365. La aplicación registrada se utiliza con fines de autenticación. Esta tarea normalmente se realiza en Azure Portal y en el cliente web de Business Central.
- La segunda tarea consiste en establecer la conexión con la URL de OneDrive y activando las funciones de OneDrive en Business Central. Esta tarea se realiza en el cliente web de Business Central. Se hace de manera diferente para la versión 21 que para las versiones 19 y 20. La versión 21 introduce una nueva **Configuración de OneDrive** que reemplaza la **Configuración de conexiones de SharePoint**.  

> [!IMPORTANT]
> [!INCLUDE[prod_short](includes/prod_short.md)] local solo se puede conectar a OneDrive alojado por Microsoft en la nube. No se admite la conexión de [!INCLUDE[prod_short](includes/prod_short.md)] local al repositorio Mis sitios de SharePoint Server.

## <a name="register-an-app-in-azure-ad-for-onedrive-integration"></a><a name="registerapp"></a>Registrar una aplicación en Azure AD para la integración de OneDrive

En esta tarea, agregará una aplicación registrada para Business Central en el inquilino de Azure AD de su plan Microsoft 365. Como otros servicios de Azure que funcionan con Business Central, OneDrive requiere una aplicación registrada en Azure Active Directory (Azure AD). La aplicación registrada proporciona servicios de autenticación y autorización entre Business Central y SharePoint, que utiliza OneDrive.

Para conocer los pasos detallados para completar este paso, consulte [Registrar una aplicación en Azure Active Directory](/dynamics365/business-central/dev-itpro/administration/register-app-azure#register-an-application-in-azure-active-directory) en la ayuda para desarrolladores y profesionales de TI.

Al registrar la aplicación, tenga en cuenta los siguientes puntos:

- Si ya ha registrado una aplicación como parte de una integración con otro producto de Microsoft, como Power BI, luego puede reutilizar esa aplicación registrada. En este caso, solo tendrá que configurar los permisos de SharePoint para la aplicación registrada existente.

- Asegúrese de que configura la aplicación registrada con los siguientes permisos delegados a la API de SharePoint:

    - AllSites.FullControl
    - User.ReadWrite.All
    
    Para Business Central 2021 lanzamiento de versiones 2 (versión 19), configure estos permisos:
    
    - AllSites.Write
    - MyFiles.Write
    - User.Read.All 

- Si está utilizando la versión 19 o 20 de Business Central, copie el **ID de la aplicación (cliente)** y el **secreto del cliente** utilizado por la aplicación registrada. Necesitará esta información en la siguiente tarea.

## <a name="get-your-onedrive-url"></a><a name="url"></a>Conseguir la URL de OneDrive

[!INCLUDE[onedrive-url](includes/onedrive-url.md)]

## <a name="set-up-the-onedrive-connection-in-version-21-and-later"></a>Configurar la conexión de OneDrive en la versión 21 y posteriores

Use este procedimiento si está usando Business Central 2022 versión 2 (versión 21) o posterior.

### <a name="prerequisites"></a>Requisitos previos

- Permiso indirecto, modificar y eliminar (imd) en la tabla **Escenario de servicio de documentos** como minimo

### <a name="run-onedrive-setup"></a>Ejecutar la configuración de OneDrive

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de OneDrive** y luego elija el enlace relacionado.
2. La primera vez que ejecute la configuración asistida, verá **Su privacidad**. Lea la inforamción de la página y, si está de acuerdo con los términos, seleccione **Aceptar** para continuar.
3. En la página **Configurar el manejo de archivos**, tiene las siguientes opciones para elegir:

   [!INCLUDE[onedrive-feature-options](includes/onedrive-feature-options.md)]

4. En la página **Configurar Business Central**, ingrese la URL de OneDrive en el campo **URL de OneDrive**.

   [¿Cómo busco mi dirección URL de OneDrive?](#url)
5. Elija **Conexión de prueba** y espere los resultados.
   - Si la prueba tiene éxito, elija **Hecho**, entonces estás listo para ir.
   - Si la prueba falla, recibirá un mensaje que describe el problema. Por lo general, el problema tiene que ver con la URL que proporcionó. Elija **Aceptar** para volver a la página **Configurar Business Central**, verifique la URL y vuelva a intentarlo.
   - Si aún no ha configurado la aplicación de Azure AD registrada, la guía **Configurar Azure Active Directory** se abre.
6. Una vez completado, el aviso de privacidad para la integración de OneDrive está acordada para todos los usuarios. Si desea cambiarlo para que los usuarios deban estar de acuerdo o en desacuerdo por sí mismos, entonces vaya a la página **Estado de los avisos de privacidad** y seleccione **Dejar que el usuario decida** para la integración de OneDrive. A continuación, se solicitará a los usuarios que acepten o no el aviso de privacidad la primera vez que utilicen las caracteristicas de OneDrive. Para obtener más información, consulte [Avisos de privacidad](privacy-notices-status.md).

## <a name="set-up-the-connection-in--version-19-and-20"></a>Configurar la conexión de [!INCLUDE[prod_short](includes/prod_short.md)] en la versión 19 y 20

Use este procedimiento si está usando el primer lanzamiento de versiones de 2022 de Business Central (versión 20) o el segundo lanzamiento de versiones de 2021 (versión 19).
> [!IMPORTANT]
> Al configurar esta función, también habilita funciones heredadas que envían archivos a OneDrive.  
>
>* La función Abrir en Excel copiará automáticamente el archivo de Excel a OneDrive, luego ábralo en Excel Online. 
>* Al exportar cualquier informe a un archivo se copiará automáticamente el archivo a OneDrive, luego ábralo en Excel Online, Word Online o OneDrive. 
>* Otras funciones también pueden abrirse automáticamente en OneDrive.

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de conexión de Microsoft SharePoint** y luego elija el enlace relacionado.
2. En el campo **Descripción**, escriba una descripción para la conexión, como **OneDrive**.
3. En el campo **Carpeta**, ingrese **Business Central**.
4. En el campo **Ubicación**, ingrese la URL de su OneDrive.

   [¿Cómo busco mi dirección URL de OneDrive?](#url)
5. En el campo **Identificación del cliente**, ingrese el ID de cliente de la aplicación registrada.
6. En el campo **Secreto del cliente**, ingrese el secreto de la aplicación registrada. 

> [!IMPORTANT]
> La página **Configuración de conexión de SharePoint** se utiliza para configurar varias funciones heredadas. La sección **General** configura la conexión con OneDrive, y la sección **Documentos compartidos** redirige archivos a SharePoint en su lugar. **Configuración de la conexión de SharePoint** ha quedado obsoleta y se eliminará en la próxima versión. Le recomendamos que no configure la sección **Documentos compartidos**. Para más información, consulte [Funciones obsoletas en la aplicación base ](/dynamics365/business-central/dev-itpro/upgrade/deprecated-features-w1#microsoft-sharepoint-connection-setup).

## <a name="after-upgrade-to-version-21"></a>Después de actualizar a la versión 21

Cuando actualiza a la versión 21 o posterior, la conexión existente a OneDrive que está configurado en la página **Configuración de la conexión de SharePoint** seguirá funcionando. Pero, como la página **Configuración de la conexión de SharePoint** se eliminará en la versión 23, le recomendamos que cambie a la nueva integración de OneDrive, como se describe en la siguiente sección. Hacer este cambio ahora hará que sea más fácil cuando la **Configuración de la conexión de SharePoint** finalmente se elimine. Además, le permitirá utilizar la guía de configuración asistida de **Configuración de OneDrive** para administrar las características de OneDrive que son accesibles para los usuarios.

## <a name="switching-from-legacy-sharepoint-to-new-onedrive-integration"></a>Cambiar SharePoint heredado a la nueva integración de OneDrive

Para cambiar a la nueva integración de OneDrive, ejecute la guía de configuración asistida de **Configuración de OneDrive**, que puede abrir directamente o desde la página **Configuración de la conexión de SharePoint** heredada. La configuración asistida de **Configuración de OneDrive** le guiará a través de la transición y le brindará información sobre los cambios que se realizarán en el camino.

Antes de comenzar con el cambio o mientras lo hace, consulte la siguiente sección para conocer algunos aspectos y consideraciones sobre el proceso. 

### <a name="about-switching-to-the-new-onedrive-integration"></a><a name="onedrivesetupmigration"></a>Acerca de cambiar a la nueva integración de OneDrive

Además de la integración de OneDrive, Business Central también puede integrarse con otros servicios, como Power BI e impresión universal. La integración con estos otros servicios también requiere una aplicación registrada de Azure AD para la autenticación. La aplicación Azure AD utilizada por estos otros servicios está configurada en la configuración asistida **Configurar las cuentas de Azure Active Directory**. Cuando cambia de la configuración de conexión de SharePoint heredada, la nueva configuración asistida **Configuración de OneDrive** cambiará su integración de OneDrive para usar también la configuración asistida de **Configurar las cuentas de Azure Active Directory**, por lo que todas las integraciones utilizan la misma aplicación Azure AD.

Este cambio tiene implicaciones a la hora de pasar a la nueva integración de OneDrive, dependiendo de si ya hay una aplicación Azure AD configurada en la configuración asistida de **Configurar sus cuentas de Azure Active Directory**. 

> [!IMPORTANT]
> Después de cambiar a la nueva configuración de OneDrive, ya no puede utilizar la página **Configuración de la conexión de SharePoint** para configurar la integración de OneDrive.

#### <a name="how-the-changes-affect-the-integration"></a>Cómo afectan los cambios a la integración

La configuración asistida de **Configuración de OneDrive** siempre usará la aplicación que está configurada en la configuración asistida **Configurar las cuentas de Azure Active Directory**, si hay una. Cuando ejecuta la configuración asistida **Configuración de OneDrive**, comparará la aplicación configurada en **Configurar sus cuentas de Azure Active Directory** con su aplicación actual configurada en **Configuración de la conexión de SharePoint**.

> [!TIP]
> En la página **Configuración de la conexión de SharePoint** y la configuración asistida **Configurar cuentas de Azure Active Directory**, la aplicación de Azure AD se identifica con el **Id. del cliente**.

- Si la aplicación en **Configurar cuentas de Azure Active Directory** es diferente a la aplicación en **Configuración de la conexión de SharePoint**, la integración de OneDrive cambiará para usar la aplicación en **Configurar cuentas de Azure Active Directory**.

   En **Configuración de OneDrive** mientras realiza el cambio, obtendrá un mensaje similar al siguiente texto: 

  `The Azure Active Directory Application used for authentication will be configured for all Business Central integrations. This means the client id will change to NNNNNNNNN-NNNN-NNNN-NNNN-NNNNNNNNNNNN, you may want to test it has the correct permissions.`

  `NNNNNNNNN-NNNN-NNNN-NNNN-NNNNNNNNNNNN` representa el ID de cliente de la aplicación en **Configurar cuentas de Azure Active Directory** que se ha cambiado a la la integración de OneDrive. 

  > [!IMPORTANT]
  > Para que la nueva integración de OneDrive funcione después de hacer el cambio, debe otorgar permiso a la aplicación para la API de SharePoint en el portal de Azure. Puede realizar este paso antes o después de cambiar a la nueva configuración de OneDrive. Para obtener más información, consulte la sección [Registrar una aplicación en Azure AD para la integración de OneDrive](#registerapp).

- Si la aplicación en **Configurar cuentas de Azure Active Directory** es la misma que la aplicación en **Configuración de la conexión de SharePoint**, la integración de OneDrive usará la misma aplicación que antes, excepto por la configuración en la configuración **Configurar cuentas de Azure Active Directory**.

   En **Configuración de OneDrive** mientras realiza el cambio, obtendrá un mensaje similar al siguiente texto:

    `The Azure Active Directory Application used for authentication will be configured for all Business Central integrations. This has already been configured with the same client id (5F78CADE-19C0-49BF-AF84-306D0579B50E).`

- Si no hay ninguna aplicación configurada en la configuración **Configurar cuentas de Azure Active Directory**, la integración de OneDrive utilizará la misma aplicación que antes.

   La configuración asistida de **Configuración de OneDrive** copiará la configuración de la aplicación en la configuración **Configurar las cuentas de Azure Active Directory**, por lo que se usará para otras integraciones que podrían configurarse más adelante.

   En **Configuración de OneDrive** mientras realiza el cambio, obtendrá un mensaje similar al siguiente texto:

   `The Azure Active Directory Application used for authentication will be configured for all Business Central integrations`.

### <a name="run-onedrive-setup-to-switch-to-the-new-onedrive-integration"></a>Ejecutar la configuración de OneDrive para cambiar a la nueva integración de OneDrive

1. Abra la página **Configuración de OneDrive** o la página **Configuración de la conexión de SharePoint**.
2. Si está usando la **Configuración de la conexión de SharePoint**, elija **Ir a la nueva configuración de OneDrive** en la notificación en la parte superior de la página.
3. Siga la guía de configuración asistida de **Configuración de OneDrive**.
4. Cuando llega a la página **Configurar el manejo de archivos**, elija una de las siguientes opciones para activar funciones:

   [!INCLUDE[onedrive-feature-options](includes/onedrive-feature-options.md)]

5. La página **Configurar Business Central** muestra la misma URL que utiliza la página de integración de OneDrive existente. Puede cambiar la URL según sea necesario.
6. Seleccione **Conexión de prueba** y siga las instrucciones.

   Si la prueba tiene éxito, seleccione **Hecho** y entonces todo estará listo. De lo contrario, use los mensajes en la página para ayudarlo a solucionar el problema.

## <a name="see-also"></a>Consulte también
[Integración de Business Central y OneDrive para la Empresa](across-onedrive-overview.md)  
[Abrir archivos de Business Central en OneDrive](across-share-onedrive.md)  
[Preguntas más frecuentes de OneDrive](admin-onedrive-faq.md)

