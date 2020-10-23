---
title: Revertir registro de salida | Documentos de Microsoft
description: En ciertas ocasiones es necesario revertir el registro de la salida. Por ejemplo, si se ha cometido un error en la introducción de los datos y se ha registrado una cantidad de salida incorrecta en una orden de producción.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: b33b0642d8cee6e26edeeece47c8fceb72c2bfa1
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2020
ms.locfileid: "3921572"
---
# <a name="reverse-output-posting"></a>Revertir el registro de la salida
En ciertas ocasiones es necesario revertir el registro de la salida. Por ejemplo, si se ha cometido un error en la introducción de los datos y se ha registrado una cantidad de salida incorrecta en una orden de producción.  

## <a name="to-reverse-an-output-posting"></a>Para revertir un registro de salida  
1.  Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Diario salida** y luego elija el enlace relacionado. Seleccione el lote.  
2. Rellene los campos según sea necesario. Para obtener más información, vea [Registro de salida y tiempos de ejecución por lotes](production-how-to-post-output-quantity.md).
3.  En el campo **Liq. por nº orden**, seleccione el movimiento de contabilidad de productos asociado. De esta forma se reserva la capacidad y los movimientos de producto.  
4. Registre la reversión registrando el diario.  

Los movimientos del diario de salida se registran como un ajuste positivo.  

## <a name="see-also"></a>Consulte también  
 [Fabricación](production-manage-manufacturing.md)    
 [Configuración de fabricación](production-configure-production-processes.md)  
 [Planificación](production-planning.md)      
 [Inventario](inventory-manage-inventory.md)  
 [Compras](purchasing-manage-purchasing.md)  
 [Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
