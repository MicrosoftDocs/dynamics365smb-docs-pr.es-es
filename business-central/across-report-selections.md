---
title: Selección de informes en Business Central
description: Obtenga información sobre cómo configurar los informes que utiliza para imprimir varios tipos de documentos en Business Central.
author: edupont04
ms.topic: conceptual
ms.search.keywords: setup, reporting
ms.search.form: 306, 307, 347, 385, 524, 865, 5932, 7401, 7355, 99000917
ms.date: 03/11/2022
ms.author: edupont
ms.openlocfilehash: 35cd5f86eeee3eecd24f63d37f8d43191dbd9be8
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2022
ms.locfileid: "8512459"
---
# <a name="report-selection-in-business-central"></a>Selección de informes en Business Central

Puede configurar informes predeterminados que se usarán para imprimir cuando trabaja con los diversos documentos de compra y venta, como pedidos, ofertas, facturas, abonos, etc. Por ejemplo, si tiene un diseño específico para las facturas de venta, puede especificar ese informe en la página **Selecciones de informes: ventas** para que se utilice para enviar o imprimir facturas de venta.  

Las páginas **Selecciones de informes** especifican qué informe se imprimirá en diferentes situaciones. [!INCLUDE [prod_short](includes/prod_short.md)] incluye configuraciones predeterminadas, pero, por supuesto, puede cambiar estos valores predeterminados. También puede agregar informes a las páginas **Selección informes** para que el sistema imprima más de un informe por cada tipo de documento, por ejemplo.  

## <a name="available-report-selections"></a>Selecciones de informes disponibles

[!INCLUDE [prod_short](includes/prod_short.md)] incluye diferentes páginas **Selección de informes** para diferentes áreas. Las siguientes tablas describen dónde puede encontrar información sobre las diferentes páginas.  

|Área o tarea  |Más información|
|--------------|----------|
|Ejemplo de cómo funciona la selección de informes (Ventas)|[Selección de informes para documentos de ventas](#example-report-selection-for-sales-documents)|
|Diseño predeterminado para correos electrónicos con documentos de compra y venta  |[Configurar textos y diseños de correo electrónico reutilizables para documentos de compra y venta](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts-for-sales-and-purchase-documents) |
|Definir diseños de cheque     |[Seleccionar una plantilla de cheques](finance-how-define-check-layouts.md) |
|Definir informes para informes de IVA (Alemania)|[Configurar informes para IVA e Intrastat](LocalFunctionality/Germany/how-to-set-up-reports-for-vat-and-intrastat.md) |

> [!TIP]
> Su [!INCLUDE [prod_short](includes/prod_short.md)] puede incluir páginas **Selección de informes** adicionales, dependiendo de su ubicación e industria, por ejemplo. Siempre puede comprobar su configuración eligiendo el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escribiendo **Selecciones de informe** y luego elija el enlace relevante.

La versión predeterminada de [!INCLUDE [prod_short](includes/prod_short.md)] incluye las siguientes páginas **Sección de informe**:

* **Ventas - Selección informes**  
* **Compras - Selección informes**  
* **Selecc. informe - Inventario**  
* **Selección informes - Flujo efectivo**  
* **Selección de informe: almacén**  
* **Selección informe - Cuenta bancaria**  
* **Selecciones de informe - Recordatorio/interés**  
* **Selección informe - Proyecto**  

## <a name="example-report-selection-for-sales-documents"></a>Ejemplo: Selección de informes para documentos de ventas

La página **Selección de informes: ventas** define los informes predeterminados que se utilizarán en diferentes escenarios para cada tipo de documento relacionado. Elija un tipo de documento en el campo **Uso** y luego agregue o revise la selección del informe. Puede configurar más de un informe y el orden de secuencia en el que se deben enviar o imprimir los informes.  

[!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

Algunos tipos de documentos se pueden enviar como archivos adjuntos de correo electrónico y otros no. Cada página **Selección de informes** muestra campos adicionales si el tipo de correo electrónico de soporte está listo para usar.  

Por ejemplo, en las páginas **Selección de informes: ventas** y **Selección de informes: compra**, los siguientes campos le ayudarán a configurar el correo electrónico:

|Nombre del campo |Descripción  |
|-----------|-------------|
|**Usar para el cuerpo del correo electrónico**| Indica que la información resumida, como el número de factura, la fecha de vencimiento y el vínculo del servicio de pago, se insertará en el cuerpo del correo electrónico que se envíe.        |
|**Usar para los datos adjuntos de correo electrónico**| Especifica que el documento relacionado se adjuntará al correo electrónico.|
|**Descripción del diseño del cuerpo del correo electrónico**|Especifica el diseño del cuerpo del correo electrónico que se utiliza, normalmente un diseño de informe personalizado. |

## <a name="see-also"></a>Consulte también .

[Configurar textos y diseños de correo electrónico reutilizables para documentos de compra y venta](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts-for-sales-and-purchase-documents)  
[Seleccionar una plantilla de cheques](finance-how-define-check-layouts.md)  
[Configurar informes para IVA e Intrastat (Alemania)](LocalFunctionality/Germany/how-to-set-up-reports-for-vat-and-intrastat.md)  
[Administrar diseños de informes y documentos](ui-manage-report-layouts.md)  
[Definir diseños de documentos para clientes y proveedores](ui-define-customer-vendor-document-layouts.md)  
[Configuración de impresoras](ui-specify-printer-selection-reports.md)  
[Informes y análisis financieros en Business Central](finance-reports.md)  
[Informes y análisis de clientes en Business Central](receivables-reports.md) 
[Informes y análisis de proveedores en Business Central](payables-reports.md)  
[Informes y análisis de activos fijos en Business Central](fa-reports.md)  
[Informes y análisis de proyecto en Business Central](project-reports.md)  
[Informes y análisis de ventas en Business Central](sales-reports.md)  
[Informes y análisis de compra en Business Central](purchase-reports.md)  
[Informes y análisis de inventario y almacén en Business Central](inventory-WMS-reports.md)  
[Informes y análisis de ensamblado en Business Central](assembly-reports.md)  
[Informes y análisis de producción en Business Central](production-reports.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]