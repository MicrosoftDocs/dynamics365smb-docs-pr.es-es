---
title: Informes IVA
description: El IVA se aplica a las transacciones que involucran bienes y servicios en España o bienes importados a España. La siguiente información proporciona más detalles sobre la funcionalidad de IVA.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 9b1130305d998edbbfcd865f577c018da5a8cfff
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/01/2020
ms.locfileid: "3189156"
---
# <a name="vat-reports"></a>Informes IVA
El IVA se aplica a las transacciones que involucran bienes y servicios en España o bienes importados a España. La siguiente información proporciona más detalles sobre la funcionalidad de IVA.  

## <a name="equivalence-charge"></a>Recargo de equivalencia  
El impuesto de recargo de equivalencia (RE) se aplica a las actividades que no siguen las reglas del IVA. Según las reglas RE, las empresas deben pagar un recargo a sus proveedores además del IVA. Sin embargo, en las facturas de ventas sólo pueden cargar el IVA sin el recargo.  

### <a name="vat-with-ec-percentage"></a>IVA con porcentaje RE  
Los grupos de registro general predefinidos tienen un porcentaje RE, además de su porcentaje de IVA. Aunque el seguimiento del RE se efectúa por separado, los valores de ambos impuestos se fusionan con el IVA siempre que es posible. Si en la tabla de grupo contable el porcentaje RE es un campo independiente, el RE se fusiona con el valor de la columna **%IVA**.  

Para imprimir libros de facturas emitidas y recibidas, el porcentaje de IVA y los porcentajes de RE se muestran en la tabla **Mov. IVA** durante el registro.  

> [!NOTE]  
>  Si el artículo no tiene IVA gravable, se muestra automáticamente el número 0 en el campo **% IVA** en las páginas de información de IVA.  

### <a name="telematic-vat"></a>IVA Telemático  
Mediante el IVA telemático se pueden diseñar y generar los informes fiscales mensuales y anuales como archivos electrónicos o impresos. Estos informes se pueden enviar a la administración fiscal a través de un programa externo o de un archivo XML del sitio Web de la administración.  

### <a name="vat-statement"></a>Declaración IVA  
La declaración de IVA muestra los importes e importes base de IVA en columnas diferentes.  

En la tabla **Nombre declar. IVA** hay dos tipos de plantillas de informe:  

- **Informe 1 columna**  
- **Informe 2 columnas**  

### <a name="vat-vies-declaration"></a>IVA - declaración VIES  
Mediante IVA - declaración VIES se puede ejecutar un archivo por lotes para generar los informes de ventas de la Union Europea (UE). El archivo por lotes exporta los movimientos al formato de archivo requerido para enviarlo a la aduana y a la administración fiscal.  

## <a name="see-also"></a>Consulte también  
 [Funcionalidad local para España](spain-local-functionality.md)   
 [Informe 340](report-340.md)   
 [Informe 347](report-347.md)
