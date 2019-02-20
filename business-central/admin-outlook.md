---
title: Usar Business Central con Outlook | Documentos de Microsoft
description: "Este servicio tiene una integración profunda con Office 365 lo que le permite administrar todas sus interacciones y correo de negocio con clientes y proveedores directamente en Outlook."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: SMTP, mail, Office 365
ms.date: 12/10/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 8a73de1aa2f4a0f633c401ea341bb7bde6579723
ms.openlocfilehash: a91f2d34cd023994dcd8eb67a9360d50d2cf3747
ms.contentlocale: es-es
ms.lasthandoff: 12/11/2018

---
# <a name="using-business-central-as-your-business-inbox-in-outlook"></a>Usar Business Central como su bandeja de entrada de empresa en Outlook
[!INCLUDE[d365fin](includes/d365fin_md.md)] introduce la posibilidad de gestionar las interacciones comerciales con sus clientes y proveedores directamente en Microsoft Outlook. Con los complementos de Outlook de [!INCLUDE[d365fin](includes/d365fin_md.md)], puede ver los datos financieros relativos a los clientes y los proveedores, así como crear y enviar documentos financieros, como por ejemplo presupuestos y facturas.  

## <a name="getting-the-add-in"></a>Obtener el complemento
Es fácil comenzar con el complemento de [!INCLUDE[d365fin](includes/d365fin_md.md)] para Outlook. En la guía de configuración asistida **Configurar su bandeja de entrada de empresa en Outlook**, puede configurar la conexión para usted o para su organización. Si su organización utiliza Office 365, debe especificar su nombre de usuario y contraseña de Office 365. Si su organización no usa Office 365, debe especificar la información sobre el Exchange Server que usa. Los complementos [!INCLUDE[d365fin](includes/d365fin_md.md)] se agregan automáticamente a su Outlook.  

A continuación, cuando abra Outlook, verá un mensaje de correo electrónico del administrador de Dynamics 365 Business Central. Los nuevos complementos se agregan a la cinta de Outlook y, en la aplicación web de Outlook, puede ver los complementos de [!INCLUDE[d365fin](includes/d365fin_md.md)] inmediatamente encima o debajo del cuerpo del mensaje de correo electrónico. Los complementos se actualizan periódicamente y recibirá la notificación de que tiene lista una nueva versión en Outlook.  

Algunas empresas que usan Office 365 restringen los permisos de los usuarios para implementar complementos. Debe asegurarse de que tiene una suscripción a Office 365 que incluye correo electrónico y permite implementar complementos. Si desea probar el complemento de todos modos, puede [probar Office 365 gratis](https://products.office.com/try).  

## <a name="using-the-contact-insights-add-in"></a>Usar el complemento Información del contacto
Supongamos que recibe un correo electrónico de un cliente que desea obtener una oferta de algunos productos. Puede abrir el complemento [!INCLUDE[d365fin](includes/d365fin_md.md)] directamente en Outlook, que reconoce al remitente como cliente y abre la ficha de cliente para su empresa. Desde este panel puede ver la información general del cliente, así como analizar en más detalle documentos específicos. También puede rebuscar en el historial de ventas del cliente. Si es un cliente nuevo, puede crearlo como nuevo en [!INCLUDE[d365fin](includes/d365fin_md.md)] sin salir de Outlook.  

En el complemento puede crear un presupuesto de ventas y reenviarlo a su cliente sin abandonar la ventana de Outlook. Toda la información que necesita para enviar el presupuesto de ventas está disponible en su bandeja de entrada de empresa de Outlook.  
Una vez tenga los datos introducidos puede registrar el presupuesto. Puede enviarlo por correo electrónico. [!INCLUDE[d365fin](includes/d365fin_md.md)] genera un archivo .PDF con el presupuesto de ventas y lo adjunta al mensaje que tiene como borrador en el complemento.  

De igual forma, si recibe un correo electrónico de un proveedor, puede utilizar el complemento para trabajar con proveedores y facturas de compra.  

En ocasiones desea ver más campos de los que puede ver en el complemento, como cuando desea rellenar líneas en una factura. Para darle un poco más de espacio para trabajar con eso, puede abrir una página independiente con el complemento. Sigue formando parte de Outlook pero dispone de más espacio. Cuando introduce datos en el documento en la vista de ventana emergente, los cambios se guardan automáticamente. Cuando haya terminado de introducir datos en el documento puede elegir el botón **Aceptar**. Seleccionando el marco del complemento en Outlook se actualiza automáticamente el documento con los cambios que haya hecho en la vista de ventana emergente.  

## <a name="creating-invoices-from-your-meeting-appointments"></a>Crear facturas de las citas de reunión
Algunos empresas registran todas las citas facturables en el calendario de Outlook. Con [!INCLUDE[d365fin](includes/d365fin_md.md)], puede crear la factura para el cliente directamente en el producto de calendario: abra la cita y, a continuación, puede abrir el complemento [!INCLUDE[d365fin](includes/d365fin_md.md)], buscar la información existente o crear una factura u otro documento de venta directamente.  

## <a name="doing-quick-document-lookup"></a>Realizar búsquedas rápidas en el documento
El complemento Vínculos de documento de [!INCLUDE[d365fin](includes/d365fin_md.md)] le da un acceso más rápido a los documentos mencionados en los mensajes de correo electrónico. El complemento está disponible para un mensaje si se reconoce el nombre de un documento en el cuerpo del correo. Abrir el complemento le proporciona un acceso rápido al documento.  

Por ejemplo, si recibe un mensaje de correo electrónico que menciona el texto *S-QUO100*, [!INCLUDE[d365fin](includes/d365fin_md.md)] lo identifica como un presupuesto de venda y de esta manera puede abrir ese documento en Outlook. En Outlook haga clic en el botón inmediatamente superior al cuerpo del correo **Vínculos de documento**. En la aplicación web de Outlook seleccione el texto *S-QUO1001* en el cuerpo del mensaje.  

En el complemento Vínculos de documento puede modificar y realizar diferentes acciones con el documento de la misma forma que lo hace en [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="adding-the-add-ins-manually"></a>Agregar los complementos manualmente
En algunos casos, los complementos no se agregan automáticamente a Outlook. Incluso si usted o un compañero han ejecutado la guía de configuración asistida en nombre de la empresa, es posible que [!INCLUDE[d365fin](includes/d365fin_md.md)] no aparezca en Outlook. Si tiene este problema, puede agregar los complementos de [!INCLUDE[d365fin](includes/d365fin_md.md)] manualmente.  

En primer lugar, debe comprobar que tiene acceso a los complementos en su cuenta de Office 365. Solo tiene que abrir Outlook Web Access en un explorador y, a continuación, agregar `/owa/#path=/options/manageapps` a la dirección URL en la barra de dirección. Se abrirá la página **Administrar complementos**, donde puede habilitar [!INCLUDE[d365fin](includes/d365fin_md.md)] para Outlook. A continuación, al volver a Outlook, [!INCLUDE[d365fin](includes/d365fin_md.md)] debe estar disponible.  

De igual forma, en el cliente de escritorio de Outlook puede comprobar que [!INCLUDE[d365fin](includes/d365fin_md.md)] se muestran en la página **Administrar complementos**.  

En ambos casos, si [!INCLUDE[d365fin](includes/d365fin_md.md)] sigue sin estar disponible, tiene que obtener los archivos del manifiesto del complemento. Para obtener más información, póngase en contacto con su administrador de Office 365.

## <a name="see-also"></a>Consulte también

[Introducción](product-get-started.md)  
[Obtener Business Central en mi dispositivo móvil](install-mobile-app.md)  
[Enviar documentos por correo electrónico](ui-how-send-documents-email.md)  
[Finanzas](finance.md)  
[Ventas](sales-manage-sales.md)  
[Compras](purchasing-manage-purchasing.md)  

