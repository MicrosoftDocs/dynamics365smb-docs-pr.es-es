---
title: Administre, elimine, o comprima los documentos | Documentos de Microsoft
description: "Conserve sus datos históricos o eliminelos."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 696100bfbcc987b1d684e7987e7fd43979813282
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="manage-documents"></a>Administración de documentos
Un rol central, como el administrador de aplicaciones, debe eliminar o comprimir periódicamente los documentos históricos para gestionar su acumulación.  

## <a name="delete-documents"></a>Eliminar documentos
En algunos casos, es posible que necesite eliminar pedidos de compra facturados que no se hayan eliminado. [!INCLUDE[d365fin](includes/d365fin_md.md)] comprueba que se hayan facturado totalmente los pedidos de compra eliminados. No puede eliminar pedidos que no haya facturado y recibido en su totalidad.  

Los pedidos de devolución generalmente se eliminan después de facturados. Cuando registra una factura, ésta se transfiere a la ventana **Histórico abono compra**. Si ha activado la casilla **Envío dev. en abono** en la ventana **Conf. compras y pagos**, la factura se transfiere a la ventana **Histórico envío devolución**. Puede eliminar los documentos a partir de un trabajo por lotes **Borrar ped. dev. compras fact.**. Antes de eliminar, el trabajo por lotes comprueba si los pedidos devueltos de compra han sido enviados y facturados totalmente.  

Los pedidos abiertos de compra no se eliminan una vez que se han procesado y facturado todos los pedidos de compra relacionados. Para eliminar pedidos abiertos de compra, puede utilizar el trabajo por lotes **Eliminar pedidos abiertos compra facturados**.  

Los pedidos de servicios facturados se suelen eliminar automáticamente después de haberse facturado en su totalidad. Cuando se registra una factura, se crea un movimiento correspondiente en la ventana **Facts. ventas (servicio) regis.** El documento registrado se puede ver en la ventana **Fact. ventas (servicio) regis.**  

Sin embargo, los pedidos de servicio no se eliminarán de forma automática si la cantidad total de dicho pedido no se ha registrado desde el pedido de servicio en sí, sino desde la ventana **Factura servicio**. En este caso, puede que tenga que eliminar los pedidos facturados que no se hayan eliminado. Para ello, ejecute el proceso **Eliminar ped. servicio facturados**.  

## <a name="see-also"></a>Consulte también  
[Administración](admin-setup-and-administration.md)  

