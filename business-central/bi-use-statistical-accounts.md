---
title: Usar cuentas estadísticas para analizar datos no transaccionales
description: Describe cómo usar las cuentas estadísticas como otro origen de datos para sus análisis.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: how-to
ms.date: 03/07/2023
ms.custom: bap-template
ms.search.keywords: 'bi, power BI, analysis, KPI, financial report'
ms.search.form: '2632, 2631, 2633, 2623, 2634'
---
# <a name="analyze-data-with-statistical-accounts"></a><a name="analyze-data-with-statistical-accounts"></a><a name="analyze-data-with-statistical-accounts"></a>Analice datos con cuentas estadísticas

Utilice cuentas estadísticas para complementar la información de los informes financieros. Las cuentas estadísticas le permiten agregar métricas que se basan en datos no transaccionales. Puede agregar los datos no transaccionales como unidades basadas en números, como:

* Número de empleados
* Pies cuadrados
* El número de clientes con cuentas vencidas

Por ejemplo, puede medir los ingresos o los costes segúnel número de personas de un departamento. El número de empleados del departamento es la unidad de la cuenta estadística. La siguiente imagen muestra un ejemplo de un informe que utiliza una cuenta estadística para mostrar los ingresos por empleado.

:::image type="content" source="media/statistical account report example.png" alt-text="Un ejemplo de un informe que incluye datos de una cuenta estadística.":::

En cuanto a su funcionamiento, las cuentas estadísticas son similares a las cuentas de registro. Almacenan las transacciones que registra utilizando diarios de cuentas estadísticos, de modo que puede usar las transacciones como datos para informes financieros. Para más información sobre los informes financieros, vaya a [Preparar Financial Reporting con categorías de cuentas y datos financieros](bi-how-work-account-schedule.md). 

Hay un par de diferencias clave entre las cuentas estadísticas y las cuentas de registro. Las cuentas estadísticas son entidades separadas y no se incluyen en los informes de balance de comprobación. Además, no necesita equilibrar los importes de débito y crédito cuando utiliza diarios de cuentas estadísticas para contabilizar asientos en una cuenta estadística. Simplemente se registra el importe.

## <a name="set-up-a-statistical-account"></a><a name="set-up-a-statistical-account"></a><a name="set-up-a-statistical-account"></a>Configurar una cuenta estadística

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Cuentas estadísticas** y luego elija el vínculo relacionado.
1. Rellene los campos en la ficha desplegable **General**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="post-amounts-to-a-statistical-account"></a><a name="post-amounts-to-a-statistical-account"></a><a name="post-amounts-to-a-statistical-account"></a>Contabilizar importes en una cuenta estadística

1. Para registrar los importes de los que desea realizar un seguimiento, en la página **Cuentas estadísticas**, elija la acción **Diario de cuentas estadísticas**.
1. En el campo **Fecha de registro**, introduzca la última fecha del periodo de registro en el que desea registrar importes.
1. Opcional: si desea realizar un seguimiento de los importes de un documento específico, en el campo **N.º de documento**, introduzca el id. del documento.
1. En el campo **N.º de cuenta estadística** , elija la cuenta estadística en la que contabilizará los importes.
1. En el campo **Descripción**, introduzca una descripción breve de lo que está midiendo.  
1. En el campo **Importe**, introduzca el importe a registrar. 
1. Opcional: si desea incluir la cuenta estadística en análisis más avanzados, especifique las dimensiones en los campos **Código de departamento** y **Código de grupo de clientes**. Para obtener más información sobre las dimensiones, vaya a [Analizar datos por dimensiones](bi-how-analyze-data-dimension.md).

## <a name="verify-statistical-account-amounts"></a><a name="verify-statistical-account-amounts"></a><a name="verify-statistical-account-amounts"></a>Verificar importes de cuentas estadísticas

En la página **Cuentas estadísticas**, use la acción **Saldo de cuentas estadísticas** para verificar que los importes registrados sean correctos para cada período.  

## <a name="include-the-statistical-account-in-a-financial-report"></a><a name="include-the-statistical-account-in-a-financial-report"></a><a name="include-the-statistical-account-in-a-financial-report"></a>Incluir la cuenta estadística en un informe financiero

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Informes financieros** y luego elija el vínculo relacionado.
1. Cree un nuevo informe financiero de una de las siguientes maneras:
    1. Para empezar desde cero, elija **Nuevo**. Para obtener más información sobre cómo crear informes financieros, vaya a [Crear un nuevo informe financiero](bi-how-work-account-schedule.md#create-a-new-financial-report).
    1. Para usar la configuración desde un informe similar que ya tiene, elija el informe que desea copiar y luego elija la acción **Copiar informe financiero** . Puede editar la configuración que copia en su nuevo informe.
1. Agregue la cuenta estadística:
    1. Si está comenzando desde cero, elija la acción **Editar definición de fila**.
    1. Para usar una definición de fila desde un informe existente, elija el informe desde el que desea copiar y luego elija la acción **Copiar definición de fila** .
1. En la página **Definición de fila**, en el campo **N.º de fila** , defina dónde aparecerá la fila en la secuencia de filas del informe.
1. En el campo **Descripción**, introduzca texto que indique lo que está midiendo.
1. En el campo **Tipo de totalización**, seleccione **Cuentas estadísticas**.
1. En el campo **Totalización**, seleccione uan cuenta estadística.
1. En el campo **Tipo de fila**, elija si desea ver el saldo en la fecha de registro o al comienzo del período de registro, o mostrar el cambio en el importe durante el período.
1. Rellene el resto de campos. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Consulte también

[Inteligencia empresarial financiera](bi.md)  
[Informes y análisis financieros en Business Central](finance-reports.md)
