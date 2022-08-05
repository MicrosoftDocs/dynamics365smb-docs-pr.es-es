---
title: 'Procedimiento: Restringir y permitir el uso de un registro'
description: Si desea restringir un registro para que no se use, puede introducir dos respuestas de flujo de trabajo en un flujo de trabajo que controle el uso del registro.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/11/2021
ms.author: edupont
ms.openlocfilehash: 7873091d64e55460986437cf255d98cd0d00b6d3
ms.sourcegitcommit: f1e272485a0e675d337a694aba3e35a5daf43920
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 07/09/2022
ms.locfileid: "9130151"
---
# <a name="restrict-and-allow-usage-of-a-record"></a>Restringir y permitir el uso de un registro

Si desea restringir un registro para que no se use en ciertas actividades, por ejemplo, hasta que se haya aprobado el registro, puede introducir dos respuestas de flujo de trabajo en un flujo de trabajo que controle el uso del registro. Una respuesta del flujo de trabajo restringirá la utilización del registro definida por el evento y las condiciones del flujo de trabajo. Otra respuesta del flujo de trabajo permitirá la utilización del registro definida por el evento y las condiciones del flujo de trabajo. Existen dos respuestas en la versión predeterminada de [!INCLUDE[prod_short](includes/prod_short.md)] para este propósito: **Agregar restricción de registro** y **Quitar restricción de registro**.

> [!NOTE]  
> La versión predeterminada de [!INCLUDE[prod_short](includes/prod_short.md)] permite restringir el registro de un registro, que se exporte como pago o que se imprima como cheque. Para utilizar otras restricciones, un socio de Microsoft debe personalizar el código de aplicación.  

> [!NOTE]  
> La funcionalidad de flujo de trabajo para restringir y para permitir usar registros no está relacionada con la funcionalidad para bloquear el registro de registros de producto, cliente y proveedor.

El procedimiento siguiente describe cómo restringir el registro de pedidos de compra hasta que se hayan aprobado. El nuevo flujo de trabajo se basará en la plantilla existente de flujo de trabajo de aprobación de factura de compra.  

## <a name="to-create-a-workflow-step-that-restricts-posting-of-unapproved-purchase-orders"></a>Para crear un paso de flujo de trabajo que restrinja el registro de pedidos de compra no aprobados

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Flujos de trabajo** y luego elija el enlace relacionado.  
2. En la página **Flujos de trabajo**, elija la acción **Nuevo flujo de trabajo de plantilla**. Para obtener más información, consulte [Crear flujos de trabajo a partir de plantillas de flujo de trabajo](across-how-to-create-workflows-from-workflow-templates.md).
3. En la página **Plantillas de flujo de trabajo**, elija la plantilla *Flujo de trabajo de aprobación de factura de compra*.  

   Tenga en cuenta que los dos primeros pasos del flujo de trabajo se aplican a restringir y permitir el uso de facturas de compra. Proceda a modificar la condición del evento en el primer paso del nuevo flujo de trabajo para especificar que se aplica a los pedidos de compra.  
4. En la ficha desplegable **Pasos de flujo de trabajo**, elija el campo **Condición on** para el primer paso y, a continuación, para el filtro **Tipo documento**, seleccione **Pedido**.  
5. Empiece a editar, eliminar o agregar otros pasos de flujo de trabajo de acuerdo con un proceso empresarial que empiece por restringir el registro de los pedidos de compra no aprobados.  

## <a name="see-also"></a>Consulte también .

[Crear flujos de trabajo](across-how-to-create-workflows.md)  
[Flujo de trabajo](across-workflow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]