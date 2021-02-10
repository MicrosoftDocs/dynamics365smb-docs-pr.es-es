---
title: Crear presupuestos contables | Documentos de Microsoft
description: Describe cómo crear presupuestos contables para prever diferentes actividades financieras y asignar dimensiones para fines de inteligencia empresarial.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: postpone
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 6018edd9d7d324c827c6c338ec700492b39bf56d
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "4747021"
---
# <a name="create-gl-budgets"></a>Crear presupuestos contables
Puede tener varios presupuestos para idénticos periodos de tiempo si crea presupuestos con nombres distintos. En primer lugar, debe configurar el nombre del presupuesto e introducir las cifras del presupuesto. El nombre del presupuesto se incluye en todos los movimientos de presupuesto que cree.  

Al crear un presupuesto, puede definir cuatro dimensiones para cada presupuesto. Estas dimensiones específicas de presupuesto se denominan dimensiones de presupuesto. Seleccione las dimensiones de presupuesto para cada uno de los presupuestos a partir de las dimensiones que ya ha configurado. Es posible utilizar las dimensiones de presupuesto para filtrar en un presupuesto y para agregar información de dimensiones a movimientos de presupuesto. Para obtener más información, consulte [Trabajar con dimensiones](finance-dimensions.md).

Los presupuestos desempeñan una función importante en la inteligencia empresarial, como los extractos financieros en función de los esquemas de cuentas que incluyen movimientos de presupuesto o al analizar los importes presupuestados frente a los reales en el plan de cuentas. Para obtener más información, consulte [Inteligencia empresarial](bi.md).

En contabilidad de costes, trabaja con los presupuestos de costes de forma similar. Para obtener más información, consulte [Crear presupuestos de costes](finance-create-cost-budgets.md).    

## <a name="to-create-a-new-gl-budget"></a>Para crear un nuevo presupuesto contable  
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), introduzca **Presupuestos generales** y luego elija el enlace relacionado.  
2. Elija la acción **Editar lista** y, a continuación, rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Seleccione la acción **Editar presupuesto**.
4. En la parte superior de la página **Presupuesto** rellene los campos según sea necesario para definir lo que se muestra.  

    Solo se mostrarán los movimientos que contengan el nombre del presupuesto que ha introducido en el campo **Nombre presupuesto**. Dado que el nombre de presupuesto acaba de crearse, no hay movimientos que coincidan con el filtro. Por tanto, la página está vacía.  
5. Para escribir una cantidad, seleccione la celda correspondiente de la matriz. Se abre la página **Movs. pptos. contabilidad**.  
6. Cree una nueva línea y rellene el campo **Importe**. Cierre la página **Movs. pptos. contabilidad**.  
7. Repita los pasos de 5 y 6 hasta que escriba todos los importes del presupuesto.  

> [!NOTE]  
>  En la ficha desplegable **Filtros** puede filtrar la información de presupuesto por las dimensiones de presupuesto que haya configurado con ese nombre de presupuesto.

## <a name="exporting-and-importing-gl-budgets-with-excel"></a>Exportar e importar presupuestos contables con Excel
Prácticamente en todas las demás páginas, puede exportar datos en páginas de presupuesto a Excel para su posterior procesamiento o análisis. Para obtener más información, consulte [Exportar los datos de negocio a Excel](about-export-data.md).

> [!NOTE]
> El plan de cuentas, en el que se basan los presupuestos contables, tiene líneas de tipo de cuenta Mayor que contienen el total de las líneas siguientes. Cuando se exporta un presupuesto contable, se exportan los datos de todas las líneas independientemente del tipo de cuenta. Sin embargo, solo se pueden volver a importar los datos de las líneas del tipo Registro. En consecuencia: <br /><br /> **Al importar un presupuesto contable, todos los valores que existían en las líneas de cabecera se eliminarán.** <br /><br /> Esto sirve para evitar cantidades totales erróneas después de importar datos que se han creado o editado en Excel.<br /><br /> **Escenario**: Usted sabe que el nuevo coste de los salarios presupuestados será de 1.200.000 DL. Desea permitir que el departamento de Salarios presupueste las tres líneas específicas (de tipo de cuenta Publicación) para Empleados a tiempo completo, Empleados a tiempo parcial y Ayuda temporal. Las tres líneas se agrupan bajo una línea de encabezado de Salarios.<br /><br />Introduzca 1.200.000 en la línea Mayor, exporte el presupuesto a Excel y luego envíelo al departamento de Salarios y dígales que distribuyan los 1.200.000 DL.<br /><br /> El departamento de Salarios distribuye el importe en las tres cuentas contables. Cuando vuelve a importar al presupuesto contable, las tres cuentas se completan con los nuevos datos de Excel, que suman 1.200.000 DL y la línea Mayor está en blanco.

## <a name="see-related-training-at-microsoft-learn"></a>Consulte Formación relacionada en [Microsoft Learn](/learn/modules/budgets-exchange-rates-dynamics-365-business-central/index)

## <a name="see-also"></a>Consulte también
[Exportar los datos de negocio a Excel](about-export-data.md)  
[Finanzas](finance.md)  
[Inteligencia empresarial](bi.md)  
[Configurar las finanzas](finance-setup-finance.md)  
[Libro mayor y plan de cuentas](finance-general-ledger.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
