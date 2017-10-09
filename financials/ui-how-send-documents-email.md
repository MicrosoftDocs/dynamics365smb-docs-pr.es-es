---
title: "Configurar contenido y datos adjuntos específicos de documento para mensajes de correo electrónico | Documentos de Microsoft"
description: "Puede definir el contenido que se insertará en el cuerpo de un mensaje de correo electrónico, por ejemplo, un vínculo de PayPal. También es posible adjuntar documentos a los mensajes de correo electrónico."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: SMTP, mail, Office 365, cover, body, PayPal, layout
ms.date: 03/30/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: afc73b146ce3c95ea47ac935e826b27f0a18d325
ms.contentlocale: es-es
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-send-documents-by-email"></a>Procedimiento: Enviar documentos por correo electrónico.
Para comunicar el contenido de documentos empresariales rápidamente a sus socios, por ejemplo la información de pagos en los documentos de venta a los clientes, puede usar la función de Informe personalizado para definir el contenido específico de un documento que se insertará en el cuerpo del correo electrónico automáticamente. Para obtener más información, vea [Administrar diseños de informes y documentos](ui-manage-report-layouts.md).

Para activar los correos electrónicos en [!INCLUDE[d365fin](includes/d365fin_md.md)], inicie la guía de configuración **Configurar correo electrónico** en la página principal.

Puede enviar por correo electrónico prácticamente todos los tipos de documento como archivos adjuntos en el mensaje directamente desde la ventana que muestra el documento. Además del archivo adjunto, puede configurar contenido específico de un documento en el cuerpo del correo electrónico con la información principal de ése documento, precedida por el texto estándar que saluda al destinatario del correo e introduce el documento en cuestión. Para ofrecer a sus clientes el pago de las ventas de forma electrónica usando un servicio de pago, como por ejemplo PayPal, puede disponer también de su información y su hipervínculo en el cuerpo del correo.

A partir de todos los documentos soportados, se inicia el envío del correo seleccionando la acción **Enviar** en los documentos registrados, o la acción **Registrar y enviar** en los documentos no registrados.

Si el campo **Correo electrónico** en la ventana **Enviar documento a** se establece en **Sí (Mensaje para configuración)**, se abre la ventana **Enviar correo electrónico** rellenada previamente con el contacto en el campo **Para:** y el documento adjunto es un archivo PDF. En el campo **Cuerpo**, puede introducir tanto el texto manualmente como disponer del campo rellenado con un contenido específico de un documento en el cuerpo del correo electrónico que ha configurado.

El procedimiento siguiente describe cómo configurar el informe **Ventas - Factura** para usarlo como contenido específico en el cuerpo del correo cuando envíe las facturas de venta registradas.

## <a name="to-set-up-a-document-specific-email-body-for-sales-invoices"></a>Para configurar un documento específico en el cuerpo de un correo electrónico para las facturas de venta
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Selección informes ventas** y, a continuación, seleccione el vínculo relacionado.
2. En la ventana **Informe selección - ventas**, en el campo **Uso**, seleccione **Facturar**.
3. En una línea nueva, en el campo **Id. informe**, seleccione, por ejemplo, informe estándar 1306.
4. Seleccione la casilla **Usar para el cuerpo del correo electrónico**.
5. Elija el campo **Código de diseño del cuerpo del correo electrónico** y seleccione una plantilla en la lista desplegable.

    Las plantillas de informes definen tanto el estilo como el contenido del cuerpo del correo, incluyendo el texto estándar que precede la información principal del documento. Puede ver todos los diseños de informe disponibles si elige el botón **Seleccionar de la lista completa** en la lista desplegable.
6. Para ver o editar el diseño en el que se basa el cuerpo del correo electrónico, seleccione el diseño en la ventana **Diseños de informe personalizados** y, a continuación, elija la acción **Editar diseño**.
7. Si desea ofrecer a sus clientes el pago de las ventas de forma electrónica puede configurar el servicio de pago relacionado, como por ejemplo PayPal y, a continuación, puede disponer también de su información y su hipervínculo en el cuerpo del correo. Para obtener más información, consulte [Procedimiento: Permitir pagos de cliente a través de PayPal](sales-how-enable-payment-service-extensions.md).
8. Elija el botón **Aceptar**.

Ahora bien, cuando selecciona, por ejemplo, la acción **Enviar** en la ventana **Factura venta reg.**, el cuerpo del correo electrónico contendrá la información del documento del informe 1306 precedida por el texto estándar siguiendo el diseño de informe que seleccionó en el paso 5.

El procedimiento siguiente describe cómo enviar una factura de ventas registrada como un mensaje de correo electrónico con un documento adjunto en formato PDF y con un contenido específico en el cuerpo del correo.

## <a name="to-send-documents-by-email"></a>Para enviar documentos por correo electrónico
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Facturas de ventas registradas** y, a continuación, elija el vínculo relacionado.
2. Seleccione la factura de ventas registrada relevante y, a continuación, elija la acción **Enviar**. Se abre la ventana **Enviar documento a**.
3. en el campo **Correo electrónico** seleccione **Sí (Mensaje para configuración)**. Para obtener más información, vea [Procedimiento: Configurar los perfiles de envío de documentos](sales-how-setup-document-send-profiles.md).
4. Elija el botón **Aceptar**. Se abre la ventana **Enviar correo electrónico**.
5. En el campo **Para:** introduzca una dirección de correo electrónico válida. El valor predeterminado es la dirección de correo electrónico del cliente.
6. En el campo **Asunto**, escriba un texto descriptivo del asunto. El valor predeterminado es el nombre del cliente y el número de factura.
7. En el campo **Archivo adjunto**, se adjunta la factura generada de forma predeterminada como un archivo PDF. Seleccione el botón de búsqueda para abrir el archivo o para adjuntar otro.
8. En el campo **Cuerpo**, escriba un mensaje breve al destinatario.

    Si se configura el contenido específico de un documento en el cuerpo del correo electrónico en la ventana **Informe selección - Ventas**, el campo **Cuerpo** se rellena automáticamente. Para obtener más información, vea "Para configurar un contenido específico de un documento en el cuerpo del correo electrónico para las facturas de venta" en este tema.
9. Haga clic en el botón **Aceptar** para enviar el correo electrónico.

> [!NOTE]  
>   Si no desea especificar la configuración del correo electrónico cada vez que envíe un documento, puede seleccionar la opción **Sí (Usar configuración predeterminada)** en el campo **Correo electrónico** en la ventana **Enviar documento a**. En ese caso, la ventana **Enviar correo electrónico** no se abrirá. Consulte el paso 4. Para obtener más información, vea [Procedimiento: Configurar los perfiles de envío de documentos](sales-how-setup-document-send-profiles.md).

## <a name="see-also"></a>Consulte también
[Administrar diseños de informes y documentos](ui-manage-report-layouts.md)  
[Configurar el correo electrónico](madeira-how-setup-email.md)  
[Facturación de ventas](sales-how-invoice-sales.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

