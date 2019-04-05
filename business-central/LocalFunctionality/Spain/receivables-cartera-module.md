---
title: Módulo Docs. cartera a cobrar
description: El módulo Docs. cartera a cobrar permite administrar las facturas generadas a partir de facturas de ventas.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 6d8ecf84d4254d4ab18653444bf66df3c161c2ff
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/08/2019
ms.locfileid: "827143"
---
# <a name="receivables-cartera-module"></a>Módulo Docs. cartera a cobrar
El módulo Docs. cartera a cobrar permite administrar las facturas generadas a partir de facturas de ventas. Los documentos se pueden administrar por:  

- Fecha de vencimiento  
- Banco  
- Valor  
- Tipo de documento  
- Divisa  

Mediante el **Diario Cartera** se pueden crear facturas manualmente. También se puede utilizar el módulo Docs. cartera a cobrar para administrar todas las facturas de ventas que la empresa proporciona a una entidad de factoring.  

## <a name="bill-groups"></a>Remesas  
Mediante el módulo Docs. cartera a cobrar, se pueden administrar remesas y remesas de descuento en la divisa local u original.  

Existen diferentes criterios para agrupar documentos en una remesa. Se pueden agrupar documentos girados para el mismo cliente, se pueden agrupar documentos que tengan la misma fecha de vencimiento, documentos girados en la misma plaza, etc. Pueden agruparse en una remesa uno o más documentos a cobrar.  

Una remesa se compone de uno o varios documentos que se agrupan para su entrega a un banco. Se puede enviar al cobro o descuento.  

Si se envían al cobro, el banco sólo es responsable de procesar el cobro de los documentos en la fecha de vencimiento.  

Si la remesa se envía al descuento, el banco avanzará el importe de la remesa (o una parte de este, en el caso de factoring) a la empresa y será responsable de cobrar en las fechas de vencimiento de los documentos que forman la remesa.  

Una remesa de facturas se puede enviar a una entidad de crédito (factor) para factoring con recurso (la empresa cubre el riesgo de insolvencia) o factoring sin recurso (el factor cubre el riesgo de insolvencia).  

Las remesas incluyen:  

- Administración de intereses al cobro o descuento  
- Intereses de facturas devueltas  
- Interés al descuento  

Con el módulo Docs. cartera a cobrar, se pueden proporcionar créditos o factoring de remesas de facturas de ventas, incluido el cálculo de intereses de la entidad de factoring. Se puede solicitar el valor anticipado de las facturas proporcionadas o sólo la administración del cobro.  

Se pueden utilizar remesas para:  

- Factoring sin recurso: la entidad de factoring asume los riesgos asociados con el no-pago.  
- Factoring con recurso: usted asume los riesgos asociados con el no-pago.  

## <a name="see-also"></a>Consulte también  
 [Módulo Cartera](cartera-module.md)   
 [Módulo Docs. cartera a pagar](payments-cartera-module.md)
