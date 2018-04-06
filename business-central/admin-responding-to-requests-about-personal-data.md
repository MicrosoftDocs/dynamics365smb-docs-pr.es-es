---
title: Respuesta a las solicitudes de datos personales
description: "Deberá responder a las solicitudes de asunto de datos."
author: bholtorf
ms.author: bholtorf
ms.custom: na
ms.date: 03/13/2018
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 89f53f24f74401ce384b54d04fbeb473aedad96d
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---

# <a name="responding-to-requests-about-personal-data"></a>Respuesta a las solicitudes de datos personales  
Los asuntos de datos pueden solicitar varios tipos de acciones relacionadas con sus datos personales. Si ha clasificado la sensibilidad de sus datos y está seguro de que son correctos, un administrador puede responder a las solicitudes utilizando la hoja de trabajo de clasificación de datos en el área de trabajo **Administrar usuarios, grupos de usuarios y permisos** o si está utilizando el cliente de Windows, en el área de trabajo **Administrador de TI**. Para obtener más información sobre la clasificación de datos y la clasificación de la confidencialidad de datos, consulte [Clasificar datos](/dynamics-nav/classifying-data) y [Clasificar confidencialidad de datos](admin-classifying-data-sensitivity.md).

La siguiente tabla proporciona ejemplos de los tipos de solicitudes a las que puede responder.

> [!Note]
> Si bien brindamos capacidades para responder a estos tipos de solicitudes y, por lo tanto, para acceder a los datos personales, es su responsabilidad garantizar que los datos personales y confidenciales se ubiquen y clasifiquen de manera apropiada.

|Tipo petición|Descripción y respuesta propuesta|
|-----|-----|
|Solicitudes de portabilidad|Un sujeto de datos puede realizar una solicitud de portabilidad de datos, lo que significa, en parte, que debe exportar los datos personales del sujeto de los datos de sus sistemas y proporcionarlos en un formato estructurado y de uso común. Para responder a estas solicitudes, utilice la Utilidad de privacidad de datos para exportar datos personales a un archivo de Excel. Con Excel, puede editar los datos personales y guardarlos en un formato legible de uso común, como .csv o .xml. Los administradores también pueden exportar datos utilizando paquetes de configuración de Rapid Start y luego configurar tablas de datos maestros y sus tablas relacionadas que contienen datos personales. |
|Solicitudes de eliminación|Un asunto de datos puede solicitarle que elimine sus datos personales. Hay varias maneras de eliminar datos personales utilizando las capacidades de personalización, pero la decisión y la implementación son su responsabilidad. En algunos casos, puede optar por editar directamente sus datos, por ejemplo, borrar un contacto y luego ejecutar el proceso Eliminar mov. cancel. reg. inter. para eliminar interacciones para el contacto. <br><br> **Nota:** Si ha especificado una fecha en el campo **Permitir eliminar documentos anteriores a** en las páginas **Configuración ventas y cobros** o **Configuración compras y pagos**, puede tener que cambiar la fecha para poder eliminar los documentos de ventas y compras publicados que haya impreso y que tengan fechas de registro en esa fecha o antes.|
|Solicitudes para su corrección|Un asunto de datos puede solicitarle que corrija los datos personales incorrectos. Existen varias formas de hacerlo. En algunos casos, puede exportar listas a Excel para editar de manera masiva múltiples registros y luego importar los datos actualizados. Para obtener más información, consulte [Exportar los datos de negocio a Excel](https://docs.microsoft.com/en-us/dynamics-nav-app/about-export-data). También puede editar manualmente los campos que contienen datos personales, como editar información sobre un cliente en la tarjeta del cliente. Sin embargo, los registros de transacciones tales como los movimientos generales, de clientes y de impuestos son esenciales para la integridad del sistema de planificación de recursos de la empresa. Si almacena datos personales en registros de transacciones comerciales, considere utilizar las capacidades de personalización para modificar dichos datos personales.|

## <a name="restrict-data-processing-for-a-data-subject"></a>Restringir el procesamiento de datos para un sujeto de datos
Un asunto de datos puede solicitarle que detenga temporalmente el procesamiento de sus datos personales. Para cumplir con dichas solicitudes, puede marcar su registro como bloqueado debido a la privacidad para detener el procesamiento de sus datos. Cuando un registro está marcado como bloqueado, no puede crear nuevas transacciones que usen ese registro. Por ejemplo, no puede crear una nueva factura para un cliente cuando el cliente o el vendedor están bloqueados. Para marcar a un asunto de datos como bloqueado, abra la tarjeta para el sujeto de datos, por ejemplo, el Cliente, Proveedor o Tarjetas de contacto, y elija la casilla de verificación **Privacidad bloqueada**. Tiene que elegir **Mostrar más** para mostrar el campo.

## <a name="handling-data-about-minors"></a>Controlar datos sobre menores
Si la edad de una persona de contacto es inferior a la edad de consentimiento legal según las leyes de su región, puede indicarlo seleccionando la casilla de verificación **Menor** en la **Tarjeta de contacto**. Al introducirlos, la casilla de verificación **Privacidad bloqueada** se seleccionará automáticamente. Cuando reciba el consentimiento del padre o tutor legal del menor, puede elegir la casilla **Consentimiento de los padres recibido** para desbloquear el contacto. Aunque puede procesar datos personales para menores, no puede usar la funcionalidad de creación de perfiles en Microsoft Dynamics 365 for Sales.

> [!Note]
> El Registro de cambios puede registrar detalles tales como cuándo y por quién se seleccionó la casilla de verificación **Consentimiento de los padres recibido**. Un administrador puede configurarlo utilizando la guía **Cambiar configuración de registro** y también eligiendo la casilla de verificación **Registrar modificación para el consentimiento de los padres** en la tarjeta de **Contacto**. Para obtener más información, vea [Registrar cambios](/dynamics-nav-app/across-log-changes).  

## <a name="see-also"></a>Consulte también
[Clasificar datos](https://docs.microsoft.com/en-us/dynamics-nav/classifying-data)  
[Clasificar confidencialidad de datos](admin-classifying-data-sensitivity.md)  
[Exportar los datos de negocio a Excel](https://docs.microsoft.com/en-us/dynamics-nav-app/about-export-data)  

