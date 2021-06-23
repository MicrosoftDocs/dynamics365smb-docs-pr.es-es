---
title: 'Detalles de diseño: Registro de órdenes de producción | Documentos de Microsoft'
description: Al igual que el registro de pedido de ensamblado, se convierten los componentes consumidos y el tiempo de máquina usado, y se envían como el producto fabricado cuando finaliza la orden de producción.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: 966760ae57f9908ec7245f8e97f6d35591142332
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/09/2021
ms.locfileid: "6214883"
---
# <a name="design-details-production-order-posting"></a>Detalles de diseño: Registro de órdenes de producción
Al igual que el registro de pedido de ensamblado, se convierten los componentes consumidos y el tiempo de máquina usado, y se envían como el producto fabricado cuando finaliza la orden de producción. Para obtener más información, consulte [Detalles de diseño: Registro de pedidos de ensamblado](design-details-assembly-order-posting.md). No obstante, el flujo del coste para los pedidos de ensamblado es menos complejo, especialmente porque el registro de coste de ensamblado solo se produce una vez, y por tanto que no genera un inventario de trabajo en curso.


Se puede realizar el seguimiento de las transacciones que se produzcan durante el proceso de fabricación a través de las siguientes etapas:  

1.  Compra de materiales y otros movimientos de fabricación.  
2.  Conversión a trabajo en curso.  
3.  Conversión a inventario de productos terminados.  
4.  Venta de productos terminados.  

Por lo tanto, aparte de las cuentas de inventario normales, una empresa de fabricación debe establecer tres cuentas de inventario independientes para registrar las transacciones en diversas etapas de producción.  

|Cta. inventario|Description|  
|-----------------------|---------------------------------------|  
|**Cuenta de materias primas**|Incluye el coste de materias primas compradas pero aún no transferidas a producción. El saldo de la cuenta de materias primas indica el coste de las materias primas disponibles.<br /><br /> Cuando las materias primas se trasladan al departamento de producción, el coste de los materiales se transfiere de la cuenta de materias primas a la cuenta de trabajo en curso.|  
|**Cuenta de trabajo en curso (WIP)**|Acumula los costes que se contraen durante la producción en el periodo contable. En la cuenta de trabajo en curso se adeuda el coste de las materias primas que se transfieren desde el almacén de materias primas, el coste de la mano de obra directa y los costes generales de fabricación que se deriven.<br /><br /> En la cuenta del trabajo en curso se carga el coste de fabricación total de las unidades que se han completado en la fábrica y se han transferido al almacén de productos terminados.|  
|**Cuenta de productos terminados**|Esta cuenta incluye el coste total de fabricación de las unidades que están completadas pero aún no se han vendido. En el momento de la venta, el coste de las unidades vendidas se transfiere de la cuenta Coste de productos vendidos.|  

El valor de inventario se calcula mediante el seguimiento de los costes de todas las entradas y salidas, tal como se expresa mediante la ecuación siguiente:  

* valor de inventario = saldos de inicio de inventario + valor de todas las entradas - valor de todas las salidas  

Dependiendo del tipo de inventario, los aumentos y las disminuciones se representan mediante distintas transacciones.  

||Aumentos|Disminuciones|  
|-|---------------|---------------|  
|**Inventario de materias primas**|-   Compras netas de material<br />-   Salida de subensamblados<br />-   Consumo negativo|Consumo de material|  
|**Inventario WIP**|-   Consumo de material<br />-   Consumo de capacidad<br />-   Gastos generales de fabricación|Salida de productos finales (coste de los productos fabricados)|  
|**Inventario de productos terminados**|Salida de productos finales (coste de los productos fabricados)|-   Ventas (coste de productos vendidos)<br />-   Salida negativa|  
|**Inventario de materias primas**|-   Compras netas de material<br />-   Salida de subensamblados<br />-   Consumo negativo|Consumo de material|  

Los valores de entradas y salidas de existencias se registran en los distintos tipos de inventario fabricado de la misma forma que para el inventario comprado. Cada vez que se produzca una entrada o una salida de existencias se crea un movimiento de producto y un movimiento de contabilidad correspondiente para el importe. Para obtener más información, consulte [Detalles de diseño: Registro de inventario](design-details-inventory-posting.md).  

Aunque los valores de las transacciones relacionadas con productos comprados se registren solo como movimientos de producto con las entradas de los valores relacionados, las transacciones relacionadas con los productos fabricados se registran como movimientos de capacidad con las entradas de los valores relacionados, además de en los movimientos de producto.  

## <a name="posting-structure"></a>Estructura de registro  
El registro de órdenes de producción de registro al inventario de trabajo en curso implica la salida, el consumo y la capacidad.  

En el diagrama siguiente se muestran las rutinas de registro relacionadas en la codeunit 22.  

![Rutinas de registro de órdenes de producción](media/design_details_inventory_costing_14_production_posting_1.png "Rutinas de registro de órdenes de producción")  

En el diagrama siguiente se muestran las asociaciones entre los movimientos resultantes y los objetos de coste.  

![Flujo de movimiento de producción](media/design_details_inventory_costing_14_production_posting_2.png "Flujo de movimiento de producción")  

El movimiento de capacidad describe el consumo de capacidad en unidades de tiempo, mientras que el movimiento de valoración relacionado describe el valor del consumo de capacidad específico.  

El movimiento de producto describe el consumo o la salida de material en términos de cantidades, mientras que el movimiento de valoración relacionado describe el valor de este determinado consumo o salida de material.  

Se puede asociar una entrada de valor que describa el valor de inventario WIP con una de las combinaciones siguientes de objetos de coste:  

-   Una línea de orden de producción, un centro de máquina o de trabajo y un movimiento de capacidad.  
-   Una línea de orden de producción, un producto y un movimiento de producto.  
-   Solo una línea de orden de producción  

Para obtener más información acerca de cómo se registran costes de producción y ensamblado en la contabilidad, consulte [Detalles de diseño: Registro de inventario](design-details-inventory-posting.md).  

## <a name="capacity-posting"></a>Registro de capacidad  
El registro de la salida de la última la línea de ruta de la orden de producción da como resultado un movimiento de capacidad para el producto final, además de su entrada de existencias.  

 El movimiento de capacidad es un registro de tiempo que se ha dedicado para producir el producto. El movimiento de valoración relacionado describe el aumento del valor de inventario del trabajo en curso, que es el valor del coste de conversión. Para obtener más información, consulte "Desde los movimientos de capacidad” en [Detalles de diseño: cuentas de contabilidad](design-details-accounts-in-the-general-ledger.md)”.  

## <a name="production-order-costing"></a>Gestión de costes del pedido de producción  
 Para controlar los costes del inventario y de producción, una empresa de fabricación debe medir el coste de las órdenes de producción, porque el coste estándar predeterminado de cada producto fabricado está capitalizado en el balance. Para obtener información acerca de por qué los productos fabricados utilizan el método de coste Estándar, consulte [Detalles de diseño: Métodos de coste](design-details-costing-methods.md).  

> [!NOTE]  
>  En entornos que no utilizan el método de coste Estándar, se capitaliza en la hoja de balance el coste real en lugar del coste estándar de los productos fabricados.  

El coste real de una orden de producción consta de los componentes de coste siguientes:  

-   Coste de material real  
-   Coste de capacidad o coste de subcontratista real  
-   Cost. gen. fabricación  

Estos costes reales se registran en la orden de producción y se comparan con el coste estándar para calcular las desviaciones. Las desviaciones se calculan por cada uno de los componentes de coste de producto: materias primas, capacidad, subcontratista, costes de subcontratistas y costes de fabricación. Se pueden analizar las desviaciones para determinar problemas, como, por ejemplo, el exceso de residuos en el procesamiento.  

En entornos de coste estándar, el coste de una orden de producción se basa en el mecanismo siguiente:  

1.  Cuando se registra la última operación de ruta, el coste de la orden de producción se registra en los movimientos de producto y se establece en el coste previsto.  

    Este coste equivale a la cantidad de salida que se registra en el diario de salida multiplicado por el coste estándar que se copia de la ficha de producto. El coste se considera previsto hasta que finaliza la orden de producción. Para obtener más información, consulte [Detalles de diseño: Registro de coste previsto](design-details-expected-cost-posting.md).  

    > [!NOTE]  
    >  Esto es distinto del registro de pedido de ensamblado, que siempre registra los costes reales. Para obtener más información, consulte [Detalles de diseño: Registro de pedidos de ensamblado](design-details-assembly-order-posting.md).  
2.  Cuando la orden de producción se establece en **Terminada**, se factura mediante la ejecución del proceso **Valorar stock - movs. producto**. Como resultado, el coste total del pedido se calcula basándose en el coste estándar de los materiales consumidos y la capacidad. Se calculan y registran las desviaciones entre los costes estándar calculados y los costes de producción reales.  

## <a name="see-also"></a>Consulte también  
 [Detalles de diseño: Coste de inventario](design-details-inventory-costing.md)   
 [Detalles de diseño: Registro de pedidos de ensamblado](design-details-assembly-order-posting.md)  
 [Gestión de costes de inventario](finance-manage-inventory-costs.md) [Finanzas](finance.md)  
 [Trabajar con Business Central](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]