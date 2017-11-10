---
title: "Cómo modificar las sugerencias de planificación en una vista gráfica | Documentos de Microsoft"
description: "Una actividad típica de planificación consiste en cambiar o añadir líneas de la hoja de planificación para modificar los pedidos de suministros sugeridos antes de confirmarlos ejecutando la función **Ejecutar mensajes acción**. Una alternativa a hacerlo en la hoja de trabajo de planificación es utilizar una vista gráfica."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 6cdd86fb96e89e99ea2378221d2991bd640f887e
ms.contentlocale: es-es
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-modify-planning-suggestions-in-a-graphical-view"></a>Cómo modificar las sugerencias de planificación en una vista gráfica
Una actividad típica de planificación consiste en cambiar o añadir líneas de la hoja de planificación para modificar los pedidos de suministros sugeridos antes de confirmarlos ejecutando la función **Ejecutar mensajes acción**. Una alternativa a hacerlo en la hoja de trabajo de planificación es utilizar una vista gráfica.

En la ventana **Disponibilidad de producto por escala de tiempo**, puede modificar algunos pedidos de suministro y sugerencias si arrastra los elementos del eje x para cambiar la cantidad o si arrastra los elementos del eje y para cambiar la fecha de vencimiento.  

 En la ventana **Disponib. prod. por escala de tiempo** y **Hoja planificación** puede realizar los cambios siguientes:  

-   Modificar un pedido de suministro sugerido que solo existe como una línea de la planificación.  
-   Modificar el pedido de suministro existente que el sistema de planificación sugiere cambiar.  
-   Crear un nuevo pedido de suministro sugerido y modificarlo.  

Para obtener más información acerca de los tipos de línea de planificación que se muestran, consulte el campo Descripción en la ficha desplegable **Cambios de eventos**.  

Cuando elige **Guardar cambios** en la ventana **Disponib. prod. por escala de tiempo**, las modificaciones realizadas se copian en la hoja de planificación o demanda. Ahora puede aplicarlos con la función **Ejecutar mensajes acción.-Plan**.  

El siguiente procedimiento muestra cómo modificar las sugerencias de suministro mediante arrastrar y soltar. Como alternativa, puede cambiar los campos **Fecha de vencimiento** y **Cantidad** en la ficha desplegable **Cambios en eventos** y ver inmediatamente los cambios gráficamente en la ficha desplegable **Escala de tiempo** en la ventana **Hoja planificación**.  

## <a name="to-modify-suggested-supply-orders-in-the-graphical-view"></a>Para modificar los pedidos de suministros sugeridos en la vista gráfica  
1.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Disponibilidad de producto por escala de tiempo** y, a continuación, seleccione el vínculo relacionado.  

    La ventana **Disponib. prod. por escala de tiempo** se abre con el número de producto, almacén y variante del producto en la línea seleccionada de la planificación prellenada en los campos en la ficha desplegable **Opciones**. La ficha desplegable **Escala de tiempo** muestra una representación gráfica del inventario proyectado del producto, incluidas las sugerencias de la planificación.  

2.  Asegúrese de que el campo **Incluir sugerencias de planificación** se ha seleccionado.  
3.  Buscar los pedidos de suministro sugeridos que desea modificar. Puede identificar los elementos modificables por el círculo verde y el icono de disco. Para obtener más información acerca de los diferentes símbolos, vea la sección "Símbolos e iconos en la ficha desplegable".  
4.  Coloque el puntero sobre el círculo verde hasta que se agrande y el puntero cambie a la forma de movimiento (cuatro flechas).  
5.  Mantenga pulsado el botón del mouse mientras arrastra el puntero hacia arriba o hacia abajo para modificar la cantidad. Mantenga pulsado el botón del mouse mientras arrastra el puntero hacia la izquierda y hacia la derecha para modificar la fecha de vencimiento.  
6.  Además de mover los elementos mediante arrastrar y soltar, puede modificar las sugerencias de planificación utilizando varias funciones del menú desplegable. Acceda al menú desplegable para el círculo verde de un producto de suministro sugerido y seleccione una las funciones siguientes  

    |Función|Description|  
    |--------------|---------------------------------------|  
    |**Crear nuevo suministro**|Cree un nuevo punto de elemento donde acceda al menú desplegable, que representa un nuevo pedido de suministro sugerido. Se convierte en una nueva línea en la hoja de planificación cuando elige **Guardar cambios**.<br /><br /> **NOTA**: Si los campos **Filtro almacén** o **Filtro variante** de la ficha desplegable **Opciones** está vacía o tiene más de un valor de filtro, el nuevo suministro se crea y guarda posteriormente en la hoja de planificación o demanda con los siguientes códigos:<br /><br /> * Si el campo de filtro está vacío, el nuevo suministro se crea sin un código de almacén o variante.<br /><br /> * Si se define más de un valor de filtro, el nuevo suministro se crea para el primer valor de filtro según el método de ordenación.<br /><br /> Si desea otro código de variante o de almacén, debe modificarlo manualmente en la nueva línea de planificación.|  
    |**Auto-Ajuste suministro**|Optimiza un nuevo suministro que ha creado en el gráfico para asegurarse de que da como resultado un inventario de cero antes del suministro siguiente.|  
    |**Eliminar suministro**|Elimina el elemento en la ficha desplegable **Escala de tiempo** y elimina la línea de planificación cuando elige **Guardar cambios**. El icono cambia a un disco que tiene una cruz de color rojo cuando se ha eliminado el suministro.<br /><br /> **NOTA**: Solo puede eliminar un suministro de tipo de mensajes de acción **Nuevo**. Después de elegir **Guardar cambios**, debe eliminar manualmente la línea de planificación en cuestión en la hoja de planificación o demanda.|  

7.  Seleccione la acción **Volver a cargar** si desea restablecer todos los cambios realizados después de la última vez que abrió la ventana **Disponibilidad de producto por escala de tiempo** o seleccionado **Volver a cargar**.  
8. Cuando se colocan los elementos donde desea en el diagrama, seleccione **Guardar cambios** para copiar la cantidad modificada y la fecha cambiada en las líneas de planificación o demanda que representan los elementos gráficos.  

Para implementar los cambios del plan de suministro, debe seguir los mensajes de acción resultantes de la hoja de planificación o demanda. Para obtener más información, consulte Ejecutar mensajes acción.-Plan..

## <a name="symbols-and-icons-on-the-timeline-fasttab"></a>Símbolos e iconos en la ficha desplegable Escala de tiempo
 |Símbolo/icono|Description|  
 |------------------|---------------------------------------|  
 |Cruz negra|Pedidos (aprovisionamiento y demanda).<br /><br /> -   No puede modificar.<br />- Visible cuando está seleccionado el campo **Mostrar inventario proyectado** (gráfico anaranjado).|  
 |Círculo rojo|Pedidos de suministros existentes que no están incluidos en las sugerencias de la planificación.<br /><br /> -   No puede modificar.<br />- Visible cuando está seleccionado el campo **Mostrar inventario proyectado** (gráfico anaranjado).|  
 |Asterisco amarillo|Previsión de la demanda.<br /><br /> -   No puede modificar.<br />-   Visible cuando el campo **Nombre de previsión** tiene un valor.<br /><br /> Cuando se seleccionan los campos **Mostrar inventario proyectado** e **Incluir sugerencias de planificación**, cada asterisco amarillo tiene una parte vinculada en el gráfico opuesto. Esto ilustra como un suministro sugerido satisface la demanda prevista.|  
 |Círculo verde con un icono en forma de disco que tiene una cruz de color rojo|Pedido de suministro sugerido con el mensaje de acción *Cancelar*.<br /><br /> -   No puede modificar.<br />- Visible cuando está seleccionado el campo **Incluir sugerencias de planificación** (gráfico verde).|  
 |Círculo verde con un icono en forma de disco que tiene un asterisco|Pedidos de suministros sugeridos con los mensajes de acción *Nuevo*.<br /><br /> -   Se puede modificar.<br />- Visible cuando está seleccionado el campo **Incluir sugerencias de planificación** (gráfico verde).|  
 |Círculo verde con un icono en forma de disco que tiene una o dos flechas|Pedidos de suministros sugeridos con el mensaje de acción *Volver a programar*, *Cambiar cdad.* o *Reprog. y Cambiar cdad.*<br /><br /> -   Se puede modificar.<br />- Visible cuando está seleccionado el campo **Incluir sugerencias de planificación** (gráfico verde).<br /><br /> Las flechas reflejan la dirección de la sugerencia de la planificación. Por ejemplo, una flecha izquierda con una flecha hacia arriba refleja el mensaje de acción *Reprog. y Cambiar cdad.* que consiste en una actualización hacia atrás y un aumento de cantidad.|  

Cuando acceda al menú desplegable para la ficha desplegable **Escala de tiempo**, las funciones siguientes aparecen dependiendo de lo que elija  

 |Función|Description|  
 |--------------|---------------------------------------|  
 |**Crear nuevo suministro**|Crea un nuevo elemento en el punto donde acceda al menú desplegable, que representa un nuevo pedido de suministro sugerido. Se convierte en una nueva línea en la hoja de planificación cuando elige **Guardar cambios** en la pestaña **Procesar**.<br /><br /> Cualquier valor de filtro que esté definido en los campos **Filtro almacén** o **Filtro variante** en la ficha desplegable **Opciones** se aplicará a nuevos pedidos de suministros. **Nota**: Si los campos de filtro están vacíos o tienen más de un valor filtro, nuevos pedidos de suministros se crean utilizando los siguientes códigos: <ul><li>Si el campo de filtro está vacío, el nuevo suministro se crea sin un código de almacén o variante.</li><li>Si se define más de un valor de filtro, el nuevo suministro se crea utilizando el primer valor de filtro según la ordenación.</li></ul> Si desea otro código de variante o de almacén en el nuevo pedido de suministro, debe modificarlo manualmente en la nueva línea de planificación.|  
 |**Auto-Ajuste suministro**|Optimiza un nuevo suministro que ha creado en el gráfico para asegurarse de que crea un inventario de cero antes del suministro siguiente.|  
 |**Eliminar suministro**|Elimina el producto en la ficha desplegable **Escala de tiempo** y elimina la línea de planificación cuando elige **Guardar cambios** en la pestaña **Proceso**. El icono cambia a un disco que tiene una cruz de color rojo cuando se ha eliminado el suministro. **Nota**: Solo puede eliminar un suministro de tipo de mensajes de acción *Nuevo*. Después de elegir **Guardar cambios** en la pestaña **Proceso** debe eliminar manualmente la línea de planificación en cuestión en la hoja de planificación o demanda.|  
 |**Mostrar documento**|Abre el pedido, la línea de planificación o la previsión que el elemento representa.|  
 |**Alejar (Ctrl++)**|Aumenta la escala del eje X, para mostrar menos días. **Nota:** También puede hacerlo pulsando Ctrl + rueda de desplazamiento de raton.|  
 |**Acercar (Ctrl+-)**|Reduce la escala del eje X, para mostrar más días. **Nota:** También puede hacerlo pulsando Ctrl + rueda de desplazamiento de raton.|  
 |**Restablecer zoom (Ctrl+0)**|Revierte la escala del eje X a la que se utilizaba antes de alejar o acercar.|  

Además de las acciones de teclado se mencionadas antes, también puede utilizar las siguientes acciones de teclado en la ficha desplegable **Escala de tiempo**.  

 |Acción de teclado|Description|  
 |---------------------|---------------------------------------|  
 |Ctrl + rueda de mouse de desfase|Cambia la escala del eje X.|  
 |Seleccione un elemento y presione Shift+Flecha|Mueve el elemento en la dirección de la flecha.|  
 |Tabulador|Va al elemento siguiente.|  
 |Mayús+Tabulador|Va al elemento anterior.|  
 |Mientras mueve un elemento, presione Esc.|Cancela el movimiento. **Nota**: No funciona si ha soltado el botón del mouse.|

## <a name="see-also"></a>Consulte también  
[Planificación](production-planning.md)   
[Configuración de fabricación](production-configure-production-processes.md)  
[Fabricación](production-manage-manufacturing.md)    
[Grupos contables inventario](inventory-manage-inventory.md)  
[Compras](purchasing-manage-purchasing.md)  
[Detalles de diseño: planificación de aprovisionamiento](design-details-supply-planning.md)   
[Procedimientos recomendados de configuración: planificación de suministros](setup-best-practices-supply-planning.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

