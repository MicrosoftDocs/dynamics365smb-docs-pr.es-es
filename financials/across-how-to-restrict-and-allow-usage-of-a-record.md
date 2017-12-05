---
title: 'Procedimiento: Restringir y permitir el uso de un registro | Documentos de Microsoft'
description: Si desea restringir un registro para que no se use en ciertas actividades, por ejemplo, hasta que se haya aprobado el registro, puede introducir dos respuestas de flujo de trabajo en un flujo de trabajo que controle el uso del registro.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: 0dc8b3eeecfbf3f4a96985f4e4adaf0b3a5a21d0
ms.contentlocale: es-es
ms.lasthandoff: 11/10/2017

---
# <a name="how-to-restrict-and-allow-usage-of-a-record"></a>Procedimiento: Restringir y permitir el uso de un registro
Si desea restringir un registro para que no se use en ciertas actividades, por ejemplo, hasta que se haya aprobado el registro, puede introducir dos respuestas de flujo de trabajo en un flujo de trabajo que controle el uso del registro. Una respuesta del flujo de trabajo restringirá la utilización del registro definida por el evento y las condiciones del flujo de trabajo. Otra respuesta del flujo de trabajo permitirá la utilización del registro definida por el evento y las condiciones del flujo de trabajo. Hay dos respuestas existentes en la versión genérica de [!INCLUDE[d365fin](includes/d365fin_md.md)] con este fin: **Restringir el uso de un registro** y **Permitir el uso de un registro**.

> [!NOTE]  
>  La versión genérica de [!INCLUDE[d365fin](includes/d365fin_md.md)] permite restringir el registro de un registro, que se exporte como pago o que se imprima como cheque. Para utilizar otras restricciones, un socio de Microsoft debe personalizar el código de aplicación.  

> [!NOTE]  
>  La funcionalidad de flujo de trabajo para restringir y para permitir usar registros no está relacionada con la funcionalidad para bloquear el registro de registros de producto, cliente y proveedor.

El procedimiento siguiente describe cómo restringir el registro de pedidos de compra hasta que se hayan aprobado. El nuevo flujo de trabajo se basará en la plantilla existente de flujo de trabajo de aprobación de factura de compra.  

## <a name="to-create-a-workflow-step-that-restricts-posting-of-unapproved-purchase-orders"></a>Para crear un paso de flujo de trabajo que restrinja el registro de pedidos de compra no aprobados  
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Flujos de trabajo** y, a continuación, seleccione el vínculo relacionado.  
2. En la ventana **Flujos de trabajo**, cree un nuevo flujo de trabajo denominado Flujo de trabajo de aprobación pedido compra. Para obtener más información, consulte [Procedimiento: Crear flujos de trabajo](across-how-to-create-workflows.md).  
3. Seleccione la acción **Copiar desde plantilla de flujo de trabajo**.  
4. Elija el campo **Código de flujo de trabajo** de origen y, a continuación, en la ventana **Plantillas de flujo de trabajo**, seleccione la plantilla de flujo de trabajo de aprobación de factura de compra.  

     Tenga en cuenta que los dos primeros pasos del flujo de trabajo se aplican a restringir y permitir el uso de facturas de compra. Proceda a modificar la condición del evento en el primer paso del nuevo flujo de trabajo para especificar que se aplica a los pedidos de compra.  
5. En la ficha desplegable **Pasos de flujo de trabajo**, elija el campo **Condiciones de evento** y, a continuación, para el filtro **Tipo documento**, seleccione **Pedido**.  
6. Empiece a editar, eliminar o agregar otros pasos de flujo de trabajo de acuerdo con un proceso empresarial que empiece por restringir el registro de los pedidos de compra no aprobados.  

## <a name="see-also"></a>Consulte también  
[Procedimiento: Crear flujos de trabajo](across-how-to-create-workflows.md)   
[Flujo de trabajo](across-workflow.md)   

