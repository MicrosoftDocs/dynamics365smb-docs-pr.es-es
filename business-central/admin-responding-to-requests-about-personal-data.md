---
title: Respuesta a las solicitudes de datos personales de usuarios
description: Este artículo explica cómo responder a las solicitudes sobre datos personales.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 04/25/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# Respuesta a las solicitudes de datos personales de usuarios

Los asuntos de datos pueden solicitar varios tipos de acciones relacionadas con sus datos personales. Por ejemplo, según algunos reglamentos y leyes de privacidad, tienen derecho a solicitar la exportación, eliminación y modificación de sus datos personales. Estas solicitudes se denominan *Solicitudes de los interesados*. Si ha clasificado la confidencialidad de sus datos y está seguro de que son correctos, un administrador puede responder a las solicitudes utilizando las opciones de la pestaña **Privacidad de datos** en el área de trabajo **Director de TI**.

## Tipos de solicitudes

La siguiente tabla proporciona ejemplos de los tipos de solicitudes a las que pueden responder los administradores.

> [!Note]
> Si bien brindamos capacidades para responder a estos tipos de solicitudes y, por lo tanto, para acceder a los datos personales, es su responsabilidad garantizar que los datos personales y confidenciales se ubiquen y clasifiquen de manera apropiada.

|Tipo petición|Descripción y respuesta propuesta|
|-----|-----|
|Solicitudes de portabilidad|Un interesado puede realizar una solicitud de portabilidad de datos. Debe exportar los datos personales del interesado de sus sistemas y proporcionarlos en un formato estructurado y de uso común. Para responder a estas solicitudes puede utilizar la **Utilidad de privacidad de datos** para exportar datos personales a un archivo de Excel o a un paquete de configuración RapidStart. Con Excel, puede editar los datos personales y guardarlos en un formato legible de uso común, como .csv o .xml. Para los paquetes de configuración de RapidStart, puede configurar tablas de datos maestros y sus tablas relacionadas que contienen datos personales. <br><br> **Nota:** Al exportar datos se especifica un nivel de sensibilidad mínimo. La exportación incluirá el mínimo y todos los niveles de sensibilidad por encima de este. Por ejemplo, si elige exportar datos clasificados como Personales, la exportación también incluirá datos clasificados como Sensibles. <br><br>Al exportar datos relacionados con un sujeto de datos, la **Utilidad de privacidad de datos** busca relaciones directas entre el sujeto de datos y los datos relacionados. La **Utilidad de privacidad de datos** no exporta automáticamente las relaciones indirectas entre los datos relacionados con el sujeto de datos y otros datos. Por ejemplo, la tabla Contacto ha relacionado directamente los datos de las Respuestas de perfil de contacto, y dicha tabla está, además, relacionada con los datos de las Preguntas de perfil. Si también desea exportar Preguntas de perfil, debe agregar esta tabla manualmente como una fila con los filtros apropiados en el paquete de configuración que crea la **Utilidad de privacidad de datos**.|
|Solicitudes de eliminación|Un asunto de datos puede solicitarle que elimine sus datos personales. Hay varias maneras de eliminar datos personales utilizando las capacidades de personalización, pero la decisión y la implementación son su responsabilidad. En algunos casos, puede editar directamente sus datos. Por ejemplo, eliminar un contacto y luego ejecutar el proceso Eliminar mov. cancel. reg. inter. para eliminar interacciones para el contacto. <br><br> **Nota:** Si ha especificado una fecha en el campo **Permitir eliminar documentos anteriores a** en las páginas **Configuración ventas y cobros** o **Configuración compras y pagos**, puede tener que cambiar la fecha para poder eliminar los documentos de ventas y compras publicados que tengan fechas de registro en esa fecha o antes.|
|Solicitudes para su corrección|Un asunto de datos puede solicitarle que corrija los datos personales incorrectos. Existen varias formas de hacerlo. En algunos casos, puede exportar listas a Excel para editar de manera masiva múltiples registros y luego importar los datos actualizados. Para obtener más información, consulte [Exportar los datos de negocio a Excel](about-export-data.md). También puede editar manualmente los campos que contienen datos personales, como editar información sobre un cliente en la tarjeta del cliente. Sin embargo, los registros como los movimientos del libro mayor general, de clientes y de impuestos son importantes. Si almacena datos personales en registros de transacciones comerciales, considere utilizar las capacidades de personalización para modificar dichos datos personales.|

## Restringir el procesamiento de datos para un interesado

Un asunto de datos puede solicitarle que detenga temporalmente el procesamiento de sus datos personales. Para cumplir con dichas solicitudes, puede marcar su registro como bloqueado debido a la privacidad para detener el procesamiento de sus datos. Cuando un registro está marcado como bloqueado, no puede crear nuevas transacciones que usen ese registro. Por ejemplo, no puede crear una nueva factura para un cliente cuando el cliente o el vendedor están bloqueados. Para marcar a un asunto de datos como bloqueado, abra la tarjeta para el sujeto de datos, por ejemplo, el Cliente, Proveedor o Tarjetas de contacto, y elija la casilla de verificación **Privacidad bloqueada**. Tiene que elegir **Mostrar más** para mostrar el campo.  

## Gestionar solicitudes de interesados cuando se utiliza una versión de prueba

Algunos tipos de datos personales forman parte de una cuenta de Microsoft 365 y solo los administradores pueden exportar los datos. El proceso para gestionar las solicitudes de los sujetos de datos es diferente según el tipo de inquilino de [!INCLUDE[prod_short](includes/prod_short.md)].

Si tiene una suscripción de pago para [!INCLUDE[prod_short](includes/prod_short.md)], los usuarios deben ponerse en contacto con el administrador de inquilinos de su organización para realizar una solicitud de interesado. Los administradores tienen los derechos administrativos y las herramientas para tender solicitudes de interesados.

Si se ha suscrito a [!INCLUDE[prod_short](includes/prod_short.md)] desde la página [Pruebas](https://trials.dynamics.com/) y todavía está usando la versión de prueba, los usuarios pueden descargar y exportar sus propios datos en la [página Privacidad del trabajo y la escuela del Azure Portal](https://portal.azure.com#blade/Microsoft_AAD_IAM/GDPRViralBlade).

En la página de Privacidad del trabajo y la escuela, también puede cerrar su cuenta. Sin embargo, le recomendamos que primero exporte y elimine todos los datos. Al eliminar su cuenta pierde el acceso a [!INCLUDE[prod_short](includes/prod_short.md)].

Todavía puede marcar personas como bloqueadas debido a la privacidad y exportar, editar o eliminar transacciones como se explica en otra sección de este artículo.  

## Exportar datos de tablas no clasificadas por interesado

Si debe exportar datos que no están clasificados de manera que se exporten automáticamente, como los datos de la tabla Respuestas de perfil, debe realizar las siguientes acciones:

* Considere si realmente debe exportar datos complementarios que no estén directamente relacionados con el contacto.
* Agregue la tabla y la relación manualmente al paquete Rapid Start y expórtelas directamente desde el paquete Rapid Start. Generamos un paquete Rapid Start para usted para que pueda modificarlo en tales situaciones.

## Controlar datos sobre menores

Si la edad de una persona de contacto es inferior a la edad de consentimiento legal según las leyes de su región, puede indicarlo seleccionando la casilla de verificación **Menor** en la **Tarjeta de contacto**. Al introducirlos, la casilla de verificación **Privacidad bloqueada** se seleccionará automáticamente. Cuando reciba el consentimiento del padre o tutor legal del menor, puede elegir la casilla **Consentimiento de los padres recibido** para desbloquear el contacto. Aunque puede procesar datos personales para menores, no puede usar la funcionalidad de creación de perfiles en Dynamics 365 Sales.

> [!Note]
> El Registro de cambios puede registrar detalles tales como cuándo y por quién se seleccionó la casilla de verificación **Consentimiento de los padres recibido**. Un administrador puede configurarlo utilizando la guía **Cambiar configuración de registro** y también eligiendo la casilla de verificación **Registrar modificación para el consentimiento de los padres** en la tarjeta de **Contacto**. Para obtener más información, vea [Registrar cambios](across-log-changes.md).  

### Consulte también

<!-- [Classifying Data](/dynamics-nav/classifying-data?toc=/dynamics365/business-central/toc.json)  
[Classifying Data Sensitivity](admin-classifying-data-sensitivity.md)  -->
[Exportar los datos de negocio a Excel](about-export-data.md)  
[Registrar cambios](across-log-changes.md)  
[Solicitudes de interesados](/microsoft-365/compliance/gdpr-data-subject-requests)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
