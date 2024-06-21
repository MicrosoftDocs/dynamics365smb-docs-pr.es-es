---
title: 'Informes de IVA [ES]'
description: El IVA se aplica a las transacciones que involucran bienes y servicios en España o bienes importados a España. La siguiente información proporciona detalles sobre la funcionalidad de IVA.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/21/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="vat-reports-in-the-spanish-version"></a>Informes de IVA en la versión en español
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

Puede declarar el IVA sobre las ventas a otros países o regiones de la Unión Europea (UE). Para más información, ver [Informar el IVA a las autoridades fiscales](../../finance-how-report-vat.md).  

[!INCLUDE [finance-ecsaleslist](../../includes/finance-ecsaleslist.md)]

## <a name="see-also"></a>Consulte también

[Funcionalidad local para España](spain-local-functionality.md)  
[Informe 340](report-340.md)  
[Informe 347](report-347.md)  
[Crear informes de IVA para las autoridades fiscales](../../finance-how-report-vat.md)  


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
