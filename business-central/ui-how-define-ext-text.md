---
title: Agregar líneas adicionales para definir descripciones ampliadas
description: Puede agregar líneas adicionales para ampliar el texto estándar que describe un producto, una cuenta y otros datos.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: b54c8c82a17cb5e1a25beca1115571733fddc2f4
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2021
ms.locfileid: "5784695"
---
# <a name="add-extended-text"></a>Agregar textos adicionales

Puede ampliar la descripción para productos, unidades de almacenamiento, cuentas de contabilidad y recursos agregando líneas adicionales como texto adicional. También puede configurar condiciones para el uso de líneas adicionales.  

La siguiente sección describe cómo agregar texto adicional a una descripción de un producto. Pero los mismos pasos se aplican a las unidades de almacenamiento, las cuentas de contabilidad y los recursos.  

## <a name="to-define-extended-text-for-an-description"></a>Para definir el texto adicional de una descripción

1. Abra la ficha de un producto al que desee agregar texto adicional y, a continuación, elija la acción **Textos adicionales**.
2. Rellene los campos **Código** y **Descripción**.
3. Seleccione **Nuevo**.
4. Rellene el campo **Cód. idioma** o seleccione la casilla **Común a todos los idiomas** si usa códigos de idioma.
5. Rellene los campos **Fecha inicial** y **Fecha final** si desea limitar las fechas en las que se utiliza el texto adicional.
6. En el campo **Texto**, escriba el texto adicional.
7. Seleccione las casillas de verificación correspondientes para los tipos de documento donde desee imprimir el texto adicional.
8. Cierre la página.

Ahora puede agregar este texto adicional a los documentos. El siguiente procedimiento explica cómo agregar texto adicional a un pedido de ventas, pero los mismos pasos se aplican a cualquier otro documento que haya especificado para el texto adicional.  

## <a name="to-add-an-extended-item-text-on-a-sales-order-line"></a>Para agregar un texto de producto adicional en un pedido de venta línea

1. Abra un pedido de venta con la línea de venta para un producto que tenga texto adicional definido. Para obtener más información, vea [Vender productos](sales-how-sell-products.md).
2. Seleccione la línea en cuestión y, a continuación, la acción **Insertar textos adicionales**.

## <a name="see-also"></a>Consulte también

[Configurar inventario](inventory-setup-inventory.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]