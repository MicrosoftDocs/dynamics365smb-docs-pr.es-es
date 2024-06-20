---
title: 'Pagos electrónicos – AEB N34.1 - [ES]'
description: 'Con la funcionalidad de pagos electrónicos, puede pagar a los proveedores mediante pagos electrónicos exportados a un formato de archivo estándar AEB N34.1.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 12/08/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Pagos electrónicos - AEB N34.1 en la versión en español
Con la funcionalidad de pagos electrónicos, puede pagar a los proveedores mediante pagos electrónicos en lugar de tener que emitir cheques en papel. Los pagos electrónicos se exportan a un formato de archivo AEB N34.1 estándar, utilizado por casi todos los bancos en España. Posteriormente, este archivo se transmite al banco.  

Podrá crear pagos electrónicos desde los diarios de pagos o desde la funcionalidad Cartera (lista de informes). Su objetivo es ocuparse de los casos siguientes:  

- Facturas y documentos de cartera abiertos y no agrupados. Si decide pagar mediante pagos electrónicos, el archivo de pago se genera desde el informe **Exportar pagos electrónicos**.  

- Facturas y documentos de cartera agrupados en una orden de pago. Si decide pagar mediante pagos electrónicos, el archivo de pago se genera desde el informe **Orden pago - Exportar N34.1**, disponible en la lista de informes de cartera.  

> [!NOTE]  
>  Los socios pueden tener que modificar este informe para satisfacer los requisitos concretos del banco de su cliente.  

Para poder hacer transferencias de pago electrónicas a un proveedor, tiene que configurar una cuenta bancaria para el proveedor. Además, tiene que configurar los vínculos de pagos electrónicos con el banco y la ficha de cuenta bancaria en [!INCLUDE[prod_short](../../includes/prod_short.md)] para que su propio banco controle los pagos electrónicos. El banco debe proporcionar el programa de transmisión.  

## Consulte también  
 [Configurar cuentas bancarias para realizar pagos electrónicos](how-to-set-up-bank-accounts-for-electronic-payments.md)   
 [Pagar a los proveedores mediante pagos electrónicos](how-to-pay-vendors-by-using-electronic-payments.md) 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]