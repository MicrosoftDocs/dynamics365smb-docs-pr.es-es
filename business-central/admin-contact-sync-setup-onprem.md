---
title: Configurar la sincronización de contactos con Outlook para Business Central local
description: Aprenda a configurar un entorno local de Business Central para sincronizar los contactos en Business Central y Outlook.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 04/04/2023
ms.custom: bap-template
---

# Configurar la sincronización de contactos con Outlook para Business Central local

En este artículo, aprenderá a configurar [!INCLUDE[prod_short](includes/prod_short.md)] local para sincronizar contactos en [!INCLUDE[prod_short](includes/prod_short.md)] con contactos en Outlook. Para obtener más información sobre la característica, vaya a [Sincronizar contactos en Business Central con Contactos en Microsoft Outlook](admin-synchronize-outlook-contacts.md).

## Introducción

La sincronización de contactos requiere el uso del protocolo OAuth 2.0 para la autenticación con Exchange Online. Anteriormente, también se admitía la autenticación básica, pero está en desuso y ya no se admite con Exchange Online. Puede leer más sobre la puesta en desuso en [Puesta en desuso de la autenticación básica en Exchange Online](/exchange/clients-and-mobile-in-exchange-online/deprecation-of-basic-authentication-exchange-online). Este cambio significa que la sincronización de contactos en Business Central puede haber dejado de funcionar en su entorno local. Este artículo explicará cómo hacer que funcione de nuevo.

## Requisitos previos

- Exchange Online, ya sea una versión independiente o mediante un plan de Microsoft 365  
- Acceso al inquilino Azure Active Directory (Azure AD) utilizado por Exchange Online
- Los usuarios de [!INCLUDE[prod_short](includes/prod_short.md)] tienen una cuenta de correo electrónico Microsoft 365 o Exchange Online, que se asigna a sus cuentas en [!INCLUDE[prod_short](includes/prod_short.md)]. Puede comprobar esta configuración en la sección **Autenticación de Microsoft 365** de su perfil de usuario en la lista **Usuarios**. 

## Configurar la sincronización de contactos

Complete los siguientes pasos para configurar la sincronización de contactos. Si está ejecutando [!INCLUDE[prod_short](includes/prod_short.md)], primavera de 2019 (v.14), tendrá que realizar un paso adicional que modifica el código de la aplicación o establece una conexión con Power BI.

1. <a name="registerapp"></a>Registre una aplicación para la API de Exchange Online en su inquilino de Azure AD.

   En esste paso, agregará una aplicación registrada en el inquilino de Azure AD de su plan de Microsoft 365 o Exchange Online. +Como otros servicios de Azure que funcionan con Business Central, Exchange Online requiere una aplicación registrada en Azure AD. La aplicación registrada proporciona servicios de autenticación y autorización entre Business Central y Exchange Online.

   Siga las instrucciones detalladas en la seccion de ayuda para desarrolladores y profesionales de IT en [Registrar una aplicación en Azure Active Directory](/dynamics365/business-central/dev-itpro/administration/register-app-azure#register-an-application-in-azure-active-directory). Mientras sigue las instrucciones, recuerde los siguientes puntos:

   - Si ya ha registrado una aplicación como parte de una integración con otro producto de Microsoft, como Power BI, luego puede reutilizar esa aplicación registrada. En este caso, solo tendrá que configurar la aplicación con los permisos de Office 365 Exchange Online descritos en el siguiente punto.

   - Configure la aplicación registrada con los siguientes permisos delegados a la API de Office 365 Exchange Online:

     - Contacts.ReadWrite
     - EWS.AccessAsUser.All

2. Para la versión 14 de [!INCLUDE[prod_short](includes/prod_short.md)], realice una de las siguientes tareas:

   - Modifique la página 6700 cambiando `FALSE` a `TRUE` en la siguiente línea de código en el desencadenador `OnPageOpen`:

     ```
     PasswordRequired := AzureADMgt.GetAccessToken(AzureADMgt.GetO365Resource,AzureADMgt.GetO365ResourceName,TRUE) = '';
     ```

   - Cree una nueva página con el siguiente código en el activador OnPageOpen:

     ```
     PasswordRequired := AzureADMgt.GetAccessToken(AzureADMgt.GetO365Resource,AzureADMgt.GetO365ResourceName,TRUE) = '';
     ```

   - Configure Power BI siguiendo las instrucciones en [Configure Business Central localmente para la integración de Power BI](admin-powerbi-setup.md#setup).

   Una vez implementada la solución que elija, solicite a los usuarios que ejecuten la página nueva o modificada o que [se conecten a Power BI](across-working-with-powerbi.md#connect). Solo tendrán que hacer este paso una vez.

## Pasos siguientes

[Sincronizar los contactos de Business Central con los de Microsoft Outlook](admin-synchronize-outlook-contacts.md)  
