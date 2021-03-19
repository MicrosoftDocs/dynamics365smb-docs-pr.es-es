---
title: 'Procedimiento: Restringir y permitir el uso de un registro | Documentos de Microsoft'
description: Si desea restringir un registro para que no se use en ciertas actividades, por ejemplo, hasta que se haya aprobado el registro, puede introducir dos respuestas de flujo de trabajo en un flujo de trabajo que controle el uso del registro.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 1c748bd115b17acf925a99f89f538cc9eca41bc3
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5384404"
---
# <a name="restrict-and-allow-usage-of-a-record"></a>Restringir y permitir el uso de un registro
Si desea restringir un registro para que no se use en ciertas actividades, por ejemplo, hasta que se haya aprobado el registro, puede introducir dos respuestas de flujo de trabajo en un flujo de trabajo que controle el uso del registro. Una respuesta del flujo de trabajo restringirá la utilización del registro definida por el evento y las condiciones del flujo de trabajo. Otra respuesta del flujo de trabajo permitirá la utilización del registro definida por el evento y las condiciones del flujo de trabajo. Hay dos respuestas existentes en la versión genérica de [!INCLUDE[prod_short](includes/prod_short.md)] con este fin: **Restringir el uso de un registro** y **Permitir el uso de un registro**.

> [!NOTE]  
>  La versión genérica de [!INCLUDE[prod_short](includes/prod_short.md)] permite restringir el registro de un registro, que se exporte como pago o que se imprima como cheque. Para utilizar otras restricciones, un socio de Microsoft debe personalizar el código de aplicación.  

> [!NOTE]  
>  La funcionalidad de flujo de trabajo para restringir y para permitir usar registros no está relacionada con la funcionalidad para bloquear el registro de registros de producto, cliente y proveedor.

El procedimiento siguiente describe cómo restringir el registro de pedidos de compra hasta que se hayan aprobado. El nuevo flujo de trabajo se basará en la plantilla existente de flujo de trabajo de aprobación de factura de compra.  

## <a name="to-create-a-workflow-step-that-restricts-posting-of-unapproved-purchase-orders"></a>Para crear un paso de flujo de trabajo que restrinja el registro de pedidos de compra no aprobados  
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Flujos de trabajo** y luego elija el enlace relacionado.  
2. En la página **Flujos de trabajo**, cree un nuevo flujo de trabajo denominado Flujo de trabajo de aprobación pedido compra. Para obtener más información, consulte [Crear flujos de trabajo](across-how-to-create-workflows.md).  
3. Seleccione la acción **Copiar desde plantilla de flujo de trabajo**.  
4. Elija el campo **Código de flujo de trabajo** de origen y, a continuación, en la página **Plantillas de flujo de trabajo**, seleccione la plantilla de flujo de trabajo de aprobación de factura de compra.  

     Tenga en cuenta que los dos primeros pasos del flujo de trabajo se aplican a restringir y permitir el uso de facturas de compra. Proceda a modificar la condición del evento en el primer paso del nuevo flujo de trabajo para especificar que se aplica a los pedidos de compra.  
5. En la ficha desplegable **Pasos de flujo de trabajo**, elija el campo **Condiciones de evento** y, a continuación, para el filtro **Tipo documento**, seleccione **Pedido**.  
6. Empiece a editar, eliminar o agregar otros pasos de flujo de trabajo de acuerdo con un proceso empresarial que empiece por restringir el registro de los pedidos de compra no aprobados.  

## <a name="see-also"></a>Consulte también  
[Crear flujos de trabajo](across-how-to-create-workflows.md)   
[Flujo de trabajo](across-workflow.md)   


[!INCLUDE[footer-include](includes/footer-banner.md)]