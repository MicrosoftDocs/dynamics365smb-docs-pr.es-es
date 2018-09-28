---
title: "Pagar a los proveedores mediante pagos electrónicos"
description: "En Business Central, puede pagar a un proveedor mediante pagos electrónicos. Los pagos se exportarán a un archivo, que luego se transferirá al banco. Después, el banco transfiere los pagos de manera electrónica de su cuenta de banco a la cuenta de banco del beneficiario (proveedor)."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: d5bbb66898f2467e2cca20a6f52ef8a42d5e18b3
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="pay-vendors-using-electronic-payments"></a>Pagar a los proveedores mediante pagos electrónicos
En [!INCLUDE[d365fin](../../includes/d365fin_md.md)], puede pagar a un proveedor mediante pagos electrónicos. Los pagos se exportarán a un archivo, que luego se transferirá al banco. Después, el banco transfiere los pagos de manera electrónica de su cuenta de banco a la cuenta de banco del beneficiario (proveedor).  

Este proceso es parecido al de los cheques automáticos.  

## <a name="to-pay-a-vendor-electronically"></a>Para pagar a un proveedor electrónicamente  

1. Seleccione el icono ![Buscar página o informe](../../media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Diarios de pagos** y, a continuación, seleccione el vínculo relacionado.  
2. Rellene los campos tal como se describe en la tabla siguiente.  

    |Campo|Description|  
    |---------------------------------|---------------------------------------|  
    |**Tipo pago por banco**|Especifique un **Pago electrónico** para crear un movimiento de cheque correspondiente a ese importe.|  
    |**Tipo pago**|Especifique el tipo de pago para el pago de transferencia especial, si corresponde. Seleccione **En blanco** si no desea usar el tipo de pago de transferencia especial. Seleccione **01** para crear un pago especial para "artículos" en la línea del diario. Seleccione **02** para crear un pago especial para "no artículos" en esta línea del diario.|  
    |**Código estadístico**|Especifique el código estadístico para el pago de transferencia especial, si corresponde. El código estadístico se tiene que usar conjuntamente con el tipo de pago. Seleccione **01** para crear un pago especial para "artículos" en la línea del diario. Seleccione **02** para crear un pago especial para "no artículos" en esta línea del diario.|  

## <a name="see-also"></a>Consulte también  
[Configurar cuentas bancarias para realizar pagos electrónicos](how-to-set-up-bank-accounts-for-electronic-payments.md)

