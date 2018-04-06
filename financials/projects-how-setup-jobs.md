---
title: Configurar precios de proyectos y grupos contables de proyectos | Documentos de Microsoft
description: "Describe cómo configurar la configuración general de los proyectos y configurar los precios de los productos de proyecto, los recursos, las cuentas contables y los grupos contables de proyectos."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 2c57b2bd4b4c99373d4ce16905fbf626e549bc1f
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-jobs"></a>Configurar proyectos
En la ventana **Configuración de proyectos**, debe especificar cómo desea utilizar determinadas características del proyecto.

En las fichas de proyecto individuales, debe configurar los precios de los productos del proyecto, los recursos del proyecto y las cuentas de proyecto, y debe configurar los grupos contables de proyectos.

## <a name="to-set-general-information-for-jobs"></a>Para configurar la información general de los proyectos
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Configuración de proyectos** y, a continuación, seleccione el vínculo relacionado.
2. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   La casilla **Aplicar vínculo uso** es bastante compleja y, por tanto, se explica en la sección siguiente.

## <a name="to-set-up-job-usage-tracking"></a>Para configurar el seguimiento de uso de proyecto
Cuando se está ejecutando un proyecto, es posible que desee saber cómo va la utilización en comparación con el plan. A hacerlo fácilmente, cree un vínculo entre las líneas de planificación de proyecto y la utilización real. Esto le permite seguir los costes y ver fácilmente cuánto trabajo queda por realizar. De forma predeterminada, el tipo de línea de planificación de proyecto es **Presupuesto**, pero utilizar el tipo de línea **Presupuesto y facturable** tiene efectos similares.

Si selecciona la casilla **Aplicar vínculo uso**, puede revisar la información de la línea de planificación de proyecto. Puede definir a la cantidad del recurso, el producto o la cuenta de contabilidad general, y después indicar qué cantidad desea transferir al diario de proyectos. El campo **Cantidad pendiente** de la línea de planificación de proyecto puede indicar qué queda por transferir y registrar en el diario de proyectos.

Cuando se selecciona la casilla **Aplicar vínculo uso**, y el tipo de la línea de planificación de proyecto es **Facturable**, el departamento financiero crea una línea de planificación de proyecto del tipo **Presupuesto** después de registrar la línea del diario.

> [!NOTE]  
>   Si la casilla **Aplicar vínculo uso** está seleccionada en la ficha de proyecto y el campo **Tipo de línea** está en blanco, se crearán las nuevas líneas de planificación de proyecto del tipo de línea **Presupuesto** al registrar las líneas de diario de proyectos. Si la casilla **Aplicar vínculo uso** no está seleccionada en la ficha de proyecto y el campo **Tipo de línea** está en blanco, no se crearán líneas de planificación de proyecto al registrar las líneas de diario de proyectos. Para obtener más información, consulte [Registro del uso para proyectos](projects-how-record-job-usage.md).

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Configuración de proyectos** y, a continuación, seleccione el vínculo relacionado.
2. Seleccione o anule la selección de la casilla **Aplicar vínculo uso**.

> [!NOTE]  
>   Puede realizar una configuración diferente de la casilla **Aplicar vínculo uso** en las fichas de proyecto individuales. En ese caso, la configuración de dicho proyecto ignorará el valor predeterminado general descrito anteriormente.

## <a name="to-set-up-prices-for-job-resources"></a>Para configurar los precios de los recursos de proyecto
Puede configurar precios concretos para los recursos de un proyecto. Para ello, debe usar la ventana **Precios recursos proyecto**.

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Proyectos** y, a continuación, seleccione el vínculo relacionado.  
2. Seleccione el proyecto correspondiente y, a continuación, elija la acción **Recurso**.
3. En la ventana **Precios recursos proyecto**, rellene los campos según sea necesario.

La información opcional de los campos **N.º tarea de proyecto**, **Tipo trabajo**, **Cód. divisa**, **% Descuento línea** y **Factor coste unitario** se usará en las líneas de planificación de proyecto y los diarios de uso cuando se introduce este recurso y se agrega al proyecto.  

Se usará el valor del campo **Precio de venta** correspondiente al recurso en las líneas de planificación de proyecto y los diarios de proyectos cuando se introduzca este recurso, un recurso asignado al grupo de recursos o cualquier recurso.  

> [!NOTE]  
>   Este precio anulará siempre los precios establecidos en la ventana **Precio de recurso/Precios de grupo de recursos** existente.

## <a name="to-set-up-prices-for-job-items"></a>Para configurar los precios de los productos de proyecto
Puede configurar precios concretos para los productos de un proyecto. Para ello, debe usar la ventana **Precios recursos proyecto**.

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Proyectos** y, a continuación, seleccione el vínculo relacionado.  
2. Seleccione el proyecto correspondiente y, a continuación, elija la acción **Producto**.
3. En la ventana **Precios productos proyecto**, rellene los campos según sea necesario.

La información opcional de los campos **N.º tarea de proyecto**, **Cód. divisa** y **% Descuento línea** se usarán en las líneas de planificación del proyecto y en los diarios de proyectos cuando se introduzca este producto o se agregue al proyecto.  

El valor del campo **Precio de venta** correspondiente al artículo se usará en las líneas de planificación del proyecto y en los diarios de proyectos cuando se introduzca este producto.  

> [!NOTE]  
>   Este precio siempre anulará el precio regular del cliente (mecanismo de “mejor precio”) de los productos. Si desea usar los mecanismos de precio regular del cliente, no debe crear ningún precio de producto para el proyecto.

## <a name="to-set-up-prices-for-job-general-ledger-accounts"></a>Para configurar precios de cuentas del proyecto
Puede configurar precios específicos para gastos contables de un proyecto. Para ello, debe usar la ventana **Precios cuentas proyecto**.

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Proyectos** y, a continuación, seleccione el vínculo relacionado.  
2. Seleccione el proyecto correspondiente y, a continuación, elija la acción **Cuenta**.  
3. En la ventana **Precios cuentas proyecto**, rellene los campos según sea necesario.

La información opcional de los campos **N.º tarea proyecto**, **Cód. divisa**, **% Descuento línea**, **Factor coste unitario** y **Coste unitario** se usará en las líneas de planificación de proyecto y los diarios de proyectos cuando se introduce esta cuenta y se agrega al proyecto.  

El valor del campo **Precio de venta** del gasto de proyecto de contabilidad se usará en las líneas de planificación de proyecto y en los diarios de proyectos cuando se introduzca esta cuenta.

## <a name="to-set-up-job-posting-groups"></a>Para configurar grupos contables del proyecto
Un aspecto de los proyectos de planificación es decidir qué cuentas de registro se deben utilizar para la valoración de proyectos. Para poder registrar proyectos, debe configurar cuentas de registro para cada grupo contable del proyecto. Un grupo contable representa un vínculo entre el proyecto y cómo debe ser tratado en la contabilidad general. Al crear un proyecto, se especifica un grupo contable y, de forma predeterminada, todas las tareas que crea para el proyecto están asociadas con ese grupo contable. Sin embargo, al crear las tareas, puede sustituir el predeterminado y seleccionar a un grupo contable que sea más adecuado.  

> [!NOTE]  
>   Se deben configurar las cuentas necesarias en el plan de cuentas antes de configurar los grupos contables. Para obtener más información, vea [Configuración o cambio del plan de cuentas](finance-setup-chart-accounts.md).  

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Grupos contables proyectos** y, a continuación, seleccione el vínculo relacionado.  
2. Elija la acción **Nuevo** y, a continuación, rellene los campos de cuenta tal como se describe en la tabla siguiente.  

| Campo Cuenta | Descripción |
| --- | --- |
| **Código** |Un código para el grupo contable. Puede escribir hasta 10 caracteres, incluso espacios. |
| **Cuenta costes WIP** |Es la cuenta de trabajo en curso para el coste calculado de WIP del proyecto, y es una cuenta de activos de capital de balance. |
| **Cta. costes acumulados trabajo en curso** |Es una cuenta del método de valor de coste o valor de ventas para el cálculo del trabajo en curso, y es una cuenta de pasivo de gastos acumulados de balance. En ella se realizarán registros cuando el ajuste del trabajo en curso exija el aumento de los costes de utilización registrados en el asiento de regularización. |
| **Cta. aplicada costes proyecto** |Es una cuenta de contrapartida de la cuenta de costes de trabajo en curso, que es complementaria de una cuenta de gastos negativa. |
| **Cta. de costes liq. productos** |Es una cuenta de contrapartida de la cuenta de costes de trabajo en curso, que es complementaria de una cuenta de gastos negativa. |
| **Cta. de costes liq. recursos** |Es una cuenta de contrapartida de la cuenta de costes de trabajo en curso, que es complementaria de una cuenta de gastos negativa. |
| **Cta. de costes liq.** |Es una cuenta de contrapartida de la cuenta de costes de trabajo en curso, que es complementaria de una cuenta de gastos negativa. |
| **Cta. ajuste costes proyecto** |Es la cuenta de contrapartida de la cuenta de costes de trabajo en curso, que es una cuenta de gastos. |
| **Cta. gastos C/G (presupuesto)** |La cuenta de ventas que se utilizará con este grupo contable para los gastos de contabilidad de las tareas del proyecto. Si se deja en blanco, se usa la cuenta introducida en la línea de planificación del proyecto. |
| **Cta. ventas acumuladas WIP** |Es la cuenta de trabajo en curso para el valor de ventas calculado de este trabajo, que es una cuenta de activos de capital de balance. En ella se realizan registros cuando el ajuste del trabajo en curso exige un aumento de los ingresos reconocidos. |
| **Cta. ventas facturadas WIP** |Es la cuenta del valor de las ventas facturadas del trabajo en curso que no se puede reconocer. Es una cuenta de ingresos anticipados de balance. |
| **Cuenta liq. ventas proy.** |Es la cuenta de contrapartida de la cuenta de ventas facturadas del trabajo en curso, que es una cuenta complementaria de ingresos. |
| **Cuenta ajuste ventas proy.** |Es la cuenta de contrapartida de la cuenta de ventas del proyecto del trabajo en curso, que es una cuenta de ingresos. |
| **Cuenta costes reconocidos** |Es la cuenta de gastos que contiene los costes reconocidos del proyecto. Normalmente, es una cuenta de cargo. |
| **Cuenta ventas reconocidas** |Es la cuenta de ingresos que contiene los ingresos reconocidos del proyecto. Normalmente, es una cuenta de ingresos. |

## <a name="see-also"></a>Consulte también
[Configuración de la administración de proyectos](projects-setup-projects.md)  
[Administrar proyectos](projects-manage-projects.md)  
[Finanzas](finance.md)  
[Compras](purchasing-manage-purchasing.md)         
[Ccial](sales-manage-sales.md)      
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

