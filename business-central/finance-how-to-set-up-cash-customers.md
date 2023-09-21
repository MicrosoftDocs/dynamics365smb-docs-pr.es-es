---
title: Configurar clientes de efectivo
description: Este tema describe los pasos necesarios para configurar la factura con un número de cliente para los clientes que pagan en efectivo.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '21, 22'
ms.date: 06/16/2021
ms.author: bholtorf
---
# <a name="set-up-cash-customers"></a>Configurar clientes de efectivo

No se puede crear una factura sin un número de cliente. Esto es válido, incluso si realiza una venta en efectivo y no tiene nada que registrar en una cuenta de cliente.  

## <a name="to-set-up-a-cash-customer"></a>Para configurar un cliente de efectivo

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Cliente** y luego elija el enlace relacionado.  
2. Cree una ficha **Cliente** nueva. Para obtener más información, vea [Registrar nuevos clientes](sales-how-register-new-customers.md).
3. En el campo **N.º**, introduzca, por ejemplo, **Efectivo**.  
4. En el campo **Nombre**, escriba **Venta en efectivo**.  
5. En la ficha desplegable **Facturación**, rellene los campos **Grupo contable cliente** y **Grupo contable negocio**.  

 Ya ha configurado un cliente que contiene suficiente información para facturarle.  

> [!NOTE]  
> Quizá haya elegido un grupo contable que se utilice también para las ventas a crédito nacionales. Si desea mantener datos por separado sobre ventas en efectivo, por ejemplo, con una cuenta de cliente o venta especial, configure un grupo contable adicional para ello.  
>
> Especifique un número de cuenta de cliente para dicho grupo contable, aunque el saldo de la cuenta quede siempre a 0 después de registrar una factura.  

## <a name="see-also"></a>Consulte también

[Administrar cobros](receivables-manage-receivables.md)  
[Registro de clientes nuevos](sales-how-register-new-customers.md)
[Finance](finance.md)  



[!INCLUDE[footer-include](includes/footer-banner.md)]
