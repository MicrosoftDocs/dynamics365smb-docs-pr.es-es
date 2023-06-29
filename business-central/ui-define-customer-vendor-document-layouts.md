---
title: Asignar diseños de documentos a clientes o proveedores
description: 'Utilice diseños de documentos para controlar la apariencia y el formato de documentos, como facturas y pedidos, que envía a clientes y proveedores.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'customized report, document layout, logo, personalize'
ms.search.form: '21, 9650'
ms.date: 04/07/2022
ms.author: edupont
---
# <a name="define-document-layouts-for-customers-and-vendors"></a><a name="define-document-layouts-for-customers-and-vendors"></a><a name="define-document-layouts-for-customers-and-vendors"></a>Definir diseños de documentos para clientes y proveedores

Los diseños de documentos usan diseños de informes para definir la apariencia de los documentos que envía a clientes y proveedores. Business Central proporciona diseños estándar, pero también puede adaptar diseños personalizados para cada uno de sus socios comerciales. Para obtener más información, vea [Crear y modificar diseños de informe personalizados](ui-how-create-custom-report-layout.md). Puede seleccionar diseños de documentos estándar y personalizados de las fichas de cliente y proveedor eligiendo la acción **Diseños de documentos**. El valor en el campo **Uso** define el proceso para el que se utiliza el diseño de documentos. Por ejemplo, para los clientes, puede utilizar los tipos de diseño de documentos **Recordatorio**, **Envío** y **Confirmación**.

Los diseños de documentos también pueden ahorrarle tiempo cuando envía documentos a contactos de clientes o proveedores por correo electrónico. Para cada diseño que asigne al cliente o contacto, puede especificar una o más direcciones de correo electrónico de contacto. Por ejemplo, puede enviar una factura a los contactos de compras y almacén del cliente. Agregar direcciones de correo electrónico de contacto es fácil. En la página **Diseños de documento**, la acción **Seleccionar correo electrónico de contactos** le permite elegir entre una lista de direcciones de correo electrónico de contacto que usted haya registrado para el cliente o proveedor. También puede agregar direcciones de correo electrónico manualmente. Si ingresa varias direcciones, sepárelas con un punto y coma y no agregue espacios entre las direcciones.

Antes de poder definir qué diseño de documento usar para cada proceso y a qué contacto enviar el documento, debe cargar todos los informes disponibles (documentos) desde la página **Seleccionar selecciones**. Puede cargar rápidamente los documentos utilizando la acción **Copiar desde selección de informe** en la página **Diseños de documentos**.

Los pasos en las siguientes secciones describen cómo definir diseños de documentos de venta desde la página **Ficha cliente**. Para los proveedores, los pasos son los mismos que desde la página **Ficha proveedor**.

## <a name="to-load-the-standard-document-layouts-for-sales-documents-for-a-customer"></a><a name="to-load-the-standard-document-layouts-for-sales-documents-for-a-customer"></a><a name="to-load-the-standard-document-layouts-for-sales-documents-for-a-customer"></a>Para cargar los diseños de documentos estándar para documentos de ventas de un cliente

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Clientes** y luego elija el enlace relacionado.
2. Abra la página **Ficha cliente** para el cliente y, a continuación, elija la acción **Diseños de documentos**.
3. En la página **Diseños de documentos**, elija la acción **Copiar desde selección de informe**.

La página **Diseños de documentos** muestra todos los diseños que están disponibles para documentos de ventas. 

## <a name="to-select-a-custom-report-layout-to-use-for-the-sales-document-layout"></a><a name="to-select-a-custom-report-layout-to-use-for-the-sales-document-layout"></a><a name="to-select-a-custom-report-layout-to-use-for-the-sales-document-layout"></a>Para seleccionar un diseño de informe personalizado para usar para el diseño de documento de venta

Si aún no ha creado un diseño de informe personalizado para el tipo de documento, deberá hacerlo primero. Para obtener más información, vea [Crear y modificar diseños de informe personalizados](ui-how-create-custom-report-layout.md).

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Clientes** y luego elija el enlace relacionado.
2. Abra la página **Ficha cliente** para el cliente y, a continuación, elija la acción **Diseños de documentos**.
3. En la página **Diseños de documento**, en la línea para un diseño de informe para el que desea utilizar un diseño personalizado, elija el campo **Descripción de diseño personalizado**.
4. En la página **Diseños de informe personalizados**, seleccione el diseño de documento que desea utilizar para el tipo de documento de ventas. Para obtener más información, vea [Crear y modificar diseños de informe personalizados](ui-how-create-custom-report-layout.md).

## <a name="to-specify-which-contact-will-receive-which-document-layout-for-a-customer"></a><a name="to-specify-which-contact-will-receive-which-document-layout-for-a-customer"></a><a name="to-specify-which-contact-will-receive-which-document-layout-for-a-customer"></a>Para especificar qué contacto recibirá cada diseño de documento para un cliente

Para ahorrar tiempo cuando envía documentos a contactos de clientes y proveedores por correo electrónico, especifique sus direcciones de correo electrónico en los diseños de documentos. Por ejemplo, puede enviar estados de cuenta de los clientes a sus contactos de contable, pedidos de venta a sus compradores o pedidos de compra a los vendedores de los proveedores.

1. En la página **Diseños de documento**, en la línea para un diseño de informe que desea enviar a un contacto específico para el cliente, elija la acción **Seleccionar correo electrónico de contactos**.
2. En la página **Contactos**, seleccione uno o más contactos y luego elija **Aceptar**.

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Consultar la [formación de Microsoft](/training/modules/change-documents-dynamics-365-business-central/) relacionada

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Consulte también

[Actualizar los diseños de informe personalizados](ui-update-report-layouts.md)  
[Crear y modificar diseños de informe personalizados](ui-how-create-custom-report-layout.md)  
[Importar y exportar un diseño de informe o documento personalizado](ui-how-import-and-export-report-layout.md)  
[Enviar documentos por correo electrónico](ui-how-send-documents-email.md)  
[Gestión de diseños de informe](ui-manage-report-layouts.md)  
[Trabajar con informes, trabajos por lotes y XMLports](ui-work-report.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
