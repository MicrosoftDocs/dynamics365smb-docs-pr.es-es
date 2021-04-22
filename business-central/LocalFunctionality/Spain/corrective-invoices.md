---
title: Facturas correctivas
description: La funcionalidad de factura correctiva permite enviar una factura correctiva cuando haya un error o conflicto que afecte al importe del IVA o a los datos fiscales. Esta factura incluye todos los datos requeridos legalmente y hace referencia a la factura o facturas originales.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 57457e6c26b7f62753b10c26a24c36352424cd7d
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2021
ms.locfileid: "5788220"
---
# <a name="corrective-invoices"></a>Facturas correctivas
La funcionalidad de factura correctiva permite enviar una factura correctiva cuando haya un error o conflicto que afecte al importe del IVA o a los datos fiscales. Esta factura incluye todos los datos requeridos legalmente y hace referencia a la factura o facturas originales. Las facturas originales no se pueden anular y siguen siendo válidas. La factura correctiva contiene las correcciones y los motivos de estas correcciones.  

Están disponibles las siguientes opciones:  

- Se pueden definir parámetros para garantizar que todas las facturas correctivas contienen la información del número de factura corregida.  
- Al preparar una factura correctiva para el registro, se pueden seleccionar facturas registradas de una lista. Estos números de factura se utilizan como identificadores de las facturas corregidas.  
- Se pueden imprimir facturas correctivas según los requisitos legales.  
- Desde una factura registrada, se puede utilizar una referencia para buscar las facturas correctivas relacionadas.  

La factura correctiva debe cumplir los requisitos siguientes:  

- Se pueden corregir varias facturas mediante una única factura correctiva. Esta debe utilizar todos los números de facturas corregidas.  
- Se deben indicar claramente los números de las facturas que se corrigen.  
- Únicamente se puede contabilizar una factura correctiva sin números de factura corregida si las correcciones son necesarias a causa de descuentos u ofertas por volumen.  

## <a name="see-also"></a>Consulte también  
 [Funcionalidad local para España](spain-local-functionality.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]