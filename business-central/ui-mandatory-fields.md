---
title: Campos obligatorios para completar procesos | Documentos de Microsoft
description: Obtenga información sobre los campos marcados con un asterisco rojo, que indica que son obligatorios y que deben rellenarse para completar procesos.
services: project-madeira
documentationcenter: ''
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2020
ms.author: solsen
ms.openlocfilehash: f525077069107e1365728aaaaf1e4791a250c6ee
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "4760372"
---
# <a name="detecting-mandatory-fields"></a>Detección de campos obligatorios
Cuando se introducen datos en páginas de [!INCLUDE[prod_short](includes/prod_short.md)], determinados campos aparecen marcados con un asterisco de color rojo. El asterisco rojo significa que el campo debe rellenarse para completar un determinado proceso que lo utilice, como registrar una transacción que utilice su valor.

Aunque el campo contiene un asterisco rojo, no se le obliga a rellenar el campo para ir a otros campos o cerrar la página. El asterisco rojo solo sirve como recordatorio de que se le bloqueará y no podrá terminar un determinado proceso.

## <a name="examples"></a>Ejemplos
En la página **Ficha cliente**, el asterisco de color rojo aparece en el campo **Nombre**, en el campo **Cód. área impuesto** y en los campos del grupo contable para indicar que no puede registrar una transacción de venta para el cliente a menos que se rellenen los campos.

En la página **Ficha producto**, el asterisco de color rojo aparece en el campo **Descripción** para indicar que no podrá especificar el producto en una línea de documento, como un pedido de venta, a menos que se rellene este campo.

## <a name="see-also"></a>Consulte también
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)
