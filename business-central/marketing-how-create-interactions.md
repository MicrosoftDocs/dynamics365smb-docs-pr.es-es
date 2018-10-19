---
title: Crear interacciones en contactos y segmentos | Documentos de Microsoft
description: "Describe cómo crear interacciones para las comunicaciones que mantenga con sus contactos y segmentos en Business Central, por ejemplo, con el correo directo."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: ee1c27157febaf848c417eb163adea2eaa586e1f
ms.contentlocale: es-es
ms.lasthandoff: 09/28/2018

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
1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Segmentos** y luego elija el enlace relacionado.
2. En la ventana **Segmento**, en la sección **Interacción**, rellene los campos para especificar qué interacción quiere asignar al segmento.

    Después de asignar una interacción al segmento puede personalizar la interacción para cada contacto particular dentro del segmento, por ejemplo seleccionando otra plantilla de interacción en las líneas de la ventana **Segmento**.  
3. Para registrar el segmento y las interacciones, seleccione la acción **Registrar**. Se abre la ventana **Grabar segmento**.
4. Active la casilla de verificación **Crear segmento seguimiento** si desea crear un segmento nuevo que contenga los mismos contactos. Para crear un segmento de seguimiento, debe haber especificado antes números de serie para los segmentos en la ventana **Configuración marketing**.

Se registra una interacción para cada contacto dentro del segmento en la tabla **Movimiento de registro de interacción** y se archiva el segmento. Puede encontrar los segmentos grabados en la ventana **Segmento grabado**.

Si activó la casilla **Crear segmento seguimiento**, se creará un nuevo segmento que contendrá los mismos contactos que el segmento recién archivado.

## <a name="see-also"></a>Consulte también
[Registrar interacciones](marketing-interactions.md)  
[Gestionar contactos](marketing-contacts.md)  
[Administrar oportunidades de venta](marketing-manage-sales-opportunities.md)  
[Configurar la gestión de relaciones](marketing-setup-marketing.md)  
[Trabajar con Business Central](ui-work-product.md)

