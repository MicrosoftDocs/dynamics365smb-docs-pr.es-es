---
title: Pagos en efectivo
description: 'A partir del 1 de enero de 2012, las empresas en España están obligadas a presentar un resumen de los pagos en efectivo que superen los 6.000,00 EUR por cada cliente por cada año.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="payments-in-cash"></a>Pagos en efectivo
A partir del 1 de enero de 2012, las empresas en España están obligadas a presentar un resumen de los pagos en efectivo que superen los 6.000,00 EUR por cada cliente por cada año.  

## <a name="reporting-payments-in-cash"></a>Realizar pagos en efectivo
Si está realizando pagos en efectivo, la siguiente secuencia de tareas enumera el orden en que generalmente se realizan:  

- Liquidación de pagos en efectivo a las facturas.  
- Creación de pagos 340 en declaración de efectivo.  

## <a name="applying-payments-in-cash-to-invoices"></a>Liquidación de pagos en efectivo a las facturas
Liquide los pagos en efectivo a las facturas que ha recibido de clientes. Para obtener información acerca de cómo liquidar pagos en facturas, vea [Administrar cobros](../../receivables-manage-receivables.md). Solo los pagos liquidados en efectivo se utilizan para realizar pagos en efectivo. Si no liquida los pagos en efectivo a las facturas, no puede indicar pagos en efectivo.  

## <a name="making-340-payments-in-cash-declaration"></a>Creación de pagos 340 en declaración de efectivo
Utilice el proceso **Modelo 340** para informar realizar pagos 340 en la declaración de efectivo. Para obtener información acerca de cómo especificar y seleccionar la información para generar la declaración, consulte Modelo 340.  

> [!NOTE]  
>  Los pagos creados a través de los bancos se excluyen.  

> [!NOTE]  
>  El importe recibido en efectivo en el archivo .txt del modelo puede contener valores distintos al importe total facturado para un cliente. Esto se debe a que no todos los pagos se realizan en efectivo.  

## <a name="see-also"></a>Consulte también
[Administrar cobros](../../receivables-manage-receivables.md)     
 [Informe 340](report-340.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
