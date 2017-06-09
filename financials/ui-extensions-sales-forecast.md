---
title: "Previsión de ventas e inventario | Documentos de Microsoft"
description: "Proporciona información sobre la extensión Previsión de inventario y ventas."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, budget
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: ebaea8b98264e981f9ad2e0abda592e2e4a72427
ms.contentlocale: es-es
ms.lasthandoff: 05/04/2017


---
# <a name="sales-and-inventory-forecast-for-dynamics-365-for-financials"></a>Previsión de inventario y ventas para Dynamics 365 for Financials
La gestión del inventario es un equilibrio entre el servicio al cliente y gestionar el coste. Por un lado, un inventario bajo requiere menos capital de trabajo, pero, por otro lado, la falta de stock puede llevar potencialmente la pérdida de ventas. La extensión de la previsión de inventario y ventas predice ventas potenciales con datos históricos y ofrece una visión general clara de la falta de stock prevista. Según la previsión, la extensión ayuda a crear solicitudes de reposición a los proveedores y le ahorra tiempo.  

## <a name="setting-up-forecasting"></a>Configurar la previsión
En [!INCLUDE[d365fin](includes/d365fin_md.md)], la conexión a [Cortana Intelligence](https://www.microsoft.com/en-us/cloud-platform/what-is-cortana-intelligence-suite) ya está configurada automáticamente. Pero puede configurar la previsión para que utilice diferentes tipos de periodo de información como, por ejemplo, cambiar la previsión mensual por la trimestral. También puede elegir el número de periodos para calcular la previsión según como desea que sea. Sugerimos que utilice la previsión mensual y con un horizonte de 12 meses.  

## <a name="using-the-forecasts"></a>Usar las previsiones
La extensión usa Cortana Intelligence para pronosticar las ventas futuras en función del historial de ventas para ayudarle a evitar la escasez de inventario. Por ejemplo, cuando elige un producto en la ventana **Productos**, la ficha del panel **Previsión del producto** muestra las ventas futuras estimadas de ese producto. De esta manera podrá ver si pronto agotará el stock del producto.  

También puede utilizar la extensión para sugerir cuándo desea almacenar el inventario. Por ejemplo, si crea un pedido de compra para Fabrikam porque desea comprar su nueva silla de escritorio, la extensión de Previsión de inventario y ventas sugerirá que también reaprovisione la silla giratoria LONDON que normalmente le compra a ese proveedor. Eso se debe a que la extensión prevé que se le agotará el stock de la silla giratoria LONDON durante los próximos dos meses, de modo que es posible que desee pedir más sillas ahora.  

## <a name="see-also"></a>Consulte también
[Ventas](sales-manage-sales.md)  
[Grupos contables inventario](inventory-manage-inventory.md)  
[Personalización de [!INCLUDE[d365fin](includes/d365fin_md.md)] utilizando extensiones](ui-extensions.md)  

