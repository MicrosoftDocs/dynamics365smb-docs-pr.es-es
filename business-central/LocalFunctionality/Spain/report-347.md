---
title: Informe 347
description: El Informe 347 es un informe anual obligatorio que todas las empresas deben enviar a la administración fiscal para reflejar las compras o ventas de un periodo determinado. Este informe también incluye entradas como el pago en efectivo que se recibió en el período.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 795882a004f859a30b672a79bbfdd88c256a6d17
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2021
ms.locfileid: "5788214"
---
# <a name="report-347"></a>Informe 347
El **Informe 347** es un informe anual obligatorio que todas las empresas deben enviar a la administración fiscal para reflejar las compras o ventas de un periodo determinado. Este informe también incluye entradas como el pago en efectivo que se recibió en el período. El **informe 347** se genera en un formato que ha aprobado la administración fiscal. Este archivo puede cargarse en el sitio web de la Agencia Tributaria o enviarse en CD-ROM. Para obtener más información, consulte el sitio web de la [Agencia Tributaria](https://www.agenciatributaria.es/AEAT.internet/en_gb/Inicio.shtml).  

## <a name="file-format-for-report-347"></a>Formato de archivo del informe 347  
El formato de archivo del **Informe 347** incluye al menos una empresa responsable, un, deponente y un registro de cliente/proveedor. Una empresa responsable es una empresa que envía la información a la Agencia Tributaria. La información de deponente se obtiene de la tabla **Información empresa** y del formulario de solicitud. La información de cliente se obtiene de las tablas **Cliente**, **Mov. cliente** y **Mov. contabilidad**. La información de proveedor se obtiene de las tablas **Proveedor** y **Mov. proveedor**.  

> [!NOTE]  
>  Si no hay ningún registro de archivo, el archivo no se crea y se muestra un mensaje de error.  

## <a name="file-format-restrictions-for-report-347"></a>Restricciones de formato de archivo del informe 347  
Antes de crear el **Informe 347**, debe tener en cuenta las siguientes restricciones de formato de archivo:  

- Todos los importes deben ser positivos.  
- Todo el texto deber estar en mayúsculas.  
- Todos los campos alfanuméricos se deben alinear a la izquierda.  
- Todos los campos numéricos deben ir alineados a la derecha.  
- Si la empresa recibe pagos en efectivo que superan el límite oficial predefinido para estas transacciones, se debe incluir un año de cuatro dígitos. El año indica cuándo se contabilizaron las facturas relacionadas con cuentas por cobrar.  
- Los caracteres especiales deben convertirse a caracteres estándar.  
- Si no contienen ningún valor, los campos alfanuméricos se dejarán en blanco y los campos numéricos se rellenarán con ceros.  

## <a name="see-also"></a>Consulte también  
 [Funcionalidad local para España](spain-local-functionality.md)   
 [Crear el informe 347](how-to-create-report-347.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]