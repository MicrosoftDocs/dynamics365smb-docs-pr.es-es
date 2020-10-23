---
title: Cómo registrar varios documentos al mismo tiempo | Documentos de Microsoft
description: En lugar de registrar documentos individuales uno por uno, puede seleccionar varios documentos no registrados en una lista para el registro por lotes, ya sea para registro inmediato o programada para, por ejemplo, al final del día.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 1fd25f8b07a359414f62ef4757162f8a73889c27
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2020
ms.locfileid: "3912726"
---
# <a name="post-multiple-documents-at-the-same-time"></a>Registrar varios documentos al mismo tiempo

En lugar de registrar documentos individuales uno por uno, puede seleccionar varios documentos no registrados en una lista para el registro inmediato o para el registro por lotes según una programación, por ejemplo, al final del día. Esto puede ser útil solo si un supervisor puede registrar documentos creados por otros usuarios o para evitar problemas de rendimiento del sistema del registro durante las horas de trabajo.

## <a name="to-post-multiple-purchase-orders-immediately"></a>Para registrar varios pedidos de compra inmediatamente

El siguiente procedimiento explica cómo registrar varios pedidos de compra inmediatamente. Los pasos son parecidos a todos los documentos de compra y venta.

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Pedidos de compra** y luego elija el enlace relacionado.
2. En la página **Pedidos de compra**, seleccione todos los pedidos que se registrarán:
3. En el campo **N.º**, elija los tres puntos verticales para abrir el menú contextual y luego elija la acción **Seleccionar más**.
4. Seleccione la casilla para todas las líneas que representan los pedidos que desea registrar al mismo tiempo.
5. Elija la acción **Registro** y, a continuación, seleccione la acción **Registrar**.
6. Elija el botón **Sí** en el mensaje de confirmación.

## <a name="to-batch-post-multiple-purchase-orders"></a>Para registrar por lotes varios pedidos de compra

El siguiente procedimiento explica cómo registrar por lotes los pedidos de compra. Los pasos son similares para todos los documentos de compra y venta donde la acción **Registro por lotes** está disponible.

> [!NOTE]
> La contabilización por lotes de documentos se realiza en segundo plano. [!INCLUDE [prodshort](includes/prodshort.md)] online incluye trabajos predeterminados para publicación en segundo plano y publicación por lotes. Para obtener más información, consulte [Uso de colas de proyectos para programar tareas](admin-job-queues-schedule-tasks.md).

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Pedidos de compra** y luego elija el enlace relacionado.  
2. En la página **Pedidos de compra**, seleccione todos los pedidos que se registrarán:
3. En el campo **N.º**, elija los tres puntos verticales para abrir el menú contextual y luego elija la acción **Seleccionar más**.
4. Seleccione la casilla para todas las líneas que representan los pedidos que desea registrar al mismo tiempo.
5. Elija la acción **Registro** y, a continuación, seleccione la acción **Registrar por lotes**.
6. En la página **Reg. lotes pedidos compra**, rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
7. Elija el botón **Aceptar**.
8. Para ver posibles problemas que han sucedido durante el registro por lotes de documentos, abra la página **Registro de mensajes de error**.

Los pedidos de compra ahora se agregarán a una entrada de cola de trabajos dedicada, que define cuándo se registran los documentos. Para obtener más información, consulte [Uso de colas de proyectos para programar tareas](admin-job-queues-schedule-tasks.md).

Si selecciona **PDF** en el campo **Tipo de salida de informe**, los pedidos de compra registrados correctamente estarán disponibles en la parte **Bandeja de entrada de informes** de su área de trabajo.

## <a name="see-also"></a>Consulte también

[Registrar documentos y diarios](ui-post-documents-journals.md)  
[Uso de colas de proyectos para programar tareas](admin-job-queues-schedule-tasks.md)  
[Editar documentos registrados](across-edit-posted-document.md)  
[Corregir o cancelar facturas de compra sin abonar](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[Búsqueda de páginas e información con Dígame](ui-search.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
