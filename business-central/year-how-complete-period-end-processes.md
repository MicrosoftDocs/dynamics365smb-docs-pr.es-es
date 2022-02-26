---
title: Actividades opcionales para periodos de cierre
description: En este tema se describen los procesos y las actividades opcionales para cerrar periodos contables en Business Central.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: overview
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, aging, creditor payments, vendor payments
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: 9442b0617691098b32e5012a5a708e14fe5a0187
ms.sourcegitcommit: 8464b37c4f1e5819aed81d9cfdc382fc3d0762fc
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/19/2022
ms.locfileid: "8012030"
---
# <a name="overview-of-tasks-to-close-accounting-periods"></a>Resumen de tareas para cerrar periodos contables

[!INCLUDE[prod_short](includes/prod_short.md)] no le fuerza a cerrar los períodos, pero numerosas actividades de fin de período (fin de mes) que puede realizar. Este tema proporciona una visión general de procesos y actividades opcionales para cerrar períodos.  

## <a name="general-ledger"></a>Contabilidad

* Especifique períodos de registro para todo el sistema y específicos para el usuario.  

    Esto especifica las fechas entre las cuales puede efectuar registros. En función de su empresa, puede permitir el registro al inicio del periodo o hacia el final. Para obtener más información, vea [Especificar periodos de registro](finance-how-specify-posting-periods.md).  
* Lleve a cabo todos los ajustes de contabilidad necesarios.  
* Actualice y registre los Diarios periódicos.  
  <!--* Process Consolidations-->
* Ejecute los esquemas de cuentas como se indica a continuación:  
  * Abra la página **Esquema cuentas** y, a continuación, seleccione la acción **Imprimir**.  

## <a name="sales-and-receivables"></a>Ventas y cobros

* Registre todos los pedidos, facturas, abonos y devoluciones de ventas.  
* Registre todo los diarios de recibo cobros.  
* Actualice y registre los diarios periódicos relativos a ventas y cobros.  
* Concilie los cobros en el libro de contabilidad.  
* Ejecute el proceso **Eliminar peds. venta factdos**.  

## <a name="purchases-and-payables"></a>Compras y pagos

* Registre todos los pedidos, facturas, abonos y devoluciones de compra.  
* Registre todos los registros de pagos.  
* Actualice y registre los diarios periódicos que son relativos a compras y pagos.  
* Ejecute el informe **Antigüedad pagos** y concilie las cuentas por pagar en el libro de contabilidad.  
* Ejecute el proceso **Eliminar peds. compra factdos**.  

## <a name="fixed-assets"></a>Activos fijos

* Todos los costes de mantenimiento se han registrado mediante los diarios periódicos de activos o facturas.
* Registrar ajustes.
* Registrar apreciación.
* Registrar depreciación.
* Actualizar y registrar el diario periódico de activos fijos.

## <a name="intercompany"></a>Intercompany

* Procesar transacciones entre empresas vinculadas

## <a name="calculate-and-process-sales-tax"></a>Calcular y procesar los impuestos de venta

* Realice los extractos de impuesto.  

## <a name="see-also"></a>Consulte también

[Cerrar años y periodos](year-close-years-periods.md)  
[Cierre de libros](year-close-books.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]