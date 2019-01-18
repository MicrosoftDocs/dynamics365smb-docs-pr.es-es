---
title: "Usar la extensión de previsión de ventas e inventario para administrar el inventario | Documentos de Microsoft"
description: "Esta extensión le ayuda a predecir ventas, obtener un resumen claro de la falta de stock prevista e incluso le ayuda a crear solicitudes de reposición para proveedores."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, budget
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 3ae36c5cb7f1738bded3947c99c197221a621f07
ms.contentlocale: es-es
ms.lasthandoff: 11/26/2018

---
# <a name="the-sales-and-inventory-forecast-extension"></a>Extensión de previsión de ventas e inventario
La gestión del inventario es un equilibrio entre el servicio al cliente y gestionar el coste. Por un lado, un inventario bajo requiere menos capital de trabajo, pero, por otro lado, la falta de stock puede llevar potencialmente la pérdida de ventas. La extensión de la previsión de inventario y ventas predice ventas potenciales con datos históricos y ofrece una visión general clara de la falta de stock prevista. Según la previsión, la extensión ayuda a crear solicitudes de reposición a los proveedores y le ahorra tiempo.  

## <a name="setting-up-forecasting"></a>Configurar la previsión
En [!INCLUDE[d365fin](includes/d365fin_md.md)], la conexión a [Cortana Intelligence](https://www.microsoft.com/en-us/cloud-platform/what-is-cortana-intelligence-suite) ya está configurada automáticamente. Pero puede configurar la previsión para que utilice diferentes tipos de periodo de información como, por ejemplo, cambiar la previsión mensual por la trimestral. También puede elegir el número de periodos para calcular la previsión según como desea que sea. Sugerimos que utilice la previsión mensual y con un horizonte de 12 meses.  

## <a name="using-the-forecasts"></a>Usar las previsiones
La extensión usa Cortana Intelligence para pronosticar las ventas futuras en función del historial de ventas para ayudarle a evitar la escasez de inventario. Por ejemplo, cuando elige un producto en la página **Productos**, la ficha del panel **Previsión del producto** muestra las ventas futuras estimadas de ese producto. De esta manera podrá ver si pronto agotará el stock del producto.  

También puede utilizar la extensión para sugerir cuándo desea almacenar el inventario. Por ejemplo, si crea un pedido de compra para Fabrikam porque desea comprar su nueva silla de escritorio, la extensión de Previsión de inventario y ventas sugerirá que también reaprovisione la silla giratoria LONDON que normalmente le compra a ese proveedor. Eso se debe a que la extensión prevé que se le agotará el stock de la silla giratoria LONDON durante los próximos dos meses, de modo que es posible que desee pedir más sillas ahora.  

## <a name="see-also"></a>Consulte también
[Ventas](sales-manage-sales.md)  
[Inventario](inventory-manage-inventory.md)  
[Personalizar [!INCLUDE[d365fin](includes/d365fin_md.md)] con extensiones](ui-extensions.md)  

