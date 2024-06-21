---
title: Usar Business Central con Outlook
description: Este servicio tiene una integración profunda con Microsoft 365 lo que le permite administrar todas sus interacciones y correo de negocio con clientes y proveedores directamente en Outlook.
author: jswymer
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'SMTP, mail, Microsoft 365'
ms.date: 04/21/2022
ms.author: jswymer
ms.service: dynamics-365-business-central
ms.reviewer: jswymer
---
# Usar Business Central como su bandeja de entrada de empresa en Outlook

[!INCLUDE[prod_short](includes/prod_short.md)] ofrece un complemento que le permite gestionar las interacciones comerciales con sus clientes y proveedores directamente en Microsoft Outlook. Con los complementos de Outlook de [!INCLUDE[prod_short](includes/prod_short.md)], puede ver los datos financieros relativos a los clientes y los proveedores, así como crear y enviar documentos financieros, como por ejemplo presupuestos y facturas.

El complemento de [!INCLUDE[prod_short](includes/prod_short.md)] consta de dos complementos independientes que proporcionan las siguientes capacidades:

- Información del contacto

   Este complemento le permite buscar información del cliente o proveedor [!INCLUDE[prod_short](includes/prod_short.md)] en los correos electrónicos de Outlook y las citas del calendario. También le permite crear y enviar documentos comerciales de [!INCLUDE[prod_short](includes/prod_short.md)], como una oferta o factura de ventas a un contacto.

- Vista de documento

   Cuando se envía un documento comercia en un correo electrónico, el complemento proporciona un enlace directo en línea desde el cuerpo del correo electrónico al documento comercial real en [!INCLUDE[prod_short](includes/prod_short.md)].

## Introducción

1. Lo primero que debe hacer es obtener el complemento [!INCLUDE[prod_short](includes/prod_short.md)] instalado en Outlook. Es posible que su administrador ya haya instalado el complemento. Entonces, si no está seguro, consulte con su administrador o vea el siguiente paso para verificar si está instalado.

    Si el complemento no se ha instalado, consulte [Instale el complemento para su propio uso](admin-outlook.md#install). 

2. Con el complemento instalado, puede acceder al complemento **[!INCLUDE[prod_short](includes/prod_short.md)]** de cualquier mensaje de correo electrónico nuevo o existente o cita de calendario en Outlook.

    Empiece por iniciar sesión en Outlook y abrir un mensaje de correo electrónico. Luego, si está usando la aplicación Outlook, vaya a la cinta y busque **[!INCLUDE[prod_short](includes/prod_short.md)]**.  O si está usando Outlook en la web, en la parte superior o inferior del mensaje de correo electrónico, busque ![Icono del complemento Business Central en Outlook.](media/outlook-business-central-icon.png) o vaya a más acciones ![Muestrar más acciones para un correo electrónico en Outlook.](media/outlook-more-actions-button.png) .

    ![Acceda a los complementos de Business Central en Outlook.](media/outlook-business-central-addin.png)

   Si instaló el complemento por su cuenta y eligió recibir un correo electrónico de muestra, revise su bandeja de entrada para ver el correo electrónico de bienvenida. Este correo electrónico proporciona información para ayudarle a comenzar.

La primera vez que usa el complemento, en el panel del complemento [!INCLUDE[prod_short](includes/prod_short.md)], es posible que se le solicite que inicie sesión. En este caso, elija **Iniciar sesión ahora** y siga las instrucciones en pantalla para iniciar sesión en Business Central con su cuenta.

> [!TIP]
> Si usa el nuevo Outlook en la web, puede anclar **[!INCLUDE[prod_short](includes/prod_short.md)]** para que sea siempre visible de inmediato, en lugar de tener que ir al botón de más acciones, lo que hace que sea útil ver la información de los contactos mientras navega por diferentes correos electrónicos.

Para obtener más información, consulte [Usar complementos en Outlook en la web](https://support.office.com/article/using-add-ins-in-outlook-on-the-web-8f2ce816-5df4-44a5-958c-f7f9d6dabdce?ns=OLWAO365B&version=16).  

## Trabajar con contactos y documentos mediante el complemento Información detallada de contactos

Supongamos que recibe un correo electrónico de un cliente que desea obtener una oferta de algunos productos. Puede abrir el complemento [!INCLUDE[prod_short](includes/prod_short.md)] directamente en Outlook, que reconoce al remitente como cliente y abre la ficha de cliente para esa empresa. Desde este panel puede ver la información general del cliente, así como analizar en más detalle documentos específicos. También puede rebuscar en el historial de ventas del cliente. Si es un contacto nuevo, puede crearlo como nuevo en [!INCLUDE[prod_short](includes/prod_short.md)] sin salir de Outlook.  

En el complemento puede crear un presupuesto de ventas y reenviarlo a su cliente sin abandonar la ventana de Outlook. Toda la información que necesita para enviar el presupuesto de ventas está disponible en su bandeja de entrada de empresa de Outlook. Una vez tenga los datos introducidos puede registrar el presupuesto y enviarlo por correo electrónico. [!INCLUDE[prod_short](includes/prod_short.md)] genera un archivo .PDF con el presupuesto de ventas y lo adjunta al mensaje que tiene como borrador en el complemento.  

De igual forma, si recibe un correo electrónico de un proveedor, puede utilizar el complemento para trabajar con proveedores y facturas de compra.  

En ocasiones desea ver más campos de los que puede ver en el complemento, como cuando desea rellenar líneas en una factura. Para darle un poco más de espacio para trabajar con eso, puede abrir una página independiente con el complemento. Sigue formando parte de Outlook pero dispone de más espacio. Cuando introduce datos en el documento en la vista de ventana emergente, los cambios se guardan automáticamente. Las siguientes secciones le guiarán a través de algunas tareas básicas para ofrecerle una comprensión general de cómo usarlo.

> [!TIP]
> Las tareas explican cómo utilizar el complemento de un mensaje de correo electrónico. Pero puede hacer lo mismo desde una cita de calendario en Outlook.

### Buscar un contacto comercial al redactar un correo electrónico

1. Cree nuevo mensaje de correo electrónico.
2. En la cinta, vaya a **[!INCLUDE[prod_short](includes/prod_short.md)]** y elija **Información detallada de contactos**. O si está usando Outlook en la web, vaya a la parte inferior del mensaje de correo electrónico, elija ![Icono del complemento Business Central en Outlook.](media/outlook-business-central-icon.png) > **Información detallada de contactos**.
3. En el panel del complemento **[!INCLUDE[prod_short](includes/prod_short.md)]** que se abre, busque y elija el contacto que desee.

    Se muestra una descripción general del contacto en el panel y el contacto se agrega en la línea **Para** del correo electrónico.

### Ver y cambiar los datos de contacto o cambiar de empresa

La barra de acciones en la parte superior del panel del complemento [!INCLUDE[prod_short](includes/prod_short.md)] incluye varias acciones que le permiten profundizar en los detalles sobre el contacto y cambiar las cosas.

![Barra de acciones del complemento Business Central en Outlook.](media/outlook-addin-action-bar.png)

Por ejemplo, puede abrir los detalles de contacto completos como los vería en [!INCLUDE[prod_short](includes/prod_short.md)]. Si trabaja con más de una empresa de [!INCLUDE[prod_short](includes/prod_short.md)], puede cambiar fácilmente entre empresas.

### Hacer seguimiento de documentos entrantes

Quizás use la lista de **Documentos entrantes** en [!INCLUDE[prod_short](includes/prod_short.md)] para realizar un seguimiento de los documentos para su procesamiento que los proveedores le envían, como una factura de compra que debe pagarse. Si lo hace, puede crear fácilmente registros de documentos entrantes desde el complemento de Outlook e incluir los archivos adjuntos de correo electrónico.

1. Cuando reciba un correo electrónico de un proveedor que tenga un archivo adjunto, elija ![Icono del complemento Business Central en Outlook.](media/outlook-business-central-icon.png) **[!INCLUDE[prod_short](includes/prod_short.md)]**  > **Información detallada de contactos**.  

2. En la barra de acción del complemento, elija **Mostrar más acciones**, luego elija **Enviar a Documentos entrantes...**. .  

### Crear y enviar un nuevo documento a un contacto

1. En la cinta o en la parte inferior del mensaje de correo electrónico, elija ![Icono del complemento Business Central en Outlook.](media/outlook-business-central-icon.png) **[!INCLUDE[prod_short](includes/prod_short.md)]** > **Nuevo**, luego elija el tipo de documento que desea crear, como **Oferta de ventas**.
2. Realice cambios en el documento en el panel del complemento **[!INCLUDE[prod_short](includes/prod_short.md)]**.
3. Cuando el documento esté listo para enviarse al contacto, en la barra de acción, elija **Mostrar más acciones**, luego elija la acción **Enviar por correo electrónico**.

### Adjuntar archivos a registros

Su bandeja de entrada de correo electrónico suele ser un origen de archivos entrantes que inician o desbloquean flujos de trabajo. Los archivos pueden incluir cosas como pagos de facturas en PDF, fotos de mercancías o requisitos en un documento de Word. Cuando trabaje en Outlook con registros de Business Central como proveedores, clientes, facturas de compra o pedidos de venta, puede adjuntar estos archivos a los registros.

Hay un par de formas de adjuntar archivos. Una forma es cargar archivos desde su dispositivo. La otra forma es cargar archivos que se adjuntan a un correo electrónico. Por ejemplo, suponga que recibe un correo electrónico con archivos de un contacto. El complemento mostrará automáticamente el registro de contacto que coincide con el remitente del correo electrónico. Desde ahí, puede navegar hasta un documento del contacto, como el último pedido de venta. Una vez que haya identificado el pedido al que se refiere el correo electrónico, cargue rápidamente los archivos del correo electrónico a ese pedido.

![Muestra cómo agregar archivos adjuntos de un correo electrónico a registros en Business Central.](media/outlook-attach-files.png)

Después de adjuntar un archivo, los compañeros de trabajo pueden descargarlo y verlo instantáneamente desde el cuadro informativo **Archivos adjuntos** en cualquiera de sus clientes de Business Central. O bien, pueden abrir el archivo en OneDrive para compartir y colaborar con su departamento.

#### Cómo adjuntar un archivo

1. Abra el correo electrónico, seleccione ![Icono del complemento Business Central en Outlook.](media/outlook-business-central-icon.png) **[!INCLUDE[prod_short](includes/prod_short.md)]**  > **Información detallada de contactos**.
2. En la barra de acciones del complemento, seleccione **Mostrar más acciones** > **Archivos adjuntos**.

    La página **Documentos adjuntos** se abre para enumerar los documentos que ya están adjuntos al registro.
3. Elija **Archivos adjuntos...**, luego elija una de las siguientes opciones:

   - Elija **Adjuntar desde correo electrónico** para cargar todos los archivos o los seleccionados que se adjuntan al correo electrónico.
   - Elija **Cargar desde archivo** para cargar uno o archivos desde su dispositivo.

> [!NOTE]
> No puede adjuntar archivos a todos los registros. Esta función está disponible para los registros que utilizan el cuadro informativo **Archivos adjuntos**, como un proveedor, un cliente, una factura de compra o un pedido de ventas.

## Ver un documento de un correo electrónico con el complemento Document View

Ya sea un correo electrónico que envió o recibió, puede mostrar cualquier documento de [!INCLUDE[prod_short](includes/prod_short.md)], como la oferta de venta, directamente en Outlook. Desde allí, puede realizar cambios y navegar a la información relacionada, tal como lo haría desde dentro de [!INCLUDE[prod_short](includes/prod_short.md)].

Si está usando la aplicación de Outlook, simplemente elija **Vínculo de documento** en la parte superior del mensaje de correo electrónico. Para Outlook en la web, busque el vínculo de referencia del documento en el mensaje de correo electrónico. El texto del enlace de referencia incluirá el número de documento, que se basa en la serie de números utilizada en [!INCLUDE[prod_short](includes/prod_short.md)]. Por ejemplo, el enlace para una oferta de venta sería algo como **Oferta de venta S-QUO1000**.  

> [!TIP]
> A partir del primer lanzamiento de versiones de 2022, los documentos se abren en una nueva ventana del navegador con todas las funciones que ya conoce de [!INCLUDE [prod_short](includes/prod_short.md)]. Puede navegar de un documento a una lista y viceversa, abrir listas en Excel, enviar documentos para imprimir y ejecutar u obtener una vista previa de informes relacionados. También tiene todos los métodos abreviados de teclado familiares allí mismo cuando abre documentos desde Outlook.  

## Consulte también

[Preparación para hacer negocios](ui-get-ready-business.md)  
[Obtener Business Central en mi dispositivo móvil](install-mobile-app.md)  
[Enviar documentos por correo electrónico](ui-how-send-documents-email.md)  
[Finanzas](finance.md)  
[Ccial](sales-manage-sales.md)  
[Compras](purchasing-manage-purchasing.md)  
[Requisitos mínimos para Outlook](product-requirements.md#outlook)  
[Usar complementos en Outlook en la web](https://support.office.com/article/Using-Add-ins-in-Outlook-on-the-web-8f2ce816-5df4-44a5-958c-f7f9d6dabdce?appver=OWB150)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
