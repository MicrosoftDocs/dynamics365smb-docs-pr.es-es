---
title: "Informe 1099 de transacciones en EE. UU. | Documentos de Microsoft"
description: "En sus documentos de compra, puede especificar que el documento está sujeto al impuesto 1099, y especificar el código 1099 para el proveedor."
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
ms.openlocfilehash: a0a31c28b6c96dc80593ac3862b97b36c3ec81c7
ms.contentlocale: es-es
ms.lasthandoff: 05/04/2017


---
# <a name="reporting-1099-transactions-in-the-us"></a>Informe 1099 de transacciones en EE. UU.
El servicio de la Agencia Tributaria de EE. UU. (IRS) requiere una o varias versiones de formulario del impuesto 1099 para los pagos a proveedores. Las copias de estos formularios se deben enviar a los proveedores anualmente el último día de enero o antes de ese día. En sus documentos de compra, puede especificar que el documento está sujeto al impuesto 1099, y especificar el código 1099 para el proveedor.  

## <a name="1099-codes"></a>Códigos 1099
En [!INCLUDE[d365fin](includes/d365fin_md.md)], la mayoría de los códigos 1099 ya están configurados de forma automática para generar los informes necesarios. Los códigos se definen en la ventana **Cuadro de formulario IRS 1099** en la que puede agregar nuevos códigos 1099. Cada proveedor sujeto a impuestos, podrá especificar el código correspondiente 1099 en la ficha desplegable **Pagos** de la ficha de proveedor.  

Con la información **Declaración de 1099 de proveedor**, puede revisar las transacciones de 1099 durante un periodo específico. Al final del año, puede imprimir las transacciones 1099 en documentos preimpresos.  

## <a name="printing-1099-tax-forms"></a>Impresión de formularios del impuesto 1099
Desde la ventana **Cuadro de formulario de IRS 1099**, podrá acceder a los formularios de impuestos siguientes:  

* Dividendos de proveedor 1099  

  Imprime el formulario federal 1099-DIV para los dividendos y la distribución. Puede imprimir todo o los formularios específicos de 1099-DIV. El informe utiliza los códigos que se aplican a los cuadros de importe del formulario DIV de la ventana **Cuadro de formulario IRS 1099**.  
* Intereses de proveedor 1099  

  Imprime el formulario federal 1099-INT para los ingresos de intereses. Puede imprimir todo o los formularios específicos de 1099-INT. El informe utiliza los códigos que se aplican a los cuadros de importe del formulario INT de la ventana **Cuadro de formulario IRS 1099**.  
* Ingresos varios de proveedor 1099  

  Imprime el formulario federal 1099-MISC para distintos ingresos. Puede imprimir todo o los formularios específicos de 1099-MISC. El informe utiliza los códigos que se aplican a los cuadros de importe del formulario MISC de la ventana **Cuadro de formulario IRS 1099**.  

Los cambios normativos que afectan a este informe y los datos de la tabla se gestionan normalmente en las actualizaciones de final del año.
Puede resultar útil ejecutar el informe **Información de proveedor 1099** para revisar los datos antes de imprimir los formularios.

## <a name="submitting-1099-tax-forms-electronically"></a>Envío electrónico de los formularios del impuesto 1099
Para enviar electrónicamente los formularios del impuesto 1099, utilice el informe **Soporte magnético de proveedor 1099**. Especifica los formularios 1099 que se pueden exportar. La información de formulario exportada por este informe es la misma que los informes que imprimen los formularios 1099 que se han descrito en la sección anterior.  

El informe utiliza los códigos que se aplican a los cuadros de importe del formulario de la ventana **Cuadro de formulario IRS 1099**. Los códigos se asignan a los cuadros de formulario en los diseños de formulario este informe, por lo que deben coincidir los datos de tabla y la versión de informe de un determinado ejercicio fiscal. Si se añaden algunos códigos personalizados a la tabla, se deben asignar a los cuadros del formulario de este objeto.  

Los cambios normativos que afectan a este informe y los datos de la tabla se gestionan normalmente en las actualizaciones de final del año.
Puede resultar útil ejecutar el informe **Información de proveedor 1099** para revisar los datos antes de generar el archivo electrónico.  

## <a name="see-also"></a>Consulte también
[Registro de proveedores nuevos](purchasing-how-register-new-vendors.md)  
[Registrar compras](purchasing-how-record-purchases.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)](ui-work-product.md)  

