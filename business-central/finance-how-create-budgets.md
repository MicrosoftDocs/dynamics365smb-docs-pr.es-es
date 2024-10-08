---
title: Creación de presupuestos contables
description: Describe cómo crear presupuestos contables para prever diferentes actividades financieras y asignar dimensiones para fines de inteligencia empresarial.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: postpone
ms.search.form: '113, 120, 121, 154, 350, 422, 7132, 7133, 7138, 7139, 9203, 9219, 9239, 9373, 9374'
ms.date: 06/10/2024
ms.service: dynamics-365-business-central
---
# <a name="create-gl-budgets"></a>Crear presupuestos contables

Puede tener varios presupuestos para idénticos periodos de tiempo si crea presupuestos con nombres distintos. En primer lugar, debe configurar el nombre del presupuesto e introducir las cifras del presupuesto. El nombre del presupuesto se incluye en todos los movimientos de presupuesto que cree.  

Al crear un presupuesto, puede asignarle dimensiones específicas, denominadas dimensiones presupuestarias. Puede utilizar las dimensiones del presupuesto para establecer filtros en un presupuesto y para añadir información de dimensión a las entradas del presupuesto. Obtenga más información en [Trabajar con dimensiones](finance-dimensions.md).

Los presupuestos juegan un papel importante en la inteligencia empresarial. Ejemplos son los extractos financieros en función de los informes financieros que incluyen movimientos de presupuesto o al analizar los importes presupuestados frente a los reales en el plan de cuentas. Obtenga más información en [Inteligencia de negocios](bi.md).

En contabilidad de costes, trabaja con los presupuestos de costes de forma similar. Más información en [Crear presupuestos de G/L](finance-create-cost-budgets.md).  

## <a name="to-create-a-new-gl-budget"></a>Para crear un nuevo presupuesto contable

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Presupuestos contables** y luego elija el enlace relacionado.  
2. Elija la acción **Editar lista** y, a continuación, rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Seleccione la acción **Editar presupuesto**.
4. En la parte superior de la página **Presupuesto** rellene los campos según sea necesario para definir lo que se muestra.  

   La página solo muestra las entradas que contienen el nombre del presupuesto introducido en el campo **Nombre presupuesto**. Dado que acaba de crear el nombre del presupuesto, no hay movimientos que coincidan con el filtro. Por tanto, la página está vacía.  
5. Para escribir una cantidad, seleccione la celda correspondiente de la matriz. Se abre la página **Movs. pptos. contabilidad**.  
6. Cree una nueva línea y rellene el campo **Importe**. Cierre la página **Movs. pptos. contabilidad**.  
7. Repita los pasos 5 y 6 para todos los importes del presupuesto.  

> [!NOTE]  
> En la ficha desplegable **Filtros** puede filtrar la información de presupuesto por las dimensiones de presupuesto que haya configurado con ese nombre de presupuesto.

## <a name="exporting-and-importing-gl-budgets-with-excel"></a>Exportar e importar presupuestos contables con Excel

Prácticamente en todas las demás páginas, puede exportar datos en páginas de presupuesto a Microsoft Excel para su posterior procesamiento o análisis. Más información en [Exportar los datos de negocio a Excel](about-export-data.md).

> [!NOTE]
> El plan de cuentas, en el que se basan los presupuestos del libro mayor, tiene líneas del tipo de cuenta Encabezado. Estas líneas contienen el total de las líneas debajo de ellas. Cuando se exporta un presupuesto contable, se exportan los datos de todas las líneas independientemente del tipo de cuenta. Sin embargo, sólo puede importar datos sobre líneas del tipo de cuenta Contabilización.

De igual forma, al importar un presupuesto contable, todos los valores que existían en las líneas de cabecera se eliminan. Se eliminan para evitar totales incorrectos después de importar datos creados o editados en Excel.

### <a name="scenario"></a>Escenario

Usted sabe que el nuevo coste de los salarios presupuestados será en moneda local (LCY) 1.200.000. Desea permitir que el departamento de Salarios presupueste las tres líneas específicas (de tipo de cuenta Publicación) para empleados a tiempo completo, empleados a tiempo parcial y ayuda temporal. Las tres líneas se agrupan bajo una línea de encabezado de Salarios.

Introduzca 1.200.000 en la línea Mayor, exporte el presupuesto a Excel y luego envíelo al departamento de Salarios y dígales que distribuyan los 1.200.000 DL.

El departamento de Salarios distribuye el importe en las tres cuentas contables. Cuando vuelve a importar al presupuesto contable, las tres cuentas se completan con los nuevos datos de Excel, que suman 1.200.000 DL y la línea Mayor está en blanco.

## <a name="see-also"></a>Consulte también .

[Exportar datos empresariales a Excel](about-export-data.md)  
[Finanzas](finance.md)  
[Inteligencia empresarial](bi.md)  
[Configurar las finanzas](finance-setup-finance.md)  
[Libro mayor y plan de cuentas](finance-general-ledger.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
