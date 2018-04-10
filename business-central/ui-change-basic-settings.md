---
title: "Ver y editar la configuración básica en Financials | Documentos de Microsoft"
description: "Obtenga información sobre cómo cambiar algunos de los valores básicos en Financials, por ejemplo, el área de trabajo, la empresa o la fecha de trabajo."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: change Role Center, notification, change company, change work date
ms.date: 03/02/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: c7f07bd3cee8d52cccf171dfd229265d65e99cba
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="changing-basic-settings"></a>Cambiar la configuración básica
En la ventana **Mi configuración**, puede ver y cambiar la configuración básica de [!INCLUDE[d365fin](includes/d365fin_md.md)].  

## <a name="role-center"></a>Área de trabajo
El área de trabajo representa la página Inicio y está designada para las necesidades del trabajo. El área de trabajo proporciona una vista general del negocio, que refleja la información, las tareas y las prioridades de su área.

En la parte superior del área de trabajo verá una barra de navegación que le brinda fácil acceso a entidades típicas para el área, como clientes, proveedores, productos, etc.

Lo que aparezca en el área de contenido principal dependerá del área de trabajo específica. Por ejemplo, en la mayoría de las áreas de trabajo, puede encontrar los mosaicos de Actividades que muestran datos actuales y se puede hacer clic o tocar para acceder fácilmente al documento seleccionado. Los Indicadores de rendimiento clave pueden configurarse para mostrar un gráfico seleccionado para una representación visual de, por ejemplo, el flujo de efectivo o ingresos y gastos. Algunas áreas de trabajo le permiten crear una lista de objetos favoritas, como clientes y proveedores o mostrar una Bandeja de entrada de informes.

### <a name="to-change-role-center"></a>Para cambiar el área de trabajo
El Área de trabajo predeterminada es **Admin. empresarial**, pero puede seleccionar otra Área de trabajo que se adapte mejor a sus necesidades.
1. En la esquina superior derecha, elija el icono **Configuración** ![Configuración](media/ui-experience/settings_icon_small.png "Icono Configuración para el área de trabajo") y, a continuación, elija **Mi configuración**.
2. En la ventana **Mi configuración**, en el campo **Área de trabajo**, seleccione el área de trabajo que quiere establecer como estándar. Por ejemplo, seleccione **Contable**.
3. Elija el botón **Aceptar**.

## <a name="company"></a>Compañía
Una empresa funciona como un contenedor de datos en [!INCLUDE[d365fin](includes/d365fin_md.md)]. Puede haber múltiples empresas en una base de datos, pero solo se puede seleccionar una a la vez.

La empresa predeterminada se llama CRONUS y solo contiene datos de demostración.

> [!TIP]  
>   Si desea que se muestre un nombre distinto para la empresa en la aplicación (por ejemplo, como en el área de trabajo), establezca el campo **Nombre** en la página **Información empresa** o el campo **Nombre para mostrar** en la página **Empresas**.  

## <a name="work-date"></a>Fecha de trabajo
La fecha predeterminada de trabajo será normalmente la fecha actual. Es posible que tenga que cambiar temporalmente la fecha de trabajo para realizar tareas como la finalización de las transacciones de una fecha que no sea la fecha actual.

> [!TIP]  
>   Escriba **w** para introducir rápidamente la fecha de trabajo en un campo de fecha. Escriba **t** para introducir rápidamente la fecha actual en el campo de fecha.

> [!IMPORTANT]  
>   La fecha de trabajo se cambia solo hasta que cierre la empresa o hasta que la fecha cambie. Si abre una empresa diferente o la misma al día siguiente y debe utilizar una fecha de trabajo diferente, tendrá que volver a definirla.

## <a name="region"></a>Región
El valor **Región** determina cómo se muestran o se forman las fechas, los tiempos, los números, y divisas.   

## <a name="changing-when-i-receive-notifications"></a>Cambio al recibir notificaciones
Seleccione este vínculo para ver o cambiar las notificaciones que recibe sobre determinados eventos o cambios de estado, cuando va a facturar a un cliente que tiene un saldo vencido o cuando el inventario disponible es inferior a la cantidad que va a vender, por ejemplo. Para obtener más información, consulte [Notificaciones inteligentes](ui-smart-notifications.md).

## <a name="see-also"></a>Consulte también
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Personalizar la experiencia de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md)  

