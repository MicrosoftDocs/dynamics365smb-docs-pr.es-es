---
title: Configurar clientes de efectivo | Documentos de Microsoft
description: En este tema se describen los pasos para configurar al cliente que paga en efectivo.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/11/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 6826c574bf63de70d76a29b45968c68c0b2e2d1f
ms.contentlocale: es-es
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-cash-customers"></a>Cómo configurar clientes de efectivo
No se puede crear una factura sin un número de cliente. Esto es válido, incluso si realiza una venta en efectivo y no tiene nada que registrar en una cuenta de cliente.  

## <a name="to-set-up-a-cash-customer"></a>Para configurar un cliente de efectivo  
1.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Cliente** y, a continuación, seleccione el vínculo relacionado.  
2.  Cree una ficha **Cliente** nueva. Para obtener más información, vea [Procedimiento: Registrar nuevos clientes](sales-how-register-new-customers.md).
3.  En el campo **N.º**, introduzca, por ejemplo, **Efectivo**.  
4.  En el campo **Nombre**, escriba **Venta en efectivo**.  
5.  En la ficha desplegable **Facturación**, rellene los campos **Grupo contable cliente** y **Grupo contable negocio**.  

 Ya ha configurado un cliente que contiene suficiente información para facturarle.  

> [!NOTE]  
>  Quizá haya elegido un grupo contable que se utilice también para las ventas a crédito nacionales. Si desea mantener datos por separado sobre ventas en efectivo, por ejemplo, con una cuenta de cliente o venta especial, configure un grupo contable adicional para ello.  
>   
>  Especifique un número de cuenta de cliente para dicho grupo contable, aunque el saldo de la cuenta quede siempre a 0 después de registrar una factura.  

## <a name="see-also"></a>Consulte también
[Administrar cobros](receivables-manage-receivables.md)  
[Registro de clientes nuevos](sales-how-register-new-customers.md)    
[Finanzas](finance.md)  


