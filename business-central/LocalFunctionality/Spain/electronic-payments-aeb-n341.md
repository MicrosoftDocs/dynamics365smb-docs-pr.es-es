---
title: Pagos electrónicos – AEB N34.1
description: Con la funcionalidad de pagos electrónicos, puede pagar a los proveedores mediante pagos electrónicos en lugar de tener que emitir cheques en papel. Los pagos electrónicos se exportan a un formato de archivo AEB N34.1 estándar, utilizado por casi todos los bancos en España.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: dcd103e2d3356d895ee430154d4ddf2daa3874cd
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2020
ms.locfileid: "3923963"
---
# <a name="electronic-payments--aeb-n341"></a>Pagos electrónicos – AEB N34.1
Con la funcionalidad de pagos electrónicos, puede pagar a los proveedores mediante pagos electrónicos en lugar de tener que emitir cheques en papel. Los pagos electrónicos se exportan a un formato de archivo AEB N34.1 estándar, utilizado por casi todos los bancos en España. Posteriormente, este archivo se transmite al banco.  

Podrá crear pagos electrónicos desde los diarios de pagos o desde la funcionalidad Cartera (lista de informes). Su objetivo es ocuparse de los casos siguientes:  

- Facturas y documentos de cartera abiertos y no agrupados. Si decide pagar mediante pagos electrónicos, el archivo de pago se genera desde el informe **Exportar pagos electrónicos**.  

- Facturas y documentos de cartera agrupados en una orden de pago. Si decide pagar mediante pagos electrónicos, el archivo de pago se genera desde el informe **Orden pago - Exportar N34.1**, disponible en la lista de informes de cartera.  

> [!NOTE]  
>  Los socios pueden tener que modificar este informe para satisfacer los requisitos concretos del banco de su cliente.  

Para poder hacer transferencias de pago electrónicas a un proveedor, tendrá que configurar una cuenta de banco para el proveedor. También tendrá que configurar los vínculos de pagos electrónicos con el banco y la ficha de cuenta de banco en [!INCLUDE[d365fin](../../includes/d365fin_md.md)] para que su propio banco controle los pagos electrónicos. El banco debe proporcionar el programa de transmisión.  

## <a name="see-also"></a>Consulte también  
 [Configurar cuentas bancarias para realizar pagos electrónicos](how-to-set-up-bank-accounts-for-electronic-payments.md)   
 [Pagar a los proveedores mediante pagos electrónicos](how-to-pay-vendors-by-using-electronic-payments.md) 
