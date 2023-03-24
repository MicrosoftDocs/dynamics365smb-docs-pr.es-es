---
title: Combinar registros duplicados de clientes o proveedores
description: Describe cómo consolidar información sobre clientes o proveedores cuando tiene entradas duplicadas sobre algunos de ellos.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: client
ms.date: 04/01/2021
ms.author: edupont
---
# Combinar registros duplicados

A medida que diferentes usuarios crean nuevas fichas de cliente, proveedor o contacto a lo largo del tiempo, o que los nuevos registros se crean automáticamente durante la migración, un cliente, proveedor o contacto puede estar representado en el sistema con más de un registro. En este caso, puede utilizar la página **Combinar duplicados** de la ficha del registro que desea conservar. La página le ofrece una visión general de los valores de campo duplicado y le ofrece funciones para seleccionar los valores que desea conservar o descartar al combinar dos registros en uno.

> [!NOTE]
> Solo los usuarios con el conjunto de permisos COMBINAR DUPLICADOS pueden utilizar esta funcionalidad.

> [!TIP]
> La página **Combinar duplicados** muestra todos los campos en los que los valores son diferentes para los dos registros que se comparan. Por lo tanto, un duplicado se indica por la página que muestra muy pocos campos. Mientras que, si la página muestra muchos campos, el registro sospechoso probablemente no sea un duplicado.

El procedimiento siguiente se basa en una ficha de cliente. Los pasos son parecidos para una ficha de proveedor y de contacto.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Clientes** y luego elija el enlace relacionado.
2. Seleccione el cliente del que sabe o sospecha que existe un registro duplicado y, a continuación, seleccione la acción **Editar**.
3. En la página **Ficha de cliente**, seleccione la acción **Combinar con**.
4. En la página **Combinar duplicado**, en el campo **Combinar con**, seleccione el cliente que cree que es un duplicado del que ha abierto, indicado en el campo **Actual**.

    La ficha desplegable **Campos** enumera los campos en los que los valores son diferentes para los dos clientes. Esto significa que si el cliente seleccionado es realmente un duplicado, solo se deben enumerar unos pocos campos, como errores de escritura y otros errores de entrada de datos.

    La ficha desplegable **Tablas relacionadas** enumera las tablas en las que hay campos con una relación en ambos clientes. Los campos **Recuento actual** y **Recuento duplicado** muestran el número de campos en las tablas relacionadas en las que se usa el valor **Nº** del cliente actual y del cliente duplicado. En la página **Combinar duplicado**, esta sección es solo informativa; sin embargo, si existen conflictos de combinación, los resolverá en la página **Combinar conflictos duplicados**. Consulte los pasos 8 a 12.   

5. Para cada campo en el que desee utilizar un valor distinto al actual, seleccione la casilla de selección **Reemplazar**. El valor del campo **Valor alternativo** se transferirá al registro actual cuando finalice el proceso.
6. Cuando haya terminado de seleccionar los valores que desea mantener o reemplazar, seleccione la acción **Combinar**.

    El sistema verifica si la combinación de valores del cliente duplicado en el cliente actual provoca conflictos. Un conflicto existe si un valor en al menos un campo de clave principal es el mismo para ambos clientes, mientras que el valor en el campo **Nº** es diferente para los dos clientes.

7. Si no se encuentran conflictos, seleccione el pulsador **Sí** en el cuadro de mensaje de confirmación.

    Se cambia el nombre del cliente duplicado de modo que todo uso de su valor **Nº** en todos los campos con relaciones con la tabla de cliente se reemplazará por el valor de **Nº** del cliente actual.
8. Si existen conflictos, seleccione la acción **Resolver (xx) conflictos antes de la combinación** en la ficha desplegable **Conflictos**, que aparecerá si existen conflictos.
9. En la página **Combinar conflictos duplicados**, seleccione la línea de una tabla relacionada con un conflicto y, a continuación, la acción **Ver detalles**.

    La página **Combinar duplicado** ahora muestra los campos en la tabla seleccionada que provocan un conflicto de combinación entre los dos registros de cliente. Observe tanto en los valores resumidos de los campos **Actual** y **Conflictos con** como en las líneas que al menos un campo de clave principal es el mismo para ambos clientes y el valor del campo **Nº** es diferente para los dos clientes.   
10. Si no desea conservar el registro de cliente duplicado, seleccione la acción **Quitar duplicado** y, a continuación, el botón **Cerrar**.

    Los valores de campo idénticos, distintos del valor del campo **Nº** se quitan del registro duplicado y se insertan en el registro actual.
11. Si desea conservar el registro de cliente duplicado después de la combinación, seleccione **Cambiar el nombre del duplicado**.
12. En las líneas, no para el campo **Nº**, donde el campo tiene el mismo valor en ambos registros, modifique el valor en el campo **Valor alternativo** y, a continuación, seleccione el botón **Cerrar**.

    El valor del campo en conflicto se actualiza en el registro duplicado para que pueda combinarse con el registro actual. El registro duplicado sigue existiendo después de la combinación.
13. Repita los pasos del 8 al 12 hasta que se resuelvan todos los conflictos. Desaparece la ficha desplegable **Conflictos**.
14. En la página **Combinar duplicado**, seleccione de nuevo la acción **Combinar** y, a continuación, seleccione el botón **Sí** en el cuadro de mensaje de confirmación.

> [!NOTE]
> Para los contactos, puede usar la funcionalidad para encontrar contactos duplicados antes de usar la página **Combinar duplicados**. Para obtener más información, vea [Búsqueda de contactos duplicados](marketing-setup-contacts.md#searching-for-duplicate-contacts).

## Consultar la [formación de Microsoft](/training/modules/trade-master-data-dynamics-365-business-central/) relacionada

## Consulte también .

[Ccial](sales-manage-sales.md)  
[Configuración de contactos](marketing-setup-contacts.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
