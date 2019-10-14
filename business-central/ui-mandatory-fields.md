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
ms.date: 10/01/2019
ms.author: solsen
ms.openlocfilehash: 6cab6247c8edb050a038ef7641b646f1a7412588
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2019
ms.locfileid: "2310833"
---
# <a name="detecting-mandatory-fields"></a>Detección de campos obligatorios
Cuando se introducen datos en páginas de [!INCLUDE[d365fin](includes/d365fin_md.md)], determinados campos aparecen marcados con un asterisco de color rojo. El asterisco rojo significa que el campo debe rellenarse para completar un determinado proceso que lo utilice, como registrar una transacción que utilice su valor.

Aunque el campo contiene un asterisco rojo, no se le obliga a rellenar el campo para ir a otros campos o cerrar la página. El asterisco rojo solo sirve como recordatorio de que se le bloqueará y no podrá terminar un determinado proceso.

## <a name="examples"></a>Ejemplos
En la página **Ficha cliente**, el asterisco de color rojo aparece en el campo **Nombre**, en el campo **Cód. área impuesto** y en los campos del grupo contable para indicar que no puede registrar una transacción de venta para el cliente a menos que se rellenen los campos.

En la página **Ficha producto**, el asterisco de color rojo aparece en el campo **Descripción** para indicar que no podrá especificar el producto en una línea de documento, como un pedido de venta, a menos que se rellene este campo.

## <a name="see-also"></a>Consulte también
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
