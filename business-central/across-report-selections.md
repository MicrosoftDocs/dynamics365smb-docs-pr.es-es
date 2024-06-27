---
title: Selección de informes en Business Central
description: Obtenga información sobre cómo configurar los informes que utiliza para imprimir varios tipos de documentos en Business Central.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'setup, reporting'
ms.search.form: '306, 307, 347, 385, 524, 865, 5932, 7401, 7355, 99000917'
ms.date: 06/13/2024
ms.service: dynamics-365-business-central
---
# Selección de informes para documentos en Business Central

Puede configurar informes predeterminados para imprimir documentos de ventas, compras y servicios, como pedidos, ofertas y facturas. Por ejemplo, si tiene un diseño específico para las facturas de venta, puede especificar ese informe en la página **Selecciones de informes: ventas**. Luego podrá utilizar el informe cuando envíe o imprima facturas de ventas.  

## Selecciones de informes disponibles

Las páginas **Selecciones de informes** especifican qué informe se imprimirá en diferentes situaciones. [!INCLUDE [prod_short](includes/prod_short.md)] proporciona configuraciones predeterminadas, pero puede cambiarlas si es necesario. También puede agregar informes a las páginas **Selección informes** para que el sistema imprima más de un informe por cada tipo de documento, por ejemplo. 

Las siguiente tabla describe dónde puede encontrar información sobre las diferentes páginas.  

|Área o tarea  |Más información|
|--------------|----------|
|Ejemplo de cómo funciona la selección de informes (ventas)|[Selección de informes para documentos de ventas](#example-report-selection-for-sales-documents)|
|Diseño predeterminado para correos electrónicos con documentos de compra y venta  |[Configurar textos y diseños de correo electrónico reutilizables para documentos de compra y venta](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts) |
|Definir diseños de cheque     |[Seleccionar una plantilla de cheques](finance-how-define-check-layouts.md) |
|Definir informes para informes de impuesto de valor añadido (IVA) (Alemania)|[Configurar informes para IVA e Intrastat](LocalFunctionality/Germany/how-to-set-up-reports-for-vat-and-intrastat.md) |

> [!TIP]
> Su [!INCLUDE [prod_short](includes/prod_short.md)] puede incluir páginas **Selección de informes** adicionales, dependiendo de su ubicación e industria, por ejemplo. Para comprobar su configuración, elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escribiendo **Selección de informe** y luego elija el enlace relevante.

La versión predeterminada de [!INCLUDE [prod_short](includes/prod_short.md)] incluye las siguientes páginas **Selección de informe**:

* **Ventas - Selección informes**  
* **Selección informe - Proyecto**  
* **Selección informe - Servicio**
* **Compras - Selección informes**  
* **Selección informes - Flujo efectivo**  
* **Selección de informe: almacén**  
* **Selecc. informe - Inventario**  
* **Selección informe - Cuenta bancaria**  
* **Selección de informes de orden de producción**  
* **Selección informe - Recordatorio e interés**  

## Ejemplo: Selección de informes para documentos de ventas

La página **Selección de informes: ventas** ofrece los informes predeterminados que se utilizarán en diferentes escenarios para cada tipo de documento relacionado. Elija un tipo de documento en el campo **Uso** y luego agregue o revise la selección del informe. Puede configurar más de un informe y epsecificar la secuencia en el que se deben enviar o imprimir los informes.  

[!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

No puede enviar todos los tipos de documentos como archivos adjuntos. Para los tipos de documentos que pueda, la página **Selección de informe** contiene campos adicionales.  

Por ejemplo, en las páginas **Selección de informes: ventas** y **Selección de informes: compra**, los siguientes campos le ayudarán a configurar el correo electrónico:

|Nombre del campo |Descripción  |
|-----------|-------------|
|**Usar para el cuerpo del correo electrónico**| Inserte información resumida, como el número de factura, la fecha de vencimiento y el enlace del servicio de pago, en un correo electrónico.        |
|**Usar para los datos adjuntos de correo electrónico**| Adjunte el documento relacionado al correo electrónico.|
|**Descripción del diseño del cuerpo del correo electrónico**|Especifique el diseño del cuerpo del correo electrónico que se utilizará. Normalmente, el diseño es un diseño de informe personalizado. |

## Consulte también .

[Configurar textos y diseños de correo electrónico reutilizables](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts)  
[Seleccionar una plantilla de cheques](finance-how-define-check-layouts.md)  
[Configurar informes para IVA e Intrastat (Alemania)](LocalFunctionality/Germany/how-to-set-up-reports-for-vat-and-intrastat.md)  
[Administrar diseños de informes y documentos](ui-manage-report-layouts.md)  
[Definir diseños de documentos para clientes y proveedores](ui-define-customer-vendor-document-layouts.md)  
[Configuración de impresoras](ui-specify-printer-selection-reports.md)  
[Informes y análisis financieros en Business Central](finance-reports.md)  
[Informes y análisis de cobros en Business Central](receivables-reports.md)  
[Informes y análisis de cuentas por pagar en Business Central](payables-reports.md)  
[Informes y análisis de activos fijos en Business Central](fa-reports.md)  
[Informes y análisis de proyecto en Business Central](project-reports.md)  
[Informes y análisis de ventas en Business Central](sales-reports.md)  
[Informes y análisis de compra en Business Central](purchase-reports.md)  
[Informes y análisis de inventario y almacén en Business Central](inventory-WMS-reports.md)  
[Informes y análisis de ensamblado en Business Central](assembly-reports.md)  
[Informes y análisis de producción en Business Central](production-reports.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
