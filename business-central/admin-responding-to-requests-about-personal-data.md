---
title: Respuesta a las solicitudes de datos personales
description: Este tema le indica cómo responder a las solicitudes sobre datos personales. Esto se conoce como solicitud de asunto de datos.
author: bholtorf
ms.service: dynamics365-business-central
ms.author: bholtorf
ms.custom: na
ms.date: 06/14/2021
ms.reviewer: na
ms.topic: conceptual
ms.openlocfilehash: 77b1470ee7df736815451c03e4afbf684803aea4
ms.sourcegitcommit: e562b45fda20ff88230e086caa6587913eddae26
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "6321967"
---
# <a name="responding-to-requests-about-users-personal-data"></a>Respuesta a las solicitudes de datos personales de usuarios  
Los asuntos de datos pueden solicitar varios tipos de acciones relacionadas con sus datos personales. Por ejemplo, según el Reglamento general de protección de datos (GDPR), los residentes de la UE tienen derecho a solicitar la exportación, eliminación y modificación de sus datos personales. Esto se conoce como *Solicitud de asunto de datos*. Si ha clasificado la confidencialidad de sus datos y está seguro de que son correctos, un administrador puede responder a las solicitudes utilizando las opciones de la pestaña **Privacidad de datos** en el área de trabajo **Director de TI**. Para obtener más información sobre la clasificación de datos y la clasificación de la confidencialidad de datos en [!INCLUDE[prod_long](includes/prod_long.md)], consulte [Clasificar datos](/dynamics-nav/classifying-data?toc=/dynamics365/business-central/toc.json) y [Clasificar confidencialidad de datos](admin-classifying-data-sensitivity.md).  

## <a name="types-of-requests"></a>Tipos de solicitudes

La siguiente tabla proporciona ejemplos de los tipos de solicitudes a las que puede responder.

> [!Note]
> Si bien brindamos capacidades para responder a estos tipos de solicitudes y, por lo tanto, para acceder a los datos personales, es su responsabilidad garantizar que los datos personales y confidenciales se ubiquen y clasifiquen de manera apropiada.

|Tipo petición|Descripción y respuesta propuesta|
|-----|-----|
|Solicitudes de portabilidad|Un sujeto de datos puede realizar una solicitud de portabilidad de datos, lo que significa, en parte, que debe exportar los datos personales del sujeto de los datos de sus sistemas y proporcionarlos en un formato estructurado y de uso común. Para responder a estas solicitudes puede utilizar la **Utilidad de privacidad de datos** para exportar datos personales a un archivo de Excel o a un paquete de configuración RapidStart. Con Excel, puede editar los datos personales y guardarlos en un formato legible de uso común, como .csv o .xml. Para los paquetes de configuración de RapidStart, puede configurar tablas de datos maestros y sus tablas relacionadas que contienen datos personales. <br><br> **Nota:** Al exportar datos se especifica un nivel de sensibilidad mínimo. La exportación incluirá el mínimo y todos los niveles de sensibilidad por encima de este. Por ejemplo, si elige exportar datos clasificados como Personales, la exportación también incluirá datos clasificados como Sensibles. <br><br>Al exportar datos relacionados con un sujeto de datos, la **Utilidad de privacidad de datos** busca relaciones directas entre el sujeto de datos y los datos relacionados. La **Utilidad de privacidad de datos** no exporta automáticamente las relaciones indirectas entre los datos relacionados con el sujeto de datos y otros datos. Por ejemplo, la tabla Contacto ha relacionado directamente los datos de las Respuestas de perfil de contacto, y dicha tabla está, además, relacionada con los datos de las Preguntas de perfil. Si también desea exportar Preguntas de perfil, debe agregar esta tabla manualmente como una fila con los filtros apropiados en el paquete de configuración que crea la **Utilidad de privacidad de datos**.|
|Solicitudes de eliminación|Un asunto de datos puede solicitarle que elimine sus datos personales. Hay varias maneras de eliminar datos personales utilizando las capacidades de personalización, pero la decisión y la implementación son su responsabilidad. En algunos casos, puede optar por editar directamente sus datos, por ejemplo, borrar un contacto y luego ejecutar el proceso Eliminar mov. cancel. reg. inter. para eliminar interacciones para el contacto. <br><br> **Nota:** Si ha especificado una fecha en el campo **Permitir eliminar documentos anteriores a** en las páginas **Configuración ventas y cobros** o **Configuración compras y pagos**, puede tener que cambiar la fecha para poder eliminar los documentos de ventas y compras publicados que haya impreso y que tengan fechas de registro en esa fecha o antes.|
|Solicitudes para su corrección|Un asunto de datos puede solicitarle que corrija los datos personales incorrectos. Existen varias formas de hacerlo. En algunos casos, puede exportar listas a Excel para editar de manera masiva múltiples registros y luego importar los datos actualizados. Para obtener más información, consulte [Exportar los datos de negocio a Excel](about-export-data.md). También puede editar manualmente los campos que contienen datos personales, como editar información sobre un cliente en la tarjeta del cliente. Sin embargo, los registros de transacciones tales como los movimientos generales, de clientes y de impuestos son esenciales para la integridad del sistema de planificación de recursos de la empresa. Si almacena datos personales en registros de transacciones comerciales, considere utilizar las capacidades de personalización para modificar dichos datos personales.|

## <a name="restrict-data-processing-for-a-data-subject"></a>Restringir el procesamiento de datos para un sujeto de datos
Un asunto de datos puede solicitarle que detenga temporalmente el procesamiento de sus datos personales. Para cumplir con dichas solicitudes, puede marcar su registro como bloqueado debido a la privacidad para detener el procesamiento de sus datos. Cuando un registro está marcado como bloqueado, no puede crear nuevas transacciones que usen ese registro. Por ejemplo, no puede crear una nueva factura para un cliente cuando el cliente o el vendedor están bloqueados. Para marcar a un asunto de datos como bloqueado, abra la tarjeta para el sujeto de datos, por ejemplo, el Cliente, Proveedor o Tarjetas de contacto, y elija la casilla de verificación **Privacidad bloqueada**. Tiene que elegir **Mostrar más** para mostrar el campo.  

## <a name="handling-data-subject-requests-while-in-trial"></a>Gestionar solicitudes de sujetos de datos durante la versión de prueba
Ciertos tipos de datos personales forman parte de su cuenta de Microsoft 365 y requieren acceso administrativo para exportarlos, si recibe una solicitud de un usuario sobre este tipo de datos personales en virtud del Reglamento general de protección de datos (GDPR). El proceso para gestionar las solicitudes de los sujetos de datos es diferente según el tipo de inquilino de [!INCLUDE[prod_short](includes/prod_short.md)].  

Si tiene una suscripción de pago para [!INCLUDE[prod_short](includes/prod_short.md)], debe ponerse en contacto con el administrador de inquilinos de su organización para solicitar el asunto de datos. El administrador tiene los derechos administrativos y herramientas a completar la solicitud.  

Si ha iniciado sesión en [!INCLUDE[prod_short](includes/prod_short.md)] en la página [Períodos de prueba](https://trials.dynamics.com/) y no se ha cambiado de esta experiencia de prueba a través de una suscripción de pago del administrador de inquilinos de su organización, puede completar su propia solicitud de datos en la [Página de privacidad de trabajo y escuela en Azure Portal](https://portal.azure.com#blade/Microsoft_AAD_IAM/GDPRViralBlade). Aquí, puede exportar y descargar sus datos personales.

En la página de Privacidad del trabajo y la escuela, también puede cerrar su cuenta. Sin embargo, le recomendamos que se asegure de haber exportado y eliminado todos los datos primero, ya que eliminar su cuenta significa perder el acceso a [!INCLUDE[prod_short](includes/prod_short.md)].  

Todavía puede marcar personas como bloqueadas debido a la privacidad y exportar, editar o eliminar transacciones como se explica en otra sección de este artículo.  

## <a name="exporting-data-from-tables-not-classified-by-data-subject"></a>Exportar datos de tablas no clasificadas por asunto de datos
Si tiene una situación en la que tiene que exportar datos que no están clasificados de manera que se exporten automáticamente, como los datos de la tabla Respuestas de perfil, debe hacer lo siguiente:
-   Considere si realmente desea o tiene que exportar estos datos suplementarios que no están relacionados con el contacto, lo que significa que no tienen relación directa con él.
-   Agregue esta tabla y relación manualmente al paquete de Rapid Start y expórtela directamente desde el paquete de Rapid Start; por ese motivo, generamos un paquete de Rapid Start automáticamente, para que pueda ajustarlo en situaciones como esta.

## <a name="handling-data-about-minors"></a>Controlar datos sobre menores
Si la edad de una persona de contacto es inferior a la edad de consentimiento legal según las leyes de su región, puede indicarlo seleccionando la casilla de verificación **Menor** en la **Tarjeta de contacto**. Al introducirlos, la casilla de verificación **Privacidad bloqueada** se seleccionará automáticamente. Cuando reciba el consentimiento del padre o tutor legal del menor, puede elegir la casilla **Consentimiento de los padres recibido** para desbloquear el contacto. Aunque puede procesar datos personales para menores, no puede usar la funcionalidad de creación de perfiles en Dynamics 365 Sales.

> [!Note]
> El Registro de cambios puede registrar detalles tales como cuándo y por quién se seleccionó la casilla de verificación **Consentimiento de los padres recibido**. Un administrador puede configurarlo utilizando la guía **Cambiar configuración de registro** y también eligiendo la casilla de verificación **Registrar modificación para el consentimiento de los padres** en la tarjeta de **Contacto**. Para obtener más información, vea [Registrar cambios](across-log-changes.md).  

## <a name="see-also"></a>Consulte también
[Clasificar datos](/dynamics-nav/classifying-data?toc=/dynamics365/business-central/toc.json)  
[Clasificar confidencialidad de datos](admin-classifying-data-sensitivity.md)  
[Exportar los datos de negocio a Excel](about-export-data.md)  
[Registrar cambios](across-log-changes.md)  
[Solicitudes de sujetos de datos del GDPR](/microsoft-365/compliance/gdpr-data-subject-requests)  


[!INCLUDE[footer-include](includes/footer-banner.md)]