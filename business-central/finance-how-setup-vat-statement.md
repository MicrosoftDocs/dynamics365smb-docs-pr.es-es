---
title: Configurar una nueva declaración de IVA
description: Este tema le explica cómo configurar una plantilla de declaración de IVA y nombres de declaración de IVA para cumplir los cambiantes requisitos de la autoridad fiscal.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'VAT, posting, tax, value-added tax'
ms.search.form: '317, 318, 320, 474'
ms.date: 06/16/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Configurar tipos de declaración de IVA y nombres de declaración de IVA

Las autoridades fiscales pueden modificar, y lo hacen, sus requisitos para registrar el IVA. Los tipos de declaración del IVA y los nombres de declaración del IVA pueden ayudarle a prepararse para los próximos cambios y hacer una transición sin problemas a los nuevos requisitos. Puede usar plantillas de declaración de IVA para configurar diferentes informes al elegir imprimir la declaración. Cada plantilla de declaración de IVA puede tener varios nombres de declaración de IVA que a su vez definen los cálculos, y puede crear un nuevo nombre de declaración de IVA cuando cambien los requisitos. Por ejemplo, un nombre podría calcular el IVA para este año basándose en los requisitos actuales y otro podría calcular el IVA basándose en los requisitos para el próximo año. Los nombres también son una forma de mantener un historial de los formatos de las declaraciones del IVA, por ejemplo, para que pueda consultar cómo calculó el IVA en años anteriores.

## Para definir una declaración de IVA

Las declaraciones de IVA le permiten calcular el importe de liquidación de IVA de un determinado periodo, por ejemplo, un trimestre.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Declaraciones de IVA** y luego elija el enlace relacionado.  
2. Elija el campo **Nombre** y después **Nuevo** en la página **Nombres declar. IVA**.
3. Rellene los campos requeridos. Por lo general, desea tener una configuración para cada combinación de grupo de registro de IVA de negocio/grupo de registro IVA de producto. Para los números de fila tiene sentido usar números o códigos equivalentes como en su declaración de IVA oficial [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

> [!Tip]
> Puede filtrar la información que incluirá la declaración, dependiendo de lo que elija en el campo **Tipo**. **Cuentas a totalizar** resulta útil cuando desea el IVA de una cuenta específica.
**Total mov. IVA** obtiene el IVA de las cuentas asignadas a las selecciones en los campos **Tipo IVA**, **Grupo reg. IVA negocio** o **Grupo reg. IVA producto**. **Filas a totalizar** permite introducir un valor o criterios de filtro rápido en el campo **Filas a totalizar**. Para obtener más información, consulte [Buscar, filtrar y ordenar datos](ui-enter-criteria-filters.md). **Descripción** se utiliza con frecuencia para agregar una nota a la declaración. Por ejemplo, puede utilizarlo como cabecera cuando haya utilizado el total de filas.

## Para obtener una vista previa de la declaración de IVA

Después de definir una declaración de IVA, puede obtener una vista previa de ella para asegurarse de que satisface sus necesidades.
> [!Tip]
> Es una práctica recomendad tener una sección en la declaración de IVA utilizando **Tipo** **Total mov. IVA** y otra sección a continuación usando **Tipo** **Cuentas a totalizar** para conciliar las cantidades basadas en la tabla **Movimiento de IVA** en comparación con el importe en **Cuentas**. También puede usar el informe **C/G: Conciliación de IVA** para este propósito.

1. Seleccione **Vista previa**.
2. Escriba un filtro de fecha para limitar la declaración a un periodo específico. Para obtener más información sobre cómo personalizar la página para mostrar el filtro de fecha, consulte [Buscar, filtrar y ordenar datos](ui-enter-criteria-filters.md).
3. Puede seleccionar diversas opciones para especificar el tipo de movimientos de IVA para incluir en la declaración.
4. En las líneas cuyo campo **Tipo** contenga **Total mov. IVA**, podrá ver una lista de los movimientos de IVA al seleccionar el importe del campo **Importe columna**.
5. Puede usar la personalización para mostrar más campos en las líneas. Por ejemplo, el importe base no realizado y el importe de IVA no realizado, si está utilizando el IVA no realizado.

## Consulte también .

[Configurar impuesto sobre valor añadido](finance-setup-vat.md)  
[Configuración del impuesto sobre el valor añadido no realizado](finance-setup-unrealized-vat.md)  
[Crear informes de IVA para la autoridad fiscal](finance-how-report-vat.md)  
[Trabajar con el IVA por ventas y compras](finance-work-with-vat.md)  
[Funcionalidad local en Business Central](about-localization.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
