---
title: Previsiones de flujo de efectivo con esquemas de cuentas
description: Este tutorial describe cómo puede utilizar los esquemas de cuentas para elaborar previsiones del flujo de efectivo en Business Central.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/24/2021
ms.author: edupont
ms.openlocfilehash: 7238b4de3b4a48c61560bc9a96a6923afe82eb93
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/19/2022
ms.locfileid: "9533487"
---
# <a name="walkthrough-making-cash-flow-forecasts-by-using-account-schedules"></a>Tutorial: elaboración de previsiones del flujo de efectivo con esquemas de cuentas

Este tutorial describe cómo puede utilizar los esquemas de cuentas para elaborar previsiones del flujo de efectivo. Los esquemas de cuentas realizan cálculos que no se puedan realizar directamente en el plan de cuentas del flujo de efectivo. En los esquemas de cuentas, puede configurar los subtotales para las recepciones y los desembolsos del flujo de efectivo. Estos subtotales se pueden incluir de los nuevos totales que pueden usarse en la elaboración de previsiones del flujo de efectivo.  

## <a name="about-this-walkthrough"></a>Acerca de este tutorial

En este tutorial se describen las siguientes tareas:  

- Configuración de un nuevo nombre de esquema de cuenta del flujo de efectivo.  
- Configuración de líneas de esquema de cuenta.  
- Configuración de un nuevo diseño de columna.  
- Asignación de un diseño de columna a un esquema de cuentas  
- Ver e imprimir la previsión del flujo de efectivo.  

### <a name="prerequisites"></a>Requisitos previos

Para completar este tutorial, necesitará:  

- [!INCLUDE[prod_short](includes/prod_short.md)]  
- Se registran las líneas de la hoja de trabajo del flujo de efectivo  

## <a name="roles"></a>Roles

En este tutorial, se demuestran las tareas realizadas por el siguiente rol de usuario:  

- Controlador  

## <a name="story"></a>Historia

Ken es un controlador de CRONUS que efectúa previsiones mensuales del flujo de efectivo. Incluye las finanzas, ventas, compras y activos fijos en la previsión y, a continuación, lo envía a CFO Sara para una perspectiva de negocio.  

## <a name="setting-up-a-new-account-schedule-name"></a>Configuración de un nuevo nombre de esquema de cuenta.

Un esquema de cuentas consta de un nombre de esquema de cuenta del flujo de efectivo con una serie de líneas y un diseño de columna.  

### <a name="to-set-up-a-new-account-schedule-name"></a>Configuración de un nuevo nombre de esquema de cuenta  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Esquemas de cuentas** y luego elija el enlace relacionado.  
2. En la página **Nombres de esquema de cuenta**, elija **Nuevo** para crear un nuevo nombre de cuenta de flujo de efectivo.  
3. En el campo **Nombre**, especifique **Previsiones**.  
4. En el campo **Descripción**, introduzca **Previsión de flujo de efectivo**.  
5. Deje en blanco los campos **Plantilla columna genér.** y **Nombre vista análisis**.  

## <a name="setting-up-account-schedule-lines"></a>Configuración de líneas de esquema de cuenta

Después de configurar el nombre del esquema de cuentas, Ken define cada línea que aparece en el esquema de cuenta del flujo de efectivo. Ken define las líneas que se pueden mostrar en los informes además de las líneas que se sólo se utilizan para realizar cálculos.  

### <a name="to-set-up-account-schedule-lines"></a>Para configurar líneas de esquema de cuenta  

1. En la página **Nombres esquemas de cuentas**, seleccione el nombre del nuevo esquema de cuentas **Previsión** y después seleccione la acción **Editar esquema cuentas**.  
2. En la página **Esquema de cuentas**, especifique cada línea como se muestra en la siguiente tabla.  

    > [!TIP]  
    >  Con la función **Insertar cuentas de coste y flete**, puede marcar rápidamente los cuentas de flujo de efectivo del plan de cuentas del flujo de efectivo y copiar las líneas del esquema de cuentas.  

    | Nº fila | Descripción              | Tipo sumatorio            | Sumatorio | Tipo fila   | Tipo importe | Mostrar |
    |---------|--------------------------|--------------------------|----------|------------|-------------|------|
    | R10     | Abrir pedidos de venta        | Cuentas movimientos de flujo de efectivo | nº 20       |Saldo periodo | Importe neto  | Sí  |
    | R10     | Alquileres                  | Cuentas movimientos de flujo de efectivo | 30       |Saldo periodo | Importe neto  | Sí  |
    | R10     | Activos financieros         | Cuentas movimientos de flujo de efectivo | 40       |Saldo periodo | Importe neto  | Sí  |
    | R10     | Venta/baja de activos fijos    | Cuentas movimientos de flujo de efectivo | 50       |Saldo periodo | Importe neto  | Sí  |
    | R10     | Inversiones privadas      | Cuentas movimientos de flujo de efectivo | 60       |Saldo periodo | Importe neto  | Sí  |
    | R10     | Albaranes varios   | Cuentas movimientos de flujo de efectivo | 70       |Saldo periodo | Importe neto  | Sí  |
    | R10     | Pedidos de servicio abiertos      | Cuentas movimientos de flujo de efectivo | 80       |Saldo periodo | Importe neto  | Sí  |
    | R20     | Total de recibos de efectivo      | Fórmula                  | R10      |Saldo periodo | Importe neto  | Sí  |
    | R20     | Total de recibos de efectivo      | Fórmula                  | R10      |Saldo periodo | Importe neto  | Sí  |
    | R30     | Pagos                 | Cuentas movimientos de flujo de efectivo | 1010     |Saldo periodo | Importe neto  | Sí  |
    | R30     | Pedidos de compra abiertos     | Cuentas movimientos de flujo de efectivo | nº 1020     |Saldo periodo | Importe neto  | Sí  |
    | R30     | Costes de personal          | Cuentas movimientos de flujo de efectivo | 1030     |Saldo periodo | Importe neto  | Sí  |
    | R30     | Costes de funcionamiento            | Cuentas movimientos de flujo de efectivo | 1040     |Saldo periodo | Importe neto  | Sí  |
    | R30     | Costes financieros            | Cuentas movimientos de flujo de efectivo | 1050     |Saldo periodo | Importe neto  | Sí  |
    | R30     | Inversiones              | Cuentas movimientos de flujo de efectivo | 1070     |Saldo periodo | Importe neto  | Sí  |
    | R30     | Consumos privados     | Cuentas movimientos de flujo de efectivo | 1090     |Saldo periodo | Importe neto  | Sí  |
    | R30     | IVA vencido                  | Cuentas movimientos de flujo de efectivo | 1100     |Saldo periodo | Importe neto  | Sí  |
    | R30     | Otros gastos           | Cuentas movimientos de flujo de efectivo | 1110     |Saldo periodo | Importe neto  | Sí  |
    | R40     | Total de desembolsos en efectivo | Fórmula                  | R30      |Saldo periodo | Importe neto  | Sí  |
    | R50     | Excedente                  | Fórmula                  | R20+R40  |Saldo periodo | Importe neto  | Sí  |
    | R60     | Fondos de flujos de efectivo          | Cuentas movimientos de flujo de efectivo | 2100     |Saldo periodo | Importe neto  | Sí  |
    | R70     | Total de flujo de efectivo          | Fórmula                  | R50+R60  |Saldo periodo | Importe neto  | Sí  |

    > [!NOTE]
    > El número de fila R10 se utiliza para capturar totales de cuentas para clientes. El número de fila R20 se utiliza para calcular la suma de todos los cobros. El número de fila R30 se utiliza para capturar totales de cuentas para proveedores. El número de fila R40 se utiliza para calcular la suma de todos los desembolsos de efectivo. El número de fila R50 se utiliza para capturar la suma de exceso de efectivo. El número de fila R60 se utiliza para capturar los fondos líquidos. El número de fila R70 se utiliza para calcular el flujo de efectivo previsto.

## <a name="setting-up-a-new-column-layout"></a>Configuración de un nuevo diseño de columna

Antes de que Ken pueda imprimir la previsión del flujo de efectivo, necesita crear el diseño de columna para la información numérica. En las columnas, define la información que desea utilizar de las líneas.

- La primera columna tiene el número *C10* con el título **Importe** y contiene el saldo del periodo.  
- La segunda columna tiene el número *C20* con el título **Saldo a la fecha** y contiene las transacciones para el periodo.  
- La tercera columna tiene el número *C30* con el título **Año completo** y contiene el saldo del periodo en los saldos del ejercicio completo.  
- Por último, asigna el diseño de columna como diseño de columna predeterminado para el esquema de cuentas **Previsiones**.  

## <a name="to-set-up-a-new-column-layout"></a>Para configurar un nuevo diseño de columna

1. En la ventana **Nombre de esquema de cuentas**, seleccione el nuevo nombre del esquema de cuentas **Previsiones** que ha creado. En la pestaña **Inicio**, en el grupo **Procesar**, elija **Editar configuración de diseño de columna**.

    > [!TIP]
    > Puede encontrar la misma acción en la página **Esquema de cuentas** si todavía está editando allí el esquema de cuentas **Pronóstico**.

2. Cree un nuevo diseño de columna con el nombre **Flujo de efectivo**.

3. Elija el botón Aceptar.

4. Introduzca cada línea exactamente como se muestra en la siguiente tabla.

    |Nº columna|Cabecera de columna|Tipo de columna|Tipo de movimiento|Tipo importe|Mostrar|  
    |----------|-------------|-----------|-----------------|-----------|----|
    |C10|Importe|Saldo periodo|Movimientos|Importe neto|Siempre|  
    |C20|Importe hasta fecha|Saldo a la fecha|Movimientos|Importe neto|Siempre|  
    |C30|Todo el ejercicio|Todo el ejercicio|Movimientos|Importe neto|Siempre|

## <a name="assigning-the-column-layout-to-the-account-schedule-name"></a>Asigna el nombre de la plantilla de columnas del esquema de cuentas.

Ken ahora está preparado para asignar el diseño de columna al nombre del esquema de cuentas.  

### <a name="to-assign-the-column-layout-to-the-account-schedule-name"></a>Para asignar el nombre de la plantilla de columnas del esquema de cuentas.  

1. En la página **Esquema de cuentas** en la que está trabajando con el esquema de cuentas **Pronóstico**, elija la acción **Editar configuración de diseño de columna**.  
2. En el campo **Nombre de diseño de columna**, seleccione el diseño de columna **Flujo de efectivo** para asignarlo como diseño de columnas predeterminado.  

### <a name="to-view-and-print-the-cash-flow-forecast"></a>Para ver e imprimir la previsión del flujo de efectivo

1. En la página **Nombres de esquemas de cuentas**, seleccione la acción **Información general** para ver la previsión del flujo de efectivo.  
2. En la página **Panorama esq. cta.**, puede seleccionar un importe y después ver los movimientos de la previsión del flujo de efectivo que conforman el importe. Además, puede ver la fórmula que se utiliza para calcular el importe. También puede filtrar los importes por fecha y dimensión.  
3. Elija la acción **Imprimir** para que se imprima la previsión de flujo de efectivo.  

## <a name="see-related-microsoft-training"></a>Consultar la [formación de Microsoft](/training/modules/forecast-cash-flow-dynamics-365-business-central/) relacionada

## <a name="see-also"></a>Consulte también .

[Trabajar con esquemas de cuentas](bi-how-work-account-schedule.md)  
[Analizar el flujo de efectivo de la empresa](finance-analyze-cash-flow.md)  
[Tutoriales de procesos empresariales](walkthrough-business-process-walkthroughs.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
