---
title: Ver y editar la configuración básica | Documentos de Microsoft
description: Obtenga información sobre cómo cambiar algunos de los valores básicos, por ejemplo, el área de trabajo, la empresa o la fecha de trabajo.
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: change Role Center, notification, change company, change work date
ms.date: 04/01/2019
ms.author: solsen
ms.openlocfilehash: d95d2f609129e4bdba35deda726323dbed2ba67a
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/29/2019
ms.locfileid: "1250978"
---
# <a name="changing-basic-settings"></a>Cambiar la configuración básica
En la página [**Mi configuración**](https://businesscentral.dynamics.com?page=9176 "Vaya directamente a la página de configuración en Business Central"), puede ver y cambiar la configuración básica de [!INCLUDE[d365fin](includes/d365fin_md.md)]. Los cambios que realice sólo afectan a su área de trabajo; no a las áreas de trabajo de otros usuarios.  

## <a name="role-center"></a> Área de trabajo
El área de trabajo representa la página Inicio, una pantalla de inicio que está designada para las necesidades específicas del trabajo en una empresa. Dependiendo de su función, el Área de trabajo le brinda una descripción general del negocio, su departamento o sus tareas personales. También le ayuda a navegar por sus tareas diarias y encontrar el trabajo que le asignaron.

-   En la parte superior, la navegación le permite cambiar entre clientes, proveedores, artículos y otras listas importantes de información. Del mismo modo, las acciones le permiten iniciar tareas, como crear una nueva factura de venta, directamente desde el Área de trabajo.

-   En el centro se encuentran las **Actividades**. Las actividades muestran datos actuales y se puede hacer clic en ellas o tocarlas para ver información más detallada. Los Indicadores de rendimiento clave pueden configurarse para mostrar un gráfico seleccionado para una representación visual de, por ejemplo, el flujo de efectivo o ingresos y gastos. También puede crear una lista de clientes favoritos en la página de inicio para las cuentas con las que hace negocios a menudo o a las que necesita prestar especial atención.

### <a name="to-change-role-center"></a>Para cambiar el área de trabajo
El Área de trabajo predeterminada es **Admin. empresarial**, pero puede seleccionar otra Área de trabajo que se adapte mejor a sus necesidades.
1. En la esquina superior derecha, elija el icono **Configuración** ![Configuración](media/ui-experience/settings_icon_small.png "Icono Configuración para el área de trabajo") y, a continuación, elija **Mi configuración**.
2. En la página **Mi configuración**, en el campo **Área de trabajo**, seleccione el área de trabajo que quiere establecer como estándar. Por ejemplo, seleccione **Contable**.
3. Elija el botón **Aceptar**.

## <a name="company"></a>Compañía
Una empresa funciona como un contenedor de datos en [!INCLUDE[d365fin](includes/d365fin_md.md)]. Puede haber múltiples empresas en una base de datos, pero solo se puede seleccionar una a la vez.

La empresa predeterminada se llama CRONUS y solo contiene datos de demostración.

> [!TIP]  
>   Si desea que se muestre un nombre distinto para la empresa en la aplicación (por ejemplo, como en el área de trabajo), establezca el campo **Nombre** en la página **Información empresa** o el campo **Nombre para mostrar** en la página **Empresas**.  

## <a name="work-date"></a>Fecha de trabajo
La fecha predeterminada de trabajo será normalmente la fecha actual. Es posible que tenga que cambiar temporalmente la fecha de trabajo para realizar tareas como la finalización de las transacciones de una fecha que no sea la fecha actual.

> [!TIP]  
>   Escriba **t** para introducir rápidamente la fecha de trabajo en un campo de fecha. Escriba **h** para introducir rápidamente la fecha actual en el campo de fecha.

> [!IMPORTANT]  
>   Después de modificar la fecha de trabajo, si cierra la sesión o cambia a otra empresa, los datos de trabajo vuelven a la fecha de trabajo predeterminada. Por lo tanto, la próxima vez que inicie sesión o vuelva a cambiar a la empresa original, es posible que tenga que volver a establecer la fecha de trabajo. 

### <a name="work-date-indication"></a>Indicación de la fecha de trabajo
<!--
Whenever the work date is not set to the current day (today), there are two indicators on pages that you open for editing:

- A reminder appears at the top of the page that tells you what the work date is set to. The reminder provides a direct link to the work date setting on the **My Settings** page so you change the date if you want. From the reminder, you can also choose to dismiss the reminder for the rest of your session. Unless you change the work date to "today", the reminder will appear the next time you sign in. 

- If you dismiss the reminder, the work date will appear in the title of the page.  
-->
Si la fecha de trabajo no está establecida en el día actual (hoy), la fecha de trabajo actual se muestra en la esquina superior izquierda de todas las páginas donde puede editar datos.
  
## <a name="region"></a> Región

El valor **Región** determina cómo se muestran o se forman las fechas, los tiempos, los números, y divisas.


## <a name="language"></a> Idioma
Cambia el idioma de la pantalla. Este campo aparece sólo cuando hay más de un idioma a elegir. 

El idioma inicial lo determina el administrador o la configuración de su navegador cuando inicia sesión en [!INCLUDE[d365fin](includes/d365fin_md.md)]. El idioma que establezca se usará en todos los dispositivos desde los que inicie sesión, como un teléfono o una tableta.

## <a name="changing-when-i-receive-notifications"></a>Cambio al recibir notificaciones
Seleccione este vínculo para ver o cambiar las notificaciones que recibe sobre determinados eventos o cambios de estado, cuando va a facturar a un cliente que tiene un saldo vencido o cuando el inventario disponible es inferior a la cantidad que va a vender, por ejemplo. Para obtener más información, consulte [Notificaciones inteligentes](ui-smart-notifications.md).

## <a name="see-also"></a>Consulte también
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Cambiar las funciones que se muestran](ui-experiences.md)  
