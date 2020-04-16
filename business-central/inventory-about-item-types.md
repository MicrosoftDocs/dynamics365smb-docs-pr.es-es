---
title: Descripción de los tipos de productos | Documentos de Microsoft
description: Puede ajustar la valoración de inventario de un producto utilizando los métodos de costes FIFO o Promedio, por ejemplo, cuando los costes de producto cambien por motivos distintos de las transacciones.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: ab3da8450586928a02d17ccce14c704ed6d7c8fe
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/01/2020
ms.locfileid: "3182401"
---
# <a name="about-item-types"></a>Acerca de los tipos de productos
En el campo **Tipo** en la página **Ficha de producto**, puede seleccionar para qué se usa el producto en su negocio y, por lo tanto, cómo se administra en el sistema. Existen tres opciones:

|Opción|Propósito típico|
|------|-----------|
|Grupos contables inventario|Una unidad física, como una bicicleta, para un soporte comercial completo.|
|No inventario|Una unidad física, como un tornillo, para soporte comercial limitado, por ejemplo, porque el artículo solo se usa internamente y tiene un bajo coste.|
|Servicio|Una unidad de tiempo de trabajo, como una hora de consultoría, para soporte comercial limitado.|

El tipo de **inventario** implica el seguimiento completo de la cantidad y el valor del inventario. Por lo tanto, todos los tipos de transacciones de artículos son compatibles y los artículos de tipo Inventario se pueden usar con todas las características de manejo de artículos.

Los tipos de **Servicio** y **No inventario** no implican el seguimiento de la cantidad y el valor del inventario. Por lo tanto, solo se admiten los tipos y las características de transacción de los elementos seleccionados.

Los tres tipos de elementos admiten las siguientes características, respectivamente.

|Tipo de producto|Ccial|Compra|Consumo de proyecto|Consumo de servicio|Consumo de ensamblado|Producción Consumo|Salida de ensamblado|Salida de producción|Transferencia de ubicación|Recuento físico|Revalorización de inventario|Inventario y valoración|Seguim. prod.|Reserva|Gestión de almacén|Planificación|
|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|
|Grupos contables inventario|Sí|Sí|Sí|Sí|Sí|Sí|Sí|Sí|Sí|Sí|Sí|Sí|Sí|Sí|Sí|Sí|
|No inventario|Sí|Sí|Sí|Sí|Sí|Sí|N.º|N.º|N.º|N.º|N.º|N.º|N.º|N.º|N.º|N.º|
|Servicio|Sí|Sí|Sí|N.º|N.º|N.º|N.º|N.º|N.º|N.º|N.º|N.º|N.º|N.º|N.º|N.º|

> [!NOTE]
> Los productos que ofrece a sus clientes pero que no desea administrar en su sistema hasta que comience a venderlos se pueden configurar como productos del catálogo. Los productos del catálogo no deben confundirse con artículos regulares de tipo No inventario. Para obtener más información, consulte [Trabajar con productos del catálogo](inventory-how-work-nonstock-items.md).

> [!NOTE]
> Los productos de los clientes con los que realiza el servicio, como una impresora, se denominan productos de servicio. Los productos de servicio no tienen nada que ver con artículos regulares o del catálogo. Sin embargo, los componentes del servicio pueden ser productos regulares. Para obtener más información, consulte [Configurar componentes de servicio y de productos](service-how-setup-service-items.md).

## <a name="see-also"></a>Consulte también
[Registro de productos nuevos](inventory-how-register-new-items.md)  
[Configurar inventario](inventory-setup-inventory.md)  
[Gestión de costes de inventario](finance-manage-inventory-costs.md)  
[Grupos contables inventario](inventory-manage-inventory.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
