---
title: "Crear series numéricas | Documentos de Microsoft"
description: "Obtenga información sobre cómo configurar series de números que asignan códigos de identificador único a las cuentas y los documentos en Dynamics 365 for Financials."
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: numbers, numbering
ms.date: 06/02/2017
ms.author: solsen
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 7cc119c5879400adf63e468259a2c3a275b71cca
ms.contentlocale: es-es
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-create-number-series"></a>Crear serie numérica
Para cada empresa configurada, se necesitan asignar códigos de identificación exclusivos a elementos como cuentas de contabilidad, cuentas de proveedores y clientes, facturas y otros documentos. La numeración es importante no sólo para la identificación. Un sistema de numeración bien diseñado también permite facilitar la gestión y el análisis de la empresa, y puede reducir el número de errores que se producen en la introducción de datos.

> [!NOTE]  
>   Le recomendamos que use los mismos códigos de serie numérica que aparecen en la ventana **Lista nº serie** de la empresa de demostración CRONUS. Es posible que los códigos como *C-FAC+* no tengan un sentido inmediato, pero [!INCLUDE[d365fin](includes/d365fin_md.md)] tiene una serie de opciones de configuración predeterminadas que dependen de estos códigos de serie numérica.

Para crear un sistema numérico, establezca uno o varios códigos para cada tipo de datos maestros o documento. Por ejemplo, puede establecer un código para la numeración de clientes, otro para la numeración de facturas de venta y aún otro para la numeración de documentos en los diarios generales. Tras establecer un código, debe establecer al menos una línea de serie numérica. Ésta contiene información tal como el primer y último número de la serie y la fecha de inicio. Puede establecer más de una línea de serie numérica por código, con una fecha de inicio diferente para cada una. La serie se usará de manera consecutiva, a partir de la serie de cada fecha de inicio correspondiente.

Las series numéricas normalmente se configuran para insertar automáticamente el siguiente número consecutivo en las nuevas fichas o documentos que cree. No obstante, también puede configurar una serie numérica que le permita introducir manualmente el nuevo número. Esta información se especifica con **Numeración manual** .

Si desea usar más de un código de serie numérica para un tipo de datos maestros, por ejemplo, usar una serie numérica diferente para categorías de productos, puede establecer relaciones de series numéricas.

## <a name="to-create-a-new-number-series"></a>Para crear una nueva serie numérica
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Nos. serie** y, a continuación, seleccione el vínculo relacionado.
2. Seleccione la acción **Nuevo**.
3. En la línea nueva, rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

**SUGERENCIA**: Para permitir la entrada manual de un número en las nuevas fichas o documentos, desmarque la casilla **Numeración predet.** y seleccione **Numeración manual** .

Ahora, al crear una nueva ficha o documento que se haya configurado para utilizar la serie numérica en cuestión, podrá rellenar manualmente el campo **Nº** con cualquier valor.  

## <a name="to-set-up-where-a-number-series-is-used"></a>Para configurar dónde se usa una serie numérica
El siguiente procedimiento muestra cómo configurar una serie numérica para el área de ventas. Los pasos son parecidos a los de otras áreas.
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Selección informes ventas** y, a continuación, seleccione el vínculo relacionado.
2. En la ventana **Ventas y cobros**, en la ficha desplegable **Serie numérica**, seleccione la serie numérica que desee para cada ficha de ficha o documento.

El número seleccionado se utilizará para rellenar el campo **Nº** en la ficha o el documento en cuestión, según la configuración que ha establecido en la línea de serie numérica.

## <a name="to-create-relationships-between-number-series"></a>Para crear relaciones entre números de serie
Si ha configurado más de un código de número de serie para el mismo tipo de información básica o transacciones, puede crear relaciones entre los códigos. Esta característica puede servirle de ayuda para decidir entre un código u otro cuando utilice un número.

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Nos. serie** y, a continuación, seleccione el vínculo relacionado.
2. Seleccione la línea con las series numéricas que desea insertar para crear relaciones y, a continuación, elija **Relaciones**.
3. En el campo **Código serie**, escriba el código del número de serie con el que desee relacionar la serie seleccionada en el paso 2.
4. Agregue una línea para cada código que desee relacionar con el número de serie seleccionado.
5. Cierre la ventana.

En lo sucesivo, cuando configure algo que requiera un número, podrá utilizar las relaciones que haya creado para seleccionar uno de los números de serie relacionados.

## <a name="see-also"></a>Consulte también
[Configurar [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

