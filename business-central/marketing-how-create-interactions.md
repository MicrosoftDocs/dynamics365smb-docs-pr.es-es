---
title: Crear interacciones en contactos y segmentos
description: Aprenda cómo crear interacciones en Business Central para las comunicaciones que mantenga con sus contactos y segmentos.
author: brentholtorf
ms.author: bholtorf
ms.topic: conceptual
ms.reviewer: ivkoleti
ms.date: 12/13/2023
ms.custom: bap-template
ms.search.keywords: 'relationship, prospect'
ms.search.forms: '5077, 5078, 5074, 5076, 5186, 5075, 5079'
---
# <a name="create-interactions-on-contacts-and-segments"></a>Crear interacciones en contactos y segmentos

Puede crear interacciones para rastrear las comunicaciones que tiene con un solo contacto o con múltiples contactos en sus segmentos. Para facilitar la creación de interacciones, [!INCLUDE [prod_short](includes/prod_short.md)] proporciona la guía de configuración asistida **Crear interacción** . La guía le ayuda a capturar los detalles importantes sobre la interacción.

Antes de crear interacciones, debe configurar las plantillas de interacción. Para obtener más información sobre plantillas de interacción, vaya a [Configurar plantillas de interacción](marketing-interactions.md).

## <a name="to-create-an-interaction-with-a-contact"></a>Para crear una interacción con un contacto

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , introduzca **Contactos**, **Vendedor** o **Entrada del registro de interacción** y luego elija el enlace relacionado.
2. Seleccione la acción **Crear interacción**.
3. Rellene los campos según sea necesario. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> Si necesita detenerse antes de haber finalizado la interacción, puede elegir **Cancelar** y luego especificar si desea guardar su configuración para poder continuar más tarde. Para obtener más información sobre las interacciones pospuestas, vaya a [Para terminar de configurar una interacción pospuesta](#to-finish-setting-up-a-postponed-interaction).

## <a name="to-create-an-interaction-on-a-segment"></a>Para crear una interacción en un segmento

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Segmentos** y luego elija el enlace relacionado.
2. Seleccione la acción **Crear interacción**.
3. Rellene los campos según sea necesario. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Después de asignar una interacción a un segmento, hay varias otras acciones que puede realizar en la página **Segmento**:
>
> * Personalice la interacción para cada contacto particular dentro del segmento, por ejemplo seleccionando otra plantilla de interacción en las líneas.  
>* Registre el segmento y las interacciones eligiendo la acción **Registrar** para abrir la página **Registrar segmento**.
> * Cree un segmento nuevo con los mismos contactos eligiendo la casilla **Crear segmento seguimiento**. Esta configuración requiere que se especifique una serie de números para los segmentos en la página **Configuración de marketing**.

Se registra una interacción para cada contacto dentro del segmento en la tabla **Movimiento de registro de interacción** y se archiva el segmento. Puede encontrar los segmentos grabados en la página **Segmento grabado**.

## <a name="to-finish-setting-up-a-postponed-interaction"></a>Para terminar de configurar una interacción aplazada

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Interacciones aplazadas** y, a continuación, elija el vínculo relacionado.
2. Elija la interacción que desea terminar y, a continuación, seleccione la acción **Reanudar**.

## <a name="see-also"></a>Consulte también

[Registrar interacciones](marketing-interactions.md)  
[Gestionar contactos](marketing-contacts.md)  
[Administrar oportunidades de venta](marketing-manage-sales-opportunities.md)  
[Trabajar con Business Central](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
