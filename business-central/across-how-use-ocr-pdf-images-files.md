---
title: Usar OCR para convertir PDF en facturas electrónicas
description: Describe cómo puede utilizar un servicio de OCR para convertir los archivos PDF de entrada o de imagen en documentos electrónicos.
documentationcenter: ''
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice'
ms.date: 06/14/2022
ms.author: edupont
---
# <a name="use-ocr-to-turn-pdf-and-image-files-into-electronic-documents"></a><a name="use-ocr-to-turn-pdf-and-image-files-into-electronic-documents"></a><a name="use-ocr-to-turn-pdf-and-image-files-into-electronic-documents"></a><a name="use-ocr-to-turn-pdf-and-image-files-into-electronic-documents"></a>Utilizar el servicio OCR para convertir archivos PDF y de imagen en documentos electrónicos

A partir de archivos PDF o de imagen que reciba desde sus socios comerciales podrá hacer que un servicio externo de OCR (reconocimiento óptico de caracteres) genere documentos electrónicos que se podrán convertir a registros de documentos en [!INCLUDE[prod_short](includes/prod_short.md)]. Por ejemplo, cuando recibe una factura de un proveedor en formato PDF, la puede [enviar al servicio de OCR desde la página **Documentos entrantes**](#to-send-a-pdf-or-image-file-to-the-ocr-service-from-the-incoming-documents-page).

Como alternativa al envío del archivo desde la página **Documentos entrantes**, el servicio OCR puede ofrecer la opción de [procesar archivos reenviados a una dirección de correo electrónico dedicada](#to-send-a-pdf-or-image-file-to-the-ocr-service-by-email). A continuación, cuando vuelve a recibir el documento electrónico, se crea automáticamente un registro de documento entrante en [!INCLUDE[prod_short](includes/prod_short.md)].

Después de unos segundos, el servicio OCR enviará el archivo procesado a la página **Documentos entrantes** como un registro de documento electrónico que se puede [convertir en una factura de compra para el proveedor](#to-receive-the-resulting-electronic-document-from-the-ocr-service), una factura de venta, una nota de crédito o un asiento de diario.

Como el OCR se basa en el reconocimiento óptico, es probable que el servicio de OCR interprete de forma incorrecta algunos caracteres del PDF o de los archivos de imagen la primera vez que procese documentos de un determinado proveedor, por ejemplo. Puede que no interprete el logotipo de la compañía como el nombre del proveedor o que pueda malinterpretar la cantidad total de un recibo debido a su diseño. Para evitar estos errores en el futuro, puede corregirlos en una versión separada de la página **Documentos entrantes**. A continuación, debe enviar de vuelta las correcciones al servicio OCR para entrenarle para que interprete los caracteres y campos específicos correctamente la próxima vez que procese un documento PDF o de imagen para el mismo proveedor. Para obtener más información, consulte [Entrenar el servicio OCR para evitar errores](across-how-use-ocr-pdf-images-files.md#to-train-the-ocr-service-to-avoid-errors).

El tráfico de archivos hacia y desde el servicio OCR se procesa mediante una entrada de cola de trabajo dedicada. Esta cola de trabajos se crea automáticamente cuando habilita la conexión del servicio OCR externo. Para obtener más información, vea [Configurar documentos entrantes](across-how-setup-income-documents.md).

> [!NOTE]
> La característica OCR la proporcionan proveedores externos. Elija un paquete de servicios que sea apropiado para su organización y o el país o la región. Encuentre servicios compatibles con [!INCLUDE[prod_short](includes/prod_short.md)] y detalles sobre las características disponibles en [AppSource.microsoft.com ](https://go.microsoft.com/fwlink/?linkid=2081646).

## <a name="to-send-a-pdf-or-image-file-to-the-ocr-service-from-the-incoming-documents-page"></a><a name="to-send-a-pdf-or-image-file-to-the-ocr-service-from-the-incoming-documents-page"></a><a name="to-send-a-pdf-or-image-file-to-the-ocr-service-from-the-incoming-documents-page"></a><a name="to-send-a-pdf-or-image-file-to-the-ocr-service-from-the-incoming-documents-page"></a>Para enviar un archivo PDF o de imagen al servicio OCR desde la página Documentos entrantes

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Documentos entrantes** y luego elija el enlace relacionado.
2. Cree un nuevo registro de documento entrante y adjunte el archivo. Para obtener más información, vea [Crear registros de documentos entrantes](across-how-create-income-document-records.md).  
3. En la página **Documentos entrantes**, seleccione una o más líneas y, a continuación, seleccione la acción **Enviar a cola de trabajos**.

   El valor del campo **Estado OCR** cambia a **Listo** . El archivo PDF o de imagen adjunto se envía al servicio OCR mediante la cola de proyectos, según la programación, si no hay errores.
4. De forma alternativa, en la página **Documentos entrantes**, seleccione una o más líneas y, a continuación, seleccione la acción **Enviar a servicio OCR** para el envío automático de los archivos para su procesamiento.

   El valor del campo **Estado OCR** cambia a **Enviado**, si no hay errores.

## <a name="to-send-a-pdf-or-image-file-to-the-ocr-service-by-email"></a><a name="to-send-a-pdf-or-image-file-to-the-ocr-service-by-email"></a><a name="to-send-a-pdf-or-image-file-to-the-ocr-service-by-email"></a><a name="to-send-a-pdf-or-image-file-to-the-ocr-service-by-email"></a>Para enviar un archivo PDF o de imagen al servicio OCR por correo electrónico

Desde su aplicación de correo electrónico, puede reenviar un correo electrónico al proveedor del servicio OCR con el archivo PDF o de imagen adjunto. Para obtener información acerca de la dirección de correo electrónico a la que enviar el archivo, consulte el sitio web del proveedor del servicio OCR.

Dado que no existe ningún registro de documento entrante para el archivo, se creará automáticamente un nuevo registro en la página **Documentos entrantes** cuando el servici OCR envíe el documento electrónico resultante. Para obtener más información, vea [Crear registros de documentos entrantes](across-how-create-income-document-records.md).

> [!NOTE]  
> Si trabaja con una tableta o un teléfono, puede enviar el archivo al servicio OCR en cuanto haya tomado una foto del documento o puede crear un documento entrante directamente. Para obtener más información, vea [Crear un documento entrante tomando una foto](across-how-create-income-document-records.md#create-an-incoming-document-record-by-taking-a-photo).

## <a name="to-receive-the-resulting-electronic-document-from-the-ocr-service"></a><a name="to-receive-the-resulting-electronic-document-from-the-ocr-service"></a><a name="to-receive-the-resulting-electronic-document-from-the-ocr-service"></a><a name="to-receive-the-resulting-electronic-document-from-the-ocr-service"></a>Para recibir el documento electrónico resultante desde el servicio OCR

El documento electrónico que se crea por el servicio de OCR desde un archivo PDF o de imagen, se recibe automáticamente en la página **Documentos entrantes** por el movimiento de cola de proyectos que se configura cuando activa el servicio de OCR.

Si no utiliza una cola de proyectos o desea recibir el documento final de OCR antes de lo acordado, puede elegir la acción **Recibir desde el servicio OCR**. Esta opción obtendrá los documentos que el servicio de OCR haya completado.

> [!NOTE]  
> Si el servicio de OCR está configurado para requerir la verificación manual de los documentos procesados, el campo **Estado OCR** contendrá **Esperando verificación**. En ese caso, ejecute los pasos siguientes para iniciar sesión en el sitio web del servicio de OCR para comprobar manualmente un documento de OCR.

1. En el campo **Estado OCR**, seleccione el hipervínculo **Esperando verificación**.
2. En el sitio web del servicio de OCR, inicie sesión con las credenciales de su cuenta de OCR. Para obtener más información, vea [Configurar un servicio OCR](across-how-setup-income-documents.md#to-set-up-an-ocr-service).

   La información del documento de OCR muestra tanto el contenido original del archivo PDF o de imagen como los valores del archivo de OCR resultantes.
3. Revise los valores de campo y edite o introduzca valores manualmente en los campos donde el servicio de OCR se ha marcado como no seguro.
4. Elija el botón **Aceptar**. El proceso de OCR se ha completado y el documento electrónico resultante se ha enviado a la página **Documentos entrantes** en [!INCLUDE[prod_short](includes/prod_short.md)], de acuerdo con la programación de las colas de proyectos.
5. Repita los pasos 2 a 4 para que se verifique cualquier otro documento de OCR.

Ahora puede empezar a crear los documentos de registro para los documentos electrónicos recibidos en [!INCLUDE[prod_short](includes/prod_short.md)], de forma manual o automática. Para obtener más información, consulte el procedimiento siguiente. También puede [conectar el registro del documento entrante nuevo al documento registrado o no registrado existente](across-how-connect-disconnect-income-document-records.md) de forma que el archivo de origen sea fácilmente accesible desde [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="to-create-a-purchase-invoice-from-an-electronic-document-received-from-the-ocr-service"></a><a name="to-create-a-purchase-invoice-from-an-electronic-document-received-from-the-ocr-service"></a><a name="to-create-a-purchase-invoice-from-an-electronic-document-received-from-the-ocr-service"></a><a name="to-create-a-purchase-invoice-from-an-electronic-document-received-from-the-ocr-service"></a>Para crear una factura de compra desde un documento electrónico recibido del servicio de OCR

El procedimiento siguiente describe cómo crear un registro de la factura de compra desde una factura recibida de un proveedor como un documento electrónico del servicio OCR. El procedimiento es el mismo que cuando crea, por ejemplo, una línea de diario general desde un recibo de gastos o un pedido de devolución de ventas desde un cliente.

> [!NOTE]  
> Los campos **Descripción** y **N.°** de las líneas creadas del documento se completarán solo si primero ha asignado el texto encontrado en el documento de OCR a los campos de [!INCLUDE[prod_short](includes/prod_short.md)]. Puede realizar esta asignándolas como las referencias de producto, para las líneas de documentos del tipo Producto. Para obtener más información, vea [Usar referencias de producto](inventory-how-use-item-cross-refs.md). También puede utilizar la función **Asignación de texto a cuenta**. Para obtener más información, consulte [Asignar texto en un documento entrante a un proveedor específico, C/G o cuenta bancaria](across-how-use-ocr-pdf-images-files.md#to-map-text-on-an-incoming-document-to-a-specific-vendor-account).

1. Seleccione la línea del documento entrante y, a continuación, seleccione la acción **Crear documento**.

Una factura de compra se creará en [!INCLUDE[prod_short](includes/prod_short.md)] según la información del documento electrónico del proveedor que recibió del servicio OCR. La información se insertará en la nueva factura de compra en función de la asignación que haya definido como una referencia o como asignación de texto a cuenta.

Los errores de validación, normalmente relacionados con datos maestros incorrectos o no presentes en [!INCLUDE[prod_short](includes/prod_short.md)], se mostrarán en la ficha desplegable **Errores y advertencias**. Para obtener más información, consulte [Gestionar errores al recibir documentos electrónicos](across-how-use-ocr-pdf-images-files.md#to-handle-errors-when-receiving-electronic-documents).

### <a name="to-map-text-on-an-incoming-document-to-a-specific-vendor-account"></a><a name="to-map-text-on-an-incoming-document-to-a-specific-vendor-account"></a><a name="to-map-text-on-an-incoming-document-to-a-specific-vendor-account"></a><a name="to-map-text-on-an-incoming-document-to-a-specific-vendor-account"></a>Para asignar texto en un documento entrante a una cuenta de proveedor específica

Para los documentos entrantes, normalmente usa la acción **Asignar texto a cuenta** para indicar que un determinado texto en una factura de proveedor recibida desde el servicio de OCR se ha asignado a una cuenta de un proveedor determinado. En el futuro, cualquier parte de la descripción del documento entrante que exista como texto de asignación significa que el campo **Número de proveedor** en el documento resultante o las líneas de diario de tipo *Cuenta de contabilidad* se rellenan con el proveedor en cuestión.

Además de asignarlo a una cuenta de proveedor o a cuentas de contabilidad, también puede asignar texto a una cuenta bancaria. Esta opción es útil, por ejemplo, en los documentos electrónicos de gastos que ya se han pagado, y para los que desea crear una línea de diario general que esté lista para registrarse en una cuenta bancaria.

1. Seleccione la línea de movimiento correspondiente del documento y seleccione la acción **Asignar texto a cuenta**. Se abre la página **Asignación de texto a cuenta**.
2. En el campo **Asignación de texto**, introduzca el texto que aparecerá en las facturas de proveedor para el que desee crear documentos de compras o líneas de diario. Puede escribir hasta 50 caracteres.
3. En el campo **Nº proveedor**, escriba el proveedor para el que se creará el documento de compra o la línea del diario resultante.
4. En el campo **N.º cta. débito**, escriba la cuenta de tipo de débito que se insertará en el documento de compra resultante o en la línea del diario de la cuenta.
5. En el campo **N.º cta. crédito**, escriba la cuenta de tipo de crédito que se insertará en el documento de compra resultante o en la línea del diario de la cuenta.

   > [!NOTE]
   > No utilice los campos **Tipo origen contr.** y **N.º origen contr.** en relación con documentos entrantes. Se usan solo para la conciliación automática de pagos. Para más información, consulte [Asignación de texto en pagos periódicos a cuentas para conciliación automática](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md).
6. Repita los pasos 2 a 5 para todo el texto de los documentos entrantes para los que desea crear documentos automáticamente.

## <a name="to-handle-errors-when-receiving-electronic-documents"></a><a name="to-handle-errors-when-receiving-electronic-documents"></a><a name="to-handle-errors-when-receiving-electronic-documents"></a><a name="to-handle-errors-when-receiving-electronic-documents"></a>Para gestionar errores al recibir documentos electrónicos

1. En la página **Documentos entrantes**, seleccione la línea de un documento entrante recibido del servicio OCR que contenga errores, indicada por el valor *Error* en el campo **Estado OCR**.
2. Seleccione la acción **Editar** para abrir la página **Documento entrante**.
3. En la ficha desplegable **Errores y advertencias**, seleccione el mensaje y, a continuación, elija la acción **Abrir registro relacionado**.
4. Se abrirá la página que contiene los datos incorrectos o que faltan, como una ficha de proveedor en la que falte un valor de campo.
5. Corrija el error o los errores tal como se describe en cada mensaje de error.
6. Continúe para procesar el documento electrónico entrante volviendo a seleccionar la acción **Crear manualmente**.
7. Repita los pasos del 5 al 6 para los errores pendientes hasta que el documento electrónico se pueda recibir correctamente.

## <a name="to-train-the-ocr-service-to-avoid-errors"></a><a name="to-train-the-ocr-service-to-avoid-errors"></a><a name="to-train-the-ocr-service-to-avoid-errors"></a><a name="to-train-the-ocr-service-to-avoid-errors"></a>Para preparar al servicio OCR para evitar errores

Como el OCR se basa en el reconocimiento óptico, puede que el servicio de OCR interprete de forma incorrecta algunos caracteres del PDF o de los archivos de imagen la primera vez que procese documentos de un determinado proveedor, por ejemplo. Puede que no interprete el logotipo de la compañía como el nombre del proveedor o que pueda malinterpretar la cantidad total de un recibo de gastos debido a su diseño. Para evitar que sigan ocurriendo este tipo de errores, puedes corregir los datos recibidos por el servicio de OCR y después enviar comentarios al servicio.

La página **Corrección de datos de OCR** que abrió desde la página **Documentos entrantes**, muestra los campos de la ficha desplegable **Información financiera** en dos columnas, una con los datos editables del OCR y la otra con los datos de solo lectura. Cuando selecciona el botón **Enviar comentarios sobre OCR** se envía el contenido de la página **Corrección de datos de OCR** al servicio de OCR. La próxima vez que el servicio procese PDF o archivos de imagen que contengan los datos en cuestión, se incorporarán sus correcciones para mejorar el reconocimiento de documentos.

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Documentos entrantes** y luego elija el enlace relacionado.
2. Abra un registro de documentos entrantes que contenga los datos recibidos del servicio OCR que desea corregir.
3. En la página **Documentos entrantes**, seleccione la acción **Corregir datos de OCR**.
4. En la página **Corrección de datos de OCR**, sobrescriba los datos en la columna editable para cada campo que tenga un valor incorrecto.
5. Para deshacer las correcciones que se hayan realizado desde que se abrió la página **Corrección de datos de OCR**, seleccione la acción **Restablecer datos de OCR**.
6. Para enviar las correcciones al servicio OCR, seleccione la acción **Enviar comentarios sobre OCR**.
7. Para guardar las correcciones, cierre la página **Corrección de datos de OCR**.

Los campos de la ficha desplegable **Información financiera** en la página **Documento entrante** se actualizan con los valores nuevos que introdujo en el paso 4.

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Consultar la [formación de Microsoft](/training/modules/incoming-documents-dynamics-365-business-central/) relacionada

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Consulte también .

[Crear registros de documentos entrantes](across-how-create-income-document-records.md)
[Cree registros de documentos entrantes directamente desde documentos y entradas](across-how-connect-disconnect-income-document-records.md)
[Documentos entrantes](across-income-documents.md)  
[Compras](purchasing-manage-purchasing.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
