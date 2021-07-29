---
title: Asignar diseños de documentos a clientes o proveedores
description: Cuando se definen diseños de informes personalizados, puede seleccionarlos de las tarjetas de clientes y proveedores para especificar que se utilizan el cliente o el proveedor en cuestión.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.date: 06/24/2021
ms.author: edupont
ms.openlocfilehash: 29b349824e2aff727cd255e612fa054f1d71610c
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 07/08/2021
ms.locfileid: "6443748"
---
# <a name="define-document-layouts-for-customers-and-vendors"></a>Definir diseños de documentos para clientes y proveedores
Cuando se definen diseños de informes personalizados, puede seleccionarlos de las tarjetas de clientes y proveedores para especificar qué diseños se utilizarán para los diferentes tipos de documentos que cree para el cliente o el proveedor en cuestión. El valor en el campo **Uso** define para qué proceso se utilizará el diseño del documento, como **Recordatorio**, **Envío** y **Confirmación**.

Además de configurar qué diseños se usarán para cada documento, puede ahorrar tiempo al enviar documentos a diferentes contactos de clientes o proveedores configurando las direcciones de correo electrónico de contactos específicos para usar con documentos específicos. Por ejemplo, los estados de cuenta de los clientes se enviarán a los contactos de contable, los pedidos de venta a los compradores de sus clientes y los pedidos de compra a los vendedores o administradores de cuentas de los proveedores.

Cuando define un diseño de documento para un cliente o proveedor, también puede especificar la dirección de correo electrónico de la persona de contacto que debe recibir el documento. Puede hacer esto rápidamente con la función **Seleccionar correo electrónico de contactos**, que filtra automáticamente las direcciones de correo electrónico de contacto registradas para el cliente o proveedor en cuestión.

Antes de poder definir qué diseño de documento usar para cada proceso y a qué contacto enviar el documento, debe cargar todos los informes disponibles (documentos) desde la página **Seleccionar selecciones**. Puede hacer esto rápidamente con la función **Copiar desde selección de informe**.

A continuación se describe cómo definir diseños de documentos de venta desde una ficha de cliente. Los pasos son los mismos que para los diseños de documentos de compra de una ficha de proveedor.

## <a name="to-enable-all-available-sales-documents-for-a-customer"></a>Para habilitar todos los documentos de venta disponibles para un cliente
1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Clientes** y luego elija el enlace relacionado.
2. Abra la ficha del cliente para el que desea definir diseños de documento por proceso de negocio.
3. En la página **Ficha de cliente**, seleccione la página **Diseños de documentos**.
4. En la página **Diseños de documentos**, elija la acción **Copiar desde selección de informe**.

La página **Diseños de documentos** para el cliente en cuestión se rellena con todos los diseños de informes para ventas que existen en el sistema. Para obtener más información sobre su creación, vea [Crear y modificar diseños de informe personalizados](ui-how-create-custom-report-layout.md).

Ahora puede pasar a ajustar la lista con cualquier diseño de informe personalizado o dirección de correo electrónico para los contactos a los que se deben enviar los documentos.

## <a name="to-select-a-custom-report-layout-to-use-for-the-sales-document-layout"></a>Para seleccionar un diseño de informe personalizado para usar para el diseño de documento de venta
Si uno o más de los diseños de informe que están definidos en la página **Diseños de documento** para el cliente no tiene un diseño de informe personalizado definido, puede hacerlo rápidamente.

1. En la página **Diseños de documento**, en la línea para un diseño de informe para el que desea utilizar un diseño personalizado, elija el campo **Descripción de diseño personalizado**. El campo se rellena si el diseño del cliente ya está seleccionado o en blanco.
2. En la página **Diseños de informe personalizados**, seleccione el diseño de documento especial que desea utilizar para el tipo de documento de venta en cuestión. Para obtener más información, vea [Crear y modificar diseños de informe personalizados](ui-how-create-custom-report-layout.md).

## <a name="to-set-up-which-contact-receives-which-document-layout-for-a-customer"></a>Para configurar qué contacto recibe cada diseño de documento para un cliente
Puede ahorrar tiempo al enviar documentos a diferentes clientes o contactos de proveedor especificando las direcciones de correo electrónico de contacto en las diferentes líneas de la página **Diseños de documento**. Por ejemplo, los estados de cuenta de los clientes se pueden enviar a los contactos de contable, los pedidos de venta a los compradores de sus clientes y los pedidos de compra a los vendedores o administradores de cuentas de los proveedores.

1. En la página **Diseños de documento**, en la línea para un diseño de informe que desea enviar a un contacto específico para el cliente, elija la acción **Seleccionar correo electrónico de contactos**.
2. En la página **Contactos**, seleccione la línea para el contacto relevante y luego elija el botón **Aceptar**.

La dirección de correo electrónico del contacto se inserta ahora en la línea de diseño de documento para que el documento de venta en cuestión, por ejemplo, los recordatorios, se envíe siempre a ese contacto en la empresa del cliente.

## <a name="see-also"></a>Consulte también  
[Actualizar los diseños de informe personalizados](ui-update-report-layouts.md)  
[Crear y modificar diseños de informe personalizados](ui-how-create-custom-report-layout.md)  
[Importar y exportar un diseño de informe o documento personalizado](ui-how-import-and-export-report-layout.md)  
[Enviar documentos por correo electrónico](ui-how-send-documents-email.md)  
[Gestión de diseños de informe](ui-manage-report-layouts.md)  
[Trabajar con informes, trabajos por lotes y XMLports](ui-work-report.md)  
[Trabajar con informes, trabajos por lotes y XMLports](ui-work-report.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]