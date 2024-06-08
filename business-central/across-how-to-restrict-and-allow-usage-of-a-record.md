---
title: Cómo restringir y permitir el uso de un registro
description: 'Para restringir un registro para que no se use, puede introducir dos respuestas de flujo de trabajo en un flujo de trabajo que controle el uso del registro.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 04/26/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="restrict-and-allow-usage-of-a-record"></a>Restringir y permitir el uso de un registro

Si desea restringir un registro para que no se use en ciertas actividades, por ejemplo, hasta que se haya aprobado el registro, puede agregar dos respuestas de flujo de trabajo en el flujo de trabajo que controle el uso del registro. Una respuesta del flujo de trabajo restringe la utilización del registro definida por el evento y las condiciones del flujo de trabajo. La otra respuesta del flujo de trabajo permite la utilización del registro definida por el evento y las condiciones del flujo de trabajo. Existen dos respuestas en la versión predeterminada de [!INCLUDE[prod_short](includes/prod_short.md)] para este propósito: **Agregar restricción de registro** y **Quitar restricción de registro**.

> [!NOTE]  
> La versión predeterminada de [!INCLUDE[prod_short](includes/prod_short.md)] permite restringir el registro de un registro, que se exporte como pago o que se imprima como cheque. Para utilizar otras restricciones, un socio de Microsoft debe personalizar el código de aplicación.  

> [!NOTE]  
> La funcionalidad de flujo de trabajo para restringir y para permitir usar registros no está relacionada con la funcionalidad para bloquear el registro de registros de producto, cliente y proveedor.

El procedimiento siguiente describe cómo restringir el registro de pedidos de compra hasta que se hayan aprobado. El nuevo flujo de trabajo se basará en la plantilla *Flujo de trabajo de aprobación de factura de compra*.  

## <a name="create-a-workflow-step-that-restricts-posting-of-unapproved-purchase-orders"></a>Crear un paso de flujo de trabajo que restrinja el registro de pedidos de compra no aprobados

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Flujos de trabajo** y luego elija el vínculo relacionado.  
2. En la página **Flujos de trabajo**, elija la acción **Nuevo flujo de trabajo de plantilla**. Obtenga más información en [Crear flujos de trabajo a partir de plantillas de flujo de trabajo](across-how-to-create-workflows-from-workflow-templates.md).
3. En la página **Plantillas de flujo de trabajo**, elija la plantilla *Flujo de trabajo de aprobación de factura de compra*.  

   Tenga en cuenta que los dos primeros pasos del flujo de trabajo se aplican a restringir y permitir el uso de facturas de compra. Modifique la condición del evento en el primer paso del nuevo flujo de trabajo para especificar que se aplica a los pedidos de compra.  
4. En la ficha desplegable **Pasos de flujo de trabajo**, elija el campo **Condición on** para el primer paso y, a continuación, para el filtro **Tipo documento**, seleccione **Pedido**.  
5. Empiece a editar, eliminar o agregar otros pasos de flujo de trabajo para reflejar un proceso empresarial que empiece por restringir el registro de los pedidos de compra no aprobados.  

## <a name="see-also"></a>Consulte también .

[Usar flujos de trabajo de aprobación](across-use-workflows.md)  
[Crear flujos de trabajo de aprobación](across-how-to-create-workflows.md)  
[Flujo de trabajo](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
