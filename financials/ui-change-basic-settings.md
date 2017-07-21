---
title: "Ver y editar la configuración básica en Financials | Documentos de Microsoft"
description: "Obtenga información sobre cómo cambiar algunos de los valores básicos en Financials, por ejemplo, el área de trabajo, la empresa o la fecha de trabajo."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: change Role Center, notification, change company, change work date
ms.date: 03/29/2017
ms.author: solsen
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: ed0a6848f07999246566ad740e02abfc561ae130
ms.contentlocale: es-es
ms.lasthandoff: 07/07/2017


---
# <a name="changing-basic-settings"></a>Cambiar la configuración básica
En la ventana **Mi configuración**, puede ver y cambiar la configuración básica de [!INCLUDE[d365fin](includes/d365fin_md.md)].  

## <a name="role-center"></a>Área de trabajo
El área de trabajo representa la página Inicio, una página de inicio que está designada para las necesidades del trabajo. En la página Inicio, tiene una vista general del negocio. A la izquierda puede ver una barra de navegación que le da un acceso sencillo a los clientes, proveedores, productos, etc.

En el centro se encuentra el mosaico Actividades. Actividades muestra los datos actuales y se puede hacer clic o pinchar sobre ellas para conseguir un acceso fácil al documento seleccionado. Los Indicadores de rendimiento clave pueden configurarse para mostrar un gráfico seleccionado para una representación visual de, por ejemplo, el flujo de efectivo o ingresos y gastos.

También puede crear una lista de Clientes favoritos en la página Inicio para las cuentas con las que hace negocios a menudo o a las que necesita prestar especial atención. Use las flechas para contraer parte de la página y haga más espacio para mostrar datos específicos. En la parte superior de la página Inicio encontrará todas las acciones que se pueden realizar con el contenido actual. Todo esto también se puede contraer y solo necesita hacer clic o pinchar en el área contraída para volverlo a ver.

El Área de trabajo predeterminada es **Admin. empresarial**, pero puede seleccionar otra Área de trabajo que se adapte mejor a sus necesidades. Para obtener más información, vea [Procedimiento: Cambiar el Área de trabajo](change-role.md)

## <a name="company"></a>Compañía
Una empresa funciona como un contenedor de datos en [!INCLUDE[d365fin](includes/d365fin_md.md)]. Puede haber múltiples empresas en una base de datos, pero solo se puede seleccionar una a la vez.

La empresa predeterminada se llama CRONUS y solo contiene datos de demostración.

> [!TIP]  
>   Si desea que se muestre un nombre distinto para la empresa en la aplicación (por ejemplo, como en la página principal), establezca el campo **Nombre** en la página **Información empresa** o el campo **Nombre para mostrar** en la página **Empresas**.  

## <a name="work-date"></a>Fecha de trabajo
La fecha predeterminada de trabajo será normalmente la fecha actual. Es posible que tenga que cambiar temporalmente la fecha de trabajo para realizar tareas como la finalización de las transacciones de una fecha que no sea la fecha actual.

> [!TIP]  
>   Escriba **w** para introducir rápidamente la fecha de trabajo en un campo de fecha. Escriba **t** para introducir rápidamente la fecha actual en el campo de fecha.

> [!IMPORTANT]  
>   La fecha de trabajo se cambia solo hasta que cierre la empresa o hasta que la fecha cambie. Si abre una empresa diferente o la misma al día siguiente y debe utilizar una fecha de trabajo diferente, tendrá que volver a definirla.

## <a name="confirmation-dialogs"></a>Cuadros de diálogo de confirmación
Use las opciones de esta sección si desea especificar comprobaciones adicionales para los documentos de registro. Estas opciones se comprueban como estándar, pero puede desmarcar las casillas para evitar advertencias o mensajes específicos.

## <a name="see-also"></a>Consulte también
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Cambiar el área de trabajo](change-role.md)  
[Personalizar la experiencia de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md)  

