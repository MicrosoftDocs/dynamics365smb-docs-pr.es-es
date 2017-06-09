---
title: "Impuesto de ventas y grupos de impuestos en EE. UU. y Canadá | Documentos de Microsoft"
description: "Obtenga información sobre cómo se configura el impuesto de ventas y cómo funcionan los grupos, las áreas, y los detalles de impuesto y las jurisdicciones fiscales."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: local
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: ff1981a428a2cd3b3864b7f0cc795a1abeab7a10
ms.contentlocale: es-es
ms.lasthandoff: 05/04/2017


---
# <a name="sales-tax-and-tax-groups-in-the-us-and-canada"></a>Impuesto de ventas y grupos de impuestos en EE. UU. y Canadá
Cuando empieza por primera vez a usa [!INCLUDE[d365fin](includes/d365fin_md.md)], puede ejecutar una guía asistida de instalación para configurar rápida y fácilmente la información de los impuestos de venta para su empresa, clientes y proveedores. En cuestión de minutos puede empezar a crear documentos de compra y venta con los impuestos calculados correctamente. Toda esto se explica [en nuestra entrada en el blog](https://madeira.microsoft.com/blog/sales-tax-setup-made-easy).
Si cambia a la opción vacía Mi empresa, recomendamos que empiece usando todas las guías asistidas de instalación incluyendo la de los impuestos de venta. Si prefiere configurar los impuestos sin asistente, este artículo explica qué debe tener en cuenta.  

## <a name="tax-groups-tax-areas-and-tax-jurisdictions"></a>Grupos de impuesto, áreas de impuesto y jurisdicciones fiscales
En [!INCLUDE[d365fin](includes/d365fin_md.md)], un grupo del impuesto representa un grupo de productos de inventario o de recursos que están sujetos a los mismos términos del impuesto. Por ejemplo, puede configurar un grupo de impuesto para los productos imponibles y otro para productos no imponibles. Deberá asignar códigos de grupo de impuestos a los productos de inventario y en las cuentas de contabilidad. De manera similar, deberá asignar códigos de área de impuesto a los clientes, las ubicaciones, y a su propia configuración de la empresa. La guía asistida de configuración le ayuda a realizar este proceso.  

Cada área del impuesto es un grupo de jurisdicciones de impuesto de ventas basado en una localización geográfica particular. Por ejemplo, el área de impuesto de Miami, Florida, incluye tres jurisdicciones del impuesto de ventas: ciudad (Miami), país (Dade), y estado (Florida). [!INCLUDE[d365fin](includes/d365fin_md.md)] incluye un conjunto limitado de áreas de impuesto con una configuración predeterminada, pero puede modificarlas y agregar nuevas áreas.  

Si configura nuevas áreas de impuesto y jurisdicciones impositivas, debe asegurarse de rellenar los campos correctamente. En Estados Unidos, los estados, los condados, las ciudades y las localidades pueden cobrar el impuesto sobre las ventas. En Canadá, el gobierno federal y las provincias pueden cobrar impuestos de venta. Las empresas recogen y remiten el impuesto de venta a esas autoridades para los productos vendidos a los usuarios finales. El impuesto de venta también se puede cobrar al impuesto de venta existente. Por ejemplo, el impuesto se puede calcular en el importe de una factura de venta que incluya ya el impuesto de otras jurisdicciones.  

En Canadá, los importes del impuesto se deben detallar en los documentos para cada jurisdicción fiscal. Se pueden mostrar hasta cuatro jurisdicciones en un documento, y se combinan las que tengan el mismo orden de impresión cuando se imprimen.  

## <a name="tax-details"></a>Detalles de impuesto
La ventana **Detalles de impuesto** muestra distintas combinaciones de jurisdicciones del impuesto de ventas y de grupos de impuesto de venta para establecer las tasas del impuesto de ventas. Por cada jurisdicción fiscal, recomendamos que configure un grupo de impuestos para el impuesto de venta normal, otro para productos o servicios que no cobran impuestos y un grupo adicional para cada tipo de producto o servicio que se gestione con una tarifa distinta del impuesto de ventas en dicha jurisdicción.  

En los Estados Unidos, cuando venda a un cliente en una ubicación donde no tiene un *situs*, o una ubicación legal en ese estado, no cobre el impuesto de ventas. Para las ubicaciones en las que no tiene un situs, asegúrese de que los campos **Impto. inferior al mínimo** y **Impto. superior al máximo** son 0,00.  

## <a name="see-also"></a>Consulte también
[Finanzas](finance.md)  
[Configurar las finanzas](finance-setup-finance.md)  
[Impuesto sobre bienes y servicios e impuesto de ventas en Canadá](ca-finance-tax.md)  
[Configuración fácil del Impuesto de ventas](https://madeira.microsoft.com/blog/sales-tax-setup-made-easy)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)](ui-work-product.md)  

