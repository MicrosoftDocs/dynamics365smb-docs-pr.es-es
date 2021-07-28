---
title: Configurar proyectos, precios y grupos contables de proyectos
description: Describe cómo configurar la configuración general de los proyectos y configurar los precios de los productos de proyecto, los recursos, las cuentas contables y los grupos contables de proyectos.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.workload: na
ms.search.keywords: project management
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: cff8ae1b376079aa1b9162cade59e88da985e263
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 07/08/2021
ms.locfileid: "6436153"
---
# <a name="set-up-jobs-prices-and-job-posting-groups"></a>Configurar proyectos, precios y grupos contables de proyectos

Como director de proyectos, puede configurar proyectos que definan cada uno de los proyectos que administra en [!INCLUDE[prod_short](includes/prod_short.md)]. En la página **Configuración de proyectos**, debe especificar cómo desea utilizar determinadas características del proyecto.

Para cada proyecto, especifique fichas de proyecto individuales con información sobre los precios de los productos del proyecto, los recursos del proyecto y las cuentas de proyecto, y debe configurar los grupos contables de proyectos.

## <a name="to-set-general-information-for-jobs"></a>Para configurar la información general de los proyectos
1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de proyectos** y luego elija el enlace relacionado.
2. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]
> El campo **Aplicar enlace de uso de forma predeterminada** indica si las entradas del libro mayor de proyectos están vinculadas a las líneas de planificación de proyecto de forma predeterminada. Elija el campo si desea aplicar esta configuración a todos los nuevos proyectos que cree. Puede habilitar o deshabilitar el seguimiento del uso del proyecto para un proyecto específico cambiando el valor del campo **Aplicar enlace de uso** en la tarjeta de trabajo individual. Las consecuencias se explican en la siguiente sección.

### <a name="to-set-up-job-usage-tracking"></a>Para configurar el seguimiento de uso de proyecto

Cuando está trbajando en un proyecto, es posible que desee saber cómo va el seguimiento en comparación con el plan. A hacerlo fácilmente, cree un vínculo entre las líneas de planificación de proyecto y la utilización real. Esto le permite seguir los costes y ver fácilmente cuánto trabajo queda por realizar. De forma predeterminada, el tipo de línea de planificación de proyecto es *Presupuesto*, pero utilizar el tipo de línea **Presupuesto y facturable** tiene efectos similares.

Después de haber establecido el seguimiento de uso escogiendo **Aplicar vínculo de uso**, puede revisar la información de la línea de planificación de proyecto. Puede definir a la cantidad del recurso, el producto o la cuenta de contabilidad general, y después indicar qué cantidad desea transferir al diario de proyectos. El campo **Cantidad pendiente** de la línea de planificación de proyecto puede indicar qué queda por transferir y registrar en el diario de proyectos.

>[!NOTE]
> Si se elige **Aplicar vínculo de uso** en el proyecto individual y el campo **Tipo de línea** de la línea de diario de proyectos o la línea de pedido es *Facturable*, se crearán las nuevas líneas de planificación de proyecto del tipo de línea *Presupuesto* al registrar el diario de proyectos o el documento de compra.  
> Para más información, vea [Registro de uso para proyectos](projects-how-record-job-usage.md) y [Administrar suministros de proyectos](projects-how-manage-project-supplies.md)

> [!IMPORTANT]
> Si el campo **Tipo de línea** de la línea del diario de proyecto o la línea de compra están en blanco, entonces no se crean líneas de planificación de proyecto cuando se registra el diario de trabajo o el documento de compra.

<!--
>[!Important]
If job usage tracking is enabled on the individual job and the **Line Type** field on the job journal or purchase line line is blank, then new job planning lines of line type *Budget* are created when you post job journal or purchase document.
If job usage tracking is not enabled and the **Line Type** field on the job journal line or purchase line is blank, then no job planning lines are created when you post job journal or purchase document.
-->


## <a name="to-set-up-prices-for-resources-items-and-general-ledger-accounts-for-jobs"></a>Para establecer los precios de recursos, productos y cuentas de contabilidad para trabajos
> [!NOTE]
> En el segundo lanzamiento de versiones de 2020, lanzamos nuevos procesos optimizados para configurar y administrar precios y descuentos. Si es un cliente nuevo, está usando la nueva experiencia. Si es un cliente existente, si está utilizando o no la nueva experiencia depende de si su administrador ha habilitado la actualización de funciones **Nueva experiencia de precios de venta** en **Administración de características**. Para más información, consulte [Habilitación de las próximas funciones antes de tiempo](/dynamics365/business-central/dev-itpro/administration/feature-management).

Puede establecer los precios de los productos, recursos, productos y cuentas de contabilidad relacionadas con un trabajo. 

#### <a name="current-experience"></a>[Experiencia actual](#tab/current-experience)
1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Proyectos** y luego elija el enlace relacionado.  
2. Seleccione la tarea y, a continuación, elija la acción **Recurso**, **Elemento** o **Cuenta P/G**.
3. En las páginas **Precios de los recursos laborales**, **Precios de artículos de trabajo** o **Precios de la cuenta P/G del trabajo**, rellene los campos según sea necesario.

La siguiente tabla muestra cómo se utilizará la información de los campos opcionales en las líneas de planificación de proyecto y los diarios cuando se elijan el recurso, el artículo o la cuenta de contabilidad para el trabajo.

|Columna 1  |Columna 2  |
|---------|---------|
|**Recursos de trabajo**|Los campos **Nº tarea de proyecto**, **Tipo de trabajo**, **Códido de divisa**, **Descuento línea %** y **Factor de coste unitario**. Se usará el valor del campo **Precio de venta** correspondiente al recurso en las líneas de planificación de proyecto y los diarios de proyectos cuando se introduzca este recurso, un recurso asignado al grupo de recursos o cualquier recurso. Tenga en cuenta que este precio anulará siempre los precios establecidos en la página **Precio de recurso/Precios de grupo de recursos** existente.|
|**Elementos de trabajo**|Los campos **N.º de tarea de proyecto**, **Códido de divisa** y **% de Descuento de línea**. El valor del campo **Precio de venta** correspondiente al artículo se usará en las líneas de planificación del proyecto y en los diarios de proyectos cuando se introduzca este producto. tenga en cuenta que este precio siempre anulará el precio regular del cliente (mecanismo de “mejor precio”) de los productos. Si desea usar los mecanismos de precio regular del cliente, no debe crear ningún precio de producto para el proyecto.|
|**Cuentas de contabilidad**|La información de los campos **N.º tarea proyecto**, **Código de divisa**, **% de descuento de línea**, **Factor de coste unitario** y **Coste unitario** se usará en las líneas de planificación de proyecto y los diarios de proyectos cuando se introduce esta cuenta de contabilidad y se agrega a un proyecto. El valor del campo **Precio de venta** del gasto de proyecto de contabilidad se usará en las líneas de planificación de proyecto y en los diarios de proyectos cuando se introduzca esta cuenta.|

---
#### <a name="new-experience"></a>[Nueva experiencia](#tab/new-experience)
1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Proyectos** y luego elija el enlace relacionado.  
2. Seleccione el proyecto correspondiente y, a continuación, elija la acción **Listas de precios de venta**.

---

## <a name="to-set-up-job-posting-groups"></a>Para configurar grupos contables del proyecto
Un aspecto de los proyectos de planificación es decidir qué cuentas de registro se deben utilizar para la valoración de proyectos. Para poder registrar proyectos, debe configurar cuentas de registro para cada grupo contable del proyecto. Un grupo contable representa un vínculo entre el proyecto y cómo debe ser tratado en la contabilidad general. Al crear un proyecto, se especifica un grupo contable y, de forma predeterminada, todas las tareas que crea para el proyecto están asociadas con ese grupo contable. Sin embargo, al crear las tareas, puede sustituir el predeterminado y seleccionar a un grupo contable que sea más adecuado.  

> [!NOTE]  
>   Se deben configurar las cuentas necesarias en el plan de cuentas antes de configurar los grupos contables. Para obtener más información, vea [Configuración o cambio del plan de cuentas](finance-setup-chart-accounts.md).  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Grupos contables de proyectos**, y luego elija el enlace relacionado.  
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
[Vídeo: Cómo crear un proyecto en Dynamics 365 Business Central](https://www.youtube.com/watch?v=VqaPWr7BWmw)  
[Administrar proyectos](projects-manage-projects.md)  
[Finanzas](finance.md)  
[Compras](purchasing-manage-purchasing.md)  
[Ccial](sales-manage-sales.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
