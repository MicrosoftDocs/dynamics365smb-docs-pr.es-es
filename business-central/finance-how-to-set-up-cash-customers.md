---
title: Configurar clientes de efectivo | Documentos de Microsoft
description: En este tema se describen los pasos para configurar al cliente que paga en efectivo.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 385a4906f36354a1b8c82f8b0a4232e3a1d35208
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5387304"
---
# <a name="set-up-cash-customers"></a>Configurar clientes de efectivo
No se puede crear una factura sin un número de cliente. Esto es válido, incluso si realiza una venta en efectivo y no tiene nada que registrar en una cuenta de cliente.  

## <a name="to-set-up-a-cash-customer"></a>Para configurar un cliente de efectivo  
1.  Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Cliente** y luego elija el enlace relacionado.  
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



[!INCLUDE[footer-include](includes/footer-banner.md)]