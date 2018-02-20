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
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: a72e6ff0a710f2d555c805e4fa28896683a819e9
ms.contentlocale: es-es
ms.lasthandoff: 01/30/2018

---
# <a name="set-up-cash-customers"></a>Configurar clientes de efectivo
No se puede crear una factura sin un número de cliente. Esto es válido, incluso si realiza una venta en efectivo y no tiene nada que registrar en una cuenta de cliente.  

## <a name="to-set-up-a-cash-customer"></a>Para configurar un cliente de efectivo  
1.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Cliente** y, a continuación, seleccione el vínculo relacionado.  
2.  Cree una ficha **Cliente** nueva. Para obtener más información, vea [Registrar nuevos clientes](sales-how-register-new-customers.md).
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
[Permite registrar nuevos clientes](sales-how-register-new-customers.md)    
[Finanzas](finance.md)  


