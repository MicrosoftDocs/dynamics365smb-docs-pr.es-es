---
title: Crear interacciones en contactos y segmentos | Documentos de Microsoft
description: Describe cómo crear interacciones para las comunicaciones que mantenga con sus contactos y segmentos en Business Central, por ejemplo, con el correo directo.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: 92965b353dadb78e50b11138a832115885518f4f
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2021
ms.locfileid: "5780712"
---
# <a name="create-interactions-on-contacts-and-segments"></a>Crear interacciones en contactos y segmentos
Puede crear interacciones para registrar todas las interacciones y comunicaciones que mantenga con sus contactos y segmentos, por ejemplo, con el correo directo.

Antes de crear interacciones, debe configurar las plantillas de interacción. Para obtener más información, vea [Configurar plantillas de interacción](marketing-interactions.md).

## <a name="to-create-an-interaction"></a>Para crear interacciones
1. Abra el contacto, el vendedor o el movimiento de registro de interacción.
2. Seleccione la acción **Crear interacción**.
3. Rellene los campos y, a continuación, elija el botón **Aceptar**.

> [!NOTE]  
>   Si tiene que ejecutar otra tarea antes de finalizar la interacción, puede seleccionar **Cancelar** y, a continuación, finalizar la interacción más adelante. Esto hace que se aplace la interacción.

## <a name="to-finish-and-delete-postponed-interactions"></a>Para finalizar y eliminar interacciones aplazadas
1. Abra el contacto, el vendedor o el movimiento de registro de interacción.
2. Seleccione **Interacciones aplazadas**.
3. Seleccione la interacción que desea terminar y, a continuación, seleccione la acción **Reanudar**.

## <a name="to-create-an-interaction-on-a-segment"></a>Para crear una interacción en un segmento
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Segmentos** y luego elija el enlace relacionado.
2. En la página **Segmento**, en la sección **Interacción**, rellene los campos para especificar qué interacción quiere asignar al segmento.

    Después de asignar una interacción al segmento puede personalizar la interacción para cada contacto particular dentro del segmento, por ejemplo seleccionando otra plantilla de interacción en las líneas de la página **Segmento**.  
3. Para registrar el segmento y las interacciones, seleccione la acción **Registrar**. Se abre la página **Grabar segmento**.
4. Active la casilla de verificación **Crear segmento seguimiento** si desea crear un segmento nuevo que contenga los mismos contactos. Para crear un segmento de seguimiento, debe haber especificado antes números de serie para los segmentos en la página **Configuración marketing**.

Se registra una interacción para cada contacto dentro del segmento en la tabla **Movimiento de registro de interacción** y se archiva el segmento. Puede encontrar los segmentos grabados en la página **Segmento grabado**.

Si activó la casilla **Crear segmento seguimiento**, se creará un nuevo segmento que contendrá los mismos contactos que el segmento recién archivado.

## <a name="see-also"></a>Consulte también
[Registrar interacciones](marketing-interactions.md)  
[Gestionar contactos](marketing-contacts.md)  
[Administrar oportunidades de venta](marketing-manage-sales-opportunities.md)  
[Trabajar con Business Central](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]