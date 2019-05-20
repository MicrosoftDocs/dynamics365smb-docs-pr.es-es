---
title: 'Tutorial: elaboración de previsiones del flujo de efectivo con esquemas de cuentas | Documentos de Microsoft'
description: Este tutorial describe cómo puede utilizar los esquemas de cuentas para elaborar previsiones del flujo de efectivo. Los esquemas de cuentas realizan cálculos que no se puedan realizar directamente en el plan de cuentas del flujo de efectivo. En los esquemas de cuentas, puede configurar los subtotales para las recepciones y los desembolsos del flujo de efectivo. Estos subtotales se pueden incluir de los nuevos totales que pueden usarse en la elaboración de previsiones del flujo de efectivo.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: c09eedbb812df909a43e514dc462dcf8c1cf182a
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/29/2019
ms.locfileid: "1249312"
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

- [!INCLUDE[d365fin](includes/d365fin_md.md)] Instalada.  
- Se registran las líneas de la hoja de trabajo del flujo de efectivo.  

## <a name="roles"></a>Roles  
En este tutorial, se demuestran las tareas realizadas por el siguiente rol de usuario:  

- Controlador  

## <a name="story"></a>Historia  
Ken es un controlador de CRONUS que efectúa previsiones mensuales del flujo de efectivo. Incluye las finanzas, ventas, compras y activos fijos en la previsión y, a continuación, lo envía a CFO Sara para una perspectiva de negocio.  

## <a name="setting-up-a-new-account-schedule-name"></a>Configuración de un nuevo nombre de esquema de cuenta.  
Un esquema de cuentas consta de un nombre de esquema de cuenta del flujo de efectivo con una serie de líneas y un diseño de columna.  

### <a name="to-set-up-a-new-account-schedule-name"></a>Configuración de un nuevo nombre de esquema de cuenta  

1.  Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Esquemas de cuentas** y luego elija el enlace relacionado.  
2.  En la página **Nombres de esquema de cuenta**, elija **Nuevo** para crear un nuevo nombre de cuenta de flujo de efectivo.  
3.  En el campo **Nombre**, especifique **Previsiones**.  
4.  En el campo **Descripción**, introduzca **Previsión de flujo de efectivo**.  
5.  Deje en blanco los campos **Plantilla columna genér.** y **Nombre vista análisis**.  

## <a name="setting-up-account-schedule-lines"></a>Configuración de líneas de esquema de cuenta  
Después de configurar el nombre del esquema de cuentas, Ken define cada línea que aparece en el esquema de cuenta del flujo de efectivo. Ken define las líneas que se pueden mostrar en los informes además de las líneas que se sólo se utilizan para realizar cálculos.  

### <a name="to-set-up-account-schedule-lines"></a>Para configurar líneas de esquema de cuenta  

1.  En la página **Nombre esquema cuenta**, seleccione el nuevo nombre del esquema de cuentas de **Previsiones** que ha creado. En la pestaña **Inicio**, en el grupo **Procesar**, elija **Editar esquema cuentas**.  
2.  En la página **Esquema cuentas**, especifique cada línea exactamente como se muestra en la siguiente tabla.  

    > [!NOTE]  
    >  Con la función **Insertar cuentas de coste y flete**, puede marcar rápidamente los cuentas de flujo de efectivo del plan de cuentas del flujo de efectivo y copiar las líneas del esquema de cuentas.  

    |Nº fila|Descripción|Tipo sumatorio|Sumatorio|Tipo fila|Tipo importe|Mostrar|  
    |-------|-----------|-------------|--------|--------|---  ------|----| |C10|Importe|Cambio neto|Movimientos|Importe neto|Siempre|  
    |C20|Importe hasta fecha|Saldo a la fecha|Movimientos|Importe neto|Siempre|  
    |C30|Todo el ejercicio|Todo el ejercicio|Movimientos|Importe neto|Siempre|  

4.  Elija el botón **Aceptar**.  

## <a name="assigning-the-column-layout-to-the-account-schedule-name"></a>Asigna el nombre de la plantilla de columnas del esquema de cuentas.  
Ken ahora está preparado para asignar el diseño de columna al nombre del esquema de cuentas.  

### <a name="to-assign-the-column-layout-to-the-account-schedule-name"></a>Para asignar el nombre de la plantilla de columnas del esquema de cuentas.  

1.  En la página **Nombres esquemas de cuentas**, seleccione **Previsión** en el campo **Nombre**.  
2.  En el campo **Plantilla columna genér.**, seleccione el diseño de columna **Flujo de efectivo** para asignar como diseño de columnas predeterminado.  

### <a name="to-view-and-print-the-cash-flow-forecast"></a>Para ver e imprimir la previsión del flujo de efectivo  
1.  En la página **Nombres de esquemas de cuentas**, seleccione la acción **Información general** para ver la previsión del flujo de efectivo.  
2.  En la página **Panorama esq. cta.**, puede seleccionar un importe y después ver los movimientos de la previsión del flujo de efectivo que conforman el importe. Además, puede ver la fórmula que se utiliza para calcular el importe. También puede filtrar los importes por fecha y dimensión.  
3.  Elija la acción **Imprimir** para que se imprima la previsión de flujo de efectivo.  

## <a name="see-also"></a>Consulte también  
 [Trabajar con esquemas de cuentas](bi-how-work-account-schedule.md)   
 [Tutoriales de procesos empresariales](walkthrough-business-process-walkthroughs.md)  
 [Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
