---
title: Usar Business Central con Outlook | Documentos de Microsoft
description: Este servicio tiene una integración profunda con Microsoft 365, lo que le permite administrar todas sus interacciones y correo de negocio con clientes y proveedores directamente en Outlook.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: SMTP, mail, Microsoft 365
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 6d2e396b21f2d5de2bb341e864df031070df1ca4
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5377953"
---
# <a name="using-business-central-as-your-business-inbox-in-outlook"></a>Usar Business Central como su bandeja de entrada de empresa en Outlook

[!INCLUDE[prod_short](includes/prod_short.md)] introduce la posibilidad de gestionar las interacciones comerciales con sus clientes y proveedores directamente en Microsoft Outlook. Con los complementos de Outlook de [!INCLUDE[prod_short](includes/prod_short.md)], puede ver los datos financieros relativos a los clientes y los proveedores, así como crear y enviar documentos financieros, como por ejemplo presupuestos y facturas.  

## <a name="getting-the-add-in"></a>Obtener el complemento
Es fácil comenzar con el complemento de [!INCLUDE[prod_short](includes/prod_short.md)] para Outlook. En la guía de configuración asistida **Configurar su bandeja de entrada de empresa en Outlook**, puede configurar la conexión para usted o para su organización si su organización usa Microsoft 365. Simplemente, especifique su nombre de usuario y contraseña de Microsoft 365, si se le solicita, y díganos si desea recibir un mensaje de correo electrónico de muestra. Los complementos [!INCLUDE[prod_short](includes/prod_short.md)] se agregan automáticamente a su Outlook. Para obtener más información, consulte [Requisitos mínimos para Outlook](product-requirements.md#outlook).  

A continuación, cuando abra Outlook, verá un mensaje de correo electrónico del *administrador de Dynamics 365 Business Central*. Los nuevos complementos se agregan a la cinta de Outlook y, en el explorador, puede ver los complementos de [!INCLUDE[prod_short](includes/prod_short.md)] inmediatamente encima o debajo del cuerpo del mensaje de correo electrónico. Los complementos se actualizan periódicamente y recibirá la notificación de que tiene lista una nueva versión en Outlook.  

> [!TIP]
> Si utiliza el nuevo Outlook en la web, los complementos de [!INCLUDE[prod_short](includes/prod_short.md)] pueden estar ocultos en **Más acciones**. Si usa el complemento con frecuencia, puede anclarlo para que siempre esté visible de inmediato. Para obtener más información, consulte [Usar complementos en Outlook en la web](https://support.office.com/article/using-add-ins-in-outlook-on-the-web-8f2ce816-5df4-44a5-958c-f7f9d6dabdce?ns=OLWAO365B&version=16).  

Si trabaja con más de una empresa de [!INCLUDE[prod_short](includes/prod_short.md)], puede cambiar fácilmente entre empresas en Outlook. En la barra de acciones del complemento, elija **Mas acciones** y, a continuación, puede ver la opción para cambiar de una empresa a otra.  

<!--TEMP-->
> [!NOTE]
> El cambio de una empresa a otra requiere la fase de lanzamiento 2 de [!INCLUDE[prod_short](includes/prod_short.md)] 2019 o posterior como se anunció en el [plan de versiones](/dynamics365-release-plan/2019wave2/dynamics365-business-central/switch-between-companies-business-inbox-outlook).

Algunas empresas que usan Microsoft 365 restringen los permisos de los usuarios para implementar los complementos. Debe asegurarse de que tiene una suscripción a Microsoft 365 que incluya correo electrónico y permita implementar los complementos. Si desea probar el complemento de todos modos, puede [probar Microsoft 365 gratis](https://www.microsoft.com/microsoft-365/try).  

## <a name="using-the-contact-insights-add-in"></a>Usar el complemento Información del contacto
Supongamos que recibe un correo electrónico de un cliente que desea obtener una oferta de algunos productos. Puede abrir el complemento [!INCLUDE[prod_short](includes/prod_short.md)] directamente en Outlook, que reconoce al remitente como cliente y abre la ficha de cliente para esa empresa. Desde este panel puede ver la información general del cliente, así como analizar en más detalle documentos específicos. También puede rebuscar en el historial de ventas del cliente. Si es un contacto nuevo, puede crearlo como nuevo en [!INCLUDE[prod_short](includes/prod_short.md)] sin salir de Outlook.  

En el complemento puede crear un presupuesto de ventas y reenviarlo a su cliente sin abandonar la ventana de Outlook. Toda la información que necesita para enviar el presupuesto de ventas está disponible en su bandeja de entrada de empresa de Outlook.  
Una vez tenga los datos introducidos puede registrar el presupuesto. Puede enviarlo por correo electrónico. [!INCLUDE[prod_short](includes/prod_short.md)] genera un archivo .PDF con el presupuesto de ventas y lo adjunta al mensaje que tiene como borrador en el complemento.  

De igual forma, si recibe un correo electrónico de un proveedor, puede utilizar el complemento para trabajar con proveedores y facturas de compra.  

En ocasiones desea ver más campos de los que puede ver en el complemento, como cuando desea rellenar líneas en una factura. Para darle un poco más de espacio para trabajar con eso, puede abrir una página independiente con el complemento. Sigue formando parte de Outlook pero dispone de más espacio. Cuando introduce datos en el documento en la vista de ventana emergente, los cambios se guardan automáticamente. Cuando haya terminado de introducir datos en el documento puede elegir el botón **Aceptar**. Seleccionando el marco del complemento en Outlook se actualiza automáticamente el documento con los cambios que haya hecho en la vista de ventana emergente.  

## <a name="creating-invoices-from-your-meeting-appointments"></a>Crear facturas de las citas de reunión
Algunos empresas registran todas las citas facturables en el calendario de Outlook. Con [!INCLUDE[prod_short](includes/prod_short.md)], puede crear la factura para el cliente directamente en el producto de calendario: abra la cita y, a continuación, puede abrir el complemento [!INCLUDE[prod_short](includes/prod_short.md)], buscar la información existente o crear una factura u otro documento de venta directamente.  

## <a name="doing-quick-document-lookup"></a>Realizar búsquedas rápidas en el documento
El complemento Vínculos de documento de [!INCLUDE[prod_short](includes/prod_short.md)] le da un acceso más rápido a los documentos mencionados en los mensajes de correo electrónico. El complemento está disponible para un mensaje si se reconoce el nombre de un documento en el cuerpo del correo. Abrir el complemento le proporciona un acceso rápido al documento.  

Por ejemplo, si recibe un mensaje de correo electrónico que menciona el texto *S-QUO100*, [!INCLUDE[prod_short](includes/prod_short.md)] lo identifica como un presupuesto de venda y de esta manera puede abrir ese documento en Outlook. En Outlook haga clic en el botón inmediatamente superior al cuerpo del correo **Vínculos de documento**. En la aplicación web de Outlook seleccione el texto *S-QUO1001* en el cuerpo del mensaje.  

En el complemento Vínculos de documento puede modificar y realizar diferentes acciones con el documento de la misma forma que lo hace en [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="adding-the-add-ins-manually"></a>Agregar los complementos manualmente
En algunos casos, los complementos no se agregan automáticamente a Outlook. Incluso si usted o un compañero han ejecutado la guía de configuración asistida en nombre de la empresa, es posible que [!INCLUDE[prod_short](includes/prod_short.md)] no aparezca en Outlook. Si tiene este problema, puede agregar los complementos de [!INCLUDE[prod_short](includes/prod_short.md)] manualmente.  

En primer lugar, debe comprobar que tiene acceso a los complementos en su cuenta de Microsoft 365. Simplemente abra su Outlook en un explorador, abra un mensaje, seleccione **Más acciones** (...) en la parte superior del mensaje y, a continuación, en la parte inferior de la lista, seleccione **Obtener complementos**. Esto abre la página **Complementos para Outlook**, donde puede activar [!INCLUDE[prod_short](includes/prod_short.md)] para su Outlook. A continuación, al volver a Outlook, [!INCLUDE[prod_short](includes/prod_short.md)] debe estar disponible.  

De igual forma, en el cliente de escritorio de Outlook puede comprobar que [!INCLUDE[prod_short](includes/prod_short.md)] se muestra en la página **Obtener complementos**.  

En ambos casos, si [!INCLUDE[prod_short](includes/prod_short.md)] sigue sin estar disponible, tiene que obtener los archivos del manifiesto del complemento. Para obtener más información, póngase en contacto con el administrador de Microsoft 365.

## <a name="using-other-email-accounts"></a>Uso de otras cuentas de correo electrónico

Los complementos están diseñados para usarse con Microsoft 365. Si utiliza [!INCLUDE[prod_short](includes/prod_short.md)] local, el administrador sabrá si puede utilizar los complementos de [!INCLUDE[prod_short](includes/prod_short.md)] en Outlook. Para más información, consulte [¿Qué dirección de correo electrónico puedo usar con [!INCLUDE[prod_short](includes/prod_short.md)] ?](across-faq.md#email), el artículo [Características que requieren circunstancias específicas](/dynamics365/business-central/dev-itpro/features-not-implemented-on-premises#features-that-require-specific-circumstances?toc=/dynamics365/business-central/toc.json) y la sección [¿Por qué el complemento de Outlook no funciona para mis usuarios?](/dynamics365/business-central/dev-itpro/faq#why-doesnt-the-outlook-add-in-work-for-my-users?toc=/dynamics365/business-central/toc.json) en las preguntas frecuentes generales del contenido de administración.  

## <a name="see-related-training-at-microsoft-learn"></a>Consulte Formación relacionada en [Microsoft Learn](/learn/modules/alternative-interfaces-dynamics-365-business-central/index)

## <a name="see-also"></a>Consulte también

[Introducción](product-get-started.md)  
[Obtener Business Central en mi dispositivo móvil](install-mobile-app.md)  
[Enviar documentos por correo electrónico](ui-how-send-documents-email.md)  
[Finanzas](finance.md)  
[Ccial](sales-manage-sales.md)  
[Compras](purchasing-manage-purchasing.md)  
[Requisitos mínimos para Outlook](product-requirements.md#outlook)  
[Usar complementos en Outlook en la web](https://support.office.com/article/Using-Add-ins-in-Outlook-on-the-web-8f2ce816-5df4-44a5-958c-f7f9d6dabdce?appver=OWB150)  


[!INCLUDE[footer-include](includes/footer-banner.md)]