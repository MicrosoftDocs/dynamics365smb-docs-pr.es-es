---
title: Configurar información de inventario general
description: Describe cómo definir la configuración de existencias general para que pueda administrar su almacén y stock.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'warehouse, stock'
ms.search.form: '30, 456, 461'
ms.date: 07/28/2021
ms.author: edupont
---
# <a name="set-up-general-inventory-information"></a><a name="set-up-general-inventory-information"></a><a name="set-up-general-inventory-information"></a><a name="set-up-general-inventory-information"></a>Configurar información de inventario general

Especifique la configuración del inventario en la página **Configuración de inventario**.

## <a name="to-set-up-general-inventory-information"></a><a name="to-set-up-general-inventory-information"></a><a name="to-set-up-general-inventory-information"></a><a name="to-set-up-general-inventory-information"></a>Para configurar la información de inventario general

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Config. existencias** y luego elija el enlace relacionado.
2. En la página **Configuración de inventario**, rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Para obtener información detallada sobre los campos de costes, **Contabilización automática de costes**, **Registro de coste previsto en P/G** y **Valoración de existencias predeterminada**, consulte [Conciliar costes de inventario con la contabilidad general](finance-how-to-post-inventory-costs-to-the-general-ledger.md), [Detalles de diseño: variación de existencias](design-details-inventory-costing.md) y [Detalles de diseño: registro de coste previsto](design-details-expected-cost-posting.md). Para obtener más información sobre el cálculo de costes en general, consulte [Gestión de variación de existencias](finance-manage-inventory-costs.md).  

Si desea que el sistema incluya un tiempo de manipulación en almacén de entrada en el cálculo del compromiso de entrega del pedido en la línea de compra, configúrelo como un valor predeterminado para las existencias, en la página **Configuración inventario** y para su almacén. Para obtener más información, consulte [Calcular las fechas de compromiso de entrega de pedido](sales-how-to-calculate-order-promising-dates.md).  

> [!NOTE]
> El campo **Ajuste automático de costes** está establecido en *Siempre* de forma predeterminada para garantizar que los valores de inventario sean siempre correctos en contabilidad, lo que a su vez mantiene actualizadas sus estadísticas de ventas y ganancias. Los cambios de costes de los movimientos de entrada, como pueden ser aquellos relacionados con las compras o con la salida de producción, se asignan a los movimientos de salida relacionados, como son las ventas o las transferencias. Esto es útil para nuevos clientes y pequeñas empresas de [!INCLUDE[prod_short](includes/prod_short.md)] con niveles de transacciones de inventario relativamente bajos.
>
> Sin embargo, a medida que crece una empresa y aumentan los niveles de inventario, esto puede ralentizar el rendimiento del sistema. Para minimizar el rendimiento reducido durante la publicación, seleccione una opción de tiempo para definir con cuanta antelación desde la fecha de trabajo puede ocurrir una transacción entrante para desencadenar potencialmente el ajuste de las entradas de valor saliente relacionadas.
>
> Alternativamente, puede ajustar manualmente los costes a intervalos regulares con el trabajo por lotes Ajustar coste - Entradas de productos. También puede desactivar el registro de costes o establecer el campo **Ajuste automático de costes** a *Nunca*. En ambos casos, se muestra una notificación desde la cual puede iniciar una guía de configuración asistida para ayudarlo a programar tareas para la cola de proyectos. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Consulte también

[Configuración de inventario](inventory-setup-inventory.md)  
[Detalles de diseño: Métodos de coste](design-details-costing-methods.md)  
[Gestionar inventario](inventory-manage-inventory.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Cambiar las funciones que se muestran](ui-experiences.md)  
[Funciones empresariales generales](ui-across-business-areas.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
