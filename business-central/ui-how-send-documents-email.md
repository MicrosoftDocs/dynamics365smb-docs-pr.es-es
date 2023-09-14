---
title: Enviar documentos y correo electrónico
description: 'Puede definir el contenido que se insertará en el cuerpo de un mensaje de correo electrónico, por ejemplo, un vínculo de PayPal. También es posible adjuntar documentos a los mensajes de correo electrónico.'
author: brentholtorf
ms.topic: conceptual
ms.workload: na
ms.search.keywords: 'SMTP, mail, Microsoft 365, cover, body, PayPal, layout'
ms.search.form: '41,'
ms.date: 04/01/2021
ms.author: bholtorf
---
# Enviar documentos y correo electrónico

Puede compartir fácilmente información y documentos, como órdenes de compra y venta y facturas, por correo electrónico directamente desde [!INCLUDE[prod_short](includes/prod_short.md)], sin tener que abrir una aplicación de correo electrónico.  

Puede enviar casi todos los tipos de documentos como archivos adjuntos PDF. Alternativamente, puede configurar un diseño de informe que incluya información del documento en el texto del correo electrónico, junto con texto que haga que el correo electrónico sea más amigable, por ejemplo, un saludo estándar. Para obtener más información, vea [Administrar diseños de informes y documentos](ui-manage-report-layouts.md).

Cuando envía facturas, puede facilitar que los clientes realicen pagos a través de un servicio de pago, como PayPal, agregando automáticamente información y un enlace al servicio en el correo electrónico. Para obtener más información, consulte [Permitir pagos de cliente a través de servicios de pago](sales-how-enable-payment-service-extensions.md).

Para activar los correos electrónicos en [!INCLUDE[prod_short](includes/prod_short.md)], inicie la guía de configuración asistida **Configurar correo electrónico**. Para obtener más información, consulte [Configurar correo electrónico](admin-how-setup-email.md).

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_short.md)] solo admite comunicaciones de correo electrónico salientes. Tampoco puede recibir respuestas desde la aplicación.

## Para enviar documentos por correo electrónico

Este procedimiento describe cómo adjuntar una factura de venta registrada a un correo electrónico como un archivo PDF y con el texto del correo electrónico específico del documento. Los pasos son los mismos para otros documentos.

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Histórico facturas venta** y luego elija el enlace relacionado.
2. Seleccione la factura, elija la acción **Imprimir/Enviar** y, después, elija **Enviar por correo electrónico**.
3. en el campo **Correo electrónico** elija **Sí (Mensaje para configuración)**. Para obtener más información, vea [Configurar los perfiles de envío de documentos](sales-how-setup-document-send-profiles.md).

    Si el campo **Correo electrónico** en la página **Enviar documento a** se establece en **Sí (Mensaje para configuración)**, se abre la página **Enviar correo electrónico** rellenada previamente con el contacto en el campo **Para:** y el documento adjunto es un archivo PDF. En el campo **Cuerpo**, puede introducir tanto el texto manualmente como disponer del campo rellenado con un contenido específico de un documento en el cuerpo del correo electrónico que ha configurado.

4. Elija el botón **Aceptar**.
5. En el campo **Para:** introduzca una dirección de correo electrónico válida. El valor predeterminado es la dirección de correo electrónico del cliente.
6. En el campo **Asunto**, escriba un texto descriptivo del asunto. El valor predeterminado es el nombre del cliente y el número de factura.
7. En el campo **Archivo adjunto**, se adjunta la factura generada de forma predeterminada como un archivo PDF.
8. En el campo **Cuerpo**, escriba un mensaje breve al destinatario.

    Si se configura el contenido específico de un documento en el texto del correo electrónico en la página **Informe selección - ventas**, el campo **Cuerpo** se rellena automáticamente. Para más información, vea [Configurar textos y diseños de correo electrónico reutilizables](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts).
9. Haga clic en el botón **Aceptar** para enviar el correo electrónico.

> [!NOTE]  
> Si no desea especificar la configuración del correo electrónico cada vez que envíe un documento, puede seleccionar la opción **Sí (Usar configuración predeterminada)** en el campo **Correo electrónico** en la página **Enviar documento a**. En ese caso, la página **Enviar correo electrónico** no se abrirá. Consulte el paso 4. Para obtener más información, vea [Configurar los perfiles de envío de documentos](sales-how-setup-document-send-profiles.md).  

## Para redactar y enviar un correo electrónico

Puede redactar rápidamente correos electrónicos para contactos, clientes, proveedores, vendedores/compradores y cuentas bancarias directamente desde las páginas de esas entidades. Solo tiene que elegir **Proceso** y luego **Enviar correo electrónico** para abrir el editor de correo electrónico. Para cuentas bancarias, la acción **Enviar correo electrónico** está en **Acciones**.

> [!TIP]
> Si a menudo envía mensajes de correo electrónico que son de naturaleza similar, o desea enviar una comunicación masiva, por ejemplo, para anunciar una campaña de ventas, el uso de plantillas de Word con correo electrónico puede acelerar el proceso. Puede crear una plantilla para entidades como clientes, proveedores y contactos, que generará el contenido de un mensaje de correo electrónico por usted e incluso personalizará el contenido para el destinatario en función de los datos en [!INCLUDE[prod_short](includes/prod_short.md)]. Para obtener más información, consulte [Usar plantillas de Word para comunicación masiva](ui-mail-merge.md).  

### Adjuntar un documento a un correo electrónico

Hay varias formas de adjuntar documentos a los correos electrónicos.

Si está asignado a un escenario de correo electrónico relacionado con la entidad a la que está enviando el correo electrónico o el documento que está enviando, es posible que se agregue automáticamente un archivo adjunto a su mensaje. Esto se debe a que se ha asignado un archivo adjunto predeterminado al escenario de correo electrónico. Puede eliminar el archivo adjunto si no desea enviarlo con su mensaje. Para más información, vea [Asignar escenarios de correo electrónico a cuentas de correo electrónico](admin-how-setup-email.md#assign-email-scenarios-to-email-accounts). 

Para adjuntar un archivo usted mismo, en el editor de correo electrónico, use las siguientes acciones:

* Elija **Agregar archivo** para seleccionar un archivo.
* Elija **Agregar archivos de la selección predeterminada** para agregar manualmente un archivo asociado con el escenario de correo electrónico.
* Elija **Agregar archivo del documento de origen** para elegir un archivo adjunto al documento con el que está trabajando. Los archivos se adjuntan al propio documento o a una o más de sus líneas.

## Documentos marcados como impresos cuando se envían

Algunos documentos de [!INCLUDE[prod_short](includes/prod_short.md)] tienen un campo que especifica cuántas veces se ha impreso el documento. El número en ese campo <!--"that field?" need a name...--> también se actualiza si envía el documento por correo electrónico porque se genera un archivo PDF para él. El número se actualiza incluso si no envía el correo electrónico. <!--guessing this is because emails are technically reports, so the counter bumps up whenever someone creates an email. Need to verify.-->

## Correos electrónicos enviados y su bandeja de salida de correo electrónico

[!INCLUDE[prod_short](includes/prod_short.md)] almacena los correos electrónicos que envía en la página **Elementos enviados**. Eso le permite reenviar correos electrónicos o reenviarlos a otra persona. Si no puede encontrar un correo electrónico en sus artículos enviados, búsquelo en la página **Bandeja de salida de correo electrónico**. 

> [!NOTE]
> Dependiendo de la extensión que su empresa utilice para el correo electrónico, los administradores pueden ver una lista de mensajes que todos han enviado, pero no el contenido de los mensajes.

La **Bandeja de salida de correo electrónico** es donde encontrará los correos electrónicos que guardó como borradores y los correos electrónicos que no se pudieron enviar, por ejemplo, si la dirección de correo electrónico no era válida. Para los mensajes que no se pudieron enviar, puede elegir **Mostrar error** o **Investigar error** para solucionar el problema.  

## Consultar la [formación de Microsoft](/training/modules/set-up-email/) relacionada

## Consulte también

[Administrar diseños de informes y documentos](ui-manage-report-layouts.md)  
[Configurar correo electrónico](admin-how-setup-email.md)  
[Facturar ventas](sales-how-invoice-sales.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
