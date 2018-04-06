---
title: Experiencia contable en Dynamics 365 | Documentos de Microsoft
description: "Información sobre el Accountant Hub de Dynamics 365."
author: edupont04
ms.service: dynamics365-accountant
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 11/10/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: 591ca492802166610f00ad5be09badd719fdb64a
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="get-started-with-included365acclongincludesd365acclongmdmd"></a>Introducción a [!INCLUDE[d365acc_long](includes/d365acc_long_md.md)]
[!INCLUDE[d365fin_early_release](includes/d365fin_early_release.md.md)]

Los negocios deben crear sus libros y firmas de contabilidad. Algunas empresas emplean un contable externo, y otras lo tienen en plantilla. Si es un contable con varios clientes, puede utilizar [!INCLUDE[d365acc](includes/d365acc_md.md)] como su panel de control para obtener una mejor visión general de sus clientes.  

Puede obtener acceso a [!INCLUDE[d365acc](includes/d365acc_md.md)] si se registra en [Dynamics 365 — Accountant Hub en Microsoft.com](https://www.microsoft.com/en-us/dynamics365/financial-insights-for-accountants).  

> [!TIP]  
>  Cuando se registra en [!INCLUDE[d365acc](includes/d365acc_md.md)], debe especificar su dirección de correo electrónico de empresa, como *me@accountant.com*. Recomendamos que utilice la misma dirección de correo electrónico cuando trabaje en el [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] de sus clientes, de modo que pueda cambiar fácilmente entre clientes. La dirección de correo electrónico debe ser una dirección de trabajo basada en Active Directory.

## <a name="working-with-individual-clients"></a>Trabajar con clientes individuales
El panel muestra la información más importante sobre cada cliente.  
![Accountant Hub](./media/accountant-get-started/accountant-dashboard-tasks.png)

La columna **Nombre del cliente** muestra los nombres de sus clientes y la columna **Nombre de la empresa** muestra todas las empresas si el cliente tiene más de una empresa en [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]. También hay campos para mostrarle las tareas que le asignaron en la empresa de su cliente, incluidas las tareas vencidas.  

Puede personalizar el panel para mostrar los puntos de datos que desea ver añadiendo o eliminando columnas. Por ejemplo, es posible que desee ver los impuestos que se deben, cuántos documentos de ventas abiertos tiene cada cliente, o el número de facturas de compra que vencen la próxima semana. Puede configurar la vista para adaptarla a sus necesidades. Si tiene varios clientes, puede utilizar filtros para ordenar la vista.  

Junto al nombre del cliente, los puntos suspensivos (...) revelan un menú corto:

-   Actualizar la empresa actual y obtener nuevos datos para el cliente  
-   Vaya al [!INCLUDE[d365fin](includes/d365fin_md.md)] del cliente  
-   Seleccionar más clientes  

De manera similar, por ejemplo, puede utilizar el menú desplegable **Resumen de cliente** para actualizar todas las empresas.  

> [!TIP]  
>  Para acceder al [!INCLUDE[d365fin](includes/d365fin_md.md)] de un cliente, seleccione el elemento de menú **Ir al cliente** y se inicia sesión automáticamente.

## <a name="company-details"></a>Detalles empresa
Puede ver más información acerca de los datos de sus clientes eligiendo el nombre de la empresa sobre la que desea saber más. Se abrirá el panel **Detalles empresa**, donde podrá ver la información adicional siguiente:  

* Saldos de cuentas de efectivo  
* Previsión flujos efectivo  
* Facturas compra vencidas  
* Facturas venta vencidas  

![Los detalles de la empresa cliente en el escritorio del contable](./media/accountant-get-started/accountant-company-details.png)

Técnicamente, ahora se ha registrado en su [!INCLUDE[d365fin](includes/d365fin_md.md)] del cliente y los datos que se ven son datos reales. Si desea estudiar atentamente los datos, como una factura de compra vencida, elija el vínculo y se le redireccionará a la empresa cliente.  

> [!TIP]  
>  Puede lanzar los libros de Excel predefinidos de la pestaña **Informes** en la cinta de opciones. Estos libros de Excel están diseñadas para estar listos para imprimir los informes financieros e informes clave, pero también puede modificarlos en función de sus necesidades. Para obtener más información, consulte [Análisis de estados financieros en Microsoft Excel](/dynamics365/financials/finance-analyze-excel?toc=/dynamics365/accountants/toc.json) en la ayuda de [!INCLUDE[d365fin](includes/d365fin_md.md)].  

En caso contrario, cierre el panel de detalles y continúe con el cliente siguiente.  

## <a name="assigned-tasks"></a>Tareas asignadas
En el [!INCLUDE[d365fin](includes/d365fin_md.md)] del cliente, puede asignarse tareas y asignarlas a otros y viceversa. Su escritorio en [!INCLUDE[d365acc](includes/d365acc_md.md)] le ofrece un resumen de las tareas asignadas por cada cliente, y puede tener acceso a una lista de todas las tareas asignadas mediante **Mis tareas de usuario** en el panel de navegación izquierdo.  

En la empresa cliente, también tiene pistas que indican sus tareas asignadas en este cliente en particular.

![Tareas asignadas al contable en la empresa cliente](./media/accountant-get-started/accountant-company-details-tasks.png)

### <a name="my-user-tasks"></a>Mis tareas de usuario
La lista **Mis tareas de usuario** de [!INCLUDE[d365acc](includes/d365acc_md.md)] le ayuda a priorizar su día al mostrar más información sobre sus tareas asignadas en todos sus clientes.  

![Mi lista de tareas asignadas como contable externo](./media/accountant-get-started/accountant-tasklist.png)

Puede ordenarlas por fecha de vencimiento, por ejemplo, o por otro tipo de datos que lo ayuden a priorizar su día. De forma predeterminada, la lista muestra todas las tareas que tiene asignadas, pero puede configurar filtros para que solo se muestren las tareas marcadas como de alta prioridad, por ejemplo.

Para elegir una tarea, simplemente selecciónela de la lista de tareas pendientes del usuario. En la cinta de opciones, el vínculo **Ir al elemento de la tarea** abrirá la ventana en la que puede realizar el trabajo.  

Cuando haya terminado una tarea, simplemente márquela como completada.  

## <a name="see-also"></a>Consulte también
[Agregar clientes al escritorio de [!INCLUDE[d365acc](includes/d365acc_md.md)]](add-client.md)  
[[!INCLUDE[d365acc_long](includes/d365acc_long_md.md)]](index.md)  
[Análisis de estados financieros en Microsoft Excel](/dynamics365/financials/finance-analyze-excel?toc=/dynamics365/accountants/toc.json)   
[Experiencias contables en [!INCLUDE[d365fin](includes/d365fin_md.md)]](/dynamics365/financials/finance-accounting?toc=/dynamics365/accountants/toc.json)  
[Dynamics 365 — Accountant Hub en Microsoft.com](https://www.microsoft.com/en-us/dynamics365/financial-insights-for-accountants)  

