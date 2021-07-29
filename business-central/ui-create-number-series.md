---
title: Crear series numéricas | Documentos de Microsoft
description: Obtenga información sobre cómo configurar series de números que asignan códigos de identificador único a las cuentas y los documentos en Business Central.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: numbers, numbering
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 3e2404a0ab9de8a761d5721da669004e393cf55c
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 07/08/2021
ms.locfileid: "6446002"
---
# <a name="create-number-series"></a>Crear numeración
Para cada empresa configurada, se necesitan asignar códigos de identificación exclusivos a elementos como cuentas de contabilidad, cuentas de proveedores y clientes, facturas y otros documentos. La numeración es importante no sólo para la identificación. Un sistema de numeración bien diseñado también permite facilitar la gestión y el análisis de la empresa, y puede reducir el número de errores que se producen en la introducción de datos.

> [!Important]
> De forma predeterminada, no se permiten saltos en las series numéricas porque, por ley, el historial exacto de las transacciones financieras debe estar disponible para auditoría y, por lo tanto, debe seguir una secuencia ininterrumpida sin números eliminados.<br /><br />
Si desea permitir huecos en ciertas series numéricas, primero consulte a su auditor o director de contabilidad para asegurarse de que cumple los requisitos legales de su país o región. Para obtener más información, vea [Espacios en serie numérica](ui-create-number-series.md#gaps-in-number-series).

> [!NOTE]  
>   Le recomendamos que use los mismos códigos de serie numérica que aparecen en la página **Lista nº serie** de la empresa de demostración CRONUS. Es posible que los códigos como *C-FAC+* no tengan un sentido inmediato, pero [!INCLUDE[prod_short](includes/prod_short.md)] tiene una serie de opciones de configuración predeterminadas que dependen de estos códigos de serie numérica.

Para crear un sistema numérico, establezca uno o varios códigos para cada tipo de datos maestros o documento. Por ejemplo, puede establecer un código para la numeración de clientes, otro para la numeración de facturas de venta y aún otro para la numeración de documentos en los diarios generales. Tras establecer un código, debe establecer al menos una línea de serie numérica. Ésta contiene información tal como el primer y último número de la serie y la fecha de inicio. Puede establecer más de una línea de serie numérica por código, con una fecha de inicio diferente para cada una. La serie se usará de manera consecutiva, a partir de la serie de cada fecha de inicio correspondiente.

> [!NOTE]
> La longitud máxima de un número en una serie de números es de 20 caracteres. Hay algunas situaciones en las que [!INCLUDE[prod_short](includes/prod_short.md)] agregará un número con un id. generado por el sistema. Por ejemplo, cuando se usan documentos como facturas para aplicar transacciones, como pagos, [!INCLUDE[prod_short](includes/prod_short.md)] genera identificadores para las transacciones aplicadas. El identificador se compone de un número de una serie de números y un id. asignado por el sistema de seis caracteres, como -12345. Si espera procesar más de 9999 documentos en diarios bancarios o de giros postales, o diarios de recibos de efectivo, configure series de números para esos tipos de documentos para que incluyan menos de 14 caracteres.

Las series numéricas normalmente se configuran para insertar automáticamente el siguiente número consecutivo en las nuevas fichas o documentos que cree. No obstante, también puede configurar una serie numérica que le permita introducir manualmente el nuevo número. Esta información se especifica con las casillas **Numeración manual**.

Si desea usar más de un código de serie numérica para un tipo de datos maestros, por ejemplo, usar una serie numérica diferente para categorías de productos, puede establecer relaciones de series numéricas.

## <a name="gaps-in-number-series"></a>Espacios en serie numérica
No todos los registros que crea en [!INCLUDE[prod_short](includes/prod_short.md)] son transacciones financieras que deben usar una numeración secuencial. Las fichas de cliente, las ofertas de venta y las actividades de almacén son ejemplos de registros a los que se les asigna un número de una serie numérica, pero no están sujetos a auditoría financiera o pueden eliminarse. Para estas series numéricas, puede seleccionar la casilla **Permitir espacios en números** en la página **Líneas nº serie**. Esta configuración también se puede cambiar después de crear la serie numérica. Para obtener más información, consulte [Para crear una nueva serie numérica](ui-create-number-series.md#to-create-a-new-number-series).

## <a name="behavior-of-the-no-field-on-documents-and-cards"></a>Comportamiento del campo de número en documentos y fichas
En documentos venta, compra y transferencia y en todas las fichas, el campo **N.º** se puede rellenar automáticamente a partir de una serie de números o manualmente, y puede configurarse para ser invisible.

El campo **Nº** se puede rellenar de tres maneras:

1. Si solo existe una serie numérica para el tipo de documento o ficha donde la casilla **Numeración predet.** está marcada y la casilla **Numeración manual** no está marcada, el campo se rellena automáticamente con el siguiente número de la serie, y el campo **N.º** no será visible.

    > [!NOTE]  
    > Si la serie numérica no funciona, por ejemplo, porque se ha quedado sin números, el campo **N.º** será visible y puede introducir un número de forma manual o resolver los problemas en la página **Nos. serie**.

2. Si hay varias series numéricas para el tipo de documento de compra o ficha, y la casilla **Numeración predet.** no está marcada para la serie numérica que hay asignada actualmente, el campo **N.º** está visible, y puede buscar en la página **Nos. serie** y seleccionar la serie numérica que desea utilizar. El número siguiente de la serie se inserta en el campo **N.º** .

3. Si no ha configurado una serie numérica para el tipo de documento o ficha, o si el campo **Numeración manual** de la serie numérica está seleccionado, el campo **N.º** está visible y deberá introducir cualquier número manualmente. Puede escribir un máximo de 20 caracteres, tanto números como letras.

Al abrir un nuevo documento o ficha para el que existe una serie numérica, la página **Configuración N.º serie** relevante se abre para que pueda configurar un número de serie para el tipo de documento o ficha antes de continuar con cualquier otra introducción de datos.

> [!NOTE]  
> Si necesita activar la numeración manual, por ejemplo, se han creado nuevas fichas de producto con un proceso de la migración de datos que ha ocultado el campo **Nº** de forma predeterminada, vaya a la página **Configuración del inventario** y elija el campo **Nº serie producto** para abrir y para definir las series numéricas relacionadas con **Numeración manual**.

## <a name="to-create-a-new-number-series"></a>Para crear una nueva serie numérica
1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Nº series** y luego elija el enlace relacionado.
2. Seleccione la acción **Nuevo**.
3. En la línea nueva, rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Seleccione la acción **Líneas**.
5. En la página **Líneas nº serie**, complete los campos para definir el uso real y el contenido de la serie numérica que creó en el paso 2.
6. Repita el paso 5 para los distintos usos de la serie numérica que necesite. El campo **Fecha inicial** define qué línea de serie numérica está activa.

## <a name="to-set-up-where-a-number-series-is-used"></a>Para configurar dónde se usa una serie numérica
El siguiente procedimiento muestra cómo configurar una serie numérica para el área de ventas. Los pasos son parecidos a los de otras áreas.
1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Ventas y cobros** y, a continuación, elija el vínculo relacionado.
2. En la página **Ventas y cobros**, en la ficha desplegable **Serie numérica**, seleccione la serie numérica que desee para cada ficha de ficha o documento.

El número seleccionado se utilizará para rellenar el campo **Nº** en la ficha o el documento en cuestión, según la configuración que ha establecido en la línea de serie numérica.

## <a name="to-create-relationships-between-number-series"></a>Para crear relaciones entre números de serie
Si ha configurado más de un código de número de serie para el mismo tipo de información básica o transacciones, puede crear relaciones entre los códigos. Esta característica puede servirle de ayuda para decidir entre un código u otro cuando utilice un número.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Nº series** y luego elija el enlace relacionado.
2. Seleccione la línea con las series numéricas que desea insertar para crear relaciones y, a continuación, elija **Relaciones**.
3. En el campo **Código serie**, escriba el código del número de serie con el que desee relacionar la serie seleccionada en el paso 2.
4. Agregue una línea para cada código que desee relacionar con el número de serie seleccionado.
5. Cierre la página.

En lo sucesivo, cuando configure algo que requiera un número, podrá utilizar las relaciones que haya creado para seleccionar uno de los números de serie relacionados.

## <a name="see-related-training-at-microsoft-learn"></a>Consulte Formación relacionada en [Microsoft Learn](/learn/modules/number-series-trail-codes-dynamics-365-business-central/index)

## <a name="see-also"></a>Consulte también
[Configurar [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]